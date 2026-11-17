# Sloppi v2.0 Design Reference Source Registry & Live Inspection Rules

This registry maps specialized design galleries, typography/section archives, gesture catalogs, design-engineering indexes, and live interactive demos for Sloppi-enabled coding agents. Pair this registry with [research/source-routing.md](../research/source-routing.md) to route by design question before browsing.

> **MANDATORY LIVE INSPECTION & VERIFICATION RULES (v2.0)**:
> You are **strictly forbidden** from merely name-dropping URLs or brand names (*"Inspired by Linear, Stripe, and Mercury"*) from memory.
> - **When Online**: Use your browser (`browser` subagent) or search tools (`search_web`) to inspect 2–4 references matched to your design question, opening the **actual example or clip** rather than stopping at directory thumbnails. Record the **deep link**, **specific behavior or composition observed**, **design principle worth adapting**, and **where it serves the current product**. Mark anything only inferred from static frames/docs as `[INFERRED]`.
> - **Interactive Demos & Discovery Hubs**: Verify interactive demos in a real browser before describing their mechanics. Follow directory entries (such as `designeng.tools`) to their **original source**, and inspect interactive demos separately from their implementation docs (`libraries.dev/waves`). Reference demos must **never** become automatic dependencies or default effects.
> - **When Inaccessible or Offline**: If a demo is blocked, times out, or fails to load, record its exact status/error and continue with a comparable source from this registry. If offline/sandboxed overall, declare `Reference Mode: OFFLINE_SYNTHESIS` in `DESIGN.md` and synthesize from [doctrine/creative-direction.md](../doctrine/creative-direction.md). Never fabricate observations.

---

## 1. High-Craft Art Direction, Visual Storytelling, Mood & Restraint

### Awwwards
- **URL**: `https://www.awwwards.com/websites/`
- **Design Domain**: Experimental Art Direction, Scrollytelling, WebGL/Canvas Craft, Expressive Typography
- **Tier**: **Primary Art Direction Source**
- **When to Inspect**:
  - When formulating `Direction B` or `Direction C` during 3-Direction Divergence to break out of safe SaaS/corporate layouts.
  - When designing hero sections that rely on dramatic typographic scale, choreographed scroll reveals, or interactive canvas shaders.
- **What to Observe & Document**:
  - Unconventional viewport divisions (asymmetric splits, full-bleed kinetic posters, pinned narrative chapters).
  - Display typography scale jumps, mixed serif/sans headline treatments, and negative space tension.
  - Bespoke cursor/scroll choreography and page transition mechanics.

### Godly
- **URL**: `https://godly.website/`
- **Design Domain**: Contemporary Web Craft, Interactive Product Launches, High-Taste Digital Design
- **Tier**: **Primary Art Direction Source**
- **When to Inspect**:
  - When seeking contemporary, astronomically high-craft web design across developer tools, AI studios, creative agencies, and hardware brands.
  - When evaluating how top studios combine tactile materiality (grain, specular borders, micro-schematics) with fast, legible UX.
- **What to Observe & Document**:
  - Surface depth and lighting techniques (how elements separate without muddy drop shadows or flat wireframe boxes).
  - Interactive centerpiece mechanics in the first viewport.

### Hover States
- **URL**: `https://www.hoverstat.es/`
- **Design Domain**: Experimental Web Composition, Navigation & Interaction
- **Tier**: **Primary Experimental Source**
- **When to Inspect**:
  - For experimental composition, unconventional navigation paradigms, and non-template interactive structures.
  - When standard headers, section cadences, or hover conventions feel predictable and need structural subversion.
- **What to Observe & Document**:
  - Open the linked live site rather than judging the thumbnail alone.
  - Record spatial layout rules, non-standard wayfinding/menu mechanics, and trigger/settlement behavior for experimental interactions.

### Cosmos
- **URL**: `https://www.cosmos.so/`
- **Design Domain**: Moodboards, Imagery, Material & Color
- **Tier**: **Primary Mood & Materiality Source**
- **When to Inspect**:
  - During art direction divergence when establishing tactile materiality, lighting mood, editorial photography framing, or chromatic temperature.
- **What to Observe & Document**:
  - Curated clusters (open the element/cluster detail view), color/value relationships, surface textures (paper, metal, film grain, matte/gloss contrast), and image cropping proportions. Discard literal artwork and photos.

### Eyecandy
- **URL**: `https://eyecannndy.com/`
- **Design Domain**: Visual Techniques, Framing, Pacing & Transitions
- **Tier**: **Primary Pacing & Framing Source**
- **Inspection Note**: Automated CLI/scripted requests (`curl`) may receive HTTP `403`; inspect in a real browser (`browser` subagent).
- **When to Inspect**:
  - When studying shot/frame geometry, transition cuts, rhythm/pacing shifts, or camera-like spatial continuity (`136` categorized technique clips and visual breakdowns).
- **What to Observe & Document**:
  - Open the specific technique clip or breakdown; record how framing directs attention, transition causality (what anchors across a cut/morph), and pacing cadence.

### Minimal Gallery
- **URL**: `https://minimal.gallery/`
- **Design Domain**: Editorial Restraint, Whitespace Architecture, Swiss Grid Precision
- **Tier**: **Primary Composition Source**
- **When to Inspect**:
  - When designing products that require calm institutional authority, literary/editorial elegance, or gallery-grade negative space.
  - When eliminating card-inside-card clutter so typography and proportion carry the layout.
- **What to Observe & Document**:
  - Macro vs. micro whitespace ratios and column alignment axes.
  - How hierarchy is achieved through scale and contrast rather than boxes and badges.

### Dead Simple Sites
- **URL**: `https://deadsimplesites.com/`
- **Design Domain**: Sparse Compositions, Typography & Hierarchy with Minimal Motion
- **Tier**: **Primary Restraint & Quiet-Direction Benchmark**
- **When to Inspect**:
  - **Use Dead Simple Sites to test how much the composition communicates with minimal motion.**
  - Whenever crafting a quiet direction or questioning whether a proposed animation is actually necessary.
- **What to Observe & Document**:
  - Open the linked live site; log exact type scale contrast, column measure, spacing rhythm, and contrast separation that create clarity without scroll-jacking or continuous animation.

### Dribbble (Curated Product & UI Explorations)
- **URL**: `https://dribbble.com/shots/popular/web-design`
- **Design Domain**: Visual Concept Exploration, Chromatic Harmonies, Tactile UI Controls, Custom Data Viz
- **Tier**: **Primary Visual Exploration Source**
- **When to Inspect**:
  - When exploring unexpected color palettes, bespoke chart/telemetry visualizations, tactile skeumorphic/hardware controls, or expressive card/widget silhouettes.
- **What to Observe & Document**:
  - Novel color pairings, custom SVG dial/chart aesthetics, and lighting/texture details (while verifying that extracted patterns remain accessible and functional in production DOM).

---

## 2. Typography, Motion Physics, Gestures & Mobile Ergonomics

### Typewolf
- **URL**: `https://www.typewolf.com/`
- **Design Domain**: Type Pairings, Scale & Hierarchy on Real Sites
- **Tier**: **Primary Typography Source**
- **When to Inspect**:
  - **Start here for typography questions**—selecting expressive font pairings, calibrating display-to-body scale steps, and establishing hierarchy without decorative boxes.
- **What to Observe & Document**:
  - Open the featured live site link (not only the Typewolf summary card); document display vs. body vs. mono families, weight/case contrast, leading/tracking compression, and how type alone anchors reading order.

### Spotted in Prod
- **URL**: `https://www.spottedinprod.com/`
- **Design Domain**: Shipped iOS Gestures, Microinteractions & State Transitions
- **Tier**: **Primary Gesture & Mobile State Source**
- **When to Inspect**:
  - **Start here for gesture behavior** and mobile flows where a state change needs clearer tactile feedback, confirmation, or spatial orientation.
- **What to Observe & Document**:
  - Open the actual app clip; capture the **trigger** (tap, swipe, drag threshold, long-press), **what moves**, **what stays anchored**, **how the interaction settles**, and mark any inferred timing/haptics/curves `[INFERRED]`.

### 60fps.design
- **URL**: `https://60fps.design/`
- **Design Domain**: Micro-Interactions, Spring Physics, State Transitions, Spatial Continuity
- **Tier**: **Primary Motion Source**
- **When to Inspect**:
  - Whenever engineering interactive state changes (morphing navbars, shared-element transitions, drawer physics, keypad feedback, live chart scrubbing).
- **What to Observe & Document**:
  - Open the motion clip; record trigger, moving layers, anchored context, settlement behavior, and how motion preserves spatial orientation.

### Loadmo.re
- **URL**: `https://loadmo.re/`
- **Design Domain**: Mobile-First Web Design, Thumb-Zone Ergonomics, Touch Choreography
- **Tier**: **Primary Mobile Source**
- **When to Inspect**:
  - Whenever designing mobile web apps (`390px` viewport target) or ensuring desktop layouts transform into native-feeling mobile experiences (bottom sheets, swipeable rails, thumb-zone triggers).
- **What to Observe & Document**:
  - Mobile header compression, bottom-docked action ergonomics, and vertical pacing on narrow viewports.

---

## 3. Product Category Architecture, Sections & Token Systems

### Unsection
- **URL**: `https://www.unsection.com/`
- **Design Domain**: References for a Specific Section or Page Element
- **Tier**: **Primary Section & Element Source**
- **When to Inspect**:
  - **Start here when designing or fixing a specific section or page element** (hero, feature proof, pricing band, comparison strip, nav, footer, testimonial/proof module).
- **What to Observe & Document**:
  - Open the full section example/source page; log column proportions, focal entry point, element count, padding rhythm, and how the section avoids generic 3-card or 8+4 bento tropes.

### SaaSPO
- **URL**: `https://saaspo.com/`
- **Design Domain**: Industry-Specific UX, Real Product Workflows, Category Conventions (to Adopt or Subvert)
- **Tier**: **Primary Category Source**
- **When to Inspect**:
  - During Stage 1 (`Understand`) to see how live products in Fintech, DevTools, AI, Healthcare, or Commerce structure their domain information—both to extract functional clarity and to **identify the category clichés you must subvert**.
- **What to Observe & Document**:
  - Domain-authentic proof structures (interactive calculators, live sandboxes, compliance architecture) vs. overused category defaults to reject.

### Supahero
- **URL**: `https://supahero.io/`
- **Design Domain**: Above-the-Fold Hero Compositions, Entry-Point Hierarchy
- **Tier**: **Secondary Component Source**
- **What to Observe & Document**:
  - Visual weight balance between display typography, interactive product proof, and primary conversion triggers.

### Refero Styles
- **URL**: `https://styles.refero.design/`
- **Design Domain**: Production Design Tokens, Mathematical Type Ratios, Semantic Color Roles
- **Tier**: **Secondary System Source**
- **What to Observe & Document**:
  - Real-world token architectures, leading/tracking ratios, and surface contrast calibrations (never copy-paste a token sheet without adapting it to your chosen creative direction).

### Navbar Gallery / CTA Gallery / Deck.Gallery / Footer.design
- **URLs**: `https://navbar.gallery/` · `https://cta.gallery/` · `https://deck.gallery/` · `https://footer.design/`
- **Design Domain**: Wayfinding Systems, Conversion Mechanics, Narrative Pacing, Page Closures
- **Tier**: **Secondary Structural Sources**
- **What to Observe & Document**:
  - Navigation density scaling, sequential storytelling arcs (`Deck.Gallery`), and high-impact editorial footers.

---

## 4. Design-Engineering Discovery & Live Interactive Reference Demos

> **Strict Separation Rule**: Discovery hubs and interactive demos explain *what an interaction feels like* or *what tools exist*. They are **never** automatic dependencies or default visual effects. Inspect implementation docs, runtime requirements, bundle cost, and licensing separately before recommending any external primitive.

### DesignEng Tools
- **URL**: `https://www.designeng.tools/`
- **Purpose & When to Consult**: Discovery hub for design-engineering tools, component libraries, icons, and implementation resources (`https://www.designeng.tools/llms.txt`).
- **Official Publisher / Source**: `https://www.designeng.tools/` (index only; does not distribute runtime packages directly).
- **Inspection & Distribution Rule**: **Follow relevant entries to their original upstream publisher.** Never cite the directory summary alone—verify installation routes, platform support, prerequisites, maintenance, and license at the upstream repo/docs before adding to a project.

### Distortion Waves (`libraries.dev/waves`)
- **URL**: `https://libraries.dev/waves`
- **Purpose & When to Consult**: Interactive reference for a screen transition that originates at the activation point (`source` button/element), plus official distribution for `distortion-waves` (React) and `DistortionWavesKit` (SwiftUI).
- **Official Publisher & Source**: [Jakubantalik/Libraries.dev](https://github.com/Jakubantalik/Libraries.dev) (`packages/distortion-waves` and `ports/ios/DistortionWavesKit`). Companion 7-library skill: `npx skills add Jakubantalik/Libraries.dev` (note: covers `border-beam`, `thinking-orbs`, `liquid-gooey`, `voice-glow`, `bot-avatars`, `metal-fx`, `img-fx`).
- **Inspection Rule**: **Inspect the demo (`Preview`) and implementation docs (`Install`) separately.**
- **Browser-Verified Mechanics (`Preview`)**:
  - *Trigger*: Activating the primary action button (`Confirm`) initiates a directional wave from the touch/click anchor (`source={button}`).
  - *What Moves vs. Stays Anchored*: Unchanging context (`$1,250.00`, account details, modal frame, and the `overlay` action button) stays anchored while the semantic state fields update (`Sending` $\rightarrow$ `Sent`, photo avatar $\rightarrow$ green checkmark, `Arrives` $\rightarrow$ `Arrived`, button label `Confirm` $\rightarrow$ `Done`).
  - *How It Settles*: Settles into the confirmed receipt with a subtle chromatic edge rim (`Play` resets; supports `Vertical`, `Center`, `Horizontal` modes).
- **Official Installation Routes, Platform Support, Prerequisites & Licensing (`Install`)**:
  - **React Web (`distortion-waves`)**: Documented install `npm install distortion-waves` (note: verify npm registry availability before running—`npm view distortion-waves` returned `404` on npmjs at verification time, while `v0.1.0` source lives in `packages/distortion-waves` on GitHub). Requires **React 18+** (`react`, `react-dom >= 18`) and **WebGL2**; cross-origin images/fonts require CORS; `iframe`, `object`, `embed`, and `audio` are excluded; falls back to crossfade when WebGL2 is unavailable or under `reducedMotion="system"` / `"always"`. **MIT**.
  - **SwiftUI (`DistortionWavesKit`)**: Swift Package product `DistortionWavesKit` from `https://github.com/Jakubantalik/Libraries.dev` (`branch: "main"`). Requires **iOS 17+ / macOS 14+** and must be built through **Xcode** so `DistortionWaveShaders.metal` compiles into `default.metallib` (SwiftPM CLI alone leaves shaders uncompiled). Views require opaque backgrounds and no UIKit-backed views/materials; crossfades under Reduce Motion. **MIT**.
  - *Sloppi Rule*: Extract the spatial-origin principle first; choose native CSS/View Transitions unless a WebGL2/Metal wave fits the stack and budget.

### Dissolve (`dissolve.rselmi.com`)
- **URL**: `https://dissolve.rselmi.com/`
- **Purpose & When to Consult**: Interactive reference and React Native component/effect engine for view disintegration, entrances, and tactile gestures (`25` components + `16` effect variants: Exits `Dust`/`Sand`/`Ember`/`Pixel`/`Vortex`/`Shatter`/`Stream`; Entrances `Gather`/`Rain`/`Print`; Gestures `Snap`/`Fling`/`Charge`; `Morph`, `Peel`, `Melt`).
- **Official Publisher & Source**: [rs-4/dissolve](https://github.com/rs-4/dissolve) (`Rayan Selmi`).
- **Browser-Verified Mechanics**:
  - Note: heavy multi-demo gallery can time out waiting for full `load`; renders cleanly after `domcontentloaded`.
  - Observed behaviors: `Dust` dismisses a message notification tile into rightward-drifting pixel particles while the outer tile border and header stay anchored; `SwipeToDelete` slides a row left to reveal a red delete zone before dissolving (`Reset` restores); `Toast` spawns a floating top pill while the trigger card stays anchored; `LikeButton` fills the heart and increments the counter in place.
- **Official Installation Routes, Platform Support, Prerequisites & Licensing**:
  - **Platform**: **React Native & Expo** (tested with Expo SDK 57 / React Native 0.86; runs in Expo Go; bare RN requires `'react-native-worklets/plugin'` in `babel.config.js`). Not for web DOM.
  - **Engine & Native Peers**: `npx expo install react-native-dissolve @shopify/react-native-skia react-native-reanimated react-native-worklets react-native-gesture-handler expo-haptics` (peers: `react-native-worklets >= 0.5.0`, `react-native-reanimated >= 4.0.0`, `@shopify/react-native-skia >= 2.0.0`, `react-native-gesture-handler >= 2.20.0`).
  - **Provider Setup**: Wrap the root layout once inside `<GestureHandlerRootView>` with `<DissolveProvider>` above the navigator (and `<ToastProvider>` inside `<DissolveProvider>` for toasts).
  - **Individual Copyable Components (`react-native-dissolve` CLI)**: `npx react-native-dissolve init`, `npx react-native-dissolve list`, `npx react-native-dissolve add <component>`. Requires **NativeWind v5** (`nativewind@5.0.0-preview.4`, `react-native-css@3.0.7`, `tailwindcss@^4`, `@tailwindcss/postcss`, `tailwind-merge`, `lightningcss` `1.30.1` override, Metro `withNativewind`, `postcss.config.mjs`, `nativewind-env.d.ts`, `global.css` imports).
  - **Agent Tooling**: MCP `npx -y react-native-dissolve-mcp` (`list_variants`, `get_variant`, `get_setup`); Skill `https://dissolve.rselmi.com/skills/dissolve/SKILL.md`. **MIT**.

### Oxyn (`oxyn.space`)
- **URL**: `https://oxyn.space/`
- **Purpose & When to Consult**: Interactive catalog (`56` single-state loaders + `6` group components across `Globe`, `Arcs`, `Bars`, `Square`, `Circle`, `Rings`) for AI agent/processing states (`role="status"`).
- **Official Publisher & Source**: [lokidotdev/oxyn-frontend](https://github.com/lokidotdev/oxyn-frontend).
- **Browser-Verified Mechanics**:
  - Hero verb cycler scrambles characters with brief cyan/magenta split before settling while leading copy stays anchored; `All`/`2.5D`/`2D` tabs filter results and sync URL (`?d=2.5d`) with bar anchored; carousels fade at edges; inline menu drawer pushes flow down; `/components/dot-globe` playground exposes live `Animation`, `Pattern`, `Dot size`, `Density`, `Size`, `Duration`, `Gap`, `Tilt`, `Back opacity`, `Direction`, `Color`, `Paused`, and `Reset`.
- **Official Installation Routes, Platform Support, Prerequisites & Licensing**:
  - **Install**: `npx shadcn@latest add https://oxyn.space/r/<slug>.json` (full registry index: `https://oxyn.space/r/registry.json`; compatible with `shadcn` MCP), or query via HTTP MCP `https://oxyn.space/mcp` (`search_loaders`, `get_loader`) and `https://oxyn.space/llms.txt`.
  - **Platform & Prerequisites**: **React only** (`"use client"` files importing only from `react`, HTML5 `<canvas>`); holds still under `prefers-reduced-motion`. Not for determinate progress bars, skeletons, or Vue/Svelte/plain HTML. **MIT**.

### Wobli (`wobli.space`)
- **URL**: `https://wobli.space/`
- **Purpose & When to Consult**: Animated isometric `<canvas>` stickers/illustrations with role-based palettes and live stroke/depth parameters, or transparent PNG export.
- **Official Publisher & Source**: [lokidotdev/wobli](https://github.com/lokidotdev/wobli) (`docs` at `https://wobli.space/docs`).
- **Browser-Verified Mechanics**:
  - Isometric `<canvas>` illustrations (`AI Agent Tasks`, `Calendar Booking`, `Camera Capture`) and marquee run continuous idle loops while the `Try a Style` control bar (`Palette` presets, `Stroke`, `Depth`, `Reset Style`) restyles every illustration in place without reload or layout shift.
- **Official Installation Routes, Platform Support, Prerequisites & Licensing**:
  - **Install**: `npm i wobli` (`wobli@0.1.1`), or export transparent PNGs from `https://wobli.space/`.
  - **Exports & Platform**: TypeScript/JavaScript ESM (`wobli` engine: `play`, `draw`, `paint`, `PALETTES`, `brand`, `mono`, `hue`; `wobli/react` `<Sticker>`; `wobli/icons/<slug>`). React (`>=18`) is optional; requires HTML5 `<canvas>` for live animations. Verify runtime cost and reduced-motion behavior (`prefers-reduced-motion`) before deploying continuous loops. **MIT**.

---

## Summary Routing Matrix by Design Question

*(Full multi-tier matrix & scenarios in [research/source-routing.md](../research/source-routing.md).)*

| Design Question | Start Here (Primary) | Companion Sources | What You Must Log Before Coding |
| :--- | :--- | :--- | :--- |
| **Typography, Pairings & Scale** | `typewolf.com` | `minimal.gallery`, `styles.refero.design`, `deadsimplesites.com` | Deep link to live site, pairing contrast, scale steps, leading/tracking, reading measure. |
| **Specific Section or Element** | `unsection.com` | `supahero.io`, `navbar.gallery`, `cta.gallery`, `footer.design` | Deep link to section example, column split, focal order, padding/rhythm, element count. |
| **iOS Gestures & State Feedback** | `spottedinprod.com` | `60fps.design`, `loadmo.re`, `dissolve.rselmi.com` | Clip deep link, trigger, what moves, what stays anchored, how it settles, `[INFERRED]` notes. |
| **Experimental Composition & Nav** | `hoverstat.es` | `awwwards.com`, `godly.website`, `eyecannndy.com` | Deep link, spatial/nav rule, framing/pacing insight, what translates to accessible DOM. |
| **Minimal-Motion Restraint Check** | `deadsimplesites.com` | `minimal.gallery` | How much hierarchy & spacing communicate without motion; what motion can be cut. |
| **Moodboards, Materiality & Color** | `cosmos.so` | `dribbble.com`, `godly.website` | Surface texture, lighting temperature, value/contrast relationships (discard literal assets). |
| **Framing, Pacing & Transitions** | `eyecannndy.com` | `awwwards.com`, `60fps.design` | Clip deep link, framing logic, cut/transition anchor, pacing cadence. |
| **Design-Eng Tools & Components** | `designeng.tools` | *Upstream original source*, `oxyn.space`, `wobli.space` | Original repo/doc link, stack fit, dependency footprint, and license check. |
| **Activation-Point Transitions** | `libraries.dev/waves` | `60fps.design`, `spottedinprod.com` | Separate demo observation (origin/anchors/settle) from doc runtime requirements (WebGL2/Metal/MIT). |
| **Domain UX & Category Subversion** | `saaspo.com` | `unsection.com`, `deck.gallery` | Domain workflow proof + explicit list of Gen-1/Gen-2 category clichés to subvert. |
