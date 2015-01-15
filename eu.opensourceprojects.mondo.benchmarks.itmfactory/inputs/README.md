Thanks to the [MoDisco](https://eclipse.org/MoDisco/) Java discoverer, we are able to extract Java models up to 1.3GB, that conform to the Java metamodel  defined in MoDisco (refinement of the JDTAST metamodel).
We kindly invite you to follow this [link](http://help.eclipse.org/luna/index.jsp?topic=%2Forg.eclipse.modisco.java.doc%2Fmediawiki%2Fjava_discoverer_benchmark%2Fuser.html&resultof=%22modisco%22%20%22java%22%20) to get more familiar with MoDisco Java Discoverer(y).  

The discovered plugins are depicted in the table below.

Sets | Plugings												   
-----|---------------------------------------------------------
Set1 | org.eclipse.jdt.apt.pluggable.core
-----|---------------------------------------------------------
Set2 | Set1 + org.eclipse.jdt.apt.pluggable.core
-----|---------------------------------------------------------
Set3 | Set2 + org.eclipse.jdt.core+ org.eclipse.jdt.compiler +
	 |  org.eclipse.jdt.apt.core
-----|---------------------------------------------------------
Set4 | Set3 + org.eclipse.jdt.core.manipulation + 
	 | org.eclipse.jdt.launching + org.eclipse.jdt.ui + 
	 |  org.eclipse.jdt.debug
-----|---------------------------------------------------------
Set5 | org.eclipse.jdt.* (all jdt plugins)
-----|---------------------------------------------------------