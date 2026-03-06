<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Aura | Material 3 Wallpapers</title>
  
  <!-- Material Symbols for M3 Icons -->
  <link href="https://fonts.googleapis.com/css2?family=Material+Symbols+Rounded:opsz,wght,FILL,GRAD@20..48,100..700,0..1,-50..200" rel="stylesheet" />
  <!-- Roboto Font for Material Typography -->
  <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;500;700&display=swap" rel="stylesheet">

  <style>
    :root {
      /* Material 3 Light Theme Color Tokens */
      --md-sys-color-background: #FDFBFF;
      --md-sys-color-on-background: #1A1B1E;
      --md-sys-color-surface: #FDFBFF;
      --md-sys-color-surface-container: #F0F0F4;
      --md-sys-color-surface-container-high: #EBEBEF;
      --md-sys-color-primary: #415F91;
      --md-sys-color-on-primary: #FFFFFF;
      --md-sys-color-primary-container: #D6E3FF;
      --md-sys-color-on-primary-container: #001B3E;
      --md-sys-color-secondary-container: #DCE2F9;
      --md-sys-color-on-secondary-container: #131C2B;
      --md-sys-color-outline: #74777F;
      
      /* Typography */
      --md-sys-typescale-body: 'Roboto', sans-serif;
    }

    /* Basic Dark Theme Support */
    @media (prefers-color-scheme: dark) {
      :root {
        --md-sys-color-background: #1A1B1E;
        --md-sys-color-on-background: #E3E2E6;
        --md-sys-color-surface: #1A1B1E;
        --md-sys-color-surface-container: #2A2B2F;
        --md-sys-color-surface-container-high: #323337;
        --md-sys-color-primary: #AAC7FF;
        --md-sys-color-on-primary: #0A305F;
        --md-sys-color-primary-container: #284777;
        --md-sys-color-on-primary-container: #D6E3FF;
        --md-sys-color-secondary-container: #3C4758;
        --md-sys-color-on-secondary-container: #DCE2F9;
        --md-sys-color-outline: #8E9099;
      }
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: var(--md-sys-typescale-body);
    }

    body {
      background-color: var(--md-sys-color-background);
      color: var(--md-sys-color-on-background);
      transition: background-color 0.3s, color 0.3s;
    }

    /* Top App Bar */
    header {
      position: sticky;
      top: 0;
      z-index: 100;
      background-color: var(--md-sys-color-background);
      padding: 16px 24px;
      display: flex;
      flex-direction: column;
      gap: 16px;
      border-bottom: 1px solid transparent;
    }

    .header-top {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .header-top h1 {
      font-size: 24px;
      font-weight: 500;
    }

    /* M3 Pill Search Bar */
    .search-bar {
      display: flex;
      align-items: center;
      background-color: var(--md-sys-color-surface-container-high);
      border-radius: 28px; /* M3 full rounding */
      padding: 0 16px;
      height: 56px;
      gap: 12px;
    }

    .search-bar input {
      background: none;
      border: none;
      outline: none;
      color: var(--md-sys-color-on-background);
      font-size: 16px;
      flex-grow: 1;
    }

    .search-bar input::placeholder {
      color: var(--md-sys-color-outline);
    }

    .search-bar .material-symbols-rounded {
      color: var(--md-sys-color-on-background);
    }

    /* M3 Filter Chips */
    .filter-chips {
      display: flex;
      gap: 8px;
      overflow-x: auto;
      padding-bottom: 8px;
      scrollbar-width: none;
    }
    
    .filter-chips::-webkit-scrollbar {
      display: none;
    }

    .chip {
      background-color: transparent;
      border: 1px solid var(--md-sys-color-outline);
      color: var(--md-sys-color-on-background);
      border-radius: 8px;
      padding: 0 16px;
      height: 32px;
      display: flex;
      align-items: center;
      font-size: 14px;
      font-weight: 500;
      cursor: pointer;
      white-space: nowrap;
      transition: 0.2s ease;
    }

    .chip.active {
      background-color: var(--md-sys-color-secondary-container);
      color: var(--md-sys-color-on-secondary-container);
      border-color: transparent;
    }

    /* Wallpaper Grid (Masonry effect using CSS Grid) */
    .gallery {
      padding: 24px;
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
      gap: 24px;
    }

    /* M3 Elevated Card */
    .card {
      background-color: var(--md-sys-color-surface-container);
      border-radius: 24px; /* M3 large border radius */
      overflow: hidden;
      display: flex;
      flex-direction: column;
      transition: transform 0.2s ease, box-shadow 0.2s ease;
      cursor: pointer;
      position: relative;
    }

    .card:hover {
      transform: translateY(-4px);
      box-shadow: 0 8px 24px rgba(0,0,0,0.1);
    }

    .card img {
      width: 100%;
      height: 300px;
      object-fit: cover;
    }

    /* Alternate aspect ratios for unique design */
    .card:nth-child(even) img {
      height: 400px;
    }

    .card-content {
      padding: 16px;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .card-title {
      font-size: 16px;
      font-weight: 500;
    }

    .card-author {
      font-size: 14px;
      color: var(--md-sys-color-outline);
      margin-top: 4px;
    }

    /* M3 Icon Buttons */
    .icon-btn {
      background: none;
      border: none;
      cursor: pointer;
      color: var(--md-sys-color-on-background);
      display: flex;
      align-items: center;
      justify-content: center;
      width: 40px;
      height: 40px;
      border-radius: 50%;
      transition: background-color 0.2s ease;
    }

    .icon-btn:hover {
      background-color: var(--md-sys-color-surface-container-high);
    }

    /* M3 Floating Action Button (FAB) */
    .fab {
      position: fixed;
      bottom: 24px;
      right: 24px;
      background-color: var(--md-sys-color-primary-container);
      color: var(--md-sys-color-on-primary-container);
      border: none;
      border-radius: 16px; /* M3 squircle */
      width: 56px;
      height: 56px;
      display: flex;
      align-items: center;
      justify-content: center;
      box-shadow: 0 4px 12px rgba(0,0,0,0.15);
      cursor: pointer;
      transition: background-color 0.2s ease, box-shadow 0.2s ease;
      z-index: 1000;
    }

    .fab:hover {
      box-shadow: 0 6px 16px rgba(0,0,0,0.2);
      filter: brightness(0.95);
    }

  </style>
</head>
<body>

  <!-- App Header -->
  <header>
    <div class="header-top">
      <h1>Aura Wallpapers</h1>
      <button class="icon-btn">
        <span class="material-symbols-rounded">account_circle</span>
      </button>
    </div>

    <!-- Search Bar -->
    <div class="search-bar">
      <span class="material-symbols-rounded">search</span>
      <input type="text" placeholder="Search wallpapers, colors, or categories...">
      <button class="icon-btn">
        <span class="material-symbols-rounded">mic</span>
      </button>
    </div>

    <!-- Filter Chips -->
    <div class="filter-chips">
      <div class="chip active" onclick="selectChip(this)">All</div>
      <div class="chip" onclick="selectChip(this)">Nature</div>
      <div class="chip" onclick="selectChip(this)">Abstract</div>
      <div class="chip" onclick="selectChip(this)">Minimalist</div>
      <div class="chip" onclick="selectChip(this)">Space</div>
      <div class="chip" onclick="selectChip(this)">Architecture</div>
      <div class="chip" onclick="selectChip(this)">Amoled</div>
      <div class="chip" onclick="selectChip(this)">3D Renders</div>
    </div>
  </header>

  <!-- Wallpaper Gallery -->
  <main class="gallery" id="gallery">
    <!-- Cards are dynamically injected via JS -->
  </main>

  <!-- Floating Action Button -->
  <button class="fab" title="Upload Wallpaper">
    <span class="material-symbols-rounded">add</span>
  </button>

  <script>
    // Logic for Filter Chips
    function selectChip(element) {
      document.querySelectorAll('.chip').forEach(chip => {
        chip.classList.remove('active');
      });
      element.classList.add('active');
    }

    // Dummy Data for Wallpapers
    const wallpapers =[
      { title: 'Neon Mountains', author: 'John Doe', img: 'https://images.unsplash.com/photo-1618005182384-a83a8bd57fbe?q=80&w=800&auto=format&fit=crop' },
      { title: 'Abstract Waves', author: 'Jane Smith', img: 'https://images.unsplash.com/photo-1550684848-fac1c5b4e853?q=80&w=800&auto=format&fit=crop' },
      { title: 'Forest Fog', author: 'Nature Lover', img: 'https://images.unsplash.com/photo-1448375240586-882707db888b?q=80&w=800&auto=format&fit=crop' },
      { title: 'Geometric Shapes', author: 'Art 3D', img: 'https://images.unsplash.com/photo-1558591710-4b4a1ae0f04d?q=80&w=800&auto=format&fit=crop' },
      { title: 'City Nights', author: 'Urbanist', img: 'https://images.unsplash.com/photo-1519501025264-65ba15a82390?q=80&w=800&auto=format&fit=crop' },
      { title: 'Desert Dunes', author: 'Explorer', img: 'https://images.unsplash.com/photo-1509316785289-025f5b846b35?q=80&w=800&auto=format&fit=crop' },
      { title: 'Ocean Blue', author: 'Marina', img: 'https://images.unsplash.com/photo-1507525428034-b723cf961d3e?q=80&w=800&auto=format&fit=crop' },
      { title: 'Cyberpunk Alley', author: 'Future 2077', img: 'https://images.unsplash.com/photo-1601134467661-3d775b999c8b?q=80&w=800&auto=format&fit=crop' }
    ];

    // Render Gallery
    const galleryContainer = document.getElementById('gallery');
    
    wallpapers.forEach(item => {
      const card = document.createElement('article');
      card.className = 'card';
      
      card.innerHTML = `
        <img src="${item.img}" alt="${item.title}" loading="lazy">
        <div class="card-content">
          <div>
            <div class="card-title">${item.title}</div>
            <div class="card-author">${item.author}</div>
          </div>
          <button class="icon-btn" title="Download">
            <span class="material-symbols-rounded">download</span>
          </button>
        </div>
      `;
      
      galleryContainer.appendChild(card);
    });
  </script>

</body>
</html>
