# Smart India Hackathon Workshop
# Date: 29-10-2026
## Register Number: 212225240151
## Name: Sivasakthi S
## Problem Title
SIH 1710: Enhancing Navigation for Railway Station Facilities and Locations
## Problem Description
Background: Railway stations are complex environments with numerous facilities and locations such as ticket counters, platforms, restrooms, food courts, and waiting areas. Passengers often face difficulties in navigating these spaces, especially in large or unfamiliar stations. Efficient and user-friendly navigation systems are crucial for improving passenger experience, reducing congestion, and ensuring timely travel connections. Description: The problem involves developing a comprehensive navigation solution for railway stations that assists passengers in locating various facilities and destinations within the station premises. This includes creating detailed maps, providing real-time directions, and integrating features such as accessibility options for individuals with disabilities. The solution should be intuitive, easy to use, and accessible via multiple platforms, including mobile devices and digital kiosks. Key challenges include updating navigation information in real-time, ensuring accuracy, and accommodating the diverse needs of all passengers. Expected Solution: The expected solution is a multi-platform navigation system that provides detailed, real-time directions to all facilities and locations within a railway station. This system should include: A mobile application with 3D interactive maps and step-by-step navigation. Digital kiosks located throughout the station with touch-screen interfaces. Voice-guided navigation for visually impaired passengers. Regular updates to reflect changes in station layout and facility locations. Integration with existing railway apps and services for seamless user experience. The solution should enhance the overall passenger experience by reducing confusion, saving time, and improving accessibility within the station.

## Problem Creater's Organization
Ministry of Railway

## Idea
RailGuide 3D uses a digital indoor map and a route-planning engine to guide passengers from their current location to a selected station facility.
Main modules:

1. Interactive station map
Displays platforms, entrances, stairs, lifts, corridors, ticket counters, restrooms, and other points of interest. Passengers can select a destination and view a highlighted route.

2. Accessible route planner
Calculates routes based on distance, accessibility requirements, stairs, lift availability, and temporary obstructions. It recommends alternatives when a route is unsuitable.

3. Smart kiosk and QR handoff
Passengers select their destination on a station kiosk. The kiosk displays directions and a QR code that opens the same route on a compatible mobile device.

4. Voice and landmark guidance
Reads instructions such as “Continue along the corridor and turn left after the ticket counter.” Supports large text, screen readers, and high-contrast display settings.

5. Station information management
Authorized staff update facility locations, opening status, lift outages, corridor closures, and map changes. The system records when information was last verified.

Important technical limitation: 
         Indoor positioning is not automatically available from GPS. A prototype can use a manually selected starting point or QR-based location checkpoints. Live positioning requires suitable infrastructure, such as BLE beacons, Wi-Fi positioning, or other installed and validated technologies.
## Proposed Solution / Architecture Diagram
<img width="1424" height="1816" alt="mermaid-diagram (1)" src="https://github.com/user-attachments/assets/b6f8306e-0e07-4577-8070-a16a2fc3414d" />


How the system works
1. The passenger selects a station and a destination.
2. The system identifies the starting point, either from a supported positioning method or a manually selected checkpoint.
3. The route engine calculates a suitable path through the station map.
4. Accessibility rules remove unsuitable paths when an accessible route is requested.
5. The interface displays the route and provides text or voice directions.
6. If a passage or facility becomes unavailable, authorized staff update its status and the system recalculates affected routes.
7. A kiosk can transfer the selected destination and route reference to a passenger's phone through a QR code.

## Use Cases
<img width="2306" height="3114" alt="mermaid-diagram" src="https://github.com/user-attachments/assets/f712b948-d776-4074-b18d-eb92ad5f53dd" />


Use-case relationships
- Include: Getting directions includes selecting or searching for a destination.
- Extend: Accessible routing extends normal route planning when accessibility preferences are enabled.
- Extend: Voice guidance extends navigation when requested.
- Extend: QR handoff extends navigation when the passenger wants to continue on a mobile device.
The diagram is a high-level use-case view. For a formal UML submission, represent use cases as ovals inside a system boundary, actors outside it, and label dashed dependency arrows <<include>> or <<extend>>.

## Technology Stack


**Frontend:** React.js, HTML, CSS, JavaScript

**Mobile Application:** React Native

**3D Map Visualization:** Three.js

**Backend:** Python Flask

**Database:** PostgreSQL

**Route Planning Algorithm:** Dijkstra’s Algorithm / A* Algorithm

**Voice Navigation:** Web Speech API / Text-to-Speech

**QR Code Integration:** QR Code Generator and Scanner

**Indoor Positioning:** QR Checkpoints / BLE Beacons

**Authentication:** Role-Based Authentication

**Version Control:** Git and GitHub

**Deployment:** Cloud Hosting

## Dependencies

**Frontend Dependencies:**
- react
- react-dom
- react-router-dom
- three
- @react-three/fiber
- @react-three/drei
- axios
- lucide-react

**Backend Dependencies:**
- Flask
- Flask-CORS
- Flask-SQLAlchemy
- psycopg2-binary
- python-dotenv
- NetworkX

**Navigation Dependencies:**
- Dijkstra's Algorithm / A* Algorithm
- Indoor Station Map Data
- Accessibility Route Data

**Voice Navigation Dependencies:**
- Web Speech API
- Browser Text-to-Speech Support

**QR Code Dependencies:**
- qrcode
- html5-qrcode

**Database Dependencies:**
- PostgreSQL
- SQLAlchemy

**Development Dependencies:**
- Node.js
- npm
- Python 3.11+
- Git
- GitHub
