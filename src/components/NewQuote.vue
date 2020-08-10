<template>
    <div class="row">
        <form>
            <div class="title">
                <label>Quote</label>
                <textarea class="form-control" rows="3" v-model="quote"></textarea>
            </div>
            <div class="inputfield">
                <button class="btn" @click.prevent="createNew">Add Quote</button>
            </div>
        </form>
    </div>
</template>


<script>

export default {
    data: function(){
        return {
            quote: ''
        };
    },
    methods: {
        createNew() {
            this.$emit('quoteAdded', this.quote);
            this.quote = '';
        }
    }    
}
</script>

<style scoped>
    div{
        font-size:20px;
        text-align: center;
        padding: 10px;
    }
    .title{
        font-size: 30px;
        text-align: center;
    }
    label{
        margin: 10px;
    }
</style>