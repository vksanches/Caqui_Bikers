<template>
    <footer>
       
        <a href="https://www.facebook.com/caquibikers/?ref=page_internal"><img src="../face_icon.png" alt="Facebook"></a>
        <a href="https://www.instagram.com/caquibikers/"> <img src="../instagran.png" alt="Instagram"> </a>
        
    </footer>

</template>

<script>

 export default { 
     name: 'Footer'
 }
 

</script>


<style scoped>
footer{
    width: 100%;
    height: 60px;
    background: #000;
    display: flex;
    justify-content: center;
    align-content: center;
}
img{
    width: 45px;
    height: 45px;
}

a{
    display: flexbox;
    margin: 0px 30px;
}
    
</style>