---
published: true
---
## "The command '/bin/sh -c locale-gen en_US.UTF-8' returned a non-zero code: 127"

I recently ran into this error message:
```csharp
The command '/bin/sh -c locale-gen en_US.UTF-8' returned a non-zero code: 127
```

After much gnashing of teeth I edited the script from ![Microsoft]()

```csharp
FROM microsoft/service-fabric-onebox
WORKDIR /home/ClusterDeployer
RUN ./setup.sh

#Generate the local
RUN locale-gen en_US.UTF-8

#Set environment variables
ENV LANG=en_US.UTF-8
ENV LANGUAGE=en_US:en
ENV LC_ALL=en_US.UTF-8
EXPOSE 19080 19000 80 443

#Start SSH before running the cluster
CMD /etc/init.d/ssh start && ./run.sh
```


to this

```csharp
FROM microsoft/service-fabric-onebox
WORKDIR /home/ClusterDeployer

# Set the locale
RUN apt-get clean && apt-get update && apt-get install -y locales
RUN locale-gen en_US.UTF-8
RUN ./setup.sh

#Generate the local
RUN locale-gen en_US.UTF-8

#Set environment variables
ENV LANG=en_US.UTF-8
ENV LANGUAGE=en_US:en
ENV LC_ALL=en_US.UTF-8
EXPOSE 19080 19000 80 443

#Start SSH before running the cluster
CMD /etc/init.d/ssh start && ./run.sh
```

Solved my issue!

**Edit:**
I ran into further issues as I progressed through the installation for ```sfctl```.

I solved it by running the following commands in sequence:

```csharp 
#i was missing these three packages to make the fourth command work
sudo easy_install pip
sudo easy_install nose
sudo easy_install tornado

pip install -I sfctl==1.1.0
```
