---
title: DEBUG\_ENGOPT\_XXX
description: The DEBUG\_ENGOPT\_XXX constants are global options that affect the behavior of the debugger engine.
ms.date: 08/10/2018
topic_type:
- apiref
ms.topic: reference
api_name:
- DEBUG_ENGOPT_XXX
api_location:
- DbgEng.h
api_type:
- HeaderDef
---

# DEBUG\_ENGOPT\_XXX

The following global options affect the behavior of the debugger engine.
<table>
<tr>
<th>Constant</th>
<th>Description</th>
</tr>
<tr VALIGN="top">
<td align="left" width="40%"><a id="DEBUG_ENGOPT_IGNORE_DBGHELP_VERSION"></a><a id="debug_engopt_ignore_dbghelp_version"></a><dl>
<dt><b>DEBUG_ENGOPT_IGNORE_DBGHELP_VERSION</b></dt>
</dl>
</td>
<td align="left" width="60%">
<p>The debugger engine generates a warning instead of an error if the version of the DbgHelp DLL does not match the version of the debugger engine.</p>
</td>
</tr>
<tr VALIGN="top">
<td align="left" width="40%"><a id="DEBUG_ENGOPT_IGNORE_EXTENSION_VERSIONS"></a><a id="debug_engopt_ignore_extension_versions"></a><dl>
<dt><b>DEBUG_ENGOPT_IGNORE_EXTENSION_VERSIONS</b></dt>
</dl>
</td>
<td align="left" width="60%">
<p>Disable version checking for extensions.  This suppresses the debugger engine's call to CheckVersion.</p>
</td>
</tr>
<tr VALIGN="top">
<td align="left" width="40%"><a id="DEBUG_ENGOPT_ALLOW_NETWORK_PATHS"></a><a id="debug_engopt_allow_network_paths"></a><dl>
<dt><b>DEBUG_ENGOPT_ALLOW_NETWORK_PATHS</b></dt>
</dl>
</td>
<td align="left" width="60%">
<p>Network shares can be used for loading symbols and extensions. This option prevents the engine from disallowing network paths when debugging some system processes and should be used with caution.</p>
<p>This option cannot be set if DEBUG_ENGOPT_DISALLOW_NETWORK_PATHS is set.</p>
</td>
</tr>
<tr VALIGN="top">
<td align="left" width="40%"><a id="DEBUG_ENGOPT_DISALLOW_NETWORK_PATHS"></a><a id="debug_engopt_disallow_network_paths"></a><dl>
<dt><b>DEBUG_ENGOPT_DISALLOW_NETWORK_PATHS</b></dt>
</dl>
</td>
<td align="left" width="60%">
<p>Network shares cannot be used for loading symbols and extensions. The engine attempts to set this option when debugging some system processes.</p>
<p>This option cannot be set if DEBUG_ENGOPT_ALLOW_NETWORK_PATHS is set.</p>
</td>
</tr>
<tr VALIGN="top">
<td align="left" width="40%"><a id="DEBUG_ENGOPT_NETWORK_PATHS"></a><a id="debug_engopt_network_paths"></a><dl>
<dt><b>DEBUG_ENGOPT_NETWORK_PATHS</b></dt>
</dl>
</td>
<td align="left" width="60%">
<p>Bitwise OR of DEBUG_ENGOPT_ALLOW_NETWORK_PATHS and DEBUG_ENGOPT_DISALLOW_NETWORK_PATHS.</p>
</td>
</tr>
<tr VALIGN="top">
<td align="left" width="40%"><a id="DEBUG_ENGOPT_IGNORE_LOADER_EXCEPTIONS"></a><a id="debug_engopt_ignore_loader_exceptions"></a><dl>
<dt><b>DEBUG_ENGOPT_IGNORE_LOADER_EXCEPTIONS</b></dt>
</dl>
</td>
<td align="left" width="60%">
<p>Ignore expected first-chance exceptions that are generated by the loader in certain older versions of Windows.</p>
</td>
</tr>
<tr VALIGN="top">
<td align="left" width="40%"><a id="DEBUG_ENGOPT_INITIAL_BREAK"></a><a id="debug_engopt_initial_break"></a><dl>
<dt><b>DEBUG_ENGOPT_INITIAL_BREAK</b></dt>
</dl>
</td>
<td align="left" width="60%">
<p>Break into the debugger at the target's initial event.</p>
</td>
</tr>
<tr VALIGN="top">
<td align="left" width="40%"><a id="DEBUG_ENGOPT_INITIAL_MODULE_BREAK"></a><a id="debug_engopt_initial_module_break"></a><dl>
<dt><b>DEBUG_ENGOPT_INITIAL_MODULE_BREAK</b></dt>
</dl>
</td>
<td align="left" width="60%">
<p>Break into the debugger when the target loads its first module.</p>
</td>
</tr>
<tr VALIGN="top">
<td align="left" width="40%"><a id="DEBUG_ENGOPT_FINAL_BREAK"></a><a id="debug_engopt_final_break"></a><dl>
<dt><b>DEBUG_ENGOPT_FINAL_BREAK</b></dt>
</dl>
</td>
<td align="left" width="60%">
<p>Break into the debugger at the target's final event. In a live user-mode target, this is when the process exits. It has no effect in kernel mode.</p>
</td>
</tr>
<tr VALIGN="top">
<td align="left" width="40%"><a id="DEBUG_ENGOPT_NO_EXECUTE_REPEAT"></a><a id="debug_engopt_no_execute_repeat.md"></a><dl>
<dt><b>DEBUG_ENGOPT_NO_EXECUTE_REPEAT</b></dt>
</dl>
</td>
<td align="left" width="60%">
<p>When given an empty command, the debugger engine does not repeat the last command.</p>
</td>
</tr>
<tr VALIGN="top">
<td align="left" width="40%"><a id="DEBUG_ENGOPT_FAIL_INCOMPLETE_INFORMATION"></a><a id="debug_engopt_fail_incomplete_information.md"></a><dl>
<dt><b>DEBUG_ENGOPT_FAIL_INCOMPLETE_INFORMATION</b></dt>
</dl>
</td>
<td align="left" width="60%">
<p>Prevent the debugger from loading modules whose images cannot be mapped.</p>
<p>The debugger attempts to load images when debugging minidumps that do not contain images.</p>
</td>
</tr>
<tr VALIGN="top">
<td align="left" width="40%"><a id="DEBUG_ENGOPT_ALLOW_READ_ONLY_BREAKPOINTS"></a><a id="debug_engopt_allow_read_only_breakpoints"></a><dl>
<dt><b>DEBUG_ENGOPT_ALLOW_READ_ONLY_BREAKPOINTS</b></dt>
</dl>
</td>
<td align="left" width="60%">
<p>Allow the debugger engine to manipulate page protections on the target to allow for setting software breakpoints in a read-only section of memory.</p>
<p>When setting software breakpoints, the engine transparently alters the target's memory to insert an interrupt instruction.</p>
</td>
</tr>
<tr VALIGN="top">
<td align="left" width="40%"><a id="DEBUG_ENGOPT_SYNCHRONIZE_BREAKPOINTS"></a><a id="debug_engopt_synchronize_breakpoints"></a><dl>
<dt><b>DEBUG_ENGOPT_SYNCHRONIZE_BREAKPOINTS</b></dt>
</dl>
</td>
<td align="left" width="60%">
<p>In live user-mode debugging, the engine  performs extra work when inserting and removing breakpoints to ensure that all threads in the target have a consistent breakpoint state at all times.</p>
<p>This option is useful when multiple threads can use the code for which the breakpoint is set. However, it can introduce the possibility of deadlocks.</p>
</td>
</tr>
<tr VALIGN="top">
<td align="left" width="40%"><a id="DEBUG_ENGOPT_DISALLOW_SHELL_COMMANDS"></a><a id="debug_engopt_disallow_shell_commands"></a><dl>
<dt><b>DEBUG_ENGOPT_DISALLOW_SHELL_COMMANDS</b></dt>
</dl>
</td>
<td align="left" width="60%">
<p>Disallow executing shell commands through the debugger.</p>
<p>After this option has been set, it cannot be unset.</p>
</td>
</tr>
<tr VALIGN="top">
<td align="left" width="40%"><a id="DEBUG_ENGOPT_KD_QUIET_MODE"></a><a id="debug-engopt-kd-quiet-mode.md"></a><dl>
<dt><b>DEBUG_ENGOPT_KD_QUIET_MODE</b></dt>
</dl>
</td>
<td align="left" width="60%">
<p>Turn on quiet mode. For more information, see <a href="sq--set-quiet-mode-.md"><b>sq (Set Quiet Mode)</b></a>. </p>
</td>
</tr>
<tr VALIGN="top">
<td align="left" width="40%"><a id="DEBUG_ENGOPT_DISABLE_MANAGED_SUPPORT"></a><a id="debug_engopt_disable_managed_support"></a><dl>
<dt><b>DEBUG_ENGOPT_DISABLE_MANAGED_SUPPORT</b></dt>
</dl>
</td>
<td align="left" width="60%">
<p>Disables debugger engine support for managed code. If support for managed code is already in use, this option has no effect.</p>
</td>
</tr>
<tr VALIGN="top">
<td align="left" width="40%"><a id="DEBUG_ENGOPT_DISABLE_MODULE_SYMBOL_LOAD"></a><a id="debug_engopt_disable_module_symbol_load"></a><dl>
<dt><b>DEBUG_ENGOPT_DISABLE_MODULE_SYMBOL_LOAD</b></dt>
</dl>
</td>
<td align="left" width="60%">
<p>The debugger does not load symbols for modules that are loaded while this flag is set.</p>
</td>
</tr>
<tr VALIGN="top">
<td align="left" width="40%"><a id="DEBUG_ENGOPT_DISABLE_EXECUTION_COMMANDS"></a><a id="debug_engopt_disable_execution_commands"></a><dl>
<dt><b>DEBUG_ENGOPT_DISABLE_EXECUTION_COMMANDS</b></dt>
</dl>
</td>
<td align="left" width="60%">
<p>Prevents any commands that would cause the target to begin executing.</p>
</td>
</tr>
<tr VALIGN="top">
<td align="left" width="40%"><a id="DEBUG_ENGOPT_DISALLOW_IMAGE_FILE_MAPPING"></a><a id="debug_engopt_disallow_image_file_mapping"></a><dl>
<dt><b>DEBUG_ENGOPT_DISALLOW_IMAGE_FILE_MAPPING</b></dt>
</dl>
</td>
<td align="left" width="60%">
<p>Disallows mapping of image files from disk. For example, this option disallows image mapping for memory
content during debugging of minidump files.
 This option does not affect existing mappings; it affects only subsequent attempts to map image files.</p>
</td>
</tr>
<tr VALIGN="top">
<td align="left" width="40%"><a id="DEBUG_ENGOPT_PREFER_DML"></a><a id="debug_engopt_prefer_dml"></a><dl>
<dt><b>DEBUG_ENGOPT_PREFER_DML</b></dt>
</dl>
</td>
<td align="left" width="60%">
<p>The debugger runs DML-enhanced versions of commands
and operations by default.</p>
</td>
</tr>
<tr VALIGN="top">
<td align="left" width="40%"><a id="DEBUG_ENGOPT_DISABLESQM"></a><a id="debug_engopt_disablesqm"></a><dl>
<dt><b>DEBUG_ENGOPT_DISABLESQM</b></dt>
</dl>
</td>
<td align="left" width="60%">
<p>Disables upload of Software Quality Metrics (SQM) data.</p>
</td>
</tr>
</table>


## Requirements

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Header</p></td>
<td align="left">DbgEng.h (include DbgEng.h)</td>
</tr>
</tbody>
</table>

 
