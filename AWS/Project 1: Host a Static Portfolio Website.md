# Static Portfolio Website

## Overview
This project involves hosting a static portfolio website using AWS services. The website is built with React and deployed using Amazon S3, Route 53, and CloudFront.

## Demo
You can view the live demo of the portfolio website here: [http://reactapp.divijjain.rocks/](http://reactapp.divijjain.rocks/)

## Services Used
- **Amazon Route 53**: Domain registration and DNS management.
- **Amazon S3**: Storage for the static website assets.
- **Amazon CloudFront**: Content delivery network (CDN) for faster delivery of the website.

## Setup and Deployment

1. **Domain Registration:**
   - Register a domain using Amazon Route 53.
   
2. **Build React Application:**
   - Build the React application using `npm run build`. This generates a `build` folder with static files.

3. **Upload to S3:**
   - Create an S3 bucket.
   - Upload the contents of the `build` folder (index.html, JavaScript files, CSS files, images, etc.) to the S3 bucket.

4. **Configure S3 Bucket:**
   - Set up the S3 bucket to host a static website. 
   - Enable static website hosting in the bucket properties.
   - Set the index document and error document as needed (e.g., `index.html`).

5. **Link Domain to S3:**
   - Set up an alias or CNAME record in Route 53 to point your domain to the S3 bucket endpoint.

6. **Configure CloudFront:**
   - Create a CloudFront distribution.
   - Set the S3 bucket as the origin for the distribution.
   - Configure caching and distribution settings as needed.
   - Update the Route 53 DNS records to use the CloudFront distribution’s domain name.

## Additional Notes
- Ensure that the S3 bucket policy allows public read access to the website files.
- Use CloudFront to enable HTTPS for secure access to the website.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
