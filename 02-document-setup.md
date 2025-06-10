---
tags: [accessibility, InDesign, document-setup, properties, metadata]
---
# 02-Document-Setup.md

# Document Setup for Accessibility

## Quick Reference
- Create new document with appropriate settings
- Set document information via File > File Info
- Configure language settings for content
- Establish page properties for export compatibility

## New Document Creation

### Step-by-step: Create Accessible Document Foundation

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

**What Success Looks Like:**
- New document opens with configured page layout
- Margins and guides are visible
- Document ready for content and accessibility setup

## Document Information and Metadata

### Step-by-step: Configure Document Metadata for Accessibility

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

**What Success Looks Like:**
- Document properties saved and accessible via File > File Info
- Metadata will carry through to PDF export
- Screen readers can access document information
- Professional document identification established

## Language Configuration

### Step-by-step: Set Document Language

1. **Set Default Document Language**
   - With no text selected: Character panel → Language dropdown
   - Choose appropriate language (e.g., "English: Australian")
   - This sets the default for all new text

![[character language.png|350]]

2. **Verify Language Settings**
   - Type → Character to open Character panel
   - Ensure correct language appears in Language field
   - This affects hyphenation and spell-checking

**What Success Looks Like:**
- Correct language selected in Character panel
- Proper hyphenation and spell-checking active
- Foundation set for accessible text handling

## Master Page Considerations

### Step-by-step: Configure Master Pages for Accessibility

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

**What Success Looks Like:**
- Master pages configured with consistent elements
- Automatic page numbering in place
- Text frames properly structured for content flow

## Validation Checkpoint

### Verify Document Foundation
- [ ] New document created with appropriate page setup
- [ ] Document metadata completed via File > File Info
- [ ] Document language set correctly
- [ ] Master pages configured (if used)
- [ ] Document ready for content creation

### Common Problems to Check
- **Missing metadata**: File > File Info fields left blank
- **Wrong language setting**: Affects accessibility and hyphenation
- **Inappropriate page setup**: Margins too small for accessible reading
- **No master page setup**: Inconsistent page elements

## Next Steps
- Proceed to [[03-Styles-and-Tags]] to create paragraph and character styles
- Set up style-to-tag mappings for export accessibility
- Begin content creation with proper semantic structure

## Troubleshooting

### "Language not available" Error
- Install additional language dictionaries via Creative Cloud
- Check Edit > Preferences > Dictionary for available languages

### Master Text Frame Issues
- Can be enabled after document creation via Layout > Margins and Columns
- Select "Master Text Frame" checkbox and apply

### Metadata Not Appearing in Export
- Ensure File > File Info is completed before export
- Check PDF export settings include document information

## Time Estimate
- New document setup: 2-3 minutes
- Document metadata configuration: 3-5 minutes
- Master page setup: 5-7 minutes
- Total: 10-15 minutes