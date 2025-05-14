---
icon: pen-to-square
---

# Document Triage Rejection Reasons

### Document Triage Rejection Reasons

### Tier 1 Critical Issues (Must Be Resolved for Spreading):

These issues prevent financial statements from being reliably understood, identified, or processed. They typically undermine the integrity, completeness, or accessibility of the data, making it impossible or too risky to produce an accurate financial spread.

* Completeness
* Validity
* Consistency
* Integrity
* Format



1. **Missing company name (integrity\_missing\_company\_name)**

A clear entity name is essential for proper attribution of financial data. Accurate identification is a fundamental prerequisite for processing. Inconsistent company name

Significant inconsistencies in company name will render the dataset unreliable. Minor inconsistencies in company names can be resolved through normalization rules, though this adds processing friction.



2. **Document Descriptor Mismatch (consistency\_document\_descriptor\_mismatch)**

The document contains significant inconsistencies or mismatches in descriptors (e.g., file name, table header, table title, or sheet name). These discrepancies cause ambiguity, making it difficult to accurately identify, classify, and process the document.



3. **Encrypted file without password (validity\_encrypted\_file\_without\_password)**

Document cannot be opened or processed, preventing any data extraction from taking place.



4. **Invalid file types (validity\_unsupported\_file\_format)**

The uploaded documents use formats not supported by the system (only .pdf and .xlsx).



5. **Redacted statement (integrity\_redacted\_statement)**

When essential financial information (such as revenue lines or total assets) is removed, the dataset becomes incomplete, compromising the integrity of the spread.



6. **Missing pages (completeness\_missing\_pages)**

Incomplete documents with missing key sections (such as portions of the balance sheet or income statement) render the dataset unreliable.



7. **Truncated line items (completeness\_truncated\_line\_items)**

Partially missing line items (truncated numbers or text) prevent confident interpretation of the data and may indicate a corrupted or poorly scanned document.



8. **Other critical issues (other\_critical\_issues)**

Other issues prevent financial statements from being reliably understood, identified, or processed.

\


### Tier 2 Suboptimal but Processable Issues

While these issues impact efficiency and require more manual intervention or produce less reliable insights, they do not strictly prohibit the creation of a financial spread. Addressing these issues will improve accuracy, reduce manual rework, and enable smoother processing.



1. **Excessive cell usage (format\_excessive\_cell\_usage)**

Multiple statements and complex formatting may slow down parsing but doesn't prevent it. Data can be extracted with additional manual effort.



2. **Non-standard statement structure (format\_non\_standard\_structure)**

The uploaded statements deviate significantly from standard reporting structures, making it difficult to identify, parse, and extract the necessary financial data efficiently.



3. **Foreign currency (format\_foreign\_currency)**

Handling foreign currency adds complexity.



4. **Unbalanced balance sheet (integrity\_unbalanced\_balance\_sheet)**

While the fundamental accounting principle requires assets = liabilities + equity, minor imbalances may still be processed depending on client tolerance.



5. **Limited line items (format\_sparse\_line\_items)**

While sparse detail reduces analysis granularity, available data can still be recorded and processed.



6. **Tampered statements (integrity\_tampered\_statement)**

Statements that have been detected as altered, manipulated, or falsified after their original creation cannot be relied upon.&#x20;



7. **Cash-basis accounting (instead of accrual) (format\_cash\_basis\_accounting)**

Depending on client’s preference - while accrual-based statements are often preferred, cash-basis data can still be spread, though it may offer less comparable insights.



8. **Missing key line item (e.g. interest expense) (completeness\_missing\_key\_line\_items)**

While the absence of specific items (such as interest expense) isn't ideal, spreads can still be completed with less comprehensive analysis.



9. **Miscellaneous minor issues: (other\_miscellaneous\_minor\_issues)**

Various minor format or quality concerns can be addressed with additional effort, impacting efficiency but not feasibility.

\


### Case Level Rejection Reasons (Problems Across the Document Set):

These issues arise when considering the entire collection of documents provided for a given case, rather than evaluating each document in isolation. While no single document may trigger a rejection, the combined set fails to provide a coherent, complete, and reliable financial picture.



1. **Missing reporting periods (completeness\_missing\_reporting\_periods)**

Not all required reporting periods are included (e.g., missing a critical quarter or year), making it impossible to conduct a complete analysis.



2. **Missing key statement types (completeness\_missing\_key\_statement\_types)**

The collection is missing entire categories of essential documents (e.g., no balance sheet or no income statement), preventing a complete financial evaluation.



3. **Conflicting entity identification (consistency\_entity\_identification\_conflict)**

Across multiple documents, there are inconsistencies in the company's name, consolidated entity, subsidiaries, or other identifying details that cannot be conclusively matched to the customer.



4. **Conflicting financial data (consistency\_financial\_data\_conflict)**

Different documents provide contradictory figures for the same statement type and period, undermining the reliability of the document set.



5. **Inconsistent accounting methods (consistency\_accounting\_method\_conflict)**

Some documents follow accrual accounting while others follow cash-basis, or use different accounting standards (e.g., GAAP vs. IFRS). Mixing different methodologies across the set can produce misleading aggregate results and complicate any meaningful comparison.



6. **Mixed currency usage (consistency\_mixed\_currency)**

Different documents use different currencies, and handling multiple currencies adds complexity.

\
\
