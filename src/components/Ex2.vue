<script>

    export default { 
        // Add code in appropriate places
        data() {
            return {
                items: ['keyboard', 'mouse', 'iPhone', 'macbook', 'adapter'],
                newItem: "Candy",
            }
        },

        methods: {
            deleteParent(index) {
                this.items.splice(index, 1);
            },
            addItem() {
                const itemName = this.newItem;
                this.items.push(itemName);
            }
        }

        

    }
</script>

<template>

    <h2>Shopping Cart</h2>
    <!-- TODO: Add Code Here -->
     <ul id="itemList">
        <li v-for="item, index in items" :key="index">
            {{ item }}<button v-on:click="deleteParent(index)">Delete!</button>
        </li>
     </ul>
     <input type="text" v-model="newItem"></input><button v-on:click="addItem">Add!</button>
   
</template>
