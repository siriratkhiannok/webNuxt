<template>
  <div style="display: flex; box-shadow: 0 5px 10px grey;">
    <div style="margin: 0 0 0 90px;">
      <img src="/img/logo.png" width="80px" alt="">
    </div>
    <div style="display: flex; margin: 0 0 0 300px; justify-content: space-around; width: 30%;">
      <p>หน้าแรก</p>
      <p>การชำระเงิน</p>
      <p>ติดต่อเรา</p>
      <p>เกี่ยวกับเรา</p>
    </div>
    <div style="margin: 0 0 0 250px;">
      <img src="/img/ms.png" width="80px" alt="">
    </div>
    <div style="margin: 10px 0 0 0px;">
      <img src="/img/pe.png" width="60px" alt="">
    </div>
  </div>

      <!-- สถานะสิ่งอำนวยความสะดวก -->
      <div style="display: flex; justify-content: center;">
        <p style="position: absolute; background-color: black; margin-top: 105px ; width: 5px; height: 80%; border-radius: 25px;"></p>
    </div>

    <div style="display: flex; justify-content: center; font-size: xx-large;"><p>สถานะสิ่งอำนวยความสะดวก</p></div>
    <div style="display: flex; justify-content: center;">
        <div style="width: 45%; height: 40px; font-size: x-large; padding-top: 0.5%; background-color: rgb(83, 152, 255); margin-right: 2%; text-align: center;">
            เครื่องซักผ้า
        </div>
        <div style="width: 45%; height: 40px; font-size: x-large; padding-top: 0.5%; background-color: rgb(83, 152, 255); margin-left: 2%; text-align: center;">
            เครื่องกดน้ำ
        </div>
    </div>
    <!-- เครื่องซักผ้าถังที่ 1 -->
    <div style="position: absolute; margin: 0 0 0 160px;">
        <div  id="s1" style=" position: absolute; margin: 120px 0 0 150px;" ref="s1">
        </div>
        <div id="area1" ref="area1" style="margin: 150px 0 0 150px; display: flex; justify-content: center; position: absolute; width: 93px; background-color: rgb(162, 250, 255); border-radius: 10px;  "></div>
        <div style="display: flex;">
            <div style="margin-top: 15vh; display: flex; ">
                <img style="cursor: pointer;" @click="show_status1()" src="/img/ซัก.png" width="120px" alt="">
                <div id="icon_status1" ref="icon_status1"></div>
            </div>
        </div>
    </div>

    <!-- เครื่องซักผ้าถังที่ 2 -->
    <div style="position: absolute; margin: 0 0 0 470px;">
        <div  id="s2" style=" position: absolute; margin: 120px 0 0 150px;">
        </div>
        <div id="area2" ref="area2" style="margin: 150px 0 0 150px; display: flex; justify-content: center; position: absolute; width: 93px; background-color: rgb(162, 250, 255); border-radius: 10px;  "></div>
        <div style="display: flex;">
            <div style="margin-top: 15vh; display: flex; ">
                <img style="cursor: pointer;" onclick="show_status2()" src="/img/ซัก.png" width="120px" alt="">
                <div id="icon_status2" ref="icon_status2"></div>
            </div>
        </div>
    </div>


        <!-- เครื่องซักผ้าถังที่ 3 -->
        <div style="position: absolute; margin: 230px 0 0 160px;">
            <div  id="s3" style=" position: absolute; margin: 120px 0 0 150px;">
            </div>
            <div id="area3" ref="area3" style="margin: 150px 0 0 150px; display: flex; justify-content: center; position: absolute; width: 93px; background-color: rgb(162, 250, 255); border-radius: 10px;  "></div>
            <div style="display: flex;">
                <div style="margin-top: 15vh; display: flex; ">
                    <img style="cursor: pointer;" onclick="show_status3()" src="/img/ซัก.png" width="120px" alt="">
                    <div id="icon_status3" ref="icon_status3"></div>
                </div>
            </div>
        </div>

        <!-- เครื่องซักผ้าถังที่ 4 -->
        <div style="position: absolute; margin: 230px 0 0 470px;">
            <div  id="s4" style=" position: absolute; margin: 120px 0 0 150px;">
            </div>
            <div id="area4" ref="area4" style="margin: 150px 0 0 150px; display: flex; justify-content: center; position: absolute; width: 93px; background-color: rgb(162, 250, 255); border-radius: 10px;  "></div>
            <div style="display: flex;">
                <div style="margin-top: 15vh; display: flex; ">
                    <img style="cursor: pointer;" onclick="show_status4()" src="/img/ซัก.png" width="120px" alt="">
                    <div id="icon_status4" ref="icon_status4"></div>
                </div>
            </div>
        </div>

            <!-- เครื่องกดน้ำ -->

    <!-- เครื่องกดน้ำที่ 1 -->
    <div style="position: absolute; margin: -35px 0 0 850px;">
        <div  id="s5" style=" position: absolute; margin: 150px 0 0 190px;">
        </div>
        <div id="area5" ref="area5" style="margin: 180px 0 0 190px; display: flex; justify-content: center; position: absolute; width: 93px; background-color: rgb(162, 250, 255); border-radius: 10px;  "></div>
        <div style="display: flex;">
            <div style="margin-top: 15vh; display: flex; ">
                <img style="cursor: pointer;" onclick="show_status5()" src="/img/น้ำ.png" width="250px" alt="">
                <div style="margin-top: 35px; margin-left: -90px;" id="icon_status5" ref="icon_status5"></div>
            </div>
        </div>
    </div>

    <!-- เครื่องซักผ้าถังที่ 2 -->
    <div style="position: absolute; margin: -35px 0 0 1150px;">
        <div  id="s6" style=" position: absolute; margin: 150px 0 0 190px;">
        </div>
        <div id="area6" ref="area6" style="margin: 180px 0 0 190px; display: flex; justify-content: center; position: absolute; width: 93px; background-color: rgb(162, 250, 255); border-radius: 10px;  "></div>
        <div style="display: flex;">
            <div style="margin-top: 15vh; display: flex; ">
                <img style="cursor: pointer;" onclick="show_status6()" src="/img/น้ำ.png" width="250px" alt="">
                <div style="margin-top: 35px; margin-left: -90px;" id="icon_status6" ref="icon_status6"></div>
            </div>
        </div>
    </div>

        <!-- เครื่องกดน้ำที่ 3 -->
        <div style="position: absolute; margin: -35px 0 0 850px;">
            <div  id="s7" style=" position: absolute; margin: 370px 0 0 190px;">
            </div>
            <div id="area7" ref="area7" style="margin: 400px 0 0 190px; display: flex; justify-content: center; position: absolute; width: 93px; background-color: rgb(162, 250, 255); border-radius: 10px;  "></div>
            <div style="display: flex;">
                <div style="margin-top: 45vh; display: flex; ">
                    <img style="cursor: pointer;" onclick="show_status7()" src="/img/น้ำ.png" width="250px" alt="">
                    <div style="margin-top: 35px; margin-left: -90px;" id="icon_status7" ref="icon_status7"></div>
                </div>
            </div>
        </div>
    
<!-- เครื่องซักผ้าถังที่ 4 -->
<div style="position: absolute; margin: -35px 0 0 1150px;">
  <div  id="s8" style=" position: absolute; margin: 370px 0 0 190px;"></div>
    <div id="area8" ref="area8" style="margin: 400px 0 0 190px; display: flex; justify-content: center; position: absolute; width: 93px; background-color: rgb(162, 250, 255); border-radius: 10px;  "></div>
      <div style="display: flex;">
          <div style="margin-top: 45vh; display: flex; ">
              <img style="cursor: pointer;" onclick="show_status8()" src="/img/น้ำ.png" width="250px" alt="">
              <div style="margin-top: 35px; margin-left: -90px;" id="icon_status8" ref="icon_status8"></div>
          </div>
      </div>
</div>

</template>
<script>
export default{
  methods:{
    // เครื่องซักผ้าเครื่องที่ 1

    show_status1() {
  // เปลี่ยนตรง id="area_s..."
  this.$refs.s1.innerHTML = '<div id="area_s1" @click="update_status1()" style="cursor: pointer;">' +
    '<p>status</p>' +
    '</div>';
  this.$refs.area1 = this.$refs.s1.querySelector('#area_s1'); // กำหนดค่าให้ this.$refs.area1
},
update_status1() {
  console.log("กุ้งตามสั่งอิคริงิก");
  this.$refs.s1.querySelector('#area_s1').innerHTML = '<div style="width: 90%; color: white;">' +
    '<div id="freecss" onclick="set_free1()" style="margin-top:5px;">ว่าง</div>' +
    '<div id="unfreecss" onclick="set_not_free1()">ไม่ว่าง</div>' +
    '<div id="unvailablecss" onclick="set_unavailable1()">งดชั่วคราว</div>' +
    '</div>';
},
set_free1(){
  this.$refs.icon_status1.innerHTML = `<p id="status_free"></P>`
    reset_area1();

},
set_not_free1(){
  this.$refs.icon_status1.innerHTML =  `<p id="status_unfree"></P>`
    reset_area1();
},
set_unavailable1(){
  this.$refs.icon_status1.innerHTML =  `<p id="status_unvailable"></P>`
    reset_area1();
},
reset_area1(){
  this.$refs.area1.innerHTML = ``
  this.$refs.s1.innerHTML = ``
},

// เครื่องซักผ้าเครื่องที่ 2

show_status2(){
    // เปลี่ยนตรง id="area_s..."
    this.$refs.s2.innerHTML = `<div id="area_s2" onclick="update_status2()" style="cursor: pointer;">
    <p>status</p>
</div>`
},
update_status2(){
  this.$refs.area2.innerHTML = `<div style="width: 90%; color: white; ">
    <div id="freecss" onclick="set_free2()" style="margin-top:5px;" >ว่าง</div>
    <div id="unfreecss" onclick="set_not_free2()">ไม่ว่าง</div>
    <div id="unvailablecss" onclick="set_unavailable2()">งดชั่วคราว</div>
</div>`
},
set_free2(){
  this.$refs.icon_status2.innerHTML = `<p id="status_free"></P>`
    reset_area2();

},
set_not_free2(){
  this.$refs.icon_status2.innerHTML =  `<p id="status_unfree"></P>`
    reset_area2();
},
set_unavailable2(){
  this.$refs.icon_status2.innerHTML =  `<p id="status_unvailable"></P>`
    reset_area2();
},
reset_area2(){
  this.$refs.area2.innerHTML = ``
  this.$refs.s2.innerHTML = ``
},


// เครื่องซักผ้าเครื่องที่ 3
show_status3(){
    // เปลี่ยนตรง id="area_s..."
    this.$refs.s3.innerHTML = `<div id="area_s3" onclick="update_status3()" style="cursor: pointer;">
    <p>status</p>
</div>`
},
update_status3(){
  this.$refs.area3.innerHTML = `<div style="width: 90%; color: white; ">
    <div id="freecss" onclick="set_free3()" style="margin-top:5px;" >ว่าง</div>
    <div id="unfreecss" onclick="set_not_free3()">ไม่ว่าง</div>
    <div id="unvailablecss" onclick="set_unavailable3()">งดชั่วคราว</div>
</div>`
},
set_free3(){
  this.$refs.icon_status3.innerHTML = `<p id="status_free"></P>`
    reset_area3();

},
set_not_free3(){
  this.$refs.icon_status3.innerHTML =  `<p id="status_unfree"></P>`
    reset_area3();
},
set_unavailable3(){
  this.$refs.icon_status3.innerHTML =  `<p id="status_unvailable"></P>`
    reset_area3();
},
reset_area3(){
  this.$refs.area3.innerHTML = ``
  this.$refs.s3.innerHTML = ``
},

// เครื่องซักผ้าเครื่องที่ 4
show_status4(){
    // เปลี่ยนตรง id="area_s..."
    this.$refs.s4.innerHTML = `<div id="area_s4" onclick="update_status4()" style="cursor: pointer;">
    <p>status</p>
</div>`
},
update_status4(){
  this.$refs.area4.innerHTML = `<div style="width: 90%; color: white; ">
    <div id="freecss" onclick="set_free4()" style="margin-top:5px;" >ว่าง</div>
    <div id="unfreecss" onclick="set_not_free4()">ไม่ว่าง</div>
    <div id="unvailablecss" onclick="set_unavailable4()">งดชั่วคราว</div>
</div>`
},
set_free4(){
  this.$refs.icon_status4.innerHTML = `<p id="status_free"></P>`
    reset_area4();

},
set_not_free4(){
  this.$refs.icon_status4.innerHTML =  `<p id="status_unfree"></P>`
    reset_area4();
},
set_unavailable4(){
  this.$refs.icon_status4.innerHTML =  `<p id="status_unvailable"></P>`
    reset_area4();
},
reset_area4(){
  this.$refs.area4.innerHTML = ``
  this.$refs.s4.innerHTML = ``
},

// เครื่องกดน้ำเครื่องที่ 1
show_status5(){
    // เปลี่ยนตรง id="area_s..."
    this.$refs.s5.innerHTML = `<div id="area_s5" onclick="update_status5()" style="cursor: pointer;">
    <p>status</p>
</div>`
},
update_status5(){
  this.$refs.area5.innerHTML = `<div style="width: 90%; color: white; ">
    <div id="freecss" onclick="set_free5()" style="margin-top:5px;" >ว่าง</div>
    <div id="unfreecss" onclick="set_not_free5()">ไม่ว่าง</div>
    <div id="unvailablecss" onclick="set_unavailable5()">งดชั่วคราว</div>
</div>`
},
set_free5(){
  this.$refs.icon_status5.innerHTML = `<p id="status_free"></P>`
    reset_area5();

},
set_not_free5(){
  this.$refs.icon_status5.innerHTML =  `<p id="status_unfree"></P>`
    reset_area5();
},
set_unavailable5(){
  this.$refs.icon_status5.innerHTML =  `<p id="status_unvailable"></P>`
    reset_area5();
},
reset_area5(){
  this.$refs.area5.innerHTML = ``
  this.$refs.s5.innerHTML = ``
},

// เครื่องกดน้ำเครื่องที่ 2
show_status6(){
    // เปลี่ยนตรง id="area_s..."
    this.$refs.s6.innerHTML = `<div id="area_s5" onclick="update_status6()" style="cursor: pointer;">
    <p>status</p>
</div>`
},
update_status6(){
  this.$refs.area6.innerHTML = `<div style="width: 90%; color: white; ">
    <div id="freecss" onclick="set_free6()" style="margin-top:5px;" >ว่าง</div>
    <div id="unfreecss" onclick="set_not_free6()">ไม่ว่าง</div>
    <div id="unvailablecss" onclick="set_unavailable6()">งดชั่วคราว</div>
</div>`
},
set_free6(){
  this.$refs.icon_status6.innerHTML = `<p id="status_free"></P>`
    reset_area6();

},
set_not_free6(){
  this.$refs.icon_status6.innerHTML =  `<p id="status_unfree"></P>`
    reset_area6();
},
set_unavailable6(){
  this.$refs.icon_status6.innerHTML =  `<p id="status_unvailable"></P>`
    reset_area6();
},
reset_area6(){
  this.$refs.area6.innerHTML = ``
  this.$refs.s6.innerHTML = ``
},

// เครื่องกดน้ำเครื่องที่ 3
 show_status7(){
    // เปลี่ยนตรง id="area_s..."
    this.$refs.s7.innerHTML = `<div id="area_s5" onclick="update_status7()" style="cursor: pointer;">
    <p>status</p>
</div>`
},
update_status7(){
  this.$refs.area7.innerHTML = `<div style="width: 90%; color: white; ">
    <div id="freecss" onclick="set_free7()" style="margin-top:5px;" >ว่าง</div>
    <div id="unfreecss" onclick="set_not_free7()">ไม่ว่าง</div>
    <div id="unvailablecss" onclick="set_unavailable7()">งดชั่วคราว</div>
</div>`
},
 set_free7(){
  this.$refs.icon_status7.innerHTML = `<p id="status_free"></P>`
    reset_area7();

},
set_not_free7(){
  this.$refs.icon_status7.innerHTML =  `<p id="status_unfree"></P>`
    reset_area7();
},
set_unavailable7(){
  this.$refs.icon_status7.innerHTML =  `<p id="status_unvailable"></P>`
    reset_area7();
},
reset_area7(){
  this.$refs.area7.innerHTML = ``
  this.$refs.s7.innerHTML = ``
},

// เครื่องกดน้ำเครื่องที่ 4
 show_status8(){
    // เปลี่ยนตรง id="area_s..."
    this.$refs.s8.innerHTML = `<div id="area_s8" onclick="update_status8()" style="cursor: pointer;">
    <p>status</p>
</div>`
},
update_status8(){
  this.$refs.area8.innerHTML = `<div style="width: 90%; color: white; ">
    <div id="freecss" onclick="set_free8()" style="margin-top:5px;" >ว่าง</div>
    <div id="unfreecss" onclick="set_not_free8()">ไม่ว่าง</div>
    <div id="unvailablecss" onclick="set_unavailable8()">งดชั่วคราว</div>
</div>`
},
set_free8(){
  this.$refs.icon_status8.innerHTML = `<p id="status_free"></P>`
    reset_area8();

},
set_not_free8(){
  this.$refs.icon_status8.innerHTML =  `<p id="status_unfree"></P>`
    reset_area8();
},
set_unavailable8(){
  this.$refs.icon_status8.innerHTML =  `<p id="status_unvailable"></P>`
    reset_area8();
},
reset_area8(){
  this.$refs.area8.innerHTML = ``
  this.$refs.s8.innerHTML = ``
},

  }
}
</script>
<style>
#freecss{
    cursor: pointer; border-radius: 10px; padding-left: 5px; background-color: rgb(73, 170, 255); margin-bottom: 5%; 
}

#freecss:hover{
    background-color:  rgb(0, 91, 171);
}
#unfreecss{
    cursor: pointer; border-radius: 10px; padding-left: 5px; background-color: rgb(73, 170, 255); margin-bottom: 5%;
}
#unfreecss:hover{
    background-color:  rgb(0, 91, 171);
}
#unvailablecss{
    margin-bottom: 5px; cursor: pointer; border-radius: 10px; padding-left: 5px; background-color: rgb(73, 170, 255);
}
#unvailablecss:hover{
    background-color:  rgb(0, 91, 171);
}
#area_s1{
    display: flex; align-items: center; justify-content: center; width: 92px; height: 25px; background-color: rgb(162, 250, 255); border-radius: 20px;
}
#area_s1::after{
    margin-top: 3px;
    content: ' \25BE';
}
#area_s1:hover{
    color:white;
    background-color:  rgb(75, 164, 242);
}

#status_free{
    width: 20px;
    height: 20px;
    border-radius: 50%;
    background-color: rgba(51, 255, 0, 1);
}
#status_unfree{
    width: 20px;
    height: 20px;
    border-radius: 50%;
    background-color: rgba(255, 0, 0, 1);
}
#status_unvailable{
    width: 20px;
    height: 20px;
    border-radius: 50%;
    background-color:rgba(250, 255, 0, 1);
}

#area_s2{
    display: flex; align-items: center; justify-content: center; width: 92px; height: 25px; background-color: rgb(162, 250, 255); border-radius: 20px;
}
#area_s2::after{
    margin-top: 3px;
    content: ' \25BE';
}
#area_s2:hover{
    color:white;
    background-color:  rgb(75, 164, 242);
}

#area_s3{
    display: flex; align-items: center; justify-content: center; width: 92px; height: 25px; background-color: rgb(162, 250, 255); border-radius: 20px;
}
#area_s3::after{
    margin-top: 3px;
    content: ' \25BE';
}
#area_s3:hover{
    color:white;
    background-color:  rgb(75, 164, 242);
}

#area_s4{
    display: flex; align-items: center; justify-content: center; width: 92px; height: 25px; background-color: rgb(162, 250, 255); border-radius: 20px;
}
#area_s4::after{
    margin-top: 3px;
    content: ' \25BE';
}
#area_s4:hover{
    color:white;
    background-color:  rgb(75, 164, 242);
}

#area_s5{
    display: flex; align-items: center; justify-content: center; width: 92px; height: 25px; background-color: rgb(162, 250, 255); border-radius: 20px;
}
#area_s5::after{
    margin-top: 3px;
    content: ' \25BE';
}
#area_s5:hover{
    color:white;
    background-color:  rgb(75, 164, 242);
}

#area_s6{
    display: flex; align-items: center; justify-content: center; width: 92px; height: 25px; background-color: rgb(162, 250, 255); border-radius: 20px;
}
#area_s6::after{
    margin-top: 3px;
    content: ' \25BE';
}
#area_s6:hover{
    color:white;
    background-color:  rgb(75, 164, 242);
}


#area_s7{
    display: flex; align-items: center; justify-content: center; width: 92px; height: 25px; background-color: rgb(162, 250, 255); border-radius: 20px;
}
#area_s7::after{
    margin-top: 3px;
    content: ' \25BE';
}
#area_s7:hover{
    color:white;
    background-color:  rgb(75, 164, 242);
}


#area_s8{
    display: flex; align-items: center; justify-content: center; width: 92px; height: 25px; background-color: rgb(162, 250, 255); border-radius: 20px;
}
#area_s8::after{
    margin-top: 3px;
    content: ' \25BE';
}
#area_s8:hover{
    color:white;
    background-color:  rgb(75, 164, 242);
}
</style>