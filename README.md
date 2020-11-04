# Labeled Monarch Butterfly Images
This repo contains raw and linked monarch butterfly images with human labeled annotations for the location of the butterflies.

## Structure

### image_urls.csv
Contains locations of monarch butterfly cluster images used in trianing the monarch butterfly counter CNN and whether those images would need to be modified before applying the annotations to them.

#### Schema
| Column Name      | Description                                                                                                                                                                         | Data                                               |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| Image Name       | Name of image as it appears in the label files.                                                                                                                                     | string                                             |
| URL              | Url where the image is located. ("not found" if image isn't found on google and is included in this repo.)                                                                          | url or "not found"                                 |
| Is Size Verified | States if size was verified. ("" if image is included in this repo.)                                                                                                                | "verified size" or "can't find correct size" or "" |
| Correct Size     | States correct size of the image for images with "can't find correct size" in the previous col. Incorrect image size will lead to mismatches in between the annotations and images. | int x int                                          |

#### data_preprocess/label_files
Collection of csv files listing the locations of the annotated butterflies.

#### data_preprocess/labeled
Collection of monarch butterfly phontos open sourced by the monarch butterfly team. (We included links for the images we don't have copyrights for in `image_urls.csv` 
