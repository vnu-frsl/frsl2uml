# Functional Requirements Specification Language (FRSL)
# Plugin frsl2uml

**Acronyms:**
- SMD: State Machine Diagram.
- CD: Class Diagram.

**Prerequisites:**
- Install frsl-1.0.0
- "Install New Software" (local Update Sites within the folder: platform:/resource/frsl-1.0.0/additional-plugins/m2m-atl-Update-4.8.0): ATL
- Clone this repo.
- Open repo: 
  - *File -> Open Project From File System -> Specify to the folder 'frsl2uml' to import org.eclipse.sme.frsl2uml. 

- In *Problem* section (in Eclipse):
  - If any project is missing *src-gen* (*xtend-gen*), add manually folder *src-gen* (*xtend-gen*) to that project.
  - Fix the error 'An API baseline has not been set for the current workspace": (1) Click the menu: Windows\Preferences\Plug-in Development\API Baselines; (2) Update the option "Missing API baseline": Error -> Warning
  - Check Java Build Path to ensure: no error with "JRE Libarary System (unbound)"
  - ...
    
**Usage\:**
- Run runtime: *Right click to any project -> Run As -> Eclipse Application*.
- In runtime environment, create general project: *File -> New Project -> General -> Project -> Next ...*
- In general project, create .frsl file: *Right click -> New -> File -> Set name "test.frsl" -> Finish*
- Gen *.frslas* from *.frsl* file:
  - Open *.frsl* file -> Right click on white space in file -> FRSL -> Save As -> FRSLAS.
- Gen SMD, CD from *.frslas* file:
  - Open *.frslas* file -> Right click on file icon -> Frslas2Uml -> Generate UML Class diagram and State Machine.
- Visualize the UML diagram (by Papyrus Plugin):
  - Install [Papyrus Plugin (By Update Sites)](https://download.eclipse.org/modeling/mdt/papyrus/updates/releases/2022-03): *Help -> Install New Software -> Paste link to "Work with"-> Enter -> Tick all package -> Next ...*
  - Right click file icon .uml -> New -> Papyrus Model -> Finish
  - To Visualize Class Diagram:
    - In 'Model Explorer' section, right click top-level meta-concept -> New Diagram -> Class Diagram
    - Right click on white space -> Filters -> Synchronized with model.
    - Ctrl+A -> Right click on white space -> Filters -> Show/Hide Contents.
  - To Visualize State Machine Diagram:
    - In 'Model Explorer' section, right click 'StateMachine' meta-concept -> New Diagram -> State Machine Diagram
    - Right click on white space -> Filters -> Synchronized with model.
    - Ctrl+A -> Right click on white space -> Filters -> Show/Hide Contents.

