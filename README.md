# دیتاست :
این دیتاست 50000 نقد مثبت و منفی در مورد فیلم های سینمایی مختلف از سایت IMDB برداشت کرده و تمام متون رو به دو دسته مثبت و منفی تقسیم نموده است. این 50000 متن تمام داده ماست و شامل داده های آموزش و آزمایش میشوند بنابراین ما 20 درصد داده ها شامل 10000 متن را برای تست جدا کرده ایم و برای ارزیابی مدل از انها استفاده کردیم. منبع : https://www.kaggle.com/datasets/lakshmi25npathi/imdb-dataset-of-50k-movie-reviews

# روش ها و الگوریتم های مورد استفاده :
این مدل سازی به صورت کلی به سه شکل کاملا متفاوت انجام شده است.
- روش اول : پیش پردازش داده ها و استخراج و آماده سازی کلمات به روش Embedding و مدل سازی از طریق شبکه عصبی Conv1D
- روش دوم : پیش پردازش و آماده سازی داده ها به روش TfidfVectorizer و مدل سازی از طریق الگوریتم های کلاسیک یادگیری ماشن.
- روش سوم : پیش پردازش داده ها و استخراج و آماده سازی کلمات به روش Embedding و مدل سازی از طریق شبکه عصبی بازگشتی GRU

لازم به ذکر است که در روش دوم از چند الگوریتم مختلف استفاده کردیم تا قدرتمند ترین الگوریتم رو برای این دیتاست بیابیم و با شبکه عصبی مقایسه کنیم. الگوریتم های مورد استفاده ما عبارتند از LogisticRegression , RandomForest , VotingClassifier

# ارزیابی :
پس از مدل سازی به هرکدام از روش های از پیش گفته شده مدل ها رو ارزیابی کردیم و نتایج رو مقایسه کردیم. نتیجه ارزیابی روش اول با طی 25 epochs و روش دوم با الگوریتم LogisticRegression تقریبا مشابه بود. هر دو مدل به دقت 90% نزدیک شدند. 
