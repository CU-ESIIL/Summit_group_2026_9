---
title: Urban Tree Biodiversity
public_mode_toggle: true
---

<!-- !!! tip "How to use this page during the Summit"
    - This page is your team’s shared workspace and final report-out page. It captures your group’s process and thinking throughout the Summit and will be used to share your work with others. 
    
    - Use this page as your team’s working record during the Summit and your final report-out.
    
    - The Summit has several different goals and thus you will use the page differently each day: Day 1 is for alignment, Day 2 is for building one useful thing, and Day 3 is for synthesis and report- out.
    
    - Look for the green buttons to indicate what you need to edit. 
    
    - Megaphones 📣 indicate which items you will be presenting during the end-of-day report-outs.

    - Only the items with megaphones will be visible when you hit the 'Summit Report Out' button. 

    - If you turn off 'Instructions' then you will only see the page content for public display.
     -->

# AI-Based Detection of Urban Tree Canopy Change Using Remote Sensing Data

<!-- !!! note "Day 1 directions"
    Change the title to the name of your project.

    [Edit Day 1 setup in Markdown](https://github.com/CU-ESIIL/Summit_group_2026_9/edit/main/docs/index.md?plain=1#L21){ .md-button target="_blank" rel="noopener" }

!!! tip "For ESIIL staff"
    Group Number: 9
    
    Breakout Room #: S124

    [ESIIL staff edit in Markdown](https://github.com/CU-ESIIL/Summit_group_2026_9/edit/main/docs/index.md?plain=1#L28){ .md-button target="_blank" rel="noopener" }
     -->
<!-- 
![Team hero image](assets/hero/hero.png)

!!! note "How to replace the image above"
    Upload an image that represents your project and welcome people to your page. 
    
    Upload your own image to `docs/assets/hero/` and replace the file named `hero.png`. Use a wide image if you can, then refresh the site preview to check how it looks.
    Keep the file path `docs/assets/hero/hero.png` if you want the Markdown above to keep working.

    [Open image folder for changing image](https://github.com/CU-ESIIL/Summit_group_2026_9/tree/main/docs/assets/hero){ .md-button target="_blank" rel="noopener" } -->


<!-- [See a completed example](example.md){ .md-button } -->

## People { #people .oasis-report-out-context }

<!-- !!! note "Day 1 task"
    Get to know your team: share your cards (5-7 mins). Update your team roster (2-3 min).

    Use the in-person name cards to guide quick introductions.

    | Name card prompts | Follow-up notes |
    |---|---|
    | ![Name card prompts for name, institution, area of expertise, research difference, and questions](assets/team/name-card-prompts.png) | ![Follow-up notes card with space for names and follow-up ideas](assets/team/name-card-followups.png) |

    [Edit People in Markdown](https://github.com/CU-ESIIL/Summit_group_2026_9/edit/main/docs/index.md?plain=1#L63){ .md-button target="_blank" rel="noopener" } -->

| Name | Affiliation | Contact | Github |
|---|---|---|---|
| Aakriti Joshi | Clemson University | aakritj@g.clemson.edu |  |
| Sara Tabatabaie | ENVD, University of Colorado, Boulder | Sara.Tabatabaie@colorado.edu |  |
| Olivia Zhang | University of Florida | oliviazhang@ufl.edu | via-zhang |

<!-- ## Team Norms and Decision Making { #team-norms-and-decision-making } -->

<!-- !!! note "Day 1 task"

    Suggested Self-Facilitation Instructions:
    
    - Round Robin: Everyone shares 1 norm that they think will be important for their team during the Summit and perhaps following the Summit (2 min).

    - After everyone has shared, make a list with as many norms as possible in GitHub (5–7 min).

    - Vote on your top 3 ideas. (Each person gets 3 votes; you can use all your votes on 1 idea or spread them out) (2 min).

    - In GitHub, move all team norms with votes to the top of the list.

    | Gradients of agreement | 
    |---|
    | ![Gradients of agreement scale for Summit teams](assets/hero/norms.png) | 

    [Edit Team Norms in Markdown](https://github.com/CU-ESIIL/Summit_group_2026_9/edit/main/docs/index.md?plain=1#L87){ .md-button target="_blank" rel="noopener" } -->
<!-- 
Our team norms:

- ...
- ...
- ...

Our decision making strategy:

... -->

## Questions 📣 { #product-direction .oasis-report-out-section .oasis-report-out-day2 }

Goal: To assess the efficiency of AI models in detecting urban tree canopy cover change over time.

Main working question:

- How effectively can AI models detect and analyze urban tree canopy change over time using remote sensing data?

- What is the most effective workflow for using AI and remote sensing data to detect changes in urban tree canopy coverage over time?

Sub-Questions:
1. Which AI or machine learning model provides the highest accuracy in detecting urban tree canopy change over time?
2. How can remote sensing imagery and urban tree inventory data be integrated to improve canopy change detection?
3. What spatial or environmental factors may contribute to observed changes in urban tree canopy cover? (the longer-term objective)
4. How can AI-assisted urban canopy monitoring support community-based urban forestry efforts?

## Data Sources 📣 { #data-exploration .oasis-report-out-section .oasis-report-out-day2 }

<b>Input data for comparison of efficiency of AI models in tree canopy detection:</b>

- Google Earth Aerial Imagery

- Microsoft Planetary Aerial Imagery

- National Land Cover Database (NLCD)

- Landsat Satellite Imagery

- National Aerial Imagery Program (NAIP) Aerial Imagery

<b>For validation/verification of AI detection of canopy after efficiency analysis, we can use the following data sources:</b>

- Tree Inventory Data

- GIS Tree/Vegetation Shapefiles for different municipalities

- iNaturalist Data

- Normalized Difference Vegetation Index (NDVI) from satellites

<b>AI Models:</b>

- Clip Segmentation - connects images with text, works with text prompts; not always the most precise for detailed canopy boundaries

- Segment Anything Model (SAM3) - separate any object from an image - outline exact canopy shape - can provide accurate boundaries, canopy area calculations, change comparison over time
https://ai.meta.com/research/sam3/

- YOLO (You Only Look Once) - finds objects in images, faster than other models in object detection, but might not have high precision for canopy boundaries
https://www.ultralytics.com/?utm_source=chatgpt.com

- OWLv2 for vegetation: uses text prompts to identify and localize objects, including vegetation, in imagery 
https://huggingface.co/google/owlv2-base-patch16
https://github.com/inuwamobarak/OWLv2

- ADE20K SegFormer - classifies objects in images; best known for land use mapping
https://github.com/CSAILVision/ADE20K

## Methods 📣 { #methods-and-code .oasis-report-out-section .oasis-report-out-day2 }

<b>Tool and Code Identification</b>
    Identified and reviewed Python code snippets and AI-based image detection tools suitable for detecting urban tree canopy coverage using remote sensing imagery.

<b>Pilot Testing with NAIP Imagery</b>
    Applied multiple AI image detection models to a small pilot study area using NAIP aerial imagery to evaluate workflow feasibility and processing performance.

<b>Model Comparison and Evaluation</b>
    Compared the performance of different AI detection tools based on processing speed, usability, and detection quality.

<b>Accuracy Assessment</b>
    Using ArcGIS to evaluate detection accuracy by comparing AI-generated canopy outputs with:
    - NDVI-based vegetation analysis
    - Existing urban tree canopy shapefiles and reference datasets

<b>Workflow Optimization</b>
    Selected the most effective AI detection workflow based on overall performance and accuracy.

<b>Multi-Dataset Testing</b>
    Applied the optimized workflow to additional datasets, including: 
    - alternative satellite imagery sources
    - Google Earth aerial imagery to test adaptability and consistency across different image types and resolutions.

<b>Analysis of Urban Tree Canopy Change</b>
    Used the finalized workflow to explore patterns and changes in urban tree canopy coverage over time.

![Research Workflow](assets/figures/figure1.png)
![Methodology](assets/figures/figure2.png)


### Next Steps

Future prospects of this project: Moving from a mapping study to an ecological diagnosis study

- Using AI-detected canopy dynamics to identify functional vulnerability hotspots in Denver's urban forest. This can be done by combining change detection with crown health proxies (NDVI stress, not just presence). 

- Socioeconomic and Environmental changes overlays to show where the urban forest is most ecologically at risk and why.

- Policy recommendations on maintaining sustainability of urban forestry and community awareness programs after identifying causes of changes in canopy cover. 

## Findings at a Glance 📣 { #findings-at-a-glance .oasis-report-out-section .oasis-report-out-day3 }

Headline 1 — what, where, how much

...

Headline 2 — change/trend/contrast

...

Headline 3 — implication for practice or policy

...

<!-- ## Visuals that tell a story 📣 { #story-visuals .oasis-report-out-section .oasis-report-out-day3 }

![Story visual](assets/figures/main_result.png)

*Visual 1: the main pattern or output we want people to remember.* -->

## What’s next? 📣 { #whats-next .oasis-report-out-section .oasis-report-out-day3 }

Short term:

- ...

Long term:

- ...

Who should see this next

- ...

## Cite & Reuse { #cite-reuse }

If you use these materials, please cite:

Summit Team. (2026). *Summit Group 2026 Team 9 — Innovation Summit 2026*. https://github.com/CU-ESIIL/Summit_group_2026_9

License: CC-BY-4.0 unless noted. 
