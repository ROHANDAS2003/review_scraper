# Review Scraper Documentation
Abbreviations

1. **GUI**: Graphical User Interface - A type of interface that allows users to interact with electronic devices through graphical icons and visual indicators.
1. **HTML**: HyperText Markup Language - The standard markup language used for creating web pages and web applications.
1. **HTTP**: Hypertext Transfer Protocol - An application protocol used for transmitting hypermedia documents, such as HTML, over the internet.
1. **API**: Application Programming Interface - A set of rules and protocols that allows different software applications to communicate with each other.
1. **URL**: Uniform Resource Locator - A reference or address used to locate resources on the internet, such as web pages, images, or files.
1. **API Key**: A unique identifier used to authenticate requests made to an API, typically provided by the service provider when accessing their API.
1. **IP**: Internet Protocol - A set of rules governing the format of data packets sent over the internet and the addressing scheme for devices connected to the internet.
1. **OS**: Operating System - Software that manages computer hardware and provides common services for computer programs.
## Overview
The Review Scraper is a Python application designed to scrape reviews from two popular e-commerce platforms: Amazon and Etsy. It offers a graphical user interface (GUI) built using PyQt5 to input URLs from these platforms, along with an Etsy API key if required, and collects reviews from the provided URLs. The collected reviews are then exported to an Excel file.
## Features
- **Scraping Amazon Reviews**: The application fetches reviews from Amazon product pages by parsing HTML using BeautifulSoup and sending HTTP requests using the Requests library.
- **Scraping Etsy Reviews**: Similarly, the application retrieves reviews from Etsy listings by utilizing the Etsy API and making HTTP requests.
- **Graphical User Interface (GUI)**: The GUI provides a user-friendly interface for users to input URLs and an Etsy API key, initiate the scraping process, and monitor the progress of reviews being collected.
- **Asynchronous Processing**: The application employs multithreading to perform scraping tasks asynchronously, ensuring a responsive user experience.
- **Export to Excel**: Once reviews are collected, they are exported to an Excel file, allowing users to analyze and manipulate the data further.
## Cloning the Repository
To clone the Wordle Game project from GitHub, follow these steps:

1. Open your terminal (Command Prompt, PowerShell, or any other terminal emulator).
1. Navigate to the directory where you want to clone the repository.
1. Run the following command: git clone https://github.com/ROHANDAS2003/review_scraper
1. Navigate into the cloned repository directory: cd review\_scraper
## Dependencies
The Review Scraper relies on the following Python libraries:

- **requests**: For making HTTP requests to fetch web pages.
- **BeautifulSoup (bs4)**: For parsing HTML content retrieved from web pages.
- **pandas**: For data manipulation and exporting reviews to Excel.
- **PyQt5**: For creating the graphical user interface.
- **urllib**: For parsing URLs.
- **random**: For generating random integers.
- **time**: For introducing delays in the scraping process.
- **os**: For interacting with the operating system.
- **re**: For regular expression operations.

Install the dependencies using pip: pip install -r requirements.txt
## Running the Program
### **Input**
1. **Amazon/Etsy URLs**: Enter the URLs of the Amazon product pages or Etsy listings from which you want to scrape reviews. You can input multiple URLs, each on a new line.
1. **Etsy API Key**: If scraping Etsy reviews, provide your Etsy API key in the designated field.
### **Operation**
1. Click on the "Start collecting" button to initiate the scraping process.
1. The application will display the progress of reviews being collected in the "Progress" label.
1. Once the scraping is complete, the collected reviews will be exported to an Excel file.
### **Output**
The exported Excel file contains the following columns:

- **title**: The title of the review.
- **rating**: The rating given by the reviewer.
- **body**: The text content of the review.
## Implementation Details
The Review Scraper consists of the following components:

- **Main Application**: The main script (Review\_Scraper.py) initializes the PyQt5 application and creates the main window for user interaction.
- **Worker Thread**: The WorkerThread class manages the scraping tasks asynchronously. It communicates with the main GUI thread to update the progress and signal completion.
- **GUI Components**: The PyQt5-based graphical user interface includes labels, text fields, buttons, and progress indicators to facilitate user input and feedback.
- **Helper Functions**: Several helper functions are implemented to handle tasks such as modifying user agents, parsing URLs, fetching web pages, extracting reviews, and exporting data to Excel.
## Limitations
- **Platform Support**: The application currently supports scraping reviews only from Amazon and Etsy. Support for additional e-commerce platforms could be added in future versions.
- **Rate Limiting**: There is a risk of being rate-limited or blocked by the platforms due to frequent scraping. Users should be cautious and adhere to the platforms' terms of service.
## Future Enhancements
Potential improvements and features for future versions of the Review Scraper may include:

- **Error Handling**: Implement robust error handling mechanisms to gracefully handle exceptions and network errors during scraping.
- **User Authentication**: Support user authentication for platforms that require login credentials to access reviews.
- **Custom Export Options**: Allow users to specify custom export formats and options for exported data.
- **Performance Optimization**: Optimize the scraping process for efficiency and faster execution.
- **Proxy Support**: Integrate proxy support to prevent IP blocking and enhance anonymity during scraping.
## Conclusion
The Review Scraper provides a convenient solution for extracting reviews from Amazon and Etsy, offering a seamless user experience through its intuitive graphical interface. With further development and refinement, it has the potential to become a versatile tool for market research, sentiment analysis, and data-driven decision-making in e-commerce businesses.

