# Edge Computing Query Model
*Query-Driven Descriptive Analytics for IoT and Edge Computing*

This repository contains the grammar of our Query model for Descriptive Analytics for IoT and Edge Computing. The parser has been developed using [ANTLR](https://www.antlr.org/) a tool for building language parsers in Java.

In the file *example.ins*, we provide some streaming analytic queries of actual interest from the domains of *IoT Transportation Analytics*, *Energy Consumption in Datacenters*, *Privacy-Aware Healthcare Analytics*, and *Microservices Auto-Scaling for Content Streaming*.

## How to run?
You can follow the steps below to download Antlr.
```bash
cd /usr/local/lib
sudo curl -O https://www.antlr.org/download/antlr-4.7.2-complete.jar
export CLASSPATH=".:/usr/local/lib/antlr-4.7.2-complete.jar:$CLASSPATH"
alias antlr4='java -jar /usr/local/lib/antlr-4.7.2-complete.jar'
alias grun='java org.antlr.v4.gui.TestRig'
```
You can run the provided examples to produce the AST (Abstract Syntax Tree) using the following command:
```bash
antlr4 InsightsAST.g4
javac InsightsAST*.java
grun Expr queries -gui < examples.ins
```
