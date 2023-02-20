# mercatorthecartographerui.github.io

See it in action at https://mercatorthecartographerui.github.io

![Cartographer.sh] (https://cartographer.sh) is a game changer in the DevSecOps domain. It has some huge benefits over what are currently available in the market such as Azure DevOps, Jenkins, Octupus etc. More to that, it is also open source, cloud native and runs on K8s.

Users implements CI/CD path using Cartographer by defining the stages and the path itself through YAML files. Which means DevOpsASCode capability is an out-of-the-box feature of cartographer. This is great. But that also means implementations are all done through yamls. Which may pose challenges such as:
- Users need to create and work with YAMLs only (and there are a lot of them). 
- The YAMLs can seem complex in nature to many; as not everybody is comfortable with yamls.
- Users will need to have clear understanding and planning before start creating CI CD using Cartographer.

These challenges can become overwhelming and obstacle for adoption. 

This UI solves these challenges by presenting users with a familiar and easy to undertand interface to Cartographer's blueprints and templates. I also comes with commons MAPs and Library of Templates for CI/CD usecases that users can follow to create or modify different DevSecOps scenarios.

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

## Customising or Configuring Mercator (the UI)

You can configure this tool with your own set of templates and blueprints (yaml files) and the organisation of it (eg: library, maps etc). 
The UI shows differet types of data based on JSON files located under assets directory. You can modify these JSONs to display data (eg: Library, Blueprints etc) suiting to your needs.

#### Configuring Library
Mercator UI shows the tiles of the library page and presents the yaml files for template from a JSON file `/assets/library/library.json`. It is an array of objects. Each object represents a tile in the `Library` section. If a tile contains more than one option then the object has an `options` array of type object. See below diagram showing how the object is represented on the tile as we all in the template create/edit page.

![Mercator - Configure Library](/assets/images/documentation/Mercator-Configure-Library.png "Mercator - Configure Library")

#### Configure ClusterXTemplate Templatisation
The UI tool understands a templatised yaml and displays it as a form. As the user fills the form the UI remplaces the templatised variables with the value collected from user input from the displayed form. The display of the form is dynamic in nature. Users can templatise a ClusterXTemplate and host it in a public repository OR file server. Then provide the URL of the file in the `Tile Object` OR (in the case of tile object has more that 1 options) in the `Option Object` in the `/assets/library/library.json` JSON file. See below as an example of Templatised ClusterSourceTemplate yaml. Notice the templatised variables in the `<VAR_NAME>` format.

![Mercator - Templatised YAML](/assets/images/documentation/Mercator-Templatised-YAML.png "Mercator - Templatised YAML")

#### Configure Form Schema
Below is how the templatised variables are presented as form by the Mercator UI.

![Mercator - Templatised ClusterSourceTemplate to Form](/assets/images/documentation/Mercator-Template-To-Form.png "Mercator - Templatised ClusterSourceTemplate to Form")

Notce few more information that are getting displayed along side the input fields per template variables. These information are coming from another JSON file `/assets/library/schema.json`. The variable is represented here as object. The JSON file contains an array of these objects. 
**Caution:** The var name must be unique in this file. This means that even if there are 2 different templates (eg: `ClusterSourceTemplate for GitPull` and `ClusterImageTemplate` for image scanning) contains the same template var (eg: `<NAME>`) there can only be one object in the `/assets/library/schema.json` JSON representing that template var (object name must be unique in the array). See below to understand what information is appearing from the JSON in the dynamic form.

![Mercator - Form Schema](/assets/images/documentation/Mercator-Form-Schema.png "Mercator - Form Schema")


#### Configure MAPs and Navigation from MAP


