---
tags: [accessibility, InDesign, setup, configuration]
---

# InDesign Setup for Accessible PDF Creation

← [[00-Navigation-Guide]] | Next: [[02-Document-Setup]] →

## Quick Reference

Essential setup checklist:
- [ ] Workspace configured for accessibility
- [ ] Essential panels visible and organised
- [ ] Spelling dictionary set to Australian English
- [ ] Accessibility preferences enabled
- [ ] Export tags visible in styles panels

**Time estimate**: 15-20 minutes

## Complete Setup Guide

### Workspace Configuration

1. **Reset to Essentials workspace**
   - Go to Window → Workspace → Essentials
   - This provides a clean starting point

2. **Add accessibility panels**
   - Window → Styles → Paragraph Styles *(if not visible)*
   - Window → Styles → Character Styles
   - Window → Styles → Object Styles
   - Window → Articles
   - Window → Utilities → Tags *(this enables export tags)*
   - Window → Pages *(F12) - essential for master page management*

3. **Arrange panels for accessibility workflow**
   - Dock Paragraph Styles and Character Styles together
   - Place Articles panel prominently (you'll use this frequently)
   - Keep Pages panel accessible for master page management
   - Keep Object Styles accessible but secondary

![[InDesign Interface1.png]]

### Essential Panels

#### Paragraph Styles Panel
**Purpose**: Creating semantic structure (headings, body text)

**Setup**:
1. Open Window → Styles → Paragraph Styles
2. Panel menu (three lines) → Panel Options → Set preview size to Large for better visibility
3. **Note**: Export tags are managed through individual style dialogs or "Edit All Export Tags" menu option

**What success looks like**: Paragraph Styles panel is visible and accessible, ready for creating semantic styles with export tags.

#### Articles Panel
**Purpose**: Controlling reading order and structure (PRIMARY accessibility method)

**Setup**:
1. Open Window → Articles
2. Dock near your styles panels
3. This panel will show your document's reading order

**Critical importance**: The Articles panel is the current expert-recommended method for controlling reading order in accessible PDFs. This will be your primary tool for ensuring screen readers encounter content in logical sequence.

**What success looks like**: Panel is visible and ready to populate with content structure.

#### Pages Panel
**Purpose**: Managing master pages and document structure (essential for accessibility)

**Setup**:
1. Open Window → Pages (F12)
2. Keep panel accessible for master page work
3. Used for applying different page templates (cover page vs content pages)

**What success looks like**: Panel shows master pages and document pages, ready for accessibility template setup in [[02-Document-Setup]].
#### Tags Panel
**Purpose**: Managing export tags for PDF structure

**Setup**:
1. Open Window → Utilities → Tags
2. This panel shows available export tags
3. Keep it accessible but not necessarily prominent

### Preferences Configuration

#### Spelling Dictionary
1. Go to Edit → Preferences → Dictionary (Ctrl+K → Dictionary)
2. Set Language to "English: Australian"
3. Click OK

#### General and Interface Preferences
1. Edit → Preferences → Interface
2. **Tool Tips**: Set to "Normal" for helpful guidance (dropdown options: Normal, None, Fast)
3. Edit → Preferences → Units & Increments
4. Set measurement units to familiar system (Millimetres for Australian users)

#### Type Preferences
1. Edit → Preferences → Type
2. **Enable "Enable in-menu font previews"** for easier font selection
3. Edit → Preferences → Advanced Type
4. **Superscript/Subscript settings** (if needed):
   - Size: Default 58.3% (adjust if required)
   - Position: Default 33.3% (adjust if required)

#### File Handling Preferences
1. Edit → Preferences → File Handling
2. **Links section**: Verify "Check Links Before Opening Document" and "Find Missing Links Before Opening Document" are enabled (helpful for accessibility workflow)
3. **Document Recovery Data**: Default settings are usually appropriate

### Advanced Configuration

#### Custom Workspace
Once you have panels arranged optimally:

1. Window → Workspace → New Workspace
2. Name it "Accessibility Workflow"
3. Check "Panel Locations" and "Menus"
4. Click OK

**What success looks like**: Your custom workspace appears in the workspace menu and you can switch to it anytime.

#### Keyboard Shortcuts
Consider setting up these shortcuts for efficiency:

1. Edit → Keyboard Shortcuts
2. Set up shortcuts for:
   - Apply Heading 1 style: F1
   - Apply Heading 2 style: F2
   - Apply Body Text style: F3
   - Show/Hide Articles panel: Ctrl+Shift+A

## What Success Looks Like

Your InDesign interface should now show:
- Paragraph Styles panel visible and accessible
- Articles panel ready for use
- Pages panel accessible for master page management
- Object Styles panel accessible
- Tags panel available
- Australian English spelling active
- Clean, organised workspace focused on accessibility tools

## Troubleshooting

**Problem**: Export Tags column not showing in Paragraph Styles
**Solution**: Export tags are not displayed as a column in current InDesign versions. Use Paragraph Styles panel menu → "Edit All Export Tags" to view and assign tags, or check individual style dialogs under "Export Tagging" section.

**Problem**: Articles panel is greyed out
**Solution**: This is normal until you have content. It will activate when you add text frames.

**Problem**: Australian English not available
**Solution**: You may need to install additional language packs. Go to Creative Cloud Desktop → Apps → Language Packs.

**Problem**: Panels keep disappearing
**Solution**: Save your workspace (Window → Workspace → New Workspace) and reset to it when needed.

**Problem**: Interface feels cluttered
**Solution**: Use tabbed panel groups. Drag panels by their tabs to group related panels together.

## Validation Checkpoint

Before proceeding, verify:
- [ ] Paragraph Styles panel is visible and accessible
- [ ] Articles panel is visible and accessible
- [ ] Pages panel is accessible for master page work
- [ ] Spelling is set to Australian English
- [ ] You can access Object Styles and Tags panels
- [ ] Workspace is saved for future use

## Next Steps

With InDesign properly configured, proceed to [[02-Document-Setup]] to learn how to create accessible document foundations.

**Previous**: [[00-Navigation-Guide]] | **Next**: [[02-Document-Setup]]