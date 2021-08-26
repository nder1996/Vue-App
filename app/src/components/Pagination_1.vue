<template>
   <div id="app">
        <!-- Resultados -->        
        <ul class="list-group">
            <li class="list-group-item text-center" v-for="(user, index) in users" v-show="(pag - 1) * NUM_RESULTS <= index  && pag * NUM_RESULTS > index">
                {{ user.name }} - {{ user.email }}
            </li>
        </ul>
        <!-- Controles -->        
        <nav aria-label="Page navigation" class="text-center">
            <ul class="pagination text-center">
                <li>
                    <a href="#" aria-label="Previous" v-show="pag != 1" @click.prevent="pag -= 1">
                        <span aria-hidden="true">Anterior</span>
                    </a>
                </li>
                <li>
                    <a href="#" aria-label="Next" v-show="pag * NUM_RESULTS / users.length < 1" @click.prevent="pag += 1">
                        <span aria-hidden="true">Siguiente</span>
                    </a>
                </li>
            </ul>
        </nav>
    </div>
</template>
<script type="text/javascript">
    

   export default{
            name: 'Pagination_1',
            data(){
                return{
                                    NUM_RESULTS: 3, // Numero de resultados por página
                pag: 1, // Página inicial
                // JSON a mostrar
                users: [{
                        "id": 1,
                        "name": "Leanne Graham",
                        "email": "Sincere@april.biz"
                    },
                    {
                        "id": 2,
                        "name": "Ervin Howell",
                        "email": "Shanna@melissa.tv"
                    },
                    {
                        "id": 3,
                        "name": "Clementine Bauch",
                        "email": "Nathan@yesenia.net"
                    },
                    {
                        "id": 4,
                        "name": "Patricia Lebsack",
                        "email": "Julianne.OConner@kory.org"
                    },
                    {
                        "id": 5,
                        "name": "Chelsey Dietrich",
                        "email": "Lucio_Hettinger@annie.ca"
                    },
                    {
                        "id": 6,
                        "name": "Mrs. Dennis Schulist",
                        "email": "Karley_Dach@jasper.info"
                    },
                    {
                        "id": 7,
                        "name": "Kurtis Weissnat",
                        "email": "Telly.Hoeger@billy.biz"
                    },
                    {
                        "id": 8,
                        "name": "Nicholas Runolfsdottir V",
                        "email": "Sherwood@rosamond.me"
                    },
                    {
                        "id": 9,
                        "name": "Glenna Reichert",
                        "email": "Chaim_McDermott@dana.io"
                    },
                    {
                        "id": 10,
                        "name": "Clementina DuBuque",
                        "email": "Rey.Padberg@karina.biz"
                    }
                ]
            }
        }
                }

</script>
<style>
#container {
    border: 5px solid red;
    /*display:flex;
    justify-content:center;*/
    text-align: center;
    margin-bottom: 25px;
    margin-top: 25px;

}

.no-box {
    padding-left: 30px;
    font-size: 40px;
}

.btn {
    background-color: rgb(179, 179, 179);
}

.btn:hover {
    color: white;
    background-color: green;
}

.Card-Principal{
    border:5px solid red;
    margin:auto;

}
</style>


