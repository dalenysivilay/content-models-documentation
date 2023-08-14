<style>
body {
  font-family: Arial, Helvetica, sans-serif;
}
</style>

---

## Content Types

- Content Types are broken down into three categories: **Components**, **Layouts**, and **Pages**
- Components contain all of the building blocks that make up the Layout type.
- Layouts are more complex components that provide the template to combine Content entries.
- Pages define the template for the respective pages and limit the content that can be added.
- This document defines content types that have been modeled for the mobile application.

---

### Components

### Banner

#### Fields:

- **Title (Text)**

  - The title of the banner, it's mandatory and unique.

- **Select Banner Type (Text)**

  - This field allows you to select the type of banner. Options include "Costco Banner Builder" and "Personalized Banner".

- **Banner Builder (Group)**

  - This is a group of fields related to the Banner Builder. Fields within this group include:
    - **Banner Image (File):** Allows you to upload an image for the banner.
    - **Banner Link (Link):** Allows you to add a URL link to the banner.
    - **Show Heading (Boolean):** If selected, shows the heading of the banner.
    - **Show Subheading (Boolean):** If selected, shows the subheading of the banner.
    - **Show Overlay Text (Boolean):** If selected, shows the overlay text on the banner.
    - **Heading Group (Group):** Contains fields related to the heading including title, subtitle, and background color.
    - **Subheading Group (Group):** Contains fields related to the subheading including title and subtitle.
    - **Overlay Text Group (Group):** Contains fields related to the overlay text, including the text itself, color, and position.
    - **Banner Description (Text):** A descriptive field for the banner.

- **Personalized Banner (Group)**
  - This is a group of fields related to the Personalized Banner. Fields within this group include:
    - **Select Provider (Global Field):** Allows you to select a provider for the banner.
    - **AdButler Zone ID (Text):** A field for the ID of the AdButler zone.
    - **Adobe Target Campaign ID (Text):** A field for the ID of the Adobe Target campaign.
    - **Criteo Campaign ID (Text):** A field for the ID of the Criteo campaign.

###### Description

This content type was created to manage banner components with providers. The visibility and requirements of certain fields are based on the chosen banner type and other factors, which can be controlled via the field rules. For example, the fields in the "Banner Builder" group will only show up if "Costco Banner Builder" is chosen as the banner type. Similarly, the fields in the "Personalized Banner" group will only show if "Personalized Banner" is chosen.

Please refer to the documentation or the specific field descriptions for more information about using these fields and their available options.

##### Banner Style Visualization

Large

![](https://lh6.googleusercontent.com/yz4oRVDE0aFJTytxrlGTbzhf-KA74aySBS-2sABJugpdb2X6cquZ5LJvc648mstHFVAuyEsWFIKxc0NA0jqb5i-ma1qVTdVzNr0X2cxzXpi24C__vJnVpgTjbRmqrH2oeMyDX-266MpgT1L_XICH1hk)

Medium

![](https://lh4.googleusercontent.com/0L53bQR4PlNKlNLuJ4HpK-4F5cBcbppIZ5kANtSp8qzWGV6VD9W7oC31Ts1r1VZTzmUtSaOpVDQ6sR_FH6h4vSArTAWgYecxFQSiJsgYzmNo6jPeJrs-3yoQ1i2CxSmcdBD_hMdvCI-Vd7CJU55oXYU)

Small

![](https://lh5.googleusercontent.com/I-zWrhJenMLEcl5GmyunmHEzqiT4I7FhOagL5GD300B3o2VOGaqD4NOHpdzUhtqo4SPDd8J7pE8e6kFdHlGD7g4JQQteUdYJJUsqqAn59wPAkQO8p34649O7k4-SLBUSKp2TXg-wuhv3EL2Jhnkp5Jc)

Square

![](https://lh4.googleusercontent.com/4hlZS2WoI9kcirfQtaS9aguTPFleQtBvDcLaB-PL0cAU3poJsogtWgEJAv8DAlKhbkpFOtypfYRP16uWdl9kOMO3N0h_ovp__oqxPKR3HYR-hsYeFksPrc2e4CzyebHzXvlnMCVg3EBU3nJdCHi0qd0)

With Sub Heading Only

![](https://lh4.googleusercontent.com/LwU1-NdB0fkpdHdsF9h0lEq3r5HE3Iru2UXKXolVjljN_m_gxtN3Va36RRse90O416Kq0GXqI9IQ9p3re7tKboFoF4Il3iQ7MgonmaKzcSOl1tc_0d3eXdDaMcaV4cgeZQCF76PLSAB9R-ht7UraqXk)

With Description Only

![](https://lh5.googleusercontent.com/Br4y5J8Vzf3w_ao7ipB9_m_UD0DGQYIRL_X1snQui_uD4GexlWOkFK3x6nCoOvMzuYvek3KK9irJQt682DNuQGZHBLUUfe4mjNdQUgMBVBErr8kJAY6dC68Ll25HOf5sZ_HbQ_2gGb-WyFz83zvqloU)

###### JSON Visualized

```
{
  "title": "Banner",
  "uid": "c_banner",
  "fields": [
    {
      "field_type": "text",
      "field_name": "Title"
    },
    {
      "field_type": "text",
      "field_name": "Select Banner Type"
    },
    {
      "field_type": "group",
      "field_name": "Banner Builder",
      "sub_fields": [
        {
          "field_type": "file",
          "field_name": "Banner Image"
        },
        {
          "field_type": "link",
          "field_name": "Banner Link"
        },
        {
          "field_type": "boolean",
          "field_name": "Show Heading"
        },
        {
          "field_type": "boolean",
          "field_name": "Show Subheading"
        },
        {
          "field_type": "boolean",
          "field_name": "Show Overlay Text"
        },
        {
          "field_type": "group",
          "field_name": "Heading Group",
          "sub_fields": [
            {
              "field_type": "text",
              "field_name": "Heading Title"
            },
            {
              "field_type": "text",
              "field_name": "Heading Subtitle"
            },
            {
              "field_type": "text",
              "field_name": "Heading Background Color"
            }
          ]
        },
        {
          "field_type": "group",
          "field_name": "Subheading Group",
          "sub_fields": [
            {
              "field_type": "text",
              "field_name": "Subheading Title"
            },
            {
              "field_type": "text",
              "field_name": "Subheading Subtitle"
            }
          ]
        },
        {
          "field_type": "group",
          "field_name": "Overlay Text Group",
          "sub_fields": [
            {
              "field_type": "text",
              "field_name": "Text"
            },
            {
              "field_type": "text",
              "field_name": "Color"
            },
            {
              "field_type": "text",
              "field_name": "position"
            }
          ]
        },
        {
          "field_type": "text",
          "field_name": "Banner Description"
        }
      ]
    },
    {
      "field_type": "group",
      "field_name": "Personalized Banner",
      "sub_fields": [
        {
          "field_type": "global_field",
          "field_name": "Select Provider"
        },
        {
          "field_type": "text",
          "field_name": "AdButler Zone ID"
        },
        {
          "field_type": "text",
          "field_name": "Adobe Target Campaign ID"
        },
        {
          "field_type": "text",
          "field_name": "Criteo Campaign ID"
        }
      ]
    }
  ]
}

```

---

### Button

#### Fields:

- **Title (Text)**

  - The title of the button, it's mandatory and unique.

- **Button Builder (Group)**
  - This is a group of fields related to the Button Builder. Fields within this group include:
    - **Button Image (File):** Allows you to upload an image for the button.

###### Description

This content type is created to manage button components. The visibility and requirements of certain fields are based on the chosen button type and other factors, which can be controlled via the field rules.

Please refer to the documentation or the specific field descriptions for more information about using these fields and their available options.

---

### Carousel

#### Fields:

- **Title (Text)**

  - The title of the carousel, it's mandatory and unique.

- **Autoplay (Boolean)**

  - Specifies whether the carousel should autoplay.

- **Controls (Boolean)**

  - Specifies whether controls should be displayed for the carousel.

- **Select Carousel Type (Dropdown)**

  - Dropdown to select the type of carousel. Choices include:
    - Banner
    - Product Card
    - Criteo
    - AdButler
    - Personalized Carousel

- **Banner Carousel (Blocks)**

  - A block type field for creating carousel items, each containing a reference to a Banner.

- **Product Card Carousel (Blocks)**

  - A block type field for creating carousel items, each containing a reference to a Product Card.

- **Personalized Carousel (Group)**
  - Group of fields related to the Personalized Carousel. Fields within this group include:
    - **Select Provider (Dropdown):** Choose from AdButler, Criteo, or Adobe Target.
    - **AdButler ID (Text):** ID related to AdButler.
    - **Campaign ID (Text):** ID related to the chosen Campaign.
    - **Page ID (Text):** ID related to the specific page.
    - **Adobe Target ID (Text):** ID related to Adobe Target.

###### Description

This content type is used to create carousels, which can be set to automatically scroll through items, and can be set to display controls to manually scroll through items. The carousel can be one of several types, and the fields that are available depend on the chosen type. This structure allows for a great deal of flexibility in creating and displaying carousels.

---

### Product Card

#### Fields:

- **Title (Text)**

  - The title of the product card. This field is mandatory and unique.

- **Select Type (Dropdown)**

  - Dropdown to select the type of product card. Choices include:
    - Product ID
    - AdButler
    - Adobe Target
    - Criteo

- **Product ID (Text)**

  - ID related to the product. To be replaced by BFF layer.

- **AdButler Zone ID (Text)**

  - ID related to the AdButler zone.

- **Adobe Target ID (Text)**

  - ID related to Adobe Target.

- **Criteo Placement ID (Text)**
  - ID related to the Criteo placement.

###### Description

The product card content type is used to display product cards with data retrieved from a BFF layer. The fields that are available depend on the type of product card chosen, allowing for a wide range of product card types to be created and displayed.

---

### Section Title

#### Fields:

- **Title (Text)**

  - The title of the Section Title content. This field is mandatory and unique.

- **Section Title (Text)**
  - The title of the section. This field is mandatory.

###### Description

The Section Title content type is used to display the title of a particular section on a page. The title is determined by the 'Section Title' field and uniquely identifies each section.

---

### Splash Banner

#### Fields:

- **Title (Text)**

  - The title of the Splash Banner content. This field is mandatory and unique.

- **URL (Text)**

  - The URL where the Splash Banner will redirect upon clicking. This field is optional.

- **Asset (File)**

  - The file that will be displayed as the Splash Banner. This field is optional and can be of any file type.

- **Date (ISO Date)**
  - The date associated with the Splash Banner. This field is optional and can contain dates between '2023-07-17T12:00:00-0400' and '2024-07-31T12:00:00-0400'.

The Splash Banner content type is used to create banners for display on a page. The banner will have a title, can contain a file, and will redirect to a specified URL upon being clicked. A date can be associated with the banner as well.

The URL pattern for accessing the Splash Banner content type is '/:title', where ':title' should be replaced with the title of a specific Splash Banner content. The URL prefix is '/'.

---

### _Gallery

#### Fields:

- **Title (Text)**

  - The title of the Gallery.

- **Gallery Heading and URL (Text)**

  - 

- **Gallery Style (Dropdown)**

  - Dropdown to select the type of carousel. Choices include:
    - Block
    - Carousel
    - Slider

- **Custom Background (Boolean)**

  - Enables usage of custom background. This field is a mandatory field that defaults to `False`

- **Gallery Background (Group)**

  - This is a group that contains the following field(s):
    - **Background Transparency (Dropdown)**
      - Dropdown to select the level of transparency. Choices include:
        - 100%
        - 90%
        - 75%
        - 50%
        - 25%
        - 10%
        - 0%
    - ** Background Color (Extension - Color Picker)**

- **Carousel Options (Group)**

  - This is a group that contains the following field(s):
    - **Show as Hero Slider (Boolean)**
    - **Enable Autoplay (Boolean)**
  
- **Item Curation (Dropdown)**

  - Dropdown to customize how items are presented. This field is mandatory. Choices include:
    - Costco
    - AdButler
    - Adobe
    - Criteo
    - new curation item 1
    - new curation item 2

- **3rd Party Curation (Group)**

  - Fields within this group include:
    - **Campaign Id (Text)**

- **Costco Curation (Group)**

  - Field(s) within this group include:
    - **Item Type (Dropdown)**
      - Choices include:
        - Banner
        - Marketing Campaign
        - Product
        - Category

- **Product Display Style (Group)**

  - This is a group of fields that controls how the product is displayed. Fields within this group include:
    - **Product Card Display Style (Dropdown)** Choices:
      - Compact
      - Informative
    - **Show Action Button (Boolean)** Default value is `False`
    - **Show Reviews (Boolean)** Default value is `False`
    - **Inventory Aware Listings** Default value is `False`

- **Category Content (Group)**

  - Group that controls how the images appear, with the following field(s):
    - **Image Form Factor (Dropdown)**
      - Controls the border radius of the image. Choices include:
        - Square
        - Rounded
        - Circular

- **Banner Content (Group)**

  - Field(s) within this group includes:
    - **Add filed (Text)**

- **Product Content (Group)**

  - Field(s) within this group includes:
    - **Reference to Product List (Text)**

