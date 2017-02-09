# GyPsY
Using Identification trees to recommend activity(Themes) to people based on certain classifiers : 
 
Possible classifiers : 
<ul>
<li> Age
<li> Gender
<li> Moods
<li> Timestamp
<li> Weather
<li> Solo/Group
</ul>

Target classifier :
<ul>
<li> Themes
</ul>

ID Tree created after providing a certain dataset : 
IdentificationTreeNode classifying by THEMES:
AGE
    12-17: TIMESTAMP
        Afternoon: GENDER
            Female: WEATHER
                Indoor: Religious
                Outdoor: Food
            Male: WEATHER
                Indoor: Entertainment
                Outdoor: Activity
        Early Morning: MOODS
            anger: WEATHER
                Indoor: Views
                Outdoor: Food
            happiness: City Feels
            neutral: City Feels
            sadness: Shopping
        Evening: MOODS
            anger: GENDER
                Female: Food
                Male: SOLO/GROUP
                    Group: Shopping
                    Solo: Entertainment
            happiness: GENDER
                Female: WEATHER
                    Indoor: Nature
                    Outdoor: Food
                Male: Entertainment
            neutral: WEATHER
                Indoor: Entertainment
                Outdoor: Religious
            sadness: Food
        Morning: GENDER
            Female: Food
            Male: WEATHER
                Indoor: Activity
                Outdoor: SOLO/GROUP
                    Group: Activity
                    Solo: Food
        Night: MOODS
            anger: Food
            happiness: Entertainment
            neutral: WEATHER
                Indoor: Views
                Outdoor: Food
            sadness: Religious
    18-24: MOODS
        Male: Entertainment
        anger: TIMESTAMP
            Afternoon: GENDER
                Female: SOLO/GROUP
                    Group: None
                    Solo: Entertainment
                Male: SOLO/GROUP
                    Group: WEATHER
                        Indoor: None
                        Outdoor: None
                    Solo: WEATHER
                        Indoor: None
                        Outdoor: Religious
            Early Morning: SOLO/GROUP
                Group: WEATHER
                    Indoor: Religious
                    Outdoor: GENDER
                        Female: Nature
                        Male: None
                Solo: GENDER
                    Female: None
                    Male: WEATHER
                        Indoor: None
                        Outdoor: Activity
            Evening: WEATHER
                Indoor: GENDER
                    Female: None
                    Male: Entertainment
                Outdoor: None
            Morning: WEATHER
                Indoor: SOLO/GROUP
                    Group: GENDER
                        Female: None
                        Male: Food
                    Solo: Activity
                Outdoor: GENDER
                    Female: Activity
                    Male: SOLO/GROUP
                        Group: None
                        Solo: None
            Night: SOLO/GROUP
                Group: GENDER
                    Female: Activity
                    Male: Entertainment
                Solo: GENDER
                    Female: None
                    Male: Entertainment
        happiness: TIMESTAMP
            Afternoon: SOLO/GROUP
                Group: GENDER
                    Female: City Feels
                    Male: Activity
                Solo: GENDER
                    Female: WEATHER
                        Indoor: City Feels
                        Outdoor: Entertainment
                    Male: Entertainment
            Early Morning: GENDER
                Female: SOLO/GROUP
                    Group: None
                    Solo: WEATHER
                        Indoor: City Feels
                        Outdoor: None
                Male: SOLO/GROUP
                    Group: None
                    Solo: Food
            Evening: SOLO/GROUP
                Group: GENDER
                    Female: Food
                    Male: WEATHER
                        Indoor: Entertainment
                        Outdoor: None
                Solo: WEATHER
                    Indoor: GENDER
                        Female: None
                        Male: None
                    Outdoor: GENDER
                        Female: Activity
                        Male: None
            Morning: GENDER
                Female: WEATHER
                    Indoor: Religious
                    Outdoor: None
                Male: SOLO/GROUP
                    Group: WEATHER
                        Indoor: Food
                        Outdoor: Entertainment
                    Solo: WEATHER
                        Indoor: Entertainment
                        Outdoor: Activity
            Night: GENDER
                Female: None
                Male: WEATHER
                    Indoor: Food
                    Outdoor: Entertainment
        neutral: TIMESTAMP
            Afternoon: SOLO/GROUP
                Group: GENDER
                    Female: None
                    Male: WEATHER
                        Indoor: None
                        Outdoor: City Feels
                Solo: GENDER
                    Female: Entertainment
                    Male: Views
            Early Morning: SOLO/GROUP
                Group: WEATHER
                    Indoor: GENDER
                        Female: Views
                        Male: None
                    Outdoor: Food
                Solo: GENDER
                    Female: WEATHER
                        Indoor: Entertainment
                        Outdoor: Views
                    Male: None
            Evening: SOLO/GROUP
                Group: GENDER
                    Female: None
                    Male: WEATHER
                        Indoor: None
                        Outdoor: None
                Solo: GENDER
                    Female: WEATHER
                        Indoor: None
                        Outdoor: Views
                    Male: None
            Morning: WEATHER
                Indoor: GENDER
                    Female: Food
                    Male: None
                Outdoor: GENDER
                    Female: None
                    Male: SOLO/GROUP
                        Group: Nature
                        Solo: Food
            Night: WEATHER
                Indoor: Entertainment
                Outdoor: GENDER
                    Female: None
                    Male: Nature
        sadness: TIMESTAMP
            Afternoon: GENDER
                Female: SOLO/GROUP
                    Group: WEATHER
                        Indoor: Religious
                        Outdoor: Nature
                    Solo: None
                Male: WEATHER
                    Indoor: None
                    Outdoor: SOLO/GROUP
                        Group: Activity
                        Solo: None
            Early Morning: WEATHER
                Indoor: None
                Outdoor: SOLO/GROUP
                    Group: Food
                    Solo: GENDER
                        Female: Food
                        Male: None
            Evening: WEATHER
                Indoor: SOLO/GROUP
                    Group: Activity
                    Solo: GENDER
                        Female: Food
                        Male: None
                Outdoor: GENDER
                    Female: None
                    Male: Entertainment
            Morning: WEATHER
                Indoor: Food
                Outdoor: SOLO/GROUP
                    Group: None
                    Solo: None
            Night: GENDER
                Female: WEATHER
                    Indoor: None
                    Outdoor: SOLO/GROUP
                        Group: Religious
                        Solo: Activity
                Male: Views
    25-24: Entertainment
    25-34: TIMESTAMP
        Afternoon: MOODS
            anger: GENDER
                Female: Food
                Male: SOLO/GROUP
                    Group: Nature
                    Solo: Activity
            neutral: SOLO/GROUP
                Group: Religious
                Solo: Food
            sadness: WEATHER
                Indoor: None
                Outdoor: City Feels
        Early Morning: MOODS
            anger: Religious
            happiness: Views
            sadness: Food
        Evening: SOLO/GROUP
            Group: GENDER
                Female: MOODS
                    anger: Religious
                    happiness: Views
                    neutral: WEATHER
                        Indoor: None
                        Outdoor: Religious
                    sadness: Religious
                Male: City Feels
            Solo: MOODS
                happiness: Nature
                neutral: Entertainment
        Morning: MOODS
            anger: City Feels
            happiness: Activity
        Night: MOODS
            anger: SOLO/GROUP
                Group: WEATHER
                    Indoor: Food
                    Outdoor: Entertainment
                Solo: Activity
            happiness: GENDER
                Female: WEATHER
                    Indoor: Food
                    Outdoor: None
                Male: Entertainment
            neutral: Food
            sadness: GENDER
                Female: Views
                Male: Entertainment
    25-34 : Nature
    35-44: MOODS
        anger: TIMESTAMP
            Afternoon: GENDER
                Female: Food
                Male: None
            Early Morning: Religious
            Evening: Religious
            Night: Nature
        happiness: TIMESTAMP
            Afternoon: SOLO/GROUP
                Group: Activity
                Solo: Food
            Early Morning: City Feels
            Evening: GENDER
                Female: City Feels
                Male: Entertainment
            Morning: Food
        neutral: TIMESTAMP
            Early Morning: GENDER
                Female: Shopping
                Male: Entertainment
            Evening: WEATHER
                Indoor: Religious
                Outdoor: Food
            Morning: Religious
        sadness: TIMESTAMP
            Early Morning: Entertainment
            Evening: GENDER
                Female: Nature
                Male: Religious
            Night: SOLO/GROUP
                Group: Religious
                Solo: Activity
    45-54: TIMESTAMP
        Afternoon: MOODS
            anger: SOLO/GROUP
                Group: Religious
                Solo: None
            happiness: Food
            neutral: Entertainment
            sadness: WEATHER
                Indoor: Religious
                Outdoor: Entertainment
        Early Morning: GENDER
            Female: Activity
            Male: Religious
        Evening: MOODS
            anger: Entertainment
            happiness: Entertainment
            neutral: Entertainment
            sadness: GENDER
                Female: Nature
                Male: Food
        Morning: Religious
        Night: GENDER
            Female: Religious
            Male: Entertainment
    55-64: MOODS
        anger: Religious
        happiness: Food
        neutral: Nature
        sadness: Religious
    65+: MOODS
        anger: Religious
        happiness: Nature
        neutral: TIMESTAMP
            Evening: Religious
            Night: City Feels
        sadness: None

