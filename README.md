# Awesome-Online-Invoicing-Payment-Tracking

# Awesome Online Invoicing & Payment Tracking

> A curated list of top Online Invoicing and Payment Tracking platforms — both SaaS/Hosted commercial solutions and open-source alternatives for creating invoices, tracking payments, and managing business finances.
> 🌟 Star this repo if you find it useful! 🌟

---

## 📋 Table of Contents

- [SaaS / Hosted Platforms](#-saas--hosted-platforms)
  - [FreshBooks](#freshbooks)
  - [QuickBooks Online](#quickbooks-online)
  - [Xero](#xero)
  - [Wave](#wave)
  - [Square Invoices](#square-invoices)
- [Open-Source Software](#-open-source-software)
  - [Invoice Ninja](#invoice-ninja)
  - [InvoiceShelf](#invoiceshelf)
  - [InvoicePlane](#invoiceplane)
  - [Kimai](#kimai)
  - [Summit (Kugie)](#summit-kugie)
  - [BillKu](#billku)
  - [Crater (Archived)](#crater-archived)
  - [FOSSBilling](#fossbilling)

---

## 🟦 SaaS / Hosted Platforms

Commercial, cloud-hosted Online Invoicing and Payment Tracking platforms. These are not open-source but are included as reference points for feature comparison.

### FreshBooks
**Type:** Accounting and invoicing for small businesses
FreshBooks provides invoicing, expense tracking, time tracking, and payment processing for freelancers and small businesses. It is known for its user-friendly interface and strong customer support, with pricing tiers based on client count.

### QuickBooks Online
**Type:** Comprehensive accounting with invoicing
QuickBooks Online is the most widely adopted small business accounting platform, with invoicing, expense tracking, bank reconciliation, and reporting. It is positioned for businesses wanting full accounting capabilities alongside invoicing, with pricing tiers based on features and company size.

### Xero
**Type:** Cloud accounting with invoicing and bank feeds
Xero provides cloud accounting with invoicing, bank reconciliation, and reporting, with a strong ecosystem of third-party integrations. It is popular among small businesses and accountants, particularly outside the US.

### Wave
**Type:** Free accounting and invoicing for small businesses
Wave offers free invoicing, accounting, and receipt scanning for small businesses, monetizing through payment processing and payroll add-ons. It is positioned as an accessible entry point for freelancers and micro-businesses.

### Square Invoices
**Type:** Invoicing integrated with Square payments
Square Invoices provides invoice creation and payment tracking within the Square ecosystem, with integrated card processing and automated reminders. It is positioned for businesses already using Square for in-person payments.

---

## 🟩 Open-Source Software

Self-hosted, community-driven Online Invoicing and Payment Tracking tools. The open-source ecosystem spans **mature platforms with e-invoicing**, **modern Laravel/Vue applications**, **time-tracking-first tools**, and **abandoned projects to avoid**.

### Invoice Ninja
**Stack:** PHP / Laravel / MySQL | **License:** Elastic License 2.0 (source-available)
Invoice Ninja is the most widely deployed open-source invoicing platform, with a health score of 96/100 and very active development . It provides invoicing, recurring invoices, client portal, expense tracking, and payment gateway integrations. **Important licensing caveat:** It uses the Elastic License 2.0, which is source-available but not OSI-approved open source, limiting commercial reuse and redistribution . **E-invoicing:** Invoice Ninja is the only self-hosted option with built-in support for **ZUGFeRD, XRechnung, Facturae, FatturaPA, and generic EN16931**, though FatturaPA is marked as not production-ready due to the Italian SDI connection not being live . Peppol network access runs through Invoice Ninja's hosted platform as part of its Enterprise plan ($18/month, 250 credits) . **Self-hosted cost:** Fully functional at no cost, with white-label branding available for $40/year .
**Best for:** Businesses wanting the most feature-complete open-source invoicing platform with EU e-invoicing compliance built in, accepting the source-available licensing and Peppol dependency.

### InvoiceShelf
**Stack:** PHP / Laravel / Vue.js / PostgreSQL | **License:** AGPL-3.0
InvoiceShelf is the actively maintained fork of the abandoned Crater project, explicitly recommended over Crater in 2026 comparisons . It provides invoicing, estimates, expense tracking, payment management, tax handling, multi-currency, customer portal, email integration, financial reports, custom fields, multiple companies, REST API, mobile apps, and Docker deployment . It is positioned as a comprehensive open-source invoicing and expense management platform for small to medium businesses. **Note:** InvoiceShelf lists no e-invoice format among its features, unlike Invoice Ninja .
**Best for:** Businesses wanting a genuinely open-source (AGPL-3.0) invoicing platform with a modern Laravel/Vue stack and active development, accepting the absence of built-in EU e-invoicing.

### InvoicePlane
**Stack:** PHP / CodeIgniter / MySQL | **License:** MIT
InvoicePlane is a self-hosted open-source application for managing quotes, invoices, clients, and payments . Features include invoice creation with saved products and tax rates, CRM-like customer management with custom fields, quote approval via a client web panel, PayPal one-click payments, and payment tracking linked to invoices . **E-invoicing:** InvoicePlane has an e-invoicing hook but ships no format in its core—you add templates from the project's InvoicePlane-e-invoices repository, which has examples for ZUGFeRD, Factur-X, and UBL . It is a mature, stable option for businesses not needing EU e-invoicing out of the box.
**Best for:** Businesses wanting a proven, MIT-licensed invoicing platform with straightforward features and optional e-invoicing templates, accepting a dated UI compared to newer alternatives.

### Kimai
**Stack:** PHP / Symfony / MySQL | **License:** AGPL-3.0
Kimai is a time-tracking-first platform where invoices are generated from approved timesheet entries, making line items the work you logged . It is the strongest choice for businesses that bill by the hour, with templates in DOCX, ODS, or XLSX formats that you design in a word processor (easier than editing CSS) . **E-invoicing:** The paid E-Invoice Plus plugin covers EN16931, XRechnung, ZUGFeRD, Factur-X, and Peppol (in beta), but not Facturae or FatturaPA . **Limitation:** Kimai takes no online payments—you email the PDF and get paid by transfer. Its free Customer Portal plugin shares timesheets and project statistics via a secret link, but not invoices .
**Best for:** Freelancers and agencies billing by the hour who want invoice generation directly from timesheets, accepting that payment collection is manual.

### Summit (Kugie)
**Stack:** Next.js / TypeScript / PostgreSQL / Drizzle | **License:** Open Source (per repository)
Summit is a modern open-source invoicing and finance tool built with Next.js and TypeScript, positioned for businesses wanting a comprehensive finance management platform . Key features include:
- **Invoicing** with PDF generation, email sending, status tracking (Draft, Sent, Paid, Overdue, Cancelled), and **Xendit payment integration** 
- **Quoting** with PDF generation, email sending, status tracking, and **one-click quote-to-invoice conversion** 
- **Expense and income tracking** with receipt uploads (Minio/S3) and categorization 
- **Recurring transactions** on daily, weekly, monthly, or yearly schedules with cron-based automation 
- **Client portal** with magic link authentication 
- **Team management** with Admin, Accountant, and Staff roles 
- **Financial reports**: Profit & Loss, Invoice Summary, Aging Receivables, Expense Breakdown 

Deploys on Railway with PostgreSQL, MinIO, and webhook processing. **Trade-off:** Payment integration is Xendit-specific (popular in Southeast Asia), not Stripe or PayPal.
**Best for:** Teams in Southeast Asia or those using Xendit wanting a modern, comprehensive invoicing and finance platform, accepting the payment gateway dependency.

### BillKu
**Stack:** NestJS / Next.js / Prisma / PostgreSQL | **License:** Open Source (per repository)
BillKu is a comprehensive open-source billing and business management platform for SMEs, combining invoicing with CRM, POS, HR/payroll, inventory, and financial reporting in a single unified platform . Key features include:
- **Full invoice lifecycle** (Draft → Sent → Partial → Paid → Overdue) with quotations, purchase orders, credit notes, delivery notes, and recurring invoices 
- **Financial reporting**: P&L, balance sheet, cash flow statement, general ledger, receivables aging, CSV & tax export 
- **CRM** with deal pipeline, activity tracking, and customer segmentation 
- **POS** with session-based cash management, barcode support, and auto-deduct inventory 
- **HR & Payroll** with automated generation, attendance tracking, and approval workflow 
- **Integrations**: WhatsApp for invoice sending and payment reminders, Indonesian payment gateways (Midtrans, Xendit, DOKU), e-commerce marketplaces (Tokopedia, Shopee, Lazada), and SMTP email 

Deploys via Docker with SQLite (dev) or PostgreSQL (prod). **Trade-off:** The breadth of features (POS, HR, CRM) makes it heavier than a dedicated invoicing tool, and payment integrations are Indonesia-focused.
**Best for:** SMEs wanting an all-in-one business platform with invoicing at its core, particularly in Indonesian markets, accepting the broader scope and regional payment focus.

### Crater (Archived)
**Stack:** Laravel / Vue.js | **License:** AGPL-3.0
Crater was a popular open-source invoicing platform, but its default branch has had **no commits for 1,329 days** as of October 2026, and InvoiceShelf's migration guide explicitly calls it "the now abandoned Crater project" . **Not recommended for new deployments.** Any guide still recommending Crater was written before the project went quiet. InvoiceShelf carries the same AGPL-3.0 license and data model, so migration is a database migration rather than a rewrite .
**Best for:** Historical reference only; use InvoiceShelf instead for an actively maintained fork.

### FOSSBilling
**Stack:** PHP / Doctrine / MySQL/MariaDB | **License:** Apache-2.0
FOSSBilling is a free and open-source billing and client management solution specifically designed for **hosting businesses**, with 1,705 stars and active development (last push September 2026) . It provides invoicing, payment processing, and client management tailored to hosting providers. It is Apache-2.0 licensed, making it permissively available for commercial use.
**Best for:** Hosting companies and web service providers needing a billing platform tailored to their specific business model, accepting the hosting-industry focus.

---

## 📊 Comparison at a Glance

| Software | License | Stack | E-Invoicing | Payment Gateways | Self-Hosted | Best For |
|----------|---------|-------|-------------|------------------|-------------|----------|
| **FreshBooks** | Proprietary | Cloud | (Check) | ✅ | ❌ | Small business accounting |
| **QuickBooks** | Proprietary | Cloud | ❌ | ✅ | ❌ | Full accounting + invoicing |
| **Invoice Ninja** | Elastic 2.0 | PHP/Laravel | ✅ ZUGFeRD/XRechnung/etc | ✅ | ✅ | EU e-invoicing + full features |
| **InvoiceShelf** | AGPL-3.0 | Laravel/Vue | ❌ | ✅ | ✅ | Active OSS invoicing |
| **InvoicePlane** | MIT | PHP/CodeIgniter | (Templates) | ✅ PayPal | ✅ | Proven MIT option |
| **Kimai** | AGPL-3.0 | PHP/Symfony | ✅ (Paid plugin) | ❌ | ✅ | Hourly billing from timesheets |
| **Summit** | Open Source | Next.js/Postgres | ❌ | ✅ Xendit | ✅ | Modern finance platform |
| **BillKu** | Open Source | NestJS/Next.js | ❌ | ✅ Indonesia-focused | ✅ | All-in-one SME platform |
| **FOSSBilling** | Apache-2.0 | PHP/Doctrine | ❌ | ✅ | ✅ | Hosting business billing |

---

## 🤝 Contributing

Contributions are welcome! If you know of an open-source Online Invoicing or Payment Tracking tool that should be listed here, please open a pull request with:

- Project name and URL
- Brief description (1–2 sentences)
- Stack and license
- Why it stands out

Please ensure the project is actively maintained (releases within the last 12 months) and genuinely open-source (or clearly note if it is source-available but not OSI-approved, as with Invoice Ninja).

**Note on the open-source ecosystem:** The invoicing landscape is dominated by **Invoice Ninja** for feature depth and EU e-invoicing compliance, but its Elastic License 2.0 is source-available rather than OSI-approved . **InvoiceShelf** is the strongest genuinely open-source (AGPL-3.0) option, having replaced the abandoned Crater project . For hourly billing, **Kimai** uniquely generates invoices directly from timesheets . **Crater** should be avoided entirely due to abandonment . The right choice depends on whether you need EU e-invoicing (Invoice Ninja), a permissive license (InvoicePlane), or modern tooling (Summit, BillKu).

---

## 📄 License

This list is released under CC0 1.0 Universal (Public Domain). The software projects listed retain their respective licenses.

---

⭐ **If this list helped you discover a useful tool, please star the repo!** ⭐
