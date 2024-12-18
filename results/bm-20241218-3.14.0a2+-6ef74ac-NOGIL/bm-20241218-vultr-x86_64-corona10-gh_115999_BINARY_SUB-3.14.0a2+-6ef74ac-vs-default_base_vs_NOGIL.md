# Results vs. default_base_vs_NOGIL

- fork: corona10
- ref: gh_115999_BINARY_SUB
- machine: linux-x86_64
- commit hash: 6ef74ac
- commit date: 2024-12-18
- overall geometric mean: 1.263x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.26x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241218-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-6ef74ac |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 258 ms                                                                 | 366 ms: 1.42x slower                                                     |
| docutils       | 2.57 sec                                                               | 3.10 sec: 1.20x slower                                                   |
| sphinx         | 996 ms                                                                 | 1.18 sec: 1.19x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.26x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241218-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-6ef74ac |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| asyncio_websockets         | 523 ms                                                                 | 518 ms: 1.01x faster                                                     |
| coroutines                 | 22.1 ms                                                                | 24.8 ms: 1.12x slower                                                    |
| async_tree_cpu_io_mixed_tg | 500 ms                                                                 | 620 ms: 1.24x slower                                                     |
| async_generators           | 363 ms                                                                 | 452 ms: 1.25x slower                                                     |
| async_tree_cpu_io_mixed    | 505 ms                                                                 | 649 ms: 1.28x slower                                                     |
| async_tree_none_tg         | 276 ms                                                                 | 356 ms: 1.29x slower                                                     |
| async_tree_io_tg           | 625 ms                                                                 | 827 ms: 1.32x slower                                                     |
| async_tree_memoization_tg  | 336 ms                                                                 | 445 ms: 1.33x slower                                                     |
| async_tree_memoization     | 345 ms                                                                 | 473 ms: 1.37x slower                                                     |
| async_tree_io              | 611 ms                                                                 | 849 ms: 1.39x slower                                                     |
| async_tree_none            | 277 ms                                                                 | 389 ms: 1.40x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.27x slower                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241218-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-6ef74ac |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 186 ms                                                                 | 184 ms: 1.01x faster                                                     |
| nbody          | 95.2 ms                                                                | 130 ms: 1.36x slower                                                     |
| float          | 80.2 ms                                                                | 138 ms: 1.73x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.33x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241218-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-6ef74ac |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_dna      | 180 ms                                                                 | 184 ms: 1.02x slower                                                     |
| regex_v8       | 24.8 ms                                                                | 25.5 ms: 1.03x slower                                                    |
| regex_effbot   | 2.76 ms                                                                | 2.92 ms: 1.06x slower                                                    |
| regex_compile  | 130 ms                                                                 | 179 ms: 1.38x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.11x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241218-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-6ef74ac |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 90.5 ms                                                                | 91.0 ms: 1.01x slower                                                    |
| xml_etree_parse      | 127 ms                                                                 | 131 ms: 1.04x slower                                                     |
| json_loads           | 25.0 us                                                                | 28.1 us: 1.12x slower                                                    |
| xml_etree_generate   | 84.8 ms                                                                | 98.4 ms: 1.16x slower                                                    |
| json_dumps           | 11.5 ms                                                                | 14.2 ms: 1.23x slower                                                    |
| tomli_loads          | 2.13 sec                                                               | 2.69 sec: 1.27x slower                                                   |
| xml_etree_process    | 59.0 ms                                                                | 78.3 ms: 1.33x slower                                                    |
| unpickle_pure_python | 215 us                                                                 | 339 us: 1.58x slower                                                     |
| pickle_pure_python   | 321 us                                                                 | 516 us: 1.61x slower                                                     |
| Geometric mean       | (ref)                                                                  | 1.24x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241218-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-6ef74ac |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                                | 17.4 ms: 1.20x slower                                                    |
| python_startup_no_site | 7.46 ms                                                                | 10.3 ms: 1.37x slower                                                    |
| Geometric mean         | (ref)                                                                  | 1.28x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241218-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-6ef74ac |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 50.6 ms                                                                | 63.4 ms: 1.25x slower                                                    |
| django_template | 35.5 ms                                                                | 50.7 ms: 1.43x slower                                                    |
| genshi_text     | 22.0 ms                                                                | 31.4 ms: 1.43x slower                                                    |
| mako            | 11.7 ms                                                                | 17.8 ms: 1.52x slower                                                    |
| Geometric mean  | (ref)                                                                  | 1.40x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241218-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-6ef74ac |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal               | 4.04 ms                                                                | 3.17 ms: 1.27x faster                                                    |
| asyncio_websockets         | 523 ms                                                                 | 518 ms: 1.01x faster                                                     |
| pidigits                   | 186 ms                                                                 | 184 ms: 1.01x faster                                                     |
| xml_etree_iterparse        | 90.5 ms                                                                | 91.0 ms: 1.01x slower                                                    |
| sqlite_synth               | 2.23 us                                                                | 2.26 us: 1.01x slower                                                    |
| regex_dna                  | 180 ms                                                                 | 184 ms: 1.02x slower                                                     |
| regex_v8                   | 24.8 ms                                                                | 25.5 ms: 1.03x slower                                                    |
| xml_etree_parse            | 127 ms                                                                 | 131 ms: 1.04x slower                                                     |
| regex_effbot               | 2.76 ms                                                                | 2.92 ms: 1.06x slower                                                    |
| create_gc_cycles           | 1.70 ms                                                                | 1.81 ms: 1.06x slower                                                    |
| json                       | 4.59 ms                                                                | 5.04 ms: 1.10x slower                                                    |
| mdp                        | 2.49 sec                                                               | 2.77 sec: 1.11x slower                                                   |
| spectral_norm              | 110 ms                                                                 | 124 ms: 1.12x slower                                                     |
| coroutines                 | 22.1 ms                                                                | 24.8 ms: 1.12x slower                                                    |
| json_loads                 | 25.0 us                                                                | 28.1 us: 1.12x slower                                                    |
| pathlib                    | 18.2 ms                                                                | 20.5 ms: 1.12x slower                                                    |
| bpe_tokeniser              | 4.34 sec                                                               | 5.01 sec: 1.15x slower                                                   |
| xml_etree_generate         | 84.8 ms                                                                | 98.4 ms: 1.16x slower                                                    |
| scimark_fft                | 338 ms                                                                 | 397 ms: 1.18x slower                                                     |
| sphinx                     | 996 ms                                                                 | 1.18 sec: 1.19x slower                                                   |
| python_startup             | 14.6 ms                                                                | 17.4 ms: 1.20x slower                                                    |
| k_core                     | 2.02 sec                                                               | 2.42 sec: 1.20x slower                                                   |
| docutils                   | 2.57 sec                                                               | 3.10 sec: 1.20x slower                                                   |
| telco                      | 7.31 ms                                                                | 8.81 ms: 1.21x slower                                                    |
| json_dumps                 | 11.5 ms                                                                | 14.2 ms: 1.23x slower                                                    |
| nqueens                    | 79.0 ms                                                                | 97.6 ms: 1.24x slower                                                    |
| many_optionals             | 1.03 ms                                                                | 1.28 ms: 1.24x slower                                                    |
| coverage                   | 80.1 ms                                                                | 99.3 ms: 1.24x slower                                                    |
| async_tree_cpu_io_mixed_tg | 500 ms                                                                 | 620 ms: 1.24x slower                                                     |
| async_generators           | 363 ms                                                                 | 452 ms: 1.25x slower                                                     |
| shortest_path              | 441 ms                                                                 | 550 ms: 1.25x slower                                                     |
| dulwich_log                | 76.4 ms                                                                | 95.4 ms: 1.25x slower                                                    |
| genshi_xml                 | 50.6 ms                                                                | 63.4 ms: 1.25x slower                                                    |
| deepcopy                   | 263 us                                                                 | 329 us: 1.25x slower                                                     |
| scimark_sparse_mat_mult    | 4.51 ms                                                                | 5.68 ms: 1.26x slower                                                    |
| sqlglot_normalize          | 108 ms                                                                 | 136 ms: 1.26x slower                                                     |
| connected_components       | 399 ms                                                                 | 503 ms: 1.26x slower                                                     |
| tomli_loads                | 2.13 sec                                                               | 2.69 sec: 1.27x slower                                                   |
| bench_mp_pool              | 85.5 ms                                                                | 109 ms: 1.27x slower                                                     |
| typing_runtime_protocols   | 158 us                                                                 | 201 us: 1.27x slower                                                     |
| sqlglot_optimize           | 53.9 ms                                                                | 68.9 ms: 1.28x slower                                                    |
| async_tree_cpu_io_mixed    | 505 ms                                                                 | 649 ms: 1.28x slower                                                     |
| meteor_contest             | 101 ms                                                                 | 130 ms: 1.29x slower                                                     |
| async_tree_none_tg         | 276 ms                                                                 | 356 ms: 1.29x slower                                                     |
| deepcopy_reduce            | 2.68 us                                                                | 3.49 us: 1.30x slower                                                    |
| deepcopy_memo              | 30.6 us                                                                | 40.2 us: 1.31x slower                                                    |
| generators                 | 29.2 ms                                                                | 38.4 ms: 1.31x slower                                                    |
| async_tree_io_tg           | 625 ms                                                                 | 827 ms: 1.32x slower                                                     |
| async_tree_memoization_tg  | 336 ms                                                                 | 445 ms: 1.33x slower                                                     |
| xml_etree_process          | 59.0 ms                                                                | 78.3 ms: 1.33x slower                                                    |
| pprint_safe_repr           | 723 ms                                                                 | 964 ms: 1.33x slower                                                     |
| crypto_pyaes               | 68.7 ms                                                                | 92.5 ms: 1.35x slower                                                    |
| pycparser                  | 1.13 sec                                                               | 1.53 sec: 1.35x slower                                                   |
| fannkuch                   | 371 ms                                                                 | 504 ms: 1.36x slower                                                     |
| pylint                     | 281 ms                                                                 | 381 ms: 1.36x slower                                                     |
| pprint_pformat             | 1.47 sec                                                               | 2.00 sec: 1.36x slower                                                   |
| nbody                      | 95.2 ms                                                                | 130 ms: 1.36x slower                                                     |
| async_tree_memoization     | 345 ms                                                                 | 473 ms: 1.37x slower                                                     |
| python_startup_no_site     | 7.46 ms                                                                | 10.3 ms: 1.37x slower                                                    |
| regex_compile              | 130 ms                                                                 | 179 ms: 1.38x slower                                                     |
| scimark_lu                 | 111 ms                                                                 | 155 ms: 1.39x slower                                                     |
| async_tree_io              | 611 ms                                                                 | 849 ms: 1.39x slower                                                     |
| async_tree_none            | 277 ms                                                                 | 389 ms: 1.40x slower                                                     |
| subparsers                 | 22.1 ms                                                                | 31.3 ms: 1.41x slower                                                    |
| 2to3                       | 258 ms                                                                 | 366 ms: 1.42x slower                                                     |
| django_template            | 35.5 ms                                                                | 50.7 ms: 1.43x slower                                                    |
| genshi_text                | 22.0 ms                                                                | 31.4 ms: 1.43x slower                                                    |
| sympy_integrate            | 20.1 ms                                                                | 29.4 ms: 1.47x slower                                                    |
| sqlalchemy_imperative      | 19.4 ms                                                                | 29.3 ms: 1.51x slower                                                    |
| mako                       | 11.7 ms                                                                | 17.8 ms: 1.52x slower                                                    |
| comprehensions             | 17.5 us                                                                | 27.1 us: 1.55x slower                                                    |
| pyflate                    | 447 ms                                                                 | 693 ms: 1.55x slower                                                     |
| unpickle_pure_python       | 215 us                                                                 | 339 us: 1.58x slower                                                     |
| thrift                     | 736 us                                                                 | 1.16 ms: 1.58x slower                                                    |
| sqlalchemy_declarative     | 127 ms                                                                 | 203 ms: 1.60x slower                                                     |
| pickle_pure_python         | 321 us                                                                 | 516 us: 1.61x slower                                                     |
| hexiom                     | 5.93 ms                                                                | 9.75 ms: 1.64x slower                                                    |
| richards                   | 45.8 ms                                                                | 76.5 ms: 1.67x slower                                                    |
| scimark_sor                | 134 ms                                                                 | 226 ms: 1.69x slower                                                     |
| richards_super             | 52.1 ms                                                                | 88.8 ms: 1.70x slower                                                    |
| sympy_str                  | 275 ms                                                                 | 475 ms: 1.72x slower                                                     |
| float                      | 80.2 ms                                                                | 138 ms: 1.73x slower                                                     |
| logging_silent             | 108 ns                                                                 | 189 ns: 1.75x slower                                                     |
| logging_format             | 6.87 us                                                                | 12.1 us: 1.76x slower                                                    |
| chaos                      | 59.2 ms                                                                | 104 ms: 1.76x slower                                                     |
| logging_simple             | 6.14 us                                                                | 10.8 us: 1.76x slower                                                    |
| scimark_monte_carlo        | 66.4 ms                                                                | 118 ms: 1.78x slower                                                     |
| sqlglot_transpile          | 1.60 ms                                                                | 2.96 ms: 1.85x slower                                                    |
| sqlglot_parse              | 1.30 ms                                                                | 2.55 ms: 1.97x slower                                                    |
| sympy_expand               | 465 ms                                                                 | 953 ms: 2.05x slower                                                     |
| raytrace                   | 266 ms                                                                 | 549 ms: 2.06x slower                                                     |
| go                         | 121 ms                                                                 | 269 ms: 2.22x slower                                                     |
| sympy_sum                  | 155 ms                                                                 | 350 ms: 2.26x slower                                                     |
| deltablue                  | 3.24 ms                                                                | 8.02 ms: 2.47x slower                                                    |
| bench_thread_pool          | 1.03 ms                                                                | 3.43 ms: 3.31x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.37x slower                                                             |
Ignored benchmarks (1) of results/bm-20241218-3.14.0a2+-6ef74ac-NOGIL/bm-20241218-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-6ef74ac.json: html5lib

- Geometric mean (including insignificant results): 1.263x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.28x
- 95% likely to have a slowdown of 1.28x
- 99% likely to have a slowdown of 1.26x

# Memory
- memory change: 1.19x