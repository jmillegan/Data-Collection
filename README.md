# Data-Collection Challenge 11
Used a lot of google on the second notebook. 
Slackflow was used as well and some questions for understanding went to chatcpt
Instructor Michael fixed some of my code on the second assignment
Had much help from my tutor sessions to make my output look as the key, as well as some coding issues i could just not figure out no matter what sources
  I was using.
Worked with my instructor who too could not figure out how to make the descending graph match the index of numbers.  We did a work around in order to get it to work. Using a 'kind' which my tutor told me about.
I copied a lot of the following code of options we tried:  I removed it from the notebook, but wanted you to see.  
I am looking for feed back specifically on how the decsending bar plot were to be coded to make the bar match the index please, or was the 'kind' commend the answer?

Line 22, the last bar plot show in the key again in asending order, however it was not asked for, so I did not code as such.


# Identify the coldest and hottest months in Curiosity's location

###########NEED HELP ON THIS TO MAKE IN DESCENDING ORDER ACCORDING TO KEY##########################

# Calculate the average temperature by month
avg_temp = df.groupby('month')['min_temp'].mean()

# Sort the average temperature in descending order
sorted_avg_temp = avg_temp.sort_values(ascending=True)
#x,y=zip(*sorted(zip(sorted_avg_temp.index, sorted_avg_temp.values)))
print(sorted_avg_temp)
# Plot the average temperature in descending order
#plt.bar(tuple(sorted_avg_temp.index), tuple(sorted_avg_temp.values))
#plt.bar(x,y)
#plt.xlabel('month')
#plt.ylabel('Temperature in Celsius')
index_strings = [str(i) for i in sorted_avg_temp.index]
plt.bar(x=index_strings, height=sorted_avg_temp)

# Customize the x-axis and y-axis ticks
#plt.xticks(range(1, 13))
#plt.yticks(range(-80, 1, 10))

#sorted_avg_temp.plot(kind='bar')

#plt.show()
#sorted_avg_temp
#print(sorted_avg_temp.index)
