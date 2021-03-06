# SmellDetectorMerger

SmellDetectorMerger is an Eclipse plug-in which uses a number of code smell detectors (some of which are products of research work) that detect different kinds of code smells. The plug-in then combines all the detected smells from the different detectors in a single view and displays them to the end user. For each smell the user can see its type, the affected element, as well as a list of names which corresponds to the detectors that spotted this specific smell.

The plug-in supports filtering the detected smells and only display those found by >=2 or >50% of the tools. These filtered results can also be used as gold standard sets, in order to calculate precision and recall for each smell type for all the detectors that can detect it. An export option is also supported in order to allow the user to export the detection results in a csv file if needed.

In case the user is interested in getting results from a limited number of detectors, the plug-in provides this option via a Preference page in Eclipse. Also, the user can select whether they want to detect a specific code smell or all available smells.

### Available detectors
* [CheckStyle](https://github.com/checkstyle/checkstyle)
* [DuDe](https://wettel.github.io/dude.html)
* [PMD](https://github.com/pmd/pmd)
* [JDeodorant](https://github.com/tsantalis/JDeodorant)
* [JSpIRIT](https://github.com/hcvazquez/JSpIRIT)
* [Organic](https://github.com/opus-research/organic)

### Supported code smells
* God Class _(CheckStyle, PMD, JDeodorant, JSpIRIT, Organic)_
* Long Method _(CheckStyle, PMD, JDeodorant, JSpIRIT, Organic)_
* Long Parameter List _(CheckStyle, PMD, Organic)_
* Feature Envy _(JDeodorant, JSpIRIT, Organic)_
* Duplicate Code _(DuDe, PMD)_
* Brain Class _(JSpIRIT, Organic)_
* Brain Method _(JSpIRIT, Organic)_
* Data Class _(JSpIRIT, Organic)_
* Dispersed Coupling _(JSpIRIT, Organic)_
* Intensive Coupling _(JSpIRIT, Organic)_
* Refused Parent Bequest _(JSpIRIT, Organic)_
* Shotgun Surgery _(JSpIRIT, Organic)_
* Tradition Breaker _(JSpIRIT)_
* Type Checking _(JDeodorant)_
* Class Data Should Be Private _(Organic)_
* Complex Class _(Organic)_
* Lazy Class _(Organic)_
* Message Chain _(Organic)_
* Speculative Generality _(Organic)_
* Spaghetti Code _(Organic)_

### Installation
1. Download the code zip file or clone the repository
2. Import the code from the zip file or the cloned repository in Eclipse
3. Export to a jar by right clicking the project and selecting _Export..._ -> _Deployable plug-ins and fragments_ -> _Finish_
4. Close any open Eclipse instances
5. Copy the jar from the selected export folder and paste it in the _dropins_ folder inside the Eclipse installation directory
6. Open Eclipse and select _File_ -> _Restart_

After completing the previous steps, the tool can run by right-clicking the root folder of the desired project and selecting _SmellDetectorMerger_ followed by the desired smell to be detected.
