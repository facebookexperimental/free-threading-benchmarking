# Results vs. default_base_vs_NOGIL

- fork: mpage
- ref: gh_115999_load_attr_
- machine: linux-x86_64
- commit hash: 1b787b3
- commit date: 2024-12-20
- overall geometric mean: 1.155x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.13x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-1b787b3 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 256 ms                                                                 | 322 ms: 1.26x slower                                                  |
| docutils       | 2.54 sec                                                               | 2.85 sec: 1.12x slower                                                |
| sphinx         | 989 ms                                                                 | 1.11 sec: 1.13x slower                                                |
| Geometric mean | (ref)                                                                  | 1.17x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-1b787b3 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 549 ms                                                                 | 483 ms: 1.14x faster                                                  |
| async_tree_cpu_io_mixed    | 566 ms                                                                 | 520 ms: 1.09x faster                                                  |
| async_tree_none_tg         | 254 ms                                                                 | 239 ms: 1.06x faster                                                  |
| async_tree_io              | 624 ms                                                                 | 606 ms: 1.03x faster                                                  |
| async_tree_io_tg           | 605 ms                                                                 | 591 ms: 1.02x faster                                                  |
| asyncio_websockets         | 523 ms                                                                 | 520 ms: 1.00x faster                                                  |
| async_tree_memoization_tg  | 307 ms                                                                 | 311 ms: 1.01x slower                                                  |
| async_tree_none            | 275 ms                                                                 | 284 ms: 1.03x slower                                                  |
| async_tree_memoization     | 332 ms                                                                 | 349 ms: 1.05x slower                                                  |
| coroutines                 | 22.2 ms                                                                | 24.4 ms: 1.10x slower                                                 |
| async_generators           | 357 ms                                                                 | 414 ms: 1.16x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-1b787b3 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                                 | 184 ms: 1.18x faster                                                  |
| float          | 74.6 ms                                                                | 81.3 ms: 1.09x slower                                                 |
| nbody          | 91.1 ms                                                                | 130 ms: 1.43x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.10x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-1b787b3 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 25.0 ms                                                                | 23.5 ms: 1.07x faster                                                 |
| regex_dna      | 181 ms                                                                 | 172 ms: 1.05x faster                                                  |
| regex_effbot   | 2.81 ms                                                                | 2.68 ms: 1.05x faster                                                 |
| regex_compile  | 127 ms                                                                 | 150 ms: 1.18x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-1b787b3 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 90.6 ms                                                                | 88.3 ms: 1.03x faster                                                 |
| xml_etree_parse      | 127 ms                                                                 | 129 ms: 1.02x slower                                                  |
| json_loads           | 26.1 us                                                                | 28.1 us: 1.08x slower                                                 |
| xml_etree_generate   | 82.9 ms                                                                | 96.0 ms: 1.16x slower                                                 |
| json_dumps           | 11.3 ms                                                                | 13.1 ms: 1.16x slower                                                 |
| pickle_pure_python   | 316 us                                                                 | 370 us: 1.17x slower                                                  |
| xml_etree_process    | 57.9 ms                                                                | 68.2 ms: 1.18x slower                                                 |
| unpickle_pure_python | 213 us                                                                 | 254 us: 1.19x slower                                                  |
| tomli_loads          | 1.90 sec                                                               | 2.52 sec: 1.33x slower                                                |
| Geometric mean       | (ref)                                                                  | 1.14x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-1b787b3 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                                | 17.1 ms: 1.16x slower                                                 |
| python_startup_no_site | 7.48 ms                                                                | 10.2 ms: 1.36x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.26x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-1b787b3 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.7 ms                                                                | 42.4 ms: 1.22x slower                                                 |
| genshi_xml      | 48.9 ms                                                                | 60.0 ms: 1.23x slower                                                 |
| genshi_text     | 21.4 ms                                                                | 28.3 ms: 1.32x slower                                                 |
| mako            | 11.5 ms                                                                | 15.6 ms: 1.36x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.28x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-1b787b3 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal               | 4.37 ms                                                                | 3.49 ms: 1.25x faster                                                 |
| pidigits                   | 217 ms                                                                 | 184 ms: 1.18x faster                                                  |
| async_tree_cpu_io_mixed_tg | 549 ms                                                                 | 483 ms: 1.14x faster                                                  |
| async_tree_cpu_io_mixed    | 566 ms                                                                 | 520 ms: 1.09x faster                                                  |
| sqlite_synth               | 2.21 us                                                                | 2.07 us: 1.07x faster                                                 |
| regex_v8                   | 25.0 ms                                                                | 23.5 ms: 1.07x faster                                                 |
| async_tree_none_tg         | 254 ms                                                                 | 239 ms: 1.06x faster                                                  |
| regex_dna                  | 181 ms                                                                 | 172 ms: 1.05x faster                                                  |
| regex_effbot               | 2.81 ms                                                                | 2.68 ms: 1.05x faster                                                 |
| async_tree_io              | 624 ms                                                                 | 606 ms: 1.03x faster                                                  |
| xml_etree_iterparse        | 90.6 ms                                                                | 88.3 ms: 1.03x faster                                                 |
| async_tree_io_tg           | 605 ms                                                                 | 591 ms: 1.02x faster                                                  |
| create_gc_cycles           | 1.85 ms                                                                | 1.82 ms: 1.02x faster                                                 |
| asyncio_websockets         | 523 ms                                                                 | 520 ms: 1.00x faster                                                  |
| async_tree_memoization_tg  | 307 ms                                                                 | 311 ms: 1.01x slower                                                  |
| xml_etree_parse            | 127 ms                                                                 | 129 ms: 1.02x slower                                                  |
| async_tree_none            | 275 ms                                                                 | 284 ms: 1.03x slower                                                  |
| json                       | 4.79 ms                                                                | 4.96 ms: 1.04x slower                                                 |
| pathlib                    | 17.9 ms                                                                | 18.8 ms: 1.05x slower                                                 |
| async_tree_memoization     | 332 ms                                                                 | 349 ms: 1.05x slower                                                  |
| logging_silent             | 106 ns                                                                 | 113 ns: 1.06x slower                                                  |
| json_loads                 | 26.1 us                                                                | 28.1 us: 1.08x slower                                                 |
| float                      | 74.6 ms                                                                | 81.3 ms: 1.09x slower                                                 |
| pycparser                  | 1.11 sec                                                               | 1.22 sec: 1.09x slower                                                |
| coroutines                 | 22.2 ms                                                                | 24.4 ms: 1.10x slower                                                 |
| dulwich_log                | 74.3 ms                                                                | 82.3 ms: 1.11x slower                                                 |
| bpe_tokeniser              | 4.28 sec                                                               | 4.76 sec: 1.11x slower                                                |
| docutils                   | 2.54 sec                                                               | 2.85 sec: 1.12x slower                                                |
| generators                 | 27.1 ms                                                                | 30.5 ms: 1.13x slower                                                 |
| sphinx                     | 989 ms                                                                 | 1.11 sec: 1.13x slower                                                |
| k_core                     | 2.06 sec                                                               | 2.32 sec: 1.13x slower                                                |
| many_optionals             | 1.03 ms                                                                | 1.18 ms: 1.14x slower                                                 |
| spectral_norm              | 97.3 ms                                                                | 113 ms: 1.16x slower                                                  |
| xml_etree_generate         | 82.9 ms                                                                | 96.0 ms: 1.16x slower                                                 |
| json_dumps                 | 11.3 ms                                                                | 13.1 ms: 1.16x slower                                                 |
| async_generators           | 357 ms                                                                 | 414 ms: 1.16x slower                                                  |
| python_startup             | 14.6 ms                                                                | 17.1 ms: 1.16x slower                                                 |
| pickle_pure_python         | 316 us                                                                 | 370 us: 1.17x slower                                                  |
| sqlglot_optimize           | 52.0 ms                                                                | 60.9 ms: 1.17x slower                                                 |
| telco                      | 7.25 ms                                                                | 8.50 ms: 1.17x slower                                                 |
| subparsers                 | 21.6 ms                                                                | 25.4 ms: 1.18x slower                                                 |
| sqlglot_normalize          | 103 ms                                                                 | 121 ms: 1.18x slower                                                  |
| xml_etree_process          | 57.9 ms                                                                | 68.2 ms: 1.18x slower                                                 |
| regex_compile              | 127 ms                                                                 | 150 ms: 1.18x slower                                                  |
| mdp                        | 2.34 sec                                                               | 2.78 sec: 1.19x slower                                                |
| bench_mp_pool              | 88.6 ms                                                                | 105 ms: 1.19x slower                                                  |
| unpickle_pure_python       | 213 us                                                                 | 254 us: 1.19x slower                                                  |
| chaos                      | 58.9 ms                                                                | 71.0 ms: 1.21x slower                                                 |
| pprint_safe_repr           | 704 ms                                                                 | 850 ms: 1.21x slower                                                  |
| logging_simple             | 5.95 us                                                                | 7.21 us: 1.21x slower                                                 |
| pprint_pformat             | 1.44 sec                                                               | 1.75 sec: 1.22x slower                                                |
| scimark_fft                | 313 ms                                                                 | 383 ms: 1.22x slower                                                  |
| pylint                     | 282 ms                                                                 | 344 ms: 1.22x slower                                                  |
| django_template            | 34.7 ms                                                                | 42.4 ms: 1.22x slower                                                 |
| thrift                     | 739 us                                                                 | 905 us: 1.22x slower                                                  |
| genshi_xml                 | 48.9 ms                                                                | 60.0 ms: 1.23x slower                                                 |
| deepcopy                   | 253 us                                                                 | 311 us: 1.23x slower                                                  |
| go                         | 116 ms                                                                 | 143 ms: 1.23x slower                                                  |
| pyflate                    | 419 ms                                                                 | 516 ms: 1.23x slower                                                  |
| sqlglot_transpile          | 1.56 ms                                                                | 1.93 ms: 1.24x slower                                                 |
| raytrace                   | 260 ms                                                                 | 322 ms: 1.24x slower                                                  |
| connected_components       | 394 ms                                                                 | 489 ms: 1.24x slower                                                  |
| logging_format             | 6.63 us                                                                | 8.27 us: 1.25x slower                                                 |
| shortest_path              | 433 ms                                                                 | 541 ms: 1.25x slower                                                  |
| nqueens                    | 77.7 ms                                                                | 97.1 ms: 1.25x slower                                                 |
| deepcopy_reduce            | 2.57 us                                                                | 3.23 us: 1.25x slower                                                 |
| 2to3                       | 256 ms                                                                 | 322 ms: 1.26x slower                                                  |
| comprehensions             | 17.0 us                                                                | 21.4 us: 1.26x slower                                                 |
| coverage                   | 79.2 ms                                                                | 100.0 ms: 1.26x slower                                                |
| typing_runtime_protocols   | 157 us                                                                 | 199 us: 1.26x slower                                                  |
| sqlalchemy_imperative      | 19.4 ms                                                                | 24.5 ms: 1.26x slower                                                 |
| deepcopy_memo              | 30.1 us                                                                | 38.4 us: 1.27x slower                                                 |
| sqlglot_parse              | 1.26 ms                                                                | 1.60 ms: 1.28x slower                                                 |
| scimark_lu                 | 111 ms                                                                 | 142 ms: 1.28x slower                                                  |
| richards                   | 42.3 ms                                                                | 54.8 ms: 1.29x slower                                                 |
| crypto_pyaes               | 67.5 ms                                                                | 87.5 ms: 1.30x slower                                                 |
| hexiom                     | 5.88 ms                                                                | 7.66 ms: 1.30x slower                                                 |
| richards_super             | 48.6 ms                                                                | 63.8 ms: 1.31x slower                                                 |
| meteor_contest             | 98.9 ms                                                                | 130 ms: 1.31x slower                                                  |
| genshi_text                | 21.4 ms                                                                | 28.3 ms: 1.32x slower                                                 |
| tomli_loads                | 1.90 sec                                                               | 2.52 sec: 1.33x slower                                                |
| scimark_sparse_mat_mult    | 4.26 ms                                                                | 5.67 ms: 1.33x slower                                                 |
| scimark_monte_carlo        | 63.4 ms                                                                | 84.6 ms: 1.33x slower                                                 |
| fannkuch                   | 365 ms                                                                 | 489 ms: 1.34x slower                                                  |
| python_startup_no_site     | 7.48 ms                                                                | 10.2 ms: 1.36x slower                                                 |
| mako                       | 11.5 ms                                                                | 15.6 ms: 1.36x slower                                                 |
| sqlalchemy_declarative     | 128 ms                                                                 | 176 ms: 1.37x slower                                                  |
| scimark_sor                | 117 ms                                                                 | 161 ms: 1.38x slower                                                  |
| nbody                      | 91.1 ms                                                                | 130 ms: 1.43x slower                                                  |
| sympy_integrate            | 19.8 ms                                                                | 28.7 ms: 1.45x slower                                                 |
| deltablue                  | 3.17 ms                                                                | 4.82 ms: 1.52x slower                                                 |
| sympy_str                  | 272 ms                                                                 | 458 ms: 1.69x slower                                                  |
| sympy_expand               | 456 ms                                                                 | 926 ms: 2.03x slower                                                  |
| sympy_sum                  | 153 ms                                                                 | 341 ms: 2.23x slower                                                  |
| bench_thread_pool          | 1.03 ms                                                                | 3.33 ms: 3.23x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.20x slower                                                          |
Ignored benchmarks (1) of results/bm-20241220-3.14.0a3+-1b787b3-NOGIL/bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-1b787b3.json: html5lib

- Geometric mean (including insignificant results): 1.155x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.15x
- 95% likely to have a slowdown of 1.15x
- 99% likely to have a slowdown of 1.13x

# Memory
- memory change: 1.20x