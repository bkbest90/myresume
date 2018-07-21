<template>
  <div class="hello">
    {{firstComeSave()}}
    <h1 v-if="firstClick == 0" style="margin-top:-50px">{{ msg }}</h1>
    <img v-if="firstClick == 0" src="../assets/BestP.png" width="250px" style="margin-top: -18px"><br>
    <img v-if="firstClick == 0" class="imgLock" src="../assets/My signature.png" width="400px" style="margin-left: 40px;margin-top: -100px;margin-bottom: -110px">
    <div v-if="firstClick != 0">
      <center>
        <table border="0" width="1000px" style="margin-top: -60px">
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
            <td v-if="cvButton == 1" width="210px"><br><img  src="../assets/BestP.png" width="190px" height="190px" style="margin-top: 60px"></td>
            <td align="left">
              <br> <br>
              <!-- My CV -->
              <center><button class="pure-button" @click="changeLanguage()" style="width:72px;height:30px;" v-if="cvButton==1">En/Th</button></center>
                <!-- CV En --> 
              <div v-if="cvButton == 1&&langCV == 'en'">
                <div style="margin-left:0px;margin-top:-64px">
                Download my CV (.PDF) >> <a target="_blank" rel="noopener noreferrer" href="https://drive.google.com/open?id=1k0h7UfeioqXLHPJHMv84B-4XUAjqjBLH" class="button pure-button button-success"
                @click="downloadCV()"><span>Download</span></a><hr>
                </div>
                <table style="font-size:20px">
                 <tr height="30px" >
                   <td align="right"><b>Name</b> : </td>
                   <td>Chayanut Pasing</td>
                 </tr>
                 <tr height="30px">
                   <td align="right"><b>Age</b> : </td>
                   <td>22 </td>
                 </tr>
                 <tr height="30px">
                    <td align="right"><b>Date of Birth</b> :</td>
                    <td>March 31<span class="sup">st</span> 1996 </td>
                 </tr>
                 <tr height="30px">
                    <td align="right"><b>Number</b> : </td>
                    <td>090-438-5216</td>
                    <td align="right"><b>Email</b> : </td>
                    <td>chayanutp39@gmail.com</td>
                 </tr>
                 <tr height="30px">
                    <td align="right"><b>Nation</b> : </td>
                    <td>Thai</td>
                    <td align="right"><b>Race</b> : </td>
                    <td>Thai</td>
                 </tr>
                 <tr height="30px">
                    <td align="right"><b>Religion</b> : </td>
                    <td>Buddhism</td>
                 </tr>
                 <tr height="30px">
                    <td align="right"><b>Marital status</b> : </td>
                    <td>Single</td>
                 </tr>
                 <tr height="30px">
                    <td align="right"><b>Height</b> : </td>
                    <td>170 cm</td>
                 </tr>
                </table>
                <table border="0" style="font-size:20px;margin-left:-185px;margin-top:3px">
                  <tr height="30px" style="margin-bottom:9px"><td><b>Military status </b> : Finished Reserved Officers Training Corps Course <p style="margin-bottom:-10px"></p></td></tr>
                  <tr height="30px"><td><b>Address</b> : 109/201 The Modish Moo 5 Kanchanaphisek Road, Lumpo, Bangbuathong, Nonthaburi 11110 </td></tr>
                  <table border="0">
                    <tr>
                      <td><br><b><p style="margin-top:-15px;margin-bottom:-15px">Education</p></b><br></td>
                    </tr>
                    <tr>
                      <td  valign="top" align="right">2014 - 2018 : </td>
                      <td>Bachelor of Technology, Major in Information Technology <br> from
		                      King Mongkut’s University of Technology North Bangkok <br>
		                      GPA 2.52 <p style="margin-bottom:-15px"></p>
                      </td>
                    </tr>
                    <tr>
                      <td  valign="top" align="right">2011 - 2013 : </td>
                      <td>Senior High school, Science – mathematics from Huahin School <br>
		                      GPA 2.38<p style="margin-bottom:-15px"></p>
                      </td>
                    </tr>
                    <tr>
                      <td  valign="top" align="right">2008 - 2010 : </td>
                      <td>Junior High school, Science – mathematics from Huahin School <br>
		                      GPA 2.92<p style="margin-bottom:-15px"></p>
                      </td>
                    </tr>
                    <tr>
                      <td width="165px"><br><b><p style="margin-top:-15px;margin-bottom:-15px"> Work Experience</p></b><br></td>
                    </tr>
                    <tr>
                      <td  valign="top" align="right">2017 : </td>
                      <td> Internship, Network Engineer department at D-Net Technology Co., Ltd.
                      </td>
                    </tr>
                  </table>
                  <table>
                    <tr>
                      <td><br><b>Senior project</b>
                      <p style="text-indent:50px;margin-top:5px"> Medical Devices Management System, It’s a borrowing system that applied QR code scanning 
                         to borrow a medical device and use GPS with NB IoT for tracking the medical device 
                         by receive the value from GPS.</p></td>
                    </tr>
                    <tr>
                      <td><br><b><p style="margin-top:-15px"> Activities</p></b>
                      <p style="text-indent:50px;margin-bottom:-15px;margin-top:-20px"> - IoT Seminar Assistant lecturer “Thailand 4.0 
                        project” of King Mongkut’s University of Technology North Bangkok
                      </p>
                      <p style="text-indent:50px;margin-bottom:0px">- 24 Hours Hacking Hospital Services Development, to solve
                         hospital’s problem in 24 hours 
                      </p>
                      </td>
                    </tr>
                    <tr>
                      <td><br><b>Skills</b>
                      <p style="text-indent:50px;margin-bottom:-15px;margin-top:5px"> - Good Microsoft Office skill
                      </p>
                      <p style="text-indent:50px;margin-bottom:-15px">- Very good computer skill
                      </p>
                      <p style="text-indent:50px;margin-bottom:-15px"> - Good programing and web coding skill
                      </p>
                      <p style="text-indent:50px;margin-bottom:-15px">- Basic Photoshop
                      </p>
                      <p style="text-indent:50px;margin-bottom:-15px"> - Interpersonal skill with service mind
                      </p>
                      <p style="text-indent:50px;margin-bottom:0px">- High sense of responsibility to handle multiple tasks
                      </p>
                      </td>
                    </tr>
                    <tr>
                      <td>
                        <br><b>English skills</b>
                        <p style="margin-top:5px">Reading : Good</p>
                        <p style="margin-top:-10px">Listening : Good</p>
                        <p style="margin-top:-10px">Writing : Fair</p>
                        <p style="margin-top:-10px;margin-bottom:0px">Speaking : Fair</p>
                      </td>
                    </tr>
                    <tr>
                      <td>
                        <br><b>Hobbies</b>
                        <p style="text-indent:50px;margin-bottom:-15px;margin-top:5px">- Read Self-help books</p>
                        <p style="text-indent:50px;margin-bottom:0px">- Listen to music and play guitar</p>
                      </td>
                    </tr>
                    <tr>
                      <td>
                        <br><b>Interest</b>
                        <p style="text-indent:50px;margin-bottom:-15px;margin-top:5px">- How to Communicate With Others With Psychology based on Sincerity</p>
                        <p style="text-indent:50px;margin-bottom:-15px">- Management and Marketing</p>
                        <p style="text-indent:50px;margin-bottom:-15px">- Sport cars and Supercars</p>
                      </td>
                    </tr>
                  </table>
                </table>
              </div>
                <!-- CV Th -->
              <div v-if="cvButton == 1&&langCV == 'th'">
                <div style="margin-left:0px;margin-top:-64px">
                Download my CV (.PDF) >> <a target="_blank" rel="noopener noreferrer" href="https://drive.google.com/open?id=1k0h7UfeioqXLHPJHMv84B-4XUAjqjBLH" class="button pure-button button-success"
                @click="downloadCV()"><span>Download</span></a> <hr>
                </div>
                <table style="font-size:20px">
                 <tr height="30px" >
                   <td align="right"><b>ชื่อ - สกุล</b> : </td>
                   <td>ชยณัฐ ผาสิงห์</td>
                 </tr>
                 <tr height="30px">
                   <td align="right"><b>อายุ</b> : </td>
                   <td>22 </td>
                 </tr>
                 <tr height="30px">
                    <td align="right"><b>วัน/เดือน/ปีเกิด</b> :</td>
                    <td>31 มีนาคม พ.ศ.2539</td>
                 </tr>
                 <tr height="30px">
                    <td align="right"><b>เบอร์โทร</b> : </td>
                    <td>090-438-5216</td>
                    <td align="right"><b>Email</b> : </td>
                    <td>chayanutp39@gmail.com</td>
                 </tr>
                 <tr height="30px">
                    <td align="right"><b>สัญชาติ</b> : </td>
                    <td>ไทย</td>
                    <td align="right"><b>เชื้อชาติ</b> : </td>
                    <td>ไทย</td>
                 </tr>
                 <tr height="30px">
                    <td align="right"><b>ศาสนา</b> : </td>
                    <td>พุทธ</td>
                 </tr>
                 <tr height="30px">
                    <td align="right"><b>สถานภาพ</b> : </td>
                    <td>โสด</td>
                 </tr>
                 <tr height="30px">
                    <td align="right"><b>สูง</b> : </td>
                    <td>170 ซม.</td>
                 </tr>
                </table>
                <table border="0" style="font-size:20px;margin-left:-185px;margin-top:3px">
                  <tr height="30px" style="margin-bottom:9px"><td><b>สถานภาพทางการทหาร</b> 
                  : สำเร็จหลักสูตรรักษาดินแดน
                  <p style="margin-bottom:-10px"></p></td></tr>
                  <tr height="30px"><td><b>ที่อยู่</b> : 109/201 The Modish หมู่ 5 ถนนกาญจนาภิเษก ตำบลลำโพ
                  อำเภอบางบัวทอง จังหวัดนนทบุรี 11110 </td></tr>
                  <table border="0">
                    <tr>
                      <td><br><b><p style="margin-top:-15px;margin-bottom:-15px">ประวัติการศึกษา</p></b><br></td>
                    </tr>
                    <tr>
                      <td  valign="top" align="right" width="240px">ปีการศึกษา 2557 - 2560 : </td>
                      <td >ระดับปริญญาตรี สาขาวิชาเทคโนโลยีสารสนเทศ <br>แขนงวิชาเทคโนโลยีเครือข่าย   
		                      คณะเทคโนโลยีและการจัดการอุตสาหกรรม <br>มหาวิทยาลัยเทคโนโลยีพระจอมเกล้าพระนครเหนือ <br>
		                      ด้วยเกรดเฉลี่ย 2.52 <p style="margin-bottom:-15px"></p>
                      </td>
                    </tr>
                    <tr>
                      <td  valign="top" align="right">ปีการศึกษา 2554 - 2556 : </td>
                      <td>ระดับมัธยมศึกษาตอนปลาย สายวิทย์ - คณิต โรงเรียนหัวหิน <br>
		                      ด้วยเกรดเฉลี่ย 2.38<p style="margin-bottom:-15px"></p>
                      </td>
                    </tr>
                    <tr>
                      <td  valign="top" align="right">ปีการศึกษา 2551 - 2553 : </td>
                      <td>ระดับมัธยมศึกษาตอนต้น สายวิทย์ - คณิต โรงเรียนหัวหิน <br>
		                      ด้วยเกรดเฉลี่ย 2.92<p style="margin-bottom:-15px"></p>
                      </td>
                    </tr>
                    <tr>
                      <td width="165px"><br><b><p style="margin-top:-15px;margin-bottom:-15px">
                         ประวัติการทำงาน</p></b><br></td>
                    </tr>
                    <tr>
                      <td  valign="top" align="right">ปีการศึกษา 2559 : </td>
                      <td> นักศึกษาฝึกงาน แผนก Network Engineer บริษัท ดีเน็ตเทคโนโลยี จำกัด
                      </td>
                    </tr>
                  </table>
                  <table>
                    <tr>
                      <td><br><b>โครงงานพิเศษระดับปริญญาตรี</b>
                      <p style="text-indent:50px;margin-top:5px"> ระบบการจัดการอุปกรณ์ทางการแพทย์
                         เป็นเว็บไซต์แพลตฟอร์มระบบยืม – คืนอุปกรณ์ทางการแพทย์โดยใช้วิธีการสแกน QR Code
                         เพื่อยืม – คืนและมีระบบติดตามอุปกรณ์โดยใช้ GPS ร่วมกับ NB IoT
                          ในการส่งค่าพิกัดเพื่อให้ทราบถึงตำแหน่งของอุปกรณ์พอสังเขป</p></td>
                    </tr>
                    <tr>
                      <td><br><b><p style="margin-top:-15px"> กิจกรรมระหว่างเรียน</p></b>
                      <p style="text-indent:50px;margin-bottom:-15px;margin-top:-20px"> - ผู้ช่วยวิทยากร โครงการอบรมเชิงปฏิบัติการเรื่อง “พัฒนาศักยภาพทุนมนุษย์เพื่อก้าวไปสู่ 
                        Thailand 4.0” ของทางมหาวิทยาลัยเทคโนโลยีพระจอมเกล้าพระนครเหนือ 6 ครั้ง
                      </p>
                      <p style="text-indent:50px;margin-bottom:0px">- เข้าร่วมกิจกรรม 24 Hours Hacking Hospital Services Development เพื่อคิดหาทางแก้ไขปัญหาต่าง
                         ๆ ให้กับโรงพยาบาลโดยใช้เทคโนโลยีเข้ามาผนวกภายในเวลา 24 ชั่วโมง
                      </p>
                      </td>
                    </tr>
                    <tr>
                      <td><br><b>ทักษะ</b>
                      <p style="text-indent:50px;margin-bottom:-15px;margin-top:5px"> - มีทักษะการใช้ Microsoft Office ได้ดี
                      </p>
                      <p style="text-indent:50px;margin-bottom:-15px">- มีทักษะการใช้คอมพิวเตอร์ดีเยี่ยม
                      </p>
                      <p style="text-indent:50px;margin-bottom:-15px"> - มีทักษะการเขียนโปรแกรม เว็บไซต์ปานกลาง
                      </p>
                      <p style="text-indent:50px;margin-bottom:-15px">- มีทักษะการใช้ Photoshop ขั้นพื้นฐาน
                      </p>
                      <p style="text-indent:50px;margin-bottom:-15px" > - มีมนุษย์สัมพันธ์ดี พูดอย่างมีเชิงและหลักการบวกกับจิตวิทยาเล็กน้อยบนพื้นฐานของความจริงใจ </p> 
                      <p style="text-indent:50px;margin-left:13px;margin-bottom:-15px">เข้ากับคนอื่นได้ง่าย</p>
                      <p style="text-indent:50px;margin-bottom:0px">- มีความรับผิดชอบสูงในการจัดการงานต่าง ๆ
                      </p>
                      </td>
                    </tr>
                    <tr>
                      <td>
                        <br><b>ทักษะภาษาอังกฤษ</b>
                        <p style="margin-top:5px">การอ่าน : ดี</p>
                        <p style="margin-top:-10px">การฟัง : ดี</p>
                        <p style="margin-top:-10px">การเขียน : พอใช้</p>
                        <p style="margin-top:-10px;margin-bottom:0px">การพูด : พอใช้</p>
                      </td>
                    </tr>
                    <tr>
                      <td>
                        <br><b>งานอดิเรก</b>
                        <p style="text-indent:50px;margin-bottom:-15px;margin-top:5px">- อ่านหนังสือแนวจิตวิทยาพัฒนาตนเอง การทำงานเป็นทีม</p>
                        <p style="text-indent:50px;margin-bottom:0px">- ฟังเพลงสากลและเล่นกีตาร์</p>
                      </td>
                    </tr>
                    <tr>
                      <td>
                        <br><b>สิ่งที่สนใจ</b>
                        <p style="text-indent:50px;margin-bottom:-15px;margin-top:5px">- การพูด การฟัง และการเข้าหาผู้อื่นโดยใช้หลักการจิตวิทยาบนพื้นฐานของความจริงใจ</p>
                        <p style="text-indent:50px;margin-bottom:-15px">- การบริหาร การตลาด</p>
                        <p style="text-indent:50px;margin-bottom:-15px">- รถสปอร์ต รถยนต์ Supercars</p>
                      </td>
                    </tr>
                  </table>
                </table>
              </div>
              <!-- My Resume -->
              <center>
              <div v-if="resumeButton == 1">
                <div style="margin-top:-35px">
                Download my resume (.PDF or .PNG) >> <a target="_blank" rel="noopener noreferrer" href="https://drive.google.com/open?id=124TVwddDyGERnV1pCUzJr20aNuNVNtvI" class="button pure-button button-secondary"
                @click="downloadResume()"><span>Download</span></a>
                </div>
                <img src="../assets/Chayanut Pasing Resume.png" width="990px" height="1400px">
               </div> 
              </center>
              <center>
                <!-- My grade -->
              <div v-if="gradeButton == 1">
                * These pictures are from official information technology system of my university <br>
                * รูปภาพเหล่านี้นำมาจากเว็บไซต์ทางการของมหาวิทยาลัย <br>
                Download my grade (.PDF or .PNG) >> <a target="_blank" rel="noopener noreferrer" href="https://drive.google.com/open?id=1p4tF0qCyybBk60O_BY4LeGAL2YOIcbiG" class="button pure-button button-warning" 
                @click="downloadGrade()"><span>Download</span></a><br>
                <img src="../assets/GradePNG_Page_1.png" width="1100px" height="1400px">
                <img src="../assets/GradePNG_Page_2.png" width="1100px" height="1400px">
                <img src="../assets/GradePNG_Page_3.png" width="1100px" height="1400px">
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
      * คลิกปุ่มเพื่อดูสิ่งที่ท่านต้องการดู <b>: )</b>
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
var langClickRef = db.ref('langClick')
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
    homeClickFire: homeClickRef,
    langClickFire: langClickRef      
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
    changeLanguage(){
      langClickRef.once("value", function(snapshot) {
        snapshot.forEach(function(data) {
          var number = data.val() + 1
          langClickRef.set({
            clickTimes: number
           })
        })
      })
      if (this.langCV=='en') {
        this.langCV = 'th'
      }else{
        this.langCV = 'en'
      }
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
.sup {
  position: relative;
  bottom: 1ex; 
  font-size: 80%;
}
</style>
