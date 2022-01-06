# NewRelic::Alerts::NrqlAlert Term

## Syntax

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON

<pre>
{
    "<a href="#duration" title="Duration">Duration</a>" : <i>Integer</i>,
    "<a href="#operator" title="Operator">Operator</a>" : <i>String</i>,
    "<a href="#priority" title="Priority">Priority</a>" : <i>String</i>,
    "<a href="#threshold" title="Threshold">Threshold</a>" : <i>Double</i>,
    "<a href="#timefunction" title="TimeFunction">TimeFunction</a>" : <i>String</i>
}
</pre>

### YAML

<pre>
<a href="#duration" title="Duration">Duration</a>: <i>Integer</i>
<a href="#operator" title="Operator">Operator</a>: <i>String</i>
<a href="#priority" title="Priority">Priority</a>: <i>String</i>
<a href="#threshold" title="Threshold">Threshold</a>: <i>Double</i>
<a href="#timefunction" title="TimeFunction">TimeFunction</a>: <i>String</i>
</pre>

## Properties

#### Duration

This is the time (in minutes) for the condition to persist before triggering an event.

_Required_: No

_Type_: Integer

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### Operator

This determines what comparison will be used between the ValueFunction and the Threshold value to trigger an event.

_Required_: No

_Type_: String

_Allowed Values_: <code>above</code> | <code>below</code> | <code>equal</code>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### Priority

This corresponds to the severity level selected when setting the Threshold values.

_Required_: No

_Type_: String

_Allowed Values_: <code>critical</code> | <code>warning</code>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### Threshold

This is the threshold that the ValueFunction must be compared to using the Operator for an event to be triggered.

_Required_: No

_Type_: Double

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### TimeFunction

This corresponds to the Threshold values.

_Required_: No

_Type_: String

_Allowed Values_: <code>all</code> | <code>any</code>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

