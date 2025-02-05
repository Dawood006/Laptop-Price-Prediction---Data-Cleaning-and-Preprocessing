# Laptop Price Prediction - Data Cleaning and Preprocessing

This repository contains the code and data for cleaning and preprocessing a dataset collected from Flipkart for predicting laptop prices. The dataset includes various features related to laptops, such as specifications, warranty details, and other attributes. The goal is to clean and preprocess the data to prepare it for machine learning models.

## Dataset Overview

The dataset was scraped from Flipkart and contains information about various laptops. The dataset includes the following columns:

### Columns and Their Meanings

1. **Unnamed: 0**: Index column (dropped during preprocessing).
2. **index**: Another index column (dropped during preprocessing).
3. **Covered in Warranty**: Details about what is covered under the warranty.
4. **Warranty Service Type**: Type of warranty service (e.g., Carry-in).
5. **Processor Variant**: Variant of the processor (e.g., N305).
6. **Clock Speed**: Clock speed of the processor.
7. **Finger Print Sensor**: Indicates whether the laptop has a fingerprint sensor.
8. **MS Office Provided**: Indicates whether MS Office is provided with the laptop.
9. **Weight**: Weight of the laptop.
10. **Processor Generation**: Generation of the processor.
11. **Screen Resolution**: Resolution of the laptop screen.
12. **Not Covered in Warranty**: Details about what is not covered under the warranty.
13. **Speakers**: Indicates whether the laptop has speakers.
14. **Sales Package**: Details about what is included in the sales package.
15. **Disk Drive**: Indicates whether the laptop has a disk drive.
16. **Suitable For**: Indicates the suitable use cases for the laptop (e.g., Gaming, Everyday Use).
17. **Backlit Keyboard**: Indicates whether the laptop has a backlit keyboard.
18. **Touchscreen**: Indicates whether the laptop has a touchscreen.
19. **Processor Name**: Name of the processor (e.g., Core i3).
20. **Bluetooth**: Bluetooth version supported by the laptop.
21. **RAM Type**: Type of RAM (e.g., DDR4, LPDDR5).
22. **Screen Type**: Type of screen (e.g., Full HD IPS LED-backlit LCD Display).
23. **id**: Unique identifier for each laptop (dropped during preprocessing).
24. **Domestic Warranty**: Details about the domestic warranty.
25. **Series**: Series of the laptop (e.g., Chromebook Plus Google AI).
26. **Operating System**: Operating system installed on the laptop (e.g., Chrome, Windows 11 Home).
27. **Model Number**: Model number of the laptop.
28. **Screen Size**: Size of the laptop screen.
29. **USB Port**: Details about the USB ports available on the laptop.
30. **SSD**: Indicates whether the laptop has an SSD.
31. **Processor Brand**: Brand of the processor (e.g., Intel, AMD).
32. **Internal Mic**: Indicates whether the laptop has an internal microphone.
33. **Wireless LAN**: Details about the wireless LAN supported by the laptop.
34. **Storage Type**: Type of storage (e.g., SSD, HDD).
35. **Color**: Color of the laptop.
36. **Battery Cell**: Number of battery cells.
37. **Type**: Type of laptop (e.g., Chromebook, Gaming Laptop).
38. **Keyboard**: Details about the keyboard.
39. **SSD Capacity**: Capacity of the SSD.
40. **Warranty Summary**: Summary of the warranty.
41. **Model Name**: Name of the laptop model.
42. **Part Number**: Part number of the laptop.
43. **RAM**: Amount of RAM in the laptop.
44. **Graphic Processor**: Details about the graphic processor.
45. **Web Camera**: Details about the web camera.
46. **Power Supply**: Details about the power supply.
47. **HDMI Port**: Indicates whether the laptop has an HDMI port.
48. **Dimensions**: Dimensions of the laptop.
49. **OS Architecture**: Architecture of the operating system (e.g., 64 bit).
50. **Face Recognition**: Indicates whether the laptop supports face recognition.
51. **Pointer Device**: Details about the pointer device.
52. **EMMC Storage Capacity**: Capacity of the eMMC storage.
53. **Dedicated Graphic Memory Type**: Type of dedicated graphic memory.
54. **Dedicated Graphic Memory Capacity**: Capacity of the dedicated graphic memory.
55. **Refresh Rate**: Refresh rate of the screen.
56. **Battery Backup**: Battery backup time.
57. **Ethernet**: Indicates whether the laptop has an Ethernet port.
58. **Expandable Memory**: Details about expandable memory.
59. **Expandable SSD Capacity**: Capacity of expandable SSD.
60. **Supported Operating System**: Operating systems supported by the laptop.
61. **Cache**: Cache memory details.
62. **Number of Cores**: Number of cores in the processor.
63. **Mic In**: Indicates whether the laptop has a microphone input.
64. **Additional Features**: Additional features of the laptop.
65. **Memory Slots**: Number of memory slots.
66. **RAM Frequency**: Frequency of the RAM.
67. **RJ45**: Indicates whether the laptop has an RJ45 port.
68. **Sound Properties**: Details about the sound properties.
69. **Lock Port**: Indicates whether the laptop has a lock port.
70. **Security Chip**: Indicates whether the laptop has a security chip.
71. **Chipset**: Details about the chipset.
72. **RPM**: RPM of the disk drive.
73. **Multi Card Slot**: Indicates whether the laptop has a multi-card slot.
74. **Hardware Interface**: Details about the hardware interface.
75. **Sound Chip**: Details about the sound chip.
76. **Included Software**: Software included with the laptop.
77. **Antivirus**: Indicates whether antivirus software is included.
78. **Inbuilt 4G LTE**: Indicates whether the laptop has inbuilt 4G LTE.
79. **Stylus Included**: Indicates whether a stylus is included.
80. **NFC Support**: Indicates whether the laptop supports NFC.
81. **Wireless WAN**: Indicates whether the laptop supports wireless WAN.
82. **Laptop Bag**: Indicates whether a laptop bag is included.
83. **System Architecture**: Architecture of the system.
84. **Brightness**: Brightness of the screen.
85. **RJ11**: Indicates whether the laptop has an RJ11 port.
86. **VGA Port**: Indicates whether the laptop has a VGA port.
87. **Color Gamut**: Color gamut of the screen.
88. **TGP**: Total Graphics Power.
89. **Other Accessories**: Other accessories included with the laptop.
90. **International Warranty**: Details about the international warranty.
91. **HDD Capacity**: Capacity of the HDD.
92. **Dock Port**: Indicates whether the laptop has a dock port.
93. **Firewire Port**: Indicates whether the laptop has a Firewire port.
94. **Read/Write Speed**: Read/write speed of the storage.
95. **S-video**: Indicates whether the laptop has an S-video port.
96. **Certification**: Certifications of the laptop.
97. **Recovery Options**: Recovery options available on the laptop.
98. **Optane Memory**: Indicates whether the laptop has Optane memory.
99. **Rating**: Rating of the laptop.
100. **price**: Price of the laptop.
101. **Link**: Link to the product page on Flipkart (dropped during preprocessing).
102. **Names**: Name of the laptop product.

## Data Cleaning and Preprocessing

The following steps were taken to clean and preprocess the data:

1. **Dropping Unnecessary Columns**: Columns like `Unnamed: 0`, `index`, `id`, and `Link` were dropped as they were not useful for analysis.
2. **Handling Duplicates**: Duplicate rows were identified and removed.
3. **Handling Missing Values**: Missing values in columns like `Finger Print Sensor`, `MS Office Provided`, `Face Recognition`, and `Number of Cores` were filled with appropriate values.
4. **Feature Engineering**: New features were created, such as `RAM (GB)`, `SSD (GB)`, `HDD (GB)`, and `Expandable Memory (GB)`, by extracting numerical values from existing columns.
5. **Encoding Categorical Variables**: Categorical variables like `Processor Brand`, `RAM Type`, and `Storage Type` were encoded using one-hot encoding or ordinal encoding.
6. **Scaling**: Numerical features were scaled using `MaxAbsScaler` to prepare them for machine learning models.
7. **Splitting Data**: The dataset was split into training and testing sets for model evaluation.

## Model Building

A Linear Regression model was used to predict the price of laptops based on the cleaned and preprocessed data. The model was evaluated using metrics like Mean Squared Error (MSE), Mean Absolute Error (MAE), and R-squared (R²).

## Repository Structure

- **Data_cleaning_Price_prediction.ipynb**: Jupyter notebook containing the code for data cleaning, preprocessing, and model building.
- **lappy2.csv**: The original dataset collected from Flipkart.

## Usage

To use this repository, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/Dawood006/[laptop-price-prediction.git](https://github.com/Dawood006/Laptop-Price-Prediction---Data-Cleaning-and-Preprocessing)
   ```
2. Navigate to the repository directory:
   ```bash
   cd laptop-price-prediction
   ```
3. Open the Jupyter notebook:
   ```bash
   jupyter notebook Data_cleaning_Price_prediction.ipynb
   ```
4. Run the notebook cells to perform data cleaning, preprocessing, and model building.

## Dependencies

- Python 3.x
- pandas
- numpy
- scikit-learn
- matplotlib
- seaborn

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- The dataset was scraped from Flipkart.
- Special thanks to the open-source community for providing the tools and libraries used in this project.

---

This README provides an overview of the dataset, the steps taken to clean and preprocess the data, and how to use the repository. For more details, refer to the Jupyter notebook included in the repository.
