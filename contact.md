---
layout: page
title: Contact Satbir
subtitle: Let's get connected
css: "/css/aboutme.css"
---

<form action="https://formspree.io/ribtas007@outlook.com" method="POST" class="form" id="contact-form">
  
  <div class="row">
    
    <div class="col-xs-6">
      <input type="email" name="_replyto" class="form-control input-lg" placeholder="Enter your Email" title="Email">
    </div>
    
    <div class="col-xs-6">
      <input type="text" name="name" class="form-control input-lg" placeholder="Your name please" title="Name">
    </div>
    
  </div>
  
  <input type="hidden" name="_subject" value="Someone sent a message on your portfolio website">
  
  <textarea type="text" name="content" class="form-control input-lg" placeholder="Leave a message for me" title="Message" required="required" rows="3">
</textarea>

  <input type="text" name="_gotcha" style="display:none">
  <input type="hidden" name="_next" value="./aboutme?message=Your message was sent successfully, thanks!" />
  
  <button type="submit" class="btn btn-lg btn-primary">Submit</button>
  
</form>
