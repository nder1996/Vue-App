<template>
    <b-container>
        <h2 class="P-Letra">Últimos Afiliados</h2>
        <p id="linea-p"></p>
        <b-row class="Marco">
            <b-col cols="12" sm="2" class="my-1" :key="index" v-for="(item, index) in paginatedItems">
                <div :class="{[`img_${item.id}`]: true}">
                </div>
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
        id: "1",
        body: "Agentes Inmobiliarios",
        url: "src/assets/img/img-1.jpg"
    },
    {
        id: "2",
        body: "Nelly Carrillo",
        url: "src/assets/img/img-2.jpg"
    },
    {
        id: "3",
        body: "Premium Rent a Car",
        url: "src/assets/img/img-3.jpg"
    },
    {
        id: "4",
        body: "Maria Teresa López Psicoterapeuta",
        url: "src/assets/img/img-4.jpg"
    },
    {
        id: "5",
        body: "Grupo Integral Consultor",
        url: "src/assets/img/img-5.jpg"
    },
    {
        id: "6",
        body: "Lunazul Virtual Shop",
        url: "src/assets/img/img-6.jpg"
    },
    {
        id: "7",
        body: "Coworking en Pereira",
        url: "src/assets/img/img-7.jpg"
    },
    {
        id: "8",
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

.img_1 {
    background-image: url('../assets/img/img-1.jpg');
   
}

.img_1:hover{
 
    background-image: url('../assets/img/img-11.jpg');
 
}


.img_2 {
   
    background-image: url('../assets/img/img-2.jpg');
  
}

.img_2:hover{
    
    background-image: url('../assets/img/img-22.jpg');
  
}

.img_3 {
    
    background-image: url('../assets/img/img-3.jpg');

}

.img_3:hover{
 
    background-image: url('../assets/img/img-33.jpg');
   
}

.img_4 {
   
    background-image: url('../assets/img/img-4.jpg');
 
}

.img_4:hover{
 
    background-image: url('../assets/img/img-44.jpg');
 
}

.img_5 {
   
    background-image: url('../assets/img/img-5.jpg');
   
}

.img_5:hover{
 
    background-image: url('../assets/img/img-55.jpg');
   
}


.img_6 {
   
    background-image: url('../assets/img/img-6.jpg');
   
}

.img_6:hover{

    background-image: url('../assets/img/img-66.jpg');
   
}

.img_7 {
   
    background-image: url('../assets/img/img-7.jpg');
   
}

.img_7:hover{
   
    background-image: url('../assets/img/img-77.jpg');
    
}

.img_8 {
   
    background-image: url('../assets/img/img-8.jpg');
  
}

.img_8:hover{
   
    background-image: url('../assets/img/img-88.jpg');

}

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
    margin-bottom: 25px;
}

.my-1 {
  text-align: center;
    width: 290px;
    margin-left: 15px;
}


.my-1 div {
  text-align: center;
  width: 265px;
  height:267px;
}

#Barra-P {
    position: relative;
    left: 75%;
}
</style>