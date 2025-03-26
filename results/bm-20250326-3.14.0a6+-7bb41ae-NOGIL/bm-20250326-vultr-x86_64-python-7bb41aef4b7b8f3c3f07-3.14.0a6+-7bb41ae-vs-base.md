# Results vs. base

- fork: python
- ref: 7bb41aef4b7b8f3c3f07
- machine: linux-x86_64
- commit hash: 7bb41ae
- commit date: 2025-03-26
- overall geometric mean: 1.004x faster
- HPT reliability: 99.57%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250325-vultr-x86_64-python-a26a301f8b09c1825b28-3.14.0a6+-a26a301 | bm-20250326-vultr-x86_64-python-7bb41aef4b7b8f3c3f07-3.14.0a6+-7bb41ae |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 299 ms                                                                 | 298 ms: 1.00x faster                                                   |
| html5lib       | 71.5 ms                                                                | 70.5 ms: 1.01x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                           |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250325-vultr-x86_64-python-a26a301f8b09c1825b28-3.14.0a6+-a26a301 | bm-20250326-vultr-x86_64-python-7bb41aef4b7b8f3c3f07-3.14.0a6+-7bb41ae |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| coroutines                 | 24.4 ms                                                                | 23.4 ms: 1.04x faster                                                  |
| async_tree_cpu_io_mixed_tg | 484 ms                                                                 | 487 ms: 1.01x slower                                                   |
| async_generators           | 385 ms                                                                 | 388 ms: 1.01x slower                                                   |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                                           |

Benchmark hidden because not significant (8): async_tree_none_tg, async_tree_memoization_tg, async_tree_io_tg, asyncio_websockets, async_tree_memoization, async_tree_io, async_tree_none, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250325-vultr-x86_64-python-a26a301f8b09c1825b28-3.14.0a6+-a26a301 | bm-20250326-vultr-x86_64-python-7bb41aef4b7b8f3c3f07-3.14.0a6+-7bb41ae |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody          | 141 ms                                                                 | 139 ms: 1.01x faster                                                   |
| pidigits       | 198 ms                                                                 | 196 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                           |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250325-vultr-x86_64-python-a26a301f8b09c1825b28-3.14.0a6+-a26a301 | bm-20250326-vultr-x86_64-python-7bb41aef4b7b8f3c3f07-3.14.0a6+-7bb41ae |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_dna      | 182 ms                                                                 | 175 ms: 1.04x faster                                                   |
| regex_v8       | 21.8 ms                                                                | 21.5 ms: 1.01x faster                                                  |
| regex_compile  | 158 ms                                                                 | 156 ms: 1.01x faster                                                   |
| regex_effbot   | 2.67 ms                                                                | 2.85 ms: 1.07x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250325-vultr-x86_64-python-a26a301f8b09c1825b28-3.14.0a6+-a26a301 | bm-20250326-vultr-x86_64-python-7bb41aef4b7b8f3c3f07-3.14.0a6+-7bb41ae |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| tomli_loads          | 2.39 sec                                                               | 2.34 sec: 1.02x faster                                                 |
| pickle_pure_python   | 360 us                                                                 | 357 us: 1.01x faster                                                   |
| json_loads           | 29.5 us                                                                | 29.6 us: 1.00x slower                                                  |
| xml_etree_process    | 70.7 ms                                                                | 70.9 ms: 1.00x slower                                                  |
| unpickle_pure_python | 256 us                                                                 | 257 us: 1.00x slower                                                   |
| json_dumps           | 12.7 ms                                                                | 12.9 ms: 1.01x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                           |

Benchmark hidden because not significant (3): xml_etree_parse, xml_etree_iterparse, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250325-vultr-x86_64-python-a26a301f8b09c1825b28-3.14.0a6+-a26a301 | bm-20250326-vultr-x86_64-python-7bb41aef4b7b8f3c3f07-3.14.0a6+-7bb41ae |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 11.1 ms                                                                | 11.1 ms: 1.00x faster                                                  |
| python_startup         | 15.7 ms                                                                | 15.7 ms: 1.00x faster                                                  |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250325-vultr-x86_64-python-a26a301f8b09c1825b28-3.14.0a6+-a26a301 | bm-20250326-vultr-x86_64-python-7bb41aef4b7b8f3c3f07-3.14.0a6+-7bb41ae |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 16.1 ms                                                                | 15.7 ms: 1.02x faster                                                  |
| django_template | 43.3 ms                                                                | 42.7 ms: 1.01x faster                                                  |
| genshi_text     | 28.6 ms                                                                | 28.4 ms: 1.01x faster                                                  |
| genshi_xml      | 59.7 ms                                                                | 60.4 ms: 1.01x slower                                                  |
| Geometric mean  | (ref)                                                                  | 1.01x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20250325-vultr-x86_64-python-a26a301f8b09c1825b28-3.14.0a6+-a26a301 | bm-20250326-vultr-x86_64-python-7bb41aef4b7b8f3c3f07-3.14.0a6+-7bb41ae |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_dna                  | 182 ms                                                                 | 175 ms: 1.04x faster                                                   |
| mdp                        | 2.73 sec                                                               | 2.62 sec: 1.04x faster                                                 |
| coroutines                 | 24.4 ms                                                                | 23.4 ms: 1.04x faster                                                  |
| nqueens                    | 99.6 ms                                                                | 96.8 ms: 1.03x faster                                                  |
| mako                       | 16.1 ms                                                                | 15.7 ms: 1.02x faster                                                  |
| comprehensions             | 21.1 us                                                                | 20.6 us: 1.02x faster                                                  |
| tomli_loads                | 2.39 sec                                                               | 2.34 sec: 1.02x faster                                                 |
| deepcopy_memo              | 39.9 us                                                                | 39.3 us: 1.02x faster                                                  |
| create_gc_cycles           | 1.38 ms                                                                | 1.36 ms: 1.02x faster                                                  |
| nbody                      | 141 ms                                                                 | 139 ms: 1.01x faster                                                   |
| html5lib                   | 71.5 ms                                                                | 70.5 ms: 1.01x faster                                                  |
| richards_super             | 65.1 ms                                                                | 64.1 ms: 1.01x faster                                                  |
| go                         | 146 ms                                                                 | 144 ms: 1.01x faster                                                   |
| django_template            | 43.3 ms                                                                | 42.7 ms: 1.01x faster                                                  |
| richards                   | 55.8 ms                                                                | 55.1 ms: 1.01x faster                                                  |
| dulwich_log                | 73.8 ms                                                                | 72.9 ms: 1.01x faster                                                  |
| scimark_fft                | 401 ms                                                                 | 397 ms: 1.01x faster                                                   |
| crypto_pyaes               | 89.2 ms                                                                | 88.2 ms: 1.01x faster                                                  |
| pidigits                   | 198 ms                                                                 | 196 ms: 1.01x faster                                                   |
| typing_runtime_protocols   | 200 us                                                                 | 198 us: 1.01x faster                                                   |
| scimark_monte_carlo        | 84.8 ms                                                                | 83.9 ms: 1.01x faster                                                  |
| regex_v8                   | 21.8 ms                                                                | 21.5 ms: 1.01x faster                                                  |
| sqlite_synth               | 2.03 us                                                                | 2.01 us: 1.01x faster                                                  |
| deltablue                  | 3.92 ms                                                                | 3.88 ms: 1.01x faster                                                  |
| pycparser                  | 1.20 sec                                                               | 1.18 sec: 1.01x faster                                                 |
| spectral_norm              | 113 ms                                                                 | 112 ms: 1.01x faster                                                   |
| gc_traversal               | 1.81 ms                                                                | 1.80 ms: 1.01x faster                                                  |
| sqlglot_v2_parse           | 1.61 ms                                                                | 1.59 ms: 1.01x faster                                                  |
| regex_compile              | 158 ms                                                                 | 156 ms: 1.01x faster                                                   |
| chaos                      | 69.6 ms                                                                | 69.0 ms: 1.01x faster                                                  |
| pickle_pure_python         | 360 us                                                                 | 357 us: 1.01x faster                                                   |
| pprint_pformat             | 1.74 sec                                                               | 1.73 sec: 1.01x faster                                                 |
| scimark_sparse_mat_mult    | 5.76 ms                                                                | 5.72 ms: 1.01x faster                                                  |
| pprint_safe_repr           | 843 ms                                                                 | 837 ms: 1.01x faster                                                   |
| sqlalchemy_declarative     | 159 ms                                                                 | 158 ms: 1.01x faster                                                   |
| deepcopy                   | 314 us                                                                 | 313 us: 1.01x faster                                                   |
| fannkuch                   | 501 ms                                                                 | 498 ms: 1.01x faster                                                   |
| many_optionals             | 1.17 ms                                                                | 1.17 ms: 1.01x faster                                                  |
| hexiom                     | 7.67 ms                                                                | 7.63 ms: 1.01x faster                                                  |
| genshi_text                | 28.6 ms                                                                | 28.4 ms: 1.01x faster                                                  |
| bench_thread_pool          | 3.17 ms                                                                | 3.16 ms: 1.00x faster                                                  |
| 2to3                       | 299 ms                                                                 | 298 ms: 1.00x faster                                                   |
| python_startup_no_site     | 11.1 ms                                                                | 11.1 ms: 1.00x faster                                                  |
| python_startup             | 15.7 ms                                                                | 15.7 ms: 1.00x faster                                                  |
| sympy_integrate            | 23.7 ms                                                                | 23.6 ms: 1.00x faster                                                  |
| bpe_tokeniser              | 4.86 sec                                                               | 4.85 sec: 1.00x faster                                                 |
| logging_silent             | 114 ns                                                                 | 114 ns: 1.00x slower                                                   |
| json_loads                 | 29.5 us                                                                | 29.6 us: 1.00x slower                                                  |
| xml_etree_process          | 70.7 ms                                                                | 70.9 ms: 1.00x slower                                                  |
| unpickle_pure_python       | 256 us                                                                 | 257 us: 1.00x slower                                                   |
| sympy_expand               | 552 ms                                                                 | 555 ms: 1.01x slower                                                   |
| k_core                     | 2.30 sec                                                               | 2.31 sec: 1.01x slower                                                 |
| async_tree_cpu_io_mixed_tg | 484 ms                                                                 | 487 ms: 1.01x slower                                                   |
| json                       | 5.07 ms                                                                | 5.10 ms: 1.01x slower                                                  |
| coverage                   | 108 ms                                                                 | 109 ms: 1.01x slower                                                   |
| connected_components       | 505 ms                                                                 | 509 ms: 1.01x slower                                                   |
| async_generators           | 385 ms                                                                 | 388 ms: 1.01x slower                                                   |
| scimark_lu                 | 142 ms                                                                 | 144 ms: 1.01x slower                                                   |
| logging_simple             | 7.25 us                                                                | 7.33 us: 1.01x slower                                                  |
| genshi_xml                 | 59.7 ms                                                                | 60.4 ms: 1.01x slower                                                  |
| json_dumps                 | 12.7 ms                                                                | 12.9 ms: 1.01x slower                                                  |
| deepcopy_reduce            | 3.20 us                                                                | 3.25 us: 1.01x slower                                                  |
| logging_format             | 8.24 us                                                                | 8.36 us: 1.01x slower                                                  |
| pyflate                    | 506 ms                                                                 | 514 ms: 1.02x slower                                                   |
| subparsers                 | 25.4 ms                                                                | 25.8 ms: 1.02x slower                                                  |
| generators                 | 31.0 ms                                                                | 32.1 ms: 1.04x slower                                                  |
| regex_effbot               | 2.67 ms                                                                | 2.85 ms: 1.07x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                                           |

Benchmark hidden because not significant (29): sqlalchemy_imperative, sqlglot_v2_transpile, async_tree_none_tg, meteor_contest, async_tree_memoization_tg, pylint, async_tree_io_tg, shortest_path, pathlib, sympy_str, bench_mp_pool, asyncio_websockets, float, async_tree_memoization, xml_etree_parse, raytrace, sqlglot_v2_normalize, async_tree_io, docutils, scimark_sor, sphinx, xml_etree_iterparse, sqlglot_v2_optimize, async_tree_none, sympy_sum, xml_etree_generate, thrift, async_tree_cpu_io_mixed, telco

- Geometric mean (including insignificant results): 1.004x faster

# HPT report

- Reliability score: 99.57% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x