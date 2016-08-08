# API diff

[![Build Status](https://travis-ci.org/material-motion/material-motion-apidiff.svg?branch=develop)](https://travis-ci.org/material-motion/material-motion-apidiff)

An API diff tool for Objective-C, Swift, and Android code that outputs markdown.

## Usage

Run `apidiff` from within a git repository like so:

    apidiff v1.0.0 develop apple src/MaterialMotionRuntime.h
    apidiff 1.0.0 develop android library

## License

Licensed under the Apache 2.0 license. See LICENSE for details.

# Example output

Auto-generated by running:

    apidiff 734d43e406f53143c2cf8440f43d858d125f0a11 6f7a52744751e511d0daf119642446c46bed1f5c apple src/MaterialMotionRuntime.h

## NewClass

*new* class: `NewClass`

*new* constructor: `NewClass()`

*new* field: `text`

*new* method: `getText()`

## MDMPlanPerforming

*removed* method: `-addPlan:` in `MDMPlanPerforming`

*modified* protocol: `MDMPlanPerforming`

| Type | swift declaration |
|---|---|
| From | `protocol MDMPlanPerforming : MDMPerforming` |
| To | `protocol PlanPerforming : Performing` |

## MDMScheduler

*modified* property: `delegate` in `MDMScheduler`

| Type | swift declaration |
|---|---|
| From | `weak var delegate: MDMSchedulerDelegate? { get set }` |
| To | `weak var delegate: SchedulerDelegate? { get set }` |

*modified* class: `MDMScheduler`

| Type | swift declaration |
|---|---|
| From | `class MDMScheduler : NSObject` |
| To | `class Scheduler : NSObject` |
