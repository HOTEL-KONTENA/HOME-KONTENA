<template>
  <div>
    <ApolloQuery ref="GQLQueryOrg" :query="require('@/gql/org/Orgs.gql')" :variables="{id: 1 }" fetch-policy='no-cache' @result="(res) => {dtOrg = res.data.Orgs.data[0]}" @error="() => { error({statusCode: 404}) }"><template v-slot="{}"></template></ApolloQuery>

    <div class="top-title" v-if="dtOrg">
      <img src="/logo.png" class="img-fluid d-inline-block align-top" alt="" />
    </div>
    <div class="row pt-3 w-100 ml-0 align-item-center footer-title" style="position: absolute; bottom: 0px;">
      <div class="col-6 text-right" v-if="dtOrg">
        <p class="text-secondary small">{{dtOrg.address}} <br/>{{dtOrg.city}}, {{dtOrg.province}}</p>
      </div>
      <div class="col-6">
        <h6 class="text-secondary mt-1">HOTELKONTENA.COM</h6>
      </div> 
    </div>
    <b-carousel v-if="dtOrg"
      id="carousel-fade"
      style="text-shadow: 0px 0px 2px #000"
      max-width="100%"
      height="100vh"
      controls
      fade
      indicators
    >
      <b-carousel-slide v-for="item in dtOrg.promos"
        caption=""
        :img-src="item.photo_url"
        style="height: 100vh !important"
      ></b-carousel-slide>
    </b-carousel>
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  components: {
    Logo
  },
  data () {
    return {
      dtOrg: null
    }
  }
}
</script>

<style>
  h6 {
    /*font-family: Biko;*/
    font-size: 1.2rem;
    letter-spacing: .2rem;
    font-weight: 400;
  }
  .top-title {
    position: fixed;
    top: 0;
    left: 3rem;
    width: 7rem;
    padding: 20px;
    height: 5rem;
    background-color: #fcfcfc;
    border: .5px solid #000;
    border-top: 0;
    z-index: 999999;
  }
  .footer-title {
    position: absolute;
    background-color: #fcfcfc;
    border: .5px solid #000;
    border-top: 0;
    bottom: 0;
    z-index: 999;
  }
</style>
