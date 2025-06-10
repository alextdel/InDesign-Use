---
tags: [accessibility, InDesign, pdf-export, adobe-pdf, accessibility-options]
---
# PDF Export for Accessibility

← [[05-Reading-Order]] | Next: [[07-Validation-Testing]] →

## Quick Reference

PDF export checklist:
- [ ] Adobe PDF (Print) preset selected
- [ ] Accessibility options enabled
- [ ] Structure and tags created
- [ ] Bookmarks from headings included
- [ ] Image quality balanced with file size
- [ ] Export settings verified before final export

**Time estimate**: 10-15 minutes

## Complete Export Guide

### Pre-Export Checklist

Before exporting, verify your document is ready:
- [ ] All styles have proper export tags assigned
- [ ] Articles panel structure is complete and logical
- [ ] Images have appropriate alt-text or are marked decorative
- [ ] Document properties (title, author) are set
- [ ] Reading order has been tested and verified

### Export Process Overview

**Critical principle**: The export settings determine whether your accessibility work is preserved in the final PDF. Incorrect settings can eliminate all accessibility features.

### Accessing Export Settings

1. **Open Export dialogue**:
   - File → Export (Ctrl+E)
   - **Format**: Adobe PDF (Print) - *Always use this option*
   - **File name**: Use descriptive name ending in .pdf
   - Click **Save**

2. **Why Adobe PDF (Print)**:
   - Provides complete control over accessibility options
   - Maintains all InDesign structure and tagging
   - Adobe PDF (Interactive) can lose accessibility features

### General Export Settings

#### Adobe PDF Preset
1. **Preset selection**:
   - **Adobe PDF Preset**: `[High Quality Print]` or `[PDF/X-4:2008]`
   - Avoid "Smallest File Size" - compromises accessibility
   - Custom settings provide most control

![[ExportQuality1.png|500]]

1. **Compatibility**:
   - **Compatibility**: Acrobat 7 (PDF 1.6) or higher
   - Higher versions support better accessibility features
   - Acrobat 2017 (PDF 1.7) recommended for current accessibility standards

![[ExportCompatibility.png|500]]

#### Pages and Spreads
1. **Pages settings**:
   - **All Pages**: Usually selected for complete document
   - **Range**: Specify if exporting partial document
   - **Spreads**: Generally leave unchecked for accessibility
   
2. **Include settings**:
   - **Hyperlinks**: ✓ Check this - essential for accessible navigation
   - **Non-printing Objects**: Check if they contain accessibility information

**Why avoid spreads**: Screen readers process single pages more effectively than spreads.

**Why include hyperlinks**: Maintains navigation structure and cross-references that screen readers rely on for document navigation.

![[ExportSettings1.svg|550]]
### Compression Settings

#### Balancing Quality and Accessibility
1. **Images compression**:
   - **Color Images**: JPEG, Maximum quality for important images
   - **Grayscale Images**: JPEG, Maximum or High quality
   - **Monochrome Images**: CCITT Group 4 compression

2. **Resolution settings**:
   - **Color Images**: 150-300 PPI (higher for detailed charts/diagrams)
   - **Grayscale Images**: 150-300 PPI
   - **Monochrome Images**: 600-1200 PPI
  > **Note:** I use 300ppi **but** ensure no upscaling - i.e. dragging images bigger than they are captured.

**Accessibility consideration**: Poor image quality can make charts and diagrams unreadable for users with low vision.

![[ExportCompressionSettings.png|550]]
### Marks and Bleeds

#### Standard Settings for Accessible Documents
1. **Printer's Marks**: All off (unless printing)
2. **Bleed and Slug**: Use document bleed settings
3. **Include**: Structure for accessibility (checked)

![[MarksAndBleeds.png|500]]
### Output Settings

#### Color Management
1. **Color Conversion**: Convert to Destination
2. **Destination**: sRGB IEC61966-2.1 (for digital documents)
3. **PDF/X Profile**: None (unless specific print requirements)
> **Note:** The colour management settings are recommended online, but I have never changed these from default InDesign settings.

![[ExportOutputSettings.png|500]]
**Accessibility note**: Consistent colour space helps with contrast validation and colour accessibility testing.

### Advanced Export Settings

#### Options
1. **Document title / File Name** - select as required
	- *Document Title* setting comes from metadata set in File Info under File menu
	- Hover over the '*i*' to see the Document Title set in File Info.
2. Language - check this is as required - will be used by screen readers.

![[ExportAdvancedSettings.png|500]]
### Essential Accessibility Options

**In the General tab of Export Adobe PDF dialogue:**

1. **Core accessibility settings**:
   - **Create Tagged PDF**: ✓ Checked (essential - this is the foundation)
   - **Create Acrobat Layers**: Usually unchecked for accessibility
   - **Hyperlinks**: ✓ Checked (essential for navigation)
   - **Bookmarks**: ✓ Checked (improves navigation)

2. **Export Layers**: Set to "Visible & Printable Layers"

#### Settings NOT in PDF Export Dialogue

**These must be configured BEFORE export:**

1. **Articles Panel structure**:
   - Location: Window → Articles
   - Set up reading order before export
   - InDesign uses this automatically if Articles exist

2. **Object Export Options** (alt-text, etc.):
   - Location: Object → Object Export Options
   - Configure alt-text for images before export
   - Set image export settings per object

3. **Reading Order control**:
   - Location: Window → Articles (preferred method)
   - Or: Export → EPUB/HTML → Content Order → "Same as Articles Panel"
   - Note: PDF export uses Articles automatically if they exist

#### Why Create Tagged PDF is Critical
Without "Create Tagged PDF" checked, your document will have:
- No semantic structure for headings, lists, etc.
- No reading order information
- Limited accessibility for screen readers
- Failed accessibility compliance

### Security Settings

#### Accessibility-Compatible Security
1. **Security method**: Password Security or Certificate Security
2. **Permissions settings**:
   - **Enable copying of text**: Must be allowed for screen readers
   - **Enable text access**: Must be allowed for accessibility
   - **Allow changes**: Consider document workflow needs

**Critical**: Never disable text access or copying - this breaks screen reader compatibility.

### Interactive Elements

#### Bookmarks and Hyperlinks
1. **Bookmarks section**:
   - **Create Bookmarks**: From Table of Contents or Headings
   - **Include Text on Hidden Layers**: Usually unchecked
   - **Create PDF Bookmarks**: Provides navigation for screen readers

2. **Hyperlinks**:
   - **Include Hyperlinks**: ✓ Checked
   - **Include Cross-References**: ✓ Checked
   - Maintains navigation functionality in PDF

**What success looks like**: PDF contains functional bookmarks matching document headings and working hyperlinks.

### Export Process

#### Final Export Steps
1. **Review all settings**:
   - General: Adobe PDF (Print) preset
   - Compression: Appropriate quality levels
   - Advanced: Tagged PDF and structure options enabled
   - Security: Text access permitted

2. **Save preset for future use**:
   - Click "Save Preset" at bottom of dialog
   - Name: "Accessible PDF Export"
   - Saves all your accessibility settings

3. **Export the PDF**:
   - Click "Export"
   - Monitor progress bar
   - Check for any error messages

#### Post-Export Verification
1. **Quick accessibility check**:
   - Open PDF in Acrobat or Reader
   - Try using Tab key to navigate
   - Test screen reader if available

2. **File properties check**:
   - File → Properties in Acrobat
   - Verify Title, Author fields populated
   - Check "Tagged PDF: Yes"

## What Success Looks Like

Your exported PDF should have:
- "Tagged PDF: Yes" in document properties
- Functional bookmarks from document headings
- Working hyperlinks and cross-references
- Preserved alt-text on images
- Logical reading order maintained from Articles panel
- Good image quality for charts and diagrams
- Reasonable file size for intended distribution

## Troubleshooting

**Problem**: Export fails with error message
**Solution**: Check for overset text, missing fonts, or corrupt images. Resolve issues in InDesign before re-exporting.

**Problem**: PDF shows "Tagged PDF: No"
**Solution**: Ensure "Create Tagged PDF" was checked in General settings (not Advanced). Re-export with correct settings.

**Problem**: Bookmarks missing from PDF
**Solution**: Check "Bookmarks" checkbox in General tab. Ensure document has proper heading styles applied and TOC generated.

**Problem**: Images appear pixelated in PDF
**Solution**: Adjust compression settings in Compression tab. Check source image resolution in InDesign.

**Problem**: File size too large
**Solution**: Reduce image quality in Compression tab. Consider optimising images before placing in InDesign.

**Problem**: Hyperlinks don't work in PDF
**Solution**: Verify "Hyperlinks" was checked in General tab. Test links in InDesign before export.

**Problem**: Reading order incorrect in PDF
**Solution**: Check Articles panel structure in InDesign before export. InDesign uses Articles panel automatically if content exists there.

**Problem**: Alt-text missing from images
**Solution**: Set alt-text in Object → Object Export Options before export. This must be done in InDesign, not in export dialogue.

**Problem**: Security prevents screen reader access
**Solution**: In Security tab, ensure text access is permitted for screen readers.

### Pre-Export Checklist
Before each export, verify:
- [ ] Document saved with latest changes
- [ ] All fonts available and not missing
- [ ] No overset text indicators
- [ ] Articles panel structure complete (if using)
- [ ] Alt-text set on images via Object Export Options
- [ ] All images properly linked
- [ ] Export preset configured correctly

### Export Settings Summary
**Essential settings for accessibility**:
- Adobe PDF (Print) format
- **General tab**: Create Tagged PDF ✓
- **General tab**: Hyperlinks ✓
- **General tab**: Bookmarks ✓
- **General tab**: Export Layers: "Visible & Printable Layers"
- **Security tab**: Enable text access for screen readers

### Pre-export Setup (in InDesign document)
- Articles panel configured for reading order
- Object Export Options set for images (alt-text)
- Proper heading styles applied
- TOC generated if using bookmarks

## Validation Checkpoint
After export, verify:
- [ ] PDF opens without errors
- [ ] Document properties show "Tagged PDF: Yes"
- [ ] Bookmarks appear and function correctly
- [ ] Hyperlinks work as expected
- [ ] File size is reasonable for distribution
- [ ] Basic navigation with Tab key functions
- [ ] Document title appears correctly in PDF viewer

## Advanced Export Tips
**Workflow efficiency**:
- Save custom export preset for consistent results
- Create export checklist specific to your organisation
- Test export settings with sample documents first

**Quality control**:
- Compare exported PDF structure to InDesign Articles panel
- Test PDFs on different devices and PDF readers
- Maintain export settings documentation for team use
## Next Steps

With your accessible PDF successfully exported, proceed to [[07-Validation-Testing]] to learn comprehensive testing methods that verify your PDF meets accessibility standards and works properly with assistive technologies.

**Previous**: [[05-Reading-Order]] | **Next**: [[07-Validation-Testing]]