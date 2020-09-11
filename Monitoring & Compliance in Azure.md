# Monitoring and Compliance in Azure

## Azure Compliance, Regulations & Standards

* Either small,m medium or enterprise level, organizations need to comply with regulations and standards
* Microsoft Azure leading the industry with 90+ compliance offerings
    - 50+ specific to regions or countries
    - 35+ compliance offerings specific to the needs of key industries, including health, government, finance, education, manufacturing and media.
* **General Data Protection Regulation (GDPR)** - European privacy law that imposes new rules on companies that collect and analyze data tied to EU residents.
* **Health Insurance Portability and Accountability Act (HIPAA)** - US federal law that regulates patient Protected Health Information (PHI)
* **International Organization for Standardization (ISO) & International Electrotechnical Commision 27018 (IEC)** - processing of personal information by cloud providers.
* **National Institue of Standards and Technology Cybersecurity Framework (NIST CSF)** - Standards, guidelines and best practices to manage cybersecurity-related risks.
* **Azure Government** - Dedicated public cloud for federal and state agencies in USA.
* **UK Government G-Cloud** - Government entities in the UK.

## Azure Blueprints

* Enables cloud architects to define a repeatable set of Azure resources that implements and follows an organization's standards, patterns and requirements
* Declarative way to orchestrate the deployments of various resource tempaltes and other artifacts
    - **Role assignments**
    - **Policy assignments**
    - **Azure Resource Manager templates**
    - **Resource groups**
* With Azure Blueprints you deploy and update cloud environemnts in a repeatable manner, using composable artifacts - ARM templates, RGs, policy assignments, RBAC
* With ARM templates, you execute the deployment but once resources are deployed there is no active connection or relationship to the template.
* With Blueprints, the relationship between the blueprint definition (what should be deployed) and the blueprint assignment (what was deployed) is preserved
* Great for tracking and auditing of deployments
* Also, with Blueprints you can also upgrade several subscriptions at once, that are governed by the same blueprint
* In a Blueprint, you can use multiple templates

## Azure Advisor

* Helps you follow best practices and optimize your Azure deployments
* Resource configuration and Usage are analyzed and recommendations are provided
    - Improve the cost effectiveness
    - Performance
    - High availability
    - Security of your Azure resources
* Available in Azure Portal and recommendations are split into 5 categories:
    - **High Availability**
        * Ensure and improve the continuity of your business-critical apps. 
    - **Security**
        * To detect threats and vulnerabilities.
    - **Performance**
        * To rimpove the speed of your apps
    - **Cost** 
        * Optimize and reduce your overall Azure spending
    - **Operational Excellence**
        * Achieve process and workflow efficiency, resource manageability and deployment best practices.
    
## Azure Monitor

* **Azure Monitor** colects, analyzes and acts on telemetry from your cloud and on-premises environments
* With **Azure Monitor** you can understand how your apps are performing and proactively identify issues affecting them and the resources they depend on
* **Azure Monitor** will monitor your cloud environment and then perform different functions such as analysis, alerting and streaming to external systems.
* Create smart alerts and automated actions.
* Monitor resources and drill into monitoring data with Azure Log Analytics
* Detect and diagnose issues across applications and dependencies with Application Insights
* Create visualizations with Azure Dashboards


## Azure Service Health

* Actually combination 3 separate smaller services
    - **Azure Status**
        * Informs you of service outages in Azure. Service impacting events, planned maintenance activities and any other changes that may affect apps availability.
        * Global view of the health of all Azure services across all Azure regions
        * Represents a global view
    - **Azure Service Health**
        * Provides a personalized view of the health of the Azure services and regions you're using
        * You may want to configure Service Health alerts to be notified of any service issues, planned maintenance or changes in Azure
    - **Azure Resource Health**
        * Provides information about the health of your individual cloud resources
        * You can combine Azure Resource Health usage with Azure Monitor, in order to configure alerts to be notified of any availability changes of your cloud resources.
        * All together, Azure Status, Azure Service Health and Azure Resource Health, provide a comprehensive view into the health Azure in general and your resources particularly.

# References