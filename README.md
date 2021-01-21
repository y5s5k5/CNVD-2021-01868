Experimental environment: win10 x64      
Software official website:http://www.v-secure.cn   
Software version:4.0.1.1445   
Affected Component: JingyunSd.exe    
  
The root cause of this vulnerability is that ordinary users can open Jingyun Antivirus, and when processing malicious samples, they did not judge the file parsing point, did not use the simulation token, and did not judge whether the target file has the write permission, and the attacker could use the symbolic link. Hijacking attack, which will delete arbitrary files with system permissions and cause local privilege escalation   
You can delete the dll path of the system dll or other high-privileged processes, provided that these paths are writable by ordinary users, and then place your dll for dll hijacking to achieve privilege escalation
