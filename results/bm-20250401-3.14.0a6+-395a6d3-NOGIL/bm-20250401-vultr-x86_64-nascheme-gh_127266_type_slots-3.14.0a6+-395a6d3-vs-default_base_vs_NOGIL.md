# Results vs. default_base_vs_NOGIL

- fork: nascheme
- ref: gh_127266_type_slots
- machine: linux-x86_64
- commit hash: 395a6d3
- commit date: 2025-04-01
- overall geometric mean: 1.177x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.17x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250401-vultr-x86_64-python-fe5c4c53e7bc6d780686-3.14.0a6+-fe5c4c5 | bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-395a6d3 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 249 ms                                                                 | 314 ms: 1.26x slower                                                     |
| docutils       | 2.53 sec                                                               | 2.90 sec: 1.15x slower                                                   |
| sphinx         | 979 ms                                                                 | 1.15 sec: 1.18x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.19x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250401-vultr-x86_64-python-fe5c4c53e7bc6d780686-3.14.0a6+-fe5c4c5 | bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-395a6d3 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 620 ms                                                                 | 574 ms: 1.08x faster                                                     |
| async_tree_cpu_io_mixed_tg | 495 ms                                                                 | 491 ms: 1.01x faster                                                     |
| async_tree_memoization_tg  | 310 ms                                                                 | 316 ms: 1.02x slower                                                     |
| async_tree_cpu_io_mixed    | 502 ms                                                                 | 521 ms: 1.04x slower                                                     |
| async_tree_none            | 271 ms                                                                 | 288 ms: 1.06x slower                                                     |
| coroutines                 | 22.9 ms                                                                | 25.1 ms: 1.10x slower                                                    |
| async_tree_memoization     | 309 ms                                                                 | 344 ms: 1.11x slower                                                     |
| async_generators           | 326 ms                                                                 | 388 ms: 1.19x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.04x slower                                                             |

Benchmark hidden because not significant (3): async_tree_none_tg, asyncio_websockets, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250401-vultr-x86_64-python-fe5c4c53e7bc6d780686-3.14.0a6+-fe5c4c5 | bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-395a6d3 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 213 ms                                                                 | 195 ms: 1.09x faster                                                     |
| float          | 70.7 ms                                                                | 81.3 ms: 1.15x slower                                                    |
| nbody          | 94.1 ms                                                                | 148 ms: 1.58x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.18x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250401-vultr-x86_64-python-fe5c4c53e7bc6d780686-3.14.0a6+-fe5c4c5 | bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-395a6d3 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_dna      | 181 ms                                                                 | 173 ms: 1.05x faster                                                     |
| regex_effbot   | 2.86 ms                                                                | 2.77 ms: 1.03x faster                                                    |
| regex_v8       | 21.6 ms                                                                | 21.8 ms: 1.01x slower                                                    |
| regex_compile  | 124 ms                                                                 | 170 ms: 1.37x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.06x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250401-vultr-x86_64-python-fe5c4c53e7bc6d780686-3.14.0a6+-fe5c4c5 | bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-395a6d3 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_parse      | 129 ms                                                                 | 130 ms: 1.01x slower                                                     |
| xml_etree_iterparse  | 92.0 ms                                                                | 93.6 ms: 1.02x slower                                                    |
| json_loads           | 27.8 us                                                                | 30.7 us: 1.11x slower                                                    |
| json_dumps           | 11.2 ms                                                                | 13.1 ms: 1.17x slower                                                    |
| xml_etree_generate   | 83.3 ms                                                                | 102 ms: 1.23x slower                                                     |
| pickle_pure_python   | 306 us                                                                 | 393 us: 1.29x slower                                                     |
| xml_etree_process    | 58.0 ms                                                                | 74.6 ms: 1.29x slower                                                    |
| unpickle_pure_python | 212 us                                                                 | 279 us: 1.31x slower                                                     |
| tomli_loads          | 1.91 sec                                                               | 2.56 sec: 1.34x slower                                                   |
| Geometric mean       | (ref)                                                                  | 1.19x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250401-vultr-x86_64-python-fe5c4c53e7bc6d780686-3.14.0a6+-fe5c4c5 | bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-395a6d3 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 15.0 ms                                                                | 15.8 ms: 1.06x slower                                                    |
| python_startup_no_site | 8.64 ms                                                                | 11.1 ms: 1.29x slower                                                    |
| Geometric mean         | (ref)                                                                  | 1.17x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250401-vultr-x86_64-python-fe5c4c53e7bc6d780686-3.14.0a6+-fe5c4c5 | bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-395a6d3 |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| django_template | 34.6 ms                                                                | 45.1 ms: 1.31x slower                                                    |
| mako            | 11.9 ms                                                                | 16.5 ms: 1.38x slower                                                    |
| genshi_xml      | 47.4 ms                                                                | 66.4 ms: 1.40x slower                                                    |
| genshi_text     | 20.5 ms                                                                | 31.0 ms: 1.51x slower                                                    |
| Geometric mean  | (ref)                                                                  | 1.40x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20250401-vultr-x86_64-python-fe5c4c53e7bc6d780686-3.14.0a6+-fe5c4c5 | bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-395a6d3 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal               | 4.36 ms                                                                | 1.80 ms: 2.43x faster                                                    |
| create_gc_cycles           | 1.87 ms                                                                | 1.36 ms: 1.37x faster                                                    |
| pidigits                   | 213 ms                                                                 | 195 ms: 1.09x faster                                                     |
| async_tree_io_tg           | 620 ms                                                                 | 574 ms: 1.08x faster                                                     |
| regex_dna                  | 181 ms                                                                 | 173 ms: 1.05x faster                                                     |
| sqlite_synth               | 2.16 us                                                                | 2.08 us: 1.04x faster                                                    |
| regex_effbot               | 2.86 ms                                                                | 2.77 ms: 1.03x faster                                                    |
| async_tree_cpu_io_mixed_tg | 495 ms                                                                 | 491 ms: 1.01x faster                                                     |
| regex_v8                   | 21.6 ms                                                                | 21.8 ms: 1.01x slower                                                    |
| xml_etree_parse            | 129 ms                                                                 | 130 ms: 1.01x slower                                                     |
| xml_etree_iterparse        | 92.0 ms                                                                | 93.6 ms: 1.02x slower                                                    |
| async_tree_memoization_tg  | 310 ms                                                                 | 316 ms: 1.02x slower                                                     |
| pathlib                    | 19.0 ms                                                                | 19.7 ms: 1.04x slower                                                    |
| async_tree_cpu_io_mixed    | 502 ms                                                                 | 521 ms: 1.04x slower                                                     |
| python_startup             | 15.0 ms                                                                | 15.8 ms: 1.06x slower                                                    |
| async_tree_none            | 271 ms                                                                 | 288 ms: 1.06x slower                                                     |
| json                       | 4.95 ms                                                                | 5.34 ms: 1.08x slower                                                    |
| coroutines                 | 22.9 ms                                                                | 25.1 ms: 1.10x slower                                                    |
| bench_mp_pool              | 89.0 ms                                                                | 97.9 ms: 1.10x slower                                                    |
| json_loads                 | 27.8 us                                                                | 30.7 us: 1.11x slower                                                    |
| async_tree_memoization     | 309 ms                                                                 | 344 ms: 1.11x slower                                                     |
| k_core                     | 2.04 sec                                                               | 2.32 sec: 1.14x slower                                                   |
| docutils                   | 2.53 sec                                                               | 2.90 sec: 1.15x slower                                                   |
| pycparser                  | 1.10 sec                                                               | 1.27 sec: 1.15x slower                                                   |
| float                      | 70.7 ms                                                                | 81.3 ms: 1.15x slower                                                    |
| json_dumps                 | 11.2 ms                                                                | 13.1 ms: 1.17x slower                                                    |
| dulwich_log                | 65.9 ms                                                                | 77.3 ms: 1.17x slower                                                    |
| sphinx                     | 979 ms                                                                 | 1.15 sec: 1.18x slower                                                   |
| pylint                     | 277 ms                                                                 | 327 ms: 1.18x slower                                                     |
| bpe_tokeniser              | 4.23 sec                                                               | 5.03 sec: 1.19x slower                                                   |
| async_generators           | 326 ms                                                                 | 388 ms: 1.19x slower                                                     |
| many_optionals             | 1.03 ms                                                                | 1.23 ms: 1.20x slower                                                    |
| telco                      | 7.43 ms                                                                | 8.97 ms: 1.21x slower                                                    |
| xml_etree_generate         | 83.3 ms                                                                | 102 ms: 1.23x slower                                                     |
| subparsers                 | 22.0 ms                                                                | 27.1 ms: 1.23x slower                                                    |
| pprint_safe_repr           | 712 ms                                                                 | 896 ms: 1.26x slower                                                     |
| 2to3                       | 249 ms                                                                 | 314 ms: 1.26x slower                                                     |
| sympy_sum                  | 155 ms                                                                 | 195 ms: 1.26x slower                                                     |
| mdp                        | 1.16 sec                                                               | 1.47 sec: 1.26x slower                                                   |
| shortest_path              | 440 ms                                                                 | 556 ms: 1.26x slower                                                     |
| deepcopy_reduce            | 2.66 us                                                                | 3.37 us: 1.27x slower                                                    |
| sqlglot_v2_optimize        | 51.7 ms                                                                | 65.8 ms: 1.27x slower                                                    |
| sqlalchemy_declarative     | 128 ms                                                                 | 162 ms: 1.27x slower                                                     |
| pprint_pformat             | 1.45 sec                                                               | 1.86 sec: 1.28x slower                                                   |
| scimark_fft                | 321 ms                                                                 | 411 ms: 1.28x slower                                                     |
| sqlalchemy_imperative      | 19.4 ms                                                                | 24.9 ms: 1.28x slower                                                    |
| sqlglot_v2_normalize       | 102 ms                                                                 | 131 ms: 1.29x slower                                                     |
| pickle_pure_python         | 306 us                                                                 | 393 us: 1.29x slower                                                     |
| python_startup_no_site     | 8.64 ms                                                                | 11.1 ms: 1.29x slower                                                    |
| xml_etree_process          | 58.0 ms                                                                | 74.6 ms: 1.29x slower                                                    |
| sympy_integrate            | 19.0 ms                                                                | 24.5 ms: 1.29x slower                                                    |
| spectral_norm              | 92.8 ms                                                                | 120 ms: 1.29x slower                                                     |
| connected_components       | 396 ms                                                                 | 511 ms: 1.29x slower                                                     |
| sympy_expand               | 458 ms                                                                 | 595 ms: 1.30x slower                                                     |
| django_template            | 34.6 ms                                                                | 45.1 ms: 1.31x slower                                                    |
| sympy_str                  | 271 ms                                                                 | 355 ms: 1.31x slower                                                     |
| unpickle_pure_python       | 212 us                                                                 | 279 us: 1.31x slower                                                     |
| pyflate                    | 410 ms                                                                 | 541 ms: 1.32x slower                                                     |
| deepcopy                   | 256 us                                                                 | 338 us: 1.32x slower                                                     |
| typing_runtime_protocols   | 156 us                                                                 | 208 us: 1.34x slower                                                     |
| nqueens                    | 76.7 ms                                                                | 103 ms: 1.34x slower                                                     |
| tomli_loads                | 1.91 sec                                                               | 2.56 sec: 1.34x slower                                                   |
| logging_silent             | 93.6 ns                                                                | 126 ns: 1.35x slower                                                     |
| scimark_lu                 | 113 ms                                                                 | 153 ms: 1.35x slower                                                     |
| chaos                      | 55.4 ms                                                                | 75.2 ms: 1.36x slower                                                    |
| sqlglot_v2_transpile       | 1.53 ms                                                                | 2.08 ms: 1.36x slower                                                    |
| comprehensions             | 16.4 us                                                                | 22.4 us: 1.37x slower                                                    |
| regex_compile              | 124 ms                                                                 | 170 ms: 1.37x slower                                                     |
| meteor_contest             | 100 ms                                                                 | 138 ms: 1.37x slower                                                     |
| coverage                   | 79.9 ms                                                                | 110 ms: 1.38x slower                                                     |
| raytrace                   | 256 ms                                                                 | 353 ms: 1.38x slower                                                     |
| crypto_pyaes               | 68.1 ms                                                                | 94.3 ms: 1.38x slower                                                    |
| fannkuch                   | 387 ms                                                                 | 536 ms: 1.38x slower                                                     |
| mako                       | 11.9 ms                                                                | 16.5 ms: 1.38x slower                                                    |
| scimark_sparse_mat_mult    | 4.39 ms                                                                | 6.10 ms: 1.39x slower                                                    |
| sqlglot_v2_parse           | 1.23 ms                                                                | 1.71 ms: 1.39x slower                                                    |
| logging_simple             | 5.96 us                                                                | 8.30 us: 1.39x slower                                                    |
| genshi_xml                 | 47.4 ms                                                                | 66.4 ms: 1.40x slower                                                    |
| hexiom                     | 5.77 ms                                                                | 8.14 ms: 1.41x slower                                                    |
| logging_format             | 6.66 us                                                                | 9.41 us: 1.41x slower                                                    |
| scimark_monte_carlo        | 63.4 ms                                                                | 90.9 ms: 1.43x slower                                                    |
| generators                 | 26.6 ms                                                                | 38.4 ms: 1.44x slower                                                    |
| deepcopy_memo              | 29.6 us                                                                | 42.7 us: 1.44x slower                                                    |
| go                         | 109 ms                                                                 | 157 ms: 1.44x slower                                                     |
| richards_super             | 47.2 ms                                                                | 68.9 ms: 1.46x slower                                                    |
| scimark_sor                | 113 ms                                                                 | 165 ms: 1.47x slower                                                     |
| richards                   | 41.1 ms                                                                | 61.0 ms: 1.48x slower                                                    |
| genshi_text                | 20.5 ms                                                                | 31.0 ms: 1.51x slower                                                    |
| deltablue                  | 2.99 ms                                                                | 4.55 ms: 1.52x slower                                                    |
| nbody                      | 94.1 ms                                                                | 148 ms: 1.58x slower                                                     |
| bench_thread_pool          | 1.04 ms                                                                | 3.20 ms: 3.08x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.23x slower                                                             |

Benchmark hidden because not significant (3): async_tree_none_tg, asyncio_websockets, async_tree_io
Ignored benchmarks (1) of results/bm-20250401-3.14.0a6+-395a6d3-NOGIL/bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-395a6d3.json: html5lib

- Geometric mean (including insignificant results): 1.177x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.19x
- 95% likely to have a slowdown of 1.18x
- 99% likely to have a slowdown of 1.17x

# Memory
- memory change: 1.19x