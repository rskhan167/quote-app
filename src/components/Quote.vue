<template>
    <div class="QuoteDiv">
        <div class="panel">
            <div class="quote">
                <slot></slot>
            </div>
        </div>
    </div>
</template>


<script>

</script>>

<style>
    .panel{
        font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
        font-size: 24px;
        color: #6e6e6e;
    }
    .QuoteDiv{
        border: #6e6e6e;
    }
    .quote{
        cursor: pointer;
    }
    .quote:hover{
        background-color: #ffe2e2;
    }
</style>