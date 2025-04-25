# Section09_Log_a_Measurement

This section explores the logging capabilities in Vector CANoe, based on **Section 9 of the Quick Start Guide**. It demonstrates how to configure a logging block, apply trigger conditions, and open/export the measurement logs.

This was executed in **View-Only Mode**, so while logging configurations could be visually explored and partially edited, **actual logging and simulation were not performed**.

---

## What Was Done in View-Only Mode
In this section, I explored how to configure logging settings and simulate a measurement process using the View-Only license of CANoe. Here's what was achieved:

### Opened the Logging Block Configuration
The process began by right-clicking on the logging block and selecting Logging File Configuration. This allowed access to settings despite simulation being disabled in view-only mode.
Screenshot: section9_logging_block_started_measurement.png

###  Configured Logging Parameters
selected the *.asc ASCII format for easier visualization and enabled filters such as logging of bus events, CAPL events, and diagnostic events. The file naming format was also set using field codes.
Screenshot: section9_logging_configuration_dialog.png

### Opened Trigger Configuration Dialog
Using the Toggle Trigger mode, we simulated logging behavior based on a timeline, including pre-trigger and post-trigger buffers.
Screenshot: section9_trigger_configuration_timeline.png

### Explored User Defined Conditions
Inside the trigger configuration, we examined how to define symbolic messages like DiagResponse_Motor or DiagRequest. These symbolic conditions are useful for advanced trigger-based logging.
Screenshot: section9_trigger_user_defined_conditions_menu.png

### Simulated Starting the Measurement
Although we couldn’t run a real simulation, we observed how CANoe indicates logging start with greyed-out indicators. This visually simulated what would happen in licensed mode.
Screenshot: section9_logging_started_continuous_mode.png

### Opened a Sample Log File
A sample log file Log_CAN1.asc was opened using the context menu option Open Logging File.... This provided insights into how log data is displayed in ASCII format.
Screenshot: section9_open_logging_file_menu.png
File Reference: Log_CAN1.asc

## What Could Have Been Done in Licensed Mode
If a fully licensed version of CANoe was available, the following enhancements and features would have been usable:

### Logging Execution
In view-only mode, you cannot start or save new log files. A licensed setup allows real-time data recording to .asc or .blf formats.

### Trigger-Based Logging
While I configured triggers, they are inactive in view-only mode. With a license, triggers like CAPL conditions or symbolic signals can start and stop logging automatically.

### Signal Export
Exporting decoded signal values to formats like .csv or .mat is disabled. Full license users can export these values for offline analysis in Excel or MATLAB.

### Logging Playback & Live Filtering
Logs can’t be replayed live. In licensed mode, one can replay, filter, and correlate logs using the Trace Window and Signal Graphs.

### CAPL Automation
In view-only mode, CAPL scripts are visible but non-executable. A full version would let users run automation, error injections, or simulate diagnostic sessions.

## Summary

This section served to **familiarize with CANoe logging workflow**, from setting filters to defining start/stop conditions. Even without a licensed setup, the following were accomplished:

- Navigated full logging configuration menu
- Understood symbolic trigger conditions
- Interpreted structure of `.asc` logs
- Documented setup using screenshots for learning and sharing
