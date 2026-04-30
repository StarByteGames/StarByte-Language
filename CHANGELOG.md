# Change Log

All notable changes to the "starbyte-language" extension will be documented in this file.

Check [Keep a Changelog](http://keepachangelog.com/) for recommendations on how to structure this file.

## [0.1.1] - 2026-04-30

### Changed
- Lowered minimum required VS Code version from `^1.118.0` to `^1.60.0`
  for broader compatibility with older VS Code installations.

## [0.1.0] - 2026-04-30

### Added
- Full TextMate grammar for StarByte covering control-flow, declaration,
  memory, and exception keywords; built-in primitive types; constants;
  preprocessor directives; string and character literals with escape
  sequences; integer, float, hex and binary numeric literals; and the
  full operator set (arithmetic, comparison, logical, bitwise,
  assignment / compound, increment, ternary).
- Distinct highlighting for function definitions vs. function calls,
  and PascalCase identifiers as type/class names.
- Language configuration: bracket pairs, auto-closing pairs (with
  `notIn` rules for strings/comments), surrounding pairs,
  indentation rules, word pattern, and `// #region` folding markers.
- Sample showcase file at `examples/test.sb`.
- Real README with feature list and install/build instructions.

## [Unreleased]