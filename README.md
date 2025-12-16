
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bennie Ward | Tattoo & Piercing Artist</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Oswald:wght@200;300;400;500;600;700&family=Inter:wght@100;200;300;400;500;600;700;800;900&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* ================================================================= */
        /* RESET & BASE STYLES */
        /* ================================================================= */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            -webkit-font-smoothing: antialiased;
            -moz-osx-font-smoothing: grayscale;
        }

        html {
            scroll-behavior: smooth;
            scroll-padding-top: 80px;
        }

        body {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, sans-serif;
            font-weight: 400;
            line-height: 1.65;
            color: #f0f0f0;
            background-color: #0a0a0a;
            overflow-x: hidden;
            position: relative;
            min-height: 100vh;
        }

        /* Noise/Grain Texture Overlay */
        body::before {
            content: '';
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='400' height='400' viewBox='0 0 400 400'%3E%3Cfilter id='noiseFilter'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.85' numOctaves='3' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23noiseFilter)' opacity='0.04'/%3E%3C/svg%3E");
            pointer-events: none;
            z-index: 9999;
            opacity: 0.4;
        }

        /* ================================================================= */
        /* COLOR VARIABLES */
        /* ================================================================= */
        :root {
            --color-bg-primary: #0a0a0a;           /* Matte Black */
            --color-bg-secondary: #111111;         /* Dark Charcoal */
            --color-bg-tertiary: #1a1a1a;          /* Medium Charcoal */
            --color-bg-quaternary: #222222;        /* Light Charcoal */
            --color-accent-primary: #8b0000;       /* Deep Blood Red */
            --color-accent-secondary: #9d0000;     /* Slightly Lighter Red */
            --color-accent-tertiary: #7a0000;      /* Slightly Darker Red */
            --color-text-primary: #f5f5f5;         /* Off-White */
            --color-text-secondary: #cccccc;       /* Light Gray */
            --color-text-tertiary: #999999;        /* Medium Gray */
            --color-border-primary: #333333;       /* Dark Border */
            --color-border-secondary: #444444;     /* Medium Border */
            --color-border-accent: #5a0000;        /* Red Border */
            --color-shadow-primary: rgba(0, 0, 0, 0.5);
            --color-shadow-secondary: rgba(0, 0, 0, 0.8);
            --color-overlay-dark: rgba(0, 0, 0, 0.75);
            --color-overlay-red: rgba(139, 0, 0, 0.85);
            --color-success: #2e7d32;
            --color-warning: #ed6c02;
            --color-error: #d32f2f;
            --color-info: #0288d1;
        }

        /* ================================================================= */
        /* TYPOGRAPHY */
        /* ================================================================= */
        h1, h2, h3, h4, h5, h6,
        .font-heading,
        .logo,
        .hero-title,
        .section-title h2,
        .pricing-card h3,
        .cta h2,
        .booking-form h3,
        .footer-content h3 {
            font-family: 'Oswald', 'Impact', 'Arial Narrow', sans-serif;
            font-weight: 600;
            letter-spacing: 1.5px;
            text-transform: uppercase;
            line-height: 1.2;
        }

        h1 {
            font-size: clamp(3rem, 8vw, 5rem);
            letter-spacing: 4px;
        }

        h2 {
            font-size: clamp(2.2rem, 5vw, 3.2rem);
            letter-spacing: 3px;
        }

        h3 {
            font-size: clamp(1.8rem, 4vw, 2.4rem);
            letter-spacing: 2px;
        }

        h4 {
            font-size: clamp(1.4rem, 3vw, 1.8rem);
            letter-spacing: 1.5px;
        }

        p, li, span, label, input, textarea, select, button, a {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, sans-serif;
        }

        p {
            font-size: 1.1rem;
            line-height: 1.75;
            margin-bottom: 1.5rem;
        }

        .text-large {
            font-size: 1.3rem;
            line-height: 1.8;
        }

        .text-small {
            font-size: 0.95rem;
            line-height: 1.5;
        }

        .text-center {
            text-align: center;
        }

        .text-left {
            text-align: left;
        }

        .text-right {
            text-align: right;
        }

        .text-accent {
            color: var(--color-accent-primary);
        }

        .text-muted {
            color: var(--color-text-tertiary);
        }

        .font-bold {
            font-weight: 700;
        }

        .font-medium {
            font-weight: 500;
        }

        .font-light {
            font-weight: 300;
        }

        /* ================================================================= */
        /* LAYOUT & CONTAINERS */
        /* ================================================================= */
        .container {
            width: 100%;
            max-width: 1280px;
            margin: 0 auto;
            padding: 0 24px;
        }

        .container-narrow {
            width: 100%;
            max-width: 900px;
            margin: 0 auto;
            padding: 0 24px;
        }

        .container-wide {
            width: 100%;
            max-width: 1600px;
            margin: 0 auto;
            padding: 0 24px;
        }

        .section {
            padding: 100px 0;
            position: relative;
        }

        .section-sm {
            padding: 60px 0;
        }

        .section-lg {
            padding: 140px 0;
        }

        .page {
            width: 100%;
            min-height: 100vh;
            position: relative;
        }

        /* ================================================================= */
        /* HEADER / NAVIGATION */
        /* ================================================================= */
        .header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 80px;
            background-color: rgba(10, 10, 10, 0.97);
            backdrop-filter: blur(12px) saturate(180%);
            -webkit-backdrop-filter: blur(12px) saturate(180%);
            border-bottom: 1px solid rgba(51, 51, 51, 0.4);
            z-index: 1000;
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
        }

        .header.scrolled {
            height: 70px;
            background-color: rgba(10, 10, 10, 0.98);
            border-bottom-color: rgba(51, 51, 51, 0.6);
            box-shadow: 0 5px 25px rgba(0, 0, 0, 0.3);
        }

        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            height: 100%;
            width: 100%;
            padding: 0 10px;
        }

        .logo {
            font-size: 1.9rem;
            font-weight: 700;
            color: var(--color-text-primary);
            letter-spacing: 3px;
            text-decoration: none;
            position: relative;
            padding: 5px 0;
            transition: color 0.3s ease;
            z-index: 1001;
        }

        .logo:hover {
            color: var(--color-accent-primary);
        }

        .logo::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100%;
            height: 2px;
            background-color: var(--color-accent-primary);
            transform: scaleX(0);
            transform-origin: right;
            transition: transform 0.4s cubic-bezier(0.4, 0, 0.2, 1);
        }

        .logo:hover::after {
            transform: scaleX(1);
            transform-origin: left;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 48px;
            align-items: center;
        }

        .nav-links li {
            position: relative;
        }

        .nav-links a {
            color: var(--color-text-primary);
            text-decoration: none;
            font-size: 1.05rem;
            font-weight: 500;
            letter-spacing: 1.2px;
            position: relative;
            padding: 8px 0;
            transition: all 0.3s ease;
            display: inline-block;
        }

        .nav-links a::before {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 0;
            height: 2px;
            background-color: var(--color-accent-primary);
            transition: width 0.4s cubic-bezier(0.4, 0, 0.2, 1);
        }

        .nav-links a:hover::before,
        .nav-links a.active::before {
            width: 100%;
        }

        .nav-links a:hover {
            color: var(--color-accent-primary);
        }

        .nav-links a.active {
            color: var(--color-accent-primary);
            font-weight: 600;
        }

        .mobile-menu-btn {
            display: none;
            background: none;
            border: none;
            color: var(--color-text-primary);
            font-size: 1.8rem;
            cursor: pointer;
            width: 44px;
            height: 44px;
            border-radius: 4px;
            align-items: center;
            justify-content: center;
            transition: all 0.3s ease;
            z-index: 1001;
        }

        .mobile-menu-btn:hover {
            background-color: rgba(255, 255, 255, 0.05);
            color: var(--color-accent-primary);
        }

        /* ================================================================= */
        /* HERO SECTION */
        /* ================================================================= */
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            position: relative;
            overflow: hidden;
            padding-top: 80px;
            background: linear-gradient(135deg, rgba(10, 10, 10, 0.95) 0%, rgba(17, 17, 17, 0.9) 100%);
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: radial-gradient(circle at 30% 50%, rgba(139, 0, 0, 0.15) 0%, transparent 70%),
                        radial-gradient(circle at 70% 20%, rgba(139, 0, 0, 0.1) 0%, transparent 60%);
            pointer-events: none;
            z-index: 0;
        }

        .hero-content {
            position: relative;
            z-index: 1;
            max-width: 900px;
            padding: 0 24px;
        }

        .hero-title {
            font-size: clamp(3.5rem, 10vw, 6rem);
            margin-bottom: 20px;
            letter-spacing: 6px;
            color: var(--color-text-primary);
            text-shadow: 0 5px 15px rgba(0, 0, 0, 0.5);
            line-height: 1.1;
        }

        .hero-subtitle {
            font-size: clamp(1.3rem, 3vw, 1.8rem);
            color: var(--color-text-secondary);
            margin-bottom: 30px;
            letter-spacing: 4px;
            font-weight: 300;
        }

        .hero-divider {
            width: 180px;
            height: 3px;
            background-color: var(--color-accent-primary);
            margin: 30px auto 35px;
            position: relative;
            overflow: hidden;
        }

        .hero-divider::after {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.4), transparent);
            animation: shimmer 3s infinite;
        }

        @keyframes shimmer {
            0% { left: -100%; }
            100% { left: 100%; }
        }

        .hero-text {
            font-size: clamp(1.1rem, 2vw, 1.4rem);
            color: var(--color-text-secondary);
            margin-bottom: 50px;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
            font-weight: 300;
            letter-spacing: 1px;
        }

        .hero-buttons {
            display: flex;
            gap: 24px;
            justify-content: center;
            flex-wrap: wrap;
            margin-top: 40px;
        }

        /* ================================================================= */
        /* BUTTONS */
        /* ================================================================= */
        .btn {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            padding: 16px 38px;
            font-size: 1.05rem;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 2px;
            border: 2px solid var(--color-accent-primary);
            border-radius: 0;
            cursor: pointer;
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
            text-decoration: none;
            position: relative;
            overflow: hidden;
            background-color: transparent;
            color: var(--color-accent-primary);
            min-width: 180px;
            text-align: center;
            z-index: 1;
        }

        .btn::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background-color: var(--color-accent-primary);
            transition: left 0.4s cubic-bezier(0.4, 0, 0.2, 1);
            z-index: -1;
        }

        .btn:hover::before {
            left: 0;
        }

        .btn:hover {
            color: var(--color-text-primary);
            box-shadow: 0 10px 25px rgba(139, 0, 0, 0.3);
            transform: translateY(-3px);
        }

        .btn:active {
            transform: translateY(-1px);
            box-shadow: 0 5px 15px rgba(139, 0, 0, 0.2);
        }

        .btn-outline {
            background-color: transparent;
            color: var(--color-accent-primary);
        }

        .btn-solid {
            background-color: var(--color-accent-primary);
            color: var(--color-text-primary);
            border-color: var(--color-accent-primary);
        }

        .btn-solid::before {
            background-color: var(--color-accent-secondary);
        }

        .btn-solid:hover {
            color: var(--color-text-primary);
            border-color: var(--color-accent-secondary);
        }

        .btn-small {
            padding: 12px 28px;
            font-size: 0.95rem;
            min-width: 140px;
        }

        .btn-large {
            padding: 20px 48px;
            font-size: 1.2rem;
            min-width: 220px;
        }

        .btn-full {
            width: 100%;
        }

        .btn-icon {
            gap: 10px;
        }

        .btn-icon i {
            font-size: 1.2rem;
        }

        /* ================================================================= */
        /* ABOUT SECTION */
        /* ================================================================= */
        .about {
            background-color: var(--color-bg-secondary);
            position: relative;
            overflow: hidden;
        }

        .about::before {
            content: '';
            position: absolute;
            top: -100px;
            right: -100px;
            width: 300px;
            height: 300px;
            background: radial-gradient(circle, rgba(139, 0, 0, 0.1) 0%, transparent 70%);
            border-radius: 50%;
            z-index: 0;
        }

        .about-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 80px;
            align-items: center;
            position: relative;
            z-index: 1;
        }

        .about-text {
            padding-right: 20px;
        }

        .section-title {
            display: flex;
            align-items: center;
            margin-bottom: 40px;
        }

        .accent-line {
            width: 6px;
            height: 50px;
            background-color: var(--color-accent-primary);
            margin-right: 20px;
            position: relative;
            overflow: hidden;
        }

        .accent-line::after {
            content: '';
            position: absolute;
            top: -100%;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(to bottom, transparent, rgba(255, 255, 255, 0.6), transparent);
            animation: lineShine 3s infinite;
        }

        @keyframes lineShine {
            0% { top: -100%; }
            100% { top: 100%; }
        }

        .section-title h2 {
            color: var(--color-text-primary);
            font-size: 2.8rem;
        }

        .about-text p {
            color: var(--color-text-secondary);
            margin-bottom: 25px;
            font-size: 1.15rem;
            line-height: 1.8;
        }

        .about-stats {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 30px;
            margin-top: 40px;
        }

        .stat-item {
            text-align: center;
            padding: 20px;
            background-color: rgba(26, 26, 26, 0.6);
            border-radius: 4px;
            border-left: 3px solid var(--color-accent-primary);
        }

        .stat-number {
            font-size: 2.5rem;
            font-weight: 700;
            color: var(--color-accent-primary);
            margin-bottom: 5px;
            font-family: 'Oswald', sans-serif;
        }

        .stat-label {
            font-size: 1rem;
            color: var(--color-text-secondary);
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .about-image {
            position: relative;
        }

        .image-wrapper {
            position: relative;
            overflow: hidden;
            border-radius: 6px;
            box-shadow: 0 25px 50px rgba(0, 0, 0, 0.5);
            height: 650px;
        }

        .artist-img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            display: block;
            transition: transform 0.8s cubic-bezier(0.4, 0, 0.2, 1);
            filter: grayscale(10%);
        }

        .image-wrapper:hover .artist-img {
            transform: scale(1.03);
            filter: grayscale(0%);
        }

        .image-grain {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='400' height='400' viewBox='0 0 400 400'%3E%3Cfilter id='noiseFilter'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.95' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23noiseFilter)' opacity='0.12'/%3E%3C/svg%3E");
            pointer-events: none;
            mix-blend-mode: overlay;
            opacity: 0.5;
        }

        .image-border {
            position: absolute;
            top: -15px;
            right: -15px;
            bottom: -15px;
            left: -15px;
            border: 2px solid var(--color-accent-primary);
            border-radius: 8px;
            z-index: -1;
            opacity: 0.4;
        }

        /* ================================================================= */
        /* GALLERY SECTION */
        /* ================================================================= */
        .gallery {
            background-color: var(--color-bg-primary);
            position: relative;
        }

        .section-title-center {
            text-align: center;
            margin-bottom: 60px;
            color: var(--color-text-primary);
            position: relative;
            display: inline-block;
            left: 50%;
            transform: translateX(-50%);
        }

        .section-title-center::after {
            content: '';
            position: absolute;
            bottom: -15px;
            left: 50%;
            transform: translateX(-50%);
            width: 100px;
            height: 3px;
            background-color: var(--color-accent-primary);
        }

        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 24px;
        }

        .gallery-item {
            position: relative;
            overflow: hidden;
            border-radius: 8px;
            aspect-ratio: 1 / 1;
            cursor: pointer;
            background-color: var(--color-bg-tertiary);
            transition: all 0.5s cubic-bezier(0.4, 0, 0.2, 1);
        }

        .gallery-item:hover {
            transform: translateY(-8px);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.6);
        }

        .gallery-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            display: block;
            transition: transform 0.8s cubic-bezier(0.4, 0, 0.2, 1);
        }

        .gallery-item:hover img {
            transform: scale(1.08);
        }

        .gallery-overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: var(--color-overlay-red);
            display: flex;
            align-items: center;
            justify-content: center;
            opacity: 0;
            transition: opacity 0.4s cubic-bezier(0.4, 0, 0.2, 1);
        }

        .gallery-item:hover .gallery-overlay {
            opacity: 1;
        }

        .gallery-overlay i {
            font-size: 3rem;
            color: var(--color-text-primary);
            transform: scale(0.8);
            transition: transform 0.4s cubic-bezier(0.4, 0, 0.2, 1);
        }

        .gallery-item:hover .gallery-overlay i {
            transform: scale(1);
        }

        .gallery-load-more {
            text-align: center;
            margin-top: 60px;
        }

        /* ================================================================= */
        /* PRICING SNAPSHOT */
        /* ================================================================= */
        .pricing {
            background-color: var(--color-bg-secondary);
        }

        .pricing-card {
            max-width: 600px;
            margin: 0 auto;
            background-color: var(--color-bg-tertiary);
            padding: 50px 60px;
            border: 3px solid var(--color-accent-primary);
            text-align: center;
            border-radius: 6px;
            position: relative;
            overflow: hidden;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.4);
        }

        .pricing-card::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(139, 0, 0, 0.1) 0%, transparent 70%);
            z-index: 0;
        }

        .pricing-card > * {
            position: relative;
            z-index: 1;
        }

        .pricing-card h3 {
            font-size: 2.2rem;
            margin-bottom: 40px;
            color: var(--color-text-primary);
            letter-spacing: 3px;
        }

        .pricing-item {
            margin-bottom: 35px;
            padding-bottom: 35px;
            border-bottom: 1px solid var(--color-border-primary);
        }

        .pricing-item:last-child {
            border-bottom: none;
            margin-bottom: 0;
            padding-bottom: 0;
        }

        .price {
            font-size: 3.5rem;
            font-weight: 700;
            color: var(--color-accent-primary);
            margin-bottom: 10px;
            font-family: 'Oswald', sans-serif;
            letter-spacing: 2px;
            text-shadow: 0 5px 15px rgba(139, 0, 0, 0.3);
        }

        .price-desc {
            font-size: 1.3rem;
            color: var(--color-text-secondary);
            font-weight: 500;
            letter-spacing: 1px;
        }

        .pricing-note {
            margin-top: 40px;
            padding: 20px;
            background-color: rgba(139, 0, 0, 0.15);
            border-left: 4px solid var(--color-accent-primary);
            text-align: left;
        }

        .pricing-note p {
            color: var(--color-text-secondary);
            font-size: 1.1rem;
            margin-bottom: 0;
            display: flex;
            align-items: center;
            gap: 12px;
        }

        .pricing-note i {
            color: var(--color-accent-primary);
            font-size: 1.3rem;
        }

        /* ================================================================= */
        /* BOOK NOW CTA */
        /* ================================================================= */
        .cta {
            background-color: var(--color-bg-primary);
            position: relative;
            overflow: hidden;
        }

        .cta::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, rgba(139, 0, 0, 0.1) 0%, rgba(10, 10, 10, 1) 100%);
            z-index: 0;
        }

        .cta .container {
            position: relative;
            z-index: 1;
        }

        .cta h2 {
            font-size: 3rem;
            margin-bottom: 40px;
            color: var(--color-text-primary);
            text-align: center;
        }

        .cta-buttons {
            display: flex;
            gap: 30px;
            justify-content: center;
            flex-wrap: wrap;
        }

        /* ================================================================= */
        /* BOOKING PAGE */
        /* ================================================================= */
        #booking-page {
            background-color: var(--color-bg-secondary);
            min-height: 100vh;
        }

        .booking {
            padding-top: 120px;
            padding-bottom: 80px;
        }

        .booking-subtitle {
            text-align: center;
            color: var(--color-text-secondary);
            margin-bottom: 60px;
            font-size: 1.2rem;
            max-width: 800px;
            margin-left: auto;
            margin-right: auto;
            line-height: 1.7;
        }

        .booking-form {
            max-width: 900px;
            margin: 0 auto;
            background-color: var(--color-bg-tertiary);
            padding: 50px;
            border-radius: 8px;
            box-shadow: 0 25px 60px rgba(0, 0, 0, 0.4);
            border: 1px solid var(--color-border-primary);
            position: relative;
        }

        .booking-form::before {
            content: '';
            position: absolute;
            top: -2px;
            left: -2px;
            right: -2px;
            bottom: -2px;
            background: linear-gradient(45deg, var(--color-accent-primary), transparent, var(--color-accent-primary));
            border-radius: 10px;
            z-index: -1;
            opacity: 0.2;
        }

        .form-step {
            display: none;
            animation: fadeIn 0.6s ease forwards;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .form-step.active {
            display: block;
        }

        .form-step h3 {
            font-size: 2rem;
            margin-bottom: 40px;
            color: var(--color-text-primary);
            border-bottom: 2px solid var(--color-border-primary);
            padding-bottom: 20px;
            position: relative;
        }

        .form-step h3::after {
            content: '';
            position: absolute;
            bottom: -2px;
            left: 0;
            width: 100px;
            height: 2px;
            background-color: var(--color-accent-primary);
        }

        .form-group {
            margin-bottom: 32px;
        }

        .form-group label {
            display: block;
            margin-bottom: 12px;
            color: var(--color-text-primary);
            font-weight: 500;
            font-size: 1.1rem;
            letter-spacing: 0.5px;
        }

        .form-group input,
        .form-group select,
        .form-group textarea {
            width: 100%;
            padding: 16px 20px;
            background-color: var(--color-bg-secondary);
            border: 2px solid var(--color-border-primary);
            border-radius: 4px;
            color: var(--color-text-primary);
            font-size: 1.05rem;
            font-family: 'Inter', sans-serif;
            transition: all 0.3s ease;
        }

        .form-group input:focus,
        .form-group select:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: var(--color-accent-primary);
            box-shadow: 0 0 0 3px rgba(139, 0, 0, 0.2);
            background-color: rgba(26, 26, 26, 0.8);
        }

        .form-group input::placeholder,
        .form-group textarea::placeholder {
            color: var(--color-text-tertiary);
        }

        .form-group textarea {
            resize: vertical;
            min-height: 150px;
            line-height: 1.6;
        }

        /* Date input warning */
        .date-warning {
            display: flex;
            align-items: center;
            gap: 10px;
            margin-top: 8px;
            color: var(--color-warning);
            font-size: 0.9rem;
            font-style: italic;
        }

        .date-warning i {
            font-size: 1rem;
        }

        /* File Upload Area */
        .file-upload-area {
            border: 3px dashed var(--color-border-primary);
            border-radius: 6px;
            padding: 50px 30px;
            text-align: center;
            position: relative;
            transition: all 0.3s ease;
            cursor: pointer;
            background-color: rgba(26, 26, 26, 0.5);
        }

        .file-upload-area.dragover {
            border-color: var(--color-accent-primary);
            background-color: rgba(139, 0, 0, 0.1);
        }

        .file-upload-area i {
            font-size: 3.5rem;
            color: var(--color-text-tertiary);
            margin-bottom: 20px;
            transition: color 0.3s ease;
        }

        .file-upload-area:hover i {
            color: var(--color-accent-primary);
        }

        .file-upload-area p {
            color: var(--color-text-secondary);
            margin-bottom: 10px;
            font-size: 1.1rem;
        }

        .file-upload-area .browse {
            color: var(--color-accent-primary);
            text-decoration: underline;
            cursor: pointer;
            font-weight: 600;
            transition: color 0.3s ease;
        }

        .file-upload-area .browse:hover {
            color: var(--color-accent-secondary);
        }

        .file-info {
            font-size: 0.95rem;
            color: var(--color-text-tertiary) !important;
            margin-top: 15px;
        }

        .file-upload-area input[type="file"] {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            opacity: 0;
            cursor: pointer;
        }

        .file-preview {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 30px;
            min-height: 60px;
        }

        .file-preview-item {
            background-color: var(--color-bg-secondary);
            padding: 15px;
            border-radius: 6px;
            display: flex;
            align-items: center;
            gap: 15px;
            max-width: 300px;
            border: 1px solid var(--color-border-primary);
            transition: all 0.3s ease;
        }

        .file-preview-item:hover {
            border-color: var(--color-accent-primary);
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.3);
        }

        .file-preview-item img {
            width: 60px;
            height: 60px;
            object-fit: cover;
            border-radius: 4px;
        }

        .file-preview-info {
            flex: 1;
            min-width: 0;
        }

        .file-preview-info .file-name {
            color: var(--color-text-primary);
            font-weight: 500;
            font-size: 0.95rem;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
            margin-bottom: 5px;
        }

        .file-preview-info .file-size {
            color: var(--color-text-tertiary);
            font-size: 0.85rem;
        }

        .file-preview-item .remove-file {
            color: var(--color-accent-primary);
            cursor: pointer;
            font-size: 1.2rem;
            transition: color 0.3s ease;
            background: none;
            border: none;
            padding: 5px;
            border-radius: 4px;
        }

        .file-preview-item .remove-file:hover {
            color: var(--color-error);
            background-color: rgba(139, 0, 0, 0.1);
        }

        /* Form Progress */
        .form-progress {
            display: flex;
            justify-content: space-between;
            margin: 60px 0 40px;
            position: relative;
            counter-reset: step;
        }

        .form-progress::before {
            content: '';
            position: absolute;
            top: 30px;
            left: 0;
            width: 100%;
            height: 3px;
            background-color: var(--color-border-primary);
            z-index: 1;
        }

        .progress-step {
            text-align: center;
            position: relative;
            z-index: 2;
            flex: 1;
        }

        .step-circle {
            width: 60px;
            height: 60px;
            border-radius: 50%;
            background-color: var(--color-bg-secondary);
            border: 3px solid var(--color-border-primary);
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 15px;
            font-weight: 700;
            color: var(--color-text-tertiary);
            transition: all 0.4s ease;
            font-size: 1.3rem;
            position: relative;
            counter-increment: step;
        }

        .step-circle::before {
            content: counter(step);
        }

        .progress-step.active .step-circle {
            background-color: var(--color-accent-primary);
            border-color: var(--color-accent-primary);
            color: var(--color-text-primary);
            box-shadow: 0 8px 20px rgba(139, 0, 0, 0.4);
        }

        .progress-step.completed .step-circle {
            background-color: var(--color-accent-primary);
            border-color: var(--color-accent-primary);
            color: var(--color-text-primary);
        }

        .progress-step.completed .step-circle::after {
            content: '✓';
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            font-size: 1.5rem;
        }

        .progress-step p {
            color: var(--color-text-tertiary);
            font-size: 1rem;
            font-weight: 500;
            text-transform: uppercase;
            letter-spacing: 1px;
            margin-top: 10px;
        }

        .progress-step.active p {
            color: var(--color-text-primary);
        }

        .progress-step.completed p {
            color: var(--color-accent-primary);
        }

        .form-buttons {
            display: flex;
            justify-content: space-between;
            margin-top: 50px;
            gap: 20px;
        }

        .form-buttons .btn {
            min-width: 160px;
        }

        /* Form Validation */
        .form-group.error input,
        .form-group.error select,
        .form-group.error textarea {
            border-color: var(--color-error);
        }

        .error-message {
            color: var(--color-error);
            font-size: 0.9rem;
            margin-top: 8px;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .error-message i {
            font-size: 1rem;
        }

        .form-success {
            display: none;
            text-align: center;
            padding: 60px 30px;
        }

        .form-success.active {
            display: block;
        }

        .success-icon {
            font-size: 5rem;
            color: var(--color-success);
            margin-bottom: 30px;
        }

        .form-success h3 {
            font-size: 2.5rem;
            color: var(--color-text-primary);
            margin-bottom: 20px;
        }

        .form-success p {
            color: var(--color-text-secondary);
            font-size: 1.2rem;
            max-width: 600px;
            margin: 0 auto 40px;
        }

        /* ================================================================= */
        /* POLICIES SECTION */
        /* ================================================================= */
        .policies {
            background-color: var(--color-bg-primary);
        }

        .section-title-left {
            font-size: 2.8rem;
            margin-bottom: 50px;
            color: var(--color-text-primary);
            position: relative;
            display: inline-block;
        }

        .section-title-left::after {
            content: '';
            position: absolute;
            bottom: -15px;
            left: 0;
            width: 100px;
            height: 3px;
            background-color: var(--color-accent-primary);
        }

        .policies-list {
            max-width: 900px;
        }

        .policy-item {
            display: flex;
            margin-bottom: 28px;
            padding-left: 25px;
            position: relative;
            align-items: flex-start;
        }

        .policy-bullet {
            position: absolute;
            left: 0;
            top: 10px;
            width: 8px;
            height: 8px;
            background-color: var(--color-accent-primary);
            border-radius: 50%;
            box-shadow: 0 0 10px rgba(139, 0, 0, 0.5);
        }

        .policy-item::before {
            content: '';
            position: absolute;
            left: 3px;
            top: 10px;
            width: 2px;
            height: calc(100% + 28px);
            background-color: var(--color-accent-primary);
            opacity: 0.3;
        }

        .policy-item:last-child::before {
            display: none;
        }

        .policy-item p {
            color: var(--color-text-secondary);
            font-size: 1.2rem;
            line-height: 1.7;
            margin-bottom: 0;
        }

        .policy-item strong {
            color: var(--color-text-primary);
            font-weight: 600;
        }

        /* ================================================================= */
        /* FOOTER */
        /* ================================================================= */
        .footer {
            background-color: var(--color-bg-tertiary);
            padding: 70px 0 40px;
            text-align: center;
            border-top: 1px solid var(--color-border-primary);
            position: relative;
        }

        .footer::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='400' height='400' viewBox='0 0 400 400'%3E%3Cfilter id='noiseFilter'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='3' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23noiseFilter)' opacity='0.08'/%3E%3C/svg%3E");
            pointer-events: none;
            z-index: 0;
        }

        .footer-content {
            position: relative;
            z-index: 1;
        }

        .footer-content h3 {
            font-size: 2.2rem;
            margin-bottom: 15px;
            color: var(--color-text-primary);
            letter-spacing: 3px;
        }

        .footer-content > p {
            color: var(--color-text-secondary);
            margin-bottom: 30px;
            font-size: 1.1rem;
        }

        .footer-links {
            display: flex;
            justify-content: center;
            gap: 40px;
            margin: 40px 0;
            flex-wrap: wrap;
        }

        .footer-links a {
            color: var(--color-text-secondary);
            text-decoration: none;
            font-size: 1.05rem;
            font-weight: 500;
            letter-spacing: 1px;
            transition: all 0.3s ease;
            position: relative;
            padding: 5px 0;
        }

        .footer-links a::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 0;
            height: 2px;
            background-color: var(--color-accent-primary);
            transition: width 0.3s ease;
        }

        .footer-links a:hover {
            color: var(--color-accent-primary);
        }

        .footer-links a:hover::after {
            width: 100%;
        }

        .social-icons {
            display: flex;
            justify-content: center;
            gap: 25px;
            margin: 40px 0;
        }

        .social-icons a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 50px;
            height: 50px;
            background-color: var(--color-bg-secondary);
            border-radius: 50%;
            color: var(--color-text-secondary);
            font-size: 1.3rem;
            text-decoration: none;
            transition: all 0.3s ease;
            border: 2px solid transparent;
        }

        .social-icons a:hover {
            background-color: var(--color-accent-primary);
            color: var(--color-text-primary);
            transform: translateY(-5px);
            border-color: var(--color-accent-primary);
            box-shadow: 0 10px 20px rgba(139, 0, 0, 0.3);
        }

        .copyright {
            margin-top: 50px;
            font-size: 0.95rem;
            color: var(--color-text-tertiary) !important;
            border-top: 1px solid var(--color-border-primary);
            padding-top: 30px;
        }

        /* ================================================================= */
        /* LIGHTBOX */
        /* ================================================================= */
        .lightbox {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: var(--color-overlay-dark);
            display: none;
            align-items: center;
            justify-content: center;
            z-index: 2000;
            opacity: 0;
            transition: opacity 0.4s ease;
            backdrop-filter: blur(10px);
        }

        .lightbox.active {
            display: flex;
            opacity: 1;
        }

        .lightbox-content {
            position: relative;
            max-width: 90%;
            max-height: 90vh;
            background-color: var(--color-bg-primary);
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 30px 80px rgba(0, 0, 0, 0.8);
            animation: lightboxAppear 0.5s cubic-bezier(0.4, 0, 0.2, 1) forwards;
        }

        @keyframes lightboxAppear {
            from {
                opacity: 0;
                transform: scale(0.9) translateY(30px);
            }
            to {
                opacity: 1;
                transform: scale(1) translateY(0);
            }
        }

        .lightbox-content img {
            max-width: 100%;
            max-height: 80vh;
            object-fit: contain;
            display: block;
        }

        .lightbox-close,
        .lightbox-prev,
        .lightbox-next {
            position: absolute;
            background-color: rgba(26, 26, 26, 0.9);
            color: var(--color-text-primary);
            border: none;
            width: 60px;
            height: 60px;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            font-size: 1.8rem;
            transition: all 0.3s ease;
            border-radius: 50%;
            z-index: 2001;
        }

        .lightbox-close:hover,
        .lightbox-prev:hover,
        .lightbox-next:hover {
            background-color: var(--color-accent-primary);
            transform: scale(1.1);
        }

        .lightbox-close {
            top: 20px;
            right: 20px;
        }

        .lightbox-prev {
            left: 20px;
            top: 50%;
            transform: translateY(-50%);
        }

        .lightbox-next {
            right: 20px;
            top: 50%;
            transform: translateY(-50%);
        }

        .lightbox-caption {
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100%;
            padding: 20px;
            background-color: rgba(10, 10, 10, 0.9);
            color: var(--color-text-primary);
            text-align: center;
            font-size: 1.1rem;
        }

        /* ================================================================= */
        /* RESPONSIVE STYLES */
        /* ================================================================= */
        @media (max-width: 1200px) {
            .container {
                max-width: 1140px;
            }
            
            .about-grid {
                gap: 60px;
            }
            
            .gallery-grid {
                gap: 20px;
            }
        }

        @media (max-width: 992px) {
            .container {
                max-width: 960px;
            }
            
            .about-grid {
                grid-template-columns: 1fr;
                gap: 60px;
            }
            
            .about-text {
                padding-right: 0;
                order: 2;
            }
            
            .about-image {
                order: 1;
            }
            
            .image-wrapper {
                max-height: 500px;
            }
            
            .gallery-grid {
                grid-template-columns: repeat(2, 1fr);
            }
            
            .nav-links {
                gap: 30px;
            }
            
            .hero-title {
                font-size: clamp(3rem, 9vw, 4.5rem);
            }
            
            .pricing-card {
                padding: 40px 50px;
            }
        }

        @media (max-width: 768px) {
            .container {
                max-width: 720px;
            }
            
            .section {
                padding: 80px 0;
            }
            
            .section-lg {
                padding: 100px 0;
            }
            
            .nav-links {
                position: fixed;
                top: 80px;
                left: -100%;
                width: 100%;
                height: calc(100vh - 80px);
                background-color: var(--color-bg-primary);
                flex-direction: column;
                align-items: center;
                justify-content: flex-start;
                padding-top: 60px;
                transition: left 0.5s cubic-bezier(0.4, 0, 0.2, 1);
                gap: 40px;
                z-index: 999;
                border-top: 1px solid var(--color-border-primary);
            }
            
            .nav-links.active {
                left: 0;
            }
            
            .mobile-menu-btn {
                display: flex;
            }
            
            .hero {
                padding-top: 100px;
                min-height: 90vh;
            }
            
            .hero-title {
                font-size: clamp(2.8rem, 10vw, 4rem);
                letter-spacing: 4px;
            }
            
            .hero-buttons {
                flex-direction: column;
                align-items: center;
                gap: 20px;
            }
            
            .hero-buttons .btn {
                width: 100%;
                max-width: 300px;
            }
            
            .about-stats {
                grid-template-columns: 1fr;
            }
            
            .gallery-grid {
                grid-template-columns: 1fr;
                max-width: 500px;
                margin-left: auto;
                margin-right: auto;
            }
            
            .pricing-card {
                padding: 30px;
            }
            
            .booking-form {
                padding: 30px;
            }
            
            .form-progress {
                flex-direction: column;
                gap: 40px;
                align-items: center;
                margin: 40px 0 30px;
            }
            
            .form-progress::before {
                display: none;
            }
            
            .progress-step {
                width: 100%;
            }
            
            .form-buttons {
                flex-direction: column;
            }
            
            .form-buttons .btn {
                width: 100%;
            }
            
            .footer-links {
                flex-direction: column;
                gap: 25px;
            }
            
            .lightbox-prev,
            .lightbox-next {
                width: 50px;
                height: 50px;
                font-size: 1.5rem;
            }
            
            .lightbox-close {
                top: 10px;
                right: 10px;
                width: 50px;
                height: 50px;
                font-size: 1.5rem;
            }
        }

        @media (max-width: 576px) {
            .container {
                padding: 0 16px;
            }
            
            .hero-title {
                font-size: clamp(2.5rem, 12vw, 3.5rem);
                letter-spacing: 3px;
            }
            
            .hero-subtitle {
                font-size: 1.2rem;
                letter-spacing: 2px;
            }
            
            .section-title h2,
            .section-title-center,
            .section-title-left {
                font-size: 2.2rem;
            }
            
            .about-text p {
                font-size: 1.05rem;
            }
            
            .pricing-card {
                padding: 25px 20px;
            }
            
            .price {
                font-size: 2.8rem;
            }
            
            .booking-form {
                padding: 25px 20px;
            }
            
            .form-step h3 {
                font-size: 1.8rem;
            }
            
            .file-upload-area {
                padding: 30px 20px;
            }
            
            .footer {
                padding: 50px 0 30px;
            }
        }

        @media (max-width: 400px) {
            .hero-title {
                font-size: 2.2rem;
            }
            
            .hero-buttons .btn {
                padding: 14px 24px;
                font-size: 0.95rem;
            }
            
            .logo {
                font-size: 1.6rem;
            }
            
            .section-title h2 {
                font-size: 1.8rem;
            }
        }

        /* ================================================================= */
        /* UTILITY CLASSES */
        /* ================================================================= */
        .mb-0 { margin-bottom: 0 !important; }
        .mb-10 { margin-bottom: 10px !important; }
        .mb-20 { margin-bottom: 20px !important; }
        .mb-30 { margin-bottom: 30px !important; }
        .mb-40 { margin-bottom: 40px !important; }
        .mb-50 { margin-bottom: 50px !important; }
        .mt-0 { margin-top: 0 !important; }
        .mt-10 { margin-top: 10px !important; }
        .mt-20 { margin-top: 20px !important; }
        .mt-30 { margin-top: 30px !important; }
        .mt-40 { margin-top: 40px !important; }
        .mt-50 { margin-top: 50px !important; }
        .py-0 { padding-top: 0 !important; padding-bottom: 0 !important; }
        .py-20 { padding-top: 20px !important; padding-bottom: 20px !important; }
        .py-40 { padding-top: 40px !important; padding-bottom: 40px !important; }
        .py-60 { padding-top: 60px !important; padding-bottom: 60px !important; }
        .px-0 { padding-left: 0 !important; padding-right: 0 !important; }
        .px-20 { padding-left: 20px !important; padding-right: 20px !important; }
        .px-40 { padding-left: 40px !important; padding-right: 40px !important; }
        .hidden { display: none !important; }
        .visible { display: block !important; }
        .flex { display: flex; }
        .flex-column { flex-direction: column; }
        .flex-row { flex-direction: row; }
        .align-center { align-items: center; }
        .justify-center { justify-content: center; }
        .justify-between { justify-content: space-between; }
        .gap-10 { gap: 10px; }
        .gap-20 { gap: 20px; }
        .gap-30 { gap: 30px; }
        .w-100 { width: 100%; }
        .h-100 { height: 100%; }
        .rounded { border-radius: 8px; }
        .rounded-sm { border-radius: 4px; }
        .rounded-lg { border-radius: 12px; }
        .shadow { box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3); }
        .shadow-lg { box-shadow: 0 20px 50px rgba(0, 0, 0, 0.4); }
        .overlay-dark { background-color: var(--color-overlay-dark); }
        .overlay-red { background-color: var(--color-overlay-red); }
        .border { border: 1px solid var(--color-border-primary); }
        .border-accent { border: 2px solid var(--color-accent-primary); }
        .bg-primary { background-color: var(--color-bg-primary); }
        .bg-secondary { background-color: var(--color-bg-secondary); }
        .bg-tertiary { background-color: var(--color-bg-tertiary); }
        .text-primary { color: var(--color-text-primary); }
        .text-secondary { color: var(--color-text-secondary); }
        .text-tertiary { color: var(--color-text-tertiary); }

        /* Scrollbar Styling */
        ::-webkit-scrollbar {
            width: 12px;
        }

        ::-webkit-scrollbar-track {
            background-color: var(--color-bg-secondary);
        }

        ::-webkit-scrollbar-thumb {
            background-color: var(--color-accent-primary);
            border-radius: 6px;
            border: 3px solid var(--color-bg-secondary);
        }

        ::-webkit-scrollbar-thumb:hover {
            background-color: var(--color-accent-secondary);
        }

        /* Selection Styling */
        ::selection {
            background-color: var(--color-accent-primary);
            color: var(--color-text-primary);
        }

        /* Focus Styling for Accessibility */
        :focus-visible {
            outline: 3px solid var(--color-accent-primary);
            outline-offset: 2px;
        }
    </style>
</head>
<body>
    <!-- PAGE 1 - HOME / PORTFOLIO -->
    <div class="page" id="home-page">
        <!-- HEADER -->
        <header class="header">
            <div class="container">
                <nav class="navbar">
                    <a href="#home-page" class="logo">BENNIE WARD</a>
                    <ul class="nav-links">
                        <li><a href="#home-page" class="active">Home</a></li>
                        <li><a href="#gallery-section">Work</a></li>
                        <li><a href="#booking-page">Book</a></li>
                    </ul>
                    <button class="mobile-menu-btn">
                        <i class="fas fa-bars"></i>
                    </button>
                </nav>
            </div>
        </header>

        <!-- HERO SECTION -->
        <section class="hero">
            <div class="hero-content">
                <h1 class="hero-title">BENNIE WARD</h1>
                <div class="hero-subtitle">Tattoo & Piercing Artist</div>
                <div class="hero-divider"></div>
                <p class="hero-text">15+ Years of Professional Tattoo Experience<br>Specializing in Custom Designs & Cover-Ups</p>
                <div class="hero-buttons">
                    <a href="#booking-page" class="btn btn-solid btn-large">Book Appointment</a>
                    <a href="#gallery-section" class="btn btn-outline btn-large">View Portfolio</a>
                </div>
            </div>
        </section>

        <!-- ABOUT ME -->
        <section class="about section">
            <div class="container">
                <div class="about-grid">
                    <div class="about-text">
                        <div class="section-title">
                            <span class="accent-line"></span>
                            <h2>About Bennie</h2>
                        </div>
                        <p class="text-large">With over 15 years of professional tattooing experience, I specialize in creating custom designs that tell your unique story. My approach blends traditional techniques with modern artistry to ensure each piece is both timeless and personal.</p>
                        <p>I believe a tattoo should be more than just ink on skin—it should be a meaningful expression of identity, memory, or aspiration. That's why I work closely with every client to understand their vision and bring it to life with precision and care.</p>
                        <p><strong class="text-primary">Specialties:</strong> Black & Grey, Traditional, Neo-Traditional, Cover-Ups, Fine Line, Geometric</p>
                        <p><strong class="text-primary">Studio:</strong> Private, clean, and professional environment with state-of-the-art equipment and strict hygiene protocols.</p>
                        
                        <div class="about-stats">
                            <div class="stat-item">
                                <div class="stat-number">15+</div>
                                <div class="stat-label">Years Experience</div>
                            </div>
                            <div class="stat-item">
                                <div class="stat-number">2000+</div>
                                <div class="stat-label">Tattoos Completed</div>
                            </div>
                            <div class="stat-item">
                                <div class="stat-number">100%</div>
                                <div class="stat-label">Sterile Equipment</div>
                            </div>
                            <div class="stat-item">
                                <div class="stat-number">500+</div>
                                <div class="stat-label">Cover-Ups</div>
                            </div>
                        </div>
                    </div>
                    <div class="about-image">
                        <div class="image-wrapper">
                            <!-- ABOUT ME IMAGE - YOUR IMAGE -->
                            <img src="https://www.dropbox.com/scl/fi/r4tucphzuppmbzb7zb3kz/IMG_7399.jpeg?rlkey=o8fgqfdm6gpdnqasq2rwnfv40&st=ptz5qhy3&raw=1" alt="Bennie Ward - Professional Tattoo Artist" class="artist-img">
                            <div class="image-grain"></div>
                            <div class="image-border"></div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- GALLERY -->
        <section class="gallery section" id="gallery-section">
            <div class="container">
                <h2 class="section-title-center">Portfolio Gallery</h2>
                <p class="text-center text-secondary mb-50" style="max-width: 700px; margin-left: auto; margin-right: auto;">A selection of recent work showcasing various styles and techniques. Click on any image to view it in full size.</p>
                
                <div class="gallery-grid">
                    <!-- GALLERY IMAGES - YOUR TATTOO WORK -->
                    <div class="gallery-item">
                        <img src="https://www.dropbox.com/scl/fi/v1pq335v1mi0mv8qhzpeg/IMG_7397.jpeg?rlkey=g21ksk3u6athp0qqot5x8o88c&st=co2ch8d9&raw=1" alt="Tattoo Work - Custom Design">
                        <div class="gallery-overlay">
                            <i class="fas fa-search-plus"></i>
                        </div>
                    </div>
                    <div class="gallery-item">
                        <img src="https://www.dropbox.com/scl/fi/exsn43ghzpjhhdpicfmf2/IMG_7396.jpeg?rlkey=2uu9xz2j9x8gg1528pilgyud9&st=fffxdb0f&raw=1" alt="Tattoo Work - Black & Grey">
                        <div class="gallery-overlay">
                            <i class="fas fa-search-plus"></i>
                        </div>
                    </div>
                    <div class="gallery-item">
                        <img src="https://www.dropbox.com/scl/fi/zabrcgj1yzoqx4bkoi7m9/IMG_7393.jpeg?rlkey=9gmc0tzwjxgh10sr1bi529xo4&st=7pzl1300&raw=1" alt="Tattoo Work - Traditional Style">
                        <div class="gallery-overlay">
                            <i class="fas fa-search-plus"></i>
                        </div>
                    </div>
                    <div class="gallery-item">
                        <img src="https://www.dropbox.com/scl/fi/cdncb6ygzun4n0qs78ldk/IMG_7391.jpeg?rlkey=isnv06zwkwpqr0x5bcjqi28qe&st=14fd50tc&raw=1" alt="Tattoo Work - Cover Up">
                        <div class="gallery-overlay">
                            <i class="fas fa-search-plus"></i>
                        </div>
                    </div>
                    <div class="gallery-item">
                        <img src="https://www.dropbox.com/scl/fi/jvzt1q1jugt881vrxlwn5/IMG_7390.jpeg?rlkey=2t3anpd63q3dttq3a7i7fzro6&st=faww5shg&raw=1" alt="Tattoo Work - Detailed Artwork">
                        <div class="gallery-overlay">
                            <i class="fas fa-search-plus"></i>
                        </div>
                    </div>
                    <div class="gallery-item">
                        <img src="https://www.dropbox.com/scl/fi/fbwtydzyvo5fzixwcqzgt/IMG_7398.jpeg?rlkey=qoyxpe5vg1co4vtabg5bz4jze&st=c08knc3q&raw=1" alt="Tattoo Work - Fine Line">
                        <div class="gallery-overlay">
                            <i class="fas fa-search-plus"></i>
                        </div>
                    </div>
                </div>
                
                <div class="gallery-load-more">
                    <a href="#booking-page" class="btn btn-outline btn-icon">
                        <i class="fas fa-images"></i> View More & Book Consultation
                    </a>
                </div>
            </div>
        </section>

        <!-- PRICING SNAPSHOT -->
        <section class="pricing section">
            <div class="container">
                <div class="pricing-card">
                    <h3>Pricing & Minimums</h3>
                    <div class="pricing-item">
                        <p class="price">$200</p>
                        <p class="price-desc">Tattoo Minimum</p>
                        <p class="text-tertiary">Small tattoos, simple designs, finger/hand pieces</p>
                    </div>
                    <div class="pricing-item">
                        <p class="price">$250</p>
                        <p class="price-desc">Cover-Up Minimum</p>
                        <p class="text-tertiary">Due to additional complexity and design work required</p>
                    </div>
                    <div class="pricing-item">
                        <p class="price">$100/hr</p>
                        <p class="price-desc">Hourly Rate (after minimum)</p>
                        <p class="text-tertiary">For larger pieces, sleeves, and detailed work</p>
                    </div>
                    <div class="pricing-note">
                        <p><i class="fas fa-exclamation-circle"></i> <strong>Important:</strong> All deposits are NON-REFUNDABLE and go toward the final price of your tattoo. Deposits secure your appointment time and cover the custom design process.</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- BOOK NOW CTA -->
        <section class="cta section-lg">
            <div class="container">
                <h2>Ready to Start Your Tattoo Journey?</h2>
                <p class="text-center text-secondary mb-40" style="max-width: 700px; margin-left: auto; margin-right: auto;">Book a consultation to discuss your ideas, get a custom design, and schedule your appointment. I'm here to help bring your vision to life.</p>
                <div class="cta-buttons">
                    <a href="#booking-page" class="btn btn-solid btn-large">Book Appointment Now</a>
                    <a href="tel:+15551234567" class="btn btn-outline btn-large btn-icon">
                        <i class="fas fa-phone"></i> Call: (555) 123-4567
                    </a>
                </div>
            </div>
        </section>
    </div>

    <!-- PAGE 2 - BOOKING & POLICIES -->
    <div class="page" id="booking-page">
        <!-- BOOKING SECTION -->
        <section class="booking section">
            <div class="container">
                <h2 class="section-title-center">Book Your Appointment</h2>
                <p class="booking-subtitle">Please fill out this form completely. The more information you provide, the better I can prepare for our consultation and design process. All information is confidential and used solely for booking purposes.</p>
                
                <form id="booking-form" class="booking-form">
                    <!-- Form Steps -->
                    <div class="form-step active" id="step-1">
                        <h3><span class="text-accent">Step 1:</span> Personal Information</h3>
                        <div class="form-group">
                            <label for="name">Full Name *</label>
                            <input type="text" id="name" name="name" required placeholder="Your full name">
                            <div class="error-message hidden" id="name-error">
                                <i class="fas fa-exclamation-circle"></i> Please enter your full name
                            </div>
                        </div>
                        <div class="form-group">
                            <label for="email">Email Address *</label>
                            <input type="email" id="email" name="email" required placeholder="you@example.com">
                            <div class="error-message hidden" id="email-error">
                                <i class="fas fa-exclamation-circle"></i> Please enter a valid email address
                            </div>
                        </div>
                        <div class="form-group">
                            <label for="phone">Phone Number *</label>
                            <input type="tel" id="phone" name="phone" required placeholder="(555) 123-4567">
                            <div class="error-message hidden" id="phone-error">
                                <i class="fas fa-exclamation-circle"></i> Please enter a valid phone number
                            </div>
                        </div>
                        <div class="form-group">
                            <label for="age">Are you 18 years of age or older? *</label>
                            <select id="age" name="age" required>
                                <option value="">Select an option</option>
                                <option value="yes">Yes, I am 18 or older</option>
                                <option value="no">No, I am under 18</option>
                            </select>
                            <div class="error-message hidden" id="age-error">
                                <i class="fas fa-exclamation-circle"></i> You must be 18+ to get a tattoo
                            </div>
                        </div>
                        <div class="form-buttons">
                            <button type="button" class="btn btn-outline next-step" data-next="2">Next Step <i class="fas fa-arrow-right"></i></button>
                        </div>
                    </div>
                    
                    <div class="form-step" id="step-2">
                        <h3><span class="text-accent">Step 2:</span> Tattoo Details</h3>
                        <div class="form-group">
                            <label for="idea">Tattoo Idea / Description *</label>
                            <textarea id="idea" name="idea" rows="5" required placeholder="Describe what you want in detail. Include any specific elements, symbols, meanings, style preferences, colors, etc. The more detail, the better!"></textarea>
                            <div class="error-message hidden" id="idea-error">
                                <i class="fas fa-exclamation-circle"></i> Please describe your tattoo idea
                            </div>
                        </div>
                        <div class="form-group">
                            <label for="size">Approximate Size *</label>
                            <select id="size" name="size" required>
                                <option value="">Select approximate size</option>
                                <option value="small">Small (under 3 inches - simple designs)</option>
                                <option value="medium">Medium (3-6 inches - most common)</option>
                                <option value="large">Large (6-10 inches - detailed work)</option>
                                <option value="xlarge">Extra Large (10+ inches - back pieces, large coverage)</option>
                                <option value="sleeve">Full Sleeve / Large Multi-Session Piece</option>
                            </select>
                            <div class="error-message hidden" id="size-error">
                                <i class="fas fa-exclamation-circle"></i> Please select a size estimate
                            </div>
                        </div>
                        <div class="form-group">
                            <label for="placement">Placement on Body *</label>
                            <input type="text" id="placement" name="placement" required placeholder="e.g., left forearm, right calf, upper back, chest, rib cage, etc.">
                            <div class="error-message hidden" id="placement-error">
                                <i class="fas fa-exclamation-circle"></i> Please specify placement
                            </div>
                        </div>
                        <div class="form-group">
                            <label for="style">Preferred Style *</label>
                            <select id="style" name="style" required>
                                <option value="">Select preferred style</option>
                                <option value="traditional">Traditional (American)</option>
                                <option value="neo-traditional">Neo-Traditional</option>
                                <option value="black-grey">Black & Grey (Realism)</option>
                                <option value="geometric">Geometric / Dotwork</option>
                                <option value="japanese">Japanese / Irezumi</option>
                                <option value="fine-line">Fine Line</option>
                                <option value="watercolor">Watercolor</option>
                                <option value="lettering">Lettering / Script</option>
                                <option value="not-sure">Not sure / Need guidance</option>
                            </select>
                            <div class="error-message hidden" id="style-error">
                                <i class="fas fa-exclamation-circle"></i> Please select a style preference
                            </div>
                        </div>
                        <div class="form-buttons">
                            <button type="button" class="btn btn-outline prev-step" data-prev="1"><i class="fas fa-arrow-left"></i> Previous</button>
                            <button type="button" class="btn btn-outline next-step" data-next="3">Next Step <i class="fas fa-arrow-right"></i></button>
                        </div>
                    </div>
                    
                    <div class="form-step" id="step-3">
                        <h3><span class="text-accent">Step 3:</span> Reference & Scheduling</h3>
                        <div class="form-group">
                            <label for="reference">Reference Images (Optional - Maximum 3)</label>
                            <div class="file-upload-area" id="file-upload-area">
                                <i class="fas fa-cloud-upload-alt"></i>
                                <p>Drag & drop your reference images here or <span class="browse">browse files</span></p>
                                <p class="file-info">Maximum 3 images • 5MB each • JPG, PNG, or PDF format</p>
                                <input type="file" id="reference" name="reference" accept="image/*,.pdf" multiple>
                                <div class="file-preview" id="file-preview"></div>
                            </div>
                            <div class="error-message hidden" id="file-error">
                                <i class="fas fa-exclamation-circle"></i> Maximum 3 files allowed
                            </div>
                        </div>
                        <div class="form-group">
                            <label for="date">Preferred Date *</label>
                            <input type="date" id="date" name="date" required min="">
                            <!-- DATE WARNING ADDED HERE -->
                            <div class="date-warning">
                                <i class="fas fa-exclamation-triangle"></i>
                                <span>Date and time may not be available. You'll receive confirmation after submission.</span>
                            </div>
                            <div class="error-message hidden" id="date-error">
                                <i class="fas fa-exclamation-circle"></i> Please select a future date
                            </div>
                        </div>
                        <div class="form-group">
                            <label for="time">Preferred Time of Day *</label>
                            <select id="time" name="time" required>
                                <option value="">Select time preference</option>
                                <option value="morning">Morning (10am - 12pm)</option>
                                <option value="afternoon">Afternoon (12pm - 4pm)</option>
                                <option value="evening">Evening (4pm - 7pm)</option>
                                <option value="flexible">Flexible / Any time available</option>
                            </select>
                            <div class="error-message hidden" id="time-error">
                                <i class="fas fa-exclamation-circle"></i> Please select a time preference
                            </div>
                        </div>
                        <div class="form-group">
                            <label for="budget">Budget Range *</label>
                            <select id="budget" name="budget" required>
                                <option value="">Select your budget range</option>
                                <option value="200-400">$200 - $400 (Minimum - Small piece)</option>
                                <option value="400-800">$400 - $800 (Medium piece)</option>
                                <option value="800-1500">$800 - $1,500 (Large detailed piece)</option>
                                <option value="1500-3000">$1,500 - $3,000 (Large multi-session)</option>
                                <option value="3000+">$3,000+ (Full sleeve / large coverage)</option>
                                <option value="unsure">Not sure / Need a quote</option>
                            </select>
                            <div class="error-message hidden" id="budget-error">
                                <i class="fas fa-exclamation-circle"></i> Please select a budget range
                            </div>
                        </div>
                        <div class="form-group">
                            <label for="notes">Additional Notes or Questions</label>
                            <textarea id="notes" name="notes" rows="4" placeholder="Any additional information, concerns, or questions you have..."></textarea>
                        </div>
                        <div class="form-buttons">
                            <button type="button" class="btn btn-outline prev-step" data-prev="2"><i class="fas fa-arrow-left"></i> Previous</button>
                            <button type="submit" class="btn btn-solid">Submit Booking Request <i class="fas fa-paper-plane"></i></button>
                        </div>
                    </div>
                    
                    <!-- Form Success Message -->
                    <div class="form-success" id="form-success">
                        <div class="success-icon">
                            <i class="fas fa-check-circle"></i>
                        </div>
                        <h3>Booking Request Submitted!</h3>
                        <p>Thank you for your booking request. I've received your information and will review your tattoo idea. I'll contact you within 1-2 business days to discuss your design, provide a quote, and confirm your appointment time.</p>
                        <p><strong>Note:</strong> The date and time you selected are not guaranteed until confirmed. You'll receive a confirmation email or call once your appointment is scheduled.</p>
                        <p>In the meantime, feel free to browse the portfolio gallery for more inspiration.</p>
                        <a href="#home-page" class="btn btn-outline mt-30">Return to Homepage</a>
                    </div>
                    
                    <!-- Progress Bar -->
                    <div class="form-progress">
                        <div class="progress-step active" data-step="1">
                            <div class="step-circle"></div>
                            <p>Personal Info</p>
                        </div>
                        <div class="progress-step" data-step="2">
                            <div class="step-circle"></div>
                            <p>Tattoo Details</p>
                        </div>
                        <div class="progress-step" data-step="3">
                            <div class="step-circle"></div>
                            <p>Scheduling</p>
                        </div>
                    </div>
                </form>
            </div>
        </section>

        <!-- POLICIES & RULES -->
        <section class="policies section">
            <div class="container">
                <h2 class="section-title-left">Studio Policies</h2>
                <p class="text-secondary mb-50" style="font-size: 1.2rem;">Please read and understand these policies before booking your appointment. These ensure a smooth process for both artist and client.</p>
                
                <div class="policies-list">
                    <div class="policy-item">
                        <div class="policy-bullet"></div>
                        <p><strong>$200 minimum</strong> for all tattoos, regardless of size or simplicity. This covers setup time, materials, and basic design work.</p>
                    </div>
                    <div class="policy-item">
                        <div class="policy-bullet"></div>
                        <p><strong>$250 cover-up minimum</strong> due to additional complexity, design challenges, and extra time required to work over existing tattoos.</p>
                    </div>
                    <div class="policy-item">
                        <div class="policy-bullet"></div>
                        <p><strong>Deposits are NON-REFUNDABLE</strong> and go toward the final price of your tattoo. Deposits secure your appointment time and cover the custom design process.</p>
                    </div>
                    <div class="policy-item">
                        <div class="policy-bullet"></div>
                        <p><strong>18+ with valid government-issued photo ID required</strong> (no exceptions). We will check and photocopy your ID for our records.</p>
                    </div>
                    <div class="policy-item">
                        <div class="policy-bullet"></div>
                        <p><strong>No call / no show = deposit forfeited</strong>. A new deposit will be required to reschedule. We understand emergencies happen—just communicate with us.</p>
                    </div>
                    <div class="policy-item">
                        <div class="policy-bullet"></div>
                        <p><strong>48-hour notice required</strong> for rescheduling or cancellation to keep your deposit. Less than 48 hours = deposit lost.</p>
                    </div>
                    <div class="policy-item">
                        <div class="policy-bullet"></div>
                        <p><strong>Designs are finalized day of appointment</strong>. Minor adjustments are expected, but major changes may require rescheduling and additional deposit.</p>
                    </div>
                    <div class="policy-item">
                        <div class="policy-bullet"></div>
                        <p><strong>No friends/guests during appointment</strong> (except for one companion for emotional support). This ensures a focused, professional environment.</p>
                    </div>
                    <div class="policy-item">
                        <div class="policy-bullet"></div>
                        <p><strong>No intoxication</strong>. If you arrive under the influence of drugs or alcohol, your appointment will be canceled and deposit forfeited.</p>
                    </div>
                    <div class="policy-item">
                        <div class="policy-bullet"></div>
                        <p><strong>Proper hygiene expected</strong>. Please arrive clean and prepared for your tattoo. The area to be tattooed should be shaved (if needed) and clean.</p>
                    </div>
                    <div class="policy-item">
                        <div class="policy-bullet"></div>
                        <p><strong>Payment in full at end of session</strong>. We accept cash, credit/debit cards, and digital payments. No checks.</p>
                    </div>
                    <div class="policy-item">
                        <div class="policy-bullet"></div>
                        <p><strong>Aftercare instructions must be followed</strong> for proper healing. We provide detailed aftercare guidelines and are available for healing questions.</p>
                    </div>
                </div>
                
                <div class="mt-50 text-center">
                    <a href="#booking-page" class="btn btn-solid btn-large">I Understand & Ready to Book</a>
                </div>
            </div>
        </section>

        <!-- FOOTER -->
        <footer class="footer">
            <div class="container">
                <div class="footer-content">
                    <h3>Bennie Ward</h3>
                    <p>Professional Tattoo & Piercing Artist</p>
                    
                    <div class="footer-links">
                        <a href="#home-page">Home</a>
                        <a href="#gallery-section">Portfolio</a>
                        <a href="#booking-page">Booking</a>
                        <a href="#policies">Policies</a>
                        <a href="tel:+15551234567">Contact</a>
                    </div>
                    
                    <div class="social-icons">
                        <a href="https://instagram.com" target="_blank" aria-label="Instagram">
                            <i class="fab fa-instagram"></i>
                        </a>
                        <a href="https://facebook.com" target="_blank" aria-label="Facebook">
                            <i class="fab fa-facebook-f"></i>
                        </a>
                        <a href="https://twitter.com" target="_blank" aria-label="Twitter">
                            <i class="fab fa-twitter"></i>
                        </a>
                        <a href="https://tiktok.com" target="_blank" aria-label="TikTok">
                            <i class="fab fa-tiktok"></i>
                        </a>
                    </div>
                    
                    <div class="contact-info">
                        <p class="text-secondary mb-10"><i class="fas fa-map-marker-alt text-accent"></i> 123 Ink Street, Art District, City, State 12345</p>
                        <p class="text-secondary mb-10"><i class="fas fa-phone text-accent"></i> <a href="tel:+15551234567" class="text-secondary">(555) 123-4567</a></p>
                        <p class="text-secondary"><i class="fas fa-envelope text-accent"></i> <a href="mailto:bennie@tattooartist.com" class="text-secondary">bennie@tattooartist.com</a></p>
                    </div>
                    
                    <p class="copyright">© <span id="current-year"></span> Bennie Ward Tattoo. All rights reserved. | Professional tattoo services for 15+ years.</p>
                </div>
            </div>
        </footer>
    </div>

    <!-- LIGHTBOX MODAL -->
    <div class="lightbox" id="lightbox">
        <div class="lightbox-content">
            <button class="lightbox-close" id="lightbox-close">
                <i class="fas fa-times"></i>
            </button>
            <button class="lightbox-prev" id="lightbox-prev">
                <i class="fas fa-chevron-left"></i>
            </button>
            <button class="lightbox-next" id="lightbox-next">
                <i class="fas fa-chevron-right"></i>
            </button>
            <img id="lightbox-img" src="" alt="Tattoo work">
            <div class="lightbox-caption" id="lightbox-caption"></div>
        </div>
    </div>

    <script>
        // =================================================================
        // DOM CONTENT LOADED
        // =================================================================
        document.addEventListener('DOMContentLoaded', function() {
            console.log('Bennie Ward Tattoo Website Loaded');
            
            // Set current year in footer
            document.getElementById('current-year').textContent = new Date().getFullYear();
            
            // =================================================================
            // HEADER SCROLL EFFECT
            // =================================================================
            const header = document.querySelector('.header');
            window.addEventListener('scroll', function() {
                if (window.scrollY > 50) {
                    header.classList.add('scrolled');
                } else {
                    header.classList.remove('scrolled');
                }
            });
            
            // =================================================================
            // MOBILE MENU TOGGLE
            // =================================================================
            const mobileMenuBtn = document.querySelector('.mobile-menu-btn');
            const navLinks = document.querySelector('.nav-links');
            const navLinksItems = document.querySelectorAll('.nav-links a');
            
            if (mobileMenuBtn) {
                mobileMenuBtn.addEventListener('click', function() {
                    navLinks.classList.toggle('active');
                    const icon = mobileMenuBtn.querySelector('i');
                    if (navLinks.classList.contains('active')) {
                        icon.classList.remove('fa-bars');
                        icon.classList.add('fa-times');
                        document.body.style.overflow = 'hidden';
                    } else {
                        icon.classList.remove('fa-times');
                        icon.classList.add('fa-bars');
                        document.body.style.overflow = 'auto';
                    }
                });
            }
            
            // Close mobile menu when clicking a link
            navLinksItems.forEach(link => {
                link.addEventListener('click', () => {
                    navLinks.classList.remove('active');
                    if (mobileMenuBtn) {
                        const icon = mobileMenuBtn.querySelector('i');
                        icon.classList.remove('fa-times');
                        icon.classList.add('fa-bars');
                        document.body.style.overflow = 'auto';
                    }
                });
            });
            
            // =================================================================
            // SET MINIMUM DATE FOR BOOKING FORM (TOMORROW)
            // =================================================================
            const dateInput = document.getElementById('date');
            if (dateInput) {
                const tomorrow = new Date();
                tomorrow.setDate(tomorrow.getDate() + 1);
                dateInput.min = tomorrow.toISOString().split('T')[0];
                
                // Set default to 2 weeks from now
                const twoWeeks = new Date();
                twoWeeks.setDate(twoWeeks.getDate() + 14);
                dateInput.value = twoWeeks.toISOString().split('T')[0];
            }
            
            // =================================================================
            // MULTI-STEP FORM FUNCTIONALITY
            // =================================================================
            const formSteps = document.querySelectorAll('.form-step');
            const nextButtons = document.querySelectorAll('.next-step');
            const prevButtons = document.querySelectorAll('.prev-step');
            const progressSteps = document.querySelectorAll('.progress-step');
            const bookingForm = document.getElementById('booking-form');
            const formSuccess = document.getElementById('form-success');
            let currentStep = 1;
            const totalSteps = 3;
            
            // Initialize form
            updateFormSteps();
            updateProgressSteps();
            
            // Next button functionality
            nextButtons.forEach(button => {
                button.addEventListener('click', function() {
                    const nextStep = parseInt(this.getAttribute('data-next'));
                    
                    // Validate current step before proceeding
                    if (validateStep(currentStep)) {
                        currentStep = nextStep;
                        updateFormSteps();
                        updateProgressSteps();
                        scrollToFormTop();
                    }
                });
            });
            
            // Previous button functionality
            prevButtons.forEach(button => {
                button.addEventListener('click', function() {
                    const prevStep = parseInt(this.getAttribute('data-prev'));
                    currentStep = prevStep;
                    updateFormSteps();
                    updateProgressSteps();
                    scrollToFormTop();
                });
            });
            
            // Form submission
            if (bookingForm) {
                bookingForm.addEventListener('submit', function(e) {
                    e.preventDefault();
                    
                    // Validate final step
                    if (validateStep(currentStep)) {
                        // If all steps valid, show success message
                        document.querySelectorAll('.form-step').forEach(step => {
                            step.style.display = 'none';
                        });
                        formSuccess.classList.add('active');
                        
                        // In a real implementation, you would send form data to a server here
                        console.log('Form submitted successfully!');
                        console.log('Form data:', getFormData());
                        
                        // Reset form after 5 seconds (for demo)
                        setTimeout(() => {
                            // Reset form
                            bookingForm.reset();
                            currentStep = 1;
                            updateFormSteps();
                            updateProgressSteps();
                            formSuccess.classList.remove('active');
                            clearFilePreview();
                        }, 5000);
                    }
                });
            }
            
            // Update form steps visibility
            function updateFormSteps() {
                formSteps.forEach(step => {
                    step.classList.remove('active');
                });
                
                const currentFormStep = document.getElementById(`step-${currentStep}`);
                if (currentFormStep) {
                    currentFormStep.classList.add('active');
                }
            }
            
            // Update progress steps
            function updateProgressSteps() {
                progressSteps.forEach((step, index) => {
                    const stepNumber = index + 1;
                    
                    step.classList.remove('active', 'completed');
                    
                    if (stepNumber < currentStep) {
                        step.classList.add('completed');
                    } else if (stepNumber === currentStep) {
                        step.classList.add('active');
                    }
                });
            }
            
            // Scroll to top of form
            function scrollToFormTop() {
                const form = document.querySelector('.booking-form');
                if (form) {
                    form.scrollIntoView({ behavior: 'smooth', block: 'start' });
                }
            }
            
            // Validate form step
            function validateStep(stepNumber) {
                let isValid = true;
                
                // Clear previous error messages
                document.querySelectorAll('.error-message').forEach(error => {
                    error.classList.add('hidden');
                });
                
                document.querySelectorAll('.form-group').forEach(group => {
                    group.classList.remove('error');
                });
                
                // Step 1 validation
                if (stepNumber === 1) {
                    const name = document.getElementById('name');
                    const email = document.getElementById('email');
                    const phone = document.getElementById('phone');
                    const age = document.getElementById('age');
                    
                    if (!name.value.trim()) {
                        showError(name, 'name-error');
                        isValid = false;
                    }
                    
                    if (!validateEmail(email.value)) {
                        showError(email, 'email-error');
                        isValid = false;
                    }
                    
                    if (!validatePhone(phone.value)) {
                        showError(phone, 'phone-error');
                        isValid = false;
                    }
                    
                    if (age.value !== 'yes') {
                        showError(age, 'age-error');
                        isValid = false;
                    }
                }
                
                // Step 2 validation
                if (stepNumber === 2) {
                    const idea = document.getElementById('idea');
                    const size = document.getElementById('size');
                    const placement = document.getElementById('placement');
                    const style = document.getElementById('style');
                    
                    if (!idea.value.trim()) {
                        showError(idea, 'idea-error');
                        isValid = false;
                    }
                    
                    if (!size.value) {
                        showError(size, 'size-error');
                        isValid = false;
                    }
                    
                    if (!placement.value.trim()) {
                        showError(placement, 'placement-error');
                        isValid = false;
                    }
                    
                    if (!style.value) {
                        showError(style, 'style-error');
                        isValid = false;
                    }
                }
                
                // Step 3 validation
                if (stepNumber === 3) {
                    const date = document.getElementById('date');
                    const time = document.getElementById('time');
                    const budget = document.getElementById('budget');
                    
                    if (!date.value) {
                        showError(date, 'date-error');
                        isValid = false;
                    } else {
                        const selectedDate = new Date(date.value);
                        const today = new Date();
                        today.setHours(0, 0, 0, 0);
                        
                        if (selectedDate <= today) {
                            showError(date, 'date-error');
                            isValid = false;
                        }
                    }
                    
                    if (!time.value) {
                        showError(time, 'time-error');
                        isValid = false;
                    }
                    
                    if (!budget.value) {
                        showError(budget, 'budget-error');
                        isValid = false;
                    }
                }
                
                return isValid;
            }
            
            // Show error message
            function showError(inputElement, errorId) {
                inputElement.parentElement.classList.add('error');
                const errorElement = document.getElementById(errorId);
                if (errorElement) {
                    errorElement.classList.remove('hidden');
                }
                inputElement.focus();
            }
            
            // Email validation
            function validateEmail(email) {
                const re = /^(([^<>()\[\]\\.,;:\s@"]+(\.[^<>()\[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/;
                return re.test(String(email).toLowerCase());
            }
            
            // Phone validation (basic)
            function validatePhone(phone) {
                const re = /^[\+]?[1-9][\d]{0,15}$/;
                const digits = phone.replace(/\D/g, '');
                return re.test(digits) && digits.length >= 10;
            }
            
            // Get all form data
            function getFormData() {
                const formData = {};
                const formElements = bookingForm.querySelectorAll('input, select, textarea');
                
                formElements.forEach(element => {
                    if (element.name && element.type !== 'file') {
                        formData[element.name] = element.value;
                    }
                });
                
                return formData;
            }
            
            // =================================================================
            // FILE UPLOAD FUNCTIONALITY
            // =================================================================
            const fileInput = document.getElementById('reference');
            const fileUploadArea = document.getElementById('file-upload-area');
            const filePreview = document.getElementById('file-preview');
            const maxFiles = 3;
            const maxFileSize = 5 * 1024 * 1024; // 5MB in bytes
            let uploadedFiles = [];
            
            if (fileInput && fileUploadArea) {
                // Click on upload area triggers file input
                fileUploadArea.addEventListener('click', function(e) {
                    if (e.target !== fileInput) {
                        fileInput.click();
                    }
                });
                
                // Drag and drop functionality
                ['dragenter', 'dragover', 'dragleave', 'drop'].forEach(eventName => {
                    fileUploadArea.addEventListener(eventName, preventDefaults, false);
                });
                
                function preventDefaults(e) {
                    e.preventDefault();
                    e.stopPropagation();
                }
                
                ['dragenter', 'dragover'].forEach(eventName => {
                    fileUploadArea.addEventListener(eventName, highlight, false);
                });
                
                ['dragleave', 'drop'].forEach(eventName => {
                    fileUploadArea.addEventListener(eventName, unhighlight, false);
                });
                
                function highlight() {
                    fileUploadArea.classList.add('dragover');
                }
                
                function unhighlight() {
                    fileUploadArea.classList.remove('dragover');
                }
                
                // Handle dropped files
                fileUploadArea.addEventListener('drop', handleDrop, false);
                
                function handleDrop(e) {
                    const dt = e.dataTransfer;
                    const files = dt.files;
                    handleFiles(files);
                }
                
                // Handle selected files
                fileInput.addEventListener('change', function() {
                    handleFiles(this.files);
                });
                
                // Process files
                function handleFiles(files) {
                    if (uploadedFiles.length + files.length > maxFiles) {
                        showFileError(`Maximum ${maxFiles} files allowed`);
                        return;
                    }
                    
                    for (let i = 0; i < files.length; i++) {
                        const file = files[i];
                        
                        // Check file size
                        if (file.size > maxFileSize) {
                            showFileError(`File "${file.name}" exceeds 5MB limit`);
                            continue;
                        }
                        
                        // Check file type
                        if (!file.type.match('image.*') && !file.name.toLowerCase().endsWith('.pdf')) {
                            showFileError(`File "${file.name}" must be an image or PDF`);
                            continue;
                        }
                        
                        // Add to uploaded files
                        uploadedFiles.push(file);
                        
                        // Create preview
                        createFilePreview(file);
                    }
                    
                    // Update file input
                    updateFileInput();
                    
                    // Clear file error if successful
                    clearFileError();
                }
                
                // Create file preview element
                function createFilePreview(file) {
                    const previewItem = document.createElement('div');
                    previewItem.className = 'file-preview-item';
                    
                    // Create unique ID for this file
                    const fileId = 'file-' + Date.now() + '-' + Math.random().toString(36).substr(2, 9);
                    
                    if (file.type.match('image.*')) {
                        const reader = new FileReader();
                        reader.onload = function(e) {
                            previewItem.innerHTML = `
                                <img src="${e.target.result}" alt="${file.name}">
                                <div class="file-preview-info">
                                    <div class="file-name">${file.name}</div>
                                    <div class="file-size">${formatFileSize(file.size)}</div>
                                </div>
                                <button type="button" class="remove-file" data-file-id="${fileId}">
                                    <i class="fas fa-times"></i>
                                </button>
                            `;
                            
                            // Add remove functionality
                            const removeBtn = previewItem.querySelector('.remove-file');
                            removeBtn.addEventListener('click', function() {
                                removeFile(fileId, file.name);
                            });
                        };
                        reader.readAsDataURL(file);
                    } else {
                        // PDF file
                        previewItem.innerHTML = `
                            <div style="width: 60px; height: 60px; background-color: var(--color-accent-primary); display: flex; align-items: center; justify-content: center; border-radius: 4px;">
                                <i class="fas fa-file-pdf" style="font-size: 2rem; color: white;"></i>
                            </div>
                            <div class="file-preview-info">
                                <div class="file-name">${file.name}</div>
                                <div class="file-size">${formatFileSize(file.size)}</div>
                            </div>
                            <button type="button" class="remove-file" data-file-id="${fileId}">
                                <i class="fas fa-times"></i>
                            </button>
                        `;
                        
                        // Add remove functionality
                        const removeBtn = previewItem.querySelector('.remove-file');
                        removeBtn.addEventListener('click', function() {
                            removeFile(fileId, file.name);
                        });
                    }
                    
                    filePreview.appendChild(previewItem);
                }
                
                // Remove file from uploads
                function removeFile(fileId, fileName) {
                    // Remove from uploadedFiles array
                    uploadedFiles = uploadedFiles.filter(file => file.name !== fileName);
                    
                    // Remove preview element
                    const previewItems = document.querySelectorAll('.file-preview-item');
                    previewItems.forEach(item => {
                        const removeBtn = item.querySelector('.remove-file');
                        if (removeBtn && removeBtn.getAttribute('data-file-id') === fileId) {
                            item.remove();
                        }
                    });
                    
                    // Update file input
                    updateFileInput();
                }
                
                // Update file input with remaining files
                function updateFileInput() {
                    // Since we can't directly set FileList, we'll store files in uploadedFiles array
                    // In a real implementation, you would use FormData to send files
                    console.log('Uploaded files:', uploadedFiles);
                }
                
                // Clear file preview
                function clearFilePreview() {
                    filePreview.innerHTML = '';
                    uploadedFiles = [];
                    fileInput.value = '';
                }
                
                // Show file error
                function showFileError(message) {
                    const fileError = document.getElementById('file-error');
                    if (fileError) {
                        fileError.innerHTML = `<i class="fas fa-exclamation-circle"></i> ${message}`;
                        fileError.classList.remove('hidden');
                    }
                }
                
                // Clear file error
                function clearFileError() {
                    const fileError = document.getElementById('file-error');
                    if (fileError) {
                        fileError.classList.add('hidden');
                    }
                }
                
                // Format file size
                function formatFileSize(bytes) {
                    if (bytes === 0) return '0 Bytes';
                    const k = 1024;
                    const sizes = ['Bytes', 'KB', 'MB', 'GB'];
                    const i = Math.floor(Math.log(bytes) / Math.log(k));
                    return parseFloat((bytes / Math.pow(k, i)).toFixed(2)) + ' ' + sizes[i];
                }
            }
            
            // =================================================================
            // GALLERY LIGHTBOX FUNCTIONALITY
            // =================================================================
            const lightbox = document.getElementById('lightbox');
            const lightboxImg = document.getElementById('lightbox-img');
            const lightboxCaption = document.getElementById('lightbox-caption');
            const lightboxClose = document.getElementById('lightbox-close');
            const lightboxPrev = document.getElementById('lightbox-prev');
            const lightboxNext = document.getElementById('lightbox-next');
            const galleryItems = document.querySelectorAll('.gallery-item');
            let currentImageIndex = 0;
            const galleryImages = [
                {
                    src: "https://www.dropbox.com/scl/fi/v1pq335v1mi0mv8qhzpeg/IMG_7397.jpeg?rlkey=g21ksk3u6athp0qqot5x8o88c&st=co2ch8d9&raw=1",
                    alt: "Tattoo Work - Custom Design"
                },
                {
                    src: "https://www.dropbox.com/scl/fi/exsn43ghzpjhhdpicfmf2/IMG_7396.jpeg?rlkey=2uu9xz2j9x8gg1528pilgyud9&st=fffxdb0f&raw=1",
                    alt: "Tattoo Work - Black & Grey"
                },
                {
                    src: "https://www.dropbox.com/scl/fi/zabrcgj1yzoqx4bkoi7m9/IMG_7393.jpeg?rlkey=9gmc0tzwjxgh10sr1bi529xo4&st=7pzl1300&raw=1",
                    alt: "Tattoo Work - Traditional Style"
                },
                {
                    src: "https://www.dropbox.com/scl/fi/cdncb6ygzun4n0qs78ldk/IMG_7391.jpeg?rlkey=isnv06zwkwpqr0x5bcjqi28qe&st=14fd50tc&raw=1",
                    alt: "Tattoo Work - Cover Up"
                },
                {
                    src: "https://www.dropbox.com/scl/fi/jvzt1q1jugt881vrxlwn5/IMG_7390.jpeg?rlkey=2t3anpd63q3dttq3a7i7fzro6&st=faww5shg&raw=1",
                    alt: "Tattoo Work - Detailed Artwork"
                },
                {
                    src: "https://www.dropbox.com/scl/fi/fbwtydzyvo5fzixwcqzgt/IMG_7398.jpeg?rlkey=qoyxpe5vg1co4vtabg5bz4jze&st=c08knc3q&raw=1",
                    alt: "Tattoo Work - Fine Line"
                }
            ];
            
            // Open lightbox when gallery item clicked
            galleryItems.forEach((item, index) => {
                item.addEventListener('click', function() {
                    currentImageIndex = index;
                    openLightbox();
                });
            });
            
            // Open lightbox
            function openLightbox() {
                if (galleryImages.length === 0) return;
                
                lightbox.classList.add('active');
                document.body.style.overflow = 'hidden';
                updateLightboxImage();
            }
            
            // Close lightbox
            function closeLightbox() {
                lightbox.classList.remove('active');
                document.body.style.overflow = 'auto';
            }
            
            // Update lightbox image
            function updateLightboxImage() {
                if (galleryImages.length === 0) return;
                
                const image = galleryImages[currentImageIndex];
                lightboxImg.src = image.src;
                lightboxImg.alt = image.alt;
                lightboxCaption.textContent = image.alt;
            }
            
            // Next image
            function nextImage() {
                if (galleryImages.length === 0) return;
                
                currentImageIndex = (currentImageIndex + 1) % galleryImages.length;
                updateLightboxImage();
            }
            
            // Previous image
            function prevImage() {
                if (galleryImages.length === 0) return;
                
                currentImageIndex = (currentImageIndex - 1 + galleryImages.length) % galleryImages.length;
                updateLightboxImage();
            }
            
            // Event listeners for lightbox controls
            if (lightboxClose) {
                lightboxClose.addEventListener('click', closeLightbox);
            }
            
            if (lightboxNext) {
                lightboxNext.addEventListener('click', nextImage);
            }
            
            if (lightboxPrev) {
                lightboxPrev.addEventListener('click', prevImage);
            }
            
            // Keyboard navigation
            document.addEventListener('keydown', function(e) {
                if (!lightbox.classList.contains('active')) return;
                
                switch (e.key) {
                    case 'Escape':
                        closeLightbox();
                        break;
                    case 'ArrowRight':
                        nextImage();
                        break;
                    case 'ArrowLeft':
                        prevImage();
                        break;
                }
            });
            
            // Close lightbox when clicking on background
            lightbox.addEventListener('click', function(e) {
                if (e.target === lightbox) {
                    closeLightbox();
                }
            });
            
            // =================================================================
            // SMOOTH SCROLL FOR ANCHOR LINKS
            // =================================================================
            document.querySelectorAll('a[href^="#"]').forEach(anchor => {
                anchor.addEventListener('click', function(e) {
                    const href = this.getAttribute('href');
                    
                    // Skip if it's just "#"
                    if (href === '#') return;
                    
                    e.preventDefault();
                    
                    const targetElement = document.querySelector(href);
                    if (targetElement) {
                        // Close mobile menu if open
                        if (navLinks.classList.contains('active')) {
                            navLinks.classList.remove('active');
                            if (mobileMenuBtn) {
                                const icon = mobileMenuBtn.querySelector('i');
                                icon.classList.remove('fa-times');
                                icon.classList.add('fa-bars');
                                document.body.style.overflow = 'auto';
                            }
                        }
                        
                        // Scroll to target
                        const headerHeight = document.querySelector('.header').offsetHeight;
                        const targetPosition = targetElement.getBoundingClientRect().top + window.pageYOffset - headerHeight;
                        
                        window.scrollTo({
                            top: targetPosition,
                            behavior: 'smooth'
                        });
                    }
                });
            });
            
            // =================================================================
            // ACTIVE NAV LINK ON SCROLL
            // =================================================================
            const sections = document.querySelectorAll('section, .page');
            const navLinksArray = document.querySelectorAll('.nav-links a');
            
            function updateActiveNavLink() {
                let current = '';
                const scrollPosition = window.scrollY + 100;
                
                sections.forEach(section => {
                    const sectionTop = section.offsetTop;
                    const sectionHeight = section.clientHeight;
                    const sectionId = section.getAttribute('id');
                    
                    if (scrollPosition >= sectionTop && scrollPosition < sectionTop + sectionHeight) {
                        current = sectionId;
                    }
                });
                
                navLinksArray.forEach(link => {
                    link.classList.remove('active');
                    const href = link.getAttribute('href');
                    if (href === `#${current}` || (current === '' && href === '#home-page')) {
                        link.classList.add('active');
                    }
                });
            }
            
            window.addEventListener('scroll', updateActiveNavLink);
            
            // =================================================================
            // FORM AUTO-SAVE TO LOCAL STORAGE (DEMO)
            // =================================================================
            const formAutoSaveKey = 'bennie-ward-booking-form';
            const formInputs = document.querySelectorAll('#booking-form input, #booking-form select, #booking-form textarea');
            
            // Load saved form data
            const savedFormData = localStorage.getItem(formAutoSaveKey);
            if (savedFormData) {
                try {
                    const formData = JSON.parse(savedFormData);
                    
                    formInputs.forEach(input => {
                        if (input.name && formData[input.name] !== undefined) {
                            input.value = formData[input.name];
                        }
                    });
                    
                    console.log('Form data loaded from local storage');
                } catch (e) {
                    console.error('Error loading form data:', e);
                }
            }
            
            // Save form data on input change
            formInputs.forEach(input => {
                input.addEventListener('input', saveFormData);
                input.addEventListener('change', saveFormData);
            });
            
            function saveFormData() {
                const formData = {};
                
                formInputs.forEach(input => {
                    if (input.name && input.type !== 'file') {
                        formData[input.name] = input.value;
                    }
                });
                
                localStorage.setItem(formAutoSaveKey, JSON.stringify(formData));
            }
            
            // Clear saved form data on successful submission
            if (bookingForm) {
                bookingForm.addEventListener('submit', function() {
                    localStorage.removeItem(formAutoSaveKey);
                });
            }
            
            // =================================================================
            // PAGE TRANSITION EFFECTS
            // =================================================================
            // Add fade-in animation to sections on scroll
            const observerOptions = {
                threshold: 0.1,
                rootMargin: '0px 0px -100px 0px'
            };
            
            const observer = new IntersectionObserver(function(entries) {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.style.opacity = '1';
                        entry.target.style.transform = 'translateY(0)';
                    }
                });
            }, observerOptions);
            
            // Observe all sections
            document.querySelectorAll('section').forEach(section => {
                section.style.opacity = '0';
                section.style.transform = 'translateY(30px)';
                section.style.transition = 'opacity 0.8s ease, transform 0.8s ease';
                observer.observe(section);
            });
            
            // =================================================================
            // CONSOLE GREETING
            // =================================================================
            console.log('%c⚡ BENNIE WARD TATTOO ⚡', 'color: #8b0000; font-size: 18px; font-weight: bold;');
            console.log('%cProfessional Tattoo Artist Website', 'color: #cccccc; font-size: 14px;');
            console.log('%c15+ Years Experience | Custom Designs | Cover-Ups', 'color: #999999; font-size: 12px;');
        });
    </script>
</body>
</html>
