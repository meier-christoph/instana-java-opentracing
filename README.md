# Instana Java OpenTracing&nbsp; [![Build Status](https://travis-ci.org/instana/instana-java-opentracing.svg?branch=master)](https://travis-ci.org/instana/instana-java-opentracing)

Instana is capable of collecting traces that are described via the [OpenTracing](http://opentracing.io) API. In order to collect such traces, this tracer implementation must be used.

The artifact is available on Maven Central. When using Maven you can include the tracer with:

```
<dependency>
  <groupId>com.instana</groupId>
  <artifactId>instana-java-opentracing</artifactId>
  <version>0.20.2</version>
</dependency>
```

The implementation's version number follows the [OpenTracing API version](https://github.com/opentracing/opentracing-java) that it implements.


The tracer is fully compliant with the OpenTracing API and is available via:

```java
io.opentracing.Tracer tracer = InstanaTracerFactory.create();
```
The Instana tracer supports context propagation using all of OpenTracing's built-in formats, i.e. `TextMap`, HTTP headers and `ByteBuffer`.

When the Instana monitoring agent is not attached, the Instana OpenTracing API will act as an inactive tracer, similarly to the [OpenTracing noop-tracer](https://github.com/opentracing/opentracing-java/tree/master/opentracing-noop).