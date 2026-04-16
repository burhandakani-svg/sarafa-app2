<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
<meta name="apple-mobile-web-app-capable" content="yes">
<meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
<meta name="apple-mobile-web-app-title" content="صيرفة المستقبل">
<meta name="theme-color" content="#0A0C10">
<link rel="manifest" href="data:application/json;base64,eyJuYW1lIjoi2YXYs9ix2K/ZhCDYp9mE2YXYudmI2YQiLCJzaG9ydF9uYW1lIjoi2YXYs9ix2K/ZhCIsInRoZW1lX2NvbG9yIjoiI0NBQTg0QyIsImJhY2tncm91bmRfY29sb3IiOiIjMEEwQzEwIiwiZGlzcGxheSI6InN0YW5kYWxvbmUiLCJpY29ucyI6W3sic3JjIjoiZGF0YTppbWFnZS9zdmcreG1sO2Jhc2U2NCxQSE4yWnlCNGJXeHVjejBpYUhSMGNEb3ZMM2QzZHk1M015NXZjbWN2TWpBd01DOXpkbWNpSUhkcFpIUm9QU0l4T0RBaUlHaGxhV2RvZEQwaU1UZ3dJaUJ6ZEhKdmEyVTlJbU5uYVc1blpYSWlJR1pwYkd3OUltWmhiV2xzZVZCeWIzWnBaR1Z5SWo0S0lDQWdJRHhuSUdGNFBTSXhNQ0lnYzJ4a1BTSXhNQ0lnWm1sc2JDMWliMnhrTFhObVlXeHpaV1E5SW1KdmJHUWlQZ29nSUNBZ0lDQWdJRHh6WmlCbWFXeHNQU0owY25WbFBTSStDaUFnSUNBZ0lDQWdJQ0FnUEhOaUlHTjBlV3hsUFNKcGJtaHZjaUlnY0dGblpUMGlNVE13TlRZM0lpQnBaRDBpWkdWbVlYVnNkQ0lnWm1sc2JDMWliMnhsTFhOMVl6MGlkWFJ5Wlc0dWNtVmthWEp6SWlCNGJXeHVjejBpYUhSMGNEb3ZMM2QzZHk1M015NXZjbWN2TWpBd01DOXpkbWNpSUhOMVl6MGlZV1J2WW1VZ1kyOXNiM0psWkNJK1BDOXpZajRLSUNBZ0lDQWdJQ0E4YzJJZ1kzUjViR1U5SW1sdWFHOXlJaUJ3WVdkbFBTSXhOVEEwTURnaUlHbGtQU0prWldaaGRXeDBJaUJtYVd4c0xXSnZiR1V0YzNWalBTSjFkSEpsYmk1eVpXUjFjbk1pSUhodGJHNXpQU0pvZEhSd09pOHZkM2QzTGpjekxtOXlaeTh5TURBd0wzTjJaeUlnYzNWalBTSmhaRzlpWlNCamIyeHZjbVZrSWo0OEwzTmlQZ29nSUNBZ0lDQWdJRHh6WmlCaFkzUnZjbUYwYVc5dVBTSTBNVEF4TURBaUlHWnBiR3c5SW5SeWRXVWlQZ29nSUNBZ0lDQWdJQ0FnSUR4ellpQmpkSGxzWlQwaWFXNXNiMk5oZEdsdmJpSWdjR0ZuWlQwaU1UY3lPVFF3SWlCcFpEMGlZM0psWVhSbFpDSStQQzl6WWo0S0lDQWdJQ0FnSUNBOEwyYytDaUFnSUR3dlp6NEsiXX0=">
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
        <div class="step-text">المدير: يسجل دخول بكلمة السر ويدير كل شيء (مرتبط بجهاز واحد)</div>
      </div>
      <div class="how-to-use-step">
        <div class="step-number">2</div>
        <div class="step-text">الزبون: المدير يسجله أولاً، ثم الزبون يدخل برقم هاتفه وكلمة السر</div>
      </div>
      <div class="how-to-use-step">
        <div class="step-number">3</div>
        <div class="step-text">كل زبون يكدر يفتح التطبيق من جهازه الخاص ويسجل دخول</div>
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
      </div>
      <div id="login-customer" style="display:none">
        <label>رقم الهاتف</label>
        <input type="tel" id="cust-phone" placeholder="+964..." value="">
        <label>كلمة السر</label>
        <input type="password" id="cust-pass" placeholder="••••••••">
        <button class="btn" onclick="loginCustomer()">دخول</button>
        <button class="btn btn-outline" onclick="showForgotPasswordModal()" style="margin-top:8px">🔑 نسيت كلمة السر؟</button>
      </div>
    </div>
  </div>
</div>

<!-- ADMIN SCREEN -->
<div id="screen-admin" class="screen">
  <div class="header">
    <div>
      <div class="header-logo">🏦 صيرفة المستقبل</div>
      <div class="header-sub">لوحة المدير</div>
    </div>
    <div style="display:flex;gap:8px">
      <button class="btn-icon" onclick="showAdminProfileModal()">👤 الملف</button>
      <button class="btn-logout" onclick="logout()">🚪 خروج</button>
    </div>
  </div>
  
  <div class="tabs">
    <button class="tab active" onclick="showTab('daily')">📊 اليومية</button>
    <button class="tab" onclick="showTab('customers')">👥 زبائن</button>
    <button class="tab" onclick="showTab('txs')">💸 حركات</button>
    <button class="tab" onclick="showTab('debts')">🔴 ديون</button>
    <button class="tab" onclick="showTab('credits')">🟢 دائنون</button>
    <button class="tab" onclick="showTab('rates')">💱 أسعار</button>
    <button class="tab" onclick="showTab('new-customer')">➕ جديد</button>
  </div>

  <!-- PANEL: اليومية -->
  <div id="panel-daily" class="tab-panel active">
    <div class="content">
      <div style="margin-bottom:16px">
        <label style="color:var(--gold);margin-bottom:8px">📅 اختر التاريخ</label>
        <input type="date" id="daily-date-picker" onchange="changeDailyDateFromPicker()" style="margin-bottom:8px;direction:ltr">
        
        <div class="calendar-shortcuts">
          <button class="calendar-shortcut active" onclick="setDailyDateShortcut('today')">📅 اليوم</button>
          <button class="calendar-shortcut" onclick="setDailyDateShortcut('yesterday')">◀ أمس</button>
          <button class="calendar-shortcut" onclick="setDailyDateShortcut('monthStart')">📆 أول الشهر</button>
          <button class="calendar-shortcut" onclick="setDailyDateShortcut('monthEnd')">📆 آخر الشهر</button>
        </div>
      </div>
      
      <div class="daily-summary">
        <div class="daily-title" id="daily-date-title">📊 2026-04-13</div>
        <div class="daily-row"><span class="daily-label">🏦 الرصيد الافتتاحي</span><span class="daily-value" id="opening-balance">0 IQD</span></div>
        <div class="daily-row"><span class="daily-label">💰 الرصيد الحالي</span><span class="daily-value" id="current-balance">0 IQD</span></div>
        <div class="daily-row"><span class="daily-label">📈 صافي الربح (IQD)</span><span class="daily-value profit" id="profit-value">+0 IQD</span></div>
      </div>
      
      <div class="office-funds">
        <div class="funds-title">
          <span>💼 موجودات الصيرفة</span>
          <button onclick="saveOfficeFunds()">💾 حفظ</button>
        </div>
        
        <div class="funds-grid">
          <div class="fund-block"><div class="fund-block-title">💵 الدينار العراقي</div><div class="fund-item"><div class="fund-label">المبلغ (IQD)</div><input type="text" id="office-iqd" class="fund-input" placeholder="0" value="0" oninput="formatNumberInput(this);updateTotalOfficeFunds()" dir="ltr"></div><div class="fund-total"><span class="fund-total-label">القيمة:</span><span class="fund-total-value" id="office-iqd-value">0 IQD</span></div></div>
          <div class="fund-block"><div class="fund-block-title">💵 الدولار الأمريكي</div><div class="fund-row"><div class="fund-item"><div class="fund-label">الكمية (USD)</div><input type="text" id="office-usd-amount" class="fund-input" placeholder="0" value="0" oninput="formatNumberInput(this);updateTotalOfficeFunds()" dir="ltr"></div><div class="fund-item"><div class="fund-label">سعر الصرف</div><input type="text" id="office-usd-rate" class="rate-input-small" placeholder="1450" value="1450" oninput="formatNumberInput(this);updateTotalOfficeFunds()" dir="ltr"></div></div><div class="fund-total"><span class="fund-total-label">القيمة (IQD):</span><span class="fund-total-value" id="office-usd-value">0 IQD</span></div></div>
          <div class="fund-block"><div class="fund-block-title">💳 كارت كورك (دولار)</div><div class="fund-row"><div class="fund-item"><div class="fund-label">الكمية (USD)</div><input type="text" id="kork-amount" class="fund-input" placeholder="0" value="0" oninput="formatNumberInput(this);updateTotalOfficeFunds()" dir="ltr"></div><div class="fund-item"><div class="fund-label">سعر الصرف</div><input type="text" id="kork-rate" class="rate-input-small" placeholder="1450" value="1450" oninput="formatNumberInput(this);updateTotalOfficeFunds()" dir="ltr"></div></div><div class="fund-total"><span class="fund-total-label">القيمة (IQD):</span><span class="fund-total-value" id="kork-value">0 IQD</span></div></div>
          <div class="fund-block"><div class="fund-block-title">🏦 فلوس بالبنوك</div><div class="fund-item"><div class="fund-label">المبلغ (IQD)</div><input type="text" id="bank-funds" class="fund-input" placeholder="0" value="0" oninput="formatNumberInput(this);updateTotalOfficeFunds()" dir="ltr"></div><div class="fund-total"><span class="fund-total-label">القيمة:</span><span class="fund-total-value" id="bank-value">0 IQD</span></div></div>
        </div>
        
        <div class="total-row"><span class="total-label">📊 إجمالي الموجودات (IQD)</span><span class="total-value" id="total-office-funds">0 IQD</span></div>
      </div>
      
      <div class="section-title">📋 حركات اليوم</div>
      <div id="daily-transactions"></div>
    </div>
  </div>

  <!-- PANEL: الزبائن -->
  <div id="panel-customers" class="tab-panel">
    <div class="content">
      <div class="search-wrap" style="position:relative;margin-bottom:16px">
        <input type="text" id="search-cust" placeholder="بحث..." oninput="renderCustomers()" style="padding-right:40px">
        <span style="position:absolute;right:14px;top:50%;transform:translateY(-50%);color:var(--muted)">🔍</span>
      </div>
      <div id="customers-list"></div>
    </div>
  </div>

  <!-- PANEL: الحركات -->
  <div id="panel-txs" class="tab-panel">
    <div class="content"><div class="section-title">💸 جميع الحركات</div><div id="all-txs-list"></div></div>
  </div>

  <!-- PANEL: الديون -->
  <div id="panel-debts" class="tab-panel">
    <div class="content">
      <div class="section-title">🔴 الزبائن المدينون (اللي مطلوب منهم)</div>
      <div id="debts-summary-container"></div>
      <div id="debts-list"></div>
    </div>
  </div>

  <!-- PANEL: الدائنون (جديد) -->
  <div id="panel-credits" class="tab-panel">
    <div class="content">
      <div class="section-title">🟢 الزبائن الدائنون (اللي مطلوب لك)</div>
      <div id="credits-summary-container"></div>
      <div id="credits-list"></div>
    </div>
  </div>

  <!-- PANEL: الأسعار -->
  <div id="panel-rates" class="tab-panel">
    <div class="content">
      <div class="section-title">💱 أسعار الصرف (IQD)</div>
      <div id="rates-list"></div>
      <button class="btn" onclick="saveRates()">💾 حفظ الأسعار</button>
      <div id="alert-rates" class="alert success" style="margin-top:12px"></div>
    </div>
  </div>

  <!-- PANEL: زبون جديد -->
  <div id="panel-new-customer" class="tab-panel">
    <div class="content">
      <div class="section-title">➕ تسجيل زبون جديد</div>
      <div id="alert-new" class="alert error"></div>
      <label>الاسم</label><input type="text" id="new-fname">
      <label>اللقب</label><input type="text" id="new-lname">
      <label>رقم الهاتف</label><input type="tel" id="new-tel" placeholder="+964...">
      <label>رقم الهوية</label><input type="text" id="new-id">
      <label>كلمة السر</label><input type="password" id="new-pass" placeholder="••••••••">
      <button class="btn" onclick="addCustomer()">✅ تسجيل</button>
      <p style="color:var(--muted);font-size:12px;margin-top:12px;text-align:center">بعد التسجيل، الزبون يكدر يسجل دخول من جهازه برقم الهاتف وكلمة السر</p>
    </div>
  </div>
</div>

<!-- CUSTOMER SCREEN -->
<div id="screen-customer" class="screen">
  <div class="header">
    <div><div class="header-logo">🏦 صيرفة المستقبل</div><div class="header-sub" id="cust-welcome-label">مرحباً</div></div>
    <button class="btn-logout" onclick="logout()">🚪 خروج</button>
  </div>
  <div class="content">
    <div class="admin-contact-card">
      <div class="admin-label">👑 المدير / الصاحب</div><div class="admin-name">برهان دكاني</div><div class="admin-phone">0750 123 4567</div>
      <a href="https://wa.me/9647501234567" target="_blank" style="text-decoration:none"><button style="width:100%;padding:12px;background:#000;border:none;border-radius:10px;color:var(--gold);font-size:16px;font-weight:700;cursor:pointer;display:flex;align-items:center;justify-content:center;gap:10px"><svg width="20" height="20" viewBox="0 0 24 24" fill="#C9A84C"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413z"/></svg>واتساب المدير</button></a>
      <a href="tel:07501234567" style="text-decoration:none"><button style="width:100%;padding:10px;background:transparent;border:1px solid #000;border-radius:10px;color:#000;font-size:14px;font-weight:700;cursor:pointer;margin-top:8px">📞 اتصال مباشر</button></a>
    </div>
    <div class="section-title">💰 رصيدي</div><div class="metrics" id="cust-balances"></div>
    <div id="cust-debt-banner"></div>
    <div class="section-title" style="margin-top:20px">📋 حركاتي</div><div id="cust-txs"></div>
    <p style="color:var(--muted);text-align:center;margin-top:20px;font-size:13px">للاستفسار أو تغيير كلمة السر، تواصل مع المدير</p>
  </div>
</div>

<!-- CUSTOMER TRANSACTIONS MODAL (مع حساب كامل) -->
<div class="modal-overlay" id="modal-customer-txs">
  <div class="modal" style="max-width:550px">
    <button class="modal-close" onclick="closeCustomerTxsModal()">×</button>
    <div class="modal-title">📋 حساب الزبون الكامل</div>
    <div id="customer-txs-name" style="color:var(--gold);margin-bottom:16px;font-weight:700"></div>
    
    <!-- الرصيد الكامل بكل العملات -->
    <div style="background:var(--bg3);border-radius:12px;padding:16px;margin-bottom:16px">
      <div style="color:var(--gold);margin-bottom:12px;font-weight:700">💰 الأرصدة الحالية</div>
      <div id="full-balance-display" class="full-balance-grid"></div>
    </div>
    
    <label>📅 من تاريخ</label><input type="date" id="txs-from-date" style="margin-bottom:8px;direction:ltr">
    <label>📅 إلى تاريخ</label><input type="date" id="txs-to-date" style="margin-bottom:8px;direction:ltr">
    
    <div class="calendar-shortcuts">
      <button class="calendar-shortcut active" onclick="setDateRangeShortcut('today')">اليوم</button>
      <button class="calendar-shortcut" onclick="setDateRangeShortcut('thisMonth')">هذا الشهر</button>
      <button class="calendar-shortcut" onclick="setDateRangeShortcut('last3Months')">آخر 3 أشهر</button>
      <button class="calendar-shortcut" onclick="setDateRangeShortcut('all')">الكل</button>
    </div>
    
    <button class="btn" onclick="applyDateRangeFilter()" style="margin-bottom:16px">🔍 عرض الحركات</button>
    <div id="customer-txs-list" style="max-height:350px;overflow-y:auto"></div>
  </div>
</div>

<!-- EDIT CUSTOMER MODAL (تعديل بيانات الزبون) -->
<div class="modal-overlay" id="modal-edit-customer">
  <div class="modal">
    <button class="modal-close" onclick="closeEditCustomerModal()">×</button>
    <div class="modal-title">✏️ تعديل بيانات الزبون</div>
    <div id="alert-edit-cust" class="alert error"></div>
    <input type="hidden" id="edit-cust-original-phone">
    <label>الاسم</label><input type="text" id="edit-cust-fname" style="direction:rtl">
    <label>اللقب</label><input type="text" id="edit-cust-lname" style="direction:rtl">
    <label>رقم الهاتف</label><input type="tel" id="edit-cust-phone" placeholder="+964..." dir="ltr">
    <label>رقم الهوية</label><input type="text" id="edit-cust-id" dir="ltr">
    <button class="btn" onclick="saveEditedCustomer()">💾 حفظ التعديلات</button>
  </div>
</div>

<!-- TX MODAL -->
<div class="modal-overlay" id="modal-tx">
  <div class="modal">
    <button class="modal-close" onclick="closeTxModal()">×</button>
    <div class="modal-title">معاملة جديدة</div><div id="alert-tx" class="alert error"></div>
    <label>نوع المعاملة</label><select id="tx-type" onchange="updatePreview()"><option value="deposit">⬆️ إيداع (الزبون أعطاني)</option><option value="withdraw">⬇️ سحب (أنا أعطيت الزبون)</option></select>
    <label>المبلغ</label><input type="text" id="tx-amount" placeholder="0" oninput="formatNumberInput(this);updatePreview()" dir="ltr">
    <label>العملة</label><select id="tx-currency" onchange="updatePreview()"><option value="USD">USD</option><option value="EUR">EUR</option><option value="TRY">TRY</option><option value="IQD" selected>IQD</option><option value="GBP">GBP</option><option value="SAR">SAR</option></select>
    <label>ملاحظة</label><input type="text" id="tx-note" placeholder="اختياري" style="direction:rtl">
    <div id="tx-preview" style="background:var(--bg3);border-radius:10px;padding:14px;margin-bottom:14px;display:none"><div style="display:flex;justify-content:space-between"><span style="color:var(--muted)">بعد المعاملة:</span><span id="preview-value" style="font-weight:700;direction:ltr">0</span></div></div>
    <button class="btn" onclick="confirmTx()">✅ تأكيد المعاملة</button>
  </div>
</div>

<!-- EDIT TX MODAL -->
<div class="modal-overlay" id="modal-edit-tx">
  <div class="modal">
    <button class="modal-close" onclick="closeEditTxModal()">×</button>
    <div class="modal-title">✏️ تعديل الحركة</div><div id="alert-edit-tx" class="alert error"></div>
    <input type="hidden" id="edit-tx-id">
    <label>المبلغ</label><input type="text" id="edit-tx-amount" placeholder="0" oninput="formatNumberInput(this)" dir="ltr">
    <label>العملة</label><select id="edit-tx-currency"><option value="USD">USD</option><option value="EUR">EUR</option><option value="TRY">TRY</option><option value="IQD">IQD</option><option value="GBP">GBP</option><option value="SAR">SAR</option></select>
    <label>ملاحظة</label><input type="text" id="edit-tx-note" placeholder="اختياري" style="direction:rtl">
    <button class="btn" onclick="saveEditedTx()">💾 حفظ التعديلات</button>
  </div>
</div>

<!-- FORGOT PASSWORD MODAL -->
<div class="modal-overlay" id="modal-forgot-password">
  <div class="modal">
    <button class="modal-close" onclick="closeForgotPasswordModal()">×</button>
    <div class="modal-title">🔑 استرجاع كلمة السر</div><div id="alert-forgot" class="alert info"></div>
    <p style="margin-bottom:16px;color:var(--muted);text-align:center">أدخل رقم هاتفك وسيتم إرسال طلب للمدير</p>
    <label>رقم الهاتف</label><input type="tel" id="forgot-phone" placeholder="+964..." dir="ltr">
    <button class="btn" onclick="sendResetRequest()">📧 إرسال الطلب</button>
    <div class="divider" style="height:1px;background:var(--border);margin:16px 0"></div>
    <p style="color:var(--muted);font-size:13px;text-align:center">أو تواصل مباشرة مع المدير:</p>
    <div style="display:flex;gap:10px;margin-top:12px">
      <a href="https://wa.me/9647501234567" target="_blank" style="flex:1;text-decoration:none"><button style="width:100%;padding:12px;background:#25D366;border:none;border-radius:10px;color:white;font-weight:700;cursor:pointer">💬 واتساب</button></a>
      <a href="tel:07501234567" style="flex:1;text-decoration:none"><button style="width:100%;padding:12px;background:var(--blue);border:none;border-radius:10px;color:white;font-weight:700;cursor:pointer">📞 اتصال</button></a>
    </div>
  </div>
</div>

<!-- RESET CUSTOMER PASSWORD MODAL -->
<div class="modal-overlay" id="modal-reset-cust-password">
  <div class="modal">
    <button class="modal-close" onclick="closeResetCustPasswordModal()">×</button>
    <div class="modal-title">🔑 إعادة تعيين كلمة سر الزبون</div><div id="alert-reset-cust" class="alert success"></div>
    <p style="margin-bottom:16px;color:var(--muted)"><span>الزبون:</span> <span id="reset-cust-name" style="color:var(--text);font-weight:700"></span></p>
    <label>كلمة السر الجديدة</label><input type="password" id="new-cust-password" placeholder="••••••••">
    <label>تأكيد كلمة السر</label><input type="password" id="confirm-cust-password" placeholder="••••••••">
    <button class="btn" onclick="resetCustomerPassword()">✅ تعيين كلمة السر الجديدة</button>
  </div>
</div>

<!-- INSTALL MODAL -->
<div class="modal-overlay" id="install-modal">
  <div class="modal"><button class="modal-close" onclick="closeInstallModal()">×</button><div class="modal-title">📲 كيفية تثبيت التطبيق</div><div id="install-instructions"></div><button class="btn" onclick="closeInstallModal()">حسناً، فهمت</button></div>
</div>

<!-- ADMIN PROFILE MODAL -->
<div class="modal-overlay" id="modal-admin-profile">
  <div class="modal">
    <button class="modal-close" onclick="closeAdminProfileModal()">×</button>
    <div class="modal-title">👤 إعدادات الآدمين</div><div id="alert-profile" class="alert success"></div>
    <label>البريد الإلكتروني للاسترداد</label><input type="email" id="admin-email" placeholder="admin@example.com" dir="ltr">
    <label>كلمة السر الحالية</label><input type="password" id="current-password" placeholder="••••••••">
    <label>كلمة السر الجديدة</label><input type="password" id="new-password" placeholder="••••••••">
    <label>تأكيد كلمة السر الجديدة</label><input type="password" id="confirm-password" placeholder="••••••••">
    <button class="btn" onclick="updateAdminProfile()">💾 حفظ التغييرات</button>
    <div class="divider" style="height:1px;background:var(--border);margin:16px 0"></div>
    <p style="color:var(--muted);font-size:12px;text-align:center">⚠️ حساب المدير مرتبط بهذا الجهاز فقط. لا يمكن الدخول من جهاز آخر.</p>
  </div>
</div>

<script>
// ==================== CORE FUNCTIONS ====================
const ENCRYPTION_KEY = "S@yr4f4#M$st4qb4l!2025*XK9@zQ7!#&^mP3rVnL8wE";
const STORE = 'sarafa_final_v2';
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
    admin: { email: '', passwordHash: ADMIN_HASH, deviceId: getDeviceId() },
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
      if (!data.admin) data.admin = { email: '', passwordHash: ADMIN_HASH, deviceId: getDeviceId() };
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
if (el('daily-date-picker')) el('daily-date-picker').value = selectedDailyDate;

function loadOfficeFunds() {
  const funds = DB.officeFunds || { iqd: 0, usd: { amount: 0, rate: 1450 }, kork: { amount: 0, rate: 1450 }, bank: 0 };
  el('office-iqd').value = fmt(funds.iqd || 0);
  el('office-usd-amount').value = fmt(funds.usd?.amount || 0);
  el('office-usd-rate').value = fmt(funds.usd?.rate || 1450);
  el('kork-amount').value = fmt(funds.kork?.amount || 0);
  el('kork-rate').value = fmt(funds.kork?.rate || 1450);
  el('bank-funds').value = fmt(funds.bank || 0);
  updateTotalOfficeFunds();
}

function updateTotalOfficeFunds() {
  const iqd = parseNumber(el('office-iqd').value);
  const usdAmount = parseNumber(el('office-usd-amount').value);
  const usdRate = parseNumber(el('office-usd-rate').value);
  const korkAmount = parseNumber(el('kork-amount').value);
  const korkRate = parseNumber(el('kork-rate').value);
  const bank = parseNumber(el('bank-funds').value);
  el('office-iqd-value').textContent = fmt(iqd) + ' IQD';
  el('office-usd-value').textContent = fmt(usdAmount * usdRate) + ' IQD';
  el('kork-value').textContent = fmt(korkAmount * korkRate) + ' IQD';
  el('bank-value').textContent = fmt(bank) + ' IQD';
  el('total-office-funds').textContent = fmt(iqd + (usdAmount * usdRate) + (korkAmount * korkRate) + bank) + ' IQD';
}

function saveOfficeFunds() { DB.officeFunds = { iqd: parseNumber(el('office-iqd').value), usd: { amount: parseNumber(el('office-usd-amount').value), rate: parseNumber(el('office-usd-rate').value) }, kork: { amount: parseNumber(el('kork-amount').value), rate: parseNumber(el('kork-rate').value) }, bank: parseNumber(el('bank-funds').value) }; save(DB); alert('✅ تم الحفظ'); }

function updateDailyLedger() { if (!DB.dailyLedger[selectedDailyDate]) DB.dailyLedger[selectedDailyDate] = { openingBalance: calculateTotalBalance(), closingBalance: 0, profit: 0 }; }

function calculateTotalBalance() {
  let total = 0;
  Object.values(DB.customers).forEach(c => { Object.entries(c.balance).forEach(([cur, amt]) => { total += amt * (DB.rates[cur] || 1); }); });
  return total;
}

function renderDailySummary() {
  updateDailyLedger();
  const daily = DB.dailyLedger[selectedDailyDate] || { openingBalance: 0, closingBalance: 0, profit: 0 };
  const currentBalance = calculateTotalBalance();
  const profit = currentBalance - daily.openingBalance;
  daily.closingBalance = currentBalance; daily.profit = profit;
  save(DB);
  el('daily-date-title').textContent = '📊 ' + selectedDailyDate;
  if (el('daily-date-picker')) el('daily-date-picker').value = selectedDailyDate;
  el('opening-balance').textContent = fmt(daily.openingBalance) + ' IQD';
  el('current-balance').textContent = fmt(currentBalance) + ' IQD';
  const profitEl = el('profit-value');
  profitEl.textContent = (profit >= 0 ? '+' : '') + fmt(profit) + ' IQD';
  profitEl.className = 'daily-value ' + (profit >= 0 ? 'profit' : 'loss');
  renderDailyTransactions();
  loadOfficeFunds();
}

function renderDailyTransactions() {
  const todayTxs = DB.transactions.filter(tx => tx.date.startsWith(selectedDailyDate.split('-').reverse().join('/')));
  const container = el('daily-transactions');
  if (todayTxs.length === 0) { container.innerHTML = `<div class="empty"><div class="empty-icon">💸</div>لا توجد حركات في هذا التاريخ</div>`; return; }
  container.innerHTML = todayTxs.reverse().map(tx => renderTxItem(tx)).join('');
}

function renderTxItem(tx) {
  const typeLabel = tx.type === 'deposit' ? 'إيداع' : 'سحب';
  return `<div class="tx-item"><div class="tx-icon ${tx.type}">${tx.type === 'deposit' ? '⬆️' : '⬇️'}</div><div class="tx-details"><div class="tx-name">${tx.customerName} - ${typeLabel}</div><div class="tx-note">${tx.note || '—'}</div><div class="tx-date">${tx.date}</div>${currentRole === 'admin' ? `<div class="tx-actions"><button class="btn-edit" onclick="editTransaction('${tx.id}')">✏️</button><button class="btn-delete" onclick="deleteTransaction('${tx.id}')">🗑️</button></div>` : ''}</div><div class="tx-amount ${tx.type}">${tx.type === 'deposit' ? '+' : '-'}${fmt(tx.amount)} ${tx.currency}</div></div>`;
}

function changeDailyDate(offset) { const date = new Date(selectedDailyDate); date.setDate(date.getDate() + offset); selectedDailyDate = date.toISOString().split('T')[0]; renderDailySummary(); updateShortcutsActive(); }
function changeDailyDateFromPicker() { selectedDailyDate = el('daily-date-picker').value; renderDailySummary(); updateShortcutsActive(); }

function setDailyDateShortcut(type) {
  const today = new Date(); let targetDate = new Date();
  if (type === 'today') targetDate = today;
  else if (type === 'yesterday') { targetDate.setDate(today.getDate() - 1); }
  else if (type === 'monthStart') { targetDate = new Date(today.getFullYear(), today.getMonth(), 1); }
  else if (type === 'monthEnd') { targetDate = new Date(today.getFullYear(), today.getMonth() + 1, 0); }
  selectedDailyDate = targetDate.toISOString().split('T')[0];
  renderDailySummary(); updateShortcutsActive();
}

function updateShortcutsActive() {
  const today = new Date().toISOString().split('T')[0];
  const yesterday = new Date(Date.now() - 86400000).toISOString().split('T')[0];
  const monthStart = new Date(new Date().getFullYear(), new Date().getMonth(), 1).toISOString().split('T')[0];
  const monthEnd = new Date(new Date().getFullYear(), new Date().getMonth() + 1, 0).toISOString().split('T')[0];
  document.querySelectorAll('.calendar-shortcut').forEach(btn => btn.classList.remove('active'));
  if (selectedDailyDate === today) document.querySelector('[onclick*="today"]')?.classList.add('active');
  else if (selectedDailyDate === yesterday) document.querySelector('[onclick*="yesterday"]')?.classList.add('active');
  else if (selectedDailyDate === monthStart) document.querySelector('[onclick*="monthStart"]')?.classList.add('active');
  else if (selectedDailyDate === monthEnd) document.querySelector('[onclick*="monthEnd"]')?.classList.add('active');
}

function renderCustomers() {
  const q = (el('search-cust')?.value || '').toLowerCase();
  const custs = Object.values(DB.customers).filter(c => (c.fname + ' ' + c.lname + ' ' + c.phone).toLowerCase().includes(q));
  const list = el('customers-list');
  if (!custs.length) { list.innerHTML = `<div class="empty"><div class="empty-icon">👥</div>لا يوجد زبائن</div>`; return; }
  list.innerHTML = custs.map(c => {
    const hasDebt = Object.values(c.balance).some(v => v < 0);
    const hasCredit = Object.values(c.balance).some(v => v > 0);
    let cardClass = 'customer-card';
    if (hasDebt) cardClass += ' has-debt';
    if (hasCredit) cardClass += ' has-credit';
    return `<div class="${cardClass}" onclick="showCustomerTransactions('${c.phone}')"><div class="cust-name">👤 ${c.fname} ${c.lname} ${hasDebt ? '<span style="color:var(--red);font-size:12px">● مديون</span>' : ''} ${hasCredit ? '<span style="color:var(--green);font-size:12px">● دائن</span>' : ''}</div><div class="cust-info">${c.phone} | ID: ${c.id_no}</div><div class="cust-balances">${Object.entries(c.balance).map(([cur, amt]) => `<span class="bal-badge ${amt < 0 ? 'neg' : amt > 0 ? 'pos' : ''}">${amt < 0 ? '-' : ''}${fmt(Math.abs(amt))} ${cur}</span>`).join('')}</div><div style="display:flex;gap:8px;margin-top:10px;flex-wrap:wrap" onclick="event.stopPropagation()"><button class="btn btn-sm" onclick="openTxModal('${c.phone}')">💸 معاملة</button><button class="btn btn-sm btn-outline" onclick="showEditCustomerModal('${c.phone}')">✏️ تعديل</button><button class="btn btn-sm btn-outline" onclick="showResetCustPasswordModal('${c.phone}')">🔑 تغيير الرمز</button><button class="btn btn-sm btn-danger" onclick="deleteCustomer('${c.phone}')">🗑️ حذف</button></div></div>`;
  }).join('');
}

// تعديل بيانات الزبون
function showEditCustomerModal(phone) {
  editingCustomerPhone = phone;
  const c = DB.customers[phone];
  el('edit-cust-original-phone').value = phone;
  el('edit-cust-fname').value = c.fname;
  el('edit-cust-lname').value = c.lname;
  el('edit-cust-phone').value = c.phone;
  el('edit-cust-id').value = c.id_no;
  el('modal-edit-customer').classList.add('show');
}
function closeEditCustomerModal() { el('modal-edit-customer').classList.remove('show'); editingCustomerPhone = null; }

function saveEditedCustomer() {
  const originalPhone = el('edit-cust-original-phone').value;
  const fname = el('edit-cust-fname').value.trim();
  const lname = el('edit-cust-lname').value.trim();
  const newPhone = el('edit-cust-phone').value.trim();
  const id_no = el('edit-cust-id').value.trim();
  
  if (!fname || !lname || !newPhone || !id_no) { alert('⚠️ أكمل جميع الحقول!'); return; }
  
  const c = DB.customers[originalPhone];
  if (originalPhone !== newPhone && DB.customers[newPhone]) { alert('⚠️ رقم الهاتف مستخدم من قبل زبون آخر!'); return; }
  
  // تحديث البيانات
  c.fname = fname;
  c.lname = lname;
  c.id_no = id_no;
  
  if (originalPhone !== newPhone) {
    DB.customers[newPhone] = c;
    delete DB.customers[originalPhone];
    // تحديث رقم الهاتف في الحركات
    DB.transactions.forEach(tx => { if (tx.phone === originalPhone) tx.phone = newPhone; });
  }
  
  save(DB);
  alert('✅ تم تحديث بيانات الزبون بنجاح');
  closeEditCustomerModal();
  renderCustomers();
}

function showCustomerTransactions(phone) {
  viewingCustomerPhone = phone;
  const c = DB.customers[phone];
  el('customer-txs-name').textContent = `${c.fname} ${c.lname} (${c.phone})`;
  
  // عرض الأرصدة الكاملة
  const balanceHtml = Object.entries(c.balance).map(([cur, amt]) => {
    const iqdValue = amt * (DB.rates[cur] || 1);
    return `<div style="background:var(--bg2);border-radius:8px;padding:10px;text-align:center"><div style="color:var(--gold);font-size:14px">${cur}</div><div style="font-weight:700;color:${amt < 0 ? 'var(--red)' : 'var(--green)'};direction:ltr">${amt < 0 ? '-' : ''}${fmt(Math.abs(amt))}</div><div style="font-size:11px;color:var(--muted);direction:ltr">= ${fmt(iqdValue)} IQD</div></div>`;
  }).join('');
  el('full-balance-display').innerHTML = balanceHtml;
  
  const today = new Date();
  const monthStart = new Date(today.getFullYear(), today.getMonth(), 1);
  el('txs-from-date').value = monthStart.toISOString().split('T')[0];
  el('txs-to-date').value = today.toISOString().split('T')[0];
  dateRangeFilter = { from: el('txs-from-date').value, to: el('txs-to-date').value };
  updateRangeShortcutsActive('thisMonth');
  renderCustomerTxsList();
  el('modal-customer-txs').classList.add('show');
}

function closeCustomerTxsModal() { el('modal-customer-txs').classList.remove('show'); viewingCustomerPhone = null; }

function setDateRangeShortcut(type) {
  const today = new Date(); let from = '', to = '';
  if (type === 'today') { from = to = today.toISOString().split('T')[0]; }
  else if (type === 'thisMonth') { from = new Date(today.getFullYear(), today.getMonth(), 1).toISOString().split('T')[0]; to = today.toISOString().split('T')[0]; }
  else if (type === 'last3Months') { from = new Date(today.getFullYear(), today.getMonth() - 3, today.getDate()).toISOString().split('T')[0]; to = today.toISOString().split('T')[0]; }
  else if (type === 'all') { from = '2000-01-01'; to = today.toISOString().split('T')[0]; }
  el('txs-from-date').value = from; el('txs-to-date').value = to;
  updateRangeShortcutsActive(type);
}

function updateRangeShortcutsActive(type) {
  document.querySelectorAll('#modal-customer-txs .calendar-shortcut').forEach(btn => btn.classList.remove('active'));
  if (type === 'today') document.querySelector('[onclick*="today"]')?.classList.add('active');
  else if (type === 'thisMonth') document.querySelector('[onclick*="thisMonth"]')?.classList.add('active');
  else if (type === 'last3Months') document.querySelector('[onclick*="last3Months"]')?.classList.add('active');
  else if (type === 'all') document.querySelector('[onclick*="all"]')?.classList.add('active');
}

function applyDateRangeFilter() { dateRangeFilter = { from: el('txs-from-date').value, to: el('txs-to-date').value }; renderCustomerTxsList(); }

function renderCustomerTxsList() {
  if (!viewingCustomerPhone) return;
  const fromDate = dateRangeFilter.from, toDate = dateRangeFilter.to;
  let txs = DB.transactions.filter(tx => tx.phone === viewingCustomerPhone);
  if (fromDate && toDate) txs = txs.filter(tx => { const txDate = tx.date.split(' ')[0].split('/').reverse().join('-'); return txDate >= fromDate && txDate <= toDate; });
  txs = txs.reverse();
  const container = el('customer-txs-list');
  if (!txs.length) { container.innerHTML = `<div class="empty"><div class="empty-icon">💸</div>لا توجد حركات</div>`; return; }
  container.innerHTML = txs.map(tx => renderTxItem(tx)).join('');
}

function deleteCustomer(phone) { if (!confirm('هل أنت متأكد من حذف هذا الزبون؟ لا يمكن التراجع!')) return; delete DB.customers[phone]; save(DB); alert('✅ تم حذف الزبون بنجاح'); renderCustomers(); renderDebts(); renderCredits(); }

function addCustomer() {
  const fname = el('new-fname').value.trim(), lname = el('new-lname').value.trim();
  const phone = el('new-tel').value.trim(), id_no = el('new-id').value.trim(), pass = el('new-pass').value;
  if (!fname || !lname || !phone || !id_no || !pass) { alert('⚠️ أكمل جميع الحقول!'); return; }
  if (DB.customers[phone]) { alert('⚠️ الهاتف مسجل مسبقاً!'); return; }
  DB.customers[phone] = { fname, lname, phone, id_no, pass: CryptoJS.SHA256(pass).toString(), balance: { USD: 0, EUR: 0, TRY: 0, IQD: 0, GBP: 0, SAR: 0 } };
  save(DB);
  el('new-fname').value = ''; el('new-lname').value = ''; el('new-tel').value = ''; el('new-id').value = ''; el('new-pass').value = '';
  alert('✅ تم التسجيل!'); showTab('customers');
}

function renderDebts() {
  const debtors = Object.values(DB.customers).filter(c => Object.values(c.balance).some(v => v < 0));
  const list = el('debts-list'), summaryContainer = el('debts-summary-container');
  let totalDebtIQD = 0, totalDebtUSD = 0;
  debtors.forEach(c => { Object.entries(c.balance).forEach(([cur, amt]) => { if (amt < 0) { if (cur === 'IQD') totalDebtIQD += Math.abs(amt); else if (cur === 'USD') totalDebtUSD += Math.abs(amt); } }); });
  const usdRate = DB.rates.USD || 1450;
  const totalDebtAll = totalDebtIQD + (totalDebtUSD * usdRate);
  summaryContainer.innerHTML = debtors.length > 0 ? `<div class="debt-summary"><div class="debt-summary-title">📊 ملخص الديون</div><div class="debt-summary-row"><span class="debt-summary-label">عدد المدينين</span><span class="debt-summary-value red">${debtors.length}</span></div><div class="debt-summary-row"><span class="debt-summary-label">مجموع الديون بالدينار</span><span class="debt-summary-value red">${fmt(totalDebtIQD)} IQD</span></div><div class="debt-summary-row"><span class="debt-summary-label">مجموع الديون بالدولار</span><span class="debt-summary-value red">${fmt(totalDebtUSD)} USD</span></div><div class="debt-total-row"><span class="debt-total-label">المجموع الكلي للديون (IQD)</span><span class="debt-total-value">${fmt(totalDebtAll)} IQD</span></div></div>` : '';
  if (!debtors.length) { list.innerHTML = `<div class="empty"><div class="empty-icon">✅</div>✅ لا يوجد زبائن مدينون</div>`; return; }
  list.innerHTML = debtors.map(c => {
    const debts = Object.entries(c.balance).filter(([, v]) => v < 0);
    return `<div class="debt-card"><div class="debt-card-header"><span class="debt-card-name">👤 ${c.fname} ${c.lname}</span><span class="debt-card-phone">${c.phone}</span></div><div class="debt-items-grid">${debts.map(([cur, amt]) => { const iqdValue = cur === 'IQD' ? Math.abs(amt) : Math.abs(amt) * usdRate; return `<div class="debt-item-card"><div class="debt-item-currency">${cur}</div><div class="debt-item-amount">${fmt(Math.abs(amt))}</div><div class="debt-item-iqd">= ${fmt(iqdValue)} IQD</div></div>`; }).join('')}</div></div>`;
  }).join('');
}

function renderCredits() {
  const creditors = Object.values(DB.customers).filter(c => Object.values(c.balance).some(v => v > 0));
  const list = el('credits-list'), summaryContainer = el('credits-summary-container');
  let totalCreditIQD = 0, totalCreditUSD = 0;
  creditors.forEach(c => { Object.entries(c.balance).forEach(([cur, amt]) => { if (amt > 0) { if (cur === 'IQD') totalCreditIQD += amt; else if (cur === 'USD') totalCreditUSD += amt; } }); });
  const usdRate = DB.rates.USD || 1450;
  const totalCreditAll = totalCreditIQD + (totalCreditUSD * usdRate);
  summaryContainer.innerHTML = creditors.length > 0 ? `<div class="credit-summary"><div class="credit-summary-title">📊 ملخص الدائنين</div><div class="credit-summary-row"><span class="credit-summary-label">عدد الدائنين</span><span class="credit-summary-value green">${creditors.length}</span></div><div class="credit-summary-row"><span class="credit-summary-label">مجموع الدائنين بالدينار</span><span class="credit-summary-value green">${fmt(totalCreditIQD)} IQD</span></div><div class="credit-summary-row"><span class="credit-summary-label">مجموع الدائنين بالدولار</span><span class="credit-summary-value green">${fmt(totalCreditUSD)} USD</span></div><div class="credit-total-row"><span class="credit-total-label">المجموع الكلي للدائنين (IQD)</span><span class="credit-total-value">${fmt(totalCreditAll)} IQD</span></div></div>` : '';
  if (!creditors.length) { list.innerHTML = `<div class="empty"><div class="empty-icon">✅</div>✅ لا يوجد زبائن دائنون</div>`; return; }
  list.innerHTML = creditors.map(c => {
    const credits = Object.entries(c.balance).filter(([, v]) => v > 0);
    return `<div class="credit-card"><div class="credit-card-header"><span class="credit-card-name">👤 ${c.fname} ${c.lname}</span><span class="credit-card-phone">${c.phone}</span></div><div class="credit-items-grid">${credits.map(([cur, amt]) => { const iqdValue = cur === 'IQD' ? amt : amt * usdRate; return `<div class="credit-item-card"><div class="credit-item-currency">${cur}</div><div class="credit-item-amount">${fmt(amt)}</div><div class="credit-item-iqd">= ${fmt(iqdValue)} IQD</div></div>`; }).join('')}</div></div>`;
  }).join('');
}

function renderRates() {
  el('rates-list').innerHTML = ['USD', 'EUR', 'TRY', 'IQD', 'GBP', 'SAR'].map(c => `<div style="background:var(--card);border:1px solid var(--border);border-radius:12px;padding:14px;margin-bottom:10px;display:flex;align-items:center;justify-content:space-between"><span style="font-weight:600">1 ${c} =</span><div style="display:flex;align-items:center;gap:8px"><input type="text" id="rate-${c}" value="${fmt(DB.rates[c] || 1)}" oninput="formatNumberInput(this)" style="width:130px;margin-bottom:0;text-align:center;font-weight:700;color:var(--gold)"><span style="color:var(--muted)">IQD</span></div></div>`).join('');
}

function saveRates() { ['USD', 'EUR', 'TRY', 'IQD', 'GBP', 'SAR'].forEach(c => { DB.rates[c] = parseNumber(el('rate-' + c).value); }); save(DB); alert('✅ تم حفظ الأسعار!'); renderDailySummary(); renderDebts(); renderCredits(); }

function renderAllTxs() { const txs = [...DB.transactions].reverse(); const list = el('all-txs-list'); if (!txs.length) { list.innerHTML = `<div class="empty"><div class="empty-icon">💸</div>لا توجد حركات</div>`; return; } list.innerHTML = txs.map(tx => renderTxItem(tx)).join(''); }

// ==================== TRANSACTIONS ====================
function openTxModal(phone) { selectedCustomerForTx = phone; el('tx-amount').value = ''; el('tx-note').value = ''; el('tx-type').value = 'deposit'; el('tx-currency').value = 'USD'; el('tx-preview').style.display = 'none'; el('modal-tx').classList.add('show'); }
function closeTxModal() { el('modal-tx').classList.remove('show'); selectedCustomerForTx = null; }
function updatePreview() { const amount = parseNumber(el('tx-amount').value), currency = el('tx-currency').value, type = el('tx-type').value; if (!amount) { el('tx-preview').style.display = 'none'; return; } const c = DB.customers[selectedCustomerForTx]; const current = c.balance[currency] || 0; const after = type === 'deposit' ? current + amount : current - amount; el('tx-preview').style.display = 'block'; el('preview-value').textContent = (after < 0 ? '-' : '') + fmt(Math.abs(after)) + ' ' + currency; el('preview-value').style.color = after < 0 ? 'var(--red)' : 'var(--green)'; }
function confirmTx() { const amount = parseNumber(el('tx-amount').value), currency = el('tx-currency').value, type = el('tx-type').value, note = el('tx-note').value.trim(); if (!amount) { alert('⚠️ أدخل المبلغ'); return; } const c = DB.customers[selectedCustomerForTx]; const current = c.balance[currency] || 0; c.balance[currency] = type === 'deposit' ? current + amount : current - amount; const now = new Date(); DB.transactions.push({ id: Date.now() + '-' + Math.random().toString(36), phone: selectedCustomerForTx, customerName: c.fname + ' ' + c.lname, type: type, amount: amount, currency: currency, note: note, date: now.toLocaleDateString('en-GB') + ' ' + now.toLocaleTimeString('en-GB', {hour: '2-digit', minute: '2-digit'}) }); save(DB); closeTxModal(); renderAdminView(); alert('✅ تمت المعاملة بنجاح'); }

function editTransaction(txId) { const tx = DB.transactions.find(t => t.id === txId); if (!tx) return; editingTxId = txId; el('edit-tx-id').value = txId; el('edit-tx-amount').value = fmt(tx.amount); el('edit-tx-currency').value = tx.currency; el('edit-tx-note').value = tx.note || ''; el('modal-edit-tx').classList.add('show'); }
function closeEditTxModal() { el('modal-edit-tx').classList.remove('show'); editingTxId = null; }
function saveEditedTx() { const tx = DB.transactions.find(t => t.id === editingTxId); if (!tx) return; const newAmount = parseNumber(el('edit-tx-amount').value), newCurrency = el('edit-tx-currency').value, newNote = el('edit-tx-note').value.trim(); if (!newAmount) { alert('⚠️ أدخل المبلغ'); return; } const c = DB.customers[tx.phone]; c.balance[tx.currency] = tx.type === 'deposit' ? c.balance[tx.currency] - tx.amount : c.balance[tx.currency] + tx.amount; c.balance[newCurrency] = tx.type === 'deposit' ? (c.balance[newCurrency] || 0) + newAmount : (c.balance[newCurrency] || 0) - newAmount; tx.amount = newAmount; tx.currency = newCurrency; tx.note = newNote; save(DB); closeEditTxModal(); renderAdminView(); alert('✅ تم تعديل الحركة بنجاح'); }
function deleteTransaction(txId) { if (!confirm('هل أنت متأكد من حذف هذه الحركة؟')) return; const txIndex = DB.transactions.findIndex(t => t.id === txId); if (txIndex === -1) return; const tx = DB.transactions[txIndex]; const c = DB.customers[tx.phone]; c.balance[tx.currency] = tx.type === 'deposit' ? c.balance[tx.currency] - tx.amount : c.balance[tx.currency] + tx.amount; DB.transactions.splice(txIndex, 1); save(DB); renderAdminView(); alert('✅ تم حذف الحركة بنجاح'); }

// ==================== CUSTOMER VIEW ====================
function renderCustomerView() { const c = DB.customers[currentUser]; if (!c) return; el('cust-welcome-label').textContent = 'مرحباً, ' + c.fname + ' ' + c.lname; el('cust-balances').innerHTML = Object.entries(c.balance).map(([cur, amt]) => `<div class="metric ${amt < 0 ? 'negative' : 'positive'}"><div class="metric-label">${cur}</div><div class="metric-value ${amt < 0 ? 'neg' : 'pos'}">${amt < 0 ? '-' : ''}${fmt(Math.abs(amt))}</div></div>`).join(''); const debts = Object.entries(c.balance).filter(([, v]) => v < 0); el('cust-debt-banner').innerHTML = debts.length ? `<div class="debt-banner"><div class="debt-banner-title">🔴 مديون:</div><div class="debt-items">${debts.map(([cur, amt]) => `<span class="debt-item" style="background:rgba(231,76,60,.15);border-radius:20px;padding:4px 12px;color:var(--red)">${fmt(Math.abs(amt))} ${cur}</span>`).join('')}</div></div>` : ''; const myTxs = DB.transactions.filter(tx => tx.phone === currentUser).reverse(); if (!myTxs.length) { el('cust-txs').innerHTML = `<div class="empty"><div class="empty-icon">💸</div>لا توجد حركات</div>`; return; } el('cust-txs').innerHTML = myTxs.map(tx => { const typeLabel = tx.type === 'deposit' ? 'إيداع' : 'سحب'; return `<div class="tx-item"><div class="tx-icon ${tx.type}">${tx.type === 'deposit' ? '⬆️' : '⬇️'}</div><div class="tx-details"><div class="tx-name">${typeLabel}</div><div class="tx-note">${tx.note || '—'}</div><div class="tx-date">${tx.date}</div></div><div class="tx-amount ${tx.type}">${tx.type === 'deposit' ? '+' : '-'}${fmt(tx.amount)} ${tx.currency}</div></div>`; }).join(''); }

// ==================== AUTH & PROFILE ====================
function switchLoginTab(tab) { el('login-admin').style.display = tab === 'admin' ? 'block' : 'none'; el('login-customer').style.display = tab === 'customer' ? 'block' : 'none'; document.querySelectorAll('.toggle-btn').forEach((b, i) => b.classList.toggle('active', (i === 0 && tab === 'admin') || (i === 1 && tab === 'customer'))); }

function loginAdmin() {
  const pass = el('admin-pass').value;
  const admin = DB.admin || { passwordHash: ADMIN_HASH, deviceId: getDeviceId() };
  const currentDeviceId = getDeviceId();
  
  // التحقق من الجهاز
  if (admin.deviceId && admin.deviceId !== currentDeviceId) {
    alert('❌ لا يمكن الدخول من هذا الجهاز! حساب المدير مرتبط بجهاز واحد فقط.');
    return;
  }
  
  if (CryptoJS.SHA256(pass).toString() === admin.passwordHash) {
    // حفظ معرف الجهاز إذا لم يكن موجوداً
    if (!admin.deviceId) {
      admin.deviceId = currentDeviceId;
      save(DB);
    }
    currentRole = 'admin'; currentUser = 'admin';
    showScreen('admin'); renderAdminView();
  } else { alert('❌ كلمة السر خاطئة!'); }
}

function loginCustomer() { const phone = el('cust-phone').value.trim(), pass = el('cust-pass').value; if (!DB.customers[phone]) { alert('❌ الزبون غير موجود!'); return; } if (DB.customers[phone].pass !== CryptoJS.SHA256(pass).toString()) { alert('❌ كلمة السر خاطئة!'); return; } currentRole = 'customer'; currentUser = phone; showScreen('customer'); renderCustomerView(); }
function logout() { currentUser = null; currentRole = null; showScreen('login'); }
function renderAdminView() { renderDailySummary(); renderCustomers(); renderAllTxs(); renderDebts(); renderCredits(); renderRates(); }
function showScreen(id) { document.querySelectorAll('.screen').forEach(s => s.classList.remove('active')); el('screen-' + id).classList.add('active'); }
function showTab(name) { document.querySelectorAll('.tab-panel').forEach(p => p.classList.remove('active')); document.querySelectorAll('.tab').forEach(t => t.classList.remove('active')); el('panel-' + name).classList.add('active'); const tabs = document.querySelectorAll('.tab'); const tabTexts = { 'daily': 'اليومية', 'customers': 'زبائن', 'txs': 'حركات', 'debts': 'ديون', 'credits': 'دائنون', 'rates': 'أسعار', 'new-customer': 'جديد' }; tabs.forEach(tab => { if (tab.textContent.includes(tabTexts[name])) tab.classList.add('active'); }); if (name === 'daily') renderDailySummary(); if (name === 'customers') renderCustomers(); if (name === 'txs') renderAllTxs(); if (name === 'debts') renderDebts(); if (name === 'credits') renderCredits(); if (name === 'rates') renderRates(); }
function goToLogin() { showScreen('login'); }

// ==================== FORGOT PASSWORD ====================
function showForgotPasswordModal() { el('modal-forgot-password').classList.add('show'); }
function closeForgotPasswordModal() { el('modal-forgot-password').classList.remove('show'); }
function sendResetRequest() { const phone = el('forgot-phone').value.trim(); if (!DB.customers[phone]) { alert('❌ رقم الهاتف غير مسجل'); return; } alert('✅ تم إرسال طلبك للمدير. سيتواصل معك قريباً'); closeForgotPasswordModal(); }

// ==================== RESET CUSTOMER PASSWORD ====================
function showResetCustPasswordModal(phone) { resetCustPhone = phone; const c = DB.customers[phone]; el('reset-cust-name').textContent = `${c.fname} ${c.lname}`; el('new-cust-password').value = ''; el('confirm-cust-password').value = ''; el('modal-reset-cust-password').classList.add('show'); }
function closeResetCustPasswordModal() { el('modal-reset-cust-password').classList.remove('show'); resetCustPhone = null; }
function resetCustomerPassword() { const newPass = el('new-cust-password').value, confirmPass = el('confirm-cust-password').value; if (newPass !== confirmPass) { alert('❌ كلمة السر غير متطابقة'); return; } if (newPass.length < 4) { alert('❌ كلمة السر قصيرة جداً'); return; } DB.customers[resetCustPhone].pass = CryptoJS.SHA256(newPass).toString(); save(DB); alert('✅ تم تغيير كلمة السر بنجاح'); closeResetCustPasswordModal(); renderCustomers(); }

// ==================== ADMIN PROFILE ====================
function showAdminProfileModal() { el('modal-admin-profile').classList.add('show'); }
function closeAdminProfileModal() { el('modal-admin-profile').classList.remove('show'); }
function updateAdminProfile() {
  const email = el('admin-email').value.trim();
  const currentPass = el('current-password').value;
  const newPass = el('new-password').value;
  const confirmPass = el('confirm-password').value;
  if (newPass) {
    if (CryptoJS.SHA256(currentPass).toString() !== (DB.admin?.passwordHash || ADMIN_HASH)) { alert('❌ كلمة السر الحالية غير صحيحة'); return; }
    if (newPass !== confirmPass) { alert('❌ كلمة السر غير متطابقة'); return; }
    if (!DB.admin) DB.admin = { email: '', passwordHash: ADMIN_HASH, deviceId: getDeviceId() };
    DB.admin.passwordHash = CryptoJS.SHA256(newPass).toString();
  }
  if (!DB.admin) DB.admin = { email: '', passwordHash: ADMIN_HASH, deviceId: getDeviceId() };
  DB.admin.email = email;
  save(DB); alert('✅ تم حفظ التغييرات'); closeAdminProfileModal();
}

// ==================== INSTALL ====================
window.addEventListener('beforeinstallprompt', (e) => { e.preventDefault(); deferredPrompt = e; });
function showInstallInstructions() { const instructions = el('install-instructions'); const isIOS = /iPhone|iPad|iPod/.test(navigator.userAgent); if (deferredPrompt) { instructions.innerHTML = `<p style="margin-bottom:16px;text-align:center">✅ جهازك يدعم التثبيت المباشر</p><button class="install-btn" onclick="installPWA()" style="font-size:16px">📱 تثبيت الآن</button>`; } else if (isIOS) { instructions.innerHTML = `<div style="text-align:center"><p style="margin-bottom:16px">📱 للتثبيت على الآيفون:</p><div style="background:var(--bg3);padding:20px;border-radius:12px"><p>1️⃣ اضغط على زر <strong style="color:var(--gold)">مشاركة 📤</strong></p><p>2️⃣ اختر <strong style="color:var(--gold)">"إضافة إلى الشاشة الرئيسية"</strong></p><p>3️⃣ اضغط <strong style="color:var(--gold)">"إضافة"</strong></p></div></div>`; } else { instructions.innerHTML = `<div style="text-align:center"><p style="margin-bottom:16px">📱 للتثبيت على الأندرويد:</p><div style="background:var(--bg3);padding:20px;border-radius:12px"><p>1️⃣ اضغط على <strong style="color:var(--gold)">⋮ (القائمة)</strong></p><p>2️⃣ اختر <strong style="color:var(--gold)">"تثبيت التطبيق"</strong></p></div></div>`; } el('install-modal').classList.add('show'); }
function installPWA() { if (deferredPrompt) { deferredPrompt.prompt(); deferredPrompt.userChoice.then(() => { deferredPrompt = null; closeInstallModal(); }); } }
function closeInstallModal() { el('install-modal').classList.remove('show'); }

// ==================== EVENT LISTENERS ====================
el('modal-tx')?.addEventListener('click', function(e) { if (e.target === this) closeTxModal(); });
el('modal-edit-tx')?.addEventListener('click', function(e) { if (e.target === this) closeEditTxModal(); });
el('modal-customer-txs')?.addEventListener('click', function(e) { if (e.target === this) closeCustomerTxsModal(); });
el('modal-edit-customer')?.addEventListener('click', function(e) { if (e.target === this) closeEditCustomerModal(); });
el('modal-forgot-password')?.addEventListener('click', function(e) { if (e.target === this) closeForgotPasswordModal(); });
el('modal-reset-cust-password')?.addEventListener('click', function(e) { if (e.target === this) closeResetCustPasswordModal(); });
el('modal-admin-profile')?.addEventListener('click', function(e) { if (e.target === this) closeAdminProfileModal(); });
el('install-modal')?.addEventListener('click', function(e) { if (e.target === this) closeInstallModal(); });
// ====================   النسخ الاحتياطي====================
  <div class="divider" style="height:1px;background:var(--border);margin:16px 0"></div>
<p style="color:var(--gold);font-weight:700;margin-bottom:10px">📦 إدارة البيانات (النسخ الاحتياطي)</p>
<div style="display:flex;gap:10px">
  <button class="btn btn-sm" onclick="exportData()" style="flex:1;background:#27ae60;color:white">📤 تصدير نسخة</button>
  <button class="btn btn-sm btn-outline" onclick="el('importFile').click()" style="flex:1">📥 استيراد نسخة</button>
  <input type="file" id="importFile" style="display:none" onchange="importData(event)">
</div>
// ====================    تقارير ====================
<button class="tab" onclick="showTab('reports')">📊 تقارير</button>

  // ==================== تقرير الحركات الإجمالي  ====================
<div id="panel-reports" class="tab-panel">
  <div class="content">
    <div class="section-title">📊 تقرير الحركات الإجمالي</div>
    <div class="card" style="margin-bottom:15px">
      <label>من تاريخ</label><input type="date" id="rep-from" class="fund-input" style="margin-bottom:10px">
      <label>إلى تاريخ</label><input type="date" id="rep-to" class="fund-input">
      <button class="btn" onclick="generateReport()">توليد التقرير</button>
    </div>
    <div id="report-results"></div>
  </div>
</div>

  // ==================== 1. طباعة الوصل (Thermal Print Style) ====================
function printReceipt(txId) {
    const tx = DB.transactions.find(t => t.id === txId);
    if (!tx) return;
    
    const printWindow = window.open('', '_blank');
    printWindow.document.write(`
        <html dir="rtl">
        <head>
            <title>وصل صيرفة المستقبل</title>
            <style>
                body { font-family: 'Tajawal', sans-serif; padding: 20px; text-align: center; color: #333; }
                .receipt-box { border: 1px dashed #000; padding: 15px; width: 300px; margin: auto; }
                .header { font-weight: bold; font-size: 20px; margin-bottom: 5px; }
                .divider { border-top: 1px dashed #000; margin: 10px 0; }
                .row { display: flex; justify-content: space-between; margin: 5px 0; font-size: 14px; }
                .footer { font-size: 12px; margin-top: 20px; }
            </style>
        </head>
        <body onload="window.print();window.close()">
            <div class="receipt-box">
                <div class="header">🏦 صيرفة المستقبل</div>
                <div>إدارة: برهان دكاني</div>
                <div class="divider"></div>
                <div class="row"><span>التاريخ:</span> <span>${tx.date}</span></div>
                <div class="row"><span>الزبون:</span> <span>${tx.customerName}</span></div>
                <div class="row"><span>النوع:</span> <span>${tx.type === 'deposit' ? 'إيداع (له)' : 'سحب (عليه)'}</span></div>
                <div class="divider"></div>
                <div style="font-size: 22px; font-weight: bold; margin: 10px 0;">
                    ${fmt(tx.amount)} ${tx.currency}
                </div>
                <div class="row"><span>ملاحظات:</span> <span>${tx.note || '—'}</span></div>
                <div class="divider"></div>
                <div class="footer">شكراً لتعاملكم معنا</div>
            </div>
        </body>
        </html>
    `);
    printWindow.document.close();
}

// تعديل دالة renderTxItem لإضافة زر الطباعة
const originalRenderTxItem = renderTxItem;
renderTxItem = function(tx) {
    let html = originalRenderTxItem(tx);
    const printBtn = `<button class="btn-edit" onclick="printReceipt('${tx.id}')" style="background:rgba(201,168,76,0.1); border-color:var(--gold); color:var(--gold); margin-right:5px">🖨️ وصل</button>`;
    return html.replace('</div><div class="tx-amount', printBtn + '</div><div class="tx-amount');
};

// ==================== 2. النسخ الاحتياطي ====================
function exportData() {
    const dataStr = localStorage.getItem(STORE);
    const blob = new Blob([dataStr], { type: "application/json" });
    const url = URL.createObjectURL(blob);
    const a = document.createElement('a');
    a.href = url;
    a.download = `Sayrafa_Backup_${new Date().toISOString().split('T')[0]}.json`;
    a.click();
}

function importData(event) {
    const file = event.target.files[0];
    if (!file) return;
    const reader = new FileReader();
    reader.onload = function(e) {
        try {
            const content = e.target.result;
            // تجربة فك التشفير للتأكد من صحة الملف
            CryptoJS.AES.decrypt(content, ENCRYPTION_KEY).toString(CryptoJS.enc.Utf8);
            localStorage.setItem(STORE, content);
            alert('✅ تم استيراد البيانات بنجاح! سيتم إعادة تحميل التطبيق.');
            location.reload();
        } catch (err) {
            alert('❌ فشل الاستيراد: الملف غير صحيح أو تالف.');
        }
    };
    reader.readAsText(file);
}

// ==================== 3. التقارير ====================
function generateReport() {
    const from = el('rep-from').value;
    const to = el('rep-to').value;
    if (!from || !to) return alert('يرجى اختيار الفترة الزمنية');

    const filtered = DB.transactions.filter(tx => {
        const txDate = tx.date.split(' ')[0].split('/').reverse().join('-');
        return txDate >= from && txDate <= to;
    });

    const report = {};
    filtered.forEach(tx => {
        if (!report[tx.currency]) report[tx.currency] = { in: 0, out: 0 };
        if (tx.type === 'deposit') report[tx.currency].in += tx.amount;
        else report[tx.currency].out += tx.amount;
    });

    let html = `<h3>من ${from} إلى ${to}</h3>`;
    for (const [cur, val] of Object.entries(report)) {
        html += `
        <div class="fund-block" style="margin-top:10px">
            <div class="fund-block-title">${cur}</div>
            <div class="daily-row"><span class="daily-label">إجمالي الإيداع (+)</span><span class="daily-value" style="color:var(--green)">${fmt(val.in)}</span></div>
            <div class="daily-row"><span class="daily-label">إجمالي السحب (-)</span><span class="daily-value" style="color:var(--red)">${fmt(val.out)}</span></div>
            <div class="daily-row" style="border-top:1px solid var(--gold)"><span class="daily-label">الصافي</span><span class="daily-value">${fmt(val.in - val.out)}</span></div>
        </div>`;
    }
    el('report-results').innerHTML = html || '<p>لا توجد حركات لهذه الفترة</p>';
}

// ==================== INIT ====================
window.addEventListener('load', () => { setTimeout(() => { el('splash').style.opacity = '0'; setTimeout(() => el('splash').style.display = 'none', 600); }, 2000); });
</script>
</body>
</html>
