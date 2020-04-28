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
        {{ survivor.name }}
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
          name: 'Acrid'
        },
        {
          name: 'Artificer'
        },
        {
          name: 'Commando'
        },
        {
          name: 'Engineer'
        },
        {
          name: 'Huntress'
        },
        {
          name: 'Loader'
        },
        {
          name: 'Mercenary'
        },
        {
          name: 'MULL-T'
        },
        {
          name: 'REX'
        }

      ]
    }
  },
  created () {
  }
}
</script>

<style>

</style>
