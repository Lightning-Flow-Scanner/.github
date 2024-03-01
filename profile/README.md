[![Lightning Flow Scanner Banner](docs/images/bannerslim.png)](https://github.com/Lightning-Flow-Scanner/.github)

## 🚀 Join our Collective Pursuit of Salesforce Flow Excellence!

The Lightning Flow Scanner is your trusted ally when building Salesforce Flows! Elevate your Salesforce Flow game and be part of our mission to champion Best Practices and empower Flow Builders. By getting involved with us on GitHub, you're fueling Salesforce Flow Excellence and boosting Flow Builders' confidence in effortlessly adopting the latest Best Practices. Let's promote excellence together!

### 🔧 What We Offer:

- ✨ [Best Practices Analysis](https://github.com/Lightning-Flow-Scanner/lightning-flow-scanner-core): Ensure your Flows adhere to the latest Best Practices through Comprehensive Static Analysis.
- 💻 [VSCode Extension](https://github.com/Lightning-Flow-Scanner/lightning-flow-scanner-vsce): An intuitive UI for effortless flow analysis.
- 🛠️ [SFDX Plugin](https://github.com/Lightning-Flow-Scanner/lightning-flow-scanner-sfdx): Seamlessly integrate into CI/CD pipelines like Github Actions.
- 🛠️ [Copado Plugin](https://success.copado.com/s/listing-detail?recordId=a54P7000003G3gBIAS): Plugin for Copado Users
- 📂 [Demo Flows](https://github.com/Lightning-Flow-Scanner/lightning-flow-scanner-example-flows): Explore real-world examples of Flow violations and their resolutions, providing practical insights to enhance your Salesforce Flow development and scanning process.
- 🤝 [Chat Room](https://matrix.to/#/#lightning-flow-scanner:matrix.org): If you have a quick question or you want to connect, feel free to join our gitter chat immediately! 

### 🔍 Best Practices Checked with our Scanner:

| Rule       | Description |
|--------------|:-----------|
| **Outdated API Version** | Introducing newer API components may lead to unexpected issues with older versions of Flows, as they might not align with the underlying mechanics. Starting from API version 50.0, the 'Api Version' attribute has been readily available on the Flow Object. To ensure smooth operation and reduce discrepancies between API versions, it is strongly advised to regularly update and maintain them. |
| **Copy API Name** | Maintaining multiple elements with a similar name, like 'Copy_X_Of_Element,' can diminish the overall readability of your Flow. When copying and pasting these elements, it's crucial to remember to update the API name of the newly created copy. |
| **DML Statement In A Loop** |  To prevent exceeding Apex governor limits, it is advisable to consolidate all your database operations, including record creation, updates, or deletions, at the conclusion of the flow. |
| **Duplicate DML Operation** |   When the flow executes database changes or actions between two screens, it's important to prevent users from navigating back between screens. Failure to do so may result in duplicate database operations being performed within the flow. |
| **Hardcoded Id** |  Avoid hard-coding IDs as they are org-specific. Instead, pass them into variables at the start of the flow. You can achieve this by utilizing merge fields in URL parameters or employing a Get Records element. |
| **Flow Naming Convention** |  The readability of a flow is of utmost importance. Establishing a naming convention for the Flow Name significantly enhances findability, searchability, and maintains overall consistency. It is advisable to include at least a domain and a brief description of the actions carried out in the flow, for instance, 'Service_OrderFulfillment'. |
| **Missing Flow Description** |   Descriptions play a vital role in documentation. We highly recommend including details about where they are used and their intended purpose. |
| **Missing Fault Path** |  At times, a flow may fail to execute a configured operation as intended. By default, the flow displays an error message to the user and notifies the admin who created the flow via email. However, you can customize this behavior by incorporating a Fault Path. |
| **Missing Null Handler**      |   When a Get Records operation doesn't find any data, it returns null. To ensure data validation, utilize a decision element on the operation result variable to check for a non-null result. |
| **SOQL Query In A Loop** |  To prevent exceeding Apex governor limits, it is advisable to consolidate all your SOQL queries at the conclusion of the flow. |
| **Unconnected Element** |  Unconnected elements which are not being used by the Flow should be avoided to keep Flows efficient and maintainable. |
| **Unused Variable**      |  To maintain the efficiency and manageability of your Flow, it's advisable to avoid including unconnected variables that are not in use. |

_More information on the rules can be found in the [Lightning Flow Scanner Core module documentation](https://github.com/Lightning-Flow-Scanner/lightning-flow-scanner-core)._
