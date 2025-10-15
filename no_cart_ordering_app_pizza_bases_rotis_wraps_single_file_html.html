<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>No‑Cart Ordering — Pizza Bases, Rotis, Wraps</title>
  <style>
    :root{--bg:#f6f7fb;--card:#fff;--text:#1f2937;--muted:#6b7280;--brand:#0ea5e9;--line:#e5e7eb}
    *{box-sizing:border-box}
    body{margin:0;font-family:system-ui,-apple-system,Segoe UI,Roboto,Ubuntu,"Helvetica Neue",Arial,sans-serif;background:linear-gradient(#ffffff,var(--bg));color:var(--text)}
    header,footer{background:#fff;border-bottom:1px solid var(--line)}
    footer{border-top:1px solid var(--line);border-bottom:none}
    .wrap{max-width:1100px;margin:0 auto;padding:16px}
    .brand{display:flex;align-items:center;gap:12px}
    .logo{width:40px;height:40px;border-radius:12px;background:var(--brand)}
    h1{font-size:20px;margin:0}
    .tabs{display:flex;gap:8px;background:#fff;border:1px solid var(--line);padding:6px;border-radius:14px;position:sticky;top:64px;z-index:10}
    .tab{padding:8px 14px;border:1px solid var(--line);background:#fff;border-radius:10px;font-weight:600;cursor:pointer}
    .tab.active{background:var(--brand);color:#fff;border-color:var(--brand)}
    .grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(250px,1fr));gap:14px}
    .card{background:var(--card);border:1px solid var(--line);border-radius:16px;padding:14px;box-shadow:0 1px 2px rgba(0,0,0,.03)}
    .card h3{margin:0 0 6px 0;font-size:16px}
    .muted{color:var(--muted);font-size:13px}
    .panel{background:#fff;border:1px solid var(--line);border-radius:16px;padding:14px}
    .two{display:grid;grid-template-columns:1fr 1fr;gap:8px}
    input,select{width:100%;padding:10px;border:1px solid var(--line);border-radius:10px}
    .qty{display:flex;align-items:center;gap:6px;margin-top:8px}
    .qty input{width:90px;text-align:center}
    .btn{border:1px solid var(--line);background:#fff;border-radius:10px;padding:10px 12px;cursor:pointer;font-weight:600}
    .btn.primary{background:var(--brand);border-color:var(--brand);color:#fff}
    .price{font-weight:700}
    .img{width:100%;height:160px;border-radius:12px;background:linear-gradient(135deg,#f3f4f6,#e5e7eb);display:flex;align-items:center;justify-content:center;color:#475569;font-weight:800;letter-spacing:.08em;margin-bottom:8px}
  </style>
</head>
<body>
  <header>
    <div class="wrap" style="display:flex;align-items:center;justify-content:space-between;height:64px">
      <div class="brand">
        <div class="logo"></div>
        <div>
          <h1>QuickBite — Order Bases</h1>
          <div class="muted" style="margin-top:-2px">Pizza Bases • Rotis • Wraps (collection only)</div>
        </div>
      </div>
    </div>
  </header>

  <main class="wrap" style="margin-top:12px">
    <!-- Customer details included in the outgoing message -->
    <section class="panel" style="margin-bottom:12px">
      <h2 style="margin:0 0 8px 0;font-size:18px">Your Details</h2>
      <div class="two">
        <input id="custName" placeholder="Your name (optional)" />
        <input id="custPhone" placeholder="Your phone (optional)" />
      </div>
      <div class="muted" style="margin-top:6px">Orders are for <b>collection</b> and payment is <b>on collection</b>.</div>
    </section>

    <div class="tabs" id="tabs">
      <button class="tab active" data-tab="pizzas">Pizza Bases</button>
      <button class="tab" data-tab="rotis">Rotis</button>
      <button class="tab" data-tab="wraps">Wraps</button>
    </div>

    <section id="menu" style="margin-top:12px"></section>
  </main>

  <footer>
    <div class="wrap" style="display:flex;align-items:center;justify-content:space-between;height:64px;font-size:14px;color:var(--muted)">
      <div>© <span id="year"></span> QuickBite.</div>
      <div>Edit prices in the <code>PRICES</code> object in the JS.</div>
    </div>
  </footer>

  <script>
    // ==== CONFIG ====
    const PHONE_NUMBER = '+27720000000'; // ← put your real number with country code
    const CURRENCY = 'R';

    // Prices per item (adjust as you like)
    const PRICES = {
      pizza_small: 20,     // Lunchbox (small) base price
      pizza_medium: 25,    // Airfryer (medium) base price
      pizza_large: 30,     // Large base price
      roti: 12,            // Plain roti
      wrap: 18             // Plain wrap
    };

    // ===== DATA (only bases; no fillings) =====
    const CATEGORIES = {
      pizzas: {
        title: 'Pizza Bases',
        items: [
          { id:'pizza-small',  name:'Lunchbox (Small) Pizza Base',  price: PRICES.pizza_small,  label:'SMALL' },
          { id:'pizza-medium', name:'Airfryer (Medium) Pizza Base', price: PRICES.pizza_medium, label:'MEDIUM' },
          { id:'pizza-large',  name:'Large Pizza Base',             price: PRICES.pizza_large,  label:'LARGE' }
        ]
      },
      rotis: {
        title: 'Rotis',
        items: [ { id:'roti', name:'Plain Roti', price: PRICES.roti, label:'ROTI' } ]
      },
      wraps: {
        title: 'Wraps',
        items: [ { id:'wrap', name:'Plain Wrap', price: PRICES.wrap, label:'WRAP' } ]
      }
    };

    const fmt = n => CURRENCY + Number(n).toFixed(2);

    function orderText({ itemName, qty, priceEach }){
      const name  = document.getElementById('custName').value.trim();
      const phone = document.getElementById('custPhone').value.trim();
      const total = priceEach * qty;
      const lines = [];
      lines.push('🧾 QuickBite Order');
      lines.push('------------------------------');
      lines.push(`${qty} × ${itemName} — ${fmt(total)}`);
      lines.push('------------------------------');
      lines.push('For: collection (pay on collection)');
      if(name)  lines.push(`Name: ${name}`);
      if(phone) lines.push(`Customer phone: ${phone}`);
      lines.push('');
      lines.push('Thank you!');
      return lines.join('\n');
    }

    function waUrl(text){
      const num = PHONE_NUMBER.replace(/[^+\d]/g, '');
      return `https://wa.me/${num}?text=${encodeURIComponent(text)}`;
    }

    function smsUrl(text){
      const num = PHONE_NUMBER.replace(/[^+\d]/g, '');
      const isIOS = /iPad|iPhone|iPod/.test(navigator.userAgent);
      return `sms:${num}${isIOS ? '&' : '?'}body=${encodeURIComponent(text)}`;
    }

    function sendOrder({ itemName, qty, priceEach }){
      const msg = orderText({ itemName, qty, priceEach });
      const w = window.open(waUrl(msg), '_blank');
      setTimeout(()=>{
        if(!w || w.closed){
          const a = document.createElement('a');
          a.href = smsUrl(msg);
          a.style.display = 'none';
          document.body.appendChild(a); a.click(); a.remove();
        }
      }, 400);
    }

    function renderCategory(key){
      const root = document.getElementById('menu');
      root.innerHTML = '';

      const grid = document.createElement('div');
      grid.className = 'grid';

      CATEGORIES[key].items.forEach(item => {
        const card = document.createElement('div');
        card.className = 'card';
        card.innerHTML = `
          <div class="img">${item.label || ''}</div>
          <h3>${item.name}</h3>
          <div class="muted">Price: <span class="price">${fmt(item.price)}</span> each</div>
          <div class="qty">
            <label class="muted" for="qty-${item.id}">Qty</label>
            <input id="qty-${item.id}" type="number" min="1" value="1" />
            <button class="btn primary" id="btn-${item.id}">Send Order</button>
          </div>
          <div class="muted" style="margin-top:6px">No cart — sending opens a message to our phone.</div>
        `;
        grid.appendChild(card);

        setTimeout(()=>{
          const btn = document.getElementById(`btn-${item.id}`);
          const qty = document.getElementById(`qty-${item.id}`);
          btn.addEventListener('click', ()=>{
            const q = Math.max(1, Math.min(999, Number(qty.value||1)));
            sendOrder({ itemName: item.name, qty: q, priceEach: item.price });
          });
        }, 0);
      });

      root.appendChild(grid);
    }

    function initTabs(){
      const tabs = Array.from(document.querySelectorAll('.tab'));
      tabs.forEach(t => t.addEventListener('click', () => {
        tabs.forEach(x => x.classList.remove('active'));
        t.classList.add('active');
        renderCategory(t.getAttribute('data-tab'));
      }));
    }

    function init(){
      initTabs();
      renderCategory('pizzas');
      document.getElementById('year').textContent = new Date().getFullYear();
    }

    document.addEventListener('DOMContentLoaded', init);
  </script>
</body>
</html>
