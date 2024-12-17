# Results vs. default_base_vs_NOGIL

- fork: corona10
- ref: gh_115999_BINARY_SUB
- machine: linux-x86_64
- commit hash: 3aa9426
- commit date: 2024-12-17
- overall geometric mean: 1.267x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.27x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-3aa9426 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 258 ms                                                                 | 368 ms: 1.42x slower                                                     |
| docutils       | 2.57 sec                                                               | 3.11 sec: 1.21x slower                                                   |
| sphinx         | 996 ms                                                                 | 1.19 sec: 1.20x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.27x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-3aa9426 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| asyncio_websockets         | 523 ms                                                                 | 518 ms: 1.01x faster                                                     |
| coroutines                 | 22.1 ms                                                                | 25.2 ms: 1.14x slower                                                    |
| async_tree_cpu_io_mixed_tg | 500 ms                                                                 | 622 ms: 1.25x slower                                                     |
| async_generators           | 363 ms                                                                 | 461 ms: 1.27x slower                                                     |
| async_tree_cpu_io_mixed    | 505 ms                                                                 | 651 ms: 1.29x slower                                                     |
| async_tree_none_tg         | 276 ms                                                                 | 358 ms: 1.30x slower                                                     |
| async_tree_io_tg           | 625 ms                                                                 | 827 ms: 1.32x slower                                                     |
| async_tree_memoization_tg  | 336 ms                                                                 | 445 ms: 1.33x slower                                                     |
| async_tree_memoization     | 345 ms                                                                 | 472 ms: 1.37x slower                                                     |
| async_tree_io              | 611 ms                                                                 | 849 ms: 1.39x slower                                                     |
| async_tree_none            | 277 ms                                                                 | 389 ms: 1.40x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.27x slower                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-3aa9426 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 186 ms                                                                 | 181 ms: 1.03x faster                                                     |
| nbody          | 95.2 ms                                                                | 132 ms: 1.39x slower                                                     |
| float          | 80.2 ms                                                                | 141 ms: 1.75x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.33x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-3aa9426 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_dna      | 180 ms                                                                 | 177 ms: 1.01x faster                                                     |
| regex_effbot   | 2.76 ms                                                                | 2.90 ms: 1.05x slower                                                    |
| regex_compile  | 130 ms                                                                 | 179 ms: 1.38x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.09x slower                                                             |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-3aa9426 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 90.5 ms                                                                | 91.9 ms: 1.02x slower                                                    |
| xml_etree_parse      | 127 ms                                                                 | 132 ms: 1.04x slower                                                     |
| json_loads           | 25.0 us                                                                | 28.7 us: 1.15x slower                                                    |
| xml_etree_generate   | 84.8 ms                                                                | 98.0 ms: 1.16x slower                                                    |
| json_dumps           | 11.5 ms                                                                | 14.2 ms: 1.23x slower                                                    |
| tomli_loads          | 2.13 sec                                                               | 2.69 sec: 1.26x slower                                                   |
| xml_etree_process    | 59.0 ms                                                                | 78.2 ms: 1.33x slower                                                    |
| unpickle_pure_python | 215 us                                                                 | 333 us: 1.55x slower                                                     |
| pickle_pure_python   | 321 us                                                                 | 517 us: 1.61x slower                                                     |
| Geometric mean       | (ref)                                                                  | 1.25x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-3aa9426 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                                | 17.5 ms: 1.20x slower                                                    |
| python_startup_no_site | 7.46 ms                                                                | 10.3 ms: 1.38x slower                                                    |
| Geometric mean         | (ref)                                                                  | 1.29x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-3aa9426 |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 50.6 ms                                                                | 64.7 ms: 1.28x slower                                                    |
| django_template | 35.5 ms                                                                | 51.4 ms: 1.45x slower                                                    |
| genshi_text     | 22.0 ms                                                                | 32.2 ms: 1.46x slower                                                    |
| mako            | 11.7 ms                                                                | 17.8 ms: 1.52x slower                                                    |
| Geometric mean  | (ref)                                                                  | 1.42x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-3aa9426 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal               | 4.04 ms                                                                | 3.52 ms: 1.15x faster                                                    |
| pidigits                   | 186 ms                                                                 | 181 ms: 1.03x faster                                                     |
| regex_dna                  | 180 ms                                                                 | 177 ms: 1.01x faster                                                     |
| asyncio_websockets         | 523 ms                                                                 | 518 ms: 1.01x faster                                                     |
| xml_etree_iterparse        | 90.5 ms                                                                | 91.9 ms: 1.02x slower                                                    |
| sqlite_synth               | 2.23 us                                                                | 2.27 us: 1.02x slower                                                    |
| xml_etree_parse            | 127 ms                                                                 | 132 ms: 1.04x slower                                                     |
| regex_effbot               | 2.76 ms                                                                | 2.90 ms: 1.05x slower                                                    |
| create_gc_cycles           | 1.70 ms                                                                | 1.84 ms: 1.08x slower                                                    |
| pathlib                    | 18.2 ms                                                                | 19.8 ms: 1.09x slower                                                    |
| json                       | 4.59 ms                                                                | 5.09 ms: 1.11x slower                                                    |
| spectral_norm              | 110 ms                                                                 | 126 ms: 1.14x slower                                                     |
| coroutines                 | 22.1 ms                                                                | 25.2 ms: 1.14x slower                                                    |
| mdp                        | 2.49 sec                                                               | 2.84 sec: 1.14x slower                                                   |
| json_loads                 | 25.0 us                                                                | 28.7 us: 1.15x slower                                                    |
| xml_etree_generate         | 84.8 ms                                                                | 98.0 ms: 1.16x slower                                                    |
| bpe_tokeniser              | 4.34 sec                                                               | 5.02 sec: 1.16x slower                                                   |
| telco                      | 7.31 ms                                                                | 8.67 ms: 1.19x slower                                                    |
| sphinx                     | 996 ms                                                                 | 1.19 sec: 1.20x slower                                                   |
| k_core                     | 2.02 sec                                                               | 2.42 sec: 1.20x slower                                                   |
| python_startup             | 14.6 ms                                                                | 17.5 ms: 1.20x slower                                                    |
| docutils                   | 2.57 sec                                                               | 3.11 sec: 1.21x slower                                                   |
| scimark_fft                | 338 ms                                                                 | 414 ms: 1.22x slower                                                     |
| json_dumps                 | 11.5 ms                                                                | 14.2 ms: 1.23x slower                                                    |
| nqueens                    | 79.0 ms                                                                | 98.0 ms: 1.24x slower                                                    |
| shortest_path              | 441 ms                                                                 | 548 ms: 1.24x slower                                                     |
| many_optionals             | 1.03 ms                                                                | 1.29 ms: 1.24x slower                                                    |
| async_tree_cpu_io_mixed_tg | 500 ms                                                                 | 622 ms: 1.25x slower                                                     |
| dulwich_log                | 76.4 ms                                                                | 95.7 ms: 1.25x slower                                                    |
| connected_components       | 399 ms                                                                 | 501 ms: 1.26x slower                                                     |
| deepcopy                   | 263 us                                                                 | 331 us: 1.26x slower                                                     |
| tomli_loads                | 2.13 sec                                                               | 2.69 sec: 1.26x slower                                                   |
| async_generators           | 363 ms                                                                 | 461 ms: 1.27x slower                                                     |
| bench_mp_pool              | 85.5 ms                                                                | 109 ms: 1.27x slower                                                     |
| sqlglot_normalize          | 108 ms                                                                 | 138 ms: 1.27x slower                                                     |
| genshi_xml                 | 50.6 ms                                                                | 64.7 ms: 1.28x slower                                                    |
| sqlglot_optimize           | 53.9 ms                                                                | 69.2 ms: 1.28x slower                                                    |
| meteor_contest             | 101 ms                                                                 | 130 ms: 1.29x slower                                                     |
| async_tree_cpu_io_mixed    | 505 ms                                                                 | 651 ms: 1.29x slower                                                     |
| coverage                   | 80.1 ms                                                                | 103 ms: 1.29x slower                                                     |
| async_tree_none_tg         | 276 ms                                                                 | 358 ms: 1.30x slower                                                     |
| deepcopy_memo              | 30.6 us                                                                | 39.9 us: 1.30x slower                                                    |
| typing_runtime_protocols   | 158 us                                                                 | 207 us: 1.31x slower                                                     |
| deepcopy_reduce            | 2.68 us                                                                | 3.53 us: 1.32x slower                                                    |
| async_tree_io_tg           | 625 ms                                                                 | 827 ms: 1.32x slower                                                     |
| async_tree_memoization_tg  | 336 ms                                                                 | 445 ms: 1.33x slower                                                     |
| xml_etree_process          | 59.0 ms                                                                | 78.2 ms: 1.33x slower                                                    |
| generators                 | 29.2 ms                                                                | 38.8 ms: 1.33x slower                                                    |
| crypto_pyaes               | 68.7 ms                                                                | 92.6 ms: 1.35x slower                                                    |
| pycparser                  | 1.13 sec                                                               | 1.53 sec: 1.35x slower                                                   |
| scimark_sparse_mat_mult    | 4.51 ms                                                                | 6.10 ms: 1.35x slower                                                    |
| pprint_safe_repr           | 723 ms                                                                 | 981 ms: 1.36x slower                                                     |
| pylint                     | 281 ms                                                                 | 382 ms: 1.36x slower                                                     |
| async_tree_memoization     | 345 ms                                                                 | 472 ms: 1.37x slower                                                     |
| regex_compile              | 130 ms                                                                 | 179 ms: 1.38x slower                                                     |
| python_startup_no_site     | 7.46 ms                                                                | 10.3 ms: 1.38x slower                                                    |
| fannkuch                   | 371 ms                                                                 | 512 ms: 1.38x slower                                                     |
| pprint_pformat             | 1.47 sec                                                               | 2.04 sec: 1.38x slower                                                   |
| async_tree_io              | 611 ms                                                                 | 849 ms: 1.39x slower                                                     |
| nbody                      | 95.2 ms                                                                | 132 ms: 1.39x slower                                                     |
| scimark_lu                 | 111 ms                                                                 | 155 ms: 1.39x slower                                                     |
| async_tree_none            | 277 ms                                                                 | 389 ms: 1.40x slower                                                     |
| 2to3                       | 258 ms                                                                 | 368 ms: 1.42x slower                                                     |
| subparsers                 | 22.1 ms                                                                | 31.5 ms: 1.43x slower                                                    |
| django_template            | 35.5 ms                                                                | 51.4 ms: 1.45x slower                                                    |
| genshi_text                | 22.0 ms                                                                | 32.2 ms: 1.46x slower                                                    |
| sympy_integrate            | 20.1 ms                                                                | 29.5 ms: 1.47x slower                                                    |
| sqlalchemy_imperative      | 19.4 ms                                                                | 29.5 ms: 1.51x slower                                                    |
| mako                       | 11.7 ms                                                                | 17.8 ms: 1.52x slower                                                    |
| unpickle_pure_python       | 215 us                                                                 | 333 us: 1.55x slower                                                     |
| comprehensions             | 17.5 us                                                                | 27.2 us: 1.55x slower                                                    |
| pyflate                    | 447 ms                                                                 | 696 ms: 1.56x slower                                                     |
| thrift                     | 736 us                                                                 | 1.15 ms: 1.57x slower                                                    |
| sqlalchemy_declarative     | 127 ms                                                                 | 204 ms: 1.60x slower                                                     |
| pickle_pure_python         | 321 us                                                                 | 517 us: 1.61x slower                                                     |
| hexiom                     | 5.93 ms                                                                | 9.71 ms: 1.64x slower                                                    |
| richards_super             | 52.1 ms                                                                | 86.3 ms: 1.66x slower                                                    |
| richards                   | 45.8 ms                                                                | 76.4 ms: 1.67x slower                                                    |
| scimark_sor                | 134 ms                                                                 | 224 ms: 1.67x slower                                                     |
| logging_silent             | 108 ns                                                                 | 184 ns: 1.71x slower                                                     |
| sympy_str                  | 275 ms                                                                 | 477 ms: 1.73x slower                                                     |
| logging_format             | 6.87 us                                                                | 12.0 us: 1.74x slower                                                    |
| logging_simple             | 6.14 us                                                                | 10.7 us: 1.74x slower                                                    |
| float                      | 80.2 ms                                                                | 141 ms: 1.75x slower                                                     |
| chaos                      | 59.2 ms                                                                | 104 ms: 1.77x slower                                                     |
| scimark_monte_carlo        | 66.4 ms                                                                | 118 ms: 1.78x slower                                                     |
| sqlglot_transpile          | 1.60 ms                                                                | 3.02 ms: 1.88x slower                                                    |
| sqlglot_parse              | 1.30 ms                                                                | 2.60 ms: 2.01x slower                                                    |
| sympy_expand               | 465 ms                                                                 | 956 ms: 2.06x slower                                                     |
| raytrace                   | 266 ms                                                                 | 548 ms: 2.06x slower                                                     |
| go                         | 121 ms                                                                 | 269 ms: 2.22x slower                                                     |
| sympy_sum                  | 155 ms                                                                 | 350 ms: 2.26x slower                                                     |
| deltablue                  | 3.24 ms                                                                | 7.94 ms: 2.45x slower                                                    |
| bench_thread_pool          | 1.03 ms                                                                | 3.43 ms: 3.31x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.38x slower                                                             |

Benchmark hidden because not significant (1): regex_v8
Ignored benchmarks (1) of results/bm-20241217-3.14.0a2+-3aa9426-NOGIL/bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-3aa9426.json: html5lib

- Geometric mean (including insignificant results): 1.267x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.29x
- 95% likely to have a slowdown of 1.28x
- 99% likely to have a slowdown of 1.27x

# Memory
- memory change: 1.19x