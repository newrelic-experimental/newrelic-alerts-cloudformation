# NewRelic::Alerts::NrqlAlert Nrql

## Syntax

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON

<pre>
{
    "<a href="#query" title="Query">Query</a>" : <i>String</i>,
    "<a href="#sincevalue" title="SinceValue">SinceValue</a>" : <i>Integer</i>
}
</pre>

### YAML

<pre>
<a href="#query" title="Query">Query</a>: <i>String</i>
<a href="#sincevalue" title="SinceValue">SinceValue</a>: <i>Integer</i>
</pre>

## Properties

#### Query

This is the NRQL query that New Relic Alerts monitors as part of a NRQL condition.

_Required_: No

_Type_: String

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### SinceValue

This is the time (in minutes) for the condition to persist before triggering an event.

_Required_: No

_Type_: Integer

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

