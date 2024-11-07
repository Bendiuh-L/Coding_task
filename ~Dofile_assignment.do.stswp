//Firstly, I accessed data, that I downloaded, and put it into Stata
use "C:\Users\Bendiuh_Yelyzaveta\Desktop\Assignment\clean\hotels-vienna.dta"
//Then I used command browse to see the table
browse
//Them I fixed common data equality errors, I got rid if missing values
tabulate rating_count, missing
browse
drop if missing(rating_count)
browse
drop offer_cat
drop neighbourhood
drop scarce_room
drop holiday
drop city_actual
//After that I prepared a sample for analysis creating a mean of ratings
egen mean_rating = mean(rating), by(distance)
//I created a summary statistics table
sum
sum price
//I created detailed summary statistics on price
sum price, detail
//Here I created a graph(histogramm) of prices
hist price
//And then I saved graph as file in Stata
graph save "Graph" "C:\Users\Bendiuh_Yelyzaveta\Desktop\Assignment\Graph.gph"
graph export "price.png", replace