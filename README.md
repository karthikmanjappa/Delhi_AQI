# Project Title :
#### Delhi AQI 
 # Project Description :
#### Air quality index (AQI) analysis is a crucial aspect of environmental data science that involves monitoring and analyzing air quality in a specific location. It aims to provide a numerical value representative of overall air quality, essential for public health and environmental management. So, if you want to learn how to analyze the Air Quality Index of a specific location, this article is for you. In this article, I’ll take you through the task of Air Quality Index Analysis using Python.
 # License :
 #### This project is licensed under the MIT License - see the LICENSE.md file for details.
 # Hourly average trends of AQI in Delhi:
 data['Hour'] = pd.to_datetime(data['date']).dt.hour
# Calculate hourly average AQI
hourly_avg_aqi = data.groupby('Hour')['AQI'].mean().reset_index()
# Create a line plot for hourly trends in AQI
fig = px.line(hourly_avg_aqi, x='Hour', y='AQI', 
title='Hourly Average AQI Trends in Delhi (Jan 2023)')
fig.update_xaxes(title="Hour of the Day")
fig.update_yaxes(title="Average AQI")
fig.show()
![Screenshot (80)](https://github.com/user-attachments/assets/b969d40b-29b5-444b-b176-7976f0b89ef9)

