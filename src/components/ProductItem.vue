<template>
    <section class="product">
        <div class="container__main">
            <div class="product__body">
                <div class="product__left">
                </div>

                <div class="product__right">
                    <h1 class="product__title">Пижама для девочек</h1>
                    <p class="product__article">Арт. 02765/46</p>

                    <div class="product__reviews">
                        <p class="product__reviews-txt">Отзывы</p>
                        <img src="" alt="Звёзды рейтинга">
                        <a href=""> 14 отзывов 
                            <svg width="10" height="15" viewBox="0 0 10 15" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <path d="M1 1L9 8L1 14.5" stroke="#333333"/>
                            </svg>
                        </a>
                    </div>

                    <div class="product__price">
                        <p class="product__price-actual">800 ₽</p>
                        <p class="product__price-old">1 500 ₽</p>

                        <svg width="16" height="16" viewBox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <path d="M4 1L12 8L4 14.5" stroke="#333333"/>
                        </svg>
                    </div>

                    <div class="product__sale">
                        <p class="product__sale-item">скидка -36%</p>
                        <p class="product__sale-item">акция -20%</p>
                    </div>

                    <form action="" class="product__select">
                        <div class="select__wrapper">
                            <button class="select__button" type="button">
                                <span class="select__button-txt">
                                    Выбрать размер
                                </span>
                                <div class="select__button-arrow">
                                    <svg width="15" height="15" viewBox="0 0 20 20" fill="none" xmlns="http://www.w3.org/2000/svg">
                                        <path d="M10.0076 15C9.74735 15 9.49713 14.8999 9.29697 14.7098L1.2903 6.70377C0.899977 6.31348 0.899977 5.68301 1.2903 5.29272C1.68063 4.90243 2.31115 4.90243 2.70147 5.29272L9.99756 12.5882L17.2936 5.29272C17.684 4.90243 18.3145 4.90243 18.7048 5.29272C19.0951 5.68301 19.0951 6.31348 18.7048 6.70377L10.6981 14.7098C10.518 14.8999 10.2678 15 10.0076 15Z" fill="#ffffff"/>
                                    </svg>                            
                                </div>
                            </button>
                            <div class="select__dropdown">
                                <ul class="select__list">
                                    <li class="select__point">
                                        <label for="" class="select__point-label">
                                            <input type="radio" class="select__point-radio hide" name="size" value="8">
                                            <span class="select__point-txt">8</span>
                                        </label>
                                    </li>


                                    <li class="select__point">
                                        <label for="" class="select__point-label">
                                            <input type="radio" class="select__point-radio hide" name="size" value="10">
                                            <span class="select__point-txt">10</span>
                                        </label>
                                    </li>

                                    <li class="select__point">
                                        <label for="" class="select__point-label">
                                            <input type="radio" class="select__point-radio hide" name="size" value="12">
                                            <span class="select__point-txt">12</span>
                                        </label>
                                    </li>


                                    <li class="select__point">
                                        <label for="" class="select__point-label">
                                            <input type="radio" class="select__point-radio hide" name="size" value="14">
                                            <span class="select__point-txt">14</span>
                                        </label>
                                    </li>
                                </ul>
                            </div>
                        </div>
                    </form>

                    <a href="" class="product__underlined">Определить размер</a>

                    <!-- Добавление в корзину -->

                    <a href="" class="product__underlined">Купить в 1 клик</a>
            
                    <div class="product__links">
                        <a href="" class="product__underlined">
                            <img src="../assets/img/product-links1.svg" alt="Иконка одежды">
                            Описание товара</a>
                        <a href="" class="product__underlined">
                            <img src="../assets/img/product-links1.svg" alt="Иконка часов">
                            Доставка и возврат</a>
                        <a href="" class="product__underlined">
                            <img src="../assets/img/product-links1.svg" alt="Иконка оплаты">
                            Способы оплаты</a>
                    </div>

                </div>
            </div>
        </div>
    </section>
</template>

<script>
// import { defineComponent } from '@vue/composition-api'

export default defineComponent({
    setup() {
        
    },
})
</script>

<style scoped lang="scss">
    .product {
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
        }

        &__article {
            font-size: 12px;
            line-height: 16px;
            align-items: center;
            letter-spacing: 0.04em;
            color: #828282;
        }

        &__reviews {
            display: flex;
            align-items: center;
            
            p {
                font-size: 14px;
                line-height: 20px;
                color: #333333;
            }

            a {
                font-size: 14px;
                line-height: 20px;
                color: #333333;
            }
        }

        &__reviews-txt {

        }

        &__price  {

        }

        &__price-actual {

        }

        &__price-old {

        }

        &__sale {

        }

        &__sale-item {

        }

        &__select {
            &__wrapper {

            }

            &__button  {

            }

            &__button-txt {

            }

            &__button-arrow {

            }

            &__dropdown {

            }

            &__list {

            }

            &__point {

            }

            &__point-label {

            }

            &__point-radio {

            }

            .hide {

            }

            &__point-txt {

            }

        }

        &__underlined {

        }

        &__links {

        }
        
}

</style>
