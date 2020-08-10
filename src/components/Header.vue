<template>
    <div class="row">
        <div class="col">
            <h3>Quotes Added</h3>
            <div class="progress">
                <div class="progressbar" :style="{width: (quoteCount / maxCount)*100 + '%'}">
                    {{ quoteCount }} / {{ maxCount }}
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props: ['quoteCount', 'maxCount']
}
</script>>

<style scoped>
    .progress{
        height: 20px;  /* Can be anything */
        position: relative;
        background: #555;
        -moz-border-radius: 25px;
        -webkit-border-radius: 25px;
        border-radius: 25px;
        padding: 10px;
        
    }
    .progressbar{
        display: block;
        height: 100%;
        border-top-right-radius: 8px;
        border-bottom-right-radius: 8px;
        border-top-left-radius: 20px;
        border-bottom-left-radius: 20px;
        background-color: cadetblue;
        position: relative;
        overflow: hidden;
        text-align: center;
        color: white;
    }
    
</style>