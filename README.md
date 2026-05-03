# 💪 A Game — Home Workout Trainer

> **No gym. No equipment. All gains.**

A Game is a fully interactive, browser-based bodybuilding trainer that uses a clickable human anatomy model and real animated human figures to teach you how to work out at home — with zero equipment.

---

## 🌐 Live Site

**[https://allan-arch-sudo.github.io/A-game/](https://allan-arch-sudo.github.io/A-game/)**

---

## 📸 Preview

| Anatomy Model | Animated Exercise | Weekly Plan |
|---|---|---|
| Click any muscle group on the front/back human model | Watch a real human figure animate the exact movement | Follow the built-in 7-day split |

---

## ✨ Features

### 🫀 Interactive Anatomy Model
- Realistic human figure with skin tones, hair, facial features, muscle definition, shorts and shoes
- **Front view** — Chest, Shoulders, Arms, Core/Abs, Quads, Calves
- **Back view** — Back, Shoulders, Arms, Glutes, Hamstrings, Calves
- Active muscle group highlights red on click
- Sidebar legend for quick muscle selection

### 🏃 Real Human Exercise Animations
Each exercise renders a full joint-based skeleton figure with:
- Head, neck, torso, upper arms, forearms, hands
- Thighs, shins, feet — all with correct joint articulation
- Smooth 4-frame motion cycles (0.66s per frame)
- Rep counter that increments as animation loops
- Frame progress tracker dots
- ▶ Play / ⏸ Pause control

### 📋 Exercise Panel
For every exercise you get:
- Sets & reps
- Muscles worked (tagged chips)
- Step-by-step instructions (numbered)
- A pro coaching tip
- Tab switching between all exercises per muscle group

### 📅 7-Day Training Plan
| Day | Focus | Muscles |
|-----|-------|---------|
| Monday | Push Day | Chest · Shoulders · Triceps |
| Tuesday | Pull Day | Back · Biceps |
| Wednesday | Legs | Quads · Glutes · Calves |
| Thursday | Active Rest | Walk · Stretch |
| Friday | Core & Glutes | Abs · Glutes · Lower Back |
| Saturday | Full Body | Compound moves only |
| Sunday | Rest | Recovery = growth |

### 🧠 Training Principles Section
6 evidence-based coaching cards covering:
- Progressive Overload
- Sleep & Recovery
- Protein Intake
- Mind-Muscle Connection
- Hydration
- Consistency

---

## 🏋️ Muscle Groups & Exercises

### Chest — Push / Anterior
| Exercise | Sets | Muscles |
|----------|------|---------|
| Push-up | 3×15 | Chest, Triceps, Front Delt |
| Wide Push-up | 3×12 | Outer Chest, Shoulders |
| Diamond Push-up | 3×10 | Inner Chest, Triceps |
| Decline Push-up | 3×12 | Upper Chest, Front Delt |

### Shoulders — Push / Deltoids
| Exercise | Sets | Muscles |
|----------|------|---------|
| Pike Push-up | 3×10 | Front Delt, Triceps |
| Lateral Raise | 3×15 | Side Delt |
| Wall Handstand | 3×20s | All 3 Delt Heads, Core |

### Arms — Biceps & Triceps
| Exercise | Sets | Muscles |
|----------|------|---------|
| Tricep Dip | 3×12 | Triceps, Chest |
| Doorframe Curl | 3×10 | Biceps, Brachialis |
| Diamond Push-up | 3×10 | Triceps, Inner Chest |

### Core & Abs — Core Stability
| Exercise | Sets | Muscles |
|----------|------|---------|
| Plank | 3×45s | Full Core, Glutes, Shoulders |
| Bicycle Crunch | 3×20 | Obliques, Upper Abs |
| Leg Raise | 3×15 | Lower Abs, Hip Flexors |

### Back — Pull / Posterior
| Exercise | Sets | Muscles |
|----------|------|---------|
| Superman Hold | 3×15 | Lower Back, Glutes, Rear Delt |
| Table Row | 3×12 | Lats, Rhomboids, Biceps |
| Reverse Snow Angel | 3×15 | Upper Back, Rear Delt |

### Legs — Lower Body / Quads
| Exercise | Sets | Muscles |
|----------|------|---------|
| Bodyweight Squat | 3×20 | Quads, Glutes, Hamstrings |
| Bulgarian Split Squat | 3×12 | Quads, Glutes, Balance |
| Jump Squat | 3×15 | Power, Explosiveness |

### Glutes — Lower Body / Posterior
| Exercise | Sets | Muscles |
|----------|------|---------|
| Glute Bridge | 4×20 | Glutes, Hamstrings, Core |
| Donkey Kick | 3×15 | Glute Max, Glute Med |
| Single-Leg Bridge | 3×15 | Glutes, Hamstrings |

### Calves — Lower Leg
| Exercise | Sets | Muscles |
|----------|------|---------|
| Calf Raise | 4×25 | Gastrocnemius, Soleus |
| Single-Leg Raise | 3×15 | Gastrocnemius, Power |

---

## 🛠️ Tech Stack

| Technology | Usage |
|------------|-------|
| **HTML5** | Single-file app, no build step |
| **CSS3** | Dark theme UI, CSS variables, grid/flex layout, animations |
| **Vanilla JavaScript** | All logic — zero dependencies, zero frameworks |
| **SVG** | Anatomy model, all human figure rendering |
| **Google Fonts** | Bebas Neue (headings) + DM Sans (body) |

### How the Animation Engine Works
The human figure is rendered entirely in SVG using a **joint-based skeleton system**:

1. A pose is defined as a set of joint angles (spine, neck, shoulder, elbow, hip, knee)
2. The `drawFigure()` function computes joint positions using trigonometry (`sin`/`cos`)
3. Limbs are drawn as capsule-shaped SVG paths between computed joint points
4. Keyframes are arrays of pose objects — `setInterval` cycles through them at 660ms
5. The anatomy model uses separate layered SVG paths per muscle group, each with a `data-id` for click targeting

---

## 🗂️ File Structure

```
A-game/
└── index.html        # Entire app — HTML + CSS + JS in one file
```

No build tools. No npm. No dependencies. Open `index.html` in any browser and it works.

---

## 🚀 Running Locally

```bash
git clone https://github.com/Allan-arch-sudo/A-game.git
cd A-game
# Open index.html in your browser
xdg-open index.html       # Linux / Zorin OS
open index.html           # macOS
start index.html          # Windows
```

---

## 🌍 Deploying to GitHub Pages

1. Go to your repo → **Settings → Pages**
2. Under **Source**, select `main` branch, `/ (root)` folder
3. Click **Save**
4. Your site goes live at `https://allan-arch-sudo.github.io/A-game/`

Or via terminal:
```bash
gh api repos/Allan-arch-sudo/A-game/pages \
  --method POST \
  --field source='{"branch":"main","path":"/"}'
```

---

## 🔮 Roadmap / Future Ideas

- [ ] Workout timer with rest countdown
- [ ] Progress tracker (sets logged per session)
- [ ] Difficulty levels (beginner / intermediate / advanced)
- [ ] Sound cues for reps
- [ ] Mobile-optimized touch gestures
- [ ] Dark/light mode toggle
- [ ] More exercises per muscle group
- [ ] Print-friendly workout card

---

## 👤 Author

**Allan** — [@Allan-arch-sudo](https://github.com/Allan-arch-sudo)

Built with Claude · Hosted on GitHub Pages

---

## 📄 License

MIT License — free to use, modify and share.
