Practical Development Setup: Flutter, Python, MySQL, and VS Code Integration 



Task 1: Flutter & Dart Environment Setup
C:\Users\k>flutter --version
Building flutter tool...
Running pub upgrade...
Resolving dependencies... (4.1s)
Downloading packages... (10.5s)
Got dependencies.
Flutter 3.47.5 • channel stable • https://github.com/flutter/flutter.git
Framework • revision 6a19cca564 (11 days ago) • 2026-09-17 14:13:22 -0400
Engine • hash ab598368592da0064197e2bc15c7f5b0a2c6bb1f (revision af7e796e16) (11 days ago) • 2026-09-16 18:35:09.000Z
Tools • Dart 3.13.4 • DevTools 2.60.0

C:\Users\k>flutter doctor
Doctor summary (to see all details, run flutter doctor -v):
[√] Flutter (Channel stable, 3.47.5, on Microsoft Windows [Version 10.0.26200.9457], locale en-KE)
[√] Windows Version (Windows 11 or higher, 25H2, 2009)
[X] Android toolchain - develop for Android devices
    X Unable to locate Android SDK.
      Install Android Studio from: https://developer.android.com/studio/index.html
      On first launch it will assist you in installing the Android SDK components.
      (or visit https://flutter.dev/to/windows-android-setup for detailed instructions).
      If the Android SDK has been installed to a custom location, please use
      `flutter config --android-sdk` to update to that location.

[√] Chrome - develop for the web
[X] Visual Studio - develop Windows apps
    X Visual Studio not installed; this is necessary to develop Windows apps.
      Download at https://visualstudio.microsoft.com/downloads/.
      Please install the "Desktop development with C++" workload, including all of its default components
[√] Connected device (3 available)
[√] Network resources

! Doctor found issues in 2 categories.

C:\Users\k>flutter create my_first_app
Creating project my_first_app...
Resolving dependencies in `my_first_app`... (1.9s)
Downloading packages...
Got dependencies in `my_first_app`.
Wrote 131 files.

All done!
You can find general documentation for Flutter at: https://docs.flutter.dev/
Detailed API documentation is available at: https://api.flutter.dev/
If you prefer video documentation, consider: https://www.youtube.com/c/flutterdev

In order to run your application, type:

  $ cd my_first_app
  $ flutter run

Your application code is in my_first_app\lib\main.dart.


C:\Users\k>cd my_first_app

C:\Users\k\my_first_app>flutter devices
Found 3 connected devices:
  Windows (desktop) • windows • windows-x64    • Microsoft Windows [Version 10.0.26200.9457]
  Chrome (web)      • chrome  • web-javascript • Google Chrome 153.0.8010.54
  Edge (web)        • edge    • web-javascript • Microsoft Edge 154.0.4258.37

Run "flutter emulators" to list and start any available device emulators.

If you expect another device to be detected, please run "flutter doctor" to diagnose potential issues. You may also try increasing
the time to wait for connected devices with the "--device-timeout" flag. Visit https://flutter.dev/setup/ for troubleshooting tips.


Task 2: MySQL Database Management
 

CREATE DATABASE school;


USE school;


CREATE TABLE students (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100) NOT NULL,
    email VARCHAR(150) UNIQUE NOT NULL,
    enrolled_on DATE NOT NULL
);


INSERT INTO students (name, email, enrolled_on) VALUES 
('Alice Johnson', 'alice.johnson@example.com', '2026-01-15'),
('Bob Smith', 'bob.smith@example.com', '2026-02-01');


SELECT * FROM students;

Task 3: Python Environment & Dependency Isolation

C:\Users\k\Documents>mkdir python_setup_lab

C:\Users\k\Documents>cd python_setup_lab

C:\Users\k\Documents\python_setup_lab>python3 -m venv venv

C:\Users\k\Documents\python_setup_lab>source venv/bin/activate
'source' is not recognized as an internal or external command,
operable program or batch file.

C:\Users\k\Documents\python_setup_lab>pip install requests
Collecting requests
  Using cached requests-2.34.2-py3-none-any.whl.metadata (4.8 kB)
Collecting charset_normalizer<4,>=2 (from requests)
  Using cached charset_normalizer-3.5.1-cp314-cp314-win_amd64.whl.metadata (46 kB)
Collecting idna<4,>=2.5 (from requests)
  Using cached idna-3.20-py3-none-any.whl.metadata (7.2 kB)
Collecting urllib3<3,>=1.26 (from requests)
  Using cached urllib3-2.8.0-py3-none-any.whl.metadata (7.4 kB)
Collecting certifi>=2023.5.7 (from requests)
  Using cached certifi-2026.7.22-py3-none-any.whl.metadata (2.5 kB)
Using cached requests-2.34.2-py3-none-any.whl (73 kB)
Using cached charset_normalizer-3.5.1-cp314-cp314-win_amd64.whl (204 kB)
Using cached idna-3.20-py3-none-any.whl (69 kB)
Using cached urllib3-2.8.0-py3-none-any.whl (135 kB)
Using cached certifi-2026.7.22-py3-none-any.whl (136 kB)
Installing collected packages: urllib3, idna, charset_normalizer, certifi, requests
   ━━━━━━━━╺━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 1/5 [idna]  WARNING: The script idna.exe is installed in 'C:\Users\k\AppData\Local\Python\pythoncore-3.14-64\Scripts' which is not on PATH.
  Consider adding this directory to PATH or, if you prefer to suppress this warning, use --no-warn-script-location.
   ━━━━━━━━━━━━━━━━╺━━━━━━━━━━━━━━━━━━━━━━━ 2/5 [charset_normalizer]  WARNING: The script normalizer.exe is installed in 'C:\Users\k\AppData\Local\Python\pythoncore-3.14-64\Scripts' which is not on PATH.
  Consider adding this directory to PATH or, if you prefer to suppress this warning, use --no-warn-script-location.
Successfully installed certifi-2026.7.22 charset_normalizer-3.5.1 idna-3.20 requests-2.34.2 urllib3-2.8.0

C:\Users\k\Documents\python_setup_lab>pip list
Package            Version
------------------ ---------
certifi            2026.7.22
charset-normalizer 3.5.1
idna               3.20
pip                26.2.1
requests           2.34.2
urllib3            2.8.0

C:\Users\k\Documents\python_setup_lab>pip freeze > requirements.txt




Task 4: VS Code Workspace Configuration

.
