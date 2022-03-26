# Benchmark Assessment Criteria
## Objective
In this exercise we ask you to create a console application that can generate benchmark data for Profit and Loss values and output it to a CSV file.
Profit and Loss is a key performance indicator used to compare one company against a set of others when deciding whether that company represents a good investment opportunity.

## What is a Benchmark?
A benchmark is just an average of values. They are often used in investment analysis to give context to the investment opportunity you are studying. 
For instance, if you are looking at the Profit and Loss (<b>PL</b>) values over time of a given company, you could compare it against the average of values of a similar set of companies, to see whether the company you are looking at is doing better or worse than the average for that type of company.

## Brief
You are tasked to generate a CSV file in a time series format for average profit/loss (<b>PL</b>) in GBP (you will need to use the exchange rate data from the API) for companies in the data set that match the sector, continent and investment stages of a specific company ("AJP") over a range of dates.

## Objectives
Pull the data and exchange rates provided by the API in the Floww.Technical.Benchmark.Api project and present it into the following format:

---
### benchmark.csv
* Filter the list based on a combination of Business Sector, Continent and Stage (for example FinTech, NA, and Seed) that match the values at the same date as company "AJP" and output a timeline of benchmarked (averaged) values based on that criteria, converting to the selected currency and ensuring the rules below are adhered to.
	* If a record doesn't have a Sector, then do not include the value in the final calculation.
	* If a record doesn't have a Continent, then do not include the value in the final calculation.
	* If a record doesn't have a Stage, then do not include the value in the final calculation.
	* Only create a benchmark value if there are at least 3 companies values at a given date that are being used to compare to ensure anonymity.
<details>
	<summary>benchmark.csv Examples</summary>

```
Console Output Example:
Example Console Output:
Selected Company: AJP
Selected Currency: GBP
```
```
Example CSV Output:
ValueDate,Value,Count
"01/01/2020",198.56,8
"01/02/2020",162.62,7
"01/03/2020",200.01,7
"01/04/2020",202.99,8
```

</details>

---

## Rules
* If there is no profit loss (<b>PL</b>) value then it shouldn't be included in the output.
* If there is no date/time value the it shouldn't be included.
* Benchmarks should only be calculated if there are 3 or more companies for a specific date/time.
* Values should be rounded to 2 decimal places.
* You can reference the API in your console application, but you should <b>not</b> edit the API code.
---

### Columns
| Name | Description |
| --- | --- |
| "sectors" | Sectors to show the benchmark for (FinTech, BioTech or AiBigData) |
| "continents" | Continents to show the benchmark for (EU, NA) |
| "stages" | Funding Round Stages to show the benchmark for(PreSeed, Seed, SeriesA, SeriesB, SeriesC) |
| "company" | Code for company selected to create benchmark for. Company List: AJP, JJB, EMM, SCL, MMF, PED, JCK, KDZ, LPL, PTH, JTT, JAB, AXW, JPL, JBH, MDW, AJB, KTG, SFH, LSW, MHS, SDM, RBF, DJT, GWM, ADR, TAA, VVD, JMT, JDH) |
| "currency" | Currency code to convert benchmark data values to (GBP, EUR or USD) |

## Summary Criteria

The finished solution **should:**
- Be written in C#.
- Be a console application.
- Include tests as appropriate.
- Include logging as appropriate.
- Contain documentation of your technical decisions.
- Be simple and concise.
- Use libraries where appropriate


The finished solution **should not:**
- Have advanced features, however discussion of anything extra you'd expect a production client to contain would be useful in the documentation.
> We give no credit for including any of the above in a submitted test, so please only focus on the "Shoulds" above.

## Other things to consider
If you do not understand something in the test, make your own assumptions and document those assumptions.
Please provide documentation (in a text file) to provide reasoning behind decisions taken in your code to help us understand why you have written the code the way you have.

---

#### Further Explanation
If, for example we asked you to provide the benchmark in USD for company MNO (a European FinTech company) we would be looking for the following:

| Date | MNO Stage | Value we're looking for |
| ---- | --------- | ----------------------- |
| Jan-20 | Seed | Average P&L value (converted to USD) of all European FinTech companies who are at Seed stage at Jan-20 |
| Feb-20 | Seed | Average P&L value (converted to USD) of all European FinTech companies who are at Seed stage at Feb-20 |
| Mar-20 | Seed | Average P&L value (converted to USD) of all European FinTech companies who are at Seed stage at Mar-20 |
| Apr-20 | Seed | Average P&L value (converted to USD) of all European FinTech companies who are at Seed stage at Apr-20 |
| May-20 | Seed | Average P&L value (converted to USD) of all European FinTech companies who are at Seed stage at May-20 |
| Jun-20 | Seed | Average P&L value (converted to USD) of all European FinTech companies who are at Seed stage at Jun-20 |
| Jul-20 | Seed | Average P&L value (converted to USD) of all European FinTech companies who are at Seed stage at Jul-20 |
| Aug-20 | Series A | Average P&L value (converted to USD) of all European FinTech companies who are at Series A stage at Aug-20 |
| Sep-20 | Series A | Average P&L value (converted to USD) of all European FinTech companies who are at Series A stage at Sep-20 |
| Oct-20 | Series A | Average P&L value (converted to USD) of all European FinTech companies who are at Series A stage at Oct-20 |
| Nov-20 | Series A | Average P&L value (converted to USD) of all European FinTech companies who are at Series A stage at Nov-20 |
| Dec-20 | Series A | Average P&L value (converted to USD) of all European FinTech companies who are at Series A stage at Dec-20 |
| Jan-21 | Series A | Average P&L value (converted to USD) of all European FinTech companies who are at Series A stage at Jan-21 |
| Feb-21 | Series A | Average P&L value (converted to USD) of all European FinTech companies who are at Series A stage at Feb-21 |
| Mar-21 | Series A | Average P&L value (converted to USD) of all European FinTech companies who are at Series A stage at Mar-21 |
| Apr-21 | Series A | Average P&L value (converted to USD) of all European FinTech companies who are at Series A stage at Apr-21 |
| May-21 | Series A | Average P&L value (converted to USD) of all European FinTech companies who are at Series A stage at May-21 |
| Jun-21 | Series A | Average P&L value (converted to USD) of all European FinTech companies who are at Series A stage at Jun-21 |
| Jul-21 | Series A | Average P&L value (converted to USD) of all European FinTech companies who are at Series A stage at Jul-21 |
| Aug-21 | Series B | Average P&L value (converted to USD) of all European FinTech companies who are at Series B stage at Aug-21 |
| Sep-21 | Series B | Average P&L value (converted to USD) of all European FinTech companies who are at Series B stage at Sep-21 |
| Oct-21 | Series B | Average P&L value (converted to USD) of all European FinTech companies who are at Series B stage at Oct-21 |
| Nov-21 | Series B | Average P&L value (converted to USD) of all European FinTech companies who are at Series B stage at Nov-21 |
| Dec-21 | Series B | Average P&L value (converted to USD) of all European FinTech companies who are at Series B stage at Dec-21 |
