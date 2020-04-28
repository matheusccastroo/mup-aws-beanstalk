# @hubroeducation/mup-aws-beanstalk Fork

As we have not received any reply for our forks and issues in the main repository, we have published a fork to add in our extensions and updates

- Updated dependencies
- Add ability to include extra files into instances
- Support for custom ebextensions config files (by @s7dhansh, https://github.com/zodern/mup-aws-beanstalk/pull/72)
- Support for different deployment policies
- Fixes for hangups on SSL

### Extra feautres

#### Custom files
```
// Add to mup config

additionalFiles: [
  {
    //Adds "mylog.log" to the logs that are tailed and exported in elastic beanstalk
    filepath: "/opt/elasticbeanstalk/tasks/taillogs.d/mylog.conf",
    content: [
      "/var/log/mylog.log*"
    ]
  },
]
```

#### Set deployment policy


```
// add to mup config

"deploymentPolicy": "Rolling"
```



## mup-aws-beanstalk

Plugin for Meteor Up to deploy using AWS Beanstalk.

Features:
- Load balancing with support for sticky sessions and web sockets
- Autoscaling
- Meteor settings.json
- Zero downtime deploys
- Automatically uses the correct node version

[Getting Started Guide](./docs/getting-started.md)

[Documentation](./docs/index.md)
