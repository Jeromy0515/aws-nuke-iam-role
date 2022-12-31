# Delete IAM Role and IAM Policy with aws-nuke

## Set Configuration

---
1. Install *aws-nuke* to reference **this [releases page](https://github.com/rebuy-de/aws-nuke/releases/tag/v2.21.2)**
2. Copy `config.yml` file  into the project directory
3. Change `<Account ID>` to your account id in `config.yml`
4. Config credentials profile with IAM User who got admin permission
```
$ aws configure
AWS Access Key ID [****************ABCD]: Access Key
AWS Secret Access Key [****************ABCD]: Secret Access Key
```
5. Create iam account alias, If not created
```
$ aws iam create-account-alias --account-alias <example>
```


## Usage
run aws-nuke using this command
```
$ aws-nuke -c config.yml
```

but *aws-nuke* only lists all found resources and exits.
This is because `--no-dry-run` flag is missing.
So if you delete resources actually, add `--no-dry-run`.
```
$ aws-nuke -c config.yml --no-dry-run
```










