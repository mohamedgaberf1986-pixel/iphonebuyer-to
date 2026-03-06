# Redesign Task: iphonebuyer.to

## Goal
Full visual redesign of index.html — new premium gold/black theme. Keep ALL JavaScript, data, and functionality 100% intact. CSS and visual layer only.

## New Design Direction: Premium Dark Gold
- Background: Deep black (#080808) with subtle gradient
- Primary accent: Rich gold (#D4AF37) and amber (#F59E0B) — replace ALL blue accents (#3b82f6, #60a5fa, #93c5fd, #1b5fc7, #2563eb)
- Cards: Near-black (#111111) with very subtle gold border, gold glow on hover
- Header: Solid black, gold "901" text, white "BUYER" text, gold updated badge
- Tables: Dark rows (#0d0d0d), gold column headers, white price text, gold hover highlight
- Category tabs: Gold underline + gold text on active (not blue)
- All buttons/badges: Gold/amber palette — no blue anywhere
- Fonts: Keep Bebas Neue + DM Sans (already loaded)
- Overall feel: Luxury reseller, premium, clean, confident — like a high-end watch shop

## Specific Content Fixes
1. Change "Updated Feb 27, 2026" → "Updated: March 2026" (find the date string and update it)
2. Add iPhone 15 Pro between iPhone 15 Pro Max section and iPhone 15 section in the iPhones tab. Use the SAME HTML structure as nearby cards. Prices:
   - 128GB: Sealed $310, Open $285
   - 256GB: Sealed $365, Open $335  
   - 512GB: Sealed $420, Open $390
   - Badge: UNLOCKED (same as others)
3. Welcome banner (class="welcome-banner"): Remove the X close button entirely. The 4 condition buttons should be the only way to dismiss it. Make it look like a clear instruction card ("Select a condition below to view prices") not a dismissable banner.
4. Admin panel redesign (keep all JS intact):
   - Apply gold/black theme consistently
   - Admin login card: gold button instead of blue, gold border on input focus
   - Stats bar: slightly larger stat cards with gold accent numbers
   - Sidebar nav items: gold active state (not blue)
   - Add a "Settings" section in admin sidebar that includes a "Change Password" field (just the HTML input + button — wire it to update the ADM_PASS variable and localStorage key "iphb_adm_pass" if it exists, otherwise just show a save button that calls: localStorage.setItem("iphb_adm_pass", newPass) and shows a success toast)

## Isolation Protocol
- Do NOT change any JavaScript functions
- Do NOT change any phone price data
- Do NOT remove any HTML elements (except the welcome banner X button)
- Do NOT change event handlers or data attributes
- Only modify: CSS styles, class names for styling purposes, color values, visual structure

## When Done
1. Save as index.html (overwrite)
2. Run: openclaw system event --text "iphonebuyer.to redesign complete — gold/black premium theme ready for review" --mode now
