<template>
  <b-container>
    <b-row
      v-for="row in Math.ceil(survivors.length/5)"
      :key="row.index"
      align-h="center"
      class="row"
    >
      <b-col
        v-for="survivor in survivors.slice((row-1)*5 , row*5)"
        :key="survivor.index"
        align="center"
      >
        <div
          class="survivorCard"
        >
          <h4>
            {{ survivor.name }}
          </h4>
          <img :src="getImage(survivor.image)">
        </div>
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
export default {
  name: 'Index',
  data () {
    return {
      survivors: [
        {
          name: 'Acrid',
          image: 'Acrid.png'
        },
        {
          name: 'Artificer',
          image: 'Artificer.png'
        },
        {
          name: 'Commando',
          image: 'Commando.png'
        },
        {
          name: 'Engineer',
          image: 'Engineer.png'
        },
        {
          name: 'Huntress',
          image: 'Huntress.png'
        },
        {
          name: 'Loader',
          image: 'Loader.png'
        },
        {
          name: 'Mercenary',
          image: 'Mercenary.png'
        },
        {
          name: 'MUL-T',
          image: 'MUL-T.png'
        },
        {
          name: 'REX',
          image: 'REX.png'
        }

      ]
    }
  },
  methods: {
    getImage (image) {
      return require('assets/' + image)
    }
  }
}
</script>

<style>
.survivorCard {
  max-width: 128px;
  border: 1px solid #ccc;
}
</style>
