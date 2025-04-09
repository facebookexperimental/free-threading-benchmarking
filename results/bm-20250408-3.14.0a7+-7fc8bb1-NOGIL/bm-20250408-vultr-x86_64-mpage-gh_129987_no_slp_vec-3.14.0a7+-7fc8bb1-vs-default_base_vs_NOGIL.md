# Results vs. default_base_vs_NOGIL

- fork: mpage
- ref: gh_129987_no_slp_vec
- machine: linux-x86_64
- commit hash: 7fc8bb1
- commit date: 2025-04-08
- overall geometric mean: 1.084x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-7fc8bb1 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 255 ms                                                                 | 291 ms: 1.14x slower                                                  |
| docutils       | 2.60 sec                                                               | 2.77 sec: 1.07x slower                                                |
| sphinx         | 1.00 sec                                                               | 1.09 sec: 1.09x slower                                                |
| Geometric mean | (ref)                                                                  | 1.10x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-7fc8bb1 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 626 ms                                                                 | 536 ms: 1.17x faster                                                  |
| async_tree_none_tg         | 263 ms                                                                 | 233 ms: 1.13x faster                                                  |
| async_tree_io              | 628 ms                                                                 | 564 ms: 1.11x faster                                                  |
| async_tree_memoization_tg  | 325 ms                                                                 | 296 ms: 1.10x faster                                                  |
| async_tree_none            | 278 ms                                                                 | 269 ms: 1.04x faster                                                  |
| coroutines                 | 24.6 ms                                                                | 23.8 ms: 1.03x faster                                                 |
| async_tree_cpu_io_mixed_tg | 503 ms                                                                 | 498 ms: 1.01x faster                                                  |
| asyncio_websockets         | 518 ms                                                                 | 516 ms: 1.00x faster                                                  |
| async_tree_memoization     | 318 ms                                                                 | 322 ms: 1.01x slower                                                  |
| async_tree_cpu_io_mixed    | 506 ms                                                                 | 528 ms: 1.04x slower                                                  |
| async_generators           | 336 ms                                                                 | 367 ms: 1.09x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.04x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-7fc8bb1 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 72.3 ms                                                                | 70.1 ms: 1.03x faster                                                 |
| pidigits       | 192 ms                                                                 | 217 ms: 1.13x slower                                                  |
| nbody          | 94.9 ms                                                                | 117 ms: 1.24x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.11x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-7fc8bb1 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 21.8 ms                                                                | 21.0 ms: 1.04x faster                                                 |
| regex_effbot   | 2.70 ms                                                                | 2.71 ms: 1.00x slower                                                 |
| regex_dna      | 171 ms                                                                 | 183 ms: 1.07x slower                                                  |
| regex_compile  | 130 ms                                                                 | 152 ms: 1.17x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.05x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-7fc8bb1 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 93.0 ms                                                                | 87.9 ms: 1.06x faster                                                 |
| json_loads           | 28.8 us                                                                | 30.7 us: 1.07x slower                                                 |
| unpickle_pure_python | 222 us                                                                 | 243 us: 1.09x slower                                                  |
| pickle_pure_python   | 318 us                                                                 | 350 us: 1.10x slower                                                  |
| xml_etree_generate   | 85.7 ms                                                                | 96.0 ms: 1.12x slower                                                 |
| tomli_loads          | 2.01 sec                                                               | 2.27 sec: 1.13x slower                                                |
| xml_etree_process    | 61.4 ms                                                                | 70.2 ms: 1.14x slower                                                 |
| json_dumps           | 11.3 ms                                                                | 13.0 ms: 1.15x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.08x slower                                                          |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-7fc8bb1 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 15.2 ms                                                                | 15.9 ms: 1.05x slower                                                 |
| python_startup_no_site | 8.68 ms                                                                | 11.2 ms: 1.29x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.16x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-7fc8bb1 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 36.7 ms                                                                | 42.5 ms: 1.16x slower                                                 |
| genshi_xml      | 50.6 ms                                                                | 58.6 ms: 1.16x slower                                                 |
| mako            | 12.3 ms                                                                | 15.5 ms: 1.26x slower                                                 |
| genshi_text     | 22.0 ms                                                                | 27.7 ms: 1.26x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.21x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-7fc8bb1 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal               | 4.34 ms                                                                | 1.77 ms: 2.45x faster                                                 |
| create_gc_cycles           | 1.86 ms                                                                | 1.33 ms: 1.40x faster                                                 |
| async_tree_io_tg           | 626 ms                                                                 | 536 ms: 1.17x faster                                                  |
| async_tree_none_tg         | 263 ms                                                                 | 233 ms: 1.13x faster                                                  |
| sqlite_synth               | 2.23 us                                                                | 2.00 us: 1.11x faster                                                 |
| async_tree_io              | 628 ms                                                                 | 564 ms: 1.11x faster                                                  |
| async_tree_memoization_tg  | 325 ms                                                                 | 296 ms: 1.10x faster                                                  |
| xml_etree_iterparse        | 93.0 ms                                                                | 87.9 ms: 1.06x faster                                                 |
| regex_v8                   | 21.8 ms                                                                | 21.0 ms: 1.04x faster                                                 |
| async_tree_none            | 278 ms                                                                 | 269 ms: 1.04x faster                                                  |
| coroutines                 | 24.6 ms                                                                | 23.8 ms: 1.03x faster                                                 |
| float                      | 72.3 ms                                                                | 70.1 ms: 1.03x faster                                                 |
| async_tree_cpu_io_mixed_tg | 503 ms                                                                 | 498 ms: 1.01x faster                                                  |
| asyncio_websockets         | 518 ms                                                                 | 516 ms: 1.00x faster                                                  |
| regex_effbot               | 2.70 ms                                                                | 2.71 ms: 1.00x slower                                                 |
| pathlib                    | 19.3 ms                                                                | 19.5 ms: 1.01x slower                                                 |
| async_tree_memoization     | 318 ms                                                                 | 322 ms: 1.01x slower                                                  |
| pycparser                  | 1.15 sec                                                               | 1.17 sec: 1.02x slower                                                |
| json                       | 5.19 ms                                                                | 5.28 ms: 1.02x slower                                                 |
| async_tree_cpu_io_mixed    | 506 ms                                                                 | 528 ms: 1.04x slower                                                  |
| python_startup             | 15.2 ms                                                                | 15.9 ms: 1.05x slower                                                 |
| dulwich_log                | 69.1 ms                                                                | 73.3 ms: 1.06x slower                                                 |
| spectral_norm              | 99.1 ms                                                                | 105 ms: 1.06x slower                                                  |
| docutils                   | 2.60 sec                                                               | 2.77 sec: 1.07x slower                                                |
| json_loads                 | 28.8 us                                                                | 30.7 us: 1.07x slower                                                 |
| regex_dna                  | 171 ms                                                                 | 183 ms: 1.07x slower                                                  |
| logging_silent             | 103 ns                                                                 | 110 ns: 1.07x slower                                                  |
| bpe_tokeniser              | 4.35 sec                                                               | 4.68 sec: 1.08x slower                                                |
| bench_mp_pool              | 89.1 ms                                                                | 95.9 ms: 1.08x slower                                                 |
| pprint_safe_repr           | 739 ms                                                                 | 799 ms: 1.08x slower                                                  |
| sphinx                     | 1.00 sec                                                               | 1.09 sec: 1.09x slower                                                |
| async_generators           | 336 ms                                                                 | 367 ms: 1.09x slower                                                  |
| unpickle_pure_python       | 222 us                                                                 | 243 us: 1.09x slower                                                  |
| pprint_pformat             | 1.51 sec                                                               | 1.65 sec: 1.09x slower                                                |
| k_core                     | 2.06 sec                                                               | 2.25 sec: 1.09x slower                                                |
| many_optionals             | 1.04 ms                                                                | 1.15 ms: 1.10x slower                                                 |
| pickle_pure_python         | 318 us                                                                 | 350 us: 1.10x slower                                                  |
| scimark_fft                | 324 ms                                                                 | 358 ms: 1.10x slower                                                  |
| pylint                     | 287 ms                                                                 | 317 ms: 1.10x slower                                                  |
| deltablue                  | 3.42 ms                                                                | 3.80 ms: 1.11x slower                                                 |
| scimark_sparse_mat_mult    | 4.59 ms                                                                | 5.10 ms: 1.11x slower                                                 |
| deepcopy_reduce            | 2.75 us                                                                | 3.07 us: 1.12x slower                                                 |
| sqlglot_v2_normalize       | 106 ms                                                                 | 119 ms: 1.12x slower                                                  |
| scimark_sor                | 115 ms                                                                 | 129 ms: 1.12x slower                                                  |
| xml_etree_generate         | 85.7 ms                                                                | 96.0 ms: 1.12x slower                                                 |
| nqueens                    | 80.2 ms                                                                | 90.0 ms: 1.12x slower                                                 |
| tomli_loads                | 2.01 sec                                                               | 2.27 sec: 1.13x slower                                                |
| pidigits                   | 192 ms                                                                 | 217 ms: 1.13x slower                                                  |
| scimark_lu                 | 118 ms                                                                 | 134 ms: 1.13x slower                                                  |
| deepcopy                   | 263 us                                                                 | 298 us: 1.13x slower                                                  |
| subparsers                 | 22.3 ms                                                                | 25.3 ms: 1.13x slower                                                 |
| sqlglot_v2_optimize        | 52.7 ms                                                                | 59.7 ms: 1.13x slower                                                 |
| 2to3                       | 255 ms                                                                 | 291 ms: 1.14x slower                                                  |
| xml_etree_process          | 61.4 ms                                                                | 70.2 ms: 1.14x slower                                                 |
| sympy_expand               | 473 ms                                                                 | 542 ms: 1.15x slower                                                  |
| json_dumps                 | 11.3 ms                                                                | 13.0 ms: 1.15x slower                                                 |
| chaos                      | 56.3 ms                                                                | 64.7 ms: 1.15x slower                                                 |
| telco                      | 7.31 ms                                                                | 8.41 ms: 1.15x slower                                                 |
| generators                 | 29.1 ms                                                                | 33.5 ms: 1.15x slower                                                 |
| mdp                        | 1.18 sec                                                               | 1.37 sec: 1.15x slower                                                |
| pyflate                    | 421 ms                                                                 | 486 ms: 1.16x slower                                                  |
| django_template            | 36.7 ms                                                                | 42.5 ms: 1.16x slower                                                 |
| genshi_xml                 | 50.6 ms                                                                | 58.6 ms: 1.16x slower                                                 |
| sympy_sum                  | 160 ms                                                                 | 186 ms: 1.16x slower                                                  |
| sqlglot_v2_transpile       | 1.60 ms                                                                | 1.87 ms: 1.17x slower                                                 |
| regex_compile              | 130 ms                                                                 | 152 ms: 1.17x slower                                                  |
| sympy_str                  | 282 ms                                                                 | 330 ms: 1.17x slower                                                  |
| sqlalchemy_imperative      | 20.6 ms                                                                | 24.1 ms: 1.17x slower                                                 |
| logging_format             | 6.98 us                                                                | 8.21 us: 1.18x slower                                                 |
| logging_simple             | 6.22 us                                                                | 7.32 us: 1.18x slower                                                 |
| go                         | 115 ms                                                                 | 136 ms: 1.18x slower                                                  |
| sympy_integrate            | 19.7 ms                                                                | 23.2 ms: 1.18x slower                                                 |
| hexiom                     | 6.12 ms                                                                | 7.23 ms: 1.18x slower                                                 |
| raytrace                   | 258 ms                                                                 | 307 ms: 1.19x slower                                                  |
| sqlalchemy_declarative     | 133 ms                                                                 | 159 ms: 1.19x slower                                                  |
| comprehensions             | 17.3 us                                                                | 20.6 us: 1.20x slower                                                 |
| sqlglot_v2_parse           | 1.29 ms                                                                | 1.54 ms: 1.20x slower                                                 |
| shortest_path              | 442 ms                                                                 | 533 ms: 1.21x slower                                                  |
| fannkuch                   | 389 ms                                                                 | 471 ms: 1.21x slower                                                  |
| scimark_monte_carlo        | 63.3 ms                                                                | 76.8 ms: 1.21x slower                                                 |
| connected_components       | 400 ms                                                                 | 487 ms: 1.22x slower                                                  |
| typing_runtime_protocols   | 160 us                                                                 | 195 us: 1.22x slower                                                  |
| crypto_pyaes               | 70.5 ms                                                                | 86.0 ms: 1.22x slower                                                 |
| deepcopy_memo              | 30.1 us                                                                | 36.8 us: 1.22x slower                                                 |
| richards                   | 44.4 ms                                                                | 54.6 ms: 1.23x slower                                                 |
| richards_super             | 50.6 ms                                                                | 62.4 ms: 1.23x slower                                                 |
| nbody                      | 94.9 ms                                                                | 117 ms: 1.24x slower                                                  |
| mako                       | 12.3 ms                                                                | 15.5 ms: 1.26x slower                                                 |
| genshi_text                | 22.0 ms                                                                | 27.7 ms: 1.26x slower                                                 |
| meteor_contest             | 101 ms                                                                 | 129 ms: 1.27x slower                                                  |
| python_startup_no_site     | 8.68 ms                                                                | 11.2 ms: 1.29x slower                                                 |
| coverage                   | 79.9 ms                                                                | 108 ms: 1.36x slower                                                  |
| bench_thread_pool          | 1.07 ms                                                                | 3.15 ms: 2.95x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.10x slower                                                          |

Benchmark hidden because not significant (1): xml_etree_parse
Ignored benchmarks (1) of results/bm-20250408-3.14.0a7+-7fc8bb1-NOGIL/bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-7fc8bb1.json: html5lib

- Geometric mean (including insignificant results): 1.084x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.08x
- 99% likely to have a slowdown of 1.07x

# Memory
- memory change: 1.20x