# Results vs. base

- fork: DinoV
- ref: deferred_dunder_new
- machine: linux-x86_64
- commit hash: 82e19c2
- commit date: 2025-02-13
- overall geometric mean: 1.003x faster
- HPT reliability: 84.98%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250213-vultr-x86_64-python-05e89c34bd8389f87bd6-3.14.0a5+-05e89c3 | bm-20250213-vultr-x86_64-DinoV-deferred_dunder_new-3.14.0a5+-82e19c2 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 305 ms                                                                 | 302 ms: 1.01x faster                                                 |
| docutils       | 2.81 sec                                                               | 2.77 sec: 1.01x faster                                               |
| html5lib       | 69.9 ms                                                                | 69.5 ms: 1.01x faster                                                |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                         |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250213-vultr-x86_64-python-05e89c34bd8389f87bd6-3.14.0a5+-05e89c3 | bm-20250213-vultr-x86_64-DinoV-deferred_dunder_new-3.14.0a5+-82e19c2 |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| asyncio_websockets         | 518 ms                                                                 | 514 ms: 1.01x faster                                                 |
| coroutines                 | 23.7 ms                                                                | 23.6 ms: 1.00x faster                                                |
| async_generators           | 374 ms                                                                 | 373 ms: 1.00x faster                                                 |
| async_tree_cpu_io_mixed_tg | 499 ms                                                                 | 502 ms: 1.01x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                                         |

Benchmark hidden because not significant (7): async_tree_none_tg, async_tree_none, async_tree_io_tg, async_tree_io, async_tree_memoization, async_tree_memoization_tg, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250213-vultr-x86_64-python-05e89c34bd8389f87bd6-3.14.0a5+-05e89c3 | bm-20250213-vultr-x86_64-DinoV-deferred_dunder_new-3.14.0a5+-82e19c2 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pidigits       | 203 ms                                                                 | 192 ms: 1.06x faster                                                 |
| nbody          | 135 ms                                                                 | 133 ms: 1.01x faster                                                 |
| float          | 75.3 ms                                                                | 76.4 ms: 1.01x slower                                                |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250213-vultr-x86_64-python-05e89c34bd8389f87bd6-3.14.0a5+-05e89c3 | bm-20250213-vultr-x86_64-DinoV-deferred_dunder_new-3.14.0a5+-82e19c2 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 2.83 ms                                                                | 2.79 ms: 1.01x faster                                                |
| regex_v8       | 23.9 ms                                                                | 23.7 ms: 1.01x faster                                                |
| regex_dna      | 182 ms                                                                 | 181 ms: 1.00x faster                                                 |
| regex_compile  | 151 ms                                                                 | 152 ms: 1.00x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250213-vultr-x86_64-python-05e89c34bd8389f87bd6-3.14.0a5+-05e89c3 | bm-20250213-vultr-x86_64-DinoV-deferred_dunder_new-3.14.0a5+-82e19c2 |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| json_dumps           | 13.0 ms                                                                | 12.7 ms: 1.02x faster                                                |
| xml_etree_generate   | 97.0 ms                                                                | 96.2 ms: 1.01x faster                                                |
| xml_etree_process    | 70.5 ms                                                                | 70.1 ms: 1.01x faster                                                |
| json_loads           | 31.5 us                                                                | 31.3 us: 1.00x faster                                                |
| pickle_pure_python   | 360 us                                                                 | 362 us: 1.01x slower                                                 |
| tomli_loads          | 2.33 sec                                                               | 2.35 sec: 1.01x slower                                               |
| xml_etree_parse      | 128 ms                                                                 | 129 ms: 1.01x slower                                                 |
| unpickle_pure_python | 248 us                                                                 | 252 us: 1.02x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                         |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250213-vultr-x86_64-python-05e89c34bd8389f87bd6-3.14.0a5+-05e89c3 | bm-20250213-vultr-x86_64-DinoV-deferred_dunder_new-3.14.0a5+-82e19c2 |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup         | 15.3 ms                                                                | 15.3 ms: 1.01x faster                                                |
| python_startup_no_site | 9.64 ms                                                                | 9.59 ms: 1.00x faster                                                |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250213-vultr-x86_64-python-05e89c34bd8389f87bd6-3.14.0a5+-05e89c3 | bm-20250213-vultr-x86_64-DinoV-deferred_dunder_new-3.14.0a5+-82e19c2 |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| django_template | 42.5 ms                                                                | 42.0 ms: 1.01x faster                                                |
| genshi_text     | 27.8 ms                                                                | 27.9 ms: 1.00x slower                                                |
| mako            | 15.7 ms                                                                | 15.9 ms: 1.01x slower                                                |
| Geometric mean  | (ref)                                                                  | 1.00x slower                                                         |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20250213-vultr-x86_64-python-05e89c34bd8389f87bd6-3.14.0a5+-05e89c3 | bm-20250213-vultr-x86_64-DinoV-deferred_dunder_new-3.14.0a5+-82e19c2 |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pidigits                   | 203 ms                                                                 | 192 ms: 1.06x faster                                                 |
| mdp                        | 2.71 sec                                                               | 2.60 sec: 1.04x faster                                               |
| richards                   | 57.5 ms                                                                | 55.5 ms: 1.04x faster                                                |
| richards_super             | 66.3 ms                                                                | 64.6 ms: 1.03x faster                                                |
| json_dumps                 | 13.0 ms                                                                | 12.7 ms: 1.02x faster                                                |
| sqlalchemy_imperative      | 24.1 ms                                                                | 23.6 ms: 1.02x faster                                                |
| deepcopy                   | 315 us                                                                 | 307 us: 1.02x faster                                                 |
| scimark_sparse_mat_mult    | 5.80 ms                                                                | 5.67 ms: 1.02x faster                                                |
| regex_effbot               | 2.83 ms                                                                | 2.79 ms: 1.01x faster                                                |
| nbody                      | 135 ms                                                                 | 133 ms: 1.01x faster                                                 |
| docutils                   | 2.81 sec                                                               | 2.77 sec: 1.01x faster                                               |
| create_gc_cycles           | 1.41 ms                                                                | 1.39 ms: 1.01x faster                                                |
| connected_components       | 496 ms                                                                 | 490 ms: 1.01x faster                                                 |
| sqlalchemy_declarative     | 157 ms                                                                 | 155 ms: 1.01x faster                                                 |
| django_template            | 42.5 ms                                                                | 42.0 ms: 1.01x faster                                                |
| subparsers                 | 25.5 ms                                                                | 25.2 ms: 1.01x faster                                                |
| 2to3                       | 305 ms                                                                 | 302 ms: 1.01x faster                                                 |
| pathlib                    | 19.3 ms                                                                | 19.1 ms: 1.01x faster                                                |
| logging_simple             | 7.18 us                                                                | 7.12 us: 1.01x faster                                                |
| xml_etree_generate         | 97.0 ms                                                                | 96.2 ms: 1.01x faster                                                |
| asyncio_websockets         | 518 ms                                                                 | 514 ms: 1.01x faster                                                 |
| gc_traversal               | 1.76 ms                                                                | 1.75 ms: 1.01x faster                                                |
| crypto_pyaes               | 89.2 ms                                                                | 88.5 ms: 1.01x faster                                                |
| regex_v8                   | 23.9 ms                                                                | 23.7 ms: 1.01x faster                                                |
| logging_format             | 8.16 us                                                                | 8.10 us: 1.01x faster                                                |
| bench_mp_pool              | 95.2 ms                                                                | 94.6 ms: 1.01x faster                                                |
| deepcopy_reduce            | 3.21 us                                                                | 3.19 us: 1.01x faster                                                |
| html5lib                   | 69.9 ms                                                                | 69.5 ms: 1.01x faster                                                |
| xml_etree_process          | 70.5 ms                                                                | 70.1 ms: 1.01x faster                                                |
| pycparser                  | 1.19 sec                                                               | 1.18 sec: 1.01x faster                                               |
| python_startup             | 15.3 ms                                                                | 15.3 ms: 1.01x faster                                                |
| json_loads                 | 31.5 us                                                                | 31.3 us: 1.00x faster                                                |
| python_startup_no_site     | 9.64 ms                                                                | 9.59 ms: 1.00x faster                                                |
| coroutines                 | 23.7 ms                                                                | 23.6 ms: 1.00x faster                                                |
| many_optionals             | 1.18 ms                                                                | 1.17 ms: 1.00x faster                                                |
| sympy_integrate            | 24.0 ms                                                                | 23.9 ms: 1.00x faster                                                |
| bench_thread_pool          | 3.33 ms                                                                | 3.32 ms: 1.00x faster                                                |
| async_generators           | 374 ms                                                                 | 373 ms: 1.00x faster                                                 |
| logging_silent             | 115 ns                                                                 | 115 ns: 1.00x faster                                                 |
| regex_dna                  | 182 ms                                                                 | 181 ms: 1.00x faster                                                 |
| hexiom                     | 7.40 ms                                                                | 7.42 ms: 1.00x slower                                                |
| scimark_sor                | 133 ms                                                                 | 134 ms: 1.00x slower                                                 |
| pprint_pformat             | 1.70 sec                                                               | 1.70 sec: 1.00x slower                                               |
| genshi_text                | 27.8 ms                                                                | 27.9 ms: 1.00x slower                                                |
| regex_compile              | 151 ms                                                                 | 152 ms: 1.00x slower                                                 |
| pprint_safe_repr           | 826 ms                                                                 | 830 ms: 1.00x slower                                                 |
| chaos                      | 70.0 ms                                                                | 70.3 ms: 1.00x slower                                                |
| pickle_pure_python         | 360 us                                                                 | 362 us: 1.01x slower                                                 |
| async_tree_cpu_io_mixed_tg | 499 ms                                                                 | 502 ms: 1.01x slower                                                 |
| tomli_loads                | 2.33 sec                                                               | 2.35 sec: 1.01x slower                                               |
| scimark_monte_carlo        | 82.8 ms                                                                | 83.4 ms: 1.01x slower                                                |
| telco                      | 8.48 ms                                                                | 8.56 ms: 1.01x slower                                                |
| deepcopy_memo              | 38.9 us                                                                | 39.2 us: 1.01x slower                                                |
| xml_etree_parse            | 128 ms                                                                 | 129 ms: 1.01x slower                                                 |
| raytrace                   | 329 ms                                                                 | 332 ms: 1.01x slower                                                 |
| mako                       | 15.7 ms                                                                | 15.9 ms: 1.01x slower                                                |
| spectral_norm              | 110 ms                                                                 | 111 ms: 1.01x slower                                                 |
| nqueens                    | 97.2 ms                                                                | 98.3 ms: 1.01x slower                                                |
| sqlglot_parse              | 1.58 ms                                                                | 1.60 ms: 1.01x slower                                                |
| go                         | 140 ms                                                                 | 142 ms: 1.01x slower                                                 |
| float                      | 75.3 ms                                                                | 76.4 ms: 1.01x slower                                                |
| coverage                   | 95.2 ms                                                                | 96.8 ms: 1.02x slower                                                |
| fannkuch                   | 492 ms                                                                 | 501 ms: 1.02x slower                                                 |
| unpickle_pure_python       | 248 us                                                                 | 252 us: 1.02x slower                                                 |
| scimark_lu                 | 138 ms                                                                 | 141 ms: 1.02x slower                                                 |
| generators                 | 31.7 ms                                                                | 32.5 ms: 1.02x slower                                                |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                                         |

Benchmark hidden because not significant (30): pylint, sphinx, async_tree_none_tg, async_tree_none, sqlite_synth, shortest_path, sqlglot_normalize, async_tree_io_tg, deltablue, async_tree_io, dulwich_log, sympy_sum, sqlglot_optimize, sympy_str, comprehensions, xml_etree_iterparse, async_tree_memoization, async_tree_memoization_tg, sympy_expand, bpe_tokeniser, k_core, genshi_xml, async_tree_cpu_io_mixed, pyflate, scimark_fft, thrift, typing_runtime_protocols, meteor_contest, json, sqlglot_transpile

- Geometric mean (including insignificant results): 1.003x faster

# HPT report

- Reliability score: 84.98% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x