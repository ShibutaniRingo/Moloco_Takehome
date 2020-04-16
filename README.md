# Moloco_Takehome
A takehome task including the Analytical part and the Regression part.
<ol>
    <li>Part 1: Data Analytics on Adops & Data Scientist Sample Data
        <ol>
            <li>Read Data
            <li>Transform timestamps
            <li>Answer to Part 1 questions
                <ol>
                    <li>Site with most unique users
                        <p>Consider only the rows with country_id = "BDV" (there are 844 such rows). For each site_id, we can compute the number of unique user_id's found in these 844 rows. Which site_id has the largest number of unique users? 
                        <p>The answer is "5NPAU" with 717 unique users.
                    <li>Four users & which sites they (each) visited more than 10 times</h4> 
                        <p>Between 2019-02-03 00:00:00 and 2019-02-04 23:59:59, there are four users who visited a certain site more than 10 times. Find these four users & which sites they (each) visited more than 10 times. (Simply provides four triples in the form (user_id, site_id, number of visits) in the box below.)
                        <p>The answer is ("LC06C3", "N0OTG",25) , ("LC3A59", "N0OTG",26), ("LC3C7E", "3POLC",15), ("LC3C9D", "N0OTG",17)
                    <li>Top three last visit sites
                        <p>For each site, compute the unique number of users whose last visit (found in the original data set) was to that site. For instance, user "LC3561"'s last visit is to "N0OTG" based on timestamp data. Based on this measure, what are top three sites? (hint: site "3POLC" is ranked at 5th with 28 users whose last visit in the data set was to 3POLC; simply provide three pairs in the form (site_id, number of users).)
                        <p>The answer is ("5NPAU", 992), ("N0OTG", 561), ("QGO3G", 289)
                    <li>The number of users whose first/last visits are to the same website</h4>
                        <p>For each user, determine the first site he/she visited and the last site he/she visited based on the timestamp data. Compute the number of users whose first/last visits are to the same website. What is the number?
                        <p>The answer is 1670.
                </ol>
        </ol>
    <li>Part 2: Linear Regression on Numerical Data
        <p>The data contains 300 rows and 3 columns (from the left, A, B, and C). Please build a good regression model which explains column C by a function of A and B.
        <p>Since column A, B and C are all numerical values, I used linear regresion with its loss fuction as MSE here.
    <ol>
        <li>Detect Null values and outliers.
            <p>There's no Null values in our dataset.
            <p>My criterion for detecting outlier (high leverage point) is: outside the interval of mean ± (2.33*standard deviation).
            <p>If we assume all the 3 variables has enough samples(Central Limit Theorem), 1% of the samples of each variable would be considered as outliers. The threshold could also be adjusted.
        <li>Do the linear regression
            <p>We have our dependant variable with 2 independant variables, the result of our regression should looks like a plane in the space.
            <p>The relationship between A, B and C is: C =  25.04 + (-1.09 * A) + (-15.02 * B)
        <li>Visualization
    </ol>
</ol>
