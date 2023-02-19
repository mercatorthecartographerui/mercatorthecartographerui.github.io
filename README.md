# mercatorthecartographerui.github.io

This UI is to complement the awesome [Cartographer.sh] (https://cartographer.sh) project. 

<br><br>

---

## The Why and How behind Mercator

#### Carto is awesome BUT why do we need an easier way?

- ***Minimal Visual*** 
    - Carto is easy BUT it seems complex because it does not have an UI.
    - UX is completely with yaml file.
    - Makes it difficult to imagine multiple components associated.
    - Creates steep learning curves.
- ***Lack of "Library of Templates"***
    - There's a github project: from where users can get some starting yaml files. But it is still super hard to understad it all.
    - Users are left to learn everything upfront then create components of their own.
    - Results in an obstacle in adoption.
- ***The human element (Absence of Map and Navigation)***
    - without a visual representation of a **"Start"** point and an **"Finish"** point it is difficult (and confusing) for the end user to follow the documentation, understand Carto's components, create and/or modify. *Creation is 4x more difficult than modifying existing.*
    - Users gets lost in YAML deluge and face difficulties in understanding. This results in a huge obstacle to adoption AND divert from leveraging its true potential.

#### Enter Mercator – the Cartographer.sh UI

- ***Intuitive Graphical UI*** 
    - Represent Cartographer.sh components (Templates/Blueprints etc) in a visual way (instead of just YAML).
    - TextBox, Buttons and Drag’n’Drop based UI to customise components according to user needs.
    - Intuitive tips and suggestion on every step of creating templates and blueprints to support learning.
    - Drag’n’drop based interaction with blueprinting increases visibility AND enhances user experience with understanding and creating from scratch or modifying an existing. 
    - Intuitive UX experience simplifies users' overall learning curve.
    - It also provides way for a quick start with Cartographer.sh which will help deliver the value quicker.
    - Users can see live updates to the underlying YAML files as they interact with the graphical UI. This complements the user's learning curve of Cartographer.sh

- ***Map and Navigation***
    - The entire process (Templates, Blueprints, associated K8s objects) is represented in a MAP giving the user visibility and better learning experience.
    - Users can self-serve navigating through MAPs. Enriching the learning, creating and modifying experience.
- ***Library of Components***
    - Provides a collection of libraries (of ClusterXTemplate, Tekton Tasks/Pipelines, Supply & Delivery Chains). The Libraries are grouped by familiar/common terminologies and purposes.
    - User can input in the templates from library as per need. Simplifies the create and modify components both on day1 and day2 tasks of starting and operationalising DevSecOps inplementations.
    - The library helps expose components to users all in one place giving a good starting point without knowing it all on day1.
    - Users (DevOps team) can easily build this collection of library fit for their own organisation as the library is easily customisable.
---
<br><br>

## Customising or Configuring Mercator

You can configure this tool with your own set of templates and blueprints (yaml files) and the organisation of it (eg: library, maps etc). 
The UI shows differet types of data based on JSON files located under assets directory. You can modify these JSONs to display data (eg: Library, Blueprints etc) suiting to your needs.

#### Configuring Library






