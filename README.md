# web-scraping-challenge
I only needed help from the AI assitant on the second part of this challenge which was scraping the data from the tables on the website and analyzing them.
The part I struggled with the most was scraping through all the rows. I was more focused on the row aspect of the data that I wasn't thinking about identifying the columns and extracting the data that way. This is the only part I needed help from the AI:
    for row in data:
    cols = row.find_all('td')
    if cols:
        id = cols[0].text
        terrestrial_date = cols[1].text
        sol = cols[2].text
        ls = cols[3].text
        month = cols[4].text
        min_temp = cols[5].text
        pressure = cols[6].text
        
        row_data = {
            'id': id,
            'terrestrial_date': terrestrial_date,
            'sol': sol,
            'ls': ls,
            'month': month,
            'min_temp': min_temp,
            'pressure': pressure}
While I was on the right track of grabbing all of the "td" text, I didn't think about grabbing the headers of the columns and storing it as you loop through the rows.
