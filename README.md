[![Build Status](https://travis-ci.com/ckaserer/travis-template.svg?branch=master)](https://travis-ci.com/ckaserer/travis-template)
![GitHub](https://img.shields.io/github/license/ckaserer/travis-template)
![Maintenance](https://img.shields.io/maintenance/yes/2020)

<p align="center">
<img alt="logo" width=250px src="https://travis-ci.com/images/logos/TravisCI-Full-Color.png">
</p>

# travis-template

A github repository template to create new repos with travis notifications. Slack notifications are enabled on failure / Mail notifications are disabled.

## First Steps

1) replace each occurance of travis-template in the badge definition with the new repository name.
2) Update your secure slack token. The travis encryption is repo based and won't work for another repo.

---

## Useful tips

### Slack Notifications

#### Bold does not work
`*bold text*` does make your text bold in 

```yaml
notifications: 
  slack: 
    template:
```
  
#### Best way to define your token

**Do not** put your secure token right underneath slack like `slack: secure:`. Otherwise you can't specify any customization.

```yaml
notifications:
  slack: 
    rooms: 
      - secure: 
```
  
### eMail Notifications

#### Deactivate Mails
Mail Notifications can only be deactivated within `.travis.yml` and hove to be deactivated per repository. There is no global setting.
  