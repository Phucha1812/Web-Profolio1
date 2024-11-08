<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <!-- reset css -->
    <link rel="stylesheet" href="./assets/css/reset.css" />
    <!-- embed fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link href="https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,400;0,500;0,600;0,700;1,400&family=Sen:wght@700&display=swap"
          rel="stylesheet" />
    <!-- styles -->
    <link rel="stylesheet" href="./assets/css/style.css" />

    <title>Web Profolio</title>
    <style>
        * {
            box-sizing: border-box;
        }

        :root {
            --font-heading: "Sen", sans-serif;
            --primary-color: #ffb900;
        }

        html {
            font-size: 62.5%;
        }

        /* khôi phục lại cỡ chữ mặc định theo rem */
        body {
            font-size: 1.6rem;
            font-family: "Poppins", sans-serif;
        }
        /* =================common================== */
        a {
            text-decoration: none;
        }

        .heading-lv2 {
            color: #171100;
            font-family: var(--font-heading);
            font-size: 3.8rem;
            font-weight: 700;
            line-height: 1.27;
            letter-spacing: -0.76px;
        }

        .btn {
            display: inline-block;
            min-width: 118px;
            padding: 0 16px;
            line-height: 50px;
            color: #fff;
            text-align: center;
            font-size: 1.6rem;
            font-weight: 600;
            border-radius: 999px;
            background: #171100;
        }

            .btn:hover {
                cursor: pointer;
                opacity: 0.9;
            }

        .main-content {
            width: 1170px;
            max-width: calc(100% - 48px);
            margin-left: auto;
            margin-right: auto;
        }

        .line-clamp {
            display: -webkit-box;
            -webkit-line-clamp: var(--line-clamp, 1);
            -webkit-box-orient: vertical;
            overflow: hidden;
        }

            .line-clamp.line-2 {
                --line-clamp: 2;
            }

        .break-all {
            word-break: break-all;
        }
        /* =================header================== */
        .header {
            background: #fffcf4;
        }

            .header.fixed {
                z-index: 1;
                position: sticky;
                top: -28px;
            }

            .header .body {
                display: flex;
                align-items: center;
                padding: 36px 0 8px;
            }

        .body .logo {
            width: 100px;
            height: 50px;
        }

        .nav {
            margin-left: auto;
        }

            .nav ul {
                display: flex;
            }

            .nav a {
                position: relative;
                color: #5f5b53;
                font-size: 1.6rem;
                padding: 8px 21px;
            }

                .nav li.active a,
                .nav a:hover {
                    color: #171100;
                    /* font-weight: 600; */
                    text-shadow: 1px 0 0 currentColor;
                }

                    .nav li.active a::after {
                        position: absolute;
                        left: 21px;
                        bottom: 6px;
                        display: block;
                        content: "";
                        width: 12px;
                        height: 2px;
                        border-radius: 1px;
                        background: #171100;
                    }

        .header .btn-sign-up {
            min-width: 144px;
        }

        .header .action {
            margin-left: 49px;
        }

        /* ================hero================== */
        .hero {
            padding: 56px 0 65px;
            background: #fffcf4;
        }

            .hero .body {
                display: flex;
            }

            /* ========= hero left ============== */
            .hero .media-block {
                position: relative;
                width: 48%;
            }

                .hero .media-block .img {
                    width: 470px;
                    height: 620px;
                    object-fit: cover;
                    border-radius: 20px;
                }

            .hero .hero-summary {
                padding: 24px;
                width: 270px;
                position: absolute;
                bottom: 48px;
                right: 0;
                border-radius: 12px;
                background: #fff;
                box-shadow: 0px 16px 32px 0px rgba(0, 0, 0, 0.05);
            }

        .hero-summary .item {
            display: flex;
            align-items: center;
        }

            .hero-summary .item + .item {
                margin-top: 22px;
            }

        .hero-summary .icon {
            width: 48px;
            height: 48px;
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            background-color: #fff9e8;
        }

        .hero-summary .icon2 {
            background-color: #fcefff;
        }

        .hero-summary .icon3 {
            background-color: #ebeaff;
        }

        .hero-summary .info {
            margin-left: 16px;
        }

        .hero-summary .label {
            color: #5f5b53;
            font-size: 1.4rem;
            line-height: 1.86; /* 185.714% */
        }

        .hero-summary .title {
            color: #171100;
            font-size: 1.8rem;
            font-weight: 600;
            line-height: 1.67; /* 166.667% */
        }

        /* =========== hero right======== */
        .hero .content-block {
            width: 52%;
            padding-left: 130px;
            padding-top: 64px;
        }

        .hero .heading {
            color: #171100;
            font-family: var(--font-heading);
            font-size: 5.8rem;
            font-size: 700;
            line-height: 1.17;
            letter-spacing: -1.16px;
        }

        .hero .desc {
            color: #5f5b53;
            font-size: 1.8rem;
            line-height: 1.67;
            margin-top: 22;
        }

        .hero .cta-group {
            background: #ffffff;
            margin-top: 38px;
            display: flex;
            align-items: center;
        }

        .hero-cta {
            min-width: 180px;
            background-color: var(--primary-color);
            line-height: 64px;
            border-radius: 32px;
        }

        .hero .watch-video {
            /* nền trong suốt */
            background: transparent;
            margin-left: 28px;
            border: none;
            display: flex;
            align-items: center;
            cursor: pointer;
        }

            .hero .watch-video .icon {
                width: 40px;
                height: 40px;
                border-radius: 40px;
                display: flex;
                align-items: center;
            }

            .hero .watch-video span {
                color: #171100;
                margin-left: 14px;
                font-size: 1.8rem;
                font-weight: 600;
                line-height: 1.67;
            }

        .hero .desc-recent {
            color: #5f5b53;
            line-height: 30px;
            font-size: 1.8rem;
            margin-top: 30px;
        }

        .hero .stats {
            margin-top: 10px;
        }

            .hero .stats strong {
                color: #171100;
                font-size: 4.4rem;
                line-height: 54px;
                font-weight: 700;
            }

                .hero .stats strong:nth-child(2) {
                    margin-left: 24px;
                }

        /* popular */
        .popular {
            padding: 65px 0;
            margin-top: 135px;
        }

        .popular-top {
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

            .popular-top .desc {
                margin-top: 16px;
                width: 458px;
                color: #5f5b53;
                font-size: 1.8rem;
                line-height: 1.67;
            }

            .popular-top .controls {
                display: flex;
                gap: 18px;
            }

            .popular-top .control-btn {
                display: flex;
                justify-content: center;
                align-items: center;
                background: transparent;
                width: 40px;
                height: 40px;
                border-radius: 50%;
                color: var(--primary-color);
                border: 1px solid var(--primary-color);
            }

                .popular-top .control-btn:hover {
                    background: var(--primary-color);
                    color: #fff;
                    cursor: pointer;
                }

        /* ==============course========== */
        .popular .course-list {
            display: flex;
            gap: 30px;
            margin-top: 55px;
        }

        .popular .course-item {
            /* tránh vỡ giao diện khi chữ hoăc hình quá to */
            flex: 1;
            background-color: #fff;
            border: 1px solid #e2dfda;
        }

        .popular .course-list .thumb {
            width: 100%;
            height: 100%;
        }

        .popular .course-info .thumb {
            border-radius: 12px 12px 0px 0px;
            height: 278px;
            object-fit: cover;
        }

        .popular .course-list .th .popular .course-item .info {
            padding: 16px 22px 22px;
        }

        .popular .course-item .head,
        .popular .course-item .rating,
        .popular .course-item .foot {
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        .popular .rating .value {
            margin-left: 6px;
            color: #fea31b;
            font-size: 16px;
            line-height: 1.75;
        }

        .popular .course-item .title a {
            color: #171100;
            font-size: 1.8rem;
            font-weight: 600;
            line-height: 1.67;
        }

        .popular .course-item .price {
            font-weight: 600;
            color: #171100;
            line-height: 26px;
            font-size: 1.4rem;
        }

        .popular .course-item .foot {
            margin-top: 12px;
        }

        .popular .course-item .desc {
            margin-top: 6px;
            color: #5f5b53;
            font-size: 1.8rem;
            line-height: 1.86;
        }

        .popular .course-item .btn-book:hover {
            background: var(--primary-color);
            color: #fff;
            cursor: pointer;
            border: 1px solid transparent;
        }

        /* =============feedback=========== */
        .feedback {
            margin-top: 135px;
            padding: 96px 0;
            background: #2e2100;
        }

        .feedback-item {
            display: flex;
        }

            .feedback-item .avatar {
                border-radius: 50%;
                width: 72px;
                height: 72px;
                object-fit: cover;
            }

            .feedback-item .info .member-name {
                font-size: 2.4rem;
                font-weight: 700;
                font-family: var(--font-heading);
                color: #ebeaff;
                margin-top: 18px;
                line-height: 34px;
            }

            .feedback-item .info .desc {
                font-size: 1.4rem;
                line-height: 26px;
                color: #bfbcb2;
            }

            .feedback-item .dots {
                gap: 6px;
                display: flex;
                margin-top: 28px;
            }

            .feedback-item .dot {
                background: #634700;
                width: 6px;
                height: 6px;
                border-radius: 50%;
            }

        .feedback .content {
            width: 66%;
            margin-left: auto;
        }

        .feedback-item .dot.active {
            background-color: var(--primary-color);
        }

        .feedback-item blockquote {
            color: #fff;
            font-size: 2.6rem;
            font-style: italic;
            line-height: 40px;
            margin-left: 30px;
        }

        /* ==========features========= */
        .features {
            margin-top: 135px;
            padding: 65px 0;
            gap: 30px;
        }

            .features .body {
                display: flex;
                justify-content: space-between;
            }

            .features .images {
                display: flex;
            }

            .features .lower {
                margin-right: 30px;
                margin-top: 24px;
                width: 270px;
                height: 404px;
                border-radius: 16px;
            }

            .features .hieghter {
                width: 270px;
                height: 405px;
                border-radius: 16px;
                margin-bottom: 24px;
            }

            .features .content {
                /* ====cho dịch sang trái ====== */
                width: 41%;
                flex-direction: column;
                justify-content: center;
            }

                .features .content .heading-lv2 {
                    font-size: 3.8rem;
                    font-weight: 700;
                    line-height: 48px;
                    margin-top: 58px;
                }

                .features .content .desc1 {
                    font-size: 1.6rem;
                    line-height: 28px;
                    color: #5f5b53;
                }

                .features .content .desc2 {
                    font-size: 1.6rem;
                    line-height: 28px;
                    color: #5f5b53;
                    margin-top: 15px;
                }

                .features .content .cta-btn {
                    border-radius: 26px;
                    margin-top: 20px;
                    width: 137px;
                    height: 50px;
                }

                    .features .content .cta-btn:hover {
                        background: var(--primary-color);
                        color: #fff;
                        cursor: pointer;
                        border: 1px solid transparent;
                    }

        /* =================features 2=============== */
        .features2 {
            padding: 65px 0;
            margin-top: 35px;
        }

            .features2 .body {
                display: flex;
                justify-content: space-between;
            }

            .features2 .content {
                margin-top: 71px;
                margin-right: 135px;
            }

            .features2 .images-features2 img {
                width: 150%;
                height: 100%;
            }

            .features2 .content .heading-lv3 {
                font-size: 3.8rem;
                font-weight: 700;
                line-height: 48px;
                color: #171100;
            }

            .features2 .content .desc {
                margin-top: 15px;
                color: #5f5b53;
                width: 570px;
                font-size: 1.6rem;
                line-height: 28px;
                height: 56px;
            }

            .features2 .content .cta-btn {
                width: 137px;
                height: 50px;
                border-radius: 26px;
                margin-top: 20px;
            }

                .features2 .content .cta-btn:hover {
                    background: var(--primary-color);
                    color: #fff;
                    cursor: pointer;
                    border: 1px solid transparent;
                }

            .features2 .images-features2 {
                width: 470px;
                height: 440px;
                border-radius: 20px;
            }

        /* =============blog============ */
        .blogs {
            margin-top: 135px;
            padding: 96px 0;
            background: #fffcf4;
        }

            .blogs .blog-top {
                text-align: center;
            }

                .blogs .blog-top .desc {
                    margin: 16px auto 0;
                    width: 448px;
                    color: #696262;
                    font-size: 1.6rem;
                    line-height: 1.75;
                }

        .blog-list {
            margin-top: 53px;
            display: flex;
        }

            .blog-list .item .igames {
                border-radius: 16px 16px 0 0;
                width: 370px;
                height: 250px;
            }

            .blog-list .info {
                flex-shrink: 0;
                background: #fff;
            }

        .blogs .item .date::before {
            content: "";
            margin-right: 4px;
            display: inline-block;
            width: 6px;
            height: 6px;
            border-radius: 50%;
            background: var(--primary-color);
        }

        .blogs .item .date::after {
            position: absolute;
            left: 0;
            bottom: 0;
            right: -27px;
            content: "";
            display: inline-block;
            height: 1px;
            border-radius: 0.5px;
            background: #c4c3c2;
        }

        .blogs .item .title {
            margin-top: 25px;
            font-size: 1.6rem;
            line-height: 28px;
            font-weight: 600;
            color: #171100;
        }

        .blogs .item .btn {
            margin-top: 13px;
            border-radius: 25px;
        }

            .blogs .item .btn:hover {
                background: var(--primary-color);
            }

        .blogs .item .dots {
            gap: 6px;
            display: flex;
            margin-top: 28px;
        }

        .blogs .item .dots {
            background: #634700;
            width: 6px;
            height: 6px;
            border-radius: 50%;
        }

        .blogs .item .dot.active {
            background-color: var(--primary-color);
        }

        /* =========feedback2======= */
        .feedback1 {
            margin-top: 135px;
            padding: 96px 0;
            background: #2e2100;
        }

            .feedback1 .box-child {
                color: #ffffff;
                background: transparent;
            }

            .feedback1 .box1 .images {
                background-color: #2e2100;
            }

            .feedback1 .images {
                width: 100px;
                height: 100px;
            }

            .feedback1 .desc {
                color: #fcefff;
            }

    </style>

</head>
<body>
    <!-- header -->
    <header class="header fixed">
        <div class="main-content">
            <div class="body">
                <!-- logo -->
                <img src="./assets/img/Logo (1).jpg" alt="" class="logo">
                <!-- nav -->
                <nav class="nav">
                    <ul>
                        <li class="active">
                            <a href="#!">Home</a>
                        </li>
                        <li>
                            <a href="#!">Courses</a>
                        </li>
                        <li>
                            <a href="#!">Pricing</a>
                        </li>
                        <li>
                            <a href="#!">Reviews</a>
                        </li>
                    </ul>
                </nav>
                <!-- btn action -->
                <!-- .action>a.btn{Sign Up} -->
                <div class="action">
                    <a href="#!" class="btn btn-sign-up">Sign Up</a>
                </div>
            </div>
        </div>
    </header>

    <!-- main -->
    <main>
        <!-- hero -->
        <div class="hero">
            <div class="main-content">
                <div class="body">
                    <!-- hero left -->
                    <div class="media-block">
                        <!-- Shift + Alt + Right Arow -->
                        <img src="./assets/img/anh1.jpg" alt="Learn without limits and spread knowledge."
                             class="img">

                        <div class="hero-summary">
                            <!-- item1 -->
                            <div class="item">
                                <div class="icon">
                                    <img src="./icon/Group 17525.jpg" alt="">
                                </div>

                                <div class="info">
                                    <p class="label">20 Courses</p>
                                    <p class="title">UI/UX Design</p>
                                </div>
                            </div>

                            <!-- item2 -->
                            <div class="item">
                                <div class="icon icon2">
                                    <img src="./icon/Group 17524.jpg" alt="">
                                </div>

                                <div class="info">
                                    <p class="label">20 Courses</p>
                                    <p class="title">Development</p>
                                </div>
                            </div>


                            <!-- item3 -->
                            <div class="item">
                                <div class="icon icon3">
                                    <img src="./icon/Group 17523.jpg" alt="">
                                </div>

                                <div class="info">
                                    <p class="label">30 Courses</p>
                                    <p class="title">Marketing</p>
                                </div>
                            </div>
                        </div>
                    </div>
                    <!-- hero right -->
                    <div class="content-block">
                        <h1 class="heading">
                            Học không giới hạn và truyền bá kiến ​​thức.
                        </h1>
                        <p class="desc">
                            Nâng cao kỹ năng lập trình và công nghệ để biến "năm nay là năm của tôi" thành hiện thực với các khóa học, chứng chỉ, và bằng cấp từ các trường đại học và công ty hàng đầu trong lĩnh vực công nghệ.
                        </p>

                        <div class="cta-group">
                            <a href="#!" class="btn hero-cta">See Courses</a>
                            <button class="watch-video">
                                <div class="icon">
                                    <img src="./icon/Polygon 2.jpg" alt="">
                                </div>
                                <span>Watch Video</span>
                            </button>
                        </div>

                        <p class="desc desc-recent">Hoạt động gần đây</p>
                        <p class="desc stats">
                            <strong>50K</strong> Students
                            <strong>70+</strong> Courses
                        </p>

                    </div>

                </div>
            </div>
        </div>


        <!--popular  -->
        <div class="popular">
            <div class="main-content">
                <div class="popular-top">
                    <!-- popular left -->
                    <div class="info">
                        <h2 class="heading-lv2">Các Kháo Học Phổ Biến</h2>
                        <p class="desc">Xây dựng kỹ năng mới với các khóa học xu hướng và tỏa sáng cho sự nghiệp tương lai.</p>
                    </div>


                    <!-- popular right -->
                    <div class="controls">
                        <button class="control-btn">
                            <svg width="8" height="14" viewBox="0 0 8 14" fill="none"
                                 xmlns="http://www.w3.org/2000/svg">
                                <path d="M7 1L1 7L7 13" stroke="currentColor" stroke-linecap="round"
                                      stroke-linejoin="round" />
                            </svg>
                        </button>
                        <button class="control-btn">
                            <svg width="8" height="14" viewBox="0 0 8 14" fill="none"
                                 xmlns="http://www.w3.org/2000/svg">
                                <path d="M1 1L7 7L1 13" stroke="currentColor" stroke-linecap="round"
                                      stroke-linejoin="round" />
                            </svg>

                        </button>
                    </div>
                </div>


                <div class="course-list">
                    <!-- item 1 -->
                    <div class="course-item">
                        <a href="#!"><img src="./assets/img/Ứng dụng quản lý sinh viên.jpg" alt="Basic web design" class="thumb"></a>
                        <div class="info">
                            <div class="head">
                                <h3 class="title"><a class="line-clamp break-all" href="#!">Ứng dụng quản lý sinh viên</a></h3>
                                <div class="rating">
                                    <img src="./icon/Star 6.jpg" alt="" class="star">
                                    <span class="value">4.5</span>
                                </div>
                            </div>
                            <p class="desc line-clamp line-2 break-all">Thiết kế ứng dụng quản lý thông tin sinh viên, giúp dễ dàng theo dõi và quản lý kết quả học tập.</p>

                            <div class="foot">
                                <span class="price">$120.75</span>
                                <button class="btn btn-book">Book Now</button>
                            </div>
                        </div>
                    </div>

                    <!-- item 2 -->
                    <div class="course-item">
                        <a href="#!"><img src="./assets/img/Website thương mại điện tử.jpg" alt="UI/UX design" class="thumb"></a>
                        <div class="info">
                            <div class="head">
                                <h3 class="title"><a class="line-clamp break-all" href="#!">Website thương mại điện tử</a></h3>
                                <div class="rating">
                                    <img src="./icon/Star 6.jpg" alt="" class="star">
                                    <span class="value">4.5</span>
                                </div>
                            </div>
                            <p class="desc  line-clamp line-2 break-all">
                                Xây dựng website bán hàng trực tuyến với tính năng giỏ hàng, thanh toán và theo dõi đơn hàng.
                            </p>

                            <div class="foot">
                                <span class="price">$120.75</span>
                                <button class="btn btn-book">Book Now</button>
                            </div>
                        </div>
                    </div>

                    <!-- item 3 -->
                    <div class="course-item">
                        <a href="#!"><img src="./assets/img/Ứng dụng quản lý công việc nhóm.jpg" alt="Web App design" class="thumb"></a>
                        <div class="info">
                            <div class="head">
                                <h3 class="title"><a class="line-clamp break-all" href="#!">Ứng dụng quản lý công việc nhóm</a></h3>
                                <div class="rating">
                                    <img src="./icon/Star 6.jpg" alt="" class="star">
                                    <span class="value">4.5</span>
                                </div>
                            </div>
                            <p class="desc  line-clamp line-2 break-all">
                                Phát triển ứng dụng giúp sinh viên lên kế hoạch, phân chia công việc và theo dõi tiến độ của các dự án nhóm.
                            </p>

                            <div class="foot">
                                <span class="price">$120.75</span>
                                <button class="btn btn-book">Book Now</button>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>


        <!-- feedback -->

        <div class="feedback">
            <div class="main-content">
                <div class="feedback-list">
                    <div class="feedback-item">
                        <!-- khối bên trái -->
                        <div class="info">
                            <img src="./assets/img/anh2.jpg" alt="Peter Moor" class="avatar">
                            <p class="member-name">Hoang Phuc</p>
                            <p class="desc">Sinh viên Thiết kế Web</p>
                            <div class="dots">
                                <span class="dot"></span>
                                <span class="dot active"></span>
                                <span class="dot"></span>
                            </div>
                        </div>

                        <!-- khối bên phải  -->
                        <div class="content">
                            <img src="./icon/Vector.jpg" alt="" class="open-quotes">
                            <blockquote>Không chỉ có hồ sơ của tôi trông ấn tượng—đầy đủ tên và logo của các tổ chức hàng đầu thế giới—mà những chứng chỉ này cũng giúp tôi tiến gần hơn đến mục tiêu nghề nghiệp bằng cách xác thực những kỹ năng tôi đã học. </blockquote>
                        </div>

                    </div>
                </div>
            </div>
        </div>


        <!--features  1-->
        <div class="features">
            <div class="main-content">
                <div class="body">
                    <div class="images">
                        <img class="lower" src="./assets/img/anh3.jpg" alt="Rectangle 10">
                        <img class="hieghter" src="./assets/img/anh3.jpg" alt="Rectangle 11">
                    </div>
                    <div class="content">
                        <h2 class="heading-lv2">Kết quả học tập thông qua nền tảng tuyệt vời của tôi</h2>
                        <p class="desc1">87% người học để phát triển nghề nghiệp báo cáo những lợi ích như được thăng chức, tăng lương hoặc bắt đầu một sự nghiệp mới.</p>
                        <p class="desc2">Báo cáo</p>
                        <a href="!#" class="btn cta-btn">Đăng Ký</a>
                    </div>
                </div>
            </div>
        </div>




        <!--features  2-->

        <div class="features2">
            <div class="main-content">
                <div class="body">
                    <div class="content">
                        <h2 class="heading-lv3">Hãy tiến một bước tiếp theo hướng tới mục tiêu cá nhân và nghề nghiệp của bạn.</h2>
                        <p class="desc">Hãy tiến một bước tiếp theo. Tham gia ngay để nhận được những gợi ý cá nhân hóa và nhiều gợi ý hơn từ toàn bộ danh mục.</p>
                        <a href="!#" class="btn cta-btn">Tham gia</a>
                    </div>

                    <div class="images-features2">
                        <img src="./assets/img/anh1.jpg" alt="Rectangle 11.1">

                    </div>
                </div>
            </div>
        </div>



        <!--===== blog=== -->
        <div class="blogs">
            <div class="main-content">
                <div class="blog-top">
                    <h2 class="heading-lv2">Our blog</h2>
                    <p class="desc">Các tin tức mới nhất của tôi</p>
                </div>

                <div class="blog-list">
                    <!-- item1 -->
                    <div class="item">
                        <img src="./assets/img/our1.jpg" alt="" class="igames">
                        <div class="info">
                            <span class="date">08 November 2024</span>
                            <a href="#!">
                                <h3 class="title">Cách trở thành một nhà thiết kế web chuyên nghiệp vào năm 2025 và tìm được việc làm từ xa?</h3>
                            </a>
                            <a href="!#" class="btn">Đọc Ngay</a>
                        </div>
                    </div>


                    <!-- item1 -->
                    <div class="item">
                        <img src="./assets/img/our2.jpg" alt="" class="igames">
                        <div class="info">
                            <span class="date">08 November 2024</span>
                            <a href="#!">
                                <h3 class="title">Cách trở thành một nhà thiết kế web chuyên nghiệp vào năm 2025 và tìm được việc làm từ xa?</h3>
                            </a>
                            <a href="!#" class="btn">Đọc Ngay</a>
                        </div>
                    </div>


                    <!-- item1 -->
                    <div class="item">
                        <img src="./assets/img/our3.jpg" alt="" class="igames">
                        <div class="info">
                            <span class="date">08 November 2024</span>
                            <a href="#!">
                                <h3 class="title">Cách trở thành một nhà thiết kế web chuyên nghiệp vào năm 2025 và tìm được việc làm từ xa?</h3>
                            </a>
                            <a href="!#" class="btn">Đọc Ngay</a>
                        </div>
                    </div>

                    <div class="dots">
                        <span class="dot"></span>
                        <span class="dot active"></span>
                        <span class="dot"></span>
                    </div>


                </div>




            </div>
        </div>



        <!-- feedback2 -->
        <div class="feedback1">
            <div class="main-content">
                <div class="feeback-list">
                    <div class="class-item">
                        <div class="box1">
                            <img src="./assets/img/Logo (1).jpg" alt="Lesion" class="images">
                            <div class="desc">Cần giúp đỡ để đạt được sự nghiệp mơ ước của bạn? Hãy tin tưởng chúng tôi. Với HoangPhuc, việc học tập trở nên dễ dàng hơn rất nhiều khi có chúng tôi đồng hành.</div>
                            <div class="box-child">
                                Sdt : 0799521235
                                <br>
                                Email: hhp18122004@gmail.com


                            </div>
                        </div>
                    </div>
                </div>

            </div>
        </div>
        </div>
        </div>

</body>
</html>
‣敗ⵢ牐景汯潩�