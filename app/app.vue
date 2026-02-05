<template>
  <div class="wedding-page">
    <!-- Home Section -->
    <section class="hero">
      <div class="hero-overlay"></div>
      <div class="hero-content">
        <p class="invitation-text">Wedding Invitation</p>
        <div class="couple-names">
          <div class="person">
            <span class="name">Dr.Min Khant Kyi </span>
          </div>
          <span class="amp">&</span>
          <div class="person">
            <span class="name">Ma Yin Thwe Tun </span>
          </div>
        </div>
        <div class="couple-company">Sunjin Myanmar Co.,Ltd</div>
        <div class="divider"></div>
        <p class="tagline">We're getting married</p>
        <p class="date">22.2.2026 (Sunday)</p>
      </div>
    </section>

    <!-- Invitation Card Section -->
    <section class="invitation-section">
      <div class="invitation-container">
        <h2 class="section-title">ဖိတ်ကြားလွှာ</h2>
        <p class="section-subtitle">Invitation Card</p>
        <div class="invitation-card" @click="showLightbox = true">
          <img src="/image/w01.jpg" alt="Myanmar Wedding Invitation Card" />
          <div class="click-hint">Click to view</div>
        </div>
      </div>
    </section>

    <!-- Lightbox Modal -->
    <div v-if="showLightbox" class="lightbox" @click="showLightbox = false">
      <button class="lightbox-close">&times;</button>
      <img src="/image/w01.jpg" alt="Myanmar Wedding Invitation Card" @click.stop />
    </div>

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
              <p>၁၃၈၇-ခု၊ တပေါင်းလဆန်း (7)ရက်</p>
              <p>၂၂-၂-၂၀၂၆ (တနင်္ဂနွေနေ့)</p>
            </div>
          </div>

          <div class="event-item">
            <div class="event-icon">🕐</div>
            <div class="event-info">
              <h3>အချိန်</h3>
              <p>နံနက် (၈:၀၀) နာရီမှ (၁၂:၀၀) နာရီထိ</p>
            </div>
          </div>

          <div class="event-item">
            <div class="event-icon">📍</div>
            <div class="event-info">
              <h3>နေရာ</h3>
              <p>မဟာဝိဇိတာရုံကျောင်းတိုက်၊၆၈လမ်း/၃၁*၃၂လမ်းကြား
                </p>
              <p>ချမ်းအေးသာဇံမြို့နယ်၊မန္တလေးမြို့</p>
            </div>
          </div>
        </div>

        <div class="event-map">
          <iframe
            src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3748.1592581077443!2d96.10395659999999!3d21.9736384!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x30cb6d0436da9465%3A0xc410cb2e3914ef85!2sMaha%20Wizidaryone%20Monastery!5e1!3m2!1sen!2smm!4v1770255326004!5m2!1sen!2smm"
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
const showLightbox = ref(false)

useHead({
  title: 'Wedding Invitation - Dr Min Khan Kyi & Yin Thway Htun',
  meta: [
    { name: 'viewport', content: 'width=device-width, initial-scale=1' }
  ],
  link: [
    { rel: 'icon', type: 'image/jpeg', href: '/image/1.jpg' }
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
  background-image: url('/image/3.jpg');
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
  cursor: pointer;
  position: relative;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.invitation-card:hover {
  transform: scale(1.02);
  box-shadow: 0 15px 50px rgba(0, 0, 0, 0.15);
}

.invitation-card img {
  width: 100%;
  height: auto;
  display: block;
  border-radius: 4px;
}

.click-hint {
  position: absolute;
  bottom: 25px;
  left: 50%;
  transform: translateX(-50%);
  background: rgba(0, 0, 0, 0.6);
  color: #fff;
  padding: 8px 16px;
  border-radius: 20px;
  font-size: 0.85rem;
  opacity: 0;
  transition: opacity 0.3s ease;
}

.invitation-card:hover .click-hint {
  opacity: 1;
}

/* Lightbox Modal */
.lightbox {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.9);
  display: flex;
  align-items: center;
  justify-content: center;
  z-index: 1000;
  cursor: pointer;
}

.lightbox img {
  max-width: 90%;
  max-height: 90%;
  object-fit: contain;
  border-radius: 4px;
  cursor: default;
}

.lightbox-close {
  position: absolute;
  top: 20px;
  right: 20px;
  background: none;
  border: none;
  color: #fff;
  font-size: 2.5rem;
  cursor: pointer;
  line-height: 1;
  padding: 10px;
  opacity: 0.8;
  transition: opacity 0.3s ease;
}

.lightbox-close:hover {
  opacity: 1;
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
