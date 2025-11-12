
</head>

<body>

  <h2>🧪 Forensic Investigation Using Procmon During Malware Infection</h2>

  <h3>AIM</h3>
  <p>
    To use <b>Procmon (Process Monitor)</b> to identify and analyze suspicious system activities caused by a malware infection during a forensic investigation.
  </p>

  <h3>FORENSIC INVESTIGATION FLOW</h3>
  <p>
    1. Identify malware infection symptoms.<br>
    2. Launch Procmon to monitor real-time system activity.<br>
    3. Set filters to capture only suspicious operations.<br>
    4. Analyze abnormal file, registry, and process behavior.<br>
    5. Save captured logs as digital forensic evidence.
  </p>

  <h3>TOOLS APPLICATION & ANALYSIS ACCURACY</h3>
  <p>
    - <b>Tool Used:</b> Procmon (Process Monitor) from Microsoft Sysinternals.<br>
    - Captures file, registry, and process actions.<br>
    - Filtering isolates malware-related behavior for accurate analysis.
  </p>

  <h3>GITHUB REPOSITORY & VERSION CONTROL</h3>
  <p>
    - Repository Name: <b>Forensic-Investigation-Procmon</b><br>
    - All reports, screenshots, and logs are uploaded.<br>
    - Version control used to maintain investigation history.
  </p>

  <h3>STEPWISE EXECUTION</h3>

  <p class="step-title">Step 1: Open Procmon Tool</p>
  <p>Run <b>Procmon.exe</b> as Administrator. The tool starts capturing all live system events such as file, registry, and process activity.</p>
  <img src="https://github.com/user-attachments/assets/7444cac9-dd00-439e-950b-65557d93baf0" alt="P1">

  <p class="step-title">Step 2: Access Filter Option</p>
  <p>From the menu, click <b>Filter → Filter...</b> or press <b>Ctrl + L</b> to open the filter configuration window.</p>
  <img src="https://github.com/user-attachments/assets/fe0b14fc-5d12-4700-b536-0503afd97093" alt="P2">

  <p class="step-title">Step 3: Add Filter Conditions</p>
  <p>
    Inside the filter window, add the following conditions:<br>
    - Process Name contains <b>malware.exe</b><br>
    - Operation is <b>WriteFile</b><br>
    - Operation is <b>RegSetValue</b><br>
    - Path contains <b>Run</b><br>
    Click <b>Add</b> then <b>OK</b> to apply.
  </p>
  <img src="https://github.com/user-attachments/assets/84ecb291-47ee-421c-a0d7-af1b99282cca" alt="P3">

  <p class="step-title">Step 4: Apply Filter and Capture Suspicious Activity</p>
  <p>After applying filters, Procmon displays only suspicious operations. Observe process, operation, and path columns carefully.</p>
  <img src="https://github.com/user-attachments/assets/1eab24a1-ea48-4805-99f2-572fa750c6aa" alt="P4">

  <p class="step-title">Step 5: Observe Registry Changes</p>
  <p>Check for <b>RegSetValue</b> operations. Malware often edits registry keys to maintain persistence in the system.</p>
  <img src="https://github.com/user-attachments/assets/b4391831-80f5-4209-8227-95b390198378" alt="P5">

  <p class="step-title">Step 6: Observe File Activity</p>
  <p>Look for operations like <b>WriteFile</b> or <b>CreateFile</b>. Malware typically writes or drops files into sensitive directories.</p>
  <img src="https://github.com/user-attachments/assets/933f1e0c-0d04-4b81-a1cb-ecc1f3412c3e" alt="P6">

  <p class="step-title">Step 7: Identify Process Behavior</p>
  <p>Monitor <b>CreateProcess</b> events to detect abnormal parent-child process creation — an indication of malware execution.</p>
  <img src="https://github.com/user-attachments/assets/edf849f8-b557-4434-8684-fcea83737f08" alt="P7">

  <p class="step-title">Step 8: Stop Capture and Save Logs</p>
  <p>Click the <b>magnifying glass icon</b> to stop capturing. Then go to <b>File → Save → Events displayed using current filter</b> and save as <b>.PML</b> log file.</p>
  <img src="https://github.com/user-attachments/assets/d7dcc0a6-2e87-40b3-90fb-f4c221c8669f" alt="P8">

  <p class="step-title">Step 9: Final Output and Evidence</p>
  <p>The saved log shows file, registry, and process activities of the malware. These logs act as forensic evidence for analysis.</p>
  <img src="https://github.com/user-attachments/assets/d663e953-13f2-44a3-8409-5041b79a7188" alt="P9">

  <h3>CONCLUSION</h3>
  <p>
    Using <b>Procmon</b>, suspicious malware activities were successfully identified — including file writes, registry modifications, and unauthorized process creation. The captured logs serve as strong digital forensic evidence.
  </p>

  
  </p>

</body>
</html>
