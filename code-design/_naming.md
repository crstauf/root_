# Naming

Naming is equally fun and challenging, mostly art with a bit of intelligence. We've no absolute way of naming things, but always consider the objectives.

## Objectives

|Objective|Description|
|:--|:--|
|1. Readability|Easily readable code makes code more easily understood.|
|2. Navigability|Code that's easy to move through makes changes faster. `CTRL + ARROW`ing across "foo-bar-zulu" is three jumps, whereas "foo_bar_zulu" is one jump.|
|3. Consistency|Code that follows a consistent naming syntax is more easily read, understood, and navigated.|

## Hierarchy of Separators
*(from bottom to top)*

- camel case (`camelCase`)
- underscore (`_`)
- dash (`-`)
- double dashes (`--`) or double underscore (`__`)

## Notes

- use double dashes to separate groups; ex: `icon--arrow--left.svg`, `.btn--green`, `.btn--not-rounded`
- use double underscores to separate groups when dashes aren't permitted, like in function or class names; ex: `action__init()`, `class Calyx_HTTP_Facebook__Authentication {}`
- use a single dash when separating words within a group
- use a single underscore if you're already using dashes
- in some situations, camel case is more readable than lots of underscores

## Examples

- `icon--social-google_plus.svg`
- `icon--social-facebook.svg`
- `calyx_inlineScript_jqueryCore()`
- `.button--primary`
- `$counter__posts`