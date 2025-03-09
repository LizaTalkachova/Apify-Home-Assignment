# MyPersonal
## What is Expedia & Hotels Review Scraper? 

With the help of the web scraper, you can extract reviews for different types of accomodation listed on Expedia.com and Hotels.com. Select any specific accomodation on either of portals, copy its URL, paste it on Apify Console, and enjoy a full report on all the reviews for the chosed accomodation.

Apify Console uses API to make a request to Expedia and Hotels portals databases and to extract information based on your criteria. 

## Why might you need the Expedia & Hotels Review Scraper? 

🏨 **Reputation analysis before booking**: Quickly gather real guest reviews to make an informed decision.
📈 **Competitive analysis for accomodation owners**: Collect customers' preferences to identify weaknesses, and improve service.
📝 **Industry insights for businesses and bloggers**: Analyze travel trends and create engaging content.
🌴 **Enhancing customer service and marketing**: Use review data to optimize advertising.

## What data can you receive via the Expedia & Hotels Review Scraper?

| Review text | Accomodation name |
| Review date | Accomodation rate |
| Reviewer's name | Accomodation host's response |
| Duration and purpose of stay | Reviewer's country of origin |

## How to use the Expedia & Hotels Review Scraper?

Apify Console is a perfect tool to use web scrapes as you don't need to go deep to technical details to received needed data. To start using the web scraper, do the following:

1. [Create an account](https://console.apify.com/sign-up) in Apify Console. 
2. Open the [Expedia & Hotels Review Scraper](https://apify.com/tri_angle/expedia-hotels-com-reviews-scraper) actor [^firstnote].
3. In the **Expedia or Hotels.com URLs** section, add as many accomodation URLs, as you want to get reviews for. 
4. Click **Save & Start** [^secondnote]. The actor starts collecting information.
5. Wait until the run gets the **Successfull* status, and open the **Output** tab to see the results.

### Input

You can either paste the accomodation URL and set up search criteria in settings, or use the JSON request. 

```
{
    "maxReviewsPerHotel": 100,
    "sortBy": "Most recent",
    "startUrls": [
        {
            "url": "https://euro.expedia.net/Rome-Hotels-Hotel-Quirinale.h1058.Hotel-Information",
            "method": "GET",
            "userData": {
                "hotel": "Hotel Quirinale",
                "doWeEndorseIt": "no opinion"
            }
        }
    ]
}
```

[^firstnote]: The web scraper is currently named a bit differently, but I decided to stick to my version all over the README. 
[^secondnote]: Once a user changes anything in the URL fields, the button renames as **Save & Start**. When a user opens the actor for the first time, he definitely needs to insert his URLs, so it would be the correct name of the button in this procedure.
