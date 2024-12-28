---
layout: page
permalink: /teaching/cmpt464-project/
title: CMPT464/764 Project Results
description: Top 4 Project Results Showcase
nav: false
---

<style>
    .results-container {
        margin-top: 2rem;
    }

    .group-section {
        margin-bottom: 3rem;
        padding: 1.5rem;
        border: 1px solid var(--global-divider-color);
        border-radius: 8px;
        background-color: var(--global-bg-color);
        box-shadow: 0 2px 4px rgba(0,0,0,0.05);
    }

    .group-section.gt {
        border: 2px solid #28a745;
    }

    .group-title {
        color: var(--global-theme-color);
        font-size: 1.5rem;
        margin-bottom: 1.5rem;
        padding-bottom: 0.5rem;
        border-bottom: 2px solid var(--global-divider-color);
    }

    .group-title.gt {
        color: #28a745;
        border-bottom: 2px solid #28a745;
    }

    .videos-grid {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        gap: 1rem;
        margin-top: 1rem;
    }

    .video-container {
        width: 100%;
        min-height: 200px;
    }

    .video-title {
        font-weight: 600;
        margin-bottom: 0.5rem;
        text-align: center;
    }

    .video-placeholder {
        width: 100%;
        height: 200px;
        background: #f0f0f0;
        border-radius: 4px;
        display: flex;
        align-items: center;
        justify-content: center;
        margin-bottom: 1rem;
    }

    .loading-text {
        color: #666;
        font-size: 0.9rem;
    }

    video {
        width: 100%;
        border-radius: 4px;
        box-shadow: 0 2px 4px rgba(0,0,0,0.1);
        max-height: 200px;
        object-fit: cover;
        opacity: 0;
        transition: opacity 0.3s;
    }

    video.loaded {
        opacity: 1;
    }

    .note {
        margin-top: 2rem;
        padding: 1rem;
        background-color: var(--global-bg-color);
        border: 1px solid var(--global-divider-color);
        border-radius: 8px;
        font-size: 0.9rem;
        color: var(--global-text-color-light);
    }

    @media (max-width: 768px) {
        .videos-grid {
            grid-template-columns: 1fr;
            max-width: 400px;
            margin: 1rem auto;
        }
        
        video {
            max-height: 300px;
        }
    }
</style>

<div class="header-info">
    <p><strong>Course:</strong> CMPT464/764 Geometric Modelling</p>
    <p><strong>Date:</strong> December 11, 2024</p>
    <p>Showcasing the top 4 performing groups' results regarding Chamfer Distance, 3D IoU, design originality and human perception, compared with ground truth models.</p>
</div>

<div class="results-container">
    <!-- Ground Truth -->
    <div class="group-section gt">
        <h2 class="group-title gt">Ground Truth Models</h2>
        <div class="videos-grid">
            <div class="video-container">
                <div class="video-title">Fertility Model (GT)</div>
                <div class="video-placeholder">
                    <span class="loading-text">Loading video...</span>
                </div>
                <video loading="lazy" preload="none" autoplay loop muted playsinline
                    onloadeddata="this.classList.add('loaded'); this.previousElementSibling.style.display='none';">
                    <source src="{{ '/assets/videos/gt/fertility.mp4' | relative_url }}" type="video/mp4">
                </video>
            </div>
            <div class="video-container">
                <div class="video-title">Suzanne Model (GT)</div>
                <div class="video-placeholder">
                    <span class="loading-text">Loading video...</span>
                </div>
                <video loading="lazy" preload="none" autoplay loop muted playsinline
                    onloadeddata="this.classList.add('loaded'); this.previousElementSibling.style.display='none';">
                    <source src="{{ '/assets/videos/gt/suzanne.mp4' | relative_url }}" type="video/mp4">
                </video>
            </div>
            <div class="video-container">
                <div class="video-title">Torus Model (GT)</div>
                <div class="video-placeholder">
                    <span class="loading-text">Loading video...</span>
                </div>
                <video loading="lazy" preload="none" autoplay loop muted playsinline
                    onloadeddata="this.classList.add('loaded'); this.previousElementSibling.style.display='none';">
                    <source src="{{ '/assets/videos/gt/torus_tri.mp4' | relative_url }}" type="video/mp4">
                </video>
            </div>
        </div>
    </div>

    <!-- First Place -->
    <div class="group-section">
        <h2 class="group-title">First Place Results</h2>
        <div class="videos-grid">
            <div class="video-container">
                <div class="video-title">Fertility Model</div>
                <div class="video-placeholder">
                    <span class="loading-text">Loading video...</span>
                </div>
                <video loading="lazy" preload="none" autoplay loop muted playsinline
                    onloadeddata="this.classList.add('loaded'); this.previousElementSibling.style.display='none';">
                    <source src="{{ '/assets/videos/1st/fertility.mp4' | relative_url }}" type="video/mp4">
                </video>
            </div>
            <div class="video-container">
                <div class="video-title">Suzanne Model</div>
                <div class="video-placeholder">
                    <span class="loading-text">Loading video...</span>
                </div>
                <video loading="lazy" preload="none" autoplay loop muted playsinline
                    onloadeddata="this.classList.add('loaded'); this.previousElementSibling.style.display='none';">
                    <source src="{{ '/assets/videos/1st/suzanne.mp4' | relative_url }}" type="video/mp4">
                </video>
            </div>
            <div class="video-container">
                <div class="video-title">Torus Model</div>
                <div class="video-placeholder">
                    <span class="loading-text">Loading video...</span>
                </div>
                <video loading="lazy" preload="none" autoplay loop muted playsinline
                    onloadeddata="this.classList.add('loaded'); this.previousElementSibling.style.display='none';">
                    <source src="{{ '/assets/videos/1st/torus_tri.mp4' | relative_url }}" type="video/mp4">
                </video>
            </div>
        </div>
    </div>

    <!-- Second Place -->
    <div class="group-section">
        <h2 class="group-title">Second Place Results</h2>
        <div class="videos-grid">
            <div class="video-container">
                <div class="video-title">Fertility Model</div>
                <div class="video-placeholder">
                    <span class="loading-text">Loading video...</span>
                </div>
                <video loading="lazy" preload="none" autoplay loop muted playsinline
                    onloadeddata="this.classList.add('loaded'); this.previousElementSibling.style.display='none';">
                    <source src="{{ '/assets/videos/2nd/fertility.mp4' | relative_url }}" type="video/mp4">
                </video>
            </div>
            <div class="video-container">
                <div class="video-title">Suzanne Model</div>
                <div class="video-placeholder">
                    <span class="loading-text">Loading video...</span>
                </div>
                <video loading="lazy" preload="none" autoplay loop muted playsinline
                    onloadeddata="this.classList.add('loaded'); this.previousElementSibling.style.display='none';">
                    <source src="{{ '/assets/videos/2nd/suzanne.mp4' | relative_url }}" type="video/mp4">
                </video>
            </div>
            <div class="video-container">
                <div class="video-title">Torus Model</div>
                <div class="video-placeholder">
                    <span class="loading-text">Loading video...</span>
                </div>
                <video loading="lazy" preload="none" autoplay loop muted playsinline
                    onloadeddata="this.classList.add('loaded'); this.previousElementSibling.style.display='none';">
                    <source src="{{ '/assets/videos/2nd/torus_tri.mp4' | relative_url }}" type="video/mp4">
                </video>
            </div>
        </div>
    </div>

    <!-- Third Place -->
    <div class="group-section">
        <h2 class="group-title">Third Place Results</h2>
        <div class="videos-grid">
            <div class="video-container">
                <div class="video-title">Fertility Model</div>
                <div class="video-placeholder">
                    <span class="loading-text">Loading video...</span>
                </div>
                <video loading="lazy" preload="none" autoplay loop muted playsinline
                    onloadeddata="this.classList.add('loaded'); this.previousElementSibling.style.display='none';">
                    <source src="{{ '/assets/videos/3rd/fertility.mp4' | relative_url }}" type="video/mp4">
                </video>
            </div>
            <div class="video-container">
                <div class="video-title">Suzanne Model</div>
                <div class="video-placeholder">
                    <span class="loading-text">Loading video...</span>
                </div>
                <video loading="lazy" preload="none" autoplay loop muted playsinline
                    onloadeddata="this.classList.add('loaded'); this.previousElementSibling.style.display='none';">
                    <source src="{{ '/assets/videos/3rd/suzanne.mp4' | relative_url }}" type="video/mp4">
                </video>
            </div>
            <div class="video-container">
                <div class="video-title">Torus Model</div>
                <div class="video-placeholder">
                    <span class="loading-text">Loading video...</span>
                </div>
                <video loading="lazy" preload="none" autoplay loop muted playsinline
                    onloadeddata="this.classList.add('loaded'); this.previousElementSibling.style.display='none';">
                    <source src="{{ '/assets/videos/3rd/torus_tri.mp4' | relative_url }}" type="video/mp4">
                </video>
            </div>
        </div>
    </div>

    <!-- Fourth Place -->
    <div class="group-section">
        <h2 class="group-title">Fourth Place Results</h2>
        <div class="videos-grid">
            <div class="video-container">
                <div class="video-title">Fertility Model</div>
                <div class="video-placeholder">
                    <span class="loading-text">Loading video...</span>
                </div>
                <video loading="lazy" preload="none" autoplay loop muted playsinline
                    onloadeddata="this.classList.add('loaded'); this.previousElementSibling.style.display='none';">
                    <source src="{{ '/assets/videos/4th/fertility.mp4' | relative_url }}" type="video/mp4">
                </video>
            </div>
            <div class="video-container">
                <div class="video-title">Suzanne Model</div>
                <div class="video-placeholder">
                    <span class="loading-text">Loading video...</span>
                </div>
                <video loading="lazy" preload="none" autoplay loop muted playsinline
                    onloadeddata="this.classList.add('loaded'); this.previousElementSibling.style.display='none';">
                    <source src="{{ '/assets/videos/4th/suzanne.mp4' | relative_url }}" type="video/mp4">
                </video>
            </div>
            <div class="video-container">
                <div class="video-title">Torus Model</div>
                <div class="video-placeholder">
                    <span class="loading-text">Loading video...</span>
                </div>
                <video loading="lazy" preload="none" autoplay loop muted playsinline
                    onloadeddata="this.classList.add('loaded'); this.previousElementSibling.style.display='none';">
                    <source src="{{ '/assets/videos/4th/torus_tri.mp4' | relative_url }}" type="video/mp4">
                </video>
            </div>
        </div>
    </div>
</div>

<div class="note">
    <p>Note: All results are presented anonymously to maintain fairness. The videos showcase the performance of each group's implementation on three standard test models: Fertility, Suzanne, and Torus. Ground truth models are provided at the top for comparison.</p>
</div>

<script>
document.addEventListener('DOMContentLoaded', function() {
    const options = {
        root: null,
        rootMargin: '50px',
        threshold: 0.1
    };

    const observer = new IntersectionObserver((entries, observer) => {
        entries.forEach(entry => {
            if (entry.isIntersecting) {
                const video = entry.target;
                video.load();
                observer.unobserve(video);
            }
        });
    }, options);

    document.querySelectorAll('video').forEach(video => {
        observer.observe(video);
    });
});
</script>