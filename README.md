# Expedia & Hotels Review Scraper
## What is Expedia & Hotels Review Scraper? 

With the help of the web scraper, you can extract reviews for different types of accomodation listed on Expedia.com and Hotels.com. Select any specific accomodation on either of portals, copy its URL, paste it on Apify Console, and enjoy a full report on all the reviews for the chosed accomodation.

Apify Console uses API to make a request to Expedia and Hotels portals databases and to extract information based on your criteria. 

## Why might you need the Expedia & Hotels Review Scraper? 

* 🏨 **Reputation analysis before booking**: Quickly gather real guest reviews to make an informed decision.
* 📈 **Competitive analysis for accomodation owners**: Collect customers' preferences to identify weaknesses, and improve service.
* 📝 **Industry insights for businesses and bloggers**: Analyze travel trends and create engaging content.
* 🌴 **Enhancing customer service and marketing**: Use review data to optimize advertising.

## What data can you receive via the Expedia & Hotels Review Scraper?

|Review text|Accomodation name|
|Review date|Accomodation rate|
|Reviewer's name|Accomodation host's response|
|Duration and purpose of stay|Reviewer's country of origin|

## Is the Expedia & Hotels Review Scraper free to use?

This Actor is [**paid per result**](https://docs.apify.com/platform/actors/running/actors-in-store#pay-per-result): it charges $1.00 for each 1,000 items in the output. You don't pay anything for using Apify Console.

## How to use the Expedia & Hotels Review Scraper?

Apify Console is a perfect tool to use web scrapes as you don't need to go deep to technical details to received needed data. To start using the web scraper, do the following:

1. [Create an account](https://console.apify.com/sign-up) in Apify Console. 
2. Open the [Expedia & Hotels Review Scraper Actor](https://apify.com/tri_angle/expedia-hotels-com-reviews-scraper) [^firstnote].
3. In the **Expedia or Hotels.com URLs** section, add as many accomodation URLs, as you want to get reviews for. 
4. Click **Save & Start** [^secondnote]. The Actor starts collecting information.
5. Wait until the run gets the **Successfull** status, and open the **Output** tab to see the results.

### Input

You can either paste the accomodation URL and set up search criteria in settings, or use the JSON request. 

```
{
    "maxReviewsPerHotel": 3,
    "sortBy": "Most recent",
    "startUrls": [
        {
            "url": "https://euro.expedia.net/Prague-Hotels-Andaz-Prague.h71468304.Hotel-Information",
            "method": "GET",
            "userData": {
                "hotel": "ANDAZ PRAGUE, BY HYATT",
                "doWeEndorseIt": "no opinion"
            }
        }
    ]
}
```
In this example, you request for 3 reviews for the Andaz Hotel in Prague starting from the most recent ones. 

As an advanced setting, you can include `userData` to your API request that will be shown in the output as `customData`. You may use this data to easily identify reviews according to accomodation.

### Output

Output is available as a raw JSON or aggregated data shown in a table. Here you see one of three reviews for the Andaz Hotel in the JSON format. [^thirdnote]

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

## FAQ

### My run works slowly or craches often. How can I make it work?

Before running the Actor the next time, try to leverage resources such as memory. [Read more](https://docs.apify.com/platform/actors/running/usage-and-resources) about usage and resources.

### Is it legal to scrape accomodation reviews data?

Our [travel domain scrapers](https://apify.com/store/categories/travel) are ethical and do not extract any private user data that users chose not to show publicly. In the result, you still can see such information as users' location or email as long as they allowed the data to be shown on Expedia or Hotels portals. 

Do not scrape personal data unless you have a legitimate reason for it. If you're unsure whether your reason is leitimate, we recommend you to consult lawyers. Read our blog post on [the legality of web scraping](https://blog.apify.com/is-web-scraping-legal/) and [ethical scrapting](https://blog.apify.com/what-is-ethical-web-scraping-and-how-do-you-do-it/) to learn more.

### 

## Scrapers you might also like

| [Booking Reviews Scraper](https://apify.com/voyager/booking-reviews-scraper) | [Tripadvisor Reviews Scraper](https://apify.com/maxcopell/tripadvisor-reviews) |
| [Booking Scraper](https://apify.com/voyager/booking-scraper) | [Airbnb Scraper](https://apify.com/tri_angle/airbnb-scraper) |
| [Skyscanner Flight✈️](https://apify.com/jupri/skyscanner-flight) | [Ryanair Scraper](https://apify.com/epctex/ryanair-scraper) |
| [Google Maps Extractor](https://apify.com/compass/google-maps-extractor) | [Yelp Scraper](https://apify.com/tri_angle/yelp-scraper) |

## Do you want to build your own scraper?

Are you missing data that you want to receive? You can always build your own scraper and customize it in any way you want! We have various [scraper templates](https://apify.com/templates) in Python, JavaScript, and TypeScript. Alternatively, you can write a scraper from scratch using the [Crawlee open-source library](https://crawlee.dev/?__hstc=160404322.714e024ea435b45bf9bb4b97d451f918.1740165708053.1741394980816.1741471921677.6&__hssc=160404322.1.1741471921677&__hsfp=2141725003&_gl=1*qmwqwp*_gcl_au*NjA3NjA4OTEwLjE3NDAxNjU3MDY.*_ga*ODIwNzM3OTg5LjE3NDAxNjU3MDc.*_ga_62P18XN9NS*MTc0MTU0OTQ4MC45LjEuMTc0MTU1MTIwMy4zMi4xLjE3MjIxMTcxMjc.). Keeping it private or publish in Apify Store is completely up to you. If you would like us to make a custom solution for you, don't hesitate to [reach out to us](https://apify.com/contact). 

## Do you need help?

We're constantly improving the performance of our Actors. If you have any technical feedback or face a bug or malfunction in the Actor's work, feel free to report it by creating a new issue [on the **Issues** tab in Apify Console](https://console.apify.com/actors/4zyibEJ79jE7VXIpA/issues).

[^firstnote]: The web scraper is currently named a bit differently, but I decided to stick to my version all over the README. 
[^secondnote]: Once a user changes anything in the URL fields, the button renames as **Save & Start**. When a user opens the actor for the first time, he definitely needs to insert his URLs, so it would be the correct name of the button in this procedure.
[^thirdnote]: I would include a screenshot of the table with the results, but it doesn't look quite attractive due to the absense of the data in some columns. It would also be good if I could define which columns to show in the table (I know it is possible for export and preview mode, but seems not in the showing mode).


