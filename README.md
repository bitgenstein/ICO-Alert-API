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
    **Sample Content:** `{ id : 26866,
      name : "Wono",
      description: "An ICO with a real name but otherwise sample data",
      amountRaised: 10521000.00,
      kycRequired: 1,
      openSourceProject: 1,
      platform: "Ethereum",
      reportLink: "https://blog.icoalert.com/wonoReport.php",
      softCapReached: 1,
      usaAccreditedInvestorsAllowed: 1,
      website: "https://wono.io",
      websiteRegistrationDate: 2018/01/20,
      whitelistRegistrationDeadline: 2018/08/20,
      whitelistRegistrationLink: "https://wono.io#whitelist",
      token: { 
          name: "Wonobytes",
          tokenSymbol: "WON",
          maximumSupply: 10000000000000000,
          smartContractAddress: "0xAB21FF3CAD411D2FF4510089A3EE211EEE",
          annualInflationRate: 0
      team: {
          {
            id: 12102,
            firstName: "John",
            lastName: "Benedict",
            email: "jbenedict@wono.io",
            linkedin: "https://linkedin.com/in/jbennydict"
          },
          {
            id: 12103,
            firstName: "Gopesh",
            lastName: "Antonopoulos",
            email: "indiaofmoney@gmail.com",
            linkedin: ""
          }
        },
      kycRequirements: {
          address: 1,
          citizenship: 1,
          email: 1,
          governmentIssuedId: 0,
          name: 1,
          phoneNumber: 0
        },
      icoParentCompany: {
          name: "Wono Holdings Ltd",
          headquarters: "China",
          incorporation: "Hong Kong",
          stockTicker: "WHH",
          website: ""
        },
      icoPartnershipCompany: {
          {
            id: 12122,
            name: "Wono Phantom Company",
            headquarters: "China",
            incorporation: "Hong Kong",
            stockTicker: "WPC",
            website: ""
          },
          {
            id: 12123,
            name: "Wono Ghost Company",
            headquarters: "China",
            incorporation: "Hong Kong",
            stockTicker: "WGC",
            website: ""
          }
        },
      icoPaymentToken: {
          {
            name: "Ethereum",
            tokenSymbol: "ETH"
          },
          {
            name: "Doge Dark",
            tokenSymbol: "DOGEDARK"
          }
        },
      icoIndustry: {
          industries: "Engineering,Cryptocurrency,Supply Chain"
        },
      icoProhibitedCountries: {
          prohibitedCountries: "USA,Kafiristan,Kyrat,Ku"
        },
      icoRounds: {
          {
            type: "private",
            timeframe: "exactDates",
            startDate: 2018/09/30,
            endDate: 2018/10/15,
            smartContractAddress: "0xC0479AC700A669E55004E9E"
          },
          {
            type: "presale",
            timeframe: "month",
            month: 11,
            year: 2018
          },
          {
            type: "presale",
            timeframe: "quarter",
            quarter: 1,
            year: 2018
          },
          {
            type: "sale"
            timeframe: "tbd"
          }
        },
      icoLinks: {
          askFm: "",
          bitcoinTalk: "https://bitcointalk.org/wono",
          blog: "https://blog.wono.io",
          bounty0x: "",
          bountyProgram: "",
          discord: "https://disco.rd/wono",
          everpedia: "",
          facebook: "https://facebook.com/wono",
          github: "",
          googlePlus: "",
          instagram: "",
          linkedIn: "https://linkedin.com/in/wono",
          medium: "https://medium.com/wono",
          mvp: "",
          promoVideo: "https://youtu.be/w08n-z1r",
          reddit: "",
          rss: "",
          slack: "",
          steemit: "",
          telegram: "https://t.me/getwono",
          twitter: "https://twitter.com/wono",
          vk: "",
          wechat: "",
          whitePaper: "https://wono.io/whitepaper",
          youtube: "https://youtube.com/wono"
        }
      icoStats: {
          myPortfolioAdds: 29,
          myPortfolioRanking: 52,
          freeClicks: 9,
          featuredClicks: 151,
          trendingClicks: 300
      }
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