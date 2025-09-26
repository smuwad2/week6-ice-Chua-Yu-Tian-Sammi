<script>
    export default { 
        data() {
            return {
                // Add code here
                id: "demo1",
                isClicked: true
                
                
            }
        },
        methods: { 
   			// Add code here
            changeColor(){
                
                if(this.isClicked){
                    return this.isClicked = false;
                } else {
                  
                    return this.isClicked = true;
                }
                
            }
            
		}
    }
</script>

<template>
    
    <!-- Modify code here -->
    <div class="container">
        <div v-bind:id="id" v-bind:class = '{"redBox" :isClicked, "blueBox" :!isClicked}' class="m-2">
            div ID : {{id}} 
        </div>
        
        <button @click="changeColor()" type="button" v-bind:class="{'btn btn-danger' : isClicked, 'btn btn-primary': !isClicked}">Change Color</button>
    </div>

</template>

<style scoped>
    .redBox {
        background-color: red;
    }
    .blueBox {
        background-color: blue;
    }
    #demo1 {
        color: black;
    }
</style>
