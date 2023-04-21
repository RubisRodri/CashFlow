<template>
    <div>
        <Layout>
            <template #header>
                <Header></Header>
            </template>
        </Layout>
    </div>
</template>

<script>
import Layout  from './Header.vue'
import Header from './Layout.vue'

export default {
    components: {
        Layout,
        Header,
    }

}
</script>
