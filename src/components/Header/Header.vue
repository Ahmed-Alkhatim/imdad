<template>
    <div class="header"  @click="closeAll">

        <div class="searcher">
            <input name = "searcher"  placeholder = "search for Supplier" />
        </div>

        <div class="icons">
            <span>
                <img :src= "check" alt = "icon"/>
            </span>
            <span>
                <img :src="chatting"  alt = "icon" @click.stop = "toggleChatDisplay"/>
                <span  class="notify">2</span>
                <div v-show = "chatDisplay" class = "notify-box" >
                <Messages :messages="messages"/>
                </div>
                <div  v-show = "chatDisplay" class="pointer"></div>
            </span>
            <span>
                <img  @click.stop="toggleNotDisplay" :src="bell"  alt = "icon"  />
                <span  class="notify">2</span>
                <Notification v-show = "notificationDisplay" />
                <div v-show = "notificationDisplay" class="pointer"></div>
            </span>
            <span>
                <img :src="warning"  alt = "icon"/>
            </span>
        </div>

        <div class="profile">
            <div class="user">
                <h2>Ahmed alkhatim</h2>
                <p>ًEdit profile</p>
            </div>
            <div class="img-container">
                <img :src= "user" alt= "profile"/>
            </div>
        </div>

    </div>
</template>

<script setup>
    import { onMounted, ref, } from "vue"
    import Messages from "./Messages.vue"
    import Notification from "./Notification.vue"
    
    // images
    import bell from "../images/bell.png"
    import chatting from "../images/chatting1.png"
    import check from "../images/check.png"
    import warning from "../images/warning.png"
    import user from "../images/user.png"

    const chatDisplay = ref(false)
    const notificationDisplay = ref(false)
  
    const messages = ref(
        [
            { name : "Ahmed", last_message : "Hello how are you "},
            { name : "Khalid", last_message : "Here we are"},
            { name : "Amin", last_message : "The last messge"}
        ]
    )

    function toggleChatDisplay()  {
        chatDisplay.value = !chatDisplay.value
        notificationDisplay.value = false
    }
    function toggleNotDisplay() {
        notificationDisplay.value = !notificationDisplay.value
        chatDisplay.value = false
    }
    function closeAll() {
        chatDisplay.value = false
        notificationDisplay.value = false
    }
    onMounted( () => {
        document.getElementsByClassName("page")[0].addEventListener( "click", () =>{
            chatDisplay.value = false
            notificationDisplay.value = false
        })
    })
</script>

<style lang="scss" scoped>

</style>