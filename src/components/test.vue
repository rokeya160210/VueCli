<template>
<div>
      <h2>Welcome</h2>
        <form class="jumbrotn container">
             
            <input type="text" name="text" v-model="input.text"  placeholder="Enter text"   />   <br><br>          
                         
            <input type="number" name="number" v-model="input.number" placeholder="Enter number"  /><br><br>    
                
             <button type="button" v-on:click="show()">Show</button>
                                  
        </form>
       
</div>
    
</template>
<script>


export default {
  name: 'test',
  components: {
    
  },
  data() {
            return {
                input: {
                    text: "",
                    number: "",
                }
            }
        },
  methods:{
        show: function(){
           // var text1 = this.input.text;
           // var number2 = this.input.number;
            //console.log(text1);
             //console.log(number2);
            
            var n = this.input.number;
        
          for (let i = 0; i < n; i++) {
            let div = document.createElement('div');
            div.innerHTML = this.input.text;
             document.body.appendChild(div);
          }

        },
     
      
  }

}
</script>
<style scoped>

</style>
