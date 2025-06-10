---
tags: [accessibility, InDesign, content, alt-text, images, lists, hyperlinks]
---
# Content Creation for Accessible PDFs

← [[03-Styles-and-Tags]] | Next: [[05-Reading-Order]] →

## Quick Reference

Content creation checklist:
- [ ] Text formatted with proper semantic styles
- [ ] Lists created with appropriate list styles
- [ ] Images have meaningful alt-text or marked as decorative
- [ ] Hyperlinks are descriptive and accessible
- [ ] Background colours meet contrast requirements
- [ ] All content follows logical structure

**Time estimate**: Variable (depends on document complexity)

## Complete Content Guide

### Text Formatting with Styles

#### Applying Heading Styles
1. **Select text to format**
   - Click in paragraph or select text range
   - Use Type Tool (T) for text selection

2. **Apply heading styles**:
   - Window → Styles → Paragraph Styles
   - Click appropriate heading style (Heading 1, Heading 2, etc.)
   - Or use keyboard shortcuts if configured (F1 for H1, F2 for H2)

3. **Verify style application**:
   - Check that Export Tags column shows correct tag (H1, H2, etc.)
   - Visual formatting should match style definition

#### Body Text Application
1. **Apply body text styles**:
   - Use "Body Text" for standard paragraphs
   - Use "Body Text First" for paragraphs immediately following headings
   - Maintain consistent spacing between paragraphs

2. **Character formatting within paragraphs**:
   - Select text for emphasis
   - Apply character styles: Strong, Emphasis, or Code
   - Window → Styles → Character Styles

**What success looks like**: Text displays proper hierarchy, and Paragraph Styles panel shows applied styles with correct export tags.

### List Creation

#### Creating Bulleted Lists
1. **Format existing text as list**:
   - Select paragraphs to convert to list items
   - Apply "Bullet List" paragraph style
   - Each paragraph becomes a separate list item

2. **Adding new list items**:
   - Type content and apply Bullet List style
   - Press Enter to create new list item
   - Style should automatically continue

3. **List formatting verification**:
   - Check that bullets display consistently
   - Verify proper indentation (6mm indent, 12mm tab)
   - Confirm export tag shows "UL"

#### Creating Numbered Lists
1. **Apply numbered list style**:
   - Select paragraphs or type new content
   - Apply "Numbered List" paragraph style
   - Numbers should appear automatically

2. **Continuing numbering**:
   - New paragraphs continue numbering sequence
   - To restart numbering: Paragraph Styles panel → Right-click → Restart Numbering

3. **Nested lists** (if needed):
   - Create modified list styles with increased indentation
   - Use consistent numbering schemes (1, a, i)

**What success looks like**: Lists display proper bullets/numbers, maintain consistent indentation, and show UL/OL export tags.

### Image Accessibility

#### Adding Images with Proper Alt-Text
1. **Place image**:
   - File → Place (Ctrl+D)
   - Select image file and click Open
   - Click to place or drag to create frame

2. **Set image accessibility properties**:
   - Select placed image
   - Object → Object Export Options
   - **Alt Text tab**:
     - **Alt Text Source**: Custom
     - **Custom Alt Text**: Write descriptive text

![[Object Export Options 1 1.png|550]]

3. **Writing effective alt-text**:
   - **Describe the content and function** of the image
   - **Be concise but complete** (aim for 125 characters or less)
   - **Don't start with "Image of" or "Picture of"**
   - **Include relevant details** that support the document content

#### Examples of Good Alt-Text
- **Chart**: "Quarterly sales increased 15% from Q1 to Q4, reaching $2.3 million"
- **Logo**: "ABC Company" (not "ABC Company logo")
- **Portrait**: "Dr Sarah Smith, Chief Medical Officer"
- **Diagram**: "Process flow: Application submitted, reviewed by manager, approved or denied"

#### Marking Decorative Images
1. **For purely decorative images**:
   - Select image
   - Object → Object Export Options
   - **Alt Text tab**:
     - **Alt Text Source**: None
   - Or apply "Decorative Image" object style

2. **What constitutes decorative**:
   - Background patterns or textures
   - Purely aesthetic borders or dividers
   - Images that don't add information to content
   - Repetitive design elements

#### Image Object Styles
1. **Apply appropriate object style**:
   - Select image
   - Window → Styles → Object Styles
   - Choose "Content Image" or "Decorative Image"
   - Verify export tag (Figure or Artifact)

**What success looks like**: Content images have descriptive alt-text and Figure tags; decorative images have no alt-text and Artifact tags.

### Hyperlink Setup for Accessibility

Creating accessible hyperlinks requires attention to link text, destination clarity, and proper tagging for screen readers. This section covers comprehensive hyperlink creation for accessible PDFs.

#### Understanding Hyperlink Accessibility

**Screen reader behaviour**: Screen readers can list all hyperlinks separately from document content, so link text must be meaningful out of context.

**Essential principles**:
- Link text describes the destination or action
- Links are distinguishable from regular text
- Link purpose is clear without surrounding context
- External links and file downloads are identified

#### Creating Text Hyperlinks

**Basic URL Hyperlinks**
1. **Select descriptive link text**:
   - Choose text that describes the destination
   - **Good**: "Download the accessibility guidelines"
   - **Poor**: "Click here" or "Read more"

2. **Create the hyperlink**:
   - Window → Interactive → Hyperlinks
   - With text selected, click Create New Hyperlink button
   - **New Hyperlink dialog options**:
     - **Link To**: URL
     - **URL**: Enter complete web address (including https://)
     - **Character Style**: [None] unless specific formatting needed

![[HyperlinkAdd2.png|550]]
2. **Hyperlink appearance settings** (for accessibility):
   - **Type**: Visible Rectangle (recommended for screen readers)
   - **Highlight**: None or Invert
   - **Colour**: Use sufficient contrast (test 3:1 ratio minimum)
   - **Width**: Thin or Medium
   - **Style**: Solid

**Email Hyperlinks**
1. **Format email addresses properly**:
   - **Text display**: "Contact support team" (not the email address itself)
   - **Or**: "support@company.com.au" (if email address must be visible)

2. **Create email link**:
   - Select contact text or email address
   - New Hyperlink → **Link To**: Email
   - **Address**: Enter email address
   - **Subject Line**: Pre-populate if appropriate (e.g., "Website feedback")

**Phone Number Hyperlinks**
1. **Format phone numbers accessibly**:
   - **Display text**: "(02) 9123 4567" or "Call our office"
   - **Link destination**: Include "tel:" protocol

2. **Create phone link**:
   - Select phone text
   - New Hyperlink → **Link To**: URL
   - **URL**: `tel:+61291234567` (international format without spaces)

#### File Download Hyperlinks

**Document Download Links**
1. **Descriptive link text with file information**:
   - Include file type and size
   - **Example**: "Annual Report 2023 (PDF, 2.4MB)"
   - **Example**: "Registration form (Word document, 156KB)"

2. **Create file link**:
   - New Hyperlink → **Link To**: File
   - **Path**: Browse to file location or enter relative path
   - **Shared Hyperlink Destination**: Enable for reuse

3. **Accessibility considerations**:
   - Mention file format in link text
   - Include file size for large downloads
   - Consider alternative formats (HTML version of PDF)

#### Internal Document Hyperlinks

**Cross-References to Headings**
1. **Create heading destinations**:
   - Ensure target text uses proper heading styles (H1-H6)
   - Hyperlinks will automatically work with tagged headings

2. **Create cross-reference**:
   - Place cursor where link should appear
   - Type → Hyperlinks & Cross-References → Insert Cross-Reference
   - **Link To**: Paragraph
   - **Document**: Current document or browse to other document
   - **Paragraph**: Select target heading from list

3. **Cross-reference format**:
   - Choose appropriate format (Page Number, Full Paragraph & Page Number, etc.)
   - **Most accessible**: "Full Paragraph & Page Number"

**Text Anchor Hyperlinks**
1. **Create text anchor at destination**:
   - Place cursor at target location
   - Type → Hyperlinks & Cross-References → New Text Anchor
   - **Name**: Descriptive name (e.g., "conclusion-section")

2. **Link to text anchor**:
   - Select link text
   - New Hyperlink → **Link To**: Text Anchor
   - **Text Anchor**: Select from dropdown list

#### Hyperlink Character Styles

**Creating Accessible Link Formatting**
1. **Create hyperlink character style**:
   - Window → Styles → Character Styles
   - New Character Style → Name: "Hyperlink"
   - **Basic Character Formats**:
     - **Colour**: Blue (#0066CC or similar accessible blue)
     - **Underline**: Apply standard underline
   - **Export Tagging**: No specific tag needed

2. **Apply consistent link styling**:
   - Select hyperlink text
   - Apply "Hyperlink" character style
   - Verify sufficient contrast (4.5:1 for normal text)

**Visited Link Styles (Optional)**
1. **Create visited link style**:
   - New Character Style → Name: "Hyperlink Visited"
   - **Colour**: Purple (#663399 or similar)
   - Apply manually if needed for printed versions

#### External Link Indicators

**Marking External Links**
1. **Add external link indicators**:
   - Include "(external link)" in link text
   - **Example**: "Visit the Australian Government website (external link)"
   - Or use consistent symbol after link text

2. **Alternative approaches**:
   - Use character style with external link icon
   - Include domain name: "Read more on example.com"
   - Group external links in separate section

#### Hyperlinked Images

**When Images Serve as Links**
For images that function as hyperlinks, the alt-text must describe both the image content and the link destination:

1. **Alt-text for linked images**:
   - Select the linked image
   - Object → Object Export Options → Alt Text tab
   - **Custom Alt Text**: Describe image and link purpose
   - **Example**: "ABC Company logo - return to homepage"
   - **Not**: "ABC Company logo" (doesn't indicate it's a link)

2. **Best practice for PDF accessibility**:
   - **Always provide adjacent text links** alongside linked images
   - Screen readers work more reliably with text-based navigation
   - **Example**: Place "Return to homepage" text link near logo
   - This ensures accessibility regardless of image link functionality

3. **Implementation approach**:
   - Use images as visual enhancement to text links
   - Don't rely solely on image links for critical navigation
   - Ensure text alternative is always available

#### Hyperlink Validation and Testing

**Pre-Export Testing**
1. **Test links in InDesign**:
   - Ctrl+click (Windows) or Cmd+click (Mac) on hyperlinks
   - Verify correct destination opens
   - Check all links work as expected

2. **Review link list**:
   - Window → Interactive → Hyperlinks
   - Review all hyperlinks in document
   - Check for duplicates or errors
   - Verify descriptive names

**Accessibility Review**
1. **Screen reader simulation**:
   - Read link text out of context
   - Ensure destination/purpose is clear
   - Verify no "click here" or similar non-descriptive text

2. **Visual accessibility**:
   - Check colour contrast of link text
   - Verify underline or other visual distinction
   - Test with View → Overprint Preview

### Background Colours and Design Elements

#### Accessible Colour Usage
1. **Contrast requirements**:
   - **Normal text**: 4.5:1 contrast ratio minimum
   - **Large text** (18pt+ or 14pt+ bold): 3:1 contrast ratio minimum
   - **Non-text elements**: 3:1 contrast ratio for UI components

2. **Testing contrast**:
   - Use online contrast checkers
   - Test with actual hex colour values
   - Consider printing in grayscale as additional test

#### Background Implementation
1. **Creating accessible backgrounds**:
   - Rectangle Tool (M) → Draw background shape
   - Apply colour through Swatches panel
   - Object → Arrange → Send to Back

2. **Background object style**:
   - Apply "Background Element" object style
   - Verify export tag is "Artifact"
   - Backgrounds shouldn't interfere with reading order

#### Colour Accessibility Guidelines
- **Don't rely on colour alone** to convey information
- **Use patterns or symbols** in addition to colour coding
- **Test for colour blindness** accessibility
- **Maintain sufficient contrast** in all colour combinations

### Tables (If Required)

#### Basic Table Creation
1. **Insert table**:
   - Table → Insert Table
   - Set rows and columns as needed
   - Enable "Header Rows" and "Footer Rows" if appropriate

2. **Table accessibility**:
   - Keep table structure simple
   - Use clear column and row headers
   - Avoid merged cells when possible
   - Consider breaking complex tables into multiple simple tables

#### Table Styling
1. **Apply consistent formatting**:
   - Create table and cell styles
   - Use adequate padding and spacing
   - Maintain readable font sizes
   - Ensure sufficient contrast

## What Success Looks Like

Your document should now contain:
- Text formatted with appropriate semantic styles
- Lists that display proper bullets/numbers with correct export tags
- Images with meaningful alt-text or properly marked as decorative
- Hyperlinks using descriptive, contextual text that work correctly
- Background elements marked as artifacts
- Consistent visual hierarchy supporting the semantic structure

## Troubleshooting

**Problem**: Style not applying correctly
**Solution**: Ensure cursor is in paragraph before applying paragraph style, or select text range for character styles

**Problem**: List numbering restarts unexpectedly
**Solution**: Check for style breaks or manual formatting. Paragraph Styles panel → Right-click → Continue Numbering

**Problem**: Alt-text not saving
**Solution**: Ensure Object Export Options dialog is fully completed and clicked OK. Re-check by reopening dialog.

**Problem**: Hyperlinks don't work
**Solution**: Check URL format includes http:// or https://. Test link by Ctrl+click in InDesign.

**Problem**: Background colours appear in front of text
**Solution**: Select background element → Object → Arrange → Send to Back

**Problem**: Images appear pixelated
**Solution**: Check image resolution (300 DPI for print, 150+ DPI for digital). Use high-quality source images.

**Problem**: Lists show inconsistent formatting
**Solution**: Verify all list items use the same list style. Check for manual overrides in paragraph formatting.

### Alt-Text Problems

**Problem**: Alt-text too long or verbose
**Solution**: Focus on essential information. Aim for 125 characters or less. Consider if detailed description belongs in document text instead.

**Problem**: Uncertain whether image is decorative
**Solution**: Ask "Does this image add information to the content?" If no, mark as decorative. If yes, write descriptive alt-text.

**Problem**: Complex images (charts, diagrams) difficult to describe
**Solution**: Provide brief alt-text describing the type and conclusion, then include detailed description in document text or caption.

### Hyperlink Problems

**Problem**: "Click here" links throughout document
**Solution**: Rewrite link text to describe destination: "Download the user manual" instead of "Click here to download"

**Problem**: Links not working in exported PDF
**Solution**: 
- Check URL format includes protocol (https://)
- Verify Hyperlinks option enabled in PDF export
- Test file paths for relative links

**Problem**: Email links not opening email client
**Solution**: 
- Ensure mailto: protocol used
- Format: `mailto:address@domain.com.au`
- Test on target system/browser

**Problem**: Phone links not working on mobile
**Solution**: 
- Use international format: `tel:+61291234567`
- Remove spaces and special characters from tel: URL
- Test on mobile device

**Problem**: Links blend in with regular text
**Solution**:
- Apply hyperlink character style with colour and underline
- Test contrast ratio (minimum 3:1 for non-text elements)
- Consider additional visual indicators

**Problem**: Too many external link indicators cluttering text
**Solution**: 
- Group external links in appendix or reference section
- Use consistent, brief indicators: "(ext)"
- Consider footnote-style numbering for external links

## Validation Checkpoint

Before proceeding, verify:
- [ ] All text uses appropriate semantic styles (not manual formatting)
- [ ] Lists display correctly with proper export tags
- [ ] All meaningful images have descriptive alt-text
- [ ] Decorative images marked with no alt-text
- [ ] Hyperlinks use descriptive text and work correctly
- [ ] Links include file type/size for downloads
- [ ] External links are appropriately indicated
- [ ] Phone numbers use international format
- [ ] Email links include proper context
- [ ] Background colours meet contrast requirements
- [ ] Document structure is logical and hierarchical

## Advanced Content Tips

**Efficiency techniques**:
- Use "Next Style" settings to speed up text entry
- Create keyboard shortcuts for frequently used styles
- Copy and paste styles between similar documents
- Create hyperlink character style for consistent link appearance

**Quality control**:
- Review document in outline view to check heading hierarchy
- Test all hyperlinks before finalising
- Consider how content will read aloud (screen reader perspective)
- Use Find/Change to locate and fix "click here" links

**Hyperlink best practices**:
- Group related external links in reference sections
- Use footnote-style referencing for extensive citations
- Consider print vs. digital presentation differences
- Maintain reading flow while providing necessary links

## Next Steps

With accessible content properly created and formatted, proceed to [[05-Reading-Order]] to organise the content flow and ensure logical reading sequence for screen readers.

**Previous**: [[03-Styles-and-Tags]] | **Next**: [[05-Reading-Order]]