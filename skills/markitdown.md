# markitdown

## Summary

Lightweight Python utility from Microsoft for converting diverse files and office documents to Markdown, built specifically for LLMs and text analysis pipelines. Preserves document structure (headings, lists, tables, links) while producing clean, token-efficient Markdown output.

## Aliases

- Microsoft MarkItDown
- markitdown

## When to use

- Converting PDFs, Word docs, PowerPoint, Excel, images, audio, HTML, CSV, JSON, XML, ZIPs, EPubs to Markdown
- Preparing documents for LLM consumption or text analysis
- Extracting structured content from office documents
- YouTube URL transcription
- CLI-based document conversion pipelines

## Official URL

https://github.com/microsoft/markitdown

## Source / repo URL

https://github.com/microsoft/markitdown

## Trigger phrases

- convert to markdown
- document to markdown
- PDF to markdown
- extract text from PDF
- office document conversion
- markitdown

## Setup

```bash
# Full install (all formats)
pip install 'markitdown[all]'

# Specific formats only
pip install 'markitdown[pdf, docx, pptx]'

# From source
git clone https://github.com/microsoft/markitdown.git
cd markitdown
pip install -e 'packages/markitdown[all]'
```

Requires Python 3.10+. Use a virtual environment.

## Usage notes

**CLI:**
```bash
markitdown path-to-file.pdf > document.md
markitdown path-to-file.pdf -o document.md
cat path-to-file.pdf | markitdown
```

**Python:**
```python
from markitdown import MarkItDown
md = MarkItDown()
result = md.convert("path-to-file.pdf")
print(result.text_content)
```

**Supported formats:** PDF, PowerPoint, Word (DOCX), Excel (XLSX), Images (EXIF + OCR), Audio (EXIF + transcription), HTML, CSV, JSON, XML, ZIP, YouTube URLs, EPubs.

**Format tags:** `[all]`, `[pptx]`, `[docx]`, `[xlsx]`, `[xls]`, `[pdf]`, `[outlook]`, `[az-doc-intel]`, `[az-content-understanding]`, `[audio-transcription]`, `[youtube-transcription]`

**Plugins:** 3rd-party plugins disabled by default. List with `markitdown --list-plugins`, enable with `markitdown --use-plugins`.

## Caveats

- Runs with current process permissions — sanitize inputs
- Use `convert_stream()` / `convert_local()` for security-sensitive contexts
- Some format conversions pull in heavy dependencies (e.g., audio transcription)

## Related

- ocr-and-documents (Hermes skill for PDF/scan text extraction)
