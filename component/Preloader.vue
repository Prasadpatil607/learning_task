<template>
    <div class="preloader p-0" id="preloader">
        <div class="loader d-flex flex-column align-items-center"><img src="../assets/egg.gif" alt=""></div>
    </div>
</template>

<style scoped>
    .preloader{
        position:fixed;
        top:0;left:0;right:0;bottom:0;
        z-index:10001;
        background-color:#fd6061;
        opacity:1;
        -webkit-transition:opacity 2s cubic-bezier(.77,0,.18,1);
        -o-transition:opacity 2s cubic-bezier(.77,0,.18,1);
        transition:opacity 2s cubic-bezier(.77,0,.18,1);
        display:-webkit-box;
        display:-ms-flexbox;
        display:flex;
        -webkit-box-align:center;
        -ms-flex-align:center;
        align-items:center;
        -webkit-box-pack:center;
        -ms-flex-pack:center;
        justify-content:center
    }
    @media (min-width:992px){
        .preloader{
            -webkit-box-align:center;
            -ms-flex-align:center;
            align-items:center;
            -webkit-box-pack:center;
            -ms-flex-pack:center;
            justify-content:center;
            padding-right:7.5rem;
            padding-bottom:4rem;
        }
    }
    .preloader.loaded{
        opacity:0;
    }
</style>