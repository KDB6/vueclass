<template>
    <section id="sliderType" class="slider__wrap nexon content">
        <h2 class="blind">슬라이드 영역</h2>
        <div class="slider__inner">
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
            <swiper-slide v-for="slider in sliders" v-bind:key="slider.text">
                <div class="swiper-slide" :class="slider.className">
                    <div class="desc">
                        <span>{{ slider.Brand }}</span>
                        <h3>{{ slider.title }}</h3>
                        <p>
                        {{ slider.desc}}
                        </p>
                        <div class="btn">
                            <a href="/">{{ slider.btn01 }}</a>
                            <a href="/" class="black"> {{ slider.btn02 }} </a>
                        </div>
                    </div>
                </div>
            </swiper-slide>
            <swiper-slide v-for="slider in sliders" v-bind:key="slider.text">
                <div class="swiper-slide" :class="slider.className">
                    <div class="desc">
                        <span>{{slider.Brand}}</span>
                        <h3>{{slider.title}}</h3>
                        <p>
                        {{slider.desc}}
                        </p>
                        <div class="btn">
                            <a href="/">{{slider.btn01}}</a>
                            <a href="/" class="black"> {{slider.btn02}} </a>
                        </div>
                    </div>
                </div>
            </swiper-slide>
            <swiper-slide v-for="slider in sliders" v-bind:key="slider.text">
                <div class="swiper-slide" :class="slider.className">
                    <div class="desc">
                        <span>{{slider.Brand}}</span>
                        <h3>{{slider.title}}</h3>
                        <p>
                            {{slider.desc}}
                        </p>
                        <div class="btn">
                            <a href="/">{{slider.btn01}}</a>
                            <a href="/" class="black"> {{slider.btn02}} </a>
                        </div>
                    </div>
                </div>
            </swiper-slide>
            </swiper>
        </div>
    </section>
</template>

<script>
import { Swiper, SwiperSlide } from "swiper/vue";
import "swiper/css";
import "swiper/css/navigation";
import "swiper/css/pagination";
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
  data: function () {
    return {
      sliders: [
        {
          className: "desc",
          Brand: "Brand",
          title: "22AW Lookbook",
          desc: "포터리는 현대사회에 알맞는 유니폼을 제안하고자 합니다.",
          btn01: "Read more",
          btn02: "Site",
        },
      ],
    };
  },
};
</script>



<style>
.slider__inner {
    /* margin-top: 70px; */
}
.slider {
    position: relative;
}
.slider__img {
    background: url(../../assets/img/slider_bg01.jpg) no-repeat center / cover;
}
.slider__img .desc {
    width: 1160px;
    margin: 0 auto;
    padding: 100px 20px;
}
.slider__img .desc span {
    font-size: 16px;
    background-color: #fff;
    padding: 1px 14px 0 14px;
    border-radius: 30px;
    text-transform: uppercase;
    margin-bottom: 10px;
    display: inline-block;
}
.slider__img .desc h3 {
    font-size: 110px;
    font-weight: 300;
    line-height: 1;
    color: #fff;
    text-transform: uppercase;
    margin-bottom: 16px;
    margin-left: -8px;
}
.slider__img .desc p {
    font-size: 20px;
    font-weight: 300;
    color: #fff;
    line-height: 1.35;
    margin-bottom: 130px;
}
.slider__img .desc .btn {}
.slider__img .desc .btn a {
    font-size: 16px;
    background-color: #fff;
    padding: 11px 50px;
    display: inline-block;
}
.slider__img .desc .btn a.black {
    background: #000;
    color: #fff;
    margin-left: 10px;
}
.slider__arrow a {
    position: absolute;
    top: 50%;
    width: 30px;
    height: 56px;
    background-image: url(../../assets/img/slider_icon.svg);
}
.slider__arrow a.left {
    left: 20px;
}
.slider__arrow a.right {
    right: 20px;
    background-position: -50px 0;
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
    background-position: -20px -70px;
}
.slider__dot a.active {
    background-position: 0 -70px;
}
.slider__dot a.play {
    background-position: -40px -70px;
}
.slider__dot a.stop {
    background-position: -60px -70px;
}

/* swiper */
.swiper-slide {
    background: url(../../assets/img/slider_bg01.jpg) no-repeat center / cover;
}
.swiper-slide .desc {
    width: 1160px;
    margin: 0 auto;
    padding: 100px 20px;
    box-sizing: border-box;
}
.swiper-slide .desc span {
    font-size: 16px;
    background-color: #fff;
    padding: 1px 14px 0 14px;
    border-radius: 30px;
    text-transform: uppercase;
    margin-bottom: 10px;
    display: inline-block;
}
.swiper-slide .desc h3 {
    font-size: 110px;
    font-weight: 300;
    line-height: 1;
    color: #fff;
    text-transform: uppercase;
    margin-bottom: 16px;
    margin-left: -8px;
}
.swiper-slide .desc p {
    font-size: 20px;
    font-weight: 300;
    color: #fff;
    line-height: 1.35;
    margin-bottom: 130px;
}
.swiper-slide .desc .btn {}
.swiper-slide .desc .btn a {
    font-size: 16px;
    background-color: #fff;
    padding: 11px 50px;
    display: inline-block;
}
.swiper-slide .desc .btn a.black {
    background: #000;
    color: #fff;
    margin-left: 10px;
}
.swiper-button-next, .swiper-button-prev {
    width: 25px !important;
    height: 50px !important;
    background: url(../../assets/img/slider_icon.svg);
}
.swiper-button-next {
    background-position: -55px 0;
}
.swiper-button-next::after, .swiper-button-prev::after {
    opacity: 0;
}

.swiper-pagination-bullet {
    width: 16px !important;
    height: 16px !important;
    background-image: url(../../assets/img/slider_icon.svg) !important;
    background-position: -20px -70px !important;
    background-color: transparent !important;
    opacity: 1 !important;
}
.swiper-pagination-bullet-active {
    background-position: 0px -70px !important;
}
.swiper-button {
    position: absolute;
    left: 50%;
    margin-left: 40px;
    bottom: 24px;
    z-index: 1000;
    display: flex;
}
.swiper-button-stop {
    background-image: url(../../assets/img/slider_icon.svg);
    background-position: -60px -70px;
    width: 16px;
    height: 16px;
}
.swiper-button-play {
    background-image: url(../../assets/img/slider_icon.svg);
    background-position: -40px -70px;
    width: 16px;
    height: 16px;
}

@media (max-width: 960px) {
    .swiper-slide .desc {
        width: 100%;
        text-align: center;
    }
    .swiper-slide .desc h3 {
        font-size: 70px;
    }
}
@media (max-width: 600px) {
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


/* @media (max-width: 768px) {
    .slider__img .desc span {
        font-size: 16px;
    }
    .slider__img .desc h3 {
        font-size: 70px;
    }
    .slider__img .desc p {
        font-size: 20px;
    }
    .slider__arrow a.left {
        display: none;
    }
    .slider__arrow a.right {
        display: none;
    }
} */
</style>