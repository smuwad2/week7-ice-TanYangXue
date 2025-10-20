<script>

    export default { 
        // Add code in appropriate places
        data() {
            return {
                items: ['keyboard', 'mouse', 'iPhone', 'macbook', 'adapter'],
                newItem: "",
            }
        },
        methods: {
            removeItem(index) {
                this.items.splice(index, 1)
            },
            addItem() {
                this.items.push(this.newItem);
            }
        }
        

    }
</script>

<template>

    <h2>Shopping Cart</h2>
    <!-- TODO: Add Code Here -->
     <ul>
        <li v-for="item, index in items">{{item}}<button v-on:click="removeItem(index)">Delete!</button></li>
     </ul>

     <input v-model=newItem></input><button v-on:click="addItem()">Add!</button>
   
</template>
