# Google-Ads-Search-Query-Mining
This Google Ads Script analyzes Search Query Report data and identifies the words and phrases that contribute most to account performance
SEARCH QUERY MINING TOOL (UNIVERSAL CLIENT VERSION)

Purpose:
This Google Ads Script analyzes Search Query Report data and identifies the words and phrases that contribute most to account performance.

The script breaks search terms into:

* Single words (1-Grams)
* Two-word phrases (2-Grams)
* Three-word phrases (3-Grams)
* Four-word phrases (4-Grams)
* Five-word phrases (5-Grams)

For each phrase, the script calculates:

* Query Count
* Impressions
* Clicks
* Cost
* Conversions
* Conversion Value
* CTR
* CPC
* Conversion Rate
* Cost per Conversion
* ROAS

Use Cases:

* Find high-converting search themes
* Discover profitable keyword opportunities
* Identify negative keyword opportunities
* Analyze account-wide search intent patterns
* Compare performance by phrase length
* Build keyword expansion lists

Client Setup Required:
Before using for a new client, only update:

1. SPREADSHEET_URL

   * Create a copy of the reporting spreadsheet.
   * Paste the new spreadsheet URL.

2. Optional campaign filters

   * CAMPAIGN_NAME_CONTAINS
   * CAMPAIGN_NAME_DOES_NOT_CONTAIN

Everything else can remain unchanged.

Recommended Schedule:

* Weekly
* Monthly

Recommended Date Range:

* Last 90 Days (default)

Safe To Run:
YES

This script:
✓ Reads Google Ads data
✓ Reads search queries
✓ Reads negative keywords
✓ Writes results to a spreadsheet

This script DOES NOT:
✗ Pause campaigns
✗ Change bids
✗ Add keywords
✗ Add negatives
✗ Edit ads
✗ Modify budgets
✗ Change account settings

**Universal Configuration Section**

**Replace your current settings section with this:**

/******************************************************************************
CLIENT CONFIGURATION
ONLY CHANGE THESE VALUES FOR EACH CLIENT
******************************************************************************/

// ===== REQUIRED =====
var SPREADSHEET_URL = "PASTE_CLIENT_SPREADSHEET_URL_HERE";

// ===== OPTIONAL FILTERS =====
var CAMPAIGN_NAME_CONTAINS = "";
var CAMPAIGN_NAME_DOES_NOT_CONTAIN = "";

// ===== DATE RANGE =====
var DATE_RANGE = "LAST_90_DAYS";

// OPTIONS:
// LAST_7_DAYS
// LAST_14_DAYS
// LAST_30_DAYS
// LAST_60_DAYS
// LAST_90_DAYS
// THIS_MONTH
// LAST_MONTH

/******************************************************************************
ADVANCED SETTINGS
USUALLY NO NEED TO CHANGE
******************************************************************************/

var CURRENCY_SYMBOL = "$";

var IGNORE_PAUSED_CAMPAIGNS = false;
var IGNORE_PAUSED_ADGROUPS = false;
var CHECK_NEGATIVES = true;

var MIN_NGRAM_LENGTH = 1;
var MAX_NGRAM_LENGTH = 5;

var CLEAR_SPREADSHEET = true;

/******************************************************************************
THRESHOLDS
******************************************************************************/

var QUERY_COUNT_THRESHOLD = 0;
var IMPRESSION_THRESHOLD = 10;
var CLICK_THRESHOLD = 0;
var COST_THRESHOLD = 0;
var CONVERSION_THRESHOLD = 0;



