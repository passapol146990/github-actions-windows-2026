# github actions windows 2026
System.ArgumentOutOfRangeException: Index and length must refer to a location within the string. (Parameter 'length')    at System.String.ThrowSubstringArgumentOutOfRange(Int32 startIndex, Int32 length)    at System.String.Substring(Int32 startIndex, Int32 length)    at GitHub.DistributedTask.Logging.ValueEncoders.PowerShellPreAmpersandEscape(String value)    at GitHub.DistributedTask.Logging.SecretMasker.AddValue(String value)    at GitHub.Runner.Worker.Worker.InitializeSecretMasker(AgentJobRequestMessage message)    at GitHub.Runner.Worker.Worker.RunAsync(String pipeIn, String pipeOut)    at GitHub.Runner.Worker.Program.MainAsync(IHostContext context, String[] args)


# How to Fix
## step 1 open powershell admin
```
[System.Globalization.CultureInfo]::CurrentCulture.Name
```
### if result 'en-US' Successfully. 
### but not use 
```
[System.Environment]::SetEnvironmentVariable("DOTNET_SYSTEM_GLOBALIZATION_INVARIANT", "1", "Machine")
```
### Close powershell 
### New powershell 
### Check step 1 again. if  'en-US' Successfully.


# run "./run.cmd" enjoy

