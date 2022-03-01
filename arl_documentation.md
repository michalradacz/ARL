# About this documentation

## Document header

## Publication status

## Version history

| Date | Version | Revision comments |
|-----|----|-------------|
| 2020-01-06 | 1.0 | First draft revision |

# ARL language

Architectural readable language

## What is ARL?

Let me present the **Architecture readable language**

Language for presenting architecture as readable text in understable form, especially for non-architect users.

This special form of presenting architectural models and knowledges is domaining specific language for users who must work with content of architecture in regulatory and guidelines texts and don\'t want to present architectonic knowledges in graphical form of many diagrams. Wanted output is readable text in easy and self-descriptive sentences and text blocks. ARL isn\'t a language itself, it is set of rules for transforming models to a textual information. It depends on model elements and relationships and their descriptions and some basic attributes or properties. That simple idea.

## Background

ARL originated from two special purposes:

1. Readable architectural knowledges for non-architect people without using and verbally describing number of complex diagrams.
2. Way to create and use and understand architecture for blind people, who aren\'t able to work with primarly visual information represented in diagrams.

ARL gives way to say what architecture wants to say but in readable and constructive text for accessible for everyone, even for non-architects.

Main author of ARL is Michal Rada, blind architect from Czech republic. He is totally blind, so he isnt able to understand complex visual information, for example complex diagrams. He is able to create complex architectural models using some special concepts and he transforms architectural knowledges and models contents to readable text for himself and his blind colleagues, but for sighted users too.

ARL originates from Michal Rada´s need to easilly create and say architectural knowledges for people who writes regulatory and guidelines documents and another users, because he wonts to draw diagrams as an architectural output.

## ARL idea

Main idea of ARL is transforming any relationships between elements in simple sentences with some additional context if needed. Absolutelly basically, main sentence must say: WHO DOES WHAT and WITH or WHEN. It expands original concept of Archimate and another languages as content for \"saying\" something and uses some principles to do it easily and understable for non-architects.

So, output from ARL transformation of model is set of descriptions of elements and as main output set of sentences from each rellevant relationship.

## And, What is NOT ARL?

ARL isnt language for constructions of elements and models. It is language for presenting architecture contents.

But with some extensible rules it can be used as source for creating parts of architecture. In three-collumn form you can declare anything. And with some basic logic you can create simple set of elements and relationship. Main problem is that you must define element´s types and relationship´s types. At this time, ARL does not contain standard concept for defining types for creation, but you can define three-collumns relationships and after it you can enter elements with their properties and relationships between elements with their properties. But, it is not so easy as modelling in visual tool.

# Glossar

There is some terms using in ARL terminology and meanings:

Element
:   Architectural concept represented by one element in model or hierarchy.

Relationship
:   One relationship between two elements represented as relationship in model.

Primary mean
:   Declaration of main mean represented by relationship

Alternate mean
:   Alternate interpretation of relationship that is important for context in describing architecture.

Statement
:   One sentence generated from one relationship.

Statement description
:   Description text from relationship´s description or documentation added as text to statement.

Set of statements
:   Logical grouping of statements. For example statements declared from relationships from one diagram.

Statement rules
:   Set of transformation rules for construct relationship as an statement. For example construct direction (STT or TTS as ARLDirection)

Output
:   Readable text or document created using composition of statements with statements description in individual context.

# Main concepts of ARL

## Concepts philosophy

ARL is universal transformation language. It can be extend of ANY language using structural elements and relationships between it. Primary purpose is using ARL to transform architectural models to readable text output, but it can be used for UML like languages and ERM languages too.

## Statements

Statement is main important concept. Statement represents relationship as sentence with readable and understable content.

## Rules

## Example construction

Simplest example is generating Statements as sentences from relationships. Each relationship is one sentence. There are WHO and WHAT as elements declared as classical concept element in Archimate and DOES as description of relationship.

| Concept            | Meaning       | Description |
|----------|----------|----------|
|  Source element     | WHO    |        Who or What is doing something represented by this relationship |
|  Relationship type |  rule        |   Rule as relationship type says what meaning the relationship represents for a readable text |
|  Relationship name |  DOES         |  Describes naturally what is a primary activity represented by this relationship. |
|  Target element    |  WHAT or WHEN |  Says that described activity is routed to this object. Represents object with secnondary mean in this relationship. |

Example:

Origin: Element John is BusinessActor with role System user. There is element App with type ApplicationComponent. And you must say, that John is user of this app.

You may do this two ways in Archimate. In both cases John is Actor and System user is Role. John assignes this role. And now:

1. You can relate System user to the App - System user is a source, relationship is an Access type and description is \"uses\" and target is App. (It says that user uses app)
2. You can relate App to the System user - App is a source element and relationship is a Serving type with description \"used by\" and System user is a target. (It says that app is used by user)

Strictly, in Archimate language, second form of relationship is right way to declare that user uses app.

Result in ARL:

1. John is System user. System user uses App.
2. John is System user. App is used by System user.

But using ARL transformation using TTS direction you can say that user uses app without need to change model content.

# ARL practically

## Basic ARL definition rules

- Statement construct: Rule for creating one Statement from one relationship or more complex sentence from rellevant more relationships as described bellow:
     -   Simple sentence: Sentence is created from ONE relationship using rule \"WWHO DOES WHAT\". Rule is \"Source element DOES (relationship description) WTarget element\".
  - Complex sentence: Sentence is created composing one sentence from MANY same type relationships. If there are one Source element and three relationships with same type and another targets, we can use rule: \"WHO DOES WHAT, WHAT and WHAT.\" Rule is: \"Source element DOES (relationship description) Target1 and Target2 and Target3,\"
- ARLDirection: Says way to construct readable sentence from relationship. Possible attributes are STT or TTS.
  - STT: Source to target. Sentence is constructed by rule \"source does target\". This is default direction.
  - TTS: Target to source. Sentence is constructed as \"Target does source\". This is useful when you want naturally say a relationship in another direction. Statement dependency: In some cases, there are some special dependencies between statements. For example \"User is Role\" and \"Role uses App\" has same dependency as \"User is Role\" and \"Role writes Data\". Concept of modal and unmodal dependencies isnt universal and may be different for each source language.
