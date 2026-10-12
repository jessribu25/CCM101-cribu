##Container Observability
404 Error Log Entry

172.17.0.1 - - [12/Oct/2026:08:37:29 +0000] "GET /hidden-admin-page HTTP/1.1" 404 153 "-" "curl/8.5.0" "-"
Application logs are essential for troubleshooting because they capture the specific request, the time it happened, and the response code for each event. This lets an engineer see exactly what a user did and where things went wrong, rather than relying on guesswork. If there were no logs, a general report like “the site isn’t working” would be almost impossible to trace to a specific cause.

The matching nginx error line is also in your screenshot, if you want a second line of evidence:

2026/10/12 08:37:29 [error] 29#29: *2 open() "/usr/share/nginx/html/hidden-admin-page" failed (2: No such file or directory), client: 172.17.0.1, server: localhost, request: "GET /hidden-admin-page HTTP/1.1", host: "localhost:8080"

##Real-Time Resource Usage (docker stats)

At the time of the screenshot, the `client-website` container was using:
   * Memory Usage: 2.711MiB / 1.859GiB
   * CPU %: 0.00%

These numbers confirm the container is running efficiently and is nowhere near exhausting the host's available CPU or memory.
