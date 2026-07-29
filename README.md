# The NYC Affordability Index

A monthly read on what New Yorkers earn and what it costs them to live here.

Every figure comes from a named public source and is refreshed on a fixed
schedule. Nothing is modeled or interpolated silently; where a number cannot
yet be established honestly, the card says so.

- **[The index](https://vitalcity-nyc.github.io/nyc-affordability-index/)** — pay and prices, refreshed monthly
- **[What already exists](https://vitalcity-nyc.github.io/nyc-affordability-index/background.html)** — the deeper annual measures this index is built against
- **[Methodology](https://vitalcity-nyc.github.io/nyc-affordability-index/methodology.html)** — estimators, geography, lags, revisions and the claims this page does not support

## Earnings

Pay is measured with **one** source: BLS Current Employment Statistics average
hourly and weekly earnings for the New York-Newark-Jersey City metro. The
Employment Cost Index and QCEW are deliberately not carried — both are
quarterly and land on different vintages, so placing either beside a monthly
reading invites comparisons between numbers that describe different periods.

## Rents

StreetEasy series are **asking medians**: the advertised price of the units
that happen to be vacant and listed. They are not what sitting tenants pay.

## Rebuilding the data

```
python3 fetch-bls.py && python3 compute-bls.py && python3 build-bls-section.py
```
