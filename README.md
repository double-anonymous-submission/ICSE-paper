# ASE-paper442
When performing fault localization in vBuggy, we observe a significant decrease of approximately 200% in the effectiveness of fault localization results in Pattern 4. Through manual analysis of bugs in Pattern 4, we observe that even though developers did not modify the fault-triggering tests, they may still have introduced developers’ knowledge affecting fault localization results. Developers may introduce their knowledge in different ways, such as modifying functions involved in test execution or adjusting the test setup configuration. Let’s take bug Lang 57 as an example. In this bug, the test suite LocaleUtilsTest was modified by adding an extra setUp method that runs before each test case. This modification was made after the bug report was submitted. The purpose of the added setUp method is to ensure that fault-triggering tests fail if the fields are not correctly initialized before the test execution starts. Thus, the results of fault localization is overestimated in vD4J as developers’ knowledge was introduced in the test setup configuration. Our finding shows that developers’ knowledge may not always be directly incorporated into the fault-triggering tests themselves. Future research may explore bugs from Pattern 4 to investigate and characterize the instances where developers’ knowledge is introduced outside of the fault-triggering tests.

This is a public repository for ASE submission #442: "Back to the Future! Studying Data Cleanness in Defects4J and its Impact on Fault Localization"

```
│
├── patterns              Dataset on individual change pattern (RQ1)
│  
├── manual_study
│   ├── code_changes      For every bug, we provide code changes on the individual faul-triggering tests between the bug creation and resolution.
│   └─ manual.xlsx        Process and results of manual study (RQ2)
│  
├── system_stats          General statistics on the studied systems (e.g., LOC)
│  
├── timeline              Dataset on the timeline of the bug report, bug fix, and modifications on the fault-triggering tests.
│   ├── bug_fix.csv			  
│   ├── bug_report.csv			
│   └─ triggering_tests.csv 
│ 
├── bug_repository.csv    List of source repositories for studied systems
└─ fault_triggering_tests.csv     List of fault-triggering tests
```
The SBFL scores and Program Spectra files can be found here: https://doi.org/10.5281/zenodo.7922699
