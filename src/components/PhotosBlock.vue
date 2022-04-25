<template>
    <section class="photos">
        <div class="container__main">

            <a href="" class="photos__styles">Посмотреть все стили</a>

            <div class="photos__body">
                <div class="photos__main">
                    <a href="" class="photos__main-photo">
                        <img src="../assets/img/photo1.png" alt="Фото товара">
                        <div class="photos__hover">
                            <img src="../assets/img/photo-more.svg" class="photos__hover-more" alt="Несколько фотографий">

                            <div class="photos__hover-center">

                                <div class="photos__hover-cart">
                                    <img src="../assets/img/photo-cart.svg" alt="Корзина">
                                    <p>Узнай, что на мне</p>
                                </div>

                                <div class="photos__hover-like">
                                    <img src="../assets/img/photo-like.svg" alt="Лайк">
                                
                                    <p>200</p>
                                </div>
                            </div>

                        </div>
                    </a>
                </div>

                <div class="photos__all">
                    <a href="" class="photos__item"><img src="../assets/img/photo2.png" alt="Фото товара">
                        <div class="photos__hover">
                            <img src="../assets/img/photo-more.svg" class="photos__hover-more" alt="Несколько фотографий">

                            <div class="photos__hover-center">

                                <div class="photos__hover-cart">
                                    <img src="../assets/img/photo-cart.svg" alt="Корзина">
                                    <p>Узнай, что на мне</p>
                                </div>

                                <div class="photos__hover-like">
                                    <img src="../assets/img/photo-like.svg" alt="Лайк">
                                
                                    <p>200</p>
                                </div>
                            </div>

                        </div>                    
                    </a>
                    <a href="" class="photos__item"><img src="../assets/img/photo4.png" alt="Фото товара">
                        <div class="photos__hover">
                            <img src="../assets/img/photo-more.svg" class="photos__hover-more" alt="Несколько фотографий">

                            <div class="photos__hover-center">

                                <div class="photos__hover-cart">
                                    <img src="../assets/img/photo-cart.svg" alt="Корзина">
                                    <p>Узнай, что на мне</p>
                                </div>

                                <div class="photos__hover-like">
                                    <img src="../assets/img/photo-like.svg" alt="Лайк">
                                
                                    <p>200</p>
                                </div>
                            </div>

                        </div>                    
                    </a>
                    <a href="" class="photos__item"><img src="../assets/img/photo3.png" alt="Фото товара">
                        <div class="photos__hover">
                            <img src="../assets/img/photo-more.svg" class="photos__hover-more" alt="Несколько фотографий">

                            <div class="photos__hover-center">

                                <div class="photos__hover-cart">
                                    <img src="../assets/img/photo-cart.svg" alt="Корзина">
                                    <p>Узнай, что на мне</p>
                                </div>

                                <div class="photos__hover-like">
                                    <img src="../assets/img/photo-like.svg" alt="Лайк">
                                
                                    <p>200</p>
                                </div>
                            </div>

                        </div>                      
                    </a>
                    <a href="" class="photos__item"><img src="../assets/img/photo5.png" alt="Фото товара">
                        <div class="photos__hover">
                            <img src="../assets/img/photo-more.svg" class="photos__hover-more" alt="Несколько фотографий">

                            <div class="photos__hover-center">

                                <div class="photos__hover-cart">
                                    <img src="../assets/img/photo-cart.svg" alt="Корзина">
                                    <p>Узнай, что на мне</p>
                                </div>

                                <div class="photos__hover-like">
                                    <img src="../assets/img/photo-like.svg" alt="Лайк">
                                
                                    <p>200</p>
                                </div>
                            </div>
                        </div>                      
                    </a>
                </div>
            </div>
        </div>
    </section>
</template>

<script>

</script>

<style scoped lang="scss">
    
.photos {

        margin-bottom: 130px;

        &__body {
            display: -webkit-box;
            display: -ms-flexbox;
            display: flex;
            gap: 16px;
        }

        &__styles {
            font-size: 14px;
            line-height: 20px;
            -webkit-text-decoration-line: underline;
                    text-decoration-line: underline;
            color: #333333;
            -ms-flex-item-align: center;
                -ms-grid-row-align: center;
                align-self: center;
            margin: 28px 0;

            &:hover,
            &:active {
                opacity: 0.7;
            }
        }

        &__main {

        }

        &__main-photo {
            position: relative; 
            
            img {
                -o-object-fit: cover;
                   object-fit: cover;
                max-width: 686px;
                max-height: 688px;
            }
        }

        &__hover {
            background: #333333;
            opacity: 0;
            position: absolute;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            display: -webkit-box;
            display: -ms-flexbox;
            display: flex;
            -webkit-box-pack: center;
                -ms-flex-pack: center;
                    justify-content: center;
            font-size: 14px;
            line-height: 20px;
            color: #FFFFFF;
            z-index: 2;
            -webkit-box-align: center;
                -ms-flex-align: center;
                    align-items: center;
            -webkit-transition: all 0.3s;
            -o-transition: all 0.3s;
            transition: all 0.3s;

            &:hover,
            &:active {
                opacity: 0.7;
            }
        }

        &__hover-more {
            width: 16px;
            height: 16px;
            position: absolute;
            top: 16px;
            right: 16px;
        }

        &__hover-center {
            text-align: center;
            display: -webkit-box;
            display: -ms-flexbox;
            display: flex;
            -webkit-box-orient: vertical;
            -webkit-box-direction: normal;
                -ms-flex-direction: column;
                    flex-direction: column;
            -webkit-box-align: center;
                -ms-flex-align: center;
                    align-items: center;
            -webkit-box-pack: center;
                -ms-flex-pack: center;
                    justify-content: center;
            z-index: 3;
            height: 100%;

            img {
                width: 48px;
                height: 48px;
                margin-bottom: 7px;
            }
        }

        &__hover-cart {
            -ms-flex-item-align: center;
                -ms-grid-row-align: center;
                align-self: center;
            margin-top: auto;
        }

        &__all {
            display: -ms-grid;
            display: grid;
            gap: 16px;
            -ms-grid-columns: 1fr 16px 1fr;
            grid-template-columns: 1fr 1fr;
        }

        &__item {
            position: relative;

            img {
                max-width: 335px;
                max-height: 336px;
                -o-object-fit: cover;
                   object-fit: cover;
            }
        }


        &__hover-like {
            display: -webkit-box;
            display: -ms-flexbox;
            display: flex;
            -webkit-box-align: center;
                -ms-flex-align: center;
                    align-items: center;
            margin-bottom: 16px;
            margin-top: auto;

            img {
                -webkit-transition: all 0.3s;
                -o-transition: all 0.3s;
                transition: all 0.3s;
                margin-right: 6px;
                max-height: 16px;
                max-width: 16px;

                &:hover {
                    -webkit-transform: scale(1.3, 1.3);
                        -ms-transform: scale(1.3, 1.3);
                            transform: scale(1.3, 1.3);
                }
            }
        }


        @media screen and (max-width: 768px) { 
            &__body {
                -webkit-box-orient: vertical;
                -webkit-box-direction: normal;
                    -ms-flex-direction: column;
                        flex-direction: column;
            }

            &__body {
                gap: 8px;
            }

            &__all {
                gap: 8px;
            }

            &__styles {
                margin: 58pxx 0;
            }

            & {
                margin-bottom: 30px;
            }
        }

    }
</style>