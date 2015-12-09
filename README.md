# Robin Java SDK
[![Build Status](https://travis-ci.org/robinpowered/robin-java-sdk.svg?branch=master)](https://travis-ci.org/robinpowered/robin-java-sdk)

This README is a work in progress.

Full API documentation is available at [docs.robinpowered.com](http://docs.robinpowered.com).

[View the Javadoc](http://robinpowered.github.io/robin-java-sdk/javadoc)

## Download

This is a pre-release "preview" library and currently only available from the 
[sonatype `snapshots` repository](https://oss.sonatype.org/content/repositories/snapshots/com/robinpowered/robin-java-sdk/) and not currently in the
Maven Central Repository.

Using Maven:

```xml
<dependency>
  <groupId>com.robinpowered</groupId>
  <artifactId>robin-java-sdk</artifactId>
  <version>1.0.0-SNAPSHOT</version>
</dependency>
```

or using Gradle:

```groovy
compile 'com.robinpowered:robin-java-sdk:1.0.0-SNAPSHOT'
```

## Getting Started

Using the Robin API requires an API access token, which can be generated by logging in a https://dashboard.robinpowered.com. 

Once you have an access token, you can instantiate the `RobinApi` class to easily make API calls:

```java
Credential credential = new AccessTokenCredential("my token");
RobinApi apiClient = new RobinApi(credential);

ApiResponse<List<Presence>> presence = apiClient.getService(PlacesService.class).getPresence(mySpaceId).getData();
```


## License 


       Copyright 2015 Robin Powered, Inc.
    
       Licensed under the Apache License, Version 2.0 (the "License");
       you may not use this file except in compliance with the License.
       You may obtain a copy of the License at
    
           http://www.apache.org/licenses/LICENSE-2.0
    
       Unless required by applicable law or agreed to in writing, software
       distributed under the License is distributed on an "AS IS" BASIS,
       WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
       See the License for the specific language governing permissions and
       limitations under the License.

