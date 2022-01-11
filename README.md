[![New Relic Experimental header](https://github.com/newrelic/opensource-website/raw/master/src/images/categories/Experimental.png)](https://opensource.newrelic.com/oss-category/#new-relic-experimental)

![GitHub forks](https://img.shields.io/github/forks/newrelic-experimental/newrelic-alerts-cloudformation?style=social)
![GitHub stars](https://img.shields.io/github/stars/newrelic-experimentalnewrelic-alerts-cloudformation?style=social)
![GitHub watchers](https://img.shields.io/github/watchers/newrelic-experimental/newrelic-alerts-cloudformation?style=social)

![GitHub all releases](https://img.shields.io/github/downloads/newrelic-experimental/newrelic-alerts-cloudformation/total)
![GitHub release (latest by date)](https://img.shields.io/github/v/release/newrelic-experimental/newrelic-alerts-cloudformation)
![GitHub last commit](https://img.shields.io/github/last-commit/newrelic-experimental/newrelic-alerts-cloudformation)
![GitHub Release Date](https://img.shields.io/github/release-date/newrelic-experimental/newrelic-alerts-cloudformation)

![GitHub issues](https://img.shields.io/github/issues/newrelic-experimental/newrelic-alerts-cloudformation)
![GitHub issues closed](https://img.shields.io/github/issues-closed/newrelic-experimental/newrelic-alerts-cloudformation)
![GitHub pull requests](https://img.shields.io/github/issues-pr/newrelic-experimental/newrelic-alerts-cloudformation)
![GitHub pull requests closed](https://img.shields.io/github/issues-pr-closed/newrelic-experimental/newrelic-alerts-cloudformation)

# newrelic-alerts-cloudformation
This repository provides an AWS CloudFormation Resource for creating or updating New Relic NRQL Alerts from a CloudFormation Stack.

This documentation assumes fluency in both NRQL Alerts and CloudFormation.

## Installation
- [Setup your environment for developing CloudFormation extensions](https://docs.aws.amazon.com/cloudformation-cli/latest/userguide/what-is-cloudformation-cli.html). At a minimum do this for Java as it's needed here.
- Ensure you have at least Java 8 installed
- Ensure you have the current version of Maven installed
- Clone this repository
- `cd` into the cloned repository directory
- Run `mvn clean package` 
- `cd` into `NrqlAlertCondition`
- To install the `NewRelic::Alerts::NrqlAlert` Resource into AWS as a privately registered extension run
  - `cfn submit --region <YOUR_REGION_HERE> --set-default`
  - You can validate the success of this operation by looking at the `CloudFormation > Registry: Activated extensions` console![](.images/Activated%20Extensions.png). Select the `Resource types` tab and set the drop down to `Privately registered`. If everything worked as it should you'll see the `NewRelic::Alerts::NrqlAlert` resource listed there.

At this point the Resource is ready for use in your Stacks.

## Usage
- See [create-alert.yaml](yaml/create-alert.yaml) for a sample of how to use the Resource.
- [The full schema for the Resource is here](NrqlAlertCondition/newrelic-alerts-nrqlalert.json).
- [The Alerts conditions API field names](https://docs.newrelic.com/docs/alerts-applied-intelligence/new-relic-alerts/advanced-alerts/rest-api-alerts/alerts-conditions-api-field-names/) is also helpful

### Trouble shooting
- If Stack creation fails first check the `CloudFormation > Stacks` console for your Stack. The `Status reason` column of the `Events` tab may have some helpful information.
- Next try the `CloudWatch > Log groups > newrelic-alerts-nrqlalert-logs` console ![](.images/CloudWatch%20Logs.png) for the current `Log events`. There you should find a detailed error message.
- Once in a while a bad Alert definition will not successfully roll back. When that happens go into the CloudWatch console, manually delete the Stack, and then `update-stack`.

## Developer Notes
- To install a new version of the Resource into CloudFormation
  - `mvn clean package`
  - `cfn submit --region <YOUR_REGION_HERE> --set-default`
- To test the Resource `create` or `update` the Stack
  - `aws cloudformation update-stack --region <YOUR_REGION_HERE> --template-body "file://yaml/create-alert.yaml" --stack-name <YOUR_COOL_STACK_NAME_HERE>`

### Helpful Links
- [CloudFormation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/Welcome.html)
- [CloudFormation CloudWatch Alarm](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cw-alarm.html)
- [CloudFormation CLI](https://docs.aws.amazon.com/cloudformation-cli/latest/userguide/what-is-cloudformation-cli.html)

### Dire warnings
- [Do not use this blog post as a guide/reference](https://newrelic.com/blog/how-to-relic/create-alerts-aws-cloudformation) as it points the Resource at the original, broken, zip file.
## Support

New Relic has open-sourced this project. This project is provided AS-IS WITHOUT WARRANTY OR DEDICATED SUPPORT. Issues and contributions should be reported to the project here on GitHub.

We encourage you to bring your experiences and questions to the [Explorers Hub](https://discuss.newrelic.com) where our community members collaborate on solutions and new ideas.

## Contributing
We encourage your contributions to improve newrelic-alerts-cloudformation! Keep in mind when you submit your pull request, you'll need to sign the CLA via the click-through using CLA-Assistant. You only have to sign the CLA one time per project. If you have any questions, or to execute our corporate CLA, required if your contribution is on behalf of a company, please drop us an email at opensource@newrelic.com.

**A note about vulnerabilities**

As noted in our [security policy](../../security/policy), New Relic is committed to the privacy and security of our customers and their data. We believe that providing coordinated disclosure by security researchers and engaging with the security community are important means to achieve our security goals.

If you believe you have found a security vulnerability in this project or any of New Relic's products or websites, we welcome and greatly appreciate you reporting it to New Relic through [HackerOne](https://hackerone.com/newrelic).

## License
newrelic-alerts-cloudformation is licensed under the [Apache 2.0](http://apache.org/licenses/LICENSE-2.0.txt) License.

newrelic-alerts-cloudformation also uses source code from third-party libraries. You can find full details on which libraries are used and the terms under which they are licensed in the third-party notices document.
