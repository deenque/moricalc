<!DOCTYPE html>
<html lang="ru">
<head>
  <!-- === МЕТАДАННЫЕ === -->
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no, viewport-fit=cover" />
  <title>$MORI COIN Калькулятор</title>
  <!-- === TELEGRAM WEBAPP === -->
  <script src="https://telegram.org/js/telegram-web-app.js"></script>
  <!-- === ИКОНКИ И ФАВИКОН === -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" />
  <link rel="icon" href="https://moristake.in/images/favicon.ico" type="image/x-icon" />
  <!-- === ШРИФТ === -->
  <style>
    @font-face {
      font-family: 'TT Firs Neue';
      src: url('https://moristake.in/fonts/TTFirsNeue-Regular.ttf') format('truetype');
      font-display: swap;
    }
    * { margin: 0; padding: 0; box-sizing: border-box; }
    html, body {
      width: 100%; height: 100%; overflow: hidden;
      background: radial-gradient(circle at 50% 50%, #1b1a12 0%, #000 100%);
      color: #fff; font-family: 'TT Firs Neue', sans-serif;
    }
    body {
      display: flex; justify-content: center; align-items: center;
      position: fixed; inset: 0;
      padding: env(safe-area-inset-top) env(safe-area-inset-right) env(safe-area-inset-bottom) env(safe-area-inset-left);
      min-height: 100dvh;
    }
    .calculator {
      backdrop-filter: blur(20px) saturate(180%);
      background: rgba(255,255,255,.08);
      border: 1px solid rgba(255,255,255,.18);
      border-radius: 24px;
      box-shadow: 0 8px 32px rgba(255,213,0,.2);
      padding: 24px 20px;
      width: 100%; max-width: 380px;
      z-index: 2; position: relative; margin: 0 auto;
    }
    h2 {
      text-align: center; margin-bottom: 4px;
      color: #FFD500; font-weight: 600; font-size: 20px; line-height: 1.2;
    }
    .subtitle {
      text-align: center; color: rgba(255,255,255,.7);
      font-size: 13px; margin-bottom: 16px;
    }
    .currency-toggle {
      display: flex; justify-content: center; gap: 8px; margin-bottom: 18px;
    }
    .currency-toggle button {
      flex: 1; display: flex; align-items: center; justify-content: center; gap: 6px;
      background: rgba(255,255,255,.07); border-radius: 12px; padding: 8px 0;
      border: 1px solid rgba(255,255,255,.1); color: #fff; font-size: 13px;
      transition: all .3s; cursor: pointer;
    }
    .currency-toggle button.active {
      color: #FFD500; font-weight: 600;
      background: rgba(255,213,0,.15); border-color: #FFD500;
    }
    .currency-toggle button img {
      width: 18px; height: 12px; border-radius: 2px;
    }
    .input-group { margin-bottom: 16px; }
    label {
      font-size: 13px; color: rgba(255,255,255,.7);
      display: block; margin-bottom: 6px;
    }
    .token-input, .price-input {
      width: 100%; padding: 12px 14px; border-radius: 12px; border: none; outline: none;
      font-size: 15px; text-align: center; background: rgba(255,255,255,.1); color: #fff;
      min-height: 48px;
    }
    .price-input { width: 130px; padding: 12px 8px; flex-shrink: 0; }
    .token-input::placeholder, .price-input::placeholder { color: rgba(255,255,255,.4); }
    .price-row { display: flex; align-items: center; gap: 8px; }
    .price-btn {
      flex: 1; background: rgba(255,255,255,.1); border: 1px solid rgba(255,255,255,.3);
      border-radius: 10px; padding: 8px 10px; color: #FFD500; font-size: 12px;
      white-space: nowrap; cursor: pointer; transition: .3s; text-align: center;
      overflow: hidden; text-overflow: ellipsis;
    }
    .price-btn:hover, .price-btn:active { background: rgba(255,255,255,.2); }
    .comment {
      text-align: center; font-size: 12px; color: rgba(255,255,255,.6); margin-top: 18px;
    }
    .btn {
      width: 100%; background: linear-gradient(135deg, #FFD500, #BFA100);
      border: none; border-radius: 12px; padding: 14px; font-size: 16px;
      color: #000; font-weight: 600; cursor: pointer; transition: all .3s;
      min-height: 52px; margin-top: 8px; font-family: 'TT Firs Neue', sans-serif;
    }
    .btn:hover, .btn:active { transform: translateY(-1px); box-shadow: 0 0 20px rgba(255,213,0,.4); }
    .btn:disabled { opacity: 0.6; cursor: not-allowed; transform: none; }
    .results {
      display: none; margin-top: 16px; text-align: center;
      opacity: 0; transition: opacity .5s ease;
    }
    .results p {
      margin: 4px 0; font-size: 15px; line-height: 1.3; color: rgba(255,255,255,0.7);
    }
    .highlight {
      background: linear-gradient(90deg, #FFD500, #FFB800);
      -webkit-background-clip: text; -webkit-text-fill-color: transparent;
      font-weight: 700; font-size: 17px;
    }
    .course-info {
      font-size: 11px; color: rgba(255,255,255,.6);
      text-align: center; margin-top: 12px;
    }
    .course-error { color: #ff6b6b; }
  </style>
</head>
<body>
  <div class="calculator">
    <h2>Калькулятор $MORI</h2>
    <p class="subtitle">(с прогнозом дохода)</p>
    <div class="currency-toggle">
      <button id="btnUSD" class="active">
        <img src="https://upload.wikimedia.org/wikipedia/en/a/a4/Flag_of_the_United_States.svg" alt="USD"> USD
      </button>
      <button id="btnRUB">
        <img src="https://upload.wikimedia.org/wikipedia/en/f/f3/Flag_of_Russia.svg" alt="RUB"> RUB
      </button>
    </div>
    <div class="input-group">
      <label for="tokenAmount">Количество ваших токенов:</label>
      <input type="text" id="tokenAmount" class="token-input" placeholder="Например: 1000">
    </div>
    <div class="input-group">
      <label for="tokenPrice">Желаемая цена $MORI</label>
      <div class="price-row">
        <input type="text" step="0.001" id="tokenPrice" class="price-input" placeholder="0,00">
        <div class="price-btn" id="priceBtn">Текущая цена</div>
      </div>
      <div class="comment">Цена 1 MORI в выбранной валюте</div>
      <p style="font-size:12px; color:rgba(255,255,255,0.6); margin:4px 0 0; text-align:center; line-height:1.2;">
        (выберите валюту, нажав на кнопку RUB или USD)
      </p>
    </div>
    <button class="btn" id="calcBtn" disabled>Рассчитать</button>
    <div class="course-info" id="courseInfo">
      Курс USD/RUB: <span id="courseStatus">Загрузка...</span>
    </div>
    <div class="results" id="resultsBlock">
      <div id="resultPrimary"></div>
      <div id="resultSecondary"></div>
    </div>
  </div>

  <!-- === MONEY.JS + ДАННЫЕ ЦБ РФ === -->
  <script src="https://www.cbr-xml-daily.ru/money.js"></script>

  <script>
    Telegram.WebApp.ready();
    Telegram.WebApp.expand();

    const btnUSD = document.getElementById('btnUSD');
    const btnRUB = document.getElementById('btnRUB');
    const priceBtn = document.getElementById('priceBtn');
    const calcBtn = document.getElementById('calcBtn');
    const resultsBlock = document.getElementById('resultsBlock');
    const resultPrimary = document.getElementById('resultPrimary');
    const resultSecondary = document.getElementById('resultSecondary');
    const courseStatus = document.getElementById('courseStatus');
    const tokenPriceInput = document.getElementById('tokenPrice');

    let currentCurrency = 'USD';
    let priceUSD = 0;
    let priceRUB = 0;
    let usdToRub = null;
    let userHasEditedPrice = false;

    tokenPriceInput.addEventListener('input', () => {
      userHasEditedPrice = true;
    });

   // === КУРС ИЗ ЦБ РФ (money.js) ===
function updateCourseFromCBR() {
  if (typeof fx === 'undefined' || !fx.rates || !fx.rates.USD) {
    courseStatus.textContent = 'Ошибка загрузки курса';
    courseStatus.className = 'course-error';
    calcBtn.disabled = true;
    setTimeout(updateCourseFromCBR, 3000);
    return;
  }

  usdToRub = 1 / fx.rates.USD; // КЛЮЧЕВАЯ СТРОКА
  const date = new Date().toLocaleDateString('ru-RU');
  courseStatus.innerHTML = `${usdToRub.toFixed(2)} <small>(ЦБ РФ, ${date})</small>`;
  courseStatus.className = '';
  calcBtn.disabled = false;
  updatePriceBtn();
}

// Запуск
if (typeof fx !== 'undefined' && fx.rates) {
  updateCourseFromCBR();
} else {
  window.addEventListener('load', () => setTimeout(updateCourseFromCBR, 500));
}
    // Ждём загрузки money.js
    if (typeof fx !== 'undefined' && fx.rates) {
      updateCourseFromCBR();
    } else {
      // Если скрипт ещё не загрузился
      window.addEventListener('load', () => {
        setTimeout(updateCourseFromCBR, 500);
      });
    }

    // Обновление раз в сутки (можно оставить, но не обязательно)
    setInterval(updateCourseFromCBR, 86400000);

    // === ЦЕНА $MORI (оставляем Jupiter или CoinGecko — на твой выбор) ===
    async function fetchMoriPrice() {
      try {
        const res = await fetch('https://api.coingecko.com/api/v3/simple/price?ids=mori-coin&vs_currencies=usd,rub');
        const data = await res.json();
        const mori = data['mori-coin'] || data['mori_coin'];
        if (mori) {
          priceUSD = mori.usd || 0;
          priceRUB = mori.rub || (mori.usd * usdToRub) || 0;
          updatePriceBtn();
        }
      } catch (e) {
        console.log('Coingecko:', e);
      }
    }

    function updatePriceBtn() {
      if (!usdToRub) return;
      let displayPrice;
      let decimals;
      if (currentCurrency === 'USD') {
        displayPrice = priceUSD;
        decimals = 6;
      } else {
        displayPrice = priceUSD * usdToRub;
        decimals = 2;
      }
      priceBtn.textContent = `Текущая: ${displayPrice ? displayPrice.toFixed(decimals) : '—'} ${currentCurrency === 'USD' ? '$' : '₽'}`;
      if (!userHasEditedPrice && displayPrice) {
        tokenPriceInput.value = displayPrice.toFixed(decimals);
      }
      priceBtn.onclick = () => {
        if (displayPrice) {
          tokenPriceInput.value = displayPrice.toFixed(decimals);
          userHasEditedPrice = true;
        }
      };
    }

    fetchMoriPrice();
    setInterval(fetchMoriPrice, 60000);

    // === ПЕРЕКЛЮЧЕНИЕ ВАЛЮТ ===
    btnUSD.onclick = () => {
      if (currentCurrency === 'USD') return;
      currentCurrency = 'USD';
      btnUSD.classList.add('active');
      btnRUB.classList.remove('active');
      updatePriceBtn();
    };
    btnRUB.onclick = () => {
      if (currentCurrency === 'RUB') return;
      currentCurrency = 'RUB';
      btnRUB.classList.add('active');
      btnUSD.classList.remove('active');
      updatePriceBtn();
    };

    // === РАСЧЁТ ===
    calcBtn.onclick = () => {
      if (!usdToRub) {
        alert('Курс не загружен. Подождите или обновите страницу.');
        return;
      }
      const amount = parseFloat(document.getElementById('tokenAmount').value.replace(',', '.')) || 0;
      const inputPrice = parseFloat(tokenPriceInput.value.replace(',', '.'));
      let priceInUSD;
      if (currentCurrency === 'USD') {
        priceInUSD = inputPrice || priceUSD;
      } else {
        priceInUSD = (inputPrice || (priceUSD * usdToRub)) / usdToRub;
      }
      if (amount <= 0 || priceInUSD <= 0) {
        alert('Введите корректные данные');
        return;
      }
      const totalUSD = amount * priceInUSD;
      const totalRUB = totalUSD * usdToRub;
      const usdStr = totalUSD.toLocaleString('ru-RU', { maximumFractionDigits: 2 }) + ' $';
      const rubStr = totalRUB.toLocaleString('ru-RU', { maximumFractionDigits: 0 }) + ' ₽';

      resultsBlock.style.display = 'block';
      resultsBlock.style.opacity = 0;
      setTimeout(() => resultsBlock.style.opacity = 1, 50);

      if (currentCurrency === 'USD') {
        resultPrimary.innerHTML = `<p>Стоимость в USD: <strong class="highlight">${usdStr}</strong></p>`;
        resultSecondary.innerHTML = `<p>Стоимость в RUB: <strong class="highlight">${rubStr}</strong></p>`;
      } else {
        resultPrimary.innerHTML = `<p>Стоимость в RUB: <strong class="highlight">${rubStr}</strong></p>`;
        resultSecondary.innerHTML = `<p>Стоимость в USD: <strong class="highlight">${usdStr}</strong></p>`;
      }
    };
  </script>
</body>
</html>
