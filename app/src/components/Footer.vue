<template>
    <footer class="container-fluid-expand-lg">
        <div class="img_logo">
            <img src="/src/assets/img/footer-logo.JPG" alt="">
        </div>
        <div class="info_footer">
            <h5>INFORMACIÓN DE CONTACTO</h5>
            <div class="info">
                <div>
                    Pereira <br> <br>
                    Cra 10 No. 50 – 26 <br>
                    Barrio Maraya <br>
                    Teléfono: (+57) 6 341 3235 <br>
                    Celular: (+57) 313 571 8406
                </div>
                <div>
                    Medellín <br> <br>
                    El Poblado, Calle 10 # 42 – 45 <br>
                    Edificio La Plaza, oficina 318 <br>
                    Teléfono: (+57) 4 545 4253 Celular: <br>
                    (+57) 310 440 9875 <br>
                </div>
                <h5>SOPORTE DIRECTO DESDE WHATSAPP</h5>
                <h6>POLÍTICA DE TRATAMIENTO DE DATOS</h6>
            </div>
            <img src="/src/assets/img/PositiveSSL_SectigoTag_300dpi.png" alt="">
        </div>
        <div class="img-london">
            <div>
                <br> <br>
                <h5>UN PROYECTO DE:</h5>
                <br>
                <img src="/src/assets/img/london.red.JPG" alt="" width="168" height="80">
                <br> <br>
                <a href="https://conectamostuempresa.com/">www.conectamostuempresa.com</a>
            </div>
        </div>
    </footer>
</template>
<style>
footer {
    position: relative;
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: center;
    background-color: rgb(88, 25, 147);
    width: 100%;

}

footer div {
    width: 30%;
    overflow: hidden;
    margin-left: 15px;
    margin-top: 30px;
    margin-bottom: 15px;
}

footer .img_logo {
    text-align: right;
}

footer .img_logo img {
    width: 65%;
    height: 250px;
}

footer .info_footer {
    text-align: center;
    height: 50%;

}

footer .info_footer h5 {
    color: white !important;
    font-size: 17px;
}

footer .info_footer h6 {
    color: white !important;
    font-size: 15px;
}

footer .info_footer img {
    /*width: 80%;
    height: 300px;*/
}

footer .info_footer .info {
    display: flex;
    justify-content: center;
    width: 93%;
    flex-direction: row;
    flex-wrap: wrap;
    height: 90%;
}

footer .info_footer .info h5 {
    position: relative;
    top: -10px;
}

footer .info_footer .info h6 {
    position: relative;
    top: -10px;
}

footer .info_footer .info div {
    width: 46%;
    font-size: 15px;
    color: white !important;
    height: 50%;
    margin-bottom: 40px;
}

footer .img-london {
    position: relative;
    justify-content: center;
    background-color: transparent;
    border-radius: 10px;

}

footer .img-london div {
    position: relative;
    text-align: center;
    background-color: white !important;
    border-radius: 10px;
    height: 300px;
    width: 70%;
    font-size: 15px;

}

footer .img-london div a {
    text-decoration: none;
    color: black;
}
</style>
<script type="text/javascript">
export default {
    name: 'Footer'
}

</script>