Qun1 - Change the query shown so that it displays Nobel prizes for 1950.

Ans - SELECT yr, subject, winner FROM nobel WHERE yr = 1950

Qun2 - Show who won the 1962 prize for literature.

Ans - SELECT winner FROM nobel WHERE yr = 1962 AND subject = 'literature'

Qun 3 - Show the year and subject that won 'Albert Einstein' his prize.

Ans - select yr, subject from nobel where winner = 'Albert Einstein'

Qun 4 - Give the name of the 'peace' winners since the year 2000, including 2000.

Ans - SELECT winner FROM nobel WHERE subject = 'Peace' AND yr >= '2000'

Qun 5 - Show all details (yr, subject, winner) of the literature prize winners for 1980 to 1989 inclusive.

Ans - SELECT * FROM nobel WHERE yr >= 1980 AND yr <= 1989 AND subject = 'Literature'

Qun 6 - Show all details of the presidential winners: Theodore Roosevelt, Thomas Woodrow Wilson, Jimmy Carter, Barack Obama

Ans - select * from nobel where winner IN('Theodore Roosevelt', 'Thomas Woodrow Wilson', 'Jimmy Carter', 'Barack Obama');

Qun 7 - Show the winners with first name John

Ans - select winner from nobel where winner like 'John%'

Qun 8 - Show the year, subject, and name of physics winners for 1980 together with the chemistry winners for 1984.

Ans - select yr,subject,winner from nobel where (subject = 'Physics' AND yr = 1980) or(subject = 'chemistry ' AND yr = 1984);

Qun 9 - Show the year, subject, and name of winners for 1980 excluding chemistry and medicine

Ans - select yr,subject,winner from nobel where yr = 1980 AND subject NOT IN('chemistry','medicine')

Qun 10 - Show year, subject, and name of people who won a 'Medicine' prize in an early year (before 1910, not including 1910) together with winners of a 'Literature' prize in a later year (after 2004, including 2004)

Ans - select * from nobel where (subject = 'Medicine' AND yr < 1910) OR (subject = 'Literature' AND yr >=2004);

Qun 11 - Find all details of the prize won by PETER GRÜNBERG

Ans - select * from nobel where winner = 'PETER GRÜNBERG'

Qun 12 - Find all details of the prize won by EUGENE O'NEILL

Ans - select * from nobel where winner = 'EUGENE O''NEILL'.

Qun 13 - Knights in order - List the winners, year and subject where the winner starts with Sir. Show the the most recent first, then by name order.

Ans - SELECT winner, yr, subject FROM nobel WHERE winner LIKE 'Sir%' ORDER BY yr DESC, winner

Qun 14 - The expression subject IN ('chemistry','physics') can be used as a value - it will be 0 or 1. Show the 1984 winners and subject ordered by subject and winner name; but list chemistry and physics last.

Ans - SELECT winner, subject FROM nobel WHERE yr=1984 ORDER BY subject IN ('Physics','Chemistry'), subject,winner
