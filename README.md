## psdemo-js-live-workflow
A demo workflow that builds an end-to-end live channel with MediaLive, MediaPackage, and CloudFront services.


## Setup
#### Environment Variables
    export AWS_REGION=eu-west-1
    export AWS_ACCESS_KEY_ID=<YOUR_ACCESS_KEY>
    export AWS_SECRET_ACCESS_KEY=<YOUR_ACCESS_SECRET>

#### Sample code
    const Backend = require('psdemo-js-live-workflow');
    /* create MediaPackage channel */
    (() => {
      Backend.MediaPackageChannel(event, context, (e, data) => {
        console.log(e, JSON.stringify(data, null, 2));
      });
    })();

    /* create MediaLive channel */
    (() => {
      Backend.MediaLiveChannel(event, context, (e, data) => {
        console.log(e, JSON.stringify(data, null, 2));
      });
    })();
