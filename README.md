org.eclipse.papyrus.onefile.rcptt.tests
=======================================

This project is an example on how to set up Rcptt tests for the Papyrus project.

To use :
 - zip the rcp you want to test
 - reference the zip in the pom.xml		
			<aut>
				<explicit>{path to the zip here}</explicit>
            </aut> 
 - mvn clean test	

The expected log result should be looking like this one : 
[INFO] Pass 1 (4) processed. 0 failed. spent: 0:13, 0:08 mins remaining. DeleteAllFilesModel. time: 12923ms
[INFO] Pass 2 (4) processed. 0 failed. spent: 0:24, 0:06 mins remaining. DeleteSampleModel. time: 10693ms
[INFO] Fail 3 (4) processed. 1 failed. spent: 0:28, 0:00 mins remaining. MoveAllFilesModel. time: 3764ms  Cause: Assertion of getItems().length failed: expected:<0> but was:<1>.
[INFO] Pass 4 (4) processed. 1 failed. spent: 0:40, 0:00 mins remaining. RenameAllFilesModel. time: 12077ms
[INFO] Failed Tests:
[INFO] MoveAllFilesModel

The third test is failing in my tested version (Papyrus Luna)

You will find the result in target\results\org.eclipse.papyrus.onefile.rcptt.tests.html
 
1 : https://eclipse.org/papyrus/
2 : https://eclipse.org/rcptt/