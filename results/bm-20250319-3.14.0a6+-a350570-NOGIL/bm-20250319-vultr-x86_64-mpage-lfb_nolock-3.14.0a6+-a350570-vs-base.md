# Results vs. base

- fork: mpage
- ref: lfb_nolock
- machine: linux-x86_64
- commit hash: a350570
- commit date: 2025-03-19
- overall geometric mean: 1.043x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6+-fd545d7 | bm-20250319-vultr-x86_64-mpage-lfb_nolock-3.14.0a6+-a350570 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| 2to3           | 301 ms                                                                 | 288 ms: 1.05x faster                                        |
| docutils       | 2.79 sec                                                               | 2.75 sec: 1.01x faster                                      |
| html5lib       | 72.2 ms                                                                | 67.2 ms: 1.07x faster                                       |
| sphinx         | 1.10 sec                                                               | 1.08 sec: 1.02x faster                                      |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6+-fd545d7 | bm-20250319-vultr-x86_64-mpage-lfb_nolock-3.14.0a6+-a350570 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| async_tree_memoization_tg  | 309 ms                                                                 | 289 ms: 1.07x faster                                        |
| async_tree_none_tg         | 240 ms                                                                 | 225 ms: 1.06x faster                                        |
| async_tree_none            | 277 ms                                                                 | 261 ms: 1.06x faster                                        |
| async_tree_memoization     | 339 ms                                                                 | 322 ms: 1.05x faster                                        |
| async_tree_io_tg           | 553 ms                                                                 | 525 ms: 1.05x faster                                        |
| async_tree_io              | 587 ms                                                                 | 557 ms: 1.05x faster                                        |
| async_generators           | 376 ms                                                                 | 372 ms: 1.01x faster                                        |
| asyncio_websockets         | 513 ms                                                                 | 518 ms: 1.01x slower                                        |
| async_tree_cpu_io_mixed_tg | 512 ms                                                                 | 555 ms: 1.08x slower                                        |
| async_tree_cpu_io_mixed    | 541 ms                                                                 | 587 ms: 1.08x slower                                        |
| Geometric mean             | (ref)                                                                  | 1.02x faster                                                |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6+-fd545d7 | bm-20250319-vultr-x86_64-mpage-lfb_nolock-3.14.0a6+-a350570 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| nbody          | 136 ms                                                                 | 105 ms: 1.29x faster                                        |
| float          | 78.2 ms                                                                | 65.3 ms: 1.20x faster                                       |
| pidigits       | 198 ms                                                                 | 228 ms: 1.15x slower                                        |
| Geometric mean | (ref)                                                                  | 1.10x faster                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6+-fd545d7 | bm-20250319-vultr-x86_64-mpage-lfb_nolock-3.14.0a6+-a350570 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| regex_dna      | 183 ms                                                                 | 165 ms: 1.10x faster                                        |
| regex_effbot   | 2.78 ms                                                                | 2.63 ms: 1.05x faster                                       |
| regex_v8       | 22.0 ms                                                                | 21.0 ms: 1.05x faster                                       |
| regex_compile  | 157 ms                                                                 | 151 ms: 1.04x faster                                        |
| Geometric mean | (ref)                                                                  | 1.06x faster                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6+-fd545d7 | bm-20250319-vultr-x86_64-mpage-lfb_nolock-3.14.0a6+-a350570 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| unpickle_pure_python | 257 us                                                                 | 236 us: 1.09x faster                                        |
| pickle_pure_python   | 363 us                                                                 | 342 us: 1.06x faster                                        |
| tomli_loads          | 2.35 sec                                                               | 2.26 sec: 1.04x faster                                      |
| xml_etree_process    | 69.9 ms                                                                | 68.7 ms: 1.02x faster                                       |
| json_loads           | 29.8 us                                                                | 29.5 us: 1.01x faster                                       |
| json_dumps           | 12.9 ms                                                                | 12.8 ms: 1.01x faster                                       |
| Geometric mean       | (ref)                                                                  | 1.02x faster                                                |

Benchmark hidden because not significant (3): xml_etree_generate, xml_etree_parse, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6+-fd545d7 | bm-20250319-vultr-x86_64-mpage-lfb_nolock-3.14.0a6+-a350570 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| python_startup_no_site | 11.2 ms                                                                | 11.1 ms: 1.01x faster                                       |
| python_startup         | 15.8 ms                                                                | 15.7 ms: 1.01x faster                                       |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6+-fd545d7 | bm-20250319-vultr-x86_64-mpage-lfb_nolock-3.14.0a6+-a350570 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| genshi_text     | 28.4 ms                                                                | 26.9 ms: 1.06x faster                                       |
| django_template | 42.7 ms                                                                | 41.4 ms: 1.03x faster                                       |
| genshi_xml      | 59.7 ms                                                                | 57.9 ms: 1.03x faster                                       |
| mako            | 15.5 ms                                                                | 15.6 ms: 1.00x slower                                       |
| Geometric mean  | (ref)                                                                  | 1.03x faster                                                |

All benchmarks:
===============

| Benchmark                  | bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6+-fd545d7 | bm-20250319-vultr-x86_64-mpage-lfb_nolock-3.14.0a6+-a350570 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| nbody                      | 136 ms                                                                 | 105 ms: 1.29x faster                                        |
| float                      | 78.2 ms                                                                | 65.3 ms: 1.20x faster                                       |
| go                         | 144 ms                                                                 | 127 ms: 1.13x faster                                        |
| scimark_fft                | 393 ms                                                                 | 347 ms: 1.13x faster                                        |
| scimark_monte_carlo        | 83.3 ms                                                                | 74.1 ms: 1.12x faster                                       |
| raytrace                   | 325 ms                                                                 | 292 ms: 1.11x faster                                        |
| deltablue                  | 3.84 ms                                                                | 3.47 ms: 1.11x faster                                       |
| sqlglot_v2_parse           | 1.60 ms                                                                | 1.45 ms: 1.10x faster                                       |
| regex_dna                  | 183 ms                                                                 | 165 ms: 1.10x faster                                        |
| chaos                      | 70.1 ms                                                                | 63.6 ms: 1.10x faster                                       |
| scimark_sparse_mat_mult    | 5.70 ms                                                                | 5.19 ms: 1.10x faster                                       |
| pyflate                    | 503 ms                                                                 | 460 ms: 1.09x faster                                        |
| fannkuch                   | 493 ms                                                                 | 452 ms: 1.09x faster                                        |
| scimark_sor                | 138 ms                                                                 | 127 ms: 1.09x faster                                        |
| sqlglot_v2_transpile       | 1.94 ms                                                                | 1.78 ms: 1.09x faster                                       |
| unpickle_pure_python       | 257 us                                                                 | 236 us: 1.09x faster                                        |
| logging_silent             | 113 ns                                                                 | 105 ns: 1.08x faster                                        |
| html5lib                   | 72.2 ms                                                                | 67.2 ms: 1.07x faster                                       |
| deepcopy_memo              | 39.1 us                                                                | 36.5 us: 1.07x faster                                       |
| richards                   | 55.2 ms                                                                | 51.5 ms: 1.07x faster                                       |
| async_tree_memoization_tg  | 309 ms                                                                 | 289 ms: 1.07x faster                                        |
| nqueens                    | 98.7 ms                                                                | 92.4 ms: 1.07x faster                                       |
| thrift                     | 892 us                                                                 | 837 us: 1.07x faster                                        |
| comprehensions             | 21.1 us                                                                | 19.8 us: 1.07x faster                                       |
| richards_super             | 64.2 ms                                                                | 60.2 ms: 1.07x faster                                       |
| bpe_tokeniser              | 4.86 sec                                                               | 4.57 sec: 1.06x faster                                      |
| async_tree_none_tg         | 240 ms                                                                 | 225 ms: 1.06x faster                                        |
| pickle_pure_python         | 363 us                                                                 | 342 us: 1.06x faster                                        |
| async_tree_none            | 277 ms                                                                 | 261 ms: 1.06x faster                                        |
| pycparser                  | 1.20 sec                                                               | 1.13 sec: 1.06x faster                                      |
| pprint_safe_repr           | 843 ms                                                                 | 798 ms: 1.06x faster                                        |
| genshi_text                | 28.4 ms                                                                | 26.9 ms: 1.06x faster                                       |
| regex_effbot               | 2.78 ms                                                                | 2.63 ms: 1.05x faster                                       |
| async_tree_memoization     | 339 ms                                                                 | 322 ms: 1.05x faster                                        |
| async_tree_io_tg           | 553 ms                                                                 | 525 ms: 1.05x faster                                        |
| async_tree_io              | 587 ms                                                                 | 557 ms: 1.05x faster                                        |
| meteor_contest             | 133 ms                                                                 | 126 ms: 1.05x faster                                        |
| crypto_pyaes               | 87.8 ms                                                                | 83.4 ms: 1.05x faster                                       |
| spectral_norm              | 112 ms                                                                 | 107 ms: 1.05x faster                                        |
| deepcopy_reduce            | 3.24 us                                                                | 3.09 us: 1.05x faster                                       |
| pprint_pformat             | 1.73 sec                                                               | 1.65 sec: 1.05x faster                                      |
| regex_v8                   | 22.0 ms                                                                | 21.0 ms: 1.05x faster                                       |
| 2to3                       | 301 ms                                                                 | 288 ms: 1.05x faster                                        |
| hexiom                     | 7.60 ms                                                                | 7.27 ms: 1.04x faster                                       |
| deepcopy                   | 312 us                                                                 | 299 us: 1.04x faster                                        |
| many_optionals             | 1.19 ms                                                                | 1.14 ms: 1.04x faster                                       |
| logging_format             | 8.33 us                                                                | 7.99 us: 1.04x faster                                       |
| scimark_lu                 | 140 ms                                                                 | 135 ms: 1.04x faster                                        |
| tomli_loads                | 2.35 sec                                                               | 2.26 sec: 1.04x faster                                      |
| logging_simple             | 7.30 us                                                                | 7.02 us: 1.04x faster                                       |
| regex_compile              | 157 ms                                                                 | 151 ms: 1.04x faster                                        |
| connected_components       | 503 ms                                                                 | 486 ms: 1.04x faster                                        |
| django_template            | 42.7 ms                                                                | 41.4 ms: 1.03x faster                                       |
| genshi_xml                 | 59.7 ms                                                                | 57.9 ms: 1.03x faster                                       |
| k_core                     | 2.31 sec                                                               | 2.25 sec: 1.03x faster                                      |
| sympy_integrate            | 24.3 ms                                                                | 23.6 ms: 1.03x faster                                       |
| sqlglot_v2_optimize        | 61.0 ms                                                                | 59.4 ms: 1.03x faster                                       |
| mdp                        | 2.79 sec                                                               | 2.73 sec: 1.02x faster                                      |
| create_gc_cycles           | 1.39 ms                                                                | 1.35 ms: 1.02x faster                                       |
| sqlglot_v2_normalize       | 121 ms                                                                 | 118 ms: 1.02x faster                                        |
| pathlib                    | 20.0 ms                                                                | 19.6 ms: 1.02x faster                                       |
| sphinx                     | 1.10 sec                                                               | 1.08 sec: 1.02x faster                                      |
| subparsers                 | 25.5 ms                                                                | 24.9 ms: 1.02x faster                                       |
| coverage                   | 97.6 ms                                                                | 95.7 ms: 1.02x faster                                       |
| shortest_path              | 544 ms                                                                 | 533 ms: 1.02x faster                                        |
| sympy_str                  | 338 ms                                                                 | 332 ms: 1.02x faster                                        |
| xml_etree_process          | 69.9 ms                                                                | 68.7 ms: 1.02x faster                                       |
| typing_runtime_protocols   | 197 us                                                                 | 194 us: 1.02x faster                                        |
| sympy_expand               | 554 ms                                                                 | 546 ms: 1.02x faster                                        |
| sqlite_synth               | 2.04 us                                                                | 2.02 us: 1.01x faster                                       |
| sympy_sum                  | 188 ms                                                                 | 185 ms: 1.01x faster                                        |
| telco                      | 8.80 ms                                                                | 8.68 ms: 1.01x faster                                       |
| docutils                   | 2.79 sec                                                               | 2.75 sec: 1.01x faster                                      |
| gc_traversal               | 1.82 ms                                                                | 1.79 ms: 1.01x faster                                       |
| bench_thread_pool          | 3.17 ms                                                                | 3.13 ms: 1.01x faster                                       |
| async_generators           | 376 ms                                                                 | 372 ms: 1.01x faster                                        |
| generators                 | 32.5 ms                                                                | 32.2 ms: 1.01x faster                                       |
| json_loads                 | 29.8 us                                                                | 29.5 us: 1.01x faster                                       |
| bench_mp_pool              | 97.4 ms                                                                | 96.7 ms: 1.01x faster                                       |
| dulwich_log                | 73.5 ms                                                                | 73.1 ms: 1.01x faster                                       |
| json_dumps                 | 12.9 ms                                                                | 12.8 ms: 1.01x faster                                       |
| python_startup_no_site     | 11.2 ms                                                                | 11.1 ms: 1.01x faster                                       |
| python_startup             | 15.8 ms                                                                | 15.7 ms: 1.01x faster                                       |
| sqlalchemy_declarative     | 158 ms                                                                 | 158 ms: 1.00x faster                                        |
| mako                       | 15.5 ms                                                                | 15.6 ms: 1.00x slower                                       |
| asyncio_websockets         | 513 ms                                                                 | 518 ms: 1.01x slower                                        |
| async_tree_cpu_io_mixed_tg | 512 ms                                                                 | 555 ms: 1.08x slower                                        |
| async_tree_cpu_io_mixed    | 541 ms                                                                 | 587 ms: 1.08x slower                                        |
| pidigits                   | 198 ms                                                                 | 228 ms: 1.15x slower                                        |
| Geometric mean             | (ref)                                                                  | 1.04x faster                                                |

Benchmark hidden because not significant (7): pylint, json, coroutines, sqlalchemy_imperative, xml_etree_generate, xml_etree_parse, xml_etree_iterparse

- Geometric mean (including insignificant results): 1.043x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.01x