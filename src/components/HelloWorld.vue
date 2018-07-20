<template>
  <div class="hello">
    {{firstComeSave()}}
    <h1 v-if="firstClick == 0" style="margin-top:-50px">{{ msg }}</h1>
    <img v-if="firstClick == 0" src="../assets/BestP.png" width="250px" style="margin-top: -18px"><br>
    <img v-if="firstClick == 0" class="imgLock" src="../assets/My signature.png" width="400px" style="margin-left: 40px;margin-top: -100px;margin-bottom: -110px">
    <div v-if="firstClick != 0">
      <center>
        <table border="1" width="1000px" style="margin-top: -60px">
          <tr valign="top">
           <td align="center" colspan="2">
             <button class="button button-secondary pure-button" style="font-size: 25px;height: 65px;width: 200px" 
             @click="resumeClicked()">
               <span>My Resume</span>
             </button>
             <button class="button button-success pure-button" style="font-size: 25px;height: 65px;width: 370px" 
             @click="cvClicked()">
               <span>My Curriculum Vitae (CV)</span>
             </button>
             <button class="button button-warning pure-button" style="font-size: 25px;height: 65px;width: 180px" 
             @click="gradeClicked()">
               <span>My Grade</span>
             </button> <br>
             <button class="pure-button" @click="homeClicked()">Home</button>
            <br>
            <h1 v-if="resumeButton == 1" style="margin-bottom: -5px">My Resume</h1>
            <h1 v-if="cvButton == 1" style="margin-bottom: -5px">My Curriculum Vitae</h1>
            <h1 v-if="gradeButton == 1" style="margin-bottom: -5px">My Grade</h1>
            </td>
          </tr>
          <tr valign="top">
            <td v-if="cvButton == 1" width="210px"><br><img  src="../assets/BestP.png" width="190px" height="190px" style="margin-top: 42px"></td>
            <td align="left">
              <br> <br>
              <!-- My CV -->
              <center><button class="pure-button" @click="changeLanguage()" style="width:72px;height:30px;" v-if="cvButton==1">En/Th</button></center>
                <!-- CV En -->
              <div v-if="cvButton == 1&&langCV == 'en'">
                <div style="margin-left:44px;margin-top:-64px">
                Download my CV >> <a href="https://drive.google.com/open?id=1k0h7UfeioqXLHPJHMv84B-4XUAjqjBLH" class="button pure-button button-success"><span>Download</span></a>
                </div>
                <table style="font-size:20px">
                 <tr height="25px" >
                   <td align="right"><b>Name</b> : </td>
                   <td>Chayanut Pasing</td>
                 </tr>
                 <tr height="25px">
                   <td align="right"><b>Age</b> : </td>
                   <td>22 </td>
                 </tr>
                 <tr height="25px">
                    <td align="right"><b>Date of Birth</b> :</td>
                    <td>31 March 1996 </td>
                 </tr>
                 <tr height="25px">
                    <td align="right"><b>Nation</b> : </td>
                    <td>Thai</td>
                 </tr>
                 <tr height="25px">
                    <td align="right"><b>Race</b> : </td>
                    <td>Thai</td>
                 </tr>
                 <tr height="25px">
                    <td align="right"><b>Religion</b> : </td>
                    <td>Bhuddhism</td>
                 </tr>
                 <tr height="25px">
                    <td align="right"><b>Marital status</b> : </td>
                    <td>Single</td>
                 </tr>
                </table>
              </div>
                <!-- CV Th -->
              <div v-if="cvButton == 1&&langCV == 'th'">
                <div style="margin-left:44px;margin-top:-64px">
                Download my CV >> <a href="https://drive.google.com/open?id=1k0h7UfeioqXLHPJHMv84B-4XUAjqjBLH" class="button pure-button button-success"><span>Download</span></a>
                </div>
                <table style="font-size:20px">
                 <tr height="25px" >
                   <td align="right"><b>ชื่อ - สกุล</b> : </td>
                   <td>ชยณัฐ ผาสิงห์</td>
                 </tr>
                 <tr height="25px">
                   <td align="right"><b>อายุ</b> : </td>
                   <td>22 </td>
                 </tr>
                 <tr height="25px">
                    <td align="right"><b>วัน/เดือน/ปีเกิด</b> :</td>
                    <td>31 มีนาคม พ.ศ.2539</td>
                 </tr>
                 <tr height="25px">
                    <td align="right"><b>สัญชาติ</b> : </td>
                    <td>ไทย</td>
                 </tr>
                 <tr height="25px">
                    <td align="right"><b>เชื้อชาติ</b> : </td>
                    <td>ไทย</td>
                 </tr>
                 <tr height="25px">
                    <td align="right"><b>ศาสนา</b> : </td>
                    <td>พุทธ</td>
                 </tr>
                 <tr height="25px">
                    <td align="right"><b>สถานะการแต่งงาน</b> : </td>
                    <td>โสด</td>
                 </tr>
                </table>
              </div>
              <!-- My Resume -->
              <center>
              <div v-if="resumeButton == 1">
                <div style="margin-top:-35px">
                Download my resume >> <a href="https://drive.google.com/open?id=124TVwddDyGERnV1pCUzJr20aNuNVNtvI" class="button pure-button button-secondary"><span>Download</span></a>
                </div>
                <img src="../assets/Chayanut Pasing Resume.png" width="990px" height="1400px">
               </div> 
              </center>
              <center>
                <!-- My grade -->
              <div v-if="gradeButton == 1">
                * These pictures are from official information technology system of my university <br>
                * รูปภาพเหล่านี้นำมาจากเว็บไซต์ทางการของมหาวิทยาลัย <br>
                Download my grade >> <a href="https://drive.google.com/open?id=1p4tF0qCyybBk60O_BY4LeGAL2YOIcbiG" class="button pure-button button-warning"><span>Download</span></a><br>
                <img src="../assets/GradePNG_Page_1.png" width="1000px" height="1400px">
                <img src="../assets/GradePNG_Page_2.png" width="1000px" height="1400px">
                <img src="../assets/GradePNG_Page_3.png" width="1000px" height="1400px">
              </div> 
              </center>
            </td>
          </tr>
        </table>
      </center>
    </div>
    <br>
    <div v-if="firstClick == 0">Chayanut Pasing <br>ชยณัฐ ผาสิงห์ <br></div>
    
    <div v-if="firstClick == 0" style="margin-top: 20px">
      * Please click a button below to look what you want <b></b><br>
      * คลิกปุ่มเพื่อดูสิ่งที่ท่านอยากดู <b>: )</b>
    </div><br>
    <button v-if="firstClick == 0" class="button button-secondary pure-button" style="font-size: 28px;width: 210px" 
    @click="resumeClicked()">
      <span>My Resume</span>
    </button>
    <button v-if="firstClick == 0" class="button button-success pure-button" style="font-size: 28px;width: 400px" 
    @click="cvClicked()">
      <span>My Curriculum Vitae (CV)</span></button>
      <button v-if="firstClick == 0" class="button button-warning pure-button" style="font-size: 28px;width: 190px" 
      @click="gradeClicked()">
      <span>My Grade</span></button>
    <br><br><p style="font-size:12px">Powered by Chayanut Pasing</p>
  </div>
</template>

<script>
import firebase from 'firebase'
var config = {
  apiKey: 'AIzaSyAFekRx4QeUhP7ZLD4IfkSR2GrprXyznk8',
  authDomain: 'chayanut-resume.firebaseapp.com',
  databaseURL: 'https://chayanut-resume.firebaseio.com',
  projectId: 'chayanut-resume',
  storageBucket: 'chayanut-resume.appspot.com',
  messagingSenderId: '422738336552'
}
var firebaseApp = firebase.initializeApp(config)
var db = firebaseApp.database()
var firstComeRef = db.ref('firstCome')
var cvClickRef = db.ref('cvClick')
var downloadCVRef = db.ref('downloadCV')
var downloadGradeRef = db.ref('downloadGrade')
var downloadResumeRef = db.ref('downloadResume')
var gradeClickRef = db.ref('gradeClick')
var resumeClickRef = db.ref('resumeClick')
var homeClickRef = db.ref('homeClick')
export default {
  name: 'HelloWorld',
  firebase: {
    firstComeFire: firstComeRef,
    cvClickFire: cvClickRef,
    downloadCVFire: downloadCVRef,
    downloadGradeFire: downloadGradeRef,
    downloadResumeFire: downloadResumeRef,
    gradeClickFire: gradeClickRef,
    resumeClickFire: resumeClickRef,
    homeClickFire: homeClickRef    
  },
  data () {
    return {
      msg: 'Welcome to my profile web page',
      resumeButton: 0,
      cvButton: 0,
      firstClick: 0,
      gradeButton: 0,
      langCV: 'en',
      firstCome: 0
    }
  },
  methods: {
    downloadGrade(){
      downloadGradeRef.once("value", function(snapshot) {
        snapshot.forEach(function(data) {
          console.log(data.val())
          var number = data.val() + 1
          downloadGradeRef.set({
            clickTimes: number
           })
        })
      })
    },
    downloadCV(){
      downloadCVRef.once("value", function(snapshot) {
        snapshot.forEach(function(data) {
          console.log(data.val())
          var number = data.val() + 1
          downloadCVRef.set({
            clickTimes: number
           })
        })
      })
    },
    downloadResume(){
      downloadResumeRef.once("value", function(snapshot) {
        snapshot.forEach(function(data) {
          console.log(data.val())
          var number = data.val() + 1
          downloadResumeRef.set({
            clickTimes: number
           })
        })
      })
    },
    gradeClicked(){
      if (this.gradeButton != 1) {
        this.gradeButton = 1
        gradeClickRef.once("value", function(snapshot) {
        snapshot.forEach(function(data) {
          console.log(data.val())
          var number = data.val() + 1
          gradeClickRef.set({
            clickTimes: number
           })
        })
      })
      }
      this.firstClick = 1
      this.cvButton = 0
      this.resumeButton = 0
    },
    cvClicked(){
      if (this.cvButton != 1) {
        this.cvButton = 1
        cvClickRef.once("value", function(snapshot) {
        snapshot.forEach(function(data) {
          console.log(data.val())
          var number = data.val() + 1
          cvClickRef.set({
            clickTimes: number
           })
        })
      })
      }
      this.firstClick = 1
      this.gradeButton = 0
      this.resumeButton = 0
    },
    homeClicked(){
           homeClickRef.once("value", function(snapshot) {
        snapshot.forEach(function(data) {
          console.log(data.val())
          var number = data.val() + 1
          homeClickRef.set({
            clickTimes: number
           })
        })
      })
      this.resumeButton=0
      this.gradeButton = 0
      this.cvButton=0
      this.firstClick=0
    },
    resumeClicked(){
      if (this.resumeButton != 1) {
          this.resumeButton = 1
        resumeClickRef.once("value", function(snapshot) {
        snapshot.forEach(function(data) {
          console.log(data.val())
          var number = data.val() + 1
          resumeClickRef.set({
            clickTimes: number
           })
        })
      })
      }
      this.firstClick = 1
      this.gradeButton = 0
      this.cvButton = 0
    },
    firstComeSave(){
      if (this.firstCome == 0) {
        firstComeRef.once("value", function(snapshot) {
        snapshot.forEach(function(data) {
          var number = data.val() + 1
          firstComeRef.set({
            clickTimes: number
           })
        })
      })
      this.firstCome = 1
      }
    },
    updateNumberOfViewer () {
      dataRef.once("value", function(snapshot) {
        snapshot.forEach(function(data) {
          console.log(data.val())
          var number = data.val() + 1
          dataRef.set({
            clickTimes: number
           })
        })
      })
    },
    changeLanguage(){
      if (this.langCV=='en') {
        this.langCV = 'th'
      }else{
        this.langCV = 'en'
      }
    },
    setData(number){
      dataRef.set({
        clickTimes: number
      })
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
h3{
  font-size: 24px;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
.button span:after {
  content: '\00bb';
  position: absolute;
  opacity: 0;
  top: 0;
  right: -20px;
  transition: 0.5s;
}

.button:hover span {
  padding-right: 25px;
}

.button:hover span:after {
  opacity: 1;
  right: 0;
}
.button {
  border-radius: 4px;
  border: none;
  color: #FFFFFF;
  text-align: center;
  /* font-size: 28px; */
  padding: 20px;
  transition: all 0.5s;
  cursor: pointer;
  margin: 5px;
}

.button span {
  cursor: pointer;
  display: inline-block;
  position: relative;
  transition: 0.5s;
}
.button-success,
.button-error,
.button-warning,
.button-secondary {
            color: white;
            border-radius: 4px;
            text-shadow: 0 1px 1px rgba(0, 0, 0, 0.2);
        }

        .button-success {
            background: rgb(28, 184, 65); /* this is a green */
        }

        .button-error {
            background: rgb(202, 60, 60); /* this is a maroon */
        }

        .button-warning {
            background: rgb(223, 117, 20); /* this is an orange */
        }

        .button-secondary {
            background: rgb(50, 150, 221); /* this is a light blue */
        }
.imgLock{
  pointer-events: none;
}
</style>
