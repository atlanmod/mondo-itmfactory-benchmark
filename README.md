# ITM Factory Benchmark

This benchmark contains two transformations and a set of queries, each addressing a different phase in a model-driven reverse engineering process. 
The use case for this benchmark is taken from the Eclipse MoDisco project.

Thanks to the [MoDisco](https://eclipse.org/MoDisco/) Java discoverer, we are able to extract Java models up to 1.3GB, that conform to the Java metamodel  defined in MoDisco (refinement of the JDTAST metamodel).
We kindly invite you to follow this [link](http://help.eclipse.org/luna/index.jsp?topic=%2Forg.eclipse.modisco.java.doc%2Fmediawiki%2Fjava_discoverer_benchmark%2Fuser.html&resultof=%22modisco%22%20%22java%22%20) to get more familiar with MoDisco Java Discoverer(y).  

The discovered plugins are depicted in the table below.

Sets | Plugings
-----|---------------------------------------------------------
Set1 | org.eclipse.jdt.apt.pluggable.core
Set2 | Set1 + org.eclipse.jdt.apt.pluggable.core
Set3 | Set2 + org.eclipse.jdt.core+ org.eclipse.jdt.compiler + org.eclipse.jdt.apt.core
Set4 | Set3 + org.eclipse.jdt.core.manipulation + org.eclipse.jdt.launching + org.eclipse.jdt.ui + org.eclipse.jdt.debug
Set5 | org.eclipse.jdt.* (all jdt plugins)

## Use cases description

### Transformations

#### Java2KDM
This transformation takes place at beginning of almost every modernization process of a Java legacy system, it comes just after the discovery of the Java model from Java projects (plugins) using the MoDisco Java Discoverer. 
This transformation generates a KDM (Knowledge Discovery Metamodel) model that defines common metadata required for deep semantic integration of application life-cycle management tools.
Based on the previously generated model, this transformation generates a UML diagram in order to allow integrating KDM-compliant tools (i. e., discoverers) with UML-compliant
tools (e.g. modelers, model transformation tools, code generators,
etc.).
#### KDM2UML
Based on the previously generated model, this transformation generates a UML diagram in order to allow integrating KDM-compliant tools (i. e., discoverers) with UML-compliant
tools (e.g. modelers, model transformation tools, code generators,etc.).

The transformations can be launched from the ant files contained in the **build** folder.

### Queries
#### Java code quality

This set of code quality transformations
identify well-known anti-patterns in Java source code and fix the
corresponding issues by a model transformation. The input format
of the transformations is a model conforming to the Java metamodel. For a specification for the transformations we refer the
reader to the implementations of these fixes in well-known codeanalysis tools like CheckStyle and PMD.
References to the documentation for each code fix considered in this benchmark can be found [here](http://checkstyle.sourceforge.net/availablechecks.html).



