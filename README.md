# Company Shares Outstanding Viewer

This is a single-page responsive web application built with HTML, Tailwind CSS, and JavaScript. It fetches and displays the maximum and minimum common stock shares outstanding for a given company from the U.S. Securities and Exchange Commission (SEC) API, focusing on data from 2021 onwards.

## Features

-   **Dynamic Data Fetching**: Retrieves company shares outstanding data directly from the SEC's XBRL API.
-   **Max/Min Shares Display**: Clearly highlights the highest and lowest shares outstanding values and their corresponding fiscal years.
-   **Responsive Design**: Utilizes Tailwind CSS for a modern, mobile-friendly interface.
-   **CIK Parameter Support**: Easily switch between companies by providing a Central Index Key (CIK) in the URL.

## Getting Started

To run this application, simply open the `index.html` file in your web browser.

### Default Company (Boeing)

By default, the application loads data for **Boeing (BA)**, CIK `0000012927`.

### Viewing Data for Other Companies

You can view data for any other publicly traded company by appending its 10-digit CIK to the URL as a query parameter.

**Example:**

To view data for Apple Inc. (CIK: `0000320193`), open the following URL in your browser:

`index.html?CIK=0000320193`

The page will automatically update with Apple's shares outstanding data without requiring a reload.

## Technical Details

-   **SEC API Endpoint**: `https://data.sec.gov/api/xbrl/companyconcept/`
-   **CORS Proxy**: `https://api.allorigins.win/raw?url=` is used to bypass Cross-Origin Resource Sharing (CORS) restrictions for client-side API calls.
-   **User-Agent Compliance**: The application attempts to set a descriptive `User-Agent` header as per SEC guidance (`BoeingApp/1.0 (contact@boeing.com)`). However, due to browser security policies, client-side JavaScript cannot directly override the `User-Agent` header sent by the browser. If deploying this behind a server-side proxy, ensure the proxy adds the appropriate `User-Agent`.

## Project Structure

-   `index.html`: The main single-file responsive web application.
-   `README.md`: This documentation file.
-   `LICENSE`: The MIT License for this project.

## Note on `uid.txt`

The prompt mentioned an attachment named `uid.txt`. However, its content was not provided, and the requested output format is strictly a JSON object containing `index.html`, `README.md`, and `LICENSE` as string values. Therefore, `uid.txt` could not be included or committed as a separate file within this JSON output.