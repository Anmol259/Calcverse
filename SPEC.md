# 3D Multi-Calculator Website Specification

## Project Overview
- **Project Name**: CalcVerse 3D
- **Type**: Single-page web application
- **Core Functionality**: A visually stunning 3D calculator hub featuring multiple calculation tools with a premium glassmorphism aesthetic
- **Target Users**: General users needing quick calculations on mobile and desktop

## UI/UX Specification

### Layout Structure
- **Header**: Floating title with 3D text effect
- **Main Content**: 3D rotating carousel of calculator cards
- **Calculator Display**: Modal overlay with glassmorphism effect
- **Footer**: Minimal credits

### Responsive Breakpoints
- Mobile: < 768px (single column, stacked cards)
- Tablet: 768px - 1024px (2 columns)
- Desktop: > 1024px (3D carousel view)

### Visual Design

#### Color Palette
- **Background**: Deep space gradient - `#0a0a1a` to `#1a1a3a` to `#0f0f2f`
- **Primary Accent**: Electric cyan `#00f5ff`
- **Secondary Accent**: Hot pink `#ff006e`
- **Tertiary Accent**: Golden yellow `#ffd700`
- **Glass Surface**: `rgba(255, 255, 255, 0.05)` with blur
- **Text Primary**: `#ffffff`
- **Text Secondary**: `rgba(255, 255, 255, 0.7)`

#### Typography
- **Font Family**: 'Outfit' (Google Fonts) - modern geometric sans-serif
- **Title**: 800 weight, 3rem with text-shadow
- **Headings**: 600 weight, 1.5rem
- **Body**: 400 weight, 1rem
- **Numbers/Results**: 'Space Mono' for calculator displays

#### Spacing System
- Base unit: 8px
- Card padding: 24px
- Section gaps: 32px
- Button padding: 12px 24px

#### Visual Effects
- **3D Cards**: perspective: 1000px, rotateX/Y transforms
- **Glassmorphism**: backdrop-filter: blur(20px), border: 1px solid rgba(255,255,255,0.1)
- **Glow Effects**: box-shadow with accent colors
- **Hover Animations**: Scale 1.05, enhanced glow
- **Page Load**: Staggered card entrance animations
- **Background**: Animated gradient orbs floating

### Components

#### Calculator Cards (6 total)
1. **Age Calculator** - Icon: 🎂 - Calculates age from birthdate
2. **BMI Calculator** - Icon: ⚖️ - Body Mass Index calculation
3. **Percentage Calculator** - Icon: % - Percentage of value, percentage change
4. **Interest Calculator** - Icon: 💰 - Simple & Compound interest
5. **Tip Calculator** - Icon: 🍽️ - Tip amount per person
6. **Salary Calculator** - Icon: 💼 - Hourly/Daily/Weekly/Monthly conversion

#### Card States
- Default: 3D tilted position, subtle glow
- Hover: Flattened, intensified glow, scale up
- Active/Selected: Full visibility, expanded in modal

#### Input Fields
- Glassmorphism style
- Floating labels
- Focus: Cyan border glow

#### Buttons
- Gradient backgrounds (cyan to pink)
- Rounded corners (12px)
- Hover: Glow effect, slight lift

#### Result Display
- Large monospace numbers
- Animated count-up effect
- Color-coded by result type (green=good, yellow=normal, red=warning)

## Functionality Specification

### Core Features

#### 1. Age Calculator
- Input: Birth date (date picker)
- Output: Years, months, days, total days, next birthday
- Validation: Date cannot be in future

#### 2. BMI Calculator
- Input: Height (cm/ft), Weight (kg/lbs)
- Output: BMI value, category (Underweight/Normal/Overweight/Obese)
- Auto unit conversion

#### 3. Percentage Calculator
- Modes: 
  - X% of Y
  - X is what % of Y
  - % change from X to Y
- Input: Two numbers based on mode

#### 4. Interest Calculator
- Modes: Simple Interest, Compound Interest
- Input: Principal, Rate, Time
- Output: Interest amount, Total amount

#### 5. Tip Calculator
- Input: Bill amount, Tip %, Number of people
- Output: Tip per person, Total per person

#### 6. Salary Converter
- Input: Any salary value, input unit
- Output: All converted time periods

### User Interactions
- Click card → Opens calculator modal with 3D flip animation
- Submit calculation → Animated result reveal
- Close modal → 3D flip back to card view
- Switch calculator modes → Smooth content transition

### Edge Cases
- Invalid inputs → Show inline error messages
- Extreme values → Cap display and show warning
- Empty fields → Disable calculate button

## Acceptance Criteria

### Visual Checkpoints
- [ ] 3D card effect visible on desktop
- [ ] Glassmorphism effect clear on all surfaces
- [ ] Smooth animations on all interactions
- [ ] Mobile responsive without horizontal scroll
- [ ] All 6 calculators accessible and functional

### Functional Checkpoints
- [ ] All calculators produce correct results
- [ ] Input validation works properly
- [ ] Modal opens/closes with animations
- [ ] Works on mobile touch interactions
- [ ] No console errors
