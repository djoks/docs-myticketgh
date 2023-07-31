---
description: API configuration values
---

# Configuration

This page provides essential information about the configuration settings required to interact with our API successfully. Here, you'll find the three key environment variables necessary for seamless integration: **Host**, **API Version**, and **Base URL**. Understanding and correctly setting these values are crucial to ensure smooth communication with our API.

**Definitions:**

1. **Host:** The "Host" environment variable specifies the domain name or IP address where our API is located. It acts as the entry point to our API server, allowing your application to establish a connection and make requests.
2. **API Version:** The "API Version" environment variable defines the specific version of our API that your application should communicate with. API versions ensure backward compatibility and allow us to introduce new features without breaking existing implementations.
3. **Base URL:** The "Base URL" environment variable represents the starting point for constructing API requests. It combines the "Host" and "API Version" to form the foundation of the API endpoints used in your application.

You can seamlessly integrate your application with our API and access its full functionalities by correctly configuring these environment variables. Refer to the documentation for further guidance on setting up and utilizing these values to maximize the potential of our API.

| Name      | Value                      |
| --------- | -------------------------- |
| HOST      | https://api.myticketgh.com |
| VERSION   | v1                         |
| BASE\_URL | {HOST}/{VERSION}/          |

