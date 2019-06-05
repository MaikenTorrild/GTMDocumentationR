# Create Google Tag Manager documentation with R

This R script generates an automated output in easy-to-read Excel format of the contents of a GTM account, using R and the GTM API.

## Usecases for this script

The output is very useful when you are auditing a GTM account, or for other data governance purposes.
It provides a format of the defined variables in GTM, including some additional contextual values. This has proven effective to share the type of data you are collecting with stakeholders in your organisation that don't have access to GTM, or are not familiar with Google Tag Manager.

## Packages used

The packages I have used are:
* googleAuthR
* openxlsx
* dplyr

## Options to configure before running the script

In order for the script to run successfully on your GTM account, you need to update some parts of the script.

### Get Google Tag Manager API credentials

You need to provide access for the script to your Google Tag Manager account via the API. This requires you to provide an API client ID and client secret. To get this access, please go to the Google developers console and create a project: https://console.developers.google.com/flows/enableapi?apiid=tagmanager&credential=client_key&pli=1

You need to use collect these credentials and add them to the "api_data" file in this R project.

### Get your GTM container ID and GTM account ID

Once you have access to GTM via your R script, please provide a valid Google Tag Manager account ID and container ID for the GTM container you would like to run the script for. You can find these values in your Google Tag Manager UI in the admin section.
