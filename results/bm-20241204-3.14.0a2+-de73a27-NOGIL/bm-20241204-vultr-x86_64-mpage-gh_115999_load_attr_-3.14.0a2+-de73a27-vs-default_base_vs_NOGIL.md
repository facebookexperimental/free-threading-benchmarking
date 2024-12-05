# Results vs. default_base_vs_NOGIL

- fork: mpage
- ref: gh_115999_load_attr_
- machine: linux-x86_64
- commit hash: de73a27
- commit date: 2024-12-04
- overall geometric mean: 1.266x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.26x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241204-vultr-x86_64-python-51cfa569e379f84b3418-3.14.0a2+-51cfa56 | bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 257 ms                                                                 | 365 ms: 1.42x slower                                                  |
| docutils       | 2.56 sec                                                               | 3.07 sec: 1.20x slower                                                |
| sphinx         | 991 ms                                                                 | 1.17 sec: 1.18x slower                                                |
| Geometric mean | (ref)                                                                  | 1.26x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241204-vultr-x86_64-python-51cfa569e379f84b3418-3.14.0a2+-51cfa56 | bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| asyncio_websockets         | 523 ms                                                                 | 520 ms: 1.01x faster                                                  |
| coroutines                 | 22.1 ms                                                                | 25.8 ms: 1.17x slower                                                 |
| async_generators           | 369 ms                                                                 | 454 ms: 1.23x slower                                                  |
| async_tree_cpu_io_mixed_tg | 486 ms                                                                 | 602 ms: 1.24x slower                                                  |
| async_tree_cpu_io_mixed    | 501 ms                                                                 | 626 ms: 1.25x slower                                                  |
| async_tree_io_tg           | 631 ms                                                                 | 798 ms: 1.26x slower                                                  |
| async_tree_io              | 629 ms                                                                 | 818 ms: 1.30x slower                                                  |
| async_tree_none_tg         | 263 ms                                                                 | 348 ms: 1.32x slower                                                  |
| async_tree_none            | 279 ms                                                                 | 379 ms: 1.36x slower                                                  |
| async_tree_memoization     | 337 ms                                                                 | 459 ms: 1.36x slower                                                  |
| async_tree_memoization_tg  | 315 ms                                                                 | 437 ms: 1.39x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.26x slower                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241204-vultr-x86_64-python-51cfa569e379f84b3418-3.14.0a2+-51cfa56 | bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 185 ms                                                                 | 183 ms: 1.01x faster                                                  |
| nbody          | 94.9 ms                                                                | 134 ms: 1.41x slower                                                  |
| float          | 78.1 ms                                                                | 142 ms: 1.82x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.36x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241204-vultr-x86_64-python-51cfa569e379f84b3418-3.14.0a2+-51cfa56 | bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 23.5 ms                                                                | 24.7 ms: 1.05x slower                                                 |
| regex_effbot   | 2.79 ms                                                                | 2.94 ms: 1.05x slower                                                 |
| regex_dna      | 173 ms                                                                 | 188 ms: 1.09x slower                                                  |
| regex_compile  | 129 ms                                                                 | 181 ms: 1.40x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.14x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241204-vultr-x86_64-python-51cfa569e379f84b3418-3.14.0a2+-51cfa56 | bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_parse      | 129 ms                                                                 | 131 ms: 1.02x slower                                                  |
| json_loads           | 25.2 us                                                                | 28.4 us: 1.13x slower                                                 |
| xml_etree_generate   | 84.9 ms                                                                | 98.2 ms: 1.16x slower                                                 |
| json_dumps           | 11.4 ms                                                                | 14.1 ms: 1.24x slower                                                 |
| tomli_loads          | 2.09 sec                                                               | 2.68 sec: 1.29x slower                                                |
| xml_etree_process    | 59.3 ms                                                                | 78.6 ms: 1.33x slower                                                 |
| unpickle_pure_python | 216 us                                                                 | 338 us: 1.57x slower                                                  |
| pickle_pure_python   | 317 us                                                                 | 513 us: 1.62x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.24x slower                                                          |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241204-vultr-x86_64-python-51cfa569e379f84b3418-3.14.0a2+-51cfa56 | bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                                | 17.2 ms: 1.18x slower                                                 |
| python_startup_no_site | 7.47 ms                                                                | 10.3 ms: 1.37x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.27x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241204-vultr-x86_64-python-51cfa569e379f84b3418-3.14.0a2+-51cfa56 | bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 50.3 ms                                                                | 63.0 ms: 1.25x slower                                                 |
| genshi_text     | 22.3 ms                                                                | 30.4 ms: 1.36x slower                                                 |
| django_template | 35.6 ms                                                                | 50.6 ms: 1.42x slower                                                 |
| mako            | 11.8 ms                                                                | 17.1 ms: 1.45x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.37x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20241204-vultr-x86_64-python-51cfa569e379f84b3418-3.14.0a2+-51cfa56 | bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal               | 4.26 ms                                                                | 3.31 ms: 1.29x faster                                                 |
| create_gc_cycles           | 1.86 ms                                                                | 1.83 ms: 1.02x faster                                                 |
| sqlite_synth               | 2.24 us                                                                | 2.22 us: 1.01x faster                                                 |
| pidigits                   | 185 ms                                                                 | 183 ms: 1.01x faster                                                  |
| asyncio_websockets         | 523 ms                                                                 | 520 ms: 1.01x faster                                                  |
| xml_etree_parse            | 129 ms                                                                 | 131 ms: 1.02x slower                                                  |
| regex_v8                   | 23.5 ms                                                                | 24.7 ms: 1.05x slower                                                 |
| regex_effbot               | 2.79 ms                                                                | 2.94 ms: 1.05x slower                                                 |
| spectral_norm              | 113 ms                                                                 | 122 ms: 1.08x slower                                                  |
| regex_dna                  | 173 ms                                                                 | 188 ms: 1.09x slower                                                  |
| pathlib                    | 18.2 ms                                                                | 20.1 ms: 1.10x slower                                                 |
| json                       | 4.53 ms                                                                | 5.07 ms: 1.12x slower                                                 |
| json_loads                 | 25.2 us                                                                | 28.4 us: 1.13x slower                                                 |
| mdp                        | 2.47 sec                                                               | 2.79 sec: 1.13x slower                                                |
| bpe_tokeniser              | 4.32 sec                                                               | 4.99 sec: 1.15x slower                                                |
| xml_etree_generate         | 84.9 ms                                                                | 98.2 ms: 1.16x slower                                                 |
| k_core                     | 2.07 sec                                                               | 2.42 sec: 1.17x slower                                                |
| coroutines                 | 22.1 ms                                                                | 25.8 ms: 1.17x slower                                                 |
| scimark_fft                | 335 ms                                                                 | 394 ms: 1.18x slower                                                  |
| python_startup             | 14.6 ms                                                                | 17.2 ms: 1.18x slower                                                 |
| sphinx                     | 991 ms                                                                 | 1.17 sec: 1.18x slower                                                |
| telco                      | 7.27 ms                                                                | 8.68 ms: 1.19x slower                                                 |
| docutils                   | 2.56 sec                                                               | 3.07 sec: 1.20x slower                                                |
| bench_mp_pool              | 88.7 ms                                                                | 108 ms: 1.22x slower                                                  |
| async_generators           | 369 ms                                                                 | 454 ms: 1.23x slower                                                  |
| many_optionals             | 1.02 ms                                                                | 1.26 ms: 1.24x slower                                                 |
| json_dumps                 | 11.4 ms                                                                | 14.1 ms: 1.24x slower                                                 |
| shortest_path              | 444 ms                                                                 | 550 ms: 1.24x slower                                                  |
| async_tree_cpu_io_mixed_tg | 486 ms                                                                 | 602 ms: 1.24x slower                                                  |
| deepcopy                   | 260 us                                                                 | 323 us: 1.24x slower                                                  |
| async_tree_cpu_io_mixed    | 501 ms                                                                 | 626 ms: 1.25x slower                                                  |
| nqueens                    | 78.6 ms                                                                | 98.1 ms: 1.25x slower                                                 |
| sqlglot_optimize           | 53.9 ms                                                                | 67.3 ms: 1.25x slower                                                 |
| connected_components       | 400 ms                                                                 | 500 ms: 1.25x slower                                                  |
| genshi_xml                 | 50.3 ms                                                                | 63.0 ms: 1.25x slower                                                 |
| dulwich_log                | 75.8 ms                                                                | 95.0 ms: 1.25x slower                                                 |
| async_tree_io_tg           | 631 ms                                                                 | 798 ms: 1.26x slower                                                  |
| sqlglot_normalize          | 107 ms                                                                 | 136 ms: 1.27x slower                                                  |
| tomli_loads                | 2.09 sec                                                               | 2.68 sec: 1.29x slower                                                |
| deepcopy_reduce            | 2.65 us                                                                | 3.41 us: 1.29x slower                                                 |
| typing_runtime_protocols   | 159 us                                                                 | 206 us: 1.29x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                                | 5.69 ms: 1.30x slower                                                 |
| fannkuch                   | 379 ms                                                                 | 492 ms: 1.30x slower                                                  |
| async_tree_io              | 629 ms                                                                 | 818 ms: 1.30x slower                                                  |
| pylint                     | 284 ms                                                                 | 372 ms: 1.31x slower                                                  |
| crypto_pyaes               | 68.3 ms                                                                | 89.7 ms: 1.31x slower                                                 |
| async_tree_none_tg         | 263 ms                                                                 | 348 ms: 1.32x slower                                                  |
| coverage                   | 78.8 ms                                                                | 104 ms: 1.32x slower                                                  |
| xml_etree_process          | 59.3 ms                                                                | 78.6 ms: 1.33x slower                                                 |
| deepcopy_memo              | 30.0 us                                                                | 40.0 us: 1.33x slower                                                 |
| meteor_contest             | 99.7 ms                                                                | 134 ms: 1.34x slower                                                  |
| pprint_safe_repr           | 723 ms                                                                 | 973 ms: 1.35x slower                                                  |
| pycparser                  | 1.13 sec                                                               | 1.52 sec: 1.35x slower                                                |
| async_tree_none            | 279 ms                                                                 | 379 ms: 1.36x slower                                                  |
| genshi_text                | 22.3 ms                                                                | 30.4 ms: 1.36x slower                                                 |
| async_tree_memoization     | 337 ms                                                                 | 459 ms: 1.36x slower                                                  |
| python_startup_no_site     | 7.47 ms                                                                | 10.3 ms: 1.37x slower                                                 |
| generators                 | 28.7 ms                                                                | 39.6 ms: 1.38x slower                                                 |
| pprint_pformat             | 1.46 sec                                                               | 2.02 sec: 1.38x slower                                                |
| async_tree_memoization_tg  | 315 ms                                                                 | 437 ms: 1.39x slower                                                  |
| subparsers                 | 22.0 ms                                                                | 30.6 ms: 1.39x slower                                                 |
| regex_compile              | 129 ms                                                                 | 181 ms: 1.40x slower                                                  |
| nbody                      | 94.9 ms                                                                | 134 ms: 1.41x slower                                                  |
| django_template            | 35.6 ms                                                                | 50.6 ms: 1.42x slower                                                 |
| 2to3                       | 257 ms                                                                 | 365 ms: 1.42x slower                                                  |
| mako                       | 11.8 ms                                                                | 17.1 ms: 1.45x slower                                                 |
| sympy_integrate            | 20.0 ms                                                                | 29.6 ms: 1.48x slower                                                 |
| thrift                     | 734 us                                                                 | 1.12 ms: 1.53x slower                                                 |
| sqlalchemy_imperative      | 18.9 ms                                                                | 28.9 ms: 1.53x slower                                                 |
| pyflate                    | 449 ms                                                                 | 703 ms: 1.57x slower                                                  |
| unpickle_pure_python       | 216 us                                                                 | 338 us: 1.57x slower                                                  |
| sqlalchemy_declarative     | 127 ms                                                                 | 201 ms: 1.59x slower                                                  |
| comprehensions             | 17.6 us                                                                | 28.1 us: 1.60x slower                                                 |
| logging_format             | 6.88 us                                                                | 11.1 us: 1.61x slower                                                 |
| pickle_pure_python         | 317 us                                                                 | 513 us: 1.62x slower                                                  |
| logging_simple             | 6.06 us                                                                | 10.1 us: 1.66x slower                                                 |
| scimark_lu                 | 109 ms                                                                 | 184 ms: 1.69x slower                                                  |
| richards                   | 46.6 ms                                                                | 79.4 ms: 1.71x slower                                                 |
| hexiom                     | 5.87 ms                                                                | 10.0 ms: 1.71x slower                                                 |
| richards_super             | 52.4 ms                                                                | 89.5 ms: 1.71x slower                                                 |
| sympy_str                  | 273 ms                                                                 | 479 ms: 1.75x slower                                                  |
| chaos                      | 58.9 ms                                                                | 104 ms: 1.77x slower                                                  |
| scimark_sor                | 134 ms                                                                 | 237 ms: 1.77x slower                                                  |
| logging_silent             | 106 ns                                                                 | 190 ns: 1.80x slower                                                  |
| float                      | 78.1 ms                                                                | 142 ms: 1.82x slower                                                  |
| scimark_monte_carlo        | 65.2 ms                                                                | 121 ms: 1.85x slower                                                  |
| sqlglot_transpile          | 1.61 ms                                                                | 3.02 ms: 1.87x slower                                                 |
| sqlglot_parse              | 1.29 ms                                                                | 2.62 ms: 2.03x slower                                                 |
| sympy_expand               | 462 ms                                                                 | 961 ms: 2.08x slower                                                  |
| raytrace                   | 264 ms                                                                 | 559 ms: 2.12x slower                                                  |
| sympy_sum                  | 154 ms                                                                 | 349 ms: 2.27x slower                                                  |
| go                         | 120 ms                                                                 | 275 ms: 2.28x slower                                                  |
| deltablue                  | 3.22 ms                                                                | 8.34 ms: 2.59x slower                                                 |
| bench_thread_pool          | 1.01 ms                                                                | 3.33 ms: 3.28x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.38x slower                                                          |

Benchmark hidden because not significant (1): xml_etree_iterparse
Ignored benchmarks (1) of results/bm-20241204-3.14.0a2+-de73a27-NOGIL/bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27.json: html5lib

- Geometric mean (including insignificant results): 1.266x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.28x
- 95% likely to have a slowdown of 1.28x
- 99% likely to have a slowdown of 1.26x

# Memory
- memory change: 1.19x