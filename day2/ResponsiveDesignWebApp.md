# Reconsidering Responsive Design for Web Application Development

## Terminology
- Web Apps vs. Web Sites
  - Web App: a html5 application which is designed to consume, manipulate and show data that is tailored to you.
  - Web Site: the same for all folks. no tailoring.
- Web Apps vs. Hybrid Apps vs. Native Apps
  - Web Apps: hosted.
  - Hybrid App: Packaged using cordova or phone gap
  - Native App: downloaded as an app

## What is Responsive Design?
- Fluid Grids
- Flexible Images
- Media Queries

## Responsive Design: A history
- Coined by [Ethan Marcotte in 2010](http://alistapart.com/article/responsive-web-design)
- Responsive Design has older origin
- Responsive design works great for website with (semi) static content

## Different Appliance
- Smartphone vs Tablet vs. Desktop
- Native Controls
- Technology Features
  - Input: touch, tap, gestures, etc
  - Keyboard + Mouse
  - 3G/4G
  - GPS
- Screen size
- We haven't accounted for using the same device in different contexts
- Are Windows Mobile 10 and a PC different Appliances?

## Responsive vs. Adapative Design
- Responsive Design: One layout that changes
- Adaptive Design: Different layouts that are chosen at run time based on how the resource is being accessed

## Adaptive Design

### Feature Prioritization
- Prioritize features that are unique to a certain appliance
- Location specifics
- Different input methods

### Hilton Case Study
- On mobile:
  - Tech:
      - Keystore: Auth
      - Inter-App communication with Uber
      - Telephone - Call
  - Content Differences
    - Reservation history
    - Confirmation Number
    - Weather
- On Desktop
  - Focus on discovery

## Approaches
- Progressive enhancements as the appliance becomes more sophisticated
- Graceful degradation: every capability tends to be available on every device

## Sencha's Solutions for Mobile & Universal Apps
- Toolkits: classic & modern: separate view logic from business logic
- responsiveConfig - Responsive Design at runtime
- Device Profiles - Device Profiles for certain Devices at App Launch
- Platform Configs - Runtime platform config based on current device classification
- Device Themes - Cupertino(iOS), Mountain View(Android), Blackberry
- Responsive Design in CSS

## How to generalize this?
_not from presentation_
