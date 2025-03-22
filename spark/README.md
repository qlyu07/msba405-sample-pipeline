# EDA
- Imported and cleaned Los Angeles crime data, building inspection data, and business listing data
- Removed null values in critical columns such as location descriptions and crime codes
- Analyzed crime distribution by types, with vehicle theft being the most common
- Examined victim demographics (age, sex, descent) and their relationships to crime types
- Created time series analysis of crime incidents and building inspections by month/year
- Analyzed crime patterns by day of week and hour of day using heatmaps
- Compared crime density across different LA areas
- Combined crime and building inspection data using spatial analysis
- Analyzed business categories and their distribution across LA
- Tracked business registration trends over time
- Examined building inspection results and their patterns
- Calculated correlations between numerical variables in the crime data
- Performed statistical analysis of crime patterns by time of day (using chi-square tests)
- Conducted spatial pattern analysis, including distance from downtown LA
- Created visualizations for all analyses including bar charts, histograms, heatmaps, boxplots, and correlation matrices

## Installing Spark:

Install prerequisites:

```
sudo apt update
sudo apt install default-jdk -y
sudo apt install curl git scala -y
```

Download:

```
wget https://dlcdn.apache.org/spark/spark-3.5.4/spark-3.5.4-bin-hadoop3.tgz
tar xvf spark-3.5.4-bin-hadoop3.tgz
```

Put Spark in its new home:

```
sudo mkdir /opt/spark
sudo mv spark-3.5.4-bin-hadoop3/* /opt/spark
sudo chmod -R 777 /opt/spark
```

Add the Spark commands to the path so you can type "pyspark"
and load the app:

```
sudo nano ~/.bashrc
```

Add the lines below at the end of the file, save and exit the file:

```
export SPARK_HOME=/opt/spark
export PATH=$PATH:$SPARK_HOME/bin:$SPARK_HOME/sbin
```

Load the changes:

```
source ~/.bashrc
```

Test that it works:

```pyspark```

While you are in `pyspark` OR while you have a pipeline running via `spark-submit` you can
access the Spark UI after you open port 4040 in your EC2 security settings.

```http://hostname:4040```


Source: https://medium.com/@patilmailbox4/install-apache-spark-on-ubuntu-ffa151e12e30
