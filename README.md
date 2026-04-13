<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
<meta name="apple-mobile-web-app-capable" content="yes">
<title>صيرفة المستقبل Pro</title>
<link href="https://fonts.googleapis.com/css2?family=Tajawal:wght@300;400;500;700&display=swap" rel="stylesheet">
<script src="https://cdnjs.cloudflare.com/ajax/libs/crypto-js/4.1.1/crypto-js.min.js"></script>
<style>
/* استخدمنا نفس الستايل الفخم مع تحسينات بسيطة للوضوح */
:root {
  --gold:#C9A84C; --gold-light:#E8C97A; --gold-dark:#9A7A30;
  --bg:#0A0C10; --bg2:#111318; --bg3:#181C24; --card:#1A1F2B;
  --border:rgba(201,168,76,0.2); --text:#F0EAD6; --muted:#8A8E9A;
  --green:#2ECC71; --red:#E74C3C; --blue:#3498DB; --r:14px;
}
*{box-sizing:border-box;margin:0;padding:0;-webkit-tap-highlight-color:transparent}
body{font-family:'Tajawal',sans-serif;background:var(--bg);color:var(--text);min-height:100vh;direction:rtl}

/* تصاميم العناصر */
.screen{display:none; padding-bottom:40px}
.screen.active{display:block}
.header{background:var(--bg2);border-bottom:1px solid var(--border);padding:16px 20px;display:flex;align-items:center;justify-content:space-between;position:sticky;top:0;z-index:100}
.card{background:var(--card);border:1px solid var(--border);border-radius:var(--r);padding:20px;margin:10px auto;max-width:500px}
input, select{width:100%;background:var(--bg3);border:1px solid var(--border);border-radius:10px;color:var(--text);padding:12px;margin-bottom:12px;font-family:inherit}
.btn{width:100%;padding:14px;background:linear-gradient(135deg,var(--gold-dark),var(--gold));border:none;border-radius:10px;color:#000;font-weight:700;cursor:pointer}
.tabs{display:flex;background:var(--bg2);overflow-x:auto;border-bottom:1px solid var(--border)}
.tab{padding:14px;flex:1;color:var(--muted);background:none;border:none;cursor:pointer;white-space:nowrap}
.tab.active{color:var(--gold);border-bottom:2px solid var(--gold)}

/* تنبيهات الحالة */
.badge{padding:4px 8px;border-radius:6px;font-size:12px;font-weight:bold}
.badge-red{background:rgba(231,76,60,0.2);color:var(--red)}
.badge-green{background:rgba(46,204,113,0.2);color:var(--green)}

/* قائمة الزبائن والحركات */
.list-item{background:var(--card);padding:15px;border-radius:12px;margin-bottom:10px;border:1px solid var(--border)}
.flex-between{display:flex;justify-content:space-between;align-items:center}
</style>
</head>
<body>

<div id="splash" style="position:fixed;inset:0;background:var(--bg);display:flex;flex-direction:column;align-items:center;justify-content:center;z-index:9999;">
  <h1 style="color:var(--gold)">🏦 صيرفة المستقبل</h1>
  <p style="color:var(--muted)">جاري تحميل النظام المحاسبي...</p>
</div>

<div id="screen-login" class="screen">
  <div style="padding:50px 20px; text-align:center">
    <h2 style="color:var(--gold);margin-bottom:30px">تسجيل الدخول</h2>
    <div class="card">
        <div style="display:flex;gap:10px;margin-bottom:20px">
            <button class="btn" id="btn-admin-tab" onclick="setRole('admin')">👑 مدير</button>
            <button class="btn" id="btn-cust-tab" style="background:var(--bg3);color:var(--text)" onclick="setRole('customer')">👤 زبون</button>
        </div>
        <div id="admin-fields">
            <input type="password" id="login-pass" placeholder="كلمة سر المدير">
        </div>
        <div id="customer-fields" style="display:none">
            <input type="tel" id="login-phone" placeholder="رقم الهاتف">
            <input type="password" id="login-cust-pass" placeholder="كلمة السر">
        </div>
        <button class="btn" onclick="handleLogin()">دخول للنظام</button>
    </div>
  </div>
</div>

<div id="screen-admin" class="screen">
  <div class="header">
    <span style="color:var(--gold);font-weight:bold">لوحة الإدارة</span>
    <button onclick="logout()" style="background:none;border:none;color:var(--red);cursor:pointer">🚪 خروج</button>
  </div>
  <div class="tabs">
    <button class="tab active" onclick="showTab('tab-customers')">الزبائن</button>
    <button class="tab" onclick="showTab('tab-daily')">اليومية</button>
    <button class="tab" onclick="showTab('tab-rates')">الأسعار</button>
  </div>

  <div id="tab-customers" class="tab-content" style="padding:15px">
    <button class="btn" style="margin-bottom:15px" onclick="openAddCustomer()">➕ إضافة زبون جديد</button>
    <input type="text" id="search-input" placeholder="🔍 ابحث عن اسم أو رقم..." oninput="renderCustomers()">
    <div id="customers-list"></div>
  </div>

  <div id="tab-daily" class="tab-content" style="padding:15px; display:none">
    <div class="card">
        <h3>💰 إجمالي الميزانية</h3>
        <div id="total-balance-summary" style="margin-top:10px; font-size:18px"></div>
    </div>
    <div id="daily-tx-list"></div>
  </div>
</div>

<div id="screen-customer" class="screen">
    <div class="header">
        <span id="welcome-name">أهلاً بك</span>
        <button onclick="logout()" style="background:none;border:none;color:var(--red);cursor:pointer">🚪 خروج</button>
    </div>
    <div style="padding:15px">
        <div class="card" style="border-right:5px solid var(--gold)">
            <h3>أرصدتي الحالية</h3>
            <div id="my-balances" style="margin-top:10px"></div>
        </div>
        <h4 style="margin:20px 0 10px">سجل الحركات</h4>
        <div id="my-tx-list"></div>
    </div>
</div>

<div id="modal-tx" style="display:none; position:fixed; inset:0; background:rgba(0,0,0,0.9); z-index:1000; padding:20px">
    <div class="card" style="margin-top:50px">
        <h3 id="tx-modal-title">إضافة حركة</h3>
        <select id="tx-type">
            <option value="deposit">📥 إيداع (الزبون سلّم مبلغ)</option>
            <option value="withdraw">📤 سحب (الزبون استلم مبلغ)</option>
        </select>
        <input type="number" id="tx-amount" placeholder="المبلغ">
        <select id="tx-currency">
            <option value="IQD">دينار عراقي</option>
            <option value="USD">دولار أمريكي</option>
        </select>
        <input type="text" id="tx-note" placeholder="ملاحظات...">
        <div style="display:flex;gap:10px">
            <button class="btn" onclick="submitTransaction()">تأكيد</button>
            <button class="btn" style="background:#555" onclick="closeModal()">إلغاء</button>
        </div>
    </div>
</div>

<script>
// --- الإعدادات والبيانات ---
const STORAGE_KEY = "FUTURE_EXCHANGE_DATA_V5";
let data = JSON.parse(localStorage.getItem(STORAGE_KEY)) || {
    customers: [],
    transactions: [],
    rates: { USD: 1500 },
    adminPass: "123456",
    adminDeviceId: null
};

let currentRole = 'admin';
let currentCustomer = null;
let activeTargetCustomer = null;

// --- نظام الأمان وبصمة الجهاز ---
function getDeviceId() {
    let id = localStorage.getItem('exchange_device_fingerprint');
    if(!id) {
        id = 'DEV-' + Math.random().toString(36).substr(2, 9).toUpperCase();
        localStorage.setItem('exchange_device_fingerprint', id);
    }
    return id;
}

// --- إدارة البيانات ---
function saveData() {
    localStorage.setItem(STORAGE_KEY, JSON.stringify(data));
}

// --- المحرك المحاسبي ---
function getCustomerBalance(phone) {
    let balances = { IQD: 0, USD: 0 };
    data.transactions.filter(t => t.customerPhone === phone).forEach(t => {
        if(t.type === 'deposit') balances[t.currency] += parseFloat(t.amount);
        else balances[t.currency] -= parseFloat(t.amount);
    });
    return balances;
}

// --- الواجهة ---
function setRole(role) {
    currentRole = role;
    document.getElementById('admin-fields').style.display = role === 'admin' ? 'block' : 'none';
    document.getElementById('customer-fields').style.display = role === 'customer' ? 'block' : 'none';
    document.getElementById('btn-admin-tab').style.background = role === 'admin' ? 'var(--gold)' : 'var(--bg3)';
    document.getElementById('btn-cust-tab').style.background = role === 'customer' ? 'var(--gold)' : 'var(--bg3)';
}

function handleLogin() {
    if(currentRole === 'admin') {
        const pass = document.getElementById('login-pass').value;
        const myId = getDeviceId();
        
        if(pass !== data.adminPass) return alert("كلمة السر خطأ");
        
        if(!data.adminDeviceId) {
            data.adminDeviceId = myId;
            saveData();
            alert("تم ربط الحساب بهذا الجهاز بنجاح");
        } else if(data.adminDeviceId !== myId) {
            return alert("عذراً، هذا الحساب مرتبط بجهاز آخر فقط!");
        }
        
        showScreen('screen-admin');
        renderCustomers();
    } else {
        const phone = document.getElementById('login-phone').value;
        const pass = document.getElementById('login-cust-pass').value;
        const user = data.customers.find(c => c.phone === phone && c.pass === pass);
        
        if(!user) return alert("البيانات غير صحيحة");
        currentCustomer = user;
        showScreen('screen-customer');
        renderCustomerPortal();
    }
}

function renderCustomers() {
    const list = document.getElementById('customers-list');
    const search = document.getElementById('search-input').value.toLowerCase();
    list.innerHTML = "";
    
    data.customers.filter(c => c.name.toLowerCase().includes(search) || c.phone.includes(search)).forEach(c => {
        const bal = getCustomerBalance(c.phone);
        const div = document.createElement('div');
        div.className = "list-item";
        div.innerHTML = `
            <div class="flex-between">
                <div>
                    <strong>${c.name}</strong><br>
                    <small style="color:var(--muted)">${c.phone}</small>
                </div>
                <div style="text-align:left">
                    <span class="${bal.IQD < 0 ? 'badge-red' : 'badge-green'}">${bal.IQD.toLocaleString()} IQD</span><br>
                    <span class="${bal.USD < 0 ? 'badge-red' : 'badge-green'}">${bal.USD.toLocaleString()} $</span>
                </div>
            </div>
            <button class="btn" style="margin-top:10px; padding:8px; font-size:12px" onclick="openTxModal('${c.phone}')">إجراء حركة مالية</button>
        `;
        list.appendChild(div);
    });
}

function openTxModal(phone) {
    activeTargetCustomer = phone;
    document.getElementById('modal-tx').style.display = 'block';
}

function submitTransaction() {
    const amount = document.getElementById('tx-amount').value;
    if(!amount || amount <= 0) return alert("أدخل مبلغ صحيح");
    
    data.transactions.push({
        id: Date.now(),
        customerPhone: activeTargetCustomer,
        type: document.getElementById('tx-type').value,
        amount: parseFloat(amount),
        currency: document.getElementById('tx-currency').value,
        note: document.getElementById('tx-note').value,
        date: new Date().toLocaleString()
    });
    
    saveData();
    closeModal();
    renderCustomers();
    renderDaily();
    alert("تمت العملية بنجاح");
}

function renderCustomerPortal() {
    document.getElementById('welcome-name').innerText = `أهلاً، ${currentCustomer.name}`;
    const bal = getCustomerBalance(currentCustomer.phone);
    document.getElementById('my-balances').innerHTML = `
        <div class="flex-between" style="font-size:20px; margin-bottom:10px">
            <span>دينار:</span> <span style="color:${bal.IQD < 0 ? 'var(--red)' : 'var(--green)'}">${bal.IQD.toLocaleString()}</span>
        </div>
        <div class="flex-between" style="font-size:20px">
            <span>دولار:</span> <span style="color:${bal.USD < 0 ? 'var(--red)' : 'var(--green)'}">${bal.USD.toLocaleString()} $</span>
        </div>
    `;
    
    const list = document.getElementById('my-tx-list');
    list.innerHTML = "";
    data.transactions.filter(t => t.customerPhone === currentCustomer.phone).reverse().forEach(t => {
        const item = document.createElement('div');
        item.className = "list-item";
        item.innerHTML = `
            <div class="flex-between">
                <span>${t.type === 'deposit' ? '📥 إيداع' : '📤 سحب'}</span>
                <span style="color:${t.type === 'deposit' ? 'var(--green)' : 'var(--red)'}">
                    ${t.amount.toLocaleString()} ${t.currency}
                </span>
            </div>
            <div style="font-size:11px; color:var(--muted); margin-top:5px">${t.date} - ${t.note}</div>
        `;
        list.appendChild(item);
    });
}

// --- وظائف عامة ---
function showScreen(id) {
    document.querySelectorAll('.screen').forEach(s => s.classList.remove('active'));
    document.getElementById(id).classList.add('active');
}

function showTab(id) {
    document.querySelectorAll('.tab-content').forEach(t => t.style.display = 'none');
    document.querySelectorAll('.tab').forEach(t => t.classList.remove('active'));
    document.getElementById(id).style.display = 'block';
    event.currentTarget.classList.add('active');
    if(id === 'tab-daily') renderDaily();
}

function openAddCustomer() {
    const name = prompt("اسم الزبون:");
    const phone = prompt("رقم الهاتف:");
    const pass = prompt("تعيين كلمة سر للزبون:");
    if(name && phone && pass) {
        data.customers.push({name, phone, pass});
        saveData();
        renderCustomers();
    }
}

function renderDaily() {
    let totalIQD = 0, totalUSD = 0;
    data.customers.forEach(c => {
        const b = getCustomerBalance(c.phone);
        totalIQD += b.IQD;
        totalUSD += b.USD;
    });
    document.getElementById('total-balance-summary').innerHTML = `
        <p>إجمالي الديون/الأرصدة (IQD): <span style="color:var(--gold)">${totalIQD.toLocaleString()}</span></p>
        <p>إجمالي الديون/الأرصدة (USD): <span style="color:var(--gold)">${totalUSD.toLocaleString()} $</span></p>
    `;
}

function closeModal() { document.getElementById('modal-tx').style.display = 'none'; }
function logout() { location.reload(); }

// تشغيل السبلش سكرين
window.onload = () => {
    setTimeout(() => {
        document.getElementById('splash').style.display = 'none';
        showScreen('screen-login');
    }, 1500);
};
</script>
</body>
</html>
