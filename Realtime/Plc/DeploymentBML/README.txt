When exporting the configuration from the XPlanar configurator, .bml files are displayed. These must be manually copied to the Runtime IPC.

Alternatively, these can be transferred to the PLC deployment. Here is an example of this. For this purpose, a copy job was created in the “Plc Project” properties/deployment from  
%SOLUTIONPATH%XPlanarDemo\Plc\DeploymentBML
to 
C:\TwinCAT\3.1\Target\Config\XPlanar\bml

registered. Now the files are automatically transferred to the correct folder when the project is activated.