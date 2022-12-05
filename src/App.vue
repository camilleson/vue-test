  <template>

  <Modal :원룸들="원룸들" :모달창="모달창" :누른거="누른거" />

  <div class="menu">
    <a v-for="(a,i) in 메뉴들" :key="i">{{a}}</a>
  </div>

  <Card @openModal="모달창 = true; 누른거 = $event" :원룸들="원룸들[i]" v-for="(작명,i) in 원룸들" :key="작명" />


  <!-- <div v-for="(b,i) in products" :key="i">
    <h4>{{ b}}</h4>
    <p>상품 가격 : 60</p>
  </div> -->
</template>

  <script>
import data from './assets/data.js'
import Modal from './Modal.vue'
import Card from './Card.vue'

export default {
  name: "App",
  //데이터를 저장하고 사용할 때 
  data() {
    
    return {
      누른거 : 0,
      원룸들 : data,
      모달창 : false,
      추천수 : [0,0,0],
      메뉴들 : ['Home', 'Shop', 'About'],
      products: ["역삼", "천호", "마포"],
      
    };
     
  },
  
  //함수를 사용할 때
  methods:{
    increase(){
      this.신고수 += 1;
    },
    decrease(){
      this.신고수 -= 1;
    }
  },
  
  components: {
     Modal, Card
  },
  
};

</script>

  <style src="./ss.css" />

