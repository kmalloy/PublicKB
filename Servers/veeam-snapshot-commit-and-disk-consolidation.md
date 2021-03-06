{{{
  "title": "Veeam Snapshot Commit & Disk Consolidation",
  "date": "12-9-2014",
  "author": "Kelly Malloy",
  "attachments": [],
  "contentIsHTML": false
}}}

<p>Currently the CenturyLink Cloud platform utilizes the snapshot management functionality of VMWare Vsphere. More information on exactly what this process is, and how it works can be found at this URL:</p>
<p>http://kb.vmware.com/selfservice/microsites/search.do?language=en_US&amp;cmd=displayKC&amp;externalId=1015180</p>
<p>Workloads that generate intensive Disk Subsystem IO (Mail systems, Database Servers, etc) can pause on occasion during the snapshot removal process. Often moving this machine to an SSD based Disk Subsystem can significantly reduce or eliminate this pause. In certain cases, a pause can still exist. There are two steps that can be taken to help with this issue:</p>

1. Submit a ticket to noc@tier3.com asking for backup disable. NOTE:&nbsp; Virtual machine backups will not be available for this machine. It will be the customer's responsibility to implement an application level backup for any important data.
2. Customer can design an active/passive design of their systems that backs up only the passive nodes, leaving active nodes available for data processing.

<p>When a customer decides to use active/passive designs there are several useful articles they can reference. There are also several things that can be tweaked to provide a better user experience. The links to those articles are below.</p>

<p>https://t3n.zendesk.com/entries/52018674-Windows-Clusters-Tuning-Network-Timeouts</p>
<p>http://technet.microsoft.com/en-us/library/ms189852%28v=sql.105%29.aspx</p>
<p>https://t3n.zendesk.com/entries/21381762-Creating-and-Managing-Server-Snapshots</p>






