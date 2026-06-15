<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>แฟ้มสะสมผลงาน | My Portfolio</title>
    
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Sarabun:wght@300;400;600;700&display=swap" rel="stylesheet">

    <style>
        /* --- 1. การตั้งค่าพื้นฐาน (Reset & Global Styles) --- */
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Sarabun', 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        html {
            scroll-behavior: smooth; /* เลื่อนหน้าจอแบบนุ่มนวล */
        }

        body {
            background-color: #FAFAFA;
            color: #333333;
            line-height: 1.6;
            padding-top: 60px; /* หลบแถว Navigation Bar แบบ Sticky */
        }

        section {
            padding: 80px 20px;
            min-height: 80vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
        }

        .container {
            width: 100%;
            max-width: 800px;
            margin: 0 auto;
        }

        h2 {
            font-size: 2.2rem;
            color: #1976D2;
            margin-bottom: 30px;
            text-align: center;
            position: relative;
        }

        h2::after {
            content: '';
            display: block;
            width: 50px;
            height: 4px;
            background-color: #2196F3;
            margin: 10px auto 0;
            border-radius: 2px;
        }

        /* --- 2. Navigation Bar (Sticky) --- */
        .navbar {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            background-color: #FFFFFF;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            z-index: 1000;
            display: flex;
            justify-content: center;
            padding: 15px 0;
        }

        .navbar a {
            color: #555555;
            text-decoration: none;
            font-weight: 600;
            margin: 0 15px;
            font-size: 1rem;
            transition: color 0.3s ease;
        }

        .navbar a:hover {
            color: #2196F3;
        }

        /* --- 3. ส่วนหัว (Header/Hero) --- */
        .hero {
            background: linear-gradient(135deg, #E3F2FD 0%, #BBDEFB 100%);
            text-align: center;
            padding: 100px 20px;
        }

        .profile-img {
            width: 200px;
            height: 200px;
            border-radius: 50%;
            object-fit: cover;
            border: 5px solid #FFFFFF;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.15);
            margin-bottom: 20px;
        }

        .hero h1 {
            font-size: 2.8rem;
            color: #0D47A1;
            margin-bottom: 10px;
        }

        .hero p {
            font-size: 1.3rem;
            color: #1E88E5;
            font-weight: 600;
        }

        /* --- 4. ส่วนประวัติย่อ (About Me) --- */
        .about {
            background-color: #FFFFFF;
        }

        .about-text {
            font-size: 1.15rem;
            text-align: center;
            max-width: 650px;
            margin: 0 auto;
            color: #555555;
        }

        /* --- 5. ส่วนความสามารถพิเศษ (Skills) --- */
        .skills {
            background-color: #E3F2FD;
        }

        .skill-container {
            width: 100%;
            background-color: #FFFFFF;
            padding: 30px;
            border-radius: 12px;
            box-shadow: 0 4px 6px rgba(0,0,0,0.05);
        }

        .skill-wrapper {
            margin-bottom: 20px;
        }

        .skill-wrapper:last-child {
            margin-bottom: 0;
        }

        .skill-info {
            display: flex;
            justify-content: space-between;
            font-weight: 600;
            margin-bottom: 5px;
            color: #0D47A1;
        }

        .progress-bar-bg {
            width: 100%;
            height: 12px;
            background-color: #ECEFF1;
            border-radius: 6px;
            overflow: hidden;
        }

        .progress-bar-fill {
            height: 100%;
            background-color: #2196F3;
            width: 0%; /* เริ่มต้นจาก 0% เพื่อทำแอนิเมชันใน JS */
            border-radius: 6px;
            transition: width 1.5s cubic-bezier(0.1, 1, 0.1, 1); /* แอนิเมชันค่อยๆ ขยาย */
        }

        /* --- 6. ส่วนช่องทางติดต่อ (Contact) --- */
        .contact {
            background-color: #FFFFFF;
        }

        .contact-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 20px;
            text-align: center;
            margin-top: 20px;
        }

        .contact-item {
            background-color: #FAFAFA;
            padding: 25px;
            border-radius: 10px;
            border: 1px solid #E3F2FD;
            text-decoration: none;
            color: #333333;
            transition: transform 0.3s ease, box-shadow 0.3s ease, background-color 0.3s ease;
        }

        .contact-item:hover {
            transform: translateY(-5px);
            box-shadow: 0 5px 15px rgba(33, 150, 243, 0.2
