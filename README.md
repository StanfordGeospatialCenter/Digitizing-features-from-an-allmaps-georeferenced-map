# From Paper Maps to Digital Data: A Complete Workshop Series

## Introduction

This repository contains a comprehensive **two-part workshop series** that teaches you how to unlock spatial data hidden in historical scanned maps. Whether you're a researcher, librarian, cartographer, or GIS enthusiast, these workshops will guide you through the complete workflow: from finding a historical map online, to georeferencing it, to extracting and digitizing real-world features from it.

---

## The Challenge: Paper Maps Hold Valuable Spatial Data

Millions of historical maps exist in digital form, stored in institutions like the Library of Congress, David Rumsey Map Collection, and Wikimedia Commons. These maps contain invaluable information about how places looked in the past—where ports operated, which railways connected cities, how urban boundaries evolved, and more.

The problem? **Most of this spatial data remains trapped in static images.** You can view a scanned historical map online, but you can't easily extract its features or overlay it with modern data. This workshop series solves that problem by teaching you a practical, efficient workflow.

---

## How These Two Workshops Work Together

### Part 1: Georeferencing with Allmaps

### Part 2: Digitizing Features in ArcGIS Online

Together, these workshops show you how to **release spatial data from historical maps in a sustainable, collaborative way**.

```
Historical Map (scanned image)
           ↓
    [WORKSHOP 1: GEOREFERENCE]
    Add ground control points
           ↓
    XYZ Tile Layer (georeferenced)
           ↓
    [WORKSHOP 2: DIGITIZE]
    Extract features into structured data
           ↓
    GeoJSON file (spatial data)
```

### Why This Workflow?

1. **No Derivative Files**: Unlike traditional GIS workflows that require downloading and storing large georeferenced image files, this approach stores only lightweight georeferencing metadata on Allmaps. The original map stays on its host institution's servers.
2. **Instant Web Access**: Allmaps converts your historical map into web-standard XYZ tiles that work in any web mapping application (Google Maps, ArcGIS Online, Leaflet, Mapbox, etc.).
3. **Collaborative and Shareable**: Your georeferencing work (ground control points) can be shared and improved by others. Your digitized data (GeoJSON) is a standard format that works with any GIS software.
4. **Scalable**: Once you master this workflow on one map, you can apply it to dozens or hundreds of maps from different institutions and time periods.
5. **Open and Sustainable**: All tools used (Allmaps, ArcGIS Online, GeoJSON) are either free or based on open standards, ensuring your work remains accessible for years to come.

---

## Workshop 1: Georeferencing with Allmaps

**What You'll Learn:**

- How to find historical maps in online repositories (David Rumsey Map Collection, etc.)
- Understanding IIIF (International Image Interoperability Framework) and why it matters
- Creating ground control points (GCPs) to align a historical map to modern geography
- Handling non-standard coordinate systems and graticules
- Exporting your georeferenced map as web-standard XYZ tiles

**Time Required:** 45–90 minutes (depending on map complexity)

**Key Takeaway:** You'll have a georeferenced historical map accessible as tiles that can be used in web mapping applications or overlaid with modern data.

➡️ **[Read Workshop 1: Georeferencing with Allmaps](GEOREFERENCING-WITH-ALLMAPS.md)**

---

## Workshop 2: Digitizing Features in ArcGIS Online

**What You'll Learn:**

- Creating feature layers (points and lines) in ArcGIS Online
- Defining data schemas with fields and controlled vocabularies (domains)
- Using the georeferenced historical map as a reference layer
- Manually digitizing features (ports, railroads, etc.) into structured data
- Configuring popups, symbology, and interactive editing apps
- Exporting your digitized data as GeoJSON for use in other GIS software

**Time Required:** 90–180 minutes (depending on the number of features)

**Key Takeaway:** You'll have extracted spatial features from a historical map into a structured, standardized dataset (GeoJSON) that can be analyzed, shared, or integrated with other GIS data.

➡️ **[Read Workshop 2: Digitizing Features in ArcGIS Online](DIGITIZING-FEATURES.md)**
