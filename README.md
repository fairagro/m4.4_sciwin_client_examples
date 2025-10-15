# SciWIn Client Examples
This repo provides all [SciWIn Client](https://github.com/fairagro/m4.4_sciwin_client) Examples from the [Documentation](https://fairagro.github.io/m4.4_sciwin_client/).

## [Getting started example](https://github.com/fairagro/m4.4_sciwin_client_demo_basic/tree/complete_run)
The getting started example is the most basic example provided with SciWIn Client. It creates a simple two-step-workflow without using containerization. It is made to get familiar with the basic capabilities of the `create` and `connect` commands.
<details><summary>Preview Workflow</summary>
<img src="https://raw.githubusercontent.com/fairagro/m4.4_sciwin_client_demo_basic/complete_run/workflow.svg" alt="workflow"/>
</details>

## [Advanced example](https://github.com/fairagro/m4.4_sciwin_client_demo/tree/complete_run)
The advanced example provides a real world use case using data from the german elections 2025 for the city of brunswick. Herein containerization is used and it is much more focused on how a real project will look like compared to the basic example. The workflow is a complex multiple-step operation which is built in two iterations.
<details><summary>Preview Workflow</summary>
<img src="https://raw.githubusercontent.com/fairagro/m4.4_sciwin_client_demo/complete_run/workflow_final.svg" alt="workflow"/>
</details>

## [Corn Prediction](https://github.com/fairagro/m4.4_demo_corn_prediction/tree/run)
This example demonstrates the usage of `s4n`  through a simplified crop yield prediction pipeline that combines soil and weather data to train models and generate county-level yield predictions for Iowa.
<details><summary>Preview Workflow</summary>
<img src="https://raw.githubusercontent.com/fairagro/m4.4_demo_corn_prediction/main/workflow.svg" alt="workflow"/>
</details>

## [Automated Metrics](https://github.com/fairagro/m4.4_metrics)
An Example Repo where the SciWin-Client Team does collect metrics about the SciWIn-Client by using a Workflow created by SciWin-Client. This Workflow is executed on a regular basis using GitHub Actions.
<details><summary>Preview Workflow</summary>

```mermaid
---
config:
  theme: base
  look: neo
  themeVariables:
    primaryColor: '#C5E0B4'
    primaryTextColor: '#231f20'
    secondaryColor: '#EEEEEE'
    lineColor: '#385723'    
    fontSize: 12px
    tertiaryTextColor: '#231f20'
    fontFamily: 'Fira Sans, trebuchet ms, verdana, arial'
---
flowchart TB
  linkStyle default stroke:#385723,stroke-width: 2px;
  subgraph inputs[Workflow Inputs]
    direction TB
    token(token)
  end
  subgraph outputs[Workflow Outputs]
    direction TB
    raw_data(raw_data)
    analyzed_data(analyzed_data)
    badge(badge)
    platform(platform)
    readme(readme)
    release(release)
  end
    collect(collect)
  token --> |token|collect
    analyze(analyze)
  collect --> |json|analyze
    announce(announce)
  analyze --> |json|announce
  collect --> |raw_data|raw_data
  analyze --> |analyzed_data|analyzed_data
  analyze --> |badge|badge
  analyze --> |platform|platform
  announce --> |readme|readme
  analyze --> |release|release
  style inputs fill:#EEEEEE,stroke-width:2px;
  style token stroke:#0f9884,fill:#6FC1B5,stroke-width:2px;
  style outputs fill:#EEEEEE,stroke-width:2px;
  style raw_data stroke:#823909,fill:#F8CBAD,stroke-width:2px;
  style analyzed_data stroke:#823909,fill:#F8CBAD,stroke-width:2px;
  style badge stroke:#823909,fill:#F8CBAD,stroke-width:2px;
  style platform stroke:#823909,fill:#F8CBAD,stroke-width:2px;
  style readme stroke:#823909,fill:#F8CBAD,stroke-width:2px;
  style release stroke:#823909,fill:#F8CBAD,stroke-width:2px;
  style collect stroke:#385723,stroke-width:2px;
  style analyze stroke:#385723,stroke-width:2px;
  style announce stroke:#385723,stroke-width:2px;
```

</details>

## Coming soon
...
