## 🌐 Join our Collective Pursuit of Salesforce Flow Excellence!

### As Seen On [Salesforce codeLive 📺](https://www.youtube.com/watch?v=VxZWfhTzEqU) 

_"Maintaining high-quality Salesforce Flows is critical for the success of your business applications. Lightning Flow Scanner is a powerful tool that can help you identify and address common issues in your Flows."_ - Mohith Shrivastava, Principal Developer Advocate at Salesforce.

- ✨ Count on us for Transparent, Up-to-Date Assessments of Flows, Driven by Our Commitment to Open Source.
- 🚀 Experience Empowerment at No Cost, Continuously Deepening Your Understanding of Flows.
- 💡 Drive Innovation by Integrating Low-Code and Traditional Development Workflows.
- 🤝 Empower All Voices to Shape the Standard of Flow Excellence Through Open Collaboration.
- 🌱 Promote Excellence and Reduce Technical Debt for Resilient Solutions.

Explore our [Flow Analysis](#extensible-flow-analysis) [![Downloads/total](https://img.shields.io/npm/dt/lightning-flow-scanner.svg)](https://www.npmjs.com/package/lightning-flow-scanner-core) in Various Forms 🔍
  - 💻 [VSCode](https://marketplace.visualstudio.com/items?itemName=ForceConfigControl.lightningflowscanner) / [Code Builder](https://open-vsx.org/extension/ForceConfigControl/lightningflowscanner) [![GitHub stars](https://img.shields.io/github/stars/Lightning-Flow-Scanner/lightning-flow-scanner-vsce)](https://github.com/Lightning-Flow-Scanner/lightning-flow-scanner-vsce/stargazers) - Examine Flows directly within VSCode or the Salesforce Code Builder. 
  - 🛠️ [Salesforce CLI](https://www.npmjs.com/package/lightning-flow-scanner) [![GitHub stars](https://img.shields.io/github/stars/Lightning-Flow-Scanner/lightning-flow-scanner-sfdx)](https://GitHub.com/Lightning-Flow-Scanner/lightning-flow-scanner-sfdx/stargazers/) - Integrate Flow Analysis into Github Actions and your CI/CD pipelines. 
  - 🚦 [Copado Pipelines](https://success.copado.com/s/listing-detail?recordId=a54P7000003G3gBIAS) - Perform Flow Analysis as a quality gate within Copado.

Furthermore, see our:
- 📂 [Demo Flows](https://github.com/Lightning-Flow-Scanner/lightning-flow-scanner-example-flows): Explore practical examples of violations and their resolutions.
- 🏛️ [Forum](https://github.com/orgs/Lightning-Flow-Scanner/discussions): Ask questions and share insights on everything related to Flows.
- 💬 [Chat Room](https://matrix.to/#/#lightning-flow-scanner:matrix.org): Connect & engage in real-time.

### Extensible Flow Analysis: 
The following are default violations are detected by our analysis:

| Rule | Description |
|--------------------------|-------------|
| **Auto Layout**  | Elements are spaced, connected, and aligned automatically in Auto Layout Mode. |
| **Copy API Name**  | Update API names when copying elements to maintain readability. |
| **DML Statement In A Loop** | Consolidate database operations to prevent exceeding governor limits. |
| **Duplicate DML Operation**  | Prevent duplicate database operations between screens. |
| **Flow Naming Convention**  | Establish a naming convention for better findability and consistency. |
| **Hardcoded Id**  | Remove hardcoded ID's to eliminate data dependencies. |
| **Inactive Flow**  | Delete unused flows to prevent unexpected behaviour.  |
| **Missing Flow Description**  | Include descriptions to document flow usage and purpose. |
| **Missing Fault Path**  | Customize error handling with a Fault Path to handle flow failures. |
| **Missing Null Handler**  | Validate data by checking for non-null results in Get Records operations. |
| **Outdated API Version**  | Regularly update API versions to avoid discrepancies and ensure compatibility. |
| **Process Builder**  | Migrate your organization's automation to Flow. |
| **SOQL Query In A Loop**  | Consolidate SOQL queries to avoid governor limit issues. |
| **Unconnected Element**  | Avoid unconnected elements to maintain flow efficiency. |
| **Unused Variable**  | Remove unused variables for better flow manageability. |

_Additional information on the default rules and the extensibility of the engine can be found in our [Documentation](https://lightning-flow-scanner.github.io/lightning-flow-scanner-core/)._
