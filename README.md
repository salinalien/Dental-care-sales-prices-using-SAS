# Dental-care-sales-prices-using-SAS
The analysis aims to determine if there is a significant difference in sale prices based on the presence or absence of Masonry Veneer.

## Code
#
ods graphics; 

proc ttest data=STAT1.ameshousing3 plots(shownull)=interval; 
    class Masonry_Veneer; 
    var SalePrice; 
    format Masonry_Veneer $NoYes.; 
    title "Two-Sample t-test Comparing Masonry Veneer, No vs. Yes"; 
run; 

title;

## The t-test results indicate the following:
- Mean SalePrice for properties without Masonry Veneer: $130,172
- Mean SalePrice for properties with Masonry Veneer: $154,705
- Significant difference in SalePrice between the two groups (p < 0.0001)
