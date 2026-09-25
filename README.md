@import url('https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600;700&family=Playfair+Display:ital,wght@0,600;1,600&display=swap');

:root {
  --primary: #0b5ed7;
  --aqua: #22c7c9;
  --teal: #008f95;
  --dark: #102a43;
  --text: #243b53;
  --muted: #627d98;
  --surface: #f7fafc;
  --white: #ffffff;
  --border: #d9e2ec;
  --success: #198754;
  --danger: #dc3545;
  --radius: 18px;
}

* { box-sizing: border-box; }
html { scroll-behavior: smooth; }
body {
  margin: 0;
  color: var(--text);
  font: 15px 'DM Sans', Arial, sans-serif;
  line-height: 1.55;
}
a { color: inherit; text-decoration: none; }
button, input, select, textarea { font: inherit; }
button { cursor: pointer; border: 0; }
img { max-width: 100%; display: block; }

.announcement {
  background: var(--dark);
  color: #fff;
  text-align: center;
  font-size: 12px;
  padding: 8px;
}
.announcement span { color: var(--aqua); padding: 0 12px; }

.header {
  max-width: 1240px;
  margin: auto;
  height: 78px;
  padding: 0 24px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 28px;
}
.logo {
  font-size: 23px;
  font-weight: 700;
  letter-spacing: -1.5px;
  color: var(--dark);
  white-space: nowrap;
}
.logo span:first-child {
  display: inline-grid;
  place-items: center;
  background: var(--primary);
  color: #fff;
  font-size: 11px;
  width: 28px;
  height: 28px;
  border-radius: 8px;
  margin-right: 5px;
}
.logo > span:last-child { color: var(--primary); }
.desktop-nav {
  display: flex;
  gap: 25px;
  font-size: 13px;
  font-weight: 600;
}
.desktop-nav a:hover, .text-link:hover { color: var(--primary); }
.header-actions {
  display: flex;
  align-items: center;
  gap: 18px;
  font-size: 22px;
}
.header-actions b {
  font-size: 10px;
  background: var(--aqua);
  color: var(--dark);
  padding: 2px 6px;
  border-radius: 20px;
  vertical-align: top;
}
.menu-button { display: none; background: none; font-size: 22px; }
.mobile-nav { display: none; }

.eyebrow {
  font-size: 11px;
  letter-spacing: 1.8px;
  text-transform: uppercase;
  color: var(--teal);
  font-weight: 700;
}

.hero {
  min-height: 570px;
  background: var(--surface);
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 30px;
  padding: 75px max(24px, calc((100% - 1150px) / 2));
  align-items: center;
}
.hero h1, .content-hero h1, .not-found h1 {
  font-size: clamp(44px, 6vw, 78px);
  line-height: 1.05;
  letter-spacing: -3px;
  color: var(--dark);
  max-width: 600px;
  margin: 18px 0;
}
.hero h1 em, .not-found h1 em {
  font-family: Georgia, serif;
  color: var(--primary);
  font-weight: 400;
}
.hero p, .content-hero p { font-size: 17px; color: var(--muted); max-width: 470px; }
.hero-actions { display: flex; gap: 25px; align-items: center; margin: 30px 0; }
.hero-trust { display: flex; gap: 20px; color: var(--muted); font-size: 11px; }
.hero-image { position: relative; }
.hero-image img {
  width: 100%;
  height: 430px;
  object-fit: cover;
  border-radius: 25px;
}
.hero-card {
  position: absolute;
  right: -20px;
  bottom: 25px;
  background: #fff;
  padding: 16px 20px;
  border-radius: 12px;
  box-shadow: 0 12px 35px rgba(16, 42, 67, 0.15);
  display: grid;
  gap: 2px;
}
.hero-card strong { font-size: 11px; color: var(--teal); text-transform: uppercase; }
.hero-card span { font-weight: 700; }
.hero-card b { color: var(--primary); font-size: 14px; }

.btn {
  display: inline-block;
  border-radius: 8px;
  padding: 13px 20px;
  font-weight: 700;
  border: 1px solid transparent;
  transition: 0.2s ease;
}
.btn:hover { transform: translateY(-1px); }
.btn-primary { background: var(--primary); color: #fff; }
.btn-primary:hover { background: #084cac; }
.btn-outline { border-color: var(--border); background: #fff; color: var(--dark); }
.btn-dark { background: var(--dark); color: #fff; }
.btn-light { background: #fff; color: var(--primary); }
.text-link { color: var(--primary); font-weight: 700; font-size: 13px; }

.section { max-width: 1150px; margin: auto; padding: 90px 24px; }
.soft-section {
  max-width: none;
  padding-left: max(24px, calc((100% - 1150px) / 2));
  padding-right: max(24px, calc((100% - 1150px) / 2));
  background: var(--surface);
}
.section-heading {
  display: flex;
  justify-content: space-between;
  align-items: end;
  margin-bottom: 35px;
}
.section h2, .promo h2 { font-size: 35px; letter-spacing: -1.5px; line-height: 1.1; margin: 10px 0; color: var(--dark); }

.category-grid { display: grid; grid-template-columns: repeat(4, 1fr); gap: 15px; }
.category-tile {
  height: 220px;
  border-radius: var(--radius);
  padding: 23px;
  color: #fff;
  position: relative;
  overflow: hidden;
}
.category-tile:after {
  content: '✦';
  position: absolute;
  right: -10px;
  bottom: -35px;
  font-size: 150px;
  opacity: 0.13;
}
.category-tile span { font-size: 11px; opacity: 0.7; }
.category-tile h3 { font-size: 25px; margin: 55px 0 0; }
.category-tile p { margin: 0; font-size: 12px; opacity: 0.8; }
.category-tile b { position: absolute; right: 23px; top: 23px; }
.tile-blue { background: var(--primary); }
.tile-aqua { background: var(--aqua); color: var(--dark); }
.tile-dark { background: var(--dark); }
.tile-sand { background: #dbad72; color: var(--dark); }

.product-grid { display: grid; grid-template-columns: repeat(4, 1fr); gap: 20px; }
.product-card { min-width: 0; }
.product-image {
  height: 285px;
  background: #eef3f7;
  border-radius: 14px;
  overflow: hidden;
  position: relative;
}
.product-image img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: 0.4s ease;
}
.product-card:hover .product-image img { transform: scale(1.04); }
.badge {
  position: absolute;
  left: 12px;
  top: 12px;
  background: #fff;
  color: var(--primary);
  font-size: 10px;
  font-weight: 700;
  padding: 5px 8px;
  border-radius: 4px;
}
.wish {
  position: absolute;
  right: 12px;
  top: 12px;
  background: #fff;
  border-radius: 50%;
  width: 32px;
  height: 32px;
  color: var(--dark);
  font-size: 20px;
}
.wish.active { color: #e25572; }
.product-info { padding: 13px 2px; }
.product-meta {
  display: flex;
  justify-content: space-between;
  color: var(--muted);
  font-size: 10px;
  text-transform: uppercase;
  letter-spacing: 0.5px;
}
.product-meta span:last-child { color: #e49c2e; }
.product-info h3 { font-size: 15px; margin: 6px 0; color: var(--dark); }
.price { font-weight: 700; color: var(--primary); }
.price del { font-size: 11px; font-weight: 400; color: var(--muted); margin-left: 5px; }
.card-bottom {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-top: 8px;
}
.card-bottom small { font-size: 10px; color: var(--muted); }
.add-mini {
  background: none;
  color: var(--teal);
  font-size: 11px;
  font-weight: 700;
}

.promo {
  max-width: 1150px;
  margin: 0 auto 90px;
  background: var(--primary);
  border-radius: 20px;
  color: #fff;
  padding: 55px 65px;
  display: flex;
  justify-content: space-between;
  overflow: hidden;
}
.promo h2 { color: #fff; }
.promo h2 em { font-family: Georgia, serif; color: var(--aqua); font-weight: 400; }
.promo p { opacity: 0.8; }
.promo-art { font-size: 110px; font-weight: 700; letter-spacing: -10px; align-self: center; opacity: 0.18; }
.promo-art span { font-family: Georgia, serif; }

.benefits { display: grid; grid-template-columns: repeat(3, 1fr); gap: 25px; }
.benefits article { border-top: 1px solid var(--border); padding-top: 20px; }
.benefit-icon { color: var(--primary); font-size: 28px; }
.benefits h3 { margin: 12px 0 5px; color: var(--dark); }
.benefits p { color: var(--muted); max-width: 280px; font-size: 13px; }

.newsletter {
  text-align: center;
  background: #e8fbfb;
  padding: 75px 20px;
}
.newsletter h2 { margin: 10px 0; color: var(--dark); }
.newsletter p { color: var(--muted); }
.newsletter-form { display: flex; max-width: 450px; margin: 25px auto 8px; }
.newsletter-form input {
  flex: 1;
  border: 1px solid var(--border);
  padding: 13px;
  border-radius: 7px 0 0 7px;
}
.newsletter-form button { border-radius: 0 7px 7px 0; }
.newsletter small { color: var(--teal); }

footer {
  background: var(--dark);
  color: #fff;
  padding: 55px max(24px, calc((100% - 1150px) / 2)) 20px;
}
.footer-main { display: grid; grid-template-columns: 2fr repeat(3, 1fr); gap: 35px; }
.footer-logo { color: #fff; }
.footer-main p { color: #a8bbcc; max-width: 220px; }
.footer-main h4 { margin-top: 0; }
.footer-main > div > a { display: block; color: #a8bbcc; font-size: 13px; margin: 8px 0; }
.footer-bottom {
  border-top: 1px solid rgba(255, 255, 255, 0.12);
  margin-top: 45px;
  padding-top: 18px;
  color: #a8bbcc;
  font-size: 11px;
  display: flex;
  justify-content: space-between;
}
.footer-bottom a { color: #fff; }

.page-shell {
  max-width: 1150px;
  margin: auto;
  padding: 55px 24px 100px;
}
.page-intro, .content-hero, .filter-head, .results-meta, .shop-toolbar, .page-intro.compact {
  display: flex;
  justify-content: space-between;
  align-items: end;
}
.content-hero {
  align-items: center;
  margin-bottom: 30px;
}
.content-hero.compact { margin-bottom: 20px; }
.content-hero h1 {
  font-size: clamp(34px, 5vw, 58px);
  letter-spacing: -2px;
  margin: 12px 0;
}
.text-center { text-align: center; display: block; }
.content-section {
  margin-top: 25px;
  padding-top: 25px;
  border-top: 1px solid var(--border);
}
.content-section h2, .info-card h2, .info-card h3 { color: var(--dark); }
.two-column {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 24px;
}
.check-list, .numbered-list, .info-list {
  padding-left: 20px;
  color: var(--muted);
}
.table-wrap { overflow-x: auto; }
table {
  width: 100%;
  border-collapse: collapse;
  min-width: 500px;
}
th, td {
  text-align: left;
  padding: 12px 10px;
  border-bottom: 1px solid var(--border);
}
th { color: var(--dark); background: var(--surface); }

.cta-box {
  margin-top: 40px;
  background: linear-gradient(135deg, #ebf8ff, #edfdfd);
  border: 1px solid var(--border);
  border-radius: 18px;
  padding: 28px 30px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 16px;
}
.cta-box.narrow { justify-content: center; }

.info-card {
  background: var(--surface);
  border: 1px solid var(--border);
  border-radius: 16px;
  padding: 24px;
}
.form-card { background: #fff; }
.form-grid {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 16px;
}
.form-grid.two { grid-template-columns: 1fr 1fr; }
.form-grid label { display: grid; gap: 6px; font-size: 12px; font-weight: 700; }
.form-grid input, .form-grid select, .form-grid textarea, .search-panel input, .auth-grid input {
  width: 100%;
  border: 1px solid var(--border);
  border-radius: 8px;
  padding: 12px 10px;
  background: #fff;
}
.form-grid .full { grid-column: 1 / -1; }
.status-note { color: var(--teal); font-size: 13px; margin-top: 12px; }

.contact-grid {
  display: grid;
  grid-template-columns: 0.9fr 1.1fr;
  gap: 24px;
  margin-top: 20px;
}

.faq-list {
  max-width: 900px;
  margin: 30px auto 0;
}
.faq-item {
  border: 1px solid var(--border);
  border-radius: 12px;
  margin-bottom: 12px;
  overflow: hidden;
  background: #fff;
}
.faq-question {
  width: 100%;
  text-align: left;
  background: transparent;
  padding: 18px 20px;
  font-weight: 700;
  color: var(--dark);
}
.faq-answer {
  display: none;
  padding: 0 20px 18px;
  color: var(--muted);
}
.faq-item.open .faq-answer { display: block; }

.search-panel {
  display: flex;
  gap: 12px;
  margin: 20px 0 30px;
}
.search-panel input {
  flex: 1;
  min-height: 50px;
}

.empty-state {
  text-align: center;
  padding: 80px 20px;
  background: var(--surface);
  border-radius: 15px;
  margin-top: 20px;
}
.empty-state > div { font-size: 35px; color: var(--aqua); }
.empty-state h2 { color: var(--dark); }

.success-box {
  max-width: 700px;
  margin: 40px auto 0;
  text-align: center;
  background: linear-gradient(135deg, #edfdfd, #eef4ff);
  border: 1px solid var(--border);
  border-radius: 20px;
  padding: 38px 24px;
}
.success-box h1 { font-size: clamp(36px, 5vw, 58px); color: var(--dark); margin: 10px 0; }
.success-grid {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 18px;
  margin: 24px 0;
}
.success-grid > div {
  background: #fff;
  border-radius: 10px;
  padding: 18px;
  border: 1px solid var(--border);
}
.success-grid span { display: block; color: var(--muted); font-size: 12px; }
.note { color: var(--muted); }

.auth-grid {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 24px;
}
.auth-grid form { display: grid; gap: 16px; }
.auth-grid label {
  display: grid;
  gap: 6px;
  font-size: 12px;
  font-weight: 700;
}
.account-grid {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 20px;
}

.page-intro h1 {
  font-size: 45px;
  line-height: 1;
  margin: 10px 0;
  color: var(--dark);
  letter-spacing: -2px;
}
.page-intro p { color: var(--muted); }
.breadcrumbs { font-size: 11px; color: var(--muted); }
.shop-page, .shop-layout {
  max-width: 1150px;
  margin: auto;
}
.shop-toolbar {
  gap: 15px;
  margin-bottom: 30px;
}
.search-box {
  display: flex;
  align-items: center;
  border: 1px solid var(--border);
  border-radius: 7px;
  flex: 1;
  max-width: 500px;
}
.search-box span { font-size: 24px; padding: 0 10px; color: var(--muted); }
.search-box input {
  border: 0;
  outline: 0;
  width: 100%;
  padding: 12px 10px;
}
.sort-label {
  font-size: 12px;
  margin-left: auto;
  display: flex;
  align-items: center;
  gap: 8px;
}
.sort-label select, .filters select {
  border: 1px solid var(--border);
  border-radius: 6px;
  background: #fff;
  padding: 10px;
}
.filter-toggle { display: none; }
.shop-layout { display: grid; grid-template-columns: 190px 1fr; gap: 35px; }
.filters { font-size: 12px; }
.filter-head {
  margin-bottom: 22px;
  font-size: 14px;
}
.filter-head button { display: none; background: none; font-size: 22px; }
.filters label {
  display: block;
  font-weight: 700;
  margin: 20px 0;
}
.filters select { display: block; width: 100%; margin-top: 8px; color: var(--muted); }
.check-row { display: flex !important; gap: 8px; }
.clear-filters { background: none; padding: 0; }
.results-meta {
  margin-bottom: 15px;
  font-size: 12px;
}
.product-detail { padding-top: 20px; }
.detail-grid { display: grid; grid-template-columns: 1.1fr 0.9fr; gap: 70px; align-items: center; margin-top: 35px; }
.detail-image { background: var(--surface); border-radius: 20px; overflow: hidden; }
.detail-image img { width: 100%; height: 570px; object-fit: cover; }
.detail-copy h1 { font-size: 48px; line-height: 1.05; letter-spacing: -2px; color: var(--dark); margin: 13px 0; }
.rating { font-size: 13px; color: #d79a2d; }
.rating span { color: var(--muted); }
.detail-price { font-size: 24px; font-weight: 700; color: var(--primary); margin: 20px 0; }
.detail-copy > p { color: var(--muted); max-width: 450px; }
.selection { margin: 28px 0; }
.selection label { display: flex; justify-content: space-between; font-weight: 700; font-size: 13px; }
.selection a { color: var(--primary); font-size: 11px; }
.size-options { display: flex; gap: 8px; margin-top: 12px; flex-wrap: wrap; }
.size { background: #fff; border: 1px solid var(--border); border-radius: 5px; padding: 9px 14px; }
.size.selected { background: var(--dark); color: #fff; border-color: var(--dark); }
.quantity { display: flex; gap: 15px; align-items: center; margin-bottom: 25px; font-size: 13px; }
.quantity label { margin-right: 15px; }
.quantity button { background: var(--surface); border-radius: 5px; padding: 6px 12px; }
.detail-actions { display: flex; gap: 10px; }
.delivery-note { border-top: 1px solid var(--border); margin-top: 30px; padding-top: 18px; display: grid; font-size: 13px; }
.delivery-note span { color: var(--muted); font-size: 11px; }
.details-lower { border-top: 1px solid var(--border); margin-top: 70px; padding: 35px 0; }
.details-lower p { color: var(--muted); }

.cart-layout, .checkout-layout { display: grid; grid-template-columns: 1.4fr 0.7fr; gap: 50px; }
.cart-item { display: flex; gap: 20px; padding: 18px 0; border-bottom: 1px solid var(--border); }
.cart-item img { width: 125px; height: 125px; object-fit: cover; border-radius: 10px; }
.cart-item h3 { margin: 3px 0; color: var(--dark); }
.cart-item p { font-size: 12px; color: var(--muted); }
.cart-item strong { color: var(--primary); }
.cart-controls { display: flex; align-items: center; gap: 12px; margin-top: 15px; font-size: 12px; }
.cart-controls button:not(.remove) { background: var(--surface); padding: 4px 10px; border-radius: 4px; }
.remove { background: none; color: var(--danger); margin-left: 15px; }
.order-summary { background: var(--surface); padding: 25px; border-radius: 12px; height: max-content; }
.order-summary h2 { color: var(--dark); margin-top: 0; font-size: 20px; }
.order-summary > div { display: flex; justify-content: space-between; margin: 13px 0; font-size: 13px; }
.order-summary span { color: var(--muted); }
.order-summary .total { font-size: 18px; }
.order-summary .total span { color: var(--dark); }
.full { width: 100%; text-align: center; margin-top: 18px; }
.continue { display: block; text-align: center; margin-top: 17px; color: var(--primary); font-size: 12px; }

.checkout-form { border: 1px solid var(--border); padding: 28px; border-radius: 12px; }
.checkout-form h2 { font-size: 20px; color: var(--dark); margin: 0 0 20px; }
.form-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 17px; margin-bottom: 30px; }
.form-grid label span { display: block; font-size: 12px; font-weight: 700; }
.form-grid input, .form-grid select, .form-grid textarea { display: block; width: 100%; border: 1px solid var(--border); border-radius: 5px; padding: 10px; margin-top: 6px; }
.form-grid .full { grid-column: 1 / -1; }
.payment-option { display: flex; gap: 12px; border: 1px solid var(--border); padding: 15px; border-radius: 7px; margin: 10px 0; }
.payment-option span { display: grid; }
.payment-option small, .form-note { color: var(--muted); font-size: 11px; }
.not-found { padding-top: 120px; padding-bottom: 160px; }
.not-found p { color: var(--muted); max-width: 420px; margin-bottom: 25px; }
.sr-only { position: absolute; width: 1px; height: 1px; overflow: hidden; clip: rect(0,0,0,0); }

@media (max-width: 800px) {
  .desktop-nav { display: none; }
  .menu-button { display: block; }
  .mobile-nav { display: none; background: #fff; padding: 10px 24px; border-bottom: 1px solid var(--border); }
  .mobile-nav.open { display: grid; }
  .mobile-nav a { padding: 10px 0; }
  .hero { grid-template-columns: 1fr; padding-top: 45px; min-height: 0; }
  .hero-image { order: -1; }
  .hero-image img { height: 300px; }
  .hero-card { right: 10px; }
  .hero h1 { font-size: 54px; }
  .hero-trust { flex-wrap: wrap; }
  .section { padding-top: 65px; padding-bottom: 65px; }
  .category-grid { grid-template-columns: 1fr 1fr; }
  .product-grid { grid-template-columns: repeat(2, 1fr); gap: 25px 12px; }
  .product-image { height: 210px; }
  .promo { margin: 0 20px 65px; padding: 35px 25px; }
  .promo-art { font-size: 65px; }
  .benefits { grid-template-columns: 1fr; }
  .footer-main { grid-template-columns: 1fr 1fr; }
  .footer-main > div:first-child { grid-column: 1 / -1; }
  .shop-layout { display: block; }
  .detail-grid, .cart-layout, .checkout-layout, .auth-grid, .contact-grid, .two-column, .account-grid { grid-template-columns: 1fr; gap: 28px; }
  .detail-image img { height: 400px; }
  .detail-copy h1 { font-size: 40px; }
  .cart-item img { width: 100px; height: 100px; }
  .filter-toggle { display: block; background: var(--surface); padding: 12px; border-radius: 6px; }
  .filters { display: none; }
  .filters.visible { display: block; position: fixed; inset: 0; background: #fff; z-index: 5; padding: 25px; overflow: auto; }
  .filter-head button { display: block; }
  .search-panel { display: block; }
  .search-panel input, .search-panel button { width: 100%; margin-top: 8px; }
}

@media (max-width: 480px) {
  .header { padding: 0 16px; }
  .header-actions { gap: 10px; }
  .hero { padding-left: 18px; padding-right: 18px; }
  .hero h1 { font-size: 47px; }
  .hero-actions { align-items: start; flex-direction: column; gap: 15px; }
  .category-tile { height: 180px; padding: 17px; }
  .category-tile h3 { margin-top: 40px; }
  .section-heading { align-items: start; display: block; }
  .section-heading .text-link { display: inline-block; margin-top: 12px; }
  .product-image { height: 175px; }
  .card-bottom small { display: none; }
  .newsletter-form { display: block; }
  .newsletter-form input, .newsletter-form button { width: 100%; border-radius: 6px; margin: 4px 0; }
  .footer-bottom { display: block; }
  .footer-bottom span { display: block; margin: 8px 0; }
  .promo { display: block; }
  .promo-art { display: none; }
  .page-intro h1 { font-size: 38px; }
  .success-grid { grid-template-columns: 1fr; }
}

@media (max-width: 560px) {
  .form-grid { grid-template-columns: 1fr; }
}

#newsletter-message {
  display: inline-block;
  margin-top: 10px;
  color: var(--teal);
}

.hidden { display: none !important; }

button[data-add], button[data-remove-wish] { border-radius: 8px; }
