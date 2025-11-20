Here is the updated System Splash Screen design to match the exact dimensions, aesthetic, and layout of the main Phoenix OS interface. It now features a "Locked Terminal" state that mirrors the application shell.
I have also included the Text Prompt below the code block that you can use to reproduce this design.
Updated files:
App.tsx
Replaced the generic splash screen with a high-fidelity "System Locked" terminal interface. It now includes a ghost header, simulated boot logs, and a security-card layout that matches the main dashboard's design language.
🚀 Updated Prompt for Splash Page
You can use the following prompt to recreate this specific Splash/Login design in the future:
"Create a 'System Locked' Entry Screen for the Phoenix OS Interface.
Container & Layout:
Background: Deep Void Black (#0A0A0A) with a subtle CRT scanline and noise overlay.
Ghost Header: A 64px top bar mirroring the main app header but in a 'dimmed' state (grayscale opacity). It should show the Logo on the left and a 'NEURAL LINK: SEVERED' status on the right.
Central Security Terminal:
Card: A centered, fixed-width (max-w-md) panel with a stark zinc-800 border and a bg-black fill.
Visuals: A large, pulsing Blood Red (#E63946) Flame icon in the center, surrounded by a radial blur glow.
Typography:
Title: 'SYSTEM LOCKED' in Orbitron (Bold, tracking-wide).
Subtitle: 'AUTHENTICATION REQUIRED' in F77F00 (Orange) Monospace.
Mini-Console: A small, rounded box below the title displaying fake boot logs (e.g., > INIT_KERNEL... OK, > MOUNTING_SHARDS...) in dim gray text.
Action: A full-width, Blood Red (#E63946) button labeled "IGNITE SYSTEM". On hover, it should slide a white sheen effect upwards.
Animation & Feel:
The entire screen should feel like a 'dormant' or 'locked' military terminal waiting for authorization. Use framer-motion for a slow fade-in."
