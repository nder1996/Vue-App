<template>
    <div id="Pagination">
        <!-- Resultados -->
        <b-container class="list-group">
            <b-row>
            <li :class="{[`card_${user.id}`]: true}" id="card-target" v-for="(user, index) in users" v-show="(pag - 1) * NUM_RESULTS <= index  && pag * NUM_RESULTS > index">
                    <b-card no-body style="max-width: 18rem;" id="Card-Info" :img-src="user.url"  img-alt="Image" img-top>
                        <br> <br>
                            <h6 class="mb-0"><strong>{{ user.title }}</strong></h6>
                        <b-card-body>
                            {{ user.body }}
                        </b-card-body>
                        <b-card-body>
                            <a href="#" class="card-link">{{ user.link_1 }}</a> <br> <br>
                            <a href="#" class="card-link">{{ user.link_2 }}</a>
                        </b-card-body>
                    </b-card>
            
            </li>
             </b-row>
        </b-container>
        <!-- Controles -->
        <nav aria-label="Page navigation" class="text-center">
            <br>
            <ul class="pagination text-center">
                <li>
                    <a href="#" aria-label="Previous" v-show="pag != 1" @click.prevent="pag -= 1">
                        <span aria-hidden="true">« Anterior</span>&nbsp;<span aria-hidden="true">Siguiente »</span>
                    </a>
                </li>
                <li>
                    <a href="#" aria-label="Next" v-show="pag * NUM_RESULTS / users.length < 1" @click.prevent="pag += 1">
                        <span aria-hidden="true">« Anterior</span>&nbsp;<span aria-hidden="true">Siguiente »</span>
                    </a>
                </li>
            </ul>
        </nav>
    </div>
</template>
<script type="text/javascript">

    console.log("")


export default {
    name: 'Pagination_1',
    data() {
        return {
            NUM_RESULTS: 3, // Numero de resultados por página
            pag: 1, // Página inicial
            // JSON a mostrar
            users: [{
                    id: "1",
                    url: "src/assets/img/card-1.jpg",
                    title: "Promociona tu negocio en Internet",
                    body: "¿Cómo promocionar tu negocio en Internet? Crea anuncios pagados en plataformas digitales como Google Adwords,Facebook Ads, entre otros. Muchas personas, cuando están iniciando a",
                    link_1: "LEER MÁS »",
                    link_2: "3 julio, 2021"
                },
                {
                    id: "2",
                    url: "src/assets/img/card-2.jpg",
                    title: "¿Qué son las páginas de aterrizaje?",
                    body: "Una Landing Page (página de aterrizaje) es una página dentro de un sitio web, desarrollada con el único objetivo de convertir los visitantes en Leads",
                    link_1: "LEER MÁS »",
                    link_2: "8 mayo, 2021"
                },
                {
                    id: "3",
                    url: "src/assets/img/card-3.jpg",
                    title: "Aprende más sobre el SEO en Instagram",
                    body: "Instagram es la red social en donde las empresas buscan exhibir sus productos, ofreciendo una conexión mucho más personal y única con los usuarios que",
                    link_1: "LEER MÁS »",
                    link_2: "24 abril, 2021"
                },
                {
                    id: "4",
                    url: "src/assets/img/card-4.jpg",
                    title: "¿Cuál es la importancia de contar con un certificado SSL?",
                    body: "SSL Abreviatura de Secure Sockets Layer (capa de sockets seguros), un protocolo para navegadores y servidores web que permite autenticar, cifrar y descifrar la información",
                    link_1: "LEER MÁS »",
                    link_2: "10 abril, 2021"
                },
                {
                    id: "5",
                    url: "src/assets/img/card-5.jpg",
                    title: "Así funciona google analytics",
                    body: "Estamos en una era donde todo es interacción digital. Pedir de comer, acudir a apps que recomiendan lugares qué visitar, películas que ver, mover nuestros",
                    link_1: "LEER MÁS »",
                    link_2: "5 marzo, 2021"
                },
                {
                    id: "6",
                    url: "src/assets/img/card-6.jpg",
                    title: "Diferencias entre SEO y SEM",
                    body: "Cuando hablamos de marketing online hay dos conceptos de los que habrás leído mucho: posicionamiento SEO y SEM. Pero ¿conoces realmente la diferencia entre SEO",
                    link_1: "LEER MÁS »",
                    link_2: "12 febrero, 2021"
                }
            ]
        }
    }
}
</script>
<style>
.list-group{
    border:5px solid red; 
    display:flex;
    justify-content:center;
}

#card-target{
    display:flex;
    justify-content:center;
    margin-left:40px;
    border:5px solid black;
    width:28%;
    height:650px;
}

#Card-Info{
    margin-top:25px;
    margin-bottom:25px;
    text-align:center;
    border:5px solid gray;
     height:610px;
}





</style>