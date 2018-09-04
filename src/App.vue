<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <h2>{{homeTeamName}}</h2>
    <input type="text" v-model="homeTeamName">
    <p>{{countHomeTeam}}</p>
    <button v-on:click="addOneHomeTeam">Add 1</button>
    <button v-on:click="removeOneHomeTeam">Remove 1</button>
    <br>
    <h2>{{awayTeamName}}</h2>
    <input type="text" v-model="awayTeamName">
    <p>{{countAwayTeam}}</p>
    <button v-on:click="addOneAwayTeam">Add 1</button>
    <button v-on:click="removeOneAwayTeam">Remove 1</button>
    <br>
  </div>
</template>

<script>
export default {
    name:"count",
    data:function(){
        return {
            countHomeTeam:0,
            countAwayTeam:0,
            homeTeamName:"Home Team Name",
            awayTeamName:"Away Team Name",
        }
    },
    methods:{
        addOneHomeTeam:function(){
            console.log("add 1 was clicked")
            this.countHomeTeam++;
        },
        removeOneHomeTeam:function(){
            console.log("remove 1 was clicked")
            this.countHomeTeam-=1;
        },
        addOneAwayTeam:function(){
            console.log("add 1 was clicked")
            this.countAwayTeam++;
        },
        removeOneAwayTeam:function(){
            console.log("remove 1 was clicked")
            this.countAwayTeam-=1;
        },

    }
}
</script>




<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
