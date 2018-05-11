/*
Title: Revenue and payment  
Sort: 90
*/

## Earning revenue
Unity Ads generates revenue by displaying paid advertisements in your game. The more traffic and [impressions](https://en.wikipedia.org/wiki/Impression_(online_media)) your game creates, the more money you can earn.
 
Unity Ads facilitates different campaign types with different billing points (for example, completed views, clicks, or installs), and always selects the highest-earning campaign to display to your users. 

### Monetization factors
The average [eCPM](https://en.wikipedia.org/wiki/Cost_per_mille) for Unity Ads depends on many factors, such as platform, region, player demographics, and in-game placements. The biggest factor is the number of players engaging in your game. The Ads monetization [**Best practices guide**](https://unityads.unity3d.com/help/monetization/best-practices) provides advice on maximizing revenue through strategic implementation.

### Analyzing revenue
You can view statistics on your Ads monetization on the [Ads Monetization Developer Dashboard](https://operate.dashboard.unity3d.com/). If your revenue displays as $0.00, you may need to be patient. Each time a video is started, it creates an impression. However, it may take around 5000 impressions for our targeting algorithms to determine the quality of users provided and start showing consistent revenue. 

For more information on using the Developer Dashboard to analyze revenue metrics, see documentation on [**Monetization statistics**](https://unityads.unity3d.com/help/monetization/statistics).

## Payment
Unity Ads now offers automated payouts for your revenue. During the transition period, you may still submit [invoices](#invoices). Both methods are detailed below. 

### Automated payouts
Eligible publishers can receive automated payouts for their Unity Ads earnings every month. This article provides a step-by-step guide to configuring automated payouts for your Organization. To get started, log in to the [Unity ID](https://id.unity.com) portal.

**Note**: Unity Ads currently only supports payouts in USD.

#### Payout profiles
In order to receive payment, you must configure a payout profile. Payout profiles are associated with Organizations. Each Organization has one profile per service, so you can only create one profile for your Unity Ads earnings.

**Note**: You must be the Organization’s **Owner** to see, create, or update its payout profile. For more information on Organizations and roles, see the **Members and Groups** section of the [**Managing your Organization**](https://docs.unity3d.com/2018.1/Documentation/Manual/OrgsManagingyourOrganization.html) documentation.

To navigate to the desired Organization’s payout profile interface:

1. Log in to the [Unity ID](https://id.unity.com) portal.
2. Select **Organizations** from the left navigation bar.
3. Select the desired Organization from the list (you can also view your role within the Organization from this list; verify that you are the Organization’s **Owner**).<br><br>
**Important**: Make sure you select the correct Organization, especially if you have Owner permissions for multiple Organizations. Failing to do so may result in not receiving payouts.<br><br>
4. Select **Payout Profile** from the left navigation bar sub-menu.

##### Creating a payout profile
From your Organization’s **Payout Profile** page, create a new profile by clicking **+ Add profile**. 

![Adding a payout profile on the Unity ID dashboard.](https://github.com/Applifier/unity-ads/wiki/monetization/PayoutProfile.png)
<p align="center"><i>Adding a payout profile on the Unity ID dashboard.</i></p>

##### SMS Two-Factor Authentication (TFA)
You must enable SMS-based [TFA](https://en.wikipedia.org/wiki/Multi-factor_authentication) in order to edit payout profiles. If you have yet to enable it for your Organization, the dashboard will prompt you to do so now. If you already set up SMS TFA authentication, skip to the [Profile information](#populating-profile-information) section below.

![Setting up SMS TFA on the Unity ID dashboard.](https://github.com/Applifier/unity-ads/wiki/monetization/TFA.png)
<p align="center"><i>Setting up SMS TFA on the Unity ID dashboard.</i></p>

1. Click **Activate TFA** > **Start setup** to begin. 
2. Confirm your Unity Developer Network (UDN) password, then click **Next**.
3. Enter a valid phone number that can receive SMS messages, then click **Next**.
4. The specified phone number will receive a 6-digit code via SMS. Enter the code on the dashboard within 60 seconds to initialize TFA.

Once you complete this step, return to the payout profile section of the dashboard (**Organizations** > select your Organization > **Payout Profile**), then select **+ Add profile**. Complete the TFA check to proceed.

##### Populating profile information
On the **Create Payout Profile** page, enter the following required information:

* **Country** and **Region**
* **Payment recipient** (**Company** or **Private individual**; note that you cannot change this after you create the profile!)
* (Companies only) **Company Name**
* (Companies only) **EU VAT** ([European Union Value Added Tax ID](https://en.wikipedia.org/wiki/European_Union_value_added_tax); this field is optional, however EU VAT-registered companies must provide an ID) 

**Note**: Finnish publishers must register as EU VAT companies. They also must be in the prepayment register ([ennakkoperintärekisteri](https://fi.wikipedia.org/wiki/Ennakkoperintärekisteri)) to receive payments.

* (Companies only) **Contact Person** and their corresponding **Email** address
* (Individuals only) **Full Name** and your corresponding **Email** address
* **Address**
* **Postal Code**
* **City**

Click **Create** to create your profile.

![Populating payout profile information on the Unity ID dashboard.](https://github.com/Applifier/unity-ads/wiki/monetization/PayoutProfileInfo.png)
<p align="center"><i>Populating payout profile information on the Unity ID dashboard.</i></p>

Your profile information is now saved. You can edit it any time by clicking the **Edit** (pencil icon) button.

##### Adding a payout method
Unity supports Paypal and bank transfers (note that Unity only currently supports local transfers in the US). To add a payout method, navigate to the **Payout Method** section of the **Payout Profile** page, then click the **Edit** or **+ Add payout method** button. 

![Adding a new payout method on the Unity ID dashboard.](https://github.com/Applifier/unity-ads/wiki/monetization/PayoutMethod.png)
<p align="center"><i>Adding a new payout method on the Unity ID dashboard.</i></p>

On the **Add Payout Method** page, select an option from the **Payout Method** drop-down menu.

![Selecting a payment method for automated payouts.](https://github.com/Applifier/unity-ads/wiki/monetization/SelectPayoutMethod.png)
<p align="center"><i>Selecting a payment method for automated payouts.</i></p>

* Select **Hold my payments** to withhold payouts until further notice. When you update this field to one of the other two methods, Unity will pay out all accumulated revenue if it meets the specified [minimum payout amount](#minimum-payout-amount-and-fulfillment).  
* Select **Bank transfer** to set up direct deposits into a specified account (see section on **Bank transfers** below). 
* Select **Paypal** to receive payments directly to your Paypal account (see section on **Paypal** below).

##### Bank transfers
You must provide banking details for the account you want to receive payments. Select **Bank transfer** from the drop-down, then click the **Add bank transfer details** button. 

You will temporarily leave the dashboard to process banking information through our secure partner [Worldpay](https://www.worldpay.com/). 

![Rerouting to Worldpay secure payment processing.](https://github.com/Applifier/unity-ads/wiki/monetization/Worldpay.png)
<p align="center"><i>Rerouting to Worldpay secure payment processing.</i></p>

The country of your bank dictates the type of transfer (local or international) and type of information Worldpay requests. 

![Example banking information form for international transfers.](https://github.com/Applifier/unity-ads/wiki/monetization/WorldpayInfo.png)
<p align="center"><i>Example banking information form for international transfers.</i></p>

Once you’ve completed the Worldpay form, you will return to the **Add Payout Method** page. 

**Note**: Depending on your bank, you may incur transfer fees associated with payment processing intermediaries. 

##### PayPal
To set up PayPal deposits, all you need to provide is the minimum payout amount (see section below) and your registered PayPal email address.

##### Minimum payout amount and fulfilment
Set a minimum amount of accrued earnings for which to receive a payment. Unity processes payments at the end of each month on a net 60 cadence, which means that your outstanding balance is paid in full and received within 60 days of each payment period, so long as your earnings met or exceeded the minimum payout amount. 

For example, if your minimum payment amount is $100, and you earn $200 in the month of March, your total earnings for that period ($200) are paid by the end of May. 

In the same scenario, if you earn $50 in March, then $50 in April, the accumulated balance meets the minimum payment amount and is paid by the end of June.      

##### Finalizing your settings
When you’ve finished specifying your payment method and minimum amount, click the **Create** button to save your selections.

#### Validating tax information
Unity must collect your relevant tax information in order to withhold taxes when applicable, as required by tax authorities. To validate your tax information, navigate to the **Payout Tax info** section of the **Payout Profile** page, then click the **Create** button. 

![Adding your tax information on the Unity ID dashboard.](https://github.com/Applifier/unity-ads/wiki/monetization/TaxInfo.png)
<p align="center"><i>Adding your tax information on the Unity ID dashboard.</i></p>

You will temporarily leave the dashboard to complete the tax interview by providing the following information: 
 
* Basic information about yourself 
* Consent to receive information reporting documentation 
* Your overall tax status
* Your electronic signature and consent to use it

When finished, click **Exit interview** to return to the **Payout Profile** page. The **Payout Tax info** section takes a few minutes to update. When it does, the **Tax status** changes to **Validated**.

#### Making changes to your profile, payout method, or tax info 
You can edit your information at any time from the **Payout Profile** page:

* In the **Payout Profile** section, click the **Edit** button (note that you cannot change the recipient type).
* In the **Payout Method** section, click the **Edit** button.
* In the **Payout Tax** info section, click the **Update** button.

**Note**: Any changes might not affect payouts for the current month. If you need the changes to take effect immediately, please [contact Unity Ads support](mailto:unityads-support@unity3d.com).

#### Payout history
You can view records of your Unity Ads payouts at any time:

1. Log in to the [Unity ID](https://id.unity.com) portal.
2. Select **Organizations** from the left navigation bar.
3. Select the desired Organization from the list.
4. Select **Transaction History** from the left navigation bar sub-menu.
5. Select the **Payouts** tab.
6. Select the date range you wish to query, then click the **Apply** button to view a list of invoices.

### Invoices
To receive payment, please submit an invoice to _accountspayable-fi@unity3d.com_. The minimum earnings balance required to submit an invoice is $100 USD. 

1. Download [Payment Request Form](https://static.applifier.com/unityads/files/WireTransferForm-UnityAds.pdf) and enter your banking information, so that Unity may direct payment to the correct account (Note that you only need to complete this step when submitting for the first time, or if your banking information has changed).
2. Download and complete the [Invoice Template](https://static.applifier.com/unityads/files/Invoice_example-UnityAds.xlsx).
3. Send the completed documents as PDF files to _accountspayable-fi@unity3d.com_.

In order to process payments, your invoice must provide banking details, including a proper [SWIFT code](https://en.wikipedia.org/wiki/ISO_9362). Other invoice requirements depend on your country’s finance laws.

#### Developer ID
To find your Developer ID on the [Developer Dashboard](https://developer.cloud.unity3d.com/projects/), select the Operate tab, then Invoices from the left navigation bar. 

![Locate your Developer ID in the Developer Dashboard](https://docs.unity3d.com/ads/DeveloperID.png)

#### Invoice numbers
Choose an invoice number that makes sense for your finance tracking. For example, you may use “0000001” for your first Unity Ads payment request. If you are submitting an invoice on behalf of a larger company, you may wish to speak with your finance team in order to determine the Invoice Number.

### Schedule
Once Unity receives your invoice, it takes 30 days to release the funds.

When you see funds deducted from your account, Unity has processed your payout and requested a bank transfer. It generally takes an additional 3-5 business days for the wire transfer to process. To protect your bank information, ONLY send invoices to _accountspayable-fi@unity3d.com_, and not to any other email accounts. Unity never requests financial information from any other email address.

### Payment methods
Currently, Unity Ads only offers payments by wire transfer. When you submit an invoice for the first time, you must include your bank account information using the [Payment Request Form](https://secure.applifier.com/unityads/files/WireTransferForm-UnityAds.pdf). If wire transfers are not possible in your region, please note that in your invoice request so the Finance team can accommodate you.

### Tax considerations
#### Requesting payment as an individual
Unity can process payment to you as an individual, rather than as a company. To submit an invoice as a private individual, simply enter your legal name in lieu of a company name. Please be sure that this name also matches an owner of your Unity organization.

In general, no taxes are deducted from payments to companies or similar entities. However, if you are a private individual, payments are governed by tax agreements between your country and Finland. These agreements exist to reduce any possible double taxation and set guidelines for personal taxation rules. Taxes for Ads income are usually between 0-15%, but may be higher for certain countries. Consult your own tax office for further guidance.

Unity will not deduct taxes from your payment. Handling taxes for your revenue is your responsibility.

#### Value Added Tax (VAT) numbers
The European Union (EU) requires members to have a [VAT](https://en.wikipedia.org/wiki/VAT_identification_number) number. The local legislation in each country specifies when you need to apply for a VAT number. If you do not have one, state ”No VAT” or “None” in the corresponding invoice field.
