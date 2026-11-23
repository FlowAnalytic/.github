![FlowAnalytic at a stadium and transit hub](flowanalytic-stadium-city.png)

![FlowAnalytic drone swarm tracking and alerts](flowanalytic-drone-swarm-alert.png)

![FlowAnalytic: Real-Time Analysis of Dense Motion](flowanalytic-crowd.png)

We’re building **FlowAnalytic**, software that turns video into real-time measurements of dense, organized motion, with applications in public safety, defense, and life sciences.

Control rooms monitor hundreds of camera feeds, yet dense crowds remain difficult to interpret. Crowd crushes develop under high density and compression, often alongside counterflow, convergence, and crowd turbulence—patterns that operators may struggle to spot across many screens. Analytics that count people or follow a single dominant flow do not fully describe these overlapping movements.

FlowAnalytic measures motion at scales ranging from individual objects to thousands of tracked features at once. It combines multiple detection methods with three tracking algorithms to measure position, displacement, speed, and direction; reconstruct trajectories; and separate intersecting flows. It also quantifies how speed and direction vary within a scene. We have applied FlowAnalytic to more than 70 distinct motion scenarios.

Tracking reveals the liaisons between moving objects—where paths cross, flows converge, and an encounter may become a collision or a confrontation. We’re building FlowAnalytic to recognize these dangerous liaisons early enough to help prevent them. A crowd need not become a confrontation; an approaching drone need not become an impact. What happens where paths meet is not beyond our control.

**Defense and security**

We have applied FlowAnalytic to military-drone footage, dense drone swarms, drone-swarm engagement, crowds, airport terminals, border-control scenes, pedestrian crossings, and traffic.

FlowAnalytic also runs directly inside network surveillance cameras as a camera application. It analyzes the camera’s own live video in real time, without a separate computer or cloud upload. We tested on-camera processing on a remote surveillance camera and built application packages for two generations of camera processors.

**Live feeds and VMS integration**

We connected FlowAnalytic to live feeds from several locations: a busy pedestrian area in New York City (a public live stream and a city traffic camera), a terminal area at Düsseldorf Airport, and a public highway camera. We also tested it on a benchmark crowd dataset from an evacuation-safety project funded by the German Federal Ministry of Education and Research. Processing ran entirely on our cloud server alongside an enterprise video management system (VMS), which received each live feed while FlowAnalytic tracked its motion in real time.

Alert rules are configured for each scene. A speed rule fires when mean flow speed stays above a limit, set from a baseline of normal motion, for a sustained period. A new-flow rule fires when an additional movement stream appears. A counterflow rule fires when an estimated group of four or more people moves against the expected direction for at least three seconds, and keeps a single incident open while the condition lasts. Each alert is sent to the VMS, which creates an alarm linked to that camera.

In live tests, the alerts behaved as configured. A steady city-center crowd triggered no speed alarms, while a public highway feed produced alarms during sustained speed increases, each backed by the measurements that triggered it. On a live airport feed, alarms appeared in the VMS as new movement streams formed. These tests guide how alerts are tuned to each scene: our counterflow rule responds to groups moving against the expected direction for several seconds and reports each episode as a single incident. When we replayed a recorded counterflow experiment through the VMS, a sustained counterflow episode produced a single alarm within seconds—one alarm for the whole event rather than repeated alerts—and a repeat run reproduced the result.

Within a configured VMS workflow, operators can receive camera-linked alarms in their monitoring client, investigate incidents, and display the relevant feed on a video wall. Our goal is to give them earlier visibility into counterflow, sudden increases in speed, dispersal, and flows converging at choke points—supporting decisions to open exits, redirect people, or dispatch staff.

“Beyond the walls of intelligence, life is defined.”

**What we’re building next**

We’re bringing on-camera processing and VMS alerts together in one demonstration: FlowAnalytic running inside a surveillance camera overlooking a live crowded scene, sending alerts through the VMS, and preserving evidence that explains each trigger.

The camera application now includes speed measurements based on camera-frame timestamps, an alert rule applied within a selected region, and a rolling history of measurements and tracking vectors before and after each alert. Next, we are connecting camera-generated events to the VMS and completing synchronized visual evidence capture.

**“It’s beyond my control”**

We welcome pilot sites with surveillance cameras overlooking busy pedestrian areas, including transit stations, plazas, venue entrances, and shopping streets.

Beyond existing street and venue camera networks, public-safety applications include compact cameras for police cars, fire trucks, schools, and border-patrol operations. Defense applications include drone and drone-swarm tracking and perimeter monitoring.

I would like to develop a field pilot for our real-time crowd-flow analysis system.

We have already conducted multiple tests using live camera feeds from several locations, including sites in New York City and Düsseldorf Airport. The system tracks movement, displays motion vectors over the live video, and generates automated alerts within security video-management software. These tests demonstrate the system operating on live pedestrian activity across different locations.

The project brings together expertise that covers the path from detecting movement to operating a system across multiple sites. Our advisors’ backgrounds include:
- software that searches organizational information and produces traceable matches, which could help operators connect alerts with response procedures, site instructions, and previous incidents;
- platforms for deploying and managing AI applications across on-site servers and cloud infrastructure, relevant to allocating computing resources, distributing updates, controlling access, and monitoring installations as camera numbers grow;
- communications and information systems supporting military operations, which add a perspective on reliable alert delivery, secure access, interoperability, and recovery from connection failures.

The camera and video-management ecosystem provides the practical foundation for deployment. Network cameras supply the live feeds, while compatible camera platforms offer the possibility of running analysis locally. Integration with video-management software places automated alerts alongside the feeds, recordings, and incident-handling tools operators already use. Data-engineering and analytical capabilities could then connect those alerts with access-control events, occupancy information, and incident records. Distributors, resellers, and integrators provide the channels through which institutional customers can acquire, install, and support the system.

I would like to build on those results by working directly with a local operator and security integrator at a station passage, venue entrance, or pedestrian bottleneck. The objectives would be to:
- configure the system for the site and agree with the operator which movement patterns warrant attention;
- evaluate automated alerts with operators, comparing detections with activity on the ground and measuring missed events, nuisance alerts, and detection delay under changing crowd and lighting conditions;
- demonstrate the complete response workflow: identify unusual movement, deliver an automated alert, review the associated video, document the operator’s response, and establish which alerts warrant action;
- define deployment requirements, including camera compatibility, local versus central processing, network access, installation costs, and ongoing support.

Being there would let me investigate questionable alerts at the site, assess camera positioning and network constraints with the installer, and determine whether processing should run near the cameras or on a central server. Meetings with a local integrator would establish installation costs, maintenance responsibilities, and support requirements.

I would like to generate a documented field evaluation, a live operator demonstration, and a concrete deployment proposal. After identifying a suitable site operator and security integrator, I would plan a visit around confirmed camera access and meetings.

- [Contact us](mailto:alexandre.matov@gmail.com)
