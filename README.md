# JSBAZAAR
IT'S A Multivendor E-COMMERCE Marketplace 
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
  <title>JSBAZAAR.COM | Premium Single-Vendor Marketplace</title>
  <!-- Google Fonts + Tailwind + Font Awesome -->
  <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;400;500;600;700;800&family=Playfair+Display:ital,wght@0,400;0,500;0,600;0,700;1,400&display=swap" rel="stylesheet">
  <script src="https://cdn.tailwindcss.com"></script>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
  <!-- Swiper CSS -->
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/swiper@11/swiper-bundle.min.css" />
  <script src="https://cdn.jsdelivr.net/npm/swiper@11/swiper-bundle.min.js"></script>
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body { font-family: 'Inter', sans-serif; background: #F8F7F4; }
    .font-serif { font-family: 'Playfair Display', serif; }
    .btn-premium { background: linear-gradient(95deg, #D4AF37 0%, #B8942E 100%); transition: all 0.3s; }
    .btn-premium:hover { transform: translateY(-2px); box-shadow: 0 10px 20px -5px rgba(212,175,55,0.4); }
    .whatsapp-float { animation: pulse 2s infinite; }
    @keyframes pulse { 0% { box-shadow: 0 0 0 0 rgba(212,175,55,0.5); } 70% { box-shadow: 0 0 0 12px rgba(212,175,55,0); } 100% { box-shadow: 0 0 0 0 rgba(212,175,55,0); } }
    .toast-notify { position: fixed; bottom: 2rem; left: 50%; transform: translateX(-50%) translateY(20px); background: #1A1E24; color: #D4AF37; padding: 0.75rem 1.75rem; border-radius: 60px; font-size: 0.85rem; z-index: 9999; opacity: 0; transition: 0.2s; pointer-events: none; white-space: nowrap; }
    .toast-notify.show { opacity: 1; transform: translateX(-50%) translateY(0); }
    .product-card { transition: all 0.3s ease; background: white; border-radius: 20px; overflow: hidden; }
    .product-card:hover { transform: translateY(-6px); box-shadow: 0 20px 30px -15px rgba(0,0,0,0.15); }
    .cart-sidebar { transition: transform 0.3s ease-in-out; }
    .modal-backdrop { transition: opacity 0.2s; }
    .vendor-section-footer { background: linear-gradient(135deg, #0F172A 0%, #1E293B 100%); }
    
    /* ========== ATTRACTIVE JSBAZAAR LOGO STYLES ========== */
    .jsbazaar-logo {
      display: flex;
      align-items: center;
      gap: 12px;
      position: relative;
      cursor: pointer;
      transition: all 0.3s ease;
    }
    .jsbazaar-logo:hover {
      transform: scale(1.02);
    }
    .logo-icon-wrapper {
      position: relative;
      width: 48px;
      height: 48px;
      background: linear-gradient(145deg, #D4AF37 0%, #A67C00 100%);
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      box-shadow: 0 8px 20px rgba(212, 175, 55, 0.3);
      animation: subtleGlow 2s ease-in-out infinite;
    }
    @keyframes subtleGlow {
      0%, 100% { box-shadow: 0 8px 20px rgba(212, 175, 55, 0.3); }
      50% { box-shadow: 0 8px 30px rgba(212, 175, 55, 0.6); }
    }
    .logo-icon-inner {
      width: 42px;
      height: 42px;
      background: #1A1E24;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      font-weight: 800;
      font-size: 24px;
      font-family: 'Playfair Display', serif;
      color: #D4AF37;
      transition: all 0.3s;
    }
    .jsbazaar-logo:hover .logo-icon-inner {
      transform: rotate(5deg) scale(1.05);
      color: #F5E6B8;
    }
    .logo-text-container {
      display: flex;
      flex-direction: column;
      line-height: 1.2;
    }
    .logo-main-text {
      font-size: 26px;
      font-weight: 800;
      letter-spacing: -0.5px;
      background: linear-gradient(135deg, #1A1E24 0%, #2D2A24 100%);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
      text-shadow: 1px 1px 2px rgba(212,175,55,0.1);
    }
    .logo-main-text span {
      background: linear-gradient(135deg, #D4AF37 0%, #F5E6B8 100%);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
      font-weight: 800;
    }
    .logo-tagline {
      font-size: 8px;
      letter-spacing: 3px;
      text-transform: uppercase;
      color: #D4AF37;
      font-weight: 600;
      margin-top: -2px;
    }
    .logo-badge {
      position: absolute;
      top: -8px;
      right: -12px;
      background: #D4AF37;
      color: #1A1E24;
      font-size: 8px;
      font-weight: 800;
      padding: 2px 8px;
      border-radius: 20px;
      letter-spacing: 0.5px;
      box-shadow: 0 2px 5px rgba(0,0,0,0.2);
    }
    @media (max-width: 768px) {
      .logo-icon-wrapper { width: 38px; height: 38px; }
      .logo-icon-inner { width: 32px; height: 32px; font-size: 18px; }
      .logo-main-text { font-size: 20px; }
      .logo-tagline { font-size: 6px; letter-spacing: 2px; }
      .logo-badge { font-size: 6px; padding: 1px 6px; top: -6px; right: -8px; }
    }
  </style>
</head>
<body class="bg-[#F8F7F4]">

  <!-- ======================== HEADER WITH ATTRACTIVE LOGO ======================== -->
  <header class="sticky top-0 z-50 bg-white/95 backdrop-blur-md shadow-lg border-b border-[#E8E2D4]">
    <div class="max-w-7xl mx-auto px-4 md:px-6">
      <div class="flex flex-wrap items-center justify-between py-3 gap-3">
        
        <!-- NEW ATTRACTIVE JSBAZAAR LOGO -->
        <div class="jsbazaar-logo" onclick="navigateTo('home')">
          <div class="logo-icon-wrapper">
            <div class="logo-icon-inner">J</div>
            <div class="logo-badge">™</div>
          </div>
          <div class="logo-text-container">
            <div class="logo-main-text">JSBAZAAR<span>.COM</span></div>
            <div class="logo-tagline">PREMIUM MARKETPLACE</div>
          </div>
        </div>
        
        <!-- Search Bar -->
        <div class="flex-1 max-w-xl mx-4 relative">
          <div class="relative">
            <input type="text" id="globalSearchInput" placeholder="Search products..." class="w-full py-3 pl-5 pr-14 border border-gray-200 rounded-full bg-gray-50 focus:ring-2 focus:ring-[#D4AF37] outline-none">
            <button id="globalSearchBtn" class="absolute right-1 top-1 bg-[#D4AF37] hover:bg-[#B8942E] text-white p-2 rounded-full w-10 h-10 flex items-center justify-center"><i class="fa-solid fa-search"></i></button>
          </div>
          <div id="globalSearchResults" class="absolute left-0 right-0 mt-2 bg-white rounded-2xl shadow-2xl z-50 hidden max-h-96 overflow-y-auto border border-gray-100"></div>
        </div>
        
        <div class="flex items-center gap-5">
          <button id="loginModalBtn" onclick="openLoginModal()" class="hidden md:flex flex-col text-left">
            <span class="text-xs text-gray-500" id="userGreetingText">Hello, Sign in</span>
            <span class="text-sm font-bold text-gray-800">Account</span>
          </button>
          <div id="userLoggedInBadge" class="hidden md:flex items-center gap-2 bg-amber-50 px-4 py-1.5 rounded-full cursor-pointer shadow-sm" onclick="openUserMenu()">
            <i class="fa-regular fa-circle-user text-[#D4AF37]"></i>
            <span id="loggedInUserName" class="text-sm font-semibold text-gray-800">User</span>
          </div>
          <button onclick="toggleCart()" class="relative"><i class="fa-solid fa-bag-shopping text-2xl text-gray-800"></i><span id="cartBadge" class="absolute -top-2 -right-2 bg-[#D4AF37] text-gray-900 text-xs font-bold w-5 h-5 rounded-full flex items-center justify-center">0</span></button>
          <button id="mobileMenuBtn" class="md:hidden text-2xl"><i class="fa-solid fa-bars"></i></button>
        </div>
      </div>
      <div class="hidden md:flex items-center gap-8 py-3 border-t border-[#F0EDE6] text-sm font-semibold text-gray-700">
        <a onclick="navigateTo('home')" class="hover:text-[#D4AF37] cursor-pointer transition">HOME</a>
        <a onclick="navigateTo('shop')" class="hover:text-[#D4AF37] cursor-pointer transition">SHOP</a>
        <a onclick="navigateTo('blog')" class="hover:text-[#D4AF37] cursor-pointer transition">BLOG</a>
        <a onclick="navigateTo('contact')" class="hover:text-[#D4AF37] cursor-pointer transition">CONTACT</a>
      </div>
    </div>
    <div id="mobileNavPanel" class="hidden md:hidden bg-white border-t border-[#F0EDE6] px-5 py-4 flex flex-col gap-3 shadow-xl">
      <a onclick="navigateTo('home'); closeMobileNav()" class="font-medium">Home</a>
      <a onclick="navigateTo('shop'); closeMobileNav()" class="font-medium">Shop</a>
      <a onclick="navigateTo('blog'); closeMobileNav()" class="font-medium">Blog</a>
      <a onclick="navigateTo('contact'); closeMobileNav()" class="font-medium">Contact</a>
      <hr><button onclick="openLoginModal()" class="text-left text-[#D4AF37] font-bold">Sign In / Register</button>
    </div>
  </header>

  <!-- ======================== HOME PAGE ======================== -->
  <div id="homePage" class="page-content active-page">
    <!-- Hero Swiper -->
    <div class="max-w-7xl mx-auto px-4 pt-5">
      <div class="swiper heroSwiper w-full h-[500px] md:h-[550px] rounded-3xl overflow-hidden shadow-2xl">
        <div class="swiper-wrapper">
          <div class="swiper-slide relative"><img src="https://images.pexels.com/photos/1640777/pexels-photo-1640777.jpeg?auto=compress&w=1600" class="w-full h-full object-cover"><div class="absolute inset-0 bg-black/40 flex items-center px-8 md:px-16"><div><h2 class="text-white text-5xl md:text-6xl font-serif font-bold">Premium Quality</h2><p class="text-white/80 mt-2">Curated products just for you</p><button onclick="navigateTo('shop')" class="mt-5 btn-premium text-gray-900 px-8 py-3 rounded-full font-bold shadow-xl">Shop Now →</button></div></div></div>
          <div class="swiper-slide relative"><img src="https://images.pexels.com/photos/3780681/pexels-photo-3780681.jpeg?auto=compress&w=1600" class="w-full h-full object-cover"><div class="absolute inset-0 bg-black/30 flex items-center px-8"><h2 class="text-white text-5xl font-serif">Luxury Electronics</h2></div></div>
          <div class="swiper-slide relative"><img src="https://images.pexels.com/photos/1043474/pexels-photo-1043474.jpeg?auto=compress&w=1600" class="w-full h-full object-cover"><div class="absolute inset-0 bg-black/30 flex items-center px-8"><h2 class="text-white text-5xl font-serif">Fashion & Lifestyle</h2></div></div>
        </div><div class="swiper-pagination"></div><div class="swiper-button-next"></div><div class="swiper-button-prev"></div>
      </div>
    </div>

    <!-- Newsletter Subscription Banner -->
    <div class="max-w-7xl mx-auto px-4 py-8 mt-2">
      <div class="bg-gradient-to-r from-gray-900 to-gray-800 rounded-2xl p-6 text-white shadow-xl border border-[#D4AF37]/20">
        <div class="flex flex-col md:flex-row justify-between items-center gap-5">
          <div><i class="fa-regular fa-envelope text-3xl text-[#D4AF37] mr-2"></i><span class="font-serif text-2xl font-bold">Exclusive Deals</span><p class="text-white/80 text-sm mt-1">Subscribe & get 10% off your first order</p></div>
          <div class="flex gap-3 w-full md:w-auto"><input type="email" id="newsletterEmail" placeholder="Your email address" class="rounded-full px-5 py-3 text-gray-800 w-full md:w-80 outline-none shadow-md"><button onclick="subscribeNewsletter()" class="btn-premium text-gray-900 px-8 py-3 rounded-full font-bold transition">Subscribe</button></div>
        </div>
      </div>
    </div>

    <!-- Featured Products -->
    <div class="max-w-7xl mx-auto px-4 py-6">
      <div class="flex justify-between items-center"><h2 class="font-serif text-3xl font-bold text-gray-900">✨ Trending Now</h2><a onclick="navigateTo('shop')" class="text-[#D4AF37] text-sm font-semibold border-b border-[#D4AF37]">View all →</a></div>
      <div id="homeProductGrid" class="grid grid-cols-2 sm:grid-cols-3 md:grid-cols-4 lg:grid-cols-5 gap-6 mt-6"></div>
    </div>

    <!-- Best Deals Banner -->
    <div class="max-w-7xl mx-auto px-4 py-8">
      <div class="bg-white rounded-2xl shadow-lg p-6 flex flex-col md:flex-row justify-between items-center gap-4 border border-amber-100">
        <div><span class="bg-red-600 text-white text-sm px-3 py-1 rounded-full font-bold">HOT DEAL</span><h2 class="font-serif text-2xl font-bold mt-2">Limited Time Offers</h2></div>
        <button onclick="navigateTo('shop')" class="btn-premium text-gray-900 px-6 py-2 rounded-full font-bold">Shop Now →</button>
      </div>
      <div id="dealsGrid" class="grid grid-cols-2 md:grid-cols-4 gap-5 mt-5"></div>
    </div>
  </div>

  <!-- ======================== SHOP PAGE ======================== -->
  <div id="shopPage" class="page-content hidden">
    <div class="max-w-7xl mx-auto px-4 py-10">
      <div class="flex flex-col md:flex-row gap-8">
        <div class="w-full md:w-64 bg-white p-5 rounded-2xl shadow-md h-fit">
          <h3 class="font-bold text-lg mb-4">Filter by Category</h3>
          <div id="filterCategoryList" class="space-y-2"></div>
          <h3 class="font-bold text-lg mt-6 mb-3">Price Range</h3>
          <select id="priceFilter" class="w-full border rounded-full px-4 py-2 text-sm">
            <option value="all">All Prices</option>
            <option value="under3000">Under PKR 3,000</option>
            <option value="3000to7000">PKR 3,000 - 7,000</option>
            <option value="above7000">Above PKR 7,000</option>
          </select>
        </div>
        <div class="flex-1"><h1 class="font-serif text-4xl font-bold">All Products</h1><p class="text-gray-500 mt-1">Premium quality, authentic brands</p><div id="shopProductGrid" class="grid grid-cols-2 md:grid-cols-3 gap-6 mt-6"></div></div>
      </div>
    </div>
  </div>

  <!-- ======================== BLOG PAGE ======================== -->
  <div id="blogPage" class="page-content hidden">
    <div class="max-w-7xl mx-auto px-4 py-12">
      <div class="text-center mb-10"><h1 class="font-serif text-5xl font-bold">Our Journal</h1><p class="text-gray-500 mt-2">Wellness tips, product guides & lifestyle</p><div class="w-20 h-0.5 bg-[#D4AF37] mx-auto mt-4"></div></div>
      <div id="blogGrid" class="grid md:grid-cols-3 gap-8"></div>
    </div>
  </div>

  <!-- ======================== CONTACT PAGE ======================== -->
  <div id="contactPage" class="page-content hidden">
    <div class="max-w-5xl mx-auto px-4 py-14">
      <div class="bg-white rounded-3xl shadow-xl p-8 border border-[#F0EDE6]">
        <h2 class="font-serif text-3xl font-bold">Customer Support</h2>
        <p class="text-gray-500 mt-1">WhatsApp: 03706436270 | Delivery all over Pakistan</p>
        <form onsubmit="handleContact(event)" class="mt-7">
          <input type="text" placeholder="Full name" class="w-full border border-gray-200 rounded-xl p-3 mb-4 bg-gray-50 focus:border-[#D4AF37] outline-none">
          <input type="tel" placeholder="WhatsApp Number" class="w-full border border-gray-200 rounded-xl p-3 mb-4 bg-gray-50 focus:border-[#D4AF37] outline-none">
          <textarea rows="3" placeholder="Your message" class="w-full border border-gray-200 rounded-xl p-3 bg-gray-50 focus:border-[#D4AF37] outline-none"></textarea>
          <button class="btn-premium text-gray-900 px-8 py-3 rounded-full font-bold mt-4">Send Message</button>
        </form>
      </div>
    </div>
  </div>

  <!-- ======================== LOGIN MODAL ======================== -->
  <div id="loginModal" class="fixed inset-0 bg-black/60 z-[2000] hidden items-center justify-center modal-backdrop" onclick="closeLoginModal(event)">
    <div class="bg-white rounded-3xl max-w-md w-full mx-4 p-7 shadow-2xl border-t-8 border-[#D4AF37]" onclick="event.stopPropagation()">
      <button onclick="closeLoginModal()" class="float-right text-2xl text-gray-400 hover:text-gray-800">&times;</button>
      <div class="text-center"><div class="w-16 h-16 bg-amber-100 rounded-full flex items-center justify-center text-3xl mx-auto"><i class="fa-regular fa-user text-[#D4AF37]"></i></div><h2 class="font-serif text-2xl font-bold mt-3">Welcome Back</h2><p class="text-gray-500 text-sm">Sign in for exclusive deals & order tracking</p></div>
      <div class="mt-6"><input type="text" id="loginName" placeholder="Full Name" class="w-full border border-gray-200 rounded-xl p-3 mb-3 bg-gray-50"><input type="email" id="loginEmail" placeholder="Email Address" class="w-full border border-gray-200 rounded-xl p-3 mb-3 bg-gray-50"><button onclick="processLogin()" class="btn-premium w-full text-gray-900 py-3 rounded-xl font-bold">Sign In</button><p class="text-center text-xs text-gray-400 mt-5">By signing in you agree to our Terms & Privacy</p></div>
    </div>
  </div>

  <!-- ======================== CART SIDEBAR ======================== -->
  <div id="cartOverlay" class="fixed inset-0 bg-black/40 z-[1000] invisible opacity-0 transition"></div>
  <div id="cartSidebar" class="fixed top-0 right-0 h-full w-full max-w-md bg-white z-[1010] shadow-2xl transform translate-x-full transition-transform flex flex-col">
    <div class="p-5 border-b border-[#F0EDE6] flex justify-between"><h2 class="font-serif text-xl font-bold">Your Cart</h2><button onclick="toggleCart()" class="text-2xl text-gray-400">&times;</button></div>
    <div id="cartItemsList" class="flex-1 overflow-y-auto p-5 space-y-4"></div>
    <div class="border-t border-[#F0EDE6] p-5 bg-gray-50"><div class="flex justify-between font-bold text-lg"><span>Total</span><span id="cartTotalSpan" class="text-[#D4AF37]">PKR 0</span></div><button onclick="checkoutWhatsApp()" class="btn-premium w-full text-gray-900 py-3 rounded-full font-bold mt-4">Proceed to Checkout</button><p class="text-center text-xs text-gray-400 mt-3">Cash on Delivery | Free Shipping</p></div>
  </div>

  <!-- ======================== TOAST & WHATSAPP ======================== -->
  <div id="toastMsg" class="toast-notify"></div>
  <a href="https://wa.me/923706436270" target="_blank" class="whatsapp-float fixed bottom-6 right-6 bg-[#D4AF37] text-gray-900 w-14 h-14 rounded-full flex items-center justify-center shadow-2xl text-2xl z-50 hover:scale-105 transition"><i class="fa-brands fa-whatsapp"></i></a>

  <!-- ======================== FOOTER (Multi-Vendor + Payment Options) ======================== -->
  <footer class="bg-gray-900 text-gray-300 mt-12 pt-12">
    <!-- Multi-Vendor Section -->
    <div class="vendor-section-footer max-w-7xl mx-auto px-4 py-8 mb-8 rounded-2xl border border-[#D4AF37]/30">
      <div class="text-center mb-6"><i class="fa-solid fa-store text-4xl text-[#D4AF37]"></i><h3 class="font-serif text-2xl font-bold text-white mt-2">Join Our Marketplace</h3><p class="text-gray-300 text-sm">Retailers, wholesalers & manufacturers — sell with us</p></div>
      <div class="grid md:grid-cols-3 gap-6">
        <div class="bg-white/10 backdrop-blur-sm rounded-xl p-5 text-center"><i class="fa-solid fa-shop text-3xl text-[#D4AF37] mb-3"></i><h4 class="font-bold text-white">Retailers</h4><p class="text-sm text-gray-300 mt-1">List your products & reach thousands of customers</p><button onclick="openVendorRegister()" class="mt-3 text-[#D4AF37] text-sm font-semibold">Register as Retailer →</button></div>
        <div class="bg-white/10 backdrop-blur-sm rounded-xl p-5 text-center"><i class="fa-solid fa-boxes text-3xl text-[#D4AF37] mb-3"></i><h4 class="font-bold text-white">Wholesalers</h4><p class="text-sm text-gray-300 mt-1">Bulk orders & B2B opportunities</p><button onclick="openVendorRegister()" class="mt-3 text-[#D4AF37] text-sm font-semibold">Register as Wholesaler →</button></div>
        <div class="bg-white/10 backdrop-blur-sm rounded-xl p-5 text-center"><i class="fa-solid fa-industry text-3xl text-[#D4AF37] mb-3"></i><h4 class="font-bold text-white">Manufacturers</h4><p class="text-sm text-gray-300 mt-1">Direct from factory to customer</p><button onclick="openVendorRegister()" class="mt-3 text-[#D4AF37] text-sm font-semibold">Register as Manufacturer →</button></div>
      </div>
      <div id="vendorModal" class="fixed inset-0 bg-black/70 z-[3000] hidden items-center justify-center" onclick="closeVendorModal(event)">
        <div class="bg-white rounded-3xl max-w-md w-full mx-4 p-7" onclick="event.stopPropagation()"><h2 class="font-serif text-2xl font-bold">Become a Seller</h2><input type="text" id="vendorShopName" placeholder="Shop/Brand Name" class="w-full border rounded-xl p-3 mt-4"><input type="text" id="vendorOwnerName" placeholder="Owner Name" class="w-full border rounded-xl p-3 mt-3"><input type="email" id="vendorEmail" placeholder="Email" class="w-full border rounded-xl p-3 mt-3"><input type="tel" id="vendorPhone" placeholder="WhatsApp Number" class="w-full border rounded-xl p-3 mt-3"><select id="vendorTypeSelect" class="w-full border rounded-xl p-3 mt-3"><option>Retailer</option><option>Wholesaler</option><option>Manufacturer</option></select><button onclick="registerVendor()" class="btn-premium w-full py-3 rounded-xl font-bold mt-5">Submit Application</button><p class="text-center text-xs text-gray-400 mt-3">Our team will contact you within 24 hours</p></div>
      </div>
    </div>

    <!-- Payment Section: JazzCash / EasyPaisa -->
    <div class="max-w-7xl mx-auto px-4 py-6 border-t border-b border-gray-800 mb-6">
      <div class="flex flex-col md:flex-row justify-between items-center gap-6">
        <div class="text-center md:text-left"><h4 class="font-bold text-white text-lg"><i class="fa-solid fa-money-bill-transfer text-[#D4AF37] mr-2"></i>Payment Options</h4><p class="text-gray-400 text-sm mt-1">Secure & convenient ways to pay</p></div>
        <div class="flex flex-wrap gap-6 justify-center">
          <div class="bg-gray-800 rounded-xl p-4 flex items-center gap-3 min-w-[160px]"><i class="fa-brands fa-cc-visa text-3xl text-[#D4AF37]"></i><div><p class="font-semibold text-white">Cash on Delivery</p><p class="text-xs text-gray-400">Pay when you receive</p></div></div>
          <div class="bg-gray-800 rounded-xl p-4 flex items-center gap-3 min-w-[160px]"><i class="fa-solid fa-mobile-alt text-3xl text-[#D4AF37]"></i><div><p class="font-semibold text-white">JazzCash</p><p class="text-xs text-gray-400">03217106293</p></div></div>
          <div class="bg-gray-800 rounded-xl p-4 flex items-center gap-3 min-w-[160px]"><i class="fa-solid fa-wallet text-3xl text-[#D4AF37]"></i><div><p class="font-semibold text-white">EasyPaisa</p><p class="text-xs text-gray-400">03217106293</p></div></div>
          <div class="bg-gray-800 rounded-xl p-4 flex items-center gap-3 min-w-[160px]"><i class="fa-solid fa-building-columns text-3xl text-[#D4AF37]"></i><div><p class="font-semibold text-white">Bank Transfer</p><p class="text-xs text-gray-400">On request</p></div></div>
        </div>
      </div>
    </div>

    <div class="max-w-7xl mx-auto px-4 grid md:grid-cols-4 gap-8 pb-8">
      <div><div class="flex items-center gap-2"><div class="bg-[#D4AF37] w-8 h-8 rounded-full flex items-center justify-center text-gray-900 font-bold">J</div><span class="font-bold text-xl text-white">JSBAZAAR<span class="text-[#D4AF37]">.COM</span></span></div><p class="text-sm text-gray-400 mt-3">Premium quality products delivered to your doorstep.</p></div>
      <div><h4 class="font-bold text-white mb-3">Quick Links</h4><ul class="space-y-2 text-sm"><li><a onclick="navigateTo('shop')" class="hover:text-[#D4AF37] cursor-pointer">Shop</a></li><li><a onclick="navigateTo('blog')" class="hover:text-[#D4AF37] cursor-pointer">Blog</a></li><li><a onclick="navigateTo('contact')" class="hover:text-[#D4AF37] cursor-pointer">Contact</a></li></ul></div>
      <div><h4 class="font-bold text-white mb-3">Contact</h4><p class="text-sm"><i class="fa-brands fa-whatsapp text-[#D4AF37] mr-2"></i> 03706436270</p><p class="text-sm mt-1"><i class="fa-solid fa-phone text-[#D4AF37] mr-2"></i> 03217106293 (JazzCash/EasyPaisa)</p></div>
      <div><h4 class="font-bold text-white mb-3">Newsletter</h4><div class="flex"><input type="email" id="footerEmail" placeholder="Your email" class="p-2 rounded-l-md text-sm flex-1 bg-gray-800 border border-gray-700 text-white"><button onclick="subscribeFooter()" class="bg-[#D4AF37] text-gray-900 px-4 rounded-r-md font-bold">Subscribe</button></div></div>
    </div>
    <div class="text-center text-xs text-gray-500 border-t border-gray-800 pt-6 pb-6">© 2025 JSBAZAAR.COM — All rights reserved. Premium Store | Multi-Vendor Marketplace</div>
  </footer>

  <script>
    // ======================== PRODUCT DATABASE ========================
    const productsDB = [
      { id: 1, name: "Epimedyumlu Macun (Turkish Herbal Paste)", price: 7500, oldPrice: 9500, image: "https://images.pexels.com/photos/1640777/pexels-photo-1640777.jpeg?auto=compress&w=300", category: "Wellness", rating: 4.9, badge: "Bestseller" },
      { id: 2, name: "Premium Wireless Headphones", price: 4599, oldPrice: 7999, image: "https://images.pexels.com/photos/3780681/pexels-photo-3780681.jpeg?auto=compress&w=300", category: "Electronics", rating: 4.7, badge: "Deal" },
      { id: 3, name: "Men's Luxury Formal Shirt", price: 1999, oldPrice: 3999, image: "https://images.pexels.com/photos/1043474/pexels-photo-1043474.jpeg?auto=compress&w=300", category: "Fashion", rating: 4.5 },
      { id: 4, name: "Organic Ashwagandha Powder", price: 1899, oldPrice: 2999, image: "https://images.pexels.com/photos/4041392/pexels-photo-4041392.jpeg?auto=compress&w=300", category: "Wellness", rating: 4.8 },
      { id: 5, name: "Smart LED TV 55 Inch", price: 89999, oldPrice: 129999, image: "https://images.pexels.com/photos/1841831/pexels-photo-1841831.jpeg?auto=compress&w=300", category: "Electronics", rating: 4.6, badge: "Premium" },
      { id: 6, name: "Women's Summer Floral Dress", price: 2499, oldPrice: 4999, image: "https://images.pexels.com/photos/1043474/pexels-photo-1043474.jpeg?auto=compress&w=300", category: "Fashion", rating: 4.7 },
      { id: 7, name: "Non-Stick Cookware Set (7 pcs)", price: 5599, oldPrice: 8999, image: "https://images.pexels.com/photos/1279330/pexels-photo-1279330.jpeg?auto=compress&w=300", category: "Home", rating: 4.4 },
      { id: 8, name: "Royal Honey & Ginseng Blend", price: 4900, oldPrice: 6900, image: "https://images.pexels.com/photos/129207/pexels-photo-129207.jpeg?auto=compress&w=300", category: "Wellness", rating: 4.9, badge: "Limited" }
    ];

    const blogPosts = [
      { id: 1, title: "The Power of Turkish Macun", excerpt: "Discover the ancient herbal blend that's taking the wellness world by storm.", image: "https://images.pexels.com/photos/1640777/pexels-photo-1640777.jpeg?w=400", date: "May 2025" },
      { id: 2, title: "5 Tips for Better Sleep", excerpt: "Natural remedies and lifestyle changes for deeper rest.", image: "https://images.pexels.com/photos/4041392/pexels-photo-4041392.jpeg?w=400", date: "April 2025" },
      { id: 3, title: "Sustainable Fashion Guide", excerpt: "How to build an eco-friendly wardrobe without breaking the bank.", image: "https://images.pexels.com/photos/1043474/pexels-photo-1043474.jpeg?w=400", date: "March 2025" }
    ];

    let cart = [];
    let currentUser = null;
    let currentCategoryFilter = "all";
    let currentPriceFilter = "all";

    function showToast(msg) { const t = document.getElementById('toastMsg'); t.innerText = msg; t.classList.add('show'); setTimeout(() => t.classList.remove('show'), 2500); }
    function addToCart(product) { const existing = cart.find(i => i.id === product.id); if(existing) existing.qty += 1; else cart.push({ ...product, qty: 1, priceNumeric: product.price }); updateCartUI(); showToast(`✓ ${product.name} added to cart`); }
    function updateCartUI() { const qty = cart.reduce((a,b)=>a+b.qty,0); document.getElementById('cartBadge').innerText = qty; const container = document.getElementById('cartItemsList'); if(!container) return; if(cart.length===0) container.innerHTML='<div class="text-center text-gray-400 py-10">Your cart is empty</div>'; else container.innerHTML = cart.map(i=>`<div class="flex gap-3 border-b border-gray-100 pb-4"><img src="${i.image}" class="w-16 h-16 object-contain rounded-lg bg-gray-50"><div class="flex-1"><p class="font-semibold text-gray-800">${i.name}</p><p class="text-[#D4AF37] font-bold">PKR ${i.price}</p><div class="flex gap-2 mt-2"><button onclick="updateQty(${i.id},-1)" class="border border-gray-300 w-7 h-7 rounded-full hover:bg-gray-100">-</button><span class="px-2">${i.qty}</span><button onclick="updateQty(${i.id},1)" class="border border-gray-300 w-7 h-7 rounded-full hover:bg-gray-100">+</button></div></div><div class="font-bold">PKR ${i.price * i.qty}</div></div>`).join(''); const total = cart.reduce((s,i)=>s+i.price*i.qty,0); document.getElementById('cartTotalSpan').innerHTML = `PKR ${total.toLocaleString()}`; }
    function updateQty(id, delta) { const idx = cart.findIndex(i=>i.id===id); if(idx!==-1){ cart[idx].qty+=delta; if(cart[idx].qty<=0) cart.splice(idx,1); updateCartUI(); } }
    function toggleCart() { document.getElementById('cartSidebar').classList.toggle('translate-x-0'); document.getElementById('cartOverlay').classList.toggle('invisible'); document.getElementById('cartOverlay').classList.toggle('opacity-0'); }
    function checkoutWhatsApp() { if(cart.length===0){ showToast("Cart is empty"); return; } let msg = "🛒 Order from JSBAZAAR.COM:\n"; cart.forEach(i=>msg+=`• ${i.name} x${i.qty} = PKR ${i.price*i.qty}\n`); const total = cart.reduce((s,i)=>s+i.price*i.qty,0); msg+=`\nTotal: PKR ${total.toLocaleString()}\nDelivery: Pakistan (COD/JazzCash/EasyPaisa available)`. window.open(`https://wa.me/923706436270?text=${encodeURIComponent(msg)}`); }
    function handleContact(e) { e.preventDefault(); showToast("✓ Message sent! We'll reply on WhatsApp within 2 hours."); }
    
    function openLoginModal() { document.getElementById('loginModal').style.display = 'flex'; document.getElementById('loginModal').classList.remove('hidden'); }
    function closeLoginModal(e) { if(!e || e.target === document.getElementById('loginModal')) { document.getElementById('loginModal').style.display = 'none'; document.getElementById('loginModal').classList.add('hidden'); } }
    function processLogin() { const name = document.getElementById('loginName').value.trim(); const email = document.getElementById('loginEmail').value.trim(); if(!name || !email) { showToast("Please enter name and email"); return; } currentUser = { name, email }; localStorage.setItem('jsbazaar_user', JSON.stringify(currentUser)); updateUserUI(); closeLoginModal(); showToast(`Welcome ${name}! Enjoy premium shopping.`); }
    function updateUserUI() { const loginBtn = document.getElementById('loginModalBtn'); const userBadge = document.getElementById('userLoggedInBadge'); if(currentUser) { if(loginBtn) loginBtn.classList.add('hidden'); if(userBadge) userBadge.classList.remove('hidden'); document.getElementById('loggedInUserName').innerText = currentUser.name.split(' ')[0]; document.getElementById('userGreetingText') && (document.getElementById('userGreetingText').innerText = `Hello, ${currentUser.name}`); } else { if(loginBtn) loginBtn.classList.remove('hidden'); if(userBadge) userBadge.classList.add('hidden'); } }
    function openUserMenu() { showToast(`Signed in as ${currentUser?.name}. Need help? WhatsApp us!`); }
    
    function subscribeNewsletter() { const email = document.getElementById('newsletterEmail').value; if(email){ localStorage.setItem('jsbazaar_email',email); showToast("🎉 Subscribed! 10% off coupon sent to your email."); document.getElementById('newsletterEmail').value=''; } else showToast("Enter valid email"); }
    function subscribeFooter() { const email = document.getElementById('footerEmail').value; if(email){ localStorage.setItem('jsbazaar_email',email); showToast("Subscribed successfully!"); document.getElementById('footerEmail').value=''; } }
    
    function openVendorRegister() { document.getElementById('vendorModal').style.display = 'flex'; document.getElementById('vendorModal').classList.remove('hidden'); }
    function closeVendorModal(e) { if(!e || e.target === document.getElementById('vendorModal')) { document.getElementById('vendorModal').style.display = 'none'; document.getElementById('vendorModal').classList.add('hidden'); } }
    function registerVendor() { const shop = document.getElementById('vendorShopName').value; const owner = document.getElementById('vendorOwnerName').value; if(!shop || !owner) { showToast("Please fill shop name and owner name"); return; } showToast(`🎉 Application submitted! We'll contact you within 24 hours.`); closeVendorModal(); document.getElementById('vendorShopName').value = ''; document.getElementById('vendorOwnerName').value = ''; document.getElementById('vendorEmail').value = ''; document.getElementById('vendorPhone').value = ''; }
    
    function navigateTo(page) { document.querySelectorAll('.page-content').forEach(el=>el.classList.add('hidden')); document.getElementById(`${page}Page`).classList.remove('hidden'); window.scrollTo({ top: 0, behavior: 'smooth' }); if(page === 'home') renderHome(); if(page === 'shop') renderShop(); if(page === 'blog') renderBlog(); }
    function renderHome() { const featured = productsDB.slice(0,5); const deals = productsDB.filter(p=>p.oldPrice).slice(0,4); document.getElementById('homeProductGrid').innerHTML = featured.map(p=>productCard(p)).join(''); document.getElementById('dealsGrid').innerHTML = deals.map(p=>productCard(p)).join(''); }
    function renderShop() { let filtered = [...productsDB]; if(currentCategoryFilter !== 'all') filtered = filtered.filter(p=>p.category === currentCategoryFilter); if(currentPriceFilter === 'under3000') filtered = filtered.filter(p=>p.price < 3000); else if(currentPriceFilter === '3000to7000') filtered = filtered.filter(p=>p.price >= 3000 && p.price <= 7000); else if(currentPriceFilter === 'above7000') filtered = filtered.filter(p=>p.price > 7000); document.getElementById('shopProductGrid').innerHTML = filtered.map(p=>productCard(p)).join(''); const cats = [...new Map(productsDB.map(p=>[p.category,p.category])).keys()]; document.getElementById('filterCategoryList').innerHTML = `<button onclick="setCategoryFilter('all')" class="block w-full text-left p-2 rounded-lg hover:bg-gray-100">All Categories</button>` + cats.map(c=>`<button onclick="setCategoryFilter('${c}')" class="block w-full text-left p-2 rounded-lg hover:bg-gray-100">${c}</button>`).join(''); }
    function setCategoryFilter(cat) { currentCategoryFilter = cat; renderShop(); }
    document.getElementById('priceFilter')?.addEventListener('change', (e) => { currentPriceFilter = e.target.value; renderShop(); });
    function renderBlog() { document.getElementById('blogGrid').innerHTML = blogPosts.map(b=>`<div class="bg-white rounded-2xl shadow-lg overflow-hidden border border-gray-100"><img src="${b.image}" class="h-56 w-full object-cover"><div class="p-5"><span class="text-[#D4AF37] text-xs uppercase tracking-wider">Wellness</span><h3 class="font-serif text-xl font-bold mt-1">${b.title}</h3><p class="text-gray-500 text-sm mt-2">${b.excerpt}</p><div class="flex justify-between items-center mt-4"><span class="text-xs text-gray-400">${b.date}</span><button onclick="showToast('Full article coming soon')" class="text-[#D4AF37] text-sm font-semibold cursor-pointer">Read →</button></div></div></div>`).join(''); }
    function productCard(p) { return `<div class="product-card bg-white rounded-xl shadow-md p-3"><img src="${p.image}" class="h-44 w-full object-cover rounded-lg"><div class="mt-2"><div class="flex justify-between"><span class="text-xs bg-amber-100 px-2 py-0.5 rounded-full">${p.badge || 'Premium'}</span><span class="text-xs">⭐ ${p.rating}</span></div><h3 class="font-semibold text-gray-800 mt-1 line-clamp-1">${p.name}</h3><div class="flex gap-2 mt-1"><span class="font-bold text-[#D4AF37]">PKR ${p.price.toLocaleString()}</span><span class="text-xs line-through text-gray-400">${p.oldPrice ? 'PKR '+p.oldPrice.toLocaleString():''}</span></div><button onclick='addToCart(${JSON.stringify(p)})' class="mt-3 w-full bg-gray-800 hover:bg-[#D4AF37] hover:text-gray-900 text-white py-2 rounded-full text-sm transition font-medium">Add to Cart</button></div></div>`; }
    
    const searchInput = document.getElementById('globalSearchInput'); const resultsDiv = document.getElementById('globalSearchResults');
    function performGlobalSearch() { const term = searchInput.value.trim().toLowerCase(); if(!term) { resultsDiv.classList.add('hidden'); return; } const filtered = productsDB.filter(p=>p.name.toLowerCase().includes(term) || p.category.toLowerCase().includes(term)); resultsDiv.innerHTML = filtered.map(p=>`<div onclick="addToCartAndClose(${JSON.stringify(p)})" class="flex gap-3 p-3 border-b hover:bg-gray-50 cursor-pointer"><img src="${p.image}" class="w-12 h-12 object-contain rounded"><div><p class="font-semibold text-gray-800">${p.name}</p><p class="text-[#D4AF37] text-sm">PKR ${p.price}</p></div></div>`).join('') || '<div class="p-4 text-gray-500 text-center">No products found</div>'; resultsDiv.classList.remove('hidden'); }
    function addToCartAndClose(p) { addToCart(p); resultsDiv.classList.add('hidden'); searchInput.value = ''; }
    document.getElementById('globalSearchBtn')?.addEventListener('click', performGlobalSearch); searchInput?.addEventListener('input', performGlobalSearch); document.addEventListener('click', (e) => { if(!resultsDiv?.contains(e.target) && e.target !== searchInput) resultsDiv?.classList.add('hidden'); });
    function closeMobileNav() { document.getElementById('mobileNavPanel')?.classList.add('hidden'); }
    
    const stored = localStorage.getItem('jsbazaar_user'); if(stored) { currentUser = JSON.parse(stored); updateUserUI(); }
    
    window.addToCart = addToCart; window.updateQty = updateQty; window.toggleCart = toggleCart; window.navigateTo = navigateTo; window.checkoutWhatsApp = checkoutWhatsApp; window.handleContact = handleContact; window.openLoginModal = openLoginModal; window.closeLoginModal = closeLoginModal; window.processLogin = processLogin; window.subscribeNewsletter = subscribeNewsletter; window.subscribeFooter = subscribeFooter; window.setCategoryFilter = setCategoryFilter; window.openUserMenu = openUserMenu; window.closeMobileNav = closeMobileNav; window.openVendorRegister = openVendorRegister; window.closeVendorModal = closeVendorModal; window.registerVendor = registerVendor;
    
    document.addEventListener('DOMContentLoaded', () => { renderHome(); renderShop(); renderBlog(); new Swiper('.heroSwiper', { loop: true, autoplay: { delay: 4500 }, pagination: { el: '.swiper-pagination', clickable: true }, navigation: { nextEl: '.swiper-button-next', prevEl: '.swiper-button-prev' } }); document.getElementById('mobileMenuBtn')?.addEventListener('click',()=>{ document.getElementById('mobileNavPanel')?.classList.toggle('hidden'); }); document.getElementById('cartOverlay')?.addEventListener('click',toggleCart); });
  </script>
</body>
</html>
