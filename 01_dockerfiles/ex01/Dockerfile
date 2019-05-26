# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Dockerfile                                         :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: awajsbro <awajsbro@student.42.fr>          +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2018/11/28 14:19:57 by awajsbro          #+#    #+#              #
#    Updated: 2018/12/05 13:39:53 by awajsbro         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

FROM debian

EXPOSE 9987/udp 10011/tcp 30033/tcp

ENV TS3SERVER_LICENSE=accept

WORKDIR /root

RUN apt update ;\
    apt upgrade tar ;\
    apt install -y bzip2 wget ;\
    wget http://dl.4players.de/ts/releases/3.5.0/teamspeak3-server_linux_amd64-3.5.0.tar.bz2 ;\
    tar -xjf teamspeak3-server_linux_amd64-3.5.0.tar.bz2

ENTRYPOINT [ "/root/teamspeak3-server_linux_amd64/ts3server_startscript.sh", "start"]

# CMD ["bash"]

# docker build -t SKETUVE .
# docker run -p 9987:9987/udp -p 10011:10011/tcp -p 30033:30033/tcp -it --rm SKETUVE
