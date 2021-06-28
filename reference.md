---
layout: page
title:  CONTACT
---



<style>

  /* main.css에서 적용 안되서 따로 적용 */


  .contact-subtitle {
    max-width: 600px;
    margin: 0 auto 40px;
    text-align: center;
    color: #5b5b5b;
  }

  .gform {
    width: 750px;
    max-width: 100%;
    margin: 0 auto;
  }

  .gform .gform-group {
    margin-bottom: 20px;
  }

  .gform .gform-group:last-child {
    margin: 40px 0 0;
  }

  .gform .gform-group label {
    display: block;
    margin-bottom: 10px;
    font-size: 11px;
    text-transform: uppercase;
    color: #5b5b5b;
  }

  .gform .gform-group .form-input {
    height: 40px;
  }

  .gform .gform-group .form-input,
  .gform .gform-group .form-textarea {
    width: 100%;
    padding: 8px 10px;
    font-size: 14px;
    border: 2px solid #f2f4fa;
    -webkit-border-radius: 3px;
    border-radius: 3px;
    outline: none;
    resize: none;
    color: #5b5b5b;
    -webkit-transition: all .25s ease;
    -o-transition: all .25s ease;
    transition: all .25s ease;
  }

  .gform .gform-group .form-input:focus,
  .gform .gform-group .form-textarea:focus {
    border: 2px solid rgba(0, 120, 217, 0.3);
  }

  .gform .gform-group .form-btn {
    font-weight: 700;
    background-color: #0078d9;
    color: #ffffff;
    -webkit-border-radius: 3px;
    border-radius: 3px;
  }

  .gform .gform-group .form-btn:hover {
    background-color: #004e8d;
  }

</style>



<!-- _config_yml이랑 관련 O-->
{% if site.contact-subtitle %}
<h5 class="contact-subtitle">{{ site.contact-subtitle }}</h5>
<hr>
{% else %}
{% endif %}
<form method="POST" data-email = "volu7070@gmail.com" class="gform"
      action="https://script.google.com/macros/s/AKfycbwx_wGOd2AI2t5Tht1oqzbofkyKB8SBs5pTHXfn2HJqN53ToEE/exec">
  <div class="gform-group">
    <label for="form-name">Your Name (Required)</label>
    <input class="form-input" type="text" name="name" id="form-name" required>
  </div>
  <div class="gform-group">
    <label for="form-email">Your Email (Required)</label>
    <input class="form-input" type="email" name="_replyto" id="form-email" required>
  </div>
  <div class="gform-group">
    <label for="form-subject">Subject</label>
    <input class="form-input" type="text" name="subject" id="form-subject">
  </div>
  <div class="gform-group">
    <label for="form-text">Your Message (Required)</label>
    <textarea class="form-textarea" name="text" rows="12" id="form-text" required></textarea>
  </div>

  <div class="gform-group">
    <button type="submit" class="form-btn btn btn-big">Send</button>
  </div>

  <!-- ** ajax이용해 양식 제출 : json 형식으로 출력 x-->
  <script data-cfasync="false" type="text/javascript"
          src="https://cdn.rawgit.com/dwyl/html-form-send-email-via-google-script-without-server/master/form-submission-handler.js"></script>

  <!-- ** 폼 send 후 감사메세지 출력 , 새로고침 없음 : form 태그에 type="submit" 없어야함(버튼으로 따로 생성은 ok)-->
  <div style="display:none" class="thankyou_message" >
    <!-- You can customize the thankyou message by editing the code below -->
    <h2><em>Thanks</em> for contacting us! We will get back to you soon!</h2>
  </div>
</form> <!-- /.form -->


