---
tags: [accessibility, InDesign, navigation, workflow]
---

# InDesign Accessible PDF Creation - Navigation Guide

## The Complete Process Overview

**Creating accessible PDFs in InDesign follows a systematic workflow with seven core stages:**

### 1. **Style-Based Semantic Structure**
- Create and apply paragraph styles for all headings (H1-H6) with proper export tags
- Allocate all text content to appropriate styles (body text, captions, quotes)
- Set up ordered and unordered list styles with correct list export tags
- Establish character styles for inline emphasis and special formatting
- **Why this matters:** Styles with export tags create the semantic structure that screen readers use to navigate

### 2. **Object and Image Accessibility**
- Apply alt text to all meaningful images, charts, and graphics using Object Export Options
- Mark decorative images as artifacts (no alt text needed)
- Create object styles for consistent image treatment and export settings
- Ensure all visual information has text equivalent
- **Why this matters:** Screen readers need text descriptions of visual content

### 3. **Logical Content Flow**
- Thread text frames in logical reading order
- Anchor images, tables, and graphics into the text flow at appropriate positions
- Use proper text wrapping to maintain reading sequence
- **Why this matters:** Determines the order screen readers present content

### 4. **Reading Order Management**
- Set up the Articles panel to define and refine reading sequence
- Group related content elements together
- Handle complex layouts with multiple columns and sidebar content
- **Why this matters:** Ensures complex layouts read in logical order

### 5. **Navigation and Links**
- Create accessible hyperlinks with descriptive text
- Add internal cross-references and bookmarks
- Set up table of contents linking
- **Why this matters:** Provides multiple ways for users to navigate the document

### 6. **Document Properties and Export**
- Add complete metadata (title, author, subject, language)
- Configure export settings for accessibility compliance
- Choose appropriate PDF/UA and tagged PDF options
- **Why this matters:** Provides document context and ensures proper PDF structure

### 7. **Validation and Testing**
- Test with PAC 2024 (PDF Accessibility Checker) for technical compliance
- Review and fix issues in Acrobat Pro
- Test with NVDA screen reader for user experience
- **Why this matters:** Confirms the document actually works for assistive technology users

## Workflow Navigation

### Quick Start Path (Experienced Users)
If you're familiar with InDesign but new to accessibility:
1. [[01-InDesign-Setup#Essential Panels]] - Get the right panels visible
2. [[03-Styles-and-Tags#Export Tags Verification]] - Add accessibility tags to existing styles
3. [[04-Content-Creation#Adding Images with Proper Alt-Text]] - Handle images and graphics
4. [[05-Reading-Order#Articles Panel Setup]] - Set reading order
5. [[06-PDF-Export#Essential Accessibility Options]] - Export correctly
6. [[07-Validation-Testing#PAC 2024 Validation Process]] - Validate results

### Complete Learning Path (New to InDesign)
Work through each guide in sequence:

| File | Time Est. | Purpose | Key Outcome |
|------|-----------|---------|-------------|
| [[01-InDesign-Setup]] | 15 min | Configure software | Workspace ready for accessibility work |
| [[02-Document-Setup]] | 10 min | Create new document | Document properties set correctly |
| [[03-Styles-and-Tags]] | 45 min | Build style system | All content uses tagged styles |
| [[04-Content-Creation]] | 60 min | Add accessible content | Text, images, links properly formatted |
| [[05-Reading-Order]] | 30 min | Manage content flow | Logical reading sequence established |
| [[06-PDF-Export]] | 15 min | Export settings | Accessible PDF created |
| [[07-Validation-Testing]] | 30 min | Test and validate | Confirmed working accessible PDF |

## File Contents Overview

### [[01-InDesign-Setup]]
**What you'll do:** Configure InDesign workspace and preferences for accessibility work
- Enable essential panels (Styles, Articles, Export Tags)
- Set Australian English dictionary
- Configure accessibility preferences
- **Result:** InDesign ready for accessible document creation

### [[02-Document-Setup]]
**What you'll do:** Create new documents with proper accessibility foundation
- Document dialogue settings for accessibility
- Add metadata (title, author, language)
- Set up master pages appropriately
- **Result:** Document foundation ready for content

### [[03-Styles-and-Tags]]
**What you'll do:** Create the semantic structure system
- Build paragraph styles for headings (H1-H6) with export tags
- Set up body text, list, and specialty styles
- Create character styles for inline formatting
- Assign appropriate export tags to each style
- **Result:** Complete style system that creates accessible PDF structure

### [[04-Content-Creation]]
**What you'll do:** Add content using accessible techniques
- Apply styles to create proper heading hierarchy
- Create accessible bulleted and numbered lists
- Add images with appropriate alt text or artifact marking
- Create accessible hyperlinks and cross-references
- Handle background colours and design elements accessibly
- **Result:** Document content structured for accessibility

### [[05-Reading-Order]]
**What you'll do:** Ensure content flows logically
- Thread text frames in reading order
- Anchor images at appropriate text positions
- Use Articles panel to manage complex layouts
- Test and adjust reading sequence
- **Result:** Content flows in logical order for screen readers

### [[06-PDF-Export]]
**What you'll do:** Export with correct accessibility settings
- Configure export dialogue for accessibility
- Choose appropriate quality and file size settings
- Enable required accessibility options
- **Result:** Tagged, accessible PDF file

### [[07-Validation-Testing]]
**What you'll do:** Verify accessibility and fix issues
- Install and use PAC 2024 (PDF Accessibility Checker) for validation
- Use Acrobat Pro accessibility checker and preflight tool for additional review
- Configure and run Acrobat's accessibility preflight profiles
- Test with NVDA screen reader for real user experience
- Fix common accessibility problems identified during testing
- **Result:** Confirmed accessible PDF that works with assistive technology

## Essential Tools for Accessibility Validation

### PAC 2024 (PDF Accessibility Checker)

**PAC 2024 is the primary validation tool for accessible PDFs.** This free tool from the PDF Association provides comprehensive accessibility testing that goes beyond Acrobat's built-in checker.

#### Why PAC 2024 is Essential
- **Industry standard:** Used by accessibility professionals globally
- **Comprehensive testing:** Checks PDF/UA compliance and WCAG requirements
- **Free and reliable:** No cost, regular updates for latest standards
- **Clear reporting:** Identifies specific issues with actionable descriptions

#### When to Use PAC 2024
1. **After every PDF export** - Basic validation check
2. **Before document delivery** - Final compliance verification
3. **During template creation** - Ensure templates produce accessible results
4. **When troubleshooting** - Identify specific accessibility issues

### Adobe Acrobat Preflight Tool

**Acrobat's Preflight tool provides professional-grade accessibility checking** with built-in remediation capabilities and detailed compliance reporting.

#### Why Use Acrobat Preflight for Accessibility
- **PDF/UA profiles:** Pre-configured accessibility standards checking
- **Integrated fixes:** Direct connection between detection and correction
- **Professional reporting:** Detailed compliance documentation
- **Batch processing:** Check multiple documents efficiently

#### Key Accessibility Preflight Profiles
- **PDF/UA-1 verification:** Complete universal accessibility compliance
- **PDF accessibility checker:** WCAG-focused validation
- **Custom profiles:** Tailored checking for specific requirements

#### When to Use Acrobat Preflight
1. **Professional validation:** When detailed compliance reporting is required
2. **Batch processing:** Multiple documents need checking
3. **Integration workflow:** Part of professional prepress processes
4. **Custom requirements:** Specific accessibility standards beyond basic compliance

### Tool Comparison and Workflow Integration

| Tool | Best For | Strengths | Use When |
|------|----------|-----------|----------|
| **PAC 2024** | Initial validation | Free, comprehensive, latest standards | Every export, final check |
| **Acrobat Preflight** | Professional validation | Integration, reporting, batch processing | Professional workflows, detailed reporting |
| **Acrobat Accessibility Checker** | Quick fixes | Built-in remediation, user-friendly | Immediate corrections |
| **NVDA Screen Reader** | User experience | Real-world testing | Final user validation |

## Common Workflow Branches

### **Existing Document Remediation**
If you're making an existing InDesign document accessible:
1. [[03-Styles-and-Tags#Style Organisation]] - Add export tags to current styles
2. [[04-Content-Creation#Adding Images with Proper Alt-Text]] - Add missing alt text
3. [[05-Reading-Order#Troubleshooting]] - Verify reading sequence
4. [[06-PDF-Export]] - Export with accessibility
5. [[07-Validation-Testing]] - Test and fix issues

### **Template Creation**
If you're building templates for others to use:
1. [[02-Document-Setup#Master Page Considerations]] - Document setup for templates
2. [[03-Styles-and-Tags#Style Organisation]] - Complete style libraries
3. [[04-Content-Creation#Advanced Content Tips]] - Usage instructions
4. Focus on [[07-Validation-Testing#Practice Exercises]] - Ensure template produces accessible results

### **Complex Layout Documents**
For documents with multiple columns, sidebars, callouts:
1. Complete standard workflow through [[04-Content-Creation]]
2. Focus heavily on [[05-Reading-Order#Common Mistakes to Avoid]]
3. Use [[07-Validation-Testing#NVDA Screen Reader Testing]] extensively

## Troubleshooting Quick Links

### Common Problems and Solutions
- **Styles not exporting correctly:** [[03-styles-and-tags#Troubleshooting]]
- **Images missing alt text:** [[04-Content-Creation#Alt-Text Problems]]
- **Wrong reading order:** [[05-Reading-Order#Troubleshooting]]
- **PDF export fails:** [[06-PDF-Export#Troubleshooting]]
- **PAC 2024 validation errors:** [[07-Validation-Testing#Common PAC 2024 Errors and Fixes]]
- **Acrobat preflight failures:** [[07-Validation-Testing#Common Preflight Accessibility Fixes]]
- **Screen reader issues:** [[07-Validation-Testing#NVDA Screen Reader Testing]]

### Emergency Fixes
If you have a deadline and need quick fixes:
1. [[07-Validation-Testing#Common Acrobat Pro Quick Fixes]] - Fix issues in exported PDF using accessibility checker
2. [[07-Validation-Testing#Common Preflight Accessibility Fixes]] - Use preflight tool for rapid compliance checking
3. [[04-Content-Creation#Adding Images with Proper Alt-Text]] - Quickly add alt text
4. [[06-PDF-Export#Essential Accessibility Options]] - Basic export settings

## Success Checkpoints

After each major section, you should be able to:
- **After Setup:** See Styles, Articles, and Export Tags panels
- **After Document Setup:** New document with proper metadata
- **After Styles:** All text content uses tagged styles
- **After Content Creation:** Images have alt text, links work properly
- **After Reading Order:** Articles panel shows logical content flow
- **After Export:** Tagged PDF file created
- **After Validation:** PAC 2024 shows no critical errors and document passes accessibility testing

## Validation Workflow Summary

Your testing process should include a comprehensive four-tool approach:

1. **PAC 2024** - Primary technical compliance checking (PDF/UA, WCAG standards)
2. **Acrobat Preflight** - Professional validation with detailed reporting and batch processing
3. **Acrobat Accessibility Checker** - Quick issue identification and integrated fixes
4. **NVDA Screen Reader** - Real user experience verification

### Recommended Validation Sequence
1. **Export from InDesign** with accessibility settings enabled
2. **PAC 2024 check** - Immediate validation for major issues
3. **Acrobat preflight** - Run PDF/UA-1 profile for detailed compliance
4. **Fix issues** using Acrobat's accessibility checker and preflight results
5. **NVDA testing** - Verify actual screen reader experience
6. **Final PAC 2024 check** - Confirm all issues resolved

This multi-tool approach ensures both technical compliance and practical usability for people using assistive technology.

## Getting Help

### If You're Stuck
1. Check the **Troubleshooting** section in each file
2. Use **Validation Checkpoints** to confirm you're on track
3. Review **What Success Looks Like** sections for visual confirmation
4. Run PAC 2024 early and often to catch issues during creation rather than after export

### Practice Documents
Start with simple documents before complex layouts:
1. **Single-column report** - Basic workflow practice
2. **Multi-page brochure** - Image and design elements
3. **Complex manual** - Advanced reading order management

---
*This guide assumes technical competence but no prior InDesign or accessibility experience. Each linked file provides complete, step-by-step procedures with screenshots and validation steps.*