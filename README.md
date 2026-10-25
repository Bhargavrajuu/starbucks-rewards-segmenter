# Starbucks Rewards Segmenter

AI solution 04 of 14 · Marketing · built for **Starbucks**

Prepared by **K Bhargav Raju**.

## Problem statement

A company treats its customers using broad demographic segments, resulting in inefficient campaigns. Develop an LLM-powered customer intelligence system that discovers meaningful behavioral segments from transaction and interaction data and recommends differentiated marketing strategies.

## Why Starbucks

Starbucks Rewards records what members buy, when, where and through which channel. That is far richer than age and income, so segments can be built on behaviour and each one gets its own offer.

## Algorithm

1. **Collect transactions and app data**: Visits, spend, time of day, mobile orders, food, offers
2. **Build RFM + behaviour features**: Recency, frequency, monetary plus 5 habit features
3. **Scale and reduce**: Standardise, then PCA to 2 dimensions for the map
4. **Cluster with K-means**: K-means++ for k = 3 to 7, pick by silhouette
5. **Validate segments**: Check that segments differ in value and offer response
6. **Profile and name**: Rule-based names; AI analyst can rename
7. **Strategy per segment**: Offer, channel, message and timing
8. **Track migration**: Compare old demographic groups with new segments

## Data

2,500 Rewards members with 6 months of transactions and app activity (sample data). All figures are illustrative and are not Starbucks's actual numbers.

## How to use

Open `index.html` in any web browser. No installation is needed; the whole tool is one self-contained file.

The controls panel lets you change number of segments, and the analysis reruns instantly. "New sample data" generates a fresh dataset.

## AI analyst panel

The "Ask the AI analyst" panel answers questions about the results in plain English through Claude. It works when the page is opened as a Claude artifact on claude.ai. Opened from GitHub, GitHub Pages or a local folder, all the models, charts and controls still run, and the panel shows that it is unavailable.
