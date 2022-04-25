<template>
    <section class="product">
        <div class="container__main">
            <div class="product__body">
                <div class="product__left">
                </div>

                <div class="product__right">
                    <h1 class="product__title" v-for="title in productTitle" :key="title">{{ title }}</h1>
                    <p class="product__article">Арт. 02765/46</p>

                    <div class="product__reviews">
                        <p class="product__reviews-txt">Отзывы</p>
                        <img src="../assets/img/rating.svg" alt="Звёзды рейтинга">
                        <a href=""> 14 отзывов 
                            <svg width="10" height="15" viewBox="0 0 10 15" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <path d="M1 1L9 8L1 14.5" stroke="#333333"/>
                            </svg>
                        </a>
                    </div>

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
                            <button class="select__button" type="button" @click="addClass" :class="{'active': isAddClass}">
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

                    <div class="product__buy">
                        <div class="product__buy-quantity">
                            <div class="product__buy-change" @click="quantity++">+</div>
                            <div class="product__buy-num">{{ quantity }} </div>
                            <div class="product__buy-change" @click="quantity--">-</div>
                        </div>

                        <button type="button" class="product__buy-cart">Добавить в корзину</button>

                        <button type="button" class="product__buy-fav">
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
            isChecked: false,
            size: "Выбрать размер",
            quantity: 1,
            productTitle: ['Пижама для девочек', ],
          }
    },
    methods: {
        addClass: function() {
        this.isAddClass = !this.isAddClass;
        },
        checkValue: function() {
            if (this.size) {
                return this.size;
            }
        }
    }
});
</script>

<style scoped lang="scss">
    .product {

        margin-top: 20px;

        &__body {
            display: flex;
            gap: 36px;
        }

        &__left {

        }

        &__right {
            display: flex;
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
            align-items: center;
            letter-spacing: 0.04em;
            color: #828282;
            margin-bottom: 8px;
        }

        &__reviews {
            display: flex;
            align-items: center;
            margin-bottom: 30px;

            p {
                font-size: 14px;
                line-height: 20px;
                color: #333333;
                margin-right: 12px;
            }

            a {
                font-size: 14px;
                line-height: 20px;
                color: #333333;
                display: flex;
                align-items: center;
                gap: 4px;
                margin-left: 4px;
            }
        }

        &__reviews-txt {

        }

        &__price  {
            display: flex;
            gap: 12px;
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
            text-decoration-line: line-through;
            color: #828282;
        }

        &__sale {
            display: flex;
            gap: 9px;
            margin-bottom: 20px;
        }

        &__sale-item {
            border: 1px solid #333333;
            font-size: 12px;
            line-height: 16px;
            display: flex;
            align-items: center;
            letter-spacing: 0.04em;
            color: #333333;
            padding: 4px 8px;
            display: flex;
            justify-content: center;
            align-content: center;
        }

        .select {
            margin-bottom: 6px;

            &__wrapper {

            }


            &__button-txt {
                color: #333333;
                font-size: 16px;
            }

            &__button  {
                border: 1px solid #333333;
                padding: 12px 16px;
                display: flex;
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
                    transition: all 0.3s;
                }
            }

            &__dropdown {
                opacity: 0;
                transform: scaleY(0);
                position: relative;
            }

            &__list {
                display: flex;
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
                display: flex;
                flex-direction: column;
                width: 100%;
                padding: 6px 12px;
                position: relative;
                transition: all 0.1s;

                &:hover,
                &:active {
                    background: #333333;
                    color: #fff;
                }
            }

            &__point-label {
                cursor: pointer;
                display: flex;
                width: 100%;
            }

            &__point-radio {
                width: 100%;
            }

            &__point-txt {

            }

        }

        &__underlined {
            margin-bottom: 10px;
            display: flex;
            gap: 4px;
            font-size: 14px;
            line-height: 20px;
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
            width: 686px;
        }
        
}

        .select__button.active + div{
            transform: scaleY(1);
            opacity: 1;
        }

        .select__button.active :nth-child(2) svg{
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

</style>
