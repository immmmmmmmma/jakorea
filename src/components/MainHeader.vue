<template>
    <div class="header">
        <div class="headerWrap d-flex container">
            <h1 class="logo"><a href=""><img :src="`./images/new_logo.svg`" alt="" class="logoImg"></a></h1>
            <nav class="row">
                <div class="fnc">
                    <a href=""><i class="fa-solid fa-magnifying-glass"></i></a>
                    <a href=""><i class="fa-solid fa-user"></i></a>
                    <a href=""><i class="fa-brands fa-facebook"></i></a>
                    <a href=""><i class="fa-brands fa-instagram"></i></a>
                    <a href=""><i class="fa-brands fa-youtube"></i></a>
                    <a href=""><i class="fa-solid fa-bars"></i></a>
                </div>
                <ul class="navbar col-12">
                    <li><a href="">제이에이코리아</a></li>
                    <li><a href="">투명경영</a></li>
                    <li><a href="">교육사업</a></li>
                    <li><a href="">기관소식</a></li>
                    <li><a href="">후원하기</a></li>
                </ul>
            </nav>
        </div>
    </div>
</template>

<script>
export default {

}
</script>

<style lang="scss">
@import url('../assets/style.css');
    .headerWrap{
     padding: 20px 0;
        .logo{
            margin: 20px;
        }
    }
    .logoImg{
        width: 218px;
    }
    .fnc{
        margin-left: auto !important;
        a{
            padding: 5px;
            font-size: 20px;
            color: #333;
            margin-right: 10px;
            .fa-user,
            .fa-magnifying-glass{
                display: none;
            }
        }
    }
    .navbar{
        display: flex;
        li{
            padding: 10px 45px 28px 45px;
            a{
                font-size: 19px;
                color: #333;
                font-weight: 700;
            }
        }

    }
    
</style>