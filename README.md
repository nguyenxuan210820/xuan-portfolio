<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Frontend Developer Portfolio</title>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: "Poppins", sans-serif;
}

body {
    background: linear-gradient(120deg, #0f172a, #1e293b, #020617);
    color: #fff;
    min-height: 100vh;
}

/* ===== HEADER ===== */
header {
    position: fixed;
    top: 0;
    width: 100%;
    padding: 20px 80px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    z-index: 100;
}

.logo {
    font-size: 20px;
    font-weight: 600;
}

.navmenu {
    display: flex;
    gap: 30px;
}

.navmenu a {
    color: #fff;
    text-decoration: none;
    font-size: 14px;
    transition: 0.3s;
}

.navmenu a:hover {
    color: #38bdf8;
}

/* ===== HERO ===== */
.hero {
    height: 100vh;
    display: grid;
    grid-template-columns: 1fr 1fr;
    align-items: center;
    padding: 120px 80px;
}

/* LEFT */
.hero-text h1 {
    font-size: 48px;
    line-height: 1.2;
}

.hero-text h1 span {
    color: #38bdf8;
}

.hero-text p {
    margin: 20px 0;
    font-size: 15px;
    color: #cbd5f5;
}

.tags {
    display: flex;
    gap: 10px;
    margin-bottom: 25px;
}

.tags span {
    background: rgba(255,255,255,0.1);
    padding: 6px 14px;
    border-radius: 20px;
    font-size: 12px;
}

/* BUTTON */
.buttons {
    display: flex;
    gap: 15px;
}

.btn {
    padding: 12px 22px;
    border-radius: 30px;
    border: 1px solid #38bdf8;
    color: #38bdf8;
    text-decoration: none;
    font-size: 14px;
    transition: 0.3s;
}

.btn.primary {
    background: #38bdf8;
    color: #020617;
}

.btn:hover {
    transform: translateY(-3px);
}

/* RIGHT IMAGE */
.hero-img img {
    width: 100%;
    max-width: 450px;
    animation: float 4s ease-in-out infinite;
}

@keyframes float {
    0% { transform: translateY(0); }
    50% { transform: translateY(-15px); }
    100% { transform: translateY(0); }
}

/* SOCIAL */
.social {
    position: fixed;
    left: 30px;
    top: 50%;
    transform: translateY(-50%);
}

.social a {
    display: block;
    margin: 15px 0;
    color: #fff;
    font-size: 20px;
    transition: 0.3s;
}

.social a:hover {
    color: #38bdf8;
}
.about {
    padding: 100px 80px;
    text-align: center;
}

.about h2 {
    font-size: 36px;
    margin-bottom: 20px;
}

.about-text {
    max-width: 600px;
    margin: auto;
    color: #cbd5f5;
    margin-bottom: 30px;
}

.about-info {
    display: flex;
    justify-content: center;
    gap: 30px;
    font-size: 14px;
}

/* RESPONSIVE */
@media (max-width: 900px) {
    header {
        padding: 20px 40px;
    }

    .hero {
        grid-template-columns: 1fr;
        text-align: center;
        padding: 120px 40px;
    }

    .hero-img {
        margin-top: 40px;
    }

    .social {
        display: none;
    }
}
/* ===== SKILLS SECTION ===== */
.skills {
    padding: 100px 80px;
    background: #020617;
}

.skills h2 {
    text-align: center;
    font-size: 36px;
    margin-bottom: 10px;
}

.skills p {
    text-align: center;
    color: #cbd5f5;
    margin-bottom: 50px;
}

.skill-box {
    max-width: 700px;
    margin: auto;
}

.skill {
    margin-bottom: 30px;
}

.skill-title {
    display: flex;
    justify-content: space-between;
    margin-bottom: 8px;
    font-size: 14px;
}

.bar {
    width: 100%;
    height: 10px;
    background: #1e293b;
    border-radius: 10px;
    overflow: hidden;
}

.bar span {
    display: block;
    height: 100%;
    background: linear-gradient(90deg, #38bdf8, #0ea5e9);
    border-radius: 10px;
    animation: load 2s ease;
}
.about {
    padding: 100px 80px;
    text-align: center;
}

.about h2 {
    font-size: 36px;
    margin-bottom: 20px;
}

.about-text {
    max-width: 600px;
    margin: auto;
    color: #cbd5f5;
    margin-bottom: 30px;
}

.about-info {
    display: flex;
    justify-content: center;
    gap: 30px;
    font-size: 14px;
}
.contact {
    padding: 100px 80px;
    text-align: center;
    background: #020617;
}

.contact h2 {
    font-size: 36px;
    margin-bottom: 10px;
}

.contact p {
    color: #cbd5f5;
    margin-bottom: 30px;
}

.contact-box div {
    margin: 10px 0;
    font-size: 14px;
}
.projects {
    padding: 100px 80px;
    background: #020617;
}

.projects h2 {
    text-align: center;
    font-size: 36px;
    margin-bottom: 10px;
}

.projects p {
    text-align: center;
    color: #cbd5f5;
    margin-bottom: 50px;
}

.project-list {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
    gap: 30px;
}

.project-card {
    background: #0f172a;
    padding: 25px;
    border-radius: 16px;
    transition: 0.3s;
}

.project-card:hover {
    transform: translateY(-10px);
    box-shadow: 0 10px 30px rgba(56,189,248,0.2);
}

.project-card h3 {
    margin-bottom: 10px;
}

.project-card p {
    font-size: 14px;
    color: #cbd5f5;
    margin-bottom: 15px;
}

.project-card span {
    font-size: 12px;
    color: #38bdf8;
}

.project-links {
    margin-top: 15px;
    display: flex;
    gap: 15px;
}

.project-links a {
    font-size: 13px;
    color: #38bdf8;
    text-decoration: none;
    border: 1px solid #38bdf8;
    padding: 6px 12px;
    border-radius: 20px;
    transition: 0.3s;
}

.project-links a:hover {
    background: #38bdf8;
    color: #020617;
}


/* % kỹ năng */
.html { width: 95%; }
.css { width: 90%; }
.js { width: 80%; }
.react { width: 70%; }

@keyframes load {
    from { width: 0; }
}

</style>
</head>
<body>

<header>
    <div class="logo">MyPortfolio</div>
    <nav class="navmenu">
        <a href="#">Home</a>
        <a href="#">About</a>
       <a href="#skills">Skills</a>
       <a href="#">Projects</a>
        <a href="#">Contact</a>
    </nav>
</header>
<section class="projects" id="projects">
    <h2>My Projects</h2>
    <p>Some projects I have built</p>

    <div class="project-list">

        <div class="project-card">
            <h3>Website Mofix</h3>
            <p>
                Xem phim chiếu rạp  
                 VÀO HÀNG TUẦN
            </p>
            <span>HTML • CSS • JavaScript</span>
           <div class="image-box">
          <img src="https://cdnv2.tgdd.vn/bhx-static/bhx/News/Images/2025/07/24/1580687/image6_202507241009569077.jpg" alt="">
          </div>

                <a href="#">GitHub</a>
            </div>
        </div>
        <span>HTML • CSS • JavaScript</span>
        <div class="project-card">'
            <h3>web THƯ VIỆN</h3>
            <p>
             Đọc sách hay mỗi ngày
            </p>
            <span>HTML • CSS • Flexbox</span>
           <div class="image-box">
          <img src="https://bizweb.dktcdn.net/100/363/455/files/trang-web-5-fd803972-12df-4c9d-99de-7b47cc8d8476.png?v=1697544686564" alt="">
          </div>

                <a href="#">GitHub</a>
            </div>
        </div>

        <div class="project-card">
            <h3>Web NHẠC HAY MỖI NGÀY</h3>
            <p>
                Mỗi ngày nghe một bản nhạc
                sẽ giúp bạn yêu đời hơn
            </p>
            <span>JavaScript • DOM</span>
           <div class="image-box">
          <img src="https://cafebiz.cafebizcdn.vn/thumb_w/600/162123310254002176/2022/5/15/photo1652579770433-1652579770522681630303.jpg" alt="">
          </div>
                <a href="#">GitHub</a>
            </div>
        </div>

    </div>
</section>
<section class="hero">
    <section class="about" id="about">
    <h2>About Me</h2>
    <p class="about-text">
       Tôi là một lập trình viên frontend tôi thích thiết kế các web giao diện cho người dùng. Tôi tốt nghiệp trường Cao Đẳng Sư Phạm Tây ninh
       Tôi đã có kinh nghiêm làm việc ở ngoài và có khoảng thơi gian thực tập 6 tháng tại trường trung học cơ sở trà Vong
    </p>

    <div class="about-info">
        <div><strong>Name:</strong> Nguyễn Thị Xuân</div>
        <div><strong>Role:</strong> Frontend Developer</div>
        <div><strong>Email:</strong> xuannguyen210820d@gmail.com</div>
    </div>
</section>

    <div class="hero-text">
        <h1>Frontend <span>Developer</span></h1>
        <p>
           Mục tiêu của tôi muốn trở thành kỹ sư IT  
           mong muốn được góp phần công sức của mình cho công ty 
           và có cơ hội làm việc vơi mọi người
        </p>

        <div class="tags">
            <span>HTML</span>
            <span>CSS</span>
            <span>JavaScript</span>
            <span>React</span>
        </div>

        <div class="buttons">
            <a href="#" class="btn primary">Projects</a>
            <a href="#" class="btn">Contact</a>
        </div>
    </div>

    <div class="hero-img">
        <!-- ẢNH MINH HỌA -->
        <img src="https://i.pinimg.com/originals/97/35/82/973582d9b0e0761a1b880edb78b7f4e7.gif" alt="developer">
    </div>
    <section class="skills" id="skills">
    <h2>My Skills</h2>
    <p>Technologies I work with</p>

    <div class="skill-box">

        <div class="skill">
            <div class="skill-title">
                <span>HTML</span>
                <span>95%</span>
            </div>
            <div class="bar">
                <span class="html"></span>
            </div>
        </div>

        <div class="skill">
            <div class="skill-title">
                <span>CSS</span>
                <span>90%</span>
            </div>
            <div class="bar">
                <span class="css"></span>
            </div>
        </div>

        <div class="skill">
            <div class="skill-title">
                <span>JavaScript</span>
                <span>80%</span>
            </div>
            <div class="bar">
                <span class="js"></span>
            </div>
        </div>

        <div class="skill">
            <div class="skill-title">
                <span>React</span>
                <span>70%</span>
            </div>
            <div class="bar">
                <span class="react"></span>
            </div>
        </div>

    </div>
</section>

<div class="social">
    <a href="#"><i class="ph ph-github-logo"></i></a>
    <a href="#"><i class="ph ph-linkedin-logo"></i></a>
    <a href="#"><i class="ph ph-instagram-logo"></i></a>
</div>
<section class="contact" id="contact">
    <h2>Contact Me</h2>
    <p>If you want to work together, feel free to reach out.</p>

    <div class="contact-box">
        <div>Email: xuannguyen210820d@gmail.com</div>
        <div>Phone: 0342094829</div>
        <div>Location: Bến cầu Tây Ninh</div>
    </div>

</body>
</html>
