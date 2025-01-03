# Results vs. default_base_vs_NOGIL

- fork: mpage
- ref: measure_non_deferred
- machine: linux-x86_64
- commit hash: b4b58dd
- commit date: 2025-01-03
- overall geometric mean: 1.141x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.12x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e | bm-20250103-vultr-x86_64-mpage-measure_non_deferred-3.14.0a3+-b4b58dd |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 254 ms                                                                 | 312 ms: 1.23x slower                                                  |
| docutils       | 2.55 sec                                                               | 2.80 sec: 1.10x slower                                                |
| sphinx         | 981 ms                                                                 | 1.11 sec: 1.14x slower                                                |
| Geometric mean | (ref)                                                                  | 1.15x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e | bm-20250103-vultr-x86_64-mpage-measure_non_deferred-3.14.0a3+-b4b58dd |
|---------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none_tg        | 250 ms                                                                 | 232 ms: 1.07x faster                                                  |
| async_tree_io_tg          | 603 ms                                                                 | 574 ms: 1.05x faster                                                  |
| async_tree_io             | 609 ms                                                                 | 600 ms: 1.01x faster                                                  |
| asyncio_websockets        | 523 ms                                                                 | 518 ms: 1.01x faster                                                  |
| async_tree_memoization_tg | 298 ms                                                                 | 303 ms: 1.02x slower                                                  |
| async_tree_none           | 272 ms                                                                 | 277 ms: 1.02x slower                                                  |
| async_tree_cpu_io_mixed   | 499 ms                                                                 | 514 ms: 1.03x slower                                                  |
| async_tree_memoization    | 327 ms                                                                 | 341 ms: 1.04x slower                                                  |
| async_generators          | 355 ms                                                                 | 419 ms: 1.18x slower                                                  |
| coroutines                | 20.8 ms                                                                | 25.2 ms: 1.21x slower                                                 |
| Geometric mean            | (ref)                                                                  | 1.03x slower                                                          |

Benchmark hidden because not significant (1): async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e | bm-20250103-vultr-x86_64-mpage-measure_non_deferred-3.14.0a3+-b4b58dd |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 192 ms                                                                 | 183 ms: 1.05x faster                                                  |
| float          | 72.2 ms                                                                | 79.9 ms: 1.11x slower                                                 |
| nbody          | 92.1 ms                                                                | 132 ms: 1.43x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.15x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e | bm-20250103-vultr-x86_64-mpage-measure_non_deferred-3.14.0a3+-b4b58dd |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 25.0 ms                                                                | 24.4 ms: 1.02x faster                                                 |
| regex_effbot   | 2.83 ms                                                                | 2.80 ms: 1.01x faster                                                 |
| regex_dna      | 182 ms                                                                 | 186 ms: 1.02x slower                                                  |
| regex_compile  | 127 ms                                                                 | 151 ms: 1.18x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.04x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e | bm-20250103-vultr-x86_64-mpage-measure_non_deferred-3.14.0a3+-b4b58dd |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 90.4 ms                                                                | 88.2 ms: 1.03x faster                                                 |
| xml_etree_parse      | 127 ms                                                                 | 130 ms: 1.02x slower                                                  |
| json_loads           | 25.9 us                                                                | 27.7 us: 1.07x slower                                                 |
| json_dumps           | 11.2 ms                                                                | 12.9 ms: 1.15x slower                                                 |
| xml_etree_generate   | 82.7 ms                                                                | 95.9 ms: 1.16x slower                                                 |
| pickle_pure_python   | 312 us                                                                 | 363 us: 1.16x slower                                                  |
| xml_etree_process    | 58.0 ms                                                                | 68.7 ms: 1.18x slower                                                 |
| unpickle_pure_python | 211 us                                                                 | 254 us: 1.20x slower                                                  |
| tomli_loads          | 1.88 sec                                                               | 2.52 sec: 1.34x slower                                                |
| Geometric mean       | (ref)                                                                  | 1.14x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e | bm-20250103-vultr-x86_64-mpage-measure_non_deferred-3.14.0a3+-b4b58dd |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 14.7 ms                                                                | 15.5 ms: 1.05x slower                                                 |
| python_startup_no_site | 7.51 ms                                                                | 9.70 ms: 1.29x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.17x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e | bm-20250103-vultr-x86_64-mpage-measure_non_deferred-3.14.0a3+-b4b58dd |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.8 ms                                                                | 43.2 ms: 1.24x slower                                                 |
| genshi_xml      | 48.3 ms                                                                | 60.0 ms: 1.24x slower                                                 |
| mako            | 11.7 ms                                                                | 15.7 ms: 1.35x slower                                                 |
| genshi_text     | 21.1 ms                                                                | 28.4 ms: 1.35x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.29x slower                                                          |

All benchmarks:
===============

| Benchmark                 | bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e | bm-20250103-vultr-x86_64-mpage-measure_non_deferred-3.14.0a3+-b4b58dd |
|---------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal              | 4.29 ms                                                                | 3.30 ms: 1.30x faster                                                 |
| async_tree_none_tg        | 250 ms                                                                 | 232 ms: 1.07x faster                                                  |
| sqlite_synth              | 2.21 us                                                                | 2.08 us: 1.06x faster                                                 |
| async_tree_io_tg          | 603 ms                                                                 | 574 ms: 1.05x faster                                                  |
| pidigits                  | 192 ms                                                                 | 183 ms: 1.05x faster                                                  |
| xml_etree_iterparse       | 90.4 ms                                                                | 88.2 ms: 1.03x faster                                                 |
| regex_v8                  | 25.0 ms                                                                | 24.4 ms: 1.02x faster                                                 |
| create_gc_cycles          | 1.84 ms                                                                | 1.80 ms: 1.02x faster                                                 |
| async_tree_io             | 609 ms                                                                 | 600 ms: 1.01x faster                                                  |
| regex_effbot              | 2.83 ms                                                                | 2.80 ms: 1.01x faster                                                 |
| asyncio_websockets        | 523 ms                                                                 | 518 ms: 1.01x faster                                                  |
| async_tree_memoization_tg | 298 ms                                                                 | 303 ms: 1.02x slower                                                  |
| async_tree_none           | 272 ms                                                                 | 277 ms: 1.02x slower                                                  |
| regex_dna                 | 182 ms                                                                 | 186 ms: 1.02x slower                                                  |
| xml_etree_parse           | 127 ms                                                                 | 130 ms: 1.02x slower                                                  |
| async_tree_cpu_io_mixed   | 499 ms                                                                 | 514 ms: 1.03x slower                                                  |
| pathlib                   | 18.0 ms                                                                | 18.6 ms: 1.03x slower                                                 |
| json                      | 4.72 ms                                                                | 4.89 ms: 1.04x slower                                                 |
| async_tree_memoization    | 327 ms                                                                 | 341 ms: 1.04x slower                                                  |
| python_startup            | 14.7 ms                                                                | 15.5 ms: 1.05x slower                                                 |
| mdp                       | 2.44 sec                                                               | 2.61 sec: 1.07x slower                                                |
| json_loads                | 25.9 us                                                                | 27.7 us: 1.07x slower                                                 |
| pycparser                 | 1.12 sec                                                               | 1.21 sec: 1.08x slower                                                |
| bench_mp_pool             | 89.5 ms                                                                | 97.8 ms: 1.09x slower                                                 |
| docutils                  | 2.55 sec                                                               | 2.80 sec: 1.10x slower                                                |
| dulwich_log               | 74.6 ms                                                                | 82.1 ms: 1.10x slower                                                 |
| logging_silent            | 103 ns                                                                 | 114 ns: 1.10x slower                                                  |
| float                     | 72.2 ms                                                                | 79.9 ms: 1.11x slower                                                 |
| bpe_tokeniser             | 4.23 sec                                                               | 4.80 sec: 1.13x slower                                                |
| k_core                    | 2.04 sec                                                               | 2.31 sec: 1.14x slower                                                |
| sphinx                    | 981 ms                                                                 | 1.11 sec: 1.14x slower                                                |
| generators                | 27.3 ms                                                                | 31.0 ms: 1.14x slower                                                 |
| json_dumps                | 11.2 ms                                                                | 12.9 ms: 1.15x slower                                                 |
| subparsers                | 22.0 ms                                                                | 25.4 ms: 1.15x slower                                                 |
| many_optionals            | 1.03 ms                                                                | 1.18 ms: 1.15x slower                                                 |
| sqlglot_normalize         | 103 ms                                                                 | 119 ms: 1.16x slower                                                  |
| telco                     | 7.27 ms                                                                | 8.43 ms: 1.16x slower                                                 |
| xml_etree_generate        | 82.7 ms                                                                | 95.9 ms: 1.16x slower                                                 |
| pickle_pure_python        | 312 us                                                                 | 363 us: 1.16x slower                                                  |
| pylint                    | 278 ms                                                                 | 326 ms: 1.17x slower                                                  |
| async_generators          | 355 ms                                                                 | 419 ms: 1.18x slower                                                  |
| regex_compile             | 127 ms                                                                 | 151 ms: 1.18x slower                                                  |
| xml_etree_process         | 58.0 ms                                                                | 68.7 ms: 1.18x slower                                                 |
| sqlglot_optimize          | 52.1 ms                                                                | 61.7 ms: 1.19x slower                                                 |
| sympy_expand              | 458 ms                                                                 | 546 ms: 1.19x slower                                                  |
| pprint_safe_repr          | 685 ms                                                                 | 822 ms: 1.20x slower                                                  |
| unpickle_pure_python      | 211 us                                                                 | 254 us: 1.20x slower                                                  |
| sympy_sum                 | 153 ms                                                                 | 185 ms: 1.20x slower                                                  |
| crypto_pyaes              | 66.5 ms                                                                | 80.2 ms: 1.21x slower                                                 |
| coroutines                | 20.8 ms                                                                | 25.2 ms: 1.21x slower                                                 |
| thrift                    | 729 us                                                                 | 885 us: 1.21x slower                                                  |
| pprint_pformat            | 1.40 sec                                                               | 1.70 sec: 1.22x slower                                                |
| scimark_fft               | 313 ms                                                                 | 382 ms: 1.22x slower                                                  |
| deepcopy                  | 255 us                                                                 | 311 us: 1.22x slower                                                  |
| spectral_norm             | 93.8 ms                                                                | 115 ms: 1.22x slower                                                  |
| sympy_integrate           | 19.6 ms                                                                | 24.1 ms: 1.23x slower                                                 |
| 2to3                      | 254 ms                                                                 | 312 ms: 1.23x slower                                                  |
| scimark_sparse_mat_mult   | 4.43 ms                                                                | 5.44 ms: 1.23x slower                                                 |
| logging_simple            | 5.94 us                                                                | 7.29 us: 1.23x slower                                                 |
| sympy_str                 | 270 ms                                                                 | 332 ms: 1.23x slower                                                  |
| sqlglot_transpile         | 1.55 ms                                                                | 1.90 ms: 1.23x slower                                                 |
| comprehensions            | 17.0 us                                                                | 21.0 us: 1.24x slower                                                 |
| chaos                     | 57.7 ms                                                                | 71.4 ms: 1.24x slower                                                 |
| django_template           | 34.8 ms                                                                | 43.2 ms: 1.24x slower                                                 |
| logging_format            | 6.72 us                                                                | 8.34 us: 1.24x slower                                                 |
| coverage                  | 79.8 ms                                                                | 99.2 ms: 1.24x slower                                                 |
| genshi_xml                | 48.3 ms                                                                | 60.0 ms: 1.24x slower                                                 |
| pyflate                   | 413 ms                                                                 | 515 ms: 1.25x slower                                                  |
| nqueens                   | 78.1 ms                                                                | 97.8 ms: 1.25x slower                                                 |
| raytrace                  | 259 ms                                                                 | 324 ms: 1.25x slower                                                  |
| deepcopy_reduce           | 2.56 us                                                                | 3.21 us: 1.25x slower                                                 |
| sqlalchemy_imperative     | 19.0 ms                                                                | 23.8 ms: 1.26x slower                                                 |
| go                        | 115 ms                                                                 | 144 ms: 1.26x slower                                                  |
| shortest_path             | 430 ms                                                                 | 541 ms: 1.26x slower                                                  |
| scimark_lu                | 111 ms                                                                 | 140 ms: 1.26x slower                                                  |
| connected_components      | 389 ms                                                                 | 490 ms: 1.26x slower                                                  |
| sqlalchemy_declarative    | 127 ms                                                                 | 161 ms: 1.26x slower                                                  |
| scimark_monte_carlo       | 63.0 ms                                                                | 79.8 ms: 1.27x slower                                                 |
| sqlglot_parse             | 1.24 ms                                                                | 1.57 ms: 1.27x slower                                                 |
| python_startup_no_site    | 7.51 ms                                                                | 9.70 ms: 1.29x slower                                                 |
| hexiom                    | 5.93 ms                                                                | 7.67 ms: 1.29x slower                                                 |
| typing_runtime_protocols  | 154 us                                                                 | 200 us: 1.30x slower                                                  |
| richards                  | 41.9 ms                                                                | 55.0 ms: 1.31x slower                                                 |
| deepcopy_memo             | 29.4 us                                                                | 38.9 us: 1.32x slower                                                 |
| meteor_contest            | 99.3 ms                                                                | 132 ms: 1.33x slower                                                  |
| tomli_loads               | 1.88 sec                                                               | 2.52 sec: 1.34x slower                                                |
| mako                      | 11.7 ms                                                                | 15.7 ms: 1.35x slower                                                 |
| genshi_text               | 21.1 ms                                                                | 28.4 ms: 1.35x slower                                                 |
| richards_super            | 48.0 ms                                                                | 64.7 ms: 1.35x slower                                                 |
| fannkuch                  | 364 ms                                                                 | 499 ms: 1.37x slower                                                  |
| deltablue                 | 3.11 ms                                                                | 4.41 ms: 1.42x slower                                                 |
| nbody                     | 92.1 ms                                                                | 132 ms: 1.43x slower                                                  |
| scimark_sor               | 113 ms                                                                 | 164 ms: 1.44x slower                                                  |
| bench_thread_pool         | 1.03 ms                                                                | 3.32 ms: 3.23x slower                                                 |
| Geometric mean            | (ref)                                                                  | 1.18x slower                                                          |

Benchmark hidden because not significant (1): async_tree_cpu_io_mixed_tg
Ignored benchmarks (1) of results/bm-20250103-3.14.0a3+-b4b58dd-NOGIL/bm-20250103-vultr-x86_64-mpage-measure_non_deferred-3.14.0a3+-b4b58dd.json: html5lib

- Geometric mean (including insignificant results): 1.141x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.15x
- 95% likely to have a slowdown of 1.13x
- 99% likely to have a slowdown of 1.12x

# Memory
- memory change: 1.19x