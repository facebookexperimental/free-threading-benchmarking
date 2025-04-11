# Results vs. default_base_vs_NOGIL

- fork: nascheme
- ref: gh_127266_type_slots
- machine: linux-x86_64
- commit hash: 57c2a44
- commit date: 2025-04-10
- overall geometric mean: 1.183x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.18x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250401-vultr-x86_64-python-fe5c4c53e7bc6d780686-3.14.0a6+-fe5c4c5 | bm-20250410-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-57c2a44 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 249 ms                                                                 | 316 ms: 1.27x slower                                                     |
| docutils       | 2.53 sec                                                               | 2.91 sec: 1.15x slower                                                   |
| sphinx         | 979 ms                                                                 | 1.15 sec: 1.18x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.20x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250401-vultr-x86_64-python-fe5c4c53e7bc6d780686-3.14.0a6+-fe5c4c5 | bm-20250410-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-57c2a44 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 620 ms                                                                 | 580 ms: 1.07x faster                                                     |
| async_tree_none_tg         | 252 ms                                                                 | 255 ms: 1.01x slower                                                     |
| async_tree_io              | 603 ms                                                                 | 613 ms: 1.02x slower                                                     |
| async_tree_memoization_tg  | 310 ms                                                                 | 320 ms: 1.03x slower                                                     |
| async_tree_cpu_io_mixed_tg | 495 ms                                                                 | 520 ms: 1.05x slower                                                     |
| async_tree_none            | 271 ms                                                                 | 290 ms: 1.07x slower                                                     |
| async_tree_cpu_io_mixed    | 502 ms                                                                 | 551 ms: 1.10x slower                                                     |
| coroutines                 | 22.9 ms                                                                | 25.6 ms: 1.12x slower                                                    |
| async_tree_memoization     | 309 ms                                                                 | 349 ms: 1.13x slower                                                     |
| async_generators           | 326 ms                                                                 | 389 ms: 1.20x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.06x slower                                                             |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250401-vultr-x86_64-python-fe5c4c53e7bc6d780686-3.14.0a6+-fe5c4c5 | bm-20250410-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-57c2a44 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 213 ms                                                                 | 202 ms: 1.05x faster                                                     |
| float          | 70.7 ms                                                                | 84.0 ms: 1.19x slower                                                    |
| nbody          | 94.1 ms                                                                | 152 ms: 1.61x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.22x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250401-vultr-x86_64-python-fe5c4c53e7bc6d780686-3.14.0a6+-fe5c4c5 | bm-20250410-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-57c2a44 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 2.86 ms                                                                | 2.77 ms: 1.03x faster                                                    |
| regex_v8       | 21.6 ms                                                                | 21.1 ms: 1.03x faster                                                    |
| regex_compile  | 124 ms                                                                 | 173 ms: 1.39x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.07x slower                                                             |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250401-vultr-x86_64-python-fe5c4c53e7bc6d780686-3.14.0a6+-fe5c4c5 | bm-20250410-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-57c2a44 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_parse      | 129 ms                                                                 | 130 ms: 1.01x slower                                                     |
| xml_etree_iterparse  | 92.0 ms                                                                | 92.9 ms: 1.01x slower                                                    |
| json_loads           | 27.8 us                                                                | 30.9 us: 1.11x slower                                                    |
| json_dumps           | 11.2 ms                                                                | 13.1 ms: 1.17x slower                                                    |
| xml_etree_generate   | 83.3 ms                                                                | 102 ms: 1.22x slower                                                     |
| xml_etree_process    | 58.0 ms                                                                | 74.4 ms: 1.28x slower                                                    |
| pickle_pure_python   | 306 us                                                                 | 399 us: 1.31x slower                                                     |
| unpickle_pure_python | 212 us                                                                 | 282 us: 1.33x slower                                                     |
| tomli_loads          | 1.91 sec                                                               | 2.62 sec: 1.37x slower                                                   |
| Geometric mean       | (ref)                                                                  | 1.19x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250401-vultr-x86_64-python-fe5c4c53e7bc6d780686-3.14.0a6+-fe5c4c5 | bm-20250410-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-57c2a44 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 15.0 ms                                                                | 15.9 ms: 1.06x slower                                                    |
| python_startup_no_site | 8.64 ms                                                                | 11.2 ms: 1.29x slower                                                    |
| Geometric mean         | (ref)                                                                  | 1.17x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250401-vultr-x86_64-python-fe5c4c53e7bc6d780686-3.14.0a6+-fe5c4c5 | bm-20250410-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-57c2a44 |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| django_template | 34.6 ms                                                                | 45.4 ms: 1.31x slower                                                    |
| mako            | 11.9 ms                                                                | 16.6 ms: 1.40x slower                                                    |
| genshi_xml      | 47.4 ms                                                                | 67.4 ms: 1.42x slower                                                    |
| genshi_text     | 20.5 ms                                                                | 31.6 ms: 1.54x slower                                                    |
| Geometric mean  | (ref)                                                                  | 1.42x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20250401-vultr-x86_64-python-fe5c4c53e7bc6d780686-3.14.0a6+-fe5c4c5 | bm-20250410-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-57c2a44 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal               | 4.36 ms                                                                | 1.81 ms: 2.41x faster                                                    |
| create_gc_cycles           | 1.87 ms                                                                | 1.39 ms: 1.35x faster                                                    |
| async_tree_io_tg           | 620 ms                                                                 | 580 ms: 1.07x faster                                                     |
| pidigits                   | 213 ms                                                                 | 202 ms: 1.05x faster                                                     |
| sqlite_synth               | 2.16 us                                                                | 2.07 us: 1.05x faster                                                    |
| regex_effbot               | 2.86 ms                                                                | 2.77 ms: 1.03x faster                                                    |
| regex_v8                   | 21.6 ms                                                                | 21.1 ms: 1.03x faster                                                    |
| xml_etree_parse            | 129 ms                                                                 | 130 ms: 1.01x slower                                                     |
| xml_etree_iterparse        | 92.0 ms                                                                | 92.9 ms: 1.01x slower                                                    |
| async_tree_none_tg         | 252 ms                                                                 | 255 ms: 1.01x slower                                                     |
| async_tree_io              | 603 ms                                                                 | 613 ms: 1.02x slower                                                     |
| async_tree_memoization_tg  | 310 ms                                                                 | 320 ms: 1.03x slower                                                     |
| pathlib                    | 19.0 ms                                                                | 19.8 ms: 1.04x slower                                                    |
| async_tree_cpu_io_mixed_tg | 495 ms                                                                 | 520 ms: 1.05x slower                                                     |
| python_startup             | 15.0 ms                                                                | 15.9 ms: 1.06x slower                                                    |
| async_tree_none            | 271 ms                                                                 | 290 ms: 1.07x slower                                                     |
| json                       | 4.95 ms                                                                | 5.32 ms: 1.07x slower                                                    |
| async_tree_cpu_io_mixed    | 502 ms                                                                 | 551 ms: 1.10x slower                                                     |
| bench_mp_pool              | 89.0 ms                                                                | 98.6 ms: 1.11x slower                                                    |
| json_loads                 | 27.8 us                                                                | 30.9 us: 1.11x slower                                                    |
| coroutines                 | 22.9 ms                                                                | 25.6 ms: 1.12x slower                                                    |
| async_tree_memoization     | 309 ms                                                                 | 349 ms: 1.13x slower                                                     |
| k_core                     | 2.04 sec                                                               | 2.32 sec: 1.14x slower                                                   |
| pycparser                  | 1.10 sec                                                               | 1.26 sec: 1.15x slower                                                   |
| docutils                   | 2.53 sec                                                               | 2.91 sec: 1.15x slower                                                   |
| json_dumps                 | 11.2 ms                                                                | 13.1 ms: 1.17x slower                                                    |
| sphinx                     | 979 ms                                                                 | 1.15 sec: 1.18x slower                                                   |
| dulwich_log                | 65.9 ms                                                                | 77.7 ms: 1.18x slower                                                    |
| pylint                     | 277 ms                                                                 | 328 ms: 1.18x slower                                                     |
| bpe_tokeniser              | 4.23 sec                                                               | 5.02 sec: 1.19x slower                                                   |
| float                      | 70.7 ms                                                                | 84.0 ms: 1.19x slower                                                    |
| async_generators           | 326 ms                                                                 | 389 ms: 1.20x slower                                                     |
| many_optionals             | 1.03 ms                                                                | 1.23 ms: 1.20x slower                                                    |
| telco                      | 7.43 ms                                                                | 9.00 ms: 1.21x slower                                                    |
| xml_etree_generate         | 83.3 ms                                                                | 102 ms: 1.22x slower                                                     |
| subparsers                 | 22.0 ms                                                                | 27.1 ms: 1.23x slower                                                    |
| mdp                        | 1.16 sec                                                               | 1.46 sec: 1.26x slower                                                   |
| sympy_sum                  | 155 ms                                                                 | 196 ms: 1.26x slower                                                     |
| pprint_safe_repr           | 712 ms                                                                 | 901 ms: 1.27x slower                                                     |
| sqlglot_v2_optimize        | 51.7 ms                                                                | 65.6 ms: 1.27x slower                                                    |
| shortest_path              | 440 ms                                                                 | 558 ms: 1.27x slower                                                     |
| 2to3                       | 249 ms                                                                 | 316 ms: 1.27x slower                                                     |
| sqlalchemy_declarative     | 128 ms                                                                 | 163 ms: 1.28x slower                                                     |
| sqlglot_v2_normalize       | 102 ms                                                                 | 131 ms: 1.28x slower                                                     |
| scimark_fft                | 321 ms                                                                 | 412 ms: 1.28x slower                                                     |
| xml_etree_process          | 58.0 ms                                                                | 74.4 ms: 1.28x slower                                                    |
| sqlalchemy_imperative      | 19.4 ms                                                                | 25.0 ms: 1.29x slower                                                    |
| sympy_expand               | 458 ms                                                                 | 590 ms: 1.29x slower                                                     |
| pprint_pformat             | 1.45 sec                                                               | 1.87 sec: 1.29x slower                                                   |
| sympy_integrate            | 19.0 ms                                                                | 24.6 ms: 1.29x slower                                                    |
| python_startup_no_site     | 8.64 ms                                                                | 11.2 ms: 1.29x slower                                                    |
| deepcopy_reduce            | 2.66 us                                                                | 3.45 us: 1.30x slower                                                    |
| connected_components       | 396 ms                                                                 | 515 ms: 1.30x slower                                                     |
| sympy_str                  | 271 ms                                                                 | 352 ms: 1.30x slower                                                     |
| pickle_pure_python         | 306 us                                                                 | 399 us: 1.31x slower                                                     |
| spectral_norm              | 92.8 ms                                                                | 122 ms: 1.31x slower                                                     |
| django_template            | 34.6 ms                                                                | 45.4 ms: 1.31x slower                                                    |
| deepcopy                   | 256 us                                                                 | 339 us: 1.32x slower                                                     |
| typing_runtime_protocols   | 156 us                                                                 | 206 us: 1.32x slower                                                     |
| nqueens                    | 76.7 ms                                                                | 102 ms: 1.33x slower                                                     |
| unpickle_pure_python       | 212 us                                                                 | 282 us: 1.33x slower                                                     |
| pyflate                    | 410 ms                                                                 | 553 ms: 1.35x slower                                                     |
| scimark_lu                 | 113 ms                                                                 | 153 ms: 1.36x slower                                                     |
| comprehensions             | 16.4 us                                                                | 22.5 us: 1.37x slower                                                    |
| tomli_loads                | 1.91 sec                                                               | 2.62 sec: 1.37x slower                                                   |
| scimark_sparse_mat_mult    | 4.39 ms                                                                | 6.04 ms: 1.38x slower                                                    |
| crypto_pyaes               | 68.1 ms                                                                | 94.0 ms: 1.38x slower                                                    |
| sqlglot_v2_transpile       | 1.53 ms                                                                | 2.11 ms: 1.38x slower                                                    |
| coverage                   | 79.9 ms                                                                | 111 ms: 1.38x slower                                                     |
| regex_compile              | 124 ms                                                                 | 173 ms: 1.39x slower                                                     |
| raytrace                   | 256 ms                                                                 | 356 ms: 1.39x slower                                                     |
| chaos                      | 55.4 ms                                                                | 77.2 ms: 1.39x slower                                                    |
| meteor_contest             | 100 ms                                                                 | 140 ms: 1.40x slower                                                     |
| mako                       | 11.9 ms                                                                | 16.6 ms: 1.40x slower                                                    |
| fannkuch                   | 387 ms                                                                 | 542 ms: 1.40x slower                                                     |
| logging_silent             | 93.6 ns                                                                | 131 ns: 1.40x slower                                                     |
| logging_simple             | 5.96 us                                                                | 8.40 us: 1.41x slower                                                    |
| logging_format             | 6.66 us                                                                | 9.47 us: 1.42x slower                                                    |
| genshi_xml                 | 47.4 ms                                                                | 67.4 ms: 1.42x slower                                                    |
| sqlglot_v2_parse           | 1.23 ms                                                                | 1.75 ms: 1.43x slower                                                    |
| hexiom                     | 5.77 ms                                                                | 8.25 ms: 1.43x slower                                                    |
| scimark_monte_carlo        | 63.4 ms                                                                | 91.3 ms: 1.44x slower                                                    |
| generators                 | 26.6 ms                                                                | 38.4 ms: 1.44x slower                                                    |
| deepcopy_memo              | 29.6 us                                                                | 42.8 us: 1.45x slower                                                    |
| scimark_sor                | 113 ms                                                                 | 165 ms: 1.46x slower                                                     |
| go                         | 109 ms                                                                 | 161 ms: 1.48x slower                                                     |
| richards_super             | 47.2 ms                                                                | 70.1 ms: 1.49x slower                                                    |
| richards                   | 41.1 ms                                                                | 62.1 ms: 1.51x slower                                                    |
| genshi_text                | 20.5 ms                                                                | 31.6 ms: 1.54x slower                                                    |
| deltablue                  | 2.99 ms                                                                | 4.64 ms: 1.55x slower                                                    |
| nbody                      | 94.1 ms                                                                | 152 ms: 1.61x slower                                                     |
| bench_thread_pool          | 1.04 ms                                                                | 3.20 ms: 3.08x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.24x slower                                                             |

Benchmark hidden because not significant (2): asyncio_websockets, regex_dna
Ignored benchmarks (1) of results/bm-20250410-3.14.0a6+-57c2a44-NOGIL/bm-20250410-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-57c2a44.json: html5lib

- Geometric mean (including insignificant results): 1.183x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.20x
- 95% likely to have a slowdown of 1.19x
- 99% likely to have a slowdown of 1.18x

# Memory
- memory change: 1.20x