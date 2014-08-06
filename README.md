# gaffer

[Foreman](https://github.com/ddollar/foreman) on JVM. It manages Procfile-based applications.

## Installation

##### Precompiled Packages

Download the [latest release](https://github.com/jingweno/gaffer/releases) and unzip it.

##### Compile from Source

```sh
$ mvn package
$ unzip target/gaffer-0.0.1-SNAPSHOT-dist.zip -d target
$ ./target/gaffer-0.0.1-SNAPSHOT-dist/bin/gaffer help
```

## Usage

```sh
$ gaffer start
$ gaffer start web
$ gaffer start -f Procfile.test -c worker=2
$ gaffer run java -jar target/hello-world-0.0.1-SNAPSHOT.jar server
```

## Implementation

`gaffer` takes advantage of [akka](http://akka.io/)'s [actors](http://en.wikipedia.org/wiki/Actor_model) to [supervise](http://doc.akka.io/docs/akka/snapshot/general/supervision.html) child-processes. More details to come as a blog post.

## License

See [License.md](https://github.com/jingweno/gaffer/blob/master/LICENSE.md).