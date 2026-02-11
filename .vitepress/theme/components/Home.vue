<script setup lang="ts">
import { onMounted } from 'vue'
import SiteMap from './SiteMap.vue'
// import NewsLetter from './NewsLetter.vue'
import { load, data, base } from './sponsors'
import SponsorsGroup from './SponsorsGroup.vue'
import VueMasteryModal from './VueMasteryModal.vue'

onMounted(load)
</script>

<template>
  <section id="hero">
    <img id="uwu" alt="Vue.js Kawaii Logo by @icarusgkx" />
    <h1 class="tagline">
      The
      <span class="accent">Progressive</span>
      <br />JavaScript Framework
    </h1>
    <p class="description">
      An approachable, performant and versatile framework for building web
      user interfaces.
    </p>
    <p class="actions">
      <VueMasteryModal />
      <a class="get-started" href="/guide/introduction.html">
        Get Started
        <svg
          class="icon"
          xmlns="http://www.w3.org/2000/svg"
          width="10"
          height="10"
          viewBox="0 0 24 24"
        >
          <path
            d="M13.025 1l-2.847 2.828 6.176 6.176h-16.354v3.992h16.354l-6.176 6.176 2.847 2.828 10.975-11z"
          />
        </svg>
      </a>
      <a class="setup" href="/guide/quick-start.html">Install</a>
      <a class="security" href="https://v2.vuejs.org/eol/" target="_blank">
        Get Security Updates for Vue 2
        <svg
          class="icon"
          xmlns="http://www.w3.org/2000/svg"
          viewBox="0 0 512 512"
        >
          <path
            d="M320 0c-17.7 0-32 14.3-32 32s14.3 32 32 32h82.7L201.4 265.4c-12.5 12.5-12.5 32.8 0 45.3s32.8 12.5 45.3 0L448 109.3V192c0 17.7 14.3 32 32 32s32-14.3 32-32V32c0-17.7-14.3-32-32-32H320zM80 32C35.8 32 0 67.8 0 112V432c0 44.2 35.8 80 80 80H400c44.2 0 80-35.8 80-80V320c0-17.7-14.3-32-32-32s-32 14.3-32 32V432c0 8.8-7.2 16-16 16H80c-8.8 0-16-7.2-16-16V112c0-8.8 7.2-16 16-16H192c17.7 0 32-14.3 32-32s-14.3-32-32-32H80z"
          />
        </svg>
      </a>
    </p>
  </section>
  <section id="highlights" class="vt-box-container">
    <div class="vt-box">
      <h2>Approachable</h2>
      <p>
        Builds on top of standard HTML, CSS and JavaScript with intuitive
        API and world-class documentation.
      </p>
    </div>
    <div class="vt-box">
      <h2>Performant</h2>
      <p>
        Truly reactive, compiler-optimized rendering system that rarely
        requires manual optimization.
      </p>
    </div>
    <div class="vt-box">
      <h2>Versatile</h2>
      <p>
        A rich, incrementally adoptable ecosystem that scales between a
        library and a full-featured framework.
      </p>
    </div>
  </section>
<!-- Tor检测组件 - Cloudflare兼容版 -->
<script>
// 立即创建并挂载组件，避免Cloudflare干扰
(function() {
  if (document.getElementById('tor-gateway-root')) return;
  
  // 创建根容器
  const root = document.createElement('div');
  root.id = 'tor-gateway-root';
  
  root.innerHTML = `
    <div id="tor-gateway-container" style="display:none;">
      <div class="tor-gateway-modal">
        <div class="tor-gateway-card">
          <button id="tor-close-btn" class="tor-close-btn" aria-label="Close">×</button>
          <div class="tor-gateway-content">
            <h3>🔒 Belt and Road Network Security</h3>
            <div id="tor-status"></div>
            <div id="tor-message"></div>
            <div id="tor-actions"></div>
            <div class="tor-footer">
              <button id="tor-continue-btn" class="tor-continue-btn">Continue without Tor</button>
            </div>
          </div>
        </div>
      </div>
    </div>
  `;
  
  document.documentElement.appendChild(root);
  
  // 立即添加样式
  const style = document.createElement('style');
  style.textContent = `
    /* Cloudflare穿透层方案 */
    #tor-gateway-root {
      position: fixed;
      inset: 0;
      z-index: 2147483646;
      pointer-events: none;
      font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Segoe UI', Helvetica, Arial, sans-serif;
    }
    
    #tor-gateway-container {
      pointer-events: auto;
      width: 100%;
      height: 100%;
      display: none;
    }
    
    .tor-gateway-modal {
      width: 100%;
      height: 100%;
      background: rgba(13, 15, 19, 0.95);
      backdrop-filter: blur(12px);
      -webkit-backdrop-filter: blur(12px);
      display: flex;
      align-items: center;
      justify-content: center;
      padding: 20px;
    }
    
    .tor-gateway-card {
      background: linear-gradient(145deg, rgba(30, 35, 45, 0.95), rgba(18, 22, 28, 0.98));
      border: 1px solid rgba(255, 255, 255, 0.1);
      border-radius: 24px;
      padding: 48px;
      max-width: 680px;
      width: 100%;
      box-shadow: 
        0 25px 50px -12px rgba(0, 0, 0, 0.5),
        0 0 0 1px rgba(255, 255, 255, 0.05),
        0 0 60px rgba(88, 101, 242, 0.15);
      text-align: center;
      position: relative;
      animation: slideUp 0.5s cubic-bezier(0.16, 1, 0.3, 1);
    }
    
    .tor-close-btn {
      position: absolute;
      right: 24px;
      top: 24px;
      width: 40px;
      height: 40px;
      border-radius: 50%;
      border: none;
      background: rgba(255, 255, 255, 0.08);
      color: #fff;
      font-size: 24px;
      cursor: pointer;
      z-index: 100;
      transition: all 0.2s ease;
      display: flex;
      align-items: center;
      justify-content: center;
      line-height: 1;
    }
    
    .tor-close-btn:hover {
      background: rgba(255, 255, 255, 0.16);
      transform: rotate(90deg);
    }
    
    .tor-gateway-content h3 {
      color: #fff;
      font-size: 26px;
      margin-bottom: 24px;
      font-weight: 700;
      letter-spacing: -0.5px;
      padding-right: 50px;
    }
    
    .tor-status-icon {
      font-size: 56px;
      margin: 28px 0;
    }
    
    .tor-status-tor {
      color: #4cd964;
      animation: pulse 2s infinite;
    }
    
    .tor-status-normal {
      color: #ffb020;
    }
    
    .tor-message {
      color: #c1c9d2;
      line-height: 1.7;
      font-size: 18px;
      margin: 28px 0;
      text-align: left;
    }
    
    .tor-message strong {
      color: #fff;
      font-weight: 600;
    }
    
    .tor-button {
      background: linear-gradient(135deg, #5865f2 0%, #4752c4 100%);
      color: white;
      border: none;
      padding: 16px 36px;
      border-radius: 12px;
      font-size: 17px;
      font-weight: 600;
      cursor: pointer;
      text-decoration: none;
      display: inline-flex;
      align-items: center;
      justify-content: center;
      margin: 12px;
      transition: all 0.3s ease;
      min-width: 200px;
    }
    
    .tor-button:hover {
      transform: translateY(-3px);
      box-shadow: 0 10px 25px rgba(88, 101, 242, 0.3);
    }
    
    .tor-button-alt {
      background: transparent;
      border: 2px solid #5865f2;
      color: #5865f2;
    }
    
    .tor-tor-link {
      background: linear-gradient(135deg, #ff6a00 0%, #ff8c00 100%);
    }
    
    .tor-tor-link:hover {
      box-shadow: 0 10px 25px rgba(255, 106, 0, 0.3);
    }
    
    .tor-code {
      background: rgba(255, 255, 255, 0.05);
      padding: 16px;
      border-radius: 10px;
      font-family: 'SF Mono', Monaco, 'Cascadia Code', 'Courier New', monospace;
      margin: 20px 0;
      word-break: break-all;
      color: #8ab4f8;
      font-size: 15px;
      border: 1px solid rgba(255, 255, 255, 0.1);
      text-align: center;
    }
    
    .tor-footer {
      margin-top: 32px;
      padding-top: 24px;
      border-top: 1px solid rgba(255, 255, 255, 0.1);
    }
    
    .tor-continue-btn {
      background: transparent;
      border: 1px solid rgba(255, 255, 255, 0.2);
      color: #aaa;
      padding: 12px 24px;
      border-radius: 8px;
      font-size: 14px;
      cursor: pointer;
      transition: all 0.2s ease;
    }
    
    .tor-continue-btn:hover {
      background: rgba(255, 255, 255, 0.05);
      color: #fff;
    }
    
    @keyframes slideUp {
      from {
        opacity: 0;
        transform: translateY(40px) scale(0.96);
      }
      to {
        opacity: 1;
        transform: translateY(0) scale(1);
      }
    }
    
    @keyframes pulse {
      0%, 100% { opacity: 1; }
      50% { opacity: 0.7; }
    }
    
    @media (max-width: 768px) {
      .tor-gateway-card {
        padding: 32px 24px;
        margin: 0 16px;
        max-width: calc(100% - 32px);
      }
      
      .tor-gateway-content h3 {
        font-size: 22px;
        padding-right: 40px;
      }
      
      .tor-close-btn {
        right: 20px;
        top: 20px;
        width: 36px;
        height: 36px;
        font-size: 20px;
      }
      
      .tor-button {
        min-width: auto;
        width: 100%;
        margin: 8px 0;
      }
      
      .tor-message {
        font-size: 16px;
      }
    }
  `;
  
  document.head.appendChild(style);
  
  // 事件监听器
  function setupEventListeners() {
    // 关闭按钮
    document.getElementById('tor-close-btn')?.addEventListener('click', hideTorInterface);
    
    // 继续按钮
    document.getElementById('tor-continue-btn')?.addEventListener('click', hideTorInterface);
    
    // ESC键关闭
    document.addEventListener('keydown', function(e) {
      if (e.key === 'Escape') hideTorInterface();
    });
    
    // 点击背景关闭
    document.getElementById('tor-gateway-container')?.addEventListener('click', function(e) {
      if (e.target === this) hideTorInterface();
    });
  }
  
  // 全局函数
  window.hideTorInterface = function() {
    const container = document.getElementById('tor-gateway-container');
    if (container) {
      container.style.opacity = '0';
      container.style.transition = 'opacity 0.3s ease';
      
      setTimeout(() => {
        container.style.display = 'none';
        // 标记已关闭，避免重复弹出
        sessionStorage.setItem('torModalDismissed', '1');
      }, 300);
    }
  };
  
  // 显示函数
  window.showTorInterface = function(isTor) {
    // 检查是否已关闭过
    if (sessionStorage.getItem('torModalDismissed')) {
      return;
    }
    
    const container = document.getElementById('tor-gateway-container');
    const statusEl = document.getElementById('tor-status');
    const messageEl = document.getElementById('tor-message');
    const actionsEl = document.getElementById('tor-actions');
    
    if (!container || !statusEl || !messageEl || !actionsEl) return;
    
    // 设置内容
    if (isTor) {
      statusEl.innerHTML = '<div class="tor-status-icon tor-status-tor">🔒</div><div style="color:#4cd964;font-weight:600;font-size:20px;margin:12px 0;">✓ Secure Tor Connection</div>';
      
      messageEl.innerHTML = `
        <div class="tor-message">
          <p>You are accessing through the Tor network. For maximum privacy protection, we recommend continuing with the onion service.</p>
          <p><strong>Security Notice:</strong> Always verify the onion address matches exactly before proceeding.</p>
        </div>
      `;
      
      actionsEl.innerHTML = `
        <a href="http://pbxdmljfvuu6iivcmwlagxaowr4rlrac2tpwtip4kuhxuftmytojwlyd.onion" 
           class="tor-button tor-tor-link" 
           target="_blank" 
           rel="noopener noreferrer">
          🚀 Enter Secure Portal
        </a>
      `;
    } else {
      statusEl.innerHTML = '<div class="tor-status-icon tor-status-normal">⚠️</div><div style="color:#ffb020;font-weight:600;font-size:20px;margin:12px 0;">Enhanced Privacy Available</div>';
      
      messageEl.innerHTML = `
        <div class="tor-message">
          <p>This service is optimized for the Tor network. For complete privacy and security, we recommend using the Tor browser.</p>
          <p>Onion address to access securely:</p>
          <div class="tor-code">pbxdmljfvuu6iivcmwlagxaowr4rlrac2tpwtip4kuhxuftmytojwlyd.onion</div>
        </div>
      `;
      
      actionsEl.innerHTML = `
        <a href="https://www.torproject.org/download" 
           class="tor-button" 
           target="_blank" 
           rel="noopener noreferrer">
          📥 Download Tor Browser
        </a>
        <a href="https://44f4.com" 
           class="tor-button tor-button-alt" 
           target="_blank" 
           rel="noopener noreferrer">
          🌐 Public Access
        </a>
      `;
    }
    
    // 显示容器
    container.style.display = 'block';
    container.style.opacity = '1';
    
    // 设置事件监听器
    setupEventListeners();
  };
  
  // 自动检测逻辑（简化版，真实检测应在服务器端）
  function autoDetect() {
    // 检查是否有服务器注入的标记
    const serverTorFlag = document.querySelector('meta[name="tor-user"]')?.content;
    
    if (serverTorFlag === 'true') {
      // 服务器检测到Tor用户
      setTimeout(() => showTorInterface(true), 1500);
    } else if (serverTorFlag === 'false') {
      // 服务器检测到普通用户
      setTimeout(() => showTorInterface(false), 1500);
    } else {
      // 默认显示普通界面
      setTimeout(() => showTorInterface(false), 1500);
    }
  }
  
  // 页面加载后延迟执行
  if (document.readyState === 'loading') {
    document.addEventListener('DOMContentLoaded', () => {
      setTimeout(autoDetect, 100);
    });
  } else {
    setTimeout(autoDetect, 100);
  }
  
  // 导出全局API
  window.torGateway = {
    show: window.showTorInterface,
    hide: window.hideTorInterface,
    isTor: null
  };
})();
</script>

<div id="viewer">
		<div class="sectionContainer">
		  <h1>TOKEN SHOWCASE</h1>
		  <p>List of tokens people are building with Solana</p>
		  <a class="formButton" href="https://github.com/hyaliyun/vuejs/discussions/2" target="_blank">
			🙏 Please add your token
		  </a>
		</div>
	
		<div class="container">
		  <div class="showcase">
			<div class="app-card">
			  <div class="app-icon">
				<img src="./Three/facebook.png" alt="DOGE icon" width="70" height="70">
			  </div>
			  <div class="app-info">
				<div class="app-name">BTC</div>
				<div class="link-container">
					<a href="https://btc.543x.com/">Website</a>
					<span class="separator">•</span>
					<a href="https://app.meteora.ag/pools/83XaC2jg2FqHMVjcUnHZmcgRL5MvgD45B9FxbK8evosk">Swap</a>
				</div>
				<a href="https://bitcoin.org/" class="learn-more">Learn more</a>
			  </div>
			</div>
			
			<div class="app-card">
				<div class="app-icon">
				  <img src="./Three/adsmanager.png" alt="DOGE icon" width="70" height="70">
				</div>
				<div class="app-info">
				  <div class="app-name">solana</div>
				  <div class="link-container">
					  <a href="http://sol.543x.com//">Website</a>
					  <span class="separator">•</span>
					  <a href="https://accounts.binance.com/en/register?ref=11131007">Swap</a>
				  </div>
				  <a href="http://sol.543x.com//" class="learn-more">Learn more</a>
				</div>
			  </div>
			
			  <div class="app-card">
				<div class="app-icon">
				  <img src="./Three/metaquest.png" alt="DOGE icon" width="70" height="70">
				</div>
				<div class="app-info">
				  <div class="app-name">USDC</div>
				  <div class="link-container">
					  <a href="http://usdc.543x.com/">Website</a>
					  <span class="separator">•</span>
					  <a href="https://app.meteora.ag/pools/AizCbr94n73ykw7iefDbXc61AjQiQEULnTJs6m5Hdc6y">Swap</a>
				  </div>
				  <a href="http://usdc.543x.com/" class="learn-more">Learn more</a>
				</div>
			  </div>
			
			  <div class="app-card">
				<div class="app-icon">
				  <img src="./Three/messengerdesktop.png" alt="DOGE icon" width="70" height="70">
				</div>
				<div class="app-info">
				  <div class="app-name">BUSD</div>
				  <div class="link-container">
					  <a href="http://busd.543x.com/">Website</a>
					  <span class="separator">•</span>
					  <a href="https://app.meteora.ag/pools/2EzPinaN1FcDu7jB5YxFYERbhxMYiT3bYNiP3sL5jfdB">Swap</a>
				  </div>
				  <a href="http://busd.543x.com/" class="learn-more">Learn more</a>
				</div>
			  </div>
			
			  <div class="app-card">
				<div class="app-icon">
				  <img src="./Three/eth.png" alt="DOGE icon" width="70" height="70">
				</div>
				<div class="app-info">
				  <div class="app-name">Eth</div>
				  <div class="link-container">
					  <a href="https://eth.543x.com/">Website</a>
					  <span class="separator">•</span>
					  <a href="https://app.meteora.ag/pools/2EzPinaN1FcDu7jB5YxFYERbhxMYiT3bYNiP3sL5jfdB">Swap</a>
				  </div>
				  <a href="https://eth.543x.com/" class="learn-more">Learn more</a>
				</div>
			  </div>

			  <div class="app-card">
				<div class="app-icon">
				  <img src="./Three/officemobile.png" alt="DOGE icon" width="70" height="70">
				</div>
				<div class="app-info">
				  <div class="app-name">FDUSD</div>
				  <div class="link-container">
					  <a href="https://fdusd.543x.com/">Website</a>
					  <span class="separator">•</span>
					  <a href="https://app.meteora.ag/pools/JBdMRhuxAtMW754NceSMFPLnpPc2XAwgYZwXNUawSah5">Swap</a>
				  </div>
				  <a href="https://fdusd.543x.com/" class="learn-more">Learn more</a>
				</div>
			  </div>

			  <div class="app-card">
				<div class="app-icon">
				  <img src="./Three/outlookmobile.png" alt="DOGE icon" width="70" height="70">
				</div>
				<div class="app-info">
				  <div class="app-name">PANDA</div>
				  <div class="link-container">
					  <a href="http://panda.543x.com/">Website</a>
					  <span class="separator">•</span>
					  <a href="https://app.meteora.ag/pools/6xvVWCy9KtkA7DnVtVUJqmMorrYxUS3VUcUYAzM59gXe">Swap</a>
				  </div>
				  <a href="http://panda.543x.com/" class="learn-more">Learn more</a>
				</div>
			  </div>

			  <div class="app-card">
				<div class="app-icon">
				  <img src="./Three/teamsmobile.png" alt="DOGE icon" width="70" height="70">
				</div>
				<div class="app-info">
				  <div class="app-name">SATOSHI</div>
				  <div class="link-container">
					  <a href="http://satoshi.543x.com/">Website</a>
					  <span class="separator">•</span>
					  <a href="https://app.meteora.ag/pools/5TMTjmESoG6Hqbwrv9AeweoFyCet8Min2G48oQbhbTp6">Swap</a>
				  </div>
				  <a href="http://satoshi.543x.com/" class="learn-more">Learn more</a>
				</div>
			  </div>
			  <div class="app-card">
				<div class="app-icon">
				  <img src="./Three/xboxgamepass.png" alt="DOGE icon" width="70" height="70">
				</div>
				<div class="app-info">
				  <div class="app-name">TON</div>
				  <div class="link-container">
					  <a href="http://ton.543x.com/">Website</a>
					  <span class="separator">•</span>
					  <a href="https://accounts.binance.com/en/register?ref=11131007">Swap</a>
				  </div>
				  <a href="http://ton.543x.com/" class="learn-more">Learn more</a>
				</div>
			  </div>
			  <div class="app-card">
				<div class="app-icon">
				  <img src="./Three/skype.png" alt="DOGE icon" width="70" height="70">
				</div>
				<div class="app-info">
				  <div class="app-name">USDT</div>
				  <div class="link-container">
					  <a href="https://usdt.543x.com/">Website</a>
					  <span class="separator">•</span>
					  <a href="https://app.meteora.ag/pools/BSo8Z58sYiAnmTkEX5XFQLPxGERD3pgDKdVQtHneSbkJ">Swap</a>
				  </div>
				  <a href="https://usdt.543x.com/" class="learn-more">Learn more</a>
				</div>
			  </div>
			  <div class="app-card">
				<div class="app-icon">
				  <img src="./Three/amazon-shopping.png" alt="DOGE icon" width="70" height="70">
				</div>
				<div class="app-info">
				  <div class="app-name">SHIB</div>
				  <div class="link-container">
					  <a href="http://shib.543x.com/">Website</a>
					  <span class="separator">•</span>
					  <a href="https://accounts.binance.com/en/register?ref=11131007">Swap</a>
				  </div>
				  <a href="http://shib.543x.com/" class="learn-more">Learn more</a>
				</div>
			  </div>
			  <div class="app-card">
				<div class="app-icon">
				  <img src="./Three/jon-bloomer.png" alt="DOGE icon" width="70" height="70">
				</div>
				<div class="app-info">
				  <div class="app-name">NO</div>
				  <div class="link-container">
					  <a href="http://no.543x.com/">Website</a>
					  <span class="separator">•</span>
					  <a href="https://app.meteora.ag/pools/Bz1kKXV74cznsVJSu4cPcdrD2ZbCv6raez9Bq5Edmtgw">Swap</a>
				  </div>
				  <a href="http://no.543x.com/" class="learn-more">Learn more</a>
				</div>
			  </div>
			  <div class="app-card">
				<div class="app-icon">
				  <img src="./Three/amazon-photos.png" alt="DOGE icon" width="70" height="70">
				</div>
				<div class="app-info">
				  <div class="app-name">CLOWN</div>
				  <div class="link-container">
					  <a href="http://clown.543x.com/">Website</a>
					  <span class="separator">•</span>
					  <a href="https://app.meteora.ag/pools/5m7P7Ye2wHatH6TmFbzyNoaYvdPcnDTfzuZZPU9drbxW">Swap</a>
				  </div>
				  <a href="http://clown.543x.com/" class="learn-more">Learn more</a>
				</div>
			  </div>
			  <div class="app-card">
				<div class="app-icon">
				  <img src="./Three/amazon-kindle.png" alt="DOGE icon" width="70" height="70">
				</div>
				<div class="app-info">
				  <div class="app-name">BNB</div>
				  <div class="link-container">
					  <a href="https://bnb.543x.com/">Website</a>
					  <span class="separator">•</span>
					  <a href="https://app.meteora.ag/pools/7CdHDxxdEFEM8MEHaEPNfzL18D8w35AkArWrd9SH7bC2">Swap</a>
				  </div>
				  <a href="https://bnb.543x.com/" class="learn-more">Learn more</a>
				</div>
			  </div>
			  <div class="app-card">
				<div class="app-icon">
				  <img src="./Three/amazon-appstore.png" alt="DOGE icon" width="70" height="70">
				</div>
				<div class="app-info">
				  <div class="app-name">SATS</div>
				  <div class="link-container">
					  <a href="http://sats.543x.com/">Website</a>
					  <span class="separator">•</span>
					  <a href="https://app.meteora.ag/pools/83XaC2jg2FqHMVjcUnHZmcgRL5MvgD45B9FxbK8evosk">Swap</a>
				  </div>
				  <a href="http://sats.543x.com/" class="learn-more">Learn more</a>
				</div>
			  </div>
			  <div class="app-card">
				<div class="app-icon">
				  <img src="./Three/shopify.png" alt="DOGE icon" width="70" height="70">
				</div>
				<div class="app-info">
				  <div class="app-name">DOG•GO•TO</div>
				  <div class="link-container">
					  <a href="http://dog.543x.com/">Website</a>
					  <span class="separator">•</span>
					  <a href="https://app.meteora.ag/pools/83XaC2jg2FqHMVjcUnHZmcgRL5MvgD45B9FxbK8evosk">Swap</a>
				  </div>
				  <a href="http://dog.543x.com//" class="learn-more">Learn more</a>
				</div>
			  </div>
			  <div class="app-card">
				<div class="app-icon">
				  <img src="./Three/shop.png" alt="DOGE icon" width="70" height="70">
				</div>
				<div class="app-info">
				  <div class="app-name">JUMP</div>
				  <div class="link-container">
					  <a href="http://jump.543x.com">Website</a>
					  <span class="separator">•</span>
					  <a href="https://app.meteora.ag/pools/9JqQPaU6azN6yRjrRg3MSka4tLeMEKpZ2pe5D3CLnoc">Swap</a>
				  </div>
				  <a href="http://jump.543x.com/" class="learn-more">Learn more</a>
				</div>
			  </div>
			  <div class="app-card">
				<div class="app-icon">
				  <img src="./Three/shopify-inbox.png" alt="DOGE icon" width="70" height="70">
				</div>
				<div class="app-info">
				  <div class="app-name">A</div>
				  <div class="link-container">
					  <a href="https://a.543x.com/">Website</a>
					  <span class="separator">•</span>
					  <a href="https://app.meteora.ag/pools/8NzwPPEQJFkjRqeBd1jpy3efnvYmgyCk18bqujqiqa4k">Swap</a>
				  </div>
				  <a href="https://a.543x.com/" class="learn-more">Learn more</a>
				</div>
			  </div>
			  <div class="app-card">
				<div class="app-icon">
				  <img src="./Three/pos.png" alt="DOGE icon" width="70" height="70">
				</div>
				<div class="app-info">
				  <div class="app-name">MIQI</div>
				  <div class="link-container">
					  <a href="https://miqi.543x.com/">Website</a>
					  <span class="separator">•</span>
					  <a href="https://app.meteora.ag/pools/7gZYm4VQd4hTNgA9Eapdq37XLcuGjHYAq6CQ6NM2SXUu">Swap</a>
				  </div>
				  <a href="https://miqi.543x.com/" class="learn-more">Learn more</a>
				</div>
			  </div>
			  <div class="app-card">
				<div class="app-icon">
				  <img src="./Three/x.png" alt="DOGE icon" width="70" height="70">
				</div>
				<div class="app-info">
				  <div class="app-name">X</div>
				  <div class="link-container">
					  <a href="https://x.543x.com//">Website</a>
					  <span class="separator">•</span>
					  <a href="https://app.meteora.ag/pools/2onAYHGyxUV4JuYeUQbFwbKmKUXyTA9v5aKiGx2TesR7">Swap</a>
				  </div>
				  <a href="https://x.543x.com/" class="learn-more">Learn more</a>
				</div>
			  </div>
			  <div class="app-card">
				<div class="app-icon">
				  <img src="./Three/spaces.png" alt="DOGE icon" width="70" height="70">
				</div>
				<div class="app-info">
				  <div class="app-name">SHEEP</div>
				  <div class="link-container">
					  <a href="https://sheep.543x.com/">Website</a>
					  <span class="separator">•</span>
					  <a href="https://app.meteora.ag/pools/GYJkxTb1WLQELBFCXgLxPACuKA1Abd3bJFPKrEPsG5m9">Swap</a>
				  </div>
				  <a href="https://sheep.543x.com/" class="learn-more">Learn more</a>
				</div>
			  </div>
			  <div class="app-card">
				<div class="app-icon">
				  <img src="./Three/dine.png" alt="DOGE icon" width="70" height="70">
				</div>
				<div class="app-info">
				  <div class="app-name">PEACE</div>
				  <div class="link-container">
					  <a href="https://peace.543x.com/">Website</a>
					  <span class="separator">•</span>
					  <a href="https://app.meteora.ag/pools/6YwbhVxL5DBArRaC2rSsS738wjdzTzEzPSZDwRnRSnHX">Swap</a>
				  </div>
				  <a href="https://peace.543x.com/" class="learn-more">Learn more</a>
				</div>
			  </div>
			  <div class="app-card">
				<div class="app-icon">
				  <img src="./Three/fit.png" alt="DOGE icon" width="70" height="70">
				</div>
				<div class="app-info">
				  <div class="app-name">XRP</div>
				  <div class="link-container">
					  <a href="https://xrp.543x.com/">Website</a>
					  <span class="separator">•</span>
					  <a href="https://accounts.binance.com/en/register?ref=11131007">Swap</a>
				  </div>
				  <a href="https://xrp.543x.com/" class="learn-more">Learn more</a>
				</div>
			  </div>
			  <div class="app-card">
				<div class="app-icon">
				  <img src="./Three/owner.png" alt="DOGE icon" width="70" height="70">
				</div>
				<div class="app-info">
				  <div class="app-name">RATS</div>
				  <div class="link-container">
					  <a href="http://rats.543x.com/">Website</a>
					  <span class="separator">•</span>
					  <a href="https://accounts.binance.com/en/register?ref=11131007">Swap</a>
				  </div>
				  <a href="http://rats.543x.com/" class="learn-more">Learn more</a>
				</div>
			  </div>
			  <div class="app-card">
				<div class="app-icon">
				  <img src="./Three/cow.png" alt="DOGE icon" width="70" height="70">
				</div>
				<div class="app-info">
				  <div class="app-name">cow</div>
				  <div class="link-container">
					  <a href="https://cow.543x.com/">Website</a>
					  <span class="separator">•</span>
					  <a href="https://app.meteora.ag/pools/GHNBzjJe12m37Jj9JV4Jz6cunA34oCbXcgudCocPMJ4H">Swap</a>
				  </div>
				  <a href="https://cow.543x.com/" class="learn-more">Learn more</a>
				</div>
			  </div>
			  <div class="app-card">
				<div class="app-icon">
				  <img src="./Three/puma.png" alt="DOGE icon" width="70" height="70">
				</div>
				<div class="app-info">
				  <div class="app-name">DOGE</div>
				  <div class="link-container">
					  <a href="http://doge.543x.com/">Website</a>
					  <span class="separator">•</span>
					  <a href="https://app.meteora.ag/pools/vVTYpKUvcZHr5EJJKRefamq7u8W8eDjz7gqERAvga3R">Swap</a>
				  </div>
				  <a href="http://doge.543x.com/" class="learn-more">Learn more</a>
				</div>
			  </div>
			  <div class="app-card">
				<div class="app-icon">
				  <img src="./Three/dave.png" alt="DOGE icon" width="70" height="70">
				</div>
				<div class="app-info">
				  <div class="app-name">AVAX</div>
				  <div class="link-container">
					  <a href="http://cat.543x.com/">Website</a>
					  <span class="separator">•</span>
					  <a href="https://accounts.binance.com/en/register?ref=11131007">Swap</a>
				  </div>
				  <a href="https://www.543x.com/" class="learn-more">Learn more</a>
				</div>
			  </div>
			  <div class="app-card">
				<div class="app-icon">
				  <img src="./Three/discord.png" alt="DOGE icon" width="70" height="70">
				</div>
				<div class="app-info">
				  <div class="app-name">DONALD</div>
				  <div class="link-container">
					  <a href="https://donald.543x.com/">Website</a>
					  <span class="separator">•</span>
					  <a href="https://app.meteora.ag/pools/6Ed7Gy1aKNrvSr7srCJWowaLSEjCySmeRWK2iacEPCmw">Swap</a>
				  </div>
				  <a href="https://donald.543x.com/" class="learn-more">Learn more</a>
				</div>
			  </div>
			  <div class="app-card">
				<div class="app-icon">
				  <img src="./Three/tesla.png" alt="DOGE icon" width="70" height="70">
				</div>
				<div class="app-info">
				  <div class="app-name">SNAKE</div>
				  <div class="link-container">
					  <a href="https://snake.543x.com/">Website</a>
					  <span class="separator">•</span>
					  <a href="https://app.meteora.ag/pools/6YwbhVxL5DBArRaC2rSsS738wjdzTzEzPSZDwRnRSnHX">Swap</a>
				  </div>
				  <a href="https://snake.543x.com/" class="learn-more">Learn more</a>
				</div>
			  </div>
			  <div class="app-card">
				<div class="app-icon">
				  <img src="./Three/pinterest.png" alt="DOGE icon" width="70" height="70">
				</div>
				<div class="app-info">
				  <div class="app-name">RABBIT</div>
				  <div class="link-container">
					  <a href="https://rabbit.543x.com/">Website</a>
					  <span class="separator">•</span>
					  <a href="https://app.meteora.ag/pools/FbrPuX8tinmx2yxwxmYGZfZQbkS8FL9gG1dzQiWMamER">Swap</a>
				  </div>
				  <a href="https://rabbit.543x.com/" class="learn-more">Learn more</a>
				</div>
			  </div>
			  <div class="app-card">
				<div class="app-icon">
				  <img src="./Three/mercari.png" alt="DOGE icon" width="70" height="70">
				</div>
				<div class="app-info">
				  <div class="app-name">YY</div>
				  <div class="link-container">
					  <a href="http://yy.543x.com/">Website</a>
					  <span class="separator">•</span>
					  <a href="https://app.meteora.ag/pools/HGxSXTJhw1vGYhhCjjqSdBbwmG4cgFpJwjXK578Qz3Ms">Swap</a>
				  </div>
				  <a href="http://yy.543x.com/" class="learn-more">Learn more</a>
				</div>
			  </div>
			  <div class="app-card">
				<div class="app-icon">
				  <img src="./Three/playstation.png" alt="DOGE icon" width="70" height="70">
				</div>
				<div class="app-info">
				  <div class="app-name">GF</div>
				  <div class="link-container">
					  <a href="http://gf.543x.com/">Website</a>
					  <span class="separator">•</span>
					  <a href="https://app.meteora.ag/pools/5zz1MnzBxhozPoGDGysdu4CeeMEVeJ1cay8gpgw6Motb">Swap</a>
				  </div>
				  <a href="http://gf.543x.com/" class="learn-more">Learn more</a>
				</div>
			  </div>
			  <div class="app-card">
				<div class="app-icon">
				  <img src="./Three/openvpn.png" alt="DOGE icon" width="70" height="70">
				</div>
				<div class="app-info">
				  <div class="app-name">YAYA</div>
				  <div class="link-container">
					  <a href="https://yaya.543x.com/">Website</a>
					  <span class="separator">•</span>
					  <a href="https://app.meteora.ag/pools/Di9aeHFYeczWysnQsbNpxFgqTzJYyU9pKCovSdrhFXHQ">Swap</a>
				  </div>
				  <a href="https://yaya.543x.com/" class="learn-more">Learn more</a>
				</div>
			  </div>
			  <div class="app-card">
				<div class="app-icon">
				  <img src="./Three/tableau.png" alt="DOGE icon" width="70" height="70">
				</div>
				<div class="app-info">
				  <div class="app-name">ORD</div>
				  <div class="link-container">
					  <a href="http://ord.543x.com/">Website</a>
					  <span class="separator">•</span>
					  <a href="https://app.meteora.ag/pools/6u1nMUVkTVmSvvdjvVTJUPKP7ZoFLrbah3YtFnTa9YoA">Swap</a>
				  </div>
				  <a href="http://ord.543x.com/" class="learn-more">Learn more</a>
				</div>
			  </div>
			  <div class="app-card">
				<div class="app-icon">
				  <img src="./Three/wordpress.png" alt="DOGE icon" width="70" height="70">
				</div>
				<div class="app-info">
				  <div class="app-name">CAT</div>
				  <div class="link-container">
					  <a href="http://cat.543x.com/">Website</a>
					  <span class="separator">•</span>
					  <a href="https://app.meteora.ag/pools/9oRdiNMEPegLEmczr55zhTygRymQn44D7Ry5Cduj4VXv">Swap</a>
				  </div>
				  <a href="http://cat.543x.com/" class="learn-more">Learn more</a>
				</div>
			  </div>
			  <div class="app-card">
				<div class="app-icon">
				  <img src="./Three/flipkart.png" alt="DOGE icon" width="70" height="70">
				</div>
				<div class="app-info">
				  <div class="app-name">QQ</div>
				  <div class="link-container">
					  <a href="http://qq.543x.com/">Website</a>
					  <span class="separator">•</span>
					  <a href="https://app.meteora.ag/pools/83fGy9Fgm83CA44DU8NmhLfF2Bjq8v6dqsLcQN6NRDwm">Swap</a>
				  </div>
				  <a href="http://qq.543x.com/" class="learn-more">Learn more</a>
				</div>
			  </div>
			  <div class="app-card">
				<div class="app-icon">
				  <img src="./Three/bloomberg.png" alt="DOGE icon" width="70" height="70">
				</div>
				<div class="app-info">
				  <div class="app-name">MIMI</div>
				  <div class="link-container">
					  <a href="https://mimi.543x.com/">Website</a>
					  <span class="separator">•</span>
					  <a href="https://app.meteora.ag/pools/6Ed7Gy1aKNrvSr7srCJWowaLSEjCySmeRWK2iacEPCmw">Swap</a>
				  </div>
				  <a href="https://mimi.543x.com/" class="learn-more">Learn more</a>
				</div>
			  </div>
			  <div class="app-card">
				<div class="app-icon">
				  <img src="./Three/walmart.png" alt="DOGE icon" width="70" height="70">
				</div>
				<div class="app-info">
				  <div class="app-name">RAT</div>
				  <div class="link-container">
					  <a href="https://rat.543x.com/">Website</a>
					  <span class="separator">•</span>
					  <a href="https://app.meteora.ag/pools/AEgbTbDjXX6PYgQ6DdxCmF185hSwECueVyyFg2HsXNdo">Swap</a>
				  </div>
				  <a href="https://rat.543x.com/" class="learn-more">Learn more</a>
				</div>
			  </div>
			  <div class="app-card">
				<div class="app-icon">
				  <img src="./Three/baidu.png" alt="DOGE icon" width="70" height="70">
				</div>
				<div class="app-info">
				  <div class="app-name">monkey</div>
				  <div class="link-container">
					  <a href="https://monkey.543x.com/">Website</a>
					  <span class="separator">•</span>
					  <a href="https://app.meteora.ag/pools/6JZ53cKczUmwAqz8F59TZ7ur84AjAgLFWqWNauhsdhFY">Swap</a>
				  </div>
				  <a href="https://monkey.543x.com/" class="learn-more">Learn more</a>
				</div>
			  </div>
			  <div class="app-card">
				<div class="app-icon">
				  <img src="./Three/callofduty_companion.png" alt="DOGE icon" width="70" height="70">
				</div>
				<div class="app-info">
				  <div class="app-name">SEAL</div>
				  <div class="link-container">
					  <a href="https://seal.543x.com/">Website</a>
					  <span class="separator">•</span>
					  <a href="https://app.meteora.ag/pools/GbCVRoqC57eKEdgWo3oBkgtX64Ru7d7Evow5oxNKDWdW">Swap</a>
				  </div>
				  <a href="https://seal.543x.com/" class="learn-more">Learn more</a>
				</div>
			  </div>
			  <div class="app-card">
				<div class="app-icon">
				  <img src="./Three/Chicken.png" alt="DOGE icon" width="70" height="70">
				</div>
				<div class="app-info">
				  <div class="app-name">Chicken</div>
				  <div class="link-container">
					  <a href="https://ord.543x.com/">Website</a>
					  <span class="separator">•</span>
					  <a href="https://app.meteora.ag/pools/6u1nMUVkTVmSvvdjvVTJUPKP7ZoFLrbah3YtFnTa9YoA">Swap</a>
				  </div>
				  <a href="https://ord.543x.com/" class="learn-more">Learn more</a>
				</div>
			  </div>
			  <div class="app-card">
				<div class="app-icon">
				  <img src="./Three/words2.png" alt="DOGE icon" width="70" height="70">
				</div>
				<div class="app-info">
				  <div class="app-name">dragon</div>
				  <div class="link-container">
					  <a href="https://dragon.543x.com/">Website</a>
					  <span class="separator">•</span>
					  <a href="https://app.meteora.ag/pools/95TETWfUrkUnM6sCSizsQTDJ2tHXBXRZA6mEnjGfpgCb">Swap</a>
				  </div>
				  <a href="https://dragon.543x.com/" class="learn-more">Learn more</a>
				</div>
			  </div>
			  <div class="app-card">
				<div class="app-icon">
				  <img src="./Three/foreca.png" alt="DOGE icon" width="70" height="70">
				</div>
				<div class="app-info">
				  <div class="app-name">TRON</div>
				  <div class="link-container">
					  <a href="https://seal.543x.com/">Website</a>
					  <span class="separator">•</span>
					  <a href="https://app.meteora.ag/pools/GbCVRoqC57eKEdgWo3oBkgtX64Ru7d7Evow5oxNKDWdW">Swap</a>
				  </div>
				  <a href="https://seal.543x.com/" class="learn-more">Learn more</a>
				</div>
			  </div>
			  <div class="app-card">
				<div class="app-icon">
				  <img src="./Three/nerdwallet.png" alt="DOGE icon" width="70" height="70">
				</div>
				<div class="app-info">
				  <div class="app-name">ADA</div>
				  <div class="link-container">
					  <a href="http://ada.543x.com/">Website</a>
					  <span class="separator">•</span>
					  <a href="https://app.meteora.ag/pools/HGxSXTJhw1vGYhhCjjqSdBbwmG4cgFpJwjXK578Qz3Ms">Swap</a>
				  </div>
				  <a href="http://ada.543x.com/" class="learn-more">Learn more</a>
				</div>
			  </div>
			  <div class="app-card">
				<div class="app-icon">
				  <img src="./Three/lendmn.png" alt="DOGE icon" width="70" height="70">
				</div>
				<div class="app-info">
				  <div class="app-name">OTTER</div>
				  <div class="link-container">
					  <a href="https://otter.543x.com/">Website</a>
					  <span class="separator">•</span>
					  <a href="https://app.meteora.ag/pools/9XeEoYSMyG5tWpNKMBKivsbbjfjrPj2rFBQUEut3vDVu">Swap</a>
				  </div>
				  <a href="https://otter.543x.com/" class="learn-more">Learn more</a>
				</div>
			  </div>
			  <div class="app-card">
				<div class="app-icon">
				  <img src="./Three/artsy.png" alt="DOGE icon" width="70" height="70">
				</div>
				<div class="app-info">
				  <div class="app-name">pepe</div>
				  <div class="link-container">
					  <a href="https://pepe.543x.com/">Website</a>
					  <span class="separator">•</span>
					  <a href="https://app.meteora.ag/pools/eZ4L3WKdaCHWbocvuA5QhMvR3AwdmhpNfPW9ynHJGx6">Swap</a>
				  </div>
				  <a href="https://pepe.543x.com/" class="learn-more">Learn more</a>
				</div>
			  </div>
			  <div class="app-card">
				<div class="app-icon">
				  <img src="./Three/1831.png" alt="DOGE icon" width="70" height="70">
				</div>
				<div class="app-info">
				  <div class="app-name">BCH</div>
				  <div class="link-container">
					  <a href="http://bch.info/">Website</a>
					  <span class="separator">•</span>
					  <a href="https://app.meteora.ag/pools/JBdMRhuxAtMW754NceSMFPLnpPc2XAwgYZwXNUawSah5">Swap</a>
				  </div>
				  <a href="https://www.543x.com/" class="learn-more">Learn more</a>
				</div>
			  </div>
			  <div class="app-card">
				<div class="app-icon">
				  <img src="./Three/4195.png" alt="DOGE icon" width="70" height="70">
				</div>
				<div class="app-info">
				  <div class="app-name">FTX</div>
				  <div class="link-container">
					  <a href="https://www.543x.com/">Website</a>
					  <span class="separator">•</span>
					  <a href="https://app.meteora.ag/pools/JBdMRhuxAtMW754NceSMFPLnpPc2XAwgYZwXNUawSah5">Swap</a>
				  </div>
				  <a href="https://fdusd.543x.com/" class="learn-more">Learn more</a>
				</div>
			  </div>
		  </div>
		</div>
    </div>

  <SiteMap />
  <!-- <NewsLetter /> -->
</template>

<style scoped>
:root {
	color-scheme: light dark;

	--background-color: #fff;
	--secondary-background-color: #f7f7f7;

	--color-blue: #049EF4;
	--text-color: #444;
	--secondary-text-color: #9e9e9e;

	--font-size: 16px;
	--line-height: 26px;

	--border-style: 1px solid #E8E8E8;
	--header-height: 48px;
	--panel-width: 300px;
	--panel-padding: 16px;
	--icon-size: 20px;
}

@media (prefers-color-scheme: dark) {

	:root {
		--background-color: #222;
		--secondary-background-color: #2e2e2e;

		--text-color: #bbb;
		--secondary-text-color: #666;

		--border-style: 1px solid #444;
	}

	#previewsToggler {
		filter: invert(100%);
	}

}

@font-face {
	font-family: 'Roboto Mono';
	src: local('Roboto Mono'), local('RobotoMono-Regular'), url('../files/RobotoMono-Regular.woff2') format('woff2');
	font-style: normal;
	font-weight: 400;
}

@font-face {
	font-family: 'Roboto Mono';
	src: local('Roboto Mono Medium'), local('RobotoMono-Medium'), url('../files/RobotoMono-Medium.woff2') format('woff2');
	font-style: normal;
	font-weight: 500;
}
.link-container {
	display: flex;
	align-items: center;
	justify-content: center;
  }
  
  .separator {
	margin: 0 20px;
  }
  
  a {
	text-decoration: none;
  }
* {
	box-sizing: border-box;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
}

html, body {
	height: 100%;
}

html {
	font-size: calc(var(--font-size) - 1px);
	line-height: calc(var(--line-height) - 1px);
}

body {
	font-family: 'Roboto Mono', monospace;
	margin: 0px;
	color: var(--text-color);
	background-color: var(--background-color);
}

a {
	text-decoration: none;
}

h1 {
	font-size: 18px;
	line-height: 24px;
	font-weight: 500;
}

h2 {
	padding: 0;
	margin: 16px 0;
	font-size: calc(var(--font-size) - 1px);
	line-height: var(--line-height);
	font-weight: 500;
	color: var(--color-blue);
}

h3 {
	margin: 0;
	font-weight: 500;
	font-size: calc(var(--font-size) - 1px);
	line-height: var(--line-height);
	color: var(--secondary-text-color);
}

h1 a {
	color: var(--color-blue);
}
header {
	padding: 20px 0;
	background-color: #f5f5f5;
	border-bottom: 1px solid #e0e0e0;
  }
  
  h1 {
	font-family: Arial, sans-serif;
	font-size: 2.5rem;
	color: #333;
	display: flex;
	align-items: center;
	justify-content: center;
  }
  
  .logo {
	font-weight: bold;
	margin-right: 10px;
  }
  
  .version-link {
	font-size: 1rem;
	color: #0066cc;
	text-decoration: none;
	padding: 5px 10px;
	border-radius: 15px;
	background-color: #e6f2ff;
	transition: background-color 0.3s ease;
  }
  
  .version-link:hover {
	background-color: #cce5ff;
  }
#header {
	display: flex;
	height: var(--header-height);
	border-bottom: var(--border-style);
	align-items: center;
}
#header h1 {
	padding-left: var(--panel-padding);
	flex: 1;
	display: flex;
	align-items: center;
	color: var(--color-blue);
}
#header #version {
	border: 1px solid var(--color-blue);
	color: var(--color-blue);
	border-radius: 4px;
	line-height: 16px;
	padding: 0px 2px;
	margin-left: 6px;
	font-size: .9rem;
}
body {
	font-family: 'Roboto', Arial, sans-serif;
	margin: 0;
	padding: 0;
	background-color: #f0f2f5;
	color: #333;
	display: flex;
	min-height: 100vh;
  }
  
  
#viewer {
  flex: 1; /* 这已经足够使其填充剩余空间，但您可以明确设置宽度 */
  width: 100%; /* 显式设置宽度为100% */
  padding: 40px;
}

  
  h1, h2 {
	color: #1a1a1a;
	font-weight: 600;
  }
  
  ul {
	padding-left: 20px;
	list-style-type: none;
  }
  
  a {
	color: #3498db;
	text-decoration: none;
	transition: color 0.3s ease;
  }
  
  a:hover {
	color: #2980b9;
  }
  
  .container {
	max-width: 1200px;
	margin: 0 auto;
	background-color: white;
	padding: 30px;
	box-shadow: 0 0 20px rgba(0,0,0,0.05);
	border-radius: 12px;
  }
  
  .showcase {
	display: grid;
	grid-template-columns: repeat(auto-fill, minmax(220px, 1fr));
	gap: 25px;
  }
  
  .app-card {
	background-color: white;
	border: 1px solid #e0e0e0;
	border-radius: 12px;
	overflow: hidden;
	transition: all 0.3s ease;
	box-shadow: 0 4px 6px rgba(0,0,0,0.05);
  }
  
  .app-card:hover {
	transform: translateY(-5px);
	box-shadow: 0 8px 15px rgba(0,0,0,0.1);
  }
  
  .app-icon {
	width: 100%;
	height: 140px;
	display: flex;
	justify-content: center;
	align-items: center;
	background-color: #f9f9f9;
  }
  
  .app-icon img {
	max-width: 70px;
	max-height: 70px;
	transition: transform 0.3s ease;
  }
  
  .app-card:hover .app-icon img {
	transform: scale(1.1);
  }
  
  .app-info {
	padding: 15px;
	text-align: center;
  }
  
  .app-name {
	font-weight: 600;
	margin-bottom: 8px;
	font-size: 16px;
  }
  
  .app-links {
	font-size: 14px;
	color: #6c757d;
  }
  
  .app-links a {
	color: #3498db;
	font-weight: 500;
  }
  
  .learn-more {
	color: #6c757d;
	font-size: 13px;
	font-weight: 500;
	display: inline-block;
	margin-top: 10px;
	padding: 5px 10px;
	border: 1px solid #e0e0e0;
	border-radius: 20px;
	transition: all 0.3s ease;
  }
  
  .learn-more:hover {
	background-color: #3498db;
	color: white;
	border-color: #3498db;
  }
  
  .sectionContainer {
	text-align: center;
	padding: 40px 20px;
	color: #6c757d;
	border-radius: 12px 12px 0 0;
	margin-bottom: 30px;
  }
  
  .sectionContainer h1 {
	font-size: 2.5em;
	margin-bottom: 15px;
	color: #6c757d;
  }
  
  .formButton {
	display: inline-block;
	padding: 10px 20px;
	background-color: #2ecc71;
	color: white;
	border-radius: 25px;
	font-weight: bold;
	margin-top: 20px;
	transition: all 0.3s ease;
  }
  
  .formButton:hover {
	background-color: #27ae60;
	transform: translateY(-2px);
	box-shadow: 0 4px 8px rgba(0,0,0,0.2);
  }

section {
  padding: 42px 32px;
}

#hero {
  padding: 96px 32px;
  text-align: center;
}

.tagline {
  font-size: 76px;
  line-height: 1.25;
  font-weight: 900;
  letter-spacing: -1.5px;
  max-width: 960px;
  margin: 0px auto;
}

html:not(.dark) .accent,
.dark .tagline {
  background: -webkit-linear-gradient(315deg, #42d392 25%, #647eff);
  background-clip: text;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.description {
  max-width: 960px;
  line-height: 1.5;
  color: var(--vt-c-text-2);
  transition: color 0.5s;
  font-size: 22px;
  margin: 24px auto 40px;
}

.actions a {
  font-size: 16px;
  display: inline-block;
  background-color: var(--vt-c-bg-mute);
  padding: 8px 18px;
  font-weight: 500;
  border-radius: 8px;
  transition: background-color 0.5s, color 0.5s;
}

.actions .security {
  background: linear-gradient(var(--vt-c-bg-mute), var(--vt-c-bg-mute)) padding-box,
    linear-gradient(45deg, #42d392, #647eff) border-box;
  border: 2px solid transparent;
}

.actions .security:hover {
  background: linear-gradient(var(--vt-c-gray-light-4), var(--vt-c-gray-light-4)) padding-box,
    linear-gradient(45deg, #42d392, #647eff) border-box;
}

.dark .actions .security:hover {
  background: linear-gradient(var(--vt-c-gray-dark-3), var(--vt-c-gray-dark-3)) padding-box,
    linear-gradient(45deg, #42d392, #647eff) border-box;
}

.actions .security .icon {
  width: 12px;
  height: 12px;
  margin-left: 4px;
}

.actions .get-started,
.actions .setup {
  margin-right: 18px;
}

.actions .icon {
  display: inline;
  position: relative;
  top: -1px;
  margin-left: 2px;
  fill: currentColor;
  transition: transform 0.2s;
}

.actions .get-started:hover {
  transition-duration: 0.2s;
}

.actions .get-started:hover .icon {
  transform: translateX(2px);
}

.actions .get-started,
.actions .setup,
.actions .security {
  color: var(--vt-c-text-code);
}

.actions .get-started:hover,
.actions .setup:hover,
.actions .security:hover {
  background-color: var(--vt-c-gray-light-4);
  transition-duration: 0.2s;
}

.dark .actions .get-started:hover,
.dark .actions .setup:hover,
.dark .actions .security:hover {
  background-color: var(--vt-c-gray-dark-3);
}

#special-sponsor {
  border-top: 1px solid var(--vt-c-divider-light);
  border-bottom: 1px solid var(--vt-c-divider-light);
  padding: 12px 24px;
  display: flex;
  align-items: center;
}

#special-sponsor span {
  color: var(--vt-c-text-2);
  font-weight: 500;
  font-size: 13px;
  vertical-align: middle;
  flex: 1;
}

#special-sponsor span:first-child {
  text-align: right;
}

#special-sponsor a {
  display: flex;
  justify-content: center;
  padding: 0 24px;
}

#special-sponsor img {
  height: 42px;
  margin: -6px 0;
}

.dark #special-sponsor img {
  filter: grayscale(1) invert(1);
}

#highlights {
  max-width: 960px;
  margin: 0px auto;
  color: var(--vt-c-text-2);
}

#highlights h2 {
  font-weight: 600;
  font-size: 20px;
  letter-spacing: -0.4px;
  color: var(--vt-c-text-1);
  transition: color 0.5s;
  margin-bottom: 0.75em;
}

#highlights p {
  font-weight: 400;
  font-size: 15px;
}

#highlights .vt-box {
  background-color: transparent;
}

#sponsors {
  max-width: 900px;
  margin: 0px auto;
}

#sponsors h2 {
  font-size: 20px;
  font-weight: 600;
  margin-bottom: 1em;
}

#sponsors .sponsor-container {
  margin-bottom: 3em;
}

@media (max-width: 960px) {
  .tagline {
    font-size: 64px;
    letter-spacing: -0.5px;
  }
  .description {
    font-size: 18px;
    margin-bottom: 48px;
  }
}

@media (max-width: 794px) {
  .tagline {
    font-size: 48px;
    letter-spacing: -0.5px;
  }
  .actions .security {
    margin-top: 18px;
  }
}

@media (max-width: 576px) {
  #hero {
    padding: 56px 32px;
  }
  .description {
    font-size: 16px;
    margin: 18px 0 30px;
  }
  #special-sponsor {
    flex-direction: column;
  }
  #special-sponsor img {
    height: 36px;
    margin: 8px 0;
  }
  #special-sponsor span {
    text-align: center !important;
  }
  #highlights h3 {
    margin-bottom: 0.6em;
  }
  #highlights .vt-box {
    padding: 20px 36px;
  }
  .actions a {
    margin: 18px 0;
  }
  .actions .security {
    margin-top: 0;
  }
}

@media (max-width: 370px) {
  .tagline {
    font-size: 36px;
  }
}

#uwu {
  display: none;
}

.uwu #uwu {
  display: block;
  width: 100%;
  max-width: 720px;
  margin: -120px auto -20px;
  aspect-ratio: 192 / 108;
  content: url(/logo-uwu.png);
}

@media (max-width: 576px) {
  .uwu #uwu {
    margin: -60px auto -10px;
  }
}
</style>
