<template>
    <div>
        <table>
            <tr>
                <th>Operating System</th>
                <th>Price</th>
            </tr>
            <tr>
                <td></td>
                <td></td>
            </tr>
        </table>
    </div>
</template>

<script>
    export default {
        name: 'Admin',
        data() {
            return {
                arrayData : JSON.parse(localStorage.getItem('data')),
                // localData: JSON.parse(localStorage.data)
            }
        },
        methods: {
            displayTable() {
                localStorage.getItem('data')
                console.log('localData');
            }
        }
    }
    console.log(arrayData)
</script>

<style scoped>

</style>