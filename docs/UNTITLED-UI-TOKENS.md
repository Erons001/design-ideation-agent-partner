# Untitled UI — Design Token Reference

Default design system used by the Design Ideation Agent when no design system is provided.

Source: https://www.untitledui.com
Figma community file: https://www.figma.com/community/file/1020079203222914671

---

## Colours

### Primary (Purple)
primary-25:  #FCFAFF
primary-50:  #F9F5FF
primary-100: #F4EBFF
primary-200: #E9D7FE
primary-300: #D6BBFB
primary-400: #B692F6
primary-500: #9E77ED
primary-600: #7F56D9  (main — buttons, active states, links)
primary-700: #6941C6  (hover)
primary-800: #53389E
primary-900: #42307D

### Gray (Neutral)
gray-25:  #FCFCFD
gray-50:  #F9FAFB
gray-100: #F2F4F7
gray-200: #EAECF0
gray-300: #D0D5DD
gray-400: #98A2B3
gray-500: #667085
gray-600: #475467
gray-700: #344054
gray-800: #1D2939
gray-900: #101828

### Semantic
Error:   #D92D20  (500: #F04438, 300: #FDA29B, 50: #FEF3F2)
Success: #039855  (500: #12B76A, 300: #6CE9A6, 50: #ECFDF3)
Warning: #DC6803  (500: #F79009, 300: #FEC84B, 50: #FFFAEB)

---

## Typography — Inter

Scale:
display-2xl: 72px / lh 90px / tracking -2%
display-xl:  60px / lh 72px / tracking -2%
display-lg:  48px / lh 60px / tracking -2%
display-md:  36px / lh 44px / tracking -2%
display-sm:  30px / lh 38px
display-xs:  24px / lh 32px
text-xl:     20px / lh 30px
text-lg:     18px / lh 28px
text-md:     16px / lh 24px
text-sm:     14px / lh 20px
text-xs:     12px / lh 18px

Weights: 400 regular, 500 medium, 600 semibold, 700 bold

---

## Spacing (4px base)

spacing-1: 4px   spacing-2: 8px   spacing-3: 12px  spacing-4: 16px
spacing-5: 20px  spacing-6: 24px  spacing-8: 32px  spacing-10: 40px
spacing-12: 48px spacing-16: 64px spacing-20: 80px spacing-24: 96px

---

## Border radius

radius-none: 0      radius-sm: 4px   radius-md: 8px
radius-lg: 12px     radius-xl: 16px  radius-2xl: 20px
radius-3xl: 24px    radius-full: 9999px

---

## Shadows

shadow-xs: 0px 1px 2px rgba(16,24,40,0.05)
shadow-sm: 0px 1px 3px rgba(16,24,40,0.10), 0px 1px 2px rgba(16,24,40,0.06)
shadow-md: 0px 4px 8px -2px rgba(16,24,40,0.10), 0px 2px 4px -2px rgba(16,24,40,0.06)
shadow-lg: 0px 12px 16px -4px rgba(16,24,40,0.08), 0px 4px 6px -2px rgba(16,24,40,0.03)
shadow-xl: 0px 20px 24px -4px rgba(16,24,40,0.08), 0px 8px 8px -4px rgba(16,24,40,0.03)
focus-ring: 0px 0px 0px 4px rgba(159,122,237,0.24)

---

## Key component specs

Button/Primary:   44-48px h, bg #7F56D9, radius 8px, text #FFFFFF 14px 600, shadow-xs
Button/Secondary: 44px h, bg #FFFFFF, border 1px #D0D5DD, radius 8px, text #344054 14px 600
Input/Default:    44px h, bg #FFFFFF, border 1px #D0D5DD, radius 8px, padding 10px 14px
Card/Default:     bg #FFFFFF, border 1px #EAECF0, radius 16px, padding 24px, shadow-sm
Badge/Primary:    bg #F4EBFF, text #6941C6, 12px 500, padding 2px 10px, radius 9999px
Progress track:   8px h, bg #EAECF0, radius 9999px
Progress fill:    8px h, bg #7F56D9, radius 9999px