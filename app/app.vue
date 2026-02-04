<template>
  <div class="wedding-page">
    <!-- Home Section -->
    <section class="hero">
      <div class="hero-overlay"></div>
      <div class="hero-content">
        <p class="invitation-text">Wedding Invitation</p>
        <h1 class="couple-names">Min Khan Kyi & Yin Thway Htun</h1>
        <div class="divider"></div>
        <p class="tagline">We're getting married</p>
        <p class="date">1st February 2026</p>
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
  </div>
</template>

<script setup lang="ts">
useHead({
  title: 'Wedding Invitation - Min Khan Kyi & Yin Thway Htun',
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
  background-image: url('/image/2.jpg');
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
  font-size: 2.2rem;
  font-weight: 400;
  letter-spacing: 2px;
  margin-bottom: 20px;
  text-shadow: 2px 2px 8px rgba(0, 0, 0, 0.3);
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

/* Mobile First - Default styles above are for mobile */

/* Tablet and up */
@media (min-width: 768px) {
  .invitation-text {
    font-size: 1.2rem;
    letter-spacing: 6px;
  }

  .couple-names {
    font-size: 3.5rem;
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
}

/* Desktop */
@media (min-width: 1024px) {
  .couple-names {
    font-size: 4rem;
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
}
</style>
