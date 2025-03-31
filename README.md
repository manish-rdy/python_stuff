dac_project/ 
│ 
├── main.py # Main orchestration script 
├── crypto_providers.xlsx # List of known crypto service providers 
├── suppressions.csv # Past RM responses for suppression logic 
├── thresholds.json # Thresholds by (country, segment) 
│ 
├── MENAT/ # Region-specific input folder (MENAT test data) 
│   ├── customer_demographics.csv 
│   ├── customer_transactions.csv 
│   └── customer_rm.csv 
│ 
├── output/ # Generated outputs (created at runtime) 
│ └── MENAT/ 
│     ├── alerts_MENAT_202503.csv # Final flagged alerts 
│     ├── non_alerts_MENAT_202503.csv # Customers with no alerts or suppressed 
│     └── intermediate_MENAT_202503.csv # Full data with flags/suppression 
│ 
├── logs/ # Auto-generated logs (created at runtime) 
│     └── log_YYYYMMDD.log # Log file for the current run 
│ 
└── utils/ # Modular helper scripts 
    ├── init.py 
    ├── date_utils.py # Calendar logic (2nd Wednesday, run month) 
    ├── data_loader.py # Loads thresholds, crypto, suppression 
    ├── emailer.py # Email notification logic 
    ├── logger.py # Logger setup 
    └── processor.py # Region processing + alert logic
