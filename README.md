
This dataset captures performance metrics averaged over 20-second intervals from approximately one million Pods belonging to over 90,000 applications across selected clusters. The data was collected during weekday evening peak hours in October 2024, outside of major promotional sale periods.

# Structure

```
.
├── README.md
└── data
    ├── raw_data.csv  # dataset 
    └── raw_data_sampled.csv  # random 100 rows of the dataset as a sample
```

##  dataset structure

Each row in the dataset corresponds to a Pod and includes basic metadata (e.g., machine type, application) as well as performance metrics.

1.Basic Information

- `pod_id` : Anonymous Pod identifier — a unique numeric ID assigned to each Pod.
- `app_id` : Anonymous application identifier — a unique numeric ID assigned to each application.
- `business_type` : Business type, including `e-commerce` and `search-recommendation`.
- `cpu_model` : CPU microarchitecture model, such as `Skylake` or `Ice Lake`.

2.CPU Performance Metrics of Pod

- `pod_cpu_used_cores` : Number of CPU cores used by the Pod.
- `pod_cpu_cpi` : Cycles Per Instruction for the Pod.
- `pod_cpu_lv1_retiring` etc. : Top-Down Microarchitecture Analysis (TMA) performance metrics.

3.Node-Level Metrics

- `node_cpu_usage`: CPU utilization for the entire node.
- `node_uncore_imc_bw_util`: Memory bandwidth utilization for the entire node.
- `node_uncore_imc_latency_ns`: Memory access latency for the entire node (in nanoseconds).