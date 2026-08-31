<script setup>
import heroImage from './assets/service-grills.svg'
import fryerImage from './assets/service-grills.svg'
import grillImage from './assets/service-grills.svg'
import holdingImage from './assets/service-holding.svg'
import riceImage from './assets/service-holding.svg'
import beverageImage from './assets/service-facility.svg'
import facilityImage from './assets/service-facility.svg'
import gordonsLogo from './assets/gordons-logo.jpg'

const portalUrl = 'https://portal.gordonsservice.com/portal'
const facebookUrl = 'https://www.facebook.com/share/19SqDJ3idv/?mibextid=wwXIfr'

const services = [
  { icon: '♨', title: 'Fryers', text: 'Diagnostics, repairs, controls, filtration, and performance restoration.', image: fryerImage, position: 'left 55%' },
  { icon: '≋', title: 'Grills & Griddles', text: 'Flat tops, clamshell grills, charbroilers, controls, and cooking systems.', image: grillImage, position: 'center 55%' },
  { icon: '⌁', title: 'Holding Equipment', text: 'Warmers, holding cabinets, heat lamps, and temperature-control equipment.', image: holdingImage, position: 'center 50%' },
  { icon: '◒', title: 'Rice Cookers', text: 'Repair and maintenance for dependable, consistent performance.', image: riceImage, position: 'right 50%' },
  { icon: '◉', title: 'Beverage Equipment', text: 'Bunn equipment, dispensers, brewers, and related commercial systems.', image: beverageImage, position: 'left 50%' },
  { icon: '⚙', title: 'Facility Services', text: 'Preventive maintenance, repairs, troubleshooting, and general facility support.', image: facilityImage, position: 'center 50%' },
]

const benefits = [
  { icon: '◴', title: 'Fast Response', text: 'Quick turnaround to minimize downtime and keep your business moving.' },
  { icon: '✓', title: 'Expert Diagnostics', text: 'Experienced troubleshooting focused on finding the actual cause.' },
  { icon: '⚙', title: 'Quality Parts', text: 'Reliable parts and proven repair solutions for long-lasting performance.' },
  { icon: '◇', title: 'Honest Service', text: 'Straightforward answers, clear communication, and fair recommendations.' },
]
</script>

<template>
  <div class="site-shell">
    <header class="topbar">
      <a class="brand" href="#home" aria-label="Gordon's Kitchen Diagnostics home">
        <img
          :src="gordonsLogo"
          alt="Gordon's Kitchen Diagnostics logo"
          style="width:82px;height:82px;object-fit:contain;border-radius:10px;background:#fff;padding:3px;box-shadow:0 0 24px rgba(22,136,255,.28)"
        />
        <div class="brand-copy"><strong>GORDON'S</strong><span>KITCHEN DIAGNOSTICS</span></div>
      </a>
      <nav class="nav-links" aria-label="Primary navigation"><a href="#home">Home</a><a href="#services">Services</a><a href="#about">About</a><a href="#service-area">Service Area</a><a :href="portalUrl">Customer Portal</a><a href="#contact">Contact</a></nav>
      <a class="button button-primary header-cta" :href="portalUrl">Request Service</a>
    </header>
    <main>
      <section id="home" class="hero-section"><div class="hero-photo" :style="{ backgroundImage: `url(${heroImage})` }" aria-hidden="true"></div><div class="hero-shade" aria-hidden="true"></div><div class="hero-content"><p class="eyebrow">Commercial kitchen equipment service • Iowa</p><h1>Keeping your kitchen running.<br /><span>So you can keep going.</span></h1><p class="hero-copy">Fast diagnostics. Honest repairs. Quality service you can count on for the commercial kitchen equipment your business relies on every day.</p><div class="hero-actions"><a class="button button-primary" :href="portalUrl">Request Service</a><a id="portal" class="button button-outline" :href="portalUrl">Customer Portal</a></div></div></section>
      <section class="benefits-section" aria-label="Why choose Gordon's"><article v-for="benefit in benefits" :key="benefit.title" class="benefit"><div class="benefit-icon">{{ benefit.icon }}</div><div><h3>{{ benefit.title }}</h3><p>{{ benefit.text }}</p></div></article></section>
      <section id="services" class="services-section section-pad"><div class="section-heading"><p class="eyebrow blue">Our services</p><h2>We service the equipment you rely on</h2><p>Focused commercial kitchen repair and facility support for restaurants and food-service operations across Iowa.</p></div><div class="service-grid"><article v-for="service in services" :key="service.title" class="service-card"><div class="service-photo" :style="{ backgroundImage: `linear-gradient(180deg, rgba(4,24,48,.03), rgba(3,20,39,.62)), url(${service.image})`, backgroundPosition: service.position }"><div class="service-icon">{{ service.icon }}</div></div><div class="service-content"><h3>{{ service.title }}</h3><p>{{ service.text }}</p></div></article></div></section>
      <section class="story-area"><div id="about" class="story-panel"><div class="flower-art" aria-hidden="true">✿</div><div><p class="eyebrow">The Gordon's standard</p><h2>Built on hard work & dedication</h2><p>Gordon's Kitchen Diagnostics is named in honor of my grandfather, Gordon, who grew the most amazing flowers through patience, hard work, and dedication. Those are the same values we bring to every job.</p><strong>We don't just fix equipment — we help keep your business moving.</strong></div></div><div id="service-area" class="iowa-panel"><div class="pin">●</div><div><p class="eyebrow">Service area</p><h2>Proudly serving all of Iowa</h2><p>From local restaurants to multi-location operations, Gordon's provides dependable service throughout the state.</p><div class="iowa-outline">IOWA</div></div></div></section>
    </main>
    <footer id="contact" class="contact-bar"><div class="contact-lead"><span class="phone-icon">☎</span><div><small>Need service today?</small><strong>We're ready to help.</strong></div></div><a href="tel:+15152904476">(515) 290-4476</a><a href="mailto:brian@gordonsservice.com">brian@gordonsservice.com</a><a :href="facebookUrl" target="_blank" rel="noopener noreferrer">Facebook</a><span>Serving customers across Iowa</span></footer>
  </div>
</template>
