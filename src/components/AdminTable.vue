<template>
    <div>
        <table>
            <thead>
                <th>Operating System</th>
                <th>Price</th>
            </thead>
            <tbody>
            <tr v-for="item in arrayData" v-bind:key="item">
                <td>{{ item.operatingSystem }}</td>
                <td>R {{ item.price }}</td>
            </tr>
            </tbody>
        </table>
    </div>
</template>

<script>

    export default {
name: 'AdminTable',
        data() {
            return {
                arrayData : JSON.parse(localStorage.getItem('data')),
            }
        },
    }
   
</script>

<style scoped>
table{
    width: 50%;
    margin: 0 auto;
    border: 1px solid black;
}

td{
    border: 2px solid rgb(80, 172, 80);
}
</style>