<template>
    <nav>
        <img src="@/assets/AROFAH.png" alt="AROFAH.png">
        <ul class="menu-container">
            <li class="menu-item" v-for="juduls in judul" :key="juduls.id">
                <a href="#">
                    {{juduls.title}}
                </a>
                <ul class="drop" v-if="juduls.id=='2'">
                    <li class="drop-item" v-for="subjuduls in subjudul" :key="subjuduls.id" >
                        <a href="#">
                            {{subjuduls.title}}
                        </a>
                    </li>
                </ul>
            </li>
        </ul>    
    </nav>
</template>

<script>
export default {
    data(){
        return{
            judul:[
                {id:1,title:"Home"},
                {id:2,title:"Informasi Jadwal"},
                {id:3,title:"Contact Us"}
            ],
            subjudul:[
                {id:1,title:"Dokter"},
                {id:2,title:"Poli"},
                {id:3,title:"Kamar"}
            ]
        }
    },
};
</script>

<style>
    *{
        padding:0;
        margin:0;
    }
    nav{
        background-color: white;
        box-shadow: 1px 1px 6px 6px rgba(211, 211, 211, 0.178);
        width:100%;
    }
    a{
        text-decoration: none;
        color:#4e9d70;
    }
    .menu-container{
        display: flex;
        justify-content: center;
        list-style: none;

    }
    .menu-item{
        padding:1rem;
    }
    .menu-item:hover{
        background-color: #4e9d7025;
        color:wheat;
    }
    img{
        height:2.5rem;
        width:12rem;
        position: absolute;
        display:flex;
        padding-left: 2rem;
        padding-top:0.2rem;
    }
    .drop{
        display:none;
    }
    .menu-item:hover .drop{
        display: flex;
        flex-direction: column;
        list-style: none;
        position: absolute;
        left:10px;
        align-item: center;
        width:180px;
        margin-top:1.1rem;
        background-color:white;
    }
</style>