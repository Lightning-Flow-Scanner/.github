[![Lightning Flow Scanner Banner](docs/images/bannerslim.png)](https://github.com/Lightning-Flow-Scanner/.github)

## 🚀 Join our Collective Pursuit of Salesforce Flow Excellence!

  **_Take your Salesforce Flows to the next level and join us in our commitment to promoting Best Practices. By getting involved, you'll help improve Flows and boost confidence among Flow Builders. Let's work together to achieve excellence!_**

### 🔧 We Offer:

- ✨ [Static Analysis](https://github.com/Lightning-Flow-Scanner/lightning-flow-scanner-core):  Ensure Flows adhere to Best Practices with our extensible Ruleset and Flow Compiler.
  - 💻 [VSCode Extension](https://github.com/Lightning-Flow-Scanner/lightning-flow-scanner-vsce): Analyze Flows directly within VSCode.
  - 💻 [Code Builder Extension](https://open-vsx.org/extension/ForceConfigControl/lightningflowscanner): Analyze Flows in the web with the Salesforce Code Builder.
  - 🛠️ [SFDX Plugin](https://github.com/Lightning-Flow-Scanner/lightning-flow-scanner-sfdx): Integrate Flow analysis into your CI/CD pipelines.
  - 🛠️ [Copado Plugin](https://success.copado.com/s/listing-detail?recordId=a54P7000003G3gBIAS): Tailored integration for Copado Users.
- 📂 [Demo Flows](https://github.com/Lightning-Flow-Scanner/lightning-flow-scanner-example-flows): Explore practical examples of violations and their resolutions.
- 🤝 [Chat Room](https://matrix.to/#/#lightning-flow-scanner:matrix.org): Join our Gitter chat for immediate support and community engagement.


### 🔍 Our Extensible Ruleset:

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

_More information on the default ruleset and how to extend it is in the [Core Module Documentation](https://github.com/Lightning-Flow-Scanner/lightning-flow-scanner-core)._
