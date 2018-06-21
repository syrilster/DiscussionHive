# DiscussionHive: https://www.discussionhive.com/

* Website is hosted on a t2.micro instance. This is where the wordpress installation is present.
* Word press uses a MySQL DB to store the plugins, comments, users and other details. This is hosted on RDS.
* The website images are stored in S3.
* For better Geo-latency, we are using a CDN by AWS: CloudFront. All requests to fetch images are routed to cloud front which store the images on the nearest edge locations.
* Cloud Front endpoint has been made secure by the AWS certificate manager.
* The website is made secure by using HTTPS protocol using the Let's Encrypt SSL provider.
