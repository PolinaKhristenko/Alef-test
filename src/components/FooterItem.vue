<template>
    <footer class="footer">
        <div class="container">
            <div class="footer__body">
                <div class="footer__nav">
                    <div class="footer__nav-item">
                        <h6 class="footer__title">покупателям</h6>

                        <ul class="footer__list">
                            <li class="footer__item"><a href="">Каталог</a></li>
                            <li class="footer__item"><a href="">Акции</a></li>
                            <li class="footer__item"><a href="">Бренды</a></li>
                        </ul>
                    </div>

                    <div class="footer__nav-item">
                        <h6 class="footer__title">о нас</h6>

                        <ul class="footer__list">
                            <li class="footer__item"><a href="">О компании</a></li>
                            <li class="footer__item"><a href="">Новости</a></li>
                            <li class="footer__item"><a href="">Команда</a></li>
                        </ul>
                    </div>
                </div>

                <div class="footer__sale">
                    <h6 class="footer__title">Узнайте первыми о новинках и акциях</h6>

                    <div class="footer__error" v-if="errors.length">
                        <p v-for="error in errors" :key="error">{{ error }}</p>
                    </div>

                    <form @submit="checkForm" action="https://vuejs.org/" method="post" novalidate="true"
                    class="footer__form" id="form1">
                        <svg width="10" height="10" viewBox="0 0 10 10" fill="none" xmlns="http://www.w3.org/2000/svg"
                        @click="resetEmail">
                            <path d="M0.700012 9.06641L9.05007 0.88337" stroke="#C4C4C4"/>
                            <path d="M9.25165 9.06641L0.901606 0.883353" stroke="#C4C4C4"/>
                        </svg>
                        <input type="email" v-model="email" name="email" placeholder="Адрес электронной почты" />
                        <button type="submit">Подписаться</button>
                    </form>
                </div>
            </div>
        </div>
    </footer>
</template>

<script>

export default ({
    data() {
        return {
        errors: [],
        email: null,
        }
    },
    methods: {
    checkForm: function (e) {
      this.errors = [];

      if (!this.email) {
        this.errors.push('Пожалуйста, укажите электронную почту');
      } else if (!this.validEmail(this.email)) {
        this.errors.push('Пожалуйста, укажите корректный адрес электронной почты');
      }

      if (!this.errors.length) {
        return true;
      }

      e.preventDefault();
    },
    validEmail: function (email) {
      var re = /^(([^<>()[\]\\.,;:\s@"]+(\.[^<>()[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/;
      return re.test(email);
    },
    resetEmail: function () {
        return this.email = "";
    }
  }
})
</script>

<style scoped lang="scss">

.footer {

    margin-bottom: 70px;

    &__body {
        display: flex;
        max-width: 1099px;
        margin: 0 auto;
    }

    &__nav {
        color: #333333;
        display: flex;
        justify-content: space-between;
        gap: 290px;
    }

    &__nav-left {

    }

    &__nav-right {

    }

    &__title {
        font-size: 16px;
        line-height: 24px;
        letter-spacing: 0.04em;
        text-transform: uppercase;
        margin-bottom: 16px;
    }

    &__list {
        display: flex;
        flex-direction: column;
        gap: 8px;
    }

    &__item {
        font-size: 14px;
        line-height: 20px;
        letter-spacing: 0.04em;
        transition: all 0.3s;

        &:hover,
        &:active {
            opacity: 0.4;
        }
    }

    &__sale {
        margin-left: auto;
        width: 452px;
    }

    &__form {
        width: 100%;
        position: relative;

        svg {
            position: absolute;
            cursor: pointer;
            transition: all 0.3s;
            right: 14px;
            top: 8px;

            &:hover,
            &:active {
                opacity: 0.6;
            }
        }

        input {
            width: 100%;
            padding: 8px 0 8px 8px;
            border-top: none;
            border-left: none;
            border-right: none;
            border-bottom: 1px solid #C4C4C4;
            margin-bottom: 35px;
        }

        button {
            background: #FFFFFF;
            border: 1px solid #333333;
            padding: 8px 28px;
            font-size: 14px;
            line-height: 20px;
            margin-left: auto;

            &:hover,
            &:active {
                background: #333333;
                color: #fff;
            }
        }
    }

        &__error {
            margin: 5px 0;

            p {
                font-size: 14px;
                color: #c90101;
            }
        }


    @media screen and (max-width: 1024px) { 
        &__nav {
            gap: 100px;
        }
    }

    @media screen and (max-width: 992px) { 
        &__nav {
            gap: 50px;
        }
    }

    @media screen and (max-width: 768px) { 
        &__nav {
            gap: 0;
            justify-content: space-between;
        }

        &__body {
            flex-direction: column;
        }

        &__sale {
            margin-top: 38px;
            margin-left: 0;
            width: 100%;
        }
    }
}

</style>


