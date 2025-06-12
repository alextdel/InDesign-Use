---
tags: [accessibility, validation, testing, PAC-2024, acrobat-pro, NVDA, screen-reader]
---
# Validation and Testing for Accessible PDFs

← [[06-pdf-export]] | [[00-navigation-guide]] →

## Quick Reference

Validation testing checklist:
- [ ] PAC 2024 automated validation passed
- [ ] Adobe Preflight accessibility profiles completed
- [ ] Acrobat Pro accessibility checker completed
- [ ] Common errors identified and fixed
- [ ] NVDA screen reader testing performed
- [ ] Manual navigation testing completed
- [ ] Final accessibility review documented

**Time estimate**: 30-60 minutes (depending on document complexity and errors found)

## Complete Validation Guide

### Testing Strategy Overview

**Four-tier testing approach**:
1. **Automated validation** - PAC 2024 for standards compliance
2. **Professional preflight** - Adobe Preflight for PDF/UA and accessibility standards
3. **Professional tools** - Acrobat Pro for detailed analysis and fixes
4. **Real-world testing** - NVDA screen reader for user experience

**Key principle**: Automated tools catch technical errors, professional tools provide detailed analysis and fixes, but human testing with assistive technology reveals usability issues.

### PAC 2024 Installation and Setup

#### Installing PAC 2024
1. **Download PAC 2024**:
   - Visit [pac.pdf-accessibility.org](https://pac.pdf-accessibility.org)
   - Download latest version (PAC 2024)
   - Free tool from PDF/UA Foundation

2. **Installation process**:
   - Unzip the downloaded PAC 2024 package into a convenient location
   - Choose the PAC 2024 directory
   - Find and run (double-click) on the PAC application
   - For convenience, pin the PAC application to the Taskbar or Start menu

3. **First launch**:
   - Open PAC 2024
   - Interface shows drag-and-drop area for PDF files
   - No additional configuration required

![[Pasted image 20250608142336.png|500]]

#### Understanding PAC 2024 Interface
**Main sections**:
- **File area**: Drag PDFs here for testing
- **Results panel**: Shows validation outcomes
- **Details panel**: Explains specific errors
- **Preview**: Shows PDF structure

### PAC 2024 Validation Process

#### Running Basic Validation
1. **Load your PDF**:
   - Drag PDF file into PAC 2024 window
   - Or File → Open to browse for file
   - PAC loads and begins analysis automatically

2. **Review validation results**:
   - **Green tick**: PDF passes PAC validation
   - **Red cross**: PDF fails with errors
   - **Orange warning**: Issues found but not critical failures

3. **Examine error details**:
   - Click on any error in results list
   - Details panel explains the specific issue
   - Preview shows location of problem in document

![[PAC Check Panel 1.png|550]]

#### Common PAC 2024 Errors and Fixes

**Error**: "Document is not tagged"
**Meaning**: PDF lacks accessibility structure
**Fix**: Re-export from InDesign with "Create Tagged PDF" enabled

**Error**: "Figure without alternative text"
**Meaning**: Image missing alt-text
**Fix**: Add alt-text in InDesign Object Export Options, re-export

**Error**: "Suspect heading"
**Meaning**: Text looks like heading but lacks proper tagging
**Fix**: Apply proper heading style with export tag in InDesign

**Error**: "Document title missing"
**Meaning**: PDF properties don't include title
**Fix**: Set title in InDesign File Info, re-export

**Error**: "Language not specified"
**Meaning**: Document language not declared
**Fix**: Set document language in InDesign preferences and document properties

**Error**: "Insufficient colour contrast"
**Meaning**: Text doesn't meet contrast requirements
**Fix**: Adjust colours in InDesign to meet 4.5:1 ratio minimum

> **Note:** WCAG check for "Distinguishable" may fail when text elements are placed above transparent or multi layer graphics. A manual check should be carried out.

### Adobe Preflight for Accessibility

#### Accessing Adobe Preflight
Adobe Preflight provides comprehensive PDF analysis including dedicated accessibility profiles that complement PAC 2024 testing.

1. **Open PDF in Acrobat Pro**:
   - Launch Adobe Acrobat Pro
   - Open your exported PDF file

2. **Access Preflight tool**:
   - **Tools** → **Preflight** (pin tool to toolbar for frequent use)
   - Or **Ctrl+Shift+X** (Windows) / **Cmd+Shift+X** (Mac)
   - Or search for "Preflight" in Tools panel

#### Accessibility-Specific Preflight Profiles

**Key Accessibility Profiles**:
1. **PDF/UA-1 compliance** - Universal Accessibility standard
2. **Accessible PDF** - General accessibility requirements
3. **WCAG 2.0 (PDF)** - Web Content Accessibility Guidelines for PDF
4. **Custom accessibility profiles** - Organisational specific requirements

#### Running PDF/UA-1 Compliance Check

**PDF/UA-1 (Universal Accessibility) is the ISO standard for accessible PDFs**:

1. **Select PDF/UA-1 profile**:
   - In Preflight panel, expand **Accessibility** section
   - Select **PDF/UA-1 compliance**
   - Click **Analyse** (not Analyse and fix - this preserves document integrity)

2. **Review results**:
   - **Green tick**: Requirement passed
   - **Red cross**: Critical failure requiring attention
   - **Yellow warning**: Issue that should be reviewed
   - **Blue "i" icon**: Informational note

3. **Interpret PDF/UA-1 results**:
   - **Document structure requirements**: Tagged content, logical structure
   - **Content requirements**: Alt-text, language specification
   - **Navigation requirements**: Bookmarks, reading order
   - **Presentation requirements**: Colour contrast, font embedding

#### Understanding Preflight vs PAC 2024

**Preflight advantages**:
- More detailed error reporting with specific page locations
- Built-in fix capabilities for many issues
- Integration with Acrobat Pro editing tools
- Additional profile options beyond basic compliance

**PAC 2024 advantages**:
- Faster, streamlined interface
- Specific PDF/UA expertise
- Independent verification tool
- Free and regularly updated

**Recommended workflow**: Use both tools complementarily:
1. PAC 2024 for quick initial validation
2. Adobe Preflight for detailed analysis and fixes

#### Common Preflight Accessibility Fixes

**Missing structure elements**:
- Preflight can identify untagged content
- Use "Analyse and fix" cautiously - review changes
- Manual tagging often more reliable than automatic fixes

**Font embedding issues**:
- Preflight identifies non-embedded fonts
- Can automatically embed fonts if licensing permits
- Critical for accessibility tool compatibility

**Colour space problems**:
- Identifies colour models that may cause accessibility issues
- Can convert to appropriate colour spaces
- Important for consistent rendering across devices

**Metadata issues**:
- Checks document title, language, and accessibility flags
- Can automatically update some metadata
- Ensures proper document identification for assistive technology

#### Custom Accessibility Profiles

**Creating organisational profiles**:
1. **Duplicate existing profile**:
   - Right-click **PDF/UA-1 compliance**
   - Select **Duplicate profile**
   - Rename for your organisation

2. **Customise checks**:
   - Add organisation-specific requirements
   - Remove checks not relevant to your workflow
   - Set custom colour contrast requirements

3. **Save and share**:
   - Export profile for team use
   - Import into other Acrobat Pro installations
   - Maintain consistency across projects

#### Preflight Reporting

**Generate accessibility reports**:
1. After running Preflight analysis
2. Click **Create report** button
3. Choose report format (PDF or XML)
4. Include in project documentation

**Report contents**:
- Summary of compliance status
- Detailed error listings with page numbers
- Specific recommendations for fixes
- Technical details for development teams

### Acrobat Pro Accessibility Checker

#### Accessing Acrobat Pro Tools
1. **Open PDF in Acrobat Pro**:
   - Launch Adobe Acrobat Pro
   - Open your exported PDF file

2. **Run Accessibility Checker**:
   - **All tools** → **Prepare for Accessibility** → **Check for Accessibility**
   - Or use the search box in Tools and type "accessibility"

![[AccessibilityCheckerSettings.png|550]]

#### Configure Accessibility Checker Options

**Report Options**:
- **Create accessibility report**: ✓ Check this (recommended)
- **Folder**: Choose location to save report
- **Attach report to document**: Optional - useful for sharing results

**Page Range**:
- **All pages in document**: Usually selected
- **Pages from**: Use if checking specific pages only

**Checking Options** (shows 31 of 32 categories available):
Default categories include:
- **Document**: Core document structure checks
  - Accessibility permission flag is set
  - Document is not image-only PDF
  - Document is tagged PDF
  - Document structure provides logical reading order
  - Text language is specified
  - Document title is showing in title bar
  - Bookmarks are present in large documents
  - Document has appropriate colour contrast

**Additional categories** (access via dropdown):
- **Page Content**: Text, images, and content accessibility
- **Forms**: Form field accessibility (if applicable)
- **Tables**: Table structure validation (if applicable)
- **Lists**: List structure and formatting
- **Headings**: Heading hierarchy and structure

#### Running the Check
1. **Recommended settings**:
   - Keep all default checks selected
   - Create accessibility report: ✓
   - All pages in document: ✓
   - Show this dialogue when Checker starts: ✓ (for future use)

2. **Click "Start Checking"** to begin analysis

#### Interpreting Accessibility Checker Results

**The Accessibility Checker Panel Structure**:

![[Pasted image 20250608150849.png|500]]

**Document Section** (shows overall document compliance):
- **Accessibility permission flag** - Passed ✓
- **Image-only PDF** - Passed ✓ 
- **Tagged PDF** - Passed ✓
- **Logical Reading Order** - Needs manual check ⚠️
- **Primary language** - Passed ✓
- **Title** - Passed ✓
- **Bookmarks** - Passed ✓
- **Colour contrast** - Needs manual check ⚠️

**Expandable Sections** (click arrow to expand):
- **Page Content** - Text and image accessibility
- **Forms** - Form field accessibility (if applicable)
- **Alternate Text** - Alt-text for images and graphics
- **Tables** - Table structure and headers
- **Lists** - List formatting and structure
- **Headings** - Heading hierarchy and tagging

#### Understanding Result Types

**Passed** (White text):
- Requirement successfully met
- No action needed

**Failed** (Red text with X):
- Critical accessibility issue
- Must be fixed for compliance
- Click item for fix options

**Needs manual check** (Blue question mark icon):
- Requires human verification
- Automatic detection not possible
- Review manually and mark as appropriate

#### Working with Results

**Expanding sections**:
1. Click arrow next to section name (Page Content, Forms, etc.)
2. View detailed results for that category
3. Address any failed items or manual checks

**Common "Needs manual check" items**:
- **Logical Reading Order**: Verify content flows logically
- **Colour contrast**: Check text meets contrast requirements
- **Meaningful sequence**: Ensure content order makes sense
- **Alternative text**: Verify alt-text accurately describes images

**Fixing issues**:
1. Right-click on failed items for fix options
2. Some fixes available directly in results panel
3. Complex issues may require accessibility tools

#### Priority Order for Fixes
1. **Critical failures** (red X) - Fix first
2. **Manual checks** for core accessibility:
   - Logical reading order
   - Alt-text accuracy
   - Colour contrast
3. **Secondary manual checks**:
   - Content sequence
   - Language identification

#### Common Acrobat Pro Quick Fixes

**Missing alt-text**:
1. Right-click error in results → Fix
2. Enter appropriate alt-text in dialogue
3. Click OK to apply

**Reading order issues**:
1. **All tools** → **Prepare for Accessibility** → **Reading Order**
2. Click "Show Order Panel" to see content sequence
3. Drag elements to correct order
4. Click "Show Order Panel" again to hide when done

**Heading structure problems**:
1. **All tools** → **Prepare for Accessibility** → **Reading Order**
2. Select text that should be heading
3. Click appropriate heading button (H1, H2, etc.) in Reading Order panel
4. Apply to fix tagging

**Table header issues**:
1. Right-click table → Table Editor
2. Select header row cells
3. Right-click → Table Cell Properties
4. Set "Scope" to "Column" or "Row" as appropriate

#### Alternative Access Method
If you can't locate tools easily:
- Use the search box in the Tools panel
- Type "accessibility" to find all accessibility-related tools
- Pin frequently used tools to the toolbar for quick access

#### Understanding Check Categories
**Critical checks for accessible PDFs**:
- Document is tagged PDF (must pass)
- Document structure provides logical reading order
- Text language is specified
- Document title showing in title bar
- Appropriate colour contrast

**Best practice checks**:
- Bookmarks present in large documents
- Accessibility permission flag set
- Document not image-only PDF

#### Understanding the Accessibility Report

**Report Summary Section**:
The report provides an overview of results:
- **Needs manual check**: Items requiring human verification
- **Passed manually**: Manual checks that have been verified
- **Failed manually**: Manual checks that failed verification
- **Skipped**: Checks not applicable to this document
- **Passed**: Automated checks that passed
- **Failed**: Critical issues requiring fixes

#### Detailed Report Categories

**Document Section** - Core accessibility requirements:
- **Accessibility permission flag**: Passed ✓
- **Image-only PDF**: Passed ✓
- **Tagged PDF**: Passed ✓
- **Logical Reading Order**: Needs manual check ⚠️
- **Primary language**: Passed ✓
- **Title**: Passed ✓
- **Bookmarks**: Passed ✓
- **Colour contrast**: Needs manual check ⚠️

**Page Content Section** - Content accessibility:
- **Tagged content**: All page content is tagged
- **Tagged annotations**: All annotations are tagged
- **Tab order**: Tab order is consistent with structure order
- **Character encoding**: Reliable character encoding is provided
- **Tagged multimedia**: All multimedia objects are tagged
- **Screen flicker**: Page will not cause screen flicker
- **Scripts**: No inaccessible scripts
- **Timed responses**: Page does not require timed responses
- **Navigation links**: Navigation links are not repetitive

**Forms Section** (if applicable):
- **Tagged form fields**: All form fields are tagged
- **Field descriptions**: All form fields have description

**Alternate Text Section** - Image accessibility:
- **Figures alternate text**: Figures require alternate text
- **Nested alternate text**: Alternate text that will never be read
- **Associated with content**: Alternate text must be associated with some content
- **Hides annotation**: Alternate text should not hide annotation
- **Other elements alternate text**: Other elements that require alternate text

**Tables Section** - Table structure:
- **Rows**: TR must be a child of Table, THead, TBody, or TFoot
- **TH and TD**: TH and TD must be children of TR
- **Headers**: Tables should have headers
- **Regularity**: Tables must contain the same number of columns in each row and rows in each column
- **Summary**: Tables must have a summary

**Lists Section** - List formatting:
- **List items**: LI must be a child of L
- **Lbl and LBody**: Lbl and LBody must be children of LI

**Headings Section** - Document structure:
- **Appropriate nesting**: Appropriate nesting

#### Action Required for Manual Checks

**Logical Reading Order** - Manual verification needed:
1. Open the PDF and test tab navigation
2. Verify content flows in logical sequence
3. Check that reading order matches visual layout
4. Mark as "Passed" in Acrobat if correct

**Colour contrast** - Manual verification needed:
1. Check text meets WCAG contrast requirements
2. Verify colour is not the only way information is conveyed
3. Test with colour vision simulation tools if available
4. Mark as "Passed" in Acrobat if compliant

#### Report Interpretation

**Excellent result example**:
- 0 Failed items = No critical accessibility barriers
- Most checks passed automatically
- Only manual verifications needed
- Document is likely highly accessible

**This type of report indicates**:
- PDF was properly exported from InDesign with tagging
- Document structure is sound
- Alt-text and form fields properly configured
- Only routine manual verification required

### NVDA Screen Reader Testing

#### Installing NVDA
1. **Download NVDA**:
   - Visit [nvaccess.org](https://nvaccess.org)
   - Download latest stable version
   - Free, open-source screen reader

2. **Installation**:
   - Run installer
   - Choose installation type (installed version recommended)
   - Complete setup process

![[NVDA Settings.png|500]]
	Settings for NVDA (Windows Version). 
	****Note:** may vary depending on NVDA version*.

3. **Basic NVDA operation**:
   - NVDA starts speaking immediately when launched
   - Press Insert+Q to quit NVDA
   - Insert key is the main NVDA modifier key

![[nvda-screen-reader-1024x538.jpg]]
#### NVDA Testing Process

#### Basic Navigation Testing
1. **Open PDF with NVDA running**:
   - Launch NVDA first
   - Open your PDF in Acrobat Reader or Acrobat Pro
   - NVDA should announce document title and reading mode

2. **Test reading flow** (verify your Articles panel protocol worked):
   - **Down arrow**: Read next line
   - **Up arrow**: Read previous line
   - **Ctrl+Home**: Go to document beginning
   - **Ctrl+End**: Go to document end

3. **Test heading navigation** (verify semantic structure):
   - **H key**: Next heading
   - **Shift+H**: Previous heading
   - **1-6 keys**: Navigate by heading levels (1 for H1, 2 for H2, etc.)

4. **Verify reading order matches Articles panel structure**:
   - Content should be encountered in the same sequence as your Articles panel organisation
   - If reading order is wrong, Articles panel may not be controlling the export (check Layers panel organisation or export settings)

#### Detailed NVDA Testing
**Link navigation**:
- **K key**: Next link
- **Shift+K**: Previous link
- **Enter**: Activate link
- Links should be announced with descriptive text

**List navigation**:
- **L key**: Next list
- **Shift+L**: Previous list
- **I key**: Navigate list items
- Lists should be announced as "list with X items"

**Graphic navigation**:
- **G key**: Next graphic
- **Shift+G**: Previous graphic
- **Alt-text should be read automatically** for meaningful images
- **Decorative images should be skipped** (marked as Artifacts)
- **Images should be encountered in logical sequence** relative to related text

**Testing image integration**:
- Navigate to images with G key
- Verify alt-text is read clearly and provides useful information
- Check that images appear in sensible order relative to text content
- Ensure decorative images don't interrupt reading flow

**Table navigation** (if document contains tables):
- **T key**: Next table
- **Ctrl+Alt+Arrow keys**: Navigate table cells
- Header information should be announced with each cell

### Error Interpretation Guide

#### Critical Errors (Must Fix)
**No accessibility structure**:
- PAC reports "Document is not tagged"
- Preflight fails PDF/UA-1 structure requirements
- Fix: Re-export with proper settings from InDesign

**Missing document title**:
- Screen reader announces filename instead of title
- Preflight flags missing metadata
- Fix: Set title in InDesign File Info

**Images without alt-text**:
- NVDA announces "graphic" with no description
- Preflight and Accessibility Checker flag missing alternate text
- Fix: Add alt-text in InDesign Object Export Options

**Poor heading structure**:
- NVDA cannot navigate by headings effectively
- Preflight identifies heading structure violations
- Fix: Apply proper heading styles with export tags

#### Warning-Level Issues (Should Fix)
**Colour contrast insufficient**:
- May affect users with low vision
- Preflight can identify specific contrast ratios
- Fix: Adjust colours to meet 4.5:1 contrast ratio

**Poor reading order**:
- NVDA encounters content in illogical sequence
- Articles panel structure doesn't match PDF reading flow
- Preflight may identify structure order issues
- Fix: Review Articles panel organisation in InDesign, ensure "Use for Reading Order in Tagged PDF" is enabled, check layer organisation as backup

**Articles panel vs Layers panel conflict**:
- Reading order follows layer structure instead of Articles panel
- Fix: Verify Articles panel settings, ensure all content included, reorganise layers (bottom = first read) as backup method

**Missing language declaration**:
- Screen reader may use wrong pronunciation
- Preflight flags language specification requirements
- Fix: Set document language in InDesign

#### Manual Check Items (Verify)
**Link context**:
- Do links make sense when announced alone?
- Are destinations clear from link text?

**Image descriptions**:
- Is alt-text meaningful and appropriate?
- Are decorative images properly excluded?

**Document structure logic**:
- Does the reading order make sense?
- Are related elements grouped appropriately?

### Practice Exercises

#### Test Document Creation
Create simple test documents to practice validation:

**Exercise 1**: Simple report
- Title (H1), two sections (H2), body text, one image
- Export and test complete validation workflow with all three tools

**Exercise 2**: Document with list
- Include bulleted and numbered lists
- Test list navigation with NVDA and validation with Preflight

**Exercise 3**: Document with links
- Internal cross-references and external web links
- Verify link functionality and description quality across all testing tools

### Validation Workflow Summary

#### Standard Testing Sequence
1. **PAC 2024 validation** - Quick standards compliance check
2. **Adobe Preflight PDF/UA-1** - Detailed professional analysis
3. **Fix critical errors** - Address any red-cross failures from both tools
4. **Acrobat Pro accessibility checker** - Comprehensive analysis and quick fixes
5. **NVDA testing** - Real-world usability verification
6. **Document fixes** - Return to InDesign for structural changes
7. **Re-export and re-test** - Verify fixes resolved issues

#### Documentation Process
**Create testing log**:
- Document name and version
- Testing date and tools used (PAC 2024, Preflight, Accessibility Checker, NVDA)
- Errors found and fixes applied
- Final validation status from all tools
- Sign-off for accessibility compliance

#### Tool Integration Strategy

**When to use each tool**:
- **PAC 2024**: Initial validation, final verification, independent confirmation
- **Adobe Preflight**: Professional analysis, detailed reporting, organisational compliance
- **Accessibility Checker**: Quick fixes, manual verification, comprehensive analysis
- **NVDA**: User experience testing, real-world validation, usability confirmation

**Complementary strengths**:
- PAC 2024 + Preflight = Comprehensive technical validation
- Accessibility Checker + Preflight = Professional remediation workflow
- All automated tools + NVDA = Complete accessibility assurance

## What Success Looks Like

A fully accessible PDF should demonstrate:
- **PAC 2024**: Green validation with no critical errors
- **Adobe Preflight**: PDF/UA-1 compliance passed
- **Acrobat Pro**: All checks passed or acceptable manual verification
- **NVDA testing**: Logical reading flow, effective navigation, clear content description
- **Manual review**: Content makes sense when experienced through assistive technology

## Troubleshooting

**Problem**: PAC 2024 won't open PDF
**Solution**: Check PDF isn't password-protected or corrupted. Try opening in Acrobat first.

**Problem**: Preflight and PAC 2024 show different results
**Solution**: Both tools are valuable - address errors found by either. Different tools may catch different issues.

**Problem**: Acrobat checker finds hundreds of errors
**Solution**: Focus on critical errors first. Many errors may be related - fixing one may resolve several.

**Problem**: NVDA reads content in wrong order
**Solution**: Review Articles panel structure in InDesign. Rebuild if necessary.

**Problem**: NVDA skips content
**Solution**: Ensure all content is included in Articles panel or properly threaded in InDesign.

**Problem**: Images described as "graphic" only
**Solution**: Verify alt-text was set in InDesign Object Export Options before export.

**Problem**: Links announced as "link" without description
**Solution**: Use descriptive link text in InDesign, avoid "click here" type phrases.

**Problem**: Headings not recognised by NVDA
**Solution**: Confirm heading styles have proper export tags (H1-H6) in InDesign.

**Problem**: Preflight passes but PAC 2024 fails
**Solution**: Check specific error in PAC 2024. Different validation engines may have different requirements.

### Common Fix Locations

**In InDesign** (requires re-export):
- Document structure and reading order
- Style export tags
- Alt-text and object properties
- Document metadata

**In Acrobat Pro** (quick fixes):
- Individual alt-text additions
- Minor reading order adjustments
- Table header corrections
- Quick tag fixes

**With Preflight** (automated fixes):
- Font embedding
- Colour space conversion
- Metadata updates
- Some structure corrections

**Design level** (major changes):
- Colour contrast issues
- Overall document structure
- Content organisation

## Validation Checkpoint

Final validation requirements:
- [ ] PAC 2024 shows green validation status
- [ ] Adobe Preflight PDF/UA-1 compliance passed
- [ ] Acrobat Pro accessibility checker passes or shows only acceptable manual checks
- [ ] NVDA can navigate document effectively using heading, link, and list navigation
- [ ] Content reads in logical order from beginning to end
- [ ] All images have appropriate alt-text or are marked decorative
- [ ] Document title and properties are properly set
- [ ] Testing results documented for compliance records

## Advanced Testing Considerations

**Additional screen readers**:
- JAWS (commercial) - test if budget allows
- VoiceOver (macOS) - for Mac user testing
- TalkBack (Android) - for mobile PDF access

**User testing**:
- Include actual screen reader users in testing when possible
- Observe real usage patterns and pain points
- Document feedback for future improvements

**Automated testing integration**:
- Consider PAC command-line version for batch testing
- Integrate accessibility testing into document production workflows
- Use Preflight profiles for organisational standards
- Establish organisational standards and checklists

**Professional workflow integration**:
- Create custom Preflight profiles for organisational requirements
- Develop standard operating procedures incorporating all testing tools
- Train team members on appropriate tool selection for different validation needs

## Workflow Completion

Congratulations! You've successfully created an accessible PDF using InDesign and validated it with professional tools. Your document should now:
- Meet WCAG 2.1 AA standards for PDF accessibility
- Pass automated validation tools (PAC 2024, Adobe Preflight)
- Meet professional accessibility standards (PDF/UA-1 compliance)
- Provide excellent user experience for screen reader users
- Serve as a template for future accessible document creation

## Return to Workflow

**For next project**: Return to [[00-navigation-guide]] to repeat the process
**For ongoing work**: Use this comprehensive validation process for all PDF publications
**For team training**: Share this guide and establish consistent workflows using all available tools

**Previous**: [[06-pdf-export]] | **Home**: [[00-navigation-guide]]