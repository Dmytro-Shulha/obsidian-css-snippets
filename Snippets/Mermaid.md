# Mermaid
```
​```mermaid
graph TD;

%% Class Definitions
%% =================

classDef FixFont font-size:11.5px;

%% Nodes
%% =====

A[CREATIVITY]:::FixFont --> B[Combinatorial]:::FixFont;
A[CREATIVITY]:::FixFont --> C[Exploratory]:::FixFont;
A[CREATIVITY]:::FixFont --> D[Transformational]:::FixFont;
B[Combinatorial] --> E[Problem-driven]:::FixFont;
B[Combinatorial] --> F[Similarity-driven]:::FixFont;
B[Combinatorial] --> G[Inspiration-driven]:::FixFont;

%% Node styles
%% ===========

style A fill:gold;  
style B fill:cyan;
style C fill:cyan;
style D fill:cyan;
style E fill:mediumvioletred;
style F fill:mediumvioletred;
style G fill:mediumvioletred;

​```
```

