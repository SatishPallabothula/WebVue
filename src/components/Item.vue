<template>

    <div class ="car" >
        <ul><h1 class = "Rental"> COMPANY NAME : {{Rental.CompanyName}}</h1></ul>
        <ul><h1 class = "Rental"> MODEL NAME : {{Rental.sModelName}}</h1></ul>
        <ul><h1 class = "Rental"> MANUFACTURED YEAR : {{Rental.ManufacturedYear}}</h1></ul>
        <ul><h1 class = "Rental"> MILEAGE(MILES) : {{Rental.Mileage}}</h1></ul>
        <ul><h1 class = "Rental"> PRICE(USD)  :  {{Rental.Price}}</h1></ul>
    </div>

</template>

<script>


export default{
    name: 'RentalItem',
    props:{
        Rental: Array
    }
}


</script>

<style scoped>


h1{
    margin: 2px;
}

div{
    background-color: lightgreen;
    color: black;
    padding: 1em;
    font-size: x-small;
}

.car{
    background-color:  lightgreen;
    color:rgb(2, 7, 16);
    padding: 1em;
    border:3px solid rgb(100, 146, 211);
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
    width:100%;
    height:250px;
    word-wrap: break-word;
    font-size: 10px;
}

</style>
