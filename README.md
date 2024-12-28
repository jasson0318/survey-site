<!DOCTYPE html>
<html lang="zh-Hant">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>藥師服務滿意度調查</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin: 0;
            padding: 20px;
        }
        .page {
            display: none;
        }
        .page.active {
            display: block;
        }
        .emotions {
            display: flex;
            justify-content: center;
            gap: 10px;
            margin-top: 20px;
        }
        .emotions img {
            width: 100px;
            height: 200px;
            cursor: pointer;
            transition: transform 0.2s;
        }
        .emotions img:hover {
            transform: scale(1.1);
        }
        img.coupon {
            max-width: 600px;
            cursor: pointer;
            transition: transform 0.2s;
        }
        img.coupon:hover {
            transform: scale(1.05);
        }
    </style>
</head>
<body>
    <!-- Page 1: Satisfaction Survey -->
    <div class="page active" id="page1">
        <h1>藥師服務滿意度調查</h1>
        <div class="emotions">
            <!-- 每個表情圖案作為獨立連結 -->
            <a href="#page2" onclick="showPage('page2')">
                <img src="happy.png.png" alt="非常滿意">
            </a>
            <a href="#page2" onclick="showPage('page2')">
                <img src="satisfied.png.png" alt="滿意">
            </a>
            <a href="#page2" onclick="showPage('page2')">
                <img src="neutral.png.png" alt="普通">
            </a>
            <a href="#page2" onclick="showPage('page2')">
                <img src="unsatisfied.png.png" alt="不滿意">
            </a>
            <a href="#page2" onclick="showPage('page2')">
                <img src="very_unsatisfied.png.png" alt="非常不滿意">
            </a>
        </div>
    </div>

    <!-- Page 2: Discount Coupon -->
    <div class="page" id="page2">
        <h1>10元商品優惠券</h1>
        <!-- 點擊優惠券圖片啟動列印功能 -->
        <img src="coupon_image.png.jpg" alt="優惠券" class="coupon" onclick="window.print()">
    </div>

    <script>
        function showPage(pageId) {
            document.querySelectorAll('.page').forEach(page => page.classList.remove('active'));
            document.getElementById(pageId).classList.add('active');
        }
    </script>
</body>
</html>
