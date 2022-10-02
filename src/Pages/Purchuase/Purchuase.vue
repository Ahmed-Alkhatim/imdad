<template>
    <div class = "content">
        <Header />
        <div class="purchuase page">
            <div class = "orders">
                <div class="headers">
                    <h2>{{page}}</h2>
                </div>
                <div class="statistics">
                    <div class = "statistic "  
                        :class="page === 'View RFQ' ? 'activepurch' : ''" 
                        @click = "setPage('View RFQ')"
                    >
                        <div>
                            <div  class="icon">
                                <img :src="down" alt = "icon"/>
                            </div>
                        </div>
                        <div>
                            <h6>5</h6>
                            <p>View RFQ</p>
                        </div>

                    </div>

                    <div class = "statistic " 
                        :class="page === 'Purchuase Oreders' ? 'activepurch' : ''" 
                        @click = "setPage('Purchuase Oreders')"
                    >

                        <div>
                            <div  class="icon">
                                <img :src="down" alt = "icon"/>
                            </div>
                        </div>
                        <div>
                            <h6>5</h6>
                            <p>Purchuase Oreders</p>
                        </div>

                    </div>

                    <div class = "statistic" 
                        :class="page === 'Saved RFQ' ? 'activepurch' : ''" 
                        @click = "setPage('Saved RFQ')"
                    >
                        <div>
                            <div  class="icon">
                                <img :src="key" alt = "icon"/>
                            </div>
                        </div>
                        <div>
                            <h6>5</h6>
                            <p>Saved RFQ</p>
                        </div>
                        
                    </div>
                </div>
            </div>

            <div class="tables">
            </div>

            <div class="tables">
            </div>
        </div>
    </div>
    <Navigator />
</template>

<script setup>
    import { ref } from 'vue';
    import { Header, Navigator } from '../../components';

    //images
    import key from "../../images/key.png"
    import down from "../../images/down-arrow.png"
    import circle from "../../images/circle.png"
    import mark from "../../images/save.png"
    import half from "../../images/half.png"

    const page = ref("Purchuase Oreders")

    const setPage = (value) => {
        page.value = value
    }

</script>

<style lang="scss" scoped>

</style>