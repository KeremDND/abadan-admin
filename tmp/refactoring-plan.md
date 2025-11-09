# Refactoring Plan

## Current Issues Found:
1. App.tsx imports from wrong paths (components/Header vs components/layout/Header)
2. Duplicate components exist (Hero.tsx vs home/Hero.tsx, etc.)
3. i18n imports need fixing (./i18n vs ./lib/i18n)
4. Components partially organized but inconsistent

## Strategy:
1. Create index files for cleaner imports
2. Remove duplicate components (keep organized versions)
3. Fix all import paths
4. Clean up unused code
5. Test build

## Files to fix:
- src/App.tsx - fix imports
- src/main.tsx - fix i18n import (already done)
- src/components/layout/LanguageToast.tsx - fix i18n import (already done)
- src/components/layout/LanguageSwitcher.tsx - fix i18n import (already done)
- src/components/gallery/Gallery.tsx - rename NewGallery to Gallery (already done)

## Duplicates to remove:
- src/components/Hero.tsx (keep home/Hero.tsx)
- src/components/Gallery.tsx (keep gallery/Gallery.tsx)
- src/components/Collaboration.tsx (keep collaboration/Collaboration.tsx)
- src/components/ColorFilterGrid.tsx (check if used)
