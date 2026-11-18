// Typing animation
const typing = document.getElementById("typing");

const words = [
    "I Miss You So Much ❤️",
    "You Are Special To Me 🌸",
    "A Little World For SenSen 💗"
];

let wordIndex = 0;
let charIndex = 0;
let deleting = false;

function typeEffect() {
    const current = words[wordIndex];

    typing.textContent = current.substring(0, charIndex);

    if (!deleting) {
        charIndex++;

        if (charIndex > current.length) {
            deleting = true;
            setTimeout(typeEffect, 1500);
            return;
        }
    } else {
        charIndex--;

        if (charIndex < 0) {
            deleting = false;
            charIndex = 0;
            wordIndex = (wordIndex + 1) % words.length;
        }
    }

    setTimeout(typeEffect, deleting ? 45 : 90);
}

typeEffect();

// Floating hearts and flowers
const symbols = ["💗","💕","🌸","🌹","💖","✨","🌷"];

function createParticle() {
    const particle = document.createElement("div");

    particle.className = "sparkle";
    particle.textContent =
        symbols[Math.floor(Math.random() * symbols.length)];

    particle.style.left = Math.random() * 100 + "vw";
    particle.style.fontSize = (15 + Math.random() * 25) + "px";
    particle.style.animationDuration = (5 + Math.random() * 6) + "s";

    document.body.appendChild(particle);

    setTimeout(() => particle.remove(), 11000);
}

setInterval(createParticle, 400);

// Scroll
function scrollToStory() {
    document.getElementById("story").scrollIntoView({
        behavior: "smooth"
    });
}

// Love letter
function openLetter() {
    const letter = document.getElementById("hiddenLetter");

    if (letter.style.display === "block") {
        letter.style.display = "none";
    } else {
        letter.style.display = "block";
        letter.scrollIntoView({
            behavior: "smooth",
            block: "center"
        });
    }
}

// Music
const music = document.getElementById("music");
const musicButton = document.getElementById("musicButton");

async function toggleMusic() {
    if (music.paused) {
        try {
            await music.play();
            musicButton.textContent = "♫ Music ON";
        } catch (error) {
            musicButton.textContent = "♫ Add music.mp3";
        }
    } else {
        music.pause();
        musicButton.textContent = "♫ Music OFF";
    }
}