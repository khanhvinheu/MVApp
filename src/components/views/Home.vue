<template>
    <div class="main__home">      
        <div class="main__slide">
            <SlideBarComponent :data="slide"/>
        </div>
        <el-divider content-position="left">
            <span class="course__title">Danh mục</span>
        </el-divider>
        <el-scrollbar>
            <div class="scrollbar-flex-content">
            <p v-for="item in category" :key="item" class="scrollbar-demo-item">
               {{ item.title }}
            </p>
            </div>
        </el-scrollbar>
        <el-divider content-position="left">
            <span class="course__title">Sản phẩm mới nhất? <el-button type="primary" size="small" round>Hot</el-button></span>
        </el-divider>
        <div class="cards">
            <CardItemComponent :data="course"/>
        </div>
        <!-- <el-divider content-position="left">
            <span class="course__title">What is Lorem Ipsum? <el-button type="success" size="small" round>New</el-button></span>
        </el-divider> -->
     
    </div>
</template>
<script>
    import SlideBarComponent from "../Common/SlideBarComponent.vue";
    import CardItemComponent from "../Common/CardItemComponent.vue";
    export default {
        components: {
            SlideBarComponent,CardItemComponent
        },
        mounted() {        
           
        },
        data() {
            return {   
                imgNotFound:'https://bitsofco.de/content/images/2018/12/Screenshot-2018-12-16-at-21.06.29.png',            
                slide: [
                    {
                        title: 'Bạn cần tìm gì?',
                        background: 'linear-gradient(to right, rgb(254, 33, 94), rgb(255, 148, 2))',
                        color: '#ffffff',
                        titleButton: 'Bắt đầu ngay',
                        img: './img/baner1.png'
                    },
                    {
                        title: 'Bạn cần tìm gì?',
                        background: 'linear-gradient(to right, rgb(254, 33, 94), rgb(255, 148, 2))',
                        color: '#ffffff',
                        titleButton: 'Bắt đầu ngay',
                        img: './img/baner1.png'
                    },
                    {
                        title: 'Bạn cần tìm gì?',
                        background: 'linear-gradient(to right, rgb(254, 33, 94), rgb(255, 148, 2))',
                        color: '#ffffff',
                        titleButton: 'Bắt đầu ngay',
                        img: './img/baner1.png'
                    },
                    // {
                    //     title: 'What is Lorem Ipsum?',
                    //     background: 'linear-gradient(to right, rgb(0, 126, 254), rgb(6, 195, 254))',
                    //     color: '#ffffff',
                    //     titleButton: 'Register Now',
                    //     img: './img/baner2.png'
                    // },
                    // {
                    //     title: 'What is Lorem Ipsum?',
                    //     background: 'linear-gradient(to right, rgb(0, 126, 254), rgb(6, 195, 254))',
                    //     color: '#ffffff',
                    //     titleButton: 'Register Now',
                    //     img: './img/baner3.png'
                    // },
                    // {
                    //     title: 'What is Lorem Ipsum?',
                    //     background: 'linear-gradient(to right, rgb(40, 119, 250), rgb(103, 23, 205))',
                    //     color: '#ffffff',
                    //     titleButton: 'Register Now',
                    //     img: './img/banner_4.png'
                    // }
                ],
                course: [
                    {
                        title: 'Nông sản',
                        background: 'https://files.fullstack.edu.vn/f8-prod/courses/7.png',                       
                        color: '#ffffff',
                        titleButton: 'Register Now',
                        creator:'Khánh Vinh'
                    },
                    // {
                    //     title: 'What is Lorem Ipsum?',
                    //     background: 'https://files.fullstack.edu.vn/f8-prod/courses/7.png',                     
                    //     color: '#ffffff',
                    //     titleButton: 'Register Now'
                    // },
                    // {
                    //     title: 'What is Lorem Ipsum?',
                    //     background: 'https://files.fullstack.edu.vn/f8-prod/courses/7.png',                      
                    //     color: '#ffffff',
                    //     titleButton: 'Register Now'
                    // },
                    // {
                    //     title: 'What is Lorem Ipsum?',
                    //     background: 'https://files.fullstack.edu.vn/f8-prod/courses/7.png',                       
                    //     color: '#ffffff',
                    //     titleButton: 'Register Now'
                    // },
                    // {
                    //     title: 'What is Lorem Ipsum?',
                    //     background: 'https://files.fullstack.edu.vn/f8-prod/courses/7.png',                       
                    //     color: '#ffffff',
                    //     titleButton: 'Register Now'
                    // },
                    // {
                    //     title: 'What is Lorem Ipsum?',
                    //     background: 'https://files.fullstack.edu.vn/f8-prod/courses/7.png',                       
                    //     color: '#ffffff',
                    //     titleButton: 'Register Now'
                    // },
                    // {
                    //     title: 'What is Lorem Ipsum?',
                    //     background: 'https://files.fullstack.edu.vn/f8-prod/courses/7.png',                       
                    //     color: '#ffffff',
                    //     titleButton: 'Register Now'
                    // },
                    // {
                    //     title: 'What is Lorem Ipsum?',
                    //     background: 'https://files.fullstack.edu.vn/f8-prod/courses/7.png',                       
                    //     color: '#ffffff',
                    //     titleButton: 'Register Now'
                    // },

                ],
                category:[
                    {title:'Mua sắm'},
                    {title:'Nhà đất'},
                    {title:'Dịch vụ'},
                    {title:'Việc làm'},
                    {title:'Blog'},
                ]
            }
        }
    }
</script>

<style scoped>
.scrollbar-flex-content {
  display: flex;
  width: 100px;
}
.scrollbar-demo-item {
  flex-shrink: 0;
  display: flex;
  align-items: center;
  justify-content: center;
  width: 80px;
  height: 80px;
  border-radius: 100px;
  margin: 10px;
  text-align: center;
  /* border-radius: 4px; */
  background: var(--el-color-danger-light-9);
  color: var(--el-color-danger);
}
</style>