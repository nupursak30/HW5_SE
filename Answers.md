__Solution 1)__  

_Advantages of using Configuration Management tools_
  1. Using Configuration tools can help the developer to greatly reduce developer's testing time so that they can spend more time on improving the quality of the code. This is because configuration management tools helps to automate test cases so now the developer can avoid writing the test cases for each change. 
  2. Developers can use the tools to carry out the task of creating new application bundles repeatedly with consistency. 
  3. Configuration management tools help the developers to efficiently manage the project management lifeccyle through the means of automation.

_Problems with using Configuration Management tools_
1. Configuration management tools are complex to understand and implement for someone who doesn't have any idea about these tools. So, if someone doesn't have a good idea about these tools and they try to implement it directly, it may result into an increase in their debugging and troubleshooting tasks instead of reducing it.
2. Even small error/inappropriate change in the configuration of these tools have the power to bring down the entire application, thereby increasing the number of precautions to be taken while configuring these tools.
3. Security becomes one of the major concerns when dealing with configuration management tools as these tools deal with automatic handling of the whole application program testing and releases, so configuration of such tools need to be secure and reliable.


__Solution 2)__
1. _Continuous Intergration:_[[1](https://www.atlassian.com/continuous-delivery/ci-vs-ci-vs-cd)]
    1. Continuous Integration simply means merging all the changes to the main branch as frequently as possible. Validation of these changes takes place via running automated test cases against the build. This helps to reduce merging code issues to a greater extent as it keeps a check on the applications and makes sure that it doesn't break whenever new commits are being converged with the main branch.
    2. Continuous Integration helps to reduce developer's testing time and thus, help them to spend more time on improving the code.

2.  _Continuous Delivery:_[[1](https://www.atlassian.com/continuous-delivery/ci-vs-ci-vs-cd)]
    1. After doing continuous integration, the next step is to go ahead and do continuous delivery. Continuous delivery makes sure that all the new changes made to the systems/applications are being released/delivered to the users as quickly as possible.Continuous Delivery achieves this by automating the release process after we have automated the testing process using continuous integration, thereby allowing us to deploy the user application at any point of time by clicking few buttons. 
    2. So, theoretically applications can be released at any time but it is always a good practice to deploy to production as early as possible as it will always be easy to troubleshoot and solve problems which may be caused by releases of small patches instead of dealing with all the problems at one time during the final release.

3. _Continuous Deployment:_[[1](https://www.atlassian.com/continuous-delivery/ci-vs-ci-vs-cd)]
    1. Continuous Deployment is the next step which comes after Continuous Delievery. With Continuous Deployment, every new change which has cleared all the test cases and stages of the production pipeline, is automatically released to the customers. So Continuous Deployment is similar to Continuous Delivery but the only difference is that the new changes are being automatically released to the users.
    2. This helps to develop applications at a faster rate as now there is no need to pause development for releases since they are getting released automatically to the users.
