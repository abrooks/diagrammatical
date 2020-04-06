# diagrammatical
A tool for automatically generating diagrams given semantic information.

This primarily intends to cover a range of software and computing specification diagrams.

## Overview

Assertion #1: Humans have a limited capacity to differentiate based on size, discrete position, color, numeracy, etc. Diagrams should be limited in the number of shapes, shape types, shape sizes, shape and line colors, etc.. (bounded by Golden Ratio steps?)

Assertion #2: Diagrams in specifications tend to convey the following _diagram attributes_:

* Importance: (typically via size, sometimes via position)
* Order (causality/dependence/sequence/flow/etc.): Typically shown by relative position (left-to-right, top-to-bottom, topleft-to-bottomright,etc.) and sometimes by arrows, connected with lines
* Boundary (containment/nesting/just-inside/crossing/just-outside/etc): Shown by postion of one shape inside or outside another
* Proximity (things that are closely associated / have natural physical position nearby): Shapes have some form of physical proximity
* Similarity grouping (not sure if this is a case of proximity... i.e. semantic proximity)

## Approach

An approach to layout is to start with a semantic graph (RDF, datoms, etc.) and apply analysis and heuristics to lay out diagrams. Relations and attributes in the semantic graph need to be mapped to one of the _diagram attributes_ above. Additional layout hints can be provided, though it is not intended that these hints would typically be about the resultant spatial layout, rather adding additional local semantics or logical groupings to assist laying out the diagram (often providing focus, or emphasis).

A diagram, once layed out, may serve as a reference diagram for other, more complicated diagrams which preserve the general layout of the first but augment it with additional information. In this way, a family of diagrams can share the same general layout and are more easily approached by readers.

It is expected that not all elements in the graph will be displayed but that some of the elements in the semantic graph will be invisible groupings or associations used in the layout.
