# leeao.net_html
<!doctype html>
<html lang="zh-CN">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width,initial-scale=1">
  <title>数位情治</title>
  <style>
    .leeao-buttons {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(180px, 1fr));
      gap: 12px;
    }
    .leeao-buttons .leeao-btn {
      padding: 10px 16px;
      border-radius: 12px;
      border: none;
      font-weight: 600;
      font-family: inherit;
      cursor: pointer;
      text-align: center;
      background: linear-gradient(180deg, #fff, #f6f8ff);
      color: #000;
      box-shadow: 0 2px 6px rgba(0,0,0,0.1);
      transition: all 0.3s ease;
    }
    .leeao-buttons .leeao-btn.primary {
      background: linear-gradient(135deg, #4f8ef7, #2b7cff);
      color: #fff;
      box-shadow: 0 4px 12px rgba(43,124,255,0.3);
    }
    .leeao-buttons .leeao-btn.primary:hover {
      box-shadow: 0 6px 20px rgba(43,124,255,0.6);
      transform: translateY(-2px);
    }
    .leeao-buttons .leeao-btn.primary:active {
      transform: scale(0.97);
      box-shadow: 0 4px 12px rgba(43,124,255,0.4);
    }
    .leeao-buttons .leeao-btn:hover {
      opacity: 0.85;
      transform: translateY(-2px);
    }
    .leeao-buttons .leeao-btn:active {
      transform: scale(0.97);
    }
    @media (max-width: 480px) {
      .leeao-buttons {
        grid-template-columns: repeat(2, 1fr);
      }
    }
    .leeao-modal-bg {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: rgba(0, 0, 0, 0.5);
      display: none;
      align-items: center;
      justify-content: center;
      z-index: 1000;
    }
    .leeao-modal {
      background: #fff;
      border-radius: 10px;
      padding: 20px;
      max-width: 600px;
      width: 90%;
      text-align: center;
    }
    .leeao-modal .images {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 10px;
      margin: 10px 0;
    }
    .leeao-modal img {
      max-width: 45%;
      height: auto;
      border-radius: 8px;
      border: 1px solid #ddd;
    }
    .leeao-close {
      margin-top: 10px;
      padding: 6px 12px;
      border: none;
      background: #2b7cff;
      color: #fff;
      border-radius: 6px;
      cursor: pointer;
    }
  </style>
</head>
<body>
  <div class="leeao-buttons">
    <button class="leeao-btn primary" id="btn-index">李敖其他网站索引</button>
    <button class="leeao-btn" id="btn-qq">加入QQ微信群</button>
    <button class="leeao-btn" id="btn-download">下载站</button>
    <button class="leeao-btn" id="btn-pass">查看登录密码</button>
  </div>

  <div class="leeao-modal-bg" id="leeaoModal">
    <div class="leeao-modal">
      <h3>加入 QQ / 微信 群</h3>
      <div class="images">
        <img src="http://tw.leeao.net:5212/f/lEiw/QQ.jpg" alt="QQ 群二维码">
        <img src="http://tw.leeao.net:5212/f/8Kh6/WX.jpg" alt="微信 群二维码">
      </div>
      <button class="leeao-close" id="leeaoClose">关闭</button>
    </div>
  </div>

  <script>
    const btnIndex = document.getElementById('btn-index');
    const btnQQ = document.getElementById('btn-qq');
    const btnDownload = document.getElementById('btn-download');
    const btnPass = document.getElementById('btn-pass');
    const modal = document.getElementById('leeaoModal');
    const closeBtn = document.getElementById('leeaoClose');

    btnIndex.addEventListener('click', () => window.open('https://leeaoweb.com/', '_blank'));
    btnDownload.addEventListener('click', () => window.open('https://download.leeao.net/', '_blank'));
    btnQQ.addEventListener('click', () => { modal.style.display = 'flex'; });
    closeBtn.addEventListener('click', () => { modal.style.display = 'none'; });
    modal.addEventListener('click', (e) => { if (e.target === modal) modal.style.display = 'none'; });
    btnPass.addEventListener('click', () => { alert('账号：李敖\n密码：1935'); });
  </script>
</body>
</html>
