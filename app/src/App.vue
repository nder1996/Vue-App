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
        <Footer></Footer>
    </div>
</template>
<script>
import Header from './components/Header.vue';
import Navbar from './components/Navbar.vue';
import Footer from './components/Footer.vue';
import Pagination from './components/Pagination.vue';


export default {
    name: 'app',
    components: {
        Header,
        Navbar,
        Footer,
        Pagination
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
</style>