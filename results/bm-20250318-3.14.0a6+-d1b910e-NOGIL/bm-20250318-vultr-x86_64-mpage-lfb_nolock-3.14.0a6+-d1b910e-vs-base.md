# Results vs. base

- fork: mpage
- ref: lfb_nolock
- machine: linux-x86_64
- commit hash: d1b910e
- commit date: 2025-03-18
- overall geometric mean: 1.040x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6+-fd545d7 | bm-20250318-vultr-x86_64-mpage-lfb_nolock-3.14.0a6+-d1b910e |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| 2to3           | 301 ms                                                                 | 289 ms: 1.04x faster                                        |
| docutils       | 2.79 sec                                                               | 2.75 sec: 1.01x faster                                      |
| html5lib       | 72.2 ms                                                                | 69.8 ms: 1.03x faster                                       |
| sphinx         | 1.10 sec                                                               | 1.08 sec: 1.02x faster                                      |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6+-fd545d7 | bm-20250318-vultr-x86_64-mpage-lfb_nolock-3.14.0a6+-d1b910e |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 512 ms                                                                 | 476 ms: 1.07x faster                                        |
| async_tree_cpu_io_mixed    | 541 ms                                                                 | 508 ms: 1.07x faster                                        |
| async_tree_io              | 587 ms                                                                 | 553 ms: 1.06x faster                                        |
| async_tree_memoization_tg  | 309 ms                                                                 | 291 ms: 1.06x faster                                        |
| async_tree_none_tg         | 240 ms                                                                 | 226 ms: 1.06x faster                                        |
| async_tree_io_tg           | 553 ms                                                                 | 524 ms: 1.06x faster                                        |
| async_tree_none            | 277 ms                                                                 | 263 ms: 1.05x faster                                        |
| async_tree_memoization     | 339 ms                                                                 | 322 ms: 1.05x faster                                        |
| async_generators           | 376 ms                                                                 | 375 ms: 1.00x faster                                        |
| asyncio_websockets         | 513 ms                                                                 | 517 ms: 1.01x slower                                        |
| coroutines                 | 23.2 ms                                                                | 23.6 ms: 1.02x slower                                       |
| Geometric mean             | (ref)                                                                  | 1.04x faster                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6+-fd545d7 | bm-20250318-vultr-x86_64-mpage-lfb_nolock-3.14.0a6+-d1b910e |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| nbody          | 136 ms                                                                 | 114 ms: 1.19x faster                                        |
| float          | 78.2 ms                                                                | 67.3 ms: 1.16x faster                                       |
| pidigits       | 198 ms                                                                 | 196 ms: 1.01x faster                                        |
| Geometric mean | (ref)                                                                  | 1.12x faster                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6+-fd545d7 | bm-20250318-vultr-x86_64-mpage-lfb_nolock-3.14.0a6+-d1b910e |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| regex_effbot   | 2.78 ms                                                                | 2.63 ms: 1.06x faster                                       |
| regex_compile  | 157 ms                                                                 | 152 ms: 1.03x faster                                        |
| regex_dna      | 183 ms                                                                 | 177 ms: 1.03x faster                                        |
| regex_v8       | 22.0 ms                                                                | 21.5 ms: 1.02x faster                                       |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6+-fd545d7 | bm-20250318-vultr-x86_64-mpage-lfb_nolock-3.14.0a6+-d1b910e |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| tomli_loads          | 2.35 sec                                                               | 2.22 sec: 1.06x faster                                      |
| unpickle_pure_python | 257 us                                                                 | 243 us: 1.06x faster                                        |
| pickle_pure_python   | 363 us                                                                 | 346 us: 1.05x faster                                        |
| xml_etree_process    | 69.9 ms                                                                | 68.3 ms: 1.02x faster                                       |
| json_loads           | 29.8 us                                                                | 29.3 us: 1.02x faster                                       |
| xml_etree_iterparse  | 88.3 ms                                                                | 87.6 ms: 1.01x faster                                       |
| json_dumps           | 12.9 ms                                                                | 12.8 ms: 1.01x faster                                       |
| xml_etree_generate   | 96.2 ms                                                                | 96.9 ms: 1.01x slower                                       |
| xml_etree_parse      | 128 ms                                                                 | 130 ms: 1.01x slower                                        |
| Geometric mean       | (ref)                                                                  | 1.02x faster                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6+-fd545d7 | bm-20250318-vultr-x86_64-mpage-lfb_nolock-3.14.0a6+-d1b910e |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| python_startup_no_site | 11.2 ms                                                                | 11.1 ms: 1.00x faster                                       |
| python_startup         | 15.8 ms                                                                | 15.8 ms: 1.00x faster                                       |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6+-fd545d7 | bm-20250318-vultr-x86_64-mpage-lfb_nolock-3.14.0a6+-d1b910e |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| genshi_text     | 28.4 ms                                                                | 27.0 ms: 1.05x faster                                       |
| genshi_xml      | 59.7 ms                                                                | 57.9 ms: 1.03x faster                                       |
| django_template | 42.7 ms                                                                | 42.0 ms: 1.02x faster                                       |
| mako            | 15.5 ms                                                                | 15.6 ms: 1.00x slower                                       |
| Geometric mean  | (ref)                                                                  | 1.02x faster                                                |

All benchmarks:
===============

| Benchmark                  | bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6+-fd545d7 | bm-20250318-vultr-x86_64-mpage-lfb_nolock-3.14.0a6+-d1b910e |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| nbody                      | 136 ms                                                                 | 114 ms: 1.19x faster                                        |
| float                      | 78.2 ms                                                                | 67.3 ms: 1.16x faster                                       |
| go                         | 144 ms                                                                 | 130 ms: 1.10x faster                                        |
| scimark_monte_carlo        | 83.3 ms                                                                | 75.8 ms: 1.10x faster                                       |
| scimark_sparse_mat_mult    | 5.70 ms                                                                | 5.22 ms: 1.09x faster                                       |
| sqlglot_v2_parse           | 1.60 ms                                                                | 1.47 ms: 1.09x faster                                       |
| scimark_fft                | 393 ms                                                                 | 363 ms: 1.08x faster                                        |
| raytrace                   | 325 ms                                                                 | 301 ms: 1.08x faster                                        |
| scimark_sor                | 138 ms                                                                 | 128 ms: 1.08x faster                                        |
| sqlglot_v2_transpile       | 1.94 ms                                                                | 1.80 ms: 1.08x faster                                       |
| async_tree_cpu_io_mixed_tg | 512 ms                                                                 | 476 ms: 1.07x faster                                        |
| chaos                      | 70.1 ms                                                                | 65.5 ms: 1.07x faster                                       |
| richards                   | 55.2 ms                                                                | 51.6 ms: 1.07x faster                                       |
| fannkuch                   | 493 ms                                                                 | 461 ms: 1.07x faster                                        |
| deltablue                  | 3.84 ms                                                                | 3.59 ms: 1.07x faster                                       |
| richards_super             | 64.2 ms                                                                | 60.1 ms: 1.07x faster                                       |
| async_tree_cpu_io_mixed    | 541 ms                                                                 | 508 ms: 1.07x faster                                        |
| pycparser                  | 1.20 sec                                                               | 1.13 sec: 1.06x faster                                      |
| nqueens                    | 98.7 ms                                                                | 92.8 ms: 1.06x faster                                       |
| async_tree_io              | 587 ms                                                                 | 553 ms: 1.06x faster                                        |
| async_tree_memoization_tg  | 309 ms                                                                 | 291 ms: 1.06x faster                                        |
| deepcopy_memo              | 39.1 us                                                                | 36.9 us: 1.06x faster                                       |
| async_tree_none_tg         | 240 ms                                                                 | 226 ms: 1.06x faster                                        |
| tomli_loads                | 2.35 sec                                                               | 2.22 sec: 1.06x faster                                      |
| unpickle_pure_python       | 257 us                                                                 | 243 us: 1.06x faster                                        |
| async_tree_io_tg           | 553 ms                                                                 | 524 ms: 1.06x faster                                        |
| bpe_tokeniser              | 4.86 sec                                                               | 4.61 sec: 1.06x faster                                      |
| regex_effbot               | 2.78 ms                                                                | 2.63 ms: 1.06x faster                                       |
| pprint_safe_repr           | 843 ms                                                                 | 799 ms: 1.05x faster                                        |
| async_tree_none            | 277 ms                                                                 | 263 ms: 1.05x faster                                        |
| genshi_text                | 28.4 ms                                                                | 27.0 ms: 1.05x faster                                       |
| async_tree_memoization     | 339 ms                                                                 | 322 ms: 1.05x faster                                        |
| pickle_pure_python         | 363 us                                                                 | 346 us: 1.05x faster                                        |
| pyflate                    | 503 ms                                                                 | 480 ms: 1.05x faster                                        |
| pprint_pformat             | 1.73 sec                                                               | 1.66 sec: 1.05x faster                                      |
| many_optionals             | 1.19 ms                                                                | 1.13 ms: 1.05x faster                                       |
| thrift                     | 892 us                                                                 | 853 us: 1.05x faster                                        |
| deepcopy_reduce            | 3.24 us                                                                | 3.10 us: 1.05x faster                                       |
| meteor_contest             | 133 ms                                                                 | 127 ms: 1.04x faster                                        |
| 2to3                       | 301 ms                                                                 | 289 ms: 1.04x faster                                        |
| deepcopy                   | 312 us                                                                 | 300 us: 1.04x faster                                        |
| crypto_pyaes               | 87.8 ms                                                                | 84.6 ms: 1.04x faster                                       |
| hexiom                     | 7.60 ms                                                                | 7.32 ms: 1.04x faster                                       |
| spectral_norm              | 112 ms                                                                 | 108 ms: 1.04x faster                                        |
| logging_simple             | 7.30 us                                                                | 7.05 us: 1.04x faster                                       |
| comprehensions             | 21.1 us                                                                | 20.4 us: 1.03x faster                                       |
| html5lib                   | 72.2 ms                                                                | 69.8 ms: 1.03x faster                                       |
| scimark_lu                 | 140 ms                                                                 | 136 ms: 1.03x faster                                        |
| sympy_integrate            | 24.3 ms                                                                | 23.5 ms: 1.03x faster                                       |
| regex_compile              | 157 ms                                                                 | 152 ms: 1.03x faster                                        |
| genshi_xml                 | 59.7 ms                                                                | 57.9 ms: 1.03x faster                                       |
| create_gc_cycles           | 1.39 ms                                                                | 1.34 ms: 1.03x faster                                       |
| regex_dna                  | 183 ms                                                                 | 177 ms: 1.03x faster                                        |
| connected_components       | 503 ms                                                                 | 489 ms: 1.03x faster                                        |
| sqlite_synth               | 2.04 us                                                                | 1.99 us: 1.03x faster                                       |
| pathlib                    | 20.0 ms                                                                | 19.5 ms: 1.03x faster                                       |
| logging_format             | 8.33 us                                                                | 8.11 us: 1.03x faster                                       |
| sympy_str                  | 338 ms                                                                 | 330 ms: 1.03x faster                                        |
| typing_runtime_protocols   | 197 us                                                                 | 192 us: 1.03x faster                                        |
| sqlglot_v2_normalize       | 121 ms                                                                 | 118 ms: 1.03x faster                                        |
| k_core                     | 2.31 sec                                                               | 2.26 sec: 1.02x faster                                      |
| regex_v8                   | 22.0 ms                                                                | 21.5 ms: 1.02x faster                                       |
| sqlglot_v2_optimize        | 61.0 ms                                                                | 59.7 ms: 1.02x faster                                       |
| xml_etree_process          | 69.9 ms                                                                | 68.3 ms: 1.02x faster                                       |
| telco                      | 8.80 ms                                                                | 8.60 ms: 1.02x faster                                       |
| mdp                        | 2.79 sec                                                               | 2.73 sec: 1.02x faster                                      |
| gc_traversal               | 1.82 ms                                                                | 1.78 ms: 1.02x faster                                       |
| logging_silent             | 113 ns                                                                 | 111 ns: 1.02x faster                                        |
| sympy_sum                  | 188 ms                                                                 | 184 ms: 1.02x faster                                        |
| sphinx                     | 1.10 sec                                                               | 1.08 sec: 1.02x faster                                      |
| json_loads                 | 29.8 us                                                                | 29.3 us: 1.02x faster                                       |
| django_template            | 42.7 ms                                                                | 42.0 ms: 1.02x faster                                       |
| shortest_path              | 544 ms                                                                 | 535 ms: 1.02x faster                                        |
| sympy_expand               | 554 ms                                                                 | 546 ms: 1.02x faster                                        |
| docutils                   | 2.79 sec                                                               | 2.75 sec: 1.01x faster                                      |
| subparsers                 | 25.5 ms                                                                | 25.1 ms: 1.01x faster                                       |
| coverage                   | 97.6 ms                                                                | 96.2 ms: 1.01x faster                                       |
| bench_thread_pool          | 3.17 ms                                                                | 3.13 ms: 1.01x faster                                       |
| sqlalchemy_imperative      | 23.9 ms                                                                | 23.6 ms: 1.01x faster                                       |
| dulwich_log                | 73.5 ms                                                                | 72.7 ms: 1.01x faster                                       |
| json                       | 5.08 ms                                                                | 5.03 ms: 1.01x faster                                       |
| pidigits                   | 198 ms                                                                 | 196 ms: 1.01x faster                                        |
| xml_etree_iterparse        | 88.3 ms                                                                | 87.6 ms: 1.01x faster                                       |
| json_dumps                 | 12.9 ms                                                                | 12.8 ms: 1.01x faster                                       |
| sqlalchemy_declarative     | 158 ms                                                                 | 157 ms: 1.01x faster                                        |
| python_startup_no_site     | 11.2 ms                                                                | 11.1 ms: 1.00x faster                                       |
| bench_mp_pool              | 97.4 ms                                                                | 97.0 ms: 1.00x faster                                       |
| python_startup             | 15.8 ms                                                                | 15.8 ms: 1.00x faster                                       |
| async_generators           | 376 ms                                                                 | 375 ms: 1.00x faster                                        |
| mako                       | 15.5 ms                                                                | 15.6 ms: 1.00x slower                                       |
| asyncio_websockets         | 513 ms                                                                 | 517 ms: 1.01x slower                                        |
| xml_etree_generate         | 96.2 ms                                                                | 96.9 ms: 1.01x slower                                       |
| xml_etree_parse            | 128 ms                                                                 | 130 ms: 1.01x slower                                        |
| coroutines                 | 23.2 ms                                                                | 23.6 ms: 1.02x slower                                       |
| generators                 | 32.5 ms                                                                | 34.0 ms: 1.05x slower                                       |
| Geometric mean             | (ref)                                                                  | 1.04x faster                                                |

Benchmark hidden because not significant (1): pylint

- Geometric mean (including insignificant results): 1.040x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.00x