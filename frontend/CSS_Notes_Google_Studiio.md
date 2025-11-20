Based on the index.html configuration and the Tailwind classes used throughout your React components, here is the comprehensive breakdown of the typography system for The Ashen Guard / Phoenix ORCH Lite.
1. Font Families
The application uses a distinct mix of sci-fi and "sacred" typography imported from Google Fonts.
Font Name	Usage & Context
Rajdhani	Primary System Font. Used for the <body>, general UI containers, Agent lists, and standard interface text. It provides the "technical/HUD" aesthetic.
Orbitron	Display & Headers. Used for the main logo ("PHOENIX ORCH"), Blade titles (e.g., "THE LEGION"), Button labels ("SPAWN NEW GUARD"), and modal headers. It has a futuristic, wide stance.
Montserrat	Input & Readability. Used specifically for the Chat Input Textarea (App.tsx) and the Tribute Poem (tribute/eternal.tsx) to ensure high readability for longer text blocks.
Cormorant Garamond	Sacred Text. Used for the Conscience Gauge status messages (e.g., "RETRIBUTION WHISPERS") to contrast the digital tech with an "ancient/eternal" feel.
Cinzel	Ritual Text. Available for sacred titles and headers, often used in "Sacred Knowledge" locks or ritual modals.
Monospace	Data & Terminal. (Browser default). Used for Digital Twin telemetry (numbers), Console/CLI, Code snippets, and JSON outputs in the Omniblade.
2. Font Sizes
The app relies on Tailwind CSS utility classes. Here is how they map to specific elements:
Display & Titles
text-8xl (96px) & text-7xl (72px): The massive "PHOENIX ORCH" title on the Intro/Ignition screen.
text-6xl (60px): Large headings in the Singularity Clock and Mobile Intro.
text-5xl (48px): Tribute poem headers.
text-4xl (36px): Mobile titles.
text-2xl (24px): Modal headers (e.g., "PHOENIX PRIME SETTINGS"), Main Header Logo.
UI Elements
text-xl (20px): Section headers within modals.
text-lg (18px): "IGNITE SYSTEM" button text, "PERSISTENCE: ACTIVE" status in Artifacts blade.
text-base (16px): Agent Names (e.g., "Alpha-Sentinel"), Chat message body text.
text-sm (14px): Chat input text, Digital Twin telemetry labels, Agent roles, List items.
text-xs (12px):
Button labels (e.g., "EXECUTE PROTOCOL", "PUSH").
Metadata tags (e.g., "Rust", "Online").
Tool descriptions in the Arsenal Forge.
text-[10px]:
Specific micro-labels (e.g., "PHOENIX // LIVE FEED").
Timestamps in chat logs.
"Protected" status badges.
text-[9px]:
"The Ashen Guard" subtitle in the header.
Deeply nested metadata (e.g., file status in Project Blade).
3. Visual Effects
Glow/Pulse: Many fonts (especially Orbitron and Monospace) are paired with animate-pulse or drop-shadow-[...] to simulate neon signs or CRT monitors.
Tracking: tracking-widest (letter-spacing) is frequently applied to Orbitron headers (e.g., THE LEGION) to enhance the cinematic, military feel.
