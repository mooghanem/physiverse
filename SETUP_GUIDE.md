# PhysiVerse - Setup & Installation Guide

## Quick Installation (2 minutes)

### Step 1: Install Python
Ensure you have Python 3.8 or higher:
```bash
python --version
```

### Step 2: Clone & Navigate
```bash
git clone https://github.com/mooghanem/physiverse.git
cd physiverse
```

### Step 3: Install Dependencies
```bash
pip install -r requirements.txt
```

### Step 4: Run the App
```bash
streamlit run app.py
```

The app will automatically open in your browser at `http://localhost:8501`

---

## 🎯 Using PhysiVerse

### Navigation
1. **Simulation Selector** (Sidebar top): Choose which physics simulation to explore
2. **Parameter Controls** (Sidebar): Adjust simulation parameters with sliders
3. **Main Dashboard**: View real-time metrics and interactive visualizations
4. **Learning Tabs** (Below visualizations): Explore theory and applications

### Example Workflows

#### 🚀 Projectile Motion
```
1. Select "Projectile Motion" from dropdown
2. Move "Initial Velocity" slider to 50 m/s
3. Move "Launch Angle" slider to 45°
4. Observe the trajectory curve update in real-time
5. Check "Max Height" metric (should be ~127 m)
6. Expand "Physics Fundamentals" to learn why 45° is optimal
```

#### 🪐 Orbital Mechanics
```
1. Select "Orbital Mechanics" from dropdown
2. Choose "Sun" from "Select Primary Body"
3. Choose "Earth" from "Select Secondary Body"
4. Adjust "Eccentricity" slider from 0 to 0.3
5. Watch the orbit shape change from circular to elliptical
6. Compare orbital period with real Earth orbital period (~365 days)
```

#### 💨 Ideal Gas
```
1. Select "Ideal Gas Behavior" from dropdown
2. Increase Temperature slider to 500 K
3. Observe velocity distribution shift and particles moving faster
4. Decrease Volume slider to compress the gas
5. Watch pressure increase and particles cluster
6. View the 3D particle cloud visualization
```

---

## 🔧 Troubleshooting

### "ModuleNotFoundError: No module named 'streamlit'"
```bash
pip install streamlit --upgrade
```

### "Port 8501 is already in use"
```bash
streamlit run app.py --server.port 8502
```

### Slow Performance
- Reduce "Number of Particles" in gas simulation
- Close other applications
- Use a modern browser (Chrome/Firefox/Safari)

### Charts Not Displaying
- Clear browser cache (Ctrl+Shift+Del)
- Refresh the page (F5)
- Try a different browser

---

## 💻 System Requirements

| Requirement | Minimum | Recommended |
|-------------|---------|-------------|
| Python | 3.8 | 3.10+ |
| RAM | 2 GB | 4+ GB |
| Disk Space | 100 MB | 500 MB |
| Browser | Chrome 80+ | Chrome/Firefox Latest |
| Internet | Not required (runs locally) | N/A |

---

## 📊 Physics Constants Used

The app uses real-world constants:

```
g (Earth gravity) = 9.81 m/s²
G (Gravitational constant) = 6.674 × 10⁻¹¹ N⋅m²/kg²
R (Gas constant) = 8.314 J/(mol⋅K)
k_B (Boltzmann constant) = 1.381 × 10⁻²³ J/K
```

---

## 🎓 Learning Resources

Each simulation includes:

1. **Theory & Formulas Tab**
   - Complete physics equations
   - Parameter definitions
   - Mathematical derivations

2. **Real-World Applications Tab**
   - Practical examples
   - Industry use cases
   - Everyday phenomena explained

3. **Interactive Breakdown Tab**
   - Step-by-step concept explanation
   - Visual demonstrations
   - Cause-and-effect relationships

---

## ⚙️ Advanced Customization

### Modifying Default Values
Edit the slider defaults in `app.py`:
```python
v0 = st.slider("Initial Velocity (m/s)", 1.0, 100.0, 50.0, 0.5)
#                                       min   max   default step
```

### Changing Colors
Update the CSS in the header section:
```python
:root {
    --primary-color: #2E86DE;      # Change this
    --secondary-color: #A23E48;    # And this
}
```

### Adding New Simulations
1. Create a new simulator class (inherit from `PhysicsSimulator`)
2. Add to sidebar selectbox options
3. Implement the physics logic
4. Add Plotly visualizations
5. Include theory tabs

---

## 🚀 Performance Optimization

For smoother performance:

```python
# Reduce time steps for faster simulation
simulator.simulate(..., time_steps=100)  # Default: 200

# Reduce particle count for gas simulation
num_particles = 500  # Default: 1000

# Clear session state periodically
if button_clicked:
    st.session_state.clear()
```

---

## 📱 Mobile & Tablet Support

PhysiVerse is responsive but works best on:
- ✅ Desktop browsers (recommended)
- ✅ Tablets in landscape mode
- ⚠️ Mobile phones (narrow viewport challenges)

For tablets, use landscape orientation for optimal layout.

---

## 🔒 Data Privacy

- ✅ All calculations run locally in your browser
- ✅ No data is sent to external servers
- ✅ No tracking or analytics
- ✅ No account creation required
- ✅ Completely offline capable

---

## 📈 Typical Use Cases

### Educational (School/University)
- Classroom demonstrations
- Virtual lab experiments
- Homework visualization
- Test preparation

### Self-Learning
- Interactive tutorials
- Concept exploration
- Real-time equation testing
- Physics visualization

### Professional
- Physics verification
- Calculation double-checking
- Teaching tool development
- Educational content creation

---

## 🎯 Next Steps

1. **Explore Simulations**: Try each of the 4 physics modules
2. **Adjust Parameters**: Change values and observe results
3. **Read Theory**: Expand educational tabs to understand formulas
4. **Compare Results**: Test different scenarios and compare outputs
5. **Share Learning**: Use for teaching or presentations

---

## 📞 Getting Help

### Common Questions

**Q: Can I run this offline?**
A: Yes! After initial download, the app runs completely offline.

**Q: Can I modify the code?**
A: Absolutely! It's open-source under MIT license.

**Q: Is it safe to use?**
A: Yes! No data leaves your computer. No malware or tracking.

**Q: Can I use this commercially?**
A: Yes, under MIT license terms.

---

## 🌟 Tips for Best Experience

1. **Use Full Screen** for best visualization
2. **Dark Room Lighting** - the dark theme is easier on eyes
3. **Read Theory First** before experimenting
4. **Adjust One Variable** at a time to see effects clearly
5. **Use Presets** (for orbital mechanics) to start with real scenarios
6. **Screenshot Results** for note-taking and sharing

---

**PhysiVerse v1.0** - Physics Learning Made Interactive 🌌

Enjoy exploring the universe of physics!