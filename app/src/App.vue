<template>
    <div id="app">
        <Header></Header>
        <Navbar></Navbar>
        <div class="slider container-expand-lg">
            <video src="src/assets/video/Centro.Virtual.mp4" type="video/mp4" frameborder="0" allowfullscreen autoplay loop muted></video>
        </div>
        <br>
        <div class="afiliados container-fluid">
            <div class="row">
                <div class="Tarjeta col-sm-6">
                    <div class="card" style="background-color:rgb(101, 18, 150); color:black">
                        <div class="card-body">
                            <br>
                            <h3 class="card-title">282 Afiliados</h3>
                            <br>
                            <p class="card-text">Conoce todas las empresas afiliadas</p>
                            <br> <br>
                            <a href="#" class="btn btn-primary bg-light">¡Click aquí!</a>
                        </div>
                        <div>
                            <img src="/src/assets/img/Afiliado.jpg" alt="">
                        </div>
                    </div>
                </div>
                <div class="Tarjeta col-sm-6">
                    <div class="card" style="background-color:rgb(255, 178, 0); color:black">
                        <div class="card-body">
                            <br>
                            <h3 class="card-title">282 Afiliados</h3>
                            <br>
                            <p class="card-text">Conoce todas las empresas afiliadas</p>
                            <br> <br>
                            <a href="#" class="btn btn-primary bg-light">¡Click aquí!</a>
                        </div>
                        <div>
                            <img src="/src/assets/img/Lampara.jpg" alt="">
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="Icon container-expand-lg">
            <div><i class="fas fa-users"></i>
                <br>
                <h4>
                    Reconocimiento
                    <br>
                    <p>¡Date a conocer a más empresas!</p>
                </h4>
            </div>
            <div>
                <i class="fab fa-google"></i>
                <br>
                <h4>
                    Posicionamiento
                    <br>
                    <p>¡Aparece en los primeros resultados de Google!</p>
                </h4>
            </div>
            <div><i class="fas fa-handshake"></i>
                <br>
                <h4>
                    Negocios directos
                    <br>
                    <p>Ofrece y obtén descuentos sólo por ser afiliado</p>
                </h4>
            </div>
        </div>
        <br>
        <Pagination></Pagination>
        <br> <br>
        <div class="Principal">
            <div class="Efecto_Parallax">
                <div>
                    <h1>¡Aprovecha esta oportunidad!</h1>
                    <h2>Solicita afiliación</h2> <br> <br> <br> <br>
                    <p>Clic aquí para afiliarse ahora</p>
                </div>
            </div>
        </div>
    <br>
        <Pagination_1></Pagination_1>
        <br>
        <Footer></Footer>
    </div>
</template>
<script>
import Header from './components/Header.vue';
import Navbar from './components/Navbar.vue';
import Footer from './components/Footer.vue';
import Pagination from './components/Pagination.vue';
import Pagination_1 from './components/Pagination_1.vue';

export default {
    name: 'app',
    components: {
        Header,
        Navbar,
        Footer,
        Pagination,
        Pagination_1
    }
}
</script>
<style lang="scss">
#app {
    width: 100%;
    height: 100%;
    overflow: hidden;
}

.slider {
    position: relative;
    left: 1px;
}

.slider video {
    position: relative;
    width: 100%;
    left: -1px;
}

.afiliados {
    margin-bottom: 10px;
}

.afiliados .row {
    /**/
}

.afiliados .row .card {
    display: flex;
    flex-direction: row;
    margin-top: 20px;
}

.afiliados .row .card div {
    width: 53%;
    color: white;
}

.afiliados .row .card div img {
    width: 100%;
}

.card-body a {
    color: black;
}

.Icon {
    position: relative;
    justify-content: center;
    display: flex;
    flex-direction: wrap;
    flex-wrap: wrap;
    width: 92%;
    /* top: -280px;*/

}

.Icon div {
    position: relative;
    margin-top: 30px;
    margin-left: 70px;
    justify-content: center;
    align-items: center;
    display: flex;
    margin-bottom: 50px;
    width: 28%;
    overflow: hidden;

}

.Icon h4 {
    position: relative;
    font-size: 1.9vw;
    margin-left: 20px;
    width: 80%;
}

.Icon p {
    font-size: 1vw;
    margin-top: 10px;
    left: 10px;
}

.Icon i {
    font-size: 60px;
    color: rgb(88, 25, 147);
    margin-left: 15px;
}



.Principal {
    display: flex;
    position: relative;
    justify-content: center;
    align-items: center;
    text-align: center;

}

.Efecto_Parallax {
    display: flex;
    height: 500px;
    width: 100%;
    background-image: url('assets/img/parallax.jpg');
    background-repeat: no-repeat;
    background-attachment: fixed;
    background-size: cover;
    background-position: center;
    justify-content: center;
    align-items: center;

}

.Efecto_Parallax div {
    position: relative;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    border: 10px solid white;
    background-color: transparent;
    width: 80%;
    height: 400px;
    color: white;
}

.Efecto_Parallax div h1 {
    position: relative;
    width: 74%;
    font-size: 4vw;
    /*background-color: rgb(0, 0, 0, 0.5);*/
}

.Efecto_Parallax div h2 {
    width: 33%;
    font-size: 3vw;
    /* background-color: rgb(0, 0, 0, 0.5);*/
    margin-top: 50px;
}

.Efecto_Parallax div p {
    width: 30%;
    font-size: 1.2vw;
    /* background-color: rgb(0, 0, 0, 0.5);*/
}


/*--------------------------------------------------*/
 #gallerywrapper {
     width:640px;
     height:450px;
     margin:0 auto;
     position:relative;
     font-family:verdana, arial, sans-serif;
 } 

 #gallerywrapper #gallery {
     position:absolute;
     left:0;
     top:0;
     height:450px;
     width:640px;
     overflow:hidden;
     text-align:center;
 } 

 #gallerywrapper #gallery div {
     width:640px; height:900px; 
     padding-top:10px; 
     position:relative;
 } 

 #gallerywrapper #gallery div img {
     clear:both; 
     display:block; 
     margin:0 auto; 
     border:0;
 } 

 #gallerywrapper #gallery div h3 {
     padding:10px 0 0 0; 
     margin:0; 
     font-size:18px;
 } 

 #gallerywrapper #gallery div p {
     padding:5px 0; 
     margin:0; 
     font-size:12px; 
     line-height:18px;
 } 

 #gallery .previous{ 
     display:inline;
     float:left;
     margin-left:80px;
     text-decoration:none;
 } 

 #gallery .next{ 
     display:inline;
     float:right;
     margin-right:80px;
     text-decoration:none;
 }

</style>