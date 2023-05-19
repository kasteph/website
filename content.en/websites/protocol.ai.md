---
title: protocol.ai
plotly: true
---

# protocol.ai

This page shows performance metrics for the
website [protocol.ai](https://protocol.ai).

## Website Probes

{{< plotly json="../../plots/latest/web-vitals-probes-count-protocol.ai.json" height="150px" >}}

## Web-Vitals Metrics measured from Europe using Kubo {#web-vitals-barchart-protocolai-kubo-eu-central-1}

<small>[What do `CLS`, `FCP`, `LCP`, etc. mean?](#metrics) | [What do `Fatal`, `Undefined`, `Poor` etc. mean?](#values)</small>

{{< plotly json="../../plots/latest/web-vitals-barchart-protocol.ai-KUBO-eu-central-1.json" height="400px" >}}

## Website Probing Success rate from different Regions {#website-retrieval-errors-protocolai}

{{< plotly json="../../plots/latest/website-retrieval-errors-protocol.ai.json" height="350px" >}}

## Unique Website Providers per Day {#website-providers-protocolai}

{{< plotly json="../../plots/latest/website-providers-protocol.ai.json" height="350px" >}}

## Kubo Metrics by Region

### Time To First Byte {#website-metric-cdf-protocolai-kubo-ttfb}

{{< plotly json="../../plots/latest/website-metric-cdf-protocol.ai-KUBO-ttfb.json" height="320px" >}}

### First Contentful Paint {#website-metric-cdf-protocolai-kubo-fcp}

{{< plotly json="../../plots/latest/website-metric-cdf-protocol.ai-KUBO-fcp.json" height="320px" >}}

### Largest Contentful Paint {#website-metric-cdf-protocolai-kubo-lcp}

{{< plotly json="../../plots/latest/website-metric-cdf-protocol.ai-KUBO-lcp.json" height="320px" >}}

## Time To First Byte Kubo/HTTP Latency Ratio {#website-http-ratio-protocolai}

{{< plotly json="../../plots/latest/website-http-ratio-protocol.ai.json" height="500px" >}}

We calculated different percentiles for the Time To First Byte metric in different regions for website requests that were done via Kubo and via plain HTTP.
Then we divided the values of Kubo by the ones from HTTP. A resulting number greater than `1` means that Kubo was slower than HTTP in that region for that percentile.
Conversely, a number less than `1` means that Kubo was faster.

## Glossary

### Metrics

| Metric   | Description                                                                                 |    Good | Needs Improvement |     Poor |
|----------|---------------------------------------------------------------------------------------------|--------:|------------------:|---------:|
| **CLS**  | [Cumulative Layout Shift](https://web.dev/cls/)                                             | < 0.10s |           < 0.25s | >= 0.25s |
| **FCP**  | [First Contentful Paint](https://web.dev/fcp/)                                              | < 1.80s |           < 3.00s | >= 3.00s |
| **LCP**  | [Largest Contentful Paint](https://web.dev/lcp/)                                            | < 2.50s |           < 4.00s | >= 4.00s |
| **TTFB** | [Time To First Byte](https://web.dev/ttfb/)                                                 | < 0.80s |           < 1.80s | >= 1.80s |
| **TTI**  | [Time To Interactive](https://developer.chrome.com/docs/lighthouse/performance/interactive) | < 3.80s |           < 7.30s | >= 7.30s |

### Values

| Value                 | Description                                                                                          |
|-----------------------|------------------------------------------------------------------------------------------------------|
| **Good**              | The value was smaller than the `good` threshold (see [Metrics](#metrics))                            |
| **Needs Improvement** | The value was larger than the `good` but smaller than the `poor` threshold (see [Metrics](#metrics)) |
| **Poor**              | The value was larger than the `poor` threshold (see [Metrics](#metrics))                             |
| **Undefined**         | We could not gather the metric because of internal measurement errors (our fault)                    |
| **Fatal**             | We could not gather the metric because we could not retrieve the website at all                      |