# Scraping Rock & Mineral Clubs with XPath

**Date:** July 5, 2026
**Project for Lede Data Analysis in Journalism**

## Summary

Scrapes the [450+ Rock and Mineral Clubs Across the USA](https://rocktumbler.com/blog/rock-and-mineral-clubs/)
directory from rocktumbler.com using `requests` and `lxml` XPath selectors. The page lists clubs in
55 state tables; the scraper walks each table's rows to pull the club name, website URL, city, and
state heading into a tidy dataset.

## Source

- Site: https://rocktumbler.com/blog/rock-and-mineral-clubs/

## Fields

| Field | XPath |
|---|---|
| Club name | `.//a` |
| Club URL | `.//a/@href` |
| City | `.//td[@width = "40%"]` |
| State | `.//preceding-sibling::table//h3//text()` |

## Files

- `hw1-rock_v3_july8Inclass_review.ipynb` — the scraper

## Requirements

`requests`, `pandas`, `lxml`, `tqdm`
