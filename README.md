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

## File Structure

- **Shallow.hs**: Defines basic data types and operations for regions (e.g., circle, rectangle, union, etc.) and transformations (e.g., translation, scaling).
- **Deep.hs**: Implements advanced features using abstract syntax trees (ASTs) for regions and transformations. Introduces deep embeddings of regions and transformations for flexible interpretation.
- **Folds.hs**: Implements higher-level abstractions using folds for both regions and transformations. Provides combiners and transformations that allow for efficient manipulation and evaluation of geometric structures.

  ## Key Concepts

- **Regions**: A region is a 2D area represented as a function that checks whether a point is inside the region. Simple shapes like circles and rectangles are defined using such functions.

- **Transformations**: A transformation is applied to a point and changes its position (e.g., translation, scaling). Combinations of multiple transformations can be chained together.

- **Abstract Syntax Trees (ASTs)**: The use of ASTs in `Deep.hs` allows for a more flexible and efficient representation of regions and transformations. ASTs enable symbolic manipulation and optimization of complex geometric expressions.

- **Lazy Evaluation**: Thanks to Haskell's lazy evaluation, complex regions (like infinite unions of shapes) are not evaluated until necessary, allowing for efficient computation and memory usage.

## Functions & Data Types

### Region and Transformation Data Types

- **Region**: A type alias for a function `(Point -> Bool)` representing a 2D region.
- **Transformation**: A type alias for a function `(Point -> Point)` representing a transformation.

### Basic Operations

#### Shallow.hs:

- `circle :: Float -> Region`: Creates a circular region.
- `rectangle :: Float -> Float -> Region`: Creates a rectangular region.
- `translation :: Float -> Float -> Transformation`: Defines a translation transformation.
- `applyTransformation :: Transformation -> Region -> Region`: Applies a transformation to a region.

#### Deep.hs:

- `toRegion :: RegionAST -> Region`: Converts an abstract region representation to a concrete region.
- `toTransformation :: TransformationAST -> Transformation`: Converts an abstract transformation representation to a concrete transformation.

### Advanced Operations

#### Folds.hs:

- `foldRegionAST :: RegionCombiner a -> RegionAST -> a`: Folds over a region AST.
- `foldTransformationAST :: TransformationCombiner a -> TransformationAST -> a`: Folds over a transformation AST.
  
