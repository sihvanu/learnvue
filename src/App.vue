<script>
export default {
    data() {
        return {
            items: ['piim',
                'sai',
                'viin',
                'õlu'],
            message: '',
            count: 0

        }
    },
    methods: {
        addItem() {
            if (this.message.trim() !== '') {
                this.items.push(this.message);
                this.message = '';
            }
        }
    }
}

</script>


<template>
    <div>
        <input type="text" v-model="message" />

        <p>Message is: {{ message }}</p>

        <button @click="addItem">Lisa ülesanne</button>
        <ul>
            <li v-for="(item, index) in items" :key="index">
                {{ item }}
            </li>
        </ul>

        <button @click="count++">You clicked me {{ count }} times.</button>
    </div>
</template>
