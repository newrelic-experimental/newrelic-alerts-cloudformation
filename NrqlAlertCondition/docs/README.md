# NewRelic::Alerts::NrqlAlert

Resource schema to create a NewRelic NRQL-based Alert

## Syntax

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON

<pre>
{
    "Type" : "NewRelic::Alerts::NrqlAlert",
    "Properties" : {
        "<a href="#apikey" title="ApiKey">ApiKey</a>" : <i>String</i>,
        "<a href="#policyid" title="PolicyId">PolicyId</a>" : <i>Integer</i>,
        "<a href="#nrqlcondition" title="NrqlCondition">NrqlCondition</a>" : <i><a href="nrqlcondition.md">NrqlCondition</a></i>
    }
}
</pre>

### YAML

<pre>
Type: NewRelic::Alerts::NrqlAlert
Properties:
    <a href="#apikey" title="ApiKey">ApiKey</a>: <i>String</i>
    <a href="#policyid" title="PolicyId">PolicyId</a>: <i>Integer</i>
    <a href="#nrqlcondition" title="NrqlCondition">NrqlCondition</a>: <i><a href="nrqlcondition.md">NrqlCondition</a></i>
</pre>

## Properties

#### ApiKey

A New Relic REST API Key

_Required_: Yes

_Type_: String

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### PolicyId

Identifier of the New Relic Alert Policy

_Required_: Yes

_Type_: Integer

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### NrqlCondition

_Required_: Yes

_Type_: <a href="nrqlcondition.md">NrqlCondition</a>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

