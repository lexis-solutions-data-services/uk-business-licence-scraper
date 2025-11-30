# UK Business Licence Scraper

![UK Business Licence Scraper](https://i.ibb.co/1FJh9zC/gov-uk-cover.png)

This Apify actor allows you to scrape business licence and regulatory information from **GOV.UK Find Licences**, the UK government's official directory of business licences, permits, and registrations. Extract comprehensive licence data including titles, descriptions, requirements, and application processes — perfect for compliance research, business planning, and regulatory intelligence.

<p align="center">
  <img src="https://apify-image-uploads-prod.s3.us-east-1.amazonaws.com/DevbkY3adMTBuoECt-actor-0cyIT5hmZHlhkAWmb-UaRaNqaYt6-Screenshot_2025-11-06_at_9.14.51.png" alt="UK Business Licence Scraper" style="height: 60px; margin-right: 15px;" /><a href="https://apify.com/lexis-solutions/uk-business-licence-scraper" target="_blank">
    <img src="https://img.shields.io/badge/Try%20it%20on-Apify-0066FF?style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iNDA4IiBoZWlnaHQ9IjQwOCIgdmlld0JveD0iMCAwIDQwOCA0MDgiIGZpbGw9Im5vbmUiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+CjxnIGNsaXAtcGF0aD0idXJsKCNjbGlwMF8zNDFfNDE1NykiPgo8cGF0aCBkPSJNMjE4LjY5NSAxMDRIMzAwLjk3QzMwMi42NDMgMTA0IDMwNCAxMDUuMzU3IDMwNCAxMDcuMDNWMjMyLjc2NkMzMDQgMjM1Ljc3OCAzMDAuMDgzIDIzNi45NDUgMjk4LjQzNCAyMzQuNDI1TDIxNi4xNTkgMTA4LjY5QzIxNC44NDEgMTA2LjY3NCAyMTYuMjg3IDEwNCAyMTguNjk1IDEwNFoiIGZpbGw9IndoaXRlIi8+CjxwYXRoIGQ9Ik0xODkuMzA1IDEwNEgxMDcuMDNDMTA1LjM1NyAxMDQgMTA0IDEwNS4zNTcgMTA0IDEwNy4wM1YyMzIuNzY2QzEwNCAyMzUuNzc4IDEwNy45MTcgMjM2Ljk0NSAxMDkuNTY2IDIzNC40MjVMMTkxLjg0IDEwOC42OUMxOTMuMTU5IDEwNi42NzQgMTkxLjcxMyAxMDQgMTg5LjMwNSAxMDRaIiBmaWxsPSJ3aGl0ZSIvPgo8cGF0aCBkPSJNMjAyLjU5MSAyMDQuNjY4TDEwOS4xMjcgMjk4LjgzNUMxMDcuMjI5IDMwMC43NDcgMTA4LjU4MyAzMDQgMTExLjI3OCAzMDRIMjk2LjhDMjk5LjQ4MyAzMDQgMzAwLjg0MiAzMDAuNzcgMjk4Ljk2NyAyOTguODUyTDIwNi45MDggMjA0LjY4NUMyMDUuNzI2IDIwMy40NzUgMjAzLjc4MiAyMDMuNDY4IDIwMi41OTEgMjA0LjY2OFoiIGZpbGw9IndoaXRlIi8+CjwvZz4KPGRlZnM+CjxjbGlwUGF0aCBpZD0iY2xpcDBfMzQxXzQxNTciPgo8cmVjdCB3aWR0aD0iMjAwIiBoZWlnaHQ9IjIwMCIgZmlsbD0id2hpdGUiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDEwNCAxMDQpIi8+CjwvY2xpcFBhdGg+CjwvZGVmcz4KPC9zdmc+Cg==&logoColor=white" alt="Try it on Apify" style="border-radius: 12px; height: 60px;" />
  </a>
</p>


---


## 📊 Actor Stats

| Stat | Value |
|------|-------|
| **Version** | `0.1.1` |
| **Last Update** | Nov 30, 2025 |

---


## 🚀 Key Features

- 🔎 Scrape business licence listings from **GOV.UK Find Licences**
- 📋 Extract detailed licence information (title, description, overview HTML)
- 🏢 Comprehensive regulatory and compliance data
- 📄 Structured data extraction
- 🔗 Related links including contact info and application URLs
- 🌐 Automatic pagination handling

---

## ❓ Why Use This Actor

- ✅ Automate licence and permit research for UK businesses
- ✅ Save hours of manual browsing through government websites
- ✅ Build comprehensive compliance databases
- ✅ Monitor regulatory changes and new licence requirements
- ✅ Support business planning and legal research
- ✅ Integrate licence data into business intelligence systems

---

## 👥 Who Is This Actor Suitable For?

- 🏢 Business consultants and advisors
- 📊 Compliance and regulatory professionals
- 🧠 Legal researchers and solicitors
- 🧰 Startup founders planning new ventures
- 📚 Business analysts and researchers
- 💼 Corporate compliance teams

---

## 📥 Input Schema

The actor accepts the following input parameters:

```json
{
  "startUrls": [
    {
      "url": "https://www.gov.uk/find-licences"
    },
    {
      "url": "https://www.gov.uk/find-licences?keywords=sell&licence_transaction_location%5B%5D=england&licence_transaction_industry%5B%5D=advertising-and-marketing"
    },
    {
      "url": "https://www.gov.uk/find-licences/solicitor-s-practising-certificate-scotland"
    }
  ],
  "maxItems": 20,
  "proxyConfiguration": {
    "useApifyProxy": false
  }
}
```

### Input Parameters

- **startUrls** (optional): Array of URLs to start scraping from. Defaults to the main licences page
- **maxItems** (optional): Maximum number of licence results to extract (default: 20)
- **proxyConfiguration** (optional): Proxy settings for anonymous scraping

### Example Start URLs

You can provide different types of URLs to scrape specific licence information:

**1. Main listing page** (scrapes all 453+ licences):

```
https://www.gov.uk/find-licences
```

**2. Filtered search results** (scrapes licences matching specific criteria):

```
https://www.gov.uk/find-licences?keywords=sell&licence_transaction_location%5B%5D=england&licence_transaction_industry%5B%5D=advertising-and-marketing
```

**3. Direct licence detail pages** (scrapes a specific licence):

```
https://www.gov.uk/find-licences/solicitor-s-practising-certificate-scotland
```

You can mix and match different URL types in the `startUrls` array to scrape exactly what you need.

---

## 📤 Output Schema

Each scraped business licence returns the following structured data:

```json
{
  "title": "Solicitor's practising certificate (Northern Ireland)",
  "url": "https://www.gov.uk/find-licences/solicitor-s-practising-certificate-northern-ireland",
  "description": "You need a practicing certificate to practise as a solicitor in Northern Ireland",
  "links": [
    {
      "text": "Contact your local council",
      "url": "https://www.gov.uk/find-local-council"
    },
    {
      "text": "Law Society of Northern Ireland",
      "url": "http://www.lawsoc-ni.org/"
    }
  ],
  "overviewHtml": "<p>If you intend to practise as a solicitor in Northern Ireland, you must:</p>\n\n<ul>\n  <li>have been admitted as a solicitor (eg completed your training)</li>\n  <li>have your name on the roll (a list of all solicitors of the Court of Judicature in Northern Ireland)</li>\n  <li>hold a practising certificate</li>\n</ul>\n\n<p>Practising certificates are issued by the <a rel=\"external\" href=\"http://www.lawsoc-ni.org/\" title=\"Law Society of Northern Ireland\">Law Society of Northern Ireland</a></p>\n\n<p>and you should contact them for an application form.</p>\n\n<p>You must pay a fee in connection with your practising certificate.</p>\n\n<h2 id=\"conditions\">Conditions</h2>\n\n<p>Conditions may be attached to a practising certificate under certain circumstances (eg where you have been the subject of disciplinary sanctions).</p>\n\n<p>You must renew your registration every year that you intend to practise as a solicitor.</p>\n\n<p>As a solicitor you must comply with rules regarding:</p>\n\n<ul>\n  <li>professional practice, conduct and discipline</li>\n  <li>continuing professional development activities</li>\n  <li>accounts and trust accounts</li>\n  <li>interest on clients&#x2019; money</li>\n  <li>inspection of practice bank accounts</li>\n  <li>requests for accountants reports</li>\n  <li>professional indemnity</li>\n</ul>\n\n<p>If you are a European lawyer you can apply to <abbr title=\"Law Society of Northern Ireland\">LSNI</abbr> for initial registration as a registered European lawyer (<abbr title=\"registered European lawyer\">REL</abbr>) if you intend to practise as a lawyer in the UK.</p>\n\n<h2 id=\"fines-and-penalties\">Fines and penalties</h2>\n\n<div role=\"note\" aria-label=\"Warning\" class=\"application-notice help-notice\">\n<p>If you practise as a solicitor without obtaining a practising certificate or an REL without being registered, you may be fined and held in contempt of court.</p>\n</div>"
}
```

### Output Fields

- **title**: The name of the business licence or permit
- **url**: Direct link to the licence information page on GOV.UK
- **description**: Brief summary of what the licence is for and who needs it
- **links**: Array of related links including contact information and application URLs
  - `text`: Link description
  - `url`: Link URL
- **overviewHtml**: Detailed HTML content about the licence including:
  - Requirements and eligibility criteria
  - Application process and steps
  - Conditions and compliance rules
  - Contact details for relevant authorities
  - Fees, penalties, and legal information

---

## Need to scrape more from GOV.UK?

Looking for job listings data from the UK government? Check out our other GOV.UK scraper:

🇬🇧 **[FindAJob DWP Gov UK Scraper](https://apify.com/lexis-solutions/findajob-dwp-gov-uk-scraper)** - Extract job listings from the UK government's official employment portal including titles, companies, locations, salaries, and posting dates. Ideal for job aggregation, labor market research, and recruitment intelligence.

---

👀 p.s.

Got feedback or need an extension?

Lexis Solutions is a [certified Apify Partner](https://apify.com/partners/find). We can help you with custom solutions or data extraction projects.

Contact us over [Email](mailto:scraping@lexis.solutions) or [LinkedIn](https://www.linkedin.com/company/lexis-solutions)

## Support Our Work 💝

If you're happy with our work and scrapers, you're welcome to leave us a company review [here](https://apify.com/partners/find/lexis-solutions/review) and leave a review for the scrapers you're subscribed to. It will take you less than a minute but it will mean a lot to us!
