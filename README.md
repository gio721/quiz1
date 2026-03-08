# quiz1
1. Prompt 1: Planning Prompt

Prompt used: "I am building a responsive website from scratch without frameworks. Can you provide a high-level plan to implement responsive breakpoints for a 4-column grid and a hero section that needs to stack on mobile devices?"

Two things I accepted from the plan:

Using display: flex with flex-direction: column for the hero section on mobile to ensure the text and image stack vertically.

Implementing a mobile-first or desktop-first approach using @media queries at specific pixel widths like 600px and 900px.

One thing I rejected: The AI suggested using a library like Bootstrap for the grid. I rejected this because the project requirements explicitly state to use "HTML and CSS only" and "no frameworks".

2. Prompt 2: Debug Prompt

Problem Statement: The hero card was overlapping the hero text on desktop instead of aligning to the far right.

CSS Snippet I asked about:

CSS
.hero { display: flex; padding: 20px; }
.hero-card { width: 240px; border: 1px solid #ddd; }
Most important part of AI response: "To push the hero-card to the right in a flex container, use justify-content: space-between on the parent .hero class, or apply margin-left: auto to the .hero-card itself."

What I changed afterward: I added justify-content: space-between; to the .hero class and ensured the container had a defined max-width so the gap was visible.

3. Verification List

Viewport sizes tested:

1200px (Desktop): Verified 4-column grid and logo/nav alignment.

768px (Tablet): Verified the grid shifted to 2 columns.

375px (Mobile): Verified the hero section stacked vertically and the grid became a single column.

Visual check: I confirmed that no content touched the screen edges by verifying the horizontal padding in the .container class.
