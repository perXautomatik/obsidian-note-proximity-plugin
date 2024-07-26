**Overview**

This fork of the Lookalike Obsidian plugin aims to address performance issues encountered when processing large vaults. By offloading computationally intensive tasks to a PowerShell script, we aim to significantly improve the plugin's responsiveness and efficiency.

**Original Plugin ([Original repository](https://github.com/jlweston/obsidian-note-proximity-plugin))**

The original Lookalike plugin, available on the Obsidian plugin store ([Link to plugin page](https://obsidian.md/plugins?id=note-promixity)), identifies other notes similar to the current note. It analyzes word frequencies across all notes in the vault and compares them to the current note.

**Fork Objectives**

- Reduce the amount of JavaScript code in the plugin.
- Offload the majority of the plugin's logic to a PowerShell script.
- Improve the plugin's performance, especially when handling large vaults.
- Maintain the core functionality of the original plugin.

**Development Process**

To achieve these objectives, the following steps were taken:

1. **Identify performance bottlenecks:** The TfIdf calculations were identified as the primary performance bottleneck.
2. **Create a PowerShell script:** A PowerShell script named `TfIdfProcessor.ps1` was created to handle the computationally intensive tasks, including text processing, statistical calculations, and vector operations.
3. **Modify JavaScript code:** The JavaScript code was reduced to primarily handle Obsidian interactions and communication with the PowerShell script.
4. **Optimize data transfer:** Efficient data structures were implemented for passing data between JavaScript and PowerShell.

**Expected Improvements**

By delegating the heavy computational load to PowerShell, we anticipate a significant performance improvement, especially when processing large vaults. The reduced JavaScript codebase should also enhance maintainability and readability.

**Usage**

The usage instructions remain the same as the original plugin:

- **From within Obsidian:** Install the plugin from the Obsidian plugin store ([Link to plugin page](https://obsidian.md/plugins?id=note-promixity)).
- **From GitHub:** Download and install the plugin manually following the instructions in the original README.

**License**

This project is licensed under the MIT License ([Link to MIT License](https://opensource.org/license/MIT)).

**Support the Original Developer**

Consider supporting the original developer of the Lookalike plugin, Jamie Weston, through Buy Me A Coffee ([Link to Buy Me A Coffee](https://www.buymeacoffee.com/jamieweston)).
