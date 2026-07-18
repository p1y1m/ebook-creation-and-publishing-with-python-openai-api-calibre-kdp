Author: Pedro Yanez Melendez

# Ebook Creation and Publishing with Python, OpenAI API, Calibre, and Amazon KDP

**Repository name:** `ebook-creation-and-publishing-with-python-openai-api-calibre-kdp`

**Repository description:**  
End-to-end ebook creation and publishing workflow using Python, OpenAI API, AI-generated text and images, EPUB assembly/editing with Calibre, and final publication through Amazon KDP.

---

## Project Overview

This repository documents an end-to-end technical workflow for creating, assembling, editing, and publishing children’s ebooks.

The project was implemented with Python in Google Colab and combines:

- AI-assisted bilingual story generation.
- AI-assisted image generation.
- Character and visual-style consistency through structured prompts.
- Automated chapter image creation.
- Markdown-based book content generation.
- EPUB assembly with Python libraries.
- Manual EPUB review and editing with Calibre.
- Final publication through Amazon Kindle Direct Publishing.

The final result was not only a script or experiment. The workflow produced real EPUB-ready books and supported publication of Kindle ebooks on Amazon KDP.

---

## Main Workflow

The project follows three main stages:

### 1. AI-Assisted Story and Book Content Generation

The notebook generates a bilingual children’s ebook in English and Spanish using the OpenAI API.

The content-generation stage includes:

- A structured prompt for a children’s book.
- Defined target age and tone.
- Chapter-by-chapter structure.
- English and Spanish sections.
- Skill boxes.
- Parent prompts.
- Mini exercises.
- Quick reference sections.
- Disclaimer text.

In the sample implementation, the generated book focuses on CBT-inspired anxiety skills for children, using short chapters and simple child-friendly language.

### 2. AI-Assisted Image Generation

The workflow also generates images through the OpenAI Images API.

The image-generation stage includes:

- A shared character bible.
- Consistent character descriptions.
- Consistent visual style.
- Watercolor children’s book illustration prompts.
- One image per chapter.
- Cover image generation.
- End-page image generation.
- Output files saved into a structured image directory.

The notebook uses a fixed character bible to keep characters, clothing, emotional tone, and visual style consistent across the ebook.

### 3. EPUB Assembly, Editing, and Publishing

After generating text and images, the workflow assembles the book into EPUB format.

The EPUB stage includes:

- Reading generated Markdown content.
- Parsing chapter headings.
- Pairing each chapter with its corresponding generated image.
- Creating XHTML chapter files.
- Adding CSS styling.
- Adding ebook metadata.
- Creating EPUB navigation, table of contents, and spine.
- Exporting the final EPUB file.
- Reviewing and editing the EPUB in Calibre.
- Publishing the final digital book through Amazon KDP.

---

## Technical Stack

- **Python**
- **Google Colab**
- **OpenAI API**
- **OpenAI ChatCompletion / text generation**
- **OpenAI Images API**
- **Google Drive integration**
- **Colab Secrets**
- **Markdown**
- **EbookLib**
- **Calibre EPUB editor**
- **Amazon Kindle Direct Publishing**
- **HTML / XHTML**
- **CSS**
- **Base64 image handling**
- **Regular expressions**
- **Automated file naming with timestamps**

---

## Security Note

The notebook is designed to use the OpenAI API key through **Google Colab Secrets**:

```python
from google.colab import userdata

api_key = userdata.get("OPENAI_API_KEY")
```

The API key is not hard-coded in the notebook.  
Anyone who clones or runs the notebook must configure their own `OPENAI_API_KEY` secret in Google Colab.

Before publishing any notebook publicly, clear outputs and confirm that no API key was printed in any cell output.

---

## Notebook Structure

The notebook includes several major execution sections:

### Content Generation

Generates the bilingual Markdown book using a structured prompt and the OpenAI API.

Key elements include:

- Book title.
- Author metadata.
- Chapter plan.
- Safety and tone instructions.
- Output format constraints.
- Markdown export.
- Downloadable `.md` output.

### Chapter Image Generation

Generates a set of chapter illustrations using a consistent character bible and image prompts.

Key elements include:

- Character definitions.
- Visual style definition.
- Scene-specific prompts.
- Output path configuration.
- Automatic image file naming.
- Chapter image files saved to Google Drive.

### EPUB Generation

Builds the final EPUB by combining generated text and generated images.

Key elements include:

- Markdown parsing.
- Chapter detection.
- Image pairing by chapter number.
- XHTML chapter generation.
- CSS styling.
- EPUB metadata.
- Table of contents.
- Navigation files.
- Final `.epub` export.

### Cover and End Page Generation

Generates additional images for the ebook cover and ending page.

Key elements include:

- Cover prompt.
- End-page prompt.
- Vertical image ratio.
- Consistent character and style setup.
- Output images saved to the project image folder.

---

## Example Output

The workflow supports outputs such as:

- Generated bilingual Markdown manuscript.
- Chapter illustrations.
- Cover image.
- End-page image.
- EPUB file.
- Calibre-edited ebook package.
- Published Amazon Kindle ebook listing.

---

## Screenshots

The following screenshots can be included in the repository under an `assets/` folder.

### Colab Image Generation Code

```markdown
![Colab AI image generation code](assets/codegenerateimage.png)
```

This screenshot shows the Python image-generation logic, including chapter prompts, character bible usage, image output naming, and generated chapter image files.

### Calibre EPUB Chapter Preview

```markdown
![Calibre EPUB chapter preview](assets/calibre_epub_chapter_preview.png)
```

This screenshot shows the final EPUB structure inside Calibre, including XHTML chapter content, the embedded illustration, and the rendered book preview.

### Amazon KDP Published Ebook Listing

```markdown
![Amazon KDP published ebook listing](assets/amazon_kdp_published_ebook_listing.png)
```

This screenshot shows the final published Kindle ebook listing on Amazon, demonstrating that the workflow reached an actual marketplace publication stage.

---

## Suggested Repository Structure

```text
ebook-creation-and-publishing-with-python-openai-api-calibre-kdp/
│
├── README.md
├── python_ai_code_generate_ebookv2.ipynb
│
├── assets/
│   ├── codegenerateimage.png
│   ├── calibre_epub_chapter_preview.png
│   └── amazon_kdp_published_ebook_listing.png
│
└── sample_outputs/
    ├── generated_markdown_sample.md
    └── epub_output_example.epub
```

---

## How to Run

1. Open the notebook in Google Colab.
2. Add an OpenAI API key in Colab Secrets using the name `OPENAI_API_KEY`.
3. Enable notebook access to the secret.
4. Mount Google Drive.
5. Configure the project folder path.
6. Run the content-generation cells.
7. Run the image-generation cells.
8. Run the EPUB-generation cells.
9. Review and edit the EPUB in Calibre.
10. Upload the final ebook package to Amazon KDP.

---

## What This Project Demonstrates

This project demonstrates the ability to connect multiple tools into one practical publishing workflow.

It combines:

- Prompt engineering.
- API usage.
- Automated text generation.
- Automated image generation.
- File handling.
- Markdown processing.
- EPUB construction.
- Digital publishing preparation.
- Final marketplace publication.

The value of the project is not only the ebook content.  
The technical achievement is the complete path from idea to code to generated assets to EPUB package to published digital product.

---

## Important Notes

This repository is intended as a technical demonstration of an AI-assisted ebook production workflow.

The sample children’s content is educational and should not be interpreted as medical, psychological, legal, or professional advice.

For sensitive topics involving children, emotional health, anxiety, bullying, or safety, content should be reviewed carefully by qualified professionals before being used in real educational or clinical settings.

---

## License

This repository can be shared as a portfolio project.  
Before using it commercially, review the terms and policies of all tools involved, including OpenAI, Amazon KDP, Calibre, and any third-party libraries.

