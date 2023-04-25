<template>
    <Layout>
        <template #header>
            <Header></Header>
        </template>
        <template #resume>
            <Resume
            :label="'Ahorro Total'"
            :totalAmount="'10000000000'"
            :amount="amount"
            >
                <template #graphic>
                    graphic
                </template>
                <template #action>
                    action
                </template>
            </Resume>
        </template>
        <template #movements>
            <Movements
            :movements="movements"
            />
        </template>

    </Layout>
</template>

<script>
import Layout from "./Layout.vue";
import Header from "./Header.vue";
import Resume from "./Resume/Index.vue";
import Movements from "./movements/Index.vue";

export default {
    components: {
    Layout,
    Header,
    Resume,
    Movements,
},
    data(){
        return {
            label:null,
            amount:null,
            movements:[{
                id:0,
                title:"movimiento",
                description:"lorem ipsum dolor sit amet, consectetur",
                amount:1000,
            }, {
                id:0,
                title:"movimiento",
                description:"lorem ipsum dolor sit amet, consectetur",
                amount:1000,
            },{
                id:0,
                title:"movimiento",
                description:"lorem ipsum dolor sit amet, consectetur",
                amount:1000,
            },{
                 id:0,
                title:"movimiento",
                description:"lorem ipsum dolor sit amet, consectetur",
                amount:1000,
             }],
        }
    }
};
</script>
