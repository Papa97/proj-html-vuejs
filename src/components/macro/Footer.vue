<template>
    <footer>
        <Subscription/>
        <GeneralFooter :posts='postArray' :tags='tagsArray'/>
        <BotttomFooter/>
    </footer>
</template>

<script>
import Subscription from '../elements/Subscription.vue';
import GeneralFooter from '../elements/GeneralFooter.vue';
import BotttomFooter from '../elements/BottomFooter.vue';

export default {
    name:'Footer',
    components : {
        Subscription,
        GeneralFooter,
        BotttomFooter
    },
    data () {
        return {
            postArray : [
                'Aenean lobortis sapien enim viverra',
                'Duis ac massa semper maximus',
                'Nunc fermint nulla eu justo sem id',
                'Aliquam posuere magna eget nibh',
                'Cras ac nulla ac consecte rutrum',
                'Fusce mattis nunc ut aliquam'
            ],
            tagsArray : [
                'Black',
                'boots',
                'Brown',
                'Casual',
                'D&G',
                'Fabric',
                'flowers',
                'Grey',
                'hat',
                'Hipster',
                'lines',
                'multi-purpose',
                'New-York',
                'Outdoors',
                'red',
                'responsive',
                'summer',
                'sweater',
                'Travel',
                'Warm',
                'White',
                'winter'
            ]
        }
    }
}
</script>

<style>

</style>