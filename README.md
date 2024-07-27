# rose-store
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>متجر الورود</title>
    <style>
        body {
            background-color: white;
            font-family: Arial, sans-serif;
            color: #333;
            direction: rtl;
        }
        header {
            background-color: #f8f9fa;
            padding: 10px 20px;
            text-align: center;
            border-bottom: 2px solid #e9ecef;
        }
        header h1 {
            margin: 0;
            color: #007bff;
        }
        nav ul {
            list-style: none;
            padding: 0;
        }
        nav ul li {
            display: inline;
            margin: 0 10px;
        }
        nav ul li a {
            text-decoration: none;
            color: #007bff;
        }
        section {
            padding: 20px;
        }
        #flowers .flower {
            border: 1px solid #e9ecef;
            padding: 10px;
            margin: 10px 0;
            background-color: #f8f9fa;
            display: inline-block;
            width: 45%;
            vertical-align: top;
            box-sizing: border-box;
        }
        #flowers .flower div {
            width: 100%;
            height: 150px;
            margin-bottom: 10px;
        }
        #flowers .flower .red { background-color: red; }
        #flowers .flower .yellow { background-color: yellow; }
        #flowers .flower .green { background-color: green; }
        #flowers .flower .orange { background-color: orange; }
        #flowers .flower .purple { background-color: purple; }
        #flowers .flower .blue { background-color: blue; }
        .flower p {
            margin: 5px 0;
        }
        .price {
            font-weight: bold;
            color: #007bff;
        }
        footer {
            text-align: center;
            padding: 10px 0;
            background-color: #f8f9fa;
            border-top: 2px solid #e9ecef;
            margin-top: 20px;
        }
        .contact-form {
            display: flex;
            flex-direction: column;
        }
        .contact-form label, .contact-form input, .contact-form textarea, .contact-form button {
            margin: 5px 0;
        }
        .order-info {
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <header>
        <h1>متجر الورود</h1>
        <nav>
            <ul>
                <li><a href="#home">الرئيسية</a></li>
                <li><a href="#flowers">الورود</a></li>
                <li><a href="#contact">التواصل</a></li>
            </ul>
        </nav>
    </header>

    <section id="home">
        <h2>مرحبا بكم في متجر الورود</h2>
        <p>نحن نقدم أجمل وأجود أنواع الورود لتناسب جميع مناسباتكم.</p>
    </section>

    <section id="flowers">
        <h2>أنواع الورود</h2>
        <div class="flower">
            <div class="red"></div>
            <h3>الورد الأحمر</h3>
            <p>الورد الأحمر يرمز إلى الحب والرومانسية. يُعتبر خيارًا مثاليًا للتعبير عن المشاعر العميقة.</p>
            <p class="price">السعر: 10 ريال</p>
        </div>
        <div class="flower">
            <div class="yellow"></div>
            <h3>التوليب</h3>
            <p>التوليب هو رمز للربيع والتجديد. يتميز بألوانه الزاهية وشكله الأنيق.</p>
            <p class="price">السعر: 15 ريال</p>
        </div>
        <div class="flower">
            <div class="green"></div>
            <h3>الزنبق</h3>
            <p>الزنبق يُعبر عن النقاء والجمال. يُستخدم في المناسبات الراقية والحفلات.</p>
            <p class="price">السعر: 20 ريال</p>
        </div>
        <div class="flower">
            <div class="orange"></div>
            <h3>دوار الشمس</h3>
            <p>دوار الشمس يرمز إلى الفرح والإيجابية. يضفي لمسة مشرقة وحيوية على أي مكان.</p>
            <p class="price">السعر: 12 ريال</p>
        </div>
        <div class="flower">
            <div class="purple"></div>
            <h3>الأوركيد</h3>
            <p>الأوركيد هو رمز للترف والجمال الغريب. يتميز بأزهاره الفريدة وألوانه المتنوعة.</p>
            <p class="price">السعر: 25 ريال</p>
        </div>
        <div class="flower">
            <div class="blue"></div>
            <h3>ديزي</h3>
            <p>الديزي يرمز إلى البراءة والنقاء. زهوره البيضاء والبسيطة تضفي لمسة من الهدوء.</p>
            <p class="price">السعر: 8 ريال</p>
        </div>
        <!-- إضافة المزيد من الورود هنا -->
    </section>

    <section id="orders">
        <h2>الطلبات</h2>
        <div class="order-info">
            <p>عدد الأشخاص الذين اشتروا: <span id="purchasedCount">0</span></p>
            <p>عدد الأشخاص في انتظار الطلب: <span id="pendingCount">0</span></p>
        </div>
    </section>

    <section id="contact">
        <h2>تواصل معنا</h2>
        <form class="contact-form">
            <label for="name">الاسم:</label>
            <input type="text" id="name" name="name" required>
            <label for="email">البريد الإلكتروني:</label>
            <input type="email" id="email" name="email" required>
            <label for="message">الرسالة:</label>
            <textarea id="message" name="message" required></textarea>
            <button type="submit">إرسال</button>
        </form>
    </section>

    <footer>
        <p>© 2024 متجر الورود</p>
    </footer>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            // عدد الأشخاص الذين اشتروا
            let purchasedCount = 150; // مثال: يمكن تحديث الرقم بناءً على البيانات الحقيقية
            // عدد الأشخاص في انتظار الطلب
            let pendingCount = 25; // مثال: يمكن تحديث الرقم بناءً على البيانات الحقيقية

            document.getElementById('purchasedCount').textContent = purchasedCount;
            document.getElementById('pendingCount').textContent = pendingCount;
        });
    </script>
</body>
</html>
