# Network Influence Analysis*

Hosts the network visualizations for HW2, as part of completed as part of a network analysis course (Dr. Teague Henry, UVA, Fall 2021). Used igraph package in R for data analysis and Cytoscape for customized visualizations. Code not included in repository. Data came from Beveridge & Shan (2016), representing weighted social network of character co-occurrences in *A Storm of Swords.* Each node represented a character, and the edge weights represented the number of times the two nodes incident on the edge appeared within 15 words of each other.


## References
Beveridge, Andrew, and Jie Shan. 2016.  
**“Network of Thrones.”** *Math Horizons* 23 (4): 18–22.  
https://doi.org/10.4169/mathhorizons.23.4.18

---

## Character-Level Network Visualizations

### Visualization 1: Character Network (Edge Weight by Width)
![Character Network](Viz/got.svg)

This undirected network represents character co-occurrences in *A Storm of Swords*. Each node represents a character, and edge weights correspond to the number of times two characters appear within 15 words of one another. Edge width reflects edge weight, with thicker edges indicating more frequent co-occurrences.

---

### Visualization 2: Character Network Colored by House
![House-Colored Network](Viz/got_house.svg)

Nodes are colored by House affiliation. Characters belonging to the same House tend to be more densely connected, though the network does not form maximally connected subgraphs or clearly isolated clusters by House. This suggests substantial interaction across Houses despite within-House cohesion.

---

### Visualization 3: Node Size by Degree
![Degree-Based Network](Viz/degree.svg)

Node size represents **degree**, or the number of distinct neighbors a character has. Tyrion exhibits the highest degree, reflecting the largest range of connections. Other main characters such as Jon and Sansa also show high degree values. High-degree nodes are more prevalent among characters located in Westeros compared to Essos-based characters (e.g., Daenerys).

---

### Visualization 4: Node Size by Degree Strength Ratio
![Degree Strength Ratio Network](Viz/dsratio.svg)

Node size represents **degree strength ratio**, capturing the average interaction frequency per connection. Hodor has the highest ratio due to a small number of neighbors combined with strong edge weights, particularly with Bran. In contrast, Tyrion’s many connections result in a lower ratio despite high overall interaction volume. Compared to degree-based sizing, this visualization shows less geographic differentiation between Westeros- and Essos-based characters.

**Summary:**  
- Visualization 3 highlights characters with the widest range of influence.  
- Visualization 4 highlights characters with the strongest relative interactions per connection.

---

## House-Level (Aggregated) Network Visualizations

### Figure 1: Edge Width by Aggregated Edge Weight
![House Network by Edge Weight](Viz/ExtraCredit3.svg)

### Figure 2: Edge Width by Aggregated Edge Degree
![House Network by Edge Degree](Viz/ExtraCredit4.svg)

These figures represent networks aggregated by House. Edge width reflects either total edge weight (Figure 1) or edge degree (Figure 2). While the metrics differ in scale, their distributions across Houses are similar.

---

### Figure 3: Node Size by Self-Loop Degree
![Self Loop Degree](Viz/ExtraCredit.svg)

### Figure 4: Node Size by Self-Loop Strength
![Self Loop Strength](Viz/ExtraCredit2.svg)

In these visualizations, edge width represents aggregated edge strength, while node size reflects either **self-loop degree** (Figure 3) or **self-loop strength** (Figure 4). Although these measures differ substantially in magnitude, they exhibit nearly identical rank ordering across Houses.

---

## Key Observations

- The **Lannister and Stark Houses** emerge as the most influential, showing strong within-House cohesion and frequent interactions between Houses.
- Essos-based and Dothraki groups are relatively isolated, each connecting primarily to the Queensguard, reflecting their geographic separation in the narrative.
- Aggregated metrics reveal consistent House-level influence patterns across multiple definitions of connectivity.


