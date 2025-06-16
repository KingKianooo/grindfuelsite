---
layout: single
title: "About GrindFuel"
permalink: /project/
author_profile: false
header:
  overlay_color: "#000"
  overlay_filter: "0.4"
  overlay_image: /assets/images/grindfuel-project.jpg
---

## GrindFuel Feature Tour

Below you’ll find short walkthrough clips that demonstrate each major part of the GrindFuel workflow.

---

### 1  Create a Project

<style>
.video-wrapper {
  margin: 1.5rem 0;
}

.play-container {
  position: relative;
  width: 100%;
  max-width: 100%;
  border-radius: 8px;
  overflow: hidden;
  margin-bottom: 1rem;
}

.play-container video {
  width: 100%;
  display: block;
  border-radius: 8px;
}

.play-button {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  background: rgba(0,0,0,0.6);
  color: white;
  font-size: 2rem;
  padding: 0.75rem 1.25rem;
  border: none;
  border-radius: 8px;
  cursor: pointer;
  z-index: 10;
  transition: background 0.3s ease;
}

.play-button:hover {
  background: rgba(0,0,0,0.8);
}
</style>

<div class="play-container">
  <video id="video-intro" playsinline>
    <source src="{{ '/assets/videos/create_new_project_page.mp4' | relative_url }}" type="video/mp4">
    Your browser does not support the video tag.
  </video>
  <button id="video-play-button" class="play-button">▶ Play</button>
</div>

<script>
document.addEventListener("DOMContentLoaded", function() {
  const video = document.getElementById("video-intro");
  const playBtn = document.getElementById("video-play-button");

  playBtn.addEventListener("click", function() {
    video.play();
    playBtn.style.display = "none";
  });

  video.addEventListener("ended", function() {
    playBtn.style.display = "block";
    video.currentTime = 0;
  });
});
</script>

GrindFuel starts by prompting you to create the project you want to tackle. Enter a **valid project name** and **due date**, then jump straight into adding the tasks that will define your success.

---

### 2  Outline Your Tasks

<div class="video-wrapper">
  <video autoplay loop muted playsinline style="width: 100%; border-radius: 8px;">
    <source src="{{ '/assets/videos/create-task.mp4' | relative_url }}" type="video/mp4">
  </video>
</div>

For every task you add, specify a **title**, an **effort estimate**, and a **due date**. You can also add an optional description for extra clarity. Checking tasks off feels great—and keeps your progress visible.

---

### 3  Turn Tasks into Checklists

<div class="video-wrapper">
  <video autoplay loop muted playsinline style="width: 100%; border-radius: 8px;">
    <source src="{{ '/assets/videos/task-checklist.mp4' | relative_url }}" type="video/mp4">
  </video>
</div>

Break complex tasks into bite-sized checklist items so you always know the next actionable step. Edit tasks or checklist items any time; your workflow adapts as you do.

---

### 4  Meet Your Digital Companion

<div class="video-wrapper">
  <video autoplay loop muted playsinline style="width: 100%; border-radius: 8px;">
    <source src="{{ '/assets/videos/andy-companion.mp4' | relative_url }}" type="video/mp4">
  </video>
</div>

Working solo doesn’t have to feel lonely. Your companion sits quietly on your dashboard, offering a calming presence and gentle encouragement as you work through your project.

---

### 5  Level Up by Getting Things Done

<div class="video-wrapper">
  <video autoplay loop muted playsinline style="width: 100%; border-radius: 8px;">
    <source src="{{ '/assets/videos/level-up.mp4' | relative_url }}" type="video/mp4">
  </video>
</div>

Each completed task grants experience points—watch meaningless numbers climb while you accomplish meaningful work.

---

### 6  Reward Yourself: Customize Andy

<div class="video-wrapper">
  <video autoplay loop muted playsinline style="width: 100%; border-radius: 8px;">
    <source src="{{ '/assets/videos/shop-accessories.mp4' | relative_url }}" type="video/mp4">
  </video>
</div>

Spend earned currency in the **Shop** to unlock unique accessories and outfits for Andy. Personalize your companion as a tangible reminder of your progress.
{% comment %}
---
layout: single
title: "About GrindFuel"
permalink: /project/
author_profile: false
header:
  overlay_color: "#000"
  overlay_filter: "0.4"
  overlay_image: /assets/images/grindfuel-project.jpg
---

## GrindFuel Feature Tour

Below you’ll find short walkthrough clips that demonstrate each major part of the GrindFuel workflow.

---

### 1  Create a Project

<video id="intro" autoplay loop playsinline style="width: 100%; border-radius: 8px;">
  <source src="{{ '/assets/videos/create_new_project_page.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

GrindFuel starts by prompting you to create the project you want to tackle. Enter a **valid project name** and **due date**, then jump straight into adding the tasks that will define your success.

---

### 2  Outline Your Tasks

<div class="video-wrapper">
  <video src="/assets/videos/create-task.mp4" loop muted playsinline style="width: 100%; border-radius: 8px;"></video>
</div>

For every task you add, specify a **title**, an **effort estimate**, and a **due date**. You can also add an optional description for extra clarity. Checking tasks off feels great—and keeps your progress visible.

---

### 3  Turn Tasks into Checklists

<div class="video-wrapper">
  <video src="/assets/videos/task-checklist.mp4" loop muted playsinline style="width: 100%; border-radius: 8px;"></video>
</div>

Break complex tasks into bite-sized checklist items so you always know the next actionable step. Edit tasks or checklist items any time; your workflow adapts as you do.

---

### 4  Meet Your Digital Companion

<div class="video-wrapper">
  <video src="/assets/videos/andy-companion.mp4" loop muted playsinline style="width: 100%; border-radius: 8px;"></video>
</div>

Working solo doesn’t have to feel lonely. Your companion sits quietly on your dashboard, offering a calming presence and gentle encouragement as you work through your project.

---

### 5  Level Up by Getting Things Done

<div class="video-wrapper">
  <video src="/assets/videos/level-up.mp4" loop muted playsinline style="width: 100%; border-radius: 8px;"></video>
</div>

Each completed task grants experience points—watch meaningless numbers climb while you accomplish meaningful work.

---

### 6  Reward Yourself: Customize Andy

<div class="video-wrapper">
  <video src="/assets/videos/shop-accessories.mp4" loop muted playsinline style="width: 100%; border-radius: 8px;"></video>
</div>

Spend earned currency in the **Shop** to unlock unique accessories and outfits for Andy. Personalize your companion as a tangible reminder of your progress.

---

{% raw %}
<script>
document.addEventListener("DOMContentLoaded", () => {
  const videos = document.querySelectorAll("video");

  const observer = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
      const video = entry.target;
      if (entry.isIntersecting) {
        video.play();
      } else {
        video.pause();
        video.currentTime = 0;
      }
    });
  }, { threshold: 0.5 });

  videos.forEach(video => {
    video.pause();
    observer.observe(video);
  });
});
</script>
{% endraw %}

<!--
{% raw %}
<style>
.video-wrapper {
  margin: 1.5rem 0;
}
</style>
{% endraw %}
-->
{% endcomment %}

{% comment %}
---
layout: single
title: "About GrindFuel"
permalink: /project/
author_profile: false
header:
  overlay_color: "#000"
  overlay_filter: "0.4"
  overlay_image: /assets/images/grindfuel-project.jpg
---

## GrindFuel Feature Tour

Below you’ll find short walkthrough clips that demonstrate each major part of the GrindFuel workflow.

---

### 1  Create a Project

<div class="video-wrapper">
  <video src="/assets/videos/create_new_project_page.mp4" autoplay loop muted playsinline style="width: 100%; border-radius: 8px;"></video>
</div>

GrindFuel starts by prompting you to create the project you want to tackle. Enter a **valid project name** and **due date**, then jump straight into adding the tasks that will define your success.

---

### 2  Outline Your Tasks

<div class="video-wrapper">
  <video src="/assets/videos/create-task.mp4" autoplay loop muted playsinline style="width: 100%; border-radius: 8px;"></video>
</div>

For every task you add, specify a **title**, an **effort estimate**, and a **due date**. You can also add an optional description for extra clarity. Checking tasks off feels great—and keeps your progress visible.

---

### 3  Turn Tasks into Checklists

<div class="video-wrapper">
  <video src="/assets/videos/task-checklist.mp4" autoplay loop muted playsinline style="width: 100%; border-radius: 8px;"></video>
</div>

Break complex tasks into bite-sized checklist items so you always know the next actionable step. Edit tasks or checklist items any time; your workflow adapts as you do.

---

### 4  Meet Your Digital Companion

<div class="video-wrapper">
  <video src="/assets/videos/andy-companion.mp4" autoplay loop muted playsinline style="width: 100%; border-radius: 8px;"></video>
</div>

Working solo doesn’t have to feel lonely. Your companion sits quietly on your dashboard, offering a calming presence and gentle encouragement as you work through your project.

---

### 5  Level Up by Getting Things Done

<div class="video-wrapper">
  <video src="/assets/videos/level-up.mp4" autoplay loop muted playsinline style="width: 100%; border-radius: 8px;"></video>
</div>

Each completed task grants experience points—watch meaningless numbers climb while you accomplish meaningful work.

---

### 6  Reward Yourself: Customize Andy

<div class="video-wrapper">
  <video src="/assets/videos/shop-accessories.mp4" autoplay loop muted playsinline style="width: 100%; border-radius: 8px;"></video>
</div>

Spend earned currency in the **Shop** to unlock unique accessories and outfits for Andy. Personalize your companion as a tangible reminder of your progress.

---

{% raw %}
<style>
.video-wrapper {
  margin: 1.5rem 0;
}
</style>
{% endraw %}
{% endcomment %}
