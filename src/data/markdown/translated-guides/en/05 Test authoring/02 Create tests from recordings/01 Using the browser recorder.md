---
title: 'Using the browser recorder'
excerpt: 'The browser recorder allows generating a k6 script based on a web session. It is available as extensions for Chrome and Firefox.'
---

The browser recorder lets you generate a k6 script based on a browser session.
It's available as an extension for [Chrome](https://chrome.google.com/webstore/detail/grafana-k6-browser-record/fbanjfonbcedhifbgikmjelkkckhhidl) and [Firefox](https://addons.mozilla.org/en-US/firefox/addon/grafana-k6-browser-recorder/).


## Before you start


Before you start, consider the following:

- [Be sure to record realistically](/test-authoring/create-tests-from-recordings/#be-sure-to-record-realistically)
- [A hybrid approach for load testing websites](/test-authoring/create-tests-from-recordings/#consider-hybrid-approach-for-load-testing-websites)

> Note that the browser recorders **do not require a cloud account**. For cloud users, check out the [Grafana Cloud](https://grafana.com/docs/grafana-cloud/k6/author-run/browser-recorder/) and [k6 Cloud](/cloud/creating-and-running-a-test/browser-recorder/) instructions.

## How to record

1. Install the [Chrome](https://chrome.google.com/webstore/detail/grafana-k6-browser-record/fbanjfonbcedhifbgikmjelkkckhhidl) or [Firefox](https://addons.mozilla.org/en-US/firefox/addon/grafana-k6-browser-recorder/) extension.
1. Open the extension by clicking the k6 logo.
2. Choose where to save the auto-generated script.
   - To save it on your local machine, select **I don't want to save tests in the cloud**. 
   - To save it on any of your Grafana Cloud k6 projects, select **Sign In**.
3. Select **Start recording** to begin recording the current browser tab. 
4. When done, select **Stop recording**.
5. Save the recorded script locally or in any of your cloud projects.
6. Edit your script as necessary. Depending on the [type of load test](/test-types/load-test-types/), you might need to change different aspects of the script. 
   Typical changes are for [load options](/using-k6/options) and to handle [correlation and dynamic data](/examples/correlation-and-dynamic-data).
7. Run the test from the CLI or Grafana Cloud k6. For more about running k6, refer to the [Running k6 guide](/get-started/running-k6).

## Troubleshooting. Try the HAR converter


If you experience problems recording a request, try the [HAR converter](/test-authoring/create-tests-from-recordings/using-the-har-converter/). 

The Browser recorder uses the HAR converter under the hood.
Like the Browser Recorder, the HAR converter creates a k6 script from the HTTP requests included in a HAR file.
 
The HAR converter can also record other tabs or pop-up windows, which the Browser Recorder cannot. 

If the error persists with the HAR converter, please provide detailed information about the problem [in a new issue](https://github.com/k6io/har-to-k6/issues). 
