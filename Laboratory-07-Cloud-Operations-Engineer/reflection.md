##Reflection

Checking the host server's resources matters even when containers are running well, because every container depends on the host underneath it. A container can be set up perfectly and still fail if the machine it runs on runs out of RAM or disk space. A container can never perform better than the hardware hosting it allows.

If a user reported that they couldn't log in, the `docker logs` command would show me the exact HTTP requests reaching the server around the time of the complaint. I could look for failed login attempts, 500-level server errors, or requests that never finished. These would show whether the issue lies with the client, the network, or the application itself.

Monitoring logs and monitoring metrics differ in what each one reveals. Logs (Checkpoint 4) are detailed, timestamped records of individual events, and they explain why something happened. Metrics (Checkpoint 5) are numerical measurements, such as CPU percentage and memory usage, collected over time, and they show that something is happening right now. Monitoring warns you that a problem exists, while logs let you dig into its cause.

Large companies running thousands of containers depend on centralized tools instead of checking each one by hand. A tool like Prometheus collects metrics from every server and container at regular intervals and keeps them in a time-series database. Grafana then turns that data into dashboards that engineers can read at a glance. This approach scales across huge fleets of machines, which running `docker stats` on one container at a time never could.

2. My ability to troubleshoot Linux environments has clearly improved since this lab. Rather than guessing at a problem from its symptoms, I now naturally turn to real data first. I check resource usage with `free`, `df`, and `top`, then compare that against container logs and live metrics before drawing any conclusion about what is actually wrong.
