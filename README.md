### 🧠 Pie Scanner API

Analyze any website and get AI-powered insights into problems, solutions, and more — via a single GET call.

---

### 🔗 Endpoint

```
GET https://api.piesolutions.ai/api/scan
```

---

### 🧾 Query Parameters

| Parameter | Required | Description                                                  |
| --------- | -------- | ------------------------------------------------------------ |
| `website` | ✅ Yes    | Full URL of the website to scan (must start with `https://`) |
| `prompt`  | ✅ Yes    | Custom prompt to guide the AI analysis (must be URL-encoded) |

---

### 📥 Example Request

No Prompt Curl
```bash
curl "https://api.piesolutions.ai/api/scan?website=https://piesolutions.ai"
```
Prompted curl
```bash
curl "https://api.piesolutions.ai/api/scan?website=https://piesolutions.ai&prompt=What%20do%20they%20do%20?"
```

---

### ✅ Example Prompt Ideas

* `Search the website, social media and reviews to find the top 3 problems.`
* `What does this business do? Summarize it in 1 sentence.`
* `Does this site have any backlinks?`

---

### 📦 Example JSON Response

```json
{
  "result": {
    "0": {
      "problem": "Unclear value proposition on homepage.",
      "solution": "Add a concise headline explaining the product and who it helps."
    },
    "1": {
      "problem": "No visible call-to-action above the fold.",
      "solution": "Add a prominent 'Get Started' or 'Contact Us' button in the header."
    }
    // ...
  }
}
```
