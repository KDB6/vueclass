<template>
    <section id="textType" class="text__warp content" :class="attr">
        <span></span>
        <h2 class="mb70">{{title[0].title}}</h2>
        <div class="text__inner" :class="layout">
            <div class="text" :class="text.style" v-for="text in sub" v-bind:key="text.text">
            <h3 class="text__title">{{ text.title }}</h3>
                <p class="text__desc">
                {{ text.desc }}
                </p>
                <a class="text_btn" href="/"> {{ text.more }} </a>
            </div>
                <!-- <h3 class="text__title">"섬세한"</h3>
                <p class="text__desc">옷의 쓰임새에 알맞게 제작된 제품들은 높은 신뢰성과 내구성을 보입니다. 옷을 입는 상황에서의 편리함, 그리고 옷을 입지 않았을 때의 외양, 소재의 성능 등 세부적인 제작 요소들을 제어하고 제품의 완결성을 높입니다.</p>
                <a class="text__btn" href="/">Read more</a>
            </div>
            <div class="text t2">
                <h3 class="text__title">"드러내지 않는"</h3>
                <p class="text__desc">우리의 제품과 브랜드는 고객에게 본질의 형태로 자연스럽게 인식되는 것을 목표로 합니다. 외양에서 드러나는 표식과 불필요한 디테일들을 제거하고, 오랫동안 호흡하며 알 수 있는 옷의 힘에 집중합니다. 드러내지 않는 디테일과 브랜드 라벨링은 옷이 보여줄 수 있는 힘을 더 강조합니다.</p>
                <a class="text__btn" href="/">Read more</a>
            </div>
            <div class="text t3">
                <h3 class="text__title">"기준이 되는"</h3>
                <p class="text__desc">우리의 제품은 현대 사회의 표준이 될 수 있는 유니폼의 시작으로부터 만들어집니다. 모호함과 복잡함의 연속이 되는 시대에, 하나의 완성도 높은 제품을 선보임으로써 기준이 되고자 합니다. 간결함을 바탕으로, 우리가 추구하는 ‘기준이 되는 옷’을 만드는 데는 퀄리티 높은 소재와 철저한 공정이 개입됩니다.</p>
                <a class="text__btn" href="/">Read more</a>
            </div>
            <div class="text t4">
                <h3 class="text__title">"정돈된 편안함"</h3>
                <p class="text__desc">우리는 일련의 과정을 통해, 포터리가 생각하는 정돈된 실루엣의 완성을 목표로 합니다. 의류의 가장 기초가 되는 ‘소재’를 바탕으로 하여, 우리가 추구하는 정돈된 실루엣의 형태로 옷을 완성합니다. 정돈된 것들은 우리에게 편안함을 줍니다.</p>
                <a class="text__btn" href="/">Read more</a>
            </div>
            <div class="text t5">
                <h3 class="text__title">"절제된 위트"</h3>
                <p class="text__desc">우리는 포터리만의 ‘해학’을 가지고, 절제된 언어로 말을 건넵니다. 문장의 말미에 걸쳐 있는 재미의 반전 요소처럼, 브랜드 곳곳에 담겨 있는 재치 있는 디테일들은 포터리가 추구하는 절제된 위트를 규정합니다. 포터리가 만들어낸 옷들의 반듯하고 절제된 이미지 속에서, 우리는 각각의 요소와 소재를 비틀어 개개인에게 여유와 재미를 전달합니다.</p>
                <a class="text__btn" href="/">Read more</a>
            </div>
            <div class="text t6">
                <h3 class="text__title">"엄격한 기준"</h3>
                <p class="text__desc">우리에게 옷은 경험하지 못한 이상적인 세계를 엮어주는 하나의 통로입니다. 최상의 경험을 위해서는 기존에 겪지 못했던 최상의 소재를 선별해내야 합니다. 그리고 엄격한 감독을 통해 만들어내는 과정에 밀착하여 완결성을 높여야 합니다. 포터리의 옷들이 만들어지는 과정부터 고객에게 전달되는 그 순간까지, 우리는 이를 하나의 긴 여정으로 보고, 엄격한 기준으로 접근합니다.</p>
                <a class="text__btn" href="/">Read more</a>
            </div> -->
        </div>
    </section>
</template>

<script>
export default {
  props: {
    attr: String,
    layout: String,
  },
  data: function () {
    return {
      title: [{ title: "POTTERY" }],
      sub: [
        {
          class: "t1",
          title: "섬세한",
          desc: "옷의 쓰임새에 알맞게 제작된 제품들은 높은 신뢰성과 내구성을 보입니다. 옷을 입는 상황에서의 편리함, 그리고 옷을 입지 않았을 때의 외양, 소재의 성능 등 세부적인 제작 요소들을 제어하고 제품의 완결성을 높입니다.",
          more: "Read more",
        },
        {
          class: "t2",
          title: "드러내지 않는",
          desc: "우리의 제품과 브랜드는 고객에게 본질의 형태로 자연스럽게 인식되는 것을 목표로 합니다. 외양에서 드러나는 표식과 불필요한 디테일들을 제거하고, 오랫동안 호흡하며 알 수 있는 옷의 힘에 집중합니다. 드러내지 않는 디테일과 브랜드 라벨링은 옷이 보여줄 수 있는 힘을 더 강조합니다.",
          more: "Read more",
        },
        {
          class: "t3",
          title: "기준이 되는",
          desc: "우리의 제품은 현대 사회의 표준이 될 수 있는 유니폼의 시작으로부터 만들어집니다. 모호함과 복잡함의 연속이 되는 시대에, 하나의 완성도 높은 제품을 선보임으로써 기준이 되고자 합니다. 간결함을 바탕으로, 우리가 추구하는 ‘기준이 되는 옷’을 만드는 데는 퀄리티 높은 소재와 철저한 공정이 개입됩니다.",
          more: "Read more",
        },
        {
          class: "t4",
          title: "정돈된 편안함",
          desc: "우리는 일련의 과정을 통해, 포터리가 생각하는 정돈된 실루엣의 완성을 목표로 합니다. 의류의 가장 기초가 되는 ‘소재’를 바탕으로 하여, 우리가 추구하는 정돈된 실루엣의 형태로 옷을 완성합니다. 정돈된 것들은 우리에게 편안함을 줍니다.",
          more: "Read more",
        },
        {
          class: "t5",
          title: "절제된 위트",
          desc: "우리는 포터리만의 ‘해학’을 가지고, 절제된 언어로 말을 건넵니다. 문장의 말미에 걸쳐 있는 재미의 반전 요소처럼, 브랜드 곳곳에 담겨 있는 재치 있는 디테일들은 포터리가 추구하는 절제된 위트를 규정합니다. 포터리가 만들어낸 옷들의 반듯하고 절제된 이미지 속에서, 우리는 각각의 요소와 소재를 비틀어 개개인에게 여유와 재미를 전달합니다.",
          more: "Read more",
        },
        {
          class: "t6",
          title: "엄격한 기준",
          desc: "우리에게 옷은 경험하지 못한 이상적인 세계를 엮어주는 하나의 통로입니다. 최상의 경험을 위해서는 기존에 겪지 못했던 최상의 소재를 선별해내야 합니다. 그리고 엄격한 감독을 통해 만들어내는 과정에 밀착하여 완결성을 높여야 합니다. 포터리의 옷들이 만들어지는 과정부터 고객에게 전달되는 그 순간까지, 우리는 이를 하나의 긴 여정으로 보고, 엄격한 기준으로 접근합니다.",
          more: "Read more",
        },
      ],
    };
  },
};
</script>

<style>
#textType {
    background-color: #f9f9f9;
}
.text__inner {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
}
.text {
    width: 32%;
    margin-bottom: 2%;
    padding: 20px;
    box-sizing: border-box;
    border-radius: 10px;
    transition: background 0.4s;
}
.text:hover {
    background: #f5f5f5;
}
.text__title {
    font-size: 24px;
    line-height: 1;
    margin-bottom: 10px;
    white-space: nowrap;
    text-overflow: ellipsis;
    position: relative;
    padding-top: 75px;
}
.text__desc {
    font-size: 18px;
    font-weight: 300;
    line-height: 1.4;
    margin-bottom: 20px;
    overflow: hidden;
    text-overflow: ellipsis;
    display: -webkit-box;
    -webkit-line-clamp: 3; 
    -webkit-box-orient: vertical;
}

.text__title::before {
    content: '';
    position: absolute;
    left: 0;
    top: 0;
    width: 60px;
    height: 60px;
    background: url(../../assets/img/text_icon.svg);
}
.text.t1 .text__title::before {
    background-position: 0 0;
}
.text.t2 .text__title::before {
    background-position: -60px 0;
}
.text.t3 .text__title::before {
    background-position: -120px 0;
}
.text.t4 .text__title::before {
    background-position: -180px 0;
}
.text.t5 .text__title::before {
    background-position: -240px 0;
}
.text.t6 .text__title::before {
    background-position: -300px 0;
}
.text__btn {
    font-size: 16px;
    line-height: 1;
    text-decoration: underline;
    text-underline-position: under;
    color: #666;
}

@media (max-width: 960px) {
    .text {
        width: 49%;
        background: #f5f5f5;
    }
}
@media (max-width: 600px) {
    .text__title {
        font-size: 24px;
    }
    .text__desc {
        font-size: 16px;
    }
}
@media (max-width: 480px) {
    .text {
        width: 100%;
    }
    .text .desc {
        font-size: 16px;
    }
}

/* @media (max-width: 768px) {
    .container {
        min-width: 768px;
        padding: 0;
    }
    .text__inner {
        width: 768px;
        flex-wrap: wrap;
        justify-content: center;
    }
    .text {
        width: 350px;
        margin-bottom: 0%;
        padding: 30px;
    }
} */
</style>