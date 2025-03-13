# MS Defender Vulnerability Management PowerBI Template - Usage Guide

## Overview

This PowerBI template provides a comprehensive vulnerability management dashboard for Microsoft Defender Vulnerability Management. The template includes pre-built visualizations, data models, and calculated measures to help security teams monitor, prioritize, and remediate vulnerabilities effectively.

## Getting Started

### Prerequisites

- **PowerBI Desktop**: Download the latest version from [Microsoft's website](https://powerbi.microsoft.com/desktop/)
- **Microsoft Defender for Endpoint** subscription with Vulnerability Management capabilities
- **API Access**: Permissions to access Microsoft Defender API endpoints

### Installation

1. Download the MS_Defender_Vulnerability_Management.pbit file
2. Double-click the file to open it in PowerBI Desktop
3. When prompted, provide the API endpoint URL for your Microsoft Defender environment
4. The template will load with sample data initially

## Connecting to Your Data

### API Connection Setup

1. In PowerBI Desktop, go to **Home** > **Transform data**
2. Select the data source connection and click **Edit**
3. Update the API endpoint URL to your Microsoft Defender environment:
   - US: `https://api.securitycenter.microsoft.com/api`
   - EU: `https://eu.api.securitycenter.microsoft.com/api`
   - UK: `https://uk.api.securitycenter.microsoft.com/api`
4. Configure authentication using your organization's credentials
5. Apply the changes and refresh the data

### Authentication

The template supports the following authentication methods:

- **OAuth2**: Recommended for most organizations
- **API Key**: If your organization uses API keys for authentication
- **Service Principal**: For automated/scheduled refreshes

## Dashboard Navigation

The template includes four main dashboards:

### 1. Overview Dashboard

Provides a high-level summary of your vulnerability posture, including:
- Exposure Score
- Microsoft Secure Score for Devices
- Vulnerability severity distribution
- Top vulnerable devices
- Remediation progress

### 2. Vulnerability Details Dashboard

Offers detailed information about specific vulnerabilities:
- Vulnerability counts by severity
- Age distribution
- Exploitable vulnerabilities
- Detailed vulnerability table
- CVSS score distribution

### 3. Device Exposure Dashboard

Focuses on device-specific vulnerability information:
- Device exposure levels
- OS platform vulnerability distribution
- Device details
- Software compliance status

### 4. Remediation Tracking Dashboard

Helps track and manage remediation activities:
- Mean Time to Remediation
- Remediation status distribution
- Timeline and progress tracking
- SLA compliance metrics

## Using the Filters

Each dashboard includes the following interactive filters:

1. **Date Range Slicer**: Filter data by time period
2. **Severity Filter**: Focus on specific vulnerability severity levels
3. **Device Group Filter**: Filter by organizational units or device groups
4. **Search Box**: Find specific devices, CVEs, or software

## Calculated Measures

The template includes several pre-built calculated measures:

- **Average Time To Action**: Average time between vulnerability detection and remediation start
- **Mean Time To Remediation**: Average time to complete vulnerability remediation
- **Vulnerability Age**: Average age of open vulnerabilities
- **Total Risk Score**: Weighted risk score based on vulnerability severity
- **Remediated Risk Score**: Risk score of remediated vulnerabilities

## Customization

### Adding Custom Visuals

1. Go to the dashboard you want to modify
2. Click the **+ Add visual** button in the Visualizations pane
3. Select the visual type and configure it with your data

### Creating Custom Measures

1. Go to **Modeling** tab
2. Click **New Measure**
3. Write your DAX expression
4. Name and format your measure

### Modifying Existing Visuals

1. Click on the visual you want to modify
2. Use the Visualization and Fields panes to adjust settings
3. Right-click for additional formatting options

## Scheduling Data Refresh

To keep your dashboard up-to-date:

1. Publish the report to PowerBI Service
2. Go to **Dataset Settings**
3. Configure **Scheduled Refresh**
4. Set the frequency based on your security monitoring needs

## Troubleshooting

### Common Issues

1. **API Connection Errors**:
   - Verify API endpoint URL is correct
   - Check authentication credentials
   - Confirm API permissions are properly set

2. **Performance Issues**:
   - Limit date ranges for faster loading
   - Consider implementing incremental refresh
   - Optimize DAX measures if needed

3. **Data Discrepancies**:
   - Verify data transformation steps
   - Check for filtering that might exclude data
   - Ensure all measures are calculating correctly

## Support and Resources

- **Microsoft Defender Documentation**: [Microsoft Defender Vulnerability Management](https://learn.microsoft.com/en-us/defender-vulnerability-management/)
- **PowerBI Documentation**: [PowerBI Learning Resources](https://learn.microsoft.com/en-us/power-bi/)
- **API Reference**: [Microsoft Defender API Documentation](https://learn.microsoft.com/en-us/defender-endpoint/api/get-all-vulnerabilities)

## Version Information

- **Template Version**: 1.0
- **Last Updated**: March 13, 2025
- **Compatible With**: Microsoft Defender for Endpoint Plan 2, Microsoft Defender XDR
