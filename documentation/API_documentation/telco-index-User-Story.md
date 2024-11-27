**User Story: Credit scoring service for banking**
<br>

| Item                      | Description | Support Qualifier |
|---------------------------|-------------|-------------------|
| Summary                   |             | M                 |
| Roles, Actor(s) and scope |             | M                 |
| NF Requirements           |             | O                 |
| Pre-conditions            |             | M                 |
| Begins when               |             | M                 |
| Step 1                    |             | (M/O/CM)          |
| Step 2                    |             | (M/O/CM           |
| ...                       |             | (M/O/CM)          |
| Step N                    |             | (M/O/CM)          |
| Ends when                 |             | M                 |
| Post-conditions           |             | M                 |
| Exceptions                |             | M                 | 

| **Item** | **Details** |
| -------- | ----------- |
| ***Summary*** | As a bank officer, I want to evaluate a micro-credit application for a customer who has no credit history within our bank. I use the Telco Index API to gather additional information about the customer's telco behavior to assess their creditworthiness. |
| ***Roles, Actors and Scope*** | **Roles:** Customer:User<br> **Actors:** Bank Officer, Bank System, Communication Service Provider (CSP)<br> **Scope:** Retrieve a relevant score calculated from the data of the CSP, enabling the bank to make an informed decision on micro-credit approval. |
| ***Pre-conditions*** | The preconditions are listed below:<br><ol><li>The bank is integrated with the CSP's Telco Index API.</li><li>The customer has consented to sharing their telco data for credit assessment purposes.</li><li>The bank officer has the necessary credentials to access the Telco Index API.</li></ol> |
| ***Activities/Steps*** | **Begins when:** The bank officer submits a micro-credit application for a customer without an existing credit history.<br><br>**Steps include:**<br><ol><li>The bank system makes a request to the Telco Index API using customer consented information.</li><li>The CSP processes the request and gathers telco-related behavioral insights.</li><li>The CSP sends a calculated score to the bank system.</li><li>The bank officer evaluates the score to assess the credit risk of the customer.</li></ol><br> **Ends when:** The bank officer either approves or declines the micro-credit application based on the insights provided. |
| ***Post-conditions*** | The bank officer has sufficient data to approve or deny the micro-credit request for a customer without a traditional credit history. |
| ***Exceptions*** | Several exceptions might occur during the Customer Insights API operations:<br>- Unauthorized: Invalid credentials provided by the bank system.<br>- Consent missing: The customer has not provided consent for sharing telco data (i.e. permission denied).<br>- Data not found: Insufficient user data available for the customer.<br>- Corporate customers: The API is not applicable for corporate customers. |


**User Story: Credit scoring service for riders**
<br>

| **Item** | **Details** |
| -------- | ----------- |
| ***Summary*** | As a service provider, I want to evaluate the creditworthiness of riders working for food delivery, errands, and other similar applications. I use the Credit Insights API to generate a score for these riders, which can be used by companies and banks to offer credit services to the riders for purchasing a motorcycle, bicycle, or electric scooter. The application can leverage the Telco Index API to complement the score generated with additional telco data, enhancing the overall credit score. |
| ***Roles, Actors and Scope*** | **Roles:** Customer:User<br> **Actors:** Service Provider, Bank System, Rider, Application Service Provider (ASP), Communication Service Provider (CSP)<br> **Scope:** Retrieve relevant behavioral data about the riders from both the delivery apps and the CSP, enabling a comprehensive credit score calculation to support credit decisions for vehicle purchases. |
| ***Pre-conditions*** | The preconditions are listed below:<br><ol><li>The service provider is integrated with both the delivery applications and the CSP's Telco Index API.</li><li>The rider has consented to share their delivery and telco data for credit assessment purposes.</li><li>The service provider has the necessary credentials to access Telco Index API and the path to route to the right CSP.</li></ol> |
| ***Activities/Steps*** | **Begins when:** The service provider initiates a credit assessment for a rider interested in purchasing a vehicle (motorcycle, bicycle, or electric scooter).<br><br>**Steps include:**<br><ol><li>The service provider collects rider activity data from the delivery applications, including job completion rates, earnings, and overall performance.</li><li>The service provider makes a request to the Telco Index API using the collected data and rider consent details.</li><li>The CSP processes the request and generates a preliminary credit score based on the rider's delivery activities.</li><li>The service provider then makes a request to the Telco Index API to retrieve additional telco-related score about the rider.</li><li>The CSP processes the request and gathers telco-related behavioral insights.The CSP sends a final enhanced credit score to the service provider, which combines both delivery app data and telco insights.</li><li>The service provider evaluates the received score to assess the rider's creditworthiness for purchasing a vehicle. **Ends when:** The service provider either approves or declines the credit application based on the insights provided. |
| ***Post-conditions*** | The service provider has sufficient data to approve or deny the credit request for a rider based on a comprehensive score derived from both delivery app activity and telco data. |
| ***Exceptions*** | Several exceptions might occur during the Telco Index API operations:<br>- Unauthorized: Invalid credentials provided by the service provider.<br>- Consent missing: The rider has not provided consent for sharing delivery or telco data (i.e. permission denied).<br>- Data not found: Insufficient data available from delivery apps or telco records for the rider.<br>- Corporate customers: The API is not applicable for corporate customers. |