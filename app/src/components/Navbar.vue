<template>
    <nav class="navbar navbar-expand-lg navbar-light bg-light">
        <div class="container-fluid">
            <a class="Logo navbar-brand" href="index.html"><img src="/src/assets/img/Logo.nav.JPG" alt=""></a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav m-auto">
                    <li class="nav-item">
                        <a class="nav-link active" aria-current="page" href="#">Inicio</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">Quienes Somos</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">Afiliados</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="Planes.html">Planes</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">Tiendas</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">Marketplace</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">Blog</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="Contacto.html">Contacto</a>
                    </li>
                </ul>
            </div>
        </div>
    </nav>
</template>
<style>
    .navbar {
    position: relaive;
    width: 100%;
    height: 90px;
    background-color: white !important;
}

.navbar .Logo {
    position: relative;
    padding-left: -10px;
    width: 14%;
    z-index: 50;
}

nav .Logo img {
    position: relative;
    left: 50%;
    height: 50px;
}


.navbar div,
.navbar ul {
    position: relative;
    background-color: rgb(255, 255, 255) !important;
    z-index: 10;
}

.navbar ul li {
    position: relative;
    font-size: 1.2vw;
    margin-left: 15px;

}
</style>
<script type="text/javascript">
export default {
    name: 'Nabar'
}
</script>