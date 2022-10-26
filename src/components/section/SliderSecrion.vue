<template>
    <swiper
    :spaceBetween="30"
    :centeredSlides="true"
    :autoplay="{
      delay: 2500,
      disableOnInteraction: false,
    }"
    :pagination="{
      clickable: true,
    }"
    :navigation="true"
    :modules="modules"
    class="mySwiper"
    >
      <swiper-slide>
        <div className="desc">
            <span>Under the Sea</span>
            <h3>Jelly fish</h3>
            <p>
              심해 그 저편에는 말랑한 해파리들이 <br />
              가득 있습니다! 우리 같이 여러 모습들을 구경해보아요.
            </p>
            <div className="btn">
              <a href="/">자세히 보기</a>
              <a href="/" className="black">
                사이트 보기
              </a>
            </div>
          </div>
      </swiper-slide>
      <swiper-slide>
        <div className="desc">
            <span>Under the Sea</span>
            <h3>Jelly fish</h3>
            <p>
              심해 그 저편에는 말랑한 해파리들이 <br />
              가득 있습니다! 우리 같이 여러 모습들을 구경해보아요.
            </p>
            <div className="btn">
              <a href="/">자세히 보기</a>
              <a href="/" className="black">
                사이트 보기
              </a>
            </div>
          </div>
      </swiper-slide>
      <swiper-slide>
        <div className="desc">
            <span>Under the Sea</span>
            <h3>Jelly fish</h3>
            <p>
              심해 그 저편에는 말랑한 해파리들이 <br />
              가득 있습니다! 우리 같이 여러 모습들을 구경해보아요.
            </p>
            <div className="btn">
              <a href="/">자세히 보기</a>
              <a href="/" className="black">
                사이트 보기
              </a>
            </div>
          </div>
      </swiper-slide>
    </swiper>
</template>

<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";

// Import Swiper styles
import "swiper/css";

import "swiper/css/pagination";
import "swiper/css/navigation";

// import required modules
import { Autoplay, Pagination, Navigation } from "swiper";

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    return {
      modules: [Autoplay, Pagination, Navigation],
    };
  },
};
</script>

<style>
.slider__inner {
    margin-top: 70px;
}
.slider {
    position: relative;
}
.slider__img {
    background: url(../../assets/img/slider_bg01.jpg) no-repeat center / cover ;
}
.slider__img:hover {
    filter: brightness(120%);
    transition: all 0.3s ease;
}
.slider__img .desc {
    width: 1160px;
    margin: 0 auto;
    padding: 100px 20px;
}
.slider__img .desc span{
    font-size: 16px;
    height: 20px;
    line-height: 15px;
    background-color: #fff;
    padding: 6px 14px 0 14px;
    border-radius: 30px;
    text-transform:uppercase;
    margin-bottom: 15px;
    display: inline-block;

}
.slider__img .desc h3{
    font-size: 110px;
    font-weight: 500;
    line-height: 1;
    color: #fff;
    text-transform: uppercase;
    margin-bottom: 16px;
    padding-top: 10px;
    margin-left: -8px;
}
.slider__img .desc p {
    font-size: 20px;
    font-weight: 300;
    color: #fff;
    line-height: 1.35;
    margin-bottom: 130px;
}
.slider__img .desc .btn {

}
.slider__img .desc .btn a{
    font-size: 16px;
    background-color: rgba(255, 255, 255, 0.800);
    padding: 11px 50px;
    display: inline-block;
}
.slider__img .desc .btn a.black {
    background: rgba(0, 0, 0,   0.555);
    color: #fff;
}
.slider__arrow a {
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    width: 30px;
    height: 56px;
    background-image: url(../../assets/img/slider_icon.svg);
}

.slider__arrow a.left {
    left: 20px;
}
.slider__arrow a.rigth {
    right: 20px;
    background-position: -50px 0px;
}

.slider__dot {
    position: absolute;
    left: 50%;
    transform: translateX(-50%);
    bottom: 25px;
}

.slider__dot a {
    display: inline-block;
    width: 16px;
    height: 16px;
    background-image: url(../../assets/img/slider_icon.svg);
    background-position: -20px -70px ;
}

.slider__dot a.active {
    background-position: 0px -70px;
}

.slider__dot a.play {
    background-position: -40px -70px;
}

.slider__dot a.stop {
    background-position: -60px -70px;
}



/* swiper */

.swiper-slide {
    background: url(../../assets/img/slider_bg01.jpg) no-repeat center / cover ;
    /* height: 500px ; */
}
.swiper-slide:nth-child(2) {
    background: url(../../assets/img/slider_bg02.jpg) no-repeat center / cover ;
    /* height: 500px ; */
}
.swiper-slide:nth-child(3) {
    background: url(../../assets/img/slider_bg03.jpg) no-repeat center / cover ;
    /* height: 500px ; */
}

.swiper-slide:hover {
    filter: brightness(120%);
    transition: all 0.3s ease;
}

.swiper-slide .desc {
    width: 1160px;
    margin: 0 auto;
    padding: 100px 20px;
    box-sizing: border-box;
}
.swiper-slide .desc span{
    font-size: 16px;
    height: 20px;
    line-height: 15px;
    background-color: #fff;
    padding: 6px 14px 0 14px;
    border-radius: 30px;
    text-transform:uppercase;
    margin-bottom: 15px;
    display: inline-block;

}
.swiper-slide .desc h3{
    font-size: 110px;
    font-weight: 500;
    line-height: 1;
    color: #fff;
    text-transform: uppercase;
    margin-bottom: 16px;
    padding-top: 10px;
    margin-left: -8px;
}
.swiper-slide .desc p {
    font-size: 20px;
    font-weight: 300;
    color: #fff;
    line-height: 1.35;
    margin-bottom: 130px;
}

.swiper-slide .desc .btn a{
    font-size: 16px;
    background-color: rgba(255, 255, 255, 0.800);
    padding: 11px 50px;
    display: inline-block;
}
.swiper-slide .desc .btn a.black {
    background: rgba(0, 0, 0, 0.555);
    color: #fff;
}
.swiper-button-next,.swiper-button-prev  {
    width: 30px !important;
    height: 56px !important;
    background-image: url(../../assets/img/slider_icon.svg);
}
.swiper-button-next {
    background-position: -50px 0px;
}
.swiper-button-next:after, .swiper-button-prev:after {
    opacity: 0;
}

.swiper-pagination-bullet {
    width: 16px;
    height: 16px;
    background-image: url(../../assets/img/slider_icon.svg) !important;
    background-position: -20px -70px;
    background-color: transparent;
    opacity: 1;
}

.swiper-pagination-bullet-active {
    background-position: 0 -70px;
}

.swiper-button {
    position: absolute;
    left: 50%;
    margin-left: 40px;
    bottom: 24px;
    z-index: 1000;
    display: flex;
    cursor: pointer;
}

.swiper-button-stop {
    background-image: url(../../assets/img/slider_icon.svg) !important;
    background-position: -60px -70px;
    width: 16px;
    height: 16px;
}

.swiper-button-play {
    background-image: url(../../assets/img/slider_icon.svg) !important;
    background-position: -40px -70px;
    width: 16px;
    height: 16px;
}

@media (max-width: 960px){
    .swiper-slide .desc {
        width: 100%;
        text-align: center;

    }

    .swiper-slide .desc h3 {
        font-size: 70px;
    }
    
}
@media (max-width: 600px){
    .swiper-slide .desc {
        padding: 80px 0;
    }
    .swiper-slide .desc h3 {
        font-size: 40px;
    }

    .swiper-slide .desc p {
        font-size: 16px;
        margin-bottom: 50px;
    }

    .swiper-slide .desc .btn a {
        padding: 10px 25px;
    }
}
@media (max-width: 480px){
   
}
</style>