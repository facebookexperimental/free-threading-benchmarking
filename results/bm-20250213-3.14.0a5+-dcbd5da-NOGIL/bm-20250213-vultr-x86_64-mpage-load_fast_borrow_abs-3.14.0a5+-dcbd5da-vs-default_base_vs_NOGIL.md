# Results vs. default_base_vs_NOGIL

- fork: mpage
- ref: load_fast_borrow_abs
- machine: linux-x86_64
- commit hash: dcbd5da
- commit date: 2025-02-13
- overall geometric mean: 1.081x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250213-vultr-x86_64-python-07f5e33f2eed50984d7a-3.14.0a5+-07f5e33 | bm-20250213-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-dcbd5da |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 256 ms                                                                 | 289 ms: 1.13x slower                                                  |
| docutils       | 2.56 sec                                                               | 2.73 sec: 1.07x slower                                                |
| sphinx         | 979 ms                                                                 | 1.08 sec: 1.10x slower                                                |
| Geometric mean | (ref)                                                                  | 1.10x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20250213-vultr-x86_64-python-07f5e33f2eed50984d7a-3.14.0a5+-07f5e33 | bm-20250213-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-dcbd5da |
|---------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg          | 631 ms                                                                 | 554 ms: 1.14x faster                                                  |
| async_tree_io             | 632 ms                                                                 | 583 ms: 1.08x faster                                                  |
| async_tree_none_tg        | 262 ms                                                                 | 248 ms: 1.06x faster                                                  |
| async_tree_memoization_tg | 320 ms                                                                 | 304 ms: 1.05x faster                                                  |
| coroutines                | 21.9 ms                                                                | 22.1 ms: 1.01x slower                                                 |
| async_tree_none           | 269 ms                                                                 | 276 ms: 1.03x slower                                                  |
| async_tree_memoization    | 323 ms                                                                 | 335 ms: 1.04x slower                                                  |
| async_tree_cpu_io_mixed   | 499 ms                                                                 | 523 ms: 1.05x slower                                                  |
| async_generators          | 322 ms                                                                 | 359 ms: 1.12x slower                                                  |
| Geometric mean            | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (2): asyncio_websockets, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250213-vultr-x86_64-python-07f5e33f2eed50984d7a-3.14.0a5+-07f5e33 | bm-20250213-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-dcbd5da |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 71.7 ms                                                                | 67.5 ms: 1.06x faster                                                 |
| pidigits       | 184 ms                                                                 | 209 ms: 1.14x slower                                                  |
| nbody          | 91.4 ms                                                                | 114 ms: 1.24x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.10x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250213-vultr-x86_64-python-07f5e33f2eed50984d7a-3.14.0a5+-07f5e33 | bm-20250213-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-dcbd5da |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 2.64 ms                                                                | 2.70 ms: 1.02x slower                                                 |
| regex_v8       | 23.3 ms                                                                | 23.8 ms: 1.02x slower                                                 |
| regex_dna      | 169 ms                                                                 | 180 ms: 1.07x slower                                                  |
| regex_compile  | 127 ms                                                                 | 141 ms: 1.11x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.06x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250213-vultr-x86_64-python-07f5e33f2eed50984d7a-3.14.0a5+-07f5e33 | bm-20250213-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-dcbd5da |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 91.4 ms                                                                | 85.5 ms: 1.07x faster                                                 |
| xml_etree_parse      | 128 ms                                                                 | 127 ms: 1.01x faster                                                  |
| unpickle_pure_python | 216 us                                                                 | 224 us: 1.03x slower                                                  |
| pickle_pure_python   | 314 us                                                                 | 326 us: 1.04x slower                                                  |
| tomli_loads          | 1.90 sec                                                               | 2.07 sec: 1.09x slower                                                |
| json_loads           | 28.4 us                                                                | 31.1 us: 1.10x slower                                                 |
| json_dumps           | 11.3 ms                                                                | 12.6 ms: 1.11x slower                                                 |
| xml_etree_generate   | 82.7 ms                                                                | 92.8 ms: 1.12x slower                                                 |
| xml_etree_process    | 57.9 ms                                                                | 66.7 ms: 1.15x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.06x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250213-vultr-x86_64-python-07f5e33f2eed50984d7a-3.14.0a5+-07f5e33 | bm-20250213-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-dcbd5da |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 14.7 ms                                                                | 15.3 ms: 1.05x slower                                                 |
| python_startup_no_site | 7.46 ms                                                                | 9.60 ms: 1.29x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.16x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250213-vultr-x86_64-python-07f5e33f2eed50984d7a-3.14.0a5+-07f5e33 | bm-20250213-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-dcbd5da |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 49.5 ms                                                                | 56.0 ms: 1.13x slower                                                 |
| django_template | 34.2 ms                                                                | 40.8 ms: 1.19x slower                                                 |
| genshi_text     | 21.6 ms                                                                | 26.0 ms: 1.20x slower                                                 |
| mako            | 11.8 ms                                                                | 15.0 ms: 1.27x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.20x slower                                                          |

All benchmarks:
===============

| Benchmark                 | bm-20250213-vultr-x86_64-python-07f5e33f2eed50984d7a-3.14.0a5+-07f5e33 | bm-20250213-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-dcbd5da |
|---------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal              | 4.45 ms                                                                | 1.74 ms: 2.56x faster                                                 |
| create_gc_cycles          | 1.83 ms                                                                | 1.39 ms: 1.32x faster                                                 |
| async_tree_io_tg          | 631 ms                                                                 | 554 ms: 1.14x faster                                                  |
| sqlite_synth              | 2.19 us                                                                | 2.01 us: 1.09x faster                                                 |
| async_tree_io             | 632 ms                                                                 | 583 ms: 1.08x faster                                                  |
| xml_etree_iterparse       | 91.4 ms                                                                | 85.5 ms: 1.07x faster                                                 |
| float                     | 71.7 ms                                                                | 67.5 ms: 1.06x faster                                                 |
| async_tree_none_tg        | 262 ms                                                                 | 248 ms: 1.06x faster                                                  |
| async_tree_memoization_tg | 320 ms                                                                 | 304 ms: 1.05x faster                                                  |
| logging_silent            | 105 ns                                                                 | 101 ns: 1.04x faster                                                  |
| xml_etree_parse           | 128 ms                                                                 | 127 ms: 1.01x faster                                                  |
| coroutines                | 21.9 ms                                                                | 22.1 ms: 1.01x slower                                                 |
| generators                | 29.0 ms                                                                | 29.3 ms: 1.01x slower                                                 |
| pycparser                 | 1.12 sec                                                               | 1.14 sec: 1.02x slower                                                |
| regex_effbot              | 2.64 ms                                                                | 2.70 ms: 1.02x slower                                                 |
| pathlib                   | 18.6 ms                                                                | 19.0 ms: 1.02x slower                                                 |
| regex_v8                  | 23.3 ms                                                                | 23.8 ms: 1.02x slower                                                 |
| scimark_sor               | 115 ms                                                                 | 117 ms: 1.02x slower                                                  |
| async_tree_none           | 269 ms                                                                 | 276 ms: 1.03x slower                                                  |
| unpickle_pure_python      | 216 us                                                                 | 224 us: 1.03x slower                                                  |
| pickle_pure_python        | 314 us                                                                 | 326 us: 1.04x slower                                                  |
| async_tree_memoization    | 323 ms                                                                 | 335 ms: 1.04x slower                                                  |
| go                        | 115 ms                                                                 | 120 ms: 1.04x slower                                                  |
| python_startup            | 14.7 ms                                                                | 15.3 ms: 1.05x slower                                                 |
| async_tree_cpu_io_mixed   | 499 ms                                                                 | 523 ms: 1.05x slower                                                  |
| bpe_tokeniser             | 4.18 sec                                                               | 4.42 sec: 1.06x slower                                                |
| json                      | 5.08 ms                                                                | 5.39 ms: 1.06x slower                                                 |
| dulwich_log               | 75.6 ms                                                                | 80.3 ms: 1.06x slower                                                 |
| docutils                  | 2.56 sec                                                               | 2.73 sec: 1.07x slower                                                |
| regex_dna                 | 169 ms                                                                 | 180 ms: 1.07x slower                                                  |
| bench_mp_pool             | 88.0 ms                                                                | 94.1 ms: 1.07x slower                                                 |
| pprint_safe_repr          | 698 ms                                                                 | 755 ms: 1.08x slower                                                  |
| deltablue                 | 3.16 ms                                                                | 3.43 ms: 1.09x slower                                                 |
| pyflate                   | 413 ms                                                                 | 450 ms: 1.09x slower                                                  |
| tomli_loads               | 1.90 sec                                                               | 2.07 sec: 1.09x slower                                                |
| pprint_pformat            | 1.42 sec                                                               | 1.55 sec: 1.09x slower                                                |
| json_loads                | 28.4 us                                                                | 31.1 us: 1.10x slower                                                 |
| sphinx                    | 979 ms                                                                 | 1.08 sec: 1.10x slower                                                |
| scimark_fft               | 319 ms                                                                 | 352 ms: 1.10x slower                                                  |
| k_core                    | 2.05 sec                                                               | 2.27 sec: 1.10x slower                                                |
| pylint                    | 279 ms                                                                 | 309 ms: 1.11x slower                                                  |
| mdp                       | 2.45 sec                                                               | 2.72 sec: 1.11x slower                                                |
| many_optionals            | 1.01 ms                                                                | 1.13 ms: 1.11x slower                                                 |
| regex_compile             | 127 ms                                                                 | 141 ms: 1.11x slower                                                  |
| json_dumps                | 11.3 ms                                                                | 12.6 ms: 1.11x slower                                                 |
| async_generators          | 322 ms                                                                 | 359 ms: 1.12x slower                                                  |
| telco                     | 7.34 ms                                                                | 8.20 ms: 1.12x slower                                                 |
| sqlglot_normalize         | 103 ms                                                                 | 115 ms: 1.12x slower                                                  |
| xml_etree_generate        | 82.7 ms                                                                | 92.8 ms: 1.12x slower                                                 |
| chaos                     | 56.3 ms                                                                | 63.4 ms: 1.13x slower                                                 |
| sqlglot_optimize          | 51.7 ms                                                                | 58.3 ms: 1.13x slower                                                 |
| 2to3                      | 256 ms                                                                 | 289 ms: 1.13x slower                                                  |
| genshi_xml                | 49.5 ms                                                                | 56.0 ms: 1.13x slower                                                 |
| hexiom                    | 5.92 ms                                                                | 6.71 ms: 1.13x slower                                                 |
| raytrace                  | 258 ms                                                                 | 293 ms: 1.13x slower                                                  |
| subparsers                | 21.8 ms                                                                | 24.8 ms: 1.13x slower                                                 |
| sqlglot_transpile         | 1.57 ms                                                                | 1.78 ms: 1.14x slower                                                 |
| pidigits                  | 184 ms                                                                 | 209 ms: 1.14x slower                                                  |
| deepcopy_memo             | 30.1 us                                                                | 34.5 us: 1.14x slower                                                 |
| deepcopy_reduce           | 2.61 us                                                                | 2.98 us: 1.14x slower                                                 |
| scimark_lu                | 112 ms                                                                 | 129 ms: 1.15x slower                                                  |
| nqueens                   | 79.6 ms                                                                | 91.4 ms: 1.15x slower                                                 |
| xml_etree_process         | 57.9 ms                                                                | 66.7 ms: 1.15x slower                                                 |
| spectral_norm             | 89.3 ms                                                                | 103 ms: 1.15x slower                                                  |
| sqlglot_parse             | 1.27 ms                                                                | 1.46 ms: 1.15x slower                                                 |
| scimark_monte_carlo       | 64.9 ms                                                                | 75.0 ms: 1.16x slower                                                 |
| logging_simple            | 5.93 us                                                                | 6.89 us: 1.16x slower                                                 |
| comprehensions            | 16.3 us                                                                | 19.0 us: 1.16x slower                                                 |
| scimark_sparse_mat_mult   | 4.50 ms                                                                | 5.24 ms: 1.17x slower                                                 |
| sympy_expand              | 455 ms                                                                 | 531 ms: 1.17x slower                                                  |
| deepcopy                  | 253 us                                                                 | 296 us: 1.17x slower                                                  |
| sympy_integrate           | 19.8 ms                                                                | 23.2 ms: 1.17x slower                                                 |
| fannkuch                  | 376 ms                                                                 | 446 ms: 1.19x slower                                                  |
| sympy_str                 | 270 ms                                                                 | 322 ms: 1.19x slower                                                  |
| django_template           | 34.2 ms                                                                | 40.8 ms: 1.19x slower                                                 |
| sympy_sum                 | 152 ms                                                                 | 181 ms: 1.19x slower                                                  |
| thrift                    | 739 us                                                                 | 882 us: 1.19x slower                                                  |
| richards                  | 42.3 ms                                                                | 50.6 ms: 1.20x slower                                                 |
| sqlalchemy_declarative    | 128 ms                                                                 | 153 ms: 1.20x slower                                                  |
| logging_format            | 6.56 us                                                                | 7.88 us: 1.20x slower                                                 |
| genshi_text               | 21.6 ms                                                                | 26.0 ms: 1.20x slower                                                 |
| connected_components      | 397 ms                                                                 | 479 ms: 1.21x slower                                                  |
| coverage                  | 79.1 ms                                                                | 95.6 ms: 1.21x slower                                                 |
| richards_super            | 48.1 ms                                                                | 58.9 ms: 1.22x slower                                                 |
| shortest_path             | 434 ms                                                                 | 533 ms: 1.23x slower                                                  |
| sqlalchemy_imperative     | 19.1 ms                                                                | 23.6 ms: 1.23x slower                                                 |
| crypto_pyaes              | 67.9 ms                                                                | 83.8 ms: 1.23x slower                                                 |
| nbody                     | 91.4 ms                                                                | 114 ms: 1.24x slower                                                  |
| meteor_contest            | 99.9 ms                                                                | 124 ms: 1.25x slower                                                  |
| typing_runtime_protocols  | 153 us                                                                 | 190 us: 1.25x slower                                                  |
| mako                      | 11.8 ms                                                                | 15.0 ms: 1.27x slower                                                 |
| python_startup_no_site    | 7.46 ms                                                                | 9.60 ms: 1.29x slower                                                 |
| bench_thread_pool         | 1.03 ms                                                                | 3.25 ms: 3.16x slower                                                 |
| Geometric mean            | (ref)                                                                  | 1.10x slower                                                          |

Benchmark hidden because not significant (2): asyncio_websockets, async_tree_cpu_io_mixed_tg
Ignored benchmarks (1) of results/bm-20250213-3.14.0a5+-dcbd5da-NOGIL/bm-20250213-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-dcbd5da.json: html5lib

- Geometric mean (including insignificant results): 1.081x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.08x
- 95% likely to have a slowdown of 1.08x
- 99% likely to have a slowdown of 1.07x

# Memory
- memory change: 1.20x