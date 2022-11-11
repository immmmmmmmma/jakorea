<template>
    <div class="header">
        <div class="headerWrap d-flex container">
            <h1 class="logo"><a href=""><img :src="`./images/new_logo.svg`" alt="" class="logoImg"></a></h1>
            <nav class="row col-9 navFncWrap">
                <div class="fnc">
                    <a href=""><i class="fa-solid fa-magnifying-glass"></i></a>
                    <a href=""><i class="fa-solid fa-user"></i></a>
                    <a href=""><i class="fa-brands fa-facebook"></i></a>
                    <a href=""><i class="fa-brands fa-instagram"></i></a>
                    <a href=""><i class="fa-brands fa-youtube"></i></a>
                    <a href=""><i class="fa-solid fa-bars"></i></a>
                </div>
                <ul class="navbar col-9">
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
    .navFncWrap{
        margin-left: 40px;
    }
    .fnc{
        display: flex;
        justify-content: flex-end;
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
        justify-content: space-between;
        margin-left: auto;
        li{
            padding: 10px 0;
            a{
                font-size: 19px;
                color: #333;
                font-weight: 700;
            }
        }

    }
    @media (max-width: 768px){
        .navbar{
            display: none;
        }
    }    
</style>