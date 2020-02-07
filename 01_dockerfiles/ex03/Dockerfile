FROM ubuntu

RUN apt-get update -y && \
    apt-get -y upgrade && \
    apt-get -y install \
    wget \
    openssh-server \
    postfix 

RUN wget \
    https://packages.gitlab.com/install/repositories/gitlab/gitlab-ce/script.deb.sh \
    && chmod 777 ./script.deb.sh && ./script.deb.sh

RUN apt-get install -y tzdata gitlab-ce

EXPOSE 443 80 22

ENTRYPOINT (/opt/gitlab/embedded/bin/runsvdir-start &) && sleep 2 && gitlab-ctl reconfigure && tail -f /dev/null



# chmod 777 gives all the permitions to the script script.deb.sh
# tzdata is a time zone data package, makes building faster
# runsvdir-start starts up runsvdir, which needs to run in the background.
# tail -f /dev/null to run the terminal, otherwise it will shut down

# build & run
# docker build -t ex03 .
# docker run -it --rm -p 8080:80 -p 8022:22 -p 8443:443 --privileged ex03
#open via web browser using ip&port

# If you will see "Whoops, GitLab is taking too much time to respond" page, 
# just wait and sometimes reload the page. It is absolutely ok. 
# After 5-10 minutes you will get a ready Gitlab.