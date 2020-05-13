# Kickstarter - Improving existing models by adding content data

## Abstract
Kickstarter's stated mission is to "help bring creative projects to life". Since 2009 it has helped connect creators with potential funders by offering an online platform to promote their projects.
	To date, there are plenty of examples online of people using the vast amount of data available on this website to predict whether a project will succeed or not on achieving its target. However, I've noticed that the majority of these models are mainly focused on variables such as the campaign duration, goal amount, project category and geographical location.
	As someone who comes from an online marketing background, there is a question that instantly comes to my mind: Is there anything we can learn regarding the content included on these project pages?

## Project Objectives
	The primary purpose of this project is to assess if adding content-related data improves predictions compared to previous models. Examples of content-related data can be: 
number of videos, static and animated images
 presence of certain words on project blurb
 presence, length and sentiment score of the different sections of each page: story, risk and challenges, environmental commitments
range of pledge thresholds to receive rewards
	Another goal is to prove or disprove whether a high number of concurrent projects has an impact on their probability to succeed. In other words: Can the crowdfunding market be saturated?
	I will also explore the data to find the latest trends and the initial impact of the pandemic on project creation.

## Personal Objectives
Besides the joy of extracting insight from a sea of data, this project was an excellent opportunity to:
Test Google Colab's notebooks and the potential to use several instances all at once.
Work through a project using cloud computing services.
Learn more about reading and creating various JSON file formats.
Try out Tableau Public to create most of the visualisations.

## Data sources
The first stage of the data collection consisted on downloading and cleaning a set of JSON files that were scraped and made available by Web Robots. This company scrapes Kickstarter's website every month and provides the most up to date information. All these files are publicly available at https://webrobots.io/kickstarter-datasets/.

There is, however, a big caveat regarding the data, as they disclaim on their website: "from April 2015 we noticed that Kickstarter started limiting how many projects user can view in a single category. This limits the amount of historic projects we can get in a single scrape run. But recent and active projects are always included". As a result, many of the earlier projects are missing on the latest file.

To gather as many projects as possible, I wrote a script that downloads and collates projects from a JSON file from each quarter. The code starts from the most recent quarter and works its way back. By doing this, it only adds the latest state of each project to the final dataset.

During the second stage, I've scraped each project to extract as much information as possible about the content. It's worth mentioning that I have given up on storing the text or any other media due to disk space constraints.
