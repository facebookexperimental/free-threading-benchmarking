# Results vs. base

- fork: mpage
- ref: measure_gc_changes
- machine: linux-x86_64
- commit hash: 0f5d11c
- commit date: 2024-12-04
- overall geometric mean: 1.006x faster
- HPT reliability: 98.54%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 | bm-20241204-vultr-x86_64-mpage-measure_gc_changes-3.14.0a2+-0f5d11c |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 377 ms                                                                 | 376 ms: 1.00x faster                                                |
| docutils       | 3.22 sec                                                               | 3.19 sec: 1.01x faster                                              |
| html5lib       | 102 ms                                                                 | 98.9 ms: 1.03x faster                                               |
| sphinx         | 1.24 sec                                                               | 1.23 sec: 1.01x faster                                              |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 | bm-20241204-vultr-x86_64-mpage-measure_gc_changes-3.14.0a2+-0f5d11c |
|-------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| coroutines              | 28.7 ms                                                                | 28.4 ms: 1.01x faster                                               |
| async_generators        | 471 ms                                                                 | 467 ms: 1.01x faster                                                |
| async_tree_cpu_io_mixed | 654 ms                                                                 | 659 ms: 1.01x slower                                                |
| Geometric mean          | (ref)                                                                  | 1.00x faster                                                        |

Benchmark hidden because not significant (8): async_tree_none_tg, asyncio_websockets, async_tree_memoization_tg, async_tree_cpu_io_mixed_tg, async_tree_none, async_tree_memoization, async_tree_io, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 | bm-20241204-vultr-x86_64-mpage-measure_gc_changes-3.14.0a2+-0f5d11c |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| nbody          | 134 ms                                                                 | 128 ms: 1.05x faster                                                |
| pidigits       | 184 ms                                                                 | 184 ms: 1.00x slower                                                |
| float          | 142 ms                                                                 | 143 ms: 1.01x slower                                                |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 | bm-20241204-vultr-x86_64-mpage-measure_gc_changes-3.14.0a2+-0f5d11c |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_effbot   | 3.03 ms                                                                | 2.67 ms: 1.13x faster                                               |
| regex_v8       | 26.1 ms                                                                | 23.8 ms: 1.10x faster                                               |
| regex_dna      | 187 ms                                                                 | 175 ms: 1.07x faster                                                |
| regex_compile  | 194 ms                                                                 | 191 ms: 1.01x faster                                                |
| Geometric mean | (ref)                                                                  | 1.08x faster                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 | bm-20241204-vultr-x86_64-mpage-measure_gc_changes-3.14.0a2+-0f5d11c |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| unpickle_pure_python | 386 us                                                                 | 379 us: 1.02x faster                                                |
| pickle_pure_python   | 562 us                                                                 | 556 us: 1.01x faster                                                |
| json_dumps           | 14.5 ms                                                                | 14.5 ms: 1.01x faster                                               |
| xml_etree_parse      | 129 ms                                                                 | 130 ms: 1.00x slower                                                |
| xml_etree_generate   | 102 ms                                                                 | 103 ms: 1.01x slower                                                |
| tomli_loads          | 2.77 sec                                                               | 2.81 sec: 1.01x slower                                              |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                        |

Benchmark hidden because not significant (3): json_loads, xml_etree_iterparse, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 | bm-20241204-vultr-x86_64-mpage-measure_gc_changes-3.14.0a2+-0f5d11c |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup | 17.4 ms                                                                | 17.4 ms: 1.00x slower                                               |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                        |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 | bm-20241204-vultr-x86_64-mpage-measure_gc_changes-3.14.0a2+-0f5d11c |
|-----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| mako            | 20.0 ms                                                                | 19.6 ms: 1.02x faster                                               |
| genshi_xml      | 67.6 ms                                                                | 66.7 ms: 1.01x faster                                               |
| django_template | 55.6 ms                                                                | 55.2 ms: 1.01x faster                                               |
| genshi_text     | 33.6 ms                                                                | 33.5 ms: 1.00x faster                                               |
| Geometric mean  | (ref)                                                                  | 1.01x faster                                                        |

All benchmarks:
===============

| Benchmark               | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 | bm-20241204-vultr-x86_64-mpage-measure_gc_changes-3.14.0a2+-0f5d11c |
|-------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_effbot            | 3.03 ms                                                                | 2.67 ms: 1.13x faster                                               |
| regex_v8                | 26.1 ms                                                                | 23.8 ms: 1.10x faster                                               |
| regex_dna               | 187 ms                                                                 | 175 ms: 1.07x faster                                                |
| nbody                   | 134 ms                                                                 | 128 ms: 1.05x faster                                                |
| html5lib                | 102 ms                                                                 | 98.9 ms: 1.03x faster                                               |
| coverage                | 102 ms                                                                 | 99.7 ms: 1.02x faster                                               |
| mako                    | 20.0 ms                                                                | 19.6 ms: 1.02x faster                                               |
| richards_super          | 101 ms                                                                 | 99.1 ms: 1.02x faster                                               |
| logging_silent          | 201 ns                                                                 | 197 ns: 1.02x faster                                                |
| deepcopy_memo           | 45.8 us                                                                | 44.9 us: 1.02x faster                                               |
| unpickle_pure_python    | 386 us                                                                 | 379 us: 1.02x faster                                                |
| generators              | 39.1 ms                                                                | 38.4 ms: 1.02x faster                                               |
| richards                | 84.0 ms                                                                | 82.6 ms: 1.02x faster                                               |
| scimark_fft             | 408 ms                                                                 | 401 ms: 1.02x faster                                                |
| pyflate                 | 737 ms                                                                 | 726 ms: 1.01x faster                                                |
| raytrace                | 611 ms                                                                 | 602 ms: 1.01x faster                                                |
| genshi_xml              | 67.6 ms                                                                | 66.7 ms: 1.01x faster                                               |
| scimark_sparse_mat_mult | 5.90 ms                                                                | 5.82 ms: 1.01x faster                                               |
| fannkuch                | 517 ms                                                                 | 511 ms: 1.01x faster                                                |
| regex_compile           | 194 ms                                                                 | 191 ms: 1.01x faster                                                |
| pickle_pure_python      | 562 us                                                                 | 556 us: 1.01x faster                                                |
| docutils                | 3.22 sec                                                               | 3.19 sec: 1.01x faster                                              |
| pprint_safe_repr        | 1.08 sec                                                               | 1.07 sec: 1.01x faster                                              |
| comprehensions          | 29.2 us                                                                | 28.9 us: 1.01x faster                                               |
| coroutines              | 28.7 ms                                                                | 28.4 ms: 1.01x faster                                               |
| sphinx                  | 1.24 sec                                                               | 1.23 sec: 1.01x faster                                              |
| django_template         | 55.6 ms                                                                | 55.2 ms: 1.01x faster                                               |
| scimark_monte_carlo     | 123 ms                                                                 | 122 ms: 1.01x faster                                                |
| async_generators        | 471 ms                                                                 | 467 ms: 1.01x faster                                                |
| bpe_tokeniser           | 5.51 sec                                                               | 5.47 sec: 1.01x faster                                              |
| json_dumps              | 14.5 ms                                                                | 14.5 ms: 1.01x faster                                               |
| go                      | 283 ms                                                                 | 281 ms: 1.00x faster                                                |
| sqlalchemy_declarative  | 208 ms                                                                 | 207 ms: 1.00x faster                                                |
| chaos                   | 112 ms                                                                 | 112 ms: 1.00x faster                                                |
| genshi_text             | 33.6 ms                                                                | 33.5 ms: 1.00x faster                                               |
| 2to3                    | 377 ms                                                                 | 376 ms: 1.00x faster                                                |
| deepcopy                | 354 us                                                                 | 353 us: 1.00x faster                                                |
| python_startup          | 17.4 ms                                                                | 17.4 ms: 1.00x slower                                               |
| pidigits                | 184 ms                                                                 | 184 ms: 1.00x slower                                                |
| xml_etree_parse         | 129 ms                                                                 | 130 ms: 1.00x slower                                                |
| scimark_lu              | 193 ms                                                                 | 194 ms: 1.00x slower                                                |
| hexiom                  | 10.8 ms                                                                | 10.8 ms: 1.00x slower                                               |
| pathlib                 | 20.6 ms                                                                | 20.7 ms: 1.01x slower                                               |
| sympy_sum               | 357 ms                                                                 | 359 ms: 1.01x slower                                                |
| sympy_str               | 492 ms                                                                 | 495 ms: 1.01x slower                                                |
| xml_etree_generate      | 102 ms                                                                 | 103 ms: 1.01x slower                                                |
| async_tree_cpu_io_mixed | 654 ms                                                                 | 659 ms: 1.01x slower                                                |
| telco                   | 8.73 ms                                                                | 8.79 ms: 1.01x slower                                               |
| spectral_norm           | 132 ms                                                                 | 134 ms: 1.01x slower                                                |
| float                   | 142 ms                                                                 | 143 ms: 1.01x slower                                                |
| logging_format          | 12.5 us                                                                | 12.6 us: 1.01x slower                                               |
| sqlglot_optimize        | 74.7 ms                                                                | 75.4 ms: 1.01x slower                                               |
| sqlglot_normalize       | 150 ms                                                                 | 151 ms: 1.01x slower                                                |
| many_optionals          | 1.36 ms                                                                | 1.37 ms: 1.01x slower                                               |
| thrift                  | 1.21 ms                                                                | 1.22 ms: 1.01x slower                                               |
| scimark_sor             | 243 ms                                                                 | 245 ms: 1.01x slower                                                |
| tomli_loads             | 2.77 sec                                                               | 2.81 sec: 1.01x slower                                              |
| crypto_pyaes            | 93.8 ms                                                                | 95.4 ms: 1.02x slower                                               |
| subparsers              | 33.0 ms                                                                | 33.7 ms: 1.02x slower                                               |
| gc_traversal            | 3.19 ms                                                                | 3.30 ms: 1.03x slower                                               |
| Geometric mean          | (ref)                                                                  | 1.01x faster                                                        |

Benchmark hidden because not significant (36): async_tree_none_tg, typing_runtime_protocols, shortest_path, pylint, sqlalchemy_imperative, connected_components, sqlite_synth, json, asyncio_websockets, deltablue, async_tree_memoization_tg, create_gc_cycles, k_core, pprint_pformat, pycparser, python_startup_no_site, deepcopy_reduce, mdp, sympy_expand, async_tree_cpu_io_mixed_tg, bench_thread_pool, async_tree_none, bench_mp_pool, async_tree_memoization, async_tree_io, json_loads, sympy_integrate, xml_etree_iterparse, xml_etree_process, dulwich_log, nqueens, async_tree_io_tg, meteor_contest, sqlglot_transpile, logging_simple, sqlglot_parse

- Geometric mean (including insignificant results): 1.006x faster

# HPT report

- Reliability score: 98.54% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x