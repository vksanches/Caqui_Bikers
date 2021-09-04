<template>
    <header>
        <nav class="container">
        <a href="/"><img id="logo" src="https://scontent.fgru8-1.fna.fbcdn.net/v/t1.6435-9/116258287_3234601993274647_2262335002916708686_n.jpg?_nc_cat=110&ccb=1-5&_nc_sid=09cbfe&_nc_ohc=R7DUR9EHwVkAX9isBLA&_nc_ht=scontent.fgru8-1.fna&oh=6bdeae68845d6b3fd6a67ba82171efee&oe=61550F4B" alt=""></a>
        
        <img v-on:click="openMenu" src="https://raw.githubusercontent.com/william-costa/wdev-mock-site-resources/master/assets/images/menu.svg" alt="Menu" id="menu-botton">
        
        <div v-on:click="closeMenu" id="menu-overlay" v-if="menuActive"></div>
        
        <div id="menu-itens" :class="{active:menuActive}">
            <img v-on:click="openMenu" id="menu-logo" alt="Abrir Menu" src="https://scontent.fgru8-1.fna.fbcdn.net/v/t1.6435-9/116258287_3234601993274647_2262335002916708686_n.jpg?_nc_cat=110&ccb=1-5&_nc_sid=09cbfe&_nc_ohc=R7DUR9EHwVkAX9isBLA&_nc_ht=scontent.fgru8-1.fna&oh=6bdeae68845d6b3fd6a67ba82171efee&oe=61550F4B">
        
        <ul>
            <li><a href="/"></a>Home</li>
            <li><a href="/eventos"></a>Eventos</li>
            <li><a href="/fotos"></a>Fotos</li>
            <li><a href="/contatos"></a>Contato</li>
        </ul>
        
        </div>



        </nav>
    </header>
</template>

<script>

export default {
    name:'Header',
    data(){
        return {
            menuActive:false
        }
    },
    methods:{
        openMenu:function(){
            this.menuActive= true;
        },
        closeMenu:function(){
            this.menuActive= false;
        }
    }
}

</script>

<style scoped>
    header{
        background: black;
        height: 70px;
        width: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
}
    nav{
        display: flex;
        justify-content: space-between;
        height: 60px ;
        align-items: center;
}
    #logo{
        width: 70px;
    }

    #menu-botton{
        width: 30px;

    }

    #menu-overlay{
        position: fixed;
        top:0px;
        left: 0px;
        width: 40%;
        height: 100vh;
        background: #000;
        opacity: 0.8;
        
    }

    #menu-logo{
        width: 70px;
        margin-top: 30px;
        margin-bottom: 10px;
    }

    #menu-itens{
        position: fixed;
        top: 0px;
        right: 0px;
        width: 60%;
        background: #c21500;  /* fallback for old browsers */
        background: -webkit-linear-gradient(to right, #FF8008, #FFC837);  /* Chrome 10-25, Safari 5.1-6 */
        background: linear-gradient(to right, #FF8008, #FFC837); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
        height: 100vh;
        display: none;
        flex-direction: column;
        justify-content: flex-start;
        align-items: center;
    }

    #menu-itens.active{
        display: flex;
    }

    ul{
        list-style: none;
        text-align: center;
        
    }

    ul li a{
        color: black;
        
    }

    ul li{
        margin: 20px 0px;
    }

    @media (min-width: 700px){
        #menu-botton,
        #menu-logo,
        #menu-overlay{
            display: none;
        }

        #menu-itens{
            display: flex;
            position: static;
            height: 60px;
            width: auto;
        }
        
        ul{
            display: flex;
        }
        ul li{
            margin: 0;
            margin-left: 20px;
        
    }
}
        
</style>
