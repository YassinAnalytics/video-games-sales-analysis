# Video games sales analysis
SQL + Power BI analysis of global video game trends (1980s-2016). Covers platform dominance, genre preferences, and regional markets.

## Context 
I analyzed a dataset of global video game sales since the 1980s to identify key trends and understand which platforms, games, and genres are most popular across different regions.

Tools used: SQL (SQLite) and Power BI

Dataset: [Video Game Sales - Kaggle](https://www.kaggle.com/datasets/gregorut/videogamesales) 
- 16598 rows
-  11 columns (console, year, genre, sales, etc.)
-  unique table

Note: Sales are in millions. PC and mobile games excluded. 271 games have no release year (left as NA to preserve data integrity).


Key Insights :
- **Regional Sales:**
  - North America: 50%
  - Europe: 25%
  - Japan: 14%

- **Top Games:**
  - *Wii Sports* (bundled with Wii) – Best seller globally
  - *GTA V* – Multi-platform, cross-generation top seller

- **Japan-Specific Trends:**
  - RPGs dominate: 40% of the market
  - Publishers: Nintendo (86%) vs Sony (14%)




## **Analysis** 

**1.	Top 5 of the platform sales per region**

 ![image](https://github.com/user-attachments/assets/11594b8c-cf07-459f-915c-ccb81b60741a)


This request will be declined for each region by changing the parameters, like for example “NA_sales” by “EU_sales”.

For the European and north American market, the most popular platform is the Wii. Surprisingly in the Japanese market, the Wii is not present in the top 5. But despite this, it’s another Nintendo console more ancient. For the rest of the world, the PlayStation 2 is the most popular. So, one of the insights we can understand is that globally the Japanese platforms are the leaders in the market since the beginning.
On the global market (all regions) the first top 4 positions are owned by Nintendo, while the last one is by Microsoft (Xbox360). Sony is not present in this top globally while the sales are among the top in European and other countries markets. It seems that most of the sales are done at a bigger level in North America and Japan.

Let’s now explore an analysis of the sales per publisher by area would be interesting to see.



**2.	Publishers comparison**

 ![image](https://github.com/user-attachments/assets/9fe07c0e-5b20-4707-85af-67de31a4b23f)



Nintendo is once again the leader. So, leader in both as a publisher and a constructor.
We can see that the most powerful market for all publishers is the North American one. On Japan side, the results are great but then following the publishers, it’s not the best performance for the non-Japanese publishers. One of the trends that can be observed is that the Japanese market is really local, and all of the best sales in Japan are from the Japanese publishers. It seems that this market has some particularities and unique tastes.
 
![image](https://github.com/user-attachments/assets/684f7388-a103-44cb-ae88-47752fbc521c)


It's worth noting that the European market is following the same trends as the North American one but at least measure. For the other countries, the trend is mostly the same too.
Let’s now explore the genre by region.

**3.	Genre by region**

The logic of the code is the same by replacing the platform by the genre.

 ![image](https://github.com/user-attachments/assets/f13abdf9-d8b8-4d88-ae41-681edb414a71)


One of the first trend that can be observed is that the sport genre is the top 1 for all markets except Japan. But still, it’s in 5th position in the market. But the RPG (role player game) are by far the leader in Japan. And this genre is not present in the top 5 of others. It indicates some differences in terms of genre amongst the region.
Now let’s explore the cross-plateforms (game published on several platforms at the same time) trends.

**4.	Cross-plateforms**

 ![image](https://github.com/user-attachments/assets/b573f20a-c4b8-4ab2-83ce-18dd21c245bd)



GTA V is the top leader of the sales and present on 5 different platforms. It’s maybe the only game cross generation (present on 3 different generations).  Super Mario Bros released on 2 different platforms follows. And the legendary Tetris. And the rest of the top 10, is hold by the Call of Duty franchise (except 8th position with Super Mario World). We can notice that the best COD sellers are the ancient ones (around 2009/2010/2011). 
 If we now check the North American market only, the same games are present but not in the same order as the global sales.
 
 ![image](https://github.com/user-attachments/assets/3ae63402-688b-4ef8-a8c9-29b168323bda)

 

For the other markets the trend is different.
For the European market, the best sellers are GTA V, FIFA and COD, and also the sims. There is no super Mario games in it.

 ![image](https://github.com/user-attachments/assets/6413b6fd-8adb-492c-a0d4-f1fd891a7937)


For the Japanese market, the results are different. We can only find Japanese games in the top 10 like Mario, Tetris, Dragon quest, Final Fantasy games. Which are the iconic licenses of the Japanese games.
 
![image](https://github.com/user-attachments/assets/25ea761b-1375-432d-af25-12bbaf1409b8)

For the others countries, GTA V is at the second position. The first position is owned by one of its predecessors GTA San Andreas. Then the trend is similar than Europe, Call of Duty games and FIFA games (and the concurrent Pro evolution soccer).
 
![image](https://github.com/user-attachments/assets/e5f3e9e3-7a20-4896-aa79-fe45e16cecdb)

**5. Temporal sales**

Now let’s see the temporal sales for the main publishers at a global level.
 
![image](https://github.com/user-attachments/assets/53e63e30-b854-47d0-90c6-0aa786f2fe7c)


Nintendo had a peak of sales between 2006 and 2009 (when the Wii was at his highest). Then the sales started to drop. We also can see that between 2004 and 2005, the sales doubled. And then were divided by 2 between 2009 and 2010.

![image](https://github.com/user-attachments/assets/b8550741-3a50-4e39-8455-708123ea1025)
  

For EA (Electronic Arts), their sales are not that changing, except for a peak between 2002 and 2011.

 ![image](https://github.com/user-attachments/assets/8a1fd183-8cc1-4832-828d-b2526716601f)


For Activision, the peak is between 2009 and 2012 when the COD sales were at the highest.

![image](https://github.com/user-attachments/assets/a23d5904-2e32-44e8-a96f-e2897785bbf1)
 

For Sony, the top sales were at the beginning of the 2000s. 

 ![image](https://github.com/user-attachments/assets/fc1750b0-4b8f-4b32-9c36-0120001b2f39)


For Ubisoft, the peak was between 2007 and 2014. This is correlated with the Assassin’s creed saga (the first one aired in 2007).

 ![image](https://github.com/user-attachments/assets/f0e702e5-090a-4866-859e-3d56e8610012)



Now we know the trends, let’s go to the Data visualization in Power BI.

## Data Vizualisation
The first step is the import and check of the data.

![image](https://github.com/user-attachments/assets/26bb92e9-2428-4ef4-9d90-a277feddf702)
 


All the columns are useful, so I keep them. But there is change to do for the type of columns: 
-	Year : Integer
-	NA_sales: number with decimal, using local US
-	EU_sales: number with decimal, using local US
-	JP_sales: number with decimal, using local US
-	Other_sales: number with decimal, using local US
-	Global_sales: number with decimal, using local US
-	Year: left as a text to not impact the dataset because of 271 NA 

Creating some measures for the analysis for global view and region view: 
-	Number of games: COUNTROWS(vgsales)
-	Total sales
-	Average sales


The dashboard will contain 5 pages. 1 per view.


**Global view:**
- Global sales repartition
- Global sales per year
- Top 5 sales
- Top 5 crossplatforms games
- A slicer for the filter of the year and platform (filter synchronized for all the dashboard)

![image](https://github.com/user-attachments/assets/937f23e7-37af-432e-b970-9aacc6316481)

 
North America sales represent almost half of the global sales and Europe 25%. The best period for the sales were between 2004 and 2012. The most sold game is Wii Sport (which was included in the Wii), then GTA V.
For cross platforms, the most sold one is GTA V (on several generations) followed by Super Mario Bros (Nintendo platforms only), then Tetris and COD.

**North America view:**
- Top 5 Platforms by sales
- Top 5 Publishers by sales
- Top 5 Genres
- Top 10 Sales

![image](https://github.com/user-attachments/assets/d9daf8ef-8654-4e0b-aecc-36607d465f36)

 
The PlayStation 2 and Xbox 360 are equals in terms of sales (25% of the market each), then the Wii is at 21%, and the PS3 and Nintendo DS at 16% both. It means that 40% of the sales are for Sony, 40% for Nintendo so 80% of the platforms are from Japanese ones while the rest is from a north American one (Microsoft). We can observe that GTA V and COD series are less positioned than in the global sales. Wii and Super Mario bros are dominating.
The most popular genre is by far the action one.

**Europe view:**
- Top 10 Sales
- Top 5 genres by sales
- Top 5 Publishers by sales
- Sales by year and platform

![image](https://github.com/user-attachments/assets/a2ef7a73-2d79-4d9d-9ae6-c23b6c608e58)
 

Wii Sport ad GTA V are dominating the sales, then we have Mario kart wii and FIFA and COD series. Like the NA market the most popular genre is action and is followed by sport. As for the Publishers Nintendo is leader with 30% of the market, followed by EA(FIFA) at 27%. Activision (cod) is at 15% of the market and Ubisoft at 12% (a European one).
The best period for the sales was between 2001 and 2015 and almost doubled between 2001 and 2009.

**Japan view:**
- Top 5 platform by video game sales
- Top 5 genres by sales
- Top 10 sales
- Nintendo vs Sony

![image](https://github.com/user-attachments/assets/116767cb-1740-4e55-99f4-be922d283d3e)

 
All platform are Japanese ones, almost 60% is from Nintendo and the rest from Sony. The RPG games represent 40% of the market, followed by action, platform and sports. In the top 10 of the sales, all are from Japanese publisher with Pokemon and Mario as leaders in terms of licenses. 
The RPG seems to be a cultural trend for the market as it’s only in this area that the sales are high. Also, we need to be aware of the popularity of JRPG which is a subcategory (the difference is not mentioned in the dataset) of the genre. And in the total sales for the two main Japanese constructors/publishers, Nintendo is the big winner against Sony by having 86% of the sales between both sales.

**Other countries view:**
- Top 10 sales
- Top 5 genres by sales
- Top 5 platforms by sales
- Top 5 Publishers by sales

 ![image](https://github.com/user-attachments/assets/9ea0c560-c8c5-431f-b00a-1051e497138e)

GTA San Andres has the most sales, followed by Wii Sport and GTA V and Gran Turismo. They are followed then by COD and FIFA series. 
The PS2 and Nintendo DS have the most sales. In terms of genres, Actions, sports and shooter are the most popular ones. In terms of sales publishers, EA is the leader with 30%, followed by Nintendo with 22% and Sony with 18%. Activision (COD) is in 4th position with 17%.

The video game industry shows strong regional differences in terms of platform preferences, publisher dominance, and genre popularity. Nintendo leads globally, especially in Japan, while games like GTA, FIFA, and Call of Duty dominate Western markets. Action and sports are the most popular genres globally, while RPGs are uniquely dominant in Japan.
This project shows how data analysis and visualization can uncover deep insights into consumer behavior in the video game industry.

## **Going further** 
-	Analyze the impact of each new consoles on the market 
-	Do an analyze by decade
-	Another analysis would also analyze the impact of the free2play games, the e-sport and also to see the part of physical and digital sales. If there are the relevant data. 
-	Analyze the impact of PC sales and mobiles sales
-	For the 271 NA for year, find and complete it for each game.
-	Analyze the drop of the sales starting 2012

## **Files included**
-	vgsales.csv : Kaggle dataset 
-	vg_key_insights.pdf : summary presentation of the insight
-	vg_powerbi_dashboard.pdf : Power Bi report file PDF
-	vg_powerbi_dashboard.pbix : Power Bi report file PBIX
-	vgsales.db : dataset
-	vgsales.sqbpro : dataset with SQL querries
