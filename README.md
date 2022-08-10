# Docker Review
## Docker Overview
Docker is an open platform for developing, shipping, and running applications. Docker enables you to separate your applications from your infrastructure so you can deliver software quickly. With Docker, you can manage your infrastructure in the same ways you manage your applications. By taking advantage of Docker’s methodologies for shipping, testing, and deploying code quickly, you can significantly reduce the delay between writing code and running it in production.
## Docker architecture
![This is an image](https://docs.docker.com/engine/images/architecture.svg)
### Benefits:
1. Fast, consistent delivery of your applications
2. Responsive deployment and scaling
3. Running more workloads on the same hardware
## Docker Usecases
- Microservices-based apps
  - This is because developers can deploy each microservice in a separate container and then integrate the containers to build out a complete application using orchestration tools.
  - Technically speaking, you could deploy microservices inside VMs or bare-metal servers as well. But containers' low resource consumption and fast start times make them better suited to microservices apps, where each microservice can be deployed and updated separately.
- Pre-deployment application testing
  - The ability to test applications inside Docker containers and then deploy them into production using the same containers is another major Docker use case.
- Early application development
  - By creating Docker container images for the app and executing them with Docker or another runtime, developers can test the app from a local development PC without execution on the host OS. They can also apply configuration settings for applications that are different from those on the host OS.
  - This is advantageous because application testing would otherwise require setting up a dedicated testing environment. Developers might do that when applications mature and they need to start testing them systematically. But, if you're just starting out with a new code base, spinning up a Docker container is a convenient way to test things without the work of creating a special dev/test environment.
- Multi-cloud or hybrid cloud applications
  - Docker containers are portable, which means they can move easily from one server or cloud environment to another with minimal configuration changes required.
- Deploying OS-agnostic applications
  - The same Docker container can typically run on any version of Linux without the need to apply special configurations based on the Linux distribution or version.
  - That said, there are limitations to this Docker use case. Docker containers created for Linux can't run on Windows and vice versa, so Docker is not completely OS-agnostic.
- Cost control
  - The efficiency of Docker containers relative to VMs makes Docker a handy option for teams that want to reduce how much they spend on infrastructure. By taking applications running in VMs and redeploying them with Docker, organizations will likely reduce their total resource consumption.
## When not to use Docker
- Security considerations
  - Applications that require strict isolation are better deployed in VMs than in containers, which don't isolate applications fully from each other or the host OS.
- GUI applications
  - Although it's technically possible to run GUI apps in Docker containers, this is harder than running command-line interface apps. This is why video games are not deployed using Docker, for instance.
- Small-scale deployments
  - Teams that deploy a small number of apps or don't update their apps frequently might be better off sticking with VMs, which are simpler to manage. The complexity of orchestrating Docker containers and managing storage for containers outweigh the benefits of Docker for small-scale deployments.
### conclusion
| Virtual Machines | Docker container |
| --- | --- |
| Hardware-level process isolation | OS level process isolation |
| Each VM has a separate OS | Each container can share OS |
| Boots in minutes | 	Boots in seconds |
| VMs are of few GBs | 	Containers are lightweight (KBs/MBs) |
| Ready-made VMs are difficult to find | Pre-built docker containers are easily available |
| VMs can move to new host easily | Containers are destroyed and re-created rather than moving |
| Creating VM takes a relatively longer time | Containers can be created in seconds |
| More resource usage | Less resource usage |

![This is an image](https://k21academy.com/wp-content/uploads/2020/05/2020_05_13_12_19_07_PowerPoint_Slide_Show_Azure_AZ104_M01_Compute_ed1_.png)
