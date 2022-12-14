<template>
    <div>
        <button v-on:click="displayData">Display Data</button>
        <div class="container">
            <div v-for="items in localData" :key="item">
                <div class="card">
                    <img :src="items.image" alt="">
                    <h4>
                    {{ items.operatingSystem }}
                    </h4>
                    <p>
                    R{{ items.price }}
                    </p>
                    <button v-on:click="displayData()">Purchase</button>
                </div>
            </div>
        </div>
    </div>
</template>

<script>

export default {
    data() {
        return {
            arrayData: [
                {
                    operatingSystem: "Windows 10",
                    price: 1200,
                    image: "https://i.postimg.cc/zByxfDBX/Windows.jpg"
                },
                {
                    operatingSystem: "Ubuntu Linux",
                    price: 980,
                    image: "https://i.postimg.cc/QMx6RJZ7/Linux.jpg"
                },
                {
                    operatingSystem: "Mac",
                    price: 2000,
                    image: "https://i.postimg.cc/25cHmLCK/Mac.jpg"
                }
            ],

            localData: JSON.parse(localStorage.data)


        };
    },
    methods: {
        displayData() {
            localStorage.setItem('data', JSON.stringify(this.arrayData));
            console.table(JSON.parse(localStorage.data))
            alert('Purchase successful');
        }
    },

}
</script>

<style scoped>
.card {
    border: 1px solid black;
    border-radius: 35px;
    width: 18rem;
    height: 22rem;
    margin: 15px;
    padding: 10px;
}

.card  img {
    height: 200px;
    width: 200px;
    object-fit: contain;
}

.card button{
    padding: 10px;
    border-radius: 10px;
}

.card button:hover{
    background-color: lightgreen;
    transition: 2s;
}

.container {
    display: flex;
    flex-direction: row;
    justify-content: center;
}
</style>