FROM yerly/hadoop-base:0.1.0

MAINTAINER yerly <yerlyhoo@gmail.com>

# move all configuration files into container
ADD files/* /usr/local/

# install scala
RUN ln -s /usr/local/scala-2.11.7 /usr/local/scala

# set scala environment variable
ENV SCALA_HOME /usr/local/scala
ENV PATH $PATH:$SCALA_HOME/bin

# install spark
RUN mv /usr/local/spark-1.4.1-bin-hadoop2.6 /usr/local/spark && \ 
mv /usr/local/log4j.properties /usr/local/spark/conf/log4j.properties && \
mv /usr/local/slaves /usr/local/spark/conf/slaves && \
mv /usr/local/spark-env.sh /usr/local/spark/conf/spark-env.sh

# set spark-env environment variable
ENV SPARK_HOME /usr/local/spark
ENV PATH $PATH:$SPARK_HOME/bin

ENV YARN_CONF_DIR /usr/local/hadoop
