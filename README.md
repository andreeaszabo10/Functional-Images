Copyright Szabo Cristina-Andreea
# Functional Images

## Overview

This project is a Haskell-based program for working with functional representations of 2D geometric regions and transformations. This project utilizes functional programming techniques to create and manipulate shapes, such as circles, rectangles, and complex regions derived from combinations of basic shapes. Transformations like translation and scaling are also supported, and the project provides an infrastructure for applying and optimizing these transformations efficiently.

The main focus of the project is to demonstrate how functional programming can be applied to the construction and manipulation of geometric shapes using abstract syntax trees (ASTs) and higher-order functions.

## Features

- **Region Representations**: Define and manipulate 2D regions such as circles, rectangles, and unions or intersections of these regions.
- **Transformations**: Apply transformations like translation and scaling to regions, and combine multiple transformations into complex transformations.
- **Optimization**: Simplify transformation chains and optimize AST representations to reduce redundant operations.
- **Lazy Evaluation**: Take advantage of Haskell's lazy evaluation to efficiently check point membership in complex regions without evaluating the entire region upfront.
- **Recursive Folding**: Use folding techniques to reduce complex data structures into simpler results, such as counting the number of basic shapes or transformations in a given region.
