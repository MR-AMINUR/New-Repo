# 🌐 Flowbit AI Dashboard

A full-stack **analytics dashboard** powered by **AI-driven insights**.  
Built with **Next.js (frontend)**, **Node.js (backend)**, **PostgreSQL (NeonDB)**, and **Vanna AI** for natural language data querying.

---

## ⚙️ Setup & Configuration

### Prerequisites
- **Node.js ≥ 18**
- **NeonDB PostgreSQL** connection (live or local)
- Environment variables configured in `.env.local`

```bash
# .env.local
DATABASE_URL="npg_V8PGH3gLzhen@ep-blue-glitter-ad8u7od3-pooler.c-2.us-east-1.aws.neon.tech"
VANNA_API_BASE_URL="https://analytics-ai-dashboard.onrender.com"

🧩 Run Locally
# Start backend
cd apps/api
npm install
npm run dev

# Start frontend
cd ../web
npm install
npm run dev


Once running:
    Frontend: http://localhost:3000
    Backend API: http://localhost:4000

🧠 API Routes & Example Responses

All endpoints are RESTful and return JSON responses.
Base URL (Production):
https://flowbit-ai-jade.vercel.app

GET /api/stats

Returns overview metrics for the dashboard.

Example Response:
{
    "totalSpendYtd": 49938.42,
    "totalInvoices": 19,
    "documentsUploaded": 19,
    "averageInvoiceValue": 3226.37
}


GET /api/invoice-trends

Returns monthly invoice volume and spend.

Example Response:
{
    "total": 19,
    "page": 1,
    "pageSize": 25,
    "rows": [
        {
            "invoice_id": "12",
            "invoice_number": "-",
            "invoice_date": null,
            "amount": 0,
            "currency": "€",
            "vendor": {
                "vendor_id": "13",
                "vendor_name": "-"
            },
            "customer": {
                "customer_id": "13",
                "customer_name": "-"
            },
            "status": "pending"
        },
        {
            "invoice_id": "10",
            "invoice_number": "1234",
            "invoice_date": "2025-11-04T00:00:00.000Z",
            "amount": -358.79,
            "currency": "-",
            "vendor": {
                "vendor_id": "11",
                "vendor_name": "Musterfirma Müller"
            },
            "customer": {
                "customer_id": "11",
                "customer_name": "Max Mustermann"
            },
            "status": "pending"
        },
        {
            "invoice_id": "11",
            "invoice_number": "1234",
            "invoice_date": "2025-11-04T00:00:00.000Z",
            "amount": -358.79,
            "currency": "€",
            "vendor": {
                "vendor_id": "12",
                "vendor_name": "Musterfirma Müller"
            },
            "customer": {
                "customer_id": "12",
                "customer_name": "Max Mustermann"
            },
            "status": "pending"
        },
        {
            "invoice_id": "22",
            "invoice_number": "S018418",
            "invoice_date": "2025-10-27T00:00:00.000Z",
            "amount": 84,
            "currency": "₹",
            "vendor": {
                "vendor_id": "23",
                "vendor_name": "LAXMIDAIRY"
            },
            "customer": null,
            "status": "pending"
        },
        {
            "invoice_id": "1",
            "invoice_number": "INV-1001",
            "invoice_date": "2025-10-01T00:00:00.000Z",
            "amount": 17700,
            "currency": "₹",
            "vendor": {
                "vendor_id": "1",
                "vendor_name": "TechNova Solutions"
            },
            "customer": {
                "customer_id": "1",
                "customer_name": "Rohit Sharma"
            },
            "status": "overdue"
        },
        {
            "invoice_id": "2",
            "invoice_number": "INV-1002",
            "invoice_date": "2025-09-12T00:00:00.000Z",
            "amount": 1428,
            "currency": "€",
            "vendor": {
                "vendor_id": "2",
                "vendor_name": "Alpha Supplies Co."
            },
            "customer": {
                "customer_id": "2",
                "customer_name": "Max Mustermann"
            },
            "status": "overdue"
        },
        {
            "invoice_id": "3",
            "invoice_number": "INV-1003",
            "invoice_date": "2025-08-20T00:00:00.000Z",
            "amount": 1176,
            "currency": "£",
            "vendor": {
                "vendor_id": "3",
                "vendor_name": "DataFlow Systems"
            },
            "customer": {
                "customer_id": "3",
                "customer_name": "John Doe"
            },
            "status": "overdue"
        },
        {
            "invoice_id": "17",
            "invoice_number": "Re-147/2025",
            "invoice_date": "2025-08-08T00:00:00.000Z",
            "amount": 2840,
            "currency": "€",
            "vendor": {
                "vendor_id": "18",
                "vendor_name": "EasyFirma GmbH & Co KG"
            },
            "customer": {
                "customer_id": "18",
                "customer_name": "Mustermann GmbH."
            },
            "status": "overdue"
        },
        {
            "invoice_id": "4",
            "invoice_number": "INV-1004",
            "invoice_date": "2025-07-15T00:00:00.000Z",
            "amount": 24780,
            "currency": "₹",
            "vendor": {
                "vendor_id": "4",
                "vendor_name": "NextGen Pvt Ltd"
            },
            "customer": {
                "customer_id": "4",
                "customer_name": "Ananya Gupta"
            },
            "status": "overdue"
        },
        {
            "invoice_id": "5",
            "invoice_number": "INV-1005",
            "invoice_date": "2025-06-10T00:00:00.000Z",
            "amount": 2975,
            "currency": "€",
            "vendor": {
                "vendor_id": "5",
                "vendor_name": "Pixel Works"
            },
            "customer": {
                "customer_id": "5",
                "customer_name": "Sophia Meyer"
            },
            "status": "overdue"
        },
        {
            "invoice_id": "6",
            "invoice_number": "INV-1006",
            "invoice_date": "2025-05-01T00:00:00.000Z",
            "amount": -327,
            "currency": "$",
            "vendor": {
                "vendor_id": "6",
                "vendor_name": "CloudAxis"
            },
            "customer": {
                "customer_id": "6",
                "customer_name": "Michael Clark"
            },
            "status": "pending"
        },
        {
            "invoice_id": "23",
            "invoice_number": "123100401",
            "invoice_date": "2024-03-01T00:00:00.000Z",
            "amount": 381.12,
            "currency": "€",
            "vendor": {
                "vendor_id": "24",
                "vendor_name": "CPB SOFTWARE (GERMANY) GMBH"
            },
            "customer": {
                "customer_id": "24",
                "customer_name": "Musterkunde AG\nMr. John Doe"
            },
            "status": "pending"
        },
        {
            "invoice_id": "13",
            "invoice_number": "RE-1001",
            "invoice_date": "2024-03-01T00:00:00.000Z",
            "amount": 19.99,
            "currency": "€",
            "vendor": {
                "vendor_id": "14",
                "vendor_name": "belegFuchs"
            },
            "customer": {
                "customer_id": "14",
                "customer_name": "Muster GmbH"
            },
            "status": "pending"
        },
        {
            "invoice_id": "14",
            "invoice_number": "DE-001",
            "invoice_date": "2024-01-01T00:00:00.000Z",
            "amount": 618.8,
            "currency": "€",
            "vendor": {
                "vendor_id": "15",
                "vendor_name": "Auto Teile Europa GmbH"
            },
            "customer": {
                "customer_id": "15",
                "customer_name": "Stefanie Johan Schmidt"
            },
            "status": "overdue"
        },
        {
            "invoice_id": "16",
            "invoice_number": "DE/01/12/2023",
            "invoice_date": "2023-12-15T00:00:00.000Z",
            "amount": 541.45,
            "currency": "€",
            "vendor": {
                "vendor_id": "17",
                "vendor_name": "Taxon GmbH"
            },
            "customer": {
                "customer_id": "17",
                "customer_name": "Klaus Kirsten GmbH"
            },
            "status": "overdue"
        },
        {
            "invoice_id": "21",
            "invoice_number": "012345",
            "invoice_date": "2020-05-27T00:00:00.000Z",
            "amount": 4645,
            "currency": "EUR",
            "vendor": {
                "vendor_id": "22",
                "vendor_name": "ABC Seller"
            },
            "customer": {
                "customer_id": "22",
                "customer_name": "XYZ Buyer\nABC Company"
            },
            "status": "overdue"
        },
        {
            "invoice_id": "15",
            "invoice_number": "1234",
            "invoice_date": "2020-01-01T00:00:00.000Z",
            "amount": 3653.3,
            "currency": "€",
            "vendor": {
                "vendor_id": "16",
                "vendor_name": "pixa"
            },
            "customer": {
                "customer_id": "16",
                "customer_name": "Max Müller"
            },
            "status": "overdue"
        },
        {
            "invoice_id": "19",
            "invoice_number": "2015-1234",
            "invoice_date": "2015-08-07T00:00:00.000Z",
            "amount": 1190,
            "currency": "€",
            "vendor": {
                "vendor_id": "20",
                "vendor_name": "Firmenname"
            },
            "customer": {
                "customer_id": "20",
                "customer_name": "Herrn Max Mustermann"
            },
            "status": "overdue"
        },
        {
            "invoice_id": "18",
            "invoice_number": "M1675",
            "invoice_date": "2014-05-28T00:00:00.000Z",
            "amount": 312.96,
            "currency": "€",
            "vendor": {
                "vendor_id": "19",
                "vendor_name": "Muster GmbH"
            },
            "customer": {
                "customer_id": "19",
                "customer_name": "Habermann & Söhne"
            },
            "status": "overdue"
        }
    ]
}



GET /api/vendors/top10

Returns top 10 vendors by total spend.

Example Response:





GET /api/category-spend

Returns spend grouped by category.

Example Response




GET /api/cash-outflow

Returns upcoming payment outflow forecast.

Example Response



GET /api/invoices

Returns searchable list of invoices with metadata.

Example Response





POST /api/chat-with-data

Forwards natural language query to Vanna AI,
which generates SQL, executes it on PostgreSQL, and returns results.

Example Request

POST /api/chat-with-data
Content-Type: application/json

{
  "question": "List top 5 vendors by spend"
}

Example Successful Response

{
    "sql": "SELECT \n    v.vendor_name, \n    SUM(il.total_price) AS total_spend\nFROM \n    vendors v\nJOIN \n    invoices i ON v.vendor_id = i.vendor_id\nJOIN \n    invoice_line_items il ON i.invoice_id = il.invoice_id\nGROUP BY \n    v.vendor_name\nORDER BY \n    total_spend DESC\nLIMIT 5;",
    "data": [
        {
            "vendor_name": "TechNova Solutions",
            "total_spend": 142500
        },
        {
            "vendor_name": "NextGen Pvt Ltd",
            "total_spend": 20000
        },
        {
            "vendor_name": "ABC Seller",
            "total_spend": 4357.6
        },
        {
            "vendor_name": "EasyFirma GmbH & Co KG",
            "total_spend": 3159.25
        },
        {
            "vendor_name": "pixa",
            "total_spend": 3070
        }
    ]
}



💬 Chat-with-Data Workflow

Frontend (Next.js) — user types a natural-language question

API Route (/api/chat-with-data) — forwards query to Vanna AI service

Vanna AI — uses LLM to generate an SQL query

PostgreSQL (NeonDB) — executes SQL to fetch real data

Dashboard — displays:

Generated SQL

Result table

Auto-rendered chart if applicable

Example flow:

User → Frontend → /api/chat-with-data → Vanna AI → PostgreSQL → JSON → UI (SQL + Chart)

Q: List top 5 vendors by spend
Generated SQL
SELECT 
    v.vendor_name, 
    SUM(il.total_price) AS total_spend
FROM 
    vendors v
JOIN 
    invoices i ON v.vendor_id = i.vendor_id
JOIN 
    invoice_line_items il ON i.invoice_id = il.invoice_id
GROUP BY 
    v.vendor_name
ORDER BY 
    total_spend DESC
LIMIT 5;
vendor_name	total_spend
TechNova Solutions	142500
NextGen Pvt Ltd	20000
ABC Seller	4357.6
EasyFirma GmbH & Co KG	3159.25
pixa	3070