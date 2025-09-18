# Git History Cleaner

Generate safe, customizable scripts to clear git repository history while preserving current files and creating proper backups.

**Experience Qualities**:
1. **Trustworthy** - Users feel confident the tool won't accidentally destroy their work through clear warnings and backup creation
2. **Efficient** - Quick generation of ready-to-use scripts without manual editing required
3. **Educational** - Users understand what each command does through clear explanations and optional command breakdown

**Complexity Level**: Light Application (multiple features with basic state)
- Handles user input, script generation, and provides educational context without requiring user accounts or complex state management

## Essential Features

### Script Generation
- **Functionality**: Generate customized git history clearing scripts based on repository name and user preferences
- **Purpose**: Eliminates manual script writing and reduces command errors
- **Trigger**: User enters repository name and clicks generate
- **Progression**: Input repo name → Configure options → Generate script → Copy/download script
- **Success criteria**: Generated script contains correct repo name and all necessary safety commands

### Safety Options
- **Functionality**: Toggle backup creation, confirmation prompts, and branch name customization
- **Purpose**: Prevents accidental data loss and accommodates different workflow preferences
- **Trigger**: User adjusts toggles before script generation
- **Progression**: Default safe settings → User customizes → Settings reflected in generated script
- **Success criteria**: Script reflects all selected safety options accurately

### Command Explanation
- **Functionality**: Breakdown of what each git command does with plain English explanations
- **Purpose**: Educates users about git operations and builds confidence in script safety
- **Trigger**: User clicks on info icons or "Explain Commands" section
- **Progression**: View script → Click explanation → Understand each step → Execute with confidence
- **Success criteria**: Clear, non-technical explanations for each git operation

### Script Output Options
- **Functionality**: Copy to clipboard, download as .sh file, or view in expandable code block
- **Purpose**: Flexible script delivery matching different user workflows and environments
- **Trigger**: User selects preferred output method after generation
- **Progression**: Generate script → Choose output format → Copy/download → Execute in terminal
- **Success criteria**: Script is properly formatted and executable in chosen format

## Edge Case Handling

- **Invalid Repository Names**: Sanitize input and show format requirements (alphanumeric, hyphens, underscores)
- **Empty Input**: Disable generate button and show helpful placeholder text
- **Very Long Repository Names**: Truncate display but preserve full name in script
- **Special Characters**: Strip dangerous characters and warn user about modifications
- **Copy Failures**: Provide fallback manual selection and download option

## Design Direction

The design should feel professional and trustworthy like a developer tool, while remaining approachable enough for less experienced users - clean, technical aesthetic with clear visual hierarchy that emphasizes safety and reliability over flashy interactions.

## Color Selection

Complementary (opposite colors) - Using a blue-green technical palette with orange accents to create trust through cool colors while using warm highlights for important actions and warnings.

- **Primary Color**: Deep Blue `oklch(0.45 0.15 240)` - Communicates reliability and technical professionalism
- **Secondary Colors**: Cool Gray `oklch(0.85 0.02 240)` for backgrounds and Muted Blue `oklch(0.65 0.08 240)` for secondary actions
- **Accent Color**: Warning Orange `oklch(0.68 0.18 45)` for attention-grabbing elements like copy buttons and important warnings
- **Foreground/Background Pairings**:
  - Background (White `oklch(1 0 0)`): Dark Gray text `oklch(0.25 0.02 240)` - Ratio 12.6:1 ✓
  - Card (Light Gray `oklch(0.98 0.01 240)`): Dark Gray text `oklch(0.25 0.02 240)` - Ratio 11.8:1 ✓
  - Primary (Deep Blue `oklch(0.45 0.15 240)`): White text `oklch(1 0 0)` - Ratio 8.9:1 ✓
  - Accent (Warning Orange `oklch(0.68 0.18 45)`): White text `oklch(1 0 0)` - Ratio 5.2:1 ✓

## Font Selection

Technical and clean typeface that conveys precision and reliability while remaining highly readable for code snippets and technical instructions.

- **Typographic Hierarchy**:
  - H1 (App Title): Inter Bold/32px/tight letter spacing
  - H2 (Section Headers): Inter SemiBold/20px/normal spacing
  - Body Text: Inter Regular/16px/relaxed line height
  - Code Blocks: JetBrains Mono Regular/14px/monospace for script output
  - Labels: Inter Medium/14px/slight letter spacing for form elements

## Animations

Subtle functionality-focused animations that provide immediate feedback without drawing attention away from the technical content - smooth state transitions and gentle hover effects reinforce the tool's reliability.

- **Purposeful Meaning**: Smooth transitions communicate system responsiveness and build trust in the tool's precision
- **Hierarchy of Movement**: Primary focus on copy button success states and form validation feedback, minimal decorative motion

## Component Selection

- **Components**: 
  - Card for main script generator container with subtle borders
  - Input with clear labeling and validation states
  - Button variants (primary for generate, secondary for copy actions)
  - Switch components for safety toggles with clear on/off states
  - Collapsible for command explanations to reduce cognitive load
  - Textarea for script output with monospace font
  - Alert components for warnings and success messages

- **Customizations**: 
  - Custom syntax highlighting for bash commands in script output
  - Copy button with animated success state and clipboard integration
  - Info tooltips for technical terms and safety explanations

- **States**: 
  - Buttons show loading, success (copied), and error states clearly
  - Input fields highlight validation errors with helpful messaging
  - Toggles have distinct visual feedback for enabled/disabled
  - Script output area shows generated/empty states

- **Icon Selection**: 
  - Copy icon for clipboard actions
  - Download icon for file export
  - Info/Question icons for help tooltips
  - Check icons for success confirmations
  - Terminal icon for script representation

- **Spacing**: 
  - Consistent 4/6/8 Tailwind spacing scale
  - Generous padding (p-6/p-8) for main containers
  - Tight spacing (gap-2/gap-4) for related form elements
  - Larger gaps (gap-6/gap-8) between distinct sections

- **Mobile**: 
  - Single column layout with full-width cards
  - Larger touch targets (min 44px) for buttons and toggles
  - Collapsible sections for script output to save vertical space
  - Simplified button groupings with priority-based stacking