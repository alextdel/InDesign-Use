---
tags: [accessibility, InDesign, styles, export-tags, semantic-structure]
---
# Styles and Export Tags for Semantic Structure

← [[02-Document-Setup]] | Next: [[04-Content-Creation]] →

## Quick Reference

Style system checklist:
- [ ] Heading styles (H1-H6) created with proper export tags
- [ ] Body text styles configured
- [ ] List styles with correct semantic tags
- [ ] Character styles for emphasis
- [ ] Object styles for images and graphics with export tags
- [ ] Export tags verified in all styles

**Time estimate**: 30-45 minutes

## Complete Styles Guide

### Understanding Export Tags

**Export tags** tell InDesign how to structure content in the PDF. Without proper tags, your PDF lacks semantic meaning for screen readers.

**Key principle**: Every style needs an appropriate export tag to create accessible PDFs.

### Heading Styles Creation

#### Understanding Document Heading Hierarchy
**Critical accessibility principle**: Proper heading structure provides navigation for screen readers.

**Document structure from [[02-Document-Setup#Document Information and Metadata]]**:
- **H1**: Document main title (cover page only - one per document)
- **H2**: Major sections (Executive Summary, Financial Results, etc.)
- **H3**: Subsections within H2 sections
- **H4-H6**: Further subdivision as needed

**Never skip heading levels**: Don't go from H2 directly to H4 - always use sequential hierarchy.

#### Creating Heading 1 Style
**Use**: Document main title on cover page only

1. **Create the style**:
   - Window → Styles → Paragraph Styles
   - Panel menu → New Paragraph Style

![[ParagraphStyleAdd1.png|500]]

2. **General settings**:
   - **Style Name**: Heading 1
   - **Based On**: `[No Paragraph Style]
   - **Next Style**: Body Text (for any subtitle text)

3. **Basic Character Formats**:
   - **Font Family**: Choose professional font (Arial, Calibri, or corporate font)
   - **Font Style**: Bold
   - **Size**: 28-36pt (larger than other headings - this is the document title)
   - **Leading**: Auto or 1.2× font size
   - **Case**: Normal
   - **Ligatures**: Leave unchecked for accessibility (avoid automatic character combinations)

![[ParagraphStyleEdit1.png|500]]
4. **Advanced Character Formats**:
   - **Language**: English: Australian

5. **Indents and Spacing**:
   - **Space Before**: 0pt (usually at top of cover page)
   - **Space After**: 12pt
   - **First Line Indent**: 0
   - **Alignment**: Centre or Left (as design requires)

6. **Export Tagging** (crucial step):
   - Click "Export Tagging" category
   - **Tag**: H1
   - **Class**: Leave blank unless specific CSS needed

![[paragraph style.png|500]]

7. **Click OK**

**Important**: H1 should only be used once per document for the main title.

#### Accessibility Considerations for All Heading Styles
**For each heading style, ensure**:
- **Ligatures checkbox unchecked** in Basic Character Formats (prevents character combinations like "fi" → "ﬁ" that can confuse screen readers)
- **Language set to English: Australian** for proper pronunciation
- **Clear font hierarchy** with sufficient size differences between levels
- **Avoid decorative fonts** that may not render properly with assistive technology

#### Creating Section Heading Styles (H2-H6)
**These are your main working heading styles for document content.**

**Heading 2** (Major sections):
- **Use**: Main document sections (Executive Summary, Financial Results, Market Analysis)
- **Font size**: 20-24pt
- **Ligatures**: Unchecked (accessibility)
- **Export Tag**: H2
- **Space Before**: 18pt, **After**: 6pt
- **Next Style**: Body Text

**Heading 3** (Subsections):
- **Use**: Subsections within H2 sections (Key Achievements, Revenue Growth)
- **Font size**: 16-18pt
- **Ligatures**: Unchecked (accessibility)
- **Export Tag**: H3
- **Space Before**: 12pt, **After**: 4pt

**Heading 4-6**: Continue pattern with unchecked Ligatures for all heading styles.

#### Heading Hierarchy Validation
**Check your heading structure**:
1. **One H1 only**: Document main title on cover page
2. **Logical progression**: H1 → H2 → H3 → H4 (no skipping levels)
3. **Consistent usage**: H2 for all major sections, H3 for subsections within H2
4. **Export tags assigned**: Every heading style has appropriate H1-H6 tag

**Example of correct hierarchy**:
- H1: Annual Report 2024 (cover page)
	- H2: Executive Summary (page 2)
		- H3: Key Achievements
		- H3: Financial Highlights
	- H2: Market Analysis (new major section)
		- H3: Industry Trends
			- H4: Technology Sector
			- H4: Healthcare Sector

### Body Text Styles

#### Main Body Text Style
1. **Create Body Text style**:
   - New Paragraph Style → General → Style Name: "Body Text"

2. **Basic Character Formats**:
   - Font Family: Same as headings or complementary readable font
   - Font Style: Regular
   - Size: 11pt or 12pt
   - Leading: Auto or 1.2× font size
   - **Ligatures**: Unchecked for accessibility

3. **Indents and Spacing**:
   - Space Before: 0pt
   - Space After: 6pt (paragraph spacing)
   - First Line Indent: 0mm (or 3mm if preferred)

4. **Export Tagging**:
   - Tag: P (for paragraph)

#### Body Text First Paragraph
Create a variant for paragraphs following headings:
- Style Name: "Body Text First"
- Based On: Body Text
- Space Before: 0pt
- First Line Indent: 0mm
- Export Tag: P

### List Styles

#### Understanding InDesign List Creation
InDesign automatically creates semantic list structure when you use the built-in Bullets and Numbering feature. The export tag on list paragraph styles should typically be P or `[Automatic]` - InDesign handles the UL/OL structure.

#### Bulleted List Style
1. **Create style**:
   - Style Name: "Bullet List"
   - Based On: Body Text

2. **Bullets and Numbering**:
   - List Type: Bullets
   - Choose appropriate bullet character (•)
   - Text After: ^t (tab character)
   - Alignment: Left
   - Left Indent: 6mm
   - First Line Indent: -6mm
   - Tab Position: 6mm

3. **Export Tagging**:
   - Tag: P or `[Automatic]` (InDesign handles list structure automatically)

**Note**: The semantic list structure (UL) is created by InDesign's native Bullets and Numbering feature, not the export tag.

#### Numbered List Style
1. **Create style**:
   - Style Name: "Numbered List"
   - Based On: Body Text

2. **Bullets and Numbering**:
   - List Type: Numbers
   - Format: 1, 2, 3... (or preferred numbering)
   - Number: ^#.^t (number, period, tab)
   - Mode: Continue from Previous Number
   - Left Indent: 6mm
   - First Line Indent: -6mm
   - Tab Position: 6mm

3. **Export Tagging**:
   - Tag: P or `[Automatic]` (InDesign handles list structure automatically)

**Note**: The semantic list structure (OL) is created by InDesign's native Bullets and Numbering feature, not the export tag.

### Character Styles

#### Emphasis Styles
Create character styles for inline formatting:

**Strong Emphasis**:
- Style Name: "Strong"
- Font Style: Bold
- Export Tag: Strong

**Italic Emphasis**:
- Style Name: "Emphasis"
- Font Style: Italic
- Export Tag: Em

**Code/Technical Text**:
- Style Name: "Code"
- Font Family: Courier New or Monaco
- Export Tag: Code

### Object Styles

Object styles ensure consistent formatting and proper export tagging for images, backgrounds, and other non-text elements. Like paragraph styles, they're essential for accessibility.

#### Creating Object Styles for Images

##### Content Image Style
1. **Open Object Styles panel**:
   - Window → Styles → Object Styles
   - Panel shows default `[Basic Graphics Frame]` and `[Basic Text Frame]`

2. **Create new object style**:
   - Click Create New Style button (page icon) at bottom of panel
   - Or Panel menu → New Object Style

3. **Configure Basic Attributes**:
   - **Style Name**: Content Image
   - **Based On**: `[None]`
   
4. **Set Frame Fitting Options** (optional but recommended):
   - Check "Frame Fitting Options" in left column
   - **Fitting**: Fit Content Proportionally
   - **Align From**: Center
   - **Crop Amount**: 0mm all sides

5. **Configure Export Tagging** (critical for accessibility):
   - Click "Export Tagging" in left column
   - **EPUB and HTML**:
     - Tag: figure
     - Class: (leave blank or add custom class)
   - **PDF**:
     - Tag: Figure
   - Click OK

##### Decorative Image Style
1. **Create another new object style**:
   - Click Create New Style button
   - **Style Name**: Decorative Image

2. **Configure Export Tagging**:
   - Click "Export Tagging" in left column
   - **EPUB and HTML**:
     - Tag: div
     - Class: decorative
   - **PDF**:
     - Tag: Artifact
   - Click OK

3. **Visual indicator** (optional):
   - In Basic Attributes, you might add:
   - Stroke: 0.5pt, Magenta (as visual reminder)
   - This won't export but helps identify decorative images

#### Creating Background Element Style

1. **Create new object style**:
   - **Style Name**: Background Element
   - **Based On**: `[None]`

2. **Configure basic attributes**:
   - Check "Fill" in left column
   - You can set default colour if desired
   - Or leave as `[None]` to apply colours individually

3. **Configure Export Tagging**:
   - **EPUB and HTML**:
     - Tag: div
     - Class: background
   - **PDF**:
     - Tag: Artifact

4. **Set Transparency** (optional):
   - Check "Effects for Object" in left column
   - Can set default opacity or blend mode
   - Useful for consistent background effects

#### Text Frame Object Styles

##### Body Text Frame Style
1. **Create new object style**:
   - **Style Name**: Body Text Frame
   - **Based On**: `[Basic Text Frame]`

2. **Configure Text Frame Options**:
   - Check "Text Frame General Options" in left column
   - **Columns**: 1
   - **Inset Spacing**: 0mm (all sides)
   - **Vertical Justification**: Top

3. **Configure Export Tagging**:
   - **PDF**: Tag: Sect (for Section)
   - This helps group related content

##### Sidebar Frame Style
1. **Create new object style**:
   - **Style Name**: Sidebar Frame
   - **Based On**: `[Basic Text Frame]`

2. **Configure appearance**:
   - Check "Fill" in left column
   - Colour: Light Grey (10% Black)
   - Check "Stroke" in left column
   - Weight: 1pt, Colour: 50% Black

3. **Configure Text Frame Options**:
   - **Inset Spacing**: 5mm (all sides)

4. **Configure Export Tagging**:
   - **PDF**: Tag: Aside

#### Applying Object Styles

1. **Select object** with Selection Tool (V)
2. **Apply style** using one of these methods:
   - Click style name in Object Styles panel
   - Right-click object → Apply Object Style → `[Style Name]`
   - Alt-click (Windows) or Option-click (Mac) style to apply without clearing overrides

#### Object Style Best Practices

1. **Naming conventions**:
   - Use descriptive names
   - Group related styles (Image-Content, Image-Decorative)
   - Be consistent across documents

1. **Style organisation**:
   - Create style groups for different object types
   - Right-click in panel → New Style Group
   - Name groups clearly (Images, Backgrounds, Frames)

3. **Important limitations**:
   - **Object styles CANNOT set alt-text**
   - Alt-text must be added individually via Object Export Options
   - Object styles CAN set the export tag (Figure, Artifact, etc.)
   - This determines how the object is treated in the PDF structure

![[Object Export Options 1.png|550]]

4. **Quick identification**:
   - Consider using subtle visual indicators
   - Decorative images: thin coloured stroke
   - Background elements: specific opacity
   - Remove these before final export if needed

### Style Organisation

#### Creating Style Groups
1. **Organise styles in folders**:
   - In Paragraph Styles panel: Panel menu → New Style Group
   - Create groups: "Headings", "Body Text", "Lists"
   - Drag styles into appropriate groups
   - Do the same for Object Styles panel

2. **Style naming conventions**:
   - Use clear, descriptive names
   - Group related styles with consistent prefixes
   - Consider alphabetical ordering within groups

### Export Tags Verification

#### Checking and Assigning Export Tags
**Method 1: Edit All Export Tags (Recommended)**
1. **Access bulk export tag editor**:
   - Paragraph Styles panel menu → "Edit All Export Tags..."
   - Select "PDF" radio button in dialog
   - Assign appropriate tags to each style from available options

2. **Verify tag assignments**:
   - Every style should have appropriate tag assigned
	   - H1, H2, H3, H4, H5, H6 for headings
	  - P for body text paragraphs
	  - P or `[Automatic]` for list styles (InDesign handles list structure automatically)
	  - Artifact for decorative elements only
  - Avoid "`[Automatic]`" for non-list styles

![[EditAllTags 1.png|500]]

**Method 2: Individual Style Dialogs**
1. **Check individual styles**:
  - Double-click any paragraph style
  - Click "Export Tagging" in left panel
  - Verify correct tag is assigned
  - Set tag if "`[Automatic]`" is selected

#### Verifying Object Style Settings

1. **Check applied styles**:
  - Select object
  - Object Styles panel shows active style
  - Plus sign (+) indicates local overrides

2. **Verify export tags**:
  - With object selected
  - Check Object Export Options → Tagged PDF tab
  - Should show the tag from your object style

3. **Test with sample export**:
  - Apply styles to test objects
  - Export small test PDF
  - Check tags in Acrobat Pro or PAC

## What Success Looks Like

Your Paragraph Styles panel should show:
- Complete heading hierarchy (H1-H6) with decreasing font sizes
- Body text styles for different contexts
- List styles using native InDesign bullet/numbering tools
- Logical style hierarchy and organisation
- Character styles available for inline formatting

Your Object Styles panel should show:
- Content Image style with Figure tag
- Decorative Image style with Artifact tag
- Background Element style with Artifact tag
- Text frame styles with appropriate semantic tags

**Export tag verification**: Use "Edit All Export Tags..." from panel menu to confirm all styles have appropriate semantic tags assigned.

## Troubleshooting

**Problem**: Export Tags column not visible
**Solution**: Paragraph Styles panel menu → Panel Options → Enable "Show Export Tags"

**Problem**: All tags show as "Automatic"
**Solution**: Edit each style → Export Tagging → Set specific tag (H1, P, etc.)

**Problem**: Can't find UL/OL tags in dropdown
**Solution**: Lists use InDesign's Bullets and Numbering feature, not export tags. Apply P tags to list styles, then format using Bullets and Numbering panel.

**Problem**: Object styles don't apply export tags
**Solution**: Check Object Style Options → Export Tagging → Ensure PDF tag is set correctly

**Problem**: Can't see object style export tags
**Solution**: Select object → Object Export Options → Tagged PDF tab to verify

## Validation Checkpoint

Before proceeding, verify:
- [ ] **Heading 1 style created for document main title** (cover page only)
- [ ] **Heading 2-6 styles created for section hierarchy** 
- [ ] **Heading hierarchy follows document structure** from [[02-Document-Setup]]
- [ ] **All heading styles have proper export tags** (H1-H6)
- [ ] **Font sizes create clear visual hierarchy** (H1 largest → H6 smallest)
- [ ] **No heading levels skipped** in planned document structure
- [ ] Body text styles have P tags
- [ ] List styles use P tags or `[Automatic]` with proper Bullets and Numbering applied
- [ ] Character styles available for emphasis
- [ ] **Object styles created for all image types**
- [ ] **Content Image style has Figure tag**
- [ ] **Decorative Image style has Artifact tag**
- [ ] **Background Element style has Artifact tag**
- [ ] No non-list styles show "`[Automatic]`" in Edit All Export Tags dialog
- [ ] Style hierarchy is logical and consistent

## Advanced Tips

**Style efficiency**:
- Use "Based On" relationships to maintain consistency
- Set "Next Style" to streamline text entry
- Create keyboard shortcuts for frequently used styles
- Use object style groups to organize image and frame styles

**Testing your styles**:
- Apply styles to sample text and objects
- Check that formatting appears as expected
- Verify export tags are properly assigned
- Do a small test export to verify PDF structure

## Next Steps

With your complete semantic style system established (including object styles), proceed to [[04-Content-Creation]] to learn how to apply these styles and add accessible content to your document.

**Previous**: [[02-Document-Setup]] | **Next**: [[04-Content-Creation]]