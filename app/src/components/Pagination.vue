<template>
  <b-container>
    <b-row>
     
      <b-col cols="12" sm="4" class="my-1" :key="index" v-for="(item, index) in paginatedItems">

         <img :src="item.url" alt="">
        <!--
        <b-card
          :bg-variant="item.url"
          text-variant="white"
          :header="item.title"
          class="text-center"
        >
      -->
          <p class="card-text">{{item.body}}</p>
        </b-card>
      </b-col>
    </b-row>

    <b-row>
      <b-col md="6" class="my-1">
        <b-pagination
          @change="onPageChanged"
          :total-rows="totalRows"
          :per-page="perPage"
          v-model="currentPage"
          class="my-0"
        />
      </b-col>
    </b-row>
  </b-container>

</template>

<script>
   console.log("ola mundo");
const items = [
  {
    title: "Primary",
    body: "Lorem ipsum dolor sit amet, consectetur adipiscing elit.",
    url: "src/assets/img/img-1.jpg"
  },
  {
    title: "Secondary",
    body: "Lorem ipsum dolor sit amet, consectetur adipiscing elit.",
    variant: "secondary",
    url: "src/assets/img/img-1.jpg"
  },
  {
    title: "Success",
    body: "Lorem ipsum dolor sit amet, consectetur adipiscing elit.",
    variant: "success",
    url: "src/assets/img/img-1.jpg"
  },
  {
    title: "Info",
    body: "Lorem ipsum dolor sit amet, consectetur adipiscing elit.",
    variant: "info",
    url: "src/assets/img/img-1.jpg"
  },
  {
    title: "Warning",
    body: "Lorem ipsum dolor sit amet, consectetur adipiscing elit.",
    variant: "warning",
    url: "src/assets/img/img-1.jpg"
  },
  {
    title: "Danger",
    body: "Lorem ipsum dolor sit amet, consectetur adipiscing elit.",
    variant: "danger",
    url: "src/assets/img/img-1.jpg"
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
</style>
