<template>
   <div class="menu">

   <div class="menu-logo">
       <h1>LOGO</h1>
   </div>

    <ul class="menu-items">
      <li>
        
        <div class="menu-block">
          <v-icon class="menu-icon" dark>create</v-icon>
          <span @click="drawer">Tanımlamalar</span>
        </div>
          

          <ul class="sub-items" v-show="open">
              <li>
                  <a href="">Malzeme Kayıtları</a>
              </li>
              <li>
                  <a href="!#">Firma Kayıtları</a>
              </li>
              <li>
                  <a href="!#">Proje Kayıtları</a>
              </li>
              <li>
                  <a href="!#">Firma Kayıtları</a>
              </li>
          </ul>
      </li>
      <li>
          <div class="menu-block">
              <v-icon class="menu-icon" dark>local_shipping</v-icon>
              <span @click="drawer_2">Sipariş İşlemleri</span>
          </div>
          

           <ul class="sub-items" v-show="open_2">
              <li>
                  <a href="" class="margin-link">Sipariş Kayıt</a>
              </li>
              <li>
                  <a href="!#" class="margin-link">Sipariş Takip</a>
              </li>
          </ul>
      </li>
      <li>
          <div class="menu-block">
           <v-icon class="menu-icon" dark>exit_to_app</v-icon>
           <span>Stok Giriş</span>
          </div>
      </li>
      <li>
          <div class="menu-block">
           <v-icon class="menu-icon" dark>sync_alt</v-icon>
           <span>Stok Çıkış</span>
          </div>
      </li>
      <li>
          <div class="menu-block">
           <v-icon class="menu-icon" dark>cancel</v-icon>
           <span>Çıkış İşlemleri</span>
          </div>
      </li>
        <li>
        
          <div class="menu-block">
           <v-icon class="menu-icon" dark>bug_report</v-icon>
           <span @click="drawer_3">Raporlar</span>
          </div>

            <ul class="sub-items" v-show="open_3">
              <li>
                  <a href="">Malzeme Listesi Raporu</a>
              </li>
              <li>
                  <a href="!#">Stok Bakiye Raporu</a>
              </li>
              <li>
                  <a href="!#">Saf Yerine Göre Rapor</a>
              </li>
              <li>
                  <a href="!#">Raf Numarasına Göre Rapor</a>
              </li>
               <li>
                  <a href="!#">Özet Rapor</a>
              </li>
               <li>
                  <a href="!#">Detaylı Stok Giriş-Çıkış</a>
              </li>
            </ul>
        </li>

        <div class="menu-block">
           <v-icon class="menu-icon" dark>history</v-icon>
           <span>Tarih Aralığında Stok Çıkış</span>
        </div>
    </ul>
   </div>
</template>


<script>
 

export default {
  name: 'Header',

  data: () => ({
      open: false,
      open_2: false,
      open_3: false,
    }),

  methods: {
      drawer(){
          this.open = !this.open
      },
      drawer_2(){
          this.open_2 = !this.open_2
      },
      drawer_3(){
          this.open_3 = !this.open_3
      }
  }
}

</script>



<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Ubuntu&display=swap');

.menu{
    width: 20%;
    height: 100vh;
    background-color:#243444;
    font-family: 'Ubuntu', sans-serif;
}


.menu-logo {
    border-bottom: 1px solid #56b6a7;
}

.menu-logo h1 {
    color: #fff;
    text-align: center;
    padding: 5px;
}

.menu-items{
    margin-left: 15px;
}

.menu-items li{
   padding: 9px 0;
   list-style-type: none;
}

span {
    color: #fff;
    cursor: pointer;
}

.menu-items a {
    text-decoration: none;
    color: 	#fff;
    
}

.menu-icon {
    color: #56b6a7;
    margin-right: 5px;
}

.sub-items{
    padding-left: 50px;
    padding-top: 5px;
    display: inline-block;
}

.sub-items li {
    position: relative;
    border-left: 1px solid #56b6a7;
}

.sub-items a {
    font-size: 14px;
}

.sub-items li::before{
    position: relative;
    top:-5px;
    width: 17px;
    border-bottom: 1px solid #56b6a7;
    content: '';
    display: inline-block;
}

.sub-items li:last-child{
    height: 1px;
    
}

.icon {
    font-size: 36px;
    color: red;
}

.menu-block {
    display: flex;
    align-items: center;
    padding: 10px;
}
</style>