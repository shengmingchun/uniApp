<template>
	 <view class="content">
        <mSearch :show="false" radius="5"  backgroundColor="#ff5a5f" border='1px #999 solid'></mSearch>
    </view>
</template>

<script>
	 import mSearch from '@/components/mehaotian-search/mehaotian-search.vue';
 export default {
    components: {
        mSearch
    },
    data() {
        return {
			
		};
    },

    methods: {
        search(e, val) {
            console.log(e, val);
            this['val'+val] = e;
        }
    }
 };
</script>

<style>
</style>
