<template>
    <header>
        <div class="container">
            <nav class="header__body">
                <a class="header__logo" href="/"><img src="../assets/img/logo.svg" alt="Логотип" class="header__logo"></a>
                <div class="header__icons">
                    <a class="header__icons-item">
                        <svg width="16" height="16" viewBox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <circle cx="8.45945" cy="4.18919" r="3.68919" stroke="#333333"/>
                            <path d="M0.5 15.3379H15.5" stroke="#333333"/>
                            <path d="M0.5 15.84C0.5 12.4347 4.84699 9.91339 8.21429 10.0023C11.4328 10.0872 15.5 12.4347 15.5 15.84" stroke="#333333"/>
                        </svg>
                    </a>

                    <a class="header__icons-item">
                        <svg width="16" height="16" viewBox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <path d="M7.90002 3.0948C6.69981 -2.52108 -2.59119 1.90389 1.76037 7.60175C6.11193 13.2996 8.40002 15.4908 8.40002 15.4908" stroke="#333333"/>
                            <path d="M7.89415 3.0948C9.09435 -2.52108 18.7304 1.90389 14.3789 7.60175C10.0273 13.2996 7.70001 15.5 7.70001 15.5" stroke="#333333"/>
                            <path d="M7.39099 2.70752L8.4043 2.70757L8.38337 3.24079H7.39099V2.70752Z" fill="#333333"/>
                        </svg>
                    </a>

                    <a class="header__icons-item">
                        <svg width="16" height="17" viewBox="0 0 16 17" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <path d="M1.25468 7.56595C1.13958 6.11201 2.2884 4.86865 3.74689 4.86865H12.2531C13.7116 4.86865 14.8604 6.11201 14.7453 7.56595L14.2203 14.1975C14.1174 15.4977 13.0323 16.5002 11.7281 16.5002H4.27189C2.96769 16.5002 1.88261 15.4977 1.77968 14.1975L1.25468 7.56595Z" stroke="#333333"/>
                            <path d="M3.99999 9.5C3.99999 9.5 3.78329 1 8.00001 1C12.2167 1 12 9.5 12 9.5" stroke="#333333"/>
                        </svg>
                    </a>

                    <a class="header__icons-burger">
                        <transition name="fade" mode="out-in">
                            <svg width="18" height="13" viewBox="0 0 18 13" fill="none" xmlns="http://www.w3.org/2000/svg"
                            v-if="!show" @click="show = !show" key="menu">
                                menu
                                <line y1="0.5" x2="18" y2="0.5" stroke="#333333"/>
                                <line y1="12.5" x2="18" y2="12.5" stroke="#333333"/>
                                <line y1="6.5" x2="18" y2="6.5" stroke="#333333"/>
                            </svg>

                            <svg width="15" height="15" viewBox="0 0 15 15" fill="none" xmlns="http://www.w3.org/2000/svg"
                            v-else @click="show = !show" key="close">
                                close
                                <line y1="-0.5" x2="19.2842" y2="-0.5" transform="matrix(-0.707107 -0.707107 -0.707107 0.707107 14 14.6357)" stroke="#333333"/>
                                <line x1="1.01046" y1="14.2822" x2="14.6464" y2="0.646203" stroke="#333333"/>
                            </svg>
                        </transition>

                        <transition name="fade">
                            <ul class="burder" v-if="show" >
                                <li><a href="">постельное белье</a></li>
                                <li><a href="">одежда для дома</a></li>
                                <li><a href="">одежда для улицы</a></li>
                                <li><a href="">выход</a></li>
                            </ul>
                        </transition>
                    </a>
                </div>
            </nav>
        </div>
    </header>
</template>



<script>
    export default {
        data() {
            return {
                show: false,
            }
        },
    };
</script>



<style scoped lang="scss">

    .header {
        width: 100%;
        border-bottom: 1px solid #E0E0E0;
        box-shadow: 0px 2px 4px rgba(0, 0, 0, 0.1);

        &__body {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 8px 0 12px 0;
        }

        &__logo {
            max-width: 67px;
            max-height: 22px;
        }

        &__icons {
            display: flex;
            gap: 24px;
            align-items: center;
            
        }
        
        &__icons-item {
            padding: 8px;

            svg {
            transition: all 0.3s;
            }

            &:hover svg,
            &:active svg {
                opacity: 0.4;
            }
        }

        &__icons-burger {
            display: none;
            padding: 8px;
            position: relative;
        }

        @media screen and (max-width: 768px) { 
            &__icons-burger  {
                display: flex;
            }
        }
    }

    .fade-enter-active,
    .fade-leave-active {
        transition: opacity 0.3s ease;
        }

    .fade-enter,
    .fade-leave-to {
        opacity: 0;
        }


</style>
