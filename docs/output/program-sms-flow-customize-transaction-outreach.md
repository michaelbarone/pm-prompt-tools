# Program Proposal Template

*Updated: $(Get-Date -Format "yyyy-MM-dd HH:mm")*

## Initial Prompt

### Program Name
SMS Flow Customize Transaction Outreach

### Elevator Pitch
We want to improve the customization of SMS outreach flows by enabling triggers based on transaction types. This enhancement will eliminate the need for hard-coded logic in the POS engine, reducing maintenance complexity and increasing system reliability. By allowing the location to customize what transactions result in certain sms outreach to customers allows finer control over guest relations, in addition to allowing Edge to ingest/process ALL customer transactions for analytics and other feature use where currently transactions are dropped(not stored) if the location does not want to trigger customer outeach. This is having impact on certain Scoreboard competitions where they do not want customer outeach but do want to track that transaction for competitions.

## Primary Motivation
<!-- Select ONE of the following by removing the [ ] and adding [X] -->
- [ ] Market Expansion: Attract new businesses to Edge and expand market reach
- [ ] User Activation: Help new businesses quickly discover value and become engaged
- [X] User Retention: Deepen adoption and reduce churn among existing Edge users
- [ ] Revenue Growth: Increase revenue through upsells or new revenue streams
- [ ] Operational Efficiency: Save time or reduce costs by improving tools/processes
- [ ] Risk Mitigation: Minimize security, compliance, performance, or reliability threats
- [ ] Maintenance: Essential fixes, updates, and housekeeping

## Impact Assessment

### Internal Impact

#### Primary Edge Beneficiary Group
<!-- Select ONE of the following by removing the [ ] and adding [X] -->
- [ ] Engineering Team
- [ ] Product Team
- [ ] Sales Team
- [ ] Customer Success
- [ ] Marketing Team
- [ ] Operations Team
- [ ] Leadership Team
- [X] All Teams

#### Edge Employee Impact
<!-- Select ONE option from each category -->

**Number of Employees Affected:**
- [ ] 1-5 employees
- [ ] 6-20 employees
- [ ] 21-50 employees
- [X] 51-100 employees
- [ ] 101-200 employees
- [ ] 201-500 employees
- [ ] 500+ employees

**Average Impact Level:**
- [ ] Minimal: Minor workflow improvements
- [ ] Low: Noticeable but small efficiency gains
- [X] Medium: Significant workflow improvements
- [ ] High: Major productivity/satisfaction boost
- [ ] Critical: Transformative impact on daily work

### External Impact

#### Primary External Beneficiary Group
<!-- Select ONE of the following by removing the [ ] and adding [X] -->
- [ ] All Customers
- [X] Business
- [X] Employees
- [ ] Consumers (guests)
- [ ] NA

#### External Impact Metrics
<!-- Select ONE option from each category -->

**Percentage of Group Affected:**
- [ ] 1-10%
- [ ] 11-25%
- [X] 26-50%
- [ ] 51-75%
- [ ] 76-90%
- [ ] 91-100%

**Average Impact Level:**
- [ ] Minimal: Slight improvement in experience
- [X] Low: Noticeable but small benefit
- [X] Medium: Clear and valuable improvement
- [ ] High: Significant value addition
- [ ] Critical: Essential improvement

## Problem Statement

### Current Problem
<!-- Provide 1-2 paragraphs describing the problem you are seeking to solve -->
```
Currently, we have no ability to customize Location Flows to send customer outreach based on different transaction types.  Every transaction we recieve will result in an attempt to send customer outreach (provided we have the required data and the guest is outside of any set frequency restrictions), which means the only way for us to not send guest outreach post visit is to disable all location flows (not ideal), or we drop (exclude from ingesting) certain transaction which does fulfill the requirement to not send guest outreach however, we lose that transaction information, meaning we cannot use that transaction in other features like scoreboard, or any analytics we could offer to the customer.

Additionally, in order to faciliate excluding transaction types, we need to hard code this logic in our POS Engine, resulting in deployments of code to make configuration changes for customers.  We really should not have any deciding logic like this in the POS Enginer, we should ingest ALL transactions it recieves for matching location in our system.  Any additional logic beyond that adds complexity and changes expectation for data availability which also makes troubleshooting some issues harder as not all location data is expected to work the same based on customer need (which may not be documented).

```

1. **Specific Pain Points**:
   - Customization is hard-coded, leading to increased maintenance efforts and decreased flexibility for customers. This rigidity limits the ability of customers to tailor SMS outreach to their specific needs and preferences.

2. **Current Limitations**:
   - The existing system does not allow customers to customize outreach for their guests effectively. This limitation hinders the ability to provide personalized experiences.
   - Transactions are often dropped, resulting in incomplete data sets. This affects the quality of analytics and the ability to leverage full data for future features and insights.
   - The support burden is increased due to the complexity of investigating issues related to customization. By limiting where customizations can occur, the program aims to reduce potential downstream issues and streamline support processes.



## Objectives and Success Metrics

### External Beneficiary Objectives
- Objective 1: Enable customers to customize SMS outreach for their guests, enhancing personalization.
- Objective 2: Improve data completeness by ingesting all transactions, leading to better analytics and feature development.

### Internal Beneficiary Objectives
- Objective 1: Reduce maintenance complexity by eliminating hard-coded logic.
- Objective 2: Decrease support burden by streamlining customization processes.

### Key Results (Success Metrics)
1. Increase in customer satisfaction scores by 20% within the first year.
2. Reduction in support tickets related to customization issues by 30%.
3. Improvement in data analytics accuracy by 25% due to complete transaction data.

## Solution Planning

### Possible Solutions

#### Solution 1: Dynamic Customization Engine
- Description: Develop a dynamic engine that allows customers to define SMS outreach rules based on transaction types.
- Pros: High flexibility, improved customer satisfaction.
- Cons: Requires significant initial development effort.
- Estimated Effort: High

#### Solution 2: Enhanced Data Ingestion
- Description: Implement a system to ingest all transaction data, regardless of outreach triggers.
- Pros: Complete data sets for analytics, improved feature development.
- Cons: May increase data storage requirements.
- Estimated Effort: Medium

## Risk Assessment

### Assumptions and Validations

#### Market Viability
- Assumption: Customers desire more control over SMS outreach customization.
- Validation: Conduct surveys and gather feedback from key customer segments.
- Confidence: High

#### User Desirability
- Assumption: Enhanced customization will lead to increased customer engagement.
- Validation: Monitor engagement metrics post-implementation.
- Confidence: Medium

#### Technical Feasibility
- Assumption: The current system can be adapted to support dynamic customization.
- Validation: Perform a technical feasibility study and prototype development.
- Confidence: Medium

#### Operational Impact
- Build Cost: Estimated at $500,000, justified by potential increase in customer retention and satisfaction.
- Maintenance Cost: Estimated at $50,000 annually, justified by reduced support burden.
- Resource Requirements: Development team, data analysts, customer support specialists.
