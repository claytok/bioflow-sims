# Biotransport Phenomena - Interactive Simulations

A comprehensive collection of interactive simulations for understanding fundamental transport processes in biological systems. Designed for senior-level biomedical engineering students, these simulations provide hands-on experience with the physical principles governing biotransport phenomena.

## 🚀 Quick Start

1. Open `index.html` in your web browser
2. Choose a simulation from the landing page
3. Interact with the controls to explore different parameters
4. Observe real-time visualizations and calculations

## 📊 Available Simulations

### 1. Blood Rheology and Non-Newtonian Behavior
**File:** `Blood_Rheology/simulation.html`

**Description:** Explore the complex rheological properties of blood, including its non-Newtonian behavior, shear-thinning characteristics, and the effects of hematocrit, temperature, and red blood cell aggregation.

**Key Features:**
- Carreau-Yasuda model for blood viscosity
- Real-time viscosity vs. shear rate curves
- Hematocrit effects on flow behavior
- Temperature dependence visualization
- Red blood cell deformation and aggregation
- Interactive flow visualization

**Parameters:**
- Hematocrit (20-60%)
- Temperature (20-40°C)
- Shear Rate (0.1-1000 s⁻¹)
- Aggregation Level (0-100%)

### 2. Mass Transport: Diffusion in Biological Systems
**File:** `Diffusion/simulation.html`

**Description:** Study molecular diffusion processes in biological systems, including concentration gradients, temperature effects, molecule size impacts, and time-dependent diffusion profiles.

**Key Features:**
- Real-time concentration profile visualization
- Temperature and molecular size effects
- Diffusion coefficient calculations
- Flux and penetration depth analysis
- Pre-configured biological scenarios
- Animated diffusion processes

**Parameters:**
- Diffusion Coefficient (1-100 × 10⁻⁹ m²/s)
- Initial Concentration (1-100 mM)
- Temperature (20-50°C)
- Molecule Size (1-5 scale)

**Biological Scenarios:**
- Oxygen diffusion in tissues
- Drug delivery across membranes
- Nutrient transport in cells
- Waste removal processes

### 3. Poiseuille Flow in Blood Vessels
**File:** `Poiseuille_Flow/simulation.html`

**Description:** Investigate laminar flow in blood vessels, including pressure gradients, velocity profiles, Reynolds number effects, and vessel geometry impacts.

**Key Features:**
- Parabolic velocity profiles
- Pressure gradient visualization
- Reynolds number analysis
- Vessel type selection
- Real-time flow animation
- Turbulent vs. laminar flow

**Parameters:**
- Pressure Gradient (100-1000 Pa/m)
- Vessel Radius (0.1-2.0 mm)
- Blood Viscosity (2-6 mPa·s)
- Vessel Type (Artery, Vein, Capillary)

## 🛠️ Technical Details

### Implementation
- **Frontend:** Pure HTML5, CSS3, and JavaScript
- **Graphics:** HTML5 Canvas for real-time visualization
- **Physics:** Mathematical models based on biotransport principles
- **Responsive Design:** Works on desktop and mobile devices

### Mathematical Models

#### Blood Rheology
- **Carreau-Yasuda Model:** η = η∞ + (η₀ - η∞)[1 + (λγ)ᵃ]^((n-1)/a)
- **Temperature Effect:** η(T) = η₀ × exp(0.025 × (37 - T))
- **Hematocrit Effect:** η(HCT) = η₀ × (1 - 0.45×HCT)^(-2.5)

#### Diffusion
- **Fick's First Law:** J = -D × ∇C
- **Temperature Effect:** D(T) = D₀ × (T/T₀)^(3/2)
- **Size Effect:** D ∝ 1/√(molecular size)

#### Poiseuille Flow
- **Velocity Profile:** v(r) = (ΔP/4μL) × (R² - r²)
- **Flow Rate:** Q = (πR⁴ΔP)/(8μL)
- **Reynolds Number:** Re = (2ρvR)/μ

## 📚 Educational Value

These simulations help students understand:

1. **Physical Principles:** Fundamental laws governing biotransport
2. **Parameter Effects:** How changing conditions affects transport
3. **Biological Relevance:** Real-world applications in physiology
4. **Mathematical Modeling:** Converting physical principles to equations
5. **Visual Learning:** Intuitive understanding through interactive graphics

## 🎯 Learning Objectives

### Blood Rheology
- Understand non-Newtonian fluid behavior
- Recognize shear-thinning characteristics
- Appreciate hematocrit effects on viscosity
- Visualize red blood cell deformation

### Diffusion
- Master Fick's laws of diffusion
- Understand concentration gradients
- Recognize temperature and size effects
- Analyze diffusion time scales

### Poiseuille Flow
- Understand laminar flow characteristics
- Recognize pressure-flow relationships
- Appreciate vessel geometry effects
- Distinguish laminar vs. turbulent flow

## 🔧 Customization

Each simulation can be customized by modifying:
- Parameter ranges and default values
- Visual appearance and color schemes
- Mathematical models and constants
- Biological scenarios and examples

## 📖 References

- Carreau, P.J. (1972). Rheological equations from molecular network theories
- Yasuda, K. (1979). Rheological properties of blood
- Fick, A. (1855). On liquid diffusion
- Poiseuille, J.L.M. (1846). Recherches expérimentales sur le mouvement des liquides

## 🤝 Contributing

This project is designed for educational purposes. Contributions to improve accuracy, add new features, or enhance educational value are welcome.

## 📄 License

Educational use - designed for biomedical engineering education.

---

**For questions or suggestions, please contact the course instructor.**
