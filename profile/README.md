[![Lightning Flow Scanner Banner](docs/images/bannerslim.png)](https://github.com/Force-Config-Control/.github)

## 🚀 Join our Collective Pursuit of Salesforce Flow Excellence! 🚀

Elevate your Salesforce Flow game and be part of our mission to champion Best Practices and empower Flow Builders. The Lightning Flow Scanner is your trusted ally when building Salesforce Flows! By starring us on GitHub, you're driving the cause of Salesforce Flow Excellence. Your support fuels our mission to help Flow Builders anywhere to confidently meet the latest Best Practices.

Together, let's advance Salesforce Flows and promote excellence!

### 🔧 What We Offer:

- ✨ Static Analysis: Identify and rectify Industry Best Practice violations.
- 🛠️ SFDX Plugin: Seamlessly integrate into CI/CD pipelines like Github Actions.
- 💻 VSCode Extension: An intuitive UI for effortless flow analysis.
- 🤝 Community: Connect with experts and share knowledge.

### 🔍 Best Practice Rules Currently Checked with the Scanner:

| Rule                          | Description                                                                                                                                                                |
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Old API version**           | Newer API components may cause older versions of Flows to start behaving incorrectly due to differences in the underlying mechanics. The Api Version has been available as an attribute on the Flow since API v50.0, and it is recommended to limit variation and to update them on a regular basis. |
| **Copy of API Name**          | Having multiple elements called Copy_X_Of_Element will decrease the readability of the Flow. If you copy and paste them, make sure to update the API name of the new copy.                                            |
| **DML statements in a loop**  | To avoid hitting Apex governor limits, we recommend grouping all of your database changes together at the end of the Flow, whether those changes create, update, or delete records.                                                               |
| **Duplicate DML operations**  | If the Flow commits changes to the database or performs actions between two screens, don't let users navigate back between screens. Otherwise, the Flow may perform duplicate database operations.                                        |
| **Hardcoded Ids**             | IDs are org-specific, so don’t hard-code IDs. Instead, pass them into variables when the Flow starts. You can do so, for example, by using merge fields in URL parameters or by using a Get Records element.                             |
| **Flow naming conventions**   | Readability of a Flow is very important. Setting a naming convention for the Flow Name will improve the findability/searchability and overall consistency. It is recommended to at least provide a domain and a short description of the actions undertaken in the Flow, for example, Service_OrderFulfillment. |
| **Missing flow description**  | Descriptions are useful for documentation purposes. It is recommended to provide information about where it is used and what it will do.                                                                                                     |
| **Missing error handlers**    | Sometimes a Flow doesn’t perform an operation that you configured it to do. By default, the Flow shows an error message to the user and emails the admin who created the Flow. However, you can control that behavior.                                 |
| **Missing null handlers**     | If a Get Records operation does not find any data, it will return null. Use a decision element on the operation result variable to validate that the result is not null.                                                                   |
| **Unconnected elements**      | Unconnected elements that are not being used by the Flow should be avoided to keep Flows efficient and maintainable.                                                                                                                    |
| **Unused variables**          | Unused variables that are not being used by the Flow should be avoided to keep the Flow more efficient and maintainable.                                                                                                                 |

_More information on the rules can be found in the [Lightning Flow Scanner Core module documentation](https://github.com/Force-Config-Control/lightning-flow-scanner-core)._
