# preprocessing_link_shp_data
Preprocessing the Speed and Geographical Data based on the SHP file

## 1. Terminology
- Urban network: Road network inside the city
- Link: The segment of a road in an urban network. Usually, from the intersection to the intersection


## 2. Why am I doing this?
- To visualize the link speed of an urban network, you need two kinds of data.
  - Table that has the link speed of the urban network by time and link ID.
  - SHP file that contains the geometry of each link. (distinguished by link ID)
- But there is a problem.
  - The link ID in the link speed data and SHP file do not match.
  - Link ID in speed data is given as the "Service ID" of a link.
  - Link ID in the SHP file is given as the "Standard ID" of a link.
- Fortunately, there is a match table given by the government.
  - Still, there are some unmatched errors.
  - Also, I want to create the connection info of urban link network in Seoul

## 3. What is the plan
- Left join two tables. Link speed data will be the left table, and SHP file will be the right table.
- Connect the links that shares same nodes in link.
- Expand the connections because there are some missing connection between links
