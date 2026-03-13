# Results

- fork: Fidget-Spinner/resume_tracing
- version: 3.15.0a7+
- config: JIT
- commit hash: [af09d44](https://github.com/Fidget%2dSpinner/cpython/commit/af09d44)
- commit date: 2026-03-13T18:18:57+08:00
- commit merge base: [0adc7289c3ab097b5608c0d288d91e1f5f236469](https://github.com/python/cpython/commit/0adc7289c3ab097b5608c0d288d91e1f5f236469)
- ref: resume_tracing

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/23045034349)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260313-macm4pro-arm64-Fidget%252dSpinner-resume_tracing-3.15.0a7%2B-af09d44.json)

### vs. 3.12.6

- Geometric mean: 1.287x faster (HPT: reliability of 100.00%, 1.15x faster at 99th %ile)
- Memory usage: 1.28x
- missing benchmarks: chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260313-macm4pro-arm64-Fidget%252dSpinner-resume_tracing-3.15.0a7%2B-af09d44-vs-3.12.6.md)
- [📈time plot](bm-20260313-macm4pro-arm64-Fidget%252dSpinner-resume_tracing-3.15.0a7%2B-af09d44-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.193x faster (HPT: reliability of 100.00%, 1.08x faster at 99th %ile)
- Memory usage: 1.23x
- missing benchmarks: chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260313-macm4pro-arm64-Fidget%252dSpinner-resume_tracing-3.15.0a7%2B-af09d44-vs-3.13.0rc2.md)
- [📈time plot](bm-20260313-macm4pro-arm64-Fidget%252dSpinner-resume_tracing-3.15.0a7%2B-af09d44-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.037x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20260313-macm4pro-arm64-Fidget%252dSpinner-resume_tracing-3.15.0a7%2B-af09d44-vs-base-mem.svg)
- [📄table](bm-20260313-macm4pro-arm64-Fidget%252dSpinner-resume_tracing-3.15.0a7%2B-af09d44-vs-base.md)
- [📈time plot](bm-20260313-macm4pro-arm64-Fidget%252dSpinner-resume_tracing-3.15.0a7%2B-af09d44-vs-base.svg)

