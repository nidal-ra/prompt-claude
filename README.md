DAR SAIFA — MASTER WEBSITE DESIGN & 3D EXPERIENCE

ROLE
Act as a senior frontend engineer, creative developer, Three.js specialist, React Three Fiber engineer, GSAP animation specialist, luxury art director, UI/UX designer, accessibility specialist, and design systems architect. Work directly inside my existing repository using Claude Code. Implement the changes, inspect the actual results, and verify them.

==================================================
MASTER RULE: TWO SCOPES, TWO DIFFERENT RESPONSIBILITIES
==================================================

This project has TWO separate scopes.

SCOPE A — ENTIRE WEBSITE:
Apply the official Dar Saifa brand palette and a cohesive, professional design system to EVERY existing website page, route, layout, template, and reusable component.

SCOPE B — ONLY THE “ABOUT OUR HOUSE” PAGE:
Create the premium cinematic, scroll-driven 3D perfume experience described in this prompt ONLY on the existing “About Our House” page.

These scopes must not be confused.

The brand palette and consistent design system apply throughout the website. The intensive Three.js scene, persistent 3D bottle, cinematic camera choreography, chapter-based scroll animation, and related immersive effects belong ONLY to the “About Our House” page.

Do not turn every page into a 3D experience. Do not add the 3D bottle canvas, chapter animations, or immersive scroll locking to the homepage, product pages, collection pages, cart, checkout, or any other page unless that functionality already exists and must be preserved.

The “About Our House” page must still use the same global design tokens and brand identity as the rest of the website.

If the current route or page label differs slightly, inspect the project and identify the page corresponding to “About Our House.” Do not create a duplicate page simply because its route has a different name.

==================================================
PART 1 — SCOPE A: APPLY THE BRAND DESIGN SYSTEM TO THE ENTIRE WEBSITE
==================================================

1. ROLE AND OBJECTIVE

Implement the official Dar Saifa color palette and a consistent luxury visual identity throughout the entire existing website.

This is a complete website-wide design-system task, not a homepage-only color change.

Inspect the existing site and update the frontend systematically. Preserve its established identity, authentic assets, page content, working features, and purchasing functionality.

Do not rebuild the entire website from scratch merely to introduce the palette.

2. DISCOVERY BEFORE CHANGES

Before editing:

- Inspect the repository structure, framework, routing system, page definitions, layouts, templates, and reusable components.
- Read CLAUDE.md, relevant project instructions, package.json, and configuration files.
- Identify every public-facing page and route, including nested and dynamic routes, product detail pages, collections, landing pages, informational pages, forms, account pages, cart, checkout, and other relevant pages that actually exist.
- Identify the current styling architecture: CSS variables, Tailwind, Sass, CSS modules, styled-components, or another system.
- Locate existing brand assets, fonts, logos, product photography, icons, illustrations, and animations.
- Identify existing dependencies and their versions before installing or replacing anything.
- Inspect existing page-specific styles, inline styles, legacy colors, component variants, and third-party components.
- Determine how the current “About Our House” page is implemented and identify its actual route.
- Identify whether the project already contains the Dar Saifa bottle model, textures, materials, logo, label, cap, liquid, and 3D scene.

Create an internal checklist of all discovered pages, shared components, and relevant visual assets before making changes.

3. DISCOVER AVAILABLE SKILLS AND TOOLS

Inspect the skills, plugins, MCP servers, browser automation, visual testing, and other capabilities genuinely available in the current Claude Code environment.

Prioritize relevant capabilities such as:

- Frontend design and implementation.
- UI/UX design.
- Design systems.
- Three.js and React Three Fiber.
- GSAP and ScrollTrigger.
- Responsive design.
- Accessibility.
- Browser automation and screenshot-based visual verification.
- Performance profiling.

Read applicable skill instructions before using them.

Use relevant capabilities that are actually available. Do not pretend a skill or plugin is installed when it is not. Do not assume ChatGPT plugins are automatically available in Claude Code.

Do not install unnecessary tools or make consequential environment changes without appropriate authorization.

4. OFFICIAL DAR SAIFA COLOR PALETTE

The following colors are the official brand colors and must be used consistently throughout the entire website.

PRIMARY COLOR:
#3D0F14 — Deep burgundy.

SECONDARY COLORS:
#241915 — Dark espresso.
#B8862B — Antique gold.
#F2EDE3 — Warm ivory.

Color roles:

#3D0F14 — PRIMARY BRAND COLOR
Use as the dominant brand color across appropriate backgrounds, important sections, primary buttons, navigation accents, active states, and key visual elements.

#241915 — DARK SUPPORTING COLOR
Use for dark sections, supporting backgrounds, typography, deep contrast, and elegant visual transitions.

#B8862B — ANTIQUE GOLD ACCENT
Use selectively for premium highlights, refined borders, icons, active indicators, subtle decorative details, and carefully chosen interactive states.

#F2EDE3 — WARM IVORY NEUTRAL
Use for light backgrounds, readable content sections, cards, whitespace, and text on dark surfaces when contrast is sufficient.

Additional colors are permitted only when necessary and must harmonize with this palette. Prefer derived tints, shades, muted neutrals, and related colors.

Maintain appropriate semantic colors for error, warning, and success states. Do not replace meaningful status colors with brand colors when doing so would make the interface confusing.

Do not use gold indiscriminately. In particular, avoid antique gold as small text on warm ivory if the contrast is insufficient.

The site should feel premium, sophisticated, cohesive, and intentionally art-directed rather than uniformly burgundy.

5. CENTRALIZED DESIGN SYSTEM

Create or update centralized design tokens using the conventions of the existing project.

Establish appropriate variables or tokens for:

- Primary brand color.
- Secondary dark color.
- Gold accent.
- Warm ivory.
- Supporting shades and tints.
- Page backgrounds and section backgrounds.
- Primary and secondary text.
- Muted text.
- Borders and dividers.
- Cards and overlays.
- Button variants.
- Input backgrounds and borders.
- Focus rings.
- Hover, active, disabled, error, and success states.
- Shadows and subtle decorative effects where appropriate.

Use existing architecture where possible. For example, update CSS custom properties or the existing Tailwind configuration rather than introducing a competing styling system.

Use shared tokens instead of scattered, inconsistent hardcoded colors.

Do not replace existing fonts or typography without a good design reason. Preserve authentic Dar Saifa branding and any existing premium typography.

6. APPLY THE SYSTEM TO EVERY PAGE

Audit every discovered page individually.

Review and update, where necessary:

- Header and navigation.
- Footer.
- Page backgrounds and section transitions.
- Headings, paragraphs, links, and text contrast.
- Primary and secondary buttons.
- Product cards and collection grids.
- Product images and image backgrounds.
- Product detail pages and product galleries.
- Price displays, badges, and purchase CTAs.
- Cart and checkout.
- Forms, inputs, validation states, and dialogs.
- Breadcrumbs, dropdowns, menus, and overlays.
- Testimonials, editorial sections, and informational content.
- Tables, pricing blocks, banners, and promotional sections.
- Icons, SVGs, illustrations, and decorative elements.
- Hover, focus, active, disabled, loading, error, and success states.
- Mobile and tablet layouts.
- Page-specific components and legacy color overrides.

Do not assume that updating the header or global CSS automatically completes the work. Check each page for unique styles, inline declarations, overrides, and third-party components.

Where shared components are used across many pages, update them centrally when appropriate and verify that the changes do not break any page.

7. CONSISTENT LUXURY VISUAL DESIGN

The entire website should feel like one coherent luxury perfume brand.

Maintain:

- Clear visual hierarchy.
- Consistent typography and spacing.
- Balanced layouts and whitespace.
- Purposeful color contrast.
- Consistent buttons, borders, radii, and shadows.
- Elegant imagery and restrained decorative effects.
- Cohesive page transitions and component styles.
- Clear product presentation and purchase actions.
- Consistent responsive behavior.

Do not make every page identical. Each page should retain its individual purpose while belonging to the same design system.

Do not apply excessive animation, decorative effects, or 3D elements globally merely to make the site look premium.

8. RESPONSIVENESS AND ACCESSIBILITY

Check the brand system across desktop, tablet, and mobile.

Verify responsive navigation, readable text, image behavior, layout spacing, form usability, keyboard focus, and interactive states.

Ensure adequate color contrast, especially for gold accents and small text.

Respect reduced-motion preferences where animation is used.

Preserve semantic HTML, accessibility attributes, and keyboard usability.

9. SCOPE A ACCEPTANCE CRITERIA

Scope A is complete only when:

- Every discovered page and route has been reviewed.
- Every relevant shared component has been reviewed.
- The official palette is applied consistently across the entire website.
- Conflicting legacy colors have been addressed.
- Shared tokens are used wherever appropriate.
- Responsive layouts and accessibility have been checked to the extent possible.
- Existing content, routes, product information, cart, checkout, and integrations remain intact.
- The intensive cinematic 3D experience has not accidentally spread to unrelated pages.
- The final report distinguishes actual implementation from checks that could not be performed.

==================================================
PART 2 — SCOPE B: REBUILD THE 3D EXPERIENCE ONLY ON “ABOUT OUR HOUSE”
==================================================

10. OBJECTIVE

Create a completely new, premium, cinematic 3D experience for the Dar Saifa “About Our House” page.

The priority is an exceptionally polished, scroll-driven 3D experience with sophisticated camera movement, realistic product rendering, a convincing perfume bottle, and a rich atmospheric introduction.

The result should feel like an award-winning luxury perfume campaign, not a generic Three.js demo.

The bottle must be the main visual character of this page.

The three most important goals are:

1. A genuinely cinematic, exceptionally smooth, scroll-driven 3D animation.
2. A realistic, premium-looking bottle with defined glass edges, convincing liquid, and sharp, authentic branding.
3. A rich, atmospheric introduction that communicates luxury rather than displaying a bottle in an empty environment.

Do not settle for a basic model rotation or a bottle that simply follows the scrollbar.

You may replace the existing 3D scene, camera, lighting, animation controller, materials, and component structure on this page if doing so improves the result.

Do not rebuild unrelated pages as part of this work.

11. INSPECT THE EXISTING ABOUT PAGE AND ASSETS

Before implementing the new experience:

- Identify the exact “About Our House” route and its current page component.
- Inspect the current layout and all existing page content.
- Locate the actual Dar Saifa perfume bottle model.
- Determine whether it is GLB, GLTF, custom geometry, or another format.
- Locate the real Dar Saifa logo, label, textures, bottle materials, cap, and liquid geometry.
- Inspect the existing camera, lights, background, scroll animation, and material assignments.
- Check existing versions of Three.js, React Three Fiber, @react-three/drei, GSAP, ScrollTrigger, and Lenis.
- Determine which assets can be reused and which need improvement.

Preserve authentic brand assets and the recognizable bottle design. Do not substitute generic perfume bottles or invented logos when authentic assets exist.

Use the actual brand story, fragrance information, ingredients, imagery, and text available in the project. Do not invent brand history, product claims, fragrance notes, awards, or other factual information.

If important information is absent, design a beautiful layout around the verified content that exists instead of fabricating facts.

12. TECHNOLOGY STACK

Prefer the following stack when compatible with the existing application:

- React.
- Three.js.
- React Three Fiber.
- @react-three/drei.
- GSAP.
- GSAP ScrollTrigger.
- Lenis for smooth scrolling.

Use the existing project architecture and dependency versions wherever possible.

Install or upgrade dependencies only when necessary, and avoid incompatible versions.

If the project does not use React, do not force a complete framework migration merely to use this preferred stack. Choose a technically appropriate solution for the existing architecture.

The implementation must be maintainable, responsive, and performant.

13. ART DIRECTION — LUXURY PERFUME

The “About Our House” experience must communicate:

- Luxury.
- Elegance.
- Sensuality.
- Sophistication.
- Craftsmanship.
- Depth.
- Cinematic quality.

Use premium fragrance advertising and professional studio product photography as artistic references.

Avoid:

- Generic futuristic environments.
- Neon effects.
- Excessive particles.
- Overwhelming bloom.
- Cheap-looking gradients.
- Uncontrolled reflections.
- Excessive camera movement.
- Constant exaggerated rotation.
- Generic stock-looking 3D compositions.
- Empty backgrounds that make the bottle look unfinished.

Use negative space intentionally, but do not confuse minimalism with an empty scene.

Every visual element must support the bottle, the brand, or the storytelling.

The official burgundy, espresso, antique gold, and warm ivory palette must guide the scene's visual direction. You may use carefully controlled light, shadow, transparency, and atmospheric shades that harmonize with these colors.

Do not turn the 3D scene into a flat collection of brand-colored shapes. It must feel physically rich and cinematic.

14. THE BOTTLE — PRIMARY VISUAL ASSET

Inspect the actual model before deciding how to improve it.

If the geometry is insufficient, improve or recreate the necessary parts while preserving the authentic silhouette, proportions, and construction.

GLASS GEOMETRY AND EDGES

Improve where needed:

- Rounded or beveled edges.
- Edge highlights.
- Glass thickness.
- Silhouette definition.
- Surface transitions.
- Reflections along the perimeter.
- Internal depth and optical appearance.

Avoid razor-sharp, mathematically perfect edges that make the bottle appear artificial.

If the model lacks sufficient geometry, add appropriate bevels or rebuild the relevant geometry. Materials alone cannot compensate for fundamentally poor geometry.

The bottle must retain a convincing silhouette from every important camera angle.

GLASS MATERIALS

Create a physically convincing glass material with appropriate:

- Transparency.
- Transmission.
- Refraction.
- Index of refraction.
- Roughness.
- Specular response.
- Thickness.
- Environment reflections.

Use physically based rendering where appropriate.

Tune the material for the actual model, lighting, and background. Do not blindly maximize transmission or transparency.

The outer glass must remain visually distinguishable from the liquid inside.

The bottle should look like thick, premium perfume glass, not a transparent plastic container.

Ensure that the glass remains readable against both light and dark sections of the environment.

BOTTLE CAP

Improve the cap's geometry and materials where necessary.

Give it convincing proportions, surface characteristics, reflections, and contact with the bottle.

Avoid making it look like an unmodified primitive placed on top.

Use subtle material variation and controlled highlights to communicate quality.

15. REALISTIC PERFUME LIQUID

The liquid must be a convincing three-dimensional volume, not a flat colored rectangle or a solid shape that fills the entire bottle.

Create an appropriate liquid volume with:

- A clearly visible liquid level.
- Correctly chosen perfume coloration based on available product references.
- Transparency and depth.
- Subtle reflections.
- Convincing interaction with the surrounding glass.
- An air space above the liquid where consistent with the real bottle.
- A subtle meniscus where appropriate.

Keep the liquid correctly positioned inside the bottle during every rotation.

Its surface must remain physically plausible. It must not slide, detach, or rotate independently in a way that looks like a floating object.

If real-time fluid simulation is too expensive or unnecessary, use a carefully modeled static liquid volume with convincing optical effects.

Prioritize realism and performance over unnecessary simulation.

The glass, liquid, and reflections must work together during camera and bottle movement.

16. AUTHENTIC DAR SAIFA LOGO

The actual Dar Saifa logo must remain recognizable, sharp, correctly proportioned, and intentionally illuminated.

Inspect how the logo is implemented in the existing asset.

If it is embedded in the model or texture, preserve it where possible. If it needs reconstruction, use the authentic logo asset.

Do not stretch, distort, blur, mirror, or accidentally hide the logo.

Preserve the appropriate physical appearance if the logo is printed, embossed, engraved, or applied as a label.

The logo is a central visual anchor of the entire 3D experience.

The scroll choreography must not spend long periods exposing a simple or empty backside of the bottle.

This requirement must influence the camera path, rotation timing, chapter transitions, and final composition.

17. CINEMATIC LIGHTING

Build a professional perfume-product lighting setup.

Use an intentional combination of:

- Large soft key lighting.
- Vertical strip lights for long glass highlights.
- Rim lighting to define the silhouette.
- Subtle fill lighting.
- Top lighting for the cap.
- Environment reflections.
- Carefully controlled shadows.
- Contrasting bright and dark areas.

The bottle needs beautiful edge highlights while the liquid and logo remain readable.

Do not simply increase every light's intensity. Position and shape lights to reveal the bottle's geometry.

Lighting should participate in the storytelling and evolve subtly during scrolling.

Possible lighting progression:

- Hero: soft, elegant, atmospheric illumination.
- Product reveal: stronger silhouette and edge definition.
- Essence chapter: warmer or more atmospheric tones.
- Close-up: dramatic but controlled reflections.
- Final product shot: clean, balanced commercial lighting.

Transitions must be gradual and intentional.

Use HDRI or environment maps where appropriate, but ensure that they complement the brand palette and do not create uncontrolled reflections.

18. INTRODUCTION — CINEMATIC REVEAL

The introduction must be visually compelling from the first viewport.

Do not place the bottle against an empty background and call it a cinematic experience.

Build depth using three visual layers.

BACKGROUND

- Rich, sophisticated environmental gradients.
- Subtle atmospheric depth.
- Dark-to-light transitions.
- Controlled environmental reflections.

MIDGROUND

- Soft light and shadow.
- Subtle atmospheric haze.
- Restrained volumetric light where appropriate.
- Extremely subtle dust or particles only if they improve the composition.
- Abstract forms or shadows only when they complement the perfume's aesthetic.

FOREGROUND

- The authentic perfume bottle.
- Beautiful glass edge highlights.
- Readable Dar Saifa branding.
- A convincing shadow or grounding effect.

Do not add decorative elements simply to fill space.

INTRODUCTORY ANIMATION

Choreograph a deliberate reveal:

1. Begin with a beautiful atmospheric composition.
2. Gradually reveal part of the bottle's silhouette through subtle light.
3. Let the glass edges begin catching the light.
4. Reveal the cap, liquid, and bottle shape.
5. Give the Dar Saifa logo a controlled highlight.
6. Present the complete bottle in a premium hero composition.
7. Begin the cinematic camera movement.
8. Transition naturally into the main scroll-driven story.

The reveal must feel deliberate and elegant, not like a generic fade-in.

The first viewport must look complete and premium before the user scrolls.

Do not force users to wait through an unnecessarily long intro before interacting with the website.

Ensure that the reveal is compatible with reduced-motion preferences.

19. SCROLL-DRIVEN 3D STORYTELLING

This is the most important interaction on the “About Our House” page.

The bottle must feel physically integrated into the page and remain visually connected to the viewer as they scroll through the story.

Do not simply move the bottle vertically according to scroll progress.

Scrolling must control a coordinated cinematic timeline containing:

- Bottle position.
- Bottle rotation.
- Camera position.
- Camera orientation and target.
- Camera distance or field of view.
- Lighting.
- Environment.
- Atmospheric effects.
- Text transitions.
- Chapter transitions.

The experience should feel as though a professional camera crew is filming the bottle while the page reveals the fragrance story.

Use a persistent 3D canvas or another architecture suitable for the project so that the bottle remains visually present across multiple chapters without unwanted remounting, flickering, or resets.

The canvas and scroll choreography must be isolated to “About Our House.”

Do not introduce global scroll hijacking or a site-wide animation controller.

20. FIVE CINEMATIC CHAPTERS

Build approximately five connected chapters. Adjust their exact length to the actual available content and the page's existing structure.

CHAPTER 1 — THE ARRIVAL

- Bottle begins in a beautiful hero composition.
- Front/logo oriented toward the viewer.
- Premium scale and framing.
- Atmospheric background.
- Subtle floating or breathing motion.
- Carefully controlled lighting.
- Slight camera push-in as scrolling begins.

The logo must be clearly readable. The transition must feel continuous.

CHAPTER 2 — THE BOTTLE

- Bottle gradually shifts to one side of the composition.
- Supporting text appears in the available negative space.
- Camera moves laterally and begins a subtle orbit.
- Bottle rotates to reveal its physical construction.
- Lighting reveals the cap, glass borders, and liquid.
- Logo returns naturally into view.

The camera must contribute to the movement. Do not achieve everything by moving the bottle.

Keep the composition balanced on desktop and adapt it intentionally for mobile.

CHAPTER 3 — THE ESSENCE

Introduce the verified fragrance story, inspiration, ingredients, craftsmanship, or brand philosophy using authentic content already available in the project.

During this chapter:

- Camera and bottle continue moving naturally.
- Bottle rotates through carefully selected angles.
- Attractive details remain the focus.
- The user does not spend excessive time looking at an empty backside.
- Environment and lighting evolve subtly.
- Atmospheric effects add depth only where appropriate.
- Text appears in harmony with camera movement.

The atmosphere should feel sophisticated, not excessively magical, futuristic, or decorative unless that direction is supported by the actual brand.

Do not invent factual perfume notes or brand history.

CHAPTER 4 — THE CINEMATIC CLOSE-UP

Create the visual climax.

Move the camera closer to reveal:

- Glass thickness and borders.
- Liquid and its surface.
- Cap materials.
- Logo or label details.
- Reflections and controlled highlights.

Use a carefully choreographed camera orbit or dolly, rather than relying on zoom alone.

Use depth of field only if it improves the composition and remains performant.

Do not blur the logo or important product details.

Avoid camera clipping, penetration into the model, distorted proportions, and excessive perspective changes.

CHAPTER 5 — THE FINAL PRODUCT

Transition into a clean, premium product presentation.

- Bottle settles into a beautiful composition.
- Logo faces the viewer.
- Glass and liquid remain clearly visible.
- Camera motion slows and settles.
- Lighting becomes balanced and commercial.
- Subtle idle animation continues.

Integrate the final scene with existing product information, pricing, links, and purchase CTAs if they are already part of the page or current design.

Do not invent product information or remove existing purchasing functionality.

The final shot should make the visitor want to examine the perfume and explore the brand.

21. FULL ROTATIONS WITHOUT THE EMPTY BACKSIDE PROBLEM

I want complete, cinematic 360-degree rotations where appropriate, without forcing the viewer to look at the empty backside for long periods.

Do not solve this by:

- Limiting all rotations to a small angle.
- Snapping abruptly back to the starting orientation.
- Permanently locking the logo toward the camera.
- Removing the genuine 3D character of the product.

Instead, choreograph the bottle and camera together.

Use a combination of:

- Continuous bottle rotation.
- Camera orbit around the bottle.
- Camera position changes.
- Camera target interpolation.
- Carefully timed transitions between front, side, and three-quarter views.

An appropriate visual rhythm could be:

FRONT / LOGO
→ THREE-QUARTER VIEW
→ SIDE / DETAIL
→ CINEMATIC ORBIT
→ FRONT / LOGO RETURNS
→ CLOSE-UP
→ FINAL FRONT PRESENTATION

Adapt this choreography to the actual bottle geometry and scroll narrative.

Inspect the real model's coordinate system and logo orientation before implementing rotations. Do not assume the front corresponds to rotation Y = 0.

Use continuous angle interpolation or explicitly designed multi-turn rotations to avoid angle wrapping, unexpected direction changes, or sudden snaps.

The animation must reverse smoothly when the user scrolls backward.

If the backside contains important details, reveal them briefly and intentionally. If it is visually simple, use the camera path, angle duration, and rotation timing to maintain interest.

The final hero and product presentation must prioritize a clear, logo-facing view.

22. CAMERA CHOREOGRAPHY

Treat the camera as a central storytelling instrument.

Use cinematic movement such as:

- Slow dolly-in and dolly-out.
- Controlled camera orbit.
- Lateral movement.
- Perspective changes.
- Smooth target movement.
- Subtle changes in field of view where appropriate.

The camera must feel like it is filming a real physical product.

Coordinate camera and bottle transforms so that the product remains properly framed.

Ensure that:

- The bottle stays within the visible composition.
- The logo is not unintentionally cropped.
- The cap does not unexpectedly leave the frame.
- The model does not intersect the camera.
- Camera motion remains stable during fast scrolling.
- Mobile framing is deliberately designed.

Use appropriate interpolation for camera position and target. Avoid abrupt lookAt changes and sudden orientation flips.

23. ANIMATION ARCHITECTURE

Build a clean, maintainable architecture suited to the existing project.

Potential components:

- PerfumeScene.
- PerfumeModel.
- PerfumeMaterials.
- PerfumeLighting.
- PerfumeCameraController.
- ScrollAnimationController.
- IdleAnimationController.
- EnvironmentEffects.
- ScrollStorySections.

Adapt the structure to the existing application rather than introducing unnecessary abstractions.

Use one master GSAP timeline connected to ScrollTrigger to coordinate the main scroll experience.

The timeline should coordinate:

- Bottle position and rotation.
- Camera position and target.
- Camera perspective where appropriate.
- Lighting transitions.
- Environment effects.
- Text and chapter transitions.

Use refs for high-frequency animation and avoid unnecessary React state updates on every frame.

Avoid multiple competing ScrollTriggers controlling the same transforms.

Ensure correct setup and cleanup, especially in React Strict Mode. Revert or kill timelines, ScrollTriggers, and event listeners appropriately when components unmount or reinitialize.

The animation must be deterministic: a given scroll position should correspond to a predictable scene state.

24. SMOOTH SCROLLING AND ANIMATION SYNCHRONIZATION

Use Lenis and GSAP ScrollTrigger together correctly when compatible with the existing application.

Ensure synchronization across supported browsers and avoid duplicate animation loops or unnecessary listeners.

Use appropriate ScrollTrigger scrubbing so the bottle and camera respond smoothly to scroll progress.

Test different smoothing values instead of assuming one value will work for every section.

The experience must remain coherent when users:

- Scroll slowly.
- Scroll quickly.
- Scroll rapidly through several chapters.
- Reverse direction.
- Stop midway through a transition.
- Navigate to another section.
- Use touch gestures on mobile.

Avoid lag, sudden jumps, unexpected resets, and animations that continue independently of scroll when they should be synchronized.

Do not use window.scrollY as the primary animation engine.

Do not add excessive smoothing that makes the bottle feel disconnected from user input.

If the project already has a smooth-scroll implementation, integrate with it rather than creating competing systems.

25. IDLE AND POINTER ANIMATION

When the user stops scrolling, the bottle should feel alive without excessive movement.

Potential effects:

- Extremely subtle vertical floating.
- Gentle rotation.
- Slight camera breathing.
- Very restrained light movement.

Separate idle animation from the scroll-driven master timeline.

Do not allow idle motion to fight the scroll timeline or cause transforms to accumulate unpredictably.

Use additive offsets or another controlled technique.

On desktop, subtle mouse parallax may be used if it improves the composition. It must never overpower the scroll choreography.

On mobile, disable pointer-specific effects and simplify motion.

Respect reduced-motion preferences by providing a less animated experience without breaking the page or hiding the product.

26. TYPOGRAPHY AND CONTENT SYNCHRONIZATION

Design the page content around the 3D composition.

Use authentic Dar Saifa typography and branding wherever available.

Coordinate text reveals with the scroll timeline:

- Elegant entrances and exits.
- Clear visual hierarchy.
- Proper spacing.
- Balanced negative space.
- Readable text against the background.

Do not place text over the logo or important bottle details.

Avoid excessive animation on every line.

Keep text in normal, accessible HTML wherever possible rather than rendering all content inside the 3D canvas.

Ensure the page remains understandable and useful if WebGL is unavailable or reduced motion is enabled.

27. PERFORMANCE AND RENDERING QUALITY

The experience must be visually impressive without being unnecessarily expensive to render.

Implement, where appropriate:

- Sensible pixel-ratio limits.
- Mobile-specific quality settings.
- Optimized geometry and textures.
- Efficient lighting.
- Proper resource disposal.
- Lazy loading where appropriate.
- Minimal React re-renders.
- Reuse of geometries and materials.
- Efficient environment and post-processing settings.
- Responsive canvas sizing.
- Cleanup of animation loops and listeners.

Use compressed GLTF/GLB assets where appropriate. Consider Draco or KTX2 only if compatible with the existing asset pipeline and correctly configured.

Avoid expensive real-time simulations when static geometry or a shader-based approach can provide an equally convincing result.

Do not add heavy post-processing effects just because they are available.

The bottle must still look premium on mobile devices.

Ensure scroll synchronization continues working after resizing or orientation changes.

Avoid unnecessary rendering when the experience is not visible, provided this does not break the animation architecture.

Provide a graceful fallback if WebGL or the 3D asset fails to load. Preserve the page's text, brand story, navigation, and other essential content.

28. RESPONSIVE EXPERIENCE — ABOUT OUR HOUSE ONLY

DESKTOP

- Full cinematic composition.
- Detailed but restrained camera choreography.
- High-quality materials within reasonable performance limits.
- Balanced text and bottle placement.

TABLET

- Adjusted camera framing.
- Simplified effects where necessary.
- Appropriate text spacing.

MOBILE

- Dedicated camera composition rather than simply shrinking the desktop scene.
- Correctly scaled or repositioned bottle.
- Reduced pixel ratio and expensive effects.
- Simplified pointer/parallax behavior.
- Reliable touch scrolling.
- Readable typography.
- Preserved logo visibility.
- No unwanted horizontal overflow.
- No bottle cropped or hidden behind text.

The mobile version must still feel premium, even if some effects are simplified.

Do not break normal website navigation or introduce scroll-locking behavior that makes the page difficult to use.

29. IMPLEMENTATION AND VALIDATION FOR THE ABOUT PAGE

After implementing the new experience:

1. Verify bottle geometry, logo orientation, and material assignments.
2. Verify the liquid is visibly inside the bottle and remains correctly positioned.
3. Review the beginning, middle, and end of every chapter.
4. Check front, three-quarter, side, and backside orientations.
5. Confirm the logo regularly returns to a clear, well-lit view.
6. Test complete rotations and ensure there are no abrupt snaps or angle reversals.
7. Test scrolling backward and forward through every transition.
8. Test fast scrolling and ensure the scene does not break.
9. Check camera clipping, object intersections, and unexpected framing.
10. Verify Lenis and ScrollTrigger synchronization if both are used.
11. Check responsive behavior and rendering performance.
12. Verify reduced-motion behavior and the non-WebGL fallback.
13. Run the available build, lint, type checks, and relevant tests.
14. Fix issues introduced by the implementation.
15. Use a browser preview or screenshots when available and refine the actual visual result.

Do not claim to have visually inspected a page if you only inspected its source code.

If browser testing is unavailable, complete code-level checks and explicitly state that visual verification remains incomplete.

==================================================
PART 3 — PROJECT-WIDE SAFETY, INTEGRATION, AND CHANGE CONTROL
==================================================

30. PRESERVE THE EXISTING WEBSITE

Do not remove existing features, routes, page content, products, product data, shopping cart behavior, checkout, integrations, or working functionality.

Do not make unrelated backend or architectural changes.

Do not replace authentic Dar Saifa assets with generic substitutes.

Do not overwrite user work without inspecting the relevant files first.

Do not make changes outside the necessary scope simply because they are easier to implement.

Do not introduce a second conflicting design system, duplicate scroll controller, or unnecessary dependency.

The existing website must remain a functioning website, not just a visually impressive About page.

31. KEEP THE TWO SCOPES SEPARATE IN THE IMPLEMENTATION

Use this strict division:

GLOBAL WEBSITE:
- Brand color tokens.
- Consistent design system.
- Shared typography and visual patterns where appropriate.
- Website-wide component styling.
- Responsive and accessible shared components.
- Page-by-page palette audit.

ABOUT OUR HOUSE ONLY:
- Persistent 3D canvas.
- Perfume bottle model and materials.
- Cinematic lighting and environment.
- Scroll-driven master GSAP timeline.
- Bottle rotation and camera choreography.
- Chapter-based storytelling.
- 3D-specific atmospheric effects.
- About-page-specific responsive 3D settings.

Shared design tokens may be used inside the 3D page, but the 3D scene and its animation controllers must not be mounted globally.

If a shared header, footer, or navigation component is modified, verify that it continues to work across all routes, including “About Our House.”

32. IMPLEMENTATION WORKFLOW

PHASE 1 — DISCOVERY

Inspect the repository, read project instructions, identify the framework, discover available skills and tools, enumerate routes, locate assets, and identify the “About Our House” page.

PHASE 2 — TWO SEPARATE AUDITS

Audit A: review every page and component for brand colors, design inconsistencies, and responsive issues.

Audit B: review the About page's current 3D scene, model geometry, logo, materials, lighting, animation, and performance.

PHASE 3 — PLAN

Create an internal page-and-component checklist for the global design system and a separate implementation plan for the About page.

Identify which changes are global and which are exclusive to the About page.

PHASE 4 — IMPLEMENT GLOBAL DESIGN SYSTEM

Establish centralized tokens and apply the palette throughout all discovered pages, routes, layouts, and relevant components.

Verify each page rather than assuming that global CSS alone is sufficient.

PHASE 5 — IMPLEMENT ABOUT PAGE EXPERIENCE

Rebuild or improve the 3D scene, materials, lighting, camera, and master scroll timeline. Integrate the cinematic experience into the existing About page without spreading it to other routes.

PHASE 6 — VERIFY

Revisit both checklists.

Verify the palette across the whole website. Separately verify the 3D experience on the About page.

Run available build and code checks. Use browser previews, screenshots, or automated tests when available.

Test relevant desktop, tablet, and mobile layouts.

Fix any regressions caused by the changes.

PHASE 7 — REPORT

Provide a clear final report that separates:

A. GLOBAL WEBSITE CHANGES
- All discovered routes and pages.
- Pages audited.
- Pages updated.
- Shared components modified.
- Color tokens introduced or updated.
- Remaining inconsistencies or limitations.

B. ABOUT OUR HOUSE 3D EXPERIENCE
- About page route.
- Bottle and material improvements.
- Lighting and environment changes.
- Scroll timeline and chapter structure.
- Camera and bottle rotation coordination.
- Logo visibility strategy.
- Responsive and performance optimizations.
- How to adjust animation timing and bottle positions.

C. VALIDATION
- Files created or modified.
- Skills and tools actually used.
- Build, lint, type checks, and tests performed.
- Visual checks actually completed.
- Failures and remaining limitations.
- Any pages or states that could not be verified and why.

Do not claim that tests passed unless they were actually run. Do not claim that all routes were visually checked if only some were opened in a browser.

==================================================
PART 4 — NON-NEGOTIABLE ACCEPTANCE CRITERIA
==================================================

GLOBAL WEBSITE REQUIREMENTS:

1. The entire existing website has been audited, not just the homepage.
2. Every discovered page, route, layout, template, and relevant component has been reviewed.
3. The official colors #3D0F14, #241915, #B8862B, and #F2EDE3 are implemented consistently.
4. Conflicting legacy colors have been addressed where appropriate.
5. Shared design tokens are used wherever appropriate.
6. Responsive behavior and accessibility have been checked to the extent possible.
7. Existing routes, content, purchasing functionality, and integrations remain intact.
8. The website retains a cohesive luxury Dar Saifa identity.

ABOUT OUR HOUSE REQUIREMENTS:

9. The immersive 3D perfume experience exists only on the “About Our House” page.
10. The authentic bottle and logo are used wherever available.
11. The glass, liquid, cap, and lighting produce a convincing premium product presentation.
12. The introduction has atmospheric depth and a deliberate cinematic reveal.
13. Scroll controls a coordinated master timeline involving the bottle, camera, lighting, and content.
14. Bottle rotation and camera movement work together to avoid prolonged, visually uninteresting backside views.
15. The logo remains sharp and regularly returns to a well-lit, front-facing composition.
16. Scrolling backward, fast scrolling, resizing, and mobile touch interaction do not break the scene.
17. Responsive behavior, performance safeguards, reduced-motion behavior, and fallbacks are implemented appropriately.
18. The final product composition is polished, readable, and integrated with the page's existing content.

PROJECT-WIDE REQUIREMENTS:

19. No unrelated features or routes have been removed.
20. No unnecessary rebuild or incompatible dependencies have been introduced.
21. Available checks have been run and relevant regressions addressed.
22. The final report clearly distinguishes implemented work from verified results and unresolved limitations.

Updating only the homepage is a failure.

Applying the 3D experience to every page is also a failure.

Applying global color changes without checking individual pages is insufficient.

Creating a beautiful About page while breaking the rest of the website is unacceptable.

==================================================
FINAL INSTRUCTION
==================================================

Start by inspecting the existing repository, project instructions, routes, assets, and available tools.

First establish the complete website-wide page checklist and the separate “About Our House” implementation plan.

Then implement the official Dar Saifa brand design system across the ENTIRE website.

After that, build the exceptional cinematic 3D perfume experience EXCLUSIVELY on the “About Our House” page.

Treat the whole website as one coherent luxury brand, but treat the About page as its own immersive storytelling experience.

Do not stop at recommendations or isolated code snippets. Implement the changes directly, preserve existing functionality, run the available checks, inspect the actual result wherever possible, and provide an honest final report.

The desired outcome is a cohesive, premium Dar Saifa website with a consistent brand identity across every page and an exceptionally polished, cinematic 3D experience on “About Our House” alone.
