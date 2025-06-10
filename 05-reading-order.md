---
tags: [accessibility, InDesign, reading-order, articles-panel, text-threading]
---
# Reading Order and Content Flow

← [[04-Content-Creation]] | Next: [[06-PDF-Export]] →

## Quick Reference

Reading order checklist:
- [ ] Text frames threaded in logical sequence
- [ ] Images anchored to relevant text
- [ ] Articles panel structure established
- [ ] "Use for Reading Order in Tagged PDF" enabled
- [ ] ALL content included in Articles panel
- [ ] Reading flow tested and verified

**Time estimate**: 20-30 minutes

## Understanding Reading Order for Accessible PDFs

**Reading order is the invisible backbone of accessible documents.** When you create a visually appealing layout in InDesign, you're designing for sighted users who can scan the page and choose their own reading path. However, screen reader users experience your document sequentially—one element at a time, in a specific order. If this order is wrong, your carefully crafted content becomes confusing, incomplete, or completely unusable for people with vision impairments.

**The visual layout you see is NOT the reading order.** Just because your heading appears above your body text on screen doesn't mean a screen reader will encounter them in that sequence. InDesign's default export behaviour can produce chaotic reading orders that jump randomly between columns, read captions before headings, or skip content entirely. The only way to guarantee correct reading order is to explicitly define it using the Articles panel—everything else is unreliable guesswork.

**This process is mandatory, not optional.** If you want your PDFs to meet accessibility standards and be usable by everyone, you must take control of reading order. The good news is that once you understand the system, it becomes a straightforward, repeatable process that takes just minutes to implement.

---

## The Correct Method for Reading Order

### Use the Articles Panel Exclusively

**The Articles panel is the ONLY reliable method** for controlling reading order in accessible PDFs.

**DO NOT rely on**:
- Layer stacking order
- The order objects were created
- Visual placement on the page
- Object arrangement commands

**Why**: Only the Articles panel guarantees correct reading order in exported PDFs. Layer order and object stacking are for visual design only - they do not control how screen readers navigate your document.

![[Articles 1.png|550]]
### Critical Reading Order Rules

1. **All content must be in the Articles panel** - if it's not in an article, screen readers may miss it or read it in the wrong order

2. **Enable "Use for Reading Order in Tagged PDF"** - this setting MUST be checked in the Articles panel menu

3. **One comprehensive article is usually best** - don't overcomplicate with multiple articles unless you have a specific need

4. **Text threading comes first** - properly threaded text frames ensure paragraphs flow correctly within the article

5. **Anchored images stay with their text** - when images are anchored in text, they maintain correct position in reading order

### Simple Workflow

1. Thread all text frames in reading order
2. Anchor all images to their relevant text
3. Create one article in Articles panel
4. Drag the main text thread into the article (anchored images come automatically)
5. Add any remaining elements in reading order
6. **Enable "Use for Reading Order in Tagged PDF"** ✓
7. Export with Articles panel order selected

## Complete Reading Order Guide

### Text Frame Threading

**Threading must be done BEFORE adding to Articles panel** to ensure proper paragraph flow.

#### Threading Process
1. **Create text frames**:
   - Type Tool (T) → Draw text frames where needed
   - Don't worry about reading order yet

2. **Thread frames in reading order**:
   - Select Selection Tool (V)
   - Click first text frame
   - Click the out port (small square at bottom-right)
   - Click next text frame to create thread
   - Continue for all text frames

3. **Verify threading**:
   - View → Extras → Show Text Threads
   - Blue lines show connections
   - Ensure logical flow (no crossing lines)

**What success looks like**: Continuous blue thread lines connecting all body text in reading sequence.
![[text threads 1.png]]

### Anchoring Images

**All meaningful images MUST be anchored to text** for proper reading order.

#### Anchoring a Graphic to a Position Within Text (InDesign)

Anchoring a graphic ensures it stays positioned relative to specific text, moving with the text as it reflows. Use one of the following methods to anchor a graphic in Adobe InDesign:

**🔹 Method 1: Cut and Paste (Inline Anchoring)**
* Select the image using the `Selection Tool (V)`.
* Cut the image (`Ctrl+X` / `Cmd+X`).
* Switch to the `Type Tool (T)`.
* Click into the text where the image should be anchored.
* Paste the image (`Ctrl+V` / `Cmd+V`).
* The image will now be placed **inline**, behaving like a text character.
* Confirm anchoring by checking:
   * The **blue anchor symbol** at the top-right of the image.
   * A **dotted line** connecting the image to the anchor point in the text.

**🔹 Method 2: Place Image as Anchored Object**
* Use the `Type Tool (T)` to place the text cursor at the desired anchor point.
* Go to `File → Place`, select the image, and click to insert.
* The image will be placed as an **inline anchored object** at the cursor location.
* Anchoring indicators appear as in Method 1.

**🔹 Method 3: Drag and Drop Anchoring (Custom Position)**
* Select the image with the `Selection Tool (V)`.
* Locate the **blue anchor symbol** at the top-right of the image frame.
* Drag the anchor symbol and drop it into the desired position within the text.
* Use `Object → Anchored Object → Options...` to set:
   * **Position**: Inline, Above Line, or Custom.
   * **Alignment**, spacing, and offset options.

**📌 Viewing Anchor Position in Text**
* To see the **in-text anchor symbol**:
   * Go to `Type → Show Hidden Characters`.
   * A small anchor marker (⬚) will appear at the point of anchoring in the text.
* To hide this marker:
   * Go to `Type → Hide Hidden Characters`.

**ℹ️ Visual Aids and Interface Options**
* The **dotted line** connecting the anchored image to its text location is visible only when the image is selected. This is a visual aid and **cannot be turned off individually**.
* To reduce on-screen clutter, optional interface elements can be toggled:
   * `View → Extras → Hide Frame Edges`
   * `View → Extras → Hide Anchored Object Control`

![[Graphic Anchor 1.png|550]]
**What success looks like**: All images show anchor symbols and move with text reflow.

### Articles Panel Setup

#### Step 1: Access Articles Panel
- Window → Interactive → Articles
- Panel should be docked for easy access

#### Step 2: Enable Critical Setting
**BEFORE adding any content**:
- Articles panel menu → **☑️ "Use for Reading Order in Tagged PDF"**
- **This setting is MANDATORY** - without it, nothing else matters
![[Articles Use Tagging.png|550]]
#### Step 3: Create Single Article
1. Click **New Article** button (page icon)
2. Name it "Main Content" or similar
3. Click OK

#### Step 4: Add ALL Content
**Add elements in exact reading order**:

1. **Select main text thread** with Selection Tool
2. **Drag into article** in Articles panel
3. **Anchored images come automatically** with their text
4. **Add any remaining elements**:
   - Non-anchored images (if any)
   - Tables
   - Sidebars
   - Captions

**Correct sequence example**:
```
📄 Main Content
   ├── H1: Document Title
   ├── P: Introduction paragraph
   ├── 🖼️ Figure: Overview diagram
   ├── H2: First Section
   ├── P: Section text
   ├── • Bullet list
   ├── 🖼️ Figure: Data chart
   ├── P: Analysis paragraph
   └── [continues in reading order...]
```

#### Step 5: Verify Complete Inclusion
**Check that NOTHING is missing**:
- Every text frame
- Every meaningful image
- Every table or chart
- All content that should be read

**Exclude only**:
- Decorative images (marked as Artifacts)
- Background elements
- Page numbers (usually)

### Common Mistakes to Avoid

**❌ Relying on layer order**
- Layers DO NOT control reading order reliably
- Articles panel overrides layer order when properly configured

**❌ Forgetting the critical setting**
- "Use for Reading Order in Tagged PDF" MUST be checked
- Check this BEFORE adding content

**❌ Partial content inclusion**
- ALL readable content must be in Articles panel
- Missing items may appear randomly or not at all

**❌ Multiple articles when one would work**
- Keep it simple - one article per page/document usually best
- Multiple articles add complexity without benefit

### Troubleshooting

**Problem**: Reading order wrong in exported PDF
**Solution**: 
1. Verify "Use for Reading Order in Tagged PDF" is ✓ checked
2. Ensure ALL content is in Articles panel
3. Check nothing is missing from the article
4. Re-export with correct settings

**Problem**: Images appear in wrong place
**Solution**: Images must be anchored to text, not floating freely

**Problem**: Some content missing from screen reader
**Solution**: That content isn't in Articles panel - add it

**Problem**: Articles panel seems to have no effect
**Solution**: The critical setting isn't enabled - check Articles panel menu

## Validation Checkpoint

Before proceeding, verify:
- [ ] All text frames are threaded in logical order
- [ ] All meaningful images are anchored to text
- [ ] Articles panel created with single article
- [ ] **"Use for Reading Order in Tagged PDF" is CHECKED** ✓
- [ ] ALL content appears in Articles panel
- [ ] Content sequence matches intended reading order
- [ ] Test by reading Articles panel items top to bottom

### Final Verification
Read through your Articles panel from top to bottom. This is EXACTLY how a screen reader will encounter your content. If it doesn't make sense in this order, fix it now.

## Next Steps

With reading order properly established through the Articles panel, proceed to [[06-PDF-Export]] to learn the specific export settings that preserve your accessibility work in the final PDF.

**Previous**: [[04-Content-Creation]] | **Next**: [[06-PDF-Export]]