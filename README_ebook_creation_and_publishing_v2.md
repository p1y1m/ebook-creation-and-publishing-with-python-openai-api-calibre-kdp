# End-to-End Ebook Creation and Publishing on Amazon with Python, OpenAI API, Calibre, and Amazon KDP

**Author:** Pedro Yanez Melendez

## Overview

This repository documents an end-to-end ebook creation and publishing workflow built with Python, Google Colab, the OpenAI API, AI-generated illustrations, EPUB construction, Calibre EPUB editing, and Amazon Kindle Direct Publishing.

The workflow was used to create bilingual children’s ebooks with structured chapters, generated illustrations, XHTML/EPUB packaging, metadata configuration, visual validation, and final publication on Amazon KDP.

## Project Scope

The implementation covers the complete path from content generation to marketplace publication:

1. Generate structured bilingual ebook content.
2. Generate chapter illustrations with consistent character and style constraints.
3. Match each chapter with its corresponding image.
4. Build EPUB-ready XHTML chapters and navigation files.
5. Apply CSS styling and ebook metadata.
6. Review and adjust the EPUB using Calibre.
7. Publish the final Kindle ebooks through Amazon KDP.

## Main Workflow

### 1. AI-Assisted Story Generation

The notebook generates bilingual story content in English and Spanish, including chapter structure, emotional learning themes, CBT-inspired skill boxes, short exercises, parent prompts, and supporting sections.

### 2. AI Image Generation

The image generation section uses structured prompts, character definitions, scene descriptions, visual-style constraints, and output-path automation to create chapter illustrations and book assets.

### 3. EPUB Assembly

The workflow programmatically assembles text and images into an EPUB structure, including XHTML chapter files, image references, CSS styling, navigation, metadata, and final ebook export.

### 4. Calibre Review

The generated EPUB is reviewed with Calibre’s EPUB editor to inspect chapter files, images, XHTML structure, styling, and rendered previews before publication.

### 5. Amazon KDP Publication

The final ebooks were published through Amazon Kindle Direct Publishing as real marketplace outputs.

## Technologies

- Python
- Google Colab
- OpenAI API
- OpenAI Images API
- Google Drive integration
- Markdown
- XHTML
- CSS
- EPUB structure
- Calibre EPUB Editor
- Amazon Kindle Direct Publishing
- Automated file naming
- Image-text page assembly
- Digital publishing workflow

## Repository Contents

- `python_ai_code_generate_ebookv2proof.ipynb`  
  Main notebook containing the ebook generation, image generation, and EPUB assembly workflow.

- `README.md`  
  Technical project documentation.

- Suggested image evidence:
  - `python-openai-api-ai-image-generation-ebook-code.png`
  - `calibre-epub-book-editing-preview-python-openai-kdp.png`
  - `amazon-kdp-published-ai-ebook-python-openai-calibre.png`

## Published Outputs

The workflow produced three Amazon KDP ebook publications:

https://www.amazon.com/dp/B0GJ6XSC8W

https://www.amazon.com/dp/B0GRVWWYT4

https://www.amazon.com/dp/B0GP19F6KZ

## Purpose

This project demonstrates how generative AI, Python automation, EPUB packaging, and publishing tools can be integrated into a reproducible digital publishing workflow that moves from generated content to final published products.
