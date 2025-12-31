---
id: prompt-source-to-markdown
description: Prompt for transforming source content (screenshots, images, documents) to markdown format while preserving 100% originality of content and formatting
author: Himel Das
---

# Transform Source Content to Markdown

## Core Principle

**100% content preservation**: Do not change 0.0001% of content. Transform format only: source → markdown. Preserve all text, structure, punctuation, capitalization, spacing, and formatting relationships.

## Input

Provide: **source content** (screenshot/image/document/any visual content). **Target file path** is optional: if not provided, use the currently opened file in the editor; if no file is open, determine or create appropriate file path based on content context.

## Process

### Target File Determination

If target file path provided, use it. If not provided: check for currently opened markdown file in editor; if found, use it; if no file open, determine or create appropriate file path based on content context and existing file structure.

### Content Extraction

Extract all text exactly as it appears; preserve titles, headings, body text, labels, wording, punctuation, capitalization, and structural elements (sections, lists, tables).

### Format Transformation

Transform to markdown while preserving content: **Headings** → `#`, `##`, `###`; **Tables** → well-formatted markdown tables with proper alignment; **Lists** → markdown list syntax; **Bold** → `**text**`; **Italic** → `*text*`; maintain original structure and hierarchy.

### Table Formatting

Use proper markdown table syntax with aligned columns, consistent spacing/padding. Right-align numeric columns (page numbers) using `:---:` or `---:`; left-align text columns. Preserve all original table content exactly.

### Markdown Guidelines

Use **only markdown syntax** (no HTML unless necessary). Format tables with proper alignment/spacing. Use appropriate header levels for hierarchy. Preserve all original formatting relationships (bold, italic, etc.).

### Content Preservation & Verification

**Critical rules**: Do not add, remove, or modify any text content, numbers, dates, or values. Do not rephrase, summarize, or correct perceived errors. Preserve all original punctuation, capitalization, and spacing. Before finalizing: verify all original content preserved exactly; check markdown syntax is valid; ensure tables properly formatted/aligned; confirm no content added/removed/modified; verify file ends with exactly one newline.

### Validation Check

After transformation, perform validation: extract all text from the transformed markdown (strip markdown formatting), compare with original source text character-by-character. Print validation result in chat: **"✓ Content Match: 100%"** if all content matches exactly, or **"✗ Content Match: [X]% - [description of discrepancies]"** if any differences found. Display this result before completing the task.

## Output

Final markdown file must: contain 100% original content unchanged; use proper markdown formatting throughout; have well-formatted tables with proper alignment; maintain original document structure; use only markdown syntax (no HTML unless necessary); end with exactly one newline character.

## Remember

Format transformation only, never content modification. 100% content preservation is mandatory. Use currently opened file if target path not provided. Always run validation check after transformation and print result in chat. Markdown formatting enhances readability without changing meaning. When in doubt, preserve original content exactly. Tables must be well-formatted with proper column alignment. Use only markdown syntax.
