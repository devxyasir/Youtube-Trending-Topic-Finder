
# Find Trending Topics for YouTube Videos

## Description

This project allows you to fetch the most popular YouTube videos from various countries using the YouTube Data API v3. By collecting video details like title, views, comments, likes, and other metadata, this tool helps you identify trending topics worldwide.

The script uses the YouTube Data API to gather the most popular videos from different countries, storing the data in CSV files for later analysis.

## Problem with API Access

If you encounter a **403 Forbidden** error while using the API, it indicates that the API key is either missing or unregistered. The error message:

```plaintext
Method doesn't allow unregistered callers (callers without established identity).
Please use API Key or other form of API consumer identity to call this API.
```

This error occurs because the request is being made without a valid API key or proper authentication.

### **How to Resolve the API Access Issue**

#### 1. **Obtain a YouTube API Key**
   - Go to the [Google Developers Console](https://console.developers.google.com/).
   - Create a new project or select an existing one.
   - Navigate to **APIs & Services** > **Credentials**.
   - Create an API key under the "API keys" section.
   - Enable the **YouTube Data API v3** for your project.
   - Use this API key in your project to authenticate requests.

#### 2. **Add the API Key to the Project**
   - Create a file named `api_key.txt` in the project folder.
   - Paste the obtained API key inside this file.

#### 3. **Update the Country Codes**
   - Create a `country_codes.txt` file and add the country codes you wish to scrape (e.g., `US`, `IN`, `GB`).

#### 4. **Running the Script**
   After you've completed the above steps, run the script with the following command:

   ```bash
   python sample.py --key_path=api_key.txt --country_code_path=country_codes.txt --output_dir=output/
   ```

   This will fetch the trending videos for the specified countries and save them in the `output/` directory.

## Features

- Fetch popular YouTube videos from multiple countries.
- Collects video metadata such as title, views, tags, description, likes, and more.
- Saves the data in CSV format for further analysis.
- Allows easy integration of country codes for worldwide data collection.

## Setup Instructions

### Prerequisites

Before running the project, make sure to have the following:
- Python 3.x installed.
- Internet connection to access the YouTube Data API.
- A valid YouTube API key (refer to the steps above).

### 1. Clone the Repository

Clone the repository to your local machine:

```bash
git clone https://github.com/your-username/Find-Trending-Topics-For-Youtube-Videos.git
cd Find-Trending-Topics-For-Youtube-Videos
```

### 2. Configure API Key and Country Codes

- Create a `api_key.txt` file in the project folder and paste your API key inside it.
- Create a `country_codes.txt` file and add the country codes you want to scrape (e.g., `US`, `IN`, `GB`).

### 3. Install Dependencies

Make sure to install the required Python packages using:

```bash
pip install -r requirements.txt
```

### 4. Run the Script

Now, you can start fetching the trending videos by running the script:

```bash
python sample.py --key_path=api_key.txt --country_code_path=country_codes.txt --output_dir=output/
```

This will fetch the trending videos for the countries specified in the `country_codes.txt` file and store them in the `output/` directory.

### 5. Viewing the Results

The fetched data will be saved in CSV files with names like `21.12.11_US_videos.csv`. You can open these CSV files to explore the details of the trending videos.

## Common Errors

### **403 Forbidden Error**

This error occurs if the API request is not authorized. Please follow the steps mentioned above to ensure your API key is correctly configured.



## Contributing

If you want to contribute to this project, feel free to fork the repository and create pull requests. All contributions are welcome!

---

## Connect with Me!

Feel free to connect with me on the following platforms:

[![GitHub](https://img.shields.io/badge/GitHub-Profile-blue)](https://github.com/jaamyasir)  
[![Facebook](https://img.shields.io/badge/Facebook-Profile-blue)](https://facebook.com/jamyasir0010)  
[![Medium](https://img.shields.io/badge/Medium-Profile-green)](https://jamyasir.medium.com/)

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
```

### Key Updates:
- **API Key Resolution Method**: The README now includes a detailed method to resolve the **403 Forbidden** error by setting up the correct API key and configuring the necessary files (`api_key.txt` and `country_codes.txt`).
- **Error Handling**: Clear instructions on how to address common API errors.
