# Siteknower Viewer for Crystal Reports 

## Description
Siteknower is simple web service solution to deliver Crystal Reports to your web browser.

It is intended for developers who use Crystal Reports in their web or desktop solutions.

Users of your software solution do not need to have Crystal Reports installed, nor the runtime or any other files and libraries otherwise required to run Crystal Reports.

## Usage
First, log in to our website https://www.siteknower.com to get your AccountCode and UserCode

The key file is StnwService.dll for desktop or StnwServiceWeb.dll for web solutions.
Put that file in the bin/debug folder for your desktop solution, or in the bin folder on the server for your web solution.

For a desktop solution, the rpt file is located anywhere on the local drive, and for the web, place it anywhere on the server.

**web application:**
```bash
using StnwServiceWeb;
...
protected void btnPrint_Click(object sender, EventArgs e)
 {
     clsStnwClassWeb tsi = new clsStnwClassWeb();
     tsi.dsRPT = dst;   // your dataset
    
     tsi.preslAccountCode = "DEMO1";  // your account code
     tsi.preslUserCode = "0000";  // your user code
     tsi.ReportFullName = "C:/MyReports/CustomerReport1.rpt";

     tsi.ShowWindow(this, HttpContext.Current);
 }
```
**desktop application:**
```bash
using StnwService;
...
      private void Button1_Click(object sender, EventArgs e)
        {
            clsStnwClass tsi = new clsStnwClass();
            tsi.dsRPT = dsCustomers;   // your dataset
       
            tsi.preslAccountCode = "DEMO1";  // your account code
            tsi.preslUserCode "0000";  // your user code
            tsi.RPTDEST = 0;
            tsi.ReportFullName = "C:/MyReports/CustomerReport1.rpt";;

            tsi.ShowForm();
        }
```
## Features
- uses a dataset and rpt file to display the report
- Feature 2
- Feature 3

## Table of Contents
1. [Installation](#installation)
2. [Usage](#usage)
3. [Contributing](#contributing)
4. [License](#license)
5. [Acknowledgments](#acknowledgments)

## Installation
1. Step 1
2. Step 2
3. Step 3

## Ack
```bash
Laku noć
This is the first line.  
This is the second line.
```

## Usage
```bash
# Example command
```

### Tips
- Use Markdown for formatting.
- Keep it concise but informative.
- Use clear and simple language.
- Update your README as your project evolves.

Feel free to modify this structure to suit your project's needs!

## Licence
Copyright © 2024-* Adacco, ltd.

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software, associated images, and associated documentation files (the
“Software”), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE
LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION
OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION
WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
