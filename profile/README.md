<h1 align="center">GroupDocs.Assembly</h1>

<h3 align="center">Powerful Document automation & reporting API to assemble templates into DOCX, PDF, XLSX, PPTX, HTML, and more than 50+ document formats</h3>

<p align="center">
  <strong>GroupDocs.Assembly</strong> is a on-premise solution for document automation and reporting API that generates documents from templates and data sources (JSON, XML, CSV, OData, databases, .NET/Java objects, REST, and more). Automate quotes, contracts, invoices, and reports across popular Office, PDF, HTML, and image formats with LINQ-based templates, barcodes, charts, conditional logic, and mail-merge style fields.
</p>

[![Product Page](https://img.shields.io/badge/Product%20Page-2865E0?style=for-the-badge&logo=appveyor&logoColor=white)](https://products.groupdocs.com/assembly/)
[![Docs](https://img.shields.io/badge/Docs-2865E0?style=for-the-badge&logo=Hugo&logoColor=white)](https://docs.groupdocs.com/assembly/)
[![Demos](https://img.shields.io/badge/Demos-2865E0?style=for-the-badge&logo=appveyor&logoColor=white)](https://products.groupdocs.app/assembly/family)
[![API](https://img.shields.io/badge/API-2865E0?style=for-the-badge&logo=html5&logoColor=white)](https://apireference.groupdocs.com/assembly/)
[![Blog](https://img.shields.io/badge/Blog-2865E0?style=for-the-badge&logo=WordPress&logoColor=white)](https://blog.groupdocs.com/category/assembly/)
[![Search](https://img.shields.io/badge/Search-2865E0?style=for-the-badge&logo=searchengin&logoColor=white)](https://search.groupdocs.com/)
[![Support](https://img.shields.io/badge/Support-2865E0?style=for-the-badge&logo=Discourse&logoColor=white)](https://forum.groupdocs.com/c/assembly)
[![Temp License](https://img.shields.io/badge/Temp%20License-2865E0?style=for-the-badge&logo=rocket&logoColor=white)](https://purchase.groupdocs.com/temporary-license)

## Latest Assembly News & Updates
- Published [GroupDocs.Assembly 25.12](https://www.nuget.org/packages/GroupDocs.Assembly/) release with importants fixes and (improvements)[https://releases.groupdocs.com/assembly/net/release-notes/2025/groupdocs-assembly-for-net-25-12-release-notes/].
- Improved barcode image generation and embedding in assembled reports under Linux.
- Enhanced [examples](https://github.com/groupdocs-assembly/GroupDocs.Assembly-for-.NET) for JSON/CSV/SQL data sources, HTML output, and attachments.

## Supported Platforms & Repository Groups

### .NET Document Automation (C#, ASP.NET, WinForms, Services)
On-premise engine to build documents from templates using LINQ syntax, mail-merge style fields, sequential data, and conditional logic. Supports CSV, JSON, XML, OData, DB queries, and custom .NET types.
- **GroupDocs.Assembly-for-.NET**: Core API with charts, barcodes, conditional/loop regions, and field updating.  
  Repo & examples: https://github.com/groupdocs-assembly/GroupDocs_Assembly_NET/tree/master/Examples
- **Showcases & Plugins**: ASP.NET Web Forms demo and plugins for progress tracking and template comparison.  
  Repo: https://github.com/groupdocs-assembly/GroupDocs_Assembly_NET/tree/master/Showcases

```csharp
// Assemble DOCX from a LINQ-enabled Word template with JSON data
DocumentAssembler assembler = new DocumentAssembler();
assembler.AssembleDocument(
    CommonUtilities.GetSourceDocument("Templates/Quote.docx"),
    CommonUtilities.SetDestinationDocument("Reports/Quote.docx"),
    new DataSourceInfo(CommonUtilities.GetJsonData("data.json"), "orders"));
```

### Java Document Automation (Maven, Spring)
Native Java library for templated document generation with regions, conditions, barcodes, and HTML resources.
- Repository: https://github.com/groupdocs-assembly/GroupDocs.Assembly-for-Java

```java
// Assemble a contract from DOCX template using a Java object data source
DocumentAssembler assembler = new DocumentAssembler();
assembler.assembleDocument(
    "Templates/Contract.docx",
    "Reports/Contract Output.docx",
    new DataSourceInfo(new CustomerData(), "customer"));
```

### Python & Node.js (via .NET or Java)
Use the .NET or Java engine from Python/Node.js to automate report generation in scripts or services.
- Python via .NET: https://github.com/groupdocs-assembly/GroupDocs.Assembly-for-Python-via-.NET  
- Node.js via Java: https://github.com/groupdocs-assembly/GroupDocs.Assembly-for-Node.js-via-Java

```python
from groupdocs.assembly import DocumentAssembler, DataSourceInfo

assembler = DocumentAssembler()
assembler.assemble_document(
    "Templates/Invoice.docx",
    "Reports/Invoice.pdf",
    DataSourceInfo({"items": items, "customer": customer}, "data"))
```

## Business Use-Cases
- Quote, invoice, and contract generation with conditional pricing and tax logic.
- Batch report assembly (orders, shipments, statements) from SQL/JSON feeds.
- Dynamic proposals and SOWs with reusable content blocks and nested regions.
- Compliance-ready PDFs with updated fields, attachments, and barcodes.
- Marketing docs: personalized brochures, event badges, and certificates.

## API Key Features & Benefits
- 50+ formats: DOCX, DOTX, XLSX, PPTX, PDF, HTML/MHTML, ODS/ODT/OTP, MSG/EML, TXT/MD, SVG.
- Template syntax: LINQ regions, mail-merge fields, conditional/loop blocks, formulas, and inline expressions.
- Data sources: JSON, XML, CSV, OData, DB/SQL, REST, custom objects, external docs, and Word/Excel tables.
- Content controls: charts, tables, lists, images, barcodes, attachments, hyperlinks, and HTML resources.
- Formatting: number/date/text casing, ordinal/cardinal/alphabetic formatting, custom format strings.
- Security & output: password-protected templates, HTML with resources, PDF, XPS, images; update fields on save.
- Cross-platform: .NET Framework/Core, Java SE/EE, Linux/Windows/macOS; COM Interop for legacy stacks.

## Getting Started
- .NET: `Install-Package GroupDocs.Assembly` or `dotnet add package GroupDocs.Assembly`
- Java: Add `groupdocs-assembly` from Maven Central.
- Run sample projects in the repositories above to assemble Word/Excel/PDF reports from JSON/SQL/CSV.

## Technical Support & Resources
- Documentation and tutorials: https://docs.groupdocs.com/assembly/
- Free support forum: https://forum.groupdocs.com/c/assembly
- Temporary license for full-feature evaluation: https://purchase.groupdocs.com/temporary-license

## Tags
`document-automation` `document-generation` `template-engine` `reporting-api` `mail-merge` `linq-templates` `word-automation` `excel-reporting` `pdf-generation` `json-to-docx` `sql-to-pdf` `data-binding` `batch-reporting` `barcode-generation` `chart-reporting` `contract-automation` `invoice-generation` `quote-builder` `document-sdk`

