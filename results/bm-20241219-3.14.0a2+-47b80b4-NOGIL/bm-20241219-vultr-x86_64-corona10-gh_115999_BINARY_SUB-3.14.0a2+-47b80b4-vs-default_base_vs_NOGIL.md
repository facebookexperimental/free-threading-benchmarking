# Results vs. default_base_vs_NOGIL

- fork: corona10
- ref: gh_115999_BINARY_SUB
- machine: linux-x86_64
- commit hash: 47b80b4
- commit date: 2024-12-19
- overall geometric mean: 1.263x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.25x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241219-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-47b80b4 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 258 ms                                                                 | 366 ms: 1.42x slower                                                     |
| docutils       | 2.57 sec                                                               | 3.10 sec: 1.20x slower                                                   |
| sphinx         | 996 ms                                                                 | 1.19 sec: 1.19x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.27x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241219-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-47b80b4 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| asyncio_websockets         | 523 ms                                                                 | 517 ms: 1.01x faster                                                     |
| coroutines                 | 22.1 ms                                                                | 24.6 ms: 1.11x slower                                                    |
| async_generators           | 363 ms                                                                 | 452 ms: 1.25x slower                                                     |
| async_tree_cpu_io_mixed_tg | 500 ms                                                                 | 624 ms: 1.25x slower                                                     |
| async_tree_cpu_io_mixed    | 505 ms                                                                 | 652 ms: 1.29x slower                                                     |
| async_tree_none_tg         | 276 ms                                                                 | 358 ms: 1.30x slower                                                     |
| async_tree_io_tg           | 625 ms                                                                 | 823 ms: 1.32x slower                                                     |
| async_tree_memoization_tg  | 336 ms                                                                 | 443 ms: 1.32x slower                                                     |
| async_tree_memoization     | 345 ms                                                                 | 472 ms: 1.37x slower                                                     |
| async_tree_io              | 611 ms                                                                 | 852 ms: 1.40x slower                                                     |
| async_tree_none            | 277 ms                                                                 | 387 ms: 1.40x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.26x slower                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241219-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-47b80b4 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 186 ms                                                                 | 182 ms: 1.02x faster                                                     |
| nbody          | 95.2 ms                                                                | 134 ms: 1.41x slower                                                     |
| float          | 80.2 ms                                                                | 140 ms: 1.74x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.34x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241219-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-47b80b4 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 24.8 ms                                                                | 24.9 ms: 1.01x slower                                                    |
| regex_dna      | 180 ms                                                                 | 184 ms: 1.02x slower                                                     |
| regex_effbot   | 2.76 ms                                                                | 2.90 ms: 1.05x slower                                                    |
| regex_compile  | 130 ms                                                                 | 179 ms: 1.38x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.10x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241219-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-47b80b4 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 90.5 ms                                                                | 91.1 ms: 1.01x slower                                                    |
| xml_etree_parse      | 127 ms                                                                 | 131 ms: 1.04x slower                                                     |
| json_loads           | 25.0 us                                                                | 28.2 us: 1.13x slower                                                    |
| xml_etree_generate   | 84.8 ms                                                                | 97.3 ms: 1.15x slower                                                    |
| tomli_loads          | 2.13 sec                                                               | 2.66 sec: 1.25x slower                                                   |
| json_dumps           | 11.5 ms                                                                | 14.5 ms: 1.26x slower                                                    |
| xml_etree_process    | 59.0 ms                                                                | 77.4 ms: 1.31x slower                                                    |
| unpickle_pure_python | 215 us                                                                 | 335 us: 1.56x slower                                                     |
| pickle_pure_python   | 321 us                                                                 | 511 us: 1.59x slower                                                     |
| Geometric mean       | (ref)                                                                  | 1.24x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241219-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-47b80b4 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                                | 17.4 ms: 1.20x slower                                                    |
| python_startup_no_site | 7.46 ms                                                                | 10.2 ms: 1.37x slower                                                    |
| Geometric mean         | (ref)                                                                  | 1.28x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241219-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-47b80b4 |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 50.6 ms                                                                | 63.3 ms: 1.25x slower                                                    |
| genshi_text     | 22.0 ms                                                                | 31.7 ms: 1.44x slower                                                    |
| django_template | 35.5 ms                                                                | 51.4 ms: 1.45x slower                                                    |
| mako            | 11.7 ms                                                                | 17.7 ms: 1.51x slower                                                    |
| Geometric mean  | (ref)                                                                  | 1.41x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241219-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-47b80b4 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal               | 4.04 ms                                                                | 3.17 ms: 1.27x faster                                                    |
| pidigits                   | 186 ms                                                                 | 182 ms: 1.02x faster                                                     |
| asyncio_websockets         | 523 ms                                                                 | 517 ms: 1.01x faster                                                     |
| regex_v8                   | 24.8 ms                                                                | 24.9 ms: 1.01x slower                                                    |
| xml_etree_iterparse        | 90.5 ms                                                                | 91.1 ms: 1.01x slower                                                    |
| regex_dna                  | 180 ms                                                                 | 184 ms: 1.02x slower                                                     |
| sqlite_synth               | 2.23 us                                                                | 2.29 us: 1.03x slower                                                    |
| xml_etree_parse            | 127 ms                                                                 | 131 ms: 1.04x slower                                                     |
| regex_effbot               | 2.76 ms                                                                | 2.90 ms: 1.05x slower                                                    |
| create_gc_cycles           | 1.70 ms                                                                | 1.80 ms: 1.06x slower                                                    |
| spectral_norm              | 110 ms                                                                 | 120 ms: 1.09x slower                                                     |
| coroutines                 | 22.1 ms                                                                | 24.6 ms: 1.11x slower                                                    |
| json                       | 4.59 ms                                                                | 5.11 ms: 1.11x slower                                                    |
| pathlib                    | 18.2 ms                                                                | 20.4 ms: 1.12x slower                                                    |
| json_loads                 | 25.0 us                                                                | 28.2 us: 1.13x slower                                                    |
| mdp                        | 2.49 sec                                                               | 2.84 sec: 1.14x slower                                                   |
| xml_etree_generate         | 84.8 ms                                                                | 97.3 ms: 1.15x slower                                                    |
| bpe_tokeniser              | 4.34 sec                                                               | 5.00 sec: 1.15x slower                                                   |
| telco                      | 7.31 ms                                                                | 8.66 ms: 1.18x slower                                                    |
| scimark_fft                | 338 ms                                                                 | 402 ms: 1.19x slower                                                     |
| sphinx                     | 996 ms                                                                 | 1.19 sec: 1.19x slower                                                   |
| k_core                     | 2.02 sec                                                               | 2.42 sec: 1.20x slower                                                   |
| python_startup             | 14.6 ms                                                                | 17.4 ms: 1.20x slower                                                    |
| docutils                   | 2.57 sec                                                               | 3.10 sec: 1.20x slower                                                   |
| nqueens                    | 79.0 ms                                                                | 96.0 ms: 1.22x slower                                                    |
| coverage                   | 80.1 ms                                                                | 99.1 ms: 1.24x slower                                                    |
| shortest_path              | 441 ms                                                                 | 546 ms: 1.24x slower                                                     |
| many_optionals             | 1.03 ms                                                                | 1.29 ms: 1.24x slower                                                    |
| deepcopy                   | 263 us                                                                 | 327 us: 1.24x slower                                                     |
| async_generators           | 363 ms                                                                 | 452 ms: 1.25x slower                                                     |
| async_tree_cpu_io_mixed_tg | 500 ms                                                                 | 624 ms: 1.25x slower                                                     |
| tomli_loads                | 2.13 sec                                                               | 2.66 sec: 1.25x slower                                                   |
| genshi_xml                 | 50.6 ms                                                                | 63.3 ms: 1.25x slower                                                    |
| dulwich_log                | 76.4 ms                                                                | 95.5 ms: 1.25x slower                                                    |
| sqlglot_normalize          | 108 ms                                                                 | 135 ms: 1.25x slower                                                     |
| json_dumps                 | 11.5 ms                                                                | 14.5 ms: 1.26x slower                                                    |
| connected_components       | 399 ms                                                                 | 501 ms: 1.26x slower                                                     |
| meteor_contest             | 101 ms                                                                 | 128 ms: 1.26x slower                                                     |
| bench_mp_pool              | 85.5 ms                                                                | 109 ms: 1.27x slower                                                     |
| sqlglot_optimize           | 53.9 ms                                                                | 68.8 ms: 1.28x slower                                                    |
| deepcopy_memo              | 30.6 us                                                                | 39.5 us: 1.29x slower                                                    |
| async_tree_cpu_io_mixed    | 505 ms                                                                 | 652 ms: 1.29x slower                                                     |
| typing_runtime_protocols   | 158 us                                                                 | 204 us: 1.29x slower                                                     |
| async_tree_none_tg         | 276 ms                                                                 | 358 ms: 1.30x slower                                                     |
| deepcopy_reduce            | 2.68 us                                                                | 3.48 us: 1.30x slower                                                    |
| generators                 | 29.2 ms                                                                | 38.1 ms: 1.30x slower                                                    |
| xml_etree_process          | 59.0 ms                                                                | 77.4 ms: 1.31x slower                                                    |
| scimark_sparse_mat_mult    | 4.51 ms                                                                | 5.93 ms: 1.32x slower                                                    |
| async_tree_io_tg           | 625 ms                                                                 | 823 ms: 1.32x slower                                                     |
| async_tree_memoization_tg  | 336 ms                                                                 | 443 ms: 1.32x slower                                                     |
| fannkuch                   | 371 ms                                                                 | 492 ms: 1.32x slower                                                     |
| crypto_pyaes               | 68.7 ms                                                                | 92.1 ms: 1.34x slower                                                    |
| pprint_safe_repr           | 723 ms                                                                 | 970 ms: 1.34x slower                                                     |
| pycparser                  | 1.13 sec                                                               | 1.52 sec: 1.34x slower                                                   |
| pylint                     | 281 ms                                                                 | 381 ms: 1.36x slower                                                     |
| async_tree_memoization     | 345 ms                                                                 | 472 ms: 1.37x slower                                                     |
| python_startup_no_site     | 7.46 ms                                                                | 10.2 ms: 1.37x slower                                                    |
| pprint_pformat             | 1.47 sec                                                               | 2.02 sec: 1.37x slower                                                   |
| regex_compile              | 130 ms                                                                 | 179 ms: 1.38x slower                                                     |
| async_tree_io              | 611 ms                                                                 | 852 ms: 1.40x slower                                                     |
| async_tree_none            | 277 ms                                                                 | 387 ms: 1.40x slower                                                     |
| scimark_lu                 | 111 ms                                                                 | 156 ms: 1.40x slower                                                     |
| nbody                      | 95.2 ms                                                                | 134 ms: 1.41x slower                                                     |
| subparsers                 | 22.1 ms                                                                | 31.2 ms: 1.41x slower                                                    |
| 2to3                       | 258 ms                                                                 | 366 ms: 1.42x slower                                                     |
| genshi_text                | 22.0 ms                                                                | 31.7 ms: 1.44x slower                                                    |
| django_template            | 35.5 ms                                                                | 51.4 ms: 1.45x slower                                                    |
| sympy_integrate            | 20.1 ms                                                                | 29.4 ms: 1.46x slower                                                    |
| mako                       | 11.7 ms                                                                | 17.7 ms: 1.51x slower                                                    |
| sqlalchemy_imperative      | 19.4 ms                                                                | 29.7 ms: 1.53x slower                                                    |
| pyflate                    | 447 ms                                                                 | 691 ms: 1.55x slower                                                     |
| thrift                     | 736 us                                                                 | 1.15 ms: 1.56x slower                                                    |
| unpickle_pure_python       | 215 us                                                                 | 335 us: 1.56x slower                                                     |
| comprehensions             | 17.5 us                                                                | 27.5 us: 1.57x slower                                                    |
| pickle_pure_python         | 321 us                                                                 | 511 us: 1.59x slower                                                     |
| sqlalchemy_declarative     | 127 ms                                                                 | 203 ms: 1.60x slower                                                     |
| hexiom                     | 5.93 ms                                                                | 9.72 ms: 1.64x slower                                                    |
| scimark_sor                | 134 ms                                                                 | 221 ms: 1.65x slower                                                     |
| richards_super             | 52.1 ms                                                                | 86.9 ms: 1.67x slower                                                    |
| richards                   | 45.8 ms                                                                | 76.9 ms: 1.68x slower                                                    |
| logging_silent             | 108 ns                                                                 | 184 ns: 1.71x slower                                                     |
| logging_format             | 6.87 us                                                                | 11.8 us: 1.71x slower                                                    |
| logging_simple             | 6.14 us                                                                | 10.6 us: 1.72x slower                                                    |
| sympy_str                  | 275 ms                                                                 | 476 ms: 1.73x slower                                                     |
| float                      | 80.2 ms                                                                | 140 ms: 1.74x slower                                                     |
| chaos                      | 59.2 ms                                                                | 105 ms: 1.78x slower                                                     |
| scimark_monte_carlo        | 66.4 ms                                                                | 120 ms: 1.81x slower                                                     |
| sqlglot_transpile          | 1.60 ms                                                                | 2.97 ms: 1.85x slower                                                    |
| sqlglot_parse              | 1.30 ms                                                                | 2.57 ms: 1.98x slower                                                    |
| sympy_expand               | 465 ms                                                                 | 953 ms: 2.05x slower                                                     |
| raytrace                   | 266 ms                                                                 | 547 ms: 2.05x slower                                                     |
| go                         | 121 ms                                                                 | 271 ms: 2.24x slower                                                     |
| sympy_sum                  | 155 ms                                                                 | 350 ms: 2.26x slower                                                     |
| deltablue                  | 3.24 ms                                                                | 7.98 ms: 2.46x slower                                                    |
| bench_thread_pool          | 1.03 ms                                                                | 3.43 ms: 3.31x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.37x slower                                                             |
Ignored benchmarks (1) of results/bm-20241219-3.14.0a2+-47b80b4-NOGIL/bm-20241219-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-47b80b4.json: html5lib

- Geometric mean (including insignificant results): 1.263x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.28x
- 95% likely to have a slowdown of 1.27x
- 99% likely to have a slowdown of 1.25x

# Memory
- memory change: 1.19x