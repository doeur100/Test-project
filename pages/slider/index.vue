<template>
  <div class="slider">
    <div class="list">
      <div class="item" v-for="(item, index) in items" :key="index">
        <img :src="item.img" alt="">
        <div class="content">
          <div class="title">{{ item.title }}</div>
          <div class="type">{{ item.type }}</div>
          <div class="description">{{ item.description }}</div>
          <div class="button">
            <button>SEE MORE</button>
          </div>
        </div>
      </div>
    </div>
    <div class="thumbnail">
      <div class="item" v-for="(thumbnail, index) in thumbnails" :key="index">
        <img :src="thumbnail.img" alt="">
      </div>
    </div>
    <div class="nextPrevArrows">
      <button class="prev" @click="moveSlider('prev')">Prev</button>
      <button class="next" @click="moveSlider('next')">Next</button>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref, onMounted } from 'vue'

const items = ref([
  {
    img: 'https://encrypted-tbn2.gstatic.com/licensed-image?q=tbn:ANd9GcTGwVa2x0c4RVl-4wQIqXYT9a9uu3REVmnF1Wy5Uhjfwayh_q-MyqW0gwBG299zRw-crdW8yGT4gs_LqsZJW0mvNXMuggLEnSGoMYPp8Q',
    title: 'MAGIC SLIDER',
    type: 'FLOWER',
    description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit...',
  },
  {
    img: 'https://encrypted-tbn1.gstatic.com/licensed-image?q=tbn:ANd9GcTHYKjYLD2Dhiy86TTKYv-6TDux84y_Z__45XNhr1Y8XMFZWysY60LbXtS7qH6WRIMhQcBgEh4VB7flwnITfmkxfB-xCZ5f2nUlLsP5qg',
    title: 'MAGIC SLIDER',
    type: 'FLOWER',
    description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit...',
  },
])

const thumbnails = ref([
  { img: 'https://encrypted-tbn1.gstatic.com/licensed-image?q=tbn:ANd9GcTHYKjYLD2Dhiy86TTKYv-6TDux84y_Z__45XNhr1Y8XMFZWysY60LbXtS7qH6WRIMhQcBgEh4VB7flwnITfmkxfB-xCZ5f2nUlLsP5qg' },
  { img: 'https://encrypted-tbn2.gstatic.com/licensed-image?q=tbn:ANd9GcTGwVa2x0c4RVl-4wQIqXYT9a9uu3REVmnF1Wy5Uhjfwayh_q-MyqW0gwBG299zRw-crdW8yGT4gs_LqsZJW0mvNXMuggLEnSGoMYPp8Q' },
  { img: 'https://encrypted-tbn3.gstatic.com/licensed-image?q=tbn:ANd9GcToHP5KjxRNU7vLmbDDFtEY2AABbEYx4phBBInV9lsW_q-rbJvVpxkOt4hdPLrVr2v4KUCF1jdEcm-D8iObMlQoLyULHKRgxg' },
  { img: 'https://encrypted-tbn3.gstatic.com/licensed-image?q=tbn:ANd9GcShElSZMhpXoMzx5v6xvJ3vNf3EjhW7JAWnhkKoWpmQ0c_HfqgQpg83v94HQbKWSVxhPrkE_93AZpJ6spuBbHr0bfirU9nONow' }
]);


const slider = ref<HTMLElement | null>(null)
const sliderList = ref<HTMLElement | null>(null)
const thumbnail = ref<HTMLElement | null>(null)

onMounted(() => {
  slider.value = document.querySelector('.slider')
  sliderList.value = slider.value?.querySelector('.list') as HTMLElement
  thumbnail.value = document.querySelector('.thumbnail') as HTMLElement
})

function moveSlider(direction: string) {
  const sliderItems = sliderList.value?.querySelectorAll('.item')
  const thumbnailItems = thumbnail.value?.querySelectorAll('.item')

  if (sliderItems && thumbnailItems) {
    if (direction === 'next') {
      sliderList.value?.appendChild(sliderItems[0])
      thumbnail.value?.appendChild(thumbnailItems[0])
      slider.value?.classList.add('next')
    } else {
      sliderList.value?.prepend(sliderItems[sliderItems.length - 1])
      thumbnail.value?.prepend(thumbnailItems[thumbnailItems.length - 1])
      slider.value?.classList.add('prev')
    }

    slider.value?.addEventListener(
      'animationend',
      () => {
        slider.value?.classList.remove(direction)
      },
      { once: true }
    )
  }
}
</script>
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
.nextPrevArrows button {
    width:40px;
    height:40px;
    border-radius:50%;
    background-color:white;
    border:none;
    font-family:monospace;
    font-weight:bold;
    cursor: pointer;
    transition:0.5s;
}

.nextPrevArrows button:hover {
    background-color:yellow;
}

/* animation part */
.slider .list .item:nth-child(1) {
    z-index:1;
}
.slider .list .item:nth-child(1) .content .title,
.slider .list .item:nth-child(1) .content .type,
.slider .list .item:nth-child(1)  .content .description,
.slider .list .item:nth-child(1)  .content .button {
    transform: translateY(50px);
    filter:blur(20px);
    opacity:0;
    animation: showContent 0.5s 1s linear 1 forwards;
}

@keyframes showContent {
    to {
        transform: translateY(0px);
        filter:blur(00px);
        opacity:1;
    }
}
.slider .list .item:nth-child(1) .content .title {
    animation-delay:0.4s;
}
.slider .list .item:nth-child(1) .content .type {
    animation-delay:0.6s;
}
.slider .list .item:nth-child(1) .content .description {
    animation-delay:0.8s;
}
.slider .list .item:nth-child(1) .content .button {
    animation-delay:1s;
}

/* Animation for next button click */
.slider.next .list .item:nth-child(1) img {
    width:150px;
    height:220px;
    position:absolute;
    bottom:50px;
    left: 50%;
    border-radius:30px;
    animation: showImage 0.5s 1s linear 1 forwards;
}
@keyframes showImage {
    to {
        bottom:0;
        left:0;
        width:100%;
        height:100%;
        border-radius:0;
    }
}

.slider.next .thumbnail .item:nth-child(1) {
    overflow:hidden;
    animation:showThumbnail 0.5s linear 1 forwards;
}

.slider.prev .list .item img {
    z-index: 100;
}
@keyframes showThumbnail {
    from {
        width:0;
        opacity:0;
    }
}

.slider.next .thumbnail {
    animation:effectNext .5s linear 1 forwards;
}
@keyframes effectNext {
    from {
        transform: translateX(150px);
    }
}

/* Animation for prev button click  */
.slider.prev .list .item:nth-child(2) {
    z-index:2;
}
.slider.prev .list .item:nth-child(2) img {
    position:absolute;
    bottom:0;
    left:0;
    animation:outFrame 0.5s linear 1 forwards;
}

@keyframes outFrame {
    to {
        width:150px;
        height:220px;
        bottom:50px;
        left:50%;
        border-radius:20px;
    }
}

.slider.prev .thumbnail .item:nth-child(1) {
    overflow:hidden;
    opacity:0;
    animation:showThumbnail .5s linear 1 forwards;
}


.slider.prev .item:nth-child(1) .content .title,
.slider.prev .item:nth-child(1) .content .type,
.slider.prev .item:nth-child(1)  .content .description,
.slider.prev .item:nth-child(1)  .content .button {
    animation:contentOut 0.5s 1s linear 1 forwards;
}
@keyframes contentOut {
    to {
        transform:translateY(-150px);
        filter:blur(20px);
        opacity:0;
    }
}
@media screen and (max-width: 678px) {
    .slider .list .item .content {
        padding-right:0;
    }
    .slider .list .item .content .title {
        font-size:30px;
    }
}

</style>