<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>منصة خدمات الجرف وإعادة الإعمار</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
    <style>
        :root {
            --primary-brown: #8B4513;
            --secondary-brown: #A0522D;
            --accent-gold: #DAA520;
            --light-brown: #DEB887;
            --light-beige: #F5F5DC;
            --dark-brown: #5D4037;
            --white: #ffffff;
            --shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            --transition: all 0.3s ease;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: var(--light-beige);
            color: var(--dark-brown);
            line-height: 1.6;
        }
        
        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* الهيدر */
        header {
            background: linear-gradient(135deg, var(--primary-brown) 0%, var(--secondary-brown) 100%);
            color: var(--white);
            padding: 1rem 0;
            box-shadow: var(--shadow);
            position: sticky;
            top: 0;
            z-index: 1000;
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .logo i {
            font-size: 2rem;
            color: var(--accent-gold);
        }
        
        .logo h1 {
            font-size: 1.8rem;
        }
        
        .logo span {
            color: var(--light-brown);
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            margin-right: 1.5rem;
        }
        
        nav ul li:last-child {
            margin-right: 0;
        }
        
        nav ul li a {
            color: var(--white);
            text-decoration: none;
            font-weight: 600;
            transition: var(--transition);
            padding: 0.5rem 1rem;
            border-radius: 4px;
        }
        
        nav ul li a:hover, nav ul li a.active {
            background-color: rgba(255, 255, 255, 0.1);
            color: var(--light-brown);
        }
        
        .mobile-menu-btn {
            display: none;
            background: none;
            border: none;
            color: var(--white);
            font-size: 1.5rem;
            cursor: pointer;
        }
        
        /* القسم الرئيسي */
        .hero {
            background: linear-gradient(rgba(139, 69, 19, 0.85), rgba(139, 69, 19, 0.9)), url('https://images.unsplash.com/photo-1504307651254-35680f356dfd?ixlib=rb-4.0.3&auto=format&fit=crop&w=1470&q=80');
            background-size: cover;
            background-position: center;
            color: var(--white);
            padding: 4rem 0;
            text-align: center;
        }
        
        .hero h2 {
            font-size: 2.5rem;
            margin-bottom: 1rem;
        }
        
        .hero p {
            font-size: 1.2rem;
            max-width: 800px;
            margin: 0 auto 2rem;
        }
        
        .btn {
            display: inline-block;
            background-color: var(--accent-gold);
            color: var(--dark-brown);
            padding: 0.8rem 2rem;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            transition: var(--transition);
            border: none;
            cursor: pointer;
            font-size: 1rem;
        }
        
        .btn:hover {
            background-color: var(--light-brown);
            transform: translateY(-3px);
            box-shadow: var(--shadow);
        }
        
        /* قسم الخدمات */
        .services {
            padding: 4rem 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 3rem;
            color: var(--primary-brown);
            position: relative;
        }
        
        .section-title:after {
            content: '';
            position: absolute;
            width: 100px;
            height: 4px;
            background-color: var(--accent-gold);
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
        }
        
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }
        
        .service-card {
            background-color: var(--white);
            border-radius: 10px;
            overflow: hidden;
            box-shadow: var(--shadow);
            transition: var(--transition);
            cursor: pointer;
        }
        
        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.15);
        }
        
        .service-icon {
            height: 200px;
            background-size: cover;
            background-position: center;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--white);
            font-size: 3rem;
            position: relative;
        }
        
        .service-icon:after {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background-color: rgba(139, 69, 19, 0.7);
        }
        
        .service-icon i {
            z-index: 1;
            background-color: rgba(218, 165, 32, 0.8);
            border-radius: 50%;
            padding: 20px;
        }
        
        .service-info {
            padding: 1.5rem;
            text-align: center;
        }
        
        .service-info h3 {
            color: var(--primary-brown);
            margin-bottom: 1rem;
        }
        
        /* قسم الحرفيين */
        .workers-section {
            background-color: var(--white);
            padding: 4rem 0;
            border-radius: 10px;
            margin: 2rem 0;
            box-shadow: var(--shadow);
        }
        
        .workers-container {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }
        
        .worker-card {
            background-color: var(--light-beige);
            border-radius: 10px;
            overflow: hidden;
            box-shadow: var(--shadow);
            transition: var(--transition);
            position: relative;
        }
        
        .worker-card:hover {
            transform: translateY(-5px);
        }
        
        .worker-img {
            height: 200px;
            background-size: cover;
            background-position: center;
        }
        
        .worker-info {
            padding: 1.5rem;
        }
        
        .worker-info h3 {
            color: var(--primary-brown);
            margin-bottom: 0.5rem;
        }
        
        .worker-specialty {
            color: var(--accent-gold);
            font-weight: 600;
            margin-bottom: 0.5rem;
        }
        
        .worker-rating {
            color: #ffc107;
            margin-bottom: 1rem;
        }
        
        .worker-details {
            display: none;
            padding: 1rem;
            background-color: var(--white);
            border-top: 1px solid var(--light-brown);
        }
        
        .worker-details.active {
            display: block;
            animation: slideDown 0.5s ease;
        }
        
        @keyframes slideDown {
            from {
                opacity: 0;
                transform: translateY(-20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        .worker-contact-btn {
            background-color: var(--accent-gold);
            color: var(--dark-brown);
            border: none;
            padding: 0.5rem 1.5rem;
            border-radius: 4px;
            cursor: pointer;
            transition: var(--transition);
            margin-top: 1rem;
            width: 100%;
            font-weight: 600;
        }
        
        .worker-contact-btn:hover {
            background-color: var(--light-brown);
        }
        
        /* قسم جدول الأسعار */
        .pricing-section {
            padding: 4rem 0;
        }
        
        .pricing-table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 2rem;
            background-color: var(--white);
            border-radius: 10px;
            overflow: hidden;
            box-shadow: var(--shadow);
        }
        
        .pricing-table th {
            background-color: var(--primary-brown);
            color: var(--white);
            padding: 1.2rem;
            text-align: right;
            font-size: 1.1rem;
        }
        
        .pricing-table td {
            padding: 1rem;
            border-bottom: 1px solid var(--light-beige);
        }
        
        .pricing-table tr:nth-child(even) {
            background-color: var(--light-beige);
        }
        
        .pricing-table tr:hover {
            background-color: rgba(222, 184, 135, 0.2);
        }
        
        .price-tag {
            background-color: var(--accent-gold);
            color: var(--dark-brown);
            padding: 0.3rem 1rem;
            border-radius: 20px;
            font-weight: 600;
            display: inline-block;
        }
        
        /* قسم التواصل */
        .contact-section {
            background-color: var(--primary-brown);
            color: var(--white);
            padding: 4rem 0;
            border-radius: 10px;
            margin: 2rem 0;
        }
        
        .contact-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }
        
        .contact-form {
            background-color: var(--white);
            padding: 2rem;
            border-radius: 10px;
            color: var(--dark-brown);
        }
        
        .form-group {
            margin-bottom: 1.5rem;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 600;
        }
        
        .form-control {
            width: 100%;
            padding: 0.8rem;
            border: 1px solid var(--light-brown);
            border-radius: 4px;
            font-size: 1rem;
            background-color: var(--light-beige);
        }
        
        .form-control:focus {
            outline: none;
            border-color: var(--accent-gold);
            box-shadow: 0 0 0 3px rgba(218, 165, 32, 0.2);
        }
        
        textarea.form-control {
            min-height: 150px;
            resize: vertical;
        }
        
        .contact-info {
            padding: 1rem;
        }
        
        .contact-info h3 {
            color: var(--light-brown);
            margin-bottom: 1.5rem;
        }
        
        .contact-item {
            display: flex;
            align-items: center;
            margin-bottom: 1.5rem;
        }
        
        .contact-item i {
            background-color: var(--accent-gold);
            color: var(--dark-brown);
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-left: 1rem;
            flex-shrink: 0;
        }
        
        /* الفوتر */
        footer {
            background-color: var(--primary-brown);
            color: var(--white);
            padding: 3rem 0 1.5rem;
            margin-top: 3rem;
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-bottom: 2rem;
        }
        
        .footer-column h3 {
            color: var(--light-brown);
            margin-bottom: 1.5rem;
            font-size: 1.2rem;
        }
        
        .footer-column ul {
            list-style: none;
        }
        
        .footer-column ul li {
            margin-bottom: 0.8rem;
        }
        
        .footer-column ul li a {
            color: var(--light-beige);
            text-decoration: none;
            transition: var(--transition);
        }
        
        .footer-column ul li a:hover {
            color: var(--accent-gold);
            padding-right: 5px;
        }
        
        .copyright {
            text-align: center;
            padding-top: 1.5rem;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: var(--light-brown);
            font-size: 0.9rem;
        }
        
        /* التجاوب مع الشاشات الصغيرة */
        @media (max-width: 992px) {
            .hero h2 {
                font-size: 2rem;
            }
            
            .services-grid, .workers-container {
                grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            }
        }
        
        @media (max-width: 768px) {
            nav ul {
                display: none;
                position: absolute;
                top: 100%;
                right: 0;
                background-color: var(--primary-brown);
                width: 100%;
                flex-direction: column;
                padding: 1rem 0;
                box-shadow: var(--shadow);
            }
            
            nav ul.show {
                display: flex;
            }
            
            nav ul li {
                margin: 0;
                text-align: center;
            }
            
            nav ul li a {
                display: block;
                padding: 1rem;
            }
            
            .mobile-menu-btn {
                display: block;
            }
            
            .header-content {
                flex-wrap: wrap;
            }
            
            .pricing-table {
                display: block;
                overflow-x: auto;
            }
        }
        
        @media (max-width: 480px) {
            .hero h2 {
                font-size: 1.8rem;
            }
            
            .hero p {
                font-size: 1rem;
            }
            
            .section-title {
                font-size: 1.5rem;
            }
            
            .services-grid, .workers-container {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <!-- الهيدر -->
    <header>
        <div class="container">
            <div class="header-content">
                <div class="logo">
                    <i class="fas fa-hard-hat"></i>
                    <h1>خدمات <span>الجرف</span></h1>
                </div>
                
                <button class="mobile-menu-btn" id="mobileMenuBtn">
                    <i class="fas fa-bars"></i>
                </button>
                
                <nav>
                    <ul id="mainNav">
                        <li><a href="#" class="active">الرئيسية</a></li>
                        <li><a href="#services">الخدمات</a></li>
                        <li><a href="#workers">الحرفيين</a></li>
                        <li><a href="#pricing">الأسعار</a></li>
                        <li><a href="#contact">التواصل</a></li>
                    </ul>
                </nav>
            </div>
        </div>
    </header>

    <!-- القسم الرئيسي -->
    <section class="hero">
        <div class="container">
            <h2>منصة خدمات الجرف وإعادة الإعمار</h2>
            <p>منصة متخصصة للربط بين أصحاب المنازل والحرفيين المحترفين في مجالات الكهرباء، السباكة، النجارة، والبناء. نوفر حلولاً سريعة وموثوقة لإعادة الإعمار.</p>
            <a href="#workers" class="btn">ابحث عن حرفي</a>
        </div>
    </section>

    <!-- قسم الخدمات -->
    <section id="services" class="services">
        <div class="container">
            <h2 class="section-title">خدماتنا المتخصصة</h2>
            
            <div class="services-grid">
                <div class="service-card">
                    <div class="service-icon" style="background-image: url('https://images.unsplash.com/photo-1621905252507-b35492cc74b4?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80');">
                        <i class="fas fa-bolt"></i>
                    </div>
                    <div class="service-info">
                        <h3>خدمات الكهرباء</h3>
                        <p>تركيب وإصلاح الأنظمة الكهربائية المنزلية والتجارية</p>
                    </div>
                </div>
                
                <div class="service-card">
                    <div class="service-icon" style="background-image: url('https://images.unsplash.com/photo-1607472586893-edb57bdc0e39?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80');">
                        <i class="fas fa-faucet"></i>
                    </div>
                    <div class="service-info">
                        <h3>خدمات السباكة</h3>
                        <p>تركيب وإصلاح الأنابيب والتجهيزات الصحية</p>
                    </div>
                </div>
                
                <div class="service-card">
                    <div class="service-icon" style="background-image: url('https://images.unsplash.com/photo-1586023492125-27b2c045efd7?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80');">
                        <i class="fas fa-hammer"></i>
                    </div>
                    <div class="service-info">
                        <h3>خدمات النجارة</h3>
                        <p>أعمال النجارة المنزلية والأثاث والديكورات الخشبية</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- قسم الحرفيين -->
    <section id="workers" class="workers-section">
        <div class="container">
            <h2 class="section-title">الحرفيون المتميزون</h2>
            <p class="text-center" style="margin-bottom: 2rem; color: var(--secondary-brown);">انقر على أي حرفي لعرض التفاصيل والتواصل المباشر</p>
            
            <div class="workers-container" id="workersContainer">
                <!-- سيتم إضافة الحرفيين عبر JavaScript -->
            </div>
        </div>
    </section>

    <!-- قسم جدول الأسعار -->
    <section id="pricing" class="pricing-section">
        <div class="container">
            <h2 class="section-title">جدول الأسعار التقديرية</h2>
            
            <table class="pricing-table">
                <thead>
                    <tr>
                        <th>نوع الخدمة</th>
                        <th>التفاصيل</th>
                        <th>السعر التقريبي</th>
                        <th>مدة التنفيذ</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>تركيب كهرباء منزل</td>
                        <td>تركيب نظام كهربائي كامل لمنزل متوسط</td>
                        <td><span class="price-tag">1500 - 3000 ريال</span></td>
                        <td>3 - 5 أيام</td>
                    </tr>
                    <tr>
                        <td>إصلاح تسرب مياه</td>
                        <td>كشف وإصلاح تسرب في الأنابيب الرئيسية</td>
                        <td><span class="price-tag">200 - 500 ريال</span></td>
                        <td>2 - 6 ساعات</td>
                    </tr>
                    <tr>
                        <td>تركيب أثاث خشبي</td>
                        <td>تركيب خزانة مطبخ أو غرفة نوم</td>
                        <td><span class="price-tag">800 - 1500 ريال</span></td>
                        <td>1 - 3 أيام</td>
                    </tr>
                    <tr>
                        <td>دهان وتشطيب</td>
                        <td>دهان جدران غرفة واحدة مع التشطيب</td>
                        <td><span class="price-tag">500 - 1000 ريال</span></td>
                        <td>1 - 2 أيام</td>
                    </tr>
                    <tr>
                        <td>صيانة عامة</td>
                        <td>فحص وصيانة دورية للأنظمة المنزلية</td>
                        <td><span class="price-tag">300 - 600 ريال</span></td>
                        <td>3 - 8 ساعات</td>
                    </tr>
                </tbody>
            </table>
        </div>
    </section>

    <!-- قسم التواصل -->
    <section id="contact" class="contact-section">
        <div class="container">
            <h2 class="section-title" style="color: var(--white);">تواصل معنا</h2>
            
            <div class="contact-container">
                <div class="contact-form">
                    <h3 style="color: var(--primary-brown); margin-bottom: 1.5rem;">اطلب خدمة</h3>
                    <form id="serviceRequestForm">
                        <div class="form-group">
                            <label for="name">الاسم الكامل</label>
                            <input type="text" id="name" class="form-control" required>
                        </div>
                        
                        <div class="form-group">
                            <label for="phone">رقم الهاتف</label>
                            <input type="tel" id="phone" class="form-control" required>
                        </div>
                        
                        <div class="form-group">
                            <label for="service">نوع الخدمة المطلوبة</label>
                            <select id="service" class="form-control" required>
                                <option value="">اختر الخدمة</option>
                                <option value="electricity">كهرباء</option>
                                <option value="plumbing">سباكة</option>
                                <option value="carpentry">نجارة</option>
                                <option value="painting">دهان</option>
                                <option value="other">خدمة أخرى</option>
                            </select>
                        </div>
                        
                        <div class="form-group">
                            <label for="description">وصف المشكلة/الخدمة</label>
                            <textarea id="description" class="form-control" required></textarea>
                        </div>
                        
                        <button type="submit" class="btn" style="width: 100%;">إرسال الطلب</button>
                    </form>
                </div>
                
                <div class="contact-info">
                    <h3>معلومات التواصل</h3>
                    
                    <div class="contact-item">
                        <i class="fas fa-map-marker-alt"></i>
                        <div>
                            <h4>العنوان</h4>
                            <p>منصة خدمات الجرف - خدمة محلية</p>
                        </div>
                    </div>
                    
                    <div class="contact-item">
                        <i class="fas fa-phone-alt"></i>
                        <div>
                            <h4>الهاتف</h4>
                            <p>+966 55 123 4567</p>
                        </div>
                    </div>
                    
                    <div class="contact-item">
                        <i class="fas fa-envelope"></i>
                        <div>
                            <h4>البريد الإلكتروني</h4>
                            <p>info@services-platform.com</p>
                        </div>
                    </div>
                    
                    <div class="contact-item">
                        <i class="fas fa-clock"></i>
                        <div>
                            <h4>أوقات العمل</h4>
                            <p>24/7 - خدمة طوارئ متاحة</p>
                        </div>
                    </div>
                    
                    <div class="contact-item">
                        <i class="fas fa-users"></i>
                        <div>
                            <h4>الحرفيون المسجلون</h4>
                            <p>أكثر من 100 حرفي معتمد</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- الفوتر -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3>خدمات الجرف</h3>
                    <p>منصة محلية تهدف إلى تيسير الوصول للحرفيين المحترفين في مجالات إعادة الإعمار والبناء. نوفر حلولاً سريعة وموثوقة.</p>
                </div>
                
                <div class="footer-column">
                    <h3>روابط سريعة</h3>
                    <ul>
                        <li><a href="#">الرئيسية</a></li>
                        <li><a href="#services">الخدمات</a></li>
                        <li><a href="#workers">الحرفيين</a></li>
                        <li><a href="#pricing">الأسعار</a></li>
                        <li><a href="#contact">طلب خدمة</a></li>
                    </ul>
                </div>
                
                <div class="footer-column">
                    <h3>أنواع الخدمات</h3>
                    <ul>
                        <li><a href="#">خدمات الكهرباء</a></li>
                        <li><a href="#">خدمات السباكة</a></li>
                        <li><a href="#">خدمات النجارة</a></li>
                        <li><a href="#">خدمات الدهان</a></li>
                        <li><a href="#">خدمات البناء</a></li>
                    </ul>
                </div>
                
                <div class="footer-column">
                    <h3>تابعنا</h3>
                    <div style="display: flex; gap: 15px; margin-top: 1rem;">
                        <a href="#" style="color: var(--white); font-size: 1.5rem;"><i class="fab fa-whatsapp"></i></a>
                        <a href="#" style="color: var(--white); font-size: 1.5rem;"><i class="fab fa-twitter"></i></a>
                        <a href="#" style="color: var(--white); font-size: 1.5rem;"><i class="fab fa-instagram"></i></a>
                        <a href="#" style="color: var(--white); font-size: 1.5rem;"><i class="fab fa-youtube"></i></a>
                    </div>
                </div>
            </div>
            
            <div class="copyright">
                <p>© 2023 منصة خدمات الجرف وإعادة الإعمار. جميع الحقوق محفوظة. | نسعى لإعادة البناء معاً</p>
            </div>
        </div>
    </footer>

    <script>
        // بيانات الحرفيين
        const workers = [
            {
                id: 1,
                name: "أحمد محمد",
                specialty: "كهرباء",
                experience: "15 سنة",
                rating: 4.8,
                image: "https://images.unsplash.com/photo-1581094794329-c8112a89af12?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80",
                description: "متخصص في التركيبات الكهربائية المنزلية والتجارية، مع خبرة واسعة في أنظمة الطاقة الشمسية.",
                phone: "0551234567",
                priceRange: "1500-3000 ريال"
            },
            {
                id: 2,
                name: "سعيد العتيبي",
                specialty: "سباكة",
                experience: "12 سنة",
                rating: 4.7,
                image: "https://images.unsplash.com/photo-1584622650111-993a426fbf0a?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80",
                description: "خبير في إصلاح التسريبات وتركيب الأنظمة الصحية، مع مهارات في أنظمة التدفئة المركزية.",
                phone: "0552345678",
                priceRange: "800-2000 ريال"
            },
            {
                id: 3,
                name: "خالد الحربي",
                specialty: "نجارة",
                experience: "18 سنة",
                rating: 4.9,
                image: "https://images.unsplash.com/photo-1560253023-3ec5d502959f?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80",
                description: "حرفي متميز في صناعة الأثاث الخشبي والديكورات المنزلية بأجود أنواع الخشب.",
                phone: "0553456789",
                priceRange: "2000-5000 ريال"
            },
            {
                id: 4,
                name: "فارس القحطاني",
                specialty: "بناء",
                experience: "20 سنة",
                rating: 4.8,
                image: "https://images.unsplash.com/photo-1568605114967-8130f3a36994?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80",
                description: "مقاول بناء محترف مع خبرة في إعادة الإعمار والترميم للمباني المتضررة.",
                phone: "0554567890",
                priceRange: "5000-15000 ريال"
            },
            {
                id: 5,
                name: "ماجد الشمري",
                specialty: "دهان",
                experience: "10 سنوات",
                rating: 4.6,
                image: "https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80",
                description: "متخصص في أعمال الدهان والتشطيبات النهائية بأحدث التقنيات والمواد.",
                phone: "0555678901",
                priceRange: "1000-3000 ريال"
            },
            {
                id: 6,
                name: "نواف الزهراني",
                specialty: "تكييف وتبريد",
                experience: "8 سنوات",
                rating: 4.5,
                image: "https://images.unsplash.com/photo-1504593811423-6dd665756598?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80",
                description: "فني تكييف معتمد لجميع الماركات العالمية مع صيانة دورية وتركيب أنظمة جديدة.",
                phone: "0556789012",
                priceRange: "800-2500 ريال"
            }
        ];

        // عرض الحرفيين
        function renderWorkers() {
            const container = document.getElementById('workersContainer');
            container.innerHTML = '';
            
            workers.forEach(worker => {
                const starRating = '★'.repeat(Math.floor(worker.rating)) + '☆'.repeat(5 - Math.floor(worker.rating));
                
                const workerCard = `
                    <div class="worker-card" data-worker-id="${worker.id}">
                        <div class="worker-img" style="background-image: url('${worker.image}');"></div>
                        <div class="worker-info">
                            <h3>${worker.name}</h3>
                            <div class="worker-specialty">${worker.specialty}</div>
                            <div class="worker-rating">${starRating} (${worker.rating})</div>
                            <p>خبرة: ${worker.experience}</p>
                            <button class="worker-contact-btn" onclick="showWorkerDetails(${worker.id})">
                                عرض التفاصيل
                            </button>
                        </div>
                        <div class="worker-details" id="details-${worker.id}">
                            <p><strong>التخصص:</strong> ${worker.specialty}</p>
                            <p><strong>الوصف:</strong> ${worker.description}</p>
                            <p><strong>نطاق الأسعار:</strong> ${worker.priceRange}</p>
                            <p><strong>رقم الهاتف:</strong> ${worker.phone}</p>
                            <button class="btn" onclick="contactWorker('${worker.name}', '${worker.phone}')" style="width: 100%; margin-top: 10px;">
                                <i class="fas fa-phone"></i> اتصل الآن
                            </button>
                        </div>
                    </div>
                `;
                
                container.innerHTML += workerCard;
            });
        }

        // عرض تفاصيل الحرفي مع jQuery Slide
        function showWorkerDetails(workerId) {
            // إغلاق جميع التفاصيل المفتوحة
            $('.worker-details').not(`#details-${workerId}`).slideUp().removeClass('active');
            
            // فتح/إغلاق التفاصيل المحددة
            $(`#details-${workerId}`).slideToggle().toggleClass('active');
        }

        // التواصل مع الحرفي
        function contactWorker(workerName, phoneNumber) {
            alert(`سيتصل بك ${workerName} على الرقم ${phoneNumber} خلال دقائق`);
        }

        // القائمة المتنقلة للهواتف
        document.addEventListener('DOMContentLoaded', function() {
            renderWorkers();
            
            const mobileMenuBtn = document.getElementById('mobileMenuBtn');
            const mainNav = document.getElementById('mainNav');
            
            mobileMenuBtn.addEventListener('click', function() {
                mainNav.classList.toggle('show');
            });
            
            // إغلاق القائمة عند النقر على رابط
            const navLinks = document.querySelectorAll('#mainNav a');
            navLinks.forEach(link => {
                link.addEventListener('click', function() {
                    mainNav.classList.remove('show');
                });
            });
            
            // نموذج طلب الخدمة
            const serviceForm = document.getElementById('serviceRequestForm');
            serviceForm.addEventListener('submit', function(e) {
                e.preventDefault();
                
                const serviceType = document.getElementById('service').value;
                const serviceNames = {
                    'electricity': 'كهرباء',
                    'plumbing': 'سباكة',
                    'carpentry': 'نجارة',
                    'painting': 'دهان',
                    'other': 'خدمة أخرى'
                };
                
                alert(`تم استلام طلبك لخدمة ${serviceNames[serviceType]}. سيتصل بك أحد ممثلينا خلال 30 دقيقة.`);
                serviceForm.reset();
            });
            
            // التنقل السلس
            document.querySelectorAll('a[href^="#"]').forEach(anchor => {
                anchor.addEventListener('click', function(e) {
                    e.preventDefault();
                    
                    const targetId = this.getAttribute('href');
                    if (targetId === '#') return;
                    
                    const targetElement = document.querySelector(targetId);
                    if (targetElement) {
                        window.scrollTo({
                            top: targetElement.offsetTop - 80,
                            behavior: 'smooth'
                        });
                    }
                });
            });
            
            // تأثير التمرير على الهيدر
            window.addEventListener('scroll', function() {
                const header = document.querySelector('header');
                if (window.scrollY > 50) {
                    header.style.boxShadow = '0 6px 12px rgba(0, 0, 0, 0.15)';
                } else {
                    header.style.boxShadow = '0 4px 6px rgba(0, 0, 0, 0.1)';
                }
            });
            
            // تأثير Hover على بطاقات الخدمات
            const serviceCards = document.querySelectorAll('.service-card');
            serviceCards.forEach(card => {
                card.addEventListener('mouseenter', function() {
                    this.style.transform = 'translateY(-10px) scale(1.02)';
                });
                
                card.addEventListener('mouseleave', function() {
                    this.style.transform = 'translateY(0) scale(1)';
                });
            });
        });
    </script>
</body>
</html>
