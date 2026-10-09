Act as a senior Three.js/WebGL engineer, physically based rendering (PBR) specialist, luxury product visualization artist, and creative frontend developer. Your task is to diagnose and repair the existing Dar Saifa perfume website's 3D bottle experience, making it visually premium, physically believable, smooth, and performant.

IMPORTANT PROJECT RULES
- Work inside the existing repository. Inspect the current code and assets before changing anything.
- Preserve the current website, routing, typography, responsive layout, interactions, and established brand identity.
- The cinematic 3D experience belongs ONLY on the "About Our House" page. Do not add a 3D canvas, heavy animation loop, or duplicate bottle scene to other routes.
- Brand palette: deep burgundy #3D0F14, dark espresso #241915, antique gold #B8862B, warm ivory #F2EDE3. The perfume liquid must complement this palette.
- Do not replace the existing bottle model with generic primitives or a generic perfume model. Preserve the Dar Saifa bottle’s identity, silhouette, cap, label, and proportions unless a specific change is necessary and justified.
- Do not claim a visual issue is fixed unless you have implemented the change and checked it using available tools. Be explicit about anything that could not be verified.
- Avoid an unnecessary full rewrite. Prefer targeted, reversible improvements to the current architecture.

PHASE 1 — AUDIT THE EXISTING PROJECT
Before editing:
1. Inspect package.json, the framework, the existing 3D renderer, scene components, model and texture assets, material definitions, lighting, camera, scroll logic, animation libraries, and CSS.
2. Identify whether the project uses vanilla Three.js, React Three Fiber (R3F), Drei, GSAP, ScrollTrigger, Lenis, Theatre.js, or other relevant tools.
3. Inspect the actual bottle model and available textures. Determine whether the model is GLB/GLTF, procedural geometry, or another format.
4. Locate duplicate bottle meshes, transparent objects, mirror planes, light-shaft geometry, post-processing passes, scroll handlers, and render loops.
5. Identify the cause of each problem below. Distinguish confirmed causes from hypotheses.
6. Check existing Claude Code skills and plugins. If available, use relevant Three.js/R3F, WebGL debugging, GSAP ScrollTrigger, and frontend-design skills. Prefer the existing project stack. Do not install duplicate libraries or run unfamiliar install commands without explaining why and checking compatibility.
7. Give me a short prioritized diagnosis, then proceed with the implementation unless a destructive change or missing asset requires my approval.

PHASE 2 — FIX THE BOTTLE MATERIALS AND GLASS
The current glass looks like a murky brown-grey haze. Make it resemble premium real perfume glass.

- Use physically based materials appropriate to the existing geometry and renderer.
- For Three.js MeshPhysicalMaterial, investigate transmission, thickness, IOR, roughness, attenuationColor, attenuationDistance, and envMapIntensity where supported and appropriate.
- Use physically plausible values as a starting point, then tune them against the actual scene. Do not blindly maximize transmission or thickness.
- Provide real environmental reflections using a suitable HDR environment or studio environment setup. Use a compatible PMREM/environment workflow for the installed Three.js version.
- Make the front and rear glass edges readable through reflections and refraction while keeping the interior liquid visible.
- Avoid turning the glass into opaque dark plastic, flat transparent surfaces, or a uniformly tinted shell.
- Account for transparent-object sorting and overlapping front/back glass surfaces. Do not apply arbitrary renderOrder values without understanding the rendering problem.
- Inspect the bottle mesh normals, face orientation, thickness, and material assignment. Correct the geometry if the model itself is causing the murky appearance.
- Keep the hero bottle visually clear against the burgundy environment.

LIQUID — REAL DEPTH, NOT A FLAT ORANGE PATCH
- Replace the current off-palette orange appearance with deep amber, cognac, or copper-amber tones that harmonize with burgundy, espresso, antique gold, and ivory.
- Make the liquid volume look three-dimensional, with believable depth, absorption, and light interaction.
- Inspect the actual liquid geometry. The liquid must sit inside the bottle and follow the intended fill level.
- Create a subtle, physically believable meniscus or curved liquid surface if the geometry and rendering approach support it.
- Ensure the liquid does not appear as a sticker, floating flat plane, or glowing orange block.
- Tune liquid color and transmission/opacity according to the selected rendering approach. Do not assume the same material parameters work for both a solid liquid volume and a thin surface.
- Prevent visible intersections, leakage through the glass, and incorrect layering.
- Keep the result elegant and restrained rather than overly saturated or artificially emissive.

LABEL, LOGO, AND MONOGRAM
- Make "DAR SAFIA" and the monogram sharp, legible, correctly positioned, and consistent with the original brand artwork.
- Inspect the source texture resolution, UV mapping, texture color space, filtering, anisotropy, and mipmap settings.
- Prefer the original high-resolution logo/label artwork if available. Do not redraw or invent a new logo.
- If needed, create a clean, high-resolution label texture or use an appropriate geometry/decal solution compatible with the current project.
- Prevent stretching, blurry text, aliasing, shimmering, and label intersections with the bottle.
- Verify the result at the actual on-screen size and at high-DPI display settings.

BLACK SIDE BOTTLES
- Preserve the intended dark design, but reveal their contours with subtle environment reflections, carefully controlled roughness, and studio rim lighting.
- Avoid pure-black surfaces with no visible shape.
- Keep the hero bottle visually dominant.
- Inspect their individual scales and spacing; use design-intended proportions rather than blindly scaling copies of the hero bottle.
- Ensure the headline remains legible and does not collide with the left bottle.

PHASE 3 — CORRECT THE GEOMETRY
- Inspect the octagonal cap for flat shading, insufficient segments, poor normals, or visibly faceted surfaces.
- Where appropriate, improve segment density and compute correct vertex normals. If the cap is intentionally faceted, preserve that design language while improving the shading.
- Preserve crisp, intentional edges where the actual design calls for them; do not indiscriminately smooth everything.
- Check bevels, silhouette, bottle shoulders, base thickness, cap alignment, and overall proportions.
- Inspect the mesh hierarchy and scene graph for duplicate bottle geometry or accidental transparent duplicates.
- Diagnose the faint ghost bottle visible in the light column. Check duplicate meshes, mirrors, overlapping transparent surfaces, reflection artifacts, and z-fighting before choosing a fix.
- Remove only confirmed unintended geometry. Do not remove deliberate artistic elements.

PHASE 4 — BUILD A PREMIUM STUDIO LIGHTING SETUP
Create a controlled luxury fragrance campaign look, not a collection of harsh white streaks and glowing planes.

- Use a deliberate studio-lighting hierarchy: key light, fill light, rim lights, and large soft reflection sources.
- Shape reflections to reveal the bottle's silhouette, glass thickness, shoulders, cap, and base.
- Avoid a distracting white stripe running through the logo or the center of the bottle.
- Use environment-map reflections that complement the direct lighting.
- Ground each bottle with a believable contact shadow on the pedestal.
- Avoid fake hovering, excessively blurred shadows, and shadows that contradict the light direction.
- Reduce the gold pedestal's excessive bloom. Use a restrained effect and an appropriate luminance threshold or selective bloom approach if supported by the existing post-processing setup.
- Make the gold edge elegant and defined instead of letting the glow bleed into the bottle base.
- Replace hard-edged vertical light-shaft planes with soft gradients, suitable alpha falloff, and restrained blending. Ensure the shafts blend into the scene rather than looking like flat cards.
- Check the light shafts for unwanted interactions with transparent glass and prevent them from creating ghost silhouettes.
- Address banding on the burgundy wall through appropriate texture precision, color management, subtle dither/noise where appropriate, or a better gradient implementation. Avoid visible grain.
- Keep the background cinematic but subordinate to the product.

PHASE 5 — COLOR MANAGEMENT AND POST-PROCESSING
- Inspect the installed Three.js version and the current renderer configuration before changing APIs.
- Use the appropriate output color space, normally SRGBColorSpace for display output, and a consistent color-management pipeline.
- Evaluate ACESFilmicToneMapping or another suitable tone-mapping approach against the existing art direction. Use it only after checking the current renderer and post-processing pipeline; avoid applying tone mapping twice.
- Tune exposure, tone mapping, environment intensity, and post-processing together.
- Preserve deep burgundy shadows, natural amber liquid, antique gold highlights, and warm ivory details.
- Avoid clipped white reflections, muddy blacks, oversaturated orange, washed-out gold, and crushed bottle detail.
- Check that texture color spaces are correct: color/albedo textures should use the appropriate sRGB handling, while non-color data maps should use the appropriate non-color space.
- Verify the final rendered colors rather than assuming the hexadecimal brand palette will look identical under every lighting condition.

PHASE 6 — REBUILD THE SCROLL EXPERIENCE
The current bottle movement appears tied to raw page scroll, causing jitter, drifting, and motion when the hero is off-screen.

- If the project already uses GSAP and ScrollTrigger, prefer one well-coordinated timeline with a section-specific ScrollTrigger rather than multiple competing scroll listeners.
- If it uses React Three Fiber, preserve the existing R3F architecture and integrate animation without forcing unnecessary React re-renders.
- Do not add R3F, GSAP, Lenis, Theatre.js, or another framework merely because it is available. Introduce a dependency only when it solves a real problem and is compatible with the project.
- Scope scroll progress to the About Our House hero section, with clear start/end points. Do not map the entire page's scroll position directly to the bottle transform.
- Use a pinned or sticky storytelling section only if it fits the existing layout and improves the experience. Preserve natural scrolling elsewhere.
- Animate the camera and bottle with intention. Use a restrained rotation of approximately 30–60 degrees only if appropriate to the bottle's orientation and design, with a subtle lift or camera transition.
- Keep the logo readable at important moments. Avoid uncontrolled movement on every axis.
- Coordinate the headline, side bottles, hero bottle, pedestal, and camera so they do not overlap.
- Add controlled damping or smoothing to the scroll-driven values. Avoid lag that makes the scene feel detached from scrolling.
- Ensure forward scrolling, reverse scrolling, fast wheel movement, touch scrolling, refreshes, and resizing all behave consistently.
- Use the correct lifecycle cleanup for GSAP timelines, ScrollTriggers, observers, animation callbacks, and event listeners. In React, account for mounting/unmounting and Strict Mode.
- Ensure ScrollTrigger refreshes when necessary after fonts, images, model assets, or layout changes. Avoid excessive refresh calls.
- Disable or simplify nonessential scroll choreography when prefers-reduced-motion is enabled.
- Do not allow the bottle to move when this hero section is off-screen.
- Do not break browser history, page navigation, or other site animations.

PHASE 7 — PERFORMANCE AND RESPONSIVE BEHAVIOR
Target a smooth, stable experience on modern desktop and acceptable performance on mobile.

- Profile before making major performance compromises.
- If using R3F, inspect Canvas settings and use an appropriate DPR range, such as [1, 1.5] or [1, 2], only after testing real devices.
- If using vanilla Three.js, apply an equivalent sensible pixel-ratio cap.
- Reduce particle count, expensive transmission layers, unnecessary transparent meshes, and costly post-processing on small or slower devices.
- Avoid rendering continuously when the scene is static. Use demand rendering or a visibility-aware render loop when compatible with the existing architecture.
- Use IntersectionObserver or a suitable equivalent to suspend nonessential rendering when the scene is off-screen. Ensure the scene resumes correctly when visible.
- Do not break GSAP or other animation updates when switching to demand rendering; explicitly request frames when needed.
- Reuse geometries, materials, textures, and render resources. Dispose of resources correctly when no longer needed.
- Prevent memory leaks, duplicate animation loops, repeated texture loads, unnecessary state updates, and repeated compilation.
- Optimize model and texture assets when needed. Prefer a properly optimized GLB/glTF asset; use mesh compression or texture compression only when compatible with the deployment pipeline and visual quality requirements.
- Lazy-load the 3D scene if it improves initial page loading without creating a poor experience.
- Add a graceful static poster or non-WebGL fallback for unsupported devices or rendering failures.
- Keep a high-quality desktop experience while scaling back expensive effects on mobile.
- Test the actual narrow-screen composition: heading, side bottles, hero bottle, pedestal, and CTA must not overlap or become unreadable.

PHASE 8 — SKILLS, TOOLS, AND LIBRARY CHOICES
Use existing project dependencies and installed Claude Code skills first.

Relevant tools to evaluate:
- Three.js for rendering and WebGL.
- React Three Fiber and Drei only if the project uses React and these fit the existing architecture.
- GSAP ScrollTrigger for section-scoped, coordinated scroll animation.
- Theatre.js only if visual timeline authoring materially helps this project.
- Blender for source-model geometry and material preparation, if the required source assets are available.
- glTF/GLB and appropriate optimization tooling for production model delivery.
- Browser developer tools and available screenshot/browser automation for visual and performance checks.

Check for relevant Claude Code skills, including:
- Three.js / WebGL skills.
- React Three Fiber skills, if applicable.
- Three.js debugging and performance skills.
- GSAP ScrollTrigger skills.
- Frontend design skills.

If these skills are not installed, do not pretend to have used them. Tell me which specific skills would help and provide the appropriate installation instructions separately. Review third-party skill source and commands before execution. Do not blindly install every suggested plugin or change package versions without checking compatibility.

Use current official documentation as the source of truth for APIs, particularly when working with version-sensitive Three.js, R3F, and GSAP features. Community skills are useful guidance, not authoritative documentation.

PHASE 9 — VERIFY THE RESULT
After implementation:
1. Run the project's existing lint, type-check, build, and relevant tests where available.
2. Inspect browser console errors, shader errors, missing assets, and WebGL warnings.
3. Use available browser or screenshot tools to inspect the actual About Our House page at desktop and mobile widths.
4. Inspect the bottle from multiple angles and at the intended final camera position. Verify glass transparency, liquid depth, label readability, cap shading, side-bottle reflections, contact shadows, and bloom.
5. Test the entire scroll timeline, including reverse scrolling, fast scrolling, resizing, and leaving/re-entering the section.
6. Verify that the 3D scene and animation do not run on unrelated pages.
7. Verify reduced-motion behavior and the fallback experience.
8. If automated visual inspection or real-device performance testing is unavailable, state that limitation honestly rather than claiming the visual result is perfect.
9. Avoid changing unrelated website functionality.

ACCEPTANCE CRITERIA
- Glass looks transparent and reflective, with believable thickness and visible bottle contents.
- Liquid has rich amber/copper depth and a convincing fill surface.
- DAR SAFIA branding is crisp and correctly mapped.
- Cap geometry and shading look intentional and premium.
- Dark side bottles have controlled reflections and readable silhouettes.
- No unintended duplicate or ghost bottle is visible.
- Bottles sit naturally on the pedestal with credible contact shadows.
- Bloom and light shafts are restrained and integrated.
- Burgundy background gradients are smooth.
- Color management is consistent and highlights retain detail.
- Scroll animation is deliberate, section-scoped, smooth, reversible, and responsive.
- Headline and bottle composition remain readable without collisions.
- Off-screen and mobile performance are handled deliberately.
- No unnecessary architectural rewrite or unrelated regression is introduced.

FINAL REPORT
When finished, provide:
- The confirmed root cause of each major issue.
- The files changed and what each change accomplishes.
- Any assets created, replaced, or still needed.
- Any dependencies added or avoided, with reasons.
- The verification performed and its actual results.
- Remaining limitations, trade-offs, or issues that require a human visual review.

Start with the audit. Fix the highest-impact visual problems first, then tune animation and performance. Do not merely describe proposed fixes: implement the appropriate changes in the existing project and verify what you can.
