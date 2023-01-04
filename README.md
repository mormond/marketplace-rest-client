# marketplace-rest-client

Use with VSCode and the excellent REST Client extension to access Microsoft commercial marketplace APIs.

1. You will need
    * An Azure subscription
    * A Partner Center account
    * Signed up for the commercial marketplace in Partner Center
    * Relevant permissions to publish (eg Developer)
1. Create an app registration in AAD (Azure Active Directory)
1. Create a SaaS offer in Partner Center
   * Register the app from the previous step to authorise access to marketplace APIs
   * Publish the offer to "preview" stage so you can "purchase" it
   * Make sure to set the price to $0
   * Make sure to set the right preview audience
1. Generate a marketplace token to call resolve
   * Make a "purchase" of your offer 
   * The token is passed as a query string parameter to the landing page
   * The landing page is registered as part of creating the SaaS offer
   * You will need to URL decode the token before use
1. Install the REST Client extension in VS Code
1. Set variables to authorize and decode a marketplace token, get subscriptions etc
    * `client_id`
    * `tenant_id`
    * `client_secret`
    * `marketplace_token`
> Note these are sensitive values and must be treated with care    

7. Use
   1. `subscription-apis.http` for subscription APIs    
   1. `operations-apis.http` for operations APIs
