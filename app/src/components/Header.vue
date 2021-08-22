<template>
    <b-container class="header_1" fluid>
        <b-container class='P-bienvenida'>
            <p>
                <br>
                Bienvenidos al Centro Comercial Virtual
            </p>
        </b-container>
        <b-container class='search'>
            <form class="form d-flex">
                <input class="busqueda form-control me-2" type="search" placeholder="Busca aquí" aria-label="Search">
                <i class="fas fa-search"></i>
            </form>
        </b-container>
        <b-container>
            <i class="fab fa-facebook"></i>
            <i class="fab fa-instagram"></i>
            <i class="fab fa-whatsapp"></i>
        </b-container>
    </b-container>
</template>
<script type="text/javascript">
export default {
    name: 'Header'
}
</script>
<style type="text/css">
.header_1 {
    position: relative;
    display: flex;
    flex-direction: row;
    justify-self: center;
    align-content: center;
    height: 60px;
    background-color: rgb(88, 25, 147) !important;
}

.header_1 form input {
    position: relative;
    width: 110%;
}

.header_1 .P-bienvenida {
    position: relative;
    width: 40%;
    left: -3%;
}

.header_1 div p {
    font-size: 1.5vw;
    color: white !important;
}

.header_1 div i {
    font-size: 1.9vw;
}

.header_1 div {
    position: relative;
    text-align: center;
    display: flex;
    justify-content: center;
    align-items: center;
    margin-left: 50px;
    width: 33%;
}

.header_1 .form {
    position: relative;
    width: 100%;
}

.header_1 .busqueda {
    position: relative;
    outline: none;
    background-color: rgb(75, 19, 128);
    border: 1px solid rgb(75, 19, 128);
}

.header_1 .busqueda::placeholder {
    color: white !important;
}


.header_1 form i {
    position: relative;
    font-size: 1.5vw;
    left: -15%;
    top: 7px;
}


.header_1 i {
    position: relative;
    padding-left: 1.2vw;
    color: white !important;
    cursor: pointer;
}
</style>