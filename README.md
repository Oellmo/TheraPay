# TheraPay

A simple desktop application built with [Neutralino.js](https://neutralino.js.org/) to help manage and track open invoices.



## ✨ Features

- **Dashboard Overview**: Get a quick summary of key metrics like total open invoice amounts and the number of open invoices.
- **Excel Data Import**: Easily import and process invoice data from a structured Excel file. The app supports drag-and-drop for convenience.
- **Patient-Centric View**: Automatically aggregates data by patient, showing a clear list of individuals with outstanding balances.
- **Detailed Invoice Breakdown**: Expand each patient's entry to see a detailed list of all their individual invoices, including status (Open or Booked).
- **PDF Generation**: Generate a professional payment reminder (Zahlungserinnerung) in PDF format for any patient with open invoices.
- **Local Data Persistence**: All imported data is saved locally, allowing for continuous tracking and state preservation between application launches.

## 🚀 Getting Started

### Installation

1.  Go to the [**Releases**](https://github.com/your-username/therapypay-app/releases) page of this repository.
2.  Download the latest `therapypay-app-windows.zip` file.
3.  Unzip the downloaded file to a location of your choice.
4.  Run the `therapypay-app-win_x64.exe` to start the application.

### How to Use

1.  Launch the application.
2.  Click the **"Bericht erstellen"** button.
3.  In the modal that appears, either drag and drop your Excel file or click to browse and select it.
4.  The dashboard and patient list will automatically update with the imported data. New data is merged with existing records.
5.  To generate a payment reminder, click the **PDF icon** next to a patient's name in the "Offene Zahlungen nach Patienten" table. A save dialog will appear, allowing you to save the PDF to your computer.

### Required Excel Format

For the import to work correctly, the Excel file must contain a sheet named exactly **`RAW DATA - bitte nicht ändern`**. This sheet needs the following columns:
- `Text` (Patient Name)
- `Referenz` (Invoice Reference Number)
- `Buchungsdatum` (Booking Date)
- `Betrag in Hauswährung` (Amount)
- `Zuordnung` (An identifier, used to filter relevant rows)

## 👨‍💻 For Developers

If you want to run or build the project from the source, follow these steps.

### Prerequisites

- Node.js (v20 or later is recommended)

### Development

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/your-username/therapypay-app.git
    cd therapypay-app
    ```
2.  **Install the Neutralinojs CLI:**
    ```bash
    npm install -g @neutralinojs/neu
    ```
3.  **Download/update framework binaries:**
    ```bash
    neu update
    ```
4.  **Run the app in development mode:**
    This will launch the application and automatically reload it when you make changes to the source files.
    ```bash
    neu run
    ```
5.  **Build for release:**
    This command bundles the application into a distributable package.
    ```bash
    neu build --release
    ```
    The final output will be located in the `dist/` directory.
