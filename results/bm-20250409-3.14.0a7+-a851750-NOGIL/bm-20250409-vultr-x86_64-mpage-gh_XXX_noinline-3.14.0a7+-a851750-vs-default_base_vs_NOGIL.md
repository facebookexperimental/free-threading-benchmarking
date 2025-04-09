# Results vs. default_base_vs_NOGIL

- fork: mpage
- ref: gh_XXX_noinline
- machine: linux-x86_64
- commit hash: a851750
- commit date: 2025-04-09
- overall geometric mean: 1.086x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250409-vultr-x86_64-python-1f5682f3a27516833f7c-3.14.0a7+-1f5682f | bm-20250409-vultr-x86_64-mpage-gh_XXX_noinline-3.14.0a7+-a851750 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------:|
| 2to3           | 246 ms                                                                 | 279 ms: 1.13x slower                                             |
| docutils       | 2.52 sec                                                               | 2.69 sec: 1.07x slower                                           |
| sphinx         | 971 ms                                                                 | 1.06 sec: 1.09x slower                                           |
| Geometric mean | (ref)                                                                  | 1.10x slower                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250409-vultr-x86_64-python-1f5682f3a27516833f7c-3.14.0a7+-1f5682f | bm-20250409-vultr-x86_64-mpage-gh_XXX_noinline-3.14.0a7+-a851750 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------:|
| async_tree_io_tg           | 608 ms                                                                 | 513 ms: 1.19x faster                                             |
| async_tree_none_tg         | 258 ms                                                                 | 223 ms: 1.16x faster                                             |
| async_tree_io              | 616 ms                                                                 | 538 ms: 1.14x faster                                             |
| async_tree_memoization_tg  | 317 ms                                                                 | 278 ms: 1.14x faster                                             |
| async_tree_none            | 272 ms                                                                 | 254 ms: 1.07x faster                                             |
| coroutines                 | 23.6 ms                                                                | 22.4 ms: 1.05x faster                                            |
| async_tree_memoization     | 310 ms                                                                 | 307 ms: 1.01x faster                                             |
| asyncio_websockets         | 517 ms                                                                 | 516 ms: 1.00x faster                                             |
| async_tree_cpu_io_mixed_tg | 493 ms                                                                 | 515 ms: 1.05x slower                                             |
| async_tree_cpu_io_mixed    | 494 ms                                                                 | 542 ms: 1.10x slower                                             |
| async_generators           | 320 ms                                                                 | 356 ms: 1.12x slower                                             |
| Geometric mean             | (ref)                                                                  | 1.04x faster                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250409-vultr-x86_64-python-1f5682f3a27516833f7c-3.14.0a7+-1f5682f | bm-20250409-vultr-x86_64-mpage-gh_XXX_noinline-3.14.0a7+-a851750 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------:|
| float          | 66.8 ms                                                                | 67.3 ms: 1.01x slower                                            |
| pidigits       | 190 ms                                                                 | 222 ms: 1.17x slower                                             |
| nbody          | 81.1 ms                                                                | 109 ms: 1.34x slower                                             |
| Geometric mean | (ref)                                                                  | 1.16x slower                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250409-vultr-x86_64-python-1f5682f3a27516833f7c-3.14.0a7+-1f5682f | bm-20250409-vultr-x86_64-mpage-gh_XXX_noinline-3.14.0a7+-a851750 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------:|
| regex_v8       | 21.0 ms                                                                | 22.0 ms: 1.04x slower                                            |
| regex_dna      | 165 ms                                                                 | 174 ms: 1.05x slower                                             |
| regex_effbot   | 2.60 ms                                                                | 2.83 ms: 1.09x slower                                            |
| regex_compile  | 123 ms                                                                 | 142 ms: 1.16x slower                                             |
| Geometric mean | (ref)                                                                  | 1.08x slower                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250409-vultr-x86_64-python-1f5682f3a27516833f7c-3.14.0a7+-1f5682f | bm-20250409-vultr-x86_64-mpage-gh_XXX_noinline-3.14.0a7+-a851750 |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------:|
| xml_etree_iterparse  | 90.7 ms                                                                | 83.9 ms: 1.08x faster                                            |
| unpickle_pure_python | 209 us                                                                 | 224 us: 1.07x slower                                             |
| pickle_pure_python   | 300 us                                                                 | 323 us: 1.08x slower                                             |
| json_loads           | 28.4 us                                                                | 30.7 us: 1.08x slower                                            |
| xml_etree_generate   | 82.9 ms                                                                | 91.9 ms: 1.11x slower                                            |
| xml_etree_process    | 58.3 ms                                                                | 65.6 ms: 1.13x slower                                            |
| json_dumps           | 11.0 ms                                                                | 12.6 ms: 1.14x slower                                            |
| tomli_loads          | 1.82 sec                                                               | 2.09 sec: 1.15x slower                                           |
| Geometric mean       | (ref)                                                                  | 1.07x slower                                                     |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250409-vultr-x86_64-python-1f5682f3a27516833f7c-3.14.0a7+-1f5682f | bm-20250409-vultr-x86_64-mpage-gh_XXX_noinline-3.14.0a7+-a851750 |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------:|
| python_startup         | 15.1 ms                                                                | 15.8 ms: 1.05x slower                                            |
| python_startup_no_site | 8.61 ms                                                                | 11.1 ms: 1.29x slower                                            |
| Geometric mean         | (ref)                                                                  | 1.16x slower                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250409-vultr-x86_64-python-1f5682f3a27516833f7c-3.14.0a7+-1f5682f | bm-20250409-vultr-x86_64-mpage-gh_XXX_noinline-3.14.0a7+-a851750 |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------:|
| django_template | 35.1 ms                                                                | 39.6 ms: 1.13x slower                                            |
| genshi_xml      | 47.3 ms                                                                | 54.9 ms: 1.16x slower                                            |
| genshi_text     | 20.1 ms                                                                | 25.6 ms: 1.27x slower                                            |
| mako            | 11.7 ms                                                                | 15.0 ms: 1.28x slower                                            |
| Geometric mean  | (ref)                                                                  | 1.21x slower                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20250409-vultr-x86_64-python-1f5682f3a27516833f7c-3.14.0a7+-1f5682f | bm-20250409-vultr-x86_64-mpage-gh_XXX_noinline-3.14.0a7+-a851750 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------:|
| gc_traversal               | 4.20 ms                                                                | 1.77 ms: 2.37x faster                                            |
| create_gc_cycles           | 1.84 ms                                                                | 1.33 ms: 1.38x faster                                            |
| async_tree_io_tg           | 608 ms                                                                 | 513 ms: 1.19x faster                                             |
| async_tree_none_tg         | 258 ms                                                                 | 223 ms: 1.16x faster                                             |
| async_tree_io              | 616 ms                                                                 | 538 ms: 1.14x faster                                             |
| async_tree_memoization_tg  | 317 ms                                                                 | 278 ms: 1.14x faster                                             |
| sqlite_synth               | 2.18 us                                                                | 2.00 us: 1.09x faster                                            |
| xml_etree_iterparse        | 90.7 ms                                                                | 83.9 ms: 1.08x faster                                            |
| async_tree_none            | 272 ms                                                                 | 254 ms: 1.07x faster                                             |
| coroutines                 | 23.6 ms                                                                | 22.4 ms: 1.05x faster                                            |
| async_tree_memoization     | 310 ms                                                                 | 307 ms: 1.01x faster                                             |
| asyncio_websockets         | 517 ms                                                                 | 516 ms: 1.00x faster                                             |
| float                      | 66.8 ms                                                                | 67.3 ms: 1.01x slower                                            |
| pathlib                    | 19.1 ms                                                                | 19.3 ms: 1.01x slower                                            |
| json                       | 5.14 ms                                                                | 5.26 ms: 1.02x slower                                            |
| pycparser                  | 1.10 sec                                                               | 1.14 sec: 1.04x slower                                           |
| regex_v8                   | 21.0 ms                                                                | 22.0 ms: 1.04x slower                                            |
| async_tree_cpu_io_mixed_tg | 493 ms                                                                 | 515 ms: 1.05x slower                                             |
| logging_silent             | 94.5 ns                                                                | 99.0 ns: 1.05x slower                                            |
| python_startup             | 15.1 ms                                                                | 15.8 ms: 1.05x slower                                            |
| regex_dna                  | 165 ms                                                                 | 174 ms: 1.05x slower                                             |
| dulwich_log                | 66.9 ms                                                                | 70.8 ms: 1.06x slower                                            |
| docutils                   | 2.52 sec                                                               | 2.69 sec: 1.07x slower                                           |
| bpe_tokeniser              | 4.18 sec                                                               | 4.47 sec: 1.07x slower                                           |
| unpickle_pure_python       | 209 us                                                                 | 224 us: 1.07x slower                                             |
| pprint_safe_repr           | 703 ms                                                                 | 755 ms: 1.07x slower                                             |
| bench_mp_pool              | 88.1 ms                                                                | 94.7 ms: 1.08x slower                                            |
| pickle_pure_python         | 300 us                                                                 | 323 us: 1.08x slower                                             |
| scimark_fft                | 311 ms                                                                 | 335 ms: 1.08x slower                                             |
| generators                 | 27.2 ms                                                                | 29.4 ms: 1.08x slower                                            |
| deltablue                  | 3.20 ms                                                                | 3.46 ms: 1.08x slower                                            |
| json_loads                 | 28.4 us                                                                | 30.7 us: 1.08x slower                                            |
| spectral_norm              | 92.5 ms                                                                | 100 ms: 1.09x slower                                             |
| regex_effbot               | 2.60 ms                                                                | 2.83 ms: 1.09x slower                                            |
| sphinx                     | 971 ms                                                                 | 1.06 sec: 1.09x slower                                           |
| many_optionals             | 1.02 ms                                                                | 1.11 ms: 1.09x slower                                            |
| pprint_pformat             | 1.44 sec                                                               | 1.57 sec: 1.10x slower                                           |
| async_tree_cpu_io_mixed    | 494 ms                                                                 | 542 ms: 1.10x slower                                             |
| pylint                     | 277 ms                                                                 | 305 ms: 1.10x slower                                             |
| scimark_sor                | 108 ms                                                                 | 119 ms: 1.11x slower                                             |
| xml_etree_generate         | 82.9 ms                                                                | 91.9 ms: 1.11x slower                                            |
| nqueens                    | 75.8 ms                                                                | 84.0 ms: 1.11x slower                                            |
| k_core                     | 2.01 sec                                                               | 2.23 sec: 1.11x slower                                           |
| async_generators           | 320 ms                                                                 | 356 ms: 1.12x slower                                             |
| sqlglot_v2_normalize       | 100 ms                                                                 | 112 ms: 1.12x slower                                             |
| subparsers                 | 21.7 ms                                                                | 24.3 ms: 1.12x slower                                            |
| deepcopy_reduce            | 2.60 us                                                                | 2.91 us: 1.12x slower                                            |
| django_template            | 35.1 ms                                                                | 39.6 ms: 1.13x slower                                            |
| xml_etree_process          | 58.3 ms                                                                | 65.6 ms: 1.13x slower                                            |
| scimark_sparse_mat_mult    | 4.32 ms                                                                | 4.87 ms: 1.13x slower                                            |
| 2to3                       | 246 ms                                                                 | 279 ms: 1.13x slower                                             |
| sqlglot_v2_optimize        | 50.1 ms                                                                | 56.9 ms: 1.14x slower                                            |
| scimark_lu                 | 111 ms                                                                 | 127 ms: 1.14x slower                                             |
| pyflate                    | 399 ms                                                                 | 456 ms: 1.14x slower                                             |
| json_dumps                 | 11.0 ms                                                                | 12.6 ms: 1.14x slower                                            |
| hexiom                     | 5.67 ms                                                                | 6.48 ms: 1.14x slower                                            |
| mdp                        | 1.13 sec                                                               | 1.29 sec: 1.15x slower                                           |
| tomli_loads                | 1.82 sec                                                               | 2.09 sec: 1.15x slower                                           |
| deepcopy                   | 248 us                                                                 | 285 us: 1.15x slower                                             |
| sympy_expand               | 455 ms                                                                 | 524 ms: 1.15x slower                                             |
| sympy_sum                  | 154 ms                                                                 | 178 ms: 1.15x slower                                             |
| chaos                      | 52.3 ms                                                                | 60.4 ms: 1.15x slower                                            |
| regex_compile              | 123 ms                                                                 | 142 ms: 1.16x slower                                             |
| genshi_xml                 | 47.3 ms                                                                | 54.9 ms: 1.16x slower                                            |
| raytrace                   | 244 ms                                                                 | 285 ms: 1.17x slower                                             |
| sqlglot_v2_transpile       | 1.50 ms                                                                | 1.75 ms: 1.17x slower                                            |
| go                         | 106 ms                                                                 | 124 ms: 1.17x slower                                             |
| pidigits                   | 190 ms                                                                 | 222 ms: 1.17x slower                                             |
| sqlalchemy_imperative      | 19.9 ms                                                                | 23.4 ms: 1.18x slower                                            |
| logging_format             | 6.64 us                                                                | 7.83 us: 1.18x slower                                            |
| sympy_str                  | 269 ms                                                                 | 317 ms: 1.18x slower                                             |
| sympy_integrate            | 18.8 ms                                                                | 22.2 ms: 1.18x slower                                            |
| telco                      | 7.02 ms                                                                | 8.29 ms: 1.18x slower                                            |
| logging_simple             | 5.86 us                                                                | 6.95 us: 1.19x slower                                            |
| comprehensions             | 16.2 us                                                                | 19.3 us: 1.19x slower                                            |
| fannkuch                   | 374 ms                                                                 | 446 ms: 1.19x slower                                             |
| sqlalchemy_declarative     | 129 ms                                                                 | 153 ms: 1.19x slower                                             |
| sqlglot_v2_parse           | 1.21 ms                                                                | 1.45 ms: 1.20x slower                                            |
| deepcopy_memo              | 29.0 us                                                                | 34.9 us: 1.20x slower                                            |
| shortest_path              | 432 ms                                                                 | 531 ms: 1.23x slower                                             |
| connected_components       | 392 ms                                                                 | 484 ms: 1.24x slower                                             |
| scimark_monte_carlo        | 59.4 ms                                                                | 73.5 ms: 1.24x slower                                            |
| crypto_pyaes               | 66.3 ms                                                                | 82.0 ms: 1.24x slower                                            |
| typing_runtime_protocols   | 153 us                                                                 | 190 us: 1.24x slower                                             |
| richards                   | 40.3 ms                                                                | 50.1 ms: 1.24x slower                                            |
| meteor_contest             | 99.0 ms                                                                | 124 ms: 1.25x slower                                             |
| richards_super             | 46.0 ms                                                                | 57.5 ms: 1.25x slower                                            |
| genshi_text                | 20.1 ms                                                                | 25.6 ms: 1.27x slower                                            |
| mako                       | 11.7 ms                                                                | 15.0 ms: 1.28x slower                                            |
| python_startup_no_site     | 8.61 ms                                                                | 11.1 ms: 1.29x slower                                            |
| nbody                      | 81.1 ms                                                                | 109 ms: 1.34x slower                                             |
| coverage                   | 79.2 ms                                                                | 108 ms: 1.36x slower                                             |
| bench_thread_pool          | 1.05 ms                                                                | 3.13 ms: 2.99x slower                                            |
| Geometric mean             | (ref)                                                                  | 1.11x slower                                                     |

Benchmark hidden because not significant (1): xml_etree_parse
Ignored benchmarks (1) of results/bm-20250409-3.14.0a7+-a851750-NOGIL/bm-20250409-vultr-x86_64-mpage-gh_XXX_noinline-3.14.0a7+-a851750.json: html5lib

- Geometric mean (including insignificant results): 1.086x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.09x
- 99% likely to have a slowdown of 1.08x

# Memory
- memory change: 1.20x