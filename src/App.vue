<script>

export default {
    data() {
        return {
            visor: '0',
            resultado: 'r',

        }
    },

    methods: {
        clear() {
            this.visor = '0'
            this.resultado = '0'
        },

        append(n) {
            if (this.visor == '0') {
                this.visor = n
            } else {
                this.visor = this.visor + n
            }
        },

        display() {
            this.resultado = eval(this.visor)
            this.visor = this.resultado
        }
    }
}

</script>

<template>

    <div id="body" class="d-flex justify-content-center w-100">
        <div style="max-width:20rem">

            <div class="border border-3 border-primary rounded " id="result">
                <h1 class="text-end m-2">{{ visor }}</h1>
            </div>

            <div class="row calculadora">
                <div class="col-12 d-flex justify-content-between mt-4 pe-1">
                    <div class=" my-1 "><button @click="clear()" class="btn btn-primary btn-circle btn-xl ">C</button>
                    </div>
                    <div class=" my-1 "><button @click="append('/')"
                            class="btn btn-primary btn-circle btn-xl ">/</button></div>
                </div>

                <div class=" my-1 col-3"><button @click="append('7')"
                        class="btn btn-secondary btn-circle btn-xl ">7</button></div>
                <div class=" my-1 col-3"><button @click="append('8')"
                        class="btn btn-secondary btn-circle btn-xl ">8</button></div>
                <div class=" my-1 col-3"><button @click="append('9')"
                        class="btn btn-secondary btn-circle btn-xl ">9</button></div>
                <div class=" my-1 col-3"><button @click="append('*')"
                        class="btn btn-primary btn-circle btn-xl ">x</button></div>

                <div class=" my-1 col-3"><button @click="append('4')"
                        class="btn btn-secondary btn-circle btn-xl ">4</button></div>
                <div class=" my-1 col-3"><button @click="append('5')"
                        class="btn btn-secondary btn-circle btn-xl ">5</button></div>
                <div class=" my-1 col-3"><button @click="append('6')"
                        class="btn btn-secondary btn-circle btn-xl ">6</button></div>
                <div class=" my-1 col-3"><button @click="append('-')"
                        class="btn btn-primary btn-circle btn-xl ">-</button></div>

                <div class=" my-1 col-3"><button @click="append('1')"
                        class="btn btn-secondary btn-circle btn-xl ">1</button></div>
                <div class=" my-1 col-3"><button @click="append('2')"
                        class="btn btn-secondary btn-circle btn-xl ">2</button></div>
                <div class=" my-1 col-3"><button @click="append('3')"
                        class="btn btn-secondary btn-circle btn-xl ">3</button></div>
                <div class=" my-1 col-3"><button @click="append('+')"
                        class="btn btn-primary btn-circle btn-xl ">+</button></div>

                <div class="col-12">
                    <div class=" row">
                        <div class=" my-1 col-3 "><button @click="append('0')"
                                class="btn btn-secondary btn-circle btn-xl ">0</button></div>
                        <div class=" my-1 col-3 "><button @click="append('.')"
                                class="btn btn-secondary btn-circle btn-xl ">.</button></div>
                        <div class=" my-1 col-6 pe-0"><button @click="display()" class="btn btn-primary btn-circle btn-xl w-100 ">=</button></div>
                    </div>
                </div>

            </div>

        </div>
    </div>

</template>
<style>
.btn-circle.btn-xl {
    width: 70px;
    height: 70px;
    padding: 10px 16px;
    border-radius: 35px;
    font-size: 24px;
    line-height: 1.33;
}

.btn-circle {
    width: 30px;
    height: 30px;
    padding: 6px 0px;
    border-radius: 15px;
    text-align: center;
    font-size: 12px;
    line-height: 1.42857;
}
</style>
