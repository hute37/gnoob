## Example Groovy Funktion

This example shows how easy it is to develop a [funktion](https://github.com/fabric8io/funktion/blob/master/README.md) in [Groovy](http://www.groovy-lang.org/).

<p align="center">
  <a href="http://fabric8.io/">
  	<img src="https://raw.githubusercontent.com/fabric8io/funktion/master/docs/images/icon.png" alt="funktion logo" width="200" height="200"/>
  </a>
</p>

The source code consists of:

* [funktion.yml](funktion.yml) to define the trigger URL (in this case HTTP)
* [main() function in groovy](src/main/groovy/io/fabric8/funktion/example/Main.groovy#L21-L23) to process incoming events

You can then run your funktion locally via:

```
mvn
```

You can then invoke it via your web browser at [http://localhost:8080/?name=Funktion](http://localhost:8080/?name=Funktion)

### Trying your funktion on Kubernetes or OpenShift

Assuming your current shell is connected to Kubernetes or OpenShift so that you can type a command like

```
kubectl get pods
````
or for OpenShift
```
oc get pods
```

Then the following command will package your funktion and run it on Kubernetes:
```
mvn install fabric8:deploy
```