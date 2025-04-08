# Results vs. base

- fork: mpage
- ref: experiment_noinline
- machine: linux-x86_64
- commit hash: 521fae6
- commit date: 2025-04-07
- overall geometric mean: 1.003x slower
- HPT reliability: 93.01%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 268 ms                                                                 | 271 ms: 1.01x slower                                                 |
| docutils       | 2.63 sec                                                               | 2.62 sec: 1.01x faster                                               |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                         |

Benchmark hidden because not significant (2): html5lib, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|-------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| coroutines              | 20.0 ms                                                                | 19.7 ms: 1.02x faster                                                |
| async_tree_cpu_io_mixed | 456 ms                                                                 | 454 ms: 1.01x faster                                                 |
| async_tree_io_tg        | 476 ms                                                                 | 481 ms: 1.01x slower                                                 |
| Geometric mean          | (ref)                                                                  | 1.00x slower                                                         |

Benchmark hidden because not significant (8): async_tree_cpu_io_mixed_tg, asyncio_websockets, async_generators, async_tree_none, async_tree_memoization_tg, async_tree_io, async_tree_memoization, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| nbody          | 110 ms                                                                 | 108 ms: 1.01x faster                                                 |
| float          | 64.2 ms                                                                | 63.8 ms: 1.01x faster                                                |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                         |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_dna      | 188 ms                                                                 | 179 ms: 1.05x faster                                                 |
| regex_effbot   | 3.03 ms                                                                | 2.96 ms: 1.02x faster                                                |
| regex_compile  | 134 ms                                                                 | 133 ms: 1.01x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                         |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| xml_etree_generate   | 85.4 ms                                                                | 83.5 ms: 1.02x faster                                                |
| xml_etree_process    | 60.4 ms                                                                | 59.6 ms: 1.01x faster                                                |
| xml_etree_parse      | 142 ms                                                                 | 141 ms: 1.01x faster                                                 |
| json_dumps           | 12.7 ms                                                                | 12.7 ms: 1.00x faster                                                |
| tomli_loads          | 1.94 sec                                                               | 1.97 sec: 1.02x slower                                               |
| unpickle_pure_python | 218 us                                                                 | 222 us: 1.02x slower                                                 |
| json_loads           | 28.8 us                                                                | 29.5 us: 1.02x slower                                                |
| pickle_pure_python   | 308 us                                                                 | 317 us: 1.03x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.00x slower                                                         |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup | 15.6 ms                                                                | 15.5 ms: 1.01x faster                                                |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                         |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 50.5 ms                                                                | 51.2 ms: 1.02x slower                                                |
| mako            | 14.1 ms                                                                | 14.4 ms: 1.02x slower                                                |
| genshi_text     | 23.0 ms                                                                | 23.6 ms: 1.03x slower                                                |
| django_template | 36.1 ms                                                                | 37.4 ms: 1.04x slower                                                |
| Geometric mean  | (ref)                                                                  | 1.02x slower                                                         |

All benchmarks:
===============

| Benchmark                | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|--------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_dna                | 188 ms                                                                 | 179 ms: 1.05x faster                                                 |
| pycparser                | 1.15 sec                                                               | 1.11 sec: 1.04x faster                                               |
| xml_etree_generate       | 85.4 ms                                                                | 83.5 ms: 1.02x faster                                                |
| create_gc_cycles         | 1.36 ms                                                                | 1.33 ms: 1.02x faster                                                |
| regex_effbot             | 3.03 ms                                                                | 2.96 ms: 1.02x faster                                                |
| coroutines               | 20.0 ms                                                                | 19.7 ms: 1.02x faster                                                |
| fannkuch                 | 416 ms                                                                 | 409 ms: 1.02x faster                                                 |
| sqlalchemy_imperative    | 22.8 ms                                                                | 22.5 ms: 1.01x faster                                                |
| nbody                    | 110 ms                                                                 | 108 ms: 1.01x faster                                                 |
| connected_components     | 479 ms                                                                 | 473 ms: 1.01x faster                                                 |
| xml_etree_process        | 60.4 ms                                                                | 59.6 ms: 1.01x faster                                                |
| pyflate                  | 447 ms                                                                 | 442 ms: 1.01x faster                                                 |
| subparsers               | 23.7 ms                                                                | 23.4 ms: 1.01x faster                                                |
| richards                 | 45.7 ms                                                                | 45.3 ms: 1.01x faster                                                |
| gc_traversal             | 2.11 ms                                                                | 2.09 ms: 1.01x faster                                                |
| sqlglot_v2_normalize     | 106 ms                                                                 | 105 ms: 1.01x faster                                                 |
| richards_super           | 53.7 ms                                                                | 53.3 ms: 1.01x faster                                                |
| float                    | 64.2 ms                                                                | 63.8 ms: 1.01x faster                                                |
| regex_compile            | 134 ms                                                                 | 133 ms: 1.01x faster                                                 |
| docutils                 | 2.63 sec                                                               | 2.62 sec: 1.01x faster                                               |
| nqueens                  | 79.1 ms                                                                | 78.6 ms: 1.01x faster                                                |
| async_tree_cpu_io_mixed  | 456 ms                                                                 | 454 ms: 1.01x faster                                                 |
| xml_etree_parse          | 142 ms                                                                 | 141 ms: 1.01x faster                                                 |
| python_startup           | 15.6 ms                                                                | 15.5 ms: 1.01x faster                                                |
| json_dumps               | 12.7 ms                                                                | 12.7 ms: 1.00x faster                                                |
| sqlalchemy_declarative   | 146 ms                                                                 | 147 ms: 1.00x slower                                                 |
| pprint_safe_repr         | 746 ms                                                                 | 750 ms: 1.01x slower                                                 |
| many_optionals           | 1.06 ms                                                                | 1.07 ms: 1.01x slower                                                |
| pprint_pformat           | 1.52 sec                                                               | 1.54 sec: 1.01x slower                                               |
| sympy_integrate          | 20.5 ms                                                                | 20.7 ms: 1.01x slower                                                |
| raytrace                 | 267 ms                                                                 | 270 ms: 1.01x slower                                                 |
| 2to3                     | 268 ms                                                                 | 271 ms: 1.01x slower                                                 |
| async_tree_io_tg         | 476 ms                                                                 | 481 ms: 1.01x slower                                                 |
| meteor_contest           | 120 ms                                                                 | 122 ms: 1.01x slower                                                 |
| sqlite_synth             | 1.95 us                                                                | 1.97 us: 1.01x slower                                                |
| scimark_sparse_mat_mult  | 4.52 ms                                                                | 4.58 ms: 1.01x slower                                                |
| go                       | 116 ms                                                                 | 117 ms: 1.01x slower                                                 |
| k_core                   | 2.17 sec                                                               | 2.19 sec: 1.01x slower                                               |
| mdp                      | 1.23 sec                                                               | 1.25 sec: 1.01x slower                                               |
| json                     | 5.10 ms                                                                | 5.16 ms: 1.01x slower                                                |
| sqlglot_v2_transpile     | 1.64 ms                                                                | 1.66 ms: 1.01x slower                                                |
| logging_format           | 7.28 us                                                                | 7.38 us: 1.01x slower                                                |
| genshi_xml               | 50.5 ms                                                                | 51.2 ms: 1.02x slower                                                |
| sympy_sum                | 166 ms                                                                 | 168 ms: 1.02x slower                                                 |
| tomli_loads              | 1.94 sec                                                               | 1.97 sec: 1.02x slower                                               |
| crypto_pyaes             | 77.1 ms                                                                | 78.3 ms: 1.02x slower                                                |
| coverage                 | 93.4 ms                                                                | 94.9 ms: 1.02x slower                                                |
| sympy_expand             | 489 ms                                                                 | 497 ms: 1.02x slower                                                 |
| deepcopy_memo            | 31.6 us                                                                | 32.2 us: 1.02x slower                                                |
| generators               | 27.7 ms                                                                | 28.1 ms: 1.02x slower                                                |
| mako                     | 14.1 ms                                                                | 14.4 ms: 1.02x slower                                                |
| unpickle_pure_python     | 218 us                                                                 | 222 us: 1.02x slower                                                 |
| spectral_norm            | 93.5 ms                                                                | 95.1 ms: 1.02x slower                                                |
| bpe_tokeniser            | 4.19 sec                                                               | 4.27 sec: 1.02x slower                                               |
| deltablue                | 3.41 ms                                                                | 3.47 ms: 1.02x slower                                                |
| typing_runtime_protocols | 171 us                                                                 | 174 us: 1.02x slower                                                 |
| sympy_str                | 294 ms                                                                 | 300 ms: 1.02x slower                                                 |
| hexiom                   | 6.11 ms                                                                | 6.25 ms: 1.02x slower                                                |
| json_loads               | 28.8 us                                                                | 29.5 us: 1.02x slower                                                |
| scimark_monte_carlo      | 64.8 ms                                                                | 66.4 ms: 1.03x slower                                                |
| genshi_text              | 23.0 ms                                                                | 23.6 ms: 1.03x slower                                                |
| scimark_sor              | 106 ms                                                                 | 108 ms: 1.03x slower                                                 |
| pickle_pure_python       | 308 us                                                                 | 317 us: 1.03x slower                                                 |
| django_template          | 36.1 ms                                                                | 37.4 ms: 1.04x slower                                                |
| logging_silent           | 78.6 ns                                                                | 83.9 ns: 1.07x slower                                                |
| Geometric mean           | (ref)                                                                  | 1.00x slower                                                         |

Benchmark hidden because not significant (30): scimark_fft, sqlglot_v2_optimize, pathlib, regex_v8, shortest_path, bench_mp_pool, pidigits, chaos, python_startup_no_site, async_tree_cpu_io_mixed_tg, deepcopy_reduce, telco, asyncio_websockets, xml_etree_iterparse, pylint, comprehensions, async_generators, sphinx, bench_thread_pool, html5lib, async_tree_none, dulwich_log, scimark_lu, deepcopy, async_tree_memoization_tg, async_tree_io, logging_simple, async_tree_memoization, sqlglot_v2_parse, async_tree_none_tg

- Geometric mean (including insignificant results): 1.003x slower

# HPT report

- Reliability score: 93.01% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x