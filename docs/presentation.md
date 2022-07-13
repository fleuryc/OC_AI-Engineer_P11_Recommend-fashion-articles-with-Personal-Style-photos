---
marp: true

paginate: true
class: invert
footer: 'Clément Fleury [![Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](https://i.creativecommons.org/l/by-nc-sa/4.0/80x15.png "Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License")](http://creativecommons.org/licenses/by-nc-sa/4.0/ "Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License")'

style: |
  @import url(https://fonts.bunny.net/css?family=asap:400|bungee:400|angkor:400);

  :root {
    font-family: Asap, Arial, sans-serif;
    background-color: snow;
    justify-content: start;
    padding: 50px;
  }

  section.invert {
    background-color: #17202A;
  }

  section.lead {
    justify-content: center;
    padding: 100px;
  }

  h1, h2, h3, h4, h5, h6 {
    font-weight: 400;
  }

  h1, h2 {
    font-family: Bungee;
    text-transform: uppercase;
    text-align: center;
  }

  h3, h4, h5, h6 {
    font-family: Angkor;
    text-transform: capitalize;
  }

  h1 {
    font-size: 4rem;
    color: crimson;
  }

  h2 {
    font-size: 2rem;
    color: navy;
  }

  h3 {
    font-size: 1.5rem;
    color: navy;
  }
  section.invert h3 {
    color: gold;
  }

  h4 {
    font-size: 1.25rem;
  }

  h5 {
    font-size: 1.125rem;
  }

  h6 {
    font-size: 1rem;
  }

  strong {
    color: tomato;
  }
  section.invert strong {
    color: aquamarine;
  }

  em {
    color: salmon;
  }
  section.invert em {
    color: aqua;
  }

  img {
    background-color: transparent;
  }
  section.invert img {
    background-color: snow;
  }

  table, img[alt~="center-img"] {
    justify-content: center;
    display: block;
    margin: 0 auto;
  }
---

<!-- _class:  lead -->

# Fashion-Insta

![center-img h:200px](https://user.oc-static.com/upload/2019/10/24/15719219304432_Capture%20d%E2%80%99e%CC%81cran%202019-10-24%20a%CC%80%2014.56.02.png "Fashion-Insta")

## Personal Style<br/>Articles Recommender

---

### Executive Summary

- **User problems**

> "_Searching_ for articles is **tedious** and _filtering_ excludes articles I **would have bought**."

> "I end-up _returning_ many articles because they **don't match my style**."

- **Solution** : _recommendations_ based on _Profile informations_ and _Personal Style photos_

| **BUILD**                             | **RUN**                          |
| ------------------------------------- | -------------------------------- |
| Budget : _100K€_                      | Costs : _6K€ / month_            |
| Duration : _4 months_                 | Returns : _15K€ / month_         |
| Main risk : _ML models accuracy_      | Time to profitability : _1 year_ |
| Considerations : _Ethics (AI biases)_ | Obligations : _Legal (RGPD)_     |

---

### Business goals

| Context                                             | Target                  |
| --------------------------------------------------- | ----------------------- |
| _visited articles_ before purchase : **26**         | **21** (_-20%_)         |
| _session duration_ before purchase : **19 minutes** | **15 minutes** (_-20%_) |
| _conversion rate_ : **2.6%**                        | **3%** (_+15%_)         |
| _return rate_ because "I don't like it." : **37%**  | **31.5%** (_-15%_)      |
|                                                     |                         |
| _average sale Value_ : **19.5€**                    | **22.5€** (_+15%_)      |
| _average sale Margin_ : **20%**                     | **22%** (_+10%_)        |

> Source : [Website and CRM statistics](https://www.blogdumoderateur.com/chiffres-cles-e-commerce-2022-taux-conversion-panier-moyen-pages-vues-session/)

---

### Expected returns

---

### Human resources

---

### Technical resources

---

### Financial resources

---

### Agile development

---

---

# Stop

---

### Curent MVP System Architecture

![center-img h:550px](img/architecture.drawio.png "Current MVP architecture")

---

### Resources inventory

| **LUIS**                                                                                                                                                                                                                                    | **Chatbot**                                                                                                                                                                                                                            | **Monitoring**                                                                                                                                                                                                                                                                                                                            |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [Language understanding model](https://www.luis.ai/applications)                                                                                                                                                                            | [Bot service](https://portal.azure.com/#@clementfleurypm.onmicrosoft.com/resource/subscriptions/da2e4791-6dd1-422b-848a-a961cef6ab89/resourceGroups/OC_P10_Bot/providers/Microsoft.BotService/botServices/fly_me/overview)             | [Application Insights](https://portal.azure.com/#@clementfleurypm.onmicrosoft.com/resource/subscriptions/da2e4791-6dd1-422b-848a-a961cef6ab89/resourceGroups/OC_P10_Bot/providers/microsoft.insights/components/ocp10-appinsights/overview)                                                                                               |
| [Authoring resource](https://portal.azure.com/#@clementfleurypm.onmicrosoft.com/resource/subscriptions/da2e4791-6dd1-422b-848a-a961cef6ab89/resourceGroups/OC_P10/providers/Microsoft.CognitiveServices/accounts/ocp10-luis-auth/overview)  | [App Service Plan](https://portal.azure.com/#@clementfleurypm.onmicrosoft.com/resource/subscriptions/da2e4791-6dd1-422b-848a-a961cef6ab89/resourceGroups/OC_P10_Bot/providers/Microsoft.Web/serverFarms/ocp10-bot-plan/webHostingPlan) | [Alert Rule](https://portal.azure.com/#view/Microsoft_Azure_Monitoring/UpdateLogSearchV2AlertRuleViewModel/alertId/%2Fsubscriptions%2Fda2e4791-6dd1-422b-848a-a961cef6ab89%2FresourceGroups%2FOC_P10_Bot%2Fproviders%2Fmicrosoft.insights%2Fscheduledqueryrules%2FWARNING%20-%20More%20than%205%20Booking%20Refused%20last%205%20minutes) |
| [Prediction resource](https://portal.azure.com/#@clementfleurypm.onmicrosoft.com/resource/subscriptions/da2e4791-6dd1-422b-848a-a961cef6ab89/resourceGroups/OC_P10/providers/Microsoft.CognitiveServices/accounts/ocp10-luis-pred/overview) | [App Service](https://portal.azure.com/#@clementfleurypm.onmicrosoft.com/resource/subscriptions/da2e4791-6dd1-422b-848a-a961cef6ab89/resourceGroups/OC_P10_Bot/providers/Microsoft.Web/sites/ocp10-bot-webapp/appServices)             | [Monitoring Dashboard](https://portal.azure.com/#@clementfleurypm.onmicrosoft.com/dashboard/private/41e0e40e-2469-4ecf-91c6-d576b3787015)                                                                                                                                                                                                 |

---

### Demo

|                     **Demo**                     |                  **Monitoring**                  |
| :----------------------------------------------: | :----------------------------------------------: |
| ![center-img h:475px](img/screencast.gif "Demo") | ![center-img h:475px](img/monitoring.png "Demo") |

---

### Target performance management policy

In order to achieve the target performance, the following policy must be implemented :

- **store** each dialogs and inferred _intents_ and _entities_ in a _database_
- **transform and load** (ETL) the raw data in a _datawarehouse_ in a _format compatible with the LUIS service_
- daily **re-train** the _language understanding model_ with the new _intents_ and _entities_ of the **successful** bookings

---

### Target production architecture

![center-img h:550px](img/target-architecture.drawio.png "Target production architecture")

---

### Next steps

- **integrate** the bot with multiple _Channels_ (Website, Discord, Teams, Slack, ...)
- **improve** the bot capacity to handle more _Intentions_ and _Entities_
- **connect** the bot to an actual _Flight booking_ system
- **monitor** more precisely the bot's performance : _errors_, _performance_, _availability_, ...
- **implement** the model continuous _training_ and _deployment_

---

<!-- _class:  lead -->

# Fly Me

## Flights booking chatbot

[![center-img h:120px](img/GitHub-Mark-120px-plus.png "GitHub")](https://github.com/fleuryc/OC_AI-Engineer_P10_Flights-booking-chatbot "Fly Me : flights booking chatbot")
