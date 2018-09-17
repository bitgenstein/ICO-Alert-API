# ICO-Alert-API
ICO Alert API

***Usage:***

**Show ICOs**
----
  Returns json data about a single ICO or all ICOs. Restrictable to enabled only, disabled only, and/or a specific date range if desired.

* **URL**

  https://sophocles.icoalert.com/api.php? [URL Params]
  
*  **URL Params**

   **Required:**
 
   * **`KEY=[string]`**
   
      Obtain your API key by requesting one from team@icoalert.com

   **Optional:**
   
   * **`FILTER=date`*
   
      Enables date filter
   
   * **`STARTDATE=[date]`*
   
   * **`ENDDATE=[date]`*
   
      Suggested format: YYYY-MM-DD. Only for use with `FILTER=date`
   
   * **`INCLUDEDISABLED=no`*
   
      Hides disabled ICOs
   
   * **`INCLUDEDISABLED=no`*
   
      Hides enabled ICOs
   
   * **`ICO=[int]`**
   
      5-digit ICO id number calls data on a specific single ICO. (This does not return more data points on the single ICO than is returned when calling multiple ICOs)

* **API Sample Calls**
  (parameter names such as KEY are case sensitive)

  * **Getting information on one ICO:**
  `https://sophocles.icoalert.com/api.php?KEY=MYKEY&ICO=26866`

  * **Getting all enabled ICOs that started or were running in August 2018:**
  `https://sophocles.icoalert.com/api.php?KEY=MYKEY&INCLUDEDISABLED=no&FILTER=date&STARTDATE=2018-08-01&ENDDATE=2018-08-31`

  * **Getting all disabled ICOs that ran in 2017:**
  `https://sophocles.icoalert.com/api.php?KEY=MYKEY&INCLUDEENABLED=no&INCLUDEDISABLED=yes&FILTER=date&STARTDATE=2018-01-01&ENDDATE=2018-12-31`

  * **Getting page 2 of the results above (limit is 50 per page):**
  `https://sophocles.icoalert.com/api.php?KEY=MYKEY&INCLUDEENABLED=no&INCLUDEDISABLED=yes&FILTER=date&STARTDATE=2018-01-01&ENDDATE=2018-12-31&PAGE=2`

* **Sample Response Content (abridged to one ICO. Data for sample purposes only):** 
    ```json
    {
      "totalICOsFound": 1,
      "totalPages": 1,
      "icosPerPage": 50,
      "currentPage": 1,
      "results": [
        {
          "id": "58351",
          "name": "OrganTree",
          "description": "Blockchain helping to solve the inefficiencies in organ matching.",
          "enabled": "true",
          "amountRaised": "0.00000000 // for non-concluded ICOs, 0 indicates no data",
          "kycRequired": "false",
          "openSourceProject": "false",
          "platform": "Ethereum",
          "reportLink": "",
          "softCapReached": "false",
          "usaAccreditedInvestorsAllowed": "false",
          "website": "http://ico.organ-tree.com",
          "emailContact": "admin@organ-tree.com",
          "emailContactName": "Ron Gologorsky",
          "businessWebsite": "http://ico.organ-tree.com",
          "incorporationLocation": "Ireland",
          "headquartersLocation": "Ireland",
          "token": [
            {
              "tokenName": "OrganTree",
              "tokenSymbol": "OGT",
              "tokenPreMinedAmount": "0.00000000",
              "tokenMaximumSupply": "2500000000.00000000",
              "tokenSmartContractAddress": "0x5df451ed892a40030078b887d0a4febde4c8f0a9",
              "tokenPriceUSD": "",
              "tokenPriceEUR": "",
              "tokenPriceBTC": "",
              "tokenPriceETH": "0.00003125"
            }
          ],
          "airdrops": [
            {
              "airdropAnnouncementLink": "",
              "airdropDate": "",
              "registrationLink": "https://docs.google.com/forms/d/e/1FAIpQLSec09suuIPKTTYsaPV-XB9qKBvJ0XV0BX7dyHZLT3JKy1MsDA/viewform",
              "airdropTokenSymbol": "ETH",
              "airdropPreMinedAmount": "0.00000000",
              "airdropSmartContract": "",
              "airdropMaximumSupply": "0.00000000"
            }
          ],
          "distribution": [
            {
              "distributionName": "Crowdsale",
              "distributionCliff": "0",
              "distributionPercentageOfTokens": "0.50"
            },
            {
              "distributionName": "Operations",
              "distributionCliff": "0",
              "distributionPercentageOfTokens": "0.20"
            },
            {
              "distributionName": "Foundation",
              "distributionCliff": "0",
              "distributionPercentageOfTokens": "0.10"
            },
            {
              "distributionName": "Bounty",
              "distributionCliff": "0",
              "distributionPercentageOfTokens": "0.03"
            },
            {
              "distributionName": "Advisors",
              "distributionCliff": "0",
              "distributionPercentageOfTokens": "0.02"
            }
          ],
          "allocation": [
            {
              "allocationType": "Advisors",
              "percentage": 20.5
            },
            {
              "allocationType": "Marketing",
              "percentage": 15.5
            },
            {
              "allocationType": "Development",
              "percentage": 64
            }
          ],
          "KYCRequirements": [
            {
              "addressRequired": "false",
              "citizenshipRequired": "true",
              "emailRequired": "true",
              "governmentIssuedIdRequired": "false",
              "nameRequired": "false",
              "phoneNumberRequired": "true"
            }
          ],
          "paymentTokens": [
            {
              "paymentTokenName": "U.S. Dollar"
            },
            {
              "paymentTokenName": "Ethereum"
            },
            {
              "paymentTokenName": "Bitcoin"
            }
          ],
          "industries": [
            {
              "industryName": "Cryptocurrency"
            },
            {
              "industryName": "Insurance"
            }
          ],
          "links": {
            "askFm": "",
            "bitcoinTalk": "",
            "blog": "",
            "bountyProgram": "\t0x5df451ed892a40030078b887d0a4febde4c8f0a9",
            "everpedia": "",
            "facebook": "https://www.facebook.com/organtree/",
            "github": "https://github.com/Organ-Tree",
            "googlePlus": "",
            "instagram": "",
            "linkedIn": "",
            "medium": "https://medium.com/@ogtsocial/organ-tree-organ-donation-ecosystem-powered-by-blockchain-506c80934cb9",
            "mvp": "organ-tree.com",
            "promoVideo": "",
            "reddit": "https://www.reddit.com/user/ORGANTREEICO/comments/8z2j1u/organ_tree/?utm_source=amp&utm_medium=top_post",
            "rss": "",
            "slack": "",
            "steemit": "",
            "telegram": "https://t.me/joinchat/JK1ozkeTeVwt7LkaemwdIw",
            "twitter": "https://twitter.com/Organ_tree",
            "vk": "",
            "wechat": "",
            "whitePaper": "https://ico.organ-tree.com/organ-tree-vision.pdf",
            "youtube": ""
          },
          "prohibitedCountries": [
            {
              "prohibitedCountryName": "United States of America"
            },
            {
              "prohibitedCountryName": "China"
            },
            {
              "prohibitedCountryName": "Singapore"
            }
          ],
          "rounds": [
            {
              "type": "private",
              "timeframe": "exactDates",
              "startDate": "2018/09/30",
              "endDate": "2018/10/15",
              "smartContractAddress": "0xC0479AC700A669E55004E9E"
            },
            {
              "type": "presale",
              "timeframe": "month",
              "month": 11,
              "year": 2018
            },
            {
              "type": "presale",
              "timeframe": "quarter",
              "quarter": 1,
              "year": 2018
            },
            {
              "type": "sale",
              "timeframe": "tbd"
            }
          ],
          "teamMembers": [
            {
              "title": "CEO",
              "firstName": "Ron",
              "lastName": "Gologorsky",
              "linkedIn": "https://www.linkedin.com/in/ron-gologorsky-a61228167/"
            }
          ]
        }
      ]
    }
