# Results vs. default_base_vs_NOGIL

- fork: mpage
- ref: gh_129987_no_slp_vec
- machine: linux-x86_64
- commit hash: 45cd786
- commit date: 2025-04-08
- overall geometric mean: 1.074x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-45cd786 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 255 ms                                                                 | 287 ms: 1.13x slower                                                  |
| docutils       | 2.60 sec                                                               | 2.75 sec: 1.06x slower                                                |
| sphinx         | 1.00 sec                                                               | 1.09 sec: 1.08x slower                                                |
| Geometric mean | (ref)                                                                  | 1.09x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-45cd786 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 626 ms                                                                 | 535 ms: 1.17x faster                                                  |
| async_tree_none_tg         | 263 ms                                                                 | 232 ms: 1.13x faster                                                  |
| async_tree_io              | 628 ms                                                                 | 556 ms: 1.13x faster                                                  |
| async_tree_memoization_tg  | 325 ms                                                                 | 292 ms: 1.11x faster                                                  |
| coroutines                 | 24.6 ms                                                                | 23.2 ms: 1.06x faster                                                 |
| async_tree_none            | 278 ms                                                                 | 265 ms: 1.05x faster                                                  |
| async_tree_cpu_io_mixed_tg | 503 ms                                                                 | 479 ms: 1.05x faster                                                  |
| asyncio_websockets         | 518 ms                                                                 | 516 ms: 1.00x faster                                                  |
| async_tree_memoization     | 318 ms                                                                 | 321 ms: 1.01x slower                                                  |
| async_generators           | 336 ms                                                                 | 367 ms: 1.09x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.05x faster                                                          |

Benchmark hidden because not significant (1): async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-45cd786 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 72.3 ms                                                                | 70.5 ms: 1.03x faster                                                 |
| pidigits       | 192 ms                                                                 | 200 ms: 1.04x slower                                                  |
| nbody          | 94.9 ms                                                                | 118 ms: 1.24x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.08x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-45cd786 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 21.8 ms                                                                | 21.4 ms: 1.02x faster                                                 |
| regex_dna      | 171 ms                                                                 | 179 ms: 1.04x slower                                                  |
| regex_effbot   | 2.70 ms                                                                | 2.93 ms: 1.08x slower                                                 |
| regex_compile  | 130 ms                                                                 | 151 ms: 1.16x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.06x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-45cd786 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 93.0 ms                                                                | 86.3 ms: 1.08x faster                                                 |
| xml_etree_parse      | 129 ms                                                                 | 128 ms: 1.01x faster                                                  |
| json_loads           | 28.8 us                                                                | 30.5 us: 1.06x slower                                                 |
| unpickle_pure_python | 222 us                                                                 | 238 us: 1.07x slower                                                  |
| pickle_pure_python   | 318 us                                                                 | 344 us: 1.08x slower                                                  |
| tomli_loads          | 2.01 sec                                                               | 2.21 sec: 1.10x slower                                                |
| xml_etree_generate   | 85.7 ms                                                                | 94.8 ms: 1.11x slower                                                 |
| xml_etree_process    | 61.4 ms                                                                | 68.3 ms: 1.11x slower                                                 |
| json_dumps           | 11.3 ms                                                                | 12.6 ms: 1.11x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.06x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-45cd786 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 15.2 ms                                                                | 15.9 ms: 1.05x slower                                                 |
| python_startup_no_site | 8.68 ms                                                                | 11.2 ms: 1.29x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.16x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-45cd786 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 36.7 ms                                                                | 40.8 ms: 1.11x slower                                                 |
| genshi_xml      | 50.6 ms                                                                | 57.9 ms: 1.14x slower                                                 |
| genshi_text     | 22.0 ms                                                                | 27.0 ms: 1.23x slower                                                 |
| mako            | 12.3 ms                                                                | 15.4 ms: 1.25x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.18x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-45cd786 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal               | 4.34 ms                                                                | 1.77 ms: 2.44x faster                                                 |
| create_gc_cycles           | 1.86 ms                                                                | 1.33 ms: 1.40x faster                                                 |
| async_tree_io_tg           | 626 ms                                                                 | 535 ms: 1.17x faster                                                  |
| async_tree_none_tg         | 263 ms                                                                 | 232 ms: 1.13x faster                                                  |
| async_tree_io              | 628 ms                                                                 | 556 ms: 1.13x faster                                                  |
| async_tree_memoization_tg  | 325 ms                                                                 | 292 ms: 1.11x faster                                                  |
| sqlite_synth               | 2.23 us                                                                | 2.01 us: 1.11x faster                                                 |
| xml_etree_iterparse        | 93.0 ms                                                                | 86.3 ms: 1.08x faster                                                 |
| coroutines                 | 24.6 ms                                                                | 23.2 ms: 1.06x faster                                                 |
| async_tree_none            | 278 ms                                                                 | 265 ms: 1.05x faster                                                  |
| async_tree_cpu_io_mixed_tg | 503 ms                                                                 | 479 ms: 1.05x faster                                                  |
| float                      | 72.3 ms                                                                | 70.5 ms: 1.03x faster                                                 |
| regex_v8                   | 21.8 ms                                                                | 21.4 ms: 1.02x faster                                                 |
| xml_etree_parse            | 129 ms                                                                 | 128 ms: 1.01x faster                                                  |
| asyncio_websockets         | 518 ms                                                                 | 516 ms: 1.00x faster                                                  |
| async_tree_memoization     | 318 ms                                                                 | 321 ms: 1.01x slower                                                  |
| pidigits                   | 192 ms                                                                 | 200 ms: 1.04x slower                                                  |
| regex_dna                  | 171 ms                                                                 | 179 ms: 1.04x slower                                                  |
| python_startup             | 15.2 ms                                                                | 15.9 ms: 1.05x slower                                                 |
| logging_silent             | 103 ns                                                                 | 108 ns: 1.05x slower                                                  |
| spectral_norm              | 99.1 ms                                                                | 105 ms: 1.06x slower                                                  |
| docutils                   | 2.60 sec                                                               | 2.75 sec: 1.06x slower                                                |
| dulwich_log                | 69.1 ms                                                                | 73.1 ms: 1.06x slower                                                 |
| json_loads                 | 28.8 us                                                                | 30.5 us: 1.06x slower                                                 |
| bpe_tokeniser              | 4.35 sec                                                               | 4.61 sec: 1.06x slower                                                |
| unpickle_pure_python       | 222 us                                                                 | 238 us: 1.07x slower                                                  |
| pprint_safe_repr           | 739 ms                                                                 | 790 ms: 1.07x slower                                                  |
| bench_mp_pool              | 89.1 ms                                                                | 96.0 ms: 1.08x slower                                                 |
| sphinx                     | 1.00 sec                                                               | 1.09 sec: 1.08x slower                                                |
| pickle_pure_python         | 318 us                                                                 | 344 us: 1.08x slower                                                  |
| scimark_fft                | 324 ms                                                                 | 351 ms: 1.08x slower                                                  |
| regex_effbot               | 2.70 ms                                                                | 2.93 ms: 1.08x slower                                                 |
| deepcopy_reduce            | 2.75 us                                                                | 2.98 us: 1.08x slower                                                 |
| deltablue                  | 3.42 ms                                                                | 3.72 ms: 1.09x slower                                                 |
| many_optionals             | 1.04 ms                                                                | 1.14 ms: 1.09x slower                                                 |
| generators                 | 29.1 ms                                                                | 31.7 ms: 1.09x slower                                                 |
| pprint_pformat             | 1.51 sec                                                               | 1.65 sec: 1.09x slower                                                |
| async_generators           | 336 ms                                                                 | 367 ms: 1.09x slower                                                  |
| k_core                     | 2.06 sec                                                               | 2.25 sec: 1.09x slower                                                |
| tomli_loads                | 2.01 sec                                                               | 2.21 sec: 1.10x slower                                                |
| pylint                     | 287 ms                                                                 | 314 ms: 1.10x slower                                                  |
| nqueens                    | 80.2 ms                                                                | 88.2 ms: 1.10x slower                                                 |
| sqlglot_v2_normalize       | 106 ms                                                                 | 117 ms: 1.10x slower                                                  |
| subparsers                 | 22.3 ms                                                                | 24.7 ms: 1.11x slower                                                 |
| xml_etree_generate         | 85.7 ms                                                                | 94.8 ms: 1.11x slower                                                 |
| scimark_sparse_mat_mult    | 4.59 ms                                                                | 5.09 ms: 1.11x slower                                                 |
| scimark_sor                | 115 ms                                                                 | 128 ms: 1.11x slower                                                  |
| django_template            | 36.7 ms                                                                | 40.8 ms: 1.11x slower                                                 |
| xml_etree_process          | 61.4 ms                                                                | 68.3 ms: 1.11x slower                                                 |
| json_dumps                 | 11.3 ms                                                                | 12.6 ms: 1.11x slower                                                 |
| sqlglot_v2_optimize        | 52.7 ms                                                                | 58.9 ms: 1.12x slower                                                 |
| pyflate                    | 421 ms                                                                 | 474 ms: 1.13x slower                                                  |
| 2to3                       | 255 ms                                                                 | 287 ms: 1.13x slower                                                  |
| deepcopy                   | 263 us                                                                 | 297 us: 1.13x slower                                                  |
| scimark_lu                 | 118 ms                                                                 | 134 ms: 1.13x slower                                                  |
| chaos                      | 56.3 ms                                                                | 63.9 ms: 1.13x slower                                                 |
| mdp                        | 1.18 sec                                                               | 1.35 sec: 1.14x slower                                                |
| genshi_xml                 | 50.6 ms                                                                | 57.9 ms: 1.14x slower                                                 |
| sympy_expand               | 473 ms                                                                 | 542 ms: 1.15x slower                                                  |
| go                         | 115 ms                                                                 | 133 ms: 1.15x slower                                                  |
| sqlglot_v2_transpile       | 1.60 ms                                                                | 1.84 ms: 1.15x slower                                                 |
| telco                      | 7.31 ms                                                                | 8.41 ms: 1.15x slower                                                 |
| hexiom                     | 6.12 ms                                                                | 7.07 ms: 1.15x slower                                                 |
| regex_compile              | 130 ms                                                                 | 151 ms: 1.16x slower                                                  |
| sympy_sum                  | 160 ms                                                                 | 185 ms: 1.16x slower                                                  |
| sympy_str                  | 282 ms                                                                 | 327 ms: 1.16x slower                                                  |
| sqlalchemy_imperative      | 20.6 ms                                                                | 23.9 ms: 1.16x slower                                                 |
| sympy_integrate            | 19.7 ms                                                                | 22.9 ms: 1.16x slower                                                 |
| logging_simple             | 6.22 us                                                                | 7.25 us: 1.17x slower                                                 |
| comprehensions             | 17.3 us                                                                | 20.2 us: 1.17x slower                                                 |
| raytrace                   | 258 ms                                                                 | 303 ms: 1.18x slower                                                  |
| logging_format             | 6.98 us                                                                | 8.20 us: 1.18x slower                                                 |
| sqlglot_v2_parse           | 1.29 ms                                                                | 1.52 ms: 1.18x slower                                                 |
| sqlalchemy_declarative     | 133 ms                                                                 | 157 ms: 1.18x slower                                                  |
| fannkuch                   | 389 ms                                                                 | 462 ms: 1.19x slower                                                  |
| richards_super             | 50.6 ms                                                                | 61.0 ms: 1.21x slower                                                 |
| shortest_path              | 442 ms                                                                 | 533 ms: 1.21x slower                                                  |
| scimark_monte_carlo        | 63.3 ms                                                                | 76.5 ms: 1.21x slower                                                 |
| crypto_pyaes               | 70.5 ms                                                                | 85.2 ms: 1.21x slower                                                 |
| richards                   | 44.4 ms                                                                | 53.8 ms: 1.21x slower                                                 |
| typing_runtime_protocols   | 160 us                                                                 | 194 us: 1.21x slower                                                  |
| deepcopy_memo              | 30.1 us                                                                | 36.6 us: 1.22x slower                                                 |
| connected_components       | 400 ms                                                                 | 488 ms: 1.22x slower                                                  |
| genshi_text                | 22.0 ms                                                                | 27.0 ms: 1.23x slower                                                 |
| nbody                      | 94.9 ms                                                                | 118 ms: 1.24x slower                                                  |
| mako                       | 12.3 ms                                                                | 15.4 ms: 1.25x slower                                                 |
| meteor_contest             | 101 ms                                                                 | 126 ms: 1.25x slower                                                  |
| python_startup_no_site     | 8.68 ms                                                                | 11.2 ms: 1.29x slower                                                 |
| coverage                   | 79.9 ms                                                                | 107 ms: 1.34x slower                                                  |
| bench_thread_pool          | 1.07 ms                                                                | 3.15 ms: 2.96x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.09x slower                                                          |

Benchmark hidden because not significant (4): async_tree_cpu_io_mixed, pycparser, pathlib, json
Ignored benchmarks (1) of results/bm-20250408-3.14.0a7+-45cd786-NOGIL/bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-45cd786.json: html5lib

- Geometric mean (including insignificant results): 1.074x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.06x

# Memory
- memory change: 1.20x