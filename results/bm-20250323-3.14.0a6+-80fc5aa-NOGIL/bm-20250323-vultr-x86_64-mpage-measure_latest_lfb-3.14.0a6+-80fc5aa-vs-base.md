# Results vs. base

- fork: mpage
- ref: measure_latest_lfb
- machine: linux-x86_64
- commit hash: 80fc5aa
- commit date: 2025-03-23
- overall geometric mean: 1.021x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250323-vultr-x86_64-python-ef06508f8ef1d2943b2f-3.14.0a6+-ef06508 | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 297 ms                                                                 | 289 ms: 1.03x faster                                                |
| docutils       | 2.77 sec                                                               | 2.75 sec: 1.01x faster                                              |
| html5lib       | 71.3 ms                                                                | 68.1 ms: 1.05x faster                                               |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                        |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250323-vultr-x86_64-python-ef06508f8ef1d2943b2f-3.14.0a6+-ef06508 | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_none_tg         | 238 ms                                                                 | 233 ms: 1.02x faster                                                |
| async_tree_memoization_tg  | 299 ms                                                                 | 294 ms: 1.02x faster                                                |
| async_tree_io              | 583 ms                                                                 | 573 ms: 1.02x faster                                                |
| async_generators           | 386 ms                                                                 | 380 ms: 1.02x faster                                                |
| async_tree_io_tg           | 550 ms                                                                 | 541 ms: 1.02x faster                                                |
| async_tree_cpu_io_mixed    | 521 ms                                                                 | 512 ms: 1.02x faster                                                |
| async_tree_memoization     | 331 ms                                                                 | 326 ms: 1.02x faster                                                |
| async_tree_cpu_io_mixed_tg | 483 ms                                                                 | 478 ms: 1.01x faster                                                |
| async_tree_none            | 277 ms                                                                 | 274 ms: 1.01x faster                                                |
| coroutines                 | 23.5 ms                                                                | 23.7 ms: 1.01x slower                                               |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                        |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250323-vultr-x86_64-python-ef06508f8ef1d2943b2f-3.14.0a6+-ef06508 | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| nbody          | 130 ms                                                                 | 120 ms: 1.08x faster                                                |
| float          | 77.5 ms                                                                | 71.8 ms: 1.08x faster                                               |
| pidigits       | 202 ms                                                                 | 198 ms: 1.02x faster                                                |
| Geometric mean | (ref)                                                                  | 1.06x faster                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250323-vultr-x86_64-python-ef06508f8ef1d2943b2f-3.14.0a6+-ef06508 | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_dna      | 180 ms                                                                 | 168 ms: 1.07x faster                                                |
| regex_compile  | 157 ms                                                                 | 153 ms: 1.03x faster                                                |
| regex_v8       | 21.5 ms                                                                | 21.3 ms: 1.01x faster                                               |
| regex_effbot   | 2.65 ms                                                                | 2.73 ms: 1.03x slower                                               |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250323-vultr-x86_64-python-ef06508f8ef1d2943b2f-3.14.0a6+-ef06508 | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| unpickle_pure_python | 255 us                                                                 | 244 us: 1.04x faster                                                |
| tomli_loads          | 2.34 sec                                                               | 2.25 sec: 1.04x faster                                              |
| pickle_pure_python   | 357 us                                                                 | 343 us: 1.04x faster                                                |
| xml_etree_iterparse  | 88.2 ms                                                                | 87.6 ms: 1.01x faster                                               |
| xml_etree_process    | 70.5 ms                                                                | 70.7 ms: 1.00x slower                                               |
| json_loads           | 29.1 us                                                                | 29.8 us: 1.03x slower                                               |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                        |

Benchmark hidden because not significant (3): xml_etree_generate, json_dumps, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250323-vultr-x86_64-python-ef06508f8ef1d2943b2f-3.14.0a6+-ef06508 | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup_no_site | 11.2 ms                                                                | 11.1 ms: 1.00x faster                                               |
| python_startup         | 15.8 ms                                                                | 15.8 ms: 1.00x faster                                               |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250323-vultr-x86_64-python-ef06508f8ef1d2943b2f-3.14.0a6+-ef06508 | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|-----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| genshi_text     | 28.2 ms                                                                | 27.1 ms: 1.04x faster                                               |
| genshi_xml      | 59.4 ms                                                                | 57.8 ms: 1.03x faster                                               |
| django_template | 42.4 ms                                                                | 41.8 ms: 1.02x faster                                               |
| mako            | 15.8 ms                                                                | 15.7 ms: 1.01x faster                                               |
| Geometric mean  | (ref)                                                                  | 1.02x faster                                                        |

All benchmarks:
===============

| Benchmark                  | bm-20250323-vultr-x86_64-python-ef06508f8ef1d2943b2f-3.14.0a6+-ef06508 | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| nbody                      | 130 ms                                                                 | 120 ms: 1.08x faster                                                |
| float                      | 77.5 ms                                                                | 71.8 ms: 1.08x faster                                               |
| scimark_sparse_mat_mult    | 5.60 ms                                                                | 5.21 ms: 1.07x faster                                               |
| regex_dna                  | 180 ms                                                                 | 168 ms: 1.07x faster                                                |
| scimark_fft                | 389 ms                                                                 | 364 ms: 1.07x faster                                                |
| fannkuch                   | 498 ms                                                                 | 466 ms: 1.07x faster                                                |
| go                         | 144 ms                                                                 | 135 ms: 1.07x faster                                                |
| deepcopy_memo              | 39.5 us                                                                | 37.3 us: 1.06x faster                                               |
| scimark_monte_carlo        | 83.3 ms                                                                | 78.9 ms: 1.06x faster                                               |
| sqlglot_v2_parse           | 1.60 ms                                                                | 1.52 ms: 1.05x faster                                               |
| meteor_contest             | 134 ms                                                                 | 128 ms: 1.05x faster                                                |
| scimark_sor                | 136 ms                                                                 | 129 ms: 1.05x faster                                                |
| deepcopy                   | 316 us                                                                 | 301 us: 1.05x faster                                                |
| html5lib                   | 71.3 ms                                                                | 68.1 ms: 1.05x faster                                               |
| deltablue                  | 3.87 ms                                                                | 3.70 ms: 1.05x faster                                               |
| unpickle_pure_python       | 255 us                                                                 | 244 us: 1.04x faster                                                |
| sqlglot_v2_transpile       | 1.94 ms                                                                | 1.85 ms: 1.04x faster                                               |
| tomli_loads                | 2.34 sec                                                               | 2.25 sec: 1.04x faster                                              |
| pickle_pure_python         | 357 us                                                                 | 343 us: 1.04x faster                                                |
| genshi_text                | 28.2 ms                                                                | 27.1 ms: 1.04x faster                                               |
| deepcopy_reduce            | 3.23 us                                                                | 3.10 us: 1.04x faster                                               |
| raytrace                   | 319 ms                                                                 | 307 ms: 1.04x faster                                                |
| richards_super             | 64.1 ms                                                                | 62.1 ms: 1.03x faster                                               |
| crypto_pyaes               | 88.8 ms                                                                | 85.9 ms: 1.03x faster                                               |
| spectral_norm              | 113 ms                                                                 | 109 ms: 1.03x faster                                                |
| bpe_tokeniser              | 4.86 sec                                                               | 4.72 sec: 1.03x faster                                              |
| chaos                      | 68.4 ms                                                                | 66.4 ms: 1.03x faster                                               |
| many_optionals             | 1.18 ms                                                                | 1.15 ms: 1.03x faster                                               |
| logging_format             | 8.39 us                                                                | 8.16 us: 1.03x faster                                               |
| genshi_xml                 | 59.4 ms                                                                | 57.8 ms: 1.03x faster                                               |
| pyflate                    | 503 ms                                                                 | 489 ms: 1.03x faster                                                |
| create_gc_cycles           | 1.38 ms                                                                | 1.34 ms: 1.03x faster                                               |
| shortest_path              | 549 ms                                                                 | 535 ms: 1.03x faster                                                |
| richards                   | 55.2 ms                                                                | 53.8 ms: 1.03x faster                                               |
| 2to3                       | 297 ms                                                                 | 289 ms: 1.03x faster                                                |
| pprint_pformat             | 1.73 sec                                                               | 1.68 sec: 1.03x faster                                              |
| regex_compile              | 157 ms                                                                 | 153 ms: 1.03x faster                                                |
| async_tree_none_tg         | 238 ms                                                                 | 233 ms: 1.02x faster                                                |
| scimark_lu                 | 141 ms                                                                 | 138 ms: 1.02x faster                                                |
| connected_components       | 502 ms                                                                 | 490 ms: 1.02x faster                                                |
| subparsers                 | 25.8 ms                                                                | 25.2 ms: 1.02x faster                                               |
| mdp                        | 2.80 sec                                                               | 2.74 sec: 1.02x faster                                              |
| pprint_safe_repr           | 834 ms                                                                 | 816 ms: 1.02x faster                                                |
| hexiom                     | 7.58 ms                                                                | 7.42 ms: 1.02x faster                                               |
| comprehensions             | 20.8 us                                                                | 20.4 us: 1.02x faster                                               |
| async_tree_memoization_tg  | 299 ms                                                                 | 294 ms: 1.02x faster                                                |
| sqlglot_v2_optimize        | 61.1 ms                                                                | 59.9 ms: 1.02x faster                                               |
| pidigits                   | 202 ms                                                                 | 198 ms: 1.02x faster                                                |
| typing_runtime_protocols   | 197 us                                                                 | 194 us: 1.02x faster                                                |
| k_core                     | 2.30 sec                                                               | 2.26 sec: 1.02x faster                                              |
| coverage                   | 109 ms                                                                 | 107 ms: 1.02x faster                                                |
| telco                      | 9.09 ms                                                                | 8.94 ms: 1.02x faster                                               |
| gc_traversal               | 1.82 ms                                                                | 1.79 ms: 1.02x faster                                               |
| async_tree_io              | 583 ms                                                                 | 573 ms: 1.02x faster                                                |
| async_generators           | 386 ms                                                                 | 380 ms: 1.02x faster                                                |
| async_tree_io_tg           | 550 ms                                                                 | 541 ms: 1.02x faster                                                |
| async_tree_cpu_io_mixed    | 521 ms                                                                 | 512 ms: 1.02x faster                                                |
| django_template            | 42.4 ms                                                                | 41.8 ms: 1.02x faster                                               |
| async_tree_memoization     | 331 ms                                                                 | 326 ms: 1.02x faster                                                |
| sympy_str                  | 337 ms                                                                 | 332 ms: 1.01x faster                                                |
| logging_silent             | 112 ns                                                                 | 111 ns: 1.01x faster                                                |
| sympy_integrate            | 23.7 ms                                                                | 23.4 ms: 1.01x faster                                               |
| async_tree_cpu_io_mixed_tg | 483 ms                                                                 | 478 ms: 1.01x faster                                                |
| async_tree_none            | 277 ms                                                                 | 274 ms: 1.01x faster                                                |
| logging_simple             | 7.39 us                                                                | 7.32 us: 1.01x faster                                               |
| regex_v8                   | 21.5 ms                                                                | 21.3 ms: 1.01x faster                                               |
| pycparser                  | 1.19 sec                                                               | 1.18 sec: 1.01x faster                                              |
| sqlglot_v2_normalize       | 120 ms                                                                 | 119 ms: 1.01x faster                                                |
| docutils                   | 2.77 sec                                                               | 2.75 sec: 1.01x faster                                              |
| xml_etree_iterparse        | 88.2 ms                                                                | 87.6 ms: 1.01x faster                                               |
| bench_thread_pool          | 3.16 ms                                                                | 3.14 ms: 1.01x faster                                               |
| nqueens                    | 97.2 ms                                                                | 96.6 ms: 1.01x faster                                               |
| mako                       | 15.8 ms                                                                | 15.7 ms: 1.01x faster                                               |
| pathlib                    | 19.9 ms                                                                | 19.8 ms: 1.01x faster                                               |
| bench_mp_pool              | 97.5 ms                                                                | 97.1 ms: 1.00x faster                                               |
| python_startup_no_site     | 11.2 ms                                                                | 11.1 ms: 1.00x faster                                               |
| python_startup             | 15.8 ms                                                                | 15.8 ms: 1.00x faster                                               |
| xml_etree_process          | 70.5 ms                                                                | 70.7 ms: 1.00x slower                                               |
| sqlalchemy_declarative     | 157 ms                                                                 | 158 ms: 1.01x slower                                                |
| coroutines                 | 23.5 ms                                                                | 23.7 ms: 1.01x slower                                               |
| sqlalchemy_imperative      | 23.8 ms                                                                | 24.1 ms: 1.01x slower                                               |
| dulwich_log                | 73.2 ms                                                                | 74.2 ms: 1.01x slower                                               |
| json_loads                 | 29.1 us                                                                | 29.8 us: 1.03x slower                                               |
| regex_effbot               | 2.65 ms                                                                | 2.73 ms: 1.03x slower                                               |
| generators                 | 31.9 ms                                                                | 33.7 ms: 1.06x slower                                               |
| Geometric mean             | (ref)                                                                  | 1.02x faster                                                        |

Benchmark hidden because not significant (11): sympy_expand, asyncio_websockets, sphinx, xml_etree_generate, json_dumps, json, xml_etree_parse, pylint, sympy_sum, sqlite_synth, thrift

- Geometric mean (including insignificant results): 1.021x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.00x