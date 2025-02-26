# Results vs. default_base_vs_NOGIL

- fork: mpage
- ref: load_fast_borrow_abs
- machine: linux-x86_64
- commit hash: b10c3be
- commit date: 2025-02-26
- overall geometric mean: 1.109x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.11x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5+-9e474a9 | bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-b10c3be |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 251 ms                                                                 | 297 ms: 1.18x slower                                                  |
| docutils       | 2.54 sec                                                               | 2.77 sec: 1.09x slower                                                |
| sphinx         | 973 ms                                                                 | 1.09 sec: 1.12x slower                                                |
| Geometric mean | (ref)                                                                  | 1.13x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5+-9e474a9 | bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-b10c3be |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 576 ms                                                                 | 490 ms: 1.18x faster                                                  |
| async_tree_cpu_io_mixed    | 592 ms                                                                 | 523 ms: 1.13x faster                                                  |
| async_tree_none_tg         | 252 ms                                                                 | 234 ms: 1.08x faster                                                  |
| async_tree_io_tg           | 591 ms                                                                 | 551 ms: 1.07x faster                                                  |
| async_tree_io              | 599 ms                                                                 | 579 ms: 1.04x faster                                                  |
| async_tree_memoization_tg  | 306 ms                                                                 | 302 ms: 1.01x faster                                                  |
| async_tree_none            | 256 ms                                                                 | 271 ms: 1.06x slower                                                  |
| async_tree_memoization     | 311 ms                                                                 | 337 ms: 1.09x slower                                                  |
| coroutines                 | 20.8 ms                                                                | 23.4 ms: 1.12x slower                                                 |
| async_generators           | 316 ms                                                                 | 367 ms: 1.16x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5+-9e474a9 | bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-b10c3be |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 247 ms                                                                 | 198 ms: 1.25x faster                                                  |
| nbody          | 84.7 ms                                                                | 122 ms: 1.44x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.05x slower                                                          |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5+-9e474a9 | bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-b10c3be |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 2.68 ms                                                                | 2.82 ms: 1.05x slower                                                 |
| regex_dna      | 170 ms                                                                 | 182 ms: 1.07x slower                                                  |
| regex_compile  | 125 ms                                                                 | 153 ms: 1.22x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.08x slower                                                          |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5+-9e474a9 | bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-b10c3be |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 89.6 ms                                                                | 88.5 ms: 1.01x faster                                                 |
| json_loads           | 28.3 us                                                                | 29.5 us: 1.04x slower                                                 |
| pickle_pure_python   | 303 us                                                                 | 347 us: 1.15x slower                                                  |
| json_dumps           | 11.1 ms                                                                | 12.7 ms: 1.15x slower                                                 |
| unpickle_pure_python | 208 us                                                                 | 241 us: 1.16x slower                                                  |
| xml_etree_generate   | 82.0 ms                                                                | 96.4 ms: 1.18x slower                                                 |
| xml_etree_process    | 57.1 ms                                                                | 69.9 ms: 1.22x slower                                                 |
| tomli_loads          | 1.82 sec                                                               | 2.29 sec: 1.25x slower                                                |
| Geometric mean       | (ref)                                                                  | 1.12x slower                                                          |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5+-9e474a9 | bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-b10c3be |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 14.8 ms                                                                | 15.6 ms: 1.05x slower                                                 |
| python_startup_no_site | 7.54 ms                                                                | 9.62 ms: 1.28x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.16x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5+-9e474a9 | bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-b10c3be |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 47.8 ms                                                                | 57.7 ms: 1.21x slower                                                 |
| django_template | 33.5 ms                                                                | 42.4 ms: 1.26x slower                                                 |
| genshi_text     | 20.6 ms                                                                | 26.9 ms: 1.31x slower                                                 |
| mako            | 11.5 ms                                                                | 15.7 ms: 1.37x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.29x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5+-9e474a9 | bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-b10c3be |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal               | 4.26 ms                                                                | 1.72 ms: 2.48x faster                                                 |
| sqlglot_normalize          | 278 ms                                                                 | 119 ms: 2.34x faster                                                  |
| create_gc_cycles           | 1.83 ms                                                                | 1.29 ms: 1.41x faster                                                 |
| pidigits                   | 247 ms                                                                 | 198 ms: 1.25x faster                                                  |
| async_tree_cpu_io_mixed_tg | 576 ms                                                                 | 490 ms: 1.18x faster                                                  |
| async_tree_cpu_io_mixed    | 592 ms                                                                 | 523 ms: 1.13x faster                                                  |
| async_tree_none_tg         | 252 ms                                                                 | 234 ms: 1.08x faster                                                  |
| async_tree_io_tg           | 591 ms                                                                 | 551 ms: 1.07x faster                                                  |
| sqlite_synth               | 2.18 us                                                                | 2.05 us: 1.06x faster                                                 |
| async_tree_io              | 599 ms                                                                 | 579 ms: 1.04x faster                                                  |
| async_tree_memoization_tg  | 306 ms                                                                 | 302 ms: 1.01x faster                                                  |
| xml_etree_iterparse        | 89.6 ms                                                                | 88.5 ms: 1.01x faster                                                 |
| json                       | 4.96 ms                                                                | 5.06 ms: 1.02x slower                                                 |
| json_loads                 | 28.3 us                                                                | 29.5 us: 1.04x slower                                                 |
| python_startup             | 14.8 ms                                                                | 15.6 ms: 1.05x slower                                                 |
| regex_effbot               | 2.68 ms                                                                | 2.82 ms: 1.05x slower                                                 |
| pathlib                    | 18.7 ms                                                                | 19.8 ms: 1.05x slower                                                 |
| logging_silent             | 103 ns                                                                 | 108 ns: 1.06x slower                                                  |
| async_tree_none            | 256 ms                                                                 | 271 ms: 1.06x slower                                                  |
| pycparser                  | 1.10 sec                                                               | 1.17 sec: 1.06x slower                                                |
| bench_mp_pool              | 88.5 ms                                                                | 94.7 ms: 1.07x slower                                                 |
| regex_dna                  | 170 ms                                                                 | 182 ms: 1.07x slower                                                  |
| async_tree_memoization     | 311 ms                                                                 | 337 ms: 1.09x slower                                                  |
| docutils                   | 2.54 sec                                                               | 2.77 sec: 1.09x slower                                                |
| dulwich_log                | 75.8 ms                                                                | 83.2 ms: 1.10x slower                                                 |
| k_core                     | 2.03 sec                                                               | 2.26 sec: 1.12x slower                                                |
| sphinx                     | 973 ms                                                                 | 1.09 sec: 1.12x slower                                                |
| coroutines                 | 20.8 ms                                                                | 23.4 ms: 1.12x slower                                                 |
| bpe_tokeniser              | 4.12 sec                                                               | 4.65 sec: 1.13x slower                                                |
| pickle_pure_python         | 303 us                                                                 | 347 us: 1.15x slower                                                  |
| json_dumps                 | 11.1 ms                                                                | 12.7 ms: 1.15x slower                                                 |
| many_optionals             | 1.01 ms                                                                | 1.15 ms: 1.15x slower                                                 |
| pylint                     | 275 ms                                                                 | 316 ms: 1.15x slower                                                  |
| unpickle_pure_python       | 208 us                                                                 | 241 us: 1.16x slower                                                  |
| async_generators           | 316 ms                                                                 | 367 ms: 1.16x slower                                                  |
| scimark_sor                | 109 ms                                                                 | 127 ms: 1.16x slower                                                  |
| subparsers                 | 21.9 ms                                                                | 25.5 ms: 1.17x slower                                                 |
| xml_etree_generate         | 82.0 ms                                                                | 96.4 ms: 1.18x slower                                                 |
| 2to3                       | 251 ms                                                                 | 297 ms: 1.18x slower                                                  |
| pprint_safe_repr           | 679 ms                                                                 | 804 ms: 1.18x slower                                                  |
| deepcopy_reduce            | 2.60 us                                                                | 3.08 us: 1.18x slower                                                 |
| raytrace                   | 254 ms                                                                 | 302 ms: 1.19x slower                                                  |
| scimark_fft                | 303 ms                                                                 | 361 ms: 1.19x slower                                                  |
| deepcopy                   | 252 us                                                                 | 300 us: 1.19x slower                                                  |
| mdp                        | 2.29 sec                                                               | 2.73 sec: 1.19x slower                                                |
| telco                      | 7.17 ms                                                                | 8.55 ms: 1.19x slower                                                 |
| sqlglot_optimize           | 50.5 ms                                                                | 60.5 ms: 1.20x slower                                                 |
| pprint_pformat             | 1.38 sec                                                               | 1.66 sec: 1.20x slower                                                |
| go                         | 110 ms                                                                 | 132 ms: 1.20x slower                                                  |
| pyflate                    | 393 ms                                                                 | 474 ms: 1.20x slower                                                  |
| sqlglot_transpile          | 1.53 ms                                                                | 1.84 ms: 1.21x slower                                                 |
| spectral_norm              | 88.1 ms                                                                | 106 ms: 1.21x slower                                                  |
| coverage                   | 79.3 ms                                                                | 95.7 ms: 1.21x slower                                                 |
| genshi_xml                 | 47.8 ms                                                                | 57.7 ms: 1.21x slower                                                 |
| sympy_expand               | 453 ms                                                                 | 548 ms: 1.21x slower                                                  |
| deltablue                  | 3.03 ms                                                                | 3.67 ms: 1.21x slower                                                 |
| logging_format             | 6.68 us                                                                | 8.11 us: 1.21x slower                                                 |
| regex_compile              | 125 ms                                                                 | 153 ms: 1.22x slower                                                  |
| thrift                     | 718 us                                                                 | 878 us: 1.22x slower                                                  |
| comprehensions             | 15.9 us                                                                | 19.5 us: 1.22x slower                                                 |
| xml_etree_process          | 57.1 ms                                                                | 69.9 ms: 1.22x slower                                                 |
| logging_simple             | 5.90 us                                                                | 7.22 us: 1.22x slower                                                 |
| sqlglot_parse              | 1.23 ms                                                                | 1.51 ms: 1.23x slower                                                 |
| sympy_integrate            | 19.4 ms                                                                | 23.8 ms: 1.23x slower                                                 |
| sqlalchemy_imperative      | 19.3 ms                                                                | 23.7 ms: 1.23x slower                                                 |
| sympy_str                  | 269 ms                                                                 | 332 ms: 1.23x slower                                                  |
| generators                 | 26.3 ms                                                                | 32.5 ms: 1.24x slower                                                 |
| sympy_sum                  | 151 ms                                                                 | 187 ms: 1.24x slower                                                  |
| scimark_sparse_mat_mult    | 4.13 ms                                                                | 5.12 ms: 1.24x slower                                                 |
| scimark_lu                 | 109 ms                                                                 | 136 ms: 1.25x slower                                                  |
| chaos                      | 53.7 ms                                                                | 66.9 ms: 1.25x slower                                                 |
| connected_components       | 387 ms                                                                 | 483 ms: 1.25x slower                                                  |
| sqlalchemy_declarative     | 126 ms                                                                 | 158 ms: 1.25x slower                                                  |
| tomli_loads                | 1.82 sec                                                               | 2.29 sec: 1.25x slower                                                |
| scimark_monte_carlo        | 61.6 ms                                                                | 77.4 ms: 1.26x slower                                                 |
| deepcopy_memo              | 29.1 us                                                                | 36.7 us: 1.26x slower                                                 |
| nqueens                    | 74.9 ms                                                                | 94.4 ms: 1.26x slower                                                 |
| shortest_path              | 426 ms                                                                 | 537 ms: 1.26x slower                                                  |
| richards                   | 42.0 ms                                                                | 53.1 ms: 1.26x slower                                                 |
| meteor_contest             | 97.8 ms                                                                | 124 ms: 1.26x slower                                                  |
| django_template            | 33.5 ms                                                                | 42.4 ms: 1.26x slower                                                 |
| fannkuch                   | 367 ms                                                                 | 466 ms: 1.27x slower                                                  |
| python_startup_no_site     | 7.54 ms                                                                | 9.62 ms: 1.28x slower                                                 |
| hexiom                     | 5.65 ms                                                                | 7.22 ms: 1.28x slower                                                 |
| typing_runtime_protocols   | 154 us                                                                 | 198 us: 1.29x slower                                                  |
| richards_super             | 47.7 ms                                                                | 61.6 ms: 1.29x slower                                                 |
| crypto_pyaes               | 65.6 ms                                                                | 85.1 ms: 1.30x slower                                                 |
| genshi_text                | 20.6 ms                                                                | 26.9 ms: 1.31x slower                                                 |
| mako                       | 11.5 ms                                                                | 15.7 ms: 1.37x slower                                                 |
| nbody                      | 84.7 ms                                                                | 122 ms: 1.44x slower                                                  |
| bench_thread_pool          | 1.03 ms                                                                | 3.29 ms: 3.20x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.13x slower                                                          |

Benchmark hidden because not significant (4): regex_v8, float, xml_etree_parse, asyncio_websockets
Ignored benchmarks (1) of results/bm-20250226-3.14.0a5+-b10c3be-NOGIL/bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-b10c3be.json: html5lib

- Geometric mean (including insignificant results): 1.109x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.14x
- 95% likely to have a slowdown of 1.12x
- 99% likely to have a slowdown of 1.11x

# Memory
- memory change: 1.20x