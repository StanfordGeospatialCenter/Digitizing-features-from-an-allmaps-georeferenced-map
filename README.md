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
1. Click **Add** → **Search for Layers**.
2. Select **My Content** and find **french_ports_railroads**.
3. Click **Add to Map**.

---

## **Step 8: Configure Symbology**
1. Click on the **french_ports_railroads** layer.
2. Select **Change Style**.
3. Configure symbology for:
   - **Ports**: Use unique symbols based on `port_type` (e.g., red circle for major ports, orange circle for minor ports).
   - **Railroads**: Use a dashed line for railroads.
4. Save your configuration.

---

## **Step 9: Configure Popups**
1. Click on the **french_ports_railroads** layer.
2. Select **Configure Pop-ups**.
3. Display the following fields:
   - `port_label`
   - `port_type`
   - `railroad_label`
   - `notes`
4. Save the changes.

---

## **Step 10: Share the Map Using an Editing App**
1. Click **Share** → **Create Web App**.
2. Select the **Editor App Template**.
3. Configure the app:
   - Enable **Editing** for adding and modifying features.
   - Configure the attribute editor to use dropdown menus for `port_type`.
4. Save and publish the app.

---

## **Step 11: Export Digitized Data to GeoJSON**
1. Go to **Content** and find the **french_ports_railroads** layer.
2. Click **Export** → **GeoJSON**.
3. Download the exported file for use in other GIS applications.

---

## **Conclusion**
By the end of this exercise, participants will have digitized the **major and minor ports** and **railroads** from the historical map. The resulting data will be standardized, exportable, and ready for analysis or integration into other projects. 

🚀 **Happy Mapping!**