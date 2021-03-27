1. Download the datasets Total Dollar Amount Invested in Small Businesses per 50 Businesses, Total Population - Community Statistical Area, and Total Employment in Arts Related Businesses.
2. Copy and paste the Employment data into a new tab called “Employment” in the Dollar Amount Invested sheet. Copy and paste the Population data into a new tab called “Population” in the Dollar Amount Invested sheet.
3. Into a new tab called “Relevant Columns,” copy and paste the columns “OBJECTID_1”, 	“CSA2010”, and “smlinvst16” from the Total Dollar Amount tab. 
4. From the “Employment” tab, copy and paste the column “artemp16” into the next column in “Relevant Columns.” 
5. From the “Population” tab, copy and paste the column “tpop10” into the next column in “Relevant Columns.”
6. Label the next column “share of population in arts employment.” In this column, divide the value in “artemp16” by the value in “tpop10”. Drag this equation down through the data.
7. Label the next column “dollars/business.” In this column, divide the value in “smlinvst16” by 50. Drag this equation down through the data.
8. Copy and paste the columns “OBECTID_1”, “CSA2010”, “share of population in arts employment,” and “dollars/business” into G14 of a new tab called “Analysis.” Ensure you use paste values instead of the general paste.
9. In H1 and H2, type “Mean” and “St Dev” respectively. 
10. In I1, calculate the mean of “share of population in arts employment” by using the equation =AVERAGE(I15:I69). Drag this equation over to the next column.
11. In I2, calculate the standard deviation of “share of population in arts employment” by using the equation =STDEV(I15:I69). Drag this equation over to the next column. 
12. Label new columns in K14 and L14 “z_share of pop in arts employment” and “z_dollars/business.” 
13. In K15, calculate the Z score of the value in “share of population in arts employment” with the equation =STANDARDIZE(I15,I$1,I$2). Drag this equation down through data. Drag this equation to the next column as well, and drag it down through the data again.
14. Set up the table of anchor neighborhoods and their Z scores starting in cell G5 with the label “Anchor #”. Label H5 “Anchor CSA,” I5 “z_share of pop in arts employment” and J5 “z_dollars/business.” 
15. In G6:G9, enter 4 random integers between 1 and 55. These will be your initial guesses for the optimization problem.
16. In H6, enter the name of the CSA corresponding to the integer using the equation =VLOOKUP(G6,G15:L69,2). Drag this equation down through the next three cells in the column. 
17. In I4 and J4, type 5 and 6 respectively. These correspond to the column numbers that the Z scores lie in. 
18. In I6, enter the Z score of share of population in arts employment corresponding to the anchor by using the equation =VLOOKUP($G6,$G$15:$L$69, I$4). Drag this equation to the next column, then down through both columns.
19. Label cells M14:P14 “distance^2 to 1,” “distance^2 to 2,” “distance^2 to 3,” and 	“distance^2 to 4” respectively. 
20. In M15, find the distance from that row’s Z scores to the first anchor’s Z scores with the equation =SUMXMY2($K15:$L15, $I$6:$J$6). Drag the equation over the next three horizontal cells. Change the 6’s to 7’s for the next column, the 6’s to 8’s for the 2nd next column, and so on. Drag all the equations through each of the four columns.
21. Label cell Q14 “Min Distance.”
22. In Q15, find the smallest distance of the four in the row using the equation =MIN(M15:P15). Drag this equation down through the column.
23. In Q10, find the sum of the minimum distances with the equation =SUM(Q15:Q69). 
24. Label cell R14 “cluster.”
25. In R15, find the cluster that the minimum distance corresponds to with the equation =MATCH(Q15, M15:P15, 0). Drag this equation down through the column.
26. In the Data tab, click Solver in the Analyze section. 
27. Set Objective to $Q$10, making it a Min. 
28. Set the cells you want to change to $G$6:$G$9. 
29. Add conditions that these cells need to be greater than or equal to 1 but less than or equal to 55, and that they need to be integers. 
30. In Options under Evolutionary, set the Mutation Rate to 0.05. Hit OK.
31. Select the Evolutionary Solving Method. Hit Solve.
32. When the Solver finishes, make sure “Keep Solver Solution” is selected and hit OK.
33. Label R1 and S1 “cluster” and “frequency” respectively. 
34. In R2:R5, enter integers 1-4. 
35. Select cells S2:S5 and type =FREQUENCY(R15:R69, R2:R5). Hit Ctrl + Shift + Enter. This returns the number of CSA’s in each cluster. 
36. Paste the table of anchor CSA’s and their Z scores as well as the table of cluster frequencies into a new tab called “Visualizations.” Ensure that you use paste value instead of general pasting.
37. Create a bar graph of the cluster characteristics, with each Z score category as a separate series and each CSA name as a horizontal axis label.
38. Create a bar graph of the cluster frequencies, with the frequencies as the series and the cluster names as the horizontal axis labels.
