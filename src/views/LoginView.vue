<template>
    <div>
        <h1>Public API Access</h1>
        <button @click="fetchData">Fetch Data from Public API</button>
        <div v-if="loading">
            <h2>Loading...</h2>
        </div>
        <div v-if="error">
            <h2>Error:</h2>
            <pre>{{ error }}</pre>
        </div>
        <div v-if="data">
            <h2>Response Data:</h2>
            <pre>{{ data }}</pre>
        </div>
    </div>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue'
import axios from 'axios'

export default defineComponent({
    name: 'PublicAPIAccess',
    setup() {
        const data = ref<string | null>(null)
        const error = ref<string | null>(null)
        const loading = ref<boolean>(false)

        const fetchData = async () => {
            loading.value = true
            error.value = null
            data.value = null
            try {
                const response = await axios.post('http://localhost:8080/api/login/username', {
                    username: 'admin',
                    password: 'admin',
                    captcha: 'AxbA',
                  uuid: '12345'
                })

                      /*try {
        const response = await axios.get('http://localhost:8080/open_api/hello');
                        console.log(response.data);*/

                if (response.data.success) {
                    data.value = JSON.stringify(response.data, null, 2)
                } else {
                    error.value = `Error: ${response.data.message}`
                }
            } catch (err) {
                console.error('Error fetching data:', err)
                error.value = 'Error fetching data: ' + err.message
            } finally {
                loading.value = false
            }
        }

        return {
            data,
            error,
            loading,
            fetchData
        }
    }
})
</script>

<style scoped>
h1 {
    color: #333;
}
button {
    margin: 10px 0;
}
pre {
    background: #f4f4f4;
    padding: 10px;
    border-radius: 5px;
}
</style>
