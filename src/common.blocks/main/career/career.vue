<template>
    <div class="career">
        <TitleView class="title"
            :titleText="'КАРЬЕРНЫЙ РОСТ'"
        />
        <div class="wrapper career-info-wrapper">
            <div class="wrapper career-info-item">
                <!-- <img class="item-image mobile-only" 
                    src="./1.webp" 
                > -->
                <img class="item-image desktop-only" 
                    src="./1.svg" 
                >
                <TextView class="item-text"
                    :text="`Наша Компания является ярким примером, 
                        где достойные люди смело и заслуженно 
                        поднимаются по карьерной лестнице. `"
                />
            </div>
            <div class="wrapper career-info-item">
                <!-- <img class="item-image mobile-only" 
                    src="./2.webp" 
                > -->
                <img class="item-image desktop-only" 
                    src="./2.svg" 
                >
                <TextView class="item-text"
                    :text="`Мы ценим стремление к развитию 
                        и предоставляем все необходимые 
                        для этого условия.`"
                />
            </div>
        </div>
        <PersonCardView class="person-card mobile-only"
            v-if="currentPersonNumber==1"
            :name="firstPerson.name"
            :job="firstPerson.job"
            :characterInfoFirstLine="firstPerson.characterInfoFirstLine"
            :characterInfoSecondLine="firstPerson.characterInfoSecondLine"
            :characterInfoThirdLine="firstPerson.characterInfoThirdLine"
            :photo="require('./3.webp')"
        />
        <PersonCardView class="person-card mobile-only"
            v-if="currentPersonNumber==2"
            :name="secondPerson.name"
            :job="secondPerson.job"
            :characterInfoFirstLine="secondPerson.characterInfoFirstLine"
            :characterInfoSecondLine="secondPerson.characterInfoSecondLine"
            :characterInfoThirdLine="secondPerson.characterInfoThirdLine"
            :photo="require('./4.webp')"
        />
        <PersonCardView class="person-card mobile-only"
            v-if="currentPersonNumber==3"
            :name="thirdPerson.name"
            :job="thirdPerson.job"
            :characterInfoFirstLine="thirdPerson.characterInfoFirstLine"
            :characterInfoSecondLine="thirdPerson.characterInfoSecondLine"
            :characterInfoThirdLine="thirdPerson.characterInfoThirdLine"
            :photo="require('./5.webp')"
        />
        <PersonCardView class="person-card desktop-only"
            v-if="currentPersonNumber==1"
            :name="firstPerson.name"
            :job="firstPerson.job"
            :characterInfoFirstLine="firstPerson.characterInfoFirstLine"
            :characterInfoSecondLine="firstPerson.characterInfoSecondLine"
            :characterInfoThirdLine="firstPerson.characterInfoThirdLine"
            :photo="require('./3.svg')"
        />
        <PersonCardView class="person-card desktop-only"
            v-if="currentPersonNumber==2"
            :name="secondPerson.name"
            :job="secondPerson.job"
            :characterInfoFirstLine="secondPerson.characterInfoFirstLine"
            :characterInfoSecondLine="secondPerson.characterInfoSecondLine"
            :characterInfoThirdLine="secondPerson.characterInfoThirdLine"
            :photo="require('./4.svg')"
        />
        <PersonCardView class="person-card desktop-only"
            v-if="currentPersonNumber==3"
            :name="thirdPerson.name"
            :job="thirdPerson.job"
            :characterInfoFirstLine="thirdPerson.characterInfoFirstLine"
            :characterInfoSecondLine="thirdPerson.characterInfoSecondLine"
            :characterInfoThirdLine="thirdPerson.characterInfoThirdLine"
            :photo="require('./5.svg')"
        />
        <button class="left-navigation-button mobile-only"
            @click="selectPreviousElement()"
        >
            <img class="card__image"
                src="./left.webp"
            >
        </button>
        <button class="left-navigation-button desktop-only"
            @click="selectPreviousElement()"
        >
            <img class="card__image"
                src="./left.svg"
            >
        </button>
        <button class="right-navigation-button mobile-only"
            @click="selectNextElement()"
        >
            <img class="card__image"
                src="./right.webp"
            >
        </button>
        <button class="right-navigation-button desktop-only"
            @click="selectNextElement()"
        >
            <img class="card__image"
                src="./right.svg"
            >
        </button>
    </div>
</template>

<script>
import TitleView from './title/title.vue'
import TextView from './text/text.vue'
import PersonCardView from './person-card/person-card.vue'
export default {
    name:'CareerView',
    components: {
        TitleView,
        TextView,
        PersonCardView
    },
    data() {
        return {
            currentPersonNumber: 1,
            firstPerson: {
                name:"Олег Воробьёв",
                job:"Прораб",
                characterInfoFirstLine:`В Компании с 2018 года. 
                    Начал с позиции плотника 
                    в строительной бригаде.`,
                characterInfoSecondLine:`В  течение года работы 
                    Олег стал бригадиром и  был  приглашён в  офис 
                    Компании на  должность штатного Производителя 
                    строительных работ.`,
                characterInfoThirdLine:`На  данный момент в  Его  подчинении 
                    находятся 9  строительных бригад. 
                    Олег вносит весомый вклад в  итоговый 
                    результат Компании, а  это  реализация 1
                    00  объектов в  год!`
            },
            secondPerson: {
                name:"Мария Обухова",
                job:"Руководитель финансовой службы",
                characterInfoFirstLine:`В декабре 2018 года заступил 
                    на должность Менеджера отдела продаж.`,
                characterInfoSecondLine:`После 9 месяцев стабильных 
                    результатов, зарекомендовав себя как надёжный 
                    сотрудник, получил ответственную должность Логиста.`,
                characterInfoThirdLine:`Через год Даниил занял должность 
                    Специалиста службы снабжения, взяв на себя помимо 
                    закупа материала ещё и крайне важную роль Сметчика.`
            },
            thirdPerson: {
                name:"Даниил Басенков",
                job:"Менеджер по снабжению",
                characterInfoFirstLine:`В декабре 2018 года заступил 
                    на должность Менеджера отдела продаж.`,
                characterInfoSecondLine:`После 9 месяцев стабильных 
                    результатов, зарекомендовав себя как надёжный 
                    сотрудник, получил ответственную должность Логиста.`,
                characterInfoThirdLine:`Через год Даниил занял должность 
                    Специалиста службы снабжения, взяв на себя помимо 
                    закупа материала ещё и крайне важную роль Сметчика.`
            },
        }
    },
    methods: {
        selectPreviousElement() {
            if (this.currentPersonNumber > 1) {
                this.currentPersonNumber -= 1;
                console.log('Prev')
            }
        },
        selectNextElement() {
            if (this.currentPersonNumber < 3) {
                this.currentPersonNumber += 1;
                console.log('Next')
            }
        }
    }
}
</script>

<style lang="scss" scoped>
    @media (max-width: 992px) {
        @import "./career-mobile";
    } 
    @media (min-width: 992px) {
        @import "./career";
    } 
    @import url(./wrapper.scss);
</style>