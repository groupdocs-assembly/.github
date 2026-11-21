<h1 align="center">GroupDocs.Assembly</h1>

<h3 align="center">Document Automation and Reporting API: Generate Reports from Templates and Data in 40+ Formats</h3>

<p align="center">
  <strong>GroupDocs.Assembly</strong> is an on-premise document automation and reporting API that fills Word, Excel, PowerPoint, email, HTML and text templates with data from JSON, XML, CSV, databases, the tables of other documents and your own objects, and saves the reports in their own format or as PDF, XPS, HTML, images and more. Templates use a LINQ-based syntax for fields, loops, tables, lists, charts, images, barcodes, hyperlinks and conditional content. SDKs for .NET, Java, Node.js and Python.
</p>

[![Product Page](https://img.shields.io/badge/Product%20Page-2865E0?style=for-the-badge&logo=appveyor&logoColor=white)](https://products.groupdocs.com/assembly/)
[![Docs](https://img.shields.io/badge/Docs-2865E0?style=for-the-badge&logo=Hugo&logoColor=white)](https://docs.groupdocs.com/assembly/)
[![Demos](https://img.shields.io/badge/Demos-2865E0?style=for-the-badge&logo=appveyor&logoColor=white)](https://products.groupdocs.app/assembly/family)
[![API](https://img.shields.io/badge/API-2865E0?style=for-the-badge&logo=html5&logoColor=white)](https://reference.groupdocs.com/assembly/)
[![Blog](https://img.shields.io/badge/Blog-2865E0?style=for-the-badge&logo=WordPress&logoColor=white)](https://blog.groupdocs.com/category/assembly/)
[![Search](https://img.shields.io/badge/Search-2865E0?style=for-the-badge&logo=searchengin&logoColor=white)](https://search.groupdocs.com/)
[![Support](https://img.shields.io/badge/Support-2865E0?style=for-the-badge&logo=Discourse&logoColor=white)](https://forum.groupdocs.com/c/assembly)
[![Temp License](https://img.shields.io/badge/Temp%20License-2865E0?style=for-the-badge&logo=rocket&logoColor=white)](https://purchase.groupdocs.com/temporary-license)

## Latest Assembly News & Updates
* **NEW:** [GroupDocs.Assembly 26.11](https://www.nuget.org/packages/GroupDocs.Assembly/26.11.0) for .NET on NuGet. [Release notes](https://releases.groupdocs.com/assembly/net/release-notes/2026/groupdocs-assembly-for-net-26-11-release-notes/).
  * **JSON Schema for JSON data:** `JsonDataSource` takes a JSON Schema, so a template can reference members that are `null`, empty or missing in the data, while misspelled names still fail.
  * **Document preview:** `DocumentAssembler.GeneratePreview` renders pages of a template or a report to PNG, JPEG or BMP, with `PreviewOptions` for pages, size and resolution.
  * Also: external resources referenced from data (for example image URLs) are no longer loaded by default, so allow their hosts with `LoadSaveOptions.WhitelistedResources`; a .NET Framework 4.8 build; `RemoveEmptyParagraphs` for spreadsheet and plain text templates; document engines 26.10.
* **NEW:** Seven .NET sample repositories on GroupDocs.Assembly 26.11: Word, Excel and PowerPoint reports from JSON, ASP.NET Core report download, Docker, null-safe templates and documents from LLM output. Links in the .NET section below.
* GroupDocs.Assembly for Python via .NET 26.11: engine 26.7 with the .NET 10 runtime embedded, the first wheels for Linux and macOS (Intel and Apple Silicon), Python 3.5 - 3.14, and Python dicts and lists as data sources. Install it with `pip install groupdocs-assembly-net` from [PyPI](https://pypi.org/project/groupdocs-assembly-net/26.11.0/). [Release notes](https://releases.groupdocs.com/assembly/python-net/release-notes/2026/groupdocs-assembly-for-python-via-net-26-11-release-notes/).
* GroupDocs.Assembly for Java 26.11: the same JSON Schema support, document preview and control of external resources as .NET 26.11, plus engines 26.10. [Release notes](https://releases.groupdocs.com/assembly/java/release-notes/2026/groupdocs-assembly-for-java-26-11-release-notes/).

## Supported Platforms & Repository Groups

### .NET Document Automation (C#, ASP.NET, Services)
Generate documents and reports from templates on .NET Framework 4.0+ (with 4.6.2 and 4.8 builds), .NET Standard 2.0 and .NET 6, 8 and 10.
* **[GroupDocs.Assembly-for-.NET](https://github.com/groupdocs-assembly/GroupDocs.Assembly-for-.NET)**: Examples for every data source, template feature and output format.
* **[GroupDocs.Assembly.Mcp](https://github.com/groupdocs-assembly/GroupDocs.Assembly.Mcp)**: MCP server that lets Claude, Cursor, GitHub Copilot and other AI agents fill Word, Excel, PowerPoint, PDF and email templates with JSON, XML or CSV data locally: `dnx GroupDocs.Assembly.Mcp --yes`, or the `groupdocs/assembly-net-mcp` Docker image.

Sample projects, one scenario each, on .NET 8:
* **[word-report-from-template-net](https://github.com/groupdocs-assembly/word-report-from-template-net)**: fill a DOCX template from a .NET object or JSON and save it as DOCX or PDF, with no Microsoft Office on the server.
* **[excel-reports-from-template-net](https://github.com/groupdocs-assembly/excel-reports-from-template-net)**: Excel reports with repeating rows from JSON; `UseSpreadsheetDataTypes` keeps the numbers numbers.
* **[powerpoint-decks-from-json-net](https://github.com/groupdocs-assembly/powerpoint-decks-from-json-net)**: PowerPoint decks from JSON, with a table that grows with the data and a picture in every row.
* **[aspnet-core-report-download-net](https://github.com/groupdocs-assembly/aspnet-core-report-download-net)**: ASP.NET Core minimal API that returns a Word or PDF report and a PNG preview of its first page.
* **[document-generation-docker-net](https://github.com/groupdocs-assembly/document-generation-docker-net)**: document generation in a Linux container, with the fonts it needs.
* **[data-safe-templates-net](https://github.com/groupdocs-assembly/data-safe-templates-net)**: missing and null data in templates: JSON Schema, `AllowMissingMembers` and `InlineErrorMessages`.
* **[llm-json-to-branded-documents-net](https://github.com/groupdocs-assembly/llm-json-to-branded-documents-net)**: Word and PDF documents from LLM output, with a JSON Schema as the contract between the model and the template.

```csharp
using GroupDocs.Assembly;
using GroupDocs.Assembly.Data;

// Fill a Word template with JSON data and save the report as PDF
var assembler = new DocumentAssembler();
assembler.AssembleDocument("template.docx", "report.pdf",
    new DataSourceInfo(new JsonDataSource("customer.json"), "customer"));
```

### Java Document Automation (Maven, Spring)
Native Java library for templated documents with loops, tables, charts, images, barcodes and conditional content.
* **[GroupDocs.Assembly-for-Java](https://github.com/groupdocs-assembly/GroupDocs.Assembly-for-Java)**: Java examples; the package `com.groupdocs:groupdocs-assembly` comes from the [GroupDocs Maven repository](https://releases.groupdocs.com/java/repo/).

```java
import com.groupdocs.assembly.DataSourceInfo;
import com.groupdocs.assembly.DocumentAssembler;
import com.groupdocs.assembly.JsonDataSource;

// Fill a Word template with JSON data and save the report as PDF
DocumentAssembler assembler = new DocumentAssembler();
assembler.assembleDocument("template.docx", "report.pdf",
    new DataSourceInfo(new JsonDataSource("customer.json"), "customer"));
```

### Node.js Document Automation (Node.js via Java)
Add report generation to Node.js services and scripts with the Java engine: `npm install @groupdocs/groupdocs.assembly`.
* [Documentation](https://docs.groupdocs.com/assembly/nodejs-java/) | [Release Notes](https://releases.groupdocs.com/assembly/nodejs-java/release-notes/)

```javascript
const assembly = require('@groupdocs/groupdocs.assembly');

// Fill a Word template with JSON data and save the report as PDF
const assembler = new assembly.DocumentAssembler();
assembler.assembleDocument('template.docx', 'report.pdf',
    new assembly.DataSourceInfo(new assembly.JsonDataSource('customer.json'), 'customer'));
```

### Python Document Automation (Python via .NET)
A self-contained Python package with the .NET runtime embedded: `pip install groupdocs-assembly-net`, Python 3.5 - 3.14 on Windows, Linux and macOS.
* **[GroupDocs.Assembly-for-Python-via-.NET](https://github.com/groupdocs-assembly/GroupDocs.Assembly-for-Python-via-.NET)**: Runnable examples for every documented scenario, with a Dockerfile.
* [PyPI](https://pypi.org/project/groupdocs-assembly-net/) | [Docs](https://docs.groupdocs.com/assembly/python-net/) | [API Reference](https://reference.groupdocs.com/assembly/python-net/) | [Release Notes](https://releases.groupdocs.com/assembly/python-net/release-notes/)

```python
from groupdocs.assembly import DataSourceInfo, DocumentAssembler

# Fill a Word template with a Python dict and save the report as PDF
customer = {"Name": "Quayside Bistro", "Product": "Harbor Blend whole bean coffee"}
DocumentAssembler().assemble_document("template.docx", "report.pdf", DataSourceInfo(customer, "customer"))
```

## Business Use-Cases
- **Quotes, invoices and contracts:** fill line items, totals and terms, with conditional pricing and clauses.
- **Batch reports:** orders, shipments and statements from SQL, JSON or CSV data.
- **Mail merge by email:** personalised MSG and EML messages with tables and lists.
- **Dashboards in documents:** charts, tables and summary figures computed in the template from the data.
- **Labels, badges and certificates:** barcodes, QR codes and images placed from the data.

## API Key Features & Benefits
- 40+ formats: Word (DOC, DOCX, DOCM, DOT, DOTX, DOTM, RTF, ODT, OTT, TXT, Markdown), Excel (XLS, XLSX, XLSM, XLSB, XLT, XLTX, XLTM, ODS), PowerPoint (PPT, PPTX, PPTM, PPS, PPSX, PPSM, POT, POTX, POTM, ODP, OTP), email (MSG, EML, EMLX) and web (HTML, MHTML) templates; reports also as PDF, XPS, OXPS, TIFF, SVG, PostScript, PCL, XAML and EPUB.
- Template syntax: expressions, loops, conditions, variables and LINQ-style data operations (filtering, ordering, grouping, aggregates).
- Data sources: JSON, XML, CSV, databases, the tables of Word, Excel and PowerPoint documents, and .NET, Java or Python objects.
- Content: tables, bulleted and numbered lists, charts, images, barcodes and QR codes, hyperlinks, bookmarks, check boxes and inserted documents.
- Formatting: number, date and text formats, ordinal, cardinal and alphabetic numbers, and text casing.
- Output: the template's own format or another of its family; fields and formulas can be updated on save.

## Getting Started
- .NET: `dotnet add package GroupDocs.Assembly`
- Java: add `com.groupdocs:groupdocs-assembly` from the GroupDocs repository, `https://releases.groupdocs.com/java/repo/`
- Node.js: `npm install @groupdocs/groupdocs.assembly`
- Python: `pip install groupdocs-assembly-net`
- Run the sample projects from the repositories above to fill Word, Excel, PowerPoint and email templates from JSON, XML and CSV data.

## Technical Support & Resources
- Documentation and tutorials: https://docs.groupdocs.com/assembly/
- Free support forum: https://forum.groupdocs.com/c/assembly
- Temporary license for full-feature evaluation: https://purchase.groupdocs.com/temporary-license

## Tags

`groupdocs-assembly` `document-automation` `document-generation` `report-generation` `template-engine` `reporting-api` `mail-merge` `linq-templates` `word-automation` `excel-reporting` `pdf-generation` `json-to-docx` `data-binding` `barcode-generation` `chart-reporting` `invoice-generation` `python`
