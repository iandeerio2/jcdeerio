# jcdeerio
ian portfolio

<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Juess Christian De Erio | Lighting Director, Designer, Resolume Operator &amp; Audio Tech</title>
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap" rel="stylesheet" />
  <script src="https://cdn.tailwindcss.com"></script>
  <script>
    tailwind.config = {
      darkMode: 'class',
      theme: {
        extend: {
          fontFamily: {
            sans: ['Inter', 'system-ui', '-apple-system', 'sans-serif'],
          },
          colors: {
            obsidian: '#07090F',
            stage: '#0D121D',
            console: '#131A2A',
            amberStage: '#F59E0B',
            cyanBeam: '#38BDF8',
            royalStage: '#2563EB',
          },
          boxShadow: {
            amberGlow: '0 0 28px -4px rgba(245, 158, 11, 0.35)',
            cyanGlow: '0 0 28px -4px rgba(56, 189, 248, 0.28)',
          },
        },
      },
    };
  </script>
  <style>
    body {
      font-family: 'Inter', system-ui, -apple-system, sans-serif;
      background-color: #07090F;
      color: #F8FAFC;
      overflow-x: hidden;
    }

    /* Subtle stage lighting beams and grid texture */
    .stage-bg {
      background-image:
        radial-gradient(ellipse 75% 45% at 15% 0%, rgba(245, 158, 11, 0.14), transparent 65%),
        radial-gradient(ellipse 70% 45% at 85% 5%, rgba(56, 189, 248, 0.14), transparent 65%),
        radial-gradient(ellipse 60% 40% at 50% 35%, rgba(37, 99, 235, 0.08), transparent 70%);
    }

    .truss-pattern {
      background-image: linear-gradient(to right, rgba(148, 163, 184, 0.05) 1px, transparent 1px),
                        linear-gradient(to bottom, rgba(148, 163, 184, 0.05) 1px, transparent 1px);
      background-size: 32px 32px;
    }

    @media print {
      .no-print {
        display: none !important;
      }
      body {
        background: #ffffff !important;
        color: #0f172a !important;
      }
      .print-card {
        background: #ffffff !important;
        color: #0f172a !important;
        border-color: #cbd5e1 !important;
        box-shadow: none !important;
      }
    }
  </style>
</head>
<body class="stage-bg truss-pattern min-h-screen antialiased selection:bg-amber-500/30 selection:text-amber-200">

  <!-- Toast Notification Banner (replaces browser alert) -->
  <div id="toastBanner" role="status" aria-live="polite"
    class="no-print fixed bottom-5 right-5 z-50 hidden max-w-sm rounded-xl border border-amber-400/40 bg-slate-900/95 px-4 py-3 text-sm font-medium text-white shadow-2xl backdrop-blur-md transition-all">
    <div class="flex items-center gap-2.5">
      <span class="inline-block h-2.5 w-2.5 rounded-full bg-amber-400"></span>
      <span id="toastMessage">Action completed.</span>
    </div>
  </div>

  <!-- Top Navigation Bar -->
  <header class="no-print sticky top-0 z-40 border-b border-slate-800/80 bg-slate-950/85 backdrop-blur-md">
    <div class="mx-auto flex max-w-7xl flex-wrap items-center justify-between gap-3 px-4 py-3 sm:px-6 lg:px-8">
      <a href="#top" class="flex items-center gap-2.5 rounded-lg p-1 text-left focus:outline-none focus:ring-2 focus:ring-amber-400">
        <span class="flex h-9 w-9 items-center justify-center rounded-lg bg-gradient-to-br from-amber-400 to-amber-600 text-sm font-extrabold text-slate-950 shadow-amberGlow">
          JC
        </span>
        <div>
          <div class="text-sm font-bold tracking-wide text-white">JUESS CHRISTIAN DE ERIO</div>
          <div class="text-[11px] font-medium text-sky-400">Davao City • Live Stage &amp; FOH</div>
        </div>
      </a>

      <nav aria-label="Primary Navigation" class="hidden items-center gap-1 md:flex">
        <a href="#profile" class="rounded-lg px-3 py-2 text-sm font-medium text-slate-300 transition hover:bg-slate-800/70 hover:text-amber-300">Profile</a>
        <a href="#rig" class="rounded-lg px-3 py-2 text-sm font-medium text-slate-300 transition hover:bg-slate-800/70 hover:text-amber-300">Technical Rig</a>
        <a href="#portfolio" class="rounded-lg px-3 py-2 text-sm font-medium text-slate-300 transition hover:bg-slate-800/70 hover:text-amber-300">Portfolio</a>
        <a href="#experience" class="rounded-lg px-3 py-2 text-sm font-medium text-slate-300 transition hover:bg-slate-800/70 hover:text-amber-300">Experience</a>
        <a href="#contact" class="rounded-lg px-3 py-2 text-sm font-medium text-slate-300 transition hover:bg-slate-800/70 hover:text-amber-300">Booking</a>
      </nav>

      <div class="flex items-center gap-2">
        <button type="button" onclick="window.print()"
          class="inline-flex items-center gap-2 rounded-xl border border-sky-400/40 bg-sky-500/15 px-3.5 py-2 text-xs font-semibold text-sky-200 transition hover:bg-sky-500/25 focus:outline-none focus:ring-2 focus:ring-sky-400 sm:text-sm">
          <svg class="h-4 w-4" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" d="M6 9V2h12v7M6 18H4a2 2 0 01-2-2v-5a2 2 0 012-2h16a2 2 0 012 2v5a2 2 0 01-2 2h-2M6 14h12v8H6v-8z" />
          </svg>
          <span>Print / Save as PDF</span>
        </button>
      </div>
    </div>
  </header>

  <main id="top" class="mx-auto max-w-7xl px-4 py-8 sm:px-6 lg:px-8 lg:py-12">

    <!-- 1. HERO & PROFILE SECTION -->
    <section id="profile" class="mb-14">
      <div class="print-card relative overflow-hidden rounded-2xl border border-slate-800/90 bg-slate-900/80 p-6 shadow-2xl backdrop-blur-sm sm:p-8 lg:p-10">
        <!-- Decorative top stage bar -->
        <div class="pointer-events-none absolute inset-x-0 top-0 h-1 bg-gradient-to-r from-amber-500 via-sky-400 to-blue-600"></div>

        <div class="grid grid-cols-1 items-start gap-8 lg:grid-cols-12">
          <!-- Portrait Column -->
          <div class="flex flex-col items-center lg:col-span-4">
            <div class="relative w-full max-w-xs overflow-hidden rounded-2xl border border-amber-400/30 bg-slate-950 shadow-amberGlow">
              <img id="portraitImg"
                src="https://placehold.co/600x760/0B101B/F59E0B?text=JUESS+CHRISTIAN%0ADE+ERIO%0AFOH+PORTRAIT"
                onerror="this.onerror=null;this.src='https://placehold.co/600x760/0B101B/38BDF8?text=Portrait+Preview';"
                alt="Portrait of Juess Christian De Erio"
                class="aspect-[4/5] w-full object-cover object-top" />
              <div class="absolute inset-x-0 bottom-0 bg-gradient-to-t from-slate-950 via-slate-950/75 to-transparent p-3.5">
                <div class="flex items-center justify-between text-xs">
                  <span class="font-semibold text-amber-400">FOH &amp; Stage Ops</span>
                  <span id="portraitStatusBadge" class="rounded-md bg-sky-500/20 px-2 py-0.5 text-[11px] font-medium text-sky-300">Default Frame</span>
                </div>
              </div>
            </div>

            <!-- Portrait Uploader & Frame Toggle -->
            <div class="no-print mt-4 flex w-full max-w-xs flex-col gap-2">
              <label for="portraitFileInput"
                class="flex cursor-pointer items-center justify-center gap-2 rounded-xl bg-gradient-to-r from-amber-500 to-amber-400 px-4 py-2.5 text-xs font-bold text-slate-950 shadow-lg transition hover:brightness-110 sm:text-sm">
                <svg class="h-4 w-4" fill="none" stroke="currentColor" stroke-width="2.2" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" d="M4 16v1a3 3 0 003 3h10a3 3 0 003-3v-1m-4-8l-4-4m0 0L8 8m4-4v12" />
                </svg>
                <span>Upload Portrait Photo</span>
              </label>
              <input id="portraitFileInput" type="file" accept="image/*" class="hidden" onchange="handlePortraitUpload(event)" />

              <div class="grid grid-cols-2 gap-2">
                <button type="button" onclick="togglePortraitFrame()"
                  class="rounded-xl border border-slate-700 bg-slate-800/80 px-3 py-2 text-xs font-semibold text-slate-200 transition hover:border-sky-400/50 hover:text-sky-300">
                  Switch Frame
                </button>
                <button type="button" onclick="resetPortrait()"
                  class="rounded-xl border border-slate-700 bg-slate-800/80 px-3 py-2 text-xs font-semibold text-slate-300 transition hover:border-amber-400/50 hover:text-amber-300">
                  Reset Photo
                </button>
              </div>
            </div>
          </div>

          <!-- Profile Info Column -->
          <div class="space-y-5 lg:col-span-8">
            <div class="inline-flex flex-wrap items-center gap-2 rounded-full border border-amber-400/30 bg-amber-500/10 px-3.5 py-1 text-xs font-semibold text-amber-300">
              <span class="h-2 w-2 rounded-full bg-amber-400"></span>
              <span>Live Event &amp; Concert Production Specialist</span>
            </div>

            <div>
              <h1 class="text-3xl font-extrabold tracking-tight text-white sm:text-4xl lg:text-5xl">
                JUESS CHRISTIAN DE ERIO
              </h1>
              <p class="mt-2.5 text-sm font-bold tracking-wide text-sky-400 sm:text-base">
                Lighting Director • Lighting Designer • Resolume Operator • Audio Technician
              </p>
            </div>

            <!-- Location & Quick Contact Bar -->
            <div class="flex flex-wrap items-center gap-2.5 rounded-xl border border-slate-800 bg-slate-950/75 p-3.5 text-xs sm:text-sm">
              <span class="inline-flex items-center gap-1.5 font-medium text-slate-200">
                <svg class="h-4 w-4 text-amber-400" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" d="M17.657 16.657L13.414 20.9a2 2 0 01-2.828 0l-4.243-4.243a8 8 0 1111.314 0z" />
                  <path stroke-linecap="round" stroke-linejoin="round" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z" />
                </svg>
                Davao City, Philippines
              </span>
              <span class="text-slate-600">|</span>

              <button type="button" onclick="copyContact('09240318162', 'Phone number')"
                class="inline-flex items-center gap-1.5 rounded-lg bg-slate-800/90 px-2.5 py-1 font-semibold text-amber-300 transition hover:bg-slate-700">
                <span>09240318162</span>
                <span class="text-[11px] text-slate-400">[Copy]</span>
              </button>

              <span class="text-slate-600">|</span>

              <button type="button" onclick="copyContact('iandeerio2@gmail.com', 'Email address')"
                class="inline-flex items-center gap-1.5 rounded-lg bg-slate-800/90 px-2.5 py-1 font-semibold text-sky-300 transition hover:bg-slate-700">
                <span>iandeerio2@gmail.com</span>
                <span class="text-[11px] text-slate-400">[Copy]</span>
              </button>
            </div>

            <!-- Professional Profile Summary -->
            <div class="space-y-2">
              <h2 class="text-xs font-bold uppercase tracking-widest text-amber-400">Professional Profile</h2>
              <p class="text-sm leading-relaxed text-slate-300 sm:text-base">
                Creative and detail-oriented Lighting Director, Lighting Designer, Resolume Operator, and Audio Technician with experience in live event production, stage lighting, visual presentation, and live audio operations. Skilled in designing and executing lighting concepts, operating professional lighting consoles, managing LED wall visuals, and mixing live audio for full-band performances. Collaborative with production teams, event organizers, performers, and technical directors to deliver smooth, high-quality productions.
              </p>
            </div>

            <!-- Key Highlights Pills -->
            <div class="grid grid-cols-1 gap-3 pt-1 sm:grid-cols-3">
              <div class="rounded-xl border border-slate-800/90 bg-slate-950/60 p-3.5">
                <div class="text-xs font-semibold uppercase tracking-wider text-amber-400">Lighting Consoles</div>
                <div class="mt-1 text-sm font-bold text-white">grandMA2 • grandMA3 • Avolites</div>
              </div>
              <div class="rounded-xl border border-slate-800/90 bg-slate-950/60 p-3.5">
                <div class="text-xs font-semibold uppercase tracking-wider text-sky-400">Visual &amp; LED Control</div>
                <div class="mt-1 text-sm font-bold text-white">Resolume Arena • Multi-Screen Cues</div>
              </div>
              <div class="rounded-xl border border-slate-800/90 bg-slate-950/60 p-3.5">
                <div class="text-xs font-semibold uppercase tracking-wider text-blue-400">Live Audio Mixing</div>
                <div class="mt-1 text-sm font-bold text-white">Midas M32 • Yamaha TF5 / DM3</div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- 2. TECHNICAL RIG & SYSTEMS MATRIX -->
    <section id="rig" class="mb-14">
      <div class="mb-6 flex flex-col justify-between gap-4 sm:flex-row sm:items-end">
        <div>
          <p class="text-xs font-bold uppercase tracking-widest text-amber-400">Systems &amp; Capabilities</p>
          <h2 class="mt-1 text-2xl font-extrabold tracking-tight text-white sm:text-3xl">Technical Rig &amp; Systems Matrix</h2>
        </div>

        <!-- Discipline Filter Tabs -->
        <div id="rigTabs" role="tablist" aria-label="Filter Technical Rig by Discipline"
          class="no-print flex flex-wrap gap-1.5 rounded-xl border border-slate-800 bg-slate-900/90 p-1.5">
          <button type="button" data-rig-filter="all" onclick="setRigFilter('all')"
            class="rig-tab active rounded-lg bg-amber-500 px-3 py-1.5 text-xs font-bold text-slate-950 transition">
            All Disciplines
          </button>
          <button type="button" data-rig-filter="lighting" onclick="setRigFilter('lighting')"
            class="rig-tab rounded-lg px-3 py-1.5 text-xs font-semibold text-slate-300 transition hover:bg-slate-800 hover:text-white">
            Lighting Control
          </button>
          <button type="button" data-rig-filter="audio" onclick="setRigFilter('audio')"
            class="rig-tab rounded-lg px-3 py-1.5 text-xs font-semibold text-slate-300 transition hover:bg-slate-800 hover:text-white">
            Audio Mixing &amp; Systems
          </button>
          <button type="button" data-rig-filter="visual" onclick="setRigFilter('visual')"
            class="rig-tab rounded-lg px-3 py-1.5 text-xs font-semibold text-slate-300 transition hover:bg-slate-800 hover:text-white">
            Visual Production
          </button>
          <button type="button" data-rig-filter="production" onclick="setRigFilter('production')"
            class="rig-tab rounded-lg px-3 py-1.5 text-xs font-semibold text-slate-300 transition hover:bg-slate-800 hover:text-white">
            Event Production
          </button>
        </div>
      </div>

      <div id="rigGrid" class="grid grid-cols-1 gap-5 md:grid-cols-2">
        <!-- Lighting Control -->
        <article data-discipline="lighting" class="print-card rounded-2xl border border-amber-500/30 bg-slate-900/80 p-6 transition hover:border-amber-400/60">
          <div class="flex items-center justify-between">
            <h3 class="text-lg font-bold text-white">Lighting Control</h3>
            <span class="rounded-full bg-amber-500/15 px-2.5 py-1 text-xs font-semibold text-amber-300">Stage &amp; FX</span>
          </div>
          <div class="mt-4 flex flex-wrap gap-2">
            <span class="rounded-lg border border-amber-400/30 bg-amber-500/10 px-2.5 py-1 text-xs font-semibold text-amber-200">MA Lighting grandMA2</span>
            <span class="rounded-lg border border-amber-400/30 bg-amber-500/10 px-2.5 py-1 text-xs font-semibold text-amber-200">MA Lighting grandMA3</span>
            <span class="rounded-lg border border-amber-400/30 bg-amber-500/10 px-2.5 py-1 text-xs font-semibold text-amber-200">Avolites Lighting Consoles</span>
          </div>
          <ul class="mt-4 space-y-1.5 text-sm text-slate-300">
            <li>• Lighting design &amp; concept execution for live stages and concerts</li>
            <li>• Console programming &amp; cue stack management</li>
            <li>• Live busking &amp; real-time music synchronization</li>
            <li>• Stage atmosphere &amp; mood creation</li>
          </ul>
        </article>

        <!-- Audio Mixing & Systems -->
        <article data-discipline="audio" class="print-card rounded-2xl border border-sky-500/30 bg-slate-900/80 p-6 transition hover:border-sky-400/60">
          <div class="flex items-center justify-between">
            <h3 class="text-lg font-bold text-white">Audio Mixing &amp; Systems</h3>
            <span class="rounded-full bg-sky-500/15 px-2.5 py-1 text-xs font-semibold text-sky-300">FOH &amp; Monitors</span>
          </div>
          <div class="mt-4 flex flex-wrap gap-2">
            <span class="rounded-lg border border-sky-400/30 bg-sky-500/10 px-2.5 py-1 text-xs font-semibold text-sky-200">Midas M32</span>
            <span class="rounded-lg border border-sky-400/30 bg-sky-500/10 px-2.5 py-1 text-xs font-semibold text-sky-200">Yamaha TF5</span>
            <span class="rounded-lg border border-sky-400/30 bg-sky-500/10 px-2.5 py-1 text-xs font-semibold text-sky-200">Yamaha DM3</span>
            <span class="rounded-lg border border-sky-400/30 bg-sky-500/10 px-2.5 py-1 text-xs font-semibold text-sky-200">Mackie Mixing Systems</span>
            <span class="rounded-lg border border-sky-400/30 bg-sky-500/10 px-2.5 py-1 text-xs font-semibold text-sky-200">PreSonus Mixing Systems</span>
          </div>
          <ul class="mt-4 space-y-1.5 text-sm text-slate-300">
            <li>• Live audio mixing for concerts, events &amp; programs</li>
            <li>• Full-band setup &amp; stage system configuration</li>
            <li>• Signal routing &amp; sound reinforcement</li>
          </ul>
        </article>

        <!-- Visual Production -->
        <article data-discipline="visual" class="print-card rounded-2xl border border-blue-500/30 bg-slate-900/80 p-6 transition hover:border-blue-400/60">
          <div class="flex items-center justify-between">
            <h3 class="text-lg font-bold text-white">Visual Production</h3>
            <span class="rounded-full bg-blue-500/15 px-2.5 py-1 text-xs font-semibold text-blue-300">Media &amp; LED</span>
          </div>
          <div class="mt-4 flex flex-wrap gap-2">
            <span class="rounded-lg border border-blue-400/30 bg-blue-500/10 px-2.5 py-1 text-xs font-semibold text-blue-200">Resolume Arena</span>
            <span class="rounded-lg border border-blue-400/30 bg-blue-500/10 px-2.5 py-1 text-xs font-semibold text-blue-200">LED Wall Operations</span>
          </div>
          <ul class="mt-4 space-y-1.5 text-sm text-slate-300">
            <li>• Video playback &amp; live show control</li>
            <li>• Live visual presentation &amp; cue synchronization</li>
            <li>• Visual content preparation &amp; organization</li>
          </ul>
        </article>

        <!-- Event Production -->
        <article data-discipline="production" class="print-card rounded-2xl border border-slate-700/80 bg-slate-900/80 p-6 transition hover:border-amber-400/50">
          <div class="flex items-center justify-between">
            <h3 class="text-lg font-bold text-white">Event Production</h3>
            <span class="rounded-full bg-slate-800 px-2.5 py-1 text-xs font-semibold text-amber-300">Show Execution</span>
          </div>
          <div class="mt-4 flex flex-wrap gap-2">
            <span class="rounded-lg border border-slate-700 bg-slate-800 px-2.5 py-1 text-xs font-semibold text-slate-200">Lighting + Audio + Video Integration</span>
          </div>
          <ul class="mt-4 space-y-1.5 text-sm text-slate-300">
            <li>• Stage and concert production workflows</li>
            <li>• Technical coordination with directors &amp; crews</li>
            <li>• Reliable live show execution under pressure</li>
          </ul>
        </article>
      </div>
    </section>

    <!-- 3. PRODUCTION PORTFOLIO & SHOWCASES -->
    <section id="portfolio" class="mb-14">
      <div class="mb-6 flex flex-col justify-between gap-4 lg:flex-row lg:items-end">
        <div>
          <p class="text-xs font-bold uppercase tracking-widest text-sky-400">Selected Shows &amp; Case Studies</p>
          <h2 class="mt-1 text-2xl font-extrabold tracking-tight text-white sm:text-3xl">Production Portfolio &amp; Showcases</h2>
        </div>

        <div class="no-print flex flex-wrap items-center gap-2">
          <!-- Category Filter Buttons -->
          <div id="portfolioFilters" class="flex flex-wrap gap-1.5 rounded-xl border border-slate-800 bg-slate-900/90 p-1.5">
            <button type="button" data-pfilter="All" onclick="setPortfolioFilter('All')"
              class="pfilter-btn rounded-lg bg-sky-500 px-3 py-1.5 text-xs font-bold text-slate-950 transition">
              All
            </button>
            <button type="button" data-pfilter="Lighting" onclick="setPortfolioFilter('Lighting')"
              class="pfilter-btn rounded-lg px-3 py-1.5 text-xs font-semibold text-slate-300 transition hover:bg-slate-800 hover:text-white">
              Lighting
            </button>
            <button type="button" data-pfilter="Resolume/LED" onclick="setPortfolioFilter('Resolume/LED')"
              class="pfilter-btn rounded-lg px-3 py-1.5 text-xs font-semibold text-slate-300 transition hover:bg-slate-800 hover:text-white">
              Resolume/LED
            </button>
            <button type="button" data-pfilter="Audio" onclick="setPortfolioFilter('Audio')"
              class="pfilter-btn rounded-lg px-3 py-1.5 text-xs font-semibold text-slate-300 transition hover:bg-slate-800 hover:text-white">
              Audio
            </button>
          </div>

          <button type="button" onclick="openAddProductionModal()"
            class="inline-flex items-center gap-1.5 rounded-xl bg-gradient-to-r from-amber-500 to-amber-400 px-4 py-2.5 text-xs font-bold text-slate-950 shadow-amberGlow transition hover:brightness-110 sm:text-sm">
            <svg class="h-4 w-4" fill="none" stroke="currentColor" stroke-width="2.5" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" d="M12 4v16m8-8H4" />
            </svg>
            <span>+ Add Production</span>
          </button>
        </div>
      </div>

      <!-- Portfolio Cards Container -->
      <div id="portfolioGrid" class="grid grid-cols-1 gap-6 md:grid-cols-2 xl:grid-cols-3">
        <!-- Populated dynamically via JS -->
      </div>
    </section>

    <!-- 4. EXPERIENCE, EDUCATION & REFERENCES SECTION -->
    <section id="experience" class="mb-14">
      <div class="mb-6">
        <p class="text-xs font-bold uppercase tracking-widest text-amber-400">Credentials &amp; Track Record</p>
        <h2 class="mt-1 text-2xl font-extrabold tracking-tight text-white sm:text-3xl">Experience, Education &amp; References</h2>
      </div>

      <div class="grid grid-cols-1 gap-6 lg:grid-cols-12">
        <!-- Experience Column -->
        <div class="space-y-5 lg:col-span-7">
          <article class="print-card rounded-2xl border border-slate-800 bg-slate-900/80 p-6">
            <div class="flex flex-wrap items-center justify-between gap-2">
              <h3 class="text-lg font-bold text-white">Freelance Lighting Director / Lighting Designer / Audio Technician</h3>
              <span class="rounded-full bg-amber-500/15 px-3 py-1 text-xs font-semibold text-amber-300">Live Events &amp; Concerts</span>
            </div>
            <ul class="mt-4 space-y-2 text-sm text-slate-300">
              <li>• Design and execute lighting concepts for live events, concerts, and special productions.</li>
              <li>• Operate professional lighting systems and coordinate cues with music, performers, and stage movements.</li>
              <li>• Create lighting atmospheres based on event themes and production requirements.</li>
              <li>• Set up, configure, and operate live audio systems for full-band performances.</li>
              <li>• Mix live audio and coordinate with production teams for smooth technical execution.</li>
            </ul>
          </article>

          <article class="print-card rounded-2xl border border-slate-800 bg-slate-900/80 p-6">
            <div class="flex flex-wrap items-center justify-between gap-2">
              <h3 class="text-lg font-bold text-white">Freelance Resolume Operator</h3>
              <span class="rounded-full bg-sky-500/15 px-3 py-1 text-xs font-semibold text-sky-300">LED &amp; Visuals</span>
            </div>
            <ul class="mt-4 space-y-2 text-sm text-slate-300">
              <li>• Operate Resolume Arena for LED walls and event display screens.</li>
              <li>• Manage video playback, visual content, and live show cues.</li>
              <li>• Synchronize visual presentations with music, performances, and show sequences.</li>
              <li>• Prepare and organize visual content for live productions and special events.</li>
            </ul>
          </article>
        </div>

        <!-- Education & References Column -->
        <div class="space-y-5 lg:col-span-5">
          <!-- Education -->
          <article class="print-card rounded-2xl border border-slate-800 bg-slate-900/80 p-6">
            <h3 class="text-xs font-bold uppercase tracking-widest text-sky-400">Education</h3>
            <div class="mt-3 text-base font-bold text-white">STI College of Davao</div>
            <div class="mt-1 text-sm text-slate-300">Bachelor of Science in Information Technology</div>
            <div class="mt-2 inline-block rounded-lg bg-slate-800 px-2.5 py-1 text-xs font-semibold text-amber-300">
              Academic Year: 2012–2013
            </div>
          </article>

          <!-- References -->
          <article class="print-card rounded-2xl border border-slate-800 bg-slate-900/80 p-6">
            <h3 class="text-xs font-bold uppercase tracking-widest text-amber-400">Professional References</h3>
            <div class="mt-4 space-y-4">
              <div class="rounded-xl border border-slate-800/90 bg-slate-950/65 p-4">
                <div class="font-bold text-white">Bernie Aguilar</div>
                <div class="text-xs font-medium text-sky-300">Training Director - AIFCP | Proprietor - Airpark Audio Pro</div>
                <div class="mt-2 flex items-center justify-between">
                  <span class="text-sm font-semibold text-amber-300">09479370376</span>
                  <button type="button" onclick="copyContact('09479370376', 'Bernie Aguilar\'s contact')"
                    class="no-print rounded-md bg-slate-800 px-2.5 py-1 text-xs font-semibold text-slate-200 transition hover:bg-slate-700">
                    Copy
                  </button>
                </div>
              </div>

              <div class="rounded-xl border border-slate-800/90 bg-slate-950/65 p-4">
                <div class="font-bold text-white">Nicobel Neri</div>
                <div class="text-xs font-medium text-sky-300">Proprietor - Cobe Lights and Sounds</div>
                <div class="mt-2 flex items-center justify-between">
                  <span class="text-sm font-semibold text-amber-300">09214467280</span>
                  <button type="button" onclick="copyContact('09214467280', 'Nicobel Neri\'s contact')"
                    class="no-print rounded-md bg-slate-800 px-2.5 py-1 text-xs font-semibold text-slate-200 transition hover:bg-slate-700">
                    Copy
                  </button>
                </div>
              </div>
            </div>
          </article>
        </div>
      </div>
    </section>

    <!-- 5. DIRECT CONTACT / BOOKING INQUIRY SECTION -->
    <section id="contact" class="no-print">
      <div class="rounded-2xl border border-slate-800 bg-slate-900/85 p-6 shadow-2xl sm:p-8">
        <div class="grid grid-cols-1 gap-8 lg:grid-cols-12">
          <div class="space-y-4 lg:col-span-5">
            <p class="text-xs font-bold uppercase tracking-widest text-amber-400">Show Bookings &amp; Technical Direction</p>
            <h2 class="text-2xl font-extrabold tracking-tight text-white sm:text-3xl">Book for Your Next Production</h2>
            <p class="text-sm leading-relaxed text-slate-300">
              Available for concerts, festivals, pageants, corporate galas, and full-band productions in Davao City and nationwide. Reach out directly for lighting direction, console operation, Resolume LED visuals, or live audio support.
            </p>

            <div class="space-y-2.5 pt-2 text-sm">
              <div class="flex items-center justify-between rounded-xl border border-slate-800 bg-slate-950/75 px-4 py-3">
                <div>
                  <div class="text-xs text-slate-400">Mobile / Direct Line</div>
                  <div class="font-bold text-amber-300">09240318162</div>
                </div>
                <button type="button" onclick="copyContact('09240318162', 'Phone number')"
                  class="rounded-lg bg-slate-800 px-3 py-1.5 text-xs font-semibold text-white transition hover:bg-slate-700">
                  Copy
                </button>
              </div>

              <div class="flex items-center justify-between rounded-xl border border-slate-800 bg-slate-950/75 px-4 py-3">
                <div>
                  <div class="text-xs text-slate-400">Email</div>
                  <div class="font-bold text-sky-300">iandeerio2@gmail.com</div>
                </div>
                <button type="button" onclick="copyContact('iandeerio2@gmail.com', 'Email address')"
                  class="rounded-lg bg-slate-800 px-3 py-1.5 text-xs font-semibold text-white transition hover:bg-slate-700">
                  Copy
                </button>
              </div>
            </div>
          </div>

          <form id="bookingForm" onsubmit="handleBookingSubmit(event)" class="space-y-4 lg:col-span-7">
            <div class="grid grid-cols-1 gap-4 sm:grid-cols-2">
              <div>
                <label for="clientName" class="mb-1.5 block text-xs font-semibold uppercase tracking-wider text-slate-300">Your Name / Organization</label>
                <input id="clientName" type="text" required placeholder="e.g., Davao Live Events"
                  class="w-full rounded-xl border border-slate-700 bg-slate-950/90 px-4 py-2.5 text-sm text-white placeholder-slate-500 focus:border-amber-400 focus:outline-none" />
              </div>
              <div>
                <label for="clientContact" class="mb-1.5 block text-xs font-semibold uppercase tracking-wider text-slate-300">Email or Mobile</label>
                <input id="clientContact" type="text" required placeholder="name@example.com / 09XX..."
                  class="w-full rounded-xl border border-slate-700 bg-slate-950/90 px-4 py-2.5 text-sm text-white placeholder-slate-500 focus:border-amber-400 focus:outline-none" />
              </div>
            </div>

            <div class="grid grid-cols-1 gap-4 sm:grid-cols-2">
              <div>
                <label for="serviceRole" class="mb-1.5 block text-xs font-semibold uppercase tracking-wider text-slate-300">Required Role</label>
                <select id="serviceRole"
                  class="w-full rounded-xl border border-slate-700 bg-slate-950/90 px-4 py-2.5 text-sm text-white focus:border-sky-400 focus:outline-none">
                  <option value="Lighting Director / Designer">Lighting Director / Designer</option>
                  <option value="Resolume Operator / LED">Resolume Operator / LED</option>
                  <option value="Audio Technician (FOH / Band)">Audio Technician (FOH / Band)</option>
                  <option value="Full Lighting + Visual + Audio">Full Lighting + Visual + Audio</option>
                </select>
              </div>
              <div>
                <label for="eventDateVenue" class="mb-1.5 block text-xs font-semibold uppercase tracking-wider text-slate-300">Event Date &amp; Venue</label>
                <input id="eventDateVenue" type="text" placeholder="e.g., Dec 18, 2026 • Davao City"
                  class="w-full rounded-xl border border-slate-700 bg-slate-950/90 px-4 py-2.5 text-sm text-white placeholder-slate-500 focus:border-sky-400 focus:outline-none" />
              </div>
            </div>

            <div>
              <label for="projectNotes" class="mb-1.5 block text-xs font-semibold uppercase tracking-wider text-slate-300">Production Brief / Console &amp; Rig Details</label>
              <textarea id="projectNotes" rows="3" required placeholder="Share stage size, console needs (grandMA2/grandMA3/Avolites, Resolume Arena, Midas M32/Yamaha TF5), schedule, or show notes..."
                class="w-full rounded-xl border border-slate-700 bg-slate-950/90 px-4 py-2.5 text-sm text-white placeholder-slate-500 focus:border-amber-400 focus:outline-none"></textarea>
            </div>

            <div class="flex flex-wrap items-center justify-between gap-3 pt-1">
              <span id="inquiryStatus" class="text-xs text-slate-400">Drafts and inquiries can also be opened directly in your mail client.</span>
              <button type="submit"
                class="inline-flex items-center justify-center rounded-xl bg-gradient-to-r from-sky-400 to-blue-600 px-5 py-2.5 text-sm font-bold text-slate-950 shadow-cyanGlow transition hover:brightness-110">
                Send Booking Inquiry
              </button>
            </div>
          </form>
        </div>
      </div>
    </section>
  </main>

  <footer class="border-t border-slate-800/80 bg-slate-950/90 py-6 text-center text-xs text-slate-400">
    <div class="mx-auto max-w-7xl px-4 sm:px-6 lg:px-8">
      JUESS CHRISTIAN DE ERIO • Lighting Director, Lighting Designer, Resolume Operator &amp; Audio Technician • Davao City, Philippines
    </div>
  </footer>

  <!-- ADD PRODUCTION MODAL -->
  <div id="addProductionModal" role="dialog" aria-modal="true" aria-labelledby="modalTitle"
    class="no-print fixed inset-0 z-50 hidden items-center justify-center bg-slate-950/80 p-4 backdrop-blur-sm">
    <div class="max-h-[90vh] w-full max-w-xl overflow-y-auto rounded-2xl border border-slate-700 bg-slate-900 p-6 shadow-2xl">
      <div class="flex items-center justify-between border-b border-slate-800 pb-4">
        <h3 id="modalTitle" class="text-lg font-bold text-white">+ Add Production Showcase</h3>
        <button type="button" onclick="closeAddProductionModal()" aria-label="Close modal"
          class="rounded-lg p-1.5 text-slate-400 transition hover:bg-slate-800 hover:text-white">
          <svg class="h-5 w-5" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" />
          </svg>
        </button>
      </div>

      <form id="addProductionForm" onsubmit="handleAddProduction(event)" class="mt-4 space-y-4">
        <div>
          <label for="prodTitle" class="mb-1 block text-xs font-semibold uppercase tracking-wider text-slate-300">Event / Production Title *</label>
          <input id="prodTitle" type="text" required placeholder="e.g., Kadayawan Concert Night"
            class="w-full rounded-xl border border-slate-700 bg-slate-950 px-3.5 py-2 text-sm text-white focus:border-amber-400 focus:outline-none" />
        </div>

        <div class="grid grid-cols-1 gap-4 sm:grid-cols-2">
          <div>
            <label for="prodVenueYear" class="mb-1 block text-xs font-semibold uppercase tracking-wider text-slate-300">Venue / Year *</label>
            <input id="prodVenueYear" type="text" required placeholder="e.g., Davao City, 2026"
              class="w-full rounded-xl border border-slate-700 bg-slate-950 px-3.5 py-2 text-sm text-white focus:border-amber-400 focus:outline-none" />
          </div>
          <div>
            <label for="prodCategory" class="mb-1 block text-xs font-semibold uppercase tracking-wider text-slate-300">Filter Tag *</label>
            <select id="prodCategory"
              class="w-full rounded-xl border border-slate-700 bg-slate-950 px-3.5 py-2 text-sm text-white focus:border-sky-400 focus:outline-none">
              <option value="Lighting">Lighting</option>
              <option value="Resolume/LED">Resolume/LED</option>
              <option value="Audio">Audio</option>
            </select>
          </div>
        </div>

        <div class="grid grid-cols-1 gap-4 sm:grid-cols-2">
          <div>
            <label for="prodRole" class="mb-1 block text-xs font-semibold uppercase tracking-wider text-slate-300">Role *</label>
            <input id="prodRole" type="text" required placeholder="e.g., Lighting Director & Resolume Op"
              class="w-full rounded-xl border border-slate-700 bg-slate-950 px-3.5 py-2 text-sm text-white focus:border-amber-400 focus:outline-none" />
          </div>
          <div>
            <label for="prodGear" class="mb-1 block text-xs font-semibold uppercase tracking-wider text-slate-300">Consoles &amp; Gear Used *</label>
            <input id="prodGear" type="text" required placeholder="e.g., grandMA3, Resolume Arena, Midas M32"
              class="w-full rounded-xl border border-slate-700 bg-slate-950 px-3.5 py-2 text-sm text-white focus:border-sky-400 focus:outline-none" />
          </div>
        </div>

        <div>
          <label for="prodNotes" class="mb-1 block text-xs font-semibold uppercase tracking-wider text-slate-300">Production Notes &amp; Highlights *</label>
          <textarea id="prodNotes" rows="3" required placeholder="Describe lighting cues, LED wall mapping, live band mixing, or stage highlights..."
            class="w-full rounded-xl border border-slate-700 bg-slate-950 px-3.5 py-2 text-sm text-white focus:border-amber-400 focus:outline-none"></textarea>
        </div>

        <div>
          <label for="prodImageFile" class="mb-1 block text-xs font-semibold uppercase tracking-wider text-slate-300">Event Photo (Local Upload)</label>
          <input id="prodImageFile" type="file" accept="image/*" onchange="previewNewProductionImage(event)"
            class="w-full rounded-xl border border-slate-700 bg-slate-950 px-3 py-2 text-xs text-slate-300 file:mr-3 file:rounded-lg file:border-0 file:bg-amber-500 file:px-3 file:py-1.5 file:text-xs file:font-bold file:text-slate-950 hover:file:bg-amber-400" />
          <div id="prodImagePreviewWrap" class="mt-2.5 hidden">
            <img id="prodImagePreview" src="" alt="Uploaded production preview"
              class="h-36 w-full rounded-xl border border-slate-700 object-cover" />
          </div>
        </div>

        <div class="flex items-center justify-end gap-2.5 border-t border-slate-800 pt-4">
          <button type="button" onclick="closeAddProductionModal()"
            class="rounded-xl border border-slate-700 px-4 py-2 text-xs font-semibold text-slate-300 transition hover:bg-slate-800 sm:text-sm">
            Cancel
          </button>
          <button type="submit"
            class="rounded-xl bg-gradient-to-r from-amber-500 to-amber-400 px-5 py-2 text-xs font-bold text-slate-950 shadow-lg transition hover:brightness-110 sm:text-sm">
            Save Production
          </button>
        </div>
      </form>
    </div>
  </div>

  <script>
    // Storage keys for persistent portfolio & portrait customization
    const STORAGE_KEYS = {
      PRODUCTIONS: 'juess_portfolio_productions_v1',
      PORTRAIT: 'juess_portfolio_portrait_v1',
      FRAME_MODE: 'juess_portfolio_frame_mode_v1',
    };

    const DEFAULT_PRODUCTIONS = [
      {
        id: 'binibining-mati-2026',
        featured: true,
        title: 'Binibining Mati 2026',
        venueYear: 'Mati / Davao Region • 2026',
        category: 'Resolume/LED',
        role: 'Lighting Designer & Visual/LED Operator',
        gear: 'Stage Lighting Rig, Laser & Neon FX, LED Display Processor',
        notes: 'Designed full-stage lighting looks, laser and neon visual accents, LED display screen content, sponsor branding graphics, and live cue synchronization.',
        image: 'https://placehold.co/800x480/0B1120/F59E0B?text=BINIBINING+MATI+2026%0ALighting+%26+LED+Stage+Show',
      },
      {
        id: 'live-concert-festival',
        featured: false,
        title: 'Live Concert & Festival Production',
        venueYear: 'Concert & Festival Stage',
        category: 'Lighting',
        role: 'Lighting Director & Resolume Operator',
        gear: 'MA Lighting grandMA2 / grandMA3, Resolume Arena',
        notes: 'Executed dynamic moving-head beam and wash cues synced to live performances alongside multi-layer LED backdrop visuals and show sequences.',
        image: 'https://placehold.co/800x480/091224/38BDF8?text=LIVE+CONCERT+%26+FESTIVAL%0AgrandMA2+%2F+grandMA3+%26+Resolume',
      },
      {
        id: 'corporate-gala-full-band',
        featured: false,
        title: 'Corporate Gala & Full-Band Live Event',
        venueYear: 'Gala & Live Stage',
        category: 'Audio',
        role: 'Lighting Designer & Live Audio Technician',
        gear: 'Avolites, Midas M32 / Yamaha TF5',
        notes: 'Delivered stage wash and truss uplighting paired with full-band stage setup, signal routing, sound reinforcement, and live FOH audio mixing.',
        image: 'https://placehold.co/800x480/0B132B/60A5FA?text=CORPORATE+GALA+%26+FULL+BAND%0AAvolites+%2C+Midas+M32+%2F+Yamaha+TF5',
      },
    ];

    let activePortfolioFilter = 'All';
    let pendingProductionImageDataUrl = '';
    let frameStyleIndex = 0;

    const PORTRAIT_FRAMES = [
      {
        label: 'Amber FOH Frame',
        src: 'https://placehold.co/600x760/0B101B/F59E0B?text=JUESS+CHRISTIAN%0ADE+ERIO%0AFOH+PORTRAIT',
      },
      {
        label: 'Cyan Stage Frame',
        src: 'https://placehold.co/600x760/081326/38BDF8?text=LIGHTING+DIRECTOR%0ARESOLUME+%26+AUDIO%0ADAVAO+CITY',
      },
    ];

    // Toast helper (avoids alert())
    function showToast(message) {
      const banner = document.getElementById('toastBanner');
      const textEl = document.getElementById('toastMessage');
      if (!banner || !textEl) return;
      textEl.textContent = message;
      banner.classList.remove('hidden');
      clearTimeout(window.__toastTimer);
      window.__toastTimer = setTimeout(() => {
        banner.classList.add('hidden');
      }, 3200);
    }

    // Clipboard helper using execCommand fallback for iframe compatibility
    function copyContact(value, label) {
      try {
        const tempInput = document.createElement('input');
        tempInput.value = value;
        tempInput.setAttribute('readonly', '');
        tempInput.style.position = 'fixed';
        tempInput.style.opacity = '0';
        document.body.appendChild(tempInput);
        tempInput.select();
        const copied = document.execCommand('copy');
        document.body.removeChild(tempInput);

        if (copied) {
          showToast(`${label} (${value}) copied to clipboard.`);
        } else {
          showToast(`${label}: ${value}`);
        }
      } catch (err) {
        showToast(`${label}: ${value}`);
      }
    }

    // Portrait upload & frame switching
    function handlePortraitUpload(event) {
      const file = event.target.files && event.target.files[0];
      if (!file) return;

      const reader = new FileReader();
      reader.onload = function (e) {
        const dataUrl = e.target.result;
        const img = document.getElementById('portraitImg');
        const badge = document.getElementById('portraitStatusBadge');
        if (img && typeof dataUrl === 'string') {
          img.src = dataUrl;
          if (badge) badge.textContent = 'Custom Photo';
          try {
            localStorage.setItem(STORAGE_KEYS.PORTRAIT, dataUrl);
          } catch (storageErr) {
            // Ignore quota issues if image is very large
          }
          showToast('Portrait photo updated.');
        }
      };
      reader.readAsDataURL(file);
    }

    function togglePortraitFrame() {
      frameStyleIndex = (frameStyleIndex + 1) % PORTRAIT_FRAMES.length;
      const preset = PORTRAIT_FRAMES[frameStyleIndex];
      const img = document.getElementById('portraitImg');
      const badge = document.getElementById('portraitStatusBadge');
      try {
        localStorage.removeItem(STORAGE_KEYS.PORTRAIT);
        localStorage.setItem(STORAGE_KEYS.FRAME_MODE, String(frameStyleIndex));
      } catch (err) {}
      if (img) img.src = preset.src;
      if (badge) badge.textContent = preset.label;
      showToast(`Switched to ${preset.label}.`);
    }

    function resetPortrait() {
      frameStyleIndex = 0;
      try {
        localStorage.removeItem(STORAGE_KEYS.PORTRAIT);
        localStorage.removeItem(STORAGE_KEYS.FRAME_MODE);
      } catch (err) {}
      const img = document.getElementById('portraitImg');
      const badge = document.getElementById('portraitStatusBadge');
      const input = document.getElementById('portraitFileInput');
      if (img) img.src = PORTRAIT_FRAMES[0].src;
      if (badge) badge.textContent = 'Default Frame';
      if (input) input.value = '';
      showToast('Portrait reset to default frame.');
    }

    function initPortraitFromStorage() {
      try {
        const savedPortrait = localStorage.getItem(STORAGE_KEYS.PORTRAIT);
        const savedFrame = localStorage.getItem(STORAGE_KEYS.FRAME_MODE);
        const img = document.getElementById('portraitImg');
        const badge = document.getElementById('portraitStatusBadge');
        if (savedPortrait && img) {
          img.src = savedPortrait;
          if (badge) badge.textContent = 'Custom Photo';
          return;
        }
        if (savedFrame !== null) {
          frameStyleIndex = Number(savedFrame) % PORTRAIT_FRAMES.length;
          if (img) img.src = PORTRAIT_FRAMES[frameStyleIndex].src;
          if (badge) badge.textContent = PORTRAIT_FRAMES[frameStyleIndex].label;
        }
      } catch (err) {}
    }

    // Technical Rig filter
    function setRigFilter(filter) {
      document.querySelectorAll('.rig-tab').forEach((btn) => {
        const isActive = btn.getAttribute('data-rig-filter') === filter;
        btn.classList.toggle('bg-amber-500', isActive);
        btn.classList.toggle('text-slate-950', isActive);
        btn.classList.toggle('font-bold', isActive);
        btn.classList.toggle('text-slate-300', !isActive);
        btn.classList.toggle('font-semibold', !isActive);
      });

      document.querySelectorAll('#rigGrid article').forEach((card) => {
        const discipline = card.getAttribute('data-discipline');
        const show = filter === 'all' || discipline === filter;
        card.classList.toggle('hidden', !show);
      });
    }

    // Portfolio state & rendering
    function loadProductions() {
      try {
        const raw = localStorage.getItem(STORAGE_KEYS.PRODUCTIONS);
        if (!raw) return [...DEFAULT_PRODUCTIONS];
        const parsed = JSON.parse(raw);
        return Array.isArray(parsed) && parsed.length ? parsed : [...DEFAULT_PRODUCTIONS];
      } catch (err) {
        return [...DEFAULT_PRODUCTIONS];
      }
    }

    function saveProductions(list) {
      try {
        localStorage.setItem(STORAGE_KEYS.PRODUCTIONS, JSON.stringify(list));
      } catch (err) {
        showToast('Saved in session (browser storage full for large images).');
      }
    }

    function escapeHtml(str) {
      return String(str || '')
        .replace(/&/g, '&amp;')
        .replace(/</g, '&lt;')
        .replace(/>/g, '&gt;')
        .replace(/"/g, '&quot;');
    }

    function getCategoryBadgeStyle(category) {
      if (category === 'Lighting') {
        return 'border-amber-400/40 bg-amber-500/15 text-amber-300';
      }
      if (category === 'Resolume/LED') {
        return 'border-sky-400/40 bg-sky-500/15 text-sky-300';
      }
      return 'border-blue-400/40 bg-blue-500/15 text-blue-300';
    }

    function setPortfolioFilter(category) {
      activePortfolioFilter = category;
      document.querySelectorAll('.pfilter-btn').forEach((btn) => {
        const isActive = btn.getAttribute('data-pfilter') === category;
        btn.classList.toggle('bg-sky-500', isActive);
        btn.classList.toggle('text-slate-950', isActive);
        btn.classList.toggle('font-bold', isActive);
        btn.classList.toggle('text-slate-300', !isActive);
        btn.classList.toggle('font-semibold', !isActive);
      });
      renderProductions();
    }

    function renderProductions() {
      const grid = document.getElementById('portfolioGrid');
      if (!grid) return;

      const items = loadProductions();
      const filtered = activePortfolioFilter === 'All'
        ? items
        : items.filter((item) => item.category === activePortfolioFilter);

      if (!filtered.length) {
        grid.innerHTML = `
          <div class="col-span-full rounded-2xl border border-dashed border-slate-700 bg-slate-900/60 p-8 text-center">
            <p class="text-sm font-semibold text-slate-300">No productions found under "${escapeHtml(activePortfolioFilter)}" yet.</p>
            <button type="button" onclick="openAddProductionModal()" class="mt-3 rounded-xl bg-amber-500 px-4 py-2 text-xs font-bold text-slate-950">
              + Add Production
            </button>
          </div>
        `;
        return;
      }

      grid.innerHTML = filtered.map((item) => {
        const safeImg = item.image || 'https://placehold.co/800x480/0B101B/F59E0B?text=STAGE+PRODUCTION';
        const fallbackImg = 'https://placehold.co/800x480/0B101B/38BDF8?text=PRODUCTION+SHOWCASE';
        return `
          <article class="print-card flex flex-col justify-between overflow-hidden rounded-2xl border ${item.featured ? 'border-amber-400/50 shadow-amberGlow' : 'border-slate-800'} bg-slate-900/85 transition hover:border-sky-400/50">
            <div>
              <div class="relative aspect-video w-full overflow-hidden bg-slate-950">
                <img src="${safeImg}"
                  onerror="this.onerror=null;this.src='${fallbackImg}';"
                  alt="${escapeHtml(item.title)}"
                  class="h-full w-full object-cover" />
                <div class="absolute left-3 top-3 flex flex-wrap gap-1.5">
                  ${item.featured ? '<span class="rounded-md bg-amber-500 px-2.5 py-0.5 text-[11px] font-extrabold text-slate-950">FEATURED</span>' : ''}
                  <span class="rounded-md border px-2.5 py-0.5 text-[11px] font-bold backdrop-blur-sm ${getCategoryBadgeStyle(item.category)}">
                    ${escapeHtml(item.category)}
                  </span>
                </div>
              </div>

              <div class="p-5">
                <div class="text-xs font-medium text-slate-400">${escapeHtml(item.venueYear)}</div>
                <h3 class="mt-1 text-lg font-bold text-white">${escapeHtml(item.title)}</h3>
                <p class="mt-1 text-xs font-semibold text-sky-300">${escapeHtml(item.role)}</p>

                <div class="mt-3 rounded-xl border border-slate-800 bg-slate-950/70 px-3 py-2 text-xs text-amber-200">
                  <span class="font-bold text-amber-400">Rig / Gear:</span> ${escapeHtml(item.gear)}
                </div>

                <p class="mt-3 text-sm leading-relaxed text-slate-300">${escapeHtml(item.notes)}</p>
              </div>
            </div>

            ${!item.featured ? `
              <div class="no-print flex items-center justify-end border-t border-slate-800/80 px-5 py-2.5">
                <button type="button" onclick="deleteProduction('${escapeHtml(item.id)}')"
                  class="text-xs font-medium text-slate-400 transition hover:text-rose-400">
                  Remove Card
                </button>
              </div>
            ` : ''}
          </article>
        `;
      }).join('');
    }

    function deleteProduction(id) {
      const updated = loadProductions().filter((item) => item.id !== id);
      saveProductions(updated);
      renderProductions();
      showToast('Production card removed.');
    }

    // Add Production modal handlers
    function openAddProductionModal() {
      pendingProductionImageDataUrl = '';
      const form = document.getElementById('addProductionForm');
      const previewWrap = document.getElementById('prodImagePreviewWrap');
      if (form) form.reset();
      if (previewWrap) previewWrap.classList.add('hidden');
      const modal = document.getElementById('addProductionModal');
      if (modal) {
        modal.classList.remove('hidden');
        modal.classList.add('flex');
      }
    }

    function closeAddProductionModal() {
      const modal = document.getElementById('addProductionModal');
      if (modal) {
        modal.classList.add('hidden');
        modal.classList.remove('flex');
      }
    }

    function previewNewProductionImage(event) {
      const file = event.target.files && event.target.files[0];
      if (!file) return;
      const reader = new FileReader();
      reader.onload = function (e) {
        pendingProductionImageDataUrl = typeof e.target.result === 'string' ? e.target.result : '';
        const preview = document.getElementById('prodImagePreview');
        const wrap = document.getElementById('prodImagePreviewWrap');
        if (preview && wrap && pendingProductionImageDataUrl) {
          preview.src = pendingProductionImageDataUrl;
          wrap.classList.remove('hidden');
        }
      };
      reader.readAsDataURL(file);
    }

    function handleAddProduction(event) {
      event.preventDefault();
      const title = document.getElementById('prodTitle').value.trim();
      const venueYear = document.getElementById('prodVenueYear').value.trim();
      const category = document.getElementById('prodCategory').value;
      const role = document.getElementById('prodRole').value.trim();
      const gear = document.getElementById('prodGear').value.trim();
      const notes = document.getElementById('prodNotes').value.trim();

      if (!title || !venueYear || !role || !gear || !notes) return;

      const newEntry = {
        id: 'prod-' + Date.now(),
        featured: false,
        title,
        venueYear,
        category,
        role,
        gear,
        notes,
        image: pendingProductionImageDataUrl || `https://placehold.co/800x480/0B101B/F59E0B?text=${encodeURIComponent(title)}`,
      };

      const existing = loadProductions();
      existing.unshift(newEntry);
      saveProductions(existing);
      closeAddProductionModal();
      renderProductions();
      showToast(`Added "${title}" to your portfolio.`);
    }

    // Booking inquiry handler
    function handleBookingSubmit(event) {
      event.preventDefault();
      const name = document.getElementById('clientName').value.trim();
      const contact = document.getElementById('clientContact').value.trim();
      const role = document.getElementById('serviceRole').value;
      const eventDate = document.getElementById('eventDateVenue').value.trim();
      const notes = document.getElementById('projectNotes').value.trim();

      const subject = encodeURIComponent(`Production Inquiry: ${role} — ${name}`);
      const body = encodeURIComponent(
        `Name / Organization: ${name}\nContact: ${contact}\nRole Needed: ${role}\nDate & Venue: ${eventDate || 'TBD'}\n\nDetails:\n${notes}`
      );

      const statusEl = document.getElementById('inquiryStatus');
      if (statusEl) {
        statusEl.textContent = `Inquiry prepared for ${name}. Opening email draft to iandeerio2@gmail.com...`;
      }
      showToast('Booking inquiry prepared for iandeerio2@gmail.com.');
      window.location.href = `mailto:iandeerio2@gmail.com?subject=${subject}&body=${body}`;
    }

    document.addEventListener('DOMContentLoaded', () => {
      initPortraitFromStorage();
      renderProductions();
    });
  </script>
</body>
</html>
