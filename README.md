# SolidLab: An Interactive Mechanics of Solids Simulator

**Course:** Mechanics of Solids · **Institute:** IIT Hyderabad · **Submitted:** November 2026
**Project author:** Midathana Lohith

SolidLab is a visual, interactive tool for first-time learners of Mechanics of Solids. Users can change loads, dimensions, and materials, then immediately see how the calculated stress, strain, deflection, and illustrative failure response changes.

## Open SolidLab

**Live application:** [https://lohith777-me.github.io/solidlab-mechanics-of-solids/](https://lohith777-me.github.io/solidlab-mechanics-of-solids/)

The application is the single-file [`index.html`](index.html). Open it in a current desktop, tablet, or mobile browser to run it locally and offline; no installation, build step, external library, or network connection is required.

## What is included

| Module | What it demonstrates | Key relationships |
|---|---|---|
| Axial loading | Stress and extension of a bar in tension or compression | $\sigma=P/A$, $\epsilon=\sigma/E$, $\Delta L=\epsilon L$ |
| Shaft torsion | Shear stress and angle of twist in a solid circular shaft | $\tau_{\max}=Tc/J$, $\theta=TL/(JG)$, $J=\pi d^4/32$ |
| Beam bending | Bending stress and deflection of a simply supported beam with a point load | $\sigma_{\max}=M(h/2)/I$, $\Delta y=Pa^2b^2/(3EIL)$ |
| SFD / BMD | Shear-force and bending-moment diagrams for point and uniformly distributed loads | $dV/dx=-w$, $dM/dx=V$ |
| Mohr's circle | 2D plane-stress transformation, principal stresses and angles, and original / rotated stress elements | $\sigma_{1,2}=\sigma_{\mathrm{avg}}\pm R$, $\tan 2\theta_p=2\tau_{xy}/(\sigma_x-\sigma_y)$ |
| Stress–strain curve | Elastic response, yield, strain hardening, necking, and fracture | $\sigma=E\epsilon$ in the elastic range |
| Universal testing machine | Virtual tensile test with adjustable gauge length and specimen area | $\sigma=F/A_0$, $\epsilon=\Delta L/L_0$ |

Material choices include structural steel, aluminum alloy, titanium alloy, ASTM A36 steel, ASTM A572 Grade 50 steel, 6061-T6 aluminum, Type 304 stainless steel, and user-defined custom properties.

## Learning and interaction features

- Beginner guides explain what each model shows, suggest an interaction, and point out what to notice.
- Interactive 3D-style model views can be rotated by dragging and restored with **Reset view**.
- Inputs, results, formula summaries, numbered calculation steps, and symbol explanations update together.
- Stress shading helps identify higher-demand regions in the member and beam views.
- Axial, torsion, and Mohr's-circle modules compare the calculated demand with an illustrative von Mises failure assessment. Stress–strain and UTM views provide near-necking / fracture indications and tensile fracture animations.
- Mohr's-circle tools include example stress states (simple tension, pure shear, equal biaxial stress, and tension with compression), principal-plane and maximum-shear shortcuts, and controls for showing or hiding stress-tensor components.
- SFD/BMD setup supports simply supported or cantilever beams with a point load or a full-span uniform distributed load.
- SI / US customary display units and light / dark themes are available; the selected theme is remembered.
- Export results as CSV or PDF, print a worked solution, or copy a link that retains the current inputs.
- Controls carry accessibility labels and the layout supports laptop, tablet, and phone screens.

## Tools and method

SolidLab is written in plain HTML, CSS, and JavaScript. The 3D-style views use custom projection and rotation code drawn on an HTML canvas; the Mohr's-circle and engineering diagrams use web graphics. No external runtime libraries are required.

Each module follows the same cycle: controls collect inputs, the relevant mechanics relationships are evaluated, then the calculations, diagrams, and visual model are redrawn. The calculations use a consistent internal SI reference basis while the interface displays supported values in the selected unit system. The worked steps show the formula and selected-value substitutions so results can be checked by hand.

Development included iterations to enlarge and improve the Mohr's-circle view, correct beam-bending and SFD/BMD behavior, and polish fracture animations.

## Learning outcomes

Working through the project helps connect course theory to physical behavior, including:

- How axial stress depends on load and area.
- Why circular-shaft torsional resistance depends strongly on diameter through $J\propto d^4$.
- How load and support conditions shape beam shear, bending moment, and deflection.
- How principal stresses follow from a plane-stress state and Mohr's circle.
- How a ductile metal progresses from elastic loading toward yield, necking, and fracture.
- How a tensile test's force and extension relate to engineering stress and strain.

## Limitations and responsible use

SolidLab is a teaching aid, not a design or safety tool. Its calculations are analytical idealizations, not finite-element analyses or certified test software. Most modules assume linear-elastic behavior, simple loading and support cases, and representative material properties. Material data vary with grade, processing, temperature, orientation, specimen geometry, and test conditions.

Stress limits and fracture points are teaching estimates, not predictions for real components. Deformation and fracture animations are visual demonstrations; they do not model or certify actual failure. The UTM visualization is not calibrated and is not a standards-compliant test machine. Independently verify all assumptions, data, and calculations before applying them to real systems.

## Future work

Potential extensions include more support and loading conditions and a column-buckling module.

## Acknowledgement of AI use

The project author reports using Claude, an AI assistant by Anthropic, to help write and improve parts of the code. The project idea, topic selection, simulator testing, and final review are attributed to the author, who takes responsibility for the submitted content.

## License

No license is specified. All rights reserved unless the author grants permission.
