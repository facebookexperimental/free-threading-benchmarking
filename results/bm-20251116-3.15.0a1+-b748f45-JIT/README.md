# Results

- fork: Fidget-Spinner/llvm_19
- version: 3.15.0a1+
- config: JIT
- commit hash: [b748f45](https://github.com/Fidget%2dSpinner/cpython/commit/b748f45)
- commit date: 2025-11-16T19:52:35Z
- commit merge base: [be699d6c7c8793d3eb464f2e5d3f10262fe3bc37](https://github.com/python/cpython/commit/be699d6c7c8793d3eb464f2e5d3f10262fe3bc37)
- ref: llvm_19

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/19417090363)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251116-macm4pro-arm64-Fidget%252dSpinner-llvm_19-3.15.0a1%2B-b748f45.json)

### vs. 3.12.6

- Geometric mean: 1.138x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.25x
- missing benchmarks: chameleon, connected_components, djangocms, docutils, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251116-macm4pro-arm64-Fidget%252dSpinner-llvm_19-3.15.0a1%2B-b748f45-vs-3.12.6.md)
- [📈time plot](bm-20251116-macm4pro-arm64-Fidget%252dSpinner-llvm_19-3.15.0a1%2B-b748f45-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.048x faster (HPT: reliability of 99.69%, 1.01x faster at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: chameleon, connected_components, djangocms, docutils, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251116-macm4pro-arm64-Fidget%252dSpinner-llvm_19-3.15.0a1%2B-b748f45-vs-3.13.0rc2.md)
- [📈time plot](bm-20251116-macm4pro-arm64-Fidget%252dSpinner-llvm_19-3.15.0a1%2B-b748f45-vs-3.13.0rc2.svg)

