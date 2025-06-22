# 🦠 UiPath COVID Statistics Notepad Writer

This UiPath automation opens a browser, searches for COVID-19 statistics for a selected country, retrieves the numbers, and writes them into Notepad in a structured format.

---

## 📌 Features

- Dynamically searches for any country's COVID-19 statistics
- Uses dynamic selectors based on the `country` variable
- Extracts:
  - Total cases
  - Deaths
  - Recovered cases
- Writes formatted results into Notepad
- Ensures no duplicate writes (resolves `Type Into` being triggered twice)
- Makes country names uppercase in output

---

## 🧩 Workflow Overview

1. **Input**: Country name (e.g., `"Egypt"`)
2. **Dynamic Selector**:
    ```vb
    "<webctrl aaname='" + country + " COVID - Coronavirus Statistics' parentid='rso' tag='SPAN' type='' class='' />"
    ```
3. **Data Extraction**: Retrieves text using `Get Text`
4. **Text Formatting**:
    ```vb
    "Corona Viurs Information about " & country.ToUpper & " Country" & vbCrLf &
    "Coronavirus Cases: " & Coronavirus_Cases & vbCrLf &
    "Deaths: " & Deaths & vbCrLf &
    "Recovered: " & Recovered & vbCrLf & vbCrLf
    ```
5. **Write to Notepad**:
   - Uses `Type Into` or `Set To Clipboard + Ctrl+V` to avoid typing errors
   - Ensures the message is only typed once

---

## 🚀 Getting Started

### Prerequisites
- UiPath Studio
- Chrome/Edge browser extension for UiPath (if browser automation is involved)

### How to Use
1. Open the project in UiPath Studio
2. Update the `country` variable to your desired country (e.g., "India", "France")
3. Run the workflow

---

## 🧠 Author

Yasmin Kadry  
🔗 [LinkedIn](https://www.linkedin.com/in/yasmin-kadry/)  

