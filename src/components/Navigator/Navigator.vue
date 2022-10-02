<template>
    <div className = "menu"  >
        <img  alt = "icon"/>
    </div>
    <div className="navigator" >
        <div className = "logo">
            <img src = {logo} alt = "logo"/>
        </div>
        <div className = "navigations">
            <ul>
                <li> 
                    <img  alt="icon" :src = "dashboard"/>
                    <span>Dashboard</span>
                </li>
                <li> 
                    <img  alt="icon" :src = "procurement"/>
                    <span> Procurement </span>
                </li>
                <li> <img :src="box" alt="icon" /><span>Invoice Center</span></li>
                <li> <img :src="analytics" alt="icon" /><span>Recieving Center</span></li>
                <li> <img :src="packages" alt="icon" /><span>User Managment</span></li>
                <li> <img :src="packages" alt="icon" /><span>Supplier Managment</span></li>
            </ul>
        </div>
    </div>
</template>

<script setup>
    import logo from "../images/one.png"
    import box from "../images/box.png"
    import procurement from "../images/procurement.png"
    import procurement1 from "../images/procurement(1).png"
    import packages from "../images/packages.png"
    import analytics from "../images/analytics.png"
    import dashboard from "../images/dashboards.png"
    import dashboard1 from "../images/dashboards(1).png"
    import menue from "../images/smenu.png"
    import smenue from "../images/menu.png"
</script>

<style lang="scss" scoped>

</style>