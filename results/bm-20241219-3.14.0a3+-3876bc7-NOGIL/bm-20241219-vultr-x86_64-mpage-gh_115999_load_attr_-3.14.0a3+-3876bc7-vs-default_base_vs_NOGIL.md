# Results vs. default_base_vs_NOGIL

- fork: mpage
- ref: gh_115999_load_attr_
- machine: linux-x86_64
- commit hash: 3876bc7
- commit date: 2024-12-19
- overall geometric mean: 1.160x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.13x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241219-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-3876bc7 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 256 ms                                                                 | 324 ms: 1.27x slower                                                  |
| docutils       | 2.54 sec                                                               | 2.86 sec: 1.12x slower                                                |
| sphinx         | 989 ms                                                                 | 1.12 sec: 1.13x slower                                                |
| Geometric mean | (ref)                                                                  | 1.17x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241219-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-3876bc7 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 549 ms                                                                 | 489 ms: 1.12x faster                                                  |
| async_tree_cpu_io_mixed    | 566 ms                                                                 | 524 ms: 1.08x faster                                                  |
| async_tree_none_tg         | 254 ms                                                                 | 241 ms: 1.06x faster                                                  |
| async_tree_io              | 624 ms                                                                 | 605 ms: 1.03x faster                                                  |
| asyncio_websockets         | 523 ms                                                                 | 518 ms: 1.01x faster                                                  |
| async_tree_memoization_tg  | 307 ms                                                                 | 312 ms: 1.02x slower                                                  |
| async_tree_none            | 275 ms                                                                 | 284 ms: 1.03x slower                                                  |
| async_tree_memoization     | 332 ms                                                                 | 351 ms: 1.06x slower                                                  |
| coroutines                 | 22.2 ms                                                                | 24.8 ms: 1.12x slower                                                 |
| async_generators           | 357 ms                                                                 | 430 ms: 1.21x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                          |

Benchmark hidden because not significant (1): async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241219-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-3876bc7 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                                 | 181 ms: 1.19x faster                                                  |
| float          | 74.6 ms                                                                | 82.7 ms: 1.11x slower                                                 |
| nbody          | 91.1 ms                                                                | 135 ms: 1.49x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.11x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241219-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-3876bc7 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 25.0 ms                                                                | 23.2 ms: 1.08x faster                                                 |
| regex_effbot   | 2.81 ms                                                                | 2.78 ms: 1.01x faster                                                 |
| regex_compile  | 127 ms                                                                 | 151 ms: 1.19x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                          |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241219-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-3876bc7 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 90.6 ms                                                                | 88.8 ms: 1.02x faster                                                 |
| xml_etree_parse      | 127 ms                                                                 | 131 ms: 1.03x slower                                                  |
| json_loads           | 26.1 us                                                                | 28.3 us: 1.08x slower                                                 |
| json_dumps           | 11.3 ms                                                                | 13.0 ms: 1.15x slower                                                 |
| xml_etree_generate   | 82.9 ms                                                                | 97.0 ms: 1.17x slower                                                 |
| pickle_pure_python   | 316 us                                                                 | 372 us: 1.18x slower                                                  |
| unpickle_pure_python | 213 us                                                                 | 252 us: 1.19x slower                                                  |
| xml_etree_process    | 57.9 ms                                                                | 69.2 ms: 1.20x slower                                                 |
| tomli_loads          | 1.90 sec                                                               | 2.50 sec: 1.32x slower                                                |
| Geometric mean       | (ref)                                                                  | 1.14x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241219-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-3876bc7 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                                | 17.1 ms: 1.17x slower                                                 |
| python_startup_no_site | 7.48 ms                                                                | 10.2 ms: 1.36x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.26x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241219-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-3876bc7 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.7 ms                                                                | 43.0 ms: 1.24x slower                                                 |
| genshi_xml      | 48.9 ms                                                                | 60.8 ms: 1.24x slower                                                 |
| genshi_text     | 21.4 ms                                                                | 28.5 ms: 1.33x slower                                                 |
| mako            | 11.5 ms                                                                | 15.6 ms: 1.35x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.29x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241219-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-3876bc7 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal               | 4.37 ms                                                                | 3.50 ms: 1.25x faster                                                 |
| pidigits                   | 217 ms                                                                 | 181 ms: 1.19x faster                                                  |
| async_tree_cpu_io_mixed_tg | 549 ms                                                                 | 489 ms: 1.12x faster                                                  |
| async_tree_cpu_io_mixed    | 566 ms                                                                 | 524 ms: 1.08x faster                                                  |
| regex_v8                   | 25.0 ms                                                                | 23.2 ms: 1.08x faster                                                 |
| sqlite_synth               | 2.21 us                                                                | 2.07 us: 1.07x faster                                                 |
| async_tree_none_tg         | 254 ms                                                                 | 241 ms: 1.06x faster                                                  |
| async_tree_io              | 624 ms                                                                 | 605 ms: 1.03x faster                                                  |
| xml_etree_iterparse        | 90.6 ms                                                                | 88.8 ms: 1.02x faster                                                 |
| create_gc_cycles           | 1.85 ms                                                                | 1.82 ms: 1.02x faster                                                 |
| regex_effbot               | 2.81 ms                                                                | 2.78 ms: 1.01x faster                                                 |
| asyncio_websockets         | 523 ms                                                                 | 518 ms: 1.01x faster                                                  |
| async_tree_memoization_tg  | 307 ms                                                                 | 312 ms: 1.02x slower                                                  |
| async_tree_none            | 275 ms                                                                 | 284 ms: 1.03x slower                                                  |
| xml_etree_parse            | 127 ms                                                                 | 131 ms: 1.03x slower                                                  |
| json                       | 4.79 ms                                                                | 5.00 ms: 1.04x slower                                                 |
| pathlib                    | 17.9 ms                                                                | 18.9 ms: 1.05x slower                                                 |
| async_tree_memoization     | 332 ms                                                                 | 351 ms: 1.06x slower                                                  |
| logging_silent             | 106 ns                                                                 | 115 ns: 1.08x slower                                                  |
| json_loads                 | 26.1 us                                                                | 28.3 us: 1.08x slower                                                 |
| pycparser                  | 1.11 sec                                                               | 1.21 sec: 1.09x slower                                                |
| float                      | 74.6 ms                                                                | 82.7 ms: 1.11x slower                                                 |
| dulwich_log                | 74.3 ms                                                                | 82.8 ms: 1.11x slower                                                 |
| coroutines                 | 22.2 ms                                                                | 24.8 ms: 1.12x slower                                                 |
| mdp                        | 2.34 sec                                                               | 2.61 sec: 1.12x slower                                                |
| bpe_tokeniser              | 4.28 sec                                                               | 4.81 sec: 1.12x slower                                                |
| docutils                   | 2.54 sec                                                               | 2.86 sec: 1.12x slower                                                |
| k_core                     | 2.06 sec                                                               | 2.33 sec: 1.13x slower                                                |
| spectral_norm              | 97.3 ms                                                                | 110 ms: 1.13x slower                                                  |
| sphinx                     | 989 ms                                                                 | 1.12 sec: 1.13x slower                                                |
| many_optionals             | 1.03 ms                                                                | 1.18 ms: 1.14x slower                                                 |
| json_dumps                 | 11.3 ms                                                                | 13.0 ms: 1.15x slower                                                 |
| generators                 | 27.1 ms                                                                | 31.3 ms: 1.15x slower                                                 |
| python_startup             | 14.6 ms                                                                | 17.1 ms: 1.17x slower                                                 |
| xml_etree_generate         | 82.9 ms                                                                | 97.0 ms: 1.17x slower                                                 |
| subparsers                 | 21.6 ms                                                                | 25.3 ms: 1.17x slower                                                 |
| pickle_pure_python         | 316 us                                                                 | 372 us: 1.18x slower                                                  |
| sqlglot_normalize          | 103 ms                                                                 | 121 ms: 1.18x slower                                                  |
| sqlglot_optimize           | 52.0 ms                                                                | 61.2 ms: 1.18x slower                                                 |
| unpickle_pure_python       | 213 us                                                                 | 252 us: 1.19x slower                                                  |
| telco                      | 7.25 ms                                                                | 8.62 ms: 1.19x slower                                                 |
| regex_compile              | 127 ms                                                                 | 151 ms: 1.19x slower                                                  |
| bench_mp_pool              | 88.6 ms                                                                | 106 ms: 1.19x slower                                                  |
| xml_etree_process          | 57.9 ms                                                                | 69.2 ms: 1.20x slower                                                 |
| pyflate                    | 419 ms                                                                 | 504 ms: 1.20x slower                                                  |
| async_generators           | 357 ms                                                                 | 430 ms: 1.21x slower                                                  |
| pprint_safe_repr           | 704 ms                                                                 | 849 ms: 1.21x slower                                                  |
| logging_simple             | 5.95 us                                                                | 7.26 us: 1.22x slower                                                 |
| pprint_pformat             | 1.44 sec                                                               | 1.76 sec: 1.22x slower                                                |
| chaos                      | 58.9 ms                                                                | 72.4 ms: 1.23x slower                                                 |
| thrift                     | 739 us                                                                 | 911 us: 1.23x slower                                                  |
| pylint                     | 282 ms                                                                 | 347 ms: 1.23x slower                                                  |
| scimark_fft                | 313 ms                                                                 | 386 ms: 1.23x slower                                                  |
| raytrace                   | 260 ms                                                                 | 322 ms: 1.24x slower                                                  |
| comprehensions             | 17.0 us                                                                | 21.0 us: 1.24x slower                                                 |
| django_template            | 34.7 ms                                                                | 43.0 ms: 1.24x slower                                                 |
| go                         | 116 ms                                                                 | 144 ms: 1.24x slower                                                  |
| deepcopy                   | 253 us                                                                 | 314 us: 1.24x slower                                                  |
| sqlglot_transpile          | 1.56 ms                                                                | 1.94 ms: 1.24x slower                                                 |
| genshi_xml                 | 48.9 ms                                                                | 60.8 ms: 1.24x slower                                                 |
| coverage                   | 79.2 ms                                                                | 98.6 ms: 1.24x slower                                                 |
| logging_format             | 6.63 us                                                                | 8.26 us: 1.25x slower                                                 |
| shortest_path              | 433 ms                                                                 | 542 ms: 1.25x slower                                                  |
| connected_components       | 394 ms                                                                 | 494 ms: 1.25x slower                                                  |
| nqueens                    | 77.7 ms                                                                | 97.4 ms: 1.25x slower                                                 |
| deepcopy_reduce            | 2.57 us                                                                | 3.23 us: 1.25x slower                                                 |
| scimark_lu                 | 111 ms                                                                 | 141 ms: 1.26x slower                                                  |
| 2to3                       | 256 ms                                                                 | 324 ms: 1.27x slower                                                  |
| sqlalchemy_imperative      | 19.4 ms                                                                | 24.5 ms: 1.27x slower                                                 |
| typing_runtime_protocols   | 157 us                                                                 | 200 us: 1.27x slower                                                  |
| sqlglot_parse              | 1.26 ms                                                                | 1.61 ms: 1.28x slower                                                 |
| hexiom                     | 5.88 ms                                                                | 7.61 ms: 1.29x slower                                                 |
| crypto_pyaes               | 67.5 ms                                                                | 88.0 ms: 1.30x slower                                                 |
| deepcopy_memo              | 30.1 us                                                                | 39.3 us: 1.30x slower                                                 |
| tomli_loads                | 1.90 sec                                                               | 2.50 sec: 1.32x slower                                                |
| meteor_contest             | 98.9 ms                                                                | 131 ms: 1.32x slower                                                  |
| genshi_text                | 21.4 ms                                                                | 28.5 ms: 1.33x slower                                                 |
| richards                   | 42.3 ms                                                                | 56.5 ms: 1.33x slower                                                 |
| fannkuch                   | 365 ms                                                                 | 488 ms: 1.34x slower                                                  |
| richards_super             | 48.6 ms                                                                | 65.8 ms: 1.35x slower                                                 |
| mako                       | 11.5 ms                                                                | 15.6 ms: 1.35x slower                                                 |
| scimark_sparse_mat_mult    | 4.26 ms                                                                | 5.78 ms: 1.36x slower                                                 |
| python_startup_no_site     | 7.48 ms                                                                | 10.2 ms: 1.36x slower                                                 |
| scimark_monte_carlo        | 63.4 ms                                                                | 86.9 ms: 1.37x slower                                                 |
| sqlalchemy_declarative     | 128 ms                                                                 | 177 ms: 1.38x slower                                                  |
| scimark_sor                | 117 ms                                                                 | 162 ms: 1.39x slower                                                  |
| sympy_integrate            | 19.8 ms                                                                | 28.9 ms: 1.46x slower                                                 |
| nbody                      | 91.1 ms                                                                | 135 ms: 1.49x slower                                                  |
| deltablue                  | 3.17 ms                                                                | 4.84 ms: 1.53x slower                                                 |
| sympy_str                  | 272 ms                                                                 | 461 ms: 1.70x slower                                                  |
| sympy_expand               | 456 ms                                                                 | 931 ms: 2.04x slower                                                  |
| sympy_sum                  | 153 ms                                                                 | 342 ms: 2.24x slower                                                  |
| bench_thread_pool          | 1.03 ms                                                                | 3.33 ms: 3.22x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.20x slower                                                          |

Benchmark hidden because not significant (2): async_tree_io_tg, regex_dna
Ignored benchmarks (1) of results/bm-20241219-3.14.0a3+-3876bc7-NOGIL/bm-20241219-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-3876bc7.json: html5lib

- Geometric mean (including insignificant results): 1.160x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.15x
- 95% likely to have a slowdown of 1.14x
- 99% likely to have a slowdown of 1.13x

# Memory
- memory change: 1.20x