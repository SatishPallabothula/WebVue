<template>
    <div class="Rentalbox">
        <div class = "Rent" v-for="Rental in Rental" :key="Rental.id">
            <Item :Rental="Rental"/>
        </div>

    </div>
    


</template>

<script>

    import Item from './Item.vue'


    export default{
        name: 'RentalBox',
        components: {
            Item
        },
        props:{
            
            Rental: Array
        }
    }

</script>

<style scoped>
.Rentalbox{


background-color: lightgreen;
color: lightblue;
display: grid;
grid-template-columns: 1fr 1fr 1fr;
border:3px solid rgb(29, 70, 127)
}

.Rent{
    display: grid;
    text-align: center;
}

</style>