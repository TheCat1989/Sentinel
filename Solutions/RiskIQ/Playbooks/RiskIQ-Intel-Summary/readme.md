# RiskIQ-Intel-Summary

## Overview
This playbook uses the RiskIQ PassiveTotal connector to automatically enrich incidents generated by Microsoft Sentinel. RiskIQ intelligence provides analyst with deeper context around vulnerabilities, threat actors, their campaigns or other noteworthy context found from analyzing the Internet. Analysts can leverage this playbook to add context to indicators found within incidents. Each comment added to the incident will link to a more detailed intelligence card from RiskIQ.

## Prerequisites
This playbook inherits API connections created and established within a base playbook. Ensure you have deployed [RiskIQ-Base](https://raw.githubusercontent.com/Azure/Azure-Sentinel/master/Solutions/RiskIQ/Playbooks/RiskIQ-Base/azuredeploy.json) prior to deploying this playbook. You will need your API credentials (email/secret) when configuring that playbook. Those can be found on your [account settings](https://community.riskiq.com/settings) page. For enterprise customers, it's preferred to use the "organization" credential pair, not the user. If you have trouble accessing your account or your credentials contact your account representative (support[@]riskiq.com).

## Deployment

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FAzure%2FAzure-Sentinel%2Fmaster%2FSolutions%2FRiskIQ%2FPlaybooks%2FRiskIQ-Intel-Summary%2Fincident-trigger%2Fazuredeploy.json" target="_blank">
    <img src="https://aka.ms/deploytoazurebutton"/>
</a>
<a href="https://portal.azure.us/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FAzure%2FAzure-Sentinel%2Fmaster%2FSolutions%2FRiskIQ%2FPlaybooks%2FRiskIQ-Intel-Summary%2Fincident-trigger%2Fazuredeploy.json" target="_blank">
    <img src="https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/deploytoazuregov.png"/>
</a>

### Post-Deployment Instructions
After deploying the playbook, you must authorize the connections leveraged.

1. Visit the playbook resource.
2. Under "Development Tools" (located on the left), click "API Connections".
3. Ensure each connection has been authorized.

**Note: If you've deployed the [RiskIQ-Base](https://raw.githubusercontent.com/Azure/Azure-Sentinel/master/Solutions/RiskIQ/Playbooks/RiskIQ-Base/azuredeploy.json) playbook, you will only need to authorize the Microsoft Sentinel connection.**