FROM debian:stable

RUN apt-get update && apt-get install motion -y
EXPOSE 8080
ADD ./Motion/motion.conf /etc/motion/motion.conf

CMD ["motion"]