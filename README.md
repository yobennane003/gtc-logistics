# AfCFTA Rules of Origin – Automated Logistics Conformance Engine

[![Validate AfCFTA Rule Execution](https://github.com/yobennane003/gtc-logistics/actions/workflows/test-rule.yml/badge.svg)](https://github.com/yobennane003/gtc-logistics/actions)

## Overview
This repository provides an executable implementation of trade and customs rules under the **African Continental Free Trade Area (AfCFTA)** agreement, specifically focusing on Chapter 31 commodities (Fertilizers and Phosphate derivatives).

The project aligns with the **Data With Direction Specification (DWDS)** and demonstrates deterministic rule computation within automated cross-border logistics pipelines (GeoTradeCorridors).

## Architecture & Components
* **`/rules`**: Formal rule expressions in JSON format adhering to DWDS structures.
* **`/tables`**: Decision tables and tariff lookup structures (`.csv`).
* **`/tests`**: Sample transaction payloads reflecting real maritime trade corridors (e.g., Jorf Lasfar to Mombasa).
* **`.github/workflows`**: Automated continuous conformance testing using GitHub Actions.

## Origin Calculation Formula
Pursuant to AfCFTA Annex 2 on Rules of Origin, the Value Added Content (VAM) is evaluated as follows:

$$VAM = \left( \frac{\text{Ex-Works Price} - \text{VNM}}{\text{Ex-Works Price}} \right) \times 100$$

Where:
* **Ex-Works Price**: Final factory/port exit valuation.
* **VNM**: Value of Non-Originating Materials.
* **Threshold**: $\ge 35\%$ for preferential tariff qualification ($0\%$ import duty).
