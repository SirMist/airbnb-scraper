[Airbnb Scraper](https://apify.com/nexgendata/airbnb-scraper?fpr=data)

## What does Airbnb Scraper do?

Airbnb Scraper extracts rental listings from Airbnb including prices, ratings, amenities, host information, and availability for any location or search criteria.

## Why use Airbnb Scraper?

Short-term rental data is valuable for pricing optimization, market research, and competitive analysis. This scraper delivers structured Airbnb listing data automatically.

## Use cases

- **Pricing Optimization**: Research competitor pricing in your rental market
- **Investment Analysis**: Evaluate short-term rental revenue potential for properties
- **Market Research**: Analyze supply, demand, and pricing trends across markets
- **Hospitality Intelligence**: Monitor competitive landscape and new listings
- **Travel Planning**: Compare listings and prices programmatically

## Input parameters

| Parameter | Type | Description |
| --- | --- | --- |
| `location` | String | City or area to search |
| `checkIn` | String | Check-in date (YYYY-MM-DD) |
| `checkOut` | String | Check-out date (YYYY-MM-DD) |
| `maxResults` | Number | Maximum results (default: 20) |

## Output example

```
{
    "title": "Cozy Studio in Manhattan",
    "price": 125,
    "rating": 4.8,
    "reviewCount": 342,
    "propertyType": "Entire apartment",
    "bedrooms": 1,
    "bathrooms": 1,
    "amenities": ["WiFi", "Kitchen", "AC"],
    "superhost": true
}
```

## Pricing

Pay-Per-Event pricing: $3.00 per 1,000 results. Platform fee: $0.005 per start.

---

 

## 💻 Code Example — Python

```
from apify_client import ApifyClient

client = ApifyClient("YOUR_APIFY_TOKEN")
run = client.actor("nexgendata/airbnb-scraper").call(run_input={
    # Fill in the input shape from the actor's input_schema
})

for item in client.dataset(run["defaultDatasetId"]).iterate_items():
    print(item)
```

## 🌐 Code Example — cURL

```
curl -X POST "https://api.apify.com/v2/acts/nexgendata~airbnb-scraper/run-sync-get-dataset-items?token=YOUR_TOKEN" \
  -H "Content-Type: application/json" \
  -d '{ /* input schema */ }'
```

## ❓ FAQ

**Q: How do I get started?**
Sign up at [apify.com](https://www.apify.com/?fpr=2ayu9b), grab your API token from Settings → Integrations, and run the actor via the Apify console, API, Python SDK, or any integration (Zapier, Make.com, n8n).

**Q: What's the typical cost per run?**
See the pricing section below. Most runs finish under $0.10 for typical batches.

**Q: Is this actor maintained?**
Yes. NexGenData maintains 165+ Apify actors and ships updates regularly. Bug reports via the Apify console issues tab get responses within 24 hours.

**Q: Can I use the output commercially?**
Yes — you own the output data. Check the target site's Terms of Service for any usage restrictions on the scraped content itself.

**Q: How do I handle rate limits?**
Apify manages concurrency and retries automatically. For very large batches (10K+ items), run multiple smaller jobs in parallel instead of one mega-job for better reliability.

## 💰 Pricing

Pay-per-event pricing — you only pay for what you actually extract.

- **Actor Start:** $0.0050
- **result:** $0.0250

## 🔗 Related NexGenData Actors

- [TripAdvisor Scraper](https://apify.com/nexgendata/tripadvisor-scraper?fpr=2ayu9b)
- [Google Maps Lead Scraper](https://apify.com/nexgendata/google-maps-scraper?fpr=2ayu9b)

## 🚀 Apify Affiliate Program

New to Apify? Sign up with our [referral link](https://www.apify.com/?fpr=2ayu9b) — you get free platform credits on signup, and you help fund the maintenance of this actor fleet.

## 📚 More From NexGenData

Explore the full catalog, tutorials, Gumroad data packs, and newsletter at **[thenextgennexus.com](https://thenextgennexus.com)** — the brand home for everything we ship.

- 📖 Tutorials & how-to guides
- 🗂️ Full actor catalog with usage examples
- 📦 Gumroad data packs (one-time purchases)
- 📬 Newsletter — monthly drops of new actors and revenue experiments

---

*Built and maintained by [NexGenData](https://apify.com/nexgendata?fpr=2ayu9b) — 165+ actors covering scraping, enrichment, MCP servers, and automation.*
🏠 Home: [thenextgennexus.com](https://thenextgennexus.com)