<script lang="ts">
  import { defineComponent } from "vue";

  export default defineComponent({

  })
</script>

<template>
  <div class="study">
    <div class="study__inner container">
      <h2 class="study__title">Как проходит обучение</h2>

      <div class="study__top">
        <div class="study__info">
          <span class="study__info-title study__span">Играя — обучаем, обучая — развиваем</span>
          <p class="study__info-descr  study__descr">Мы взяли все самое лучшее из традиционных и современных методик обучения и развития детей.
            Обучение английскому языку происходит легко и интересно, ведь малыши не зубрят материал по учебникам, а познают его через игру, сказки, книги и музыку. <br>
            Наша методика также включает в себя обучение по программе Cambridge. Благодаря этому, наши ученики без труда сдают международные и государственные экзамены.
          </p>
        </div>

        <div class="study__show">
          <span class="study__show-title study__span">Посмотрите, как проходят наши занятия</span>
          <div class="study__show-video">
            <iframe width="431" height="231" src="https://www.youtube.com/embed/0O3E8mRhmic?si=eQ-53IGaSd1qD8nf" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
          </div>
        </div>
      </div>

      <div class="study__bottom">
        <div class="study__bottom-left">
          <div class="study__development">
            <span class="study__development-title study__span">Развитие 10 видов интеллекта</span>
            <div class="study__development-descr study__descr">Учимся общаться, развивать эмоциональный, творческий интеллект и многое другое</div>
          </div>
          <div class="study__teachers">
            <span class="study__teachers-title study__span">Педагоги — носители языка</span>
            <div class="study__teachers-descr study__descr">Занятия ведут преподаватели из США, Великобритании и Канады, для которых английский язык является родным</div>
          </div>
        </div>

        <div class="study__bottom-right">
          <div class="study__language">
            <span class="study__language-title study__span">Языковое погружение</span>
            <div class="study__language-descr study__descr">Занятия проходят полностью на английском языке, независимо от типа задания</div>
          </div>
          <div class="study__groups">
            <span class="study__groups-title study__span">Небольшие группы</span>
            <div class="study__groups-descr study__descr">Дети занимаются в группах до 5 человек, что позволяет применять индивидуальный подход к каждому</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
  .study {

    &__inner {
      padding: 130px 0;
    }

    &__title {
      margin-bottom: 80px;
      text-align: center;
      font-size: 36px;
      font-style: normal;
      font-weight: 500;
      line-height: 1;
    }

    &__top {
      position: relative;
      display: flex;
      justify-content: space-between;
      margin-bottom: 130px;

      &::before {
        content: "";
        position: absolute;
        width: 89px;
        height: 115px;
        top: 0;
        left: -150px;
        background-image: url(../assets/icons/girl.svg);
        background-repeat: no-repeat;
      }

      &::after {
        content: "";
        position: absolute;
        width: 135px;
        height: 68px;
        top: -180px;
        right: -70px;
        background-image: url(../assets/icons/rocket.svg);
        background-repeat: no-repeat;
      }
    }

    &__info {
      max-width: 414px;
    }

    &__span {
      display: block;
      font-size: 20px;
      font-style: normal;
      font-weight: 500;
      line-height: 1;
      margin-bottom: 20px;
    }

    &__info-title,
    &__show-title {
      margin-bottom: 30px;
    }

    &__descr {
      font-size: 16px;
      font-style: normal;
      font-weight: 400;
      line-height: 1.4;
    }

    &__show-video iframe{
      border-radius: 12px;
      opacity: 0.7;

      &:hover {
        opacity: 1;
        transition: 0.3s all linear;
      }
    }

    &__bottom {
      position: relative;
      display: flex;
      justify-content: space-between;

      &-left {
        max-width: 300px;
        padding-top: 81px;
      }

      &-right {
        max-width: 244px;
        padding-top: 35px;
      }
      
      &::before {
        content: "";
        position: absolute;
        width: 332px;
        height: 381px;
        top: 22px;
        left: 50%;
        transform: translateX(-50%);
        background-image: url(../assets/images/child.png);
      }
    }

    &__development {
      position: relative;
      margin-bottom: 185px;

      &::before {
        content: "";
        position: absolute;
        width: 182px;
        height: 61px;
        top: -80px;
        right: -80px;
        background-image: url(../assets/icons/vector-top-left.svg);
        background-repeat: no-repeat;
      }
    }

    &__teachers {
      position: relative;

      &::before {
        content: "";
        position: absolute;
        width: 130px;
        height: 118px;
        top: -140px;
        right: 4px;
        background-image: url(../assets/icons/vector-bottom-left.svg);
        background-repeat: no-repeat;
      }
    }

    &__language {
      position: relative;
      margin-bottom: 161px;

      &::before {
        content: "";
        position: absolute;
        width: 140px;
        height: 105px;
        bottom: -114px;
        left: -72px;
        background-image: url(../assets/icons/vector-top-right.svg);
        background-repeat: no-repeat;
      }
    }

    &__groups {
      position: relative;

      &::before {
        content: "";
        position: absolute;
        width: 143px;
        height: 56px;
        bottom: -24px;
        left: -150px;
        background-image: url(../assets/icons/vector-bottom-right.svg);
        background-repeat: no-repeat;
      }
    }
  }
</style>