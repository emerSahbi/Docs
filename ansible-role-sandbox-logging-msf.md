# ansible-role-sandbox-logging-msf

This repository contains an Ansible role dedicated to logging Metasploit Framework commands executed locally within the CyberRangeCZ sandbox environments. Given Metasploit's role as a primary tool for penetration testing, comprehensive logging of its usage is paramount for effective cybersecurity training, assessment, and analysis.

## Key Features:

*   **Metasploit Command Logging**: Enables the capture of commands entered into the Metasploit console.
*   **Enhanced History Recording**: Modifies the default Metasploit behavior by patching the `/lib/rex/ui/text/shell.rb` file. This ensures that *all* commands, both correct/known and incorrect/unknown, are recorded to the history file. This enhanced logging provides deeper insights into trainee thought processes and debugging efforts.
*   **Requires Metasploit**: Assumes that Metasploit Framework is already installed on the target machine.
*   **Requires Root Access**: Modifying core Metasploit files requires elevated privileges (`become: yes`).
*   **User-Specific Application**: The role's effects are limited to users known at the time of its execution. Therefore, if new users are being provisioned, the `ansible-role-user-access` role must be executed *before* this role to ensure proper logging for those users.

## Importance in CyberRangeCZ:

This role is exceptionally valuable for instructors and trainers in the CyberRangeCZ platform:

*   **Detailed Trainee Assessment**: Provides a granular view of how trainees interact with Metasploit, allowing instructors to evaluate their understanding of the tool, their exploit selection, payload generation, and post-exploitation techniques.
*   **Learning Process Insight**: By logging incorrect commands, instructors can understand common errors or misconceptions, facilitating targeted feedback and improving learning outcomes.
*   **Incident Reconstruction**: Aids in reconstructing the sequence of events during a simulated attack, which is vital for debriefing and teaching incident response procedures.
*   **Compliance and Auditing**: Creates a verifiable record of actions performed with a powerful tool like Metasploit within a controlled environment.

This role contributes significantly to making the CyberRangeCZ training environments highly observable and auditable, enhancing the educational value of offensive security exercises.
