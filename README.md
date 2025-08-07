body {
    background: #101010;
    color: #ff3333;
    font-family: 'Courier New', Courier, monospace;
    margin: 0;
    padding: 0;
    height: 100vh;
    width: 100vw;
    overflow: hidden;
}

.hacked-screen {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    height: 100vh;
    width: 100vw;
    background: linear-gradient(135deg, #2d0000 0%, #1a1a1a 100%);
    text-align: center;
    animation: flickerBG 2s infinite alternate;
}

.hacked-screen h1 {
    font-size: 4rem;
    color: #ff0000;
    text-shadow: 0 0 20px #ff0000, 0 0 40px #ff3333;
    margin-bottom: 20px;
    animation: flicker 1s infinite alternate;
    letter-spacing: 2px;
}

.hacked-screen p {
    font-size: 1.5rem;
    background: #222;
    padding: 20px 40px;
    border-radius: 10px;
    box-shadow: 0 0 10px #ff333355;
    color: #ff8888;
    animation: typewriter 3s steps(40) 1s 1 normal both;
    border: 2px solid #ff2222;
}

/* Flicker effect for h1 */
@keyframes flicker {
    0%, 19%, 21%, 23%, 25%, 54%, 56%, 100% {
        opacity: 1;
        text-shadow: 0 0 20px #ff0000, 0 0 40px #ff3333;
    }
    20%, 22%, 24%, 55% {
        opacity: 0.5;
        text-shadow: none;
    }
}

/* Flicker background animation */
@keyframes flickerBG {
    0% {
        background: linear-gradient(135deg, #2d0000 0%, #1a1a1a 100%);
    }
    100% {
        background: linear-gradient(135deg, #1a1a1a 0%, #2d0000 100%);
    }
}

/* Typewriter effect for p */
@keyframes typewriter {
    from {
        width: 0;
        color: #222;
    }
    to {
        width: 100%;
        color: #ff8888;
    }
}

.hacked-screen p {
    overflow: hidden;
    white-space: nowrap;
    border-right: 3px solid #ff4444;
    width: 0;
    animation: typewriter 3s steps(40) 1s 1 normal both;
}
