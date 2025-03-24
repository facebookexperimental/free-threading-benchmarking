# Results vs. base

- fork: mpage
- ref: measure_latest_lfb
- machine: linux-x86_64
- commit hash: 80fc5aa
- commit date: 2025-03-23
- overall geometric mean: 1.025x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250323-vultr-x86_64-python-ef06508f8ef1d2943b2f-3.14.0a6+-ef06508 | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 256 ms                                                                 | 250 ms: 1.03x faster                                                |
| docutils       | 2.59 sec                                                               | 2.57 sec: 1.01x faster                                              |
| sphinx         | 998 ms                                                                 | 985 ms: 1.01x faster                                                |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250323-vultr-x86_64-python-ef06508f8ef1d2943b2f-3.14.0a6+-ef06508 | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_memoization     | 324 ms                                                                 | 312 ms: 1.04x faster                                                |
| async_tree_none_tg         | 262 ms                                                                 | 252 ms: 1.04x faster                                                |
| async_tree_io_tg           | 652 ms                                                                 | 632 ms: 1.03x faster                                                |
| async_tree_memoization_tg  | 313 ms                                                                 | 303 ms: 1.03x faster                                                |
| async_tree_none            | 280 ms                                                                 | 271 ms: 1.03x faster                                                |
| async_generators           | 334 ms                                                                 | 326 ms: 1.03x faster                                                |
| async_tree_io              | 630 ms                                                                 | 619 ms: 1.02x faster                                                |
| async_tree_cpu_io_mixed    | 512 ms                                                                 | 505 ms: 1.02x faster                                                |
| async_tree_cpu_io_mixed_tg | 497 ms                                                                 | 490 ms: 1.01x faster                                                |
| Geometric mean             | (ref)                                                                  | 1.02x faster                                                        |

Benchmark hidden because not significant (2): coroutines, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250323-vultr-x86_64-python-ef06508f8ef1d2943b2f-3.14.0a6+-ef06508 | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| nbody          | 99.6 ms                                                                | 90.8 ms: 1.10x faster                                               |
| pidigits       | 208 ms                                                                 | 194 ms: 1.07x faster                                                |
| float          | 74.6 ms                                                                | 70.9 ms: 1.05x faster                                               |
| Geometric mean | (ref)                                                                  | 1.07x faster                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250323-vultr-x86_64-python-ef06508f8ef1d2943b2f-3.14.0a6+-ef06508 | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_compile  | 129 ms                                                                 | 125 ms: 1.04x faster                                                |
| regex_effbot   | 2.60 ms                                                                | 2.58 ms: 1.01x faster                                               |
| regex_dna      | 170 ms                                                                 | 173 ms: 1.02x slower                                                |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                        |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250323-vultr-x86_64-python-ef06508f8ef1d2943b2f-3.14.0a6+-ef06508 | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| tomli_loads          | 1.97 sec                                                               | 1.87 sec: 1.06x faster                                              |
| pickle_pure_python   | 318 us                                                                 | 302 us: 1.05x faster                                                |
| unpickle_pure_python | 222 us                                                                 | 213 us: 1.04x faster                                                |
| xml_etree_generate   | 85.6 ms                                                                | 83.0 ms: 1.03x faster                                               |
| xml_etree_process    | 60.0 ms                                                                | 58.4 ms: 1.03x faster                                               |
| json_loads           | 27.8 us                                                                | 27.2 us: 1.02x faster                                               |
| xml_etree_iterparse  | 92.6 ms                                                                | 91.2 ms: 1.02x faster                                               |
| xml_etree_parse      | 130 ms                                                                 | 129 ms: 1.01x faster                                                |
| json_dumps           | 11.2 ms                                                                | 11.0 ms: 1.01x faster                                               |
| Geometric mean       | (ref)                                                                  | 1.03x faster                                                        |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250323-vultr-x86_64-python-ef06508f8ef1d2943b2f-3.14.0a6+-ef06508 | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup_no_site | 8.61 ms                                                                | 8.64 ms: 1.00x slower                                               |
| python_startup         | 14.9 ms                                                                | 15.0 ms: 1.01x slower                                               |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250323-vultr-x86_64-python-ef06508f8ef1d2943b2f-3.14.0a6+-ef06508 | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|-----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| genshi_text     | 22.5 ms                                                                | 20.5 ms: 1.10x faster                                               |
| genshi_xml      | 50.9 ms                                                                | 47.9 ms: 1.06x faster                                               |
| django_template | 36.5 ms                                                                | 34.5 ms: 1.06x faster                                               |
| mako            | 12.0 ms                                                                | 11.9 ms: 1.01x faster                                               |
| Geometric mean  | (ref)                                                                  | 1.06x faster                                                        |

All benchmarks:
===============

| Benchmark                  | bm-20250323-vultr-x86_64-python-ef06508f8ef1d2943b2f-3.14.0a6+-ef06508 | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| generators                 | 30.7 ms                                                                | 27.1 ms: 1.13x faster                                               |
| genshi_text                | 22.5 ms                                                                | 20.5 ms: 1.10x faster                                               |
| nbody                      | 99.6 ms                                                                | 90.8 ms: 1.10x faster                                               |
| gc_traversal               | 4.44 ms                                                                | 4.08 ms: 1.09x faster                                               |
| logging_silent             | 102 ns                                                                 | 93.9 ns: 1.09x faster                                               |
| raytrace                   | 269 ms                                                                 | 249 ms: 1.08x faster                                                |
| pidigits                   | 208 ms                                                                 | 194 ms: 1.07x faster                                                |
| deepcopy                   | 268 us                                                                 | 252 us: 1.07x faster                                                |
| deepcopy_memo              | 30.4 us                                                                | 28.6 us: 1.06x faster                                               |
| deepcopy_reduce            | 2.81 us                                                                | 2.64 us: 1.06x faster                                               |
| scimark_monte_carlo        | 67.5 ms                                                                | 63.5 ms: 1.06x faster                                               |
| richards                   | 43.8 ms                                                                | 41.3 ms: 1.06x faster                                               |
| genshi_xml                 | 50.9 ms                                                                | 47.9 ms: 1.06x faster                                               |
| django_template            | 36.5 ms                                                                | 34.5 ms: 1.06x faster                                               |
| nqueens                    | 83.1 ms                                                                | 78.5 ms: 1.06x faster                                               |
| tomli_loads                | 1.97 sec                                                               | 1.87 sec: 1.06x faster                                              |
| richards_super             | 49.7 ms                                                                | 47.2 ms: 1.05x faster                                               |
| pickle_pure_python         | 318 us                                                                 | 302 us: 1.05x faster                                                |
| float                      | 74.6 ms                                                                | 70.9 ms: 1.05x faster                                               |
| pprint_pformat             | 1.49 sec                                                               | 1.42 sec: 1.05x faster                                              |
| pprint_safe_repr           | 732 ms                                                                 | 697 ms: 1.05x faster                                                |
| sqlglot_v2_transpile       | 1.61 ms                                                                | 1.54 ms: 1.05x faster                                               |
| sqlglot_v2_parse           | 1.30 ms                                                                | 1.24 ms: 1.05x faster                                               |
| pycparser                  | 1.15 sec                                                               | 1.10 sec: 1.05x faster                                              |
| go                         | 114 ms                                                                 | 109 ms: 1.04x faster                                                |
| unpickle_pure_python       | 222 us                                                                 | 213 us: 1.04x faster                                                |
| sqlglot_v2_optimize        | 52.7 ms                                                                | 50.6 ms: 1.04x faster                                               |
| chaos                      | 57.4 ms                                                                | 55.2 ms: 1.04x faster                                               |
| regex_compile              | 129 ms                                                                 | 125 ms: 1.04x faster                                                |
| async_tree_memoization     | 324 ms                                                                 | 312 ms: 1.04x faster                                                |
| async_tree_none_tg         | 262 ms                                                                 | 252 ms: 1.04x faster                                                |
| scimark_fft                | 330 ms                                                                 | 318 ms: 1.04x faster                                                |
| sqlglot_v2_normalize       | 104 ms                                                                 | 100 ms: 1.04x faster                                                |
| async_tree_io_tg           | 652 ms                                                                 | 632 ms: 1.03x faster                                                |
| async_tree_memoization_tg  | 313 ms                                                                 | 303 ms: 1.03x faster                                                |
| pyflate                    | 421 ms                                                                 | 408 ms: 1.03x faster                                                |
| xml_etree_generate         | 85.6 ms                                                                | 83.0 ms: 1.03x faster                                               |
| async_tree_none            | 280 ms                                                                 | 271 ms: 1.03x faster                                                |
| comprehensions             | 17.0 us                                                                | 16.5 us: 1.03x faster                                               |
| xml_etree_process          | 60.0 ms                                                                | 58.4 ms: 1.03x faster                                               |
| k_core                     | 2.07 sec                                                               | 2.02 sec: 1.03x faster                                              |
| fannkuch                   | 400 ms                                                                 | 390 ms: 1.03x faster                                                |
| 2to3                       | 256 ms                                                                 | 250 ms: 1.03x faster                                                |
| hexiom                     | 6.13 ms                                                                | 5.98 ms: 1.03x faster                                               |
| async_generators           | 334 ms                                                                 | 326 ms: 1.03x faster                                                |
| scimark_sor                | 114 ms                                                                 | 111 ms: 1.03x faster                                                |
| sympy_str                  | 279 ms                                                                 | 272 ms: 1.02x faster                                                |
| json_loads                 | 27.8 us                                                                | 27.2 us: 1.02x faster                                               |
| sympy_expand               | 469 ms                                                                 | 458 ms: 1.02x faster                                                |
| pathlib                    | 19.5 ms                                                                | 19.1 ms: 1.02x faster                                               |
| async_tree_io              | 630 ms                                                                 | 619 ms: 1.02x faster                                                |
| meteor_contest             | 101 ms                                                                 | 99.1 ms: 1.02x faster                                               |
| sympy_integrate            | 19.8 ms                                                                | 19.5 ms: 1.02x faster                                               |
| scimark_lu                 | 116 ms                                                                 | 114 ms: 1.02x faster                                                |
| xml_etree_iterparse        | 92.6 ms                                                                | 91.2 ms: 1.02x faster                                               |
| mdp                        | 2.32 sec                                                               | 2.29 sec: 1.02x faster                                              |
| async_tree_cpu_io_mixed    | 512 ms                                                                 | 505 ms: 1.02x faster                                                |
| crypto_pyaes               | 70.7 ms                                                                | 69.8 ms: 1.01x faster                                               |
| sphinx                     | 998 ms                                                                 | 985 ms: 1.01x faster                                                |
| async_tree_cpu_io_mixed_tg | 497 ms                                                                 | 490 ms: 1.01x faster                                                |
| mako                       | 12.0 ms                                                                | 11.9 ms: 1.01x faster                                               |
| many_optionals             | 1.04 ms                                                                | 1.03 ms: 1.01x faster                                               |
| bpe_tokeniser              | 4.34 sec                                                               | 4.29 sec: 1.01x faster                                              |
| xml_etree_parse            | 130 ms                                                                 | 129 ms: 1.01x faster                                                |
| shortest_path              | 442 ms                                                                 | 438 ms: 1.01x faster                                                |
| json_dumps                 | 11.2 ms                                                                | 11.0 ms: 1.01x faster                                               |
| sympy_sum                  | 157 ms                                                                 | 155 ms: 1.01x faster                                                |
| subparsers                 | 22.4 ms                                                                | 22.2 ms: 1.01x faster                                               |
| regex_effbot               | 2.60 ms                                                                | 2.58 ms: 1.01x faster                                               |
| docutils                   | 2.59 sec                                                               | 2.57 sec: 1.01x faster                                              |
| python_startup_no_site     | 8.61 ms                                                                | 8.64 ms: 1.00x slower                                               |
| python_startup             | 14.9 ms                                                                | 15.0 ms: 1.01x slower                                               |
| connected_components       | 394 ms                                                                 | 398 ms: 1.01x slower                                                |
| coverage                   | 79.4 ms                                                                | 80.4 ms: 1.01x slower                                               |
| regex_dna                  | 170 ms                                                                 | 173 ms: 1.02x slower                                                |
| sqlalchemy_imperative      | 19.7 ms                                                                | 20.1 ms: 1.02x slower                                               |
| spectral_norm              | 90.9 ms                                                                | 92.9 ms: 1.02x slower                                               |
| logging_simple             | 6.01 us                                                                | 6.14 us: 1.02x slower                                               |
| logging_format             | 6.66 us                                                                | 6.84 us: 1.03x slower                                               |
| deltablue                  | 3.14 ms                                                                | 3.24 ms: 1.03x slower                                               |
| Geometric mean             | (ref)                                                                  | 1.03x faster                                                        |

Benchmark hidden because not significant (15): pylint, json, dulwich_log, telco, typing_runtime_protocols, bench_thread_pool, sqlalchemy_declarative, coroutines, asyncio_websockets, thrift, bench_mp_pool, regex_v8, create_gc_cycles, sqlite_synth, scimark_sparse_mat_mult

- Geometric mean (including insignificant results): 1.025x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.00x