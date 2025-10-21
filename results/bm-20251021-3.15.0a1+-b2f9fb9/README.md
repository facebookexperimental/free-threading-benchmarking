# Results

- fork: python/b2f9fb9db29296410f76
- version: 3.15.0a1+
- config: 
- commit hash: [b2f9fb9](https://github.com/python/cpython/commit/b2f9fb9)
- commit date: 2025-10-21T00:54:44+01:00
- commit merge base: [e09837fcbf39d07c0af51aa936e95c50aed4787c](https://github.com/python/cpython/commit/e09837fcbf39d07c0af51aa936e95c50aed4787c)
- ref: b2f9fb9db29296410f76

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18668828028)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251021-macm4pro-arm64-python-b2f9fb9db29296410f76-3.15.0a1%2B-b2f9fb9.json)

### vs. 3.12.6

- Geometric mean: 1.106x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251021-macm4pro-arm64-python-b2f9fb9db29296410f76-3.15.0a1%2B-b2f9fb9-vs-3.12.6.md)
- [📈time plot](bm-20251021-macm4pro-arm64-python-b2f9fb9db29296410f76-3.15.0a1%2B-b2f9fb9-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.026x faster (HPT: reliability of 97.77%, 1.00x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251021-macm4pro-arm64-python-b2f9fb9db29296410f76-3.15.0a1%2B-b2f9fb9-vs-3.13.0rc2.md)
- [📈time plot](bm-20251021-macm4pro-arm64-python-b2f9fb9db29296410f76-3.15.0a1%2B-b2f9fb9-vs-3.13.0rc2.svg)

