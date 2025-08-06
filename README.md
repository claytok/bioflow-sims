# Biotransport Phenomena - Interactive Simulations

A comprehensive web-based learning platform for understanding fundamental transport processes in biological systems. Designed for senior-level biomedical engineering students, these interactive simulations provide hands-on experience with the physical principles governing biotransport phenomena.

## 🚀 Quick Start

1. **Open the platform:** Navigate to `index.html` in your web browser
2. **Choose a simulation:** Select from the landing page cards
3. **Explore interactively:** Adjust parameters and observe real-time changes
4. **Learn the physics:** Each simulation includes mathematical models and biological context

## 📱 Mobile Optimized

All simulations are fully responsive and optimized for mobile devices:
- **Touch-friendly controls** with larger tap targets
- **Responsive layouts** that adapt to screen size
- **Mobile-optimized visualizations** that scale appropriately
- **Single-column layouts** on small screens for better usability

## 📊 Available Simulations

### 1. 🧮 Math Review: Essential Tools for Biotransport
**File:** `math/index.html`

**Description:** Comprehensive mathematical foundation covering partial derivatives, vector calculus, coordinate systems, and differential equations essential for biotransport phenomena.

**Key Features:**
- Interactive gradient demonstrations
- Coordinate system comparisons (Cartesian vs. Cylindrical)
- Real-time mathematical visualizations
- Biological examples and applications
- Practice problems with solutions

**Topics Covered:**
- Partial derivatives and chain rule
- Vector calculus (gradient, divergence)
- Coordinate systems for blood vessels
- Ordinary and partial differential equations

### 2. 🔄 Lagrangian vs Eulerian Perspectives
**File:** `Euler/index.html`

**Description:** Interactive comparison of Lagrangian and Eulerian frames of reference in fluid dynamics through animated red blood cell tracking.

**Key Features:**
- Side-by-side Lagrangian and Eulerian views
- Animated red blood cell tracking
- Real-time flow measurement simulation
- Educational explanations of each perspective
- Interactive controls for animation speed

**Learning Objectives:**
- Understand material vs. spatial descriptions
- Compare particle tracking vs. fixed-point measurement
- Apply concepts to drug delivery and flow measurement

### 3. 🩸 Blood Rheology and Non-Newtonian Behavior
**File:** `Blood_Rheology/index.html`

**Description:** Explore the complex rheological properties of blood, including non-Newtonian behavior, shear-thinning characteristics, and clinical condition effects.

**Key Features:**
- Carreau-Yasuda model implementation
- Real-time viscosity vs. shear rate curves
- Clinical scenario buttons (Normal, Anemia, Polycythemia, Sickle Cell, Diabetes)
- Biological context labels for all parameters
- Interactive flow visualization with RBC deformation

**Parameters:**
- Hematocrit (20-60%) with biological context
- Temperature (20-40°C) with clinical relevance
- Shear Rate (0.1-1000 s⁻¹) with flow type labels
- Aggregation Level (0-100%) with pathological context

**Clinical Scenarios:**
- **Normal Blood:** Standard hematocrit and aggregation
- **Anemia:** Reduced RBC count and viscosity
- **Polycythemia:** Elevated RBC count and viscosity
- **Sickle Cell:** Abnormal RBC shape and increased aggregation
- **Diabetes:** Elevated aggregation due to glucose effects

### 4. 💧 Poiseuille Flow in Blood Vessels
**File:** `Poiseuille_Flow/index.html`

**Description:** Investigate laminar flow in blood vessels with biologically accurate parameters and real-time flow visualization.

**Key Features:**
- Parabolic velocity profiles with moving particles
- Biologically realistic vessel parameters
- Clinical scenario buttons (Artery, Vein, Capillary, Stenosis, Aneurysm, Exercise, Anemia, Diabetes)
- Real-time Reynolds number and wall shear stress calculations
- Flow rate display with appropriate units (μL/min to fL/min)

**Parameters:**
- Pressure Gradient (10-25,000 Pa/m) with vessel context
- Vessel Radius (0.004-5 mm) with biological labels
- Blood Viscosity (2-10 mPa·s) with clinical context

**Vessel Types:**
- **Artery:** High pressure, large radius, fast flow
- **Vein:** Lower pressure, medium radius, moderate flow
- **Capillary:** Very low pressure, tiny radius, slow flow
- **Stenosis:** Constricted vessel with increased velocity
- **Aneurysm:** Expanded vessel with decreased velocity

### 5. 🌊 Reynolds Transport Theorem (RTT)
**File:** `RTT/index.html`

**Description:** Visualize the fundamental bridge between Lagrangian and Eulerian perspectives in fluid mechanics through interactive control volume analysis.

**Key Features:**
- Toggle between Eulerian and Lagrangian views
- Interactive control volume and material volume visualization
- Clinical scenarios (Normal, Stenosis, Aneurysm, Drug Injection)
- Real-time particle tracking and measurement
- Educational explanations of RTT concepts

**Learning Objectives:**
- Understand control volume vs. material volume
- Connect experimental measurements to material tracking
- Apply RTT to clinical flow measurements

### 6. 🌊 Mass Transport: Diffusion in Biological Systems
**File:** `Diffusion/index.html`

**Description:** Study molecular diffusion processes with smooth, realistic visualizations and biologically relevant scenarios.

**Key Features:**
- Smooth concentration gradient visualization (no blinking particles)
- Biologically accurate diffusion coefficients
- Scenario-specific molecule types and colors
- Real-time flux and penetration depth calculations
- Temperature and concentration effects

**Biological Scenarios:**
- **O₂ Diffusion:** Fast diffusion (50 × 10⁻⁹ m²/s), tiny molecule
- **Drug Delivery:** Slow diffusion (2 × 10⁻⁹ m²/s), very large molecule
- **Glucose Transport:** Medium diffusion (15 × 10⁻⁹ m²/s), large molecule
- **Urea Removal:** Fast diffusion (30 × 10⁻⁹ m²/s), small molecule

## 🛠️ Technical Implementation

### Architecture
- **Frontend:** Pure HTML5, CSS3, and JavaScript
- **Graphics:** HTML5 Canvas for real-time visualization
- **Physics:** Mathematical models based on biotransport principles
- **Responsive Design:** Mobile-first approach with touch optimization
- **Deployment:** Netlify-ready with proper configuration

### File Structure
```
bioflow-sims-main/
├── index.html                    # Main landing page
├── bioflowsim.png               # Favicon and branding
├── math/index.html              # Math review module
├── Euler/index.html             # Lagrangian vs Eulerian
├── Blood_Rheology/index.html    # Blood rheology simulation
├── Poiseuille_Flow/index.html   # Poiseuille flow simulation
├── RTT/index.html               # Reynolds Transport Theorem
├── Diffusion/index.html         # Diffusion simulation
├── netlify.toml                 # Deployment configuration
├── _redirects                   # URL routing
└── deploy-checklist.md          # Deployment guide
```

### Mathematical Models

#### Blood Rheology
- **Carreau-Yasuda Model:** η = η∞ + (η₀ - η∞)[1 + (λγ)ᵃ]^((n-1)/a)
- **Temperature Effect:** η(T) = η₀ × exp(0.025 × (37 - T))
- **Hematocrit Effect:** η(HCT) = η₀ × (1 - 0.45×HCT)^(-2.5)
- **Aggregation Effect:** η₀ = η₀_base × (1 + 2 × aggregation)

#### Diffusion
- **Fick's First Law:** J = -D × ∇C
- **Fick's Second Law:** ∂C/∂t = D∇²C
- **Temperature Effect:** D(T) = D₀ × (T/T₀)^(3/2)
- **Size Effect:** D ∝ 1/√(molecular size)

#### Poiseuille Flow
- **Velocity Profile:** v(r) = (ΔP/4μL) × (R² - r²)
- **Flow Rate:** Q = (πR⁴ΔP)/(8μL)
- **Reynolds Number:** Re = (2ρvR)/μ
- **Wall Shear Stress:** τ = (4μQ)/(πR³)

#### Reynolds Transport Theorem
- **Material Derivative:** D/Dt = ∂/∂t + v·∇
- **RTT Equation:** D/Dt ∫∫∫_sys ρη dV = ∂/∂t ∫∫∫_CV ρη dV + ∫∫_CS ρη(v·n) dA

## 🎓 Educational Features

### Interactive Learning
- **Real-time parameter adjustment** with immediate visual feedback
- **Biological context labels** explaining parameter significance
- **Clinical scenario buttons** for realistic applications
- **Mathematical equation displays** with explanations
- **Self-assessment opportunities** through interactive exploration

### Mobile Optimization
- **Touch-friendly controls** with 44px minimum tap targets
- **Responsive layouts** that adapt to all screen sizes
- **Optimized typography** for mobile readability
- **Single-column layouts** on small screens

## 🚀 Deployment

### Local Development
1. Clone the repository
2. Open `index.html` in a web browser
3. All simulations work offline

### Netlify Deployment
- **Automatic deployment** from GitHub
- **Custom domain support**
- **HTTPS enabled**
- **Global CDN** for fast loading

### Configuration Files
- `netlify.toml`: Build and redirect configuration
- `_redirects`: URL routing for clean navigation

## 📚 Learning Objectives

### By the end of this platform, students will be able to:
1. **Understand fundamental biotransport principles** through interactive exploration
2. **Apply mathematical models** to biological systems
3. **Compare different analytical approaches** (Lagrangian vs. Eulerian)
4. **Interpret clinical measurements** in terms of underlying physics
5. **Design experiments** based on transport principles
6. **Analyze complex biological systems** using simplified models
7. **Navigate between different coordinate systems** and analytical frameworks

## 🎯 Target Audience

- **Senior-level biomedical engineering students**
- **Graduate students** in bioengineering and related fields
- **Researchers** needing interactive visualization tools
- **Educators** looking for engaging teaching materials
- **Anyone interested** in understanding biotransport phenomena through interactive learning

## 🔧 Customization

### Adding New Simulations
1. Create a new folder with `index.html`
2. Add favicon reference: `<link rel="icon" type="image/png" href="../bioflowsim.png">`
3. Include mobile-responsive CSS
4. Add card to main `index.html`

### Modifying Parameters
- All parameters are easily adjustable in the JavaScript files
- Biological scenarios can be modified in the `scenarios` objects
- Mathematical models are clearly documented in comments

## 📄 License

This project is designed for educational use. Please contact the author for commercial applications.

## 👨‍🏫 Author

**Dr. Katherine Clayton** - Biomedical Engineering Educator

---

*Built with modern web technologies for optimal learning experience across all devices.*
