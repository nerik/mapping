[« Mapping with OpenStreetMap](https://github.com/mapbox/mapping/wiki/Mapping-with-OpenStreetMap)

To get started, set up your work environment with the tools you would need. This guide walks you through creating an account on OpenStreetMap.org and setting up your editor to get started mapping.

## Set up an OpenStreetMap Account

1. Go to OpenStreetMap.org and create an account: [https://www.openstreetmap.org/user/new](https://www.openstreetmap.org/user/new)
2. **IMPORTANT** add a picture of yourself to your profile
3. Add a profile description like below

### Profile description

It is useful to include:

- The areas you are interested in mapping
- A nice message that allows others to get in touch
- Links to your homepage/twitter etc that allows people to follow you

*(format in [Markdown]( http://en.wikipedia.org/wiki/Markdown))*

Here is a good example:

![](https://s3.amazonaws.com/f.cl.ly/items/0h1C3r251C081I0n2t3x/Screen%20Shot%202014-12-12%20at%205.11.43%20PM.png)

## Install JOSM

We are using the Java OpenStreetMap Editor (JOSM) for most tasks. Here's how to get set up.

### 1. Download and install JRE

For running JOSM you'll need JRE - the Java Runtime Environment. [Download and install JRE]( http://www.oracle.com/technetwork/java/javase/downloads/server-jre8-downloads-2133154.html).

### 2. Download JOSM

[Go to the JOSM web site](https://josm.openstreetmap.de/wiki/Download) to download the latest tested version of JOSM. Place it in a common location for applications on your operating system.

- OSX: `/Applications/`
- Windows: `C:\Program Files\`

### 3. Open JOSM

You can now open the JOSM application you downloaded with a double click.

If you want JOSM to use more memory and you're using [Linux](http://wiki.openstreetmap.org/wiki/JOSM/Linux) you can also run it with:

    ~$ java -Xmx1024M -DproxyHost=$PROXY -DproxyPort=8080 -jar josm-tested.jar

Once JOSM is up and running it looks like this. Go find the preferences dialog, you'll need it for the next couple of steps. You can access it from under the light switch icon.

![](https://s3.amazonaws.com/f.cl.ly/items/1u073X3U3E371c122f22/Screen%20Shot%202014-12-12%20at%203.23.22%20PM.png)

### 4. Enable expert mode

Open the preferences dialog and enable "Expert mode".

![screen shot 2015-10-15 at 2 19 34 pm](https://cloud.githubusercontent.com/assets/353700/10509019/201ba324-7348-11e5-953f-c179e6e07ad8.png)

### 5. Add user and password

Now it's time to connect to OpenStreetMap. Add the user name and password of the account you just created on OpenStreetMap to JOSM.

![screen shot 2015-10-15 at 2 18 50 pm](https://cloud.githubusercontent.com/assets/353700/10509020/201cab02-7348-11e5-97c5-69fb726d11a9.png)

Now you should be able to retrieve data from OpenStreetMap by clicking on the button with the green down error in the top left:

![](https://s3.amazonaws.com/f.cl.ly/items/1o2A3Y383P1d2Z0c283d/josm.gif)

### 6. Enable Remote Control

Remote control allows you to launch JOSM directly from the map on OpenStreetMap.org. To enable Remote Control, check this box in the settings:

![screen shot 2015-10-15 at 2 14 07 pm](https://cloud.githubusercontent.com/assets/353700/10508886/5ff266a0-7347-11e5-9b9a-0cda2bbcf05c.png)

Also check the 'Download objects to a new layer' option. Now you should be able to retrieve data directly starting on OpenStreetMap.org like this:

![](https://s3.amazonaws.com/f.cl.ly/items/3R0Q3Y3W1b0h3j0k242e/josm.gif)