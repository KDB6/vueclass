<template>
    <section id="imgTextType" class="imgText__wrap content" :class="attr">
        <h2 class="blind">{{top[0].text}}</h2>
        <div class="imgText__inner" :class="layout">
            <div class="imgText__txt">
                <span>{{top[0].text}}</span>
                <h3>{{top[0].text}}</h3>
                <p>{{top[1].text}}</p>
                    <ul>
                        <li v-for="title in imgText" v-bind:key="title.text">
                        <a href="/">{{title.text}}</a>
                    </li>
                </ul>
            </div>
            <div class="imgText__img img1">
                <a href="#">NEW ARRIVALS</a>
            </div>
            <div class="imgText__img img2">
                <a href="#" class="blue">BEST</a>
            </div>
        </div>
    </section>
</template>

<script>
export default {
  props: {
    attr: String,
    layout: String
  },
  data: function () {
    return {
      top: [
        { text: "NEW ARRIVALS"},
        { text: "새로움의 시작"},
      ],
      imgText: [
        { text: "All" },
        { text: "Shirt" },
        { text: "Knit" },
        { text: "T-Shirt" },
        { text: "Jacket" },
        { text: "Pants" },
      ],
    };
  },
}
</script>

<style>
.imgText__inner {
    display: flex;
    justify-content: space-between;
}
.imgText__inner > div {
    width: 32%;
    height: 500px;
}
.imgText__txt {
    width: 32%;
}
.imgText__txt span {
    font-size: 16px;
    color: #666;
    text-decoration: underline;
    text-underline-position: under;
    margin-bottom: 20px;
    display: block;
}
.imgText__txt p {
    font-size: 18px;
    font-weight: 300;
    line-height: 1.5;
    color: #666;
    margin-bottom: 10px;
}
.imgText__txt h3 {
    font-size: 50px;
    font-weight: 300;
    margin-bottom: 20px;
}
.imgText__txt ul li{
    font-size: 18px;
    font-weight: 300;
    line-height: 1.6;
    margin-left: 20px;
    color: #666;
}
.imgText__txt ul li a {
    color: #666;
}
.imgText__txt ul li::before {
    content: '';
    width: 5px;
    height: 3px;
    border-radius: 50%;
    position: absolute;
    left: 5px;
    top: 9px;
}
.imgText__img{
    border-radius: 10px;
    position: relative;
}
.imgText__img a {
    position: absolute;
    left: 30px;
    bottom: 30px;
    background-color: #64646470;
    color: #fff;
    font-size: 18px;
    padding: 10px 30px;
    border-radius: 30px;
    display: inline-block;
}
.imgText__img a.blue {
    background-color: #44444470;
}
.imgText__img.img1 {
    background: url(../../assets/img/imgText_bg01.jpg) no-repeat center;
}
.imgText__img.img2 {
    background: url(../../assets/img/imgText_bg02.jpg) no-repeat center;
}

@media (max-width: 960px) {
    .imgText__inner {
        flex-wrap: wrap;
    }
    .imgText__txt h3 {
        font-size: 40px;
    }
    .imgText__txt p {
        margin-bottom: 60px;
    }
    .imgText__inner > div.imgText__txt {
        width: 100%;
        height: auto;
        text-align: center;
    }
    .imgText__inner > div.imgText__txt ul {
        display: none;
    }
    .imgText__inner > div.imgText__img {
        width: 49%;
    }
    .imgText__img a {
        left: 11%;
        bottom: 5%;
    }
}
@media (max-width: 600px) {
    .imgText__txt span {
        font-size: 14px;
        margin-bottom: 10px;
    }
    .imgText__txt h3 {
        font-size: 30px;
    }
    .imgText__txt p {
        margin-bottom: 50px;
        font-size: 16px;
    }
    .imgText__inner > div.imgText__img {
        width: 100%;
        height: 300px;
    }
    .imgText__inner > div.imgText__img.img1 {
        margin-bottom: 20px;
    }
    .imgText__img a {
        left: 5%;
        bottom: 5%;
    }
}

/* @media (max-width: 768px) {
    .imgText__inner {
        min-width: 768px;
        display: block;
    }
    .imgText__txt {
        margin-left: 15px;
        min-width: 768px;
        margin-bottom: 20px;
    }
    .imgText__txt ul li {
        display: inline;
        list-style: none;
    }
    .imgText__all {
        margin-left: 15px;
    }
} */
</style>