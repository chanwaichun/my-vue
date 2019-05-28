<template>
    <div class="test">
        <div class="nav clearfix">
            <ul>
                <li v-for="(item,index) in list" :key="index" @mouseover="show($event,index)" @mouseleave="hide($event,index)">{{item}}</li>
            </ul>
        </div>
    </div>
</template>
<script>
export default {
     name:'test',
     data()
     {
         return({
             list:[1,2,3,4],
             currentIndex:null,
         })
     },
     methods:
     {
         show(event,index)
         {

             this.currentIndex = index;
          
             event.target.style.transition="all 1s";
             event.target.style.backgroundColor="red";
             event.target.style.height="100px";

         },
         hide(event,index)
         {
             this.currentIndex = index;
             event.target.style.transition="all 1s";
             event.target.style.backgroundColor="white";
             event.target.style.height="40px";
         }
        
     }   
}
</script>
<style lang="scss" scoped>
    .test
    {
        width: 100%;

        .nav
        {
            width:1000px;
            margin:0 auto;
            ul
            {
                float:right;
                li
                {
                    text-align: center;
                    height: 40px;
                    width: 100px;
                    line-height: 40px;
                    float:left;
                    // list-style: none;
                }
            }
        }
    }
</style>
