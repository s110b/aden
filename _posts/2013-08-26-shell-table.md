---
layout: post
title: " Shell Commands and What They Do "
description: ""
category: 
tags: []
---



`The C shell provides the following built-in commands:`
<table width="100%" cellspacing="0" cellpadding="5" border="1" align="center">
    <tbody>
        <tr valign="top" align="left">
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif"><i><b>#</b></i></font>
            </td>
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif">Marks a command.</font>
            </td>
        </tr>
        <tr valign="top" align="left">
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif"><i><b>alias</b></i></font>
            </td>
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif">Displays alias.</font>
            </td>
        </tr>
        <tr valign="top" align="left">
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif"><i><b>bg</b></i></font>
            </td>
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif">Resumes job in the background.</font>
            </td>
        </tr>
        <tr valign="top" align="left">
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif"><i><b>break</b></i></font>
            </td>
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif">Resumes execution after the loop.</font>
            </td>
        </tr>
        <tr valign="top" align="left">
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif"><i><b>breaksw</b></i></font>
            </td>
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif">Breaks from a switch command; resumes after the endsw command.</font>
            </td>
        </tr>
        <tr valign="top" align="left">
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif"><i><b>case</b></i></font>
            </td>
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif">Defines a label in a switch command.</font>
            </td>
        </tr>
        <tr valign="top" align="left">
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif"><i><b>cd</b></i></font>
            </td>
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif">Changes directory.</font>
            </td>
        </tr>
        <tr valign="top" align="left">
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif"><i><b>chdir</b></i></font>
            </td>
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif">Changes directory, same as <i>cd</i>.</font>
            </td>
        </tr>
        <tr valign="top" align="left">
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif"><i><b>continue</b></i></font>
            </td>
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif">Continues a loop.</font>
            </td>
        </tr>
        <tr valign="top" align="left">
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif"><i><b>default</b></i></font>
            </td>
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif">Specifies the default case in a switch.</font>
            </td>
        </tr>
        <tr valign="top" align="left">
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif"><i><b>dirs</b></i></font>
            </td>
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif">Displays the directory stack.</font>
            </td>
        </tr>
        <tr valign="top" align="left">
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif"><i><b>echo</b></i></font>
            </td>
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif">Writes arguments to the standard output of the shell.</font>
            </td>
        </tr>
        <tr valign="top" align="left">
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif"><i><b>eval</b></i></font>
            </td>
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif">Evaluates a command.</font>
            </td>
        </tr>
        <tr valign="top" align="left">
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif"><i><b>exec</b></i></font>
            </td>
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif">Executes the command in the current shell.</font>
            </td>
        </tr>
        <tr valign="top" align="left">
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif"><i><b>exit</b></i></font>
            </td>
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif">Exits the shell.</font>
            </td>
        </tr>
        <tr valign="top" align="left">
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif"><i><b>fg</b></i></font>
            </td>
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif">Brings a job in the foreground.</font>
            </td>
        </tr>
        <tr valign="top" align="left">
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif"><i><b>foreach</b></i></font>
            </td>
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif">Specifies a looping control statement and execute a sequence of commands until reaching an end command.</font>
            </td>
        </tr>
        <tr valign="top" align="left">
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif"><i><b>glob</b></i></font>
            </td>
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif">Writes arguments to the standard output of the shell, like the echo command, but without the new line.</font>
            </td>
        </tr>
        <tr valign="top" align="left">
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif"><i><b>goto</b></i></font>
            </td>
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif">Continues execution after the specified label.</font>
            </td>
        </tr>
        <tr valign="top" align="left">
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif"><i><b>hashstat</b></i></font>
            </td>
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif">Displays hash table statistics.</font>
            </td>
        </tr>
        <tr valign="top" align="left">
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif"><i><b>history</b></i></font>
            </td>
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif">Displays the history list.</font>
            </td>
        </tr>
        <tr valign="top" align="left">
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif"><i><b>if</b></i></font>
            </td>
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif">Executes a command if condition met.</font>
            </td>
        </tr>
        <tr valign="top" align="left">
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif"><i><b>jobs</b></i></font>
            </td>
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif">Lists active jobs.</font>
            </td>
        </tr>
    </tbody>
</table>
<table width="100%" cellspacing="0" cellpadding="5" border="1" align="center">
    <tbody>
        <tr valign="top" align="left">
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif"><i><b>kill</b></i></font>
            </td>
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif">Sends a signal to a process. <i>term</i> (terminate) is the default signal.</font>
            </td>
        </tr>
        <tr valign="top" align="left">
            <td>
                <p>
                    <font size="2" face="Verdana, Arial, Helvetica, sans-serif"><i><b>limit</b></i></font>
                </p>
            </td>
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif">Sets or list system resource limits.</font>
            </td>
        </tr>
        <tr valign="top" align="left">
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif"><i><b>login</b></i></font>
            </td>
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif">Logs on.</font>
            </td>
        </tr>
        <tr valign="top" align="left">
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif"><i><b>logout</b></i></font>
            </td>
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif">Logs out.</font>
            </td>
        </tr>
        <tr valign="top" align="left">
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif"><i><b>nice</b></i></font>
            </td>
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif">Changes the priority of commands run in the shell.</font>
            </td>
        </tr>
        <tr valign="top" align="left">
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif"><i><b>nohup</b></i></font>
            </td>
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif">Ignores the hangup signal.</font>
            </td>
        </tr>
        <tr valign="top" align="left">
            <td>
                <p>
                    <font size="2" face="Verdana, Arial, Helvetica, sans-serif"><i><b>notify</b></i></font>
                </p>
            </td>
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif">Notifies the user about changes in job status.</font>
            </td>
        </tr>
        <tr valign="top" align="left">
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif"><i><b>onintr</b></i></font>
            </td>
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif">Tells the shell what to do on interrupt.</font>
            </td>
        </tr>
        <tr valign="top" align="left">
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif"><i><b>popd</b></i></font>
            </td>
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif">Pops the top directory off the directory stack and changes to the new top directory.</font>
            </td>
        </tr>
        <tr valign="top" align="left">
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif"><i><b>pushd</b></i></font>
            </td>
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif">Exchanges the top two elements of the directory stack.</font>
            </td>
        </tr>
        <tr valign="top" align="left">
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif"><i><b>rehash</b></i></font>
            </td>
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif">Re-computes the hash table of the contents of the directories in the path shell variable.</font>
            </td>
        </tr>
        <tr valign="top" align="left">
            <td>
                <p>
                    <font size="2" face="Verdana, Arial, Helvetica, sans-serif"><i><b>repeat</b></i></font>
                </p>
            </td>
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif">Repeats the execution of a command.</font>
            </td>
        </tr>
        <tr valign="top" align="left">
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif"><i><b>set</b></i></font>
            </td>
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif">Displays or set the value of a shell variable.</font>
            </td>
        </tr>
        <tr valign="top" align="left">
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif"><i><b>setenv</b></i></font>
            </td>
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif">Sets environment variables.</font>
            </td>
        </tr>
        <tr valign="top" align="left">
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif"><i><b>shift</b></i></font>
            </td>
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif">Shifts shell arguments.</font>
            </td>
        </tr>
        <tr valign="top" align="left">
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif"><i><b>source</b></i></font>
            </td>
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif">Reads commands from a script.</font>
            </td>
        </tr>
        <tr valign="top" align="left">
            <td>
                <p>
                    <font size="2" face="Verdana, Arial, Helvetica, sans-serif"><i><b>stop</b></i></font>
                </p>
            </td>
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif">Stops a background job.</font>
            </td>
        </tr>
        <tr valign="top" align="left">
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif"><i><b>suspend</b></i></font>
            </td>
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif">Stops the current shell.</font>
            </td>
        </tr>
        <tr valign="top" align="left">
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif"><i><b>switch</b></i></font>
            </td>
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif">Starts a switch.</font>
            </td>
        </tr>
        <tr valign="top" align="left">
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif"><i><b>time</b></i></font>
            </td>
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif">Displays the time used to execute commands.</font>
            </td>
        </tr>
        <tr valign="top" align="left">
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif"><i><b>umask</b></i></font>
            </td>
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif">Shows or set file permissions.</font>
            </td>
        </tr>
        <tr valign="top" align="left">
            <td>
                <p>
                    <font size="2" face="Verdana, Arial, Helvetica, sans-serif"><i><b>unalias</b></i></font>
                </p>
            </td>
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif">Removes command alias.</font>
            </td>
        </tr>
        <tr valign="top" align="left">
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif"><i><b>unhash</b></i></font>
            </td>
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif">Disables the internal hash table.</font>
            </td>
        </tr>
        <tr valign="top" align="left">
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif"><i><b>unlimit</b></i></font>
            </td>
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif">Removes limitations on system Resource.</font>
            </td>
        </tr>
        <tr valign="top" align="left">
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif"><i><b>unset</b></i></font>
            </td>
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif">Deletes shell variables.</font>
            </td>
        </tr>
        <tr valign="top" align="left">
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif"><i><b>unsetenv</b></i></font>
            </td>
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif">Deletes environment variables.</font>
            </td>
        </tr>
        <tr valign="top" align="left">
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif"><i><b>wait</b></i></font>
            </td>
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif">Waits for background jobs to complete.</font>
            </td>
        </tr>
        <tr valign="top" align="left">
            <td>
                <p>
                    <font size="2" face="Verdana, Arial, Helvetica, sans-serif"><i><b>while …end</b></i></font>
                </p>
            </td>
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif">Executes the commands between the while and matching end statements repeatedly.</font>
            </td>
        </tr>
        <tr valign="top" align="left">
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif"><i><b>@</b></i></font>
            </td>
            <td>
                <font size="2" face="Verdana, Arial, Helvetica, sans-serif">Displays or set the values of all the shell variables.</font>
            </td>
        </tr>
    </tbody>
</table>
