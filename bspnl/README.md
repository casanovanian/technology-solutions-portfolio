# bspnl — Financial Performance & Revenue Dashboard

**Domain:** Management reporting, financial visibility, and spreadsheet workflow simplification  
**Portfolio status:** Functional browser-based dashboard with Excel import and local reporting capabilities.

[← Back to portfolio](../README.md)

## Business challenge

Finance reporting often depends on spreadsheet formats that are familiar to finance teams but cumbersome for management to explore. Reviewing monthly performance, year-to-date trends, and revenue against budget can require repetitive filtering or rebuilding summaries.

## Solution

bspnl is a lightweight financial dashboard that converts structured Excel reports into interactive, management-friendly views without requiring a database or account-based hosting service.

### Documented capabilities

- Import Excel workbooks directly in the browser
- Monthly and year-to-date profit-and-loss calculations
- Revenue views using budget, actual-sales, and utility data sources
- Handling of multiple month-heading formats and changing report periods
- Data validation for missing, duplicate, or conflicting month columns
- Revenue and customer-level reporting, with coverage indicators
- Landscape print/PDF-friendly reporting
- Local JSON backup and restore for revenue reporting

## High-level architecture

```mermaid
flowchart LR
    A[Finance Excel files] --> B[Browser-local import]
    B --> C[Validation and normalisation]
    C --> D[Financial calculations]
    D --> E[P&L and revenue dashboards]
    E --> F[Print / export]
```

**Technology:** HTML, CSS, JavaScript, browser-based spreadsheet parsing, and standalone static web distribution.

**Privacy-oriented design:** The documented import workflow processes Excel files in the browser rather than sending them to a server. No server is required for the standalone dashboard.

## Architecture and delivery decisions

- Preserve established spreadsheet inputs while improving the reading experience.
- Recalculate key metrics from underlying details rather than reusing visual-only summary values.
- Make missing periods and inconsistent inputs visible instead of silently guessing.
- Support straightforward offline/local distribution without a new application backend.

## Evidence and maturity

The private repository documents the standalone dashboard, Excel-import scenarios, and regression tests for import refreshes, calculations, and reporting. No quantified time savings or financial results are asserted.

## Leadership perspective

Demonstrates the ability to identify a narrow business pain point, design a proportionate solution, and improve information access without introducing unnecessary enterprise infrastructure.

## Disclosure

Source workbooks, client-specific financial figures, logos, original screenshots, and source code are not included in this public portfolio.
