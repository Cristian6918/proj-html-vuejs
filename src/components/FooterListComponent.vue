<template>
<div class='footer-list'>
    <h1>{{title}}</h1>
    <ul v-if='title==="Contact Us"'>
        <li> <i class="fa-solid fa-location-dot"></i> {{adress}}</li>
        <li> <i class="fa-solid fa-square-phone"></i> {{tel}}</li>
        <li> <i class="fa-regular fa-envelope"></i> {{mail}}</li>
    </ul>
    <ul>
        <li v-for="el in elements" :key='el'> <i class="fa-solid fa-angle-right"></i> {{el}}</li>
    </ul>
</div>
  
</template>

<script>
export default {
    props:["title","elements","adress","tel","mail","id"]

}
</script>

<style lang="scss" scoped>
@import '../assets/style/common.scss';

.footer-list{
    width:20%;
    h1{
        color:white;
        margin-bottom:1em;
    }
}

ul{
    color:#cccccc;
    list-style-type: none;
    padding-inline-start: 0;

    li{
        cursor:pointer;
        margin-bottom:10px;

        &:hover{
            color:#eeeeee;
        }
    }
}

</style>