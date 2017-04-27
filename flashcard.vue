<template>
<div>
    <div @click="isToggle=!isToggle" v-bind:style="{backgroundColor: colorFront}"  v-show="isToggle" class="animated flipInX k-border flashcard">
        <div class="card-header white"> {{headerFront}} </div>
        <div class="card-content center ">
            <h1>{{front}}</h1>
             <img v-if="imgFront!=''" :src="imgFront" width="200" height="200">
         </div>
        <div class="card-footer white" style="">{{footerFront}}</div>
    </div>
    <div @click="isToggle=!isToggle" v-bind:style="{backgroundColor: colorBack,color: 'white'}" v-show="!isToggle" class="animated flipInX flashcard">
        <div class="card-header"> {{headerBack}}</div>
        <div class="card-content center">
            <h1>{{back}}</h1>
             <img v-if="imgBack!=''" :src="imgBack" width="200" height="200">
        </div>
        <div class="card-footer">{{footerBack}}</div>
    </div>
</div>

</template>
<script>
export default {
    data() {
        return {
            isToggle: false,
        }
    }, props: {
        imgFront: {
            type: String,
            default: ''
        },
        imgBack: {
            type: String,
            default: ''
        },
        front: {
            type: String,
            default: ''
        },
        back: {
            type: String,
            default: ''
        },
        colorFront: {
            type: String,
            default: 'white'
        },
        colorBack: {
            type: String,
            default: 'indigo'
        },
        headerFront: {
            type: String,
            default: 'Info'
        },
        headerBack: {
            type: String,
            default: 'Answer'
        },
        footerFront: {
            type: String,
            default: 'Click to show Back'
        },
        footerBack: {
            type: String,
            default: 'Click to show Front'
        }


    }
}
</script>
<style scoped>
.flashcard {
    cursor: pointer;
    border-radius: 10px;
    margin: 20px;
    padding: 25px;
    box-shadow: 0 0px 10px rgba(0, 0, 0, 0.4);
    text-align: center;
}

.flashcard:hover {
    box-shadow: 0 0px 25px rgba(0, 0, 0, 0.8);
}

.animated {
    animation-duration: 1s;
    animation-fill-mode: both;
}

@keyframes flipInX {
    from {
        transform: perspective(400px) rotate3d(1, 0, 0, 90deg);
        animation-timing-function: ease-in;
        opacity: 0;
    }
    40% {
        transform: perspective(400px) rotate3d(1, 0, 0, -20deg);
        animation-timing-function: ease-in;
    }
    60% {
        transform: perspective(400px) rotate3d(1, 0, 0, 10deg);
        opacity: 1;
    }
    80% {
        transform: perspective(400px) rotate3d(1, 0, 0, -5deg);
    }
    to {
        transform: perspective(400px);
    }
}

.flipInX {
    backface-visibility: visible !important;
    animation-name: flipInX;
}
</style>
