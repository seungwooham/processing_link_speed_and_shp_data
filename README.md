# preprocessing_link_shp_data
Preprocessing the Speed and Geographical Data based on SHP file

1. Terminology
- Urban network: Road network inside the city
- Link: The segment of a road in urban network. Usually from the intersection to intersection

2. Why am I doing this?
- To visualize the link speed of urban network, you need two kind of data.
  - Table that has link speed of urban network by time and link id.
  - SHP file that contains the geometry of each link. (distinguished by link id)
- But there is a problem.
 - The link id in a link speed data and SHP file does not match.
 - Link id in speed data is given as "Service ID" of a link.
 - Link id in SHP file is given as "Standard ID" of a link.
- Fortunately, there is a match table given from the government.
  - Still, there is some unmatched error.

3. dd
