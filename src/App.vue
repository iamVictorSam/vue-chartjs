<template>
  <h1>{{ polarName }}</h1>
  <Chart :type="polar" :data="polarData" />
</template>

<script>
import Chart from './components/Chart.vue'


export default {
  name: 'App',
  components: {
    Chart,
  },
  data() {
    return {
      barName: 'Bar Chart',
      bar: 'bar',
      barData: {
        labels: ['Isaac', 'Morah', 'Sam', 'Jess', 'Suka'],
        datasets: [{
          label: 'Score between 5 pupils',
          data: [10, 4.8, 17.7, 20, 14],
          backgroundColor: [
            'rgba(17, 50, 64, 0.4)',
            'rgba(94, 72, 0, 0.4)',
            'rgba(171, 122, 232, 0.4)',
            'rgba(27, 25, 169, 0.4)',
            'rgba(141, 47, 108, 0.4)'
          ],
          borderColor: [
            'rgba(17, 50, 64, 1)',
            'rgba(94, 72, 0, 1)',
            '	rgba(171, 122, 232, 1)',
            'rgba(27, 25, 169, 1)',
            'rgba(141, 47, 108, 1)'
          ],
          borderWidth: 2
        }]
      },

      doughnutName: 'Doughnut Chart',
      doughnut: 'doughnut',
      doughnutData: {
        labels: ['Sleep', 'Gym', 'Code', 'Nap', 'Hike'],
        datasets: [{
          label: 'My Daily Activiy',
          data: [7, 2.5, 8, 1.5, 1],
          backgroundColor: [
            'purple ',
            'gold',
            'teal',
            'skyblue',
            'grey'
          ],
          borderWidth: 1,
          hoverOffset: 8
        }]
      },

      polarName: 'Polar Area Chart',
      polar: 'polarArea',
      polarData: {
        labels: ['JavaScript', 'Dart', 'C#', 'Typescript', 'Rust'],
        datasets: [{
          label: 'Programming Language Strength',
          data: [13, 15, 4, 8, 7],
          backgroundColor: [
            'yellow',
            'skyblue',
            'lightgreen',
            'blue',
            'orange'
          ],

          borderWidth: 5
        }]
      }
    }

  },


}


</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
