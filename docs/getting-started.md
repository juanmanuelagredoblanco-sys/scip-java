body {
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    background-color: #f0f0f0;
    margin: 0;
}

.envelope {
    position: relative;
    width: 300px;
    height: 200px;
    background-color: #fff;
    border-radius: 8px;
    box-shadow: 0 4px 8px rgba(0,0,0,0.1);
    cursor: pointer;
    transition: transform 0.5s ease;
}

.flap {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 50%;
    background-color: #e0e0e0;
    border-top-left-radius: 8px;
    border-top-right-radius: 8px;
    transform-origin: top;
    transition: transform 0.5s ease;
}

.letter {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    padding: 20px;
    box-sizing: border-box;
    text-align: center;
    opacity: 0;
    transition: opacity 0.5s ease;
}

.envelope.open .flap {
    transform: rotateX(180deg);
    z-index: 1;
}

.envelope.open .letter {
    opacity: 1;
    z-index: 2;
}
