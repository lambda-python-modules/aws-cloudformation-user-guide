# AWS::SES::ReceiptRuleSet<a name="aws-resource-ses-receiptruleset"></a>

The `AWS::SES::ReceiptRuleSet` resource specifies an empty rule set for Amazon SES\. For more information, see [CreateReceiptRuleSet](https://docs.aws.amazon.com/ses/latest/APIReference/API_CreateReceiptRuleSet.html) in the *Amazon Simple Email Service API Reference*\. 

**Topics**
+ [Syntax](#aws-resource-ses-receiptruleset-syntax)
+ [Properties](#aws-resource-ses-receiptruleset-properties)
+ [Return Values](#aws-resource-ses-receiptruleset-returnvalues)
+ [Example](#aws-resource-ses-receiptruleset-examples)
+ [See Also](#aws-resource-ses-receiptruleset-seealso)

## Syntax<a name="aws-resource-ses-receiptruleset-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ses-receiptruleset-syntax.json"></a>

```
{
  "Type" : "AWS::SES::ReceiptRuleSet",
  "Properties" : {
    "[RuleSetName](#cfn-ses-receiptruleset-rulesetname)" : String
  }
}
```

### YAML<a name="aws-resource-ses-receiptruleset-syntax.yaml"></a>

```
Type: "AWS::SES::ReceiptRuleSet"
Properties:
  [RuleSetName](#cfn-ses-receiptruleset-rulesetname): String
```

## Properties<a name="aws-resource-ses-receiptruleset-properties"></a>

`RuleSetName`  <a name="cfn-ses-receiptruleset-rulesetname"></a>
The name of the rule set to create\. The name must:  
+ Contain only ASCII letters \(a\-z, A\-Z\), numbers \(0\-9\), underscores \(\_\), or dashes \(\-\)\.
+ Start and end with a letter or number\.
+ Contain less than 64 characters\.
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## Return Values<a name="aws-resource-ses-receiptruleset-returnvalues"></a>

### Ref<a name="aws-resource-ses-receiptruleset-ref"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Example<a name="aws-resource-ses-receiptruleset-examples"></a>

### <a name="aws-resource-ses-receiptruleset-example1"></a>

#### JSON<a name="aws-resource-ses-receiptruleset-example1.json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Description": "AWS SES ReceiptRuleSet Sample Template",
    "Parameters": {
        "ReceiptRuleSetName": {
            "Type": "String"
        }
    },
    "Resources": {
        "ReceiptRuleSet": {
            "Type": "AWS::SES::ReceiptRuleSet",
            "Properties": {
                "RuleSetName": {
                    "Ref": "ReceiptRuleSetName"
                }
            }
        }
    }
}
```

#### YAML<a name="aws-resource-ses-receiptruleset-example1.yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: 'AWS SES ReceiptRuleSet Sample Template'
Parameters:
  ReceiptRuleSetName:
    Type: String
Resources:
  ReceiptRuleSet:
    Type: AWS::SES::ReceiptRuleSet
    Properties:
      RuleSetName: !Ref ReceiptRuleSetName
```

## See Also<a name="aws-resource-ses-receiptruleset-seealso"></a>
+ [Creating Receipt Rules for Amazon SES Email Receiving](https://docs.aws.amazon.com/ses/latest/DeveloperGuide/receiving-email-receipt-rules.html) in the *Amazon Simple Email Service Developer Guide*
+ [CreateReceiptRuleSet](https://docs.aws.amazon.com/ses/latest/APIReference/API_CreateReceiptRuleSet.html) in the *Amazon Simple Email Service API Reference*