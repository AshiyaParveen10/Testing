[Sysdig Secure](https://www.sysdig.com/products/platform){target=`_blank`} is an AI-powered Application Security Platform that helps organizations:
testing now
* Identify and prioritize real risks
* Detect, investigate, and respond to real-time threats
* Get unified visibility and eliminate siloes

Integrating with Sysdig Secure enables you to **receive vulnerability, compliance, and identity findings via the Seemplicity Platform.**

## Prerequisites
To integrate your Sysdig Secure setup, you'll need to provide your **API Server URL** and **Access Token** to Seemplicity. You can review the official documentation site [here](https://docs.sysdig.com/en/docs/sysdig-secure/){target=`_blank`}.

:::(Warning) (your title goes here)
To access the Vulnerability Engine in Sysdig Secure, you must be credentialed as a user with at least [Advanced User](https://docs.sysdig.com/en/docs/administration/administration-settings/user-and-team-administration/manage-teams-and-roles/#:~:text=team%20member%20permissions.-,Advanced%20User%3A,-In%20Sysdig%20Monitor) permissions.
:::

* To obtain your **API Server URL**, review the SaaS Regions and IP Ranges [topic](https://docs.sysdig.com/en/administration/saas-regions-and-ip-ranges/#sysdig-platform-regions){target=`_blank`}.
* To obtain your **Sysdig API (Access) Token**, review their official documentation [here](https://docs.sysdig.com/en/administration/retrieve-the-sysdig-api-token/){target=`_blank`}.
* **Copy and save** these data points for setup in the Seemplicity platform.
   
## Add an Instance

1. In Seemplicity, go to **Settings** > **Integrations - Data Sources** >  **Sysdig Secure** > **Integrate**.
2. In the **Name** field, enter a descriptive name for this instance.
3. In the **API Server URL** and **Access Token** fields, paste the values you saved from Sysdig Secure.
4. For each type of finding that you want Seemplicity to collect, select its **respective checkbox**. You can select **Collect Host Vulnerabilities**, **Collect Container Vulnerabilities**, **Collect Container Image Vulnerabilities**, and/or **Collect CSPM Findings**.
    :::(Info) (Collect CSPM Findings)
    This single checkbox collects all three Sysdig posture families: cloud posture (CSPM), Kubernetes posture (KSPM), and host configuration benchmarks. They arrive in Seemplicity as three separate finding types.
    :::
5. In the Collection Settings,
    1. Select the **enabled toggle**.
    3. Select **when to collect data** (daily or weekly) and **time**.
6. In the Automatic Resolution Settings, enter values (in number of days) for **Last Reported Time** and **Last Collected Time.**  
     :::(Warning) (Important)
     Seemplicity uses Last Collected Time and Last Reported Time to relate to when we collect data from data sources and when the third party records a finding. Set your Last Collected Time value to a number that is **equal or less than** the Last Reported Time.
     :::
7. When finished, select **Save**.
