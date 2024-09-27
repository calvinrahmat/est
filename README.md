Vikram Request

Have crossed checked the project that was migration to Bitbucket, seems okay at repository branches and commit histories. But, would request to check on the below areas as well before migrate everything. These are important key aspects from Development Operations.

1. Push Rules:
- We have JIRA project key in push rule to restrict the commits.
- The rule is in regix format, may be check how those can be migrated in Bitbucket.

3. Protected Branches:
- development, release, hotfix and master are key protected branches.
- These branches must be protected from delete operation.
- release and hotfix branches are mandatory to review and approve by minimum of 1 approver (lead)
- master branch is mandatory to review & approve by minimum of 1 approver (lead) and merge should be done by us (DevOps)
- There may be workflow cycle for pushing the source code e.g. feature -> development -> release -> master

4. Repository Mirror
- All the External Bitbucket project should have mirror link to synch on internal bitbucket.
- If possible can restrict with Specific branches mirroring.

5. Protected Tags:
- Protected tags are enabled for some projects, so pls see how to migrate those as well.
- If possible, protected tags can be enabled in generic pattern with standard naming.

6. Merge Approvals
- Currently, we have a rule minimum of one approver accept the merge request for release, hotfix and master branches where those are important branches.
- As mentioned above, we as (DevOps) part of second level approver / restricted to evaluate the request.

7. Users and Groups
- Users are to be migrated with respect to project or group as per GITLAB.
- If possible, create a project group to tag the users to simply the access.
- GITLAB AD group must be tagged in Bitbucket and users are able to access by setting 2FA.
- We found today, user license to be added in order to login by them.

8. Webhooks
- GITLAB was established with SSH to checkout the source at Jenkins Server to build. So, pls setup webhook to avoid Jenkins pipeline break up.
- Help us on the Bitbucket URL update in Jenkins as this is needed.
- Also, share us the plugin that is required for Jenkins to communicate with Bitbucket.
