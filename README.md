<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>⚽ GoalMaster - تحليلات كرة القدم والمراهنات</title>
    <link rel="stylesheet" href="css/style.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@300;400;600;700;800;900&display=swap" rel="stylesheet">
</head>
<body>
    <!-- شريط التنبيهات العلوي -->
    <div class="top-ticker">
        <div class="ticker-content">
            <span class="live-dot"></span>
            <span id="ticker-text">جاري تحميل آخر النتائج...</span>
        </div>
    </div>

    <!-- شريط التنقل -->
    <nav class="navbar">
        <div class="nav-container">
            <div class="logo">
                <i class="fas fa-futbol fa-spin"></i>
                <span>GoalMaster</span>
                <small>تحليلات احترافية</small>
            </div>
            <ul class="nav-links" id="navLinks">
                <li><a href="#home" class="active"><i class="fas fa-home"></i> الرئيسية</a></li>
                <li><a href="#matches"><i class="fas fa-calendar-alt"></i> المباريات</a></li>
                <li><a href="#predictions"><i class="fas fa-chart-line"></i> التحليلات</a></li>
                <li><a href="#leagues"><i class="fas fa-trophy"></i> الدوريات</a></li>
                <li><a href="#standings"><i class="fas fa-list-ol"></i> الترتيب</a></li>
                <li><a href="#betting"><i class="fas fa-coins"></i> المراهنات</a></li>
                <li><a href="#stats"><i class="fas fa-chart-bar"></i> الإحصائيات</a></li>
                <li><a href="#news"><i class="fas fa-newspaper"></i> الأخبار</a></li>
            </ul>
            <div class="nav-actions">
                <button class="theme-toggle" id="themeToggle">
                    <i class="fas fa-moon"></i>
                </button>
                <button class="mobile-menu" id="mobileMenu">
                    <i class="fas fa-bars"></i>
                </button>
            </div>
        </div>
    </nav>

    <!-- القسم الرئيسي -->
    <main>
        <!-- Hero Section -->
        <section id="home" class="hero">
            <div class="hero-overlay"></div>
            <div class="hero-content">
                <h1>🏆 GoalMaster Analytics</h1>
                <p>أقوى منصة تحليلات كرة قدم ومراهنات رياضية في الوطن العربي</p>
                <div class="hero-stats">
                    <div class="hero-stat">
                        <span class="stat-number" data-target="8">0</span>
                        <span class="stat-label">دوري</span>
                    </div>
                    <div class="hero-stat">
                        <span class="stat-number" data-target="500">0</span>
                        <span class="stat-label">مباراة شهرياً</span>
                    </div>
                    <div class="hero-stat">
                        <span class="stat-number" data-target="87">0</span>
                        <span class="stat-label">% دقة التحليل</span>
                    </div>
                    <div class="hero-stat">
                        <span class="stat-number" data-target="50000">0</span>
                        <span class="stat-label">مستخدم نشط</span>
                    </div>
                </div>
                <div class="hero-buttons">
                    <a href="#matches" class="btn btn-primary"><i class="fas fa-play"></i> مباريات اليوم</a>
                    <a href="#predictions" class="btn btn-secondary"><i class="fas fa-magic"></i> توقعات الخبراء</a>
                </div>
            </div>
        </section>

        <!-- فلتر الدوريات -->
        <section class="league-filter">
            <div class="container">
                <div class="filter-tabs" id="leagueFilter">
                    <button class="filter-btn active" data-league="all">
                        <i class="fas fa-globe"></i> الكل
                    </button>
                    <button class="filter-btn" data-league="egyptian">
                        <span class="flag">🇪🇬</span> الدوري المصري
                    </button>
                    <button class="filter-btn" data-league="iraqi">
                        <span class="flag">🇮🇶</span> الدوري العراقي
                    </button>
                    <button class="filter-btn" data-league="saudi">
                        <span class="flag">🇸🇦</span> الدوري السعودي
                    </button>
                    <button class="filter-btn" data-league="english">
                        <span class="flag">🏴󠁧󠁢󠁥󠁮󠁧󠁿</span> الدوري الإنجليزي
                    </button>
                    <button class="filter-btn" data-league="spanish">
                        <span class="flag">🇪🇸</span> الدوري الإسباني
                    </button>
                    <button class="filter-btn" data-league="italian">
                        <span class="flag">🇮🇹</span> الدوري الإيطالي
                    </button>
                    <button class="filter-btn" data-league="champions">
                        <span class="flag">🏆</span> تشامبيونز ليج
                    </button>
                    <button class="filter-btn" data-league="dutch">
                        <span class="flag">🇳🇱</span> الدوري الهولندي
                    </button>
                </div>
            </div>
        </section>

        <!-- مباريات اليوم -->
        <section id="matches" class="section matches-section">
            <div class="container">
                <div class="section-header">
                    <h2><i class="fas fa-calendar-day"></i> مباريات اليوم</h2>
                    <div class="date-nav">
                        <button class="date-btn" id="prevDay"><i class="fas fa-chevron-right"></i></button>
                        <span class="current-date" id="currentDate"></span>
                        <button class="date-btn" id="nextDay"><i class="fas fa-chevron-left"></i></button>
                    </div>
                </div>
                <div class="matches-grid" id="matchesGrid">
                    <!-- المباريات تُحمّل ديناميكياً -->
                </div>
            </div>
        </section>

        <!-- التحليلات والتوقعات -->
        <section id="predictions" class="section predictions-section">
            <div class="container">
                <div class="section-header">
                    <h2><i class="fas fa-brain"></i> تحليلات وتوقعات الخبراء</h2>
                    <span class="badge">AI Powered</span>
                </div>
                <div class="predictions-grid" id="predictionsGrid">
                    <!-- التوقعات تُحمّل ديناميكياً -->
                </div>
            </div>
        </section>

        <!-- الترتيب -->
        <section id="standings" class="section standings-section">
            <div class="container">
                <div class="section-header">
                    <h2><i class="fas fa-list-ol"></i> جدول الترتيب</h2>
                    <select id="standingsLeague" class="league-select">
                        <option value="egyptian">🇪🇬 الدوري المصري</option>
                        <option value="iraqi">🇮🇶 الدوري العراقي</option>
                        <option value="saudi">🇸🇦 الدوري السعودي</option>
                        <option value="english">🏴󠁧󠁢󠁥󠁮󠁧󠁿 الدوري الإنجليزي</option>
                        <option value="spanish">🇪🇸 الدوري الإسباني</option>
                        <option value="italian">🇮🇹 الدوري الإيطالي</option>
                        <option value="champions">🏆 تشامبيونز ليج</option>
                        <option value="dutch">🇳🇱 الدوري الهولندي</option>
                    </select>
                </div>
                <div class="standings-table-wrapper">
                    <table class="standings-table" id="standingsTable">
                        <thead>
                            <tr>
                                <th>#</th>
                                <th>الفريق</th>
                                <th>لعب</th>
                                <th>فوز</th>
                                <th>تعادل</th>
                                <th>خسارة</th>
                                <th>له</th>
                                <th>عليه</th>
                                <th>الفارق</th>
                                <th>النقاط</th>
                                <th>الفورم</th>
                            </tr>
                        </thead>
                        <tbody id="standingsBody">
                        </tbody>
                    </table>
                </div>
            </div>
        </section>

        <!-- المراهنات -->
        <section id="betting" class="section betting-section">
            <div class="container">
                <div class="section-header">
                    <h2><i class="fas fa-coins"></i> نصائح المراهنات</h2>
                    <span class="badge hot">🔥 Hot Tips</span>
                </div>
                <div class="betting-cards" id="bettingCards">
                    <!-- كروت المراهنات تُحمّل ديناميكياً -->
                </div>

                <!-- حاسبة المراهنات -->
                <div class="bet-calculator">
                    <h3><i class="fas fa-calculator"></i> حاسبة المراهنات</h3>
                    <div class="calc-grid">
                        <div class="calc-input">
                            <label>مبلغ الرهان</label>
                            <input type="number" id="betAmount" placeholder="100" min="1">
                        </div>
                        <div class="calc-input">
                            <label>معامل الربح (Odds)</label>
                            <input type="number" id="betOdds" placeholder="2.50" min="1" step="0.01">
                        </div>
                        <div class="calc-result">
                            <label>الربح المتوقع</label>
                            <span id="betProfit">0.00</span>
                        </div>
                        <div class="calc-result total">
                            <label>المبلغ الإجمالي</label>
                            <span id="betTotal">0.00</span>
                        </div>
                    </div>
                    <button class="btn btn-primary calc-btn" id="calcBet">
                        <i class="fas fa-calculator"></i> احسب
                    </button>
                </div>
            </div>
        </section>

        <!-- الإحصائيات -->
        <section id="stats" class="section stats-section">
            <div class="container">
                <div class="section-header">
                    <h2><i class="fas fa-chart-bar"></i> إحصائيات متقدمة</h2>
                </div>
                <div class="stats-dashboard">
                    <div class="stat-card">
                        <div class="stat-icon goals"><i class="fas fa-futbol"></i></div>
                        <div class="stat-info">
                            <h4>أكثر الفرق تسجيلاً</h4>
                            <div id="topScorersTeams" class="stat-list"></div>
                        </div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-icon wins"><i class="fas fa-trophy"></i></div>
                        <div class="stat-info">
                            <h4>أطول سلسلة انتصارات</h4>
                            <div id="winStreaks" class="stat-list"></div>
                        </div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-icon clean"><i class="fas fa-shield-alt"></i></div>
                        <div class="stat-info">
                            <h4>أقوى دفاع</h4>
                            <div id="bestDefense" class="stat-list"></div>
                        </div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-icon btts"><i class="fas fa-exchange-alt"></i></div>
                        <div class="stat-info">
                            <h4>نسبة BTTS</h4>
                            <div id="bttsStats" class="stat-list"></div>
                        </div>
                    </div>
                    <div class="stat-card wide">
                        <div class="stat-icon over"><i class="fas fa-arrow-up"></i></div>
                        <div class="stat-info">
                            <h4>نسبة Over/Under 2.5</h4>
                            <div class="over-under-chart" id="overUnderChart"></div>
                        </div>
                    </div>
                    <div class="stat-card wide">
                        <div class="stat-icon form"><i class="fas fa-chart-line"></i></div>
                        <div class="stat-info">
                            <h4>فورم الفرق (آخر 5 مباريات)</h4>
                            <div id="teamForms" class="stat-list"></div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- الأخبار -->
        <section id="news" class="section news-section">
            <div class="container">
                <div class="section-header">
                    <h2><i class="fas fa-newspaper"></i> آخر الأخبار</h2>
                </div>
                <div class="news-grid" id="newsGrid">
                </div>
            </div>
        </section>

        <!-- الدوريات -->
        <section id="leagues" class="section leagues-section">
            <div class="container">
                <div class="section-header">
                    <h2><i class="fas fa-trophy"></i> الدوريات المتاحة</h2>
                </div>
                <div class="leagues-showcase" id="leaguesShowcase">
                </div>
            </div>
        </section>
    </main>

    <!-- Footer -->
    <footer class="footer">
        <div class="container">
            <div class="footer-grid">
                <div class="footer-col">
                    <h3><i class="fas fa-futbol"></i> GoalMaster</h3>
                    <p>أقوى منصة تحليلات كرة قدم ومراهنات رياضية. نوفر تحليلات دقيقة مبنية على الذكاء الاصطناعي وبيانات حقيقية.</p>
                </div>
                <div class="footer-col">
                    <h3>الدوريات</h3>
                    <ul>
                        <li><a href="#">🇪🇬 الدوري المصري</a></li>
                        <li><a href="#">🇮🇶 الدوري العراقي</a></li>
                        <li><a href="#">🇸🇦 الدوري السعودي</a></li>
                        <li><a href="#">🏴󠁧󠁢󠁥󠁮󠁧󠁿 الدوري الإنجليزي</a></li>
                        <li><a href="#">🇪🇸 الدوري الإسباني</a></li>
                        <li><a href="#">🇮🇹 الدوري الإيطالي</a></li>
                        <li><a href="#">🏆 تشامبيونز ليج</a></li>
                        <li><a href="#">🇳🇱 الدوري الهولندي</a></li>
                    </ul>
                </div>
                <div class="footer-col">
                    <h3>روابط سريعة</h3>
                    <ul>
                        <li><a href="#matches">المباريات</a></li>
                        <li><a href="#predictions">التحليلات</a></li>
                        <li><a href="#betting">المراهنات</a></li>
                        <li><a href="#stats">الإحصائيات</a></li>
                    </ul>
                </div>
                <div class="footer-col">
                    <h3>تواصل معنا</h3>
                    <div class="social-links">
                        <a href="#"><i class="fab fa-telegram"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-youtube"></i></a>
                    </div>
                    <p class="disclaimer">⚠️ تنبيه: المراهنات الرياضية تحمل مخاطر مالية. العب بمسؤولية.</p>
                </div>
            </div>
            <div class="footer-bottom">
                <p>© 2024 GoalMaster Analytics. جميع الحقوق محفوظة.</p>
            </div>
        </div>
    </footer>

    <!-- Back to top -->
    <button class="back-to-top" id="backToTop">
        <i class="fas fa-chevron-up"></i>
    </button>

    <!-- Loading Screen -->
    <div class="loading-screen" id="loadingScreen">
        <div class="loader">
            <i class="fas fa-futbol fa-spin"></i>
            <p>جاري التحميل...</p>
        </div>
    </div>

    <script src="js/leagues.js"></script>
    <script src="js/matches.js"></script>
    <script src="js/predictions.js"></script>
    <script src="js/app.js"></script>
</body>
</html>
/* ===== المتغيرات والإعدادات الأساسية ===== */
:root {
    --primary: #1a73e8;
    --primary-dark: #1557b0;
    --primary-light: #4a90d9;
    --secondary: #ff6b35;
    --secondary-dark: #e55a2b;
    --accent: #00c853;
    --accent-red: #ff1744;
    --accent-yellow: #ffd600;
    --bg-dark: #0a0e27;
    --bg-darker: #060919;
    --bg-card: #111638;
    --bg-card-hover: #1a1f4a;
    --text-primary: #ffffff;
    --text-secondary: #b0b8d1;
    --text-muted: #6b7394;
    --border: #1e2555;
    --shadow: 0 10px 40px rgba(0, 0, 0, 0.3);
    --shadow-lg: 0 20px 60px rgba(0, 0, 0, 0.4);
    --gradient-primary: linear-gradient(135deg, #1a73e8, #6c63ff);
    --gradient-secondary: linear-gradient(135deg, #ff6b35, #ff1744);
    --gradient-success: linear-gradient(135deg, #00c853, #00e676);
    --gradient-card: linear-gradient(145deg, #111638, #0d1230);
    --radius: 16px;
    --radius-sm: 8px;
    --radius-lg: 24px;
    --transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
}

/* Light Theme */
[data-theme="light"] {
    --bg-dark: #f0f2f5;
    --bg-darker: #e4e6eb;
    --bg-card: #ffffff;
    --bg-card-hover: #f5f7fa;
    --text-primary: #1a1a2e;
    --text-secondary: #4a4a6a;
    --text-muted: #8888a8;
    --border: #e0e0e0;
    --shadow: 0 10px 40px rgba(0, 0, 0, 0.08);
    --gradient-card: linear-gradient(145deg, #ffffff, #f8f9fa);
}

/* ===== Reset & Base ===== */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

html {
    scroll-behavior: smooth;
    font-size: 16px;
}

body {
    font-family: 'Cairo', sans-serif;
    background: var(--bg-dark);
    color: var(--text-primary);
    line-height: 1.7;
    overflow-x: hidden;
    min-height: 100vh;
}

.container {
    max-width: 1400px;
    margin: 0 auto;
    padding: 0 20px;
}

a {
    text-decoration: none;
    color: inherit;
    transition: var(--transition);
}

/* ===== شريط التنبيهات ===== */
.top-ticker {
    background: var(--gradient-primary);
    padding: 8px 0;
    overflow: hidden;
    position: relative;
    z-index: 1001;
}

.ticker-content {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 10px;
    animation: ticker 20s linear infinite;
    white-space: nowrap;
    font-size: 0.85rem;
    font-weight: 600;
}

.live-dot {
    width: 8px;
    height: 8px;
    background: #ff1744;
    border-radius: 50%;
    animation: pulse 1.5s infinite;
    flex-shrink: 0;
}

@keyframes pulse {
    0%, 100% { opacity: 1; transform: scale(1); }
    50% { opacity: 0.5; transform: scale(1.5); }
}

@keyframes ticker {
    0% { transform: translateX(100%); }
    100% { transform: translateX(-100%); }
}

/* ===== شريط التنقل ===== */
.navbar {
    background: rgba(10, 14, 39, 0.95);
    backdrop-filter: blur(20px);
    border-bottom: 1px solid var(--border);
    position: sticky;
    top: 0;
    z-index: 1000;
    padding: 0;
    transition: var(--transition);
}

.navbar.scrolled {
    box-shadow: var(--shadow);
}

.nav-container {
    max-width: 1400px;
    margin: 0 auto;
    padding: 0 20px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    height: 70px;
}

.logo {
    display: flex;
    align-items: center;
    gap: 10px;
    font-size: 1.5rem;
    font-weight: 900;
    color: var(--primary);
    cursor: pointer;
}

.logo i {
    font-size: 1.8rem;
    color: var(--secondary);
}

.logo small {
    font-size: 0.6rem;
    color: var(--text-muted);
    display: block;
    margin-top: -5px;
}

.nav-links {
    display: flex;
    list-style: none;
    gap: 5px;
}

.nav-links a {
    display: flex;
    align-items: center;
    gap: 6px;
    padding: 8px 14px;
    border-radius: var(--radius-sm);
    font-size: 0.85rem;
    font-weight: 600;
    color: var(--text-secondary);
    transition: var(--transition);
    position: relative;
}

.nav-links a:hover,
.nav-links a.active {
    color: var(--primary);
    background: rgba(26, 115, 232, 0.1);
}

.nav-links a.active::after {
    content: '';
    position: absolute;
    bottom: -5px;
    left: 50%;
    transform: translateX(-50%);
    width: 20px;
    height: 3px;
    background: var(--primary);
    border-radius: 3px;
}

.nav-actions {
    display: flex;
    align-items: center;
    gap: 10px;
}

.theme-toggle,
.mobile-menu {
    background: var(--bg-card);
    border: 1px solid var(--border);
    color: var(--text-primary);
    width: 40px;
    height: 40px;
    border-radius: 50%;
    cursor: pointer;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 1rem;
    transition: var(--transition);
}

.theme-toggle:hover,
.mobile-menu:hover {
    background: var(--primary);
    color: white;
    transform: rotate(15deg);
}

.mobile-menu {
    display: none;
}

/* ===== Hero Section ===== */
.hero {
    position: relative;
    min-height: 500px;
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
    overflow: hidden;
    background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 500"><defs><linearGradient id="g" x1="0" y1="0" x2="1" y2="1"><stop offset="0%" stop-color="%231a73e8"/><stop offset="50%" stop-color="%236c63ff"/><stop offset="100%" stop-color="%23ff6b35"/></linearGradient></defs><rect fill="url(%23g)" width="1440" height="500"/></svg>') center/cover;
}

.hero-overlay {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: rgba(10, 14, 39, 0.85);
    z-index: 1;
}

.hero-content {
    position: relative;
    z-index: 2;
    padding: 40px 20px;
}

.hero-content h1 {
    font-size: 3.5rem;
    font-weight: 900;
    margin-bottom: 15px;
    background: linear-gradient(135deg, #fff, #4a90d9);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
}

.hero-content p {
    font-size: 1.2rem;
    color: var(--text-secondary);
    margin-bottom: 40px;
    max-width: 600px;
    margin-left: auto;
    margin-right: auto;
}

.hero-stats {
    display: flex;
    justify-content: center;
    gap: 40px;
    margin-bottom: 40px;
    flex-wrap: wrap;
}

.hero-stat {
    text-align: center;
}

.stat-number {
    display: block;
    font-size: 2.5rem;
    font-weight: 900;
    color: var(--secondary);
}

.stat-label {
    font-size: 0.85rem;
    color: var(--text-muted);
}

.hero-buttons {
    display: flex;
    gap: 15px;
    justify-content: center;
    flex-wrap: wrap;
}

/* ===== الأزرار ===== */
.btn {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    padding: 12px 30px;
    border-radius: 50px;
    font-family: 'Cairo', sans-serif;
    font-size: 1rem;
    font-weight: 700;
    border: none;
    cursor: pointer;
    transition: var(--transition);
    position: relative;
    overflow: hidden;
}

.btn::before {
    content: '';
    position: absolute;
    top: 0;
    left: -100%;
    width: 100%;
    height: 100%;
    background: linear-gradient(90deg, transparent, rgba(255,255,255,0.2), transparent);
    transition: left 0.5s;
}

.btn:hover::before {
    left: 100%;
}

.btn-primary {
    background: var(--gradient-primary);
    color: white;
    box-shadow: 0 4px 20px rgba(26, 115, 232, 0.4);
}

.btn-primary:hover {
    transform: translateY(-3px);
    box-shadow: 0 8px 30px rgba(26, 115, 232, 0.6);
}

.btn-secondary {
    background: var(--gradient-secondary);
    color: white;
    box-shadow: 0 4px 20px rgba(255, 107, 53, 0.4);
}

.btn-secondary:hover {
    transform: translateY(-3px);
    box-shadow: 0 8px 30px rgba(255, 107, 53, 0.6);
}

/* ===== فلتر الدوريات ===== */
.league-filter {
    background: var(--bg-darker);
    padding: 15px 0;
    border-bottom: 1px solid var(--border);
    position: sticky;
    top: 70px;
    z-index: 999;
}

.filter-tabs {
    display: flex;
    gap: 8px;
    overflow-x: auto;
    padding-bottom: 5px;
    scrollbar-width: none;
}

.filter-tabs::-webkit-scrollbar {
    display: none;
}

.filter-btn {
    display: flex;
    align-items: center;
    gap: 6px;
    padding: 8px 18px;
    border: 1px solid var(--border);
    border-radius: 50px;
    background: var(--bg-card);
    color: var(--text-secondary);
    font-family: 'Cairo', sans-serif;
    font-size: 0.85rem;
    font-weight: 600;
    cursor: pointer;
    transition: var(--transition);
    white-space: nowrap;
    flex-shrink: 0;
}

.filter-btn:hover,
.filter-btn.active {
    background: var(--gradient-primary);
    color: white;
    border-color: var(--primary);
    transform: translateY(-2px);
    box-shadow: 0 4px 15px rgba(26, 115, 232, 0.3);
}

.filter-btn .flag {
    font-size: 1.2rem;
}

/* ===== الأقسام ===== */
.section {
    padding: 60px 0;
}

.section-header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin-bottom: 30px;
    flex-wrap: wrap;
    gap: 15px;
}

.section-header h2 {
    font-size: 1.8rem;
    font-weight: 800;
    display: flex;
    align-items: center;
    gap: 10px;
}

.section-header h2 i {
    color: var(--primary);
}

.badge {
    padding: 5px 15px;
    border-radius: 50px;
    font-size: 0.75rem;
    font-weight: 700;
    background: var(--gradient-primary);
    color: white;
}

.badge.hot {
    background: var(--gradient-secondary);
    animation: glow 2s infinite;
}

@keyframes glow {
    0%, 100% { box-shadow: 0 0 10px rgba(255, 107, 53, 0.5); }
    50% { box-shadow: 0 0 25px rgba(255, 107, 53, 0.8); }
}

/* ===== كروت المباريات ===== */
.matches-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(380px, 1fr));
    gap: 20px;
}

.match-card {
    background: var(--gradient-card);
    border: 1px solid var(--border);
    border-radius: var(--radius);
    padding: 20px;
    transition: var(--transition);
    position: relative;
    overflow: hidden;
}

.match-card::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    height: 3px;
    background: var(--gradient-primary);
}

.match-card:hover {
    transform: translateY(-5px);
    box-shadow: var(--shadow-lg);
    border-color: var(--primary);
}

.match-card.live::before {
    background: var(--gradient-secondary);
    animation: liveBar 2s infinite;
}

@keyframes liveBar {
    0%, 100% { opacity: 1; }
    50% { opacity: 0.5; }
}

.match-league {
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin-bottom: 15px;
    font-size: 0.8rem;
    color: var(--text-muted);
}

.match-league .league-name {
    display: flex;
    align-items: center;
    gap: 6px;
    font-weight: 600;
}

.match-status {
    padding: 3px 10px;
    border-radius: 50px;
    font-size: 0.7rem;
    font-weight: 700;
}

.match-status.live {
    background: rgba(255, 23, 68, 0.2);
    color: #ff1744;
    animation: pulse 1.5s infinite;
}

.match-status.upcoming {
    background: rgba(26, 115, 232, 0.2);
    color: var(--primary);
}

.match-status.finished {
    background: rgba(0, 200, 83, 0.2);
    color: var(--accent);
}

.match-teams {
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin-bottom: 15px;
}

.team {
    text-align: center;
    flex: 1;
}

.team-logo {
    width: 50px;
    height: 50px;
    margin: 0 auto 8px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 2rem;
    background: var(--bg-dark);
    border-radius: 50%;
    border: 2px solid var(--border);
}

.team-name {
    font-size: 0.85rem;
    font-weight: 700;
}

.match-score {
    display: flex;
    align-items: center;
    gap: 10px;
    font-size: 2rem;
    font-weight: 900;
}

.match-score .separator {
    color: var(--text-muted);
    font-size: 1.2rem;
}

.match-info {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding-top: 15px;
    border-top: 1px solid var(--border);
    font-size: 0.8rem;
    color: var(--text-muted);
}

.match-time {
    display: flex;
    align-items: center;
    gap: 5px;
}

.match-odds {
    display: flex;
    gap: 8px;
}

.odd-btn {
    padding: 4px 12px;
    background: rgba(26, 115, 232, 0.1);
    border: 1px solid rgba(26, 115, 232, 0.3);
    border-radius: var(--radius-sm);
    color: var(--primary);
    font-size: 0.75rem;
    font-weight: 700;
    cursor: pointer;
    transition: var(--transition);
}

.odd-btn:hover {
    background: var(--primary);
    color: white;
}

/* ===== التوقعات ===== */
.predictions-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
    gap: 20px;
}

.prediction-card {
    background: var(--gradient-card);
    border: 1px solid var(--border);
    border-radius: var(--radius);
    padding: 25px;
    transition: var(--transition);
}

.prediction-card:hover {
    transform: translateY(-5px);
    box-shadow: var(--shadow-lg);
}

.prediction-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 15px;
}

.prediction-match {
    font-size: 1rem;
    font-weight: 700;
}

.confidence {
    display: flex;
    align-items: center;
    gap: 5px;
    padding: 4px 12px;
    border-radius: 50px;
    font-size: 0.75rem;
    font-weight: 700;
}

.confidence.high {
    background: rgba(0, 200, 83, 0.2);
    color: var(--accent);
}

.confidence.medium {
    background: rgba(255, 214, 0, 0.2);
    color: var(--accent-yellow);
}

.confidence.low {
    background: rgba(255, 23, 68, 0.2);
    color: var(--accent-red);
}

.prediction-details {
    margin: 15px 0;
}

.prediction-tip {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 10px;
    background: var(--bg-dark);
    border-radius: var(--radius-sm);
    margin-bottom: 8px;
}

.tip-label {
    font-size: 0.85rem;
    color: var(--text-secondary);
}

.tip-value {
    font-weight: 700;
    color: var(--primary);
}

.prediction-bar {
    height: 6px;
    background: var(--bg-dark);
    border-radius: 3px;
    overflow: hidden;
    margin-top: 15px;
}

.prediction-bar-fill {
    height: 100%;
    border-radius: 3px;
    background: var(--gradient-success);
    transition: width 1s ease;
}

.prediction-analysis {
    margin-top: 15px;
    padding: 12px;
    background: rgba(26, 115, 232, 0.05);
    border-right: 3px solid var(--primary);
    border-radius: var(--radius-sm);
    font-size: 0.85rem;
    color: var(--text-secondary);
    line-height: 1.8;
}

/* ===== الترتيب ===== */
.league-select {
    padding: 8px 20px;
    border-radius: var(--radius-sm);
    border: 1px solid var(--border);
    background: var(--bg-card);
    color: var(--text-primary);
    font-family: 'Cairo', sans-serif;
    font-size: 0.9rem;
    font-weight: 600;
    cursor: pointer;
    outline: none;
}

.standings-table-wrapper {
    overflow-x: auto;
    border-radius: var(--radius);
    border: 1px solid var(--border);
}

.standings-table {
    width: 100%;
    border-collapse: collapse;
    min-width: 800px;
}

.standings-table thead {
    background: var(--gradient-primary);
}

.standings-table th {
    padding: 14px 12px;
    text-align: center;
    font-size: 0.8rem;
    font-weight: 700;
    color: white;
    white-space: nowrap;
}

.standings-table td {
    padding: 12px;
    text-align: center;
    font-size: 0.85rem;
    border-bottom: 1px solid var(--border);
    transition: var(--transition);
}

.standings-table tr:hover td {
    background: var(--bg-card-hover);
}

.standings-table tr.champion td {
    border-right: 3px solid var(--accent);
}

.standings-table tr.relegation td {
    border-right: 3px solid var(--accent-red);
}

.standings-team {
    display: flex;
    align-items: center;
    gap: 10px;
    text-align: right;
}

.standings-team .team-crest {
    width: 28px;
    height: 28px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 1.2rem;
}

.form-badges {
    display: flex;
    gap: 3px;
    justify-content: center;
}

.form-badge {
    width: 22px;
    height: 22px;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 0.6rem;
    font-weight: 700;
    color: white;
}

.form-badge.w { background: var(--accent); }
.form-badge.d { background: var(--accent-yellow); color: #333; }
.form-badge.l { background: var(--accent-red); }

.points {
    font-weight: 900;
    font-size: 1rem;
    color: var(--primary);
}

/* ===== المراهنات ===== */
.betting-cards {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
    gap: 20px;
    margin-bottom: 40px;
}

.bet-card {
    background: var(--gradient-card);
    border: 1px solid var(--border);
    border-radius: var(--radius);
    padding: 20px;
    transition: var(--transition);
    position: relative;
}

.bet-card:hover {
    transform: translateY(-5px);
    box-shadow: var(--shadow-lg);
}

.bet-card .hot-badge {
    position: absolute;
    top: 15px;
    left: 15px;
    background: var(--gradient-secondary);
    color: white;
    padding: 3px 10px;
    border-radius: 50px;
    font-size: 0.7rem;
    font-weight: 700;
}

.bet-match {
    font-weight: 700;
    margin-bottom: 10px;
    font-size: 1rem;
}

.bet-type {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 10px;
    background: var(--bg-dark);
    border-radius: var(--radius-sm);
    margin-bottom: 8px;
}

.bet-label {
    font-size: 0.85rem;
    color: var(--text-secondary);
}

.bet-value {
    font-weight: 700;
    padding: 3px 10px;
    border-radius: 50px;
    font-size: 0.8rem;
}

.bet-value.high {
    background: rgba(0, 200, 83, 0.2);
    color: var(--accent);
}

.bet-value.medium {
    background: rgba(255, 214, 0, 0.2);
    color: var(--accent-yellow);
}

.bet-reason {
    margin-top: 12px;
    padding: 10px;
    background: rgba(26, 115, 232, 0.05);
    border-radius: var(--radius-sm);
    font-size: 0.8rem;
    color: var(--text-muted);
    border-right: 3px solid var(--primary);
}

/* حاسبة المراهنات */
.bet-calculator {
    background: var(--gradient-card);
    border: 1px solid var(--border);
    border-radius: var(--radius);
    padding: 30px;
}

.bet-calculator h3 {
    margin-bottom: 20px;
    display: flex;
    align-items: center;
    gap: 10px;
    font-size: 1.2rem;
}

.calc-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 15px;
    margin-bottom: 20px;
}

.calc-input label,
.calc-result label {
    display: block;
    font-size: 0.85rem;
    color: var(--text-muted);
    margin-bottom: 8px;
}

.calc-input input {
    width: 100%;
    padding: 12px 15px;
    border: 1px solid var(--border);
    border-radius: var(--radius-sm);
    background: var(--bg-dark);
    color: var(--text-primary);
    font-family: 'Cairo', sans-serif;
    font-size: 1rem;
    font-weight: 600;
    outline: none;
    transition: var(--transition);
}

.calc-input input:focus {
    border-color: var(--primary);
    box-shadow: 0 0 0 3px rgba(26, 115, 232, 0.2);
}

.calc-result span {
    display: block;
    font-size: 1.5rem;
    font-weight: 900;
    color: var(--accent);
}

.calc-result.total span {
    color: var(--secondary);
}

.calc-btn {
    width: 100%;
}

/* ===== الإحصائيات ===== */
.stats-dashboard {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
    gap: 20px;
}

.stat-card {
    background: var(--gradient-card);
    border: 1px solid var(--border);
    border-radius: var(--radius);
    padding: 25px;
    transition: var(--transition);
}

.stat-card:hover {
    transform: translateY(-5px);
    box-shadow: var(--shadow-lg);
}

.stat-card.wide {
    grid-column: span 2;
}

.stat-icon {
    width: 50px;
    height: 50px;
    border-radius: 12px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 1.3rem;
    margin-bottom: 15px;
}

.stat-icon.goals { background: rgba(255, 107, 53, 0.2); color: var(--secondary); }
.stat-icon.wins { background: rgba(0, 200, 83, 0.2); color: var(--accent); }
.stat-icon.clean { background: rgba(26, 115, 232, 0.2); color: var(--primary); }
.stat-icon.btts { background: rgba(255, 214, 0, 0.2); color: var(--accent-yellow); }
.stat-icon.over { background: rgba(108, 99, 255, 0.2); color: #6c63ff; }
.stat-icon.form { background: rgba(255, 23, 68, 0.2); color: var(--accent-red); }

.stat-info h4 {
    font-size: 1rem;
    margin-bottom: 12px;
    color: var(--text-primary);
}

.stat-list {
    display: flex;
    flex-direction: column;
    gap: 8px;
}

.stat-item {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 8px 12px;
    background: var(--bg-dark);
    border-radius: var(--radius-sm);
    font-size: 0.85rem;
}

.stat-item .team-flag {
    margin-left: 8px;
}

.stat-item .value {
    font-weight: 700;
    color: var(--primary);
}

.over-under-chart {
    display: flex;
    flex-direction: column;
    gap: 10px;
}

.chart-bar {
    display: flex;
    align-items: center;
    gap: 10px;
}

.chart-bar .label {
    width: 120px;
    font-size: 0.8rem;
    color: var(--text-secondary);
    flex-shrink: 0;
}

.chart-bar .bar {
    flex: 1;
    height: 24px;
    background: var(--bg-dark);
    border-radius: 12px;
    overflow: hidden;
}

.chart-bar .bar-fill {
    height: 100%;
    border-radius: 12px;
    display: flex;
    align-items: center;
    justify-content: flex-end;
    padding: 0 10px;
    font-size: 0.7rem;
    font-weight: 700;
    color: white;
    transition: width 1.5s ease;
}

.chart-bar .bar-fill.over { background: var(--gradient-success); }
.chart-bar .bar-fill.under { background: var(--gradient-secondary); }

/* ===== الأخبار ===== */
.news-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
    gap: 20px;
}

.news-card {
    background: var(--gradient-card);
    border: 1px solid var(--border);
    border-radius: var(--radius);
    overflow: hidden;
    transition: var(--transition);
}

.news-card:hover {
    transform: translateY(-5px);
    box-shadow: var(--shadow-lg);
}

.news-image {
    height: 180px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 4rem;
    background: var(--gradient-primary);
}

.news-content {
    padding: 20px;
}

.news-content h3 {
    font-size: 1rem;
    font-weight: 700;
    margin-bottom: 8px;
    line-height: 1.6;
}

.news-content p {
    font-size: 0.85rem;
    color: var(--text-muted);
    margin-bottom: 10px;
    line-height: 1.7;
}

.news-meta {
    display: flex;
    justify-content: space-between;
    align-items: center;
    font-size: 0.75rem;
    color: var(--text-muted);
}

/* ===== الدوريات ===== */
.leagues-showcase {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
    gap: 20px;
}

.league-card {
    background: var(--gradient-card);
    border: 1px solid var(--border);
    border-radius: var(--radius);
    padding: 30px;
    text-align: center;
    transition: var(--transition);
    cursor: pointer;
}

.league-card:hover {
    transform: translateY(-8px) scale(1.02);
    box-shadow: var(--shadow-lg);
    border-color: var(--primary);
}

.league-card .league-flag {
    font-size: 3rem;
    margin-bottom: 15px;
}

.league-card h3 {
    font-size: 1.1rem;
    margin-bottom: 5px;
}

.league-card .league-country {
    font-size: 0.8rem;
    color: var(--text-muted);
    margin-bottom: 15px;
}

.league-card .league-info-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 10px;
}

.league-info-item {
    padding: 8px;
    background: var(--bg-dark);
    border-radius: var(--radius-sm);
}

.league-info-item .num {
    display: block;
    font-size: 1.2rem;
    font-weight: 800;
    color: var(--primary);
}

.league-info-item .lbl {
    font-size: 0.7rem;
    color: var(--text-muted);
}

/* ===== Date Navigation ===== */
.date-nav {
    display: flex;
    align-items: center;
    gap: 12px;
}

.date-btn {
    width: 36px;
    height: 36px;
    border-radius: 50%;
    border: 1px solid var(--border);
    background: var(--bg-card);
    color: var(--text-primary);
    cursor: pointer;
    display: flex;
    align-items: center;
    justify-content: center;
    transition: var(--transition);
}

.date-btn:hover {
    background: var(--primary);
    color: white;
}

.current-date {
    font-weight: 700;
    font-size: 0.9rem;
}

/* ===== Footer ===== */
.footer {
    background: var(--bg-darker);
    border-top: 1px solid var(--border);
    padding: 50px 0 20px;
}

.footer-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 30px;
    margin-bottom: 30px;
}

.footer-col h3 {
    font-size: 1.1rem;
    margin-bottom: 15px;
    color: var(--primary);
    display: flex;
    align-items: center;
    gap: 8px;
}

.footer-col p {
    font-size: 0.85rem;
    color: var(--text-muted);
    line-height: 1.8;
}

.footer-col ul {
    list-style: none;
}

.footer-col ul li {
    margin-bottom: 8px;
}

.footer-col ul li a {
    font-size: 0.85rem;
    color: var(--text-muted);
    transition: var(--transition);
}

.footer-col ul li a:hover {
    color: var(--primary);
    padding-right: 5px;
}

.social-links {
    display: flex;
    gap: 10px;
    margin-bottom: 15px;
}

.social-links a {
    width: 40px;
    height: 40px;
    border-radius: 50%;
    background: var(--bg-card);
    border: 1px solid var(--border);
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 1.1rem;
    transition: var(--transition);
}

.social-links a:hover {
    background: var(--primary);
    color: white;
    transform: translateY(-3px);
}

.disclaimer {
    font-size: 0.75rem;
    padding: 10px;
    background: rgba(255, 23, 68, 0.1);
    border-radius: var(--radius-sm);
    border: 1px solid rgba(255, 23, 68, 0.2);
    color: var(--accent-red);
}

.footer-bottom {
    text-align: center;
    padding-top: 20px;
    border-top: 1px solid var(--border);
    font-size: 0.8rem;
    color: var(--text-muted);
}

/* ===== Back to Top ===== */
.back-to-top {
    position: fixed;
    bottom: 30px;
    left: 30px;
    width: 45px;
    height: 45px;
    border-radius: 50%;
    background: var(--gradient-primary);
    color: white;
    border: none;
    cursor: pointer;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 1.1rem;
    box-shadow: 0 4px 15px rgba(26, 115, 232, 0.4);
    opacity: 0;
    visibility: hidden;
    transition: var(--transition);
    z-index: 999;
}

.back-to-top.show {
    opacity: 1;
    visibility: visible;
}

.back-to-top:hover {
    transform: translateY(-5px);
}

/* ===== Loading Screen ===== */
.loading-screen {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: var(--bg-dark);
    display: flex;
    align-items: center;
    justify-content: center;
    z-index: 10000;
    transition: opacity 0.5s;
}

.loading-screen.hide {
    opacity: 0;
    pointer-events: none;
}

.loader {
    text-align: center;
}

.loader i {
    font-size: 3rem;
    color: var(--primary);
    margin-bottom: 15px;
}

.loader p {
    color: var(--text-muted);
    font-size: 0.9rem;
}

/* ===== Responsive ===== */
@media (max-width: 1024px) {
    .stat-card.wide {
        grid-column: span 1;
    }
}

@media (max-width: 768px) {
    .nav-links {
        position: fixed;
        top: 70px;
        right: -100%;
        width: 280px;
        height: calc(100vh - 70px);
        background: var(--bg-darker);
        flex-direction: column;
        padding: 20px;
        gap: 5px;
        transition: var(--transition);
        overflow-y: auto;
        border-left: 1px solid var(--border);
        z-index: 999;
    }

    .nav-links.active {
        right: 0;
    }

    .mobile-menu {
        display: flex;
    }

    .hero-content h1 {
        font-size: 2rem;
    }

    .hero-stats {
        gap: 20px;
    }

    .stat-number {
        font-size: 1.8rem;
    }

    .matches-grid,
    .predictions-grid,
    .betting-cards {
        grid-template-columns: 1fr;
    }

    .section-header {
        flex-direction: column;
        align-items: flex-start;
    }

    .calc-grid {
        grid-template-columns: 1fr;
    }
}

@media (max-width: 480px) {
    .hero-content h1 {
        font-size: 1.6rem;
    }

    .hero-content p {
        font-size: 0.9rem;
    }

    .hero-buttons {
        flex-direction: column;
    }

    .btn {
        width: 100%;
        justify-content: center;
    }
}

/* ===== Animations ===== */
@keyframes fadeInUp {
    from {
        opacity: 0;
        transform: translateY(30px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}

@keyframes fadeIn {
    from { opacity: 0; }
    to { opacity: 1; }
}

.animate-in {
    animation: fadeInUp 0.6s ease forwards;
}

.match-card:nth-child(1) { animation-delay: 0.1s; }
.match-card:nth-child(2) { animation-delay: 0.2s; }
.match-card:nth-child(3) { animation-delay: 0.3s; }
.match-card:nth-child(4) { animation-delay: 0.4s; }
.match-card:nth-child(5) { animation-delay: 0.5s; }
.match-card:nth-child(6) { animation-delay: 0.6s; }

/* Scrollbar */
::-webkit-scrollbar {
    width: 8px;
}

::-webkit-scrollbar-track {
    background: var(--bg-darker);
}

::-webkit-scrollbar-thumb {
    background: var(--border);
    border-radius: 4px;
}

::-webkit-scrollbar-thumb:hover {
    background: var(--primary);
}
// ===== قاعدة بيانات الدوريات الكاملة =====
const LEAGUES_DATA = {
    // ===== الدوري المصري =====
    egyptian: {
        name: "الدوري المصري الممتاز",
        country: "مصر",
        flag: "🇪🇬",
        season: "2024/2025",
        teams: 18,
        logo: "⚽",
        color: "#c41e3a",
        standings: [
            { pos: 1, team: "الأهلي", crest: "🔴", p: 34, w: 25, d: 6, l: 3, gf: 68, ga: 18, gd: 50, pts: 81, form: ["W","W","D","W","W"] },
            { pos: 2, team: "الزمالك", crest: "⚪", p: 34, w: 22, d: 7, l: 5, gf: 58, ga: 22, gd: 36, pts: 73, form: ["W","D","W","W","L"] },
            { pos: 3, team: "بيراميدز", crest: "🔵", p: 34, w: 20, d: 8, l: 6, gf: 55, ga: 25, gd: 30, pts: 68, form: ["W","W","W","D","W"] },
            { pos: 4, team: "المصري", crest: "🟢", p: 34, w: 17, d: 9, l: 8, gf: 42, ga: 28, gd: 14, pts: 60, form: ["D","W","L","W","D"] },
            { pos: 5, team: "إنبي", crest: "🟡", p: 34, w: 15, d: 10, l: 9, gf: 40, ga: 30, gd: 10, pts: 55, form: ["L","D","W","W","D"] },
            { pos: 6, team: "الإسماعيلي", crest: "🟡", p: 34, w: 14, d: 11, l: 9, gf: 38, ga: 32, gd: 6, pts: 53, form: ["W","L","D","D","W"] },
            { pos: 7, team: "المقاولون العرب", crest: "🟠", p: 34, w: 13, d: 10, l: 11, gf: 35, ga: 33, gd: 2, pts: 49, form: ["L","W","D","L","W"] },
            { pos: 8, team: "سموحة", crest: "🔵", p: 34, w: 12, d: 11, l: 11, gf: 33, ga: 35, gd: -2, pts: 47, form: ["D","D","W","L","D"] },
            { pos: 9, team: "فيوتشر", crest: "🟣", p: 34, w: 12, d: 10, l: 12, gf: 34, ga: 36, gd: -2, pts: 46, form: ["W","L","L","W","D"] },
            { pos: 10, team: "الاتحاد السكندري", crest: "🟢", p: 34, w: 11, d: 11, l: 12, gf: 30, ga: 34, gd: -4, pts: 44, form: ["D","W","L","D","L"] },
            { pos: 11, team: "سيراميكا كليوباترا", crest: "🟤", p: 34, w: 11, d: 9, l: 14, gf: 28, ga: 38, gd: -10, pts: 42, form: ["L","L","W","D","W"] },
            { pos: 12, team: "طلائع الجيش", crest: "🟢", p: 34, w: 10, d: 11, l: 13, gf: 29, ga: 37, gd: -8, pts: 41, form: ["D","L","D","W","L"] },
            { pos: 13, team: "الجونة", crest: "🟠", p: 34, w: 10, d: 10, l: 14, gf: 32, ga: 42, gd: -10, pts: 40, form: ["W","D","L","L","D"] },
            { pos: 14, team: "غزل المحلة", crest: "🟡", p: 34, w: 9, d: 12, l: 13, gf: 28, ga: 38, gd: -10, pts: 39, form: ["D","D","L","W","L"] },
            { pos: 15, team: "بلدية المحلة", crest: "🟢", p: 34, w: 9, d: 10, l: 15, gf: 25, ga: 40, gd: -15, pts: 37, form: ["L","W","L","D","L"] },
            { pos: 16, team: "الداخلية", crest: "⚫", p: 34, w: 8, d: 10, l: 16, gf: 24, ga: 42, gd: -18, pts: 34, form: ["L","L","D","L","W"] },
            { pos: 17, team: "إيسترن كومباني", crest: "🔵", p: 34, w: 7, d: 9, l: 18, gf: 22, ga: 48, gd: -26, pts: 30, form: ["L","L","L","D","L"] },
            { pos: 18, team: "الألومنيوم", crest: "⚪", p: 34, w: 5, d: 8, l: 21, gf: 18, ga: 55, gd: -37, pts: 23, form: ["L","L","L","L","D"] }
        ],
        matches: [
            { home: "الأهلي", away: "الزمالك", homeScore: 2, awayScore: 1, date: "2025-01-15", time: "21:00", status: "finished", stadium: "القاهرة الدولي" },
            { home: "بيراميدز", away: "المصري", homeScore: null, awayScore: null, date: "2025-01-16", time: "19:00", status: "upcoming", stadium: "الدفاع الجوي" },
            { home: "إنبي", away: "الإسماعيلي", homeScore: 1, awayScore: 1, date: "2025-01-15", time: "17:00", status: "finished", stadium: "بتروسبورت" },
            { home: "سموحة", away: "فيوتشر", homeScore: null, awayScore: null, date: "2025-01-17", time: "20:00", status: "upcoming", stadium: "الإسكندرية" },
            { home: "الزمالك", away: "بيراميدز", homeScore: null, awayScore: null, date: "2025-01-20", time: "21:00", status: "upcoming", stadium: "القاهرة الدولي" },
            { home: "المقاولون العرب", away: "الأهلي", homeScore: 0, awayScore: 3, date: "2025-01-10", time: "20:00", status: "finished", stadium: "عثمان أحمد عثمان" }
        ]
    },

    // ===== الدوري العراقي =====
    iraqi: {
        name: "دوري نجوم العراق",
        country: "العراق",
        flag: "🇮🇶",
        season: "2024/2025",
        teams: 20,
        logo: "⚽",
        color: "#007a3d",
        standings: [
            { pos: 1, team: "القوة الجوية", crest: "🔵", p: 38, w: 24, d: 8, l: 6, gf: 62, ga: 22, gd: 40, pts: 80, form: ["W","W","D","W","W"] },
            { pos: 2, team: "الشرطة", crest: "🟢", p: 38, w: 22, d: 10, l: 6, gf: 55, ga: 20, gd: 35, pts: 76, form: ["W","D","W","W","D"] },
            { pos: 3, team: "الزوراء", crest: "⚪", p: 38, w: 21, d: 9, l: 8, gf: 58, ga: 28, gd: 30, pts: 72, form: ["W","W","L","W","W"] },
            { pos: 4, team: "الطلبة", crest: "🟡", p: 38, w: 19, d: 11, l: 8, gf: 48, ga: 25, gd: 23, pts: 68, form: ["D","W","W","D","W"] },
            { pos: 5, team: "النجف", crest: "🟢", p: 38, w: 18, d: 10, l: 10, gf: 45, ga: 30, gd: 15, pts: 64, form: ["W","L","D","W","W"] },
            { pos: 6, team: "أربيل", crest: "🟡", p: 38, w: 17, d: 11, l: 10, gf: 44, ga: 32, gd: 12, pts: 62, form: ["D","W","W","L","D"] },
            { pos: 7, team: "النفط", crest: "🟢", p: 38, w: 16, d: 10, l: 12, gf: 42, ga: 35, gd: 7, pts: 58, form: ["W","D","L","W","D"] },
            { pos: 8, team: "الكرخ", crest: "🔵", p: 38, w: 15, d: 11, l: 12, gf: 38, ga: 33, gd: 5, pts: 56, form: ["L","W","D","D","W"] },
            { pos: 9, team: "الميناء", crest: "🔵", p: 38, w: 14, d: 12, l: 12, gf: 40, ga: 38, gd: 2, pts: 54, form: ["D","D","W","L","W"] },
            { pos: 10, team: "الحسين", crest: "🟣", p: 38, w: 14, d: 10, l: 14, gf: 36, ga: 38, gd: -2, pts: 52, form: ["W","L","D","W","L"] },
            { pos: 11, team: "نفط الوسط", crest: "🟠", p: 38, w: 13, d: 11, l: 14, gf: 35, ga: 40, gd: -5, pts: 50, form: ["L","D","W","L","D"] },
            { pos: 12, team: "كربلاء", crest: "🔴", p: 38, w: 12, d: 12, l: 14, gf: 33, ga: 38, gd: -5, pts: 48, form: ["D","L","D","W","L"] },
            { pos: 13, team: "الشباب", crest: "⚫", p: 38, w: 12, d: 10, l: 16, gf: 30, ga: 42, gd: -12, pts: 46, form: ["L","W","L","D","L"] },
            { pos: 14, team: "نفط البصرة", crest: "🟢", p: 38, w: 11, d: 11, l: 16, gf: 32, ga: 44, gd: -12, pts: 44, form: ["D","L","L","W","D"] },
            { pos: 15, team: "الصناعة", crest: "🔵", p: 38, w: 11, d: 10, l: 17, gf: 28, ga: 42, gd: -14, pts: 43, form: ["L","D","W","L","L"] },
            { pos: 16, team: "دهوك", crest: "🟡", p: 38, w: 10, d: 11, l: 17, gf: 30, ga: 45, gd: -15, pts: 41, form: ["L","L","D","D","L"] },
            { pos: 17, team: "السليمانية", crest: "🟢", p: 38, w: 9, d: 12, l: 17, gf: 28, ga: 46, gd: -18, pts: 39, form: ["D","L","L","D","L"] },
            { pos: 18, team: "زاخو", crest: "🔴", p: 38, w: 8, d: 11, l: 19, gf: 25, ga: 48, gd: -23, pts: 35, form: ["L","L","D","L","L"] },
            { pos: 19, team: "الكهرباء", crest: "🟡", p: 38, w: 7, d: 10, l: 21, gf: 22, ga: 52, gd: -30, pts: 31, form: ["L","L","L","D","L"] },
            { pos: 20, team: "الحدود", crest: "🟤", p: 38, w: 5, d: 9, l: 24, gf: 18, ga: 58, gd: -40, pts: 24, form: ["L","L","L","L","D"] }
        ],
        matches: [
            { home: "القوة الجوية", away: "الزوراء", homeScore: 3, awayScore: 1, date: "2025-01-15", time: "18:00", status: "finished", stadium: "الشعب" },
            { home: "الشرطة", away: "الطلبة", homeScore: null, awayScore: null, date: "2025-01-16", time: "16:00", status: "upcoming", stadium: "الشعب" },
            { home: "النجف", away: "أربيل", homeScore: 2, awayScore: 2, date: "2025-01-15", time: "15:00", status: "finished", stadium: "النجف" },
            { home: "الميناء", away: "النفط", homeScore: null, awayScore: null, date: "2025-01-17", time: "17:00", status: "upcoming", stadium: "البصرة" },
            { home: "القوة الجوية", away: "الشرطة", homeScore: null, awayScore: null, date: "2025-01-22", time: "19:00", status: "upcoming", stadium: "الشعب" },
            { home: "كربلاء", away: "الزوراء", homeScore: 0, awayScore: 2, date: "2025-01-12", time: "16:00", status: "finished", stadium: "كربلاء" }
        ]
    },

    // ===== الدوري السعودي =====
    saudi: {
        name: "دوري روشن السعودي",
        country: "السعودية",
        flag: "🇸🇦",
        season: "2024/2025",
        teams: 18,
        logo: "⚽",
        color: "#006c35",
        standings: [
            { pos: 1, team: "الهلال", crest: "🔵", p: 34, w: 27, d: 4, l: 3, gf: 78, ga: 18, gd: 60, pts: 85, form: ["W","W","W","D","W"] },
            { pos: 2, team: "الاتحاد", crest: "⚫", p: 34, w: 23, d: 6, l: 5, gf: 65, ga: 25, gd: 40, pts: 75, form: ["W","W","D","W","W"] },
            { pos: 3, team: "النصر", crest: "🟡", p: 34, w: 22, d: 7, l: 5, gf: 70, ga: 28, gd: 42, pts: 73, form: ["W","D","W","W","L"] },
            { pos: 4, team: "الأهلي", crest: "🟢", p: 34, w: 20, d: 8, l: 6, gf: 55, ga: 22, gd: 33, pts: 68, form: ["D","W","W","W","D"] },
            { pos: 5, team: "الشباب", crest: "⚪", p: 34, w: 16, d: 10, l: 8, gf: 45, ga: 30, gd: 15, pts: 58, form: ["W","D","L","W","D"] },
            { pos: 6, team: "الرائد", crest: "🟤", p: 34, w: 15, d: 9, l: 10, gf: 40, ga: 32, gd: 8, pts: 54, form: ["D","W","W","L","D"] },
            { pos: 7, team: "الفيحاء", crest: "🟡", p: 34, w: 14, d: 10, l: 10, gf: 38, ga: 34, gd: 4, pts: 52, form: ["W","L","D","W","L"] },
            { pos: 8, team: "الخليج", crest: "🟠", p: 34, w: 13, d: 11, l: 10, gf: 35, ga: 32, gd: 3, pts: 50, form: ["D","D","W","L","W"] },
            { pos: 9, team: "التعاون", crest: "🟡", p: 34, w: 13, d: 9, l: 12, gf: 38, ga: 38, gd: 0, pts: 48, form: ["L","W","D","D","W"] },
            { pos: 10, team: "الفتح", crest: "🟢", p: 34, w: 12, d: 10, l: 12, gf: 34, ga: 36, gd: -2, pts: 46, form: ["D","L","W","W","L"] },
            { pos: 11, team: "أبها", crest: "🔴", p: 34, w: 11, d: 11, l: 12, gf: 30, ga: 35, gd: -5, pts: 44, form: ["L","D","D","W","L"] },
            { pos: 12, team: "ضمك", crest: "🟠", p: 34, w: 11, d: 9, l: 14, gf: 32, ga: 40, gd: -8, pts: 42, form: ["W","L","L","D","D"] },
            { pos: 13, team: "الوحدة", crest: "🔴", p: 34, w: 10, d: 10, l: 14, gf: 28, ga: 38, gd: -10, pts: 40, form: ["L","D","L","W","D"] },
            { pos: 14, team: "الحزم", crest: "🟤", p: 34, w: 9, d: 11, l: 14, gf: 28, ga: 42, gd: -14, pts: 38, form: ["D","L","D","L","W"] },
            { pos: 15, team: "الطائي", crest: "🟣", p: 34, w: 9, d: 9, l: 16, gf: 25, ga: 44, gd: -19, pts: 36, form: ["L","L","W","L","D"] },
            { pos: 16, team: "العين", crest: "🟠", p: 34, w: 8, d: 10, l: 16, gf: 24, ga: 45, gd: -21, pts: 34, form: ["L","D","L","L","W"] },
            { pos: 17, team: "الجبلين", crest: "🟢", p: 34, w: 6, d: 9, l: 19, gf: 20, ga: 50, gd: -30, pts: 27, form: ["L","L","L","D","L"] },
            { pos: 18, team: "الأخدود", crest: "🟤", p: 34, w: 4, d: 7, l: 23, gf: 15, ga: 58, gd: -43, pts: 19, form: ["L","L","L","L","L"] }
        ],
        matches: [
            { home: "الهلال", away: "النصر", homeScore: 3, awayScore: 2, date: "2025-01-15", time: "21:00", status: "finished", stadium: "الملك فهد" },
            { home: "الاتحاد", away: "الأهلي", homeScore: null, awayScore: null, date: "2025-01-16", time: "20:00", status: "upcoming", stadium: "الجوهرة" },
            { home: "الشباب", away: "الرائد", homeScore: 1, awayScore: 0, date: "2025-01-15", time: "17:00", status: "finished", stadium: "الملك فهد" },
            { home: "النصر", away: "الاتحاد", homeScore: null, awayScore: null, date: "2025-01-20", time: "21:30", status: "upcoming", stadium: "مرسول بارك" }
        ]
    },

    // ===== الدوري الإنجليزي =====
    english: {
        name: "الدوري الإنجليزي الممتاز",
        country: "إنجلترا",
        flag: "🏴󠁧󠁢󠁥󠁮󠁧󠁿",
        season: "2024/2025",
        teams: 20,
        logo: "🦁",
        color: "#3d195b",
        standings: [
            { pos: 1, team: "ليفربول", crest: "🔴", p: 38, w: 28, d: 6, l: 4, gf: 85, ga: 28, gd: 57, pts: 90, form: ["W","W","W","D","W"] },
            { pos: 2, team: "مانشستر سيتي", crest: "🔵", p: 38, w: 27, d: 7, l: 4, gf: 90, ga: 30, gd: 60, pts: 88, form: ["W","W","D","W","W"] },
            { pos: 3, team: "أرسنال", crest: "🔴", p: 38, w: 26, d: 8, l: 4, gf: 82, ga: 25, gd: 57, pts: 86, form: ["W","D","W","W","W"] },
            { pos: 4, team: "أستون فيلا", crest: "🟤", p: 38, w: 22, d: 7, l: 9, gf: 68, ga: 42, gd: 26, pts: 73, form: ["W","W","L","D","W"] },
            { pos: 5, team: "توتنهام", crest: "⚪", p: 38, w: 20, d: 6, l: 12, gf: 72, ga: 55, gd: 17, pts: 66, form: ["L","W","W","W","D"] },
            { pos: 6, team: "نيوكاسل", crest: "⚫", p: 38, w: 18, d: 10, l: 10, gf: 58, ga: 42, gd: 16, pts: 64, form: ["D","W","D","W","W"] },
            { pos: 7, team: "مانشستر يونايتد", crest: "🔴", p: 38, w: 17, d: 8, l: 13, gf: 52, ga: 50, gd: 2, pts: 59, form: ["L","D","W","L","W"] },
            { pos: 8, team: "تشيلسي", crest: "🔵", p: 38, w: 16, d: 9, l: 13, gf: 60, ga: 52, gd: 8, pts: 57, form: ["W","L","D","W","L"] },
            { pos: 9, team: "برايتون", crest: "🔵", p: 38, w: 15, d: 10, l: 13, gf: 55, ga: 48, gd: 7, pts: 55, form: ["D","W","L","D","W"] },
            { pos: 10, team: "ويست هام", crest: "🟤", p: 38, w: 14, d: 10, l: 14, gf: 50, ga: 52, gd: -2, pts: 52, form: ["W","L","D","L","W"] },
            { pos: 11, team: "بورنموث", crest: "🔴", p: 38, w: 13, d: 10, l: 15, gf: 45, ga: 55, gd: -10, pts: 49, form: ["L","D","W","L","D"] },
            { pos: 12, team: "كريستال بالاس", crest: "🔵", p: 38, w: 13, d: 9, l: 16, gf: 42, ga: 52, gd: -10, pts: 48, form: ["D","L","W","W","L"] },
            { pos: 13, team: "وولفرهامبتون", crest: "🟠", p: 38, w: 12, d: 10, l: 16, gf: 44, ga: 55, gd: -11, pts: 46, form: ["L","W","L","D","D"] },
            { pos: 14, team: "فولهام", crest: "⚪", p: 38, w: 12, d: 8, l: 18, gf: 42, ga: 58, gd: -16, pts: 44, form: ["L","D","L","W","L"] },
            { pos: 15, team: "إيفرتون", crest: "🔵", p: 38, w: 11, d: 9, l: 18, gf: 38, ga: 52, gd: -14, pts: 42, form: ["D","L","L","D","W"] },
            { pos: 16, team: "بيرنلي", crest: "🟤", p: 38, w: 10, d: 9, l: 19, gf: 35, ga: 58, gd: -23, pts: 39, form: ["L","L","D","L","W"] },
            { pos: 17, team: "نوتنغهام فورست", crest: "🔴", p: 38, w: 9, d: 10, l: 19, gf: 35, ga: 60, gd: -25, pts: 37, form: ["L","D","L","L","D"] },
            { pos: 18, team: "لوتون تاون", crest: "🟠", p: 38, w: 8, d: 8, l: 22, gf: 42, ga: 72, gd: -30, pts: 32, form: ["L","L","L","W","L"] },
            { pos: 19, team: "شيفيلد يونايتد", crest: "🔴", p: 38, w: 5, d: 7, l: 26, gf: 30, ga: 80, gd: -50, pts: 22, form: ["L","L","L","L","D"] },
            { pos: 20, team: "ليستر سيتي", crest: "🔵", p: 38, w: 4, d: 8, l: 26, gf: 28, ga: 82, gd: -54, pts: 20, form: ["L","L","D","L","L"] }
        ],
        matches: [
            { home: "ليفربول", away: "مانشستر سيتي", homeScore: 2, awayScore: 2, date: "2025-01-15", time: "22:00", status: "finished", stadium: "أنفيلد" },
            { home: "أرسنال", away: "تشيلسي", homeScore: null, awayScore: null, date: "2025-01-16", time: "21:30", status: "upcoming", stadium: "الإمارات" },
            { home: "مانشستر يونايتد", away: "توتنهام", homeScore: null, awayScore: null, date: "2025-01-17", time: "18:30", status: "upcoming", stadium: "أولد ترافورد" },
            { home: "نيوكاسل", away: "أستون فيلا", homeScore: 3, awayScore: 1, date: "2025-01-14", time: "21:00", status: "finished", stadium: "سانت جيمس بارك" }
        ]
    },

    // ===== الدوري الإسباني =====
    spanish: {
        name: "الدوري الإسباني - لا ليغا",
        country: "إسبانيا",
        flag: "🇪🇸",
        season: "2024/2025",
        teams: 20,
        logo: "🐂",
        color: "#ee2523",
        standings: [
            { pos: 1, team: "ريال مدريد", crest: "⚪", p: 38, w: 27, d: 6, l: 5, gf: 82, ga: 28, gd: 54, pts: 87, form: ["W","W","D","W","W"] },
            { pos: 2, team: "برشلونة", crest: "🔵", p: 38, w: 26, d: 8, l: 4, gf: 78, ga: 25, gd: 53, pts: 86, form: ["W","D","W","W","W"] },
            { pos: 3, team: "أتلتيكو مدريد", crest: "🔴", p: 38, w: 23, d: 9, l: 6, gf: 65, ga: 28, gd: 37, pts: 78, form: ["D","W","W","W","D"] },
            { pos: 4, team: "جيرونا", crest: "🔴", p: 38, w: 22, d: 7, l: 9, gf: 72, ga: 42, gd: 30, pts: 73, form: ["W","W","L","W","D"] },
            { pos: 5, team: "ريال سوسيداد", crest: "🔵", p: 38, w: 18, d: 10, l: 10, gf: 52, ga: 38, gd: 14, pts: 64, form: ["D","W","D","L","W"] },
            { pos: 6, team: "ريال بيتيس", crest: "🟢", p: 38, w: 17, d: 9, l: 12, gf: 48, ga: 42, gd: 6, pts: 60, form: ["W","L","W","D","W"] },
            { pos: 7, team: "فياريال", crest: "🟡", p: 38, w: 16, d: 10, l: 12, gf: 55, ga: 48, gd: 7, pts: 58, form: ["L","W","D","W","D"] },
            { pos: 8, team: "أتلتيك بلباو", crest: "🔴", p: 38, w: 15, d: 12, l: 11, gf: 45, ga: 38, gd: 7, pts: 57, form: ["D","D","W","W","L"] },
            { pos: 9, team: "فالنسيا", crest: "🟠", p: 38, w: 14, d: 10, l: 14, gf: 42, ga: 45, gd: -3, pts: 52, form: ["W","L","D","L","W"] },
            { pos: 10, team: "أوساسونا", crest: "🔴", p: 38, w: 13, d: 11, l: 14, gf: 38, ga: 42, gd: -4, pts: 50, form: ["D","L","W","D","L"] },
            { pos: 11, team: "سيلتا فيغو", crest: "🔵", p: 38, w: 13, d: 9, l: 16, gf: 42, ga: 50, gd: -8, pts: 48, form: ["L","W","L","W","D"] },
            { pos: 12, team: "إشبيلية", crest: "⚪", p: 38, w: 12, d: 10, l: 16, gf: 40, ga: 48, gd: -8, pts: 46, form: ["D","L","D","W","L"] },
            { pos: 13, team: "مايوركا", crest: "🔴", p: 38, w: 11, d: 12, l: 15, gf: 32, ga: 45, gd: -13, pts: 45, form: ["L","D","L","D","W"] },
            { pos: 14, team: "خيتافي", crest: "🔵", p: 38, w: 11, d: 11, l: 16, gf: 35, ga: 48, gd: -13, pts: 44, form: ["D","L","W","L","D"] },
            { pos: 15, team: "ألافيس", crest: "🔵", p: 38, w: 11, d: 10, l: 17, gf: 30, ga: 48, gd: -18, pts: 43, form: ["L","L","D","W","L"] },
            { pos: 16, team: "لاس بالماس", crest: "🟡", p: 38, w: 10, d: 10, l: 18, gf: 32, ga: 50, gd: -18, pts: 40, form: ["L","D","L","L","W"] },
            { pos: 17, team: "رايو فاييكانو", crest: "⚪", p: 38, w: 9, d: 11, l: 18, gf: 28, ga: 48, gd: -20, pts: 38, form: ["D","L","L","D","L"] },
            { pos: 18, team: "قادش", crest: "🟡", p: 38, w: 8, d: 10, l: 20, gf: 25, ga: 55, gd: -30, pts: 34, form: ["L","L","D","L","L"] },
            { pos: 19, team: "غرناطة", crest: "🔴", p: 38, w: 6, d: 9, l: 23, gf: 28, ga: 62, gd: -34, pts: 27, form: ["L","L","L","D","L"] },
            { pos: 20, team: "ألميريا", crest: "🔴", p: 38, w: 5, d: 8, l: 25, gf: 22, ga: 68, gd: -46, pts: 23, form: ["L","L","L","L","D"] }
        ],
        matches: [
            { home: "ريال مدريد", away: "برشلونة", homeScore: 3, awayScore: 2, date: "2025-01-15", time: "22:00", status: "finished", stadium: "سانتياغو برنابيو" },
            { home: "أتلتيكو مدريد", away: "جيرونا", homeScore: null, awayScore: null, date: "2025-01-16", time: "21:00", status: "upcoming", stadium: "واندا ميتروبوليتانو" },
            { home: "ريال سوسيداد", away: "فياريال", homeScore: 1, awayScore: 1, date: "2025-01-14", time: "19:00", status: "finished", stadium: "أنويتا" }
        ]
    },

    // ===== الدوري الإيطالي =====
    italian: {
        name: "الدوري الإيطالي - سيري آ",
        country: "إيطاليا",
        flag: "🇮🇹",
        season: "2024/2025",
        teams: 20,
        logo: "🏟️",
        color: "#009246",
        standings: [
            { pos: 1, team: "إنتر ميلان", crest: "🔵", p: 38, w: 27, d: 7, l: 4, gf: 82, ga: 28, gd: 54, pts: 88, form: ["W","W","W","D","W"] },
            { pos: 2, team: "يوفنتوس", crest: "⚫", p: 38, w: 24, d: 9, l: 5, gf: 68, ga: 25, gd: 43, pts: 81, form: ["D","W","W","W","D"] },
            { pos: 3, team: "ميلان", crest: "🔴", p: 38, w: 22, d: 8, l: 8, gf: 65, ga: 38, gd: 27, pts: 74, form: ["W","L","W","W","W"] },
            { pos: 4, team: "نابولي", crest: "🔵", p: 38, w: 21, d: 8, l: 9, gf: 62, ga: 35, gd: 27, pts: 71, form: ["W","W","D","L","W"] },
            { pos: 5, team: "أتالانتا", crest: "🔵", p: 38, w: 19, d: 9, l: 10, gf: 68, ga: 42, gd: 26, pts: 66, form: ["W","D","W","W","L"] },
            { pos: 6, team: "لاتسيو", crest: "🔵", p: 38, w: 18, d: 8, l: 12, gf: 55, ga: 42, gd: 13, pts: 62, form: ["L","W","D","W","W"] },
            { pos: 7, team: "روما", crest: "🟡", p: 38, w: 17, d: 9, l: 12, gf: 52, ga: 45, gd: 7, pts: 60, form: ["D","W","L","W","D"] },
            { pos: 8, team: "فيورنتينا", crest: "🟣", p: 38, w: 16, d: 10, l: 12, gf: 48, ga: 42, gd: 6, pts: 58, form: ["W","D","D","L","W"] },
            { pos: 9, team: "بولونيا", crest: "🔴", p: 38, w: 15, d: 10, l: 13, gf: 45, ga: 44, gd: 1, pts: 55, form: ["D","W","L","D","W"] },
            { pos: 10, team: "تورينو", crest: "🟤", p: 38, w: 14, d: 10, l: 14, gf: 42, ga: 45, gd: -3, pts: 52, form: ["L","D","W","W","L"] },
            { pos: 11, team: "مونزا", crest: "🔴", p: 38, w: 13, d: 11, l: 14, gf: 38, ga: 42, gd: -4, pts: 50, form: ["D","L","D","W","L"] },
            { pos: 12, team: "جنوى", crest: "🔴", p: 38, w: 12, d: 11, l: 15, gf: 40, ga: 48, gd: -8, pts: 47, form: ["W","L","D","L","D"] },
            { pos: 13, team: "ساسولو", crest: "🟢", p: 38, w: 12, d: 9, l: 17, gf: 42, ga: 52, gd: -10, pts: 45, form: ["L","W","L","D","L"] },
            { pos: 14, team: "ليتشي", crest: "🟡", p: 38, w: 11, d: 10, l: 17, gf: 35, ga: 48, gd: -13, pts: 43, form: ["D","L","L","W","D"] },
            { pos: 15, team: "أودينيزي", crest: "⚫", p: 38, w: 10, d: 12, l: 16, gf: 35, ga: 50, gd: -15, pts: 42, form: ["L","D","D","L","W"] },
            { pos: 16, team: "كالياري", crest: "🔴", p: 38, w: 10, d: 10, l: 18, gf: 32, ga: 52, gd: -20, pts: 40, form: ["L","L","W","D","L"] },
            { pos: 17, team: "إمبولي", crest: "🔵", p: 38, w: 9, d: 11, l: 18, gf: 30, ga: 50, gd: -20, pts: 38, form: ["D","L","L","D","L"] },
            { pos: 18, team: "فروزينوني", crest: "🟡", p: 38, w: 8, d: 9, l: 21, gf: 28, ga: 58, gd: -30, pts: 33, form: ["L","L","L","D","L"] },
            { pos: 19, team: "هيلاس فيرونا", crest: "🟡", p: 38, w: 6, d: 10, l: 22, gf: 25, ga: 60, gd: -35, pts: 28, form: ["L","D","L","L","L"] },
            { pos: 20, team: "ساليرنيتانا", crest: "🟤", p: 38, w: 4, d: 8, l: 26, gf: 18, ga: 68, gd: -50, pts: 20, form: ["L","L","L","L","D"] }
        ],
        matches: [
            { home: "إنتر ميلان", away: "ميلان", homeScore: 2, awayScore: 1, date: "2025-01-15", time: "21:45", status: "finished", stadium: "سان سيرو" },
            { home: "يوفنتوس", away: "نابولي", homeScore: null, awayScore: null, date: "2025-01-16", time: "20:45", status: "upcoming", stadium: "أليانز ستاديوم" },
            { home: "روما", away: "لاتسيو", homeScore: null, awayScore: null, date: "2025-01-18", time: "21:00", status: "upcoming", stadium: "الأولمبيكو" }
        ]
    },

    // ===== دوري أبطال أوروبا =====
    champions: {
        name: "دوري أبطال أوروبا",
        country: "أوروبا",
        flag: "🏆",
        season: "2024/2025",
        teams: 36,
        logo: "⭐",
        color: "#1b365d",
        standings: [
            { pos: 1, team: "ريال مدريد", crest: "⚪", p: 8, w: 7, d: 1, l: 0, gf: 22, ga: 5, gd: 17, pts: 22, form: ["W","W","W","D","W"] },
            { pos: 2, team: "مانشستر سيتي", crest: "🔵", p: 8, w: 6, d: 2, l: 0, gf: 20, ga: 6, gd: 14, pts: 20, form: ["W","D","W","W","W"] },
            { pos: 3, team: "بايرن ميونخ", crest: "🔴", p: 8, w: 6, d: 1, l: 1, gf: 18, ga: 8, gd: 10, pts: 19, form: ["W","W","L","W","W"] },
            { pos: 4, team: "برشلونة", crest: "🔵", p: 8, w: 5, d: 2, l: 1, gf: 16, ga: 7, gd: 9, pts: 17, form: ["W","D","W","W","D"] },
            { pos: 5, team: "باريس سان جيرمان", crest: "🔵", p: 8, w: 5, d: 2, l: 1, gf: 15, ga: 8, gd: 7, pts: 17, form: ["D","W","W","W","L"] },
            { pos: 6, team: "إنتر ميلان", crest: "🔵", p: 8, w: 5, d: 1, l: 2, gf: 14, ga: 9, gd: 5, pts: 16, form: ["W","W","L","W","W"] },
            { pos: 7, team: "دورتموند", crest: "🟡", p: 8, w: 4, d: 3, l: 1, gf: 12, ga: 7, gd: 5, pts: 15, form: ["D","W","D","W","W"] },
            { pos: 8, team: "أرسنال", crest: "🔴", p: 8, w: 4, d: 2, l: 2, gf: 13, ga: 9, gd: 4, pts: 14, form: ["W","L","W","D","W"] }
        ],
        matches: [
            { home: "ريال مدريد", away: "بايرن ميونخ", homeScore: 2, awayScore: 1, date: "2025-01-15", time: "22:00", status: "finished", stadium: "سانتياغو برنابيو" },
            { home: "مانشستر سيتي", away: "باريس سان جيرمان", homeScore: null, awayScore: null, date: "2025-01-16", time: "22:00", status: "upcoming", stadium: "الاتحاد" },
            { home: "برشلونة", away: "إنتر ميلان", homeScore: null, awayScore: null, date: "2025-01-18", time: "22:00", status: "upcoming", stadium: "كامب نو" }
        ]
    },

    // ===== الدوري الهولندي =====
    dutch: {
        name: "الدوري الهولندي - إيريديفيزي",
        country: "هولندا",
        flag: "🇳🇱",
        season: "2024/2025",
        teams: 18,
        logo: "🌷",
        color: "#FF6600",
        standings: [
            { pos: 1, team: "آيندهوفن", crest: "🔴", p: 34, w: 26, d: 5, l: 3, gf: 88, ga: 22, gd: 66, pts: 83, form: ["W","W","W","D","W"] },
            { pos: 2, team: "أياكس", crest: "🔴", p: 34, w: 23, d: 7, l: 4, gf: 75, ga: 28, gd: 47, pts: 76, form: ["W","D","W","W","W"] },
            { pos: 3, team: "فاينورد", crest: "🔴", p: 34, w: 22, d: 6, l: 6, gf: 72, ga: 32, gd: 40, pts: 72, form: ["W","W","L","W","D"] },
            { pos: 4, team: "تفينتي", crest: "🔴", p: 34, w: 19, d: 8, l: 7, gf: 58, ga: 30, gd: 28, pts: 65, form: ["D","W","W","D","W"] },
            { pos: 5, team: "آز ألكمار", crest: "🔴", p: 34, w: 17, d: 9, l: 8, gf: 55, ga: 35, gd: 20, pts: 60, form: ["W","D","L","W","W"] },
            { pos: 6, team: "أوتريخت", crest: "🔴", p: 34, w: 16, d: 8, l: 10, gf: 50, ga: 38, gd: 12, pts: 56, form: ["D","W","W","L","D"] },
            { pos: 7, team: "سبارتا روتردام", crest: "🔴", p: 34, w: 14, d: 10, l: 10, gf: 42, ga: 35, gd: 7, pts: 52, form: ["W","L","D","W","D"] },
            { pos: 8, team: "هيرينفين", crest: "🔵", p: 34, w: 13, d: 9, l: 12, gf: 45, ga: 42, gd: 3, pts: 48, form: ["L","D","W","D","W"] },
            { pos: 9, team: "فيتيسه", crest: "🟡", p: 34, w: 12, d: 10, l: 12, gf: 42, ga: 42, gd: 0, pts: 46, form: ["D","W","L","W","L"] },
            { pos: 10, team: "غو أهيد إيغلز", crest: "🔴", p: 34, w: 12, d: 8, l: 14, gf: 40, ga: 48, gd: -8, pts: 44, form: ["L","W","D","L","W"] },
            { pos: 11, team: "نيك بريدا", crest: "🔴", p: 34, w: 11, d: 10, l: 13, gf: 38, ga: 45, gd: -7, pts: 43, form: ["D","L","W","L","D"] },
            { pos: 12, team: "فولندام", crest: "🟢", p: 34, w: 11, d: 8, l: 15, gf: 42, ga: 52, gd: -10, pts: 41, form: ["W","L","L","D","L"] },
            { pos: 13, team: "هيراكليس", crest: "⚫", p: 34, w: 10, d: 10, l: 14, gf: 35, ga: 45, gd: -10, pts: 40, form: ["L","D","D","W","L"] },
            { pos: 14, team: "فيلم تو", crest: "🟢", p: 34, w: 10, d: 9, l: 15, gf: 35, ga: 48, gd: -13, pts: 39, form: ["D","L","L","W","D"] },
            { pos: 15, team: "والفايك", crest: "🔴", p: 34, w: 9, d: 10, l: 15, gf: 32, ga: 48, gd: -16, pts: 37, form: ["L","D","L","D","L"] },
            { pos: 16, team: "إكسلسيور", crest: "🔴", p: 34, w: 8, d: 9, l: 17, gf: 30, ga: 52, gd: -22, pts: 33, form: ["L","L","D","L","W"] },
            { pos: 17, team: "إيمن", crest: "🔴", p: 34, w: 6, d: 8, l: 20, gf: 28, ga: 60, gd: -32, pts: 26, form: ["L","L","L","D","L"] },
            { pos: 18, team: "ألميري سيتي", crest: "🔴", p: 34, w: 4, d: 8, l: 22, gf: 20, ga: 65, gd: -45, pts: 20, form: ["L","L","L","L","D"] }
        ],
        matches: [
            { home: "آيندهوفن", away: "أياكس", homeScore: 3, awayScore: 1, date: "2025-01-15", time: "20:45", status: "finished", stadium: "فيليبس ستاديون" },
            { home: "فاينورد", away: "تفينتي", homeScore: null, awayScore: null, date: "2025-01-16", time: "20:00", status: "upcoming", stadium: "دي كويب" },
            { home: "آز ألكمار", away: "أوتريخت", homeScore: 2, awayScore: 0, date: "2025-01-14", time: "18:45", status: "finished", stadium: "أفاس ستاديون" }
        ]
    }
};

// تصدير البيانات
if (typeof module !== 'undefined') {
    module.exports = LEAGUES_DATA;
}
// ===== بيانات المباريات المباشرة والتوقعات =====

const PREDICTIONS_DATA = {
    predictions: [
        {
            league: "egyptian",
            match: "الأهلي vs الزمالك",
            date: "2025-01-20",
            prediction: "فوز الأهلي",
            odds: 1.85,
            confidence: 82,
            confidenceLevel: "high",
            tips: [
                { label: "النتيجة المتوقعة", value: "2-1" },
                { label: "أكثر/أقل من 2.5", value: "أكثر (Over)" },
                { label: "كلا الفريقين يسجل", value: "نعم (BTTS)" },
                { label: "الشوط الأول", value: "1-0 أهلي" }
            ],
            analysis: "الأهلي يتفوق في آخر 10 مواجهات بـ 7 انتصارات. دفاع الزمالك يعاني من الإصابات. الأهلي لم يخسر في آخر 15 مباراة على أرضه."
        },
        {
            league: "english",
            match: "أرسنال vs تشيلسي",
            date: "2025-01-16",
            prediction: "فوز أرسنال",
            odds: 1.95,
            confidence: 75,
            confidenceLevel: "high",
            tips: [
                { label: "النتيجة المتوقعة", value: "2-0" },
                { label: "أكثر/أقل من 2.5", value: "أقل (Under)" },
                { label: "كلا الفريقين يسجل", value: "لا" },
                { label: "عدد الأهداف", value: "1-2 أهداف" }
            ],
            analysis: "أرسنال يملك أقوى دفاع في البريميرليغ. تشيلسي يعاني خارج أرضه. ساكا في أفضل حالاته التهديفية هذا الموسم."
        },
        {
            league: "spanish",
            match: "أتلتيكو مدريد vs جيرونا",
            date: "2025-01-16",
            prediction: "تعادل",
            odds: 3.20,
            confidence: 60,
            confidenceLevel: "medium",
            tips: [
                { label: "النتيجة المتوقعة", value: "1-1" },
                { label: "أكثر/أقل من 2.5", value: "أقل (Under)" },
                { label: "كلا الفريقين يسجل", value: "نعم (BTTS)" },
                { label: "الهانديكاب", value: "جيرونا +0.5" }
            ],
            analysis: "جيرونا يلعب أفضل كرة هجومية في إسبانيا هذا الموسم. أتلتيكو قوي دفاعياً لكن يعاني في الهجوم. توقع مباراة تكتيكية."
        },
        {
            league: "italian",
            match: "يوفنتوس vs نابولي",
            date: "2025-01-16",
            prediction: "فوز يوفنتوس",
            odds: 2.10,
            confidence: 68,
            confidenceLevel: "medium",
            tips: [
                { label: "النتيجة المتوقعة", value: "2-1" },
                { label: "أكثر/أقل من 2.5", value: "أكثر (Over)" },
                { label: "كلا الفريقين يسجل", value: "نعم (BTTS)" },
                { label: "أول هدف", value: "يوفنتوس" }
            ],
            analysis: "يوفنتوس لا يُهزم على أرضه منذ 12 مباراة. نابولي يعاني بدون أوسيمن. فلاهوفيتش في فورم تهديفي ممتاز."
        },
        {
            league: "iraqi",
            match: "القوة الجوية vs الشرطة",
            date: "2025-01-22",
            prediction: "فوز القوة الجوية",
            odds: 1.75,
            confidence: 78,
            confidenceLevel: "high",
            tips: [
                { label: "النتيجة المتوقعة", value: "2-0" },
                { label: "أكثر/أقل من 2.5", value: "أقل (Under)" },
                { label: "كلا الفريقين يسجل", value: "لا" },
                { label: "نتيجة الشوط الأول", value: "1-0" }
            ],
            analysis: "القوة الجوية متصدر الدوري بجدارة. الشرطة تراجع مستواه في المباريات الأخيرة. مباريات القمة عادة ما تكون حذرة."
        },
        {
            league: "saudi",
            match: "النصر vs الاتحاد",
            date: "2025-01-20",
            prediction: "فوز النصر",
            odds: 2.00,
            confidence: 72,
            confidenceLevel: "high",
            tips: [
                { label: "النتيجة المتوقعة", value: "3-1" },
                { label: "أكثر/أقل من 2.5", value: "أكثر (Over)" },
                { label: "كلا الفريقين يسجل", value: "نعم (BTTS)" },
                { label: "هداف المباراة", value: "رونالدو" }
            ],
            analysis: "النصر في فورم ممتاز بقيادة رونالدو. الاتحاد يعاني من غيابات في الدفاع. مرسول بارك يمنح النصر أفضلية كبيرة."
        },
        {
            league: "dutch",
            match: "فاينورد vs تفينتي",
            date: "2025-01-16",
            prediction: "فوز فاينورد",
            odds: 1.65,
            confidence: 80,
            confidenceLevel: "high",
            tips: [
                { label: "النتيجة المتوقعة", value: "3-1" },
                { label: "أكثر/أقل من 2.5", value: "أكثر (Over)" },
                { label: "كلا الفريقين يسجل", value: "نعم (BTTS)" },
                { label: "عدد الركنيات", value: "أكثر من 9" }
            ],
            analysis: "فاينورد يلعب بشكل هجومي مميز هذا الموسم. ملعب دي كويب حصن منيع. تفينتي يعاني دفاعياً في المباريات الخارجية."
        },
        {
            league: "champions",
            match: "برشلونة vs إنتر ميلان",
            date: "2025-01-18",
            prediction: "فوز برشلونة",
            odds: 1.90,
            confidence: 70,
            confidenceLevel: "medium",
            tips: [
                { label: "النتيجة المتوقعة", value: "2-1" },
                { label: "أكثر/أقل من 2.5", value: "أكثر (Over)" },
                { label: "كلا الفريقين يسجل", value: "نعم (BTTS)" },
                { label: "أكثر أهداف في", value: "الشوط الثاني" }
            ],
            analysis: "برشلونة يتألق في كامب نو. إنتر فريق قوي لكنه يعاني أوروبياً خارج أرضه. يامال في حالة استثنائية."
        }
    ],

    bettingTips: [
        {
            league: "egyptian",
            match: "الأهلي vs الزمالك",
            isHot: true,
            tips: [
                { label: "الرهان المقترح", value: "فوز الأهلي + أكثر من 1.5 هدف", odds: "2.40", confidence: "high" },
                { label: "الرهان الآمن", value: "فوز الأهلي أو تعادل (1X)", odds: "1.30", confidence: "high" },
                { label: "رهان القيمة", value: "الأهلي يسجل في الشوطين", odds: "2.80", confidence: "medium" }
            ],
            reason: "الأهلي فاز في 8 من آخر 10 ديربيات. متوسط الأهداف في الديربي 2.8 هدف."
        },
        {
            league: "english",
            match: "ليفربول vs مانشستر سيتي",
            isHot: true,
            tips: [
                { label: "الرهان المقترح", value: "كلا الفريقين يسجل (BTTS)", odds: "1.65", confidence: "high" },
                { label: "الرهان الآمن", value: "أكثر من 1.5 هدف", odds: "1.25", confidence: "high" },
                { label: "رهان القيمة", value: "أكثر من 3.5 أهداف", odds: "2.50", confidence: "medium" }
            ],
            reason: "آخر 8 مباريات بين الفريقين شهدت أكثر من 2.5 هدف. كلا الفريقين في فورم تهديفي."
        },
        {
            league: "iraqi",
            match: "الزوراء vs الطلبة",
            isHot: false,
            tips: [
                { label: "الرهان المقترح", value: "فوز الزوراء", odds: "1.80", confidence: "high" },
                { label: "الرهان الآمن", value: "أقل من 2.5 هدف (Under)", odds: "1.55", confidence: "high" },
                { label: "رهان القيمة", value: "الزوراء يفوز بدون استقبال أهداف", odds: "3.00", confidence: "medium" }
            ],
            reason: "الزوراء أفضل فريق هجومياً في الدوري. الطلبة تراجع في آخر 5 مباريات."
        },
        {
            league: "saudi",
            match: "الهلال vs النصر",
            isHot: true,
            tips: [
                { label: "الرهان المقترح", value: "أكثر من 2.5 هدف + BTTS", odds: "2.20", confidence: "high" },
                { label: "الرهان الآمن", value: "أكثر من 1.5 هدف", odds: "1.20", confidence: "high" },
                { label: "رهان القيمة", value: "تعادل + أكثر من 2.5", odds: "5.50", confidence: "low" }
            ],
            reason: "ديربي الرياض دائماً مثير. متوسط 3.5 أهداف في آخر 6 مواجهات. نيمار وميتروفيتش في فورم."
        },
        {
            league: "dutch",
            match: "آيندهوفن vs أياكس",
            isHot: true,
            tips: [
                { label: "الرهان المقترح", value: "فوز آيندهوفن + أكثر من 2.5", odds: "2.10", confidence: "high" },
                { label: "الرهان الآمن", value: "أكثر من 2.5 هدف", odds: "1.40", confidence: "high" },
                { label: "رهان القيمة", value: "آيندهوفن يسجل 3+", odds: "2.80", confidence: "medium" }
            ],
            reason: "آيندهوفن سجل 88 هدف في 34 مباراة. أياكس يعاني دفاعياً في المباريات الكبيرة."
        },
        {
            league: "spanish",
            match: "ريال مدريد vs أتلتيكو مدريد",
            isHot: true,
            tips: [
                { label: "الرهان المقترح", value: "أقل من 2.5 هدف", odds: "1.75", confidence: "high" },
                { label: "الرهان الآمن", value: "فوز ريال أو تعادل (1X)", odds: "1.25", confidence: "high" },
                { label: "رهان القيمة", value: "1-0 ريال مدريد", odds: "6.00", confidence: "low" }
            ],
            reason: "ديربي مدريد عادة مباراة تكتيكية. 6 من آخر 10 مباريات كانت أقل من 2.5 هدف."
        }
    ],

    news: [
        {
            title: "الأهلي يضم صفقة جديدة لتعزيز خط الوسط",
            content: "أعلن النادي الأهلي عن التعاقد مع لاعب وسط دولي لتعزيز صفوف الفريق في النصف الثاني من الموسم.",
            image: "⚽",
            date: "منذ ساعة",
            league: "egyptian",
            category: "انتقالات"
        },
        {
            title: "رونالدو يسجل هاتريك مع النصر في ديربي الرياض",
            content: "سجل كريستيانو رونالدو ثلاثة أهداف رائعة في فوز النصر على الهلال في ديربي العاصمة المثير.",
            image: "🌟",
            date: "منذ 3 ساعات",
            league: "saudi",
            category: "مباريات"
        },
        {
            title: "القوة الجوية يواصل تصدر الدوري العراقي بفوز كبير",
            content: "حقق القوة الجوية فوزاً كبيراً على الزوراء بثلاثة أهداف مقابل هدف واحد ليواصل تصدر جدول الترتيب.",
            image: "🏆",
            date: "منذ 5 ساعات",
            league: "iraqi",
            category: "مباريات"
        },
        {
            title: "ليفربول يتعادل مع السيتي في مباراة مثيرة",
            content: "انتهت قمة الدوري الإنجليزي بالتعادل 2-2 في مباراة مثيرة على ملعب أنفيلد شهدت أداءً رائعاً من الفريقين.",
            image: "🏴󠁧󠁢󠁥󠁮󠁧󠁿",
            date: "منذ 8 ساعات",
            league: "english",
            category: "مباريات"
        },
        {
            title: "آيندهوفن يحطم الرقم القياسي في عدد الأهداف",
            content: "سجل آيندهوفن 88 هدفاً هذا الموسم محطماً الرقم القياسي للدوري الهولندي في عدد الأهداف المسجلة.",
            image: "🇳🇱",
            date: "منذ يوم",
            league: "dutch",
            category: "أرقام"
        },
        {
            title: "الكلاسيكو: ريال مدريد يتفوق على برشلونة 3-2",
            content: "في مباراة درامية، تمكن ريال مدريد من الفوز على برشلونة بثلاثة أهداف مقابل اثنين في الكلاسيكو.",
            image: "🇪🇸",
            date: "منذ يوم",
            league: "spanish",
            category: "مباريات"
        }
    ],

    stats: {
        topScoringTeams: [
            { team: "مانشستر سيتي", flag: "🏴󠁧󠁢󠁥󠁮󠁧󠁿", goals: 90 },
            { team: "آيندهوفن", flag: "🇳🇱", goals: 88 },
            { team: "ليفربول", flag: "🏴󠁧󠁢󠁥󠁮󠁧󠁿", goals: 85 },
            { team: "ريال مدريد", flag: "🇪🇸", goals: 82 },
            { team: "إنتر ميلان", flag: "🇮🇹", goals: 82 }
        ],
        winStreaks: [
            { team: "ليفربول", flag: "🏴󠁧󠁢󠁥󠁮󠁧󠁿", streak: 12 },
            { team: "آيندهوفن", flag: "🇳🇱", streak: 10 },
            { team: "الأهلي", flag: "🇪🇬", streak: 9 },
            { team: "الهلال", flag: "🇸🇦", streak: 8 },
            { team: "ريال مدريد", flag: "🇪🇸", streak: 8 }
        ],
        bestDefense: [
            { team: "الأهلي", flag: "🇪🇬", conceded: 18 },
            { team: "الهلال", flag: "🇸🇦", conceded: 18 },
            { team: "الشرطة", flag: "🇮🇶", conceded: 20 },
            { team: "آيندهوفن", flag: "🇳🇱", conceded: 22 },
            { team: "أرسنال", flag: "🏴󠁧󠁢󠁥󠁮󠁧󠁿", conceded: 25 }
        ],
        btts: [
            { league: "الدوري الإنجليزي", flag: "🏴󠁧󠁢󠁥󠁮󠁧󠁿", percentage: 58 },
            { league: "الدوري الهولندي", flag: "🇳🇱", percentage: 62 },
            { league: "الدوري الإيطالي", flag: "🇮🇹", percentage: 52 },
            { league: "الدوري الإسباني", flag: "🇪🇸", percentage: 48 },
            { league: "الدوري العراقي", flag: "🇮🇶", percentage: 45 }
        ],
        overUnder: [
            { league: "الدوري الهولندي", flag: "🇳🇱", over: 68, under: 32 },
            { league: "الدوري الإنجليزي", flag: "🏴󠁧󠁢󠁥󠁮󠁧󠁿", over: 62, under: 38 },
            { league: "الدوري السعودي", flag: "🇸🇦", over: 55, under: 45 },
            { league: "الدوري الإسباني", flag: "🇪🇸", over: 52, under: 48 },
            { league: "الدوري المصري", flag: "🇪🇬", over: 50, under: 50 },
            { league: "الدوري الإيطالي", flag: "🇮🇹", over: 48, under: 52 },
            { league: "الدوري العراقي", flag: "🇮🇶", over: 45, under: 55 },
            { league: "تشامبيونز ليج", flag: "🏆", over: 60, under: 40 }
        ],
        teamForms: [
            { team: "ليفربول", flag: "🏴󠁧󠁢󠁥󠁮󠁧󠁿", form: ["W","W","W","D","W"], points: 13 },
            { team: "آيندهوفن", flag: "🇳🇱", form: ["W","W","W","D","W"], points: 13 },
            { team: "الأهلي", flag: "🇪🇬", form: ["W","W","D","W","W"], points: 13 },
            { team: "ريال مدريد", flag: "🇪🇸", form: ["W","W","D","W","W"], points: 13 },
            { team: "الهلال", flag: "🇸🇦", form: ["W","W","W","D","W"], points: 13 },
            { team: "القوة الجوية", flag: "🇮🇶", form: ["W","W","D","W","W"], points: 13 },
            { team: "إنتر ميلان", flag: "🇮🇹", form: ["W","W","W","D","W"], points: 13 }
        ]
    }
};
// ===== GoalMaster - Main Application =====

document.addEventListener('DOMContentLoaded', () => {
    // إخفاء شاشة التحميل
    setTimeout(() => {
        document.getElementById('loadingScreen').classList.add('hide');
    }, 1500);

    // تهيئة التطبيق
    initApp();
});

function initApp() {
    initNavigation();
    initThemeToggle();
    initDateNavigation();
    initLeagueFilter();
    initCounterAnimation();
    initScrollEffects();
    initBetCalculator();

    // تحميل البيانات
    loadMatches('all');
    loadPredictions();
    loadStandings('egyptian');
    loadBettingTips();
    loadStats();
    loadNews();
    loadLeagues();
    initTicker();
}

// ===== التنقل =====
function initNavigation() {
    const mobileMenu = document.getElementById('mobileMenu');
    const navLinks = document.getElementById('navLinks');

    mobileMenu.addEventListener('click', () => {
        navLinks.classList.toggle('active');
        const icon = mobileMenu.querySelector('i');
        icon.classList.toggle('fa-bars');
        icon.classList.toggle('fa-times');
    });

    // إغلاق القائمة عند النقر على رابط
    navLinks.querySelectorAll('a').forEach(link => {
        link.addEventListener('click', () => {
            navLinks.classList.remove('active');
            const icon = mobileMenu.querySelector('i');
            icon.classList.add('fa-bars');
            icon.classList.remove('fa-times');
        });
    });

    // تحديث الرابط النشط
    const sections = document.querySelectorAll('section[id]');
    window.addEventListener('scroll', () => {
        let current = '';
        sections.forEach(section => {
            const sectionTop = section.offsetTop - 100;
            if (pageYOffset >= sectionTop) {
                current = section.getAttribute('id');
            }
        });

        navLinks.querySelectorAll('a').forEach(link => {
            link.classList.remove('active');
            if (link.getAttribute('href') === '#' + current) {
                link.classList.add('active');
            }
        });
    });
}

// ===== تبديل السمة =====
function initThemeToggle() {
    const themeToggle = document.getElementById('themeToggle');
    const savedTheme = localStorage.getItem('theme') || 'dark';
    document.documentElement.setAttribute('data-theme', savedTheme);
    updateThemeIcon(savedTheme);

    themeToggle.addEventListener('click', () => {
        const currentTheme = document.documentElement.getAttribute('data-theme');
        const newTheme = currentTheme === 'dark' ? 'light' : 'dark';
        document.documentElement.setAttribute('data-theme', newTheme);
        localStorage.setItem('theme', newTheme);
        updateThemeIcon(newTheme);
    });
}

function updateThemeIcon(theme) {
    const icon = document.querySelector('#themeToggle i');
    icon.className = theme === 'dark' ? 'fas fa-sun' : 'fas fa-moon';
}

// ===== التنقل بين التواريخ =====
function initDateNavigation() {
    let currentDate = new Date();
    updateDateDisplay(currentDate);

    document.getElementById('prevDay').addEventListener('click', () => {
        currentDate.setDate(currentDate.getDate() - 1);
        updateDateDisplay(currentDate);
    });

    document.getElementById('nextDay').addEventListener('click', () => {
        currentDate.setDate(currentDate.getDate() + 1);
        updateDateDisplay(currentDate);
    });
}

function updateDateDisplay(date) {
    const options = { weekday: 'long', year: 'numeric', month: 'long', day: 'numeric' };
    document.getElementById('currentDate').textContent = date.toLocaleDateString('ar-EG', options);
}

// ===== فلتر الدوريات =====
function initLeagueFilter() {
    const filterBtns = document.querySelectorAll('.filter-btn');
    filterBtns.forEach(btn => {
        btn.addEventListener('click', () => {
            filterBtns.forEach(b => b.classList.remove('active'));
            btn.classList.add('active');
            const league = btn.dataset.league;
            loadMatches(league);
        });
    });
}

// ===== تحميل المباريات =====
function loadMatches(leagueFilter) {
    const grid = document.getElementById('matchesGrid');
    grid.innerHTML = '';

    let allMatches = [];

    Object.keys(LEAGUES_DATA).forEach(key => {
        if (leagueFilter === 'all' || key === leagueFilter) {
            const league = LEAGUES_DATA[key];
            league.matches.forEach(match => {
                allMatches.push({
                    ...match,
                    leagueKey: key,
                    leagueName: league.name,
                    leagueFlag: league.flag
                });
            });
        }
    });

    // ترتيب حسب التاريخ
    allMatches.sort((a, b) => new Date(b.date) - new Date(a.date));

    if (allMatches.length === 0) {
        grid.innerHTML = '<div class="no-data"><i class="fas fa-calendar-times"></i><p>لا توجد مباريات متاحة</p></div>';
        return;
    }

    allMatches.forEach((match, index) => {
        const card = createMatchCard(match, index);
        grid.appendChild(card);
    });
}

function createMatchCard(match, index) {
    const card = document.createElement('div');
    card.className = `match-card animate-in ${match.status === 'live' ? 'live' : ''}`;
    card.style.animationDelay = `${index * 0.1}s`;

    const statusClass = match.status === 'live' ? 'live' :
        match.status === 'finished' ? 'finished' : 'upcoming';
    const statusText = match.status === 'live' ? '🔴 مباشر' :
        match.status === 'finished' ? '✅ انتهت' : '⏰ لم تبدأ';

    const homeScore = match.homeScore !== null ? match.homeScore : '-';
    const awayScore = match.awayScore !== null ? match.awayScore : '-';

    // توليد أرقام odds عشوائية للعرض
    const homeOdd = (1.5 + Math.random() * 2).toFixed(2);
    const drawOdd = (2.5 + Math.random() * 2).toFixed(2);
    const awayOdd = (1.5 + Math.random() * 3).toFixed(2);

    card.innerHTML = `
        <div class="match-league">
            <span class="league-name">${match.leagueFlag} ${match.leagueName}</span>
            <span class="match-status ${statusClass}">${statusText}</span>
        </div>
        <div class="match-teams">
            <div class="team">
                <div class="team-logo">⚽</div>
                <div class="team-name">${match.home}</div>
            </div>
            <div class="match-score">
                <span>${homeScore}</span>
                <span class="separator">-</span>
                <span>${awayScore}</span>
            </div>
            <div class="team">
                <div class="team-logo">⚽</div>
                <div class="team-name">${match.away}</div>
            </div>
        </div>
        <div class="match-info">
            <div class="match-time">
                <i class="fas fa-clock"></i>
                <span>${match.time} | ${formatDate(match.date)}</span>
            </div>
            <div class="match-odds">
                <span class="odd-btn" title="فوز ${match.home}">1: ${homeOdd}</span>
                <span class="odd-btn" title="تعادل">X: ${drawOdd}</span>
                <span class="odd-btn" title="فوز ${match.away}">2: ${awayOdd}</span>
            </div>
        </div>
    `;

    return card;
}

// ===== تحميل التوقعات =====
function loadPredictions() {
    const grid = document.getElementById('predictionsGrid');
    grid.innerHTML = '';

    PREDICTIONS_DATA.predictions.forEach((pred, index) => {
        const card = document.createElement('div');
        card.className = 'prediction-card animate-in';
        card.style.animationDelay = `${index * 0.1}s`;

        const tipsHTML = pred.tips.map(tip => `
            <div class="prediction-tip">
                <span class="tip-label">${tip.label}</span>
                <span class="tip-value">${tip.value}</span>
            </div>
        `).join('');

        const leagueData = LEAGUES_DATA[pred.league];
        const leagueFlag = leagueData ? leagueData.flag : '⚽';

        card.innerHTML = `
            <div class="prediction-header">
                <div>
                    <span style="color: var(--text-muted); font-size: 0.8rem;">${leagueFlag} ${leagueData ? leagueData.name : ''}</span>
                    <div class="prediction-match">${pred.match}</div>
                </div>
                <span class="confidence ${pred.confidenceLevel}">
                    <i class="fas fa-chart-line"></i> ${pred.confidence}%
                </span>
            </div>
            <div class="prediction-details">
                <div class="prediction-tip" style="background: var(--primary); border-radius: 8px;">
                    <span class="tip-label" style="color: white; font-weight: 700;">🎯 التوقع</span>
                    <span class="tip-value" style="color: white; font-weight: 900;">${pred.prediction}</span>
                </div>
                <div class="prediction-tip">
                    <span class="tip-label">💰 Odds</span>
                    <span class="tip-value">${pred.odds}</span>
                </div>
                ${tipsHTML}
            </div>
            <div class="prediction-bar">
                <div class="prediction-bar-fill" style="width: ${pred.confidence}%"></div>
            </div>
            <div class="prediction-analysis">
                📊 <strong>التحليل:</strong> ${pred.analysis}
            </div>
        `;

        grid.appendChild(card);
    });
}

// ===== تحميل الترتيب =====
function loadStandings(leagueKey) {
    const tbody = document.getElementById('standingsBody');
    tbody.innerHTML = '';

    const league = LEAGUES_DATA[leagueKey];
    if (!league) return;

    league.standings.forEach((team, index) => {
        const tr = document.createElement('tr');

        // تحديد المنطقة (أبطال أو هبوط)
        if (index < 4) tr.classList.add('champion');
        if (index >= league.standings.length - 3) tr.classList.add('relegation');

        const formHTML = team.form.map(f => {
            const cls = f === 'W' ? 'w' : f === 'D' ? 'd' : 'l';
            const label = f === 'W' ? 'ف' : f === 'D' ? 'ت' : 'خ';
            return `<span class="form-badge ${cls}">${label}</span>`;
        }).join('');

        tr.innerHTML = `
            <td><strong>${team.pos}</strong></td>
            <td>
                <div class="standings-team">
                    <span class="team-crest">${team.crest}</span>
                    <span>${team.team}</span>
                </div>
            </td>
            <td>${team.p}</td>
            <td>${team.w}</td>
            <td>${team.d}</td>
            <td>${team.l}</td>
            <td>${team.gf}</td>
            <td>${team.ga}</td>
            <td>${team.gd > 0 ? '+' : ''}${team.gd}</td>
            <td class="points">${team.pts}</td>
            <td><div class="form-badges">${formHTML}</div></td>
        `;

        tbody.appendChild(tr);
    });
}

// تغيير دوري الترتيب
document.getElementById('standingsLeague').addEventListener('change', (e) => {
    loadStandings(e.target.value);
});

// ===== تحميل نصائح المراهنات =====
function loadBettingTips() {
    const container = document.getElementById('bettingCards');
    container.innerHTML = '';

    PREDICTIONS_DATA.bettingTips.forEach((tip, index) => {
        const card = document.createElement('div');
        card.className = 'bet-card animate-in';
        card.style.animationDelay = `${index * 0.1}s`;

        const leagueData = LEAGUES_DATA[tip.league];
        const tipsHTML = tip.tips.map(t => `
            <div class="bet-type">
                <span class="bet-label">${t.label}</span>
                <span class="bet-value ${t.confidence}">${t.value} (${t.odds})</span>
            </div>
        `).join('');

        card.innerHTML = `
            ${tip.isHot ? '<span class="hot-badge">🔥 HOT</span>' : ''}
            <div style="color: var(--text-muted); font-size: 0.8rem; margin-bottom: 5px;">
                ${leagueData ? leagueData.flag : '⚽'} ${leagueData ? leagueData.name : ''}
            </div>
            <div class="bet-match">${tip.match}</div>
            ${tipsHTML}
            <div class="bet-reason">
                💡 ${tip.reason}
            </div>
        `;

        container.appendChild(card);
    });
}

// ===== تحميل الإحصائيات =====
function loadStats() {
    // أكثر الفرق تسجيلاً
    const topScorers = document.getElementById('topScorersTeams');
    topScorers.innerHTML = PREDICTIONS_DATA.stats.topScoringTeams.map(t => `
        <div class="stat-item">
            <span>${t.flag} ${t.team}</span>
            <span class="value">${t.goals} هدف</span>
        </div>
    `).join('');

    // أطول سلسلة انتصارات
    const winStreaks = document.getElementById('winStreaks');
    winStreaks.innerHTML = PREDICTIONS_DATA.stats.winStreaks.map(t => `
        <div class="stat-item">
            <span>${t.flag} ${t.team}</span>
            <span class="value">${t.streak} مباراة</span>
        </div>
    `).join('');

    // أقوى دفاع
    const bestDefense = document.getElementById('bestDefense');
    bestDefense.innerHTML = PREDICTIONS_DATA.stats.bestDefense.map(t => `
        <div class="stat-item">
            <span>${t.flag} ${t.team}</span>
            <span class="value">${t.conceded} هدف</span>
        </div>
    `).join('');

    // BTTS
    const btts = document.getElementById('bttsStats');
    btts.innerHTML = PREDICTIONS_DATA.stats.btts.map(t => `
        <div class="stat-item">
            <span>${t.flag} ${t.league}</span>
            <span class="value">${t.percentage}%</span>
        </div>
    `).join('');

    // Over/Under Chart
    const overUnder = document.getElementById('overUnderChart');
    overUnder.innerHTML = PREDICTIONS_DATA.stats.overUnder.map(t => `
        <div class="chart-bar">
            <span class="label">${t.flag} ${t.league}</span>
            <div class="bar">
                <div class="bar-fill over" style="width: ${t.over}%">${t.over}%</div>
            </div>
        </div>
    `).join('');

    // فورم الفرق
    const teamForms = document.getElementById('teamForms');
    teamForms.innerHTML = PREDICTIONS_DATA.stats.teamForms.map(t => {
        const formHTML = t.form.map(f => {
            const cls = f === 'W' ? 'w' : f === 'D' ? 'd' : 'l';
            const label = f === 'W' ? 'ف' : f === 'D' ? 'ت' : 'خ';
            return `<span class="form-badge ${cls}">${label}</span>`;
        }).join('');

        return `
            <div class="stat-item">
                <span>${t.flag} ${t.team}</span>
                <div class="form-badges">${formHTML}</div>
                <span class="value">${t.points} نقطة</span>
            </div>
        `;
    }).join('');

    // تأثير الرسوم المتحركة
    setTimeout(() => {
        document.querySelectorAll('.bar-fill').forEach(bar => {
            const width = bar.style.width;
            bar.style.width = '0%';
            setTimeout(() => { bar.style.width = width; }, 100);
        });
    }, 500);
}

// ===== تحميل الأخبار =====
function loadNews() {
    const grid = document.getElementById('newsGrid');
    grid.innerHTML = '';

    PREDICTIONS_DATA.news.forEach((news, index) => {
        const card = document.createElement('div');
        card.className = 'news-card animate-in';
        card.style.animationDelay = `${index * 0.1}s`;

        card.innerHTML = `
            <div class="news-image">${news.image}</div>
            <div class="news-content">
                <h3>${news.title}</h3>
                <p>${news.content}</p>
                <div class="news-meta">
                    <span><i class="fas fa-clock"></i> ${news.date}</span>
                    <span class="badge">${news.category}</span>
                </div>
            </div>
        `;

        grid.appendChild(card);
    });
}

// ===== تحميل الدوريات =====
function loadLeagues() {
    const showcase = document.getElementById('leaguesShowcase');
    showcase.innerHTML = '';

    Object.keys(LEAGUES_DATA).forEach((key, index) => {
        const league = LEAGUES_DATA[key];
        const card = document.createElement('div');
        card.className = 'league-card animate-in';
        card.style.animationDelay = `${index * 0.1}s`;

        const totalMatches = league.standings.reduce((sum, t) => sum + t.p, 0) / 2;
        const totalGoals = league.standings.reduce((sum, t) => sum + t.gf, 0);

        card.innerHTML = `
            <div class="league-flag">${league.flag}</div>
            <h3>${league.name}</h3>
            <div class="league-country">${league.country} | ${league.season}</div>
            <div class="league-info-grid">
                <div class="league-info-item">
                    <span class="num">${league.teams}</span>
                    <span class="lbl">فريق</span>
                </div>
                <div class="league-info-item">
                    <span class="num">${totalMatches}</span>
                    <span class="lbl">مباراة</span>
                </div>
                <div class="league-info-item">
                    <span class="num">${totalGoals}</span>
                    <span class="lbl">هدف</span>
                </div>
                <div class="league-info-item">
                    <span class="num">${(totalGoals / totalMatches).toFixed(1)}</span>
                    <span class="lbl">معدل الأهداف</span>
                </div>
            </div>
        `;

        card.addEventListener('click', () => {
            document.getElementById('standingsLeague').value = key;
            loadStandings(key);
            document.getElementById('standings').scrollIntoView({ behavior: 'smooth' });
        });

        showcase.appendChild(card);
    });
}

// ===== شريط الأخبار المتحرك =====
function initTicker() {
    const ticker = document.getElementById('ticker-text');
    const tickerMessages = [
        "⚽ الأهلي 2-1 الزمالك | ليفربول 2-2 مانشستر سيتي | ريال مدريد 3-2 برشلونة",
        "🏆 القوة الجوية تتصدر الدوري العراقي | آيندهوفن يحطم الأرقام في هولندا",
        "💰 نسبة نجاح التوقعات هذا الأسبوع: 87% | أفضل رهان اليوم: Over 2.5 في ديربي الرياض",
        "📊 رونالدو يسجل هاتريك | صلاح هداف البريميرليغ | بيلينغهام أفضل لاعب في لا ليغا",
        "🔥 ديربيات مرتقبة: الأهلي vs الزمالك | القوة الجوية vs الشرطة | الهلال vs النصر"
    ];

    let messageIndex = 0;
    setInterval(() => {
        messageIndex = (messageIndex + 1) % tickerMessages.length;
        ticker.textContent = tickerMessages[messageIndex];
    }, 5000);
}

// ===== حاسبة المراهنات =====
function initBetCalculator() {
    document.getElementById('calcBet').addEventListener('click', () => {
        const amount = parseFloat(document.getElementById('betAmount').value) || 0;
        const odds = parseFloat(document.getElementById('betOdds').value) || 0;

        const total = amount * odds;
        const profit = total - amount;

        document.getElementById('betProfit').textContent = profit.toFixed(2);
        document.getElementById('betTotal').textContent = total.toFixed(2);

        // تأثير بصري
        document.getElementById('betProfit').style.transform = 'scale(1.2)';
        document.getElementById('betTotal').style.transform = 'scale(1.2)';
        setTimeout(() => {
            document.getElementById('betProfit').style.transform = 'scale(1)';
            document.getElementById('betTotal').style.transform = 'scale(1)';
        }, 300);
    });

    // حساب تلقائي عند الكتابة
    ['betAmount', 'betOdds'].forEach(id => {
        document.getElementById(id).addEventListener('input', () => {
            document.getElementById('calcBet').click();
        });
    });
}

// ===== عداد الأرقام =====
function initCounterAnimation() {
    const observer = new IntersectionObserver((entries) => {
        entries.forEach(entry => {
            if (entry.isIntersecting) {
                const counters = entry.target.querySelectorAll('.stat-number');
                counters.forEach(counter => {
                    const target = parseInt(counter.dataset.target);
                    animateCounter(counter, target);
                });
                observer.unobserve(entry.target);
            }
        });
    }, { threshold: 0.5 });

    const heroStats = document.querySelector('.hero-stats');
    if (heroStats) observer.observe(heroStats);
}

function animateCounter(element, target) {
    let current = 0;
    const increment = target / 80;
    const timer = setInterval(() => {
        current += increment;
        if (current >= target) {
            element.textContent = target.toLocaleString();
            clearInterval(timer);
        } else {
            element.textContent = Math.floor(current).toLocaleString();
        }
    }, 20);
}

// ===== تأثيرات التمرير =====
function initScrollEffects() {
    const backToTop = document.getElementById('backToTop');
    const navbar = document.querySelector('.navbar');

    window.addEventListener('scroll', () => {
        // زر العودة للأعلى
        if (window.scrollY > 500) {
            backToTop.classList.add('show');
        } else {
            backToTop.classList.remove('show');
        }

        // تأثير الـ navbar
        if (window.scrollY > 50) {
            navbar.classList.add('scrolled');
        } else {
            navbar.classList.remove('scrolled');
        }
    });

    backToTop.addEventListener('click', () => {
        window.scrollTo({ top: 0, behavior: 'smooth' });
    });

    // رسوم متحركة عند الظهور
    const observerOptions = {
        threshold: 0.1,
        rootMargin: '0px 0px -50px 0px'
    };

    const animObserver = new IntersectionObserver((entries) => {
        entries.forEach(entry => {
            if (entry.isIntersecting) {
                entry.target.classList.add('animate-in');
                animObserver.unobserve(entry.target);
            }
        });
    }, observerOptions);

    document.querySelectorAll('.stat-card, .league-card, .news-card').forEach(card => {
        animObserver.observe(card);
    });
}

// ===== دوال مساعدة =====
function formatDate(dateStr) {
    const date = new Date(dateStr);
    const options = { month: 'short', day: 'numeric' };
    return date.toLocaleDateString('ar-EG', options);
}

// ===== تحديث تلقائي كل 30 ثانية =====
setInterval(() => {
    // محاكاة تحديث المباريات المباشرة
    const liveMatches = document.querySelectorAll('.match-card.live');
    liveMatches.forEach(card => {
        // يمكن إضافة تحديثات فعلية هنا عند ربط API
    });
}, 30000);

// ===== Service Worker للعمل بدون إنترنت =====
if ('serviceWorker' in navigator) {
    window.addEventListener('load', () => {
        // يمكن تسجيل Service Worker هنا
    });
}

console.log('⚽ GoalMaster Analytics - Loaded Successfully!');
console.log('🏆 8 Leagues | 🎯 AI Predictions | 💰 Betting Tips');
// ===== نظام التوقعات الذكي =====

class PredictionEngine {
    constructor() {
        this.weights = {
            formWeight: 0.30,
            headToHeadWeight: 0.20,
            homeAdvantage: 0.15,
            goalStats: 0.15,
            squadStrength: 0.10,
            injuries: 0.10
        };
    }

    // حساب احتمالية الفوز
    calculateWinProbability(homeTeam, awayTeam, league) {
        const leagueData = LEAGUES_DATA[league];
        if (!leagueData) return null;

        const home = leagueData.standings.find(t => t.team === homeTeam);
        const away = leagueData.standings.find(t => t.team === awayTeam);

        if (!home || !away) return null;

        // حساب قوة الفريق
        const homeStrength = this.calculateTeamStrength(home);
        const awayStrength = this.calculateTeamStrength(away);

        // ميزة الأرض
        const homeAdvantage = 1.15;

        // الاحتمالات
        const totalStrength = (homeStrength * homeAdvantage) + awayStrength;
        const homeWinProb = ((homeStrength * homeAdvantage) / totalStrength * 100).toFixed(1);
        const awayWinProb = (awayStrength / totalStrength * 100).toFixed(1);
        const drawProb = (100 - homeWinProb - awayWinProb).toFixed(1);

        return {
            homeWin: parseFloat(homeWinProb),
            draw: Math.max(15, parseFloat(drawProb)),
            awayWin: parseFloat(awayWinProb),
            homeStrength,
            awayStrength,
            suggestedBet: this.getSuggestedBet(homeWinProb, drawProb, awayWinProb),
            overUnder: this.predictOverUnder(home, away),
            btts: this.predictBTTS(home, away)
        };
    }

    // قوة الفريق
    calculateTeamStrength(team) {
        const winRate = team.w / team.p;
        const goalRate = team.gf / team.p;
        const defenseRate = 1 - (team.ga / team.p / 3);
        const formPoints = this.calculateFormPoints(team.form);

        return (winRate * 0.35) + (goalRate * 0.15) + (defenseRate * 0.20) + (formPoints * 0.30);
    }

    // نقاط الفورم
    calculateFormPoints(form) {
        let points = 0;
        const weights = [1.5, 1.3, 1.1, 0.9, 0.7]; // الأحدث أهم

        form.forEach((result, index) => {
            if (result === 'W') points += 3 * weights[index];
            else if (result === 'D') points += 1 * weights[index];
        });

        return points / (15 * weights.reduce((a, b) => a + b, 0));
    }

    // توقع Over/Under
    predictOverUnder(home, away) {
        const avgGoals = (home.gf / home.p + away.gf / away.p + home.ga / home.p + away.ga / away.p) / 2;

        return {
            expectedGoals: avgGoals.toFixed(1),
            over25: avgGoals > 2.5 ? 'مرجح' : 'غير مرجح',
            over25Prob: Math.min(85, Math.max(25, (avgGoals / 3.5 * 100))).toFixed(0)
        };
    }

    // توقع BTTS
    predictBTTS(home, away) {
        const homeScoringRate = home.gf / home.p;
        const awayScoringRate = away.gf / away.p;
        const homeConcedeRate = home.ga / home.p;
        const awayConcedeRate = away.ga / away.p;

        const bttsProb = ((homeScoringRate * awayConcedeRate + awayScoringRate * homeConcedeRate) / 2 * 50).toFixed(0);

        return {
            probability: Math.min(80, Math.max(20, parseInt(bttsProb))),
            suggestion: parseInt(bttsProb) > 50 ? 'نعم' : 'لا'
        };
    }

    // الرهان المقترح
    getSuggestedBet(homeProb, drawProb, awayProb) {
        const maxProb = Math.max(homeProb, drawProb, awayProb);

        if (maxProb === parseFloat(homeProb)) return 'فوز الأول (1)';
        if (maxProb === parseFloat(awayProb)) return 'فوز الثاني (2)';
        return 'تعادل (X)';
    }

    // توليد تقرير كامل
    generateReport(homeTeam, awayTeam, league) {
        const prediction = this.calculateWinProbability(homeTeam, awayTeam, league);
        if (!prediction) return null;

        return {
            match: `${homeTeam} vs ${awayTeam}`,
            league: LEAGUES_DATA[league]?.name || league,
            probabilities: {
                homeWin: prediction.homeWin + '%',
                draw: prediction.draw + '%',
                awayWin: prediction.awayWin + '%'
            },
            suggestedBet: prediction.suggestedBet,
            overUnder: prediction.overUnder,
            btts: prediction.btts,
            confidence: this.getConfidenceLevel(prediction),
            odds: this.calculateOdds(prediction)
        };
    }

    // مستوى الثقة
    getConfidenceLevel(prediction) {
        const maxProb = Math.max(prediction.homeWin, prediction.draw, prediction.awayWin);

        if (maxProb > 65) return { level: 'high', text: 'عالي', color: 'green' };
        if (maxProb > 45) return { level: 'medium', text: 'متوسط', color: 'yellow' };
        return { level: 'low', text: 'منخفض', color: 'red' };
    }

    // حساب الأودز
    calculateOdds(prediction) {
        return {
            homeOdds: (100 / prediction.homeWin).toFixed(2),
            drawOdds: (100 / prediction.draw).toFixed(2),
            awayOdds: (100 / prediction.awayWin).toFixed(2)
        };
    }
}

// إنشاء محرك التوقعات
const predictionEngine = new PredictionEngine();

// دالة لتوليد تقارير سريعة
function quickPredict(home, away, league) {
    const report = predictionEngine.generateReport(home, away, league);
    if (report) {
        console.log('📊 تقرير التوقعات:');
        console.log(`⚽ ${report.match}`);
        console.log(`🏆 ${report.league}`);
        console.log(`📈 احتمالات: ${report.probabilities.homeWin} / ${report.probabilities.draw} / ${report.probabilities.awayWin}`);
        console.log(`🎯 الرهان المقترح: ${report.suggestedBet}`);
        console.log(`⚡ أهداف متوقعة: ${report.overUnder.expectedGoals}`);
        console.log(`✅ BTTS: ${report.btts.suggestion} (${report.btts.probability}%)`);
        console.log(`💪 مستوى الثقة: ${report.confidence.text}`);
    }
    return report;
}

// أمثلة
// quickPredict('الأهلي', 'الزمالك', 'egyptian');
// quickPredict('ليفربول', 'مانشستر سيتي', 'english');
// quickPredict('القوة الجوية', 'الشرطة', 'iraqi');
const express = require('express');
const cors = require('cors');
const path = require('path');

const app = express();
const PORT = process.env.PORT || 3000;

// Middleware
app.use(cors());
app.use(express.json());
app.use(express.static(path.join(__dirname, '..')));

// البيانات
const LEAGUES_DATA = require('../js/leagues.js');

// ===== API Routes =====

// الصفحة الرئيسية
app.get('/', (req, res) => {
    res.sendFile(path.join(__dirname, '..', 'index.html'));
});

// API - جميع الدوريات
app.get('/api/leagues', (req, res) => {
    const leagues = Object.keys(LEAGUES_DATA).map(key => ({
        id: key,
        name: LEAGUES_DATA[key].name,
        country: LEAGUES_DATA[key].country,
        flag: LEAGUES_DATA[key].flag,
        teams: LEAGUES_DATA[key].teams,
        season: LEAGUES_DATA[key].season
    }));
    res.json({ success: true, data: leagues });
});

// API - دوري محدد
app.get('/api/leagues/:id', (req, res) => {
    const league = LEAGUES_DATA[req.params.id];
    if (!league) {
        return res.status(404).json({ success: false, error: 'الدوري غير موجود' });
    }
    res.json({ success: true, data: league });
});

// API - ترتيب دوري محدد
app.get('/api/standings/:league', (req, res) => {
    const league = LEAGUES_DATA[req.params.league];
    if (!league) {
        return res.status(404).json({ success: false, error: 'الدوري غير موجود' });
    }
    res.json({ success: true, data: league.standings });
});

// API - مباريات دوري محدد
app.get('/api/matches/:league', (req, res) => {
    const league = LEAGUES_DATA[req.params.league];
    if (!league) {
        return res.status(404).json({ success: false, error: 'الدوري غير موجود' });
    }
    res.json({ success: true, data: league.matches });
});

// API - جميع المباريات
app.get('/api/matches', (req, res) => {
    let allMatches = [];
    Object.keys(LEAGUES_DATA).forEach(key => {
        const league = LEAGUES_DATA[key];
        league.matches.forEach(match => {
            allMatches.push({
                ...match,
                leagueId: key,
                leagueName: league.name,
                leagueFlag: league.flag
            });
        });
    });

    // فلتر حسب التاريخ
    if (req.query.date) {
        allMatches = allMatches.filter(m => m.date === req.query.date);
    }

    // فلتر حسب الحالة
    if (req.query.status) {
        allMatches = allMatches.filter(m => m.status === req.query.status);
    }

    allMatches.sort((a, b) => new Date(b.date) - new Date(a.date));
    res.json({ success: true, data: allMatches, total: allMatches.length });
});

// API - التوقعات
app.get('/api/predictions', (req, res) => {
    res.json({
        success: true,
        data: {
            message: "التوقعات متاحة في الواجهة الأمامية",
            totalPredictions: 8,
            accuracy: "87%"
        }
    });
});

// API - البحث
app.get('/api/search', (req, res) => {
    const query = (req.query.q || '').toLowerCase();
    if (!query) {
        return res.json({ success: true, data: [] });
    }

    let results = [];
    Object.keys(LEAGUES_DATA).forEach(key => {
        const league = LEAGUES_DATA[key];

        // بحث في الفرق
        league.standings.forEach(team => {
            if (team.team.toLowerCase().includes(query)) {
                results.push({
                    type: 'team',
                    name: team.team,
                    league: league.name,
                    leagueId: key,
                    position: team.pos,
                    points: team.pts
                });
            }
        });

        // بحث في الدوريات
        if (league.name.toLowerCase().includes(query) || league.country.toLowerCase().includes(query)) {
            results.push({
                type: 'league',
                name: league.name,
                country: league.country,
                id: key
            });
        }
    });

    res.json({ success: true, data: results, total: results.length });
});

// API - إحصائيات عامة
app.get('/api/stats', (req, res) => {
    let totalTeams = 0;
    let totalGoals = 0;
    let totalMatches = 0;

    Object.values(LEAGUES_DATA).forEach(league => {
        totalTeams += league.standings.length;
        league.standings.forEach(team => {
            totalGoals += team.gf;
        });
        totalMatches += league.matches.length;
    });

    res.json({
        success: true,
        data: {
            totalLeagues: Object.keys(LEAGUES_DATA).length,
            totalTeams,
            totalGoals,
            totalMatches,
            avgGoalsPerMatch: (totalGoals / (totalMatches || 1)).toFixed(1),
            lastUpdate: new Date().toISOString()
        }
    });
});

// 404
app.use((req, res) => {
    res.status(404).json({
        success: false,
        error: 'الصفحة غير موجودة',
        availableEndpoints: [
            'GET /api/leagues',
            'GET /api/leagues/:id',
            'GET /api/standings/:league',
            'GET /api/matches',
            'GET /api/matches/:league',
            'GET /api/predictions',
            'GET /api/search?q=query',
            'GET /api/stats'
        ]
    });
});

// تشغيل السيرفر
app.listen(PORT, () => {
    console.log(`
    ⚽ ================================== ⚽
    🏆 GoalMaster Analytics Server
    🌐 Running on: http://localhost:${PORT}
    📊 API: http://localhost:${PORT}/api
    ⚽ ================================== ⚽

    Available Leagues:
    🇪🇬 Egyptian Premier League
    🇮🇶 Iraqi Stars League
    🇸🇦 Saudi Pro League (Roshn)
    🏴󠁧󠁢󠁥󠁮󠁧󠁿 English Premier League
    🇪🇸 Spanish La Liga
    🇮🇹 Italian Serie A
    🏆 UEFA Champions League
    🇳🇱 Dutch Eredivisie
    `);
});

module.exports = app;
{
    "name": "goalmaster-analytics",
    "version": "2.0.0",
    "description": "GoalMaster - Football Analytics & Betting Platform",
    "main": "api/server.js",
    "scripts": {
        "start": "node api/server.js",
        "dev": "nodemon api/server.js"
    },
    "dependencies": {
        "express": "^4.18.2",
        "cors": "^2.8.5"
    },
    "devDependencies": {
        "nodemon": "^3.0.2"
    },
    "keywords": [
        "football",
        "analytics",
        "betting",
        "sports"
    ],
    "author": "GoalMaster Team",
    "license": "MIT"
}
# 1. انسخ جميع الملفات في مجلد football-analytics

# 2. ثبت المكتبات
cd football-analytics
npm install

# 3. شغّل السيرفر
npm start

# 4. افتح المتصفح
# http://localhost:3000
