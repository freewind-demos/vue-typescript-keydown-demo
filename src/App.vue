<template>

    <div>
        <input type="text" autofocus placeholder="press up/down/left/right/enter"
               v-on:keydown.up="pressUp()"
               v-on:keydown.right="pressRight()"
               v-on:keydown.down="pressDown()"
               v-on:keydown.left="pressLeft()"
               v-on:keydown.enter="pressEnter()"
        >
        <div>You pressed {{ key }}</div>
    </div>

</template>

<script lang="ts">
    import {Component, Vue} from 'vue-property-decorator'

    @Component({})
    export default class App extends Vue {
        key: string = ''

        pressUp() {
            this.key = 'up arrow'
        }

        pressDown() {
            this.key = 'down arrow'
        }

        pressLeft() {
            this.key = 'left arrow'
        }

        pressRight() {
            this.key = 'right arrow'
        }

        pressEnter() {
            this.key = 'enter'
        }
    }
</script>

<style scoped>
    input {
        width: 400px
    }
</style>
