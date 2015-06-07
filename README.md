# onyx-starter

A starter project to get your feet wet with Onyx `0.6.0-RC1`. Uses the core.async plugin for both input and output. Requires no external dependencies.

## Walk Through

[WALKTHROUGH.md](WALKTHROUGH.md) walks through the repository in detail.

## Usage

##### Clone the repo

`git clone git@github.com:MichaelDrogalis/onyx-starter.git`

##### Run the sample job

Run the tests to see it work. Tail `onyx.log` for Onyx output.

```text
lein test
```

##### Expected output

```clojure
{:loud-output
 [{:word "HeY!"}
  {:word "ThErE!"}
  {:word "UsEr!"}
  {:word "It's!"}
  {:word "ReAlLy!"}
  {:word "NiCe!"}
  {:word "OuTsIdE!"}
  {:word "I!"}
  {:word "LiVe!"}
  {:word "In!"}
  {:word "ReDmOnD!"}
  :done]

 :question-output
 [{:word "HeY?"}
  {:word "ThErE?"}
  {:word "UsEr?"}
  {:word "It's?"}
  {:word "ReAlLy?"}
  {:word "NiCe?"}
  {:word "OuTsIdE?"}
  {:word "I?"}
  {:word "LiVe?"}
  {:word "In?"}
  {:word "ReDmOnD?"}
  :done]
```

##### Dashboard

If you would like to use the [Onyx
Dashboard](https://github.com/onyx-platform/onyx-dashboard) to inspect the
cluster, download the
[uberjar](https://github.com/onyx-platform/onyx-dashboard/#deployment).

In core.clj evaluate the sample file bit by bit, as above.

After evaluating the line: 
`(def env (onyx.api/start-env env-config))`
start the dashboard by:

`ZOOKEEPER_ADDR="127.0.0.1:2188" java -jar onyx-dashboard-VERSION-NUMBER.jar`

## License

Copyright © 2015 Michael Drogalis

Distributed under the Eclipse Public License either version 1.0 or (at
your option) any later version.
