The purpose of this library is to make it easy for Java programs to host Clojure by using the Java Scripting API. The Clojure Scripting Engine provides a concrete implementation of the API as a lightweight layer that wraps the **Clojure Runtime**. It is available as a service provider through the class `ScriptEngineManager`.

The engine offers all the functionality from the `ScriptEngineFactory` and `ScriptEngine` interfaces. Instances of `ScriptEngine` also implement `Invocable` and `Compilable`. Client code may run Clojure code; define bindings to Java objects; obtain Clojure implementations of Java interfaces; invoke Clojure functions; and compile Clojure libraries to .class files.

The distribution ZIP file contains the following:
  * The library in binary form in file clojure-jsr223.jar
  * Clojure-specific javadoc files for the API
  * The source code
  * Sample host programs


---

To use the Clojure Scripting Engine, place the file **clojure-jsr223.jar** in the same location where you keep files clojure.jar and clojure-contrib.jar, and add it to your classpath. Then you may get an instance of the engine this way:

```
ScriptEngineManager factory = new ScriptEngineManager();
ScriptEngine engine = factory.getEngineByName("Clojure");
```

---

02/01/11 - The new zip version 1.2 has a fix for getting bindings
declared in Clojure code (vars) from any namespace.
NOTE: Bindings will come now as namespace/var, like user/foo, myns/bar

Putting bindings to the engine works the same, but now you have
the option of using the format namespace/var.

---

Thanks again to Matthias for putting this version out in Clojars:
```
<dependency>
    <groupId>clojure-jsr223</groupId>
    <artifactId>clojure-jsr223</artifactId>
    <version>1.0</version>
  </dependency>
```

---

See the javadoc for details on how to use the API for Clojure code.

For suggestions and bug reports please use the Issues tab.
For discussion, go to the [Clojure group](http://groups.google.com/group/clojure).