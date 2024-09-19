<template>
    <div class="main">
        <div class="container">
             <div class="slider-wrapper">
                <button id="prev-slide" class="slider-button material-symbols-outlined">chevron_left</button>
                <div class="image-list">
                    <img src="https://cdn.britannica.com/49/94449-050-ECB0E7C2/Angkor-Wat-temple-complex-Camb.jpg" alt="img-1" class="image-item">
                    <img src="https://cdn.britannica.com/49/94449-050-ECB0E7C2/Angkor-Wat-temple-complex-Camb.jpg" alt="img-2" class="image-item">
                    <img src="https://cdn.britannica.com/49/94449-050-ECB0E7C2/Angkor-Wat-temple-complex-Camb.jpg" alt="img-3" class="image-item">
                    <img src="https://cdn.britannica.com/49/94449-050-ECB0E7C2/Angkor-Wat-temple-complex-Camb.jpg" alt="img-4" class="image-item">
                    <img src="https://cdn.britannica.com/49/94449-050-ECB0E7C2/Angkor-Wat-temple-complex-Camb.jpg" alt="img-5" class="image-item">
                    <img src="https://cdn.britannica.com/49/94449-050-ECB0E7C2/Angkor-Wat-temple-complex-Camb.jpg" alt="img-6" class="image-item">
                    <img src="https://cdn.britannica.com/49/94449-050-ECB0E7C2/Angkor-Wat-temple-complex-Camb.jpg" alt="img-7" class="image-item">
                    <img src="https://cdn.britannica.com/49/94449-050-ECB0E7C2/Angkor-Wat-temple-complex-Camb.jpg" alt="img-8" class="image-item">
                    <img src="https://cdn.britannica.com/49/94449-050-ECB0E7C2/Angkor-Wat-temple-complex-Camb.jpg" alt="img-9" class="image-item">
                    <img src="https://cdn.britannica.com/49/94449-050-ECB0E7C2/Angkor-Wat-temple-complex-Camb.jpg" alt="img-10" class="image-item">
                </div>
                <button id="next-slide" class="slider-button material-symbols-outlined">chevron_right</button>
             </div>
             <div class="slider-scrollbar">
                 <div class="scrollbar-track">
                     <div class="scrollbar-thumb"></div>
                 </div>
             </div>
        </div>
    </div>
</template>

<style scoped>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}
.main {
    display:flex;
    align-items:center;
    justify-content:center;
    min-height:100vh;
    background:teal;
}
.container {
    max-width: 1200px;
    width:95%;
}

.slider-wrapper .slider-button {
    position:absolute;
    outline:none;
    top:50%;
    border:none;
    height:50px;
    width:50px;
    color:#fff;
    background: #000;
    font-size:2.2rem;
    cursor: pointer;
    border-radius:50%;
    transform:translateY(-50%);
}
.slider-wrapper .slider-button#prev-slide {
    left:-20px;
}
.slider-wrapper .slider-button#next-slide {
    right:-20px;
}
.slider-wrapper .image-list {
    display:grid;
    gap:18px;
    font-size:0;
    overflow-x:auto;
    scrollbar-width:none;
    grid-template-columns:repeat(10, 1fr);
    margin-bottom:30px;
}
.slider-wrapper .image-list::-webkit-scrollbar {
    display:none;
}

.slider-wrapper .image-list .image-item{
    width:325px;
    height:400px;
    object-fit:cover;
}
.container .slider-scrollbar {
    height:24px;
    width:100%;
    display:flex;
    align-items:center;
}
.slider-scrollbar .scrollbar-track {
    height:2px;
    width:100%;
    background:#ccc;
    position: relative;
    border-radius:4px;
}
.slider-scrollbar:hover .scrollbar-track {
    height:4px;
}
.slider-scrollbar .scrollbar-thumb {
    position:absolute;
    height:100%;
    width:50%;
    background:#000;
    border-radius: inherit;
    cursor: grab;
}
.slider-scrollbar .scrollbar-thumb:active {
    cursor:grabbing;
    height:8px;
    top: -2px;
}
.slider-scrollbar .scrollbar-thumb::after {
    content:"";
    position:absolute;
    left:0;
    right:0;
    top:-10px;
    bottom:-10px;
}
</style>