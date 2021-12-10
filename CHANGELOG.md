# Changelog

## [Next]
- Add `pbip/dev-linter` to help find errors in operation definitions
- Add `pcr/estimate-cost-sort` to pick path based on estimate cost

## [2021.11.16-alpha]
- Add extension point `::p.error/wrap-attribute-error`
- Fix batch calls with distinct parameters
- Add `pco/final-value` helper to mark a value as final

## [2021.10.20-alpha]
- Add optimizations to OR branches that are sub-paths of each other
- Support new `::pco/cache-key` setting for custom cache keys at resolver level

## [2021.10.19-alpha]
- Fix foreign mutation on async runner
- Remove viz request snapshots to allow multiple connectors on the same meshed graph
- Fix the flow of params on foreign-ast
- Fix nested dependency process
- Infer output shape in constantly resolver
- Parallel processor 🎉

## [2021.08.14-alpha]
- Fix cache store specs
- Add `::pcr/wrap-process-sequence-item` plugin entry point
- Add `filtered-sequence-items-plugin` new built-in plugin
- Batch support for dynamic resolvers
- Batch support on foreign requests
- BREAKING CHANGE: Dynamic resolvers always get rich inputs with input data and foreign ast
- Dynamic mutations also go as input parts with params 

## [2021.07.30-alpha]
- Fix lenient mode optional inputs, it was marking errors when it shouldn't

## [2021.07.27-alpha]
- Support disable input destructuring validation on `pco/resolver` with the flag `::pco/disable-validate-input-destructuring?`
- Run `::pco/transform` before running the resolver validations
- Fixed bug when combining batch + disabled cache + missing outputs doing infinite loops

## [2021.07.23-alpha]
- Add `p.eql/process-one` and `p.a.eql/process-one` helpers

## [2021.07.19-alpha]
- BREAKING CHANGE: Strict mode by default, now errors surface quickly
- BREAKING CHANGE: Remove `remove-stats-plugin`, now must use the env flag `:com.wsscode.pathom3.connect.runner/omit-run-stats?` instead
- Optional lenient mode via setting `:com.wsscode.pathom3.error/lenient-mode? true` on env
- Boundary interface now accepts `:pathom/lenient-mode?` so the client can configure it
- `attribute-errors-plugin` is deprecated, when using lenient mode that behavior comes automatically
- Fix async runner reversing lists
- Add `ctry` helper to handle exceptions in sync and async at same time
- Foreign connection errors get wrapped to enrich the error context
- Add spec for `::pci/index-source-id`
- Detect cycles in nested inputs to prevent stack overflow at planner
- Support foreign unions
- Entities can decide union path via `::pf.eql/union-entry-key`

## [2021.07.10-1-alpha]
- Add more info to pom.xml to add repository links from clojars and cljdoc

## [2021.07.10-alpha]
- Add transit dependencies to fix cljdoc compilation

## [2021.07.9-alpha]
- Initial JAR release
