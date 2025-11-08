# Results vs. base

- fork: Fidget-Spinner
- ref: tracing_jit
- machine: linux-x86_64
- commit hash: 7e2bc1d
- commit date: 2025-11-08
- overall geometric mean: 1.014x faster
- HPT reliability: 97.03%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20251101-vultr-x86_64-python-b1554146c29182803d1d-3.15.0a1+-b155414 | bm-20251108-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7e2bc1d |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 255 ms                                                                 | 250 ms: 1.02x faster                                                    |
| docutils       | 2.63 sec                                                               | 2.76 sec: 1.05x slower                                                  |
| html5lib       | 61.4 ms                                                                | 69.5 ms: 1.13x slower                                                   |
| sphinx         | 993 ms                                                                 | 1.02 sec: 1.02x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.05x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20251101-vultr-x86_64-python-b1554146c29182803d1d-3.15.0a1+-b155414 | bm-20251108-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7e2bc1d |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_generators           | 364 ms                                                                 | 359 ms: 1.01x faster                                                    |
| coroutines                 | 24.3 ms                                                                | 24.4 ms: 1.00x slower                                                   |
| async_tree_io_tg           | 594 ms                                                                 | 602 ms: 1.01x slower                                                    |
| async_tree_cpu_io_mixed    | 484 ms                                                                 | 491 ms: 1.01x slower                                                    |
| async_tree_memoization_tg  | 306 ms                                                                 | 312 ms: 1.02x slower                                                    |
| async_tree_none_tg         | 243 ms                                                                 | 248 ms: 1.02x slower                                                    |
| async_tree_cpu_io_mixed_tg | 486 ms                                                                 | 497 ms: 1.02x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                            |

Benchmark hidden because not significant (4): async_tree_none, asyncio_websockets, async_tree_io, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20251101-vultr-x86_64-python-b1554146c29182803d1d-3.15.0a1+-b155414 | bm-20251108-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7e2bc1d |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 70.6 ms                                                                | 60.7 ms: 1.16x faster                                                   |
| nbody          | 84.6 ms                                                                | 83.3 ms: 1.02x faster                                                   |
| pidigits       | 209 ms                                                                 | 210 ms: 1.00x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.06x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20251101-vultr-x86_64-python-b1554146c29182803d1d-3.15.0a1+-b155414 | bm-20251108-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7e2bc1d |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 22.6 ms                                                                | 21.4 ms: 1.05x faster                                                   |
| regex_compile  | 126 ms                                                                 | 124 ms: 1.01x faster                                                    |
| regex_dna      | 175 ms                                                                 | 180 ms: 1.03x slower                                                    |
| regex_effbot   | 2.59 ms                                                                | 2.73 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20251101-vultr-x86_64-python-b1554146c29182803d1d-3.15.0a1+-b155414 | bm-20251108-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7e2bc1d |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pickle_pure_python   | 307 us                                                                 | 297 us: 1.03x faster                                                    |
| xml_etree_iterparse  | 85.4 ms                                                                | 82.7 ms: 1.03x faster                                                   |
| json_dumps           | 9.31 ms                                                                | 9.14 ms: 1.02x faster                                                   |
| xml_etree_parse      | 129 ms                                                                 | 128 ms: 1.01x faster                                                    |
| unpickle_pure_python | 184 us                                                                 | 182 us: 1.01x faster                                                    |
| json_loads           | 27.9 us                                                                | 28.2 us: 1.01x slower                                                   |
| xml_etree_generate   | 77.0 ms                                                                | 77.9 ms: 1.01x slower                                                   |
| xml_etree_process    | 53.7 ms                                                                | 54.4 ms: 1.01x slower                                                   |
| tomli_loads          | 1.75 sec                                                               | 1.85 sec: 1.06x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20251101-vultr-x86_64-python-b1554146c29182803d1d-3.15.0a1+-b155414 | bm-20251108-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7e2bc1d |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 12.4 ms                                                                | 12.5 ms: 1.01x slower                                                   |
| python_startup_no_site | 7.24 ms                                                                | 7.28 ms: 1.01x slower                                                   |
| Geometric mean         | (ref)                                                                  | 1.01x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20251101-vultr-x86_64-python-b1554146c29182803d1d-3.15.0a1+-b155414 | bm-20251108-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7e2bc1d |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako           | 10.7 ms                                                                | 10.8 ms: 1.01x slower                                                   |
| genshi_text    | 20.5 ms                                                                | 21.2 ms: 1.04x slower                                                   |
| genshi_xml     | 49.3 ms                                                                | 53.6 ms: 1.09x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                            |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20251101-vultr-x86_64-python-b1554146c29182803d1d-3.15.0a1+-b155414 | bm-20251108-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7e2bc1d |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| richards                   | 42.2 ms                                                                | 20.9 ms: 2.02x faster                                                   |
| richards_super             | 48.4 ms                                                                | 25.2 ms: 1.92x faster                                                   |
| float                      | 70.6 ms                                                                | 60.7 ms: 1.16x faster                                                   |
| spectral_norm              | 96.7 ms                                                                | 83.3 ms: 1.16x faster                                                   |
| logging_silent             | 99.6 ns                                                                | 87.2 ns: 1.14x faster                                                   |
| deltablue                  | 3.15 ms                                                                | 2.79 ms: 1.13x faster                                                   |
| scimark_monte_carlo        | 62.0 ms                                                                | 55.2 ms: 1.12x faster                                                   |
| scimark_sor                | 108 ms                                                                 | 98.2 ms: 1.10x faster                                                   |
| scimark_lu                 | 110 ms                                                                 | 102 ms: 1.07x faster                                                    |
| chaos                      | 57.1 ms                                                                | 53.4 ms: 1.07x faster                                                   |
| pyflate                    | 401 ms                                                                 | 377 ms: 1.06x faster                                                    |
| regex_v8                   | 22.6 ms                                                                | 21.4 ms: 1.05x faster                                                   |
| deepcopy_memo              | 26.6 us                                                                | 25.2 us: 1.05x faster                                                   |
| go                         | 107 ms                                                                 | 102 ms: 1.04x faster                                                    |
| pprint_pformat             | 1.44 sec                                                               | 1.38 sec: 1.04x faster                                                  |
| pickle_pure_python         | 307 us                                                                 | 297 us: 1.03x faster                                                    |
| xml_etree_iterparse        | 85.4 ms                                                                | 82.7 ms: 1.03x faster                                                   |
| thrift                     | 764 us                                                                 | 745 us: 1.03x faster                                                    |
| meteor_contest             | 99.8 ms                                                                | 97.5 ms: 1.02x faster                                                   |
| crypto_pyaes               | 67.8 ms                                                                | 66.3 ms: 1.02x faster                                                   |
| 2to3                       | 255 ms                                                                 | 250 ms: 1.02x faster                                                    |
| json_dumps                 | 9.31 ms                                                                | 9.14 ms: 1.02x faster                                                   |
| coverage                   | 82.3 ms                                                                | 81.0 ms: 1.02x faster                                                   |
| nbody                      | 84.6 ms                                                                | 83.3 ms: 1.02x faster                                                   |
| scimark_sparse_mat_mult    | 4.21 ms                                                                | 4.15 ms: 1.02x faster                                                   |
| regex_compile              | 126 ms                                                                 | 124 ms: 1.01x faster                                                    |
| gc_traversal               | 4.40 ms                                                                | 4.34 ms: 1.01x faster                                                   |
| async_generators           | 364 ms                                                                 | 359 ms: 1.01x faster                                                    |
| xml_etree_parse            | 129 ms                                                                 | 128 ms: 1.01x faster                                                    |
| unpickle_pure_python       | 184 us                                                                 | 182 us: 1.01x faster                                                    |
| bench_mp_pool              | 12.6 ms                                                                | 12.5 ms: 1.01x faster                                                   |
| comprehensions             | 16.1 us                                                                | 16.0 us: 1.01x faster                                                   |
| coroutines                 | 24.3 ms                                                                | 24.4 ms: 1.00x slower                                                   |
| pidigits                   | 209 ms                                                                 | 210 ms: 1.00x slower                                                    |
| bpe_tokeniser              | 3.96 sec                                                               | 3.98 sec: 1.00x slower                                                  |
| python_startup             | 12.4 ms                                                                | 12.5 ms: 1.01x slower                                                   |
| python_startup_no_site     | 7.24 ms                                                                | 7.28 ms: 1.01x slower                                                   |
| mako                       | 10.7 ms                                                                | 10.8 ms: 1.01x slower                                                   |
| sqlglot_v2_parse           | 1.21 ms                                                                | 1.22 ms: 1.01x slower                                                   |
| hexiom                     | 5.97 ms                                                                | 6.03 ms: 1.01x slower                                                   |
| scimark_fft                | 257 ms                                                                 | 260 ms: 1.01x slower                                                    |
| fannkuch                   | 363 ms                                                                 | 367 ms: 1.01x slower                                                    |
| json_loads                 | 27.9 us                                                                | 28.2 us: 1.01x slower                                                   |
| xml_etree_generate         | 77.0 ms                                                                | 77.9 ms: 1.01x slower                                                   |
| xml_etree_process          | 53.7 ms                                                                | 54.4 ms: 1.01x slower                                                   |
| pathlib                    | 17.5 ms                                                                | 17.8 ms: 1.01x slower                                                   |
| create_gc_cycles           | 1.94 ms                                                                | 1.97 ms: 1.01x slower                                                   |
| async_tree_io_tg           | 594 ms                                                                 | 602 ms: 1.01x slower                                                    |
| async_tree_cpu_io_mixed    | 484 ms                                                                 | 491 ms: 1.01x slower                                                    |
| sqlglot_v2_transpile       | 1.51 ms                                                                | 1.53 ms: 1.02x slower                                                   |
| subparsers                 | 45.0 ms                                                                | 45.7 ms: 1.02x slower                                                   |
| deepcopy                   | 245 us                                                                 | 249 us: 1.02x slower                                                    |
| telco                      | 159 ms                                                                 | 162 ms: 1.02x slower                                                    |
| generators                 | 27.5 ms                                                                | 28.0 ms: 1.02x slower                                                   |
| async_tree_memoization_tg  | 306 ms                                                                 | 312 ms: 1.02x slower                                                    |
| async_tree_none_tg         | 243 ms                                                                 | 248 ms: 1.02x slower                                                    |
| async_tree_cpu_io_mixed_tg | 486 ms                                                                 | 497 ms: 1.02x slower                                                    |
| sphinx                     | 993 ms                                                                 | 1.02 sec: 1.02x slower                                                  |
| logging_simple             | 5.77 us                                                                | 5.92 us: 1.03x slower                                                   |
| regex_dna                  | 175 ms                                                                 | 180 ms: 1.03x slower                                                    |
| genshi_text                | 20.5 ms                                                                | 21.2 ms: 1.04x slower                                                   |
| sympy_expand               | 487 ms                                                                 | 506 ms: 1.04x slower                                                    |
| many_optionals             | 1.23 ms                                                                | 1.28 ms: 1.04x slower                                                   |
| sympy_integrate            | 19.4 ms                                                                | 20.2 ms: 1.04x slower                                                   |
| sqlglot_v2_optimize        | 51.4 ms                                                                | 53.7 ms: 1.05x slower                                                   |
| nqueens                    | 81.5 ms                                                                | 85.4 ms: 1.05x slower                                                   |
| docutils                   | 2.63 sec                                                               | 2.76 sec: 1.05x slower                                                  |
| regex_effbot               | 2.59 ms                                                                | 2.73 ms: 1.05x slower                                                   |
| raytrace                   | 251 ms                                                                 | 265 ms: 1.05x slower                                                    |
| sqlglot_v2_normalize       | 103 ms                                                                 | 108 ms: 1.06x slower                                                    |
| tomli_loads                | 1.75 sec                                                               | 1.85 sec: 1.06x slower                                                  |
| pylint                     | 293 ms                                                                 | 312 ms: 1.06x slower                                                    |
| sympy_sum                  | 158 ms                                                                 | 169 ms: 1.07x slower                                                    |
| dulwich_log                | 69.7 ms                                                                | 74.7 ms: 1.07x slower                                                   |
| sympy_str                  | 282 ms                                                                 | 306 ms: 1.08x slower                                                    |
| genshi_xml                 | 49.3 ms                                                                | 53.6 ms: 1.09x slower                                                   |
| html5lib                   | 61.4 ms                                                                | 69.5 ms: 1.13x slower                                                   |
| mdp                        | 1.16 sec                                                               | 1.33 sec: 1.14x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                            |

Benchmark hidden because not significant (16): async_tree_none, deepcopy_reduce, django_template, shortest_path, connected_components, logging_format, sqlite_synth, pprint_safe_repr, pycparser, json, asyncio_websockets, k_core, bench_thread_pool, typing_runtime_protocols, async_tree_io, async_tree_memoization

- Geometric mean (including insignificant results): 1.014x faster

# HPT report

- Reliability score: 97.03% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.01x