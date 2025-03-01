# Results vs. default_base_vs_NOGIL

- fork: mpage
- ref: load_fast_borrow_abs
- machine: linux-x86_64
- commit hash: f012a9f
- commit date: 2025-02-28
- overall geometric mean: 1.108x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x slower
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250228-vultr-x86_64-python-75f38af7810af1c3ca56-3.14.0a5+-75f38af | bm-20250228-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-f012a9f |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 247 ms                                                                 | 297 ms: 1.20x slower                                                  |
| docutils       | 2.51 sec                                                               | 2.79 sec: 1.11x slower                                                |
| sphinx         | 969 ms                                                                 | 1.10 sec: 1.14x slower                                                |
| Geometric mean | (ref)                                                                  | 1.15x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250228-vultr-x86_64-python-75f38af7810af1c3ca56-3.14.0a5+-75f38af | bm-20250228-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-f012a9f |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 600 ms                                                                 | 537 ms: 1.12x faster                                                  |
| async_tree_none_tg         | 253 ms                                                                 | 229 ms: 1.10x faster                                                  |
| async_tree_io              | 604 ms                                                                 | 572 ms: 1.06x faster                                                  |
| async_tree_memoization_tg  | 308 ms                                                                 | 299 ms: 1.03x faster                                                  |
| async_tree_cpu_io_mixed_tg | 472 ms                                                                 | 485 ms: 1.03x slower                                                  |
| async_tree_none            | 259 ms                                                                 | 271 ms: 1.05x slower                                                  |
| async_tree_memoization     | 313 ms                                                                 | 331 ms: 1.06x slower                                                  |
| async_tree_cpu_io_mixed    | 485 ms                                                                 | 521 ms: 1.07x slower                                                  |
| coroutines                 | 21.3 ms                                                                | 23.8 ms: 1.12x slower                                                 |
| async_generators           | 320 ms                                                                 | 369 ms: 1.15x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250228-vultr-x86_64-python-75f38af7810af1c3ca56-3.14.0a5+-75f38af | bm-20250228-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-f012a9f |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 70.3 ms                                                                | 69.9 ms: 1.01x faster                                                 |
| pidigits       | 187 ms                                                                 | 198 ms: 1.05x slower                                                  |
| nbody          | 84.2 ms                                                                | 119 ms: 1.41x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.14x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250228-vultr-x86_64-python-75f38af7810af1c3ca56-3.14.0a5+-75f38af | bm-20250228-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-f012a9f |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 24.7 ms                                                                | 24.3 ms: 1.02x faster                                                 |
| regex_effbot   | 2.84 ms                                                                | 2.82 ms: 1.01x faster                                                 |
| regex_dna      | 177 ms                                                                 | 184 ms: 1.04x slower                                                  |
| regex_compile  | 123 ms                                                                 | 152 ms: 1.24x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.06x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250228-vultr-x86_64-python-75f38af7810af1c3ca56-3.14.0a5+-75f38af | bm-20250228-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-f012a9f |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 89.6 ms                                                                | 88.1 ms: 1.02x faster                                                 |
| xml_etree_parse      | 128 ms                                                                 | 128 ms: 1.00x slower                                                  |
| json_loads           | 28.4 us                                                                | 29.3 us: 1.03x slower                                                 |
| unpickle_pure_python | 208 us                                                                 | 234 us: 1.13x slower                                                  |
| xml_etree_generate   | 82.8 ms                                                                | 95.7 ms: 1.16x slower                                                 |
| json_dumps           | 11.0 ms                                                                | 12.7 ms: 1.16x slower                                                 |
| pickle_pure_python   | 297 us                                                                 | 344 us: 1.16x slower                                                  |
| xml_etree_process    | 57.7 ms                                                                | 68.8 ms: 1.19x slower                                                 |
| tomli_loads          | 1.87 sec                                                               | 2.25 sec: 1.20x slower                                                |
| Geometric mean       | (ref)                                                                  | 1.11x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250228-vultr-x86_64-python-75f38af7810af1c3ca56-3.14.0a5+-75f38af | bm-20250228-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-f012a9f |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 14.8 ms                                                                | 15.7 ms: 1.06x slower                                                 |
| python_startup_no_site | 7.52 ms                                                                | 9.67 ms: 1.29x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.17x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250228-vultr-x86_64-python-75f38af7810af1c3ca56-3.14.0a5+-75f38af | bm-20250228-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-f012a9f |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 47.6 ms                                                                | 57.4 ms: 1.21x slower                                                 |
| django_template | 33.1 ms                                                                | 42.6 ms: 1.29x slower                                                 |
| genshi_text     | 20.3 ms                                                                | 26.5 ms: 1.31x slower                                                 |
| mako            | 11.3 ms                                                                | 15.4 ms: 1.36x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.29x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20250228-vultr-x86_64-python-75f38af7810af1c3ca56-3.14.0a5+-75f38af | bm-20250228-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-f012a9f |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal               | 4.45 ms                                                                | 1.74 ms: 2.57x faster                                                 |
| sqlglot_normalize          | 277 ms                                                                 | 119 ms: 2.33x faster                                                  |
| create_gc_cycles           | 1.83 ms                                                                | 1.33 ms: 1.37x faster                                                 |
| async_tree_io_tg           | 600 ms                                                                 | 537 ms: 1.12x faster                                                  |
| async_tree_none_tg         | 253 ms                                                                 | 229 ms: 1.10x faster                                                  |
| sqlite_synth               | 2.18 us                                                                | 2.01 us: 1.08x faster                                                 |
| async_tree_io              | 604 ms                                                                 | 572 ms: 1.06x faster                                                  |
| async_tree_memoization_tg  | 308 ms                                                                 | 299 ms: 1.03x faster                                                  |
| regex_v8                   | 24.7 ms                                                                | 24.3 ms: 1.02x faster                                                 |
| xml_etree_iterparse        | 89.6 ms                                                                | 88.1 ms: 1.02x faster                                                 |
| regex_effbot               | 2.84 ms                                                                | 2.82 ms: 1.01x faster                                                 |
| float                      | 70.3 ms                                                                | 69.9 ms: 1.01x faster                                                 |
| xml_etree_parse            | 128 ms                                                                 | 128 ms: 1.00x slower                                                  |
| async_tree_cpu_io_mixed_tg | 472 ms                                                                 | 485 ms: 1.03x slower                                                  |
| json_loads                 | 28.4 us                                                                | 29.3 us: 1.03x slower                                                 |
| regex_dna                  | 177 ms                                                                 | 184 ms: 1.04x slower                                                  |
| pathlib                    | 18.8 ms                                                                | 19.5 ms: 1.04x slower                                                 |
| logging_silent             | 102 ns                                                                 | 107 ns: 1.05x slower                                                  |
| async_tree_none            | 259 ms                                                                 | 271 ms: 1.05x slower                                                  |
| pidigits                   | 187 ms                                                                 | 198 ms: 1.05x slower                                                  |
| async_tree_memoization     | 313 ms                                                                 | 331 ms: 1.06x slower                                                  |
| python_startup             | 14.8 ms                                                                | 15.7 ms: 1.06x slower                                                 |
| pycparser                  | 1.09 sec                                                               | 1.17 sec: 1.07x slower                                                |
| async_tree_cpu_io_mixed    | 485 ms                                                                 | 521 ms: 1.07x slower                                                  |
| bench_mp_pool              | 88.1 ms                                                                | 95.0 ms: 1.08x slower                                                 |
| scimark_fft                | 309 ms                                                                 | 342 ms: 1.11x slower                                                  |
| dulwich_log                | 74.8 ms                                                                | 82.8 ms: 1.11x slower                                                 |
| bpe_tokeniser              | 4.15 sec                                                               | 4.60 sec: 1.11x slower                                                |
| k_core                     | 2.03 sec                                                               | 2.26 sec: 1.11x slower                                                |
| docutils                   | 2.51 sec                                                               | 2.79 sec: 1.11x slower                                                |
| coroutines                 | 21.3 ms                                                                | 23.8 ms: 1.12x slower                                                 |
| unpickle_pure_python       | 208 us                                                                 | 234 us: 1.13x slower                                                  |
| sphinx                     | 969 ms                                                                 | 1.10 sec: 1.14x slower                                                |
| scimark_sor                | 110 ms                                                                 | 126 ms: 1.14x slower                                                  |
| many_optionals             | 999 us                                                                 | 1.14 ms: 1.14x slower                                                 |
| async_generators           | 320 ms                                                                 | 369 ms: 1.15x slower                                                  |
| telco                      | 7.27 ms                                                                | 8.39 ms: 1.15x slower                                                 |
| xml_etree_generate         | 82.8 ms                                                                | 95.7 ms: 1.16x slower                                                 |
| json_dumps                 | 11.0 ms                                                                | 12.7 ms: 1.16x slower                                                 |
| pickle_pure_python         | 297 us                                                                 | 344 us: 1.16x slower                                                  |
| pylint                     | 272 ms                                                                 | 316 ms: 1.16x slower                                                  |
| pprint_safe_repr           | 680 ms                                                                 | 793 ms: 1.17x slower                                                  |
| pyflate                    | 405 ms                                                                 | 474 ms: 1.17x slower                                                  |
| deepcopy_reduce            | 2.57 us                                                                | 3.02 us: 1.18x slower                                                 |
| scimark_sparse_mat_mult    | 4.38 ms                                                                | 5.15 ms: 1.18x slower                                                 |
| go                         | 110 ms                                                                 | 129 ms: 1.18x slower                                                  |
| subparsers                 | 21.5 ms                                                                | 25.4 ms: 1.18x slower                                                 |
| raytrace                   | 254 ms                                                                 | 299 ms: 1.18x slower                                                  |
| pprint_pformat             | 1.39 sec                                                               | 1.64 sec: 1.18x slower                                                |
| mdp                        | 2.30 sec                                                               | 2.72 sec: 1.19x slower                                                |
| sqlglot_transpile          | 1.53 ms                                                                | 1.83 ms: 1.19x slower                                                 |
| xml_etree_process          | 57.7 ms                                                                | 68.8 ms: 1.19x slower                                                 |
| deepcopy                   | 245 us                                                                 | 293 us: 1.19x slower                                                  |
| sqlglot_optimize           | 50.6 ms                                                                | 60.4 ms: 1.19x slower                                                 |
| deltablue                  | 3.01 ms                                                                | 3.61 ms: 1.20x slower                                                 |
| 2to3                       | 247 ms                                                                 | 297 ms: 1.20x slower                                                  |
| tomli_loads                | 1.87 sec                                                               | 2.25 sec: 1.20x slower                                                |
| genshi_xml                 | 47.6 ms                                                                | 57.4 ms: 1.21x slower                                                 |
| spectral_norm              | 88.6 ms                                                                | 107 ms: 1.21x slower                                                  |
| comprehensions             | 15.9 us                                                                | 19.2 us: 1.21x slower                                                 |
| logging_simple             | 5.94 us                                                                | 7.22 us: 1.22x slower                                                 |
| generators                 | 26.9 ms                                                                | 32.7 ms: 1.22x slower                                                 |
| sqlglot_parse              | 1.24 ms                                                                | 1.51 ms: 1.22x slower                                                 |
| sympy_expand               | 452 ms                                                                 | 551 ms: 1.22x slower                                                  |
| thrift                     | 705 us                                                                 | 859 us: 1.22x slower                                                  |
| scimark_monte_carlo        | 62.5 ms                                                                | 76.4 ms: 1.22x slower                                                 |
| logging_format             | 6.71 us                                                                | 8.20 us: 1.22x slower                                                 |
| chaos                      | 53.7 ms                                                                | 65.9 ms: 1.23x slower                                                 |
| sympy_integrate            | 19.3 ms                                                                | 23.6 ms: 1.23x slower                                                 |
| scimark_lu                 | 111 ms                                                                 | 137 ms: 1.23x slower                                                  |
| coverage                   | 79.0 ms                                                                | 97.5 ms: 1.23x slower                                                 |
| deepcopy_memo              | 28.7 us                                                                | 35.4 us: 1.23x slower                                                 |
| regex_compile              | 123 ms                                                                 | 152 ms: 1.24x slower                                                  |
| connected_components       | 392 ms                                                                 | 484 ms: 1.24x slower                                                  |
| sympy_str                  | 267 ms                                                                 | 331 ms: 1.24x slower                                                  |
| sympy_sum                  | 150 ms                                                                 | 186 ms: 1.24x slower                                                  |
| fannkuch                   | 372 ms                                                                 | 462 ms: 1.24x slower                                                  |
| sqlalchemy_declarative     | 125 ms                                                                 | 156 ms: 1.25x slower                                                  |
| hexiom                     | 5.69 ms                                                                | 7.10 ms: 1.25x slower                                                 |
| shortest_path              | 427 ms                                                                 | 536 ms: 1.26x slower                                                  |
| typing_runtime_protocols   | 152 us                                                                 | 192 us: 1.26x slower                                                  |
| nqueens                    | 74.4 ms                                                                | 94.0 ms: 1.26x slower                                                 |
| sqlalchemy_imperative      | 18.9 ms                                                                | 23.9 ms: 1.27x slower                                                 |
| richards                   | 41.2 ms                                                                | 52.8 ms: 1.28x slower                                                 |
| python_startup_no_site     | 7.52 ms                                                                | 9.67 ms: 1.29x slower                                                 |
| django_template            | 33.1 ms                                                                | 42.6 ms: 1.29x slower                                                 |
| meteor_contest             | 99.4 ms                                                                | 129 ms: 1.30x slower                                                  |
| crypto_pyaes               | 65.6 ms                                                                | 85.0 ms: 1.30x slower                                                 |
| richards_super             | 47.1 ms                                                                | 61.2 ms: 1.30x slower                                                 |
| genshi_text                | 20.3 ms                                                                | 26.5 ms: 1.31x slower                                                 |
| mako                       | 11.3 ms                                                                | 15.4 ms: 1.36x slower                                                 |
| nbody                      | 84.2 ms                                                                | 119 ms: 1.41x slower                                                  |
| bench_thread_pool          | 1.03 ms                                                                | 3.29 ms: 3.20x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.13x slower                                                          |

Benchmark hidden because not significant (2): asyncio_websockets, json
Ignored benchmarks (1) of results/bm-20250228-3.14.0a5+-f012a9f-NOGIL/bm-20250228-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-f012a9f.json: html5lib

- Geometric mean (including insignificant results): 1.108x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.12x
- 95% likely to have a slowdown of 1.12x
- 99% likely to have a slowdown of 1.10x

# Memory
- memory change: 1.21x