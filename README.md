<style>
/* 1. Floating Animation for Avatar/Circle */
@keyframes float {
    0%, 100% {
        transform: translateY(0px);
    }
    50% {
        transform: translateY(-20px);
    }
}

/* 2. Pulse Glow Animation */
@keyframes pulse-glow {
    0%, 100% {
        box-shadow: 0 0 20px rgba(99, 102, 241, 0.5);
    }
    50% {
        box-shadow: 0 0 40px rgba(99, 102, 241, 0.8);
    }
}

/* 3. Gradient Background Animation */
@keyframes gradient-shift {
    0% {
        background-position: 0% 50%;
    }
    50% {
        background-position: 100% 50%;
    }
    100% {
        background-position: 0% 50%;
    }
}

/* 4. Fade In Up Animation */
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

/* 5. Scale In Animation */
@keyframes scaleIn {
    from {
        opacity: 0;
        transform: scale(0.8);
    }
    to {
        opacity: 1;
        transform: scale(1);
    }
}

/* Apply animations to elements */

/* Avatar floating effect */
img[alt="Shahriar Sami Avatar"] {
    animation: float 6s ease-in-out infinite;
    border-radius: 50%;
}

/* Online status pulse - FIXED: Use a class instead of :contains() */
.online-status {
    animation: pulse-glow 2s ease-in-out infinite;
}

/* Section animations */
h1, h2, h3 {
    animation: fadeInUp 0.8s ease-out;
}

/* Table rows stagger animation */
table tr {
    animation: fadeInUp 0.5s ease-out;
    animation-fill-mode: both;
}

table tr:nth-child(1) {
    animation-delay: 0.1s;
}

table tr:nth-child(2) {
    animation-delay: 0.2s;
}

table tr:nth-child(3) {
    animation-delay: 0.3s;
}

/* Badge/Tag animations */
img[src*="shields.io"] {
    animation: scaleIn 0.5s ease-out;
    transition: transform 0.3s ease;
}

img[src*="shields.io"]:hover {
    transform: scale(1.1) translateY(-5px);
}

/* Link hover animations */
a {
    transition: all 0.3s ease;
    position: relative;
}

a:hover {
    transform: translateY(-2px);
    text-shadow: 0 0 10px rgba(99, 102, 241, 0.5);
}

/* Gradient animated background for headers */
h1, h2 {
    background: linear-gradient(-45deg, #6366f1, #8b5cf6, #a855f7, #6366f1);
    background-size: 400% 400%;
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    animation: gradient-shift 15s ease infinite;
}

/* Smooth scroll behavior */
html {
    scroll-behavior: smooth;
}

/* Loading animation for images */
img {
    opacity: 0;
    animation: scaleIn 0.5s ease-out forwards;
}

/* Stagger animation for list items */
ul li, ol li {
    opacity: 0;
    animation: fadeInUp 0.5s ease-out forwards;
}

ul li:nth-child(1) {
    animation-delay: 0.1s;
}

ul li:nth-child(2) {
    animation-delay: 0.2s;
}

ul li:nth-child(3) {
    animation-delay: 0.3s;
}

ul li:nth-child(4) {
    animation-delay: 0.4s;
}

ul li:nth-child(5) {
    animation-delay: 0.5s;
}

/* Button/Link animations */
a[href*="#works"],
a[href*="#contact"] {
    display: inline-block;
    padding: 10px 20px;
    background: linear-gradient(135deg, #6366f1, #8b5cf6);
    color: white;
    border-radius: 8px;
    text-decoration: none;
    animation: pulse-glow 3s ease-in-out infinite;
    transition: all 0.3s ease;
}

a[href*="#works"]:hover,
a[href*="#contact"]:hover {
    transform: translateY(-3px) scale(1.05);
    box-shadow: 0 10px 30px rgba(99, 102, 241, 0.4);
}

/* Card hover effects */
section {
    transition: all 0.3s ease;
}

section:hover {
    transform: translateY(-5px);
    box-shadow: 0 10px 30px rgba(99, 102, 241, 0.2);
}
</style>
