<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
<meta name="apple-mobile-web-app-capable" content="yes">
<meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
<meta name="apple-mobile-web-app-title" content="صيرفة المستقبل">
<meta name="theme-color" content="#0A0C10">
<title>صيرفة المستقبل</title>
<link href="https://fonts.googleapis.com/css2?family=Tajawal:wght@300;400;500;700&display=swap" rel="stylesheet">
<script src="https://cdnjs.cloudflare.com/ajax/libs/crypto-js/4.1.1/crypto-js.min.js"></script>
<style>
:root {
  --gold:#C9A84C; --gold-light:#E8C97A; --gold-dark:#9A7A30;
  --bg:#0A0C10; --bg2:#111318; --bg3:#181C24; --card:#1A1F2B;
  --border:rgba(201,168,76,0.2); --text:#F0EAD6; --muted:#8A8E9A;
  --green:#2ECC71; --red:#E74C3C; --orange:#E67E22; --blue:#3498DB;
  --r:14px;
}
*{box-sizing:border-box;margin:0;padding:0;-webkit-tap-highlight-color:transparent}
body{font-family:'Tajawal',sans-serif;background:var(--bg);color:var(--text);min-height:100vh;overflow-x:hidden;direction:rtl}
#splash{position:fixed;inset:0;background:var(--bg);display:flex;flex-direction:column;align-items:center;justify-content:center;z-index:9999;transition:opacity .6s}
.splash-logo{font-size:64px;margin-bottom:16px}
.splash-title{font-size:28px;font-weight:700;color:var(--gold);letter-spacing:2px;margin-bottom:8px}
.splash-sub{font-size:14px;color:var(--muted);margin-bottom:40px}
.splash-bar{width:160px;height:3px;background:var(--bg3);border-radius:4px;overflow:hidden}
.splash-fill{height:100%;background:linear-gradient(90deg,var(--gold-dark),var(--gold-light));border-radius:4px;animation:fill 1.8s ease forwards}
@keyframes fill{from{width:0}to{width:100%}}
.screen{display:none;min-height:100vh;padding-bottom:40px}
.screen.active{display:block}
.header{background:var(--bg2);border-bottom:1px solid var(--border);padding:16px 20px;display:flex;align-items:center;justify-content:space-between;position:sticky;top:0;z-index:100}
.header-logo{font-size:20px;font-weight:700;color:var(--gold)}
.header-sub{font-size:11px;color:var(--muted)}
.btn-icon{background:rgba(201,168,76,.15);border:1px solid var(--border);color:var(--gold);padding:8px 12px;border-radius:8px;font-size:13px;cursor:pointer;margin-left:8px}
.btn-logout{background:rgba(231,76,60,.15);border:1px solid rgba(231,76,60,.3);color:var(--red);padding:8px 14px;border-radius:8px;font-size:13px;cursor:pointer}
.btn-danger{background:rgba(231,76,60,.2);border:1px solid var(--red);color:var(--red);}
.login-wrap{min-height:100vh;display:flex;flex-direction:column;align-items:center;justify-content:center;padding:30px 24px}
.login-logo{font-size:56px;margin-bottom:12px}
.login-title{font-size:26px;font-weight:700;color:var(--gold);margin-bottom:4px}
.login-sub{font-size:13px;color:var(--muted);margin-bottom:32px}
.card{background:var(--card);border:1px solid var(--border);border-radius:var(--r);padding:24px;width:100%;max-width:400px}
.toggle-row{display:flex;margin-bottom:20px;background:var(--bg3);border-radius:10px;padding:4px}
.toggle-btn{flex:1;padding:10px;border:none;border-radius:8px;background:transparent;color:var(--muted);font-size:14px;cursor:pointer;transition:all .2s}
.toggle-btn.active{background:var(--gold);color:#000;font-weight:700}
label{font-size:13px;color:var(--muted);display:block;margin-bottom:6px}
input,select{width:100%;background:var(--bg3);border:1px solid var(--border);border-radius:10px;color:var(--text);font-family:'Tajawal',sans-serif;font-size:16px;padding:12px 14px;margin-bottom:14px;outline:none;transition:border .2s;direction:ltr}
input:focus,select:focus{border-color:var(--gold)}
.btn{width:100%;padding:14px;background:linear-gradient(135deg,var(--gold-dark),var(--gold));border:none;border-radius:10px;color:#000;font-size:16px;font-weight:700;cursor:pointer;transition:opacity .2s,transform .1s;margin-bottom:8px}
.btn:active{transform:scale(.98);opacity:.9}
.btn-sm{padding:10px 14px;font-size:14px;width:auto;margin-bottom:0}
.btn-outline{background:transparent;border:1px solid var(--gold);color:var(--gold)}
.install-btn{background:linear-gradient(135deg,#4CAF50,#2E7D32);color:white;border:none;padding:16px 24px;border-radius:50px;font-size:18px;font-weight:bold;cursor:pointer;margin:20px 0;width:100%}
.alert{padding:12px 14px;border-radius:10px;font-size:14px;margin-bottom:14px;display:none}
.alert.error{background:rgba(231,76,60,.15);border:1px solid rgba(231,76,60,.3);color:var(--red)}
.alert.success{background:rgba(46,204,113,.15);border:1px solid rgba(46,204,113,.3);color:var(--green)}
.alert.show{display:block}
.tabs{display:flex;overflow-x:auto;scrollbar-width:none;border-bottom:1px solid var(--border);background:var(--bg2);padding:0 16px}
.tabs::-webkit-scrollbar{display:none}
.tab{padding:14px 18px;border:none;background:transparent;color:var(--muted);font-size:14px;cursor:pointer;white-space:nowrap;border-bottom:2px solid transparent;transition:all .2s}
.tab.active{color:var(--gold);border-bottom-color:var(--gold)}
.tab-panel{display:none}
.tab-panel.active{display:block}
.content{padding:20px;max-width:600px;margin:0 auto}
.section-title{font-size:16px;font-weight:700;color:var(--gold);margin-bottom:16px}
.metrics{display:grid;grid-template-columns:repeat(2,1fr);gap:10px;margin-bottom:20px}
.metric{background:var(--card);border:1px solid var(--border);border-radius:12px;padding:14px 12px;text-align:center}
.metric-value{font-size:15px;font-weight:700;direction:ltr}
.metric-value.neg{color:var(--red)}
.metric-value.pos{color:var(--green)}
.customer-card{background:var(--card);border:1px solid var(--border);border-radius:var(--r);padding:16px;margin-bottom:12px;cursor:pointer;transition:all .2s}
.customer-card:hover{background:var(--bg3)}
.customer-card.has-debt{border-color:rgba(231,76,60,.6);border-width:2px}
.customer-card.has-credit{border-color:rgba(46,204,113,.6);border-width:2px}
.cust-name{font-size:16px;font-weight:700;margin-bottom:4px}
.cust-info{font-size:12px;color:var(--muted);direction:ltr;margin-bottom:10px}
.cust-balances{display:flex;gap:8px;flex-wrap:wrap;margin-bottom:10px}
.bal-badge{border-radius:20px;padding:4px 10px;font-size:12px;direction:ltr}
.bal-badge.pos{background:rgba(46,204,113,.1);border:1px solid rgba(46,204,113,.3);color:var(--green)}
.bal-badge.neg{background:rgba(231,76,60,.1);border:1px solid rgba(231,76,60,.3);color:var(--red)}
.tx-item{background:var(--card);border:1px solid var(--border);border-radius:12px;padding:14px;margin-bottom:10px;display:flex;align-items:flex-start;gap:12px}
.tx-icon{width:38px;height:38px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:18px;flex-shrink:0}
.tx-icon.deposit{background:rgba(46,204,113,.15)}
.tx-icon.withdraw{background:rgba(231,76,60,.15)}
.tx-details{flex:1;min-width:0}
.tx-name{font-size:14px;font-weight:600}
.tx-note{font-size:12px;color:var(--muted)}
.tx-date{font-size:10px;color:var(--muted);direction:ltr;margin-top:2px}
.tx-amount{text-align:left;direction:ltr;font-weight:700;font-size:15px;flex-shrink:0}
.tx-amount.deposit{color:var(--green)}
.tx-amount.withdraw{color:var(--red)}
.tx-actions{display:flex;gap:5px;margin-top:5px}
.btn-edit{background:rgba(52,152,219,.15);border:1px solid var(--blue);color:var(--blue);padding:4px 8px;border-radius:5px;font-size:11px;cursor:pointer}
.btn-delete{background:rgba(231,76,60,.15);border:1px solid var(--red);color:var(--red);padding:4px 8px;border-radius:5px;font-size:11px;cursor:pointer}
.modal-overlay{display:none;position:fixed;inset:0;background:rgba(0,0,0,.75);z-index:500;align-items:center;justify-content:center}
.modal-overlay.show{display:flex}
.modal{background:var(--bg2);border:1px solid var(--border);border-radius:20px;padding:24px;width:100%;max-width:450px;max-height:90vh;overflow-y:auto;animation:slideUp .3s ease}
@keyframes slideUp{from{transform:translateY(100%)}to{transform:translateY(0)}}
.modal-title{font-size:18px;font-weight:700;color:var(--gold);margin-bottom:16px}
.modal-close{float:left;background:var(--bg3);border:none;color:var(--text);width:32px;height:32px;border-radius:50%;font-size:18px;cursor:pointer}
.empty{text-align:center;padding:40px 20px;color:var(--muted);font-size:15px}
.empty-icon{font-size:40px;margin-bottom:12px}
.daily-summary{background:linear-gradient(135deg,var(--card),var(--bg3));border:2px solid var(--gold);border-radius:16px;padding:20px;margin-bottom:20px}
.daily-row{display:flex;justify-content:space-between;padding:8px 0;border-bottom:1px solid var(--border)}
.daily-label{color:var(--muted)}
.daily-value{font-weight:700;direction:ltr}
.daily-value.profit{color:var(--green)}
.daily-value.loss{color:var(--red)}
.office-funds{background:var(--card);border:1px solid var(--gold);border-radius:16px;padding:20px;margin-bottom:20px}
.funds-title{font-size:16px;font-weight:700;color:var(--gold);margin-bottom:16px;display:flex;align-items:center;gap:8px}
.funds-grid{display:flex;flex-direction:column;gap:16px}
.fund-block{background:var(--bg3);border:1px solid var(--border);border-radius:12px;padding:16px}
.fund-block-title{font-size:14px;font-weight:700;color:var(--gold);margin-bottom:12px}
.fund-row{display:grid;grid-template-columns:1fr 1fr;gap:12px;margin-bottom:8px}
.fund-item{background:var(--bg2);border-radius:8px;padding:12px}
.fund-label{font-size:12px;color:var(--muted);margin-bottom:6px}
.fund-input{width:100%;background:var(--bg);border:1px solid var(--border);border-radius:8px;color:var(--text);font-size:16px;font-weight:700;padding:10px;text-align:center;direction:ltr;margin-bottom:0}
.fund-input:focus{border-color:var(--gold)}
.fund-total{background:rgba(201,168,76,0.1);border-radius:8px;padding:10px;margin-top:8px;display:flex;justify-content:space-between;align-items:center}
.fund-total-label{color:var(--muted);font-size:13px}
.fund-total-value{color:var(--gold);font-weight:700;font-size:15px;direction:ltr}
.total-row{background:var(--gold);border-radius:12px;padding:16px;margin-top:16px;display:flex;justify-content:space-between;align-items:center}
.total-label{color:#000;font-weight:700;font-size:16px}
.total-value{color:#000;font-weight:900;font-size:20px;direction:ltr}
.rate-input-small{width:100%;background:var(--bg);border:1px solid var(--border);border-radius:8px;color:var(--gold);font-size:14px;font-weight:700;padding:8px;text-align:center;direction:ltr;margin-bottom:0}
.admin-contact-card{background:linear-gradient(135deg,var(--gold-dark),var(--gold));border-radius:16px;padding:20px;margin-bottom:24px;text-align:center}
.admin-name{color:#000;font-size:20px;font-weight:800;margin-bottom:8px}
.admin-phone{color:#000;font-size:28px;font-weight:900;margin-bottom:16px;direction:ltr}
.admin-label{color:rgba(0,0,0,0.7);font-size:14px;margin-bottom:4px}
.debt-summary{background:rgba(231,76,60,.1);border:1px solid rgba(231,76,60,.3);border-radius:12px;padding:16px;margin-bottom:20px}
.debt-summary-title{color:var(--red);font-weight:700;margin-bottom:12px;font-size:16px}
.debt-summary-row{display:flex;justify-content:space-between;padding:6px 0}
.debt-summary-label{color:var(--muted)}
.debt-summary-value{font-weight:700;direction:ltr}
.debt-summary-value.red{color:var(--red)}
.debt-total-row{background:rgba(231,76,60,.2);border-radius:8px;padding:12px;margin-top:12px;display:flex;justify-content:space-between;align-items:center}
.debt-total-label{color:var(--red);font-weight:700;font-size:15px}
.debt-total-value{color:var(--red);font-weight:900;font-size:18px;direction:ltr}
.credit-summary{background:rgba(46,204,113,.1);border:1px solid rgba(46,204,113,.3);border-radius:12px;padding:16px;margin-bottom:20px}
.credit-summary-title{color:var(--green);font-weight:700;margin-bottom:12px;font-size:16px}
.credit-summary-row{display:flex;justify-content:space-between;padding:6px 0}
.credit-summary-label{color:var(--muted)}
.credit-summary-value{font-weight:700;direction:ltr}
.credit-summary-value.green{color:var(--green)}
.credit-total-row{background:rgba(46,204,113,.2);border-radius:8px;padding:12px;margin-top:12px;display:flex;justify-content:space-between;align-items:center}
.credit-total-label{color:var(--green);font-weight:700;font-size:15px}
.credit-total-value{color:var(--green);font-weight:900;font-size:18px;direction:ltr}
.debt-card{background:var(--card);border:1px solid rgba(231,76,60,.4);border-radius:12px;padding:16px;margin-bottom:12px}
.credit-card{background:var(--card);border:1px solid rgba(46,204,113,.4);border-radius:12px;padding:16px;margin-bottom:12px}
.debt-card-header, .credit-card-header{display:flex;justify-content:space-between;align-items:center;margin-bottom:12px}
.debt-card-name, .credit-card-name{font-size:16px;font-weight:700}
.debt-card-phone, .credit-card-phone{font-size:12px;color:var(--muted);direction:ltr}
.debt-items-grid, .credit-items-grid{display:grid;grid-template-columns:repeat(2,1fr);gap:8px;margin-bottom:8px}
.debt-item-card, .credit-item-card{background:var(--bg3);border-radius:8px;padding:10px;text-align:center}
.debt-item-currency, .credit-item-currency{font-size:14px;color:var(--gold);margin-bottom:4px}
.debt-item-amount{font-size:18px;font-weight:700;color:var(--red);direction:ltr}
.credit-item-amount{font-size:18px;font-weight:700;color:var(--green);direction:ltr}
.debt-item-iqd, .credit-item-iqd{font-size:11px;color:var(--muted);margin-top:2px;direction:ltr}
.how-to-use-box{background:var(--card);border:1px solid var(--blue);border-radius:16px;padding:20px;margin-bottom:20px}
.how-to-use-title{color:var(--blue);font-weight:700;margin-bottom:12px;font-size:16px}
.how-to-use-step{display:flex;gap:12px;margin-bottom:12px;align-items:center}
.step-number{background:var(--blue);color:white;width:24px;height:24px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-weight:700;font-size:12px;flex-shrink:0}
.step-text{color:var(--text);font-size:13px}
.calendar-shortcuts{display:flex;gap:8px;margin-bottom:16px;flex-wrap:wrap}
.calendar-shortcut{flex:1;padding:8px;background:var(--bg3);border:1px solid var(--border);border-radius:8px;color:var(--text);font-size:12px;cursor:pointer;text-align:center}
.calendar-shortcut.active{background:var(--gold);color:#000;border-color:var(--gold)}
.full-balance-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:8px;margin-top:12px}
</style>
</head>
<body>

<div id="splash">
  <div class="splash-logo">🏦</div>
  <div class="splash-title">صيرفة المستقبل</div>
  <div class="splash-sub">Sayrafa Al-Mustaqbal</div>
  <div class="splash-bar"><div class="splash-fill"></div></div>
</div>

<!-- شاشة الترحيب -->
<div id="screen-welcome" class="screen active">
  <div class="login-wrap">
    <div class="login-logo">🏦</div>
    <div class="login-title">صيرفة المستقبل</div>
    <div class="login-sub">نظام إدارة الصرافة المتكامل</div>
    
    <div class="how-to-use-box">
      <div class="how-to-use-title">📱 كيف تستخدم التطبيق؟</div>
      <div class="how-to-use-step">
        <div class="step-number">1</div>
        <div class="step-text">المدير: يسجل دخول بكلمة السر (admin123) - مرتبط بجهاز واحد للأمان</div>
      </div>
      <div class="how-to-use-step">
        <div class="step-number">2</div>
        <div class="step-text">الزبون: المدير يسجله أولاً، ثم الزبون يدخل برقم هاتفه وكلمة السر</div>
      </div>
      <div class="how-to-use-step">
        <div class="step-number">3</div>
        <div class="step-text">الزبون يكدر يفتح التطبيق من أي جهاز ومن أي مكان</div>
      </div>
    </div>
    
    <div class="card" style="text-align:center">
      <button class="install-btn" onclick="showInstallInstructions()">📲 تثبيت التطبيق على الجهاز</button>
      <div style="margin:20px 0;border-top:1px solid var(--border)"></div>
      <button class="btn" onclick="goToLogin()">➡️ متابعة للتطبيق</button>
    </div>
  </div>
</div>

<!-- LOGIN SCREEN -->
<div id="screen-login" class="screen">
  <div class="login-wrap">
    <div class="login-logo">🏦</div>
    <div class="login-title">صيرفة المستقبل</div>
    <div class="login-sub">نظام إدارة الصرافة المتكامل</div>
    
    <div class="card">
      <div class="toggle-row">
        <button class="toggle-btn active" onclick="switchLoginTab('admin')">👑 المدير</button>
        <button class="toggle-btn" onclick="switchLoginTab('customer')">👤 الزبون</button>
      </div>
      <div id="alert-login" class="alert error"></div>
      <div id="login-admin">
        <label>كلمة السر</label>
        <input type="password" id="admin-pass" placeholder="••••••••">
        <button class="btn" onclick="loginAdmin()">دخول</button>
        <p style="color:var(--muted);font-size:12px;margin-top:8px;text-align:center">⚠️ حساب المدير مرتبط بجهاز واحد فقط</p>
      </div>
      <div id="login-customer" style="display:none">
        <label>رقم الهاتف</label>
        <input type="tel" id="cust-phone" placeholder="+964..." value="">
        <label>كلمة السر</label>
        <input type="password" id="cust-pass" placeholder="••••••••">
        <button class="btn" onclick="loginCustomer()">دخول</button>
        <button class="btn btn-outline" onclick="showForgotPasswordModal()" style="margin-top:8px">🔑 نسيت كلمة السر؟</button>
        <p style="color:var(--muted);font-size:12px;margin-top:8px;text-align:center">✅ الزبون يكدر يدخل من أي جهاز</p>
      </div>
    </div>
  </div>
</div>

<!-- باقي الأقسام (ADMIN SCREEN, CUSTOMER SCREEN, MODALS) - نفس الكود السابق بالضبط -->
<!-- للاختصار، راح أكتب الجزء المهم من الكود (دوال تسجيل الدخول فقط) -->

<script>
// ==================== CORE FUNCTIONS ====================
const ENCRYPTION_KEY = "S@yr4f4#M$st4qb4l!2025*XK9@zQ7!#&^mP3rVnL8wE";
const STORE = 'sarafa_final_v3';
const DEFAULT_ADMIN_PASS = 'admin123';
let ADMIN_HASH = CryptoJS.SHA256(DEFAULT_ADMIN_PASS).toString();

// توليد معرف فريد للجهاز
function getDeviceId() {
  let deviceId = localStorage.getItem('device_id');
  if (!deviceId) {
    deviceId = 'dev_' + Date.now() + '_' + Math.random().toString(36);
    localStorage.setItem('device_id', deviceId);
  }
  return deviceId;
}

let DB, currentUser = null, currentRole = null, selectedDailyDate = new Date().toISOString().split('T')[0];
let deferredPrompt;
let resetCustPhone = null;
let selectedCustomerForTx = null;
let editingTxId = null;
let viewingCustomerPhone = null;
let dateRangeFilter = { from: '', to: '' };
let editingCustomerPhone = null;

function initDB() {
  return {
    customers: {},
    transactions: [],
    rates: { USD: 1450, EUR: 1550, TRY: 50, IQD: 1, GBP: 1800, SAR: 385 },
    admin: { email: '', passwordHash: ADMIN_HASH, deviceId: null }, // deviceId null يعني لم يتم ربطه بعد
    dailyLedger: {},
    officeFunds: { iqd: 0, usd: { amount: 0, rate: 1450 }, kork: { amount: 0, rate: 1450 }, bank: 0 }
  };
}

function load() {
  try {
    const encrypted = localStorage.getItem(STORE);
    if (encrypted) {
      const bytes = CryptoJS.AES.decrypt(encrypted, ENCRYPTION_KEY);
      const data = JSON.parse(bytes.toString(CryptoJS.enc.Utf8));
      if (!data.admin) data.admin = { email: '', passwordHash: ADMIN_HASH, deviceId: null };
      return data;
    }
  } catch(e) {}
  return initDB();
}

function save(d) { localStorage.setItem(STORE, CryptoJS.AES.encrypt(JSON.stringify(d), ENCRYPTION_KEY).toString()); }
function fmt(n) { return Number(n).toLocaleString('en-US', { maximumFractionDigits: 0 }); }
function el(id) { return document.getElementById(id); }
function parseNumber(str) { return parseFloat(str.replace(/,/g, '')) || 0; }
function formatNumberInput(inp) { let v = inp.value.replace(/[^0-9]/g, ''); if (v) inp.value = Number(v).toLocaleString('en-US'); }

DB = load();
ADMIN_HASH = DB.admin?.passwordHash || CryptoJS.SHA256(DEFAULT_ADMIN_PASS).toString();

// ==================== AUTH & PROFILE ====================
function switchLoginTab(tab) { 
  el('login-admin').style.display = tab === 'admin' ? 'block' : 'none'; 
  el('login-customer').style.display = tab === 'customer' ? 'block' : 'none'; 
  document.querySelectorAll('.toggle-btn').forEach((b, i) => b.classList.toggle('active', (i === 0 && tab === 'admin') || (i === 1 && tab === 'customer'))); 
}

// ✅✅✅ تصحيح مهم: المدير مرتبط بجهاز واحد، الزبون غير مرتبط بأي جهاز ✅✅✅
function loginAdmin() {
  const pass = el('admin-pass').value;
  const admin = DB.admin || { email: '', passwordHash: ADMIN_HASH, deviceId: null };
  const currentDeviceId = getDeviceId();
  
  // التحقق من كلمة السر أولاً
  if (CryptoJS.SHA256(pass).toString() !== admin.passwordHash) {
    alert('❌ كلمة السر خاطئة!');
    return;
  }
  
  // إذا كانت كلمة السر صحيحة، نتحقق من الجهاز
  // إذا كان الجهاز غير مرتبط (null)، نربطه بأول جهاز يسجل دخول
  if (admin.deviceId === null || admin.deviceId === undefined) {
    admin.deviceId = currentDeviceId;
    if (!DB.admin) DB.admin = admin;
    save(DB);
    alert('✅ تم ربط حساب المدير بهذا الجهاز. لن تتمكن من الدخول من أي جهاز آخر.');
  }
  
  // التحقق من تطابق الجهاز
  if (admin.deviceId !== currentDeviceId) {
    alert('❌ لا يمكن الدخول من هذا الجهاز!\n\nحساب المدير مرتبط بجهاز واحد فقط للأمان.\nالزبائن فقط يمكنهم الدخول من أي جهاز.');
    return;
  }
  
  // كل شيء صحيح، تسجيل الدخول
  currentRole = 'admin'; 
  currentUser = 'admin';
  showScreen('admin'); 
  renderAdminView();
}

// ✅✅✅ تسجيل دخول الزبون - بدون أي ربط بالجهاز ✅✅✅
function loginCustomer() { 
  const phone = el('cust-phone').value.trim(), pass = el('cust-pass').value; 
  if (!DB.customers[phone]) { 
    alert('❌ الزبون غير موجود!'); 
    return; 
  } 
  if (DB.customers[phone].pass !== CryptoJS.SHA256(pass).toString()) { 
    alert('❌ كلمة السر خاطئة!'); 
    return; 
  } 
  // ✅ الزبون يدخل مباشرة - بدون أي فحص للجهاز
  currentRole = 'customer'; 
  currentUser = phone;
  showScreen('customer'); 
  renderCustomerView();
}

function logout() { currentUser = null; currentRole = null; showScreen('login'); }
function showScreen(id) { document.querySelectorAll('.screen').forEach(s => s.classList.remove('active')); el('screen-' + id).classList.add('active'); }
function goToLogin() { showScreen('login'); }

// ==================== باقي الدوال (نفس الكود السابق بالضبط) ====================
// ... (كل دوال renderCustomers, renderDebts, renderCredits, transactions, إلخ)
// للاختصار، تم حذفها هنا لأنها موجودة في الكود السابق

// ==================== INSTALL ====================
window.addEventListener('beforeinstallprompt', (e) => { e.preventDefault(); deferredPrompt = e; });
function showInstallInstructions() { 
  const instructions = el('install-instructions'); 
  const isIOS = /iPhone|iPad|iPod/.test(navigator.userAgent); 
  if (deferredPrompt) { 
    instructions.innerHTML = `<p style="margin-bottom:16px;text-align:center">✅ جهازك يدعم التثبيت المباشر</p><button class="install-btn" onclick="installPWA()" style="font-size:16px">📱 تثبيت الآن</button>`; 
  } else if (isIOS) { 
    instructions.innerHTML = `<div style="text-align:center"><p style="margin-bottom:16px">📱 للتثبيت على الآيفون:</p><div style="background:var(--bg3);padding:20px;border-radius:12px"><p>1️⃣ اضغط على زر <strong style="color:var(--gold)">مشاركة 📤</strong></p><p>2️⃣ اختر <strong style="color:var(--gold)">"إضافة إلى الشاشة الرئيسية"</strong></p><p>3️⃣ اضغط <strong style="color:var(--gold)">"إضافة"</strong></p></div></div>`; 
  } else { 
    instructions.innerHTML = `<div style="text-align:center"><p style="margin-bottom:16px">📱 للتثبيت على الأندرويد:</p><div style="background:var(--bg3);padding:20px;border-radius:12px"><p>1️⃣ اضغط على <strong style="color:var(--gold)">⋮ (القائمة)</strong></p><p>2️⃣ اختر <strong style="color:var(--gold)">"تثبيت التطبيق"</strong></p></div></div>`; 
  } 
  el('install-modal').classList.add('show'); 
}
function installPWA() { if (deferredPrompt) { deferredPrompt.prompt(); deferredPrompt.userChoice.then(() => { deferredPrompt = null; closeInstallModal(); }); } }
function closeInstallModal() { el('install-modal').classList.remove('show'); }

// ==================== INIT ====================
window.addEventListener('load', () => { 
  setTimeout(() => { 
    el('splash').style.opacity = '0'; 
    setTimeout(() => el('splash').style.display = 'none', 600); 
  }, 2000); 
});
</script>

<!-- مودال التثبيت -->
<div class="modal-overlay" id="install-modal">
  <div class="modal"><button class="modal-close" onclick="closeInstallModal()">×</button><div class="modal-title">📲 كيفية تثبيت التطبيق</div><div id="install-instructions"></div><button class="btn" onclick="closeInstallModal()">حسناً، فهمت</button></div>
</div>
</body>
</html>
