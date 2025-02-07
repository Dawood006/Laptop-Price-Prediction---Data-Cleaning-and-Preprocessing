# Laptop Price Prediction - Data Cleaning and Preprocessing

This repository contains the code and data for cleaning and preprocessing a dataset collected from [Flipkart](https://www.flipkart.com)🛒 for predicting laptop prices 💻. The dataset includes various features related to laptops, such as specifications, warranty details, and other attributes. The goal is to clean and preprocess the data to prepare it for machine learning models.

## Dataset Overview

The dataset was scraped from [Flipkart](https://www.flipkart.com) and contains information about various laptops. The dataset includes the following columns:

### Columns and Their Meanings

1. **Covered in Warranty**: Details about what is covered under the warranty.
2. **Warranty Service Type**: Type of warranty service (e.g., Carry-in).
3. **Processor Variant**: Variant of the processor (e.g., N305).
4. **Clock Speed**: Clock speed of the processor.
5. **Finger Print Sensor**: Indicates whether the laptop has a fingerprint sensor.
6. **MS Office Provided**: Indicates whether MS Office is provided with the laptop.
7. **Weight**: Weight of the laptop.
8. **Processor Generation**: Generation of the processor.
9. **Screen Resolution**: Resolution of the laptop screen.
10. **Not Covered in Warranty**: Details about what is not covered under the warranty.
11. **Speakers**: Indicates whether the laptop has speakers.
12. **Sales Package**: Details about what is included in the sales package.
13. **Disk Drive**: Indicates whether the laptop has a disk drive.
14. **Suitable For**: Indicates the suitable use cases for the laptop (e.g., Gaming, Everyday Use).
15. **Backlit Keyboard**: Indicates whether the laptop has a backlit keyboard.
16. **Touchscreen**: Indicates whether the laptop has a touchscreen.
17. **Processor Name**: Name of the processor (e.g., Core i3).
18. **Bluetooth**: Bluetooth version supported by the laptop.
19. **RAM Type**: Type of RAM (e.g., DDR4, LPDDR5).
20. **Screen Type**: Type of screen (e.g., Full HD IPS LED-backlit LCD Display).
21. **Domestic Warranty**: Details about the domestic warranty.
22. **Series**: Series of the laptop (e.g., Chromebook Plus Google AI).
23. **Operating System**: Operating system installed on the laptop (e.g., Chrome, Windows 11 Home).
24. **Model Number**: Model number of the laptop.
25. **Screen Size**: Size of the laptop screen.
26. **USB Port**: Details about the USB ports available on the laptop.
27. **SSD**: Indicates whether the laptop has an SSD.
28. **Processor Brand**: Brand of the processor (e.g., Intel, AMD).
29. **Internal Mic**: Indicates whether the laptop has an internal microphone.
30. **Wireless LAN**: Details about the wireless LAN supported by the laptop.
31. **Storage Type**: Type of storage (e.g., SSD, HDD).
32. **Color**: Color of the laptop.
33. **Battery Cell**: Number of battery cells.
34. **Type**: Type of laptop (e.g., Chromebook, Gaming Laptop).
35. **Keyboard**: Details about the keyboard.
36. **SSD Capacity**: Capacity of the SSD.
37. **Warranty Summary**: Summary of the warranty.
38. **Model Name**: Name of the laptop model.
39. **Part Number**: Part number of the laptop.
40. **RAM**: Amount of RAM in the laptop.
41. **Graphic Processor**: Details about the graphic processor.
42. **Web Camera**: Details about the web camera.
43. **Power Supply**: Details about the power supply.
44. **HDMI Port**: Indicates whether the laptop has an HDMI port.
45. **Dimensions**: Dimensions of the laptop.
46. **OS Architecture**: Architecture of the operating system (e.g., 64 bit).
47. **Face Recognition**: Indicates whether the laptop supports face recognition.
48. **Pointer Device**: Details about the pointer device.
49. **EMMC Storage Capacity**: Capacity of the eMMC storage.
50. **Dedicated Graphic Memory Type**: Type of dedicated graphic memory.
51. **Dedicated Graphic Memory Capacity**: Capacity of the dedicated graphic memory.
52. **Refresh Rate**: Refresh rate of the screen.
53. **Battery Backup**: Battery backup time.
54. **Ethernet**: Indicates whether the laptop has an Ethernet port.
55. **Expandable Memory**: Details about expandable memory.
56. **Expandable SSD Capacity**: Capacity of expandable SSD.
57. **Supported Operating System**: Operating systems supported by the laptop.
58. **Cache**: Cache memory details.
59. **Number of Cores**: Number of cores in the processor.
60. **Mic In**: Indicates whether the laptop has a microphone input.
61. **Additional Features**: Additional features of the laptop.
62. **Memory Slots**: Number of memory slots.
63. **RAM Frequency**: Frequency of the RAM.
64. **RJ45**: Indicates whether the laptop has an RJ45 port.
65. **Sound Properties**: Details about the sound properties.
66. **Lock Port**: Indicates whether the laptop has a lock port.
67. **Security Chip**: Indicates whether the laptop has a security chip.
68. **Chipset**: Details about the chipset.
69. **RPM**: RPM of the disk drive.
70. **Multi Card Slot**: Indicates whether the laptop has a multi-card slot.
71. **Hardware Interface**: Details about the hardware interface.
72. **Sound Chip**: Details about the sound chip.
73. **Included Software**: Software included with the laptop.
74. **Antivirus**: Indicates whether antivirus software is included.
75. **Inbuilt 4G LTE**: Indicates whether the laptop has inbuilt 4G LTE.
76. **Stylus Included**: Indicates whether a stylus is included.
77. **NFC Support**: Indicates whether the laptop supports NFC.
78. **Wireless WAN**: Indicates whether the laptop supports wireless WAN.
79. **Laptop Bag**: Indicates whether a laptop bag is included.
80. **System Architecture**: Architecture of the system.
81. **Brightness**: Brightness of the screen.
82. **RJ11**: Indicates whether the laptop has an RJ11 port.
83. **VGA Port**: Indicates whether the laptop has a VGA port.
84. **Color Gamut**: Color gamut of the screen.
85. **TGP**: Total Graphics Power.
86. **Other Accessories**: Other accessories included with the laptop.
87. **International Warranty**: Details about the international warranty.
88. **HDD Capacity**: Capacity of the HDD.
89. **Dock Port**: Indicates whether the laptop has a dock port.
90. **Firewire Port**: Indicates whether the laptop has a Firewire port.
91. **Read/Write Speed**: Read/write speed of the storage.
92. **S-video**: Indicates whether the laptop has an S-video port.
93. **Certification**: Certifications of the laptop.
94. **Recovery Options**: Recovery options available on the laptop.
95. **Optane Memory**: Indicates whether the laptop has Optane memory.
96. **Rating**: Rating of the laptop.
97. **price**: Price of the laptop.
98. **Names**: Name of the laptop product.

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
- **lappy2.csv**: The original dataset collected from [Flipkart](https://www.flipkart.com). [Download the dataset here](lappy2.csv).

## Usage

To use this repository, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/Dawood006/Laptop-Price-Prediction---Data-Cleaning-and-Preprocessing.git
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

- The dataset was scraped from [Flipkart](https://www.flipkart.com/).
- Special thanks to the open-source community for providing the tools and libraries used in this project.

---

This README provides an overview of the dataset, the steps taken to clean and preprocess the data, and how to use the repository. For more details, refer to the Jupyter notebook included in the repository.
