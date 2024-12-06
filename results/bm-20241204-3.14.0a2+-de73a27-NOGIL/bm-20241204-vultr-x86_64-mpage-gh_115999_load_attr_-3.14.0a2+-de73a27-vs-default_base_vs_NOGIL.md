# Results vs. default_base_vs_NOGIL

- fork: mpage
- ref: gh_115999_load_attr_
- machine: linux-x86_64
- commit hash: de73a27
- commit date: 2024-12-04
- overall geometric mean: 1.263x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.25x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241204-vultr-x86_64-python-51cfa569e379f84b3418-3.14.0a2+-51cfa56 | bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 257 ms                                                                 | 363 ms: 1.41x slower                                                  |
| docutils       | 2.56 sec                                                               | 3.08 sec: 1.20x slower                                                |
| sphinx         | 991 ms                                                                 | 1.17 sec: 1.18x slower                                                |
| Geometric mean | (ref)                                                                  | 1.26x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241204-vultr-x86_64-python-51cfa569e379f84b3418-3.14.0a2+-51cfa56 | bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| asyncio_websockets         | 523 ms                                                                 | 520 ms: 1.01x faster                                                  |
| coroutines                 | 22.1 ms                                                                | 25.5 ms: 1.16x slower                                                 |
| async_generators           | 369 ms                                                                 | 459 ms: 1.25x slower                                                  |
| async_tree_cpu_io_mixed_tg | 486 ms                                                                 | 606 ms: 1.25x slower                                                  |
| async_tree_cpu_io_mixed    | 501 ms                                                                 | 626 ms: 1.25x slower                                                  |
| async_tree_io_tg           | 631 ms                                                                 | 804 ms: 1.27x slower                                                  |
| async_tree_io              | 629 ms                                                                 | 821 ms: 1.31x slower                                                  |
| async_tree_none_tg         | 263 ms                                                                 | 350 ms: 1.33x slower                                                  |
| async_tree_none            | 279 ms                                                                 | 379 ms: 1.36x slower                                                  |
| async_tree_memoization     | 337 ms                                                                 | 459 ms: 1.36x slower                                                  |
| async_tree_memoization_tg  | 315 ms                                                                 | 439 ms: 1.39x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.26x slower                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241204-vultr-x86_64-python-51cfa569e379f84b3418-3.14.0a2+-51cfa56 | bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 185 ms                                                                 | 181 ms: 1.02x faster                                                  |
| nbody          | 94.9 ms                                                                | 126 ms: 1.33x slower                                                  |
| float          | 78.1 ms                                                                | 139 ms: 1.77x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.32x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241204-vultr-x86_64-python-51cfa569e379f84b3418-3.14.0a2+-51cfa56 | bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 2.79 ms                                                                | 2.89 ms: 1.04x slower                                                 |
| regex_v8       | 23.5 ms                                                                | 24.7 ms: 1.05x slower                                                 |
| regex_dna      | 173 ms                                                                 | 185 ms: 1.07x slower                                                  |
| regex_compile  | 129 ms                                                                 | 178 ms: 1.38x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.13x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241204-vultr-x86_64-python-51cfa569e379f84b3418-3.14.0a2+-51cfa56 | bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 91.8 ms                                                                | 91.2 ms: 1.01x faster                                                 |
| xml_etree_parse      | 129 ms                                                                 | 131 ms: 1.02x slower                                                  |
| json_loads           | 25.2 us                                                                | 28.3 us: 1.12x slower                                                 |
| xml_etree_generate   | 84.9 ms                                                                | 97.6 ms: 1.15x slower                                                 |
| json_dumps           | 11.4 ms                                                                | 13.9 ms: 1.23x slower                                                 |
| tomli_loads          | 2.09 sec                                                               | 2.64 sec: 1.26x slower                                                |
| xml_etree_process    | 59.3 ms                                                                | 78.2 ms: 1.32x slower                                                 |
| unpickle_pure_python | 216 us                                                                 | 332 us: 1.54x slower                                                  |
| pickle_pure_python   | 317 us                                                                 | 512 us: 1.62x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.23x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241204-vultr-x86_64-python-51cfa569e379f84b3418-3.14.0a2+-51cfa56 | bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                                | 17.2 ms: 1.18x slower                                                 |
| python_startup_no_site | 7.47 ms                                                                | 10.3 ms: 1.38x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.27x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241204-vultr-x86_64-python-51cfa569e379f84b3418-3.14.0a2+-51cfa56 | bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 50.3 ms                                                                | 62.7 ms: 1.25x slower                                                 |
| genshi_text     | 22.3 ms                                                                | 30.3 ms: 1.36x slower                                                 |
| django_template | 35.6 ms                                                                | 50.5 ms: 1.42x slower                                                 |
| mako            | 11.8 ms                                                                | 16.9 ms: 1.44x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.36x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20241204-vultr-x86_64-python-51cfa569e379f84b3418-3.14.0a2+-51cfa56 | bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal               | 4.26 ms                                                                | 3.53 ms: 1.21x faster                                                 |
| pidigits                   | 185 ms                                                                 | 181 ms: 1.02x faster                                                  |
| sqlite_synth               | 2.24 us                                                                | 2.21 us: 1.01x faster                                                 |
| xml_etree_iterparse        | 91.8 ms                                                                | 91.2 ms: 1.01x faster                                                 |
| asyncio_websockets         | 523 ms                                                                 | 520 ms: 1.01x faster                                                  |
| xml_etree_parse            | 129 ms                                                                 | 131 ms: 1.02x slower                                                  |
| regex_effbot               | 2.79 ms                                                                | 2.89 ms: 1.04x slower                                                 |
| regex_v8                   | 23.5 ms                                                                | 24.7 ms: 1.05x slower                                                 |
| regex_dna                  | 173 ms                                                                 | 185 ms: 1.07x slower                                                  |
| spectral_norm              | 113 ms                                                                 | 121 ms: 1.07x slower                                                  |
| pathlib                    | 18.2 ms                                                                | 20.1 ms: 1.10x slower                                                 |
| json                       | 4.53 ms                                                                | 5.01 ms: 1.10x slower                                                 |
| json_loads                 | 25.2 us                                                                | 28.3 us: 1.12x slower                                                 |
| mdp                        | 2.47 sec                                                               | 2.79 sec: 1.13x slower                                                |
| xml_etree_generate         | 84.9 ms                                                                | 97.6 ms: 1.15x slower                                                 |
| scimark_fft                | 335 ms                                                                 | 388 ms: 1.16x slower                                                  |
| coroutines                 | 22.1 ms                                                                | 25.5 ms: 1.16x slower                                                 |
| k_core                     | 2.07 sec                                                               | 2.41 sec: 1.16x slower                                                |
| bpe_tokeniser              | 4.32 sec                                                               | 5.04 sec: 1.16x slower                                                |
| python_startup             | 14.6 ms                                                                | 17.2 ms: 1.18x slower                                                 |
| sphinx                     | 991 ms                                                                 | 1.17 sec: 1.18x slower                                                |
| docutils                   | 2.56 sec                                                               | 3.08 sec: 1.20x slower                                                |
| telco                      | 7.27 ms                                                                | 8.84 ms: 1.22x slower                                                 |
| nqueens                    | 78.6 ms                                                                | 95.6 ms: 1.22x slower                                                 |
| bench_mp_pool              | 88.7 ms                                                                | 108 ms: 1.22x slower                                                  |
| json_dumps                 | 11.4 ms                                                                | 13.9 ms: 1.23x slower                                                 |
| many_optionals             | 1.02 ms                                                                | 1.27 ms: 1.24x slower                                                 |
| sqlglot_optimize           | 53.9 ms                                                                | 67.0 ms: 1.24x slower                                                 |
| shortest_path              | 444 ms                                                                 | 553 ms: 1.24x slower                                                  |
| genshi_xml                 | 50.3 ms                                                                | 62.7 ms: 1.25x slower                                                 |
| async_generators           | 369 ms                                                                 | 459 ms: 1.25x slower                                                  |
| async_tree_cpu_io_mixed_tg | 486 ms                                                                 | 606 ms: 1.25x slower                                                  |
| deepcopy                   | 260 us                                                                 | 325 us: 1.25x slower                                                  |
| async_tree_cpu_io_mixed    | 501 ms                                                                 | 626 ms: 1.25x slower                                                  |
| dulwich_log                | 75.8 ms                                                                | 94.9 ms: 1.25x slower                                                 |
| connected_components       | 400 ms                                                                 | 501 ms: 1.25x slower                                                  |
| tomli_loads                | 2.09 sec                                                               | 2.64 sec: 1.26x slower                                                |
| sqlglot_normalize          | 107 ms                                                                 | 136 ms: 1.27x slower                                                  |
| async_tree_io_tg           | 631 ms                                                                 | 804 ms: 1.27x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                                | 5.62 ms: 1.28x slower                                                 |
| coverage                   | 78.8 ms                                                                | 101 ms: 1.28x slower                                                  |
| typing_runtime_protocols   | 159 us                                                                 | 205 us: 1.29x slower                                                  |
| fannkuch                   | 379 ms                                                                 | 489 ms: 1.29x slower                                                  |
| deepcopy_reduce            | 2.65 us                                                                | 3.46 us: 1.30x slower                                                 |
| async_tree_io              | 629 ms                                                                 | 821 ms: 1.31x slower                                                  |
| pylint                     | 284 ms                                                                 | 371 ms: 1.31x slower                                                  |
| xml_etree_process          | 59.3 ms                                                                | 78.2 ms: 1.32x slower                                                 |
| pprint_safe_repr           | 723 ms                                                                 | 954 ms: 1.32x slower                                                  |
| meteor_contest             | 99.7 ms                                                                | 132 ms: 1.32x slower                                                  |
| nbody                      | 94.9 ms                                                                | 126 ms: 1.33x slower                                                  |
| crypto_pyaes               | 68.3 ms                                                                | 90.5 ms: 1.33x slower                                                 |
| async_tree_none_tg         | 263 ms                                                                 | 350 ms: 1.33x slower                                                  |
| deepcopy_memo              | 30.0 us                                                                | 40.1 us: 1.34x slower                                                 |
| generators                 | 28.7 ms                                                                | 38.6 ms: 1.34x slower                                                 |
| pycparser                  | 1.13 sec                                                               | 1.52 sec: 1.35x slower                                                |
| pprint_pformat             | 1.46 sec                                                               | 1.98 sec: 1.36x slower                                                |
| genshi_text                | 22.3 ms                                                                | 30.3 ms: 1.36x slower                                                 |
| async_tree_none            | 279 ms                                                                 | 379 ms: 1.36x slower                                                  |
| async_tree_memoization     | 337 ms                                                                 | 459 ms: 1.36x slower                                                  |
| python_startup_no_site     | 7.47 ms                                                                | 10.3 ms: 1.38x slower                                                 |
| regex_compile              | 129 ms                                                                 | 178 ms: 1.38x slower                                                  |
| async_tree_memoization_tg  | 315 ms                                                                 | 439 ms: 1.39x slower                                                  |
| subparsers                 | 22.0 ms                                                                | 30.9 ms: 1.40x slower                                                 |
| 2to3                       | 257 ms                                                                 | 363 ms: 1.41x slower                                                  |
| django_template            | 35.6 ms                                                                | 50.5 ms: 1.42x slower                                                 |
| mako                       | 11.8 ms                                                                | 16.9 ms: 1.44x slower                                                 |
| sympy_integrate            | 20.0 ms                                                                | 29.5 ms: 1.48x slower                                                 |
| unpickle_pure_python       | 216 us                                                                 | 332 us: 1.54x slower                                                  |
| sqlalchemy_imperative      | 18.9 ms                                                                | 29.2 ms: 1.54x slower                                                 |
| thrift                     | 734 us                                                                 | 1.15 ms: 1.56x slower                                                 |
| pyflate                    | 449 ms                                                                 | 703 ms: 1.57x slower                                                  |
| comprehensions             | 17.6 us                                                                | 27.8 us: 1.58x slower                                                 |
| sqlalchemy_declarative     | 127 ms                                                                 | 201 ms: 1.59x slower                                                  |
| logging_format             | 6.88 us                                                                | 11.0 us: 1.60x slower                                                 |
| pickle_pure_python         | 317 us                                                                 | 512 us: 1.62x slower                                                  |
| hexiom                     | 5.87 ms                                                                | 9.82 ms: 1.67x slower                                                 |
| logging_simple             | 6.06 us                                                                | 10.2 us: 1.68x slower                                                 |
| richards_super             | 52.4 ms                                                                | 88.0 ms: 1.68x slower                                                 |
| richards                   | 46.6 ms                                                                | 78.8 ms: 1.69x slower                                                 |
| scimark_lu                 | 109 ms                                                                 | 187 ms: 1.71x slower                                                  |
| sympy_str                  | 273 ms                                                                 | 476 ms: 1.74x slower                                                  |
| chaos                      | 58.9 ms                                                                | 103 ms: 1.74x slower                                                  |
| logging_silent             | 106 ns                                                                 | 186 ns: 1.76x slower                                                  |
| scimark_sor                | 134 ms                                                                 | 237 ms: 1.77x slower                                                  |
| float                      | 78.1 ms                                                                | 139 ms: 1.77x slower                                                  |
| scimark_monte_carlo        | 65.2 ms                                                                | 118 ms: 1.81x slower                                                  |
| sqlglot_transpile          | 1.61 ms                                                                | 2.96 ms: 1.84x slower                                                 |
| sqlglot_parse              | 1.29 ms                                                                | 2.57 ms: 1.99x slower                                                 |
| sympy_expand               | 462 ms                                                                 | 955 ms: 2.07x slower                                                  |
| raytrace                   | 264 ms                                                                 | 559 ms: 2.12x slower                                                  |
| go                         | 120 ms                                                                 | 270 ms: 2.24x slower                                                  |
| sympy_sum                  | 154 ms                                                                 | 349 ms: 2.27x slower                                                  |
| deltablue                  | 3.22 ms                                                                | 8.20 ms: 2.55x slower                                                 |
| bench_thread_pool          | 1.01 ms                                                                | 3.34 ms: 3.29x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.37x slower                                                          |

Benchmark hidden because not significant (1): create_gc_cycles
Ignored benchmarks (1) of results/bm-20241204-3.14.0a2+-de73a27-NOGIL/bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27.json: html5lib

- Geometric mean (including insignificant results): 1.263x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.27x
- 95% likely to have a slowdown of 1.27x
- 99% likely to have a slowdown of 1.25x

# Memory
- memory change: 1.20x