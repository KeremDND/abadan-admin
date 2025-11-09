# Unused Assets and Images Report

## Summary

- **Total images found**: 677
- **Used images**: ~110
- **Unused images**: ~640

## Categories of Unused Assets

### 1. CDN Optimized Images (`public/cdn/`)
**Status**: ~530 files
- These are optimized versions of product images in multiple formats (AVIF, WebP, JPG) and sizes (480, 768, 1080, 1440)
- **Recommendation**: Keep if using an image optimization system. Otherwise, these can be deleted as they're not directly referenced in code.

### 2. Screenshots
**Status**: 1 file
- `public/Screenshot 2025-08-28 at 12.07.03.png`
- **Recommendation**: **Safe to delete** - this is a development screenshot

### 3. Old Hero Background Images
**Status**: ~12 files
- Multiple versions of hero backgrounds in different sizes:
  - `abadan-haly-home-page-background-1280.*`
  - `abadan-haly-home-page-background-1920.*`
  - `abadan-haly-home-page-background-2560.*`
  - `abadan-haly-home-page-background.*` (base versions)
- **Recommendation**: **Safe to delete** if not using responsive `<picture>` elements. Currently using single `abadan haly main hero.jpg`

### 4. Duplicate/Unused Product Images
**Status**: ~25 files
- Duplicate at root: `public/Images/abadan-haly-Nusay- Cream- 2048- carpet.jpg` (also exists in `Halylar/`)
- Images in `Halylar/` folders not referenced in `data/products.ts`:
  - Various Cream, Grey, Dark Grey variants not in product catalog
- **Recommendation**: Review before deleting - might be future products or backups

### 5. Old Page Images
**Status**: ~3 files
- `public/Images/page-images/Abadan Haly collab page.png` (PNG version - using JPG)
- `public/Images/page-images/Abadan Haly home page backgroound 2.png` (typo in filename)
- `public/Images/page-images/Abadan Haly home page backgroound.png` (typo in filename)
- **Recommendation**: **Safe to delete** - using JPG version and these have typos

### 6. Other Unused Images
**Status**: ~1 file
- `public/Images/Abadan Haly website background.jpg`
- **Recommendation**: Review - might be a fallback or old asset

## Files Safe to Delete Immediately

1. `public/Screenshot 2025-08-28 at 12.07.03.png`
2. `public/Images/page-images/Abadan Haly collab page.png`
3. `public/Images/page-images/Abadan Haly home page backgroound 2.png`
4. `public/Images/page-images/Abadan Haly home page backgroound.png`
5. All files in `public/cdn/` if not using image optimization (verify first)

## Files to Review Before Deleting

1. Unused product images in `public/Images/Halylar/` - might be future products
2. Old hero background variants - might be needed for responsive images
3. `public/Images/Abadan Haly website background.jpg` - check if used as fallback

## Estimated Space Savings

- CDN directory: ~500MB+ (if deleted)
- Screenshots: ~1MB
- Old backgrounds: ~50MB
- Duplicate images: ~10MB

**Total potential savings**: ~560MB+ (if CDN directory is not needed)

## Next Steps

1. ✅ Review this report
2. ⏳ Delete confirmed unused files
3. ⏳ Verify CDN directory usage
4. ⏳ Update `.gitignore` if needed
5. ⏳ Document image optimization strategy

