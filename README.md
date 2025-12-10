# 🔧 CNC Feeds & Speeds Calculator

A student-friendly, research-backed feeds and speeds calculator designed for the **Mason Innovation Exchange (MIX) Fabrication Lab** at George Mason University.

![Calculator Preview](https://img.shields.io/badge/Platform-Web-blue) ![License](https://img.shields.io/badge/License-Educational-green) ![Status](https://img.shields.io/badge/Status-Active-success)

---

## 📖 Overview

This calculator provides safe, conservative cutting parameters optimized for **educational CNC workshops** with mixed skill levels. It features a complete database of Whiteside router bits and research-based chipload values that prioritize student safety while maintaining productivity.

**Designed for:**
- Avid Desktop CNC Router
- VCarve Pro CAM Software
- Mach4 Controller
- Mixed skill level users (beginner to advanced)

---

## ✨ Key Features

### 🗂️ Complete Whiteside Bit Database
- **Upcut Spirals** - Solid carbide (1/8", 3/16", 1/4")
- **Downcut Spirals** - Solid carbide (1/8", 3/16", 1/4")
- **Compression Bits** - For clean top and bottom edges
- **Ball Nose Bits** - 3D carving and contouring
- **Tapered Ball Nose** - Detailed work and V-carving
- **Specialty Bits** - Bowl & tray, plunge roundover, carving liner

### 🪵 Material Support
- **Plywood** - Sheet goods and panels
- **Softwood** - Pine, cedar, and similar
- **Hardwood** - Cherry, maple, walnut
- **MDF** - Medium-density fiberboard
- **Acrylic** - Plastics and acrylics

### ⚙️ Operation Modes
- **Roughing** - Fast material removal (40-50% stepover)
- **Finishing** - Fine surface quality (10-15% stepover)
- **Pocketing** - Enclosed area clearing
- **Profiling** - Edge cutting and contouring

### 🛡️ Safety Features
- **Feed Rate Cap** - Maximum 200 IPM for safety
- **Conservative Plunge Rates** - Formula: `min(Feed × 0.3, 60 IPM)`
- **Aggressive Feed Warnings** - Alerts when speeds exceed 160 IPM
- **Student-Friendly Defaults** - Typical range: 130-150 IPM
- **Test Cut Reminders** - Built-in safety messaging

### 🎛️ Custom Calculator
Enter your preferred cutting parameters:
- **Depth per Pass** - Customize based on material condition
- **Stepover %** - Adjust for finish quality
- **Custom Chipload** - Override defaults for advanced users

The calculator automatically computes optimal feed and plunge rates while respecting all safety caps.

---

## 🚀 Getting Started

### Option 1: Use Online (Recommended)
Visit the live calculator:
```
https://[your-username].github.io/cnc-feeds-calculator/
```

### Option 2: Download and Run Locally
1. Download `index.html`
2. Open in any web browser
3. Works completely offline!

### Option 3: Install as Mobile App
**On iPhone/iPad:**
1. Open calculator in Safari
2. Tap Share button (square with arrow)
3. Select "Add to Home Screen"
4. Access like a native app!

**On Android:**
1. Open calculator in Chrome
2. Tap menu (three dots)
3. Select "Add to Home screen"
4. Launch from app drawer

---

## 📊 Technical Specifications

### Chipload Values (Research-Based)

All values optimized for **1/4" diameter, 2-flute bits at 18,000 RPM**:

| Material | Chipload (in/tooth) | Roughing Feed | Finishing Feed |
|----------|---------------------|---------------|----------------|
| **Plywood** | 0.0045 | 162 IPM | 108 IPM |
| **Softwood** | 0.0050 | 180 IPM* | 108 IPM |
| **Hardwood** | 0.0042 | 151 IPM | 108 IPM |
| **MDF** | 0.0055 | 198 IPM* | 126 IPM |
| **Acrylic** | 0.0030 | 108 IPM | 72 IPM |

*\*Marked as "Aggressive" - suitable for experienced users*

### Safety Parameters

| Parameter | Formula | Cap | Notes |
|-----------|---------|-----|-------|
| **Feed Rate** | RPM × Flutes × Chipload | 200 IPM | Capped for safety |
| **Plunge Rate** | min(Feed × 0.3, 60 IPM) | 60 IPM | Very conservative |
| **Depth per Pass** | Bit Diameter × Material Factor | Varies | Typically 0.125" for 1/4" bit in hardwood |
| **Stepover** | Operation-dependent | 50% max | 40-50% roughing, 10-15% finishing |

### Calculation Examples

**Example 1: Hardwood Pocketing**
- Material: Hardwood (Cherry)
- Bit: RU2075 (1/4" upcut spiral)
- Operation: Pocketing
- RPM: 18,000

**Results:**
- Feed Rate: 137 IPM
- Plunge Rate: 41 IPM
- Depth per Pass: 0.125"
- Stepover: 45%

**Example 2: MDF Roughing**
- Material: MDF
- Bit: RU2075 (1/4" upcut spiral)
- Operation: Roughing
- RPM: 18,000

**Results:**
- Feed Rate: 198 IPM (marked aggressive)
- Plunge Rate: 59 IPM
- Depth per Pass: 0.188"
- Stepover: 45%

---

## 🎓 Educational Use

This calculator is specifically designed for **workshop and classroom environments** where:
- Users have mixed experience levels
- Material quality varies
- Safety is the top priority
- Bit crashes must be minimized
- Machines are shared equipment

### For Instructors
- Conservative defaults reduce accidents
- Aggressive feeds are clearly marked
- Built-in safety reminders
- Encourages test cuts before final work

### For Students
- Clear, easy-to-understand interface
- No confusing technical jargon
- Visual warnings for risky parameters
- Learn proper feeds and speeds methodology

### For Advanced Users
- Custom calculator mode
- Ability to override all parameters
- Access to underlying formulas
- Can push speeds for production work

---

## 📐 Formulas Used

### Feed Rate
```
Feed Rate (IPM) = RPM × Number of Flutes × Chipload
```

### Plunge Rate
```
Plunge Rate (IPM) = min(Feed Rate × 0.3, 60)
```
Conservative 30% ratio with absolute 60 IPM cap prevents bit crashes.

### Depth per Pass
```
Depth per Pass = Bit Diameter × Material Factor
```
Material factors range from 0.2 to 1.0 depending on hardness and operation type.

### Stepover Percentage
```
Roughing: 40-50% of bit diameter
Finishing: 10-15% of bit diameter
Pocketing: 40-50% of bit diameter
Profiling: 100% (full width)
```

---

## ⚠️ Safety Guidelines

**Always follow these safety practices:**

1. ✅ **Make test cuts** in scrap material before cutting final pieces
2. ✅ **Start conservative** (130-150 IPM range) and increase gradually
3. ✅ **Listen for changes** in motor sound (squealing = too slow, harsh grinding = too fast)
4. ✅ **Watch for burning** - indicates feed too slow or RPM too high
5. ✅ **Check for chatter** - indicates feed too fast or insufficient rigidity
6. ✅ **Inspect bits regularly** - dull bits require slower feeds
7. ✅ **Secure workpieces properly** - use vacuum, clamps, or tabs
8. ✅ **Clear chips frequently** - packed chips cause heat and poor cuts

**When to reduce feeds/speeds:**
- Material is harder than expected
- Bit is becoming dull
- Surface finish is poor
- Machine vibration increases
- Burning or melting occurs
- Loud chattering or squealing

**When you can increase feeds/speeds:**
- Clean cuts with good chip formation
- No burning or discoloration
- Smooth machine operation
- Good surface finish
- Experienced operator

---

## 🔄 Updates and Maintenance

### Version History
- **v1.0** (December 2024) - Initial release
  - Complete Whiteside bit database
  - Research-based chipload values
  - Conservative safety parameters
  - Custom calculator mode

### Planned Features
- Metric unit support
- Additional bit manufacturers
- Cut time estimation
- Material cost calculator
- Print-friendly cut sheets

### Contributing
This calculator is maintained by the MIX Workshop. For suggestions or issues:
- Contact MIX staff directly
- Submit feedback via workshop
- Propose changes based on real-world testing

---

## 📱 Mobile Optimization

The calculator is fully responsive and works on:
- ✅ Desktop computers (Windows, Mac, Linux)
- ✅ Tablets (iPad, Android tablets)
- ✅ Smartphones (iPhone, Android)
- ✅ Works offline after initial load
- ✅ Touch-friendly interface
- ✅ No app store required

---

## 🛠️ Technical Details

**Built with:**
- Pure HTML5, CSS3, JavaScript
- No external dependencies
- No framework bloat
- Runs entirely in browser
- ~50KB total file size

**Browser Support:**
- Chrome/Edge (recommended)
- Safari (iOS/macOS)
- Firefox
- Any modern browser with JavaScript enabled

---

## 👨‍🏫 About

**Created by:** Tan  
**For:** Mason Innovation Exchange (MIX) Fabrication Lab  
**Institution:** George Mason University  
**Purpose:** Educational CNC machining with emphasis on safety

The MIX is a student-focused makerspace providing access to CNC routers, laser cutters, 3D printers, and other digital fabrication tools. This calculator supports our mission of safe, accessible, hands-on learning.

---

## 📄 License

**Free for educational use.**

You may:
- ✅ Use in educational settings
- ✅ Modify for your workshop needs
- ✅ Share with students and colleagues
- ✅ Deploy on your institution's servers

Please credit:
- Mason Innovation Exchange (MIX)
- Tan, Makerspace Associate
- George Mason University

---

## 📞 Contact & Support

**Questions about the calculator?**
- Visit the MIX Workshop during open hours
- Contact MIX staff via GMU channels

**Questions about CNC machining at GMU?**
- Attend MIX workshop training sessions
- Schedule one-on-one consultations
- Join the MIX student community

---

## 🙏 Acknowledgments

This calculator incorporates research and best practices from:
- Whiteside Machine Company specifications
- Amana Tool chipload charts
- CNC community forums (CNCZone, Practical Machinist)
- Real-world testing at the MIX Workshop
- Feedback from students and workshop staff

Special thanks to the MIX team and GMU students who tested and provided feedback during development.

---

## 🔗 Resources

**Learn More:**
- [Whiteside Router Bits](https://www.whitesiderouterbits.com/)
- [VCarve Pro Documentation](https://www.vectric.com/products/vcarve-pro)
- [CNC Basics Guide](https://www.cnccookbook.com/)

**MIX Workshop:**
- Visit us at George Mason University
- Check our website for hours and training schedules
- Follow us on social media for updates

---

**Remember: These are recommendation settings. Always make test cuts in scrap material before cutting your final piece!**

---

Made with ❤️ for the maker community at GMU
