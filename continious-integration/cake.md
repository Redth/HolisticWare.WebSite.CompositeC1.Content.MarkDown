# Cake


## Internal compiler error

### Problem

	Compiling build script...
	unknown.cake (33,20): 
	Internal compiler error during parsingSystem.ArgumentOutOfRangeException: 
	Index was out of range. Must be non-negative and less than the size of the collection.
	Parameter name: index
		at System.ThrowHelper.ThrowArgumentOutOfRangeException (ExceptionArgument argument, ExceptionResource resource) <0x1973b00 + 0x0004d> in <filename unknown>:0 

		
### [Re]Solution/Workaround

	check trailing ';'
	

## Win32Exception - StartProcess

### Problem
	
	Error: System.ComponentModel.Win32Exception: 
	ApplicationName='external/binaries-xtensive/bat/compile-android.sh', 
	CommandLine='', 
	CurrentDirectory='/Projects/gl.xc.CI/XPlat-PInvoke/PJSIP', 
	Native error= Cannot find the specified file
		at System.Diagnostics.Process.Start_noshell (System.Diagnostics.ProcessStartInfo startInfo, System.Diagnostics.Process process) <0x3d04668 + 0x0055f> in <filename unknown>:0 	

### [Re]Solution/Workaround

Add execute right

	process_executable = @"chmod";
	process_arguments = @"+x ./external/binaries-xtensive/bat/compile-android.sh";
	StartProcess(process_executable, process_arguments);

	


