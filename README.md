# DiscussionHive: https://www.discussionhive.com/

![discussionhive](https://user-images.githubusercontent.com/6800366/41781477-4a02c790-7655-11e8-9ebc-511321771298.PNG)

* Website is hosted on a t2.micro instance. Wordpress has been installed here.
* Word press uses a MySQL DB to store the installed plugins, user comments, users information and other details. This is hosted on MYSQL managed by AWS RDS.
* This website's images are stored in AWS S3.
* For better Geo-latency, I am making use of a CDN by AWS: **CloudFront**. All requests to fetch images are routed to cloud front first which inturn fetches the image from S3 and store the images on the nearest edge locations.
* Cloud Front endpoint has been made secure by using the **AWS certificate manager**.
* The website itself has been made secure by using HTTPS protocol using the Let's Encrypt SSL provider.
