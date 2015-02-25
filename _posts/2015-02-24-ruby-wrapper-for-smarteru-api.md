---
layout: post
title: Ruby Wrapper For SmarterU API
comments: true
author: sasha
p-category: Back End Development
---

# Ruby Wrapper For SmarterU API
![EyeCue Lab]({{ site.postimage }}smarteru.jpg)


Just released a Ruby wrapper for the SmarterU API that we have used on one of our Rails projects. Allows performing operations within a SmarterU account. This library constructs the xml post request with credentials and your json input parameters, makes an API call and returns a json after parsing the xml response.

SmarterU is online training platform with a bunch of learning management features from e-learning course creator to SCORM compliance to executive dashboards and reporting.

<br>
### Basic ruby library usage

API wrapper can be used from the command line or as part of some Ruby web framework. First install the gem:

    gem install smarteru

Instantiate a client with your SmarterU credentials. You can get it [here](http://smarteru.com/)

    require 'smarteru'
    client = Smarteru::Client.new(account_api_key: "ACCOUNT_API_KEY", user_api_key: "USER_API_KEY")

Make api calls. You can find a list of API endpoints [here](http://help.smarteru.com/)

    response = client.request('getGroup', {group: {name: 'MyGroup'}})
    response.result =>
      {
        group: {
          name: "MyGroup",
          group_id: nil,
          created_date: "2015-01-22 23:42:55.553",
          modified_date: "2015-01-23 01:25:02.013",
          description: {
            p: "Group Description ..."
          },
          home_group_message: {
            p: "Welcome to The Group"
          },
          notification_emails: nil,
          user_count: "2",
          learning_module_count: "2",
          tags: nil,
          status: "Active"
        }
      }


### Testing

    bundle install
    rake


Available [here](https://github.com/eyecuelab/labnotebook) and on rubygems.org
