# Results vs. default_base_vs_NOGIL

- fork: mpage
- ref: measure_interp_loop_
- machine: linux-x86_64
- commit hash: 5264e56
- commit date: 2025-03-15
- overall geometric mean: 1.092x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 | bm-20250315-vultr-x86_64-mpage-measure_interp_loop_-3.14.0a5+-5264e56 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 258 ms                                                                 | 296 ms: 1.15x slower                                                  |
| docutils       | 2.61 sec                                                               | 2.77 sec: 1.06x slower                                                |
| sphinx         | 995 ms                                                                 | 1.09 sec: 1.10x slower                                                |
| Geometric mean | (ref)                                                                  | 1.10x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 | bm-20250315-vultr-x86_64-mpage-measure_interp_loop_-3.14.0a5+-5264e56 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 628 ms                                                                 | 536 ms: 1.17x faster                                                  |
| async_tree_none_tg         | 267 ms                                                                 | 231 ms: 1.16x faster                                                  |
| async_tree_io              | 630 ms                                                                 | 576 ms: 1.09x faster                                                  |
| async_tree_memoization_tg  | 318 ms                                                                 | 300 ms: 1.06x faster                                                  |
| async_tree_cpu_io_mixed_tg | 504 ms                                                                 | 484 ms: 1.04x faster                                                  |
| async_tree_none            | 277 ms                                                                 | 270 ms: 1.03x faster                                                  |
| coroutines                 | 23.4 ms                                                                | 23.1 ms: 1.01x faster                                                 |
| async_tree_memoization     | 329 ms                                                                 | 333 ms: 1.01x slower                                                  |
| async_generators           | 339 ms                                                                 | 372 ms: 1.10x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.04x faster                                                          |

Benchmark hidden because not significant (2): asyncio_websockets, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 | bm-20250315-vultr-x86_64-mpage-measure_interp_loop_-3.14.0a5+-5264e56 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 75.8 ms                                                                | 73.3 ms: 1.03x faster                                                 |
| pidigits       | 187 ms                                                                 | 191 ms: 1.02x slower                                                  |
| nbody          | 102 ms                                                                 | 125 ms: 1.22x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.07x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 | bm-20250315-vultr-x86_64-mpage-measure_interp_loop_-3.14.0a5+-5264e56 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 2.77 ms                                                                | 2.66 ms: 1.04x faster                                                 |
| regex_v8       | 24.5 ms                                                                | 23.7 ms: 1.04x faster                                                 |
| regex_dna      | 179 ms                                                                 | 180 ms: 1.00x slower                                                  |
| regex_compile  | 130 ms                                                                 | 155 ms: 1.20x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 | bm-20250315-vultr-x86_64-mpage-measure_interp_loop_-3.14.0a5+-5264e56 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 93.4 ms                                                                | 88.6 ms: 1.05x faster                                                 |
| xml_etree_parse      | 130 ms                                                                 | 129 ms: 1.01x faster                                                  |
| json_loads           | 27.0 us                                                                | 29.5 us: 1.09x slower                                                 |
| pickle_pure_python   | 324 us                                                                 | 356 us: 1.10x slower                                                  |
| unpickle_pure_python | 224 us                                                                 | 250 us: 1.11x slower                                                  |
| xml_etree_generate   | 86.5 ms                                                                | 96.9 ms: 1.12x slower                                                 |
| json_dumps           | 11.2 ms                                                                | 12.7 ms: 1.13x slower                                                 |
| tomli_loads          | 2.00 sec                                                               | 2.33 sec: 1.16x slower                                                |
| xml_etree_process    | 60.1 ms                                                                | 70.0 ms: 1.17x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.09x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 | bm-20250315-vultr-x86_64-mpage-measure_interp_loop_-3.14.0a5+-5264e56 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 14.9 ms                                                                | 15.7 ms: 1.05x slower                                                 |
| python_startup_no_site | 8.63 ms                                                                | 11.1 ms: 1.29x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.17x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 | bm-20250315-vultr-x86_64-mpage-measure_interp_loop_-3.14.0a5+-5264e56 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 37.2 ms                                                                | 42.1 ms: 1.13x slower                                                 |
| genshi_xml      | 51.0 ms                                                                | 59.9 ms: 1.17x slower                                                 |
| genshi_text     | 21.9 ms                                                                | 28.0 ms: 1.28x slower                                                 |
| mako            | 12.1 ms                                                                | 15.8 ms: 1.31x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.22x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 | bm-20250315-vultr-x86_64-mpage-measure_interp_loop_-3.14.0a5+-5264e56 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal               | 4.76 ms                                                                | 1.71 ms: 2.78x faster                                                 |
| create_gc_cycles           | 1.83 ms                                                                | 1.29 ms: 1.41x faster                                                 |
| async_tree_io_tg           | 628 ms                                                                 | 536 ms: 1.17x faster                                                  |
| async_tree_none_tg         | 267 ms                                                                 | 231 ms: 1.16x faster                                                  |
| sqlite_synth               | 2.21 us                                                                | 2.02 us: 1.10x faster                                                 |
| async_tree_io              | 630 ms                                                                 | 576 ms: 1.09x faster                                                  |
| async_tree_memoization_tg  | 318 ms                                                                 | 300 ms: 1.06x faster                                                  |
| xml_etree_iterparse        | 93.4 ms                                                                | 88.6 ms: 1.05x faster                                                 |
| regex_effbot               | 2.77 ms                                                                | 2.66 ms: 1.04x faster                                                 |
| async_tree_cpu_io_mixed_tg | 504 ms                                                                 | 484 ms: 1.04x faster                                                  |
| regex_v8                   | 24.5 ms                                                                | 23.7 ms: 1.04x faster                                                 |
| float                      | 75.8 ms                                                                | 73.3 ms: 1.03x faster                                                 |
| async_tree_none            | 277 ms                                                                 | 270 ms: 1.03x faster                                                  |
| coroutines                 | 23.4 ms                                                                | 23.1 ms: 1.01x faster                                                 |
| xml_etree_parse            | 130 ms                                                                 | 129 ms: 1.01x faster                                                  |
| pycparser                  | 1.16 sec                                                               | 1.17 sec: 1.00x slower                                                |
| regex_dna                  | 179 ms                                                                 | 180 ms: 1.00x slower                                                  |
| pathlib                    | 19.6 ms                                                                | 19.7 ms: 1.01x slower                                                 |
| async_tree_memoization     | 329 ms                                                                 | 333 ms: 1.01x slower                                                  |
| pidigits                   | 187 ms                                                                 | 191 ms: 1.02x slower                                                  |
| json                       | 4.89 ms                                                                | 5.11 ms: 1.04x slower                                                 |
| python_startup             | 14.9 ms                                                                | 15.7 ms: 1.05x slower                                                 |
| docutils                   | 2.61 sec                                                               | 2.77 sec: 1.06x slower                                                |
| bpe_tokeniser              | 4.43 sec                                                               | 4.76 sec: 1.07x slower                                                |
| dulwich_log                | 67.5 ms                                                                | 72.9 ms: 1.08x slower                                                 |
| bench_mp_pool              | 88.2 ms                                                                | 95.2 ms: 1.08x slower                                                 |
| generators                 | 29.7 ms                                                                | 32.4 ms: 1.09x slower                                                 |
| pylint                     | 285 ms                                                                 | 312 ms: 1.09x slower                                                  |
| json_loads                 | 27.0 us                                                                | 29.5 us: 1.09x slower                                                 |
| logging_silent             | 99.6 ns                                                                | 109 ns: 1.10x slower                                                  |
| async_generators           | 339 ms                                                                 | 372 ms: 1.10x slower                                                  |
| sphinx                     | 995 ms                                                                 | 1.09 sec: 1.10x slower                                                |
| pickle_pure_python         | 324 us                                                                 | 356 us: 1.10x slower                                                  |
| mdp                        | 2.50 sec                                                               | 2.77 sec: 1.11x slower                                                |
| subparsers                 | 22.7 ms                                                                | 25.2 ms: 1.11x slower                                                 |
| unpickle_pure_python       | 224 us                                                                 | 250 us: 1.11x slower                                                  |
| k_core                     | 2.06 sec                                                               | 2.30 sec: 1.12x slower                                                |
| many_optionals             | 1.04 ms                                                                | 1.16 ms: 1.12x slower                                                 |
| xml_etree_generate         | 86.5 ms                                                                | 96.9 ms: 1.12x slower                                                 |
| django_template            | 37.2 ms                                                                | 42.1 ms: 1.13x slower                                                 |
| json_dumps                 | 11.2 ms                                                                | 12.7 ms: 1.13x slower                                                 |
| thrift                     | 754 us                                                                 | 859 us: 1.14x slower                                                  |
| pprint_safe_repr           | 737 ms                                                                 | 841 ms: 1.14x slower                                                  |
| chaos                      | 58.5 ms                                                                | 66.9 ms: 1.14x slower                                                 |
| pyflate                    | 425 ms                                                                 | 486 ms: 1.14x slower                                                  |
| 2to3                       | 258 ms                                                                 | 296 ms: 1.15x slower                                                  |
| deepcopy_reduce            | 2.73 us                                                                | 3.13 us: 1.15x slower                                                 |
| pprint_pformat             | 1.50 sec                                                               | 1.73 sec: 1.15x slower                                                |
| sqlglot_normalize          | 104 ms                                                                 | 121 ms: 1.16x slower                                                  |
| telco                      | 7.64 ms                                                                | 8.85 ms: 1.16x slower                                                 |
| raytrace                   | 267 ms                                                                 | 310 ms: 1.16x slower                                                  |
| sqlglot_optimize           | 52.7 ms                                                                | 61.2 ms: 1.16x slower                                                 |
| tomli_loads                | 2.00 sec                                                               | 2.33 sec: 1.16x slower                                                |
| xml_etree_process          | 60.1 ms                                                                | 70.0 ms: 1.17x slower                                                 |
| logging_simple             | 6.05 us                                                                | 7.08 us: 1.17x slower                                                 |
| scimark_sor                | 116 ms                                                                 | 136 ms: 1.17x slower                                                  |
| genshi_xml                 | 51.0 ms                                                                | 59.9 ms: 1.17x slower                                                 |
| sqlglot_transpile          | 1.62 ms                                                                | 1.90 ms: 1.17x slower                                                 |
| sympy_expand               | 465 ms                                                                 | 552 ms: 1.19x slower                                                  |
| sqlalchemy_declarative     | 131 ms                                                                 | 156 ms: 1.19x slower                                                  |
| sympy_integrate            | 20.1 ms                                                                | 23.8 ms: 1.19x slower                                                 |
| spectral_norm              | 95.9 ms                                                                | 114 ms: 1.19x slower                                                  |
| scimark_fft                | 334 ms                                                                 | 398 ms: 1.19x slower                                                  |
| deepcopy                   | 261 us                                                                 | 311 us: 1.19x slower                                                  |
| deltablue                  | 3.12 ms                                                                | 3.72 ms: 1.19x slower                                                 |
| go                         | 113 ms                                                                 | 135 ms: 1.19x slower                                                  |
| scimark_sparse_mat_mult    | 4.70 ms                                                                | 5.61 ms: 1.19x slower                                                 |
| sympy_sum                  | 156 ms                                                                 | 186 ms: 1.19x slower                                                  |
| sqlglot_parse              | 1.32 ms                                                                | 1.57 ms: 1.19x slower                                                 |
| regex_compile              | 130 ms                                                                 | 155 ms: 1.20x slower                                                  |
| sympy_str                  | 278 ms                                                                 | 334 ms: 1.20x slower                                                  |
| sqlalchemy_imperative      | 19.8 ms                                                                | 23.7 ms: 1.20x slower                                                 |
| logging_format             | 6.73 us                                                                | 8.08 us: 1.20x slower                                                 |
| coverage                   | 81.1 ms                                                                | 97.6 ms: 1.20x slower                                                 |
| crypto_pyaes               | 71.5 ms                                                                | 86.6 ms: 1.21x slower                                                 |
| comprehensions             | 17.2 us                                                                | 20.9 us: 1.21x slower                                                 |
| nqueens                    | 81.4 ms                                                                | 98.9 ms: 1.21x slower                                                 |
| fannkuch                   | 401 ms                                                                 | 490 ms: 1.22x slower                                                  |
| nbody                      | 102 ms                                                                 | 125 ms: 1.22x slower                                                  |
| hexiom                     | 6.10 ms                                                                | 7.48 ms: 1.23x slower                                                 |
| scimark_monte_carlo        | 66.6 ms                                                                | 81.8 ms: 1.23x slower                                                 |
| richards                   | 42.7 ms                                                                | 52.4 ms: 1.23x slower                                                 |
| richards_super             | 49.8 ms                                                                | 61.2 ms: 1.23x slower                                                 |
| shortest_path              | 445 ms                                                                 | 548 ms: 1.23x slower                                                  |
| scimark_lu                 | 114 ms                                                                 | 141 ms: 1.23x slower                                                  |
| typing_runtime_protocols   | 158 us                                                                 | 196 us: 1.24x slower                                                  |
| deepcopy_memo              | 30.8 us                                                                | 38.3 us: 1.24x slower                                                 |
| connected_components       | 402 ms                                                                 | 502 ms: 1.25x slower                                                  |
| genshi_text                | 21.9 ms                                                                | 28.0 ms: 1.28x slower                                                 |
| python_startup_no_site     | 8.63 ms                                                                | 11.1 ms: 1.29x slower                                                 |
| meteor_contest             | 101 ms                                                                 | 131 ms: 1.29x slower                                                  |
| mako                       | 12.1 ms                                                                | 15.8 ms: 1.31x slower                                                 |
| bench_thread_pool          | 1.05 ms                                                                | 3.16 ms: 2.99x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.11x slower                                                          |

Benchmark hidden because not significant (2): asyncio_websockets, async_tree_cpu_io_mixed
Ignored benchmarks (1) of results/bm-20250315-3.14.0a5+-5264e56-NOGIL/bm-20250315-vultr-x86_64-mpage-measure_interp_loop_-3.14.0a5+-5264e56.json: html5lib

- Geometric mean (including insignificant results): 1.092x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.10x
- 95% likely to have a slowdown of 1.09x
- 99% likely to have a slowdown of 1.08x

# Memory
- memory change: 1.20x