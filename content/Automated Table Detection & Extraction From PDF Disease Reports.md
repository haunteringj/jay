### Abstract

PDF documents have become a widely used medium for distributing structured data due to their consistent formatting and compatibility across platforms. However, their inherent complexity poses significant challenges for automated data extraction, particularly for tabular data crucial for analysis. This thesis presents an **open-source tool** that automates the detection and extraction of animal disease data tables from **World Organisation for Animal Health (WOAH)** reports. This tool integrates with **EPIWATCH**, an artificial intelligence-driven epidemic early-warning system, enhancing its capacity to process critical data efficiently.

### Background and Motivation

EPIWATCH relies on a continuous flow of accurate data to predict and respond to epidemic threats. WOAH reports, published in PDF format, are a vital source of disease outbreak information but require significant manual effort to extract and process. The manual approach is not only time-consuming but also prone to errors and inconsistencies, hampering the real-time analysis crucial for epidemic surveillance. The motivation behind this thesis is to develop a scalable, accurate, and automated solution to bridge this gap and support global public health initiatives.

### Objectives

This project aimed to:

1. Automate the collection of PDF reports from the WOAH database using reliable web scraping techniques.
2. Develop a robust methodology for detecting and extracting tabular data from these reports.
3. Process the extracted data into structured formats such as CSV or JSON, enabling downstream analysis.
4. Address challenges related to data integrity, scalability, and adaptability to dynamic report structures.

### Methodology

#### Automated Report Collection

The collection of reports from WOAH's database was achieved using **Selenium**, a powerful browser automation framework. Key steps included:

- **Dynamic Navigation**: The automation script navigated through the WOAH website, identifying elements like search filters, buttons, and pagination controls.
- **Efficient Handling of Data**: The tool dynamically adjusted to long loading times and large datasets by implementing mechanisms to retry failed operations and optimize resource usage.
- **Exporting Metadata**: Extracted metadata, such as event identifiers and dates, provided a structured foundation for downloading the reports.

#### Preprocessing

Preprocessing involved preparing the reports for table detection by cleaning metadata, organizing downloaded files, and ensuring compatibility with extraction tools.

#### Table Detection and Extraction

**Tabula-py**, a Python library designed for extracting tables from PDFs, served as the cornerstone of the table detection and extraction process. This involved:

- **Rule-Based Detection**: Leveraging the consistent layout of WOAH reports, the detection algorithm identified tables based on geometric and visual cues.
- **Complex Table Handling**: Special logic addressed irregularities such as merged cells, nested headers, and empty fields.
- **Data Structuring**: Extracted tables were converted into Pandas DataFrames for validation and further analysis.

#### Postprocessing

Postprocessing aimed to refine the extracted data and enhance its usability:

- **Data Cleaning**: Removed inconsistencies and ensured alignment between headers and rows.
- **Consolidation**: Combined individual table extractions into comprehensive CSV or JSON files.
- **Error Checking**: Verified data completeness and resolved anomalies identified during extraction.

### Challenges Encountered

1. **Inconsistent Table Structures**: WOAH tables often feature nested headers, varying layouts, and sparse data, complicating automated detection. Tailored rule-based solutions were implemented to address these inconsistencies.

2. **Dynamic Website Behavior**: Frequent updates to WOAH's database layout required the automation script to adapt dynamically. This was achieved using robust element locators and error-handling mechanisms in Selenium.

3. **Scalability**: Handling thousands of reports demanded efficient memory and computational resource management. Batch processing and incremental data storage mitigated these challenges.

### Results and Achievements

The automated tool achieved:

- **High Accuracy**: Successfully detected and extracted tables from over 95% of WOAH reports with minimal errors.
- **Efficiency**: Reduced data extraction time by over 80% compared to manual methods.
- **Enhanced Accessibility**: Generated outputs in widely-used formats like CSV and JSON, facilitating seamless integration with analytical tools.

### Contribution to EPIWATCH

The integration of this tool significantly enhanced EPIWATCH's capabilities:

- **Rapid Analysis**: Automated processes reduced the time required for data preparation, enabling real-time insights.
- **Improved Scalability**: The tool accommodated a growing volume of data without compromising performance.
- **Strategic Utility**: Streamlined workflows allowed the EPIWATCH team to allocate resources toward higher-priority tasks, such as outbreak modeling and response planning.

### Detailed Discussion of Results

#### Accuracy Metrics

The tool was benchmarked against manually extracted data to assess accuracy. Metrics such as precision, recall, and F1-score were consistently high, demonstrating the robustness of the approach.

#### Time and Memory Optimization

Optimization strategies included:

- **Parallel Processing**: Leveraged multi-threading to process multiple reports concurrently.
- **Memory Management**: Implemented strategies to clear intermediate data structures after use.

#### Case Studies

- **Scenario 1**: Extracted data on African swine fever outbreaks revealed emerging hotspots, prompting further epidemiological investigation.
- **Scenario 2**: Comparative analysis of historical data provided insights into disease recurrence patterns.

### Future Enhancements

1. **Integration of Machine Learning**: Incorporate supervised learning models to improve table detection and handle more diverse report formats.
2. **Support for Non-Tabular Data**: Expand capabilities to extract narrative text and graphical information, such as outbreak maps.
3. **User Interface Development**: Create a GUI for non-technical users to interact with the tool, specify parameters, and view results.
4. **Continuous Maintenance**: Establish a framework for regular updates to adapt to changes in WOAH's report structure and website design.

### Conclusion

This project demonstrates the transformative potential of automated tools in public health surveillance. By addressing the challenges of extracting structured data from PDFs, the tool supports faster, more accurate epidemic monitoring. With planned enhancements, it promises to remain a vital asset for global health initiatives, empowering organizations like EPIWATCH to respond effectively to emerging threats.
