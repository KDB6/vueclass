<template>
    <section id="imageType" class="image__wrap content" :class="attr">
        <h2>{{top[0].title}}</h2>
        <p>{{top[1].desc}}</p>
        <div class="image__inner container" :class="layout">
            <article class="image img1">
                <h3 class="image__title">{{text[0].title}}</h3>
                <p class="image__desc">{{text[0].desc}}</p>
                <a class="image__btn" href="/" title="자세히 보기">{{text[0].btn}}</a>
            </article>
            <article class="image img2">
                <h3 class="image__title">{{text[1].title}}</h3>
                <p class="image__desc">{{text[1].desc}}</p>
                <a class="image__btn" href="/" title="자세히 보기">{{text[1].btn}}</a>
            </article>
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
        { title: "POTTERY"},
        { desc: "포터리는 좋은 옷을 통해 삶을 더 좋게 빚어 나갑니다."},
      ],
      text: [
        {
            title: "우리의 목적",
            desc: "포터리는 현대사회에 알맞는 유니폼을 제안하고자 합니다. 과거의 유니폼은 한 집단에 소속된 특징을 보여주는 옷이었다면, 현대의 유니폼은 개개인의 라이프스타일 또한 대변할 수 있는 옷이 되었습니다.",
            btn: "Read more"
        },
        { 
            title: "우리의 미션",
            desc: "COMPANY<br>'포터리는 다양한 직군을 관찰하고 그들의 문화와 환경에 맞는 소속감과 통일성이 있는 유니폼을 제공하는 서비스를 진행합니다.",
            btn: "Read more"
        },
      ],
    };
  },
}
</script>

<style>
#imageType {
    background-color: #f9f9f9;
}
.image__inner {
    display: flex;
    justify-content: space-between;
}
.image {
    width: 49%;
    height: 370px;
    color: #fff;
    padding: 200px 30px 30px 30px;
    box-sizing: border-box;
}
.image.img1 {
    background: url(../../assets/img/image01_01.jpg) no-repeat center;
}
.image.img2 {
    background: url(../../assets/img/image01_02.jpg) no-repeat center;
}
.image__title {
    font-size: 32px;
    margin-bottom: 10px;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
}
.image__desc {
    font-size: 16px;
    font-weight: 300;
    margin-bottom: 10px;
    line-height: 1.5;
    overflow: hidden;
    text-overflow: ellipsis;
    display: -webkit-box;
    -webkit-line-clamp: 2;
    -webkit-box-orient: vertical;
}
.image__btn {
    font-size: 16px;
    color: #fff;
    background-color: #cdcdcd40;
    padding: 10px 20px;
    display: inline-block;
}
.image__btn.yellow {
    background-color: #cdcdcd40;
}

@media (max-width: 960px) {

}
@media (max-width: 600px) {
    .image__inner {
        flex-direction: column;
    }
    .image {
        width: 100%;
        padding: 205px 20px 20px 20px;
    }
    .image:first-child {
        margin-bottom: 20px;
    }
    .image__title {
        font-size: 24px;
    }
    .image__desc {
        font-size: 16px;
    }
}
</style>