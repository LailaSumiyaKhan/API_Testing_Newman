# Running Postman Collection with Newman and Generating Reports with htmlextra

This guide explains how to run the provided Postman collection using Newman and generate an HTML report using the `newman-reporter-htmlextra` package.

## Prerequisites

Make sure you have the following installed:

1. [Node.js](https://nodejs.org/)
2. [Postman](https://www.postman.com/) (for exporting collections if needed)
3. Newman:
   ```bash
   npm install -g newman
   ```
4. htmlextra reporter:
   ```bash
   npm install -g newman-reporter-htmlextra
   ```

## Steps to Run the Collection

### 1. Save the Collection File
Save the provided JSON collection file as `practice-evershop.postman_collection.json` in your project directory.

### 2. Command to Run the Collection
Use the following Newman command to execute the collection and generate the HTML report:

```bash
newman run practice-evershop.postman_collection.json \
```

### 3. Generate HTML Report
```bash
newman run practice-evershop.postman_collection.json -r htmlextra
```

### 4. View the Report
After the command completes, an HTML report named `newman-report.html` will be generated in the current directory. Open this file in a browser to view the detailed test results.

## Notes
- Make sure the collection contains all required variables like `product_name`, `product_sku`, etc.
- The environment file should contain any necessary tokens or configurations.

## Report Preview

### Summary
![summary](report_preview/summary.png)

![requests](report_preview/requests.png)


