---
layout: page
title: Contact
subtitle: Get in touch with us
---

<style>
  .contact-container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 20px;
  }
  
  .contact-info {
    background-color: #f8f9fa;
    padding: 30px;
    border-radius: 10px;
    margin-bottom: 30px;
  }
  
  .contact-item {
    margin-bottom: 20px;
    display: flex;
    align-items: center;
  }
  
  .contact-item i {
    color: #007bff;
    margin-right: 15px;
    width: 20px;
    text-align: center;
  }
  
  .map-container {
    margin-top: 30px;
    border-radius: 10px;
    overflow: hidden;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  }
  
  .map-responsive {
    overflow: hidden;
    padding-bottom: 400px;
    position: relative;
    height: 0;
  }
  
  .map-responsive iframe {
    left: 0;
    top: 0;
    height: 100%;
    width: 100%;
    position: absolute;
    border: none;
  }
  
  @media (max-width: 768px) {
    .contact-container {
      padding: 10px;
    }
    
    .contact-info {
      padding: 20px;
    }
    
    .map-responsive {
      padding-bottom: 300px;
    }
  }
</style>

<div class="contact-container">
  
  <!-- Contact Information -->
  <div class="contact-info">
    <h3 style="margin-bottom: 25px; color: #333;">📍 Contact Information</h3>
    
    <div class="contact-item">
      <i class="fas fa-map-marker-alt"></i>
      <div>
        <strong>Address:</strong><br>
        Department of Computing, Mong Man Wai Building<br>
        The Hong Kong Polytechnic University<br>
        Hung Hom, Kowloon, Hong Kong SAR
      </div>
    </div>
    
    <div class="contact-item">
      <i class="fas fa-envelope"></i>
      <div>
        <strong>Email:</strong><br>
        <a href="mailto:jc-jingcai.guo@polyu.edu.hk">jc-jingcai.guo@polyu.edu.hk</a>
      </div>
    </div>
    
    <div class="contact-item">
      <i class="fas fa-phone"></i>
      <div>
        <strong>Phone:</strong><br>
        +852 2766 4009
      </div>
    </div>
    
    <div class="contact-item">
      <i class="fas fa-building"></i>
      <div>
        <strong>Office:</strong><br>
        PQ749, Department of Computing
      </div>
    </div>
  </div>
  
  <!-- Map Section -->
  <div class="map-container">
    <h3 style="margin-bottom: 20px; color: #333;">🗺️ Find Us</h3>
    <div class="map-responsive">
      <!-- Google Maps Embed for Hong Kong Polytechnic University -->
      <iframe 
        src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3691.8947725858537!2d114.17699431495395!3d22.303658885316654!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x340400e83e2fc723%3A0xcc7d8318c5f6b7e8!2sThe%20Hong%20Kong%20Polytechnic%20University!5e0!3m2!1sen!2shk!4v1640000000000!5m2!1sen!2shk" 
        allowfullscreen="" 
        loading="lazy" 
        referrerpolicy="no-referrer-when-downgrade">
      </iframe>
    </div>
  </div>
  
  <!-- Additional Information -->
  <div style="margin-top: 30px; padding: 20px; background-color: #e9ecef; border-radius: 10px;">
    <h4 style="color: #333; margin-bottom: 15px;">🚇 How to Get Here</h4>
    <ul style="color: #555;">
      <li><strong>MTR:</strong> Take the East Rail Line to Hung Hom Station (Exit B2)</li>
      <li><strong>Bus:</strong> Multiple bus routes serve the university area</li>
      <li><strong>Taxi:</strong> Show the driver: 香港理工大學 (Hong Kong Polytechnic University)</li>
    </ul>
  </div>
  
</div>
