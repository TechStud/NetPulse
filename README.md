# NetPulse - Real-time Latency Visualizer

NetPulse is a sophisticated, browser-based utility for real-time application-layer network latency monitoring. It provides a rich, graphical, per-second timeline of application-layer round-trip times (RTT) to _any_ web host, complete with continuous statistics and an intuitive network path visualization.

## Features

- **Real-time Timeline Graph:** A color-coded, interactive sparkline graph visualizes latency for each minute of the monitoring session.
- **Dynamic Network Path Visualizer:** An animated, at-a-glance view of the network path from your device, through your gateway and the internet, to the target host.
- **Live Statistics:** Per-minute and aggregate statistics including Min, Avg, Max latency, and packet loss.
- **Configurable Monitoring:** Set the target host, duration, monitoring frequency (requests per second), and latency thresholds.
- **Light & Dark Themes:** Automatically detects system preference and allows manual toggling.
- **Data Export:** Export session data and visuals to PNG, PDF, CSV, or XLSX for analysis and reporting.
- **Shareable Sessions:** Easily share/bookmark a pre-configured monitoring session via a unique URL.
- **No Installation Required:** Lightweight and runs entirely in your web browser.

## Technology Stack

NetPulse is a modern, client-side web application built with:

- **React:** For building the user interface.
- **TypeScript:** For type safety and improved code quality.
- **Tailwind CSS:** For styling and a responsive design.

## How to Run

Modern web browsers have security policies that prevent JavaScript modules from loading correctly when you open an `index.html` file directly from your local disk (i.e., using a `file:///` path). To run NetPulse, you _may_ need to serve the files using a simple local web server.

Here are two easy, cross-platform ways to do this:

### Option 1: Using Python (Recommended)

If you have Python 3 installed, this is the simplest method.

1.  Open a terminal or command prompt.
2.  Navigate to the directory where you have the `index.html` file and other project files.
3.  Run the following command:
    ```bash
    python3 -m http.server 8080
    ```
    (If you have an older Python 2 installation, you might need to use `python -m SimpleHTTPServer`).
4.  Open your web browser and navigate to: **http://localhost:8080**

### Option 2: Using Node.js / npx

If you have Node.js and npm installed, you can use the `serve` package.

1.  Open a terminal or command prompt.
2.  Navigate to the directory where you have the `index.html` file.
3.  Run the following command:
    ```bash
    npx serve
    ```
4.  The command will output a local address, typically **http://localhost:3000**. Open this URL in your web browser.


## ⚠️ Security Notice

**This tool is intended for internal, diagnostic, and personal use only.**

It should **NOT** be hosted on a public-facing web server! The application makes direct network requests from the user's browser, and hosting it publicly could be misinterpreted or misused. It is designed to be run in a trusted, local environment.

## System Requirements

- **Operating System:** OS Agnostic (Windows, macOS, Linux).
- **Browser:** A modern, up-to-date web browser with JavaScript enabled.
- **Network:** An active internet connection.
