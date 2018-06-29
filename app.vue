<template>
    <div class="main">
        <!--       <div class="app_in">fang{{msg}}</div>
        <div class="app_out">tang123</div> -->
        <div class="card" v-for="(item,index) in listData">
            <ul>
                <li>{{item.title}}</li>
                <li>{{item.des}}</li>
                <li>{{item.source}}</li>
            </ul>
        </div>
    </div>
</template>
<script type="text/ecmascript-6">
export default {
    data: () => {
        return {
            msg: 'Vue',
            listData: []
        }
    },
    methods: {

    },
    mounted() {

        let item = {title:'news title',des:'news content',source:'news tag'};
        for(let i=0;i<3;i++){
            this.listData.push(item);
        }
        // 跨域
        let url = 'http://api01.bitspaceman.com:8000/news/qihoo?apikey=FWR9Qcf9UMiK0tK3cNxGPFU688OzpQXCnuW9NXoPRa8M4xk5PVHcO5xE77YP590y&kw=白';
        // this.$http.get(url)
        //     .then(function(response) {
        //         console.log(response);
        //         if (response && response.data) {
        //             let list = [];
        //             response.data.forEach(item => {
        //                 list.push({ title: item.title, des: item.content, source: item.posterScreenName })
        //             })
        //             this.listData = list;
        //         }
        //         console.log('list ...',this.listData);
        //     })
        //     .catch(function(error) {
        //         console.log('error ...',error);
        //     });
    }
};
</script>
<!-- tip:  -->
<!-- scoped  if set the css is only apply to this page . else css is global-->
<style scoped lang="scss" rel="stylesheet/scss">
@import "./style.scss";
.main {
    .card {
        background-color: #efefef;
        font-size: rem(14);
        margin: rem(5);
        height: 200px;
    }
}
</style>