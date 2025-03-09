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

[^firstnote]: The web scraper is currently named a bit differently, but I decided to stick to my version all over the README. 
[^secondnote]: Once a user changes anything in the URL fields, the button renames as **Save & Start**. When a user opens the actor for the first time, he definitely needs to insert his URLs, so it would be the correct name of the button in this procedure.
[^thirdnote]: I would include a screenshot of the table with the results, but it doesn't look quite attractive due to the absense of the data in some columns. It would also be good if I could define which columns to show in the table (I know it is possible for export and preview mode, but seems not in the showing mode).
