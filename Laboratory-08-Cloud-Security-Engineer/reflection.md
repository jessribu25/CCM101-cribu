# 1. Reflection

A host-based firewall keeps a server protected even when the physical network perimeter has been breached, because it enforces security on the server itself rather than only at the network's edge. If an attacker gets past a router or network firewall and reaches the machine directly, UFW still checks every connection attempt against its own rules and drops anything not explicitly permitted. The server never assumes the network around it is trustworthy.

Managing open ports is essential to shrinking a server's attack surface, since each open port is a possible way in. A port serving software with a known vulnerability practically invites an attack. Closing every port the server doesn't need removes whole categories of attacks before anyone can attempt them.

Exposing a database port like 3306 to the public internet is dangerous because anyone online can try to connect straight to the database and skip the application layer completely. Databases usually store the most sensitive information in a system, so one that faces brute-force login attempts or known exploits directly can be compromised without an attacker ever touching the web application in front of it.

This mission changed how I think about server security. Before configuring UFW myself, I hadn't fully realized that a newly deployed server is vulnerable from the moment it goes online, not only after months of neglect. One missed step, such as enabling the firewall before allowing SSH, can lock out an administrator just as easily as a misconfigured rule can leave a server wide open.

# 2. GitHub Portfolio

My GitHub portfolio now shows eight completed missions, each building on the one before it, from basic Linux navigation in Mission 1 to infrastructure as code, observability, and now security hardening. Looking at the repository as a whole, it feels less like a collection of unrelated assignments and more like steady progress toward real cloud engineering practice.
