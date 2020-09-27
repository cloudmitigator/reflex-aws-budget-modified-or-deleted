# reflex-aws-budget-modified-or-deleted
A Reflex rule for detecting the modification or deletion of an AWS Budget.

To learn more about AWS Budgets, see [the AWS Documentation](https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/budgets-managing-costs.html).

## Getting Started
To get started using Reflex, check out [the Reflex Documentation](https://docs.cloudmitigator.com/).

## Usage
To use this rule either add it to your `reflex.yaml` configuration file:  
```
rules:
  aws:
    - budget-modified-or-deleted:
        version: latest
```

or add it directly to your Terraform:  
```
module "budget-modified-or-deleted" {
  source            = "git::https://github.com/reflexivesecurity/reflex-aws-budget-modified-or-deleted.git?ref=latest"
  sns_topic_arn     = module.central-sns-topic.arn
  reflex_kms_key_id = module.reflex-kms-key.key_id
}
```

Note: The `sns_topic_arn` and `reflex_kms_key_id` example values shown here assume you generated resources with `reflex build`. If you are using the Terraform on its own you need to provide your own valid values.

## Configuration
This rule has no configuration options.

## Contributing
If you are interested in contributing, please review [our contribution guide](https://docs.cloudmitigator.com/about/contributing.html).

## License
This Reflex rule is made available under the MPL 2.0 license. For more information view the [LICENSE](https://github.com/reflexivesecurity/reflex-aws-budget-modified-or-deleted/blob/master/LICENSE) 
