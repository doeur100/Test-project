<template>
     <div class="slider">
         <div class="list">
            <div class="list">
                <div class="item">
                    <img src="https://encrypted-tbn2.gstatic.com/licensed-image?q=tbn:ANd9GcTGwVa2x0c4RVl-4wQIqXYT9a9uu3REVmnF1Wy5Uhjfwayh_q-MyqW0gwBG299zRw-crdW8yGT4gs_LqsZJW0mvNXMuggLEnSGoMYPp8Q" alt="">
                    <div class="content">
                        <div class="title">MAGIC SLIDER</div>
                        <div class="type">FLOWER</div>
                        <div class="description">
                            Lorem ipsum dolor sit amet consectetur adipisicing elit. Nesciunt, asperiores officiis illum harum culpa maxime minima dolor quasi ab voluptas architecto ullam explicabo omnis placeat quis nihil beatae eos vero?
                        </div>
                        <div class="button">
                            <button>SEE MORE</button>
                        </div>
                    </div>
                </div>
                <div class="item">
                    <img src="https://encrypted-tbn2.gstatic.com/licensed-image?q=tbn:ANd9GcTGwVa2x0c4RVl-4wQIqXYT9a9uu3REVmnF1Wy5Uhjfwayh_q-MyqW0gwBG299zRw-crdW8yGT4gs_LqsZJW0mvNXMuggLEnSGoMYPp8Q" alt="">
                    <div class="content">
                        <div class="title">MAGIC SLIDER</div>
                        <div class="type">FLOWER</div>
                        <div class="description">
                            Lorem ipsum dolor sit amet consectetur adipisicing elit. Nesciunt, asperiores officiis illum harum culpa maxime minima dolor quasi ab voluptas architecto ullam explicabo omnis placeat quis nihil beatae eos vero?
                        </div>
                        <div class="button">
                            <button>SEE MORE</button>
                        </div>
                    </div>
                </div>
                <div class="item">
                    <img src="https://encrypted-tbn2.gstatic.com/licensed-image?q=tbn:ANd9GcTGwVa2x0c4RVl-4wQIqXYT9a9uu3REVmnF1Wy5Uhjfwayh_q-MyqW0gwBG299zRw-crdW8yGT4gs_LqsZJW0mvNXMuggLEnSGoMYPp8Q" alt="">
                    <div class="content">
                        <div class="title">MAGIC SLIDER</div>
                        <div class="type">FLOWER</div>
                        <div class="description">
                            Lorem ipsum dolor sit amet consectetur adipisicing elit. Nesciunt, asperiores officiis illum harum culpa maxime minima dolor quasi ab voluptas architecto ullam explicabo omnis placeat quis nihil beatae eos vero?
                        </div>
                        <div class="button">
                            <button>SEE MORE</button>
                        </div>
                    </div>
                </div>
                <div class="item">
                    <img src="https://encrypted-tbn2.gstatic.com/licensed-image?q=tbn:ANd9GcTGwVa2x0c4RVl-4wQIqXYT9a9uu3REVmnF1Wy5Uhjfwayh_q-MyqW0gwBG299zRw-crdW8yGT4gs_LqsZJW0mvNXMuggLEnSGoMYPp8Q" alt="">
                    <div class="content">
                        <div class="title">MAGIC SLIDER</div>
                        <div class="type">FLOWER</div>
                        <div class="description">
                            Lorem ipsum dolor sit amet consectetur adipisicing elit. Nesciunt, asperiores officiis illum harum culpa maxime minima dolor quasi ab voluptas architecto ullam explicabo omnis placeat quis nihil beatae eos vero?
                        </div>
                        <div class="button">
                            <button>SEE MORE</button>
                        </div>
                    </div>
                </div>
            </div>
         </div>
         <div class="thumbnail">
                <div class="item">
                    <img src="https://encrypted-tbn1.gstatic.com/licensed-image?q=tbn:ANd9GcTHYKjYLD2Dhiy86TTKYv-6TDux84y_Z__45XNhr1Y8XMFZWysY60LbXtS7qH6WRIMhQcBgEh4VB7flwnITfmkxfB-xCZ5f2nUlLsP5qg" alt="">
                </div>
                <div class="item">
                    <img src="https://encrypted-tbn1.gstatic.com/licensed-image?q=tbn:ANd9GcTHYKjYLD2Dhiy86TTKYv-6TDux84y_Z__45XNhr1Y8XMFZWysY60LbXtS7qH6WRIMhQcBgEh4VB7flwnITfmkxfB-xCZ5f2nUlLsP5qg" alt="">
                </div>
                <div class="item">
                    <img src="https://encrypted-tbn1.gstatic.com/licensed-image?q=tbn:ANd9GcTHYKjYLD2Dhiy86TTKYv-6TDux84y_Z__45XNhr1Y8XMFZWysY60LbXtS7qH6WRIMhQcBgEh4VB7flwnITfmkxfB-xCZ5f2nUlLsP5qg" alt="">
                </div>
                <div class="item">
                    <img src="https://encrypted-tbn1.gstatic.com/licensed-image?q=tbn:ANd9GcTHYKjYLD2Dhiy86TTKYv-6TDux84y_Z__45XNhr1Y8XMFZWysY60LbXtS7qH6WRIMhQcBgEh4VB7flwnITfmkxfB-xCZ5f2nUlLsP5qg" alt="">
                </div>
         </div>
         <div class="nextPrevArrows">
            <button class="prev"></button>
            <button class="next"></button>
         </div>
     </div>
</template>

<style scoped>
* {
    margin:0;
    padding:0;
    box-sizing: border-box;
}
body {
    font-family:"Poppins", sans-serif;
}
a {
    text-decoration:none;
}

/*slider section */
.slider {
    width:100vw;
    height:100vh;
    overflow: hidden;
    position: relative;
    margin-top:-50px;
}

.slider .list .item {
    width:100%;
    height:100%;
    position:absolute;
    inset:0 0 0 0;
}
.slider .list .item img {
    width:100%;
    height:100%;
    object-fit:cover;
}
.slider .list .item  .content {
    position:absolute;
    top:20%;
    width:1140px;
    max-width:80%;
    left:  50%;
    transform:translateX(-50%);
    padding-right:30%;
    box-sizing:border-box;
    color:#fff;
    text-shadow:0 5px 10px #0004;
}

.slider .list .item  .content .title,
.slider .list .item  .content .type {
    font-size:5em ;
    font-weight:bold;
    line-height:1.3em;
}
.slider .list .item  .content .type  {
    color:yellow;
}
.slider .list .item  .content .description {
    font-size:14px;
}
.slider .list .item  .content  .button button {
    border:none;
    background-color:#eee;
    color:black;
    padding:7px 15px;
    font-family:"Poppins",sans-serif;
    font-weight:500;
    cursor: pointer;
    letter-spacing:2px;
    transition:0.4s;
}
.slider .list .item  .content  .button button:hover {
    background:yellow;
 
}
.thumbnail {
    display:flex;
    gap: 20px;
    position:absolute;
    bottom:50px;
    left:50%;
    width:max-content;
    z-index:100;
}

.thumbnail .item {
    width:150px;
    height:220px;
    flex-shrink: 0;
    position: relative;
} 
.thumbnail .item img {
    width:100%;
    height:100%;
    object-fit:cover;
    border-radius:20px;
    box-shadow: 5px 0 15px rgba(0,0,0,0.3);
}

.nextPrevArrows {
    position:absolute;
    top:80%;
    right:52%;
    z-index:100;
    width:300px;
    max-width:30%;
    gap:10px;
    align-items:center;
}
</style>