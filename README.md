<style>
/* Animation Keyframes */
@keyframes float {
  0%, 100% { transform: translateY(0px) rotate(0deg); }
  50% { transform: translateY(-20px) rotate(2deg); }
}

@keyframes pulse-glow {
  0%, 100% { box-shadow: 0 0 20px rgba(99, 102, 241, 0.4); }
  50% { box-shadow: 0 0 40px rgba(99, 102, 241, 0.7); }
}

@keyframes gradient-shift {
  0% { background-position: 0% 50%; }
  50% { background-position: 100% 50%; }
  100% { background-position: 0% 50%; }
}

@keyframes fadeInUp {
  from { opacity: 0; transform: translateY(30px); }
  to { opacity: 1; transform: translateY(0); }
}

@keyframes scaleIn {
  from { opacity: 0; transform: scale(0.85); }
  to { opacity: 1; transform: scale(1); }
}

@keyframes slideInLeft {
  from { opacity: 0; transform: translateX(-30px); }
  to { opacity: 1; transform: translateX(0); }
}

@keyframes slideInRight {
  from { opacity: 0; transform: translateX(30px); }
  to { opacity: 1; transform: translateX(0); }
}

@keyframes typing {
  from { width: 0; }
  to { width: 100%; }
}

@keyframes blink {
  50% { border-color: transparent; }
}

@keyframes blob-bounce {
  0%, 100% { transform: translate(0, 0) scale(1); }
  25% { transform: translate(10px, -10px) scale(1.05); }
  50% { transform: translate(-5px, 15px) scale(0.95); }
  75% { transform: translate(15px, 5px) scale(1.02); }
}

/* Global Styles */
* {
  transition: all 0.3s ease;
}

html {
  scroll-behavior: smooth;
}

/* Header Animations */
h1, h2 {
  background: linear-gradient(-45deg, #6366f1, #8b5cf6, #a855f7, #6366f1);
  background-size: 400% 400%;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  animation: gradient-shift 15s ease infinite;
}

h1 {
  animation: fadeInUp 0.8s ease-out, gradient-shift 15s ease infinite;
}

h2 {
  animation: fadeInUp 0.8s ease-out 0.2s both, gradient-shift 15s ease infinite;
}

h3 {
  animation: fadeInUp 0.8s ease-out 0.3s both;
}

/* Avatar Animation */
img[alt="Shahriar Sami Avatar"] {
  animation: float 6s ease-in-out infinite;
  border-radius: 50%;
  box-shadow: 0 10px 40px rgba(99, 102, 241, 0.3);
}

/* Online Status */
b:contains("ONLINE"), strong:contains("ONLINE") {
  animation: pulse-glow 2s ease-in-out infinite;
  display: inline-block;
  padding: 5px 15px;
  border-radius: 20px;
  background: rgba(99, 102, 241, 0.1);
}

/* Table Animations */
table {
  animation: scaleIn 0.6s ease-out;
}

table tr {
  animation: fadeInUp 0.5s ease-out both;
}

table tr:nth-child(1) { animation-delay: 0.1s; }
table tr:nth-child(2) { animation-delay: 0.2s; }
table tr:nth-child(3) { animation-delay: 0.3s; }

/* Badge/Tag Animations */
img[src*="shields.io"] {
  animation: scaleIn 0.5s ease-out both;
  transition: transform 0.3s ease, filter 0.3s ease;
  filter: drop-shadow(0 4px 6px rgba(0,0,0,0.1));
}

img[src*="shields.io"]:hover {
  transform: scale(1.15) translateY(-5px);
  filter: drop-shadow(0 10px 20px rgba(99, 102, 241, 0.3)) brightness(1.1);
}

/* Stagger badge animations */
img[src*="shields.io"]:nth-child(1) { animation-delay: 0.1s; }
img[src*="shields.io"]:nth-child(2) { animation-delay: 0.2s; }
img[src*="shields.io"]:nth-child(3) { animation-delay: 0.3s; }
img[src*="shields.io"]:nth-child(4) { animation-delay: 0.4s; }
img[src*="shields.io"]:nth-child(5) { animation-delay: 0.5s; }
img[src*="shields.io"]:nth-child(6) { animation-delay: 0.6s; }
img[src*="shields.io"]:nth-child(7) { animation-delay: 0.7s; }
img[src*="shields.io"]:nth-child(8) { animation-delay: 0.8s; }

/* Link Animations */
a {
  position: relative;
  display: inline-block;
  transition: all 0.3s ease;
}

a:hover {
  transform: translateY(-3px);
  text-shadow: 0 0 10px rgba(99, 102, 241, 0.5);
}

a[href*="#works"], a[href*="#contact"] {
  padding: 10px 20px;
  background: linear-gradient(135deg, #6366f1, #8b5cf6);
  color: white !important;
  border-radius: 8px;
  text-decoration: none !important;
  animation: pulse-glow 3s ease-in-out infinite;
  box-shadow: 0 4px 15px rgba(99, 102, 241, 0.3);
}

a[href*="#works"]:hover, a[href*="#contact"]:hover {
  transform: translateY(-5px) scale(1.05);
  box-shadow: 0 10px 30px rgba(99, 102, 241, 0.5);
}

/* Section Animations */
section, hr + * {
  animation: fadeInUp 0.8s ease-out both;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

section:hover {
  transform: translateY(-5px);
}

/* List Item Animations */
ul li, ol li {
  opacity: 0;
  animation: slideInLeft 0.5s ease-out forwards;
  transition: all 0.3s ease;
}

ul li:nth-child(1) { animation-delay: 0.1s; }
ul li:nth-child(2) { animation-delay: 0.2s; }
ul li:nth-child(3) { animation-delay: 0.3s; }
ul li:nth-child(4) { animation-delay: 0.4s; }
ul li:nth-child(5) { animation-delay: 0.5s; }

ul li:hover {
  transform: translateX(10px);
  color: #6366f1;
}

/* Code/Tag Animations */
code, strong {
  animation: scaleIn 0.4s ease-out both;
  transition: all 0.3s ease;
}

code:hover, strong:hover {
  transform: scale(1.05);
  background: rgba(99, 102, 241, 0.1);
}

/* Image Animations */
img {
  opacity: 0;
  animation: scaleIn 0.6s ease-out forwards;
  transition: transform 0.3s ease, filter 0.3s ease;
}

img:hover {
  transform: scale(1.05);
  filter: brightness(1.1);
}

/* Blockquote Animation */
blockquote {
  border-left: 4px solid #6366f1;
  animation: slideInLeft 0.8s ease-out;
  transition: all 0.3s ease;
  position: relative;
  overflow: hidden;
}

blockquote::before {
  content: '';
  position: absolute;
  top: 0;
  left: -100%;
  width: 100%;
  height: 100%;
  background: linear-gradient(90deg, transparent, rgba(99, 102, 241, 0.1), transparent);
  animation: shimmer 3s infinite;
}

@keyframes shimmer {
  0% { left: -100%; }
  100% { left: 100%; }
}

blockquote:hover {
  transform: translateX(10px);
  border-left-color: #8b5cf6;
  box-shadow: 5px 0 20px rgba(99, 102, 241, 0.2);
}

/* Horizontal Rule Animation */
hr {
  border: none;
  height: 2px;
  background: linear-gradient(90deg, transparent, #6366f1, transparent);
  animation: slideInRight 1s ease-out;
  position: relative;
  overflow: hidden;
}

hr::after {
  content: '';
  position: absolute;
  top: 0;
  left: -100%;
  width: 100%;
  height: 100%;
  background: linear-gradient(90deg, transparent, #a855f7, transparent);
  animation: shimmer 2s infinite;
}

/* Navigation Links */
p a[href^="#"] {
  padding: 5px 10px;
  margin: 0 5px;
  border-radius: 5px;
  transition: all 0.3s ease;
}

p a[href^="#"]:hover {
  background: rgba(99, 102, 241, 0.1);
  transform: translateY(-2px);
}

/* Card-like Elements */
div, section {
  transition: all 0.3s ease;
}

/* Special hover effect for project cards */
h3:has(+ blockquote), h3:has(+ p) {
  cursor: pointer;
}

h3:has(+ blockquote):hover, h3:has(+ p):hover {
  color: #6366f1;
  transform: translateX(5px);
}

/* Emoji animations */
emoji, span:contains("📡"), span:contains("⚡"), span:contains("📬"), span:contains("🌐"), span:contains("🕐") {
  animation: float 3s ease-in-out infinite;
  display: inline-block;
}

/* Loading animation for all elements */
* {
  animation-duration: 0.5s;
  animation-fill-mode: both;
}

/* Responsive animation reduction */
@media (prefers-reduced-motion: reduce) {
  * {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
  }
}
</style>

# Shahriar - Future-Ready Developer
## SAMI.DEV

[Home](#home) | [About](#about) | [Works](#works) | [Let's Talk](#contact)

[Home](#home) | [About](#about) | [Works](#works) | [Contact Me](#contact)

---

> System Online

### Shahriar Sami

> CSE Student @ AIUB. Architecting efficient software solutions with a focus on clean code and scalable design.

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

- **4.00** Current CGPA
- ![Location](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRVvqzn5ASPrIyuxcGJYva-IhP1EHrsas_5Yx6ZecgwpMrsHBth1mjopFiZn4vvFmt407m-&s) Dhaka, BD | Base of Operations

---

### 2. ACADEMIC DATABASE

**2024 - Present**  
B.Sc. in Computer Science Engineering  
American International University - Bangladesh (AIUB)  
[AIUB](https://www.aiub.edu/)  
![AIUB Logo](https://drive.google.com/thumbnail?id=13pGUL9xn3CG-Bi-xY06GB8cE4BLcdnpo&sz=w1000)  
**CGPA 4.00 / 4.00**

**2022 - 2024**  
Higher Secondary Certificate (Science)  
Jhenaidah KC College  
**GPA 5.00 / 5.00**

**2021 - 2022**  
Secondary School Certificate (Science)  
Jhenaidha Govt. High School  
[JGHS](http://www.jhenidahghs.edu.bd/)  
![JGHS](data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wCEAAkGBxMTEhUTExMVFhUXGR8aGBgYGBofGBgaHSAYGiAeGxsaHSggHR0lHRkfITEhJSkrLi4uGx8zODMsNygtLi0BCgoKDg0OGxAQGy0lICUtLS0vLy0tLS0tLS8tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLf/AABEIAKoBKQMBIgACEQEDEQH/xAAbAAACAwEBAQAAAAAAAAAAAAADBAIFBgEAB//EAEcQAAECBAQCCAQDBgQFAgcAAAECEQADITEEEkFRBWEGEyIycYGRoUKxwfBS0fEUI2JykuEVU4LSM0NjosKy4gcWJERUc5P/xAAZAQADAQEBAAAAAAAAAAAAAAABAgMABAX/xAAtEQACAgICAQIFAwQDAAAAAAAAAQIRAyESMVEEQRMiYYHwcaGxMpHB0RRS8f/aAAwDAQACEQMRAD8AocHMUGGQlw4F81wGHtSGlTUF0qH8wLUVXcN9iFJmKKSwWo0o4LJH8OhsKja0BQpz2lE8zUn6wON9nBKJdSuHS6KTQPs4IAYg+Iq3nvBp80A9nRi471C4ZrM/m0IYbEVKtGqBdqDl4w9MVnTmubjdtS/I/XWOeOFQld2T5O9n0HovxFM6SkOorSkZioAE3DirsGZzF0BHznorxCVJXmmBdAapcpFCXKQKFn/vp9AGOlOEmYkFQBAJahLC+r0a8WjFXs61K0MRMCOFQFyA9A+p28YnF9IBxo7HWjoEYBxo80SAiQEYxBo80EaOgRjUDyxxoK0eaMGgTRxoKRESIwCDREpjmJnpQMyiwcCxNTQWiqxXSWQiYqUesKk3yoJAqB46xroDLJUuIFMRkY4TJPXIClBiQGqWcN6jnFHxLpGpCT+76uYxIEw0IB5XJA7rg2dnDtzElEvCmF14qWFiWVpCyHCSQCRWwN7RildK8TRRKGagSmhoavfnQ/lFTJxswzEzeypZLOp7ggjMxBP9ze0D43hErRuOkmOEuUUBQExYAA1Yu58GBjGzlBKSdhDEyYVsokkkkrJLur+HloNISxIK1hA3q9uT8nvyBjSdnTijSIYNLJKi+aYco5OwPsoDZiuGMNwgdatGYpQlaytRuEJUXPM2A5kQCet1uHKZdE6V38WJJ5qPle8b/dqmS0kOuYVrI2clCPIHMeahtCPor7lVjsT1iypgkWSkWSkUCR4D3eKniGJyjnpD2IWEh4p0yjNU5dicqfGFQwvhk63Ufbn4xo8BhUSJfXzQ70Qj8av9o1PlyiGA4WmUtUyb/wAOWADupRqEp3OvIVio4vxBeJmGrIT2SzsALIRy3OtRd2wOxTiOMmYhecqdOYVdgs5mYbIGwv4d6E4uSBYl/WPYg9lhYV86GCTmqdL/AFHsW8oARYmn39j5CAT/AIQ9Wr5kkeTLFYOqpbw+l/SF5gdW7kAUqT2Wpu2kAKL/AKCTmnrT+KWT5go9u0Y3OWKPoZ0aXIJnTqKKWEvaxJWbZqWFvONdHRCLrZz5Jrlo+WcKwoxCsiiyywCiVVAYMwBqwAD0qdgI7i5aJS1ykqzdodvs5Wbk9QTUg6W0gEjEpUMqwA/xVbXvJdiC9aXbnB1JyhsoIIuDTxDUr5+URaaYJ9dHkKantbz9IfwM45gO6BT9T5e0eT1cpIK5edwFKTmSG7rb07wL2oXojQKVcjSr05kXLQF8xGUSwkJdVHGgPtX2h2dNzrl5lVQe+QCWcM9HLOqn8UIy5zBhteCk0FPP7tBcLAm0W3F+NzZyckwpUEzAtKcrUGYd25FdY0nRjpGZkwSV2Y5VLI6xRB10OzCr3jFJVUHXn92hrB4jIvrcqVF9R2XcVIHPyrCtOLseOTdM+sZY6ExkuKdLylEsy0pKj3w4NQ/ZpYEt2vSLPotxVWIE1SlJLLZISD2U3AcgE+PKKKborou2jsdj0ME9HoBjcWmUgzFkhKalgSfQRTz+lkgVTmUAWV2Vpy7O6WrYO1W3gNpBov4Di8SmWgrUaDYOT4AVJ5RTDpZIIBAW+YJKWGZLgl1B6Cny3EZfjPG04ooKpRGUlkhQUsK3CQQGIN2uA+kK5pAbS7L0dLErmJKJkoSnGYLcTG1YeYIu7c4jxPpcLYcOXYlYPllrY3c+kYaauqgEEUcijgOWA8AfOOBVr+fOkT5SkiMsj6Q9xbia5q+smGoDJCSwSK2D7nUwl1qmUnOoBVTUsbd4C9hfaCYcyyCZgBo/xAvXsk6OLGvO8AKQDYM1GrWli1SHG4Z+UFLyTpvtjaMfMQnqhMWlALgAlgXenzgHEcWuaorKnL3tXe7C3tA8Jh1KqEFQHMgBy5Hj5ecNcKSC5SB3mZgwYB+1dzdhaGQYxt0Onsoc0+lPbwhOWnLL6z/mTXCQdE2f5h9s8HxxzqCBY1PgOX3rDEzBiYmWpAJUoqSkPsQkD2qd3MMdXQLhMkB5hYpllwD8cw1D+brPINrEZyrklyak7k3hqchKWQhsqXdQ+NR7y/NgBySmKbiWIPcTc/KEY6EsUvrF5fhFSfv79Is+E4IE9Yrsy5bF/CwG6i1tYHwzh+Y5RRKe0tRsALk8oDxziOcdVK7MtANdQW7x/jUNPhH/cDMW6QcZVPmZUgpSO7slBOh1JaquXhCCmoBRI0/P1jT9IsEjrkhKQE9UGAsAHpGXmBn8WgtUBMjNFDzgc9Rod9OTkf+N9I5NN92+jfTzh3gXApuJYJogd+YodmwoBqad0HWphew3XYlhMNMmrCJacyjoLMXqTomzk8o+hdG+i6MMy1MudbNokGjIBt43LmztFlwjhErDiyxUtmUe8sjVR8zSwcw+SBU0EWjCtshLI3pEGjmWFcZjAlJUpQloGpLP97CsZ/8Ax7Cc/wChX5QXOgLG2Y+dw4pqmvKIycQpFPVKqpPkaRZ4biCF07p2P0No7j8KCk0rF54Vx5Rdonjz3NQkqbBdYmawZKTWgDVOxDA6MI9iZRplSXAqAPa+lrDcwvMwKkWqINIxvwqGYD+oeB18D7RyvHx6KySl0G4cM5YvY1Dmtra1agg8sFyl7Vrt4G9dBEcMsDOt3DAP/Z6X/WPTCnK4A3oT7NqfS8NP5Un5/wB0c6dzaf5oYkh6uSx9/pZ4ckzAHpzq3g1a6/bRW4Wb2kqXUEgl3Ljzqbw7iEBCmQvMg6kEbXBHPnEXJXTH46tE0kMzA1rvrrcQ3w3E9VMTMSR2S+Wva00B5RXhfK8N4QZqAC9S4fTQh7fSDKKSsRWmfRMFxuSUJzTQVN2jlUA/g3Z8DDSOKSS7TUU3UB84w02Ul7u1608nr986RQhNe83P+8MpFXoliveJpmKWeomGaiY6VATD+7Zj2clTqalr3oBksXgerUywWBZaQyFEt3glKi9WLGlAzvFnJUHoWIsQWPqCfzir4lMUVstRUc13PrWu3tyiWVUZ57XQqRTVzV6XuCW15itQIGjMjuk7g1Ym4al3847MJcgv+tR+cFSpak0BYd6via6+YhdRWyW+2DE5SyCouAQCVmlSWBPraGcZghlKkzQtQ74J7tHvV3HlTlRdSioEM4Y2D5QNtg+0TkTyEsDQGtn8bOd6k2hutjclXRBWFAAcVZyHpqGc6wYrKctTmsLUuzuPKBIUwLkvV3NK+BpACSd4HfZPdjskqAUl1AGpHwk1NksAW1iuVNVmDu4tufFtawZmPe2iM4jSvlURkknYLYrldWUHVvXb2peL7DyhKlhLu1Sdzd/dvKKmSBmGYkNW3Onjt5HlDmIndYQhJvU+Fz5RSLOjFRErISV2VMoncJ3fwf0UIt+Hry4ZFO0SsI/hQSAVeJYpH+qEJWETOCVAkJdYJ2QnqiTtmOYsdSoaGG8RNAcsEgCg0SkUA8hDtnQtiWOnhCYruG4ZUxeUAlavYefhBUJM1YU2rIG/OHOMYtMr91KYzFJAWdAzOKfCDfc0oASVGFuK45IbDSCDqVN3j+I/wg90G9/CknUGUWuSbnmT5wJeGUAe6fDTns0Sm4pSzkBDaWZI3FKN9ICZhCctTmsLUuzuPKBIUwLkvV3NK+BpACSd4HfZPdjskqAUl1AGpHwk1NksAW1iuVNVmDu4tufFtawZmPe2iM4jSvlURkknYLYrldWUHVvXb2peL7DyhKlhLu1Sdzd/dvKKmSBmGYkNW3Onjt5HlDmIndYQhJvU+Fz5RSLOjFRErISV2VMoncJ3fwf0UIt+Hry4ZFO0SsI/hQSAVeJYpH+qEJWETOCVAkJdYJ2QnqiTtmOYsdSoaGG8RNAcsEgCg0SkUA8hDtnQtiWOnhCYruG4ZUxeUAlavYefhBUJM1YU2rIG/OHOMYtMr91KYzFJAWdAzOKfCDfc0oASVGFuK45IbDSCDqVN3j+I/wg90G9/CknUGUWuSbnmT5wJeGUAe6fDTns0Sm4pSzkBDaWZI3FKN9ICZhCctTmsLUuzuPKBIUwLkvV3NK+BpACSd4HfZPdjskqAUl1AGpHwk1NksAW1iuVNVmDu4tufFtawZmPe2iM4jSvlURkknYLYrldWUHVvXb2peL7DyhKlhLu1Sdzd/dvKKmSBmGYkNW3Onjt5HlDmIndYQhJvU+Fz5RSLOjFRErISV2VMoncJ3fwf0UIt+Hry4ZFO0SsI/hQSAVeJYpH+qEJWETOCVAkJdYJ2QnqiTtmOYsdSoaGG8RNAcsEgCg0SkUA8hDtnQtiWOnhCYruG4ZUxeUAlavYefhBUJM1YU2rIG/OHOMYtMr91KYzFJAWdAzOKfCDfc0oASVGFuK45IbDSCDqVN3j+I/wg90G9/CknUGUWuSbnmT5wJeGUAe6fDTns0Sm4pSzkBDaWZI3FKN9ICZhCctTmsLUuzuPKBIUwLkvV3NK+BpACSd4HfZPdjskqAUl1AGpHwk1NksAW1iuVNVmDu4tufFtawZmPe2iM4jSvlURkknYLYrldWUHVvXb2peL7DyhKlhLu1Sdzd/dvKKmSBmGYkNW3Onjt5HlDmIndYQhJvU+Fz5RSLOjFRErISV2VMoncJ3fwf0UIt+Hry4ZFO0SsI/hQSAVeJYpH+qEJWETOCVAkJdYJ2QnqiTtmOYsdSoaGG8RNAcsEgCg0SkUA8hDtnQtiWOnhCYruG4ZUxeUAlavYefhBUJM1YU2rIG/OHOMYtMr91KYzFJAWdAzOKfCDfc0oASVGFuK45IbDSCDqVN3j+I/wg90G9/CknUGUWuSbnmT5wJeGUAe6fDTns0Sm4pSzkBDaWZI3FKN9ICZhCctTmsLUuzuPKBIUwLkvV3NK+BpACSd4HfZPdjskqAUl1AGpHwk1NksAW1iuVNVmDu4tufFtawZmPe2iM4jSvlURkknYLYrldWUHVvXb2peL7DyhKlhLu1Sdzd/dvKKmSBmGYkNW3Onjt5HlDmIndYQhJvU+Fz5RSLOjFRErISV2VMoncJ3fwf0UIt+Hry4ZFO0SsI/hQSAVeJYpH+qEJWETOCVAkJdYJ2QnqiTtmOYsdSoaGG8RNAcsEgCg0SkUA8hDtnQtiWOnhCYruG4ZUxeUAlavYefhBUJM1YU2rIG/OHOMYtMr91KYzFJAWdAzOKfCDfc0oASVGFuK45IbDSCDqVN3j+I/wg90G9/CknUGUWuSbnmT5wJeGUAe6fDTns0Sm4pSzkBDaWZI3FKN9ICZhCctTmsLUuzuPKBIUwLkvV3NK+BpACSd4HfZPdjskqAUl1AGpHwk1NksAW1iuVNVmDu4tufFtawZmPe2iM4jSvlURkknYLY...... [truncated for brevity]

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

### 🏥 Healthcare Center
> `JAVA SWING` `JSON`

A comprehensive desktop application designed to digitize healthcare operations, streamlining patient management and blood bank inventory.

[Case Study](#) | [GitHub](#)

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

---

### 📝 Contact Form

> ⚠️ *Note: Interactive forms don't work in GitHub README. Use the email link above or visit my portfolio website for the full interactive form.*

| Field | Options/Placeholder |
|-------|-------------------|
| **USER IDENTIFICATION** | Full Name |
| **COMM CHANNEL** | Email Address |
| **SUBJECT PARAMETER** | `New Project Proposal` \| `Hiring Collaboration` \| `Technical Consultation` \| `Just Saying Hi` |
| **DATA STREAM** | Describe your vision... |

[📤 TRANSMIT MESSAGE](mailto:shahriar.sami@mail.com?subject=New%20Project%20Proposal&body=Hello%20Shahriar%2C%0A%0A)

---

> © 2025 SHAHRIAR SAMI. ALL RIGHTS RESERVED
