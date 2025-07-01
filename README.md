<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>迁知社 - 探索无限可能</title>
    <style>
        :root {
            --primary-color: #6a4c93;
            --secondary-color: #8a5a44;
            --accent-color: #f8f1ff;
            --text-color: #333;
            --light-text: #f8f9fa;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: var(--accent-color);
            color: var(--text-color);
            line-height: 1.6;
        }
        
        header {
            background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
            color: var(--light-text);
            padding: 2rem 0;
            text-align: center;
            position: relative;
            overflow: hidden;
        }
        
        .header-content {
            position: relative;
            z-index: 2;
        }
        
        header::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100" preserveAspectRatio="none"><path d="M0,0 L100,0 L100,100 Q50,80 0,100 Z" fill="rgba(0,0,0,0.1)"/></svg>');
            background-size: 100% 100%;
            opacity: 0.3;
            z-index: 1;
        }
        
        h1 {
            font-size: 3rem;
            margin-bottom: 1rem;
            font-weight: 300;
        }
        
        .subtitle {
            font-size: 1.2rem;
            font-style: italic;
            margin-bottom: 1.5rem;
        }
        
        nav {
            background-color: rgba(0, 0, 0, 0.2);
            padding: 1rem;
            position: sticky;
            top: 0;
            z-index: 100;
            backdrop-filter: blur(5px);
        }
        
        nav ul {
            display: flex;
            justify-content: center;
            list-style: none;
            flex-wrap: wrap;
        }
        
        nav li {
            margin: 0 1.5rem;
        }
        
        nav a {
            color: var(--light-text);
            text-decoration: none;
            font-weight: 500;
            padding: 0.5rem 0;
            position: relative;
            transition: all 0.3s ease;
        }
        
        nav a::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 0;
            height: 2px;
            background-color: var(--light-text);
            transition: width 0.3s ease;
        }
        
        nav a:hover::after {
            width: 100%;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 2rem;
        }
        
        section {
            margin-bottom: 3rem;
            animation: fadeIn 1s ease-in-out;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        h2 {
            color: var(--primary-color);
            margin-bottom: 1.5rem;
            font-size: 2rem;
            position: relative;
            display: inline-block;
        }
        
        h2::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 0;
            width: 50%;
            height: 3px;
            background-color: var(--secondary-color);
        }
        
        p {
            margin-bottom: 1.5rem;
            font-size: 1.1rem;
        }
        
        .quote {
            font-style: italic;
            padding: 1.5rem;
            background-color: rgba(106, 76, 147, 0.1);
            border-left: 4px solid var(--primary-color);
            margin: 2rem 0;
        }
        
        .features {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }
        
        .feature-card {
            background-color: white;
            border-radius: 8px;
            padding: 2rem;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        
        .feature-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.15);
        }
        
        .feature-card h3 {
            color: var(--primary-color);
            margin-bottom: 1rem;
        }
        
        .feature-icon {
            font-size: 2.5rem;
            margin-bottom: 1rem;
            color: var(--secondary-color);
        }
        
        .library-container, .meeting-container {
            background-color: white;
            border-radius: 8px;
            padding: 2rem;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            margin-top: 2rem;
        }
        
        .book-list, .meeting-list {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 1.5rem;
            margin-top: 1.5rem;
        }
        
        .book, .meeting {
            border: 1px solid #eee;
            border-radius: 5px;
            padding: 1rem;
            transition: all 0.3s ease;
        }
        
        .book:hover, .meeting:hover {
            border-color: var(--primary-color);
            box-shadow: 0 3px 10px rgba(106, 76, 147, 0.2);
        }
        
        .book h4, .meeting h4 {
            color: var(--primary-color);
            margin-bottom: 0.5rem;
        }
        
        .book p, .meeting p {
            font-size: 0.9rem;
            color: #666;
        }
        
        .btn {
            display: inline-block;
            background-color: var(--primary-color);
            color: white;
            padding: 0.8rem 1.5rem;
            border-radius: 30px;
            text-decoration: none;
            font-weight: 500;
            transition: all 0.3s ease;
            border: none;
            cursor: pointer;
            margin-top: 1rem;
        }
        
        .btn:hover {
            background-color: var(--secondary-color);
            transform: translateY(-2px);
        }
        
        .btn-outline {
            background-color: transparent;
            border: 2px solid var(--primary-color);
            color: var(--primary-color);
        }
        
        .btn-outline:hover {
            background-color: var(--primary-color);
            color: white;
        }
        
        form {
            margin-top: 1.5rem;
        }
        
        .form-group {
            margin-bottom: 1.5rem;
        }
        
        label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 500;
        }
        
        input, textarea, select {
            width: 100%;
            padding: 0.8rem;
            border: 1px solid #ddd;
            border-radius: 4px;
            font-size: 1rem;
        }
        
        textarea {
            min-height: 150px;
            resize: vertical;
        }
        
        footer {
            background-color: var(--primary-color);
            color: var(--light-text);
            text-align: center;
            padding: 2rem 0;
            margin-top: 3rem;
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            margin: 1rem 0;
        }
        
        .social-links a {
            color: var(--light-text);
            margin: 0 1rem;
            font-size: 1.5rem;
            transition: all 0.3s ease;
        }
        
        .social-links a:hover {
            transform: translateY(-3px);
            color: var(--accent-color);
        }
        
        @media (max-width: 768px) {
            h1 {
                font-size: 2.2rem;
            }
            
            nav ul {
                flex-direction: column;
                align-items: center;
            }
            
            nav li {
                margin: 0.5rem 0;
            }
            
            .features {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="header-content">
            <h1>迁知社</h1>
            <p class="subtitle">「每一个人都拥有无限的自由」</p>
            <p>成立于2025年</p>
        </div>
    </header>
    
    <nav>
        <ul>
            <li><a href="#about">关于我们</a></li>
            <li><a href="#philosophy">理念</a></li>
            <li><a href="#library">图书馆</a></li>
            <li><a href="#meetings">会议室</a></li>
            <li><a href="#join">加入我们</a></li>
        </ul>
    </nav>
    
    <div class="container">
        <section id="about">
            <h2>关于迁知社</h2>
            <p>迁知社是一个致力于探索转移可能性的组织，由溯梦于2025年创立。我们相信每个人都拥有超越界限的能力，而转移正是这种能力的体现。</p>
            
            <div class="quote">
                "界限只存在于心中，当你意识到自己的无限性，所有的门都会为你打开。" — 溯梦
            </div>
            
            <div class="features">
                <div class="feature-card">
                    <div class="feature-icon">🕊️</div>
                    <h3>自由探索</h3>
                    <p>我们鼓励每位成员以自己的方式探索转移的可能性，没有固定的路径，只有无限的可能。</p>
                </div>
                
                <div class="feature-card">
                    <div class="feature-icon">📚</div>
                    <h3>知识共享</h3>
                    <p>我们的图书馆收集了来自不同世界的知识与经验，供所有寻求者参考。</p>
                </div>
                
                <div class="feature-card">
                    <div class="feature-icon">🌌</div>
                    <h3>共同成长</h3>
                    <p>在会议室中，我们分享各自的发现与困惑，相互支持，共同进步。</p>
                </div>
            </div>
        </section>
        
        <section id="philosophy">
            <h2>我们的理念</h2>
            <p>迁知社不追求科学的解释，我们相信每个人与生俱来的感知与直觉。转移不是技术，而是一种觉醒，是对自我本质的重新认识。</p>
            <p>在这里，没有对错之分，没有固定的方法论。我们尊重每个人的独特体验，因为每个人的路径都是独一无二的。</p>
            
            <div class="quote">
                "当你停止用头脑思考'如何做到'，而开始用心感受'已经存在'，转移就自然发生了。" — 迁知社格言
            </div>
        </section>
        
        <section id="library">
            <h2>图书馆</h2>
            <p>我们的图书馆收藏了关于转移的各种记录、个人体验和启示。这些资料来自不同的世界和地区，供所有寻求者参考。</p>
            
            <div class="library-container">
                <h3>精选藏书</h3>
                <div class="book-list">
                    <div class="book">
                        <h4>《六本外国转移书藉》</h4>
                        <p>译者：溯梦</p>
                        <p>六位外国作者的转移体验记录及实践手册。</p>
                        <a href="#" class="btn btn-outline">阅读摘录</a>
                    </div>
                    
                    <div class="book">
                        <h4>《转移随笔》</h4>
                        <p>作者：溯梦</p>
                        <p>社长的个人笔记，深度闸述转移，个人转移经历及问题解答。</p>
                        <a href="#" class="btn btn-outline">阅读摘录</a>
                    </div>
                    
                    <div class="book">
                        <h4>《转移者调查报告》</h4>
                        <p>作者：多位贡献者</p>
                        <p>迁知社成员的转移记录合集。</p>
                        <a href="#" class="btn btn-outline">阅读摘录</a>
                    </div>
                    
                    <div class="book">
                        <h4>《迁知报》</h4>
                        <p>作者：溯梦</p>
                        <p>转移研究。</p>
                        <a href="#" class="btn btn-outline">阅读摘录</a>
                    </div>
                </div>
                
                <a href="#" class="btn">浏览全部藏书</a>
            </div>
        </section>
        
        <section id="meetings">
            <h2>会议室</h2>
            <p>我们的会议室是分享与交流的空间。在这里，成员们可以讨论自己的转移体验，提出问题，或只是倾听他人的故事。</p>
            
            <div class="meeting-container">
                <h3>近期活动</h3>
                <div class="meeting-list">
                    <div class="meeting">
                        <h4>新月分享会</h4>
                        <p>时间：每月第一个新月夜</p>
                        <p>开放给所有成员的分享会，主题自由。</p>
                        <a href="#" class="btn btn-outline">报名参加</a>
                    </div>
                    
                    <div class="meeting">
                        <h4>深度转移研讨</h4>
                        <p>时间：每周三晚</p>
                        <p>针对有经验的转移者的深度讨论。</p>
                        <a href="#" class="btn btn-outline">报名参加</a>
                    </div>
                    
                    <div class="meeting">
                        <h4>新手指引</h4>
                        <p>时间：每周六下午</p>
                        <p>为对转移感兴趣的新人提供的基础指引。</p>
                        <a href="#" class="btn btn-outline">报名参加</a>
                    </div>
                    
                    <div class="meeting">
                        <h4>特别讲座：跨世界艺术</h4>
                        <p>时间：2025年8月15日</p>
                        <p>探讨不同世界的艺术表达形式。</p>
                        <a href="#" class="btn btn-outline">报名参加</a>
                    </div>
                </div>
                
                <a href="#" class="btn">查看完整日程</a>
            </div>
        </section>
        
        <section id="join">
            <h2>加入我们</h2>
            <p>如果你感受到召唤，欢迎加入迁知社。我们不需要特定的资质或背景，只需要一颗开放和探索的心。</p>
            
            <div class="library-container">
                <form>
                    <div class="form-group">
                        <label for="name">姓名</label>
                        <input type="text" id="name" name="name" required>
                    </div>
                    
                    <div class="form-group">
                        <label for="email">电子邮箱</label>
                        <input type="email" id="email" name="email" required>
                    </div>
                    
                    <div class="form-group">
                        <label for="experience">你与转移的初次接触</label>
                        <textarea id="experience" name="experience"></textarea>
                    </div>
                    
                    <div class="form-group">
                        <label for="interest">你对迁知社的哪些方面感兴趣？</label>
                        <select id="interest" name="interest">
                            <option value="">请选择...</option>
                            <option value="library">图书馆资源</option>
                            <option value="meetings">会议室讨论</option>
                            <option value="research">转移研究</option>
                            <option value="all">全部</option>
                        </select>
                    </div>
                    
                    <button type="submit" class="btn">提交申请</button>
                </form>
            </div>
        </section>
    </div>
    
    <footer>
        <p>迁知社 © 2025 - 无限自由探索</p>
        <div class="social-links">
            <a href="#">🌐</a>
            <a href="#">📧</a>
            <a href="#">📱</a>
        </div>
        <p>联系邮箱：contact@qianzhishe.org</p>
    </footer>
    
    <script>
        // 平滑滚动
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });
        
        // 表单提交
        const form = document.querySelector('form');
        if(form) {
            form.addEventListener('submit', function(e) {
                e.preventDefault();
                alert('感谢你的申请！我们会尽快与你联系。');
                this.reset();
            });
        }
    </script>
</body>
</html>
