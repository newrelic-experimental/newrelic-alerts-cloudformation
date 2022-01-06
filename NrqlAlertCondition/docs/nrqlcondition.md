# NewRelic::Alerts::NrqlAlert NrqlCondition

## Syntax

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON

<pre>
{
    "<a href="#enabled" title="Enabled">Enabled</a>" : <i>Boolean</i>,
    "<a href="#expectedgroups" title="ExpectedGroups">ExpectedGroups</a>" : <i>Integer</i>,
    "<a href="#id" title="Id">Id</a>" : <i>Integer</i>,
    "<a href="#ignoreoverlap" title="IgnoreOverlap">IgnoreOverlap</a>" : <i>Boolean</i>,
    "<a href="#name" title="Name">Name</a>" : <i>String</i>,
    "<a href="#nrql" title="Nrql">Nrql</a>" : <i><a href="nrql.md">Nrql</a></i>,
    "<a href="#runbookurl" title="RunbookUrl">RunbookUrl</a>" : <i>String</i>,
    "<a href="#terms" title="Terms">Terms</a>" : <i>[ <a href="term.md">Term</a>, ... ]</i>,
    "<a href="#type" title="Type">Type</a>" : <i>String</i>,
    "<a href="#valuefunction" title="ValueFunction">ValueFunction</a>" : <i>String</i>,
    "<a href="#violationtimelimitseconds" title="ViolationTimeLimitSeconds">ViolationTimeLimitSeconds</a>" : <i>Integer</i>
}
</pre>

### YAML

<pre>
<a href="#enabled" title="Enabled">Enabled</a>: <i>Boolean</i>
<a href="#expectedgroups" title="ExpectedGroups">ExpectedGroups</a>: <i>Integer</i>
<a href="#id" title="Id">Id</a>: <i>Integer</i>
<a href="#ignoreoverlap" title="IgnoreOverlap">IgnoreOverlap</a>: <i>Boolean</i>
<a href="#name" title="Name">Name</a>: <i>String</i>
<a href="#nrql" title="Nrql">Nrql</a>: <i><a href="nrql.md">Nrql</a></i>
<a href="#runbookurl" title="RunbookUrl">RunbookUrl</a>: <i>String</i>
<a href="#terms" title="Terms">Terms</a>: <i>
      - <a href="term.md">Term</a></i>
<a href="#type" title="Type">Type</a>: <i>String</i>
<a href="#valuefunction" title="ValueFunction">ValueFunction</a>: <i>String</i>
<a href="#violationtimelimitseconds" title="ViolationTimeLimitSeconds">ViolationTimeLimitSeconds</a>: <i>Integer</i>
</pre>

## Properties

#### Enabled

This is the status of your alert condition and is optional. The default is false.

_Required_: No

_Type_: Boolean

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### ExpectedGroups

This is the number of groups you expect to see at any given time. It is used in combination with the OpenViolationOnGroupOverlay option.

_Required_: No

_Type_: Integer

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### Id

Condition ID Returned from NewRelic

_Required_: No

_Type_: Integer

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### IgnoreOverlap

If disabled, New Relic looks for a convergence of groups. If the condition is looking for 2 or more groups, and the returned values cannot be separated into that number of distinct groups, then that will also produce a violation.

_Required_: No

_Type_: Boolean

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### Name

This is a title for your condition and will allow you identify it in the New Relics Alerts UI.

_Required_: No

_Type_: String

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### Nrql

_Required_: No

_Type_: <a href="nrql.md">Nrql</a>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### RunbookUrl

URL to display in notifications.

_Required_: No

_Type_: String

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### Terms

_Required_: No

_Type_: List of <a href="term.md">Term</a>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### Type

This defines the type of metric that will be used for the alert.

_Required_: No

_Type_: String

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### ValueFunction

Function to be applied to the Threshold values.

_Required_: No

_Type_: String

_Allowed Values_: <code>single_value</code> | <code>sum</code>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### ViolationTimeLimitSeconds

Use to automatically close instance-based violations after the number of seconds specified.

_Required_: No

_Type_: Integer

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

