<template>
  <div class="wedding-page">
    <!-- Home Section -->
    <section class="hero">
      <div class="hero-overlay"></div>
      <div class="hero-content">
        <p class="invitation-text">Wedding Invitation</p>
        <div class="couple-names">
          <div class="person">
            <span class="name">Min Khan Kyi</span>
            <span class="degree">(BVSc)</span>
          </div>
          <span class="amp">&</span>
          <div class="person">
            <span class="name">Yin Thway Htun</span>
            <span class="degree">(BVSc)</span>
          </div>
        </div>
        <div class="couple-company">Sunjin Myanmar Co.,Ltd</div>
        <div class="divider"></div>
        <p class="tagline">We're getting married</p>
        <p class="date">12-02-2026 (Friday)</p>
      </div>
    </section>

    <!-- Invitation Card Section -->
    <section class="invitation-section">
      <div class="invitation-container">
        <h2 class="section-title">ဖိတ်ကြားလွှာ</h2>
        <p class="section-subtitle">Invitation Card</p>
        <div class="invitation-card">
          <img src="/image/4.jpg" alt="Myanmar Wedding Invitation Card" />
        </div>
      </div>
    </section>

    <!-- Event Details Section -->
    <section class="event-section">
      <div class="event-container">
        <h2 class="section-title">အခမ်းအနားအချိန်နှင့်နေရာ</h2>
        <p class="section-subtitle">Event Details</p>

        <div class="event-details">
          <div class="event-item">
            <div class="event-icon">📅</div>
            <div class="event-info">
              <h3>ရက်စွဲ</h3>
              <p>၁၃၈၅-ခု၊ တပို့တွဲလပြည့်ကျော်(၁၁)ရက်</p>
              <p>12-02-2026 (ကြာသပတေးနေ့)</p>
            </div>
          </div>

          <div class="event-item">
            <div class="event-icon">🕐</div>
            <div class="event-info">
              <h3>အချိန်</h3>
              <p>နံနက် (၇:၀၀) နာရီမှ (၁၀:၀၀) နာရီထိ</p>
            </div>
          </div>

          <div class="event-item">
            <div class="event-icon">📍</div>
            <div class="event-info">
              <h3>နေရာ</h3>
              <p>မုံရွာမြို့၊ ချမ်းမြဝတီရပ်ကွက်၊</p>
              <p>ဗန္ဓုလလမ်း (ဆည်မြောင်ရုံးလမ်း) နှင့် အနော်ရထားလမ်း (ရေကူးကန်လမ်း) ထောင့်၊</p>
              <p>ဗိုလ်မှူးသန်းမြင့် (ငြိမ်း) နေအိမ်</p>
            </div>
          </div>
        </div>

        <div class="event-map">
          <iframe
            src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d59914.23376991547!2d95.10697379260115!3d22.106599035298093!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x30ca98d563cb266b%3A0x56b860fde1c4e9ca!2sMonywa%2C%20Myanmar%20(Burma)!5e1!3m2!1sen!2ssg!4v1770215373834!5m2!1sen!2ssg"
            width="100%"
            height="300"
            style="border:0;"
            allowfullscreen=""
            loading="lazy"
            referrerpolicy="no-referrer-when-downgrade">
          </iframe>
        </div>
      </div>
    </section>

    <!-- Photo Gallery Section -->
    <section class="gallery-section">
      <div class="gallery-container">
        <h2 class="section-title">ဓာတ်ပုံများ</h2>
        <p class="section-subtitle">Photo Gallery</p>
        <div class="gallery-grid">
          <div class="gallery-item">
            <img src="/image/1.jpg" alt="Wedding Photo 1" />
          </div>
          <div class="gallery-item">
            <img src="/image/2.jpg" alt="Wedding Photo 2" />
          </div>
          <div class="gallery-item">
            <img src="/image/3.jpg" alt="Wedding Photo 3" />
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup lang="ts">
useHead({
  title: 'Wedding Invitation - Dr Min Khan Kyi & Yin Thway Htun',
  meta: [
    { name: 'viewport', content: 'width=device-width, initial-scale=1' }
  ]
})
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html, body {
  height: 100%;
  font-family: 'Georgia', 'Times New Roman', serif;
}

.wedding-page {
  min-height: 100vh;
}

/* Hero Section */
.hero {
  position: relative;
  height: 100vh;
  min-height: 600px;
  background-image: url('/image/mobile-bg.png');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  display: flex;
  align-items: center;
  justify-content: center;
}

.hero-overlay {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: linear-gradient(
    to bottom,
    rgba(0, 0, 0, 0.3) 0%,
    rgba(0, 0, 0, 0.1) 50%,
    rgba(0, 0, 0, 0.4) 100%
  );
}

.hero-content {
  position: relative;
  z-index: 1;
  text-align: center;
  color: #fff;
  padding: 20px;
}

.invitation-text {
  font-size: 1rem;
  letter-spacing: 4px;
  text-transform: uppercase;
  margin-bottom: 16px;
  opacity: 0.9;
  font-weight: 300;
}

.couple-names {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 8px;
  margin-bottom: 15px;
}

.person {
  display: flex;
  align-items: baseline;
  gap: 8px;
}

.person .name {
  font-size: 1.8rem;
  font-weight: 400;
  letter-spacing: 2px;
  color: #d4af37;
  text-shadow: 2px 2px 8px rgba(0, 0, 0, 0.5);
}

.person .degree {
  font-size: 1rem;
  font-weight: 300;
  color: #fff;
  opacity: 0.9;
}

.amp {
  font-size: 1.2rem;
  color: #fff;
  opacity: 0.8;
}

.couple-company {
  font-size: 0.9rem;
  color: #fff;
  opacity: 0.85;
  margin-bottom: 20px;
  letter-spacing: 1px;
}

.divider {
  width: 60px;
  height: 2px;
  background: #fff;
  margin: 0 auto 20px;
  opacity: 0.8;
}

.tagline {
  font-size: 1.1rem;
  font-style: italic;
  opacity: 0.9;
  letter-spacing: 1px;
  margin-bottom: 12px;
}

.date {
  font-size: 1.2rem;
  letter-spacing: 3px;
  opacity: 0.95;
  font-weight: 300;
}

/* Invitation Card Section */
.invitation-section {
  background: linear-gradient(135deg, #f8f6f2 0%, #ede8e0 100%);
  padding: 60px 20px;
}

.invitation-container {
  max-width: 600px;
  margin: 0 auto;
  text-align: center;
}

.section-title {
  font-size: 1.8rem;
  color: #8b7355;
  margin-bottom: 8px;
  font-weight: 400;
}

.section-subtitle {
  font-size: 1rem;
  color: #a89070;
  letter-spacing: 2px;
  text-transform: uppercase;
  margin-bottom: 30px;
}

.invitation-card {
  background: #fff;
  padding: 15px;
  border-radius: 8px;
  box-shadow: 0 10px 40px rgba(0, 0, 0, 0.1);
}

.invitation-card img {
  width: 100%;
  height: auto;
  display: block;
  border-radius: 4px;
}

/* Event Details Section */
.event-section {
  background: #fff;
  padding: 60px 20px;
}

.event-container {
  max-width: 700px;
  margin: 0 auto;
  text-align: center;
}

.event-details {
  display: flex;
  flex-direction: column;
  gap: 25px;
  margin-bottom: 40px;
}

.event-item {
  display: flex;
  align-items: flex-start;
  gap: 15px;
  text-align: left;
  background: linear-gradient(135deg, #f8f6f2 0%, #ede8e0 100%);
  padding: 20px;
  border-radius: 10px;
}

.event-icon {
  font-size: 1.8rem;
  flex-shrink: 0;
}

.event-info h3 {
  font-size: 1.1rem;
  color: #8b7355;
  margin-bottom: 8px;
  font-weight: 500;
}

.event-info p {
  font-size: 0.95rem;
  color: #5a5a5a;
  line-height: 1.6;
  margin: 0;
}

.event-map {
  border-radius: 10px;
  overflow: hidden;
  box-shadow: 0 8px 30px rgba(0, 0, 0, 0.1);
}

.event-map iframe {
  display: block;
}

/* Photo Gallery Section */
.gallery-section {
  background: #fff;
  padding: 60px 20px;
}

.gallery-container {
  max-width: 800px;
  margin: 0 auto;
  text-align: center;
}

.gallery-grid {
  display: grid;
  grid-template-columns: 1fr;
  gap: 20px;
}

.gallery-item {
  overflow: hidden;
  border-radius: 8px;
  box-shadow: 0 8px 30px rgba(0, 0, 0, 0.12);
}

.gallery-item img {
  width: 100%;
  height: auto;
  display: block;
  transition: transform 0.3s ease;
}

.gallery-item:hover img {
  transform: scale(1.02);
}

/* Mobile First - Default styles above are for mobile */

/* Tablet and up */
@media (min-width: 768px) {
  .invitation-text {
    font-size: 1.2rem;
    letter-spacing: 6px;
  }

  .couple-names {
    flex-direction: row;
    gap: 20px;
  }

  .person .name {
    font-size: 2.5rem;
  }

  .person .degree {
    font-size: 1.1rem;
  }

  .amp {
    font-size: 1.5rem;
  }

  .couple-company {
    font-size: 1rem;
  }

  .tagline {
    font-size: 1.3rem;
  }

  .date {
    font-size: 1.4rem;
  }

  .divider {
    width: 80px;
  }

  .invitation-section {
    padding: 80px 40px;
  }

  .section-title {
    font-size: 2.2rem;
  }

  .invitation-card {
    padding: 20px;
  }

  .event-section {
    padding: 80px 40px;
  }

  .event-item {
    padding: 25px;
  }

  .event-icon {
    font-size: 2rem;
  }

  .event-info h3 {
    font-size: 1.2rem;
  }

  .event-info p {
    font-size: 1rem;
  }

  .event-map iframe {
    height: 350px;
  }

  .gallery-section {
    padding: 80px 40px;
  }

  .gallery-grid {
    grid-template-columns: repeat(2, 1fr);
    gap: 25px;
  }
}

/* Desktop */
@media (min-width: 1024px) {
  .hero {
    background-image: url('/image/desktop-bg.png');
  }

  .person .name {
    font-size: 3rem;
  }

  .person .degree {
    font-size: 1.2rem;
  }

  .amp {
    font-size: 1.8rem;
  }

  .couple-company {
    font-size: 1.1rem;
  }

  .invitation-text {
    font-size: 1.4rem;
  }

  .tagline {
    font-size: 1.5rem;
  }

  .date {
    font-size: 1.5rem;
  }

  .invitation-section {
    padding: 100px 40px;
  }

  .event-section {
    padding: 100px 40px;
  }

  .event-details {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 25px;
  }

  .event-item:last-child {
    grid-column: 1 / -1;
  }

  .event-map iframe {
    height: 400px;
  }

  .gallery-section {
    padding: 100px 40px;
  }

  .gallery-grid {
    gap: 30px;
  }
}
</style>
