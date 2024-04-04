# prometheus-demo
A demo to explore implementing a prometheus exporter implementation outside of otel


# Description
We are starting this project to explore how we can implement a custom prometheus exporter that would help implement the reset functionality. This is also to show how much we would actually need to maintain within Nirmata. 
Otel expects a reader interface
```
	provider := metric.NewMeterProvider(metric.WithReader(exporter))
	meter := provider.Meter(meterName)
```
that we will implement internally using the prometheus client_golang library and use all other otel functionality as needed

# Notes
This is still a WIP while we explore all options.
