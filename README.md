# **Workshop Tutorial: Digitizing French Ports and Railroads in ArcGIS Online**

## **Introduction**
This tutorial will guide you through creating an **ArcGIS Online** application for digitizing **ports** and **railroads** using a historical map of French ports and railroads. The goal is to convert key features from the map into geospatial data.

### **About the XYZ Tiles**
The map used for this digitization task is accessible as an **XYZ tile layer** via a **IIIF manifest**. This setup enables viewing and digitizing the historical map within ArcGIS Online.

- **IIIF Manifest URL**:  
  `https://purl.stanford.edu/zc368qw3281/iiif/manifest`
  
- **Viewer Link**:  
  [Stanford Digital Repository Viewer](https://purl.stanford.edu/zc368qw3281)
![alt text](./images/image.png)

- **Allmaps.org Link**
- https://editor.allmaps.org/#/collection?url=https%3A%2F%2Fpurl.stanford.edu%2Fzc368qw3281%2Fiiif%2Fmanifest&image=d95dc4e2f0f60fb8

![alt text](./images/screenshot%202025-02-08%20at%2012.30.18 PM.png)
---

## **Step 1: Login to ArcGIS Online**
1. Open a web browser and navigate to [Stanford's ArcGIS Online Org](https://stanford.maps.arcgis.com):  https://stanford.maps.arcgis.com  
   ![alt text](<images/screenshot 2025-02-08 at 12.36.23 PM.png>)
2. Click **Sign In**.

![alt text](<images/screenshot 2025-02-08 at 12.38.27 PM.png>)

3. Click the blue **Stanford University** button

3. You should be bounced to Stanford's SIngle SIgn-On (SSO). Use your Stanford SUNetID and Password to login

---

## **Step 2: Create a New Feature Dataset**
1. Click **Content** in the top menu.
2. Select **New Item** → **Feature Layer** → **Define Your Own Layer**.

![alt text](<images/screenshot 2025-02-08 at 12.42.32 PM.png>)

![alt text](<images/screenshot 2025-02-08 at 12.45.54 PM.png>)

3. Under "Specify name and type" Add **Lines and Points** as the geometry type and name the layers `Ports` and `Railroads`

![alt text](<images/screenshot 2025-02-08 at 1.09.46 PM.png>)

4. Click **Next**, and name the dataset **french_ports_railroads_[your initials or SUNetID]** 

![alt text](<images/screenshot 2025-02-08 at 12.50.27 PM.png>)

2. Click **Save**.

---

## **Step 3: Customize the Data Schema**

At this point, you should be redirected to the **Details Page** for the **french_ports_railrods_SUNetID** Layer.

### **Adding Fields (Columns)**
![alt text](<images/screenshot 2025-02-08 at 3.23.21 PM.png>)
1. Click on **Data** at the top of the **Details Page**.
2. CONfirm that `Layer:Ports` is selected in the **Layer** Dropdown, And click on **Fields** 
 to change to the **Fields** view.
 
 ![alt text](<images/screenshot 2025-02-08 at 3.25.56 PM.png>)
3. Click on the **+Add** Button and use the following image to fill the **Add Field** dialog.

![alt text](<images/screenshot 2025-02-08 at 3.27.51 PM.png>)

4. Repeat the previous step to add and define the following fields for the dataset (*note that you will change to the Railroads Layer and add it's new fields*):

| Field Name       | Data Type | Length | Description                              |
|------------------|-----------|--------|------------------------------------------|
| `port_label`     | Text      | 50     | Name or identifier for the port.         |
| `port_type`      | Text      | 50     | Classification of the port (major/minor).|
| `railroad_label` | Text      | 50     | Name or identifier for the railroad.     |
| `notes`          | Text      | 255    | Additional observations or comments (both layers).     |

---

## **Step 4: Create a Controlled Vocabulary List for a Field (domain)**

To standardize the input for `port_type`, create a domain for controlled vocabulary:

1. From the **Data>Fields** page in the feature layer Details for the `Ports Layer`, click on the `port-type` Field value to open it's details page.
2. Click on **Create List**, create the following values:
   - **Port Type**: Add the values:
     - **Major**
     - **Minor**

![alt text](<images/screenshot 2025-02-08 at 3.41.58 PM.png>)
3. Click Save to assign this list (domain) to the `port_type` field.

![alt text](<images/screenshot 2025-02-08 at 3.43.31 PM.png>)

---

## **Step 5: Create an Editing Group**
Here, we will create a group that allows anyone with membership to edit the items that are shared with the group. In this case, we will share our Feature Layers to the group, so that we can share the work of digitizing features from our map. 

1. Click on the **Groups** link at the top of the page, then click **Create Group**.  

| Setting | Description |
|---------|-------------|
| Name | **"OSS Map Editors [SUNetID]"**. |
| Group visibility | **All organization members** |
| How can people join this group? | **By Request** |
| Who can contribute | **All group members** |
| Enable | **Allow group members to update all items**. |
| Who can see full members list | **Anyone who can view the group** |  

1. Check the **Shared Update** option, to allow editing by group members
2. Click **Save**

![alt text](<images/screenshot 2025-02-09 at 2.19.23 PM.png>)
---

## **Step 6: Create a Map**
1. Click **Map** in the ArcGIS Online menu.
2. Click **Add** → **Add Layer from URL**.

![alt text](<images/screenshot 2025-02-09 at 2.20.54 PM.png>)

3. Paste the **XYZ tile URL** generated from the IIIF manifest (This can be found on the [**Results** page of the Allmaps Editor](https://editor.allmaps.org/#/results?url=https%3A%2F%2Fpurl.stanford.edu%2Fzc368qw3281%2Fiiif%2Fmanifest&image=d95dc4e2f0f60fb8) for the map we are working with).

![alt text](<images/screenshot 2025-02-09 at 2.22.22 PM.png>)

4. Confirm `Type: Tile Layer` is automatically detected after the paste. 

![alt text](<images/screenshot 2025-02-09 at 7.56.09 PM.png>)

5. Click **Next**
6. Give your layer a **Title** and **Attribution**

![alt text](<images/screenshot 2025-02-09 at 7.58.32 PM.png>)

6. Click **Add to map**.
7. Save your map as `France Roads and Ports Digitization (SUNetID)`  
![alt text](<images/screenshot 2025-02-09 at 8.00.20 PM.png>)  
![alt text](<images/screenshot 2025-02-09 at 8.02.01 PM.png>)  

---
![alt text](<images/screenshot 2025-02-09 at 8.03.18 PM.png>)  


## **Step 7: Add the Feature Layer for Digitization**  


1. Click **Add** → **Browse Layers**.

2. Select **My Content** and find **french_ports_railroad_[SUNetID]s**.  

![alt text](<images/screenshot 2025-02-09 at 8.06.01 PM.png>)

3. Click **+Add**.
4. Click the ![ ](<images/screenshot 2025-02-09 at 8.11.02 PM.png>)Arrow at the top of the panel to close it 

---

## **Step 8: Configure Symbology**
1. Click on the small arrow next to the  **french_ports_railroads** layer to expand it.
2. Select the **Ports** layer
3. Select **Edit layer style** in the resulting Properties Panel, on the right.
4. Click on **+Field** and check the box next to `Port Type`

![alt text](<images/screenshot 2025-02-09 at 8.16.20 PM.png>)

5. Click **Add**
6. In the **Pick a style** dialog, click on **Style options** for the **Types (unique symbols)**

![alt text](<images/screenshot 2025-02-09 at 8.17.49 PM.png>)

7. Configure symbology for:
   - **Ports**: Use unique symbols based on `port_type` (e.g., 10pt red circle for major ports, 6pt orange circle for minor ports).

![alt text](<images/screenshot 2025-02-09 at 8.20.52 PM.png>)![alt text](<images/screenshot 2025-02-09 at 8.21.52 PM.png>)

8. Click **Done** and **Done** to save the changes and dismiss the Properties Panel.

8. Return to the Layers Panel on the left and configure the symbology for the `Railroads` feature layer
   - **Railroads**: Use a dashed line for railroads.
9. Save your configuration.![alt text](<images/screenshot 2025-02-09 at 8.26.27 PM.png>)

---

## **Step 9: Configure Popups**  


1. Click on the **Port** feature layer to open the Properties, again.
2. Click on the **Pop-ups** button.
3. Expand the **Fields list** and confirm the following fields:
   - `port_label`
   - `port_type`
   - `notes`
4. **Drag and Drop** the Fields to rearrange them, if needed. 

![alt text](<images/screenshot 2025-02-09 at 8.34.04 PM.png>)

5. Click on the **Railroads** feature layer and confirm the following fields:
   - `railroad_label`
   - `Notes`
6. Click on the **X** to remove the `Shape_Length` field from the pop-up
7. **Save** the changes to your Map.

---

## **Step 10: Share the Map Using an Editing App**


1. Click **Create app** → **Instant Apps**.

![alt text](<images/screenshot 2025-02-09 at 8.41.45 PM.png>)

2. Click on **Choose** on the **Sidebar App Template**.  

![alt text](<images/screenshot 2025-02-09 at 8.43.10 PM.png>)  

1. Fill out the **Create app - Sidebar** dialog and click **Create app**

![alt text](<images/screenshot 2025-02-09 at 8.43.53 PM.png>)

4. Configure the app:
   - Click on the **Search settings** Button and use `edit` as the search term
   - Click on **Edit tools** and click **Continue** to exit Express Mode and continue configuring your app
   - Toggle on **Edit tools** for adding and modifying features.
   - Expand the **french_ports_railroads_SUNetID** Layer and check the boxes for `Railroads` and `Ports`
   - Configure the attribute editor to use dropdown menus for `port_type`.


![alt text](<images/screenshot 2025-02-09 at 8.59.05 PM.png>)

1. Click **Publish** and **Confirm** to save and publish the app.

![alt text](<images/screenshot 2025-02-09 at 8.57.36 PM.png>)

---

## **Step 11: Share the app**
1. After publishing the app, the Share dialog will be presented. Click on **Change share settings**
2. In the resulting **Share** dialog, click on the **Edit group sharing** button
![alt text](<images/screenshot 2025-02-09 at 9.01.51 PM.png>)


3. Search for your **OSS Editing Group** in the resulting **Group sharing** and check it's box

![alt text](<images/screenshot 2025-02-09 at 9.02.37 PM.png>)

4. Click **Apply**  
5. Click **Save**
6. Click **Review sharing** to share the Map and Feature Layers with the OSS Editing Group, as well.

![alt text](<images/screenshot 2025-02-09 at 9.04.55 PM.png>)

7. Click **Update sharing** to update teh sharing settings to match your app.

![alt text](<images/screenshot 2025-02-09 at 9.06.52 PM.png>)

8. Click **Publish** again to save your changes
9. Click the **Launch** button  


![alt text](<images/screenshot 2025-02-09 at 9.08.47 PM.png>)

---

## **Step 12: DIgitize your features**

1. Click on the **Edit** button to open the **Editor Tool Panel**
2. Select the Ports template icon, and place it on one of the ports in your map
3. Add the Port Label
4. Use the Port Type drop-down to select the `port-type`
5. Click Create to save the feature
6. Continue digitizing the Ports until you hve completed the task ( or just practice for a bit)
7. Click the **Back arrow** to return to the Editor Tools main panel

![alt text](<images/screenshot 2025-02-09 at 9.12.56 PM.png>)  

![alt text](<images/screenshot 2025-02-10 at 9.14.26 AM.png>)
---

## **Step 13: Export Digitized Data to GeoJSON**
1. Open another instance of https://stanford.maps.arcgis.com in a new browser tab and navigate to **Content** and find the **french_ports_railroads** layer.
2. Click **Export** → **GeoJSON**.
3. Download the exported file for use in other GIS applications.

---

## **Conclusion**
By the end of this exercise, participants will have digitized the **major and minor ports** and **railroads** from the historical map. The resulting data will be standardized, exportable, and ready for analysis or integration into other projects. 

🚀 **Happy Mapping!**