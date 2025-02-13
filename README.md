            ###################################### ███████ ████████ ██      ######################################  
            ###################################### ██         ██    ██      ###################################### 
            ###################################### █████      ██    ██      ###################################### 
            ###################################### ██         ██    ██      ###################################### 
            ###################################### ███████    ██    ███████ ###################################### 


# OLX (Opotional Mobile Phone) Dataset Extraction

## Overview
This Python script scrapes (mobile phone)"make it optional" listings from OLX Pakistan, specifically for Lahore(i will make it optional). It extracts the number of listings available for different phone brands under various conditions (Used, New, Open-Box, For Parts, and Refurbished) and organizes the data into a structured table.

## Features
- Scrapes mobile phone listing counts from OLX Lahore.
- Supports multiple filters (Used, New, Open-Box, For Parts, Refurbished).
- Extracts brand-wise listing counts.
- Organizes data into a structured pandas DataFrame.
- Implements data cleaning and deduplication.

## Installation
To run this script, you need to have Python installed along with the following dependencies:

```sh
pip install requests beautifulsoup4 pandas
```

## Usage
Simply run the script to fetch and display the structured mobile phone listing data:

```sh
python olx_scraper.py
```

## How It Works
1. **Define Filters:**
   - The script includes different conditions like `Used`, `New`, `Open-Box`, etc.
2. **Scrape Data:**
   - It makes HTTP requests to OLX for each condition and extracts the listing count for each brand.
3. **Process Data:**
   - Extracted data is cleaned, formatted, and stored in a pandas DataFrame.
4. **Display Output:**
   - The final table presents a clear comparison of brand-wise listing counts across different conditions.

## Example Output
### Before
```
{'?filter=new_used_eq_used': {'Apple iPhone': 14162, 'Samsung Mobile': 4899, 'OPPO': 2095, 'Vivo': 2065, 'Infinix': 1992, 'One Plus': 1860, 'Xiaomi': 1477, 'Google': 1212, 'Tecno': 902, 'Huawei': 809, 'Realme': 539, 'Other Mobiles': 4}}
{'?filter=new_used_eq_new': {'Apple iPhone': 3442, 'Samsung Mobile': 1148, 'Google': 686, 'Vivo': 516, 'One Plus': 493, 'Infinix': 435, '
'OPPO': 432, 'Xiaomi': 370, 'Nokia': 306, 'Tecno': 186, 'Other Mobiles': 154, 'Realme': 142, 'Sony': 102, 'Huawei': 75, 'Motorola': 62, I
'Itel': 51, 'LG': 47, 'Zte': 24, 'Honor': 16, 'Acer': 12}}
{'?filter=new_used_eq_open-box': {'Apple iPhone': 965, 'Samsung Mobile': 411, 'Infinix': 305, 'Vivo': 252, 'Xiaomi': 247, 'OPPO': 193, 'TTecno': 152, 'Realme': 98, 'Google': 91, 'Other Mobiles': 87, 'One Plus': 82, 'Itel': 43, 'Nokia': 22, 'Huawei': 15, 'Calme': 12, 'Honor:': 10, 'Motorola': 9, 'Mobilink JazzX': 8, 'QMobile': 7, 'Zte': 7}}
{'?filter=new_used_eq_for-parts-or-not-working': {'Apple iPhone': 112, 'Samsung Mobile': 76, 'Google': 40, 'One Plus': 32, 'Xiaomi': 30,  'Huawei': 21, 'OPPO': 14, 'Infinix': 9, 'Nokia': 7, 'Vivo': 7, 'Tecno': 6, 'Other Mobiles': 5, 'LG': 4, 'Sony': 4, 'Motorola': 3, 'Hono'r': 2, 'BlackBerry': 1, 'HTC': 1, 'Lava': 1, 'QMobile': 1}}
{'?filter=new_used_eq_refurbished': {'OPPO': 133, 'Apple iPhone': 23, 'Samsung Mobile': 20, 'Vivo': 12, 'One Plus': 10, 'Google': 6, 'Xiaaomi': 5, 'Huawei': 4, 'Tecno': 4, 'Acer': 3, 'Infinix': 2, 'Realme': 2, 'Alcatel': 1, 'Five': 1, 'Honor': 1, 'LG': 1, 'Sony': 1, 'OtherM Mobiles': 1}}
P
```
### After
```
                Total   Used   New  Open-Box  For Parts  Refurbished
Acer                0      0    11         0          0            3
Alcatel             0      0     0         0          0            1
Apple iPhone    18663  14133  3441       964        102           23
Asus                0      0     0         0          1            0
BlackBerry          0      0     0         0          1            1
Calme               0      0     0        11          0            0
Google           2053   1228   686        93         39            7
Honor             151    125    14         9          2            1
Huawei            923    816    66        15         20            6
Infinix          2735   1982   434       308          9            2
Itel              219    119    50        50          0            0
LG                262    208    46         0          5            1
Mobilink JazzX     63     48     0         6          0            0
Motorola          316    238    63        12          3            0
Nokia             576    244   301        24          7            0
OPPO             2833   2058   428       197         14          136
One Plus         2476   1854   491        89         32           10
Other Mobiles     689    442   155        85          6            1
Realme            773    529   140       101          0            2
Samsung Mobile   6542   4902  1139       407         74           20
Sony              398    286   100         7          4            1
Tecno            1218    892   174       143          6            3
Vivo             2878   2081   522       256          7           12
Xiaomi           2137   1494   369       240         29            5
Zte                90     52    28        10          0            0
```

## Notes
- The script extracts data based on specific HTML selectors. If OLX updates its website structure, the selectors may need adjustments.
- The script removes duplicate records before presenting the final dataset.

#    Up coming Questions    


 
## License
This project is open-source and available under the MIT License.

---

Enjoy scraping! 🚀

