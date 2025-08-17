---
layout: post
title: Contact Us
---

<form id="emailForm">
  <input type="text" id="name" placeholder="Your Name" required>
  <input type="email" id="email" placeholder="Your Email" required>
  <textarea id="message" placeholder="Your Message" required></textarea>
  <button type="submit">Send Message</button>
</form>

<script>
  document.getElementById('emailForm').addEventListener('submit', function(e) {
    e.preventDefault();
    
    const name = encodeURIComponent(document.getElementById('name').value);
    const email = encodeURIComponent(document.getElementById('email').value);
    const message = encodeURIComponent(document.getElementById('message').value);
    
    const subject = `Message from ${name}`;
    const body = `${message}\n\n---\nReply to: ${email}`;
    
    window.location.href = `mailto:EXAMPLE@gmail.com?subject=${subject}&body=${body}`;
  });
</script>