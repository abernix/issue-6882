# [meteor/meteor#6882](https://github.com/meteor/meteor/issue/6882)
Auth0 sample app with Meteor 1.3
Thanks to **@mitiaptest** for originally creating this repo.  This has been updated to use my (test) credentials.

#### Steps to Reproduce (on OS X)

##### Clone
    git clone <this repo>

##### Make `meteor.local` resolve on your (entire) local network
(Run this in its own terminal and keep it running)

    dns-sd -P meteor _http._tcp "" 80 meteor.local <YOUR_HOST_IP>

##### Run Meteor
    ROOT_URL=http://meteor.local:3000 meteor run ios-device --port 0.0.0.0:3000 --settings settings.json --mobile-server http://meteor.local:3000

##### Try Logging In!
* **Username:** funnybunny2@mailinator.com
* **Password:** Password123

**Allowed Callback URLs:** http://meteor.local:3000/_oauth/auth0

**Allowed CORS** http://meteor.local:3000/