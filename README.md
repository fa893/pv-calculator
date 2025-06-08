<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PV Calculator - حاسبة الطاقة الشمسية</title>
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- أيقونات -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- خط عربي -->
    <link href="https://fonts.googleapis.com/css2?family=Tajawal:wght@400;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Tajawal', sans-serif;
        }
        .card-hover:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
        }
        @media (max-width: 768px) {
            nav ul {
                flex-direction: column;
                gap: 0.5rem;
            }
        }
    </style>
</head>
<body class="bg-gray-50 min-h-screen flex flex-col">
    <!-- Header ثابت لجميع الصفحات -->
    <header class="bg-blue-900 text-white shadow-lg sticky top-0 z-50">
        <div class="container mx-auto px-4 py-3 flex flex-col md:flex-row justify-between items-center">
            <div class="flex items-center space-x-2 mb-4 md:mb-0">
                <i class="fas fa-solar-panel text-2xl text-yellow-400"></i>
                <h1 class="text-xl font-bold">PV Calculator</h1>
            </div>
            <nav>
                <ul class="flex flex-wrap justify-center gap-4 md:gap-6">
                    <li><a href="index.html" class="hover:text-yellow-400 flex items-center"><i class="fas fa-home ml-1"></i> الرئيسية</a></li>
                    <li><a href="services.html" class="hover:text-yellow-400 flex items-center"><i class="fas fa-tools ml-1"></i> الخدمات</a></li>
                    <li><a href="blog.html" class="hover:text-yellow-400 flex items-center"><i class="fas fa-blog ml-1"></i> المدونة</a></li>
                    <li><a href="about.html" class="hover:text-yellow-400 flex items-center"><i class="fas fa-info-circle ml-1"></i> من نحن</a></li>
                    <li><a href="contact.html" class="hover:text-yellow-400 flex items-center"><i class="fas fa-envelope ml-1"></i> اتصل بنا</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- المحتوى الديناميكي (يتغير حسب الصفحة) -->
    <main class="flex-grow container mx-auto px-4 py-8">
        <!-- الصفحة الرئيسية -->
        <div id="home-page">
            <section class="text-center mb-12">
                <h2 class="text-3xl font-bold text-blue-800 mb-4">حاسبة الطاقة الشمسية الذكية</h2>
                <p class="text-gray-700 max-w-2xl mx-auto">أداة متكاملة لتصميم أنظمة الطاقة الشمسية بدقة، سواء كنت مستخدمًا عاديًا أو مهندسًا متخصصًا.</p>
                <img src="https://via.placeholder.com/800x400?text=Solar+Panel+System" alt="أنظمة شمسية" class="mx-auto mt-6 rounded-lg shadow-md w-full max-w-2xl">
            </section>

            <section class="grid grid-cols-1 md:grid-cols-3 gap-6 mb-12">
                <div class="bg-white p-6 rounded-lg shadow-md border-t-4 border-blue-600 transition duration-300 card-hover">
                    <i class="fas fa-bolt text-3xl text-blue-600 mb-3"></i>
                    <h3 class="text-xl font-semibold mb-2">حساب الاستهلاك</h3>
                    <p class="text-gray-600">أدخل استهلاكك الكهربائي أو ارفع فاتورة الكهرباء.</p>
                </div>
                <div class="bg-white p-6 rounded-lg shadow-md border-t-4 border-green-600 transition duration-300 card-hover">
                    <i class="fas fa-map-marked-alt text-3xl text-green-600 mb-3"></i>
                    <h3 class="text-xl font-semibold mb-2">تحديد الموقع</h3>
                    <p class="text-gray-600">اختر موقعك لحساب الإشعاع الشمسي بدقة.</p>
                </div>
                <div class="bg-white p-6 rounded-lg shadow-md border-t-4 border-yellow-600 transition duration-300 card-hover">
                    <i class="fas fa-chart-line text-3xl text-yellow-600 mb-3"></i>
                    <h3 class="text-xl font-semibold mb-2">النتائج والتقارير</h3>
                    <p class="text-gray-600">احصل على تقرير مفصل مع توصيات مخصصة.</p>
                </div>
            </section>

            <div class="text-center">
                <a href="services.html" class="bg-blue-600 hover:bg-blue-700 text-white font-bold py-3 px-8 rounded-full inline-flex items-center transition duration-300">
                    ابدأ الآن <i class="fas fa-arrow-left mr-2"></i>
                </a>
            </div>
        </div>

        <!-- صفحة الخدمات -->
        <div id="services-page" class="hidden">
            <h2 class="text-3xl font-bold text-blue-800 mb-8 text-center">خدمات حاسبة الطاقة الشمسية</h2>
            
            <div class="bg-white rounded-lg shadow-md p-6 mb-8">
                <h3 class="text-2xl font-semibold text-green-700 mb-4 flex items-center">
                    <i class="fas fa-user mr-2"></i> وضع المستخدم العادي
                </h3>
                <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                    <div class="border border-gray-200 rounded-lg p-4">
                        <h4 class="font-bold mb-2 flex items-center"><i class="fas fa-bolt text-yellow-500 mr-2"></i> حساب الاستهلاك</h4>
                        <p class="text-gray-600 mb-3">أدخل استهلاكك الشهري بالكيلوواط ساعة:</p>
                        <input type="number" class="w-full p-2 border border-gray-300 rounded mb-3" placeholder="مثال: 500 kWh">
                        <button class="bg-blue-600 text-white px-4 py-2 rounded hover:bg-blue-700">حساب</button>
                    </div>
                    <div class="border border-gray-200 rounded-lg p-4">
                        <h4 class="font-bold mb-2 flex items-center"><i class="fas fa-upload text-blue-500 mr-2"></i> رفع فاتورة الكهرباء</h4>
                        <div class="border-2 border-dashed border-gray-300 rounded-lg p-4 text-center">
                            <i class="fas fa-file-invoice text-3xl text-gray-400 mb-2"></i>
                            <p class="text-gray-500">اسحب وأسقط ملف الفاتورة هنا أو</p>
                            <button class="mt-2 bg-gray-200 hover:bg-gray-300 px-4 py-2 rounded">اختر ملف</button>
                        </div>
                    </div>
                </div>
            </div>

            <div class="bg-white rounded-lg shadow-md p-6">
                <h3 class="text-2xl font-semibold text-blue-700 mb-4 flex items-center">
                    <i class="fas fa-user-cog mr-2"></i> وضع المهندس المختص
                </h3>
                <div class="space-y-6">
                    <div>
                        <h4 class="font-bold mb-2"><i class="fas fa-solar-panel mr-2 text-orange-500"></i> مواصفات الألواح</h4>
                        <div class="grid grid-cols-1 md:grid-cols-3 gap-4">
                            <select class="p-2 border border-gray-300 rounded">
                                <option>نوع اللوح الشمسي</option>
                                <option>Mono-crystalline</option>
                                <option>Poly-crystalline</option>
                                <option>Thin Film</option>
                            </select>
                            <input type="number" class="p-2 border border-gray-300 rounded" placeholder="قدرة اللوح (W)">
                            <input type="number" class="p-2 border border-gray-300 rounded" placeholder="الكفاءة (%)">
                        </div>
                    </div>
                    <div>
                        <h4 class="font-bold mb-2"><i class="fas fa-map-marker-alt mr-2 text-green-500"></i> بيانات الموقع</h4>
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                            <input type="text" class="p-2 border border-gray-300 rounded" placeholder="المدينة">
                            <div class="flex space-x-2">
                                <input type="number" class="p-2 border border-gray-300 rounded flex-grow" placeholder="زاوية الميل">
                                <input type="number" class="p-2 border border-gray-300 rounded flex-grow" placeholder="الاتجاه (0-360)">
                            </div>
                        </div>
                    </div>
                    <button class="bg-green-600 hover:bg-green-700 text-white font-bold py-2 px-6 rounded">
                        <i class="fas fa-calculator mr-2"></i> احسب النظام
                    </button>
                </div>
            </div>
        </div>

        <!-- صفحة من نحن -->
        <div id="about-page" class="hidden">
            <div class="max-w-4xl mx-auto">
                <h2 class="text-3xl font-bold text-blue-800 mb-8 text-center">من نحن</h2>
                
                <div class="bg-white rounded-lg shadow-md p-6 mb-8">
                    <div class="flex flex-col md:flex-row items-center mb-6">
                        <img src="https://via.placeholder.com/150?text=Team" alt="فريق العمل" class="rounded-full w-32 h-32 object-cover mb-4 md:mb-0 md:mr-6">
                        <div>
                            <h3 class="text-2xl font-semibold text-blue-700">فريق PV Calculator</h3>
                            <p class="text-gray-600 mt-2">نحن فريق من خبراء الطاقة المتجددة والمطورين الذين يعملون على تبسيط تقنيات الطاقة الشمسية للجميع.</p>
                        </div>
                    </div>
                    
                    <div class="space-y-6">
                        <div>
                            <h4 class="text-xl font-semibold text-green-700 mb-3 flex items-center">
                                <i class="fas fa-bullseye mr-2"></i> رؤيتنا
                            </h4>
                            <p class="text-gray-700">تقديم أدوات ذكية تساعد في انتشار أنظمة الطاقة الشمسية في العالم العربي بطريقة سهلة ومبسطة.</p>
                        </div>
                        
                        <div>
                            <h4 class="text-xl font-semibold text-blue-700 mb-3 flex items-center">
                                <i class="fas fa-chart-line mr-2"></i> إحصائيات
                            </h4>
                            <div class="grid grid-cols-2 md:grid-cols-4 gap-4 text-center">
                                <div class="bg-blue-50 p-4 rounded-lg">
                                    <div class="text-3xl font-bold text-blue-600">+500</div>
                                    <div class="text-gray-600">نظام محسوب</div>
                                </div>
                                <div class="bg-green-50 p-4 rounded-lg">
                                    <div class="text-3xl font-bold text-green-600">+3</div>
                                    <div class="text-gray-600">سنوات خبرة</div>
                                </div>
                                <div class="bg-yellow-50 p-4 rounded-lg">
                                    <div class="text-3xl font-bold text-yellow-600">10</div>
                                    <div class="text-gray-600">دولة عربية</div>
                                </div>
                                <div class="bg-purple-50 p-4 rounded-lg">
                                    <div class="text-3xl font-bold text-purple-600">98%</div>
                                    <div class="text-gray-600">رضا العملاء</div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- صفحة المدونة -->
        <div id="blog-page" class="hidden">
            <h2 class="text-3xl font-bold text-blue-800 mb-8 text-center">مدونة الطاقة الشمسية</h2>
            
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
                <div class="bg-white rounded-lg shadow-md overflow-hidden hover:shadow-lg transition duration-300">
                    <img src="https://via.placeholder.com/400x250?text=Blog+1" alt="مقال 1" class="w-full h-48 object-cover">
                    <div class="p-4">
                        <div class="text-sm text-blue-600 mb-2">15 مايو 2024</div>
                        <h3 class="text-xl font-semibold mb-2">كيف تختار نظام الطاقة الشمسية المنزلية؟</h3>
                        <p class="text-gray-600 mb-4">دليل مفصل لاختيار النظام الأمثل لمنزلك مع مقارنة بين الخيارات المتاحة.</p>
                        <a href="#" class="text-blue-600 hover:text-blue-800 font-medium">اقرأ المزيد →</a>
                    </div>
                </div>
                
                <div class="bg-white rounded-lg shadow-md overflow-hidden hover:shadow-lg transition duration-300">
                    <img src="https://via.placeholder.com/400x250?text=Blog+2" alt="مقال 2" class="w-full h-48 object-cover">
                    <div class="p-4">
                        <div class="text-sm text-blue-600 mb-2">2 أبريل 2024</div>
                        <h3 class="text-xl font-semibold mb-2">أحدث تقنيات الألواح الشمسية 2024</h3>
                        <p class="text-gray-600 mb-4">تعرف على أحدث التطورات في عالم الخلايا الشمسية وكيفية الاستفادة منها.</p>
                        <a href="#" class="text-blue-600 hover:text-blue-800 font-medium">اقرأ المزيد →</a>
                    </div>
                </div>
                
                <div class="bg-white rounded-lg shadow-md overflow-hidden hover:shadow-lg transition duration-300">
                    <img src="https://via.placeholder.com/400x250?text=Blog+3" alt="مقال 3" class="w-full h-48 object-cover">
                    <div class="p-4">
                        <div class="text-sm text-blue-600 mb-2">20 مارس 2024</div>
                        <h3 class="text-xl font-semibold mb-2">حساب العائد المالي للنظام الشمسي</h3>
                        <p class="text-gray-600 mb-4">كيف تحسب فترة استرداد تكلفة النظام الشمسي وتوفيرك المالي على المدى البعيد.</p>
                        <a href="#" class="text-blue-600 hover:text-blue-800 font-medium">اقرأ المزيد →</a>
                    </div>
                </div>
            </div>
            
            <div class="mt-8 text-center">
                <button class="bg-blue-600 hover:bg-blue-700 text-white font-bold py-2 px-6 rounded">
                    عرض المزيد من المقالات
                </button>
            </div>
        </div>

        <!-- صفحة اتصل بنا -->
        <div id="contact-page" class="hidden">
            <div class="max-w-4xl mx-auto">
                <h2 class="text-3xl font-bold text-blue-800 mb-8 text-center">اتصل بنا</h2>
                
                <div class="bg-white rounded-lg shadow-md p-6">
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
                        <div>
                            <h3 class="text-xl font-semibold text-blue-700 mb-4">نموذج التواصل</h3>
                            <form class="space-y-4">
                                <div>
                                    <label class="block text-gray-700 mb-1">الاسم الكامل</label>
                                    <input type="text" class="w-full p-2 border border-gray-300 rounded">
                                </div>
                                <div>
                                    <label class="block text-gray-700 mb-1">البريد الإلكتروني</label>
                                    <input type="email" class="w-full p-2 border border-gray-300 rounded">
                                </div>
                                <div>
                                    <label class="block text-gray-700 mb-1">رقم الهاتف</label>
                                    <input type="tel" class="w-full p-2 border border-gray-300 rounded">
                                </div>
                                <div>
                                    <label class="block text-gray-700 mb-1">الرسالة</label>
                                    <textarea rows="4" class="w-full p-2 border border-gray-300 rounded"></textarea>
                                </div>
                                <button type="submit" class="bg-blue-600 hover:bg-blue-700 text-white font-bold py-2 px-6 rounded">
                                    إرسال الرسالة
                                </button>
                            </form>
                        </div>
                        
                        <div>
                            <h3 class="text-xl font-semibold text-blue-700 mb-4">معلومات التواصل</h3>
                            <div class="space-y-4">
                                <div class="flex items-start">
                                    <i class="fas fa-map-marker-alt text-2xl text-blue-600 mt-1 mr-3"></i>
                                    <div>
                                        <h4 class="font-semibold">العنوان</h4>
                                        <p class="text-gray-600">شارع الملك عبدالله، الرياض، المملكة العربية السعودية</p>
                                    </div>
                                </div>
                                <div class="flex items-start">
                                    <i class="fas fa-phone-alt text-2xl text-green-600 mt-1 mr-3"></i>
                                    <div>
                                        <h4 class="font-semibold">الهاتف</h4>
                                        <p class="text-gray-600">+966 12 345 6789</p>
                                    </div>
                                </div>
                                <div class="flex items-start">
                                    <i class="fas fa-envelope text-2xl text-red-600 mt-1 mr-3"></i>
                                    <div>
                                        <h4 class="font-semibold">البريد الإلكتروني</h4>
                                        <p class="text-gray-600">info@pvcCalculator.com</p>
                                    </div>
                                </div>
                            </div>
                            
                            <div class="mt-6">
                                <h4 class="font-semibold mb-2">ساعات العمل</h4>
                                <ul class="space-y-2 text-gray-600">
                                    <li class="flex justify-between">
                                        <span>الأحد - الخميس:</span>
                                        <span>8 ص - 5 م</span>
                                    </li>
                                    <li class="flex justify-between">
                                        <span>الجمعة - السبت:</span>
                                        <span>إجازة</span>
                                    </li>
                                </ul>
                            </div>
                            
                            <div class="mt-6">
                                <h4 class="font-semibold mb-2">تابعنا على</h4>
                                <div class="flex space-x-4">
                                    <a href="#" class="text-blue-600 hover:text-blue-800 text-2xl"><i class="fab fa-twitter"></i></a>
                                    <a href="#" class="text-blue-700 hover:text-blue-900 text-2xl"><i class="fab fa-facebook"></i></a>
                                    <a href="#" class="text-red-600 hover:text-red-800 text-2xl"><i class="fab fa-youtube"></i></a>
                                    <a href="#" class="text-purple-600 hover:text-purple-800 text-2xl"><i class="fab fa-instagram"></i></a>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </main>

    <!-- Footer ثابت لجميع الصفحات -->
    <footer class="bg-gray-800 text-white py-8 mt-12">
        <div class="container mx-auto px-4">
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <div>
                    <h4 class="text-lg font-bold mb-4">PV Calculator</h4>
                    <p>أداة متقدمة لحساب أنظمة الطاقة الشمسية بدقة وكفاءة.</p>
                </div>
                <div>
                    <h4 class="text-lg font-bold mb-4">روابط سريعة</h4>
                    <ul class="space-y-2">
                        <li><a href="index.html" class="hover:text-yellow-400">الرئيسية</a></li>
                        <li><a href="services.html" class="hover:text-yellow-400">الخدمات</a></li>
                        <li><a href="blog.html" class="hover:text-yellow-400">المدونة</a></li>
                    </ul>
                </div>
                <div>
                    <h4 class="text-lg font-bold mb-4">تواصل معنا</h4>
                    <div class="flex space-x-4">
                        <a href="#" class="text-blue-400 hover:text-white"><i class="fab fa-facebook-f"></i></a>
                        <a href="#" class="text-blue-400 hover:text-white"><i class="fab fa-twitter"></i></a>
                        <a href="#" class="text-red-400 hover:text-white"><i class="fab fa-youtube"></i></a>
                    </div>
                </div>
            </div>
            <hr class="border-gray-700 my-6">
            <p class="text-center text-gray-400">© 2024 PV Calculator. جميع الحقوق محفوظة.</p>
        </div>
    </footer>

    <!-- JavaScript للتبديل بين الصفحات -->
    <script>
        // تحديد الصفحة الحالية من عنوان URL
        function showPage() {
            const path = window.location.pathname.split('/').pop();
            const pageId = path.replace('.html', '-page');
            
            // إخفاء جميع الصفحات
            document.querySelectorAll('main > div').forEach(div => {
                div.classList.add('hidden');
            });
            
            // إظهار الصفحة المطلوبة
            const currentPage = document.getElementById(pageId) || document.getElementById('home-page');
            if(currentPage) currentPage.classList.remove('hidden');
        }
        
        // تشغيل عند تحميل الصفحة
        document.addEventListener('DOMContentLoaded', showPage);
    </script>
</body>
</html>
