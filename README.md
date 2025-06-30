<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>迁知社 | Mindshift Society</title>
    <style>
        :root {
            --primary: #4a6fa5;
            --secondary: #166088;
            --accent: #4fc3f7;
            --light: #f8f9fa;
            --dark: #212529;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }
        
        body {
            background-color: var(--light);
            color: var(--dark);
            line-height: 1.6;
        }
        
        header {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white;
            padding: 2rem 0;
            text-align: center;
            position: relative;
            overflow: hidden;
        }
        
        .header-content {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
            position: relative;
            z-index: 2;
        }
        
        .logo {
            font-size: 2.5rem;
            font-weight: 700;
            margin-bottom: 0.5rem;
        }
        
        .slogan {
            font-size: 1.2rem;
            opacity: 0.9;
            margin-bottom: 1.5rem;
        }
        
        nav {
            background-color: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            padding: 1rem;
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        .nav-container {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .nav-links {
            display: flex;
            list-style: none;
        }
        
        .nav-links li {
            margin-left: 2rem;
        }
        
        .nav-links a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
        }
        
        .nav-links a:hover {
            color: var(--accent);
        }
        
        .mobile-menu-btn {
            display: none;
            background: none;
            border: none;
            color: white;
            font-size: 1.5rem;
            cursor: pointer;
        }
        
        main {
            max-width: 1200px;
            margin: 2rem auto;
            padding: 0 20px;
        }
        
        section {
            margin-bottom: 3rem;
        }
        
        h2 {
            color: var(--secondary);
            margin-bottom: 1.5rem;
            position: relative;
            padding-bottom: 0.5rem;
        }
        
        h2::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 60px;
            height: 3px;
            background-color: var(--accent);
        }
        
        .mission-statement {
            background-color: white;
            padding: 2rem;
            border-radius: 8px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            margin-bottom: 2rem;
        }
        
        .activities-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }
        
        .activity-card {
            background-color: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s;
        }
        
        .activity-card:hover {
            transform: translateY(-5px);
        }
        
        .card-img {
            height: 200px;
            background-color: var(--primary);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 2rem;
        }
        
        .card-content {
            padding: 1.5rem;
        }
        
        .card-content h3 {
            margin-bottom: 1rem;
            color: var(--secondary);
        }
        
        .btn {
            display: inline-block;
            background-color: var(--primary);
            color: white;
            padding: 0.8rem 1.5rem;
            border-radius: 4px;
            text-decoration: none;
            font-weight: 500;
            transition: background-color 0.3s;
            border: none;
            cursor: pointer;
        }
        
        .btn:hover {
            background-color: var(--secondary);
        }
        
        .btn-outline {
            background-color: transparent;
            border: 2px solid var(--primary);
            color: var(--primary);
        }
        
        .btn-outline:hover {
            background-color: var(--primary);
            color: white;
        }
        
        footer {
            background-color: var(--dark);
            color: white;
            padding: 3rem 0;
            text-align: center;
        }
        
        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            margin: 1.5rem 0;
            list-style: none;
        }
        
        .social-links li {
            margin: 0 1rem;
        }
        
        .social-links a {
            color: white;
            font-size: 1.5rem;
            transition: color 0.3s;
        }
        
        .social-links a:hover {
            color: var(--accent);
        }
        
        .copyright {
            opacity: 0.7;
            font-size: 0.9rem;
        }
        
        @media (max-width: 768px) {
            .nav-links {
                display: none;
                position: absolute;
                top: 100%;
                left: 0;
                width: 100%;
                background-color: var(--secondary);
                flex-direction: column;
                padding: 1rem 0;
            }
            
            .nav-links.active {
                display: flex;
            }
            
            .nav-links li {
                margin: 0;
                text-align: center;
                padding: 0.5rem 0;
            }
            
            .mobile-menu-btn {
                display: block;
            }
            
            .logo {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="header-content">
            <div class="logo">Mindshift Society</div>
            <div class="slogan">探索意识边界 · 推动意识转移</div>
        </div>
    </header>
    
    <nav>
        <div class="nav-container">
            <div class="brand">迁知社</div>
            <button class="mobile-menu-btn">☰</button>
            <ul class="nav-links">
                <li><a href="#about">关于我们</a></li>
                <li><a href="#activities">活动项目</a></li>
                <li><a href="#research">研究成果</a></li>
                <li><a href="#join">加入我们</a></li>
                <li><a href="#contact">联系我们</a></li>
            </ul>
        </div>
    </nav>
    
    <main>
        <section id="about">
            <h2>关于迁知社</h2>
            <div class="mission-statement">
                <p>迁知社是一个致力于研究意识转移的前沿组织。我们汇聚了来自神经科学、心理学、哲学、人工智能等领域的探索者，共同探索人类意识的无限可能。</p>
                <p>我们的使命是通过跨学科研究和实践，推动人类认知边界的扩展，探索意识转移的技术与理论，为人类自由开辟新路径。</p>
            </div>
        </section>
        
        <section id="activities">
            <h2>我们的活动</h2>
            <div class="activities-grid">
                <div class="activity-card">
                    <div class="card-img">🧠</div>
                    <div class="card-content">
                        <h3>转移研讨会</h3>
                        <p>定期举办的跨学科研讨会，邀请领域专家分享最新研究成果，探讨意识转移的理论与实践。</p>
                        <a href="#" class="btn">了解更多</a>
                    </div>
                </div>
                
                <div class="activity-card">
                    <div class="card-img">🔬</div>
                    <div class="card-content">
                        <h3>认知工作坊</h3>
                        <p>通过实践验证的方法和技术，帮助参与者体验不同的世界。</p>
                        <a href="#" class="btn">了解更多</a>
                    </div>
                </div>
                
                <div class="activity-card">
                    <div class="card-img">📚</div>
                    <div class="card-content">
                        <h3>知识转移库</h3>
                        <p>建立开放的知识库，将前沿研究成果转化为可实践的认知工具和方法。</p>
                        <a href="#" class="btn">了解更多</a>
                    </div>
                </div>
            </div>
        </section>
        
        <section id="join">
            <h2>加入我们</h2>
            <p>无论你是研究者、实践者还是对意识转移充满热情的普通人，迁知社都欢迎你的加入。</p>
            <div style="margin-top: 2rem;">
                <a href="#" class="btn">成为会员</a>
                <a href="#" class="btn btn-outline" style="margin-left: 1rem;">志愿者申请</a>
            </div>
        </section>
    </main>
    
    <footer id="contact">
        <div class="footer-content">
            <h3>迁知社 Mindshift Society</h3>
            <ul class="social-links">
                <li><a href="#">qq</a></li>
                <li><a href="#">小红书</a></li>
                <li><a href="#">xmpp</a></li>
                <li><a href="#">childichat</a></li>
                <li><a href="#">Discord</a></li>
            </ul>
            <p class="copyright">© 2025 迁知社 版权所有</p>
        </div>
    </footer>
    
    <script>
        // 移动端菜单切换
        const menuBtn = document.querySelector('.mobile-menu-btn');
        const navLinks = document.querySelector('.nav-links');
        
        menuBtn.addEventListener('click', () => {
            navLinks.classList.toggle('active');
        });
        
        // 平滑滚动
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                
                if(this.getAttribute('href') === '#') return;
                
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
                
                // 关闭移动端菜单
                navLinks.classList.remove('active');
            });
        });
        
        // 导航栏滚动效果
        window.addEventListener('scroll', () => {
            const nav = document.querySelector('nav');
            if(window.scrollY > 50) {
                nav.style.backgroundColor = 'rgba(22, 96, 136, 0.95)';
            } else {
                nav.style.backgroundColor = 'rgba(255, 255, 255, 0.1)';
            }
        });
    </script>
</body>
</html>
