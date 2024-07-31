---
title: Form Processing
description: 
date: 2024-05-30
tags:
  - Javascript
  - HTML
  - Bootstrap
---
<p>This session was a deep-dive into the <b>form elements</b> and their <b>attributes</b> (such as input and type), as well as correct and safe practices around <b>data collection</b>. We covered <b>validation</b>, which was also an early introduction to Javascript.</p>

<h2>Take-away Task</h2>

To put into practice what we learnt, we each built a contact form to add to our blogs. My working form can now be found under <a href="/content/contact-me.njk">Contact Me</a>, and below is my code.

<h2>Key points:</h2>
<ul>
  <li><p>Within my form tag, I've used <b>semantic elements</b> such as <b>fieldset</b>, <b>legend</b> and <b>label</b>, rather than simple divs</p></li>
  <li><p>I've specified how the form data should be sent to the server using the <b>method="POST"</b> attribute within my form tag</p></li>
  <li><p>Because I'm using a Netlify form, I've used the <b>netlify</b> attribute inside my form tag, rather than <b>action</b> attribute.</p></li>
  <li><p>You'll see that I've used a bit of <b>bootstrap</b> styling too!</p></li>
</ul>

```html

<form name="contact-us" method="POST" netlify>
  <fieldset class="row g-3">
      <legend>✉️ Contact Form</legend>
      <div class="col-md-6">
        <label for="firstName" class="form-label">First Name:</label><br>
        <input name="firstName" id="firstName" class="form-control" type="text" required>
      </div>
      <div class="col-md-6">
        <label for="lastName" class="form-label">Last Name:</label><br>
        <input name="lastName" id="lastName" type="text" class="form-control" required>
      </div>
      <br><br>
      <div class="col-12">
        <label for="email" class="form-label">Email Address:</label><br>
        <input name= "email" id="email" type="email" class="form-control" required>
      </div>
      <br><br>
      <div class="col-12">
        <label for="message" class="form-label">Type your message here:</label><br>
        <textarea name="message" id="message" class="form-control" rows="6" required></textarea>
      </div>
      <br><br>
      <div class="col-12">
        <input name="terms" type="checkbox" id="terms" required>
        <label name="terms" for="terms">I accept the Terms & Conditions</label>
      </div>
      <input type="submit" value="Submit">
  </fieldset>
</form>
```