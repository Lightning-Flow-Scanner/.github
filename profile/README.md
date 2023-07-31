[![Lightning Flow Scanner Banner](docs/images/banner.png)](https://github.com/Force-Config-Control/.github)

_**Salesforce**_ is heavily innovating its **_No-Code/Low-Code Solutions_** and there is a **rising need** for ways to **ensure industry best practices are being followed** to fully leverage this innovation, whilst still preventing or minimizing certain technical debt that can arise when using Salesforce Flows. **Lightning Flow Scanner** is a **free** and **open-source tool** that can perform **static analysis on _Salesforce Flows_, _Process Builders_** and **_Workflows_** to **identify violations of industry best practices**. It is available as a **_[SFDX plugin](https://www.npmjs.com/package/lightning-flow-scanner)_** which can be used in a **_CLI_**(implementable in _CI/CD pipelines_ like _Github Actions_) and as a **_[VSCode extension](https://marketplace.visualstudio.com/items?itemName=ForceConfigControl.lightningflowscanner)_** that provides a **_UI_**. Our aim is to **become a community** that shares their knowledge on best practices as **open standards** in a **plug & play manner**, so **_Flow Builders_ can feel confident their _Flows_ meet every latest _Best Practice_.** 

####  Current Checks Included:
| Rule       | Description |
|--------------|:-----------|
| **Old API version** | Newer API components may cause older versions of Flows to start behaving incorrectly due to differences in the underlying mechanics. The Api Version has been available as an attribute on the Flow since API v50.0 and it is recommended to limit variation and to update them on a regular basis. |
| **DML statements in a loop** |  To avoid hitting Apex governor limits, we recommend grouping all of your database changes together at the end of the flow, whether those changes create, update, or delete records. |
| **Duplicate DML operations** |   If the flow commits changes to the database or performs actions between two screens, don't let users navigate back between screen. Otherwise, the flow may perform duplicate database operations. |
| **Hardcoded Ids** |  IDs are org-specific, so don’t hard-code IDs. Instead, pass them into variables when the flow starts. You can do so, for example, by using merge fields in URL parameters or by using a Get Records element. |
| **Flow naming conventions** |  Readability of a flow is very important. Setting a naming convention for the Flow Name will improve the findability/searchability and overall consistency. It is recommended to at least provide a domain and a short description of the actions undertaken in the flow, in example Service_OrderFulfillment. |
| **Missing flow description** |   Descriptions are useful for documentation purposes. It is recommended to provide information about where it is used and what it will do. |
| **Missing error handlers** |  Sometimes a flow doesn’t perform an operation that you configured it to do. By default, the flow shows an error message to the user and emails the admin who created the flow. However, you can control that behavior. |
| **Missing null handlers**      |   If a Get Records operation does not find any data it will return null. Use a decision element on the operation result variable to validate that the result is not null. |
| **Unconnected elements** |  Unconnected elements which are not being used by the Flow should be avoided to keep Flows efficient and maintainable. |
| **Unused variables**      |  Unused variables which are not being used by the Flow should be avoided to keep Flow more efficient and maintainable. |

_More information on the rules can be found in the [lfs-core module documentation](https://github.com/Force-Config-Control/lightning-flow-scanner-core)._
