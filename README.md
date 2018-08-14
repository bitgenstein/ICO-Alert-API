# sophocles_api
Sophocles API

***Usage:***

**Show ICO**
----
  Returns json data about a single ICO.

* **URL**

  /icos/:id

* **Method:**

  `GET`
  
*  **URL Params**

   **Required:**
 
   `id=[integer]`

* **Data Params**

  None

* **Success Response:**

  * **Code:** 200 <br />
    **Sample Content:** `{ id : 26866,<br />
      name : "Wono",<br />
      description: "An ICO with a real name but otherwise sample data",<br />
      amountRaised: 10521000.00,<br />
      kycRequired: 1,<br />
      openSourceProject: 1,<br />
      platform: "Ethereum",<br />
      reportLink: "https://blog.icoalert.com/wonoReport.php",<br />
      softCapReached: 1,<br />
      usaAccreditedInvestorsAllowed: 1,<br />
      website: "https://wono.io",<br />
      websiteRegistrationDate: 2018/01/20,<br />
      whitelistRegistrationDeadline: 2018/08/20,<br />
      whitelistRegistrationLink: "https://wono.io#whitelist",<br />
      token: {<br />
          name: "Wonobytes",<br />
          tokenSymbol: "WON",<br />
          maximumSupply: 10000000000000000,<br />
          smartContractAddress: "0xAB21FF3CAD411D2FF4510089A3EE211EEE",<br />
          annualInflationRate: 0<br />
      team: {<br />
          {<br />
            id: 12102,<br />
            firstName: "John",<br />
            lastName: "Benedict",<br />
            email: "jbenedict@wono.io",<br />
            linkedin: "https://linkedin.com/in/jbennydict"<br />
          },<br />
          {<br />
            id: 12103,<br />
            firstName: "Gopesh",<br />
            lastName: "Antonopoulos",<br />
            email: "indiaofmoney@gmail.com",<br />
            linkedin: ""<br />
          }<br />
        },<br />
      kycRequirements: {<br />
          address: 1,<br />
          citizenship: 1,<br />
          email: 1,<br />
          governmentIssuedId: 0,<br />
          name: 1,<br />
          phoneNumber: 0<br />
        },<br />
      icoParentCompany: {<br />
          name: "Wono Holdings Ltd",<br />
          headquarters: "China",<br />
          incorporation: "Hong Kong",<br />
          stockTicker: "WHH",<br />
          website: ""<br />
        },<br />
      icoPartnershipCompany: {<br />
          {<br />
            id: 12122,<br />
            name: "Wono Phantom Company",<br />
            headquarters: "China",<br />
            incorporation: "Hong Kong",<br />
            stockTicker: "WPC",<br />
            website: ""<br />
          },<br />
          {<br />
            id: 12123,<br />
            name: "Wono Ghost Company",<br />
            headquarters: "China",<br />
            incorporation: "Hong Kong",<br />
            stockTicker: "WGC",<br />
            website: ""<br />
          }<br />
        },<br />
      icoPaymentToken: {<br />
          {<br />
            name: "Ethereum",<br />
            tokenSymbol: "ETH"<br />
          },<br />
          {<br />
            name: "Doge Dark",<br />
            tokenSymbol: "DOGEDARK"<br />
          }<br />
        },<br />
      icoIndustry: {<br />
          industries: "Engineering,Cryptocurrency,Supply Chain"<br />
        },<br />
      icoProhibitedCountries: {<br />
          prohibitedCountries: "USA,Kafiristan,Kyrat,Ku"<br />
        },<br />
      icoRounds: {<br />
          {<br />
            type: "private",<br />
            timeframe: "exactDates",<br />
            startDate: 2018/09/30,<br />
            endDate: 2018/10/15,<br />
            smartContractAddress: "0xC0479AC700A669E55004E9E"<br />
          },<br />
          {<br />
            type: "presale",<br />
            timeframe: "month",<br />
            month: 11,<br />
            year: 2018<br />
          },<br />
          {<br />
            type: "presale",<br />
            timeframe: "quarter",<br />
            quarter: 1,<br />
            year: 2018<br />
          },<br />
          {<br />
            type: "sale"<br />
            timeframe: "tbd"<br />
          }<br />
        },<br />
      icoLinks: {<br />
          askFm: "",<br />
          bitcoinTalk: "https://bitcointalk.org/wono",<br />
          blog: "https://blog.wono.io",<br />
          bounty0x: "",<br />
          bountyProgram: "",<br />
          discord: "https://disco.rd/wono",<br />
          everpedia: "",<br />
          facebook: "https://facebook.com/wono",<br />
          github: "",<br />
          googlePlus: "",<br />
          instagram: "",<br />
          linkedIn: "https://linkedin.com/in/wono",<br />
          medium: "https://medium.com/wono",<br />
          mvp: "",<br />
          promoVideo: "https://youtu.be/w08n-z1r",<br />
          reddit: "",<br />
          rss: "",<br />
          slack: "",<br />
          steemit: "",<br />
          telegram: "https://t.me/getwono",<br />
          twitter: "https://twitter.com/wono",<br />
          vk: "",<br />
          wechat: "",<br />
          whitePaper: "https://wono.io/whitepaper",<br />
          youtube: "https://youtube.com/wono"<br />
        }<br />
      icoStats: {<br />
          myPortfolioAdds: 29,<br />
          myPortfolioRanking: 52,<br />
          freeClicks: 9,<br />
          featuredClicks: 151,<br />
          trendingClicks: 300<br />
      }<br />
    }`
 
* **Error Response:**

  * **Code:** 404 NOT FOUND <br />
    **Content:** `{ error : "ICO doesn't exist" }`

  OR

  * **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{ error : "You are unauthorized to make this request." }`

* **Sample Call:**

  ```javascript
    $.ajax({
      url: "/icos/26866",
      dataType: "json",
      type : "GET",
      success : function(r) {
        console.log(r);
      }
    });
  ```
