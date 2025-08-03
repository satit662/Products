<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Modern E-commerce UI</title>
    
    <!-- Tailwind CSS for styling -->
    <script src="https://cdn.tailwindcss.com"></script>
    
    <!-- Google Fonts (Sarabun for Thai) -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Sarabun:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    
    <!-- Lucide Icons -->
    <script src="https://unpkg.com/lucide@latest"></script>

    <style>
        /* Custom styles */
        body {
            font-family: 'Sarabun', sans-serif;
            background-color: #f8f9fa;
        }
        /* Style for active navigation link */
        .nav-link-active {
            color: #1a1a1a;
            font-weight: 600;
        }
        /* Simple transition for page switching */
        .page {
            display: none;
            animation: fadeIn 0.5s;
        }
        .page.active {
            display: block;
        }
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }
        /* Custom scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #f1f1f1;
        }
        ::-webkit-scrollbar-thumb {
            background: #d1d5db;
            border-radius: 10px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #9ca3af;
        }
    </style>
</head>
<body class="text-gray-800">

    <!-- Main Container -->
    <div id="app-container" class="max-w-7xl mx-auto bg-white shadow-lg">

        <!-- Header -->
        <header class="sticky top-0 bg-white/80 backdrop-blur-md border-b border-gray-200 z-40">
            <nav class="container mx-auto px-4 sm:px-6 lg:px-8">
                <div class="flex items-center justify-between h-16">
                    <!-- Logo -->
                    <div class="flex-shrink-0">
                        <a href="#" class="text-2xl font-bold tracking-wider nav-link" data-page="home">URBAN.</a>
                    </div>

                    <!-- Desktop Navigation -->
                    <div class="hidden md:flex md:items-center md:space-x-8">
                        <a href="#" class="text-gray-500 hover:text-gray-900 nav-link" data-page="home">หน้าแรก</a>
                        <a href="#" class="text-gray-500 hover:text-gray-900 nav-link" data-page="shop">สินค้าทั้งหมด</a>
                        <a href="#" class="text-gray-500 hover:text-gray-900 nav-link" data-page="shop">คอลเลคชั่นใหม่</a>
                        <a href="#" class="text-red-500 hover:text-red-700 font-semibold nav-link" data-page="shop">ลดราคา</a>
                    </div>

                    <!-- Icons -->
                    <div class="flex items-center space-x-4">
                        <button class="text-gray-500 hover:text-gray-900">
                            <i data-lucide="search" class="w-5 h-5"></i>
                        </button>
                        <button class="text-gray-500 hover:text-gray-900">
                            <i data-lucide="user" class="w-5 h-5"></i>
                        </button>
                        <button id="cart-button" class="relative text-gray-500 hover:text-gray-900">
                            <i data-lucide="shopping-bag" class="w-5 h-5"></i>
                            <span id="cart-count" class="absolute -top-2 -right-2 bg-red-500 text-white text-xs rounded-full w-4 h-4 flex items-center justify-center">3</span>
                        </button>
                        <button id="mobile-menu-button" class="md:hidden text-gray-500 hover:text-gray-900">
                            <i data-lucide="menu" class="w-6 h-6"></i>
                        </button>
                    </div>
                </div>
            </nav>
            <!-- Mobile Menu -->
            <div id="mobile-menu" class="hidden md:hidden px-4 pt-2 pb-4 space-y-2 border-t border-gray-200">
                <a href="#" class="block text-gray-600 hover:bg-gray-100 rounded p-2 nav-link" data-page="home">หน้าแรก</a>
                <a href="#" class="block text-gray-600 hover:bg-gray-100 rounded p-2 nav-link" data-page="shop">สินค้าทั้งหมด</a>
                <a href="#" class="block text-gray-600 hover:bg-gray-100 rounded p-2 nav-link" data-page="shop">คอลเลคชั่นใหม่</a>
                <a href="#" class="block text-red-500 hover:bg-red-50 rounded p-2 font-semibold nav-link" data-page="shop">ลดราคา</a>
            </div>
        </header>

        <!-- Main Content Area -->
        <main id="main-content">

            <!-- Home Page -->
            <section id="home" class="page active">
                <!-- Hero Section -->
                <div class="relative bg-gray-900">
                    <div class="absolute inset-0">
                        <img src="https://images.unsplash.com/photo-1523381294911-8d3cead13475?q=80&w=2070&auto=format&fit=crop" class="w-full h-full object-cover" alt="เสื้อผ้าแฟชั่น">
                        <div class="absolute inset-0 bg-gray-900/60"></div>
                    </div>
                    <div class="relative container mx-auto px-4 sm:px-6 lg:px-8 py-24 sm:py-32 text-center text-white">
                        <h1 class="text-4xl sm:text-5xl lg:text-6xl font-extrabold tracking-tight">Summer Collection 2025</h1>
                        <p class="mt-4 max-w-2xl mx-auto text-lg sm:text-xl text-gray-300">ค้นพบสไตล์ที่เป็นคุณกับคอลเลคชั่นใหม่ล่าสุดของเรา</p>
                        <button class="mt-8 bg-white text-gray-900 font-bold py-3 px-8 rounded-full hover:bg-gray-200 transition duration-300 transform hover:scale-105 nav-link" data-page="shop">
                            ช้อปเลย
                        </button>
                    </div>
                </div>

                <!-- Featured Products Section -->
                <div class="py-12 sm:py-16">
                    <div class="container mx-auto px-4 sm:px-6 lg:px-8">
                        <h2 class="text-2xl sm:text-3xl font-bold text-center mb-8">สินค้าแนะนำ</h2>
                        <div class="grid grid-cols-2 md:grid-cols-4 gap-4 sm:gap-6">
                            <!-- Product Card 1 -->
                            <div class="group cursor-pointer" onclick="navigateTo('product-detail')">
                                <div class="overflow-hidden rounded-lg bg-gray-100">
                                    <img src="https://placehold.co/400x500/e2e8f0/334155?text=Product+1" alt="สินค้า 1" class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-300">
                                </div>
                                <h3 class="mt-3 text-sm sm:text-base font-medium text-gray-800">เสื้อยืดลายกราฟิก</h3>
                                <p class="mt-1 text-base sm:text-lg font-semibold text-gray-900">฿790</p>
                            </div>
                            <!-- Product Card 2 -->
                            <div class="group cursor-pointer" onclick="navigateTo('product-detail')">
                                <div class="overflow-hidden rounded-lg bg-gray-100">
                                    <img src="https://placehold.co/400x500/d1d5db/334155?text=Product+2" alt="สินค้า 2" class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-300">
                                </div>
                                <h3 class="mt-3 text-sm sm:text-base font-medium text-gray-800">กางเกงยีนส์ขาสั้น</h3>
                                <p class="mt-1 text-base sm:text-lg font-semibold text-gray-900">฿1,290</p>
                            </div>
                            <!-- Product Card 3 -->
                            <div class="group cursor-pointer" onclick="navigateTo('product-detail')">
                                <div class="overflow-hidden rounded-lg bg-gray-100">
                                    <img src="https://placehold.co/400x500/bbf7d0/334155?text=Product+3" alt="สินค้า 3" class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-300">
                                </div>
                                <h3 class="mt-3 text-sm sm:text-base font-medium text-gray-800">หมวกแก๊ปสีเขียว</h3>
                                <p class="mt-1 text-base sm:text-lg font-semibold text-gray-900">฿550</p>
                            </div>
                            <!-- Product Card 4 -->
                            <div class="group cursor-pointer" onclick="navigateTo('product-detail')">
                                <div class="overflow-hidden rounded-lg bg-gray-100">
                                    <img src="https://placehold.co/400x500/fecaca/334155?text=Product+4" alt="สินค้า 4" class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-300">
                                </div>
                                <h3 class="mt-3 text-sm sm:text-base font-medium text-gray-800">รองเท้าผ้าใบสีแดง</h3>
                                <p class="mt-1 text-base sm:text-lg font-semibold text-gray-900">฿2,400</p>
                            </div>
                        </div>
                    </div>
                </div>
            </section>

            <!-- Shop Page (Product Listing) -->
            <section id="shop" class="page">
                <div class="container mx-auto px-4 sm:px-6 lg:px-8 py-8">
                    <h1 class="text-3xl font-bold mb-2">สินค้าทั้งหมด</h1>
                    <p class="text-gray-500 mb-6">พบกับสินค้ากว่า 128 รายการ</p>
                    
                    <!-- Filters -->
                    <div class="flex flex-col sm:flex-row justify-between items-center mb-6 gap-4">
                        <div class="flex space-x-2 overflow-x-auto pb-2">
                             <button class="bg-gray-200 text-gray-700 px-4 py-2 rounded-full text-sm font-medium whitespace-nowrap">หมวดหมู่</button>
                             <button class="bg-gray-200 text-gray-700 px-4 py-2 rounded-full text-sm font-medium whitespace-nowrap">ราคา</button>
                             <button class="bg-gray-200 text-gray-700 px-4 py-2 rounded-full text-sm font-medium whitespace-nowrap">สี</button>
                        </div>
                        <div class="flex-shrink-0">
                            <select class="border border-gray-300 rounded-full px-4 py-2 text-sm focus:ring-indigo-500 focus:border-indigo-500">
                                <option>เรียงตาม: ใหม่ล่าสุด</option>
                                <option>เรียงตาม: ราคาต่ำไปสูง</option>
                                <option>เรียงตาม: ราคาสูงไปต่ำ</option>
                            </select>
                        </div>
                    </div>

                    <!-- Product Grid -->
                    <div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-4 sm:gap-6">
                        <!-- Repeat Product Card for listing -->
                        <script>
                            for (let i = 1; i <= 12; i++) {
                                document.write(`
                                <div class="group cursor-pointer" onclick="navigateTo('product-detail')">
                                    <div class="overflow-hidden rounded-lg bg-gray-100">
                                        <img src="https://placehold.co/400x500/e2e8f0/334155?text=Item+${i}" alt="สินค้า ${i}" class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-300">
                                    </div>
                                    <h3 class="mt-3 text-sm sm:text-base font-medium text-gray-800">สินค้าตัวอย่าง ${i}</h3>
                                    <p class="mt-1 text-base sm:text-lg font-semibold text-gray-900">฿${Math.floor(Math.random() * 2000) + 500}</p>
                                </div>
                                `);
                            }
                        </script>
                    </div>
                </div>
            </section>

            <!-- Product Detail Page -->
            <section id="product-detail" class="page">
                 <div class="container mx-auto px-4 sm:px-6 lg:px-8 py-8">
                    <div class="grid md:grid-cols-2 gap-8 lg:gap-12">
                        <!-- Image Gallery -->
                        <div>
                            <div class="aspect-w-1 aspect-h-1 bg-gray-100 rounded-lg overflow-hidden mb-4">
                               <img id="main-product-image" src="https://placehold.co/600x600/e2e8f0/334155?text=Product" alt="Main product" class="w-full h-full object-cover">
                            </div>
                            <div class="grid grid-cols-4 gap-2">
                                <img src="https://placehold.co/150x150/e2e8f0/334155?text=View+1" class="cursor-pointer rounded-md border-2 border-indigo-500" onclick="changeImage('https://placehold.co/600x600/e2e8f0/334155?text=View+1')">
                                <img src="https://placehold.co/150x150/d1d5db/334155?text=View+2" class="cursor-pointer rounded-md border-2 border-transparent hover:border-indigo-500" onclick="changeImage('https://placehold.co/600x600/d1d5db/334155?text=View+2')">
                                <img src="https://placehold.co/150x150/bbf7d0/334155?text=View+3" class="cursor-pointer rounded-md border-2 border-transparent hover:border-indigo-500" onclick="changeImage('https://placehold.co/600x600/bbf7d0/334155?text=View+3')">
                                <img src="https://placehold.co/150x150/fecaca/334155?text=View+4" class="cursor-pointer rounded-md border-2 border-transparent hover:border-indigo-500" onclick="changeImage('https://placehold.co/600x600/fecaca/334155?text=View+4')">
                            </div>
                        </div>
                        <!-- Product Info -->
                        <div>
                            <h1 class="text-3xl lg:text-4xl font-bold">เสื้อยืดลายกราฟิก</h1>
                            <p class="text-2xl lg:text-3xl font-semibold mt-2 text-indigo-600">฿790</p>
                            
                            <div class="mt-4">
                                <h3 class="text-sm font-medium text-gray-900">สี</h3>
                                <div class="flex items-center space-x-3 mt-2">
                                    <label class="relative -m-0.5 flex cursor-pointer items-center justify-center rounded-full p-0.5 focus:outline-none ring-2 ring-indigo-500 ring-offset-1"><input type="radio" name="color-choice" value="White" class="sr-only"><span aria-hidden="true" class="h-8 w-8 bg-white rounded-full border border-black border-opacity-10"></span></label>
                                    <label class="relative -m-0.5 flex cursor-pointer items-center justify-center rounded-full p-0.5 focus:outline-none ring-gray-400"><input type="radio" name="color-choice" value="Gray" class="sr-only"><span aria-hidden="true" class="h-8 w-8 bg-gray-500 rounded-full border border-black border-opacity-10"></span></label>
                                    <label class="relative -m-0.5 flex cursor-pointer items-center justify-center rounded-full p-0.5 focus:outline-none ring-gray-400"><input type="radio" name="color-choice" value="Black" class="sr-only"><span aria-hidden="true" class="h-8 w-8 bg-black rounded-full border border-black border-opacity-10"></span></label>
                                </div>
                            </div>
                            
                            <div class="mt-6">
                                <h3 class="text-sm font-medium text-gray-900">ขนาด</h3>
                                <div class="grid grid-cols-4 gap-4 mt-2">
                                    <label class="group relative flex items-center justify-center rounded-md border py-3 px-4 text-sm font-medium uppercase hover:bg-gray-50 focus:outline-none cursor-pointer bg-white text-gray-900 shadow-sm"><input type="radio" name="size-choice" value="S" class="sr-only"><span>S</span></label>
                                    <label class="group relative flex items-center justify-center rounded-md border py-3 px-4 text-sm font-medium uppercase hover:bg-gray-50 focus:outline-none cursor-pointer bg-white text-gray-900 shadow-sm"><input type="radio" name="size-choice" value="M" class="sr-only"><span>M</span></label>
                                    <label class="group relative flex items-center justify-center rounded-md border py-3 px-4 text-sm font-medium uppercase hover:bg-gray-50 focus:outline-none cursor-pointer bg-white text-gray-900 shadow-sm"><input type="radio" name="size-choice" value="L" class="sr-only"><span>L</span></label>
                                    <label class="group relative flex items-center justify-center rounded-md border py-3 px-4 text-sm font-medium uppercase hover:bg-gray-50 focus:outline-none cursor-not-allowed bg-gray-50 text-gray-200"><input type="radio" name="size-choice" value="XL" disabled class="sr-only"><span>XL</span></label>
                                </div>
                            </div>
                            
                            <button class="mt-8 w-full bg-indigo-600 text-white font-bold py-3 px-8 rounded-lg hover:bg-indigo-700 transition duration-300 transform hover:scale-105 flex items-center justify-center">
                                <i data-lucide="shopping-cart" class="w-5 h-5 mr-2"></i>
                                เพิ่มลงตะกร้า
                            </button>

                            <div class="mt-8">
                                <h3 class="text-lg font-semibold">รายละเอียดสินค้า</h3>
                                <p class="text-gray-600 mt-2">เสื้อยืดคอตตอน 100% คุณภาพพรีเมียม สวมใส่สบาย ระบายอากาศได้ดี พิมพ์ลายกราฟิกสุดเท่ด้วยเทคนิคพิเศษ สีไม่ตก ไม่ซีด เหมาะสำหรับทุกโอกาส</p>
                            </div>
                        </div>
                    </div>
                </div>
            </section>
        </main>

        <!-- Footer -->
        <footer class="bg-gray-900 text-white">
            <div class="container mx-auto px-4 sm:px-6 lg:px-8 py-12">
                <div class="grid grid-cols-1 md:grid-cols-4 gap-8">
                    <div>
                        <h3 class="text-lg font-semibold">URBAN.</h3>
                        <p class="mt-2 text-gray-400 text-sm">แฟชั่นที่บ่งบอกความเป็นตัวคุณ</p>
                    </div>
                    <div>
                        <h3 class="text-base font-semibold">ช่วยเหลือ</h3>
                        <ul class="mt-4 space-y-2 text-sm">
                            <li><a href="#" class="text-gray-400 hover:text-white">คำถามที่พบบ่อย</a></li>
                            <li><a href="#" class="text-gray-400 hover:text-white">การจัดส่ง</a></li>
                            <li><a href="#" class="text-gray-400 hover:text-white">การคืนสินค้า</a></li>
                        </ul>
                    </div>
                    <div>
                        <h3 class="text-base font-semibold">เกี่ยวกับเรา</h3>
                        <ul class="mt-4 space-y-2 text-sm">
                            <li><a href="#" class="text-gray-400 hover:text-white">เรื่องราวของเรา</a></li>
                            <li><a href="#" class="text-gray-400 hover:text-white">ร่วมงานกับเรา</a></li>
                        </ul>
                    </div>
                    <div>
                        <h3 class="text-base font-semibold">ติดตามข่าวสาร</h3>
                        <p class="mt-2 text-gray-400 text-sm">รับโปรโมชั่นและข่าวสารก่อนใคร</p>
                        <div class="mt-4 flex">
                            <input type="email" placeholder="อีเมลของคุณ" class="w-full rounded-l-md border-0 bg-white/10 px-3 py-2 text-white placeholder-gray-400 focus:ring-0 sm:text-sm">
                            <button class="bg-indigo-600 rounded-r-md px-3 hover:bg-indigo-500"><i data-lucide="send" class="w-5 h-5"></i></button>
                        </div>
                    </div>
                </div>
                <div class="mt-8 border-t border-gray-800 pt-8 text-center text-sm text-gray-400">
                    <p>&copy; 2025 URBAN. All rights reserved.</p>
                </div>
            </div>
        </footer>

    </div>

    <!-- Shopping Cart Panel -->
    <div id="cart-panel" class="fixed inset-0 bg-black bg-opacity-50 z-50 hidden" aria-labelledby="slide-over-title" role="dialog" aria-modal="true">
      <div class="absolute inset-0" id="cart-overlay"></div>
      <div id="cart-content" class="fixed inset-y-0 right-0 flex max-w-full pl-10 transform transition ease-in-out duration-500 translate-x-full">
        <div class="w-screen max-w-md">
          <div class="flex h-full flex-col overflow-y-scroll bg-white shadow-xl">
            <div class="flex-1 overflow-y-auto px-4 py-6 sm:px-6">
              <div class="flex items-start justify-between">
                <h2 class="text-lg font-medium text-gray-900" id="slide-over-title">ตะกร้าสินค้า</h2>
                <div class="ml-3 flex h-7 items-center">
                  <button type="button" id="close-cart-button" class="relative -m-2 p-2 text-gray-400 hover:text-gray-500">
                    <i data-lucide="x" class="w-6 h-6"></i>
                  </button>
                </div>
              </div>

              <div class="mt-8">
                <div class="flow-root">
                  <ul role="list" class="-my-6 divide-y divide-gray-200">
                    <!-- Cart Item 1 -->
                    <li class="flex py-6">
                      <div class="h-24 w-24 flex-shrink-0 overflow-hidden rounded-md border border-gray-200">
                        <img src="https://placehold.co/100x100/e2e8f0/334155?text=Item" alt="Product" class="h-full w-full object-cover object-center">
                      </div>
                      <div class="ml-4 flex flex-1 flex-col">
                        <div>
                          <div class="flex justify-between text-base font-medium text-gray-900">
                            <h3><a href="#">เสื้อยืดลายกราฟิก</a></h3>
                            <p class="ml-4">฿790</p>
                          </div>
                          <p class="mt-1 text-sm text-gray-500">สีขาว / ไซส์ M</p>
                        </div>
                        <div class="flex flex-1 items-end justify-between text-sm">
                          <p class="text-gray-500">จำนวน: 1</p>
                          <div class="flex">
                            <button type="button" class="font-medium text-indigo-600 hover:text-indigo-500">ลบ</button>
                          </div>
                        </div>
                      </div>
                    </li>
                    <!-- Cart Item 2 -->
                    <li class="flex py-6">
                      <div class="h-24 w-24 flex-shrink-0 overflow-hidden rounded-md border border-gray-200">
                        <img src="https://placehold.co/100x100/d1d5db/334155?text=Item" alt="Product" class="h-full w-full object-cover object-center">
                      </div>
                      <div class="ml-4 flex flex-1 flex-col">
                        <div>
                          <div class="flex justify-between text-base font-medium text-gray-900">
                            <h3><a href="#">กางเกงยีนส์ขาสั้น</a></h3>
                            <p class="ml-4">฿1,290</p>
                          </div>
                           <p class="mt-1 text-sm text-gray-500">สีฟ้า / ไซส์ L</p>
                        </div>
                        <div class="flex flex-1 items-end justify-between text-sm">
                          <p class="text-gray-500">จำนวน: 1</p>
                          <div class="flex">
                            <button type="button" class="font-medium text-indigo-600 hover:text-indigo-500">ลบ</button>
                          </div>
                        </div>
                      </div>
                    </li>
                  </ul>
                </div>
              </div>
            </div>

            <div class="border-t border-gray-200 px-4 py-6 sm:px-6">
              <div class="flex justify-between text-base font-medium text-gray-900">
                <p>ยอดรวม</p>
                <p>฿2,080</p>
              </div>
              <p class="mt-0.5 text-sm text-gray-500">ค่าจัดส่งจะถูกคำนวณในขั้นตอนชำระเงิน</p>
              <div class="mt-6">
                <a href="#" class="flex items-center justify-center rounded-md border border-transparent bg-indigo-600 px-6 py-3 text-base font-medium text-white shadow-sm hover:bg-indigo-700">ชำระเงิน</a>
              </div>
              <div class="mt-6 flex justify-center text-center text-sm text-gray-500">
                <p>
                  หรือ
                  <button type="button" id="continue-shopping-button" class="font-medium text-indigo-600 hover:text-indigo-500">
                    เลือกซื้อสินค้าต่อ
                    <span aria-hidden="true"> &rarr;</span>
                  </button>
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>


    <script>
        document.addEventListener('DOMContentLoaded', function () {
            // Initialize Lucide Icons
            lucide.createIcons();

            const pages = document.querySelectorAll('.page');
            const navLinks = document.querySelectorAll('.nav-link');
            const mainContent = document.getElementById('main-content');
            
            // --- Page Navigation Logic ---
            function showPage(pageId) {
                pages.forEach(page => {
                    page.classList.remove('active');
                });
                const newPage = document.getElementById(pageId);
                if (newPage) {
                    newPage.classList.add('active');
                    // Scroll to top on page change
                    window.scrollTo(0, 0);
                }
                
                // Update active nav link style
                navLinks.forEach(link => {
                    if (link.dataset.page === pageId) {
                        link.classList.add('nav-link-active');
                    } else {
                        link.classList.remove('nav-link-active');
                    }
                });
                
                // Close mobile menu on navigation
                document.getElementById('mobile-menu').classList.add('hidden');
            }

            navLinks.forEach(link => {
                link.addEventListener('click', function (e) {
                    e.preventDefault();
                    const pageId = this.dataset.page;
                    showPage(pageId);
                });
            });

            // Make the initial page active
            showPage('home');

            // --- Global Navigation Function ---
            window.navigateTo = function(pageId) {
                showPage(pageId);
            }

            // --- Product Detail Image Changer ---
            window.changeImage = function(newSrc) {
                document.getElementById('main-product-image').src = newSrc;
                // Update active thumbnail border
                const thumbnails = document.querySelectorAll('.grid.grid-cols-4 img');
                thumbnails.forEach(thumb => {
                    if (thumb.src.includes(newSrc.split('/').pop().split('?')[0])) {
                        thumb.classList.add('border-indigo-500');
                        thumb.classList.remove('border-transparent');
                    } else {
                        thumb.classList.remove('border-indigo-500');
                        thumb.classList.add('border-transparent');
                    }
                });
            }

            // --- Mobile Menu Toggle ---
            const mobileMenuButton = document.getElementById('mobile-menu-button');
            const mobileMenu = document.getElementById('mobile-menu');
            mobileMenuButton.addEventListener('click', function () {
                mobileMenu.classList.toggle('hidden');
            });

            // --- Shopping Cart Panel Logic ---
            const cartPanel = document.getElementById('cart-panel');
            const cartContent = document.getElementById('cart-content');
            const cartButton = document.getElementById('cart-button');
            const closeCartButton = document.getElementById('close-cart-button');
            const cartOverlay = document.getElementById('cart-overlay');
            const continueShoppingButton = document.getElementById('continue-shopping-button');

            function openCart() {
                cartPanel.classList.remove('hidden');
                document.body.style.overflow = 'hidden'; // Prevent background scroll
                setTimeout(() => {
                    cartContent.classList.remove('translate-x-full');
                }, 10);
            }

            function closeCart() {
                cartContent.classList.add('translate-x-full');
                setTimeout(() => {
                    cartPanel.classList.add('hidden');
                    document.body.style.overflow = '';
                }, 500);
            }

            cartButton.addEventListener('click', openCart);
            closeCartButton.addEventListener('click', closeCart);
            cartOverlay.addEventListener('click', closeCart);
            continueShoppingButton.addEventListener('click', closeCart);
        });
    </script>
</body>
</html>
