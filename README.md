## Overview

This project is a Python script that automates the extraction of names using an autocomplete API. It systematically queries the API and retrieves names, ensuring that the maximum number of possible names are collected and stored efficiently.

## Approach

### Version 1 (v1)

* Initially, I started by testing the API with simple queries like a, followed by other letters and combinations.

* I observed that the maximum number of results returned per request was 10.

* The API had a rate limit of 100 requests per minute.

* The results were returned in JSON format.

* Based on these observations, I wrote a Python script to automate the extraction process.

* Script created for testing/exploration script.ipynb

### Search Algorithm

* Implemented Breadth-First Search (BFS) to ensure that the script explores all possible name prefixes efficiently.

* If an API request returned the maximum number of names (10 in v1), it indicated more names could exist with extended prefixes.

* The script then recursively added new characters to the prefix and continued searching.

* Names were collected and saved in a JSON file for easy retrieval.

## Version Updates

### Version 2 (v2)

* The API was updated to support names containing digits (0-9).

* I observed that the maximum number of results returned per request was 12.

* The API had a rate limit of 50 requests per minute.

* Modified the script to include digits in the prefix search space.

* Adjusted the request handling to maintain efficiency.

* Script created for testing/exploration script2.ipynb

### Version 3 (v3)

* The API further evolved to include lowercase letters (a-z), digits (0-9), and special characters (+, -, ., and spaces).

* Updated the character set to include +, -, .,and spaces in addition to letters and numbers.

* I observed that the maximum number of results returned per request was 15.

* Ensured proper URL encoding to handle spaces in API queries.

* Maintained BFS traversal to extract the maximum possible names.

* Script created for testing/exploration script.ipynb

## Features

* Automated name extraction using BFS
* Handles rate limits and retries failed requests
* Saves extracted names in a JSON file
* Supports latest API updates with extended character set