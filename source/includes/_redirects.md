# Booking Redirects

In addition to price information, your users will need a url that redirects them to where they can book their ticket. 

You can redirect your users directly to the supplier's website (airline or travel agent)

> Example deeplink

```json
"PricingOptions": [
        {
          "Agents": [
            4499211
          ],
          "QuoteAgeInMinutes": 0,
          "Price": 83.41,
          "DeeplinkUrl": "http://partners.api.skyscanner.net/apiservices/deeplink/v2?_cje=jzj5DawL5zJyT%2bnfe1..."
        },
      
```

When using [flights live prices](#flights-live-prices) or [car hire live prices](#car-hire-live-prices) urls (or deeplinks) are provided in the response to redirect users to the third-party supplier's website with the details of the itinerary that was selected. 

![deeplink page](/images/deeplink.png)

You can customise the redirect page by replacing the default logo with your own logo. Please see [How can I put my logo on the redirect page?](https://support.business.skyscanner.net/hc/en-us/articles/208180985-How-can-I-put-my-logo-on-the-redirect-page-) for more information.

See how it looks with your logo

<form action="redirect_page.html" method="GET" style="margin: 0 30px">
  <input type="text" name="logo_url" value="logo url"/>
  <input type="submit" value="test"/>
</form>

<aside class="notice">
Skyscanner has no control over the third-party website. In some cases the selected itinerary will be ready to book. In other cases the search criteria will be pre-populated but the end-user will have to search through the results to find their itinerary.
</aside>

<aside class="warning">
Please <b>do not cache the deeplinks</b> as they are only valid while your session is active. Once the session has timed out you will need to create a new session and refresh all the results and deeplink urls. 
</aside>  