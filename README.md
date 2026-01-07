🖱️ Tap and Reveal Activity

A modern, grid-based interactive component designed for information discovery. This activity uses a "card-flip" alternative where detailed information slides up over a category tile upon interaction.

🚀 Live Demo

Explore the Tap and Reveal Activity Component Here

✨ Project Overview

The Tap and Reveal Activity is designed for touch and click interactions, making it ideal for mobile-first educational content. It presents high-level categories that, when engaged, reveal deeper bulleted content through a smooth sliding transition.

Key Features

Responsive Grid Layout: Automatically shifts from a single-column layout on mobile to a balanced 2x2 grid on larger screens.

Layered Interaction: * Visual Layer: Features a prominent plus (+) button and a bold category title.

Info Panel: A hidden layer that slides up from the bottom when the card is activated.

Smooth Transitions: Uses a custom cubic-bezier timing function for the panel slide, providing a premium, non-linear movement feel.

Interactive Affordance: * Hover Effects: Cards scale slightly (1.02x) and borders change to brand Teal on hover.

Icon Feedback: The plus button scales and changes color on hover, then fades out as the info panel covers it.

Close Hinting: Includes a "Tap to close" instruction within the revealed panel to guide user navigation.

🛠️ Technical Implementation

State Management: A lightweight toggleReveal(element) JavaScript function handles the activation. Unlike the accordion, this allows for multiple cards to be open simultaneously if the user chooses.

CSS Architecture:

Aspect Ratio: Uses aspect-ratio: 16/10 to ensure uniform card sizes regardless of content length, maintaining grid symmetry.

Absolute Positioning: The info-panel is positioned absolutely at bottom: -100% and transitions to bottom: 0 when the .active class is applied.

Flexbox Layout: Both the visual layer and the info panel use Flexbox for perfect vertical and horizontal centering of text and icons.

📂 Design Tokens

Midnight Blue (#1f2a52): Primary color for text, headers, and hover states of the plus button.

Teal (#00bec7): Accent color for the plus button background, panel borders, and bullet points.

Light Aqua (#d2f0f0): Background color for the revealed info panels to differentiate the "content" state from the "title" state.

Slate Grey (#abb5bf): Used for the "Tap to close" instructional text.

📖 Usage Instructions

To add a new card to the grid, insert the following structure inside the .grid-container:

<div class="reveal-item" onclick="toggleReveal(this)">
    <div class="visual-layer">
        <div class="plus-button">+</div>
        <span class="category-title">Your Title Here</span>
    </div>
    <div class="info-panel">
        <h3>Heading</h3>
        <ul>
            <li>Bullet point information.</li>
        </ul>
        <p class="close-hint">Tap to close</p>
    </div>
</div>


📄 License

MIT License - Developed as part of the accounts-eles UI component library.
