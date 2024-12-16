# Results vs. default_base_vs_NOGIL

- fork: corona10
- ref: gh_115999_BINARY_SUB
- machine: linux-x86_64
- commit hash: 7b72e7b
- commit date: 2024-12-17
- overall geometric mean: 1.266x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.26x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-7b72e7b |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 258 ms                                                                 | 368 ms: 1.43x slower                                                     |
| docutils       | 2.57 sec                                                               | 3.10 sec: 1.20x slower                                                   |
| sphinx         | 996 ms                                                                 | 1.19 sec: 1.19x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.27x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-7b72e7b |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| asyncio_websockets         | 523 ms                                                                 | 518 ms: 1.01x faster                                                     |
| coroutines                 | 22.1 ms                                                                | 24.4 ms: 1.10x slower                                                    |
| async_tree_cpu_io_mixed_tg | 500 ms                                                                 | 625 ms: 1.25x slower                                                     |
| async_generators           | 363 ms                                                                 | 454 ms: 1.25x slower                                                     |
| async_tree_cpu_io_mixed    | 505 ms                                                                 | 649 ms: 1.28x slower                                                     |
| async_tree_none_tg         | 276 ms                                                                 | 363 ms: 1.32x slower                                                     |
| async_tree_io_tg           | 625 ms                                                                 | 833 ms: 1.33x slower                                                     |
| async_tree_memoization_tg  | 336 ms                                                                 | 450 ms: 1.34x slower                                                     |
| async_tree_memoization     | 345 ms                                                                 | 473 ms: 1.37x slower                                                     |
| async_tree_io              | 611 ms                                                                 | 855 ms: 1.40x slower                                                     |
| async_tree_none            | 277 ms                                                                 | 390 ms: 1.41x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.27x slower                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-7b72e7b |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 186 ms                                                                 | 181 ms: 1.02x faster                                                     |
| nbody          | 95.2 ms                                                                | 131 ms: 1.37x slower                                                     |
| float          | 80.2 ms                                                                | 139 ms: 1.74x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.32x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-7b72e7b |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 24.8 ms                                                                | 25.1 ms: 1.01x slower                                                    |
| regex_effbot   | 2.76 ms                                                                | 2.83 ms: 1.02x slower                                                    |
| regex_dna      | 180 ms                                                                 | 185 ms: 1.03x slower                                                     |
| regex_compile  | 130 ms                                                                 | 178 ms: 1.37x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.10x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-7b72e7b |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 90.5 ms                                                                | 91.4 ms: 1.01x slower                                                    |
| xml_etree_parse      | 127 ms                                                                 | 131 ms: 1.03x slower                                                     |
| json_loads           | 25.0 us                                                                | 28.6 us: 1.14x slower                                                    |
| xml_etree_generate   | 84.8 ms                                                                | 97.5 ms: 1.15x slower                                                    |
| json_dumps           | 11.5 ms                                                                | 14.3 ms: 1.24x slower                                                    |
| tomli_loads          | 2.13 sec                                                               | 2.67 sec: 1.25x slower                                                   |
| xml_etree_process    | 59.0 ms                                                                | 78.2 ms: 1.32x slower                                                    |
| unpickle_pure_python | 215 us                                                                 | 335 us: 1.56x slower                                                     |
| pickle_pure_python   | 321 us                                                                 | 519 us: 1.62x slower                                                     |
| Geometric mean       | (ref)                                                                  | 1.24x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-7b72e7b |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                                | 17.5 ms: 1.20x slower                                                    |
| python_startup_no_site | 7.46 ms                                                                | 10.3 ms: 1.37x slower                                                    |
| Geometric mean         | (ref)                                                                  | 1.28x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-7b72e7b |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 50.6 ms                                                                | 65.1 ms: 1.29x slower                                                    |
| django_template | 35.5 ms                                                                | 51.6 ms: 1.45x slower                                                    |
| genshi_text     | 22.0 ms                                                                | 32.0 ms: 1.46x slower                                                    |
| mako            | 11.7 ms                                                                | 17.9 ms: 1.52x slower                                                    |
| Geometric mean  | (ref)                                                                  | 1.43x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-7b72e7b |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal               | 4.04 ms                                                                | 3.21 ms: 1.26x faster                                                    |
| pidigits                   | 186 ms                                                                 | 181 ms: 1.02x faster                                                     |
| asyncio_websockets         | 523 ms                                                                 | 518 ms: 1.01x faster                                                     |
| xml_etree_iterparse        | 90.5 ms                                                                | 91.4 ms: 1.01x slower                                                    |
| regex_v8                   | 24.8 ms                                                                | 25.1 ms: 1.01x slower                                                    |
| regex_effbot               | 2.76 ms                                                                | 2.83 ms: 1.02x slower                                                    |
| sqlite_synth               | 2.23 us                                                                | 2.28 us: 1.03x slower                                                    |
| regex_dna                  | 180 ms                                                                 | 185 ms: 1.03x slower                                                     |
| xml_etree_parse            | 127 ms                                                                 | 131 ms: 1.03x slower                                                     |
| create_gc_cycles           | 1.70 ms                                                                | 1.80 ms: 1.06x slower                                                    |
| coroutines                 | 22.1 ms                                                                | 24.4 ms: 1.10x slower                                                    |
| json                       | 4.59 ms                                                                | 5.06 ms: 1.10x slower                                                    |
| spectral_norm              | 110 ms                                                                 | 123 ms: 1.11x slower                                                     |
| mdp                        | 2.49 sec                                                               | 2.78 sec: 1.12x slower                                                   |
| pathlib                    | 18.2 ms                                                                | 20.5 ms: 1.12x slower                                                    |
| json_loads                 | 25.0 us                                                                | 28.6 us: 1.14x slower                                                    |
| xml_etree_generate         | 84.8 ms                                                                | 97.5 ms: 1.15x slower                                                    |
| bpe_tokeniser              | 4.34 sec                                                               | 5.00 sec: 1.15x slower                                                   |
| telco                      | 7.31 ms                                                                | 8.71 ms: 1.19x slower                                                    |
| sphinx                     | 996 ms                                                                 | 1.19 sec: 1.19x slower                                                   |
| scimark_fft                | 338 ms                                                                 | 403 ms: 1.19x slower                                                     |
| python_startup             | 14.6 ms                                                                | 17.5 ms: 1.20x slower                                                    |
| k_core                     | 2.02 sec                                                               | 2.43 sec: 1.20x slower                                                   |
| docutils                   | 2.57 sec                                                               | 3.10 sec: 1.20x slower                                                   |
| nqueens                    | 79.0 ms                                                                | 97.8 ms: 1.24x slower                                                    |
| json_dumps                 | 11.5 ms                                                                | 14.3 ms: 1.24x slower                                                    |
| coverage                   | 80.1 ms                                                                | 99.3 ms: 1.24x slower                                                    |
| dulwich_log                | 76.4 ms                                                                | 95.1 ms: 1.24x slower                                                    |
| many_optionals             | 1.03 ms                                                                | 1.29 ms: 1.25x slower                                                    |
| shortest_path              | 441 ms                                                                 | 551 ms: 1.25x slower                                                     |
| async_tree_cpu_io_mixed_tg | 500 ms                                                                 | 625 ms: 1.25x slower                                                     |
| async_generators           | 363 ms                                                                 | 454 ms: 1.25x slower                                                     |
| tomli_loads                | 2.13 sec                                                               | 2.67 sec: 1.25x slower                                                   |
| deepcopy                   | 263 us                                                                 | 330 us: 1.26x slower                                                     |
| connected_components       | 399 ms                                                                 | 504 ms: 1.26x slower                                                     |
| typing_runtime_protocols   | 158 us                                                                 | 200 us: 1.27x slower                                                     |
| sqlglot_normalize          | 108 ms                                                                 | 137 ms: 1.27x slower                                                     |
| bench_mp_pool              | 85.5 ms                                                                | 109 ms: 1.27x slower                                                     |
| meteor_contest             | 101 ms                                                                 | 129 ms: 1.28x slower                                                     |
| sqlglot_optimize           | 53.9 ms                                                                | 69.3 ms: 1.28x slower                                                    |
| async_tree_cpu_io_mixed    | 505 ms                                                                 | 649 ms: 1.28x slower                                                     |
| scimark_sparse_mat_mult    | 4.51 ms                                                                | 5.80 ms: 1.29x slower                                                    |
| genshi_xml                 | 50.6 ms                                                                | 65.1 ms: 1.29x slower                                                    |
| deepcopy_memo              | 30.6 us                                                                | 40.2 us: 1.31x slower                                                    |
| async_tree_none_tg         | 276 ms                                                                 | 363 ms: 1.32x slower                                                     |
| deepcopy_reduce            | 2.68 us                                                                | 3.55 us: 1.32x slower                                                    |
| xml_etree_process          | 59.0 ms                                                                | 78.2 ms: 1.32x slower                                                    |
| async_tree_io_tg           | 625 ms                                                                 | 833 ms: 1.33x slower                                                     |
| generators                 | 29.2 ms                                                                | 39.0 ms: 1.33x slower                                                    |
| fannkuch                   | 371 ms                                                                 | 497 ms: 1.34x slower                                                     |
| async_tree_memoization_tg  | 336 ms                                                                 | 450 ms: 1.34x slower                                                     |
| pprint_safe_repr           | 723 ms                                                                 | 974 ms: 1.35x slower                                                     |
| crypto_pyaes               | 68.7 ms                                                                | 92.9 ms: 1.35x slower                                                    |
| pprint_pformat             | 1.47 sec                                                               | 2.01 sec: 1.36x slower                                                   |
| pylint                     | 281 ms                                                                 | 383 ms: 1.36x slower                                                     |
| pycparser                  | 1.13 sec                                                               | 1.55 sec: 1.36x slower                                                   |
| async_tree_memoization     | 345 ms                                                                 | 473 ms: 1.37x slower                                                     |
| regex_compile              | 130 ms                                                                 | 178 ms: 1.37x slower                                                     |
| nbody                      | 95.2 ms                                                                | 131 ms: 1.37x slower                                                     |
| python_startup_no_site     | 7.46 ms                                                                | 10.3 ms: 1.37x slower                                                    |
| async_tree_io              | 611 ms                                                                 | 855 ms: 1.40x slower                                                     |
| subparsers                 | 22.1 ms                                                                | 31.0 ms: 1.40x slower                                                    |
| scimark_lu                 | 111 ms                                                                 | 156 ms: 1.40x slower                                                     |
| async_tree_none            | 277 ms                                                                 | 390 ms: 1.41x slower                                                     |
| 2to3                       | 258 ms                                                                 | 368 ms: 1.43x slower                                                     |
| django_template            | 35.5 ms                                                                | 51.6 ms: 1.45x slower                                                    |
| genshi_text                | 22.0 ms                                                                | 32.0 ms: 1.46x slower                                                    |
| sympy_integrate            | 20.1 ms                                                                | 29.4 ms: 1.47x slower                                                    |
| sqlalchemy_imperative      | 19.4 ms                                                                | 29.5 ms: 1.51x slower                                                    |
| mako                       | 11.7 ms                                                                | 17.9 ms: 1.52x slower                                                    |
| comprehensions             | 17.5 us                                                                | 27.2 us: 1.56x slower                                                    |
| unpickle_pure_python       | 215 us                                                                 | 335 us: 1.56x slower                                                     |
| pyflate                    | 447 ms                                                                 | 699 ms: 1.56x slower                                                     |
| thrift                     | 736 us                                                                 | 1.16 ms: 1.57x slower                                                    |
| sqlalchemy_declarative     | 127 ms                                                                 | 204 ms: 1.61x slower                                                     |
| pickle_pure_python         | 321 us                                                                 | 519 us: 1.62x slower                                                     |
| hexiom                     | 5.93 ms                                                                | 9.81 ms: 1.65x slower                                                    |
| scimark_sor                | 134 ms                                                                 | 225 ms: 1.68x slower                                                     |
| richards                   | 45.8 ms                                                                | 78.4 ms: 1.71x slower                                                    |
| richards_super             | 52.1 ms                                                                | 89.9 ms: 1.73x slower                                                    |
| sympy_str                  | 275 ms                                                                 | 478 ms: 1.73x slower                                                     |
| float                      | 80.2 ms                                                                | 139 ms: 1.74x slower                                                     |
| logging_silent             | 108 ns                                                                 | 188 ns: 1.75x slower                                                     |
| logging_format             | 6.87 us                                                                | 12.0 us: 1.75x slower                                                    |
| logging_simple             | 6.14 us                                                                | 10.9 us: 1.78x slower                                                    |
| chaos                      | 59.2 ms                                                                | 105 ms: 1.78x slower                                                     |
| scimark_monte_carlo        | 66.4 ms                                                                | 119 ms: 1.79x slower                                                     |
| sqlglot_transpile          | 1.60 ms                                                                | 3.00 ms: 1.87x slower                                                    |
| sqlglot_parse              | 1.30 ms                                                                | 2.59 ms: 2.00x slower                                                    |
| sympy_expand               | 465 ms                                                                 | 958 ms: 2.06x slower                                                     |
| raytrace                   | 266 ms                                                                 | 555 ms: 2.08x slower                                                     |
| sympy_sum                  | 155 ms                                                                 | 350 ms: 2.26x slower                                                     |
| go                         | 121 ms                                                                 | 274 ms: 2.27x slower                                                     |
| deltablue                  | 3.24 ms                                                                | 8.08 ms: 2.49x slower                                                    |
| bench_thread_pool          | 1.03 ms                                                                | 3.42 ms: 3.30x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.38x slower                                                             |
Ignored benchmarks (1) of results/bm-20241217-3.14.0a2+-7b72e7b-NOGIL/bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-7b72e7b.json: html5lib

- Geometric mean (including insignificant results): 1.266x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.28x
- 95% likely to have a slowdown of 1.28x
- 99% likely to have a slowdown of 1.26x

# Memory
- memory change: 1.19x