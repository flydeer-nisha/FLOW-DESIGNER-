# Auto Ticket Classification using Flow Designer - ServiceNow
Platform: ServiceNow Yokohama / Washington

Objective: Automatically classify incoming Incidents / Catalog Tasks based on keywords and assign to correct Assignment Group and Priority using Flow Designer.

Use Case:
If Short Description contains "laptop", "hardware", "keyboard" -> Assign to Hardware, Category: Hardware
If contains "password", "login", "access" -> Assign to Service Desk, Category: Software
If contains "network", "wifi", "vpn" -> Assign to Network, Category: Network
If contains "server down", "critical" -> High Priority

Flow Name: Auto Ticket Classification
Application: Global
Trigger: Incident Created / Updated

## Implementation Summary
1. Created Flow in Flow Designer
2. Added Decision logic based on Short Description keywords
3. Update Record action to set Assignment Group, Category, Priority
4. Added Work Notes for audit
5. Tested with 4 test cases - all passed
