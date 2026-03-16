<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>我的设计作品</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            line-height: 1.6;
            color: #333;
            background-color: #f8f9fa;
        }

        a {
            text-decoration: none;
            color: inherit;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

       
        /* 导航栏样式 */
        nav {
            background-color: white;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            position: fixed;
            top: 0;
            width: 100%;
            z-index: 100;
        }

        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 0;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: 700;
            color: #2c3e50;
        }

        /* 背景设置样式 */
        .background-settings {
            padding: 20px 0;
            background-color: #fff;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            margin-top: 70px;
        }

        .background-settings h3 {
            text-align: center;
            margin-bottom: 20px;
            color: #2c3e50;
        }

        .background-settings input {
            width: 300px;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 5px;
            margin-right: 10px;
        }

        .background-settings button {
            padding: 10px 20px;
            background-color: #3498db;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        .background-settings button:hover {
            background-color: #2980b9;
        }

        /* 图片展示区样式 */
        .images {
            padding: 100px 0;
            background-color: #f8f9fa;
        }

        .image-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
        }

        .image-grid img {
            width: 100%;
            height: auto;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            transition: transform 0.3s;
        }

        .image-grid img:hover {
            transform: scale(1.05);
        }

        /* 页脚样式 */
        footer {
            background-color: #2c3e50;
            color: white;
            text-align: center;
            padding: 30px 0;
        }

        /* 响应式调整 */
        @media (max-width: 768px) {
            .image-grid {
                grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            }
        }

        /* 平滑滚动 */
        html {
            scroll-behavior: smooth;
        }

        /* 模态框样式 */
        .modal {
            display: none;
            position: fixed;
            z-index: 1000;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0,0,0,0.9);
            justify-content: center;
            align-items: center;
        }

        .modal-content {
            display: block;
            max-width: 90%;
            max-height: 90%;
            width: auto;
            height: auto;
        }

        .close {
            position: absolute;
            top: 15px;
            right: 35px;
            color: #f1f1f1;
            font-size: 40px;
            font-weight: bold;
            transition: 0.3s;
            cursor: pointer;
        }

        .close:hover,
        .close:focus {
            color: #bbb;
            text-decoration: none;
        }

        .prev, .next {
            position: absolute;
            top: 50%;
            transform: translateY(-50%);
            color: #f1f1f1;
            font-size: 40px;
            font-weight: bold;
            cursor: pointer;
            transition: 0.3s;
            user-select: none;
        }

        .prev {
            left: 15px;
        }

        .next {
            right: 15px;
        }

        .prev:hover, .next:hover {
            color: #bbb;
        }
    </style>
</head>
<body>
    <!-- 导航栏 -->
    <nav>
        <div class="container nav-container">
            <div class="logo">Bonnie</div>
        </div>
    </nav>

    <!-- 图片展示 -->
    <section class="images">
        <div class="container">
            <h2 style="text-align: center; font-size: 2.5rem; margin-bottom: 60px; color: #2c3e50;">个人作品展示</h2>
            <div class="image-grid">
                 <img src="https://bonnie-2020-1411039470.cos.ap-guangzhou.myqcloud.com/2026/0.jpg" alt="图片2" width="1920" height="1080">
                <img src="https://bonnie-2020-1411039470.cos.ap-guangzhou.myqcloud.com/2026/2022%20%281%29.jpg" alt="图片3" width="1920" height="1080">
                <img src="https://bonnie-2020-1411039470.cos.ap-guangzhou.myqcloud.com/2026/3-1.jpg" alt="图片2" width="1920" height="1080">
                <img src="https://bonnie-2020-1411039470.cos.ap-guangzhou.myqcloud.com/2026/3-0.jpg" alt="图片3" width="1920" height="1080">
                <img src="https://bonnie-2020-1411039470.cos.ap-guangzhou.myqcloud.com/2026/3-3.jpg"  alt="图片4" width="1920" height="1080">
                <img src="https://bonnie-2020-1411039470.cos.ap-guangzhou.myqcloud.com/2026/3-2.jpg" alt="图片5" width="1920" height="1080">
                <img src="https://bonnie-2020-1411039470.cos.ap-guangzhou.myqcloud.com/2026/6-1.png" alt="图片6" width="1920" height="1080">
                <img src="https://bonnie-2020-1411039470.cos.ap-guangzhou.myqcloud.com/2026/5-3.jpg" alt="图片7" width="1920" height="1080">
                <img src="https://bonnie-2020-1411039470.cos.ap-guangzhou.myqcloud.com/2026/4-2.jpg" alt="图片7" width="1920" height="1080">
                <img src="https://bonnie-2020-1411039470.cos.ap-guangzhou.myqcloud.com/2026/5-1.jpg" alt="图片8" width="1920" height="1080">
                <img src="https://bonnie-2020-1411039470.cos.ap-guangzhou.myqcloud.com/2026/7-1.jpg" alt="图片9" width="1920" height="1080">
                <img src="https://bonnie-2020-1411039470.cos.ap-guangzhou.myqcloud.com/2026/4-1.jpg" alt="图片10" width="1920" height="1080">
                <img src="https://bonnie-2020-1411039470.cos.ap-guangzhou.myqcloud.com/2026/7-2.jpg" alt="图片11" width="1920" height="1080">
                <img src="https://bonnie-2020-1411039470.cos.ap-guangzhou.myqcloud.com/2026/6-3.jpg" alt="图片30" width="1920" height="1080">
                <img src="https://bonnie-2020-1411039470.cos.ap-guangzhou.myqcloud.com/2026/6-1.jpg" alt="图片28" width="1920" height="1080">
                <img src="https://bonnie-2020-1411039470.cos.ap-guangzhou.myqcloud.com/2026/6-2.jpg" alt="图片29" width="1920" height="1080">
                <img src="https://bonnie-2020-1411039470.cos.ap-guangzhou.myqcloud.com/2026/7-3.jpg" alt="图片19" width="1920" height="1080">
                <img src="https://bonnie-2020-1411039470.cos.ap-guangzhou.myqcloud.com/2026/6-4.jpg" alt="图片20" width="1920" height="1080">
                <img src="https://bonnie-2020-1411039470.cos.ap-guangzhou.myqcloud.com/2026/8-1.jpg" alt="图片20" width="1920" height="1080">
                <img src="https://bonnie-2020-1411039470.cos.ap-guangzhou.myqcloud.com/2026/2022%20%282%29.jpg" alt="图片21" width="1920" height="1080">
                <img src="https://bonnie-2020-1411039470.cos.ap-guangzhou.myqcloud.com/2026/2022%20%283%29.jpg" alt="图片22" width="1920" height="1080">
                <img src="https://bonnie-2020-1411039470.cos.ap-guangzhou.myqcloud.com/2026/2022%20%284%29.jpg" alt="图片23" width="1920" height="1080">
                <img src="https://bonnie-2020-1411039470.cos.ap-guangzhou.myqcloud.com/2026/2022%20%285%29.jpg" alt="图片24" width="1920" height="1080">
                <img src="https://bonnie-2020-1411039470.cos.ap-guangzhou.myqcloud.com/2026/2022%20%286%29.jpg" alt="图片25" width="1920" height="1080">
                <img src="https://bonnie-2020-1411039470.cos.ap-guangzhou.myqcloud.com/2026/2022%20%287%29.jpg" alt="图片26" width="1920" height="1080">
                <img src="https://bonnie-2020-1411039470.cos.ap-guangzhou.myqcloud.com/2026/2022%20%288%29.jpg" alt="图片27" width="1920" height="1080">
            </div>
        </div>
    </section>

    <!-- 模态框 -->
    <div id="modal" class="modal">
        <span class="close">&times;</span>
        <span class="prev">&lt;</span>
        <span class="next">&gt;</span>
        <img class="modal-content" id="modal-img">
    </div>

 
    <!-- 页脚 -->
    <footer>
        <div class="container">
            <p>&copy; 2026 Bonnie | 保留所有权利</p>
        </div>
    </footer>

    <script>
        // 获取模态框元素
        var modal = document.getElementById("modal");
        var modalImg = document.getElementById("modal-img");
        var closeBtn = document.getElementsByClassName("close")[0];
        var prevBtn = document.querySelector('.prev');
        var nextBtn = document.querySelector('.next');
        var currentIndex;

        // 为每个图片添加点击事件
        var images = document.querySelectorAll(".image-grid img");
        images.forEach(function(img, index) {
            img.onclick = function() {
                modal.style.display = "flex";
                modalImg.src = this.src;
                currentIndex = index;
            }
        });

        // 关闭模态框
        closeBtn.onclick = function() {
            modal.style.display = "none";
        }

        // 点击模态框背景关闭
        modal.onclick = function(event) {
            if (event.target == modal) {
                modal.style.display = "none";
            }
        }

        // 上一张图片
        prevBtn.onclick = function(e) {
            e.stopPropagation();
            currentIndex = (currentIndex - 1 + images.length) % images.length;
            modalImg.src = images[currentIndex].src;
        }

        // 下一张图片
        nextBtn.onclick = function(e) {
            e.stopPropagation();
            currentIndex = (currentIndex + 1) % images.length;
            modalImg.src = images[currentIndex].src;
        }

        // 键盘导航
        document.addEventListener('keydown', function(e) {
            if (modal.style.display === 'block') {
                if (e.key === 'ArrowLeft') {
                    prevBtn.click();
                } else if (e.key === 'ArrowRight') {
                    nextBtn.click();
                } else if (e.key === 'Escape') {
                    modal.style.display = 'none';
                }
            }
        });
    </script>
</body>
</html>
