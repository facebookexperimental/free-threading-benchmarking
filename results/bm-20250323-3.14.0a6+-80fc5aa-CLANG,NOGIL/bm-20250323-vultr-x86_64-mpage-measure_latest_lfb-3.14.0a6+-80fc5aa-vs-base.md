# Results vs. base

- fork: mpage
- ref: measure_latest_lfb
- machine: linux-x86_64
- commit hash: 80fc5aa
- commit date: 2025-03-23
- overall geometric mean: 1.026x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250323-vultr-x86_64-python-ef06508f8ef1d2943b2f-3.14.0a6+-ef06508 | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 277 ms                                                                 | 269 ms: 1.03x faster                                                |
| docutils       | 2.66 sec                                                               | 2.63 sec: 1.01x faster                                              |
| html5lib       | 63.8 ms                                                                | 61.7 ms: 1.04x faster                                               |
| sphinx         | 1.04 sec                                                               | 1.03 sec: 1.00x faster                                              |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250323-vultr-x86_64-python-ef06508f8ef1d2943b2f-3.14.0a6+-ef06508 | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_io              | 531 ms                                                                 | 519 ms: 1.02x faster                                                |
| async_tree_memoization     | 305 ms                                                                 | 299 ms: 1.02x faster                                                |
| async_tree_io_tg           | 495 ms                                                                 | 486 ms: 1.02x faster                                                |
| async_tree_none            | 254 ms                                                                 | 250 ms: 1.01x faster                                                |
| async_tree_memoization_tg  | 270 ms                                                                 | 267 ms: 1.01x faster                                                |
| async_tree_none_tg         | 214 ms                                                                 | 211 ms: 1.01x faster                                                |
| async_tree_cpu_io_mixed    | 469 ms                                                                 | 464 ms: 1.01x faster                                                |
| coroutines                 | 19.9 ms                                                                | 19.7 ms: 1.01x faster                                               |
| async_tree_cpu_io_mixed_tg | 432 ms                                                                 | 430 ms: 1.01x faster                                                |
| async_generators           | 333 ms                                                                 | 332 ms: 1.00x faster                                                |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                        |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250323-vultr-x86_64-python-ef06508f8ef1d2943b2f-3.14.0a6+-ef06508 | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| nbody          | 119 ms                                                                 | 108 ms: 1.10x faster                                                |
| float          | 68.7 ms                                                                | 64.2 ms: 1.07x faster                                               |
| Geometric mean | (ref)                                                                  | 1.06x faster                                                        |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250323-vultr-x86_64-python-ef06508f8ef1d2943b2f-3.14.0a6+-ef06508 | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                                 | 135 ms: 1.04x faster                                                |
| regex_effbot   | 2.97 ms                                                                | 2.99 ms: 1.01x slower                                               |
| regex_v8       | 21.7 ms                                                                | 21.8 ms: 1.01x slower                                               |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                        |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250323-vultr-x86_64-python-ef06508f8ef1d2943b2f-3.14.0a6+-ef06508 | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                                               | 2.00 sec: 1.05x faster                                              |
| pickle_pure_python   | 326 us                                                                 | 311 us: 1.05x faster                                                |
| unpickle_pure_python | 228 us                                                                 | 218 us: 1.04x faster                                                |
| xml_etree_parse      | 143 ms                                                                 | 141 ms: 1.02x faster                                                |
| xml_etree_generate   | 85.6 ms                                                                | 84.1 ms: 1.02x faster                                               |
| xml_etree_process    | 60.7 ms                                                                | 59.7 ms: 1.02x faster                                               |
| xml_etree_iterparse  | 85.7 ms                                                                | 84.3 ms: 1.02x faster                                               |
| json_dumps           | 12.8 ms                                                                | 12.6 ms: 1.01x faster                                               |
| json_loads           | 29.5 us                                                                | 29.3 us: 1.01x faster                                               |
| Geometric mean       | (ref)                                                                  | 1.03x faster                                                        |

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup_no_site, python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250323-vultr-x86_64-python-ef06508f8ef1d2943b2f-3.14.0a6+-ef06508 | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|-----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| genshi_text     | 24.9 ms                                                                | 23.4 ms: 1.07x faster                                               |
| genshi_xml      | 52.7 ms                                                                | 50.6 ms: 1.04x faster                                               |
| django_template | 37.5 ms                                                                | 36.5 ms: 1.03x faster                                               |
| mako            | 14.8 ms                                                                | 14.4 ms: 1.03x faster                                               |
| Geometric mean  | (ref)                                                                  | 1.04x faster                                                        |

All benchmarks:
===============

| Benchmark                  | bm-20250323-vultr-x86_64-python-ef06508f8ef1d2943b2f-3.14.0a6+-ef06508 | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| scimark_fft                | 334 ms                                                                 | 294 ms: 1.13x faster                                                |
| deltablue                  | 3.63 ms                                                                | 3.27 ms: 1.11x faster                                               |
| nbody                      | 119 ms                                                                 | 108 ms: 1.10x faster                                                |
| scimark_monte_carlo        | 70.3 ms                                                                | 65.0 ms: 1.08x faster                                               |
| pyflate                    | 472 ms                                                                 | 438 ms: 1.08x faster                                                |
| scimark_sparse_mat_mult    | 4.78 ms                                                                | 4.46 ms: 1.07x faster                                               |
| float                      | 68.7 ms                                                                | 64.2 ms: 1.07x faster                                               |
| raytrace                   | 285 ms                                                                 | 267 ms: 1.07x faster                                                |
| logging_silent             | 91.2 ns                                                                | 85.3 ns: 1.07x faster                                               |
| go                         | 126 ms                                                                 | 118 ms: 1.07x faster                                                |
| chaos                      | 60.4 ms                                                                | 56.7 ms: 1.07x faster                                               |
| genshi_text                | 24.9 ms                                                                | 23.4 ms: 1.07x faster                                               |
| richards                   | 48.0 ms                                                                | 45.2 ms: 1.06x faster                                               |
| deepcopy_memo              | 34.0 us                                                                | 32.1 us: 1.06x faster                                               |
| fannkuch                   | 435 ms                                                                 | 412 ms: 1.06x faster                                                |
| richards_super             | 56.6 ms                                                                | 53.7 ms: 1.05x faster                                               |
| tomli_loads                | 2.11 sec                                                               | 2.00 sec: 1.05x faster                                              |
| sqlglot_v2_parse           | 1.42 ms                                                                | 1.35 ms: 1.05x faster                                               |
| pprint_pformat             | 1.62 sec                                                               | 1.54 sec: 1.05x faster                                              |
| deepcopy_reduce            | 2.81 us                                                                | 2.68 us: 1.05x faster                                               |
| pprint_safe_repr           | 786 ms                                                                 | 751 ms: 1.05x faster                                                |
| pickle_pure_python         | 326 us                                                                 | 311 us: 1.05x faster                                                |
| scimark_lu                 | 117 ms                                                                 | 112 ms: 1.04x faster                                                |
| regex_compile              | 141 ms                                                                 | 135 ms: 1.04x faster                                                |
| unpickle_pure_python       | 228 us                                                                 | 218 us: 1.04x faster                                                |
| scimark_sor                | 112 ms                                                                 | 107 ms: 1.04x faster                                                |
| deepcopy                   | 272 us                                                                 | 260 us: 1.04x faster                                                |
| sqlglot_v2_transpile       | 1.72 ms                                                                | 1.65 ms: 1.04x faster                                               |
| genshi_xml                 | 52.7 ms                                                                | 50.6 ms: 1.04x faster                                               |
| connected_components       | 498 ms                                                                 | 479 ms: 1.04x faster                                                |
| hexiom                     | 6.66 ms                                                                | 6.41 ms: 1.04x faster                                               |
| nqueens                    | 85.6 ms                                                                | 82.7 ms: 1.04x faster                                               |
| html5lib                   | 63.8 ms                                                                | 61.7 ms: 1.04x faster                                               |
| meteor_contest             | 122 ms                                                                 | 118 ms: 1.03x faster                                                |
| many_optionals             | 1.11 ms                                                                | 1.08 ms: 1.03x faster                                               |
| 2to3                       | 277 ms                                                                 | 269 ms: 1.03x faster                                                |
| shortest_path              | 532 ms                                                                 | 516 ms: 1.03x faster                                                |
| django_template            | 37.5 ms                                                                | 36.5 ms: 1.03x faster                                               |
| comprehensions             | 17.5 us                                                                | 17.0 us: 1.03x faster                                               |
| telco                      | 8.20 ms                                                                | 7.98 ms: 1.03x faster                                               |
| mako                       | 14.8 ms                                                                | 14.4 ms: 1.03x faster                                               |
| sqlglot_v2_optimize        | 54.5 ms                                                                | 53.2 ms: 1.03x faster                                               |
| sqlglot_v2_normalize       | 107 ms                                                                 | 104 ms: 1.02x faster                                                |
| async_tree_io              | 531 ms                                                                 | 519 ms: 1.02x faster                                                |
| sympy_integrate            | 21.7 ms                                                                | 21.2 ms: 1.02x faster                                               |
| async_tree_memoization     | 305 ms                                                                 | 299 ms: 1.02x faster                                                |
| bpe_tokeniser              | 4.38 sec                                                               | 4.29 sec: 1.02x faster                                              |
| xml_etree_parse            | 143 ms                                                                 | 141 ms: 1.02x faster                                                |
| sympy_expand               | 508 ms                                                                 | 498 ms: 1.02x faster                                                |
| async_tree_io_tg           | 495 ms                                                                 | 486 ms: 1.02x faster                                                |
| xml_etree_generate         | 85.6 ms                                                                | 84.1 ms: 1.02x faster                                               |
| pycparser                  | 1.16 sec                                                               | 1.14 sec: 1.02x faster                                              |
| logging_format             | 7.57 us                                                                | 7.44 us: 1.02x faster                                               |
| xml_etree_process          | 60.7 ms                                                                | 59.7 ms: 1.02x faster                                               |
| xml_etree_iterparse        | 85.7 ms                                                                | 84.3 ms: 1.02x faster                                               |
| async_tree_none            | 254 ms                                                                 | 250 ms: 1.01x faster                                                |
| bench_thread_pool          | 3.12 ms                                                                | 3.07 ms: 1.01x faster                                               |
| async_tree_memoization_tg  | 270 ms                                                                 | 267 ms: 1.01x faster                                                |
| k_core                     | 2.21 sec                                                               | 2.19 sec: 1.01x faster                                              |
| dulwich_log                | 71.7 ms                                                                | 70.8 ms: 1.01x faster                                               |
| sympy_str                  | 306 ms                                                                 | 302 ms: 1.01x faster                                                |
| json_dumps                 | 12.8 ms                                                                | 12.6 ms: 1.01x faster                                               |
| async_tree_none_tg         | 214 ms                                                                 | 211 ms: 1.01x faster                                                |
| typing_runtime_protocols   | 175 us                                                                 | 173 us: 1.01x faster                                                |
| docutils                   | 2.66 sec                                                               | 2.63 sec: 1.01x faster                                              |
| subparsers                 | 24.5 ms                                                                | 24.3 ms: 1.01x faster                                               |
| sympy_sum                  | 172 ms                                                                 | 170 ms: 1.01x faster                                                |
| async_tree_cpu_io_mixed    | 469 ms                                                                 | 464 ms: 1.01x faster                                                |
| coroutines                 | 19.9 ms                                                                | 19.7 ms: 1.01x faster                                               |
| crypto_pyaes               | 79.6 ms                                                                | 79.0 ms: 1.01x faster                                               |
| coverage                   | 94.8 ms                                                                | 94.1 ms: 1.01x faster                                               |
| json_loads                 | 29.5 us                                                                | 29.3 us: 1.01x faster                                               |
| async_tree_cpu_io_mixed_tg | 432 ms                                                                 | 430 ms: 1.01x faster                                                |
| sphinx                     | 1.04 sec                                                               | 1.03 sec: 1.00x faster                                              |
| async_generators           | 333 ms                                                                 | 332 ms: 1.00x faster                                                |
| gc_traversal               | 2.07 ms                                                                | 2.08 ms: 1.00x slower                                               |
| spectral_norm              | 91.7 ms                                                                | 92.2 ms: 1.01x slower                                               |
| regex_effbot               | 2.97 ms                                                                | 2.99 ms: 1.01x slower                                               |
| regex_v8                   | 21.7 ms                                                                | 21.8 ms: 1.01x slower                                               |
| generators                 | 27.4 ms                                                                | 28.3 ms: 1.03x slower                                               |
| mdp                        | 2.68 sec                                                               | 2.83 sec: 1.05x slower                                              |
| Geometric mean             | (ref)                                                                  | 1.03x faster                                                        |

Benchmark hidden because not significant (15): logging_simple, thrift, sqlalchemy_imperative, pylint, json, sqlalchemy_declarative, pidigits, pathlib, python_startup_no_site, bench_mp_pool, python_startup, asyncio_websockets, regex_dna, sqlite_synth, create_gc_cycles

- Geometric mean (including insignificant results): 1.026x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.01x