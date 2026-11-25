---
permalink: /
title: ""
excerpt: ""
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

{% if site.google_scholar_stats_use_cdn %}
{% assign gsDataBaseUrl = "https://cdn.jsdelivr.net/gh/" | append: site.repository | append: "@" %}
{% else %}
{% assign gsDataBaseUrl = "https://raw.githubusercontent.com/" | append: site.repository | append: "/" %}
{% endif %}
{% assign url = gsDataBaseUrl | append: "google-scholar-stats/gs_data_shieldsio.json" %}

<span class='anchor' id='about-me'></span>

<p>
I am a PhD candidate in Computer Science at <a href="https://www.stonybrook.edu/">Stony Brook University</a>, advised by <a href="https://paolacascante.com/">Prof. Paola Cascante-Bonilla</a> as part of the <a href="https://paolacascante.com/lab/">SPEL lab</a>. My research spans computer vision and natural language processing, with a focus on vision-language models, social scene understanding, and privacy-preserving AI. Before starting my PhD, I was a research assistant at the Federal University of Rio Grande do Sul.
</p>

<p>
In 2022, I obtained my Master's in Computer Science from <a href="http://www.ufrgs.br/ufrgs/inicial">Federal University of Rio Grande do Sul</a>, where I worked with <a href="https://www.inf.ufrgs.br/~crjung/">Prof. Claudio Rosito Jung</a> at the Department of Informatics. Our research focused on spherical images and oriented object detection; our Probabilistic IoU (ProbIoU) loss is now used for oriented boxes in <a href="https://github.com/ultralytics/ultralytics">Ultralytics YOLO</a> (YOLOv8, YOLO11, YOLO26). Previously, I obtained a Bachelor of Science in Computer Science from <a href="https://www.unitru.edu.pe/">National University of Trujillo</a>. During my undergraduate studies, I did an exchange program for a year at the <a href="https://www.icmc.usp.br/en/">University of São Paulo (ICMC)</a>.
</p>

**Research Interests:** VLM Reasoning, Social Scene Understanding, Privacy-Preserving AI, Open-Vocabulary Object Detection.

# 🔭 Research Directions

<div class="research-grid">
  <figure class="research-card">
    <video class="research-media" autoplay muted loop playsinline preload="metadata"
           poster="videos/egogroups.jpg" aria-label="EgoGroups annotation example: tracked people grouped into social groups in a first-person video">
      <source src="videos/egogroups.mp4" type="video/mp4">
    </video>
    <figcaption>
      <strong>Social Scene Understanding</strong>
      <span>Detecting social groups in first-person video across cultures and crowds (<a href="https://lab-spell.github.io/EgoGroups/">EgoGroups</a>).</span>
    </figcaption>
  </figure>
  <figure class="research-card">
    <video class="research-media" autoplay muted loop playsinline preload="metadata"
           poster="videos/figpriv.jpg" aria-label="A receipt photo masked by Gemini 2.5, GPT-4o, Mistral OCR, full fine-grained masking, and FiG-Priv, which masks only the high-risk numbers">
      <source src="videos/figpriv.mp4" type="video/mp4">
    </video>
    <figcaption>
      <strong>Privacy-Preserving AI</strong>
      <span>Fine-grained masking of private content in images captured by blind and low-vision users (<a href="https://artcs1.github.io/VLMPrivacy/">FiG-Priv, COLM 2025</a>).</span>
    </figcaption>
  </figure>
  <figure class="research-card">
    <video class="research-media" autoplay muted loop playsinline preload="metadata"
           poster="videos/probiou_hrsc.jpg" aria-label="Oriented ship detections on HRSC2016 trained with L1, GWD, KLD, and ProbIoU losses">
      <source src="videos/probiou_hrsc.mp4" type="video/mp4">
    </video>
    <figcaption>
      <strong>Oriented Object Detection</strong>
      <span>Gaussian box representations and losses, now used in Ultralytics YOLO (<a href="https://artcs1.github.io/ProbIoU-Loss/">ProbIoU</a>, <a href="https://artcs1.github.io/GauCho/">GauCho</a>).</span>
    </figcaption>
  </figure>
</div>

<script>
  // Respect "reduce motion": don't autoplay the research videos.
  if (window.matchMedia && window.matchMedia('(prefers-reduced-motion: reduce)').matches) {
    document.querySelectorAll('.research-media[autoplay]').forEach(function (v) { v.removeAttribute('autoplay'); v.pause(); v.controls = true; });
  }
</script>

# 🔥 News
- *2026.03*: &nbsp;📢 New preprint: **EgoGroups**, a first-person benchmark for detecting social groups in the wild!
- *2025.07*: &nbsp;🎉🎉 One paper accepted at **COLM'25**!
- *2025.02*: &nbsp;🎉🎉 One paper accepted at **CVPR'25**!
- *2024.10*: &nbsp;🎉🎉 One paper accepted at **WACV'25**!
- *2024.08*: &nbsp;🎉🎉 Started my PhD at **Stony Brook University**!

# 📝 Publications 


<div class='paper-box'><div class='paper-box-image'><div><div class="badge">arXiv 2026</div><img src='images/egogroups2026.jpg' alt="EgoGroups" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[EgoGroups: A Benchmark For Detecting Social Groups of People in the Wild](https://arxiv.org/abs/2603.22249)  
**arXiv preprint, 2026**

**Jeffri Murrugarra-Llerena**, Pranav Chitale, Zicheng Liu, Kai Ao, Yujin Ham, Guha Balakrishnan, Paola Cascante-Bonilla

<span class='paper-summary'>A first-person video benchmark for social group detection spanning 64 countries, crowd levels, and weather/time-of-day conditions; VLMs and LLMs can beat supervised baselines zero-shot, while crowd density and cultural region strongly affect performance.</span>

[**Project**](https://lab-spell.github.io/EgoGroups/) **|** [**Code**](https://github.com/lab-spell/EgoGroups) **|** [**Arxiv**](https://arxiv.org/abs/2603.22249)
</div>
</div>

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">COLM 2025</div><img src='images/colm2025.jpg' alt="COLM2025" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[Beyond Blanket Masking: Examining Granularity for Privacy Protection in Images Captured by Blind and Low Vision Users](https://arxiv.org/abs/2508.09245)  
**COLM 2025**

**Jeffri Murrugarra-Llerena\***, Haoran Niu\*, K. Suzanne Barber, Hal Daumé III, Yang Trista Cao, Paola Cascante-Bonilla

<span class='paper-summary'>FiG-Priv selectively masks only high-risk private content in photos taken by blind and low-vision users, preserving 26% more image content and improving VLM usefulness by 11% compared with blanket masking.</span>

[**Project**](https://artcs1.github.io/VLMPrivacy/) **|** [**Code**](https://github.com/Artcs1/VLM-Privacy) **|** [**Arxiv**](https://arxiv.org/abs/2508.09245)
</div>
</div>


<div class='paper-box'><div class='paper-box-image'><div><div class="badge">CVPR 2025</div><img src='images/cvpr2025.png' alt="CVPR2025" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[GauCho: Gaussian Distributions with Cholesky Decomposition for Oriented Object Detection](https://ieeexplore.ieee.org/document/11094078)  
**CVPR 2025**

Jose Henrique Lima Marques\*, **Jeffri Murrugarra-Llerena\***, Claudio Rosito Jung

<span class='paper-summary'>Predicts Gaussian distributions directly via Cholesky decomposition instead of oriented boxes, avoiding angular discontinuities; introduces Oriented Ellipses and works as a drop-in replacement for standard OBB heads.</span>

[**Project**](https://artcs1.github.io/GauCho/) **|** [**Code**](https://github.com/jhlmarques/GauCho) **|** [**Arxiv**](https://arxiv.org/abs/2502.01565)
</div>
</div>

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">WACV 2025</div><img src='images/wacv_2025.jpg' alt="WACV2025" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[Noise-Aware Evaluation of Object Detectors](https://ieeexplore.ieee.org/document/10943665)  
**WACV 2025**

**Jeffri Murrugarra-Llerena**, Claudio Rosito Jung

<span class='paper-summary'>An evaluation protocol for object detectors that accounts for noise in ground-truth bounding-box annotations.</span>

</div>
</div>



<div class='paper-box'><div class='paper-box-image'><div><div class="badge">IEEE TIP 2024</div><img src='images/ieee_tip2024.jpg' alt="IEEETIP2024" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[Probabilistic Intersection-Over-Union for Training and Evaluation of Oriented Object Detectors](https://ieeexplore.ieee.org/document/10382963)  
**IEEE Transactions on Image Processing, 2024**

🔥 *Adopted as the oriented-box localization loss in Ultralytics YOLOv8, YOLO11, and YOLO26.*

**Jeffri Murrugarra-Llerena**, Lucas Kirsten, Luis Felip Zeni, Claudio Rosito Jung

<span class='paper-summary'>Models oriented boxes as Gaussian distributions to obtain a differentiable, closed-form localization loss that also serves as an evaluation metric, with fewer hyperparameters than KLD and GWD.</span>

[**Project**](https://artcs1.github.io/ProbIoU-Loss/) **|** [**Code**](https://github.com/Artcs1/probiou-mmrotate) **|** [**Arxiv**](https://arxiv.org/abs/2106.06072)
</div>
</div>


<div class='paper-box'><div class='paper-box-image'><div><div class="badge">EMNLP 2022</div><img src='images/emnlp2022.png' alt="EMNLP2022" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[Improving Embeddings Representations for Comparing Higher Education Curricula: A Use Case in Computing](https://aclanthology.org/2022.emnlp-main.776/)  
**EMNLP, 2022**

**Jeffri Murrugarra-Llerena**, Fernando Manchego, Nils Murrugarra-Llerena

<span class='paper-summary'>Fine-tunes word embeddings with metric learning and course-guided attention to compare study-program curricula, with a use case contrasting computing curricula in the USA and Latin America.</span>

[**Project**](https://artcs1.github.io/DLCurriculas/) **|** [**Code**](https://github.com/Artcs1/DL_curriculas)
</div>
</div>


<div class='paper-box'><div class='paper-box-image'><div><div class="badge">CVPRW 2022</div><img src='images/cvprw_2022_2.jpg' alt="CVPRW 2022" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[Can We Trust Bounding Box Annotations for Object Detection?](https://ieeexplore.ieee.org/document/9857206)  
**CVPRW, 2022**

**Jeffri Murrugarra-Llerena**, Lucas Kirsten, Claudio Rosito Jung

<span class='paper-summary'>Studies how errors and variability in human bounding-box annotations affect the training and evaluation of object detectors.</span>
 
</div>
</div>


<div class='paper-box'><div class='paper-box-image'><div><div class="badge">CVPRW 2022</div><img src='images/cvprw2022_1.png' alt="CVPRW 2022" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[Pose Estimation for Two-View Panoramas Based on Keypoint Matching: A Comparative Study and Critical Analysis](https://ieeexplore.ieee.org/document/9857392)  
**CVPRW, 2022**

**Jeffri Murrugarra-Llerena**, Thiago Silveira, Claudio Rosito Jung

<span class='paper-summary'>A comparative study of keypoint matching and pose estimation methods for 360° panoramas, including tangent-plane projections to reduce spherical distortion.</span>

[**Project**](https://artcs1.github.io/POSE-KEYPOINTS-PANORAMA/) **|** [**Code**](https://github.com/Artcs1/Keypoints)
</div>
</div>


<div class='paper-box'><div class='paper-box-image'><div><div class="badge">ACM CSUR 2022</div><img src='images/csur2022.jpg' alt="ACM CSUR 2022" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[3D Scene Geometry Estimation from 360° Imagery: A Survey](https://dl.acm.org/doi/10.1145/3519021)  
**ACM CSUR, 2022**

Thiago Silveira, Paulo G. L. Pinto, **Jeffri Murrugarra-Llerena**, Claudio Jung

<span class='paper-summary'>A survey of 3D scene geometry estimation from omnidirectional images, covering spherical camera models, monocular layout and depth inference, and spherical stereo.</span>

[**Arxiv**](https://arxiv.org/abs/2401.09252)
</div>
</div>



# 🎖 Honors and Awards
- **ICVSS Scholarship**, International Computer Vision Summer School (2025).
- **VETTO Grant**, awarded to support data annotation for the EgoGroups project.
- **Khipu Assistant Grant**, to serve as a teaching/lab assistant at the Khipu AI Summer School.
- **Travel awards**: ICML 2019, CVPR 2022, EMNLP 2022, KHIPU 2023, LXAI-ICCV 2023, LXAI-CVPR 2025, COLM 2025.
- **Runner-up**, IA-CKATON para la Seguridad Vial hackathon (2022).
- **Runner-up**, Entel Challenge: Object Detection hackathon (2022).
- **CNPq Scholarship** for master's studies (2020–2022).
- **Ranked 1st** in the department, National University of Trujillo (2015–2019).

# 📖 Education
- **2024.08 - Now**, PhD in Computer Science, Stony Brook University (SBU), NY, USA. Advisor: Paola Cascante-Bonilla.
- **2020.03 - 2022.08**, Master in Computer Science, Federal University of Rio Grande do Sul (UFRGS), Porto Alegre, Brazil. Advisor: Claudio Rosito Jung.  
  Thesis: *Probabilistic Intersection-over-Union for Training and Evaluation of Oriented Object Detectors*.
- **2018.03 - 2018.12**, Exchange student, University of São Paulo (ICMC), São Carlos, Brazil. Represented USP at the ICPC Brazil Subregional (Maratona de Programação SBC) 2018.
- **2015.03 - 2019.12**, Bachelor in Computer Science, National University of Trujillo (UNT), Peru. Ranked 1st in the department.

# 🔬 Research Experience
- **2026.01 - Now**, Research Assistant, [Synthetic Perception and Learning Lab (SPEL)](https://paolacascante.com/lab/), Stony Brook University. Advisor: Paola Cascante-Bonilla.
- **2020.03 - 2024.01**, Research Assistant, Computer Vision Lab, Federal University of Rio Grande do Sul. Advisor: Claudio Rosito Jung.

# 👨‍🏫 Teaching
- **2024.08 - 2025.12**, Teaching Assistant, Stony Brook University: Analysis of Algorithms; Artificial Intelligence.
- **2024.01 - 2024.08**, Lecturer, National University of Engineering (UNI), Lima, Peru: Introduction to Algorithms and Machine Learning.
- **2020.03 - 2020.08**, Teaching Assistant, Federal University of Rio Grande do Sul: Introduction to Programming.

# 🤝 Service
- **Reviewer**: NeurIPS, CVPR, ECCV, AAAI, BMVC, IEEE TIP, and workshops.
- **Organizer**, Taller Peruano para Promover la Investigación en Inteligencia Artificial, Phaw AI, Peru (2024.07).
- **Organizer**, 1er Encuentro de Egresados de Ciencias de la Computación, SECC, Trujillo, Peru (2019.10).
