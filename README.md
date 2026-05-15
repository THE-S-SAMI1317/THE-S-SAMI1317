<style>
/* Add these animations to your CSS */

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

/* Online status pulse */
b:contains("ONLINE") {
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

table tr:nth-child(1) { animation-delay: 0.1s; }
table tr:nth-child(2) { animation-delay: 0.2s; }
table tr:nth-child(3) { animation-delay: 0.3s; }

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

ul li:nth-child(1) { animation-delay: 0.1s; }
ul li:nth-child(2) { animation-delay: 0.2s; }
ul li:nth-child(3) { animation-delay: 0.3s; }
ul li:nth-child(4) { animation-delay: 0.4s; }
ul li:nth-child(5) { animation-delay: 0.5s; }

/* Button/Link animations */
a[href*="#works"], a[href*="#contact"] {
    display: inline-block;
    padding: 10px 20px;
    background: linear-gradient(135deg, #6366f1, #8b5cf6);
    color: white;
    border-radius: 8px;
    text-decoration: none;
    animation: pulse-glow 3s ease-in-out infinite;
    transition: all 0.3s ease;
}

a[href*="#works"]:hover, a[href*="#contact"]:hover {
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

# Shahriar - Future-Ready Developer
## SAMI.DEV

[Home](#home) | [About](#about) | [Works](#works) | [Let's Talk](#contact)

[Home](#home) | [About](#about) | [Works](#works) | [Contact Me](#contact)

---


### Shahriar Sami

> CSE Student AIUB. Architecting efficient software solutions with a focus on clean code and scalable design.

[Explore Works](#works)

![Shahriar Sami Avatar](https://avatars.githubusercontent.com/u/153972636?s=400&u=f3213e855e19a82ac8cd4d1310d4123f21382879&v=4)

**ONLINE**

**Shahriar Sami** `<Developer />`

| ID | LOC | EXP |
|----|-----|-----|
| 25-63748-3 | Dhaka, BD | Level 1 |

---

## Decoding The Dev

### 1. INTRODUCTION

**Driven by Innovation, Powered by Code.**

I am a first-year Computer Science Engineering student at AIUB with a perfect 4.00 CGPA. My journey is defined by a relentless curiosity for how things work under the hood. From low-level Java logic to high-level web architecture, I aim to build systems that matter.

`Java Specialist` | `Problem Solver` | `Gamer`

- ![Location](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRVvqzn5ASPrIyuxcGJYva-IhP1EHrsas_5Yx6ZecgwpMrsHBth1mjopFiZn4vvFmt407m-&s) Dhaka, BD | Base of Operations

---

### 2. ACADEMIC DATABASE

**2024 - Present**  
B.Sc. in Computer Science Engineering  
American International University - Bangladesh (AIUB)  
[AIUB](https://www.aiub.edu/)  
![AIUB Logo](https://drive.google.com/thumbnail?id=13pGUL9xn3CG-Bi-xY06GB8cE4BLcdnpo&sz=w1000)  

**2022 - 2024**  
Higher Secondary Certificate (Science)  
Jhenaidah KC College  
**GPA 5.00 / 5.00**

**2021 - 2022**  
Secondary School Certificate (Science)  
Jhenaidha Govt. High School  
[JGHS](http://www.jhenidahghs.edu.bd/)  
![JGHS]  
**GPA 5.00 / 5.00 (Golden)**

---

### 3. TECH ARSENAL

| Java | Python | JS | HTML | CSS | C | SQL | Git |
|------|--------|----|------|-----|---|-----|-----|
| ![Java](https://img.shields.io/badge/Java-ED8B00?logo=java&logoColor=white) | ![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white) | ![JS](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black) | ![HTML](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white) | ![CSS](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white) | ![C](https://img.shields.io/badge/C-00599C?logo=c&logoColor=white) | ![SQL](https://img.shields.io/badge/MySQL-4479A1?logo=mysql&logoColor=white) | ![Git](https://img.shields.io/badge/Git-F05032?logo=git&logoColor=white) |

---

### 4. HOBBIES & INTERESTS

`Travelling` | `Gaming` | `Drawing` | `Photography`

---

## PROJECTS

### Selected Works

[View GitHub](https://github.com/THE-S-SAMI1317)

---

> ⚠️ **Work in Progress**  
> Something exciting is brewing in the lab. Check back soon for new deployments.

---

## SYSTEM ONLINE

### Initiate Connection

> Ready to start a new project? Send a transmission below.

#### 📡 SIGNAL STRENGTH
**Direct Neural Link**  
⚡ Fastest response within 2 hours.

#### 📬 Contact Details
- **Primary Mail**: [shahriar.sami@mail.com](mailto:shahriar.sami@mail.com)
- **Base Location**: Dhaka, Bangladesh

#### 🌐 Global Nodes
[![GitHub](https://img.shields.io/badge/GitHub-181717?logo=github&logoColor=white)](#) [![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?logo=linkedin&logoColor=white)](#) [![Instagram](https://img.shields.io/badge/Instagram-E4405F?logo=instagram&logoColor=white)](#) [![Facebook](https://img.shields.io/badge/Facebook-1877F2?logo=facebook&logoColor=white)](#)

#### 🕐 SERVER TIME (DHAKA)
`00:00:00` *(static representation - live clock requires JavaScript)*

> © 2025 SHAHRIAR SAMI. ALL RIGHTS RESERVED
