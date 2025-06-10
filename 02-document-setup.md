---
tags: [accessibility, InDesign, document-setup, properties, metadata]
---
---
tags: [accessibility, InDesign, document-setup, properties, metadata]
---
# Document Setup for Accessibility

← [[01-InDesign-Setup]] | Next: [[03-Styles-and-Tags]] →

## Quick Reference

Document setup checklist:
- [ ] New document created with appropriate page setup
- [ ] Document metadata completed via File > File Info
- [ ] Document language set correctly
- [ ] Master pages configured (if used)
- [ ] Document ready for content creation

**Time estimate**: 10-15 minutes

## Complete Document Setup Guide

### New Document Creation

#### Step-by-step: Create Accessible Document Foundation

1. **Launch InDesign and Create New Document**
   - File → New → Document
   - Intent: Choose "Print" for PDF output or "Web" for digital-first workflows
   - Page Size: Select appropriate size for intended use
   - Orientation: Portrait or Landscape as needed

2. **Configure Page Setup**
   - **Margins**: Set appropriate margins (minimum 12mm for print accessibility)
   - **Columns**: Configure column structure
   - **Bleed**: Add bleed if printing (typically 3mm)
   - **Slug**: Optional area for production notes

3. **Advanced Options (click "More Options" if needed)**
   - **Master Text Frame**: Tick if document will be primarily text-based
   - **Primary Text Frame**: Helps establish proper text flow for accessibility

4. **Click "Create"**

**What success looks like**: New document opens with configured page layout, margins and guides are visible, document ready for content and accessibility setup.

### Document Information and Metadata

#### Step-by-step: Configure Document Metadata for Accessibility

1. **Access Document Information**
   - File → File Info
   - Document Information dialog opens

![[file metadata.png|500]]

2. **Complete Essential Accessibility Fields (Basic Tab)**
   - **Document Title**: Enter descriptive document title (not filename)
     - Example: "Annual Accessibility Report 2024"
     - This appears in screen readers and PDF viewers as the document title
   
   - **Author**: Enter author name(s)
     - Individual or organisation name
     - Used in exported PDFs for identification
     - Note: "Semicolons or commas can be used to separate multiple values"
   
   - **Author Title**: Optional field for author's position/role
     - Example: "Accessibility Manager" or "Communications Director"
   
   - **Description**: Comprehensive description of document content and purpose
     - Multi-line text field for detailed explanation
     - Example: "This annual report details our organisation's accessibility initiatives, compliance measures, and achievements for 2024. It includes performance metrics, case studies, and strategic plans for continued improvement."
     - Critical for screen reader users to understand document context
   
   - **Keywords**: Add relevant accessibility and content keywords
     - Large text area for comprehensive keyword list
     - Separated by commas or semicolons
     - Example: "accessibility, annual report, compliance, WCAG, inclusive design, universal access, disability support"
     - Improves searchability and document categorisation

3. **Additional Recommended Fields**
   - **Creator**: Software information (auto-populated)
   - **Copyright**: Copyright information if applicable

4. **Click "OK" to save metadata**

**What success looks like**: Document properties saved and accessible via File > File Info, metadata will carry through to PDF export, screen readers can access document information.

### Language Configuration

#### Step-by-step: Set Document Language

1. **Set Default Document Language**
   - With no text selected: Character panel → Language dropdown
   - Choose appropriate language (e.g., "English: Australian")
   - This sets the default for all new text

![[character language.png|350]]

2. **Verify Language Settings**
   - Type → Character to open Character panel
   - Ensure correct language appears in Language field
   - This affects hyphenation and spell-checking

**What success looks like**: Correct language selected in Character panel, proper hyphenation and spell-checking active, foundation set for accessible text handling.

### Master Page Considerations

#### Step-by-step: Configure Master Pages for Accessibility

Create a page type for each distinct page-type required. Generally one master page style will be needed for the page containing the H1 tag and then at least one other for the remaining pages.

Example: A document needs to have the title on each page in a banner. In this case, create a master page containing a banner with a H1 title, plus a second master page containing the same banner and title but the text is marked as an artifact to avoid multiple H1 tags.

1. **Access Master Pages**
   - Pages panel → Double-click "A-Master"
   - Master page editing mode active

2. **Set Up Accessible Master Elements**
   - **Page numbers**: Place automatic page numbering
   - **Headers/Footers**: Add consistent navigation elements
   - **Margins and guides**: Establish content boundaries

3. **Configure Master Text Frame (if used)**
   - Ensure proper text frame setup
   - Set appropriate margins and column guides
   - Return to document pages when complete

**What success looks like**: Master pages configured with consistent elements, automatic page numbering in place, text frames properly structured for content flow.

## What Success Looks Like

Your document should now have:
- Proper document foundation with accessibility-friendly page setup
- Complete metadata that will carry through to PDF export
- Correct language settings for proper pronunciation and hyphenation
- Master pages configured for consistent, accessible page elements
- Document ready to receive semantic styles and structured content

## Troubleshooting

**Problem**: "Language not available" Error
**Solution**: Install additional language dictionaries via Creative Cloud. Check Edit > Preferences > Dictionary for available languages.

**Problem**: Master Text Frame Issues
**Solution**: Can be enabled after document creation via Layout > Margins and Columns. Select "Master Text Frame" checkbox and apply.

**Problem**: Metadata Not Appearing in Export
**Solution**: Ensure File > File Info is completed before export. Check PDF export settings include document information.

**Problem**: Cannot access File Info dialog
**Solution**: Ensure document is saved first. Some metadata fields may not be accessible for unsaved documents.

**Problem**: Master page elements appearing on document pages
**Solution**: Check that master page items are properly positioned and not overridden on document pages unless intentional.

**Problem**: Page margins too small for accessibility
**Solution**: Minimum 12mm margins recommended for print accessibility. Adjust via Layout > Margins and Columns.

## Validation Checkpoint

Before proceeding, verify:
- [ ] New document created with appropriate page setup
- [ ] Margins set to minimum 12mm for accessibility
- [ ] Document metadata completed via File > File Info (Title, Author, Description, Keywords)
- [ ] Document language set to "English: Australian"
- [ ] Master pages configured with consistent elements (if used)
- [ ] Automatic page numbering in place (if required)
- [ ] Document ready for semantic style creation

## Next Steps

With your accessible document foundation established, proceed to [[03-Styles-and-Tags]] to create the semantic structure system that will make your content accessible to screen readers.

**Previous**: [[01-InDesign-Setup]] | **Next**: [[03-Styles-and-Tags]]