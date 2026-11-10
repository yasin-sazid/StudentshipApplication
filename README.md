# Studentship Certificate Application

A JavaFX application modeling a studentship-certificate workflow with separate student and administrator interfaces. Developed as an object-oriented programming hackathon project, it combines desktop forms, persisted student records, and a bank-service interaction.

## Application workflow

- Students and administrators select their role at sign-in.
- Administrators create student entries through a dedicated form.
- Student records are loaded and stored through `StuInfoFile` and the student model classes.
- A signed-in student submits an application through the student interface.
- The submission workflow contacts a local bank service and produces a `certificate.txt` document.

## Repository structure

| Project | Responsibility |
| --- | --- |
| `Studentship Application/` | JavaFX forms, controllers, student models, and file persistence |
| `BankServer/` | Socket-based bank service and account storage |
| `BankClient/` | Standalone bank client |

Within the JavaFX project, `package1.Main` loads the login view. `Controller` handles role-aware login, `adminController` creates records, and `afterLogInController` coordinates application submission. FXML files separate view layouts from controller behavior.

## Launch the workflow

Use a JDK and JavaFX controls/FXML support. Import each directory as its own Java project with `src/` marked as the source root, retaining the FXML resources in `package1`.

1. Start `BankServer` using `mainPackage.MainClass`.
2. Run the JavaFX project's `package1.Main` from its project directory.
3. Use the administrator or student role to follow the corresponding workflow.

The student submission handler connects to `localhost:7921`. The bank projects' account data and the JavaFX project's `studentInfo` file provide the persisted state used by the exercises.

## Technical focus

FXML/controller separation, role-based desktop navigation, serialized domain records, Java sockets, and generated document output connect several object-oriented programming concepts in one application.

**Author:** Yasin Sazid, BSSE 1006 — SE 306, second year, third semester.
