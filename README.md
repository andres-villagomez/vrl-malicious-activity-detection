# VRL Malicious Activity Detection Functions

## Overview

This project is designed to detect various forms of malicious activity using [Vector](https://vector.dev) and Vector Remap Language (VRL). The project includes VRL scripts that are integrated into a main Vector configuration file to monitor and detect suspicious activities such as:

- Port scanning
- Access by forbidden IP addresses
- Unauthorized file access by specific roles
- Multiple failed login attempts

## Project Structure

- **`vector-main.yml`**: The main Vector configuration file that integrates all the VRL scripts.
- **`vrl-malicious_activity_detection_functions/`**: (Optional) Contains individual VRL scripts for each detection function. This folder may be deleted after integration.

## VRL Scripts

The following VRL scripts are included and integrated into the `vector-main.yml`:

1. **Port Scanning Detection**
   - Detects port scanning activities based on the number of different ports accessed.

2. **Forbidden IP Address Detection**
   - Flags any access attempts from a list of known bad IP addresses.

3. **Unauthorized Role Access Detection**
   - Monitors file access events and flags unauthorized role access to sensitive files.

4. **Multiple Failed Login Attempts Detection**
   - Detects multiple failed login attempts within a short period.

## Setup and Configuration

### 1. Prerequisites

- **Vector**: Ensure that Vector is installed on your system. You can install Vector by running the following command:
  ```bash
  curl -fsSL https://sh.vector.dev | sh