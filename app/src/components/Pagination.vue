<template>
    <b-container>
        <h2 class="P-Letra">Últimos Afiliados</h2>
        <p id="linea-p"></p>
        <b-row class="Marco">
            <b-col cols="12" sm="2" class="my-1" :key="index" v-for="(item, index) in paginatedItems">
                <img :src="item.url" alt="">
                <p class="card-text">{{item.body}}</p>
            </b-col>
        </b-row>
        <b-row>
            <b-col md="6" class="my-1" id="Barra-P">
                <b-pagination @change="onPageChanged" :total-rows="totalRows" :per-page="perPage" v-model="currentPage" class="my-0" />
            </b-col>
        </b-row>
    </b-container>
</template>
<script>
console.log("ola mundo");
const items = [{
        body: "Agentes Inmobiliarios",
        url: "src/assets/img/img-1.jpg"
    },
    {
        body: "Nelly Carrillo",
        url: "src/assets/img/img-2.jpg"
    },
    {
        body: "Premium Rent a Car",
        url: "src/assets/img/img-3.jpg"
    },
    {
        body: "Maria Teresa López Psicoterapeuta",
        url: "src/assets/img/img-4.jpg"
    },
    {
        body: "Grupo Integral Consultor",
        url: "src/assets/img/img-5.jpg"
    },
    {
        body: "Lunazul Virtual Shop",
        url: "src/assets/img/img-6.jpg"
    },
    {
        body: "Coworking en Pereira",
        url: "src/assets/img/img-7.jpg"
    },
    {
        body: "OCLLS",
        url: "src/assets/img/img-8.jpg"
    }
];

export default {
    name: "MyBootstrapGrid",
    data() {
        return {
            items: items,
            paginatedItems: items,
            currentPage: 1,
            perPage: 4,
            totalRows: items.length
        };
    },
    computed: {},
    methods: {
        paginate(page_size, page_number) {
            let itemsToParse = this.items;
            this.paginatedItems = itemsToParse.slice(
                page_number * page_size,
                (page_number + 1) * page_size
            );
        },
        onPageChanged(page) {
            this.paginate(this.perPage, page - 1);
        }
    },
    mounted() {
        this.paginate(this.perPage, 0);
    }
};
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.P-Letra {
    text-align: center;
}

#linea-p {
    position: relative;
    left: 42%;
    border-bottom: 5px solid black;
    width: 14%;
    height: 10px;
}

.Marco {
    display: flex;
    justify-content: left;
}

.my-1 {
    width: 290px;

    margin-left: 15px;
}


.my-1 img {
    width: 270px;
}

#Barra-P {
    position: relative;
    left: 75%;
}
</style>