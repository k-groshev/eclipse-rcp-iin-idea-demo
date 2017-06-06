Just for demo.

I've created sample Eclipse RCP application with Eclipse Neon and import it to intelliJ IDEA Ultimate 2017.1.3 (EAP). 
I set up OSGi Framework to my Neon installation and add plugins directory as a library. After that, I've add this library as a
compile dependency to the main module. Defined OSGI facet and set manifest reference to my Eclipse-made MANIFEST.MF.

After that I've build project without any error. Created new launch configuration upon OSGi template with my bundle and some eclipse 
ones as described here: http://wiki.eclipse.org/Eclipse4/RCP/FAQ#Why_won.27t_my_application_start.3F

got error with this stacktrace:

!ENTRY org.eclipse.osgi 4 0 2017-06-06 11:55:26.002
!MESSAGE Application error
!STACK 1
java.lang.IllegalStateException: Unable to acquire application service. Ensure that the org.eclipse.core.runtime bundle is resolved and started (see config.ini).
	at org.eclipse.core.runtime.internal.adaptor.EclipseAppLauncher.start(EclipseAppLauncher.java:78)
	at org.eclipse.core.runtime.adaptor.EclipseStarter.run(EclipseStarter.java:388)
	at org.eclipse.core.runtime.adaptor.EclipseStarter.run(EclipseStarter.java:243)
	at org.eclipse.core.runtime.adaptor.EclipseStarter.main(EclipseStarter.java:216)
	at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
	at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62)
	at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
	at java.lang.reflect.Method.invoke(Method.java:497)
	at com.intellij.rt.execution.CommandLineWrapper.main(CommandLineWrapper.java:65)
