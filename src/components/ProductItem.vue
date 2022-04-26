<template>
    <section class="product">
        <div class="container__main">
            <div class="product__body">
                <div class="product__left">
                    <div class="product__left-main">
                        <img :src='productPhoto' :key="productPhoto" alt="Фото с товаром" />
                    </div>

                    <div class="product__left-all">
                        <img @click="changePhoto($event)" src="../assets/img/product1.png" id="0"
                        class="product__left-item" alt="Фото с товаром" >
                        <img @click="changePhoto($event)" src="../assets/img/product2.png" id="1"
                        class="product__left-item" alt="Фото с товаром">
                        <img @click="changePhoto($event)"  src="../assets/img/product3.png" id="2"
                        class="product__left-item" alt="Фото с товаром">
                    </div>
                </div>

                <div class="product__right">
                    <h1 class="product__title" v-for="title in productTitle" :key="title">{{ title }}</h1>
                    <p class="product__article">Арт. 02765/46</p>

                    <a href="" class="product__reviews">
                        <p class="product__reviews-txt">Отзывы</p>
                        <img src="../assets/img/rating.svg" alt="Звёзды рейтинга">
                        <div href=""> 14 отзывов 
                            <svg width="10" height="15" viewBox="0 0 10 15" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <path d="M1 1L9 8L1 14.5" stroke="#333333"/>
                            </svg>
                        </div>
                    </a>

                    <div class="product__price">
                        <p class="product__price-actual">800 ₽</p>
                        <p class="product__price-old">1 500 ₽</p>

                        <a href=""><svg width="10" height="15" viewBox="0 0 10 15" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <path d="M1 1L9 8L1 14.5" stroke="#333333"/>
                        </svg></a>
                    </div>

                    <div class="product__sale">
                        <p class="product__sale-item">скидка -36%</p>
                        <p class="product__sale-item">акция -20%</p>
                    </div>

                    <form action="#" class="product__select" id="form2">
                        <div class="select__wrapper">
                            <button class="select__button" type="button" @click="addClass" 
                            :class="{'active': isAddClass}">
                                <span class="select__button-txt">
                                    {{ size }}
                                </span>
                                <div class="select__button-arrow">
                                    <svg width="16" height="10" viewBox="0 0 16 10" fill="none" xmlns="http://www.w3.org/2000/svg">
                                        <path d="M14.75 0.75L7.75 8.75L1.25 0.75" stroke="#333333"/>
                                    </svg>                          
                                </div>
                            </button>
                            <div class="select__dropdown"> 
                                <ul class="select__list">
                                    <li class="select__point">
                                        <label for="" class="select__point-label">
                                            <input type="radio" v-model="size" class="select__point-radio hide" name="size" value="8">
                                            <span class="select__point-txt">8</span>
                                        </label>
                                    </li>


                                    <li class="select__point">
                                        <label for="" class="select__point-label">
                                            <input type="radio" v-model="size" class="select__point-radio hide" name="size" value="10">
                                            <span class="select__point-txt">10</span>
                                        </label>
                                    </li>

                                    <li class="select__point">
                                        <label for="" class="select__point-label">
                                            <input type="radio" v-model="size" class="select__point-radio hide" name="size" value="12">
                                            <span class="select__point-txt">12</span>
                                        </label>
                                    </li>


                                    <li class="select__point">
                                        <label for="" class="select__point-label">
                                            <input type="radio" v-model="size" class="select__point-radio hide" name="size" value="14">
                                            <span class="select__point-txt">14</span>
                                        </label>
                                    </li>
                                </ul>
                            </div>
                        </div>
                    </form>

                    <a href="" class="product__underlined">Определить размер</a>

                    <p :key="infoMessage" class="product__message"> {{ infoMessage }}</p>

                    <div class="product__buy">

                        <div class="product__buy-quantity">
                            <div class="product__buy-change" @click="quantity++">
                                <svg width="9" height="20" viewBox="0 0 9 20" fill="none" xmlns="http://www.w3.org/2000/svg">
                                    <path d="M4.46387 9.59277H7.28027V10.5361H4.46387V13.4482H3.51367V10.5361H0.710938V9.59277H3.51367V6.66699H4.46387V9.59277Z" fill="#333333"/>
                                    </svg>
                                </div>
                            <div class="product__buy-num">{{ quantity }} </div>
                            <div class="product__buy-change" @click="quantity--">
                                <svg width="7" height="20" viewBox="0 0 7 20" fill="none" xmlns="http://www.w3.org/2000/svg">
                                    <path d="M0.560547 11.7666V10.7275H6.43945V11.7666H0.560547Z" fill="#333333"/>
                                </svg>
                            </div>
                        </div>

                        <button type="button" class="product__buy-cart black-btn" @click="cartMessage" >Добавить в корзину</button>

                        <button type="button" class="product__buy-fav black-btn" @click="favMessage">
                            <svg width="16" height="16" viewBox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <path d="M7.90002 3.0948C6.69981 -2.52108 -2.59119 1.90389 1.76037 7.60175C6.11193 13.2996 8.40002 15.4908 8.40002 15.4908" stroke="white"/>
                                <path d="M7.89415 3.0948C9.09435 -2.52108 18.7304 1.90389 14.3789 7.60175C10.0273 13.2996 7.70001 15.5 7.70001 15.5" stroke="white"/>
                                <path d="M7.39099 2.70752L8.4043 2.70757L8.38337 3.24079H7.39099V2.70752Z" fill="white"/>
                            </svg>
                        </button>
                    </div>

                    <a href="" class="product__underlined">Купить в 1 клик</a>

                    <div class="product__line"></div>

                    <div class="product__links">
                        <a href="" class="product__underlined">
                            <img src="../assets/img/product-links1.svg" alt="Иконка одежды">
                            Описание товара</a>
                        <a href="" class="product__underlined">
                            <img src="../assets/img/product-links2.svg" alt="Иконка часов">
                            Доставка и возврат</a>
                        <a href="" class="product__underlined">
                            <img src="../assets/img/product-links3.svg" alt="Иконка оплаты">
                            Способы оплаты</a>
                    </div>

                </div>
            </div>
        </div>
    </section>
</template>

<script>

export default ({
    data() {
          return {
            isAddClass: false,
            size: "Выбрать размер",
            quantity: 1,
            productTitle: ['Пижама для девочек', ],
            infoMessage: "",
            productPhoto: require("../assets/img/product1.png"),
            photos: [
                {img: require("../assets/img/product1.png")},
                {img: require("../assets/img/product2.png")},
                {img: require("../assets/img/product3.png")},
            ],
          }
    },

    methods: {
        
        // Замена главного фото

        changePhoto: function (event) {
            let targetId = event.currentTarget.id;
            this.productPhoto = this.photos[targetId].img;
        },

        // Переключатель класса 'active'

        addClass: function() {
            this.isAddClass = !this.isAddClass;
        },

        // Селект с размерами

        checkValue: function() {
            if (this.size) {
                return this.size;
            }
        },

        // Добавление в "Избранное"

        favMessage: function() {
            if (this.quantity > 0) {
                this.infoMessage = "Товар '" + this.productTitle + "' в количестве '" + this.quantity + "' единиц добавлен в избранное"
                return this.infoMessage;  
            } else {
                this.infoMessage = "Пожалуйста, укажите количество"
                return this.infoMessage;  
            }
        },

        // Добавление в корзину

        cartMessage: function() {
            if (this.quantity > 0) {
                this.infoMessage = "Товар '" + this.productTitle + "' в количестве '" + this.quantity + "' единиц добавлен в корзину"
                return this.infoMessage;
            } else {
                this.infoMessage = "Пожалуйста, укажите количество"
                return this.infoMessage;             
            }
        },
    },
});
</script>

<style scoped lang="scss">
    .product {

        margin-top: 70px;


        &__body {
            display: -webkit-box;
            display: -ms-flexbox;
            display: flex;
            gap: 36px;
        }

        &__left {
            position: relative;

            &-main {
                overflow: hidden;
                width: 686px;
                height: auto;

                img {
                    width: 100%;
                    height: 100%;
                    -o-object-fit: cover;
                       object-fit: cover;
                }
            }

            &-item {
                z-index: 2;
                width: 70px;
                height: 91px;
                display: -webkit-box;
                display: -ms-flexbox;
                display: flex;
                -webkit-box-orient: vertical;
                -webkit-box-direction: normal;
                    -ms-flex-direction: column;
                        flex-direction: column;
                cursor: pointer;
                -webkit-transition: all 0.3s;
                -o-transition: all 0.3s;
                transition: all 0.3s;

                &:hover,
                &:active {
                    opacity: 0.7;
                }

            }

            &-all {
                position: absolute;
                top: 5%;
                left: 5%;
                display: -webkit-box;
                display: -ms-flexbox;
                display: flex;
                -webkit-box-orient: vertical;
                -webkit-box-direction: normal;
                    -ms-flex-direction: column;
                        flex-direction: column;
                gap: 7px;
            }
        }

        &__right {
            display: -webkit-box;
            display: -ms-flexbox;
            display: flex;
            -webkit-box-orient: vertical;
            -webkit-box-direction: normal;
                -ms-flex-direction: column;
                    flex-direction: column;
        }

        &__title {
            font-weight: 600;
            font-size: 18px;
            line-height: 24px;
            color: #333333;
            margin-bottom: 4px;
        }

        &__article {
            font-size: 12px;
            line-height: 16px;
            -webkit-box-align: center;
                -ms-flex-align: center;
                    align-items: center;
            letter-spacing: 0.04em;
            color: #828282;
            margin-bottom: 8px;
        }

        &__reviews {
            display: -webkit-box;
            display: -ms-flexbox;
            display: flex;
            -webkit-box-align: center;
                -ms-flex-align: center;
                    align-items: center;
            margin-bottom: 30px;

            p {
                font-size: 14px;
                line-height: 20px;
                color: #333333;
                margin-right: 12px;
            }

            div {
                font-size: 14px;
                line-height: 20px;
                color: #333333;
                display: -webkit-box;
                display: -ms-flexbox;
                display: flex;
                -webkit-box-align: center;
                    -ms-flex-align: center;
                        align-items: center;
                gap: 4px;
                margin-left: 4px;
            }
        }

        &__reviews-txt {

        }

        &__price  {
            display: -webkit-box;
            display: -ms-flexbox;
            display: flex;
            gap: 12px;
            -webkit-box-align: center;
                -ms-flex-align: center;
                    align-items: center;
            margin-bottom: 8px;
        }

        &__price-actual {
            font-weight: 700;
            font-size: 24px;
            line-height: 24px;
            text-transform: uppercase;
            color: #333333;
        }

        &__price-old {
            font-size: 14px;
            line-height: 20px;
            -webkit-text-decoration-line: line-through;
                    text-decoration-line: line-through;
            color: #828282;
        }

        &__sale {
            display: -webkit-box;
            display: -ms-flexbox;
            display: flex;
            gap: 9px;
            margin-bottom: 20px;
        }

        &__sale-item {
            border: 1px solid #333333;
            font-size: 12px;
            line-height: 16px;
            display: -webkit-box;
            display: -ms-flexbox;
            display: flex;
            -webkit-box-align: center;
                -ms-flex-align: center;
                    align-items: center;
            letter-spacing: 0.04em;
            color: #333333;
            padding: 4px 8px;
            display: flex;
            -webkit-box-pack: center;
                -ms-flex-pack: center;
                    justify-content: center;
            -ms-flex-line-pack: center;
                align-content: center;
        }

        &__select {
            margin: 6px 0;
        }

        .select {

            &__wrapper {

            }


            &__button-txt {
                color: #333333;
                font-size: 16px;
            }

            &__button  {
                border: 1px solid #333333;
                padding: 12px 16px;
                display: -webkit-box;
                display: -ms-flexbox;
                display: flex;
                -webkit-box-pack: justify;
                    -ms-flex-pack: justify;
                        justify-content: space-between;
                background: #fff;
                font-size: 14px;
                line-height: 20px;
                color: #333333;
                width: 315px;


                &:hover,
                &:active {
                    background: #333333;
                    
                    span {
                        color: #fff;
                    }
                    
                    svg path {
                        stroke: #fff;
                    }
                }
            }


            &__button-arrow {
                svg {
                    -webkit-transition: all 0.3s;
                    -o-transition: all 0.3s;
                    transition: all 0.3s;
                }
            }

            &__dropdown {
                opacity: 0;
                -webkit-transform: scaleY(0);
                    -ms-transform: scaleY(0);
                        transform: scaleY(0);
                position: relative;
            }

            &__list {
                display: -webkit-box;
                display: -ms-flexbox;
                display: flex;
                -webkit-box-orient: vertical;
                -webkit-box-direction: normal;
                    -ms-flex-direction: column;
                        flex-direction: column;
                width: 315px;
                position: absolute;
                top: 2px;
                left: 0;
                border: 1px solid #333333;
                gap: 1px;
                background: #fff;
            }

            &__point {
                display: -webkit-box;
                display: -ms-flexbox;
                display: flex;
                -webkit-box-orient: vertical;
                -webkit-box-direction: normal;
                    -ms-flex-direction: column;
                        flex-direction: column;
                width: 100%;
                padding: 6px 12px;
                position: relative;
                -webkit-transition: all 0.1s;
                -o-transition: all 0.1s;
                transition: all 0.1s;

                &:hover,
                &:active {
                    background: #333333;
                    color: #fff;
                }
            }

            &__point-label {
                cursor: pointer;
                display: -webkit-box;
                display: -ms-flexbox;
                display: flex;
                width: 100%;
            }

            &__point-radio {
                width: 100%;
            }

            &__point-txt {

            }

        }

        &__message {
            font-size: 12px;
            line-height: 20px;
            letter-spacing: 0.04em;
            color: #c90101;
            height: 6px;
        }

        &__buy {

            display: -webkit-box;

            display: -ms-flexbox;

            display: flex;
            margin: 40px 0 6px 0;
            -ms-flex-wrap: wrap;
                flex-wrap: wrap;
            gap: 8px;

            &-quantity {
                max-width: 145px;
                max-height: 50px;
                display: -webkit-box;
                display: -ms-flexbox;
                display: flex;
                font-size: 14px;
                line-height: 20px;
                letter-spacing: 0.04em;
                color: #333333;
                background: #F2F2F2;
                -webkit-box-align: center;
                    -ms-flex-align: center;
                        align-items: center;
                -webkit-box-pack: center;
                    -ms-flex-pack: center;
                        justify-content: center;
                gap: 20px;
            }

            &-change {
                cursor: pointer;
                padding: 12px 20px;

                &:hover,
                &:active {
                    background: #a6a6a6;
                }

            }

            &-num {
                padding: 12px 0;
            }

            &-cart {
                padding: 12px 28px;
            }

            &-fav {
                padding: 14px;
            }

        }

        &__underlined {
            margin-bottom: 10px;
            display: -webkit-box;
            display: -ms-flexbox;
            display: flex;
            gap: 4px;
            font-size: 14px;
            line-height: 20px;
            -webkit-text-decoration-line: underline;
                    text-decoration-line: underline;
            color: #333333;

            &:hover,
            &:active {
                opacity: 0.7;
            }
        }

        &__links {

        }

        &__line {
            padding-top: 20px;
            border-bottom: 0.5px solid #C4C4C4;
            margin-bottom: 20px;
            width: 100%;
        }

        @media screen and (max-width: 1100px) { 
            &__body {
                gap: 15px
            }

        }


        @media screen and (max-width: 1024px) { 
            &__buy {
                margin-top: 0;
            }


            &__left-main {
                width: 100%;
                height: auto;
            }

            &__buy-cart {
                margin-left: 0;
            }

        }


        @media screen and (max-width: 768px) { 
            &__body {
                -webkit-box-orient: vertical;
                -webkit-box-direction: normal;
                    -ms-flex-direction: column;
                        flex-direction: column;
            }

            &__line {
                width: 100vw;
                margin-left: -20px;
            }

            &__right {
                margin-left: 20px;
            }

            &__buy {
                -webkit-box-orient: vertical;
                -webkit-box-direction: normal;
                    -ms-flex-direction: column;
                        flex-direction: column;
                margin-top: 40px;
            }

        }
        
}

        .select__button.active + div{
            -webkit-transform: scaleY(1);
                -ms-transform: scaleY(1);
                    transform: scaleY(1);
            opacity: 1;
        }

        .select__button.active :nth-child(2) svg{
            -webkit-transform: rotateZ(360deg) scaleY(-1);
                -ms-transform: rotate(360deg) scaleY(-1);
                    transform: rotateZ(360deg) scaleY(-1);
            opacity: 1;
        }

        .hide {
            opacity: 0;
            position: absolute;
            height: 100%;
            width: 100%;
            cursor: pointer;
        }

        .black-btn {
            background: #333333;
            border: 1px solid #333333;
            font-size: 14px;
            line-height: 20px;
            color: #FFFFFF;
            display: -webkit-box;
            display: -ms-flexbox;
            display: flex;
            -webkit-box-align: center;
                -ms-flex-align: center;
                    align-items: center;
            -webkit-box-pack: center;
                -ms-flex-pack: center;
                    justify-content: center;
            margin-right: 4px;
            width: -webkit-fit-content;
            width: -moz-fit-content;
            width: fit-content;

            svg path {
                -webkit-transition: stroke 0.3s;
                -o-transition: stroke 0.3s;
                transition: stroke 0.3s;
            }

            &:hover,
            &:active {
                color:#333333;
                background: #fff;
                border-color: transparent;

                svg path {
                    stroke: #333333;
                }
            }
        }

</style>
