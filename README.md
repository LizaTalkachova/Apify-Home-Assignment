# Expedia & Hotels Review Scraper
## 🗒️ What is Expedia & Hotels Review Scraper? 

With the help of the web scraper, you can extract reviews for different types of accommodation listed on **Expedia.com** and **Hotels.com**. Select any specific accommodation on either of portals, copy its URL, paste it on Apify Console, and enjoy a full report on all the reviews for the chosen accommodation.

Apify Console uses **API** to make a request to Expedia and Hotels portals databases and to extract information based on your criteria. 

## 📊 Why might you need the Expedia & Hotels Review Scraper? 

* 🏨 **Reputation analysis before booking**: Quickly gather real guest reviews to make an informed decision.
* 📈 **Competitive analysis for accommodation owners**: Collect customers' preferences to identify weaknesses, and improve service.
* 📝 **Industry insights for businesses and bloggers**: Analyze travel trends and create engaging content.
* 🌴 **Enhancing customer service and marketing**: Use review data to optimize advertising.

## ℹ️ What data can you receive via the Expedia & Hotels Review Scraper? [^notefirst]

|           |                 |
|-----------|-----------------|
|Review text|Accommodation name|
|Review date|Accommodation rate|
|Reviewer's name|Accommodation host's response|
|Duration and purpose of stay|Reviewer's country of origin| 

## 💸 Is the Expedia & Hotels Review Scraper free to use?

This Actor is [**paid per result**](https://docs.apify.com/platform/actors/running/actors-in-store#pay-per-result): it charges $1.00 for each 1,000 items in the output. You don't pay anything for using Apify Console. You can watch your expenses [in the **Billing** section](https://console.apify.com/billing/current-period).

## ⏯️ How to use the Expedia & Hotels Review Scraper?

Apify Console is a perfect tool to use web scrapes as you don't need to go deep into technical details to receive needed data. To start using the web scraper, do the following:

1. [Create an account](https://console.apify.com/sign-up) in Apify Console. 
2. Open the [Expedia & Hotels Review Scraper Actor](https://apify.com/tri_angle/expedia-hotels-com-reviews-scraper) [^notesecond].
3. In the **Expedia or Hotels.com URLs** section, add as many accommodation URLs, as you want to get reviews for. 
4. Click **Save & Start** [^notethird]. The Actor starts collecting information.
5. Wait until the run gets the **Successful** status, and open the **Output** tab to see the results.

### Input

You can either paste the accommodation URL and set up search criteria in settings, or use the JSON request. [^notefourth] [^notefifth]

```
{
    "maxReviewsPerHotel": 3, //The number of records you will receive per hotel
    "sortBy": "Most recent", //The sort order
    "startUrls": [
        {
            "url": "https://euro.expedia.net/Prague-Hotels-Andaz-Prague.h71468304.Hotel-Information", //The accommodation URL
            "method": "GET", //The type of the endpoint
            "userData": {
                "hotel": "ANDAZ PRAGUE, BY HYATT", //The accommodation name
                "doWeEndorseIt": "no opinion" //User data you want to put into the request 
            }
        }
    ]
}
```
In this example, you request for 3 reviews for the Andaz Hotel in Prague starting from the most recent ones.
> [!NOTE]
> The sorting oder doesn't influence the records order in the output.

As an advanced setting, you can include `userData` to your API request that will be shown in the output as `customData`. You may use this data to easily identify reviews according to accommodation.

### Output

Output is available as a raw JSON or aggregated data shown in a table. Here you see one of three reviews for the Andaz Hotel in the JSON format. [^notesixth]

```
[
    {
        "contentDirectFeedbackPromptId": null,
        "id": "67bedb8d4570c67eb5cb94c2",
        "superlative": "Excellent",
        "locale": "de_CH",
        "title": "Great place for a luxurious weekend in Prague",
        "brandType": "",
        "disclaimer": null,
        "reviewScoreWithDescription": {
            "label": "10 out of 10 Excellent",
            "value": "10/10 Excellent",
            "__typename": "LodgingEnrichedMessage"
        },
        "text": "Excellent hotel, great location and very friendly staff",
        "highlightedText": null,
        "seeMoreAnalytics": {
            "linkName": "See more reviews",
            "referrerId": "HOT.HIS.See_more.",
            "__typename": "ClientSideAnalytics"
        },
        "submissionTime": {
            "longDateFormat": "Feb 26, 2025",
            "__typename": "DateTime"
        },
        "impressionAnalytics": null,
        "themes": [
            {
                "icon": {
                    "id": "sentiment_4",
                    "__typename": "Icon"
                },
                "label": "Liked: Cleanliness, staff & service, property conditions & facilities, room comfort",
                "__typename": "ReviewThemes"
            }
        ],
        "reviewFooter": {
            "messages": [
                {
                    "seoStructuredData": {
                        "itemscope": true,
                        "itemprop": "author",
                        "itemtype": "https://schema.org/Person",
                        "content": "Daniel",
                        "__typename": "SEOStructuredData"
                    },
                    "text": {
                        "text": "Stayed 3 nights in Dec 2024",
                        "__typename": "EGDSPlainText"
                    },
                    "__typename": "PropertyReviewFooterMessage"
                }
            ],
            "__typename": "PropertyReviewFooterSection"
        },
        "reviewAnalytics": "{\"metadata\":{\"packer_version\":\"1.0.1\"},\"events\":{\"review.presented\":{\"v1\":{\"event_data\":{\"event\":{\"event_name\":\"review.presented\",\"event_version\":\"1.0.0\",\"event_type\":\"Impression\",\"action_location\":\"reviews_overlay\"},\"additional_context\":{\"user_interface\":{\"component_id\":\"67bedb8d4570c67eb5cb94c2\",\"component_position\":1,\"component_name\":\"NEWEST_TO_OLDEST_BY_LANGUAGE.all\"}}}}}}}",
        "reviewInteractionSections": [
            {
                "primaryDisplayString": "0",
                "accessibilityLabel": "Mark review 1 as helpful. 0 other users found review 1 helpful.",
                "reviewInteractionType": "HELPFUL_REVIEW",
                "feedbackAnalytics": {
                    "linkName": "Helpful review",
                    "referrerId": "HOT.HIS.ReviewsOverlay.THUMB_UP.UPVOTE",
                    "__typename": "ClientSideAnalytics"
                },
                "__typename": "PropertyReviewInteraction"
            },
            {
                "primaryDisplayString": null,
                "accessibilityLabel": null,
                "reviewInteractionType": "REVIEW_REPORT_FLAG",
                "feedbackAnalytics": null,
                "__typename": "PropertyReviewInteraction"
            },
            {
                "primaryDisplayString": "See more",
                "accessibilityLabel": "See more from Daniel's review",
                "reviewInteractionType": "REVIEW_EXPAND_LABEL",
                "feedbackAnalytics": null,
                "__typename": "PropertyReviewInteraction"
            },
            {
                "primaryDisplayString": "See less",
                "accessibilityLabel": "See less from Daniel's review",
                "reviewInteractionType": "REVIEW_COLLAPSE_LABEL",
                "feedbackAnalytics": null,
                "__typename": "PropertyReviewInteraction"
            }
        ],
        "__typename": "PropertyReview",
        "reviewAuthorAttribution": {
            "text": "Daniel",
            "__typename": "LodgingHeader"
        },
        "photoSection": null,
        "photos": [],
        "travelers": [],
        "translationInfo": {
            "loadingTranslationText": "Loading translation...",
            "targetLocale": null,
            "translatedBy": {
                "description": "Translated by Google",
                "__typename": "Mark"
            },
            "translationCallToActionLabel": "Translate with Google",
            "seeOriginalText": "See original",
            "__typename": "PropertyReviewTranslationInfo"
        },
        "propertyReviewSource": null,
        "reviewRegion": null,
        "managementResponses": [],
        "hotelId": "71468304",
        "reviewPosition": 1,
        "customData": {
            "hotel": "Hotel Quirinale",
            "doWeEndorseIt": "no opinion"
        }
    }
]
```
You can export the output in many formats:
* JSON
* CSV
* XML
* Excel
* HTML Table
* RSS
* JSONL

You can select specific data to export, set a limit of records, set a number of records to skip, or unwind specific data in case if it is an array or an object. 

### Limitations

You can set a limit for the number of records per run. It is useful if you want to control your budget for the specific actor as you won't be charged for records that exceed the limit. To do it, open the Expedia & Hotels Review Scraper > the **Input** tab. Open **Run options**, and set the maximum charged results.

## ❓ FAQ

### Can I schedule the Actor?

Yes, you can define how often the Actor will run. Read more about [a schedule](https://docs.apify.com/platform/schedules) in Apify Console.

### How long is the output data available in Apify Console?

We store records of the last 10 runs of *all* the actors until you delete them. The rest is stored for the number of days according to your pricing plan. You can always upgrade the plan [in your Apify Console account](https://console.apify.com/billing/limits). Read more about [storages](https://docs.apify.com/platform/storage/usage#data-retention) so you never lose the data.

### Is it legal to scrape accommodation reviews data?

Our [travel domain scrapers](https://apify.com/store/categories/travel) are ethical and do not extract any private user data that users chose not to show publicly. In the result, you still can see such information as users' location or email as long as they allowed the data to be shown on Expedia or Hotels portals. 

Do not scrape personal data unless you have a legitimate reason for it. If you're unsure whether your reason is legitimate, we recommend you to consult lawyers. Read our blog post on [the legality of web scraping](https://blog.apify.com/is-web-scraping-legal/) and [ethical scraping](https://blog.apify.com/what-is-ethical-web-scraping-and-how-do-you-do-it/) to learn more.

### Can I use Apify API to work with the Actor?

Yes, Apify has rich public API library of **RESTful** endpoints. 

To explore different API clients, click **API** > **API clients** on the [main Expedia & Hotels Review Scraper page](https://console.apify.com/actors/4zyibEJ79jE7VXIpA/input).

Refer to [Apify API documentation](https://docs.apify.com/api/v2) for the list of available endpoints.

### Can I integrate the actor with other tools?

We offer various tools which you can integrate the actor with: from native Apify tools to AI ecosystems or other popular tools, such as [Gmail](https://mail.google.com/), [Slack](https://slack.com/), [GitHub](https://github.com/), [Flowise](https://flowiseai.com/). You can find all the options [on the **Integrations** tab](https://console.apify.com/actors/4zyibEJ79jE7VXIpA/integrations) 

Integration tools like [Zapier](https://zapier.com/) or [Make](https://www.make.com/en) allow leveraging data you receive via web scrapers in the most efficient ways.

You also can add your custom webhook to receive data once the Actor performs an action. 

## 💡 Troubleshooting

### My run works slowly or crashes often. How can I make it work?

Before running the Actor the next time, try to leverage resources such as memory. You also can add a timeout.  [Read more](https://docs.apify.com/platform/actors/running/usage-and-resources) about usage and resources.

## 📓 Scrapers you might also like

|                                                                              |                                                                                |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Booking Reviews Scraper](https://apify.com/voyager/booking-reviews-scraper) | [Tripadvisor Reviews Scraper](https://apify.com/maxcopell/tripadvisor-reviews) |
| [Booking Scraper](https://apify.com/voyager/booking-scraper) | [Airbnb Scraper](https://apify.com/tri_angle/airbnb-scraper) |
| [Expedia Hotels 3.0a](https://apify.com/jupri/expedia-hotels) | [Hotel Review Aggregator](https://apify.com/tri_angle/hotel-review-aggregator) |
| [Google Maps Extractor](https://apify.com/compass/google-maps-extractor) | [Yelp Scraper](https://apify.com/tri_angle/yelp-scraper) | [^noteseventh]

## 🛠️ Do you want to build your own scraper?

Are you missing data that you want to receive? You can always build your own scraper and customize it in any way you want! We have various [scraper templates](https://apify.com/templates) in Python, JavaScript, and TypeScript. Alternatively, you can write a scraper from scratch using the [Crawlee open-source library](https://crawlee.dev/?__hstc=160404322.714e024ea435b45bf9bb4b97d451f918.1740165708053.1741394980816.1741471921677.6&__hssc=160404322.1.1741471921677&__hsfp=2141725003&_gl=1*qmwqwp*_gcl_au*NjA3NjA4OTEwLjE3NDAxNjU3MDY.*_ga*ODIwNzM3OTg5LjE3NDAxNjU3MDc.*_ga_62P18XN9NS*MTc0MTU0OTQ4MC45LjEuMTc0MTU1MTIwMy4zMi4xLjE3MjIxMTcxMjc.). Keeping it private or publishing it in the Apify Store is completely up to you. If you would like us to make a custom solution for you, don't hesitate to [reach out to us](https://apify.com/contact). 

## 🩹 Do you need help?

We're constantly improving the performance of our Actors. If you have any technical feedback or face a bug or malfunction in the Actor's work, feel free to report it by creating a new issue [on the **Issues** tab in Apify Console](https://console.apify.com/actors/4zyibEJ79jE7VXIpA/issues).

[^notefirst]: As far as I know, GitHub doesn't support tables without headers, so I had to leave it as it is (empty headers).
[^notesecond]: The web scraper is currently named a bit differently, but I decided to stick to my version all over the README. 
[^notethird]: Once a user changes anything in the URL fields, the button renames as **Save & Start**. When a user opens the actor for the first time, he definitely needs to insert his URLs, so it would be the correct name of the button in this procedure.
[^notefourth]: In the JSON code block, I left comments on each parameter to let users understand what the input means.
[^notefifth]: I'm not sure the doWeEndorseIt parameter stands for the user data, but I had to leave a comment for the sake of consistency.
[^notesixth]: I would include a screenshot of the table with the results, but it doesn't look quite attractive due to the absence of the data in some columns. It would also be good if I could define which columns to show in the table (I know it is possible for export and preview mode, but seems not in the showing mode).
[^noteseventh]: As far as I know, GitHub doesn't support tables without headers, so I had to leave it as it is (empty headers).
