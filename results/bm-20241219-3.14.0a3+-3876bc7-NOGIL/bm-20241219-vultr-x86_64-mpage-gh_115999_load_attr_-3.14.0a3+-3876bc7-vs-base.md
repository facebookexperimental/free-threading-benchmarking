# Results vs. base

- fork: mpage
- ref: gh_115999_load_attr_
- machine: linux-x86_64
- commit hash: 3876bc7
- commit date: 2024-12-19
- overall geometric mean: 1.116x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241219-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-3876bc7 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 361 ms                                                                 | 324 ms: 1.11x faster                                                  |
| docutils       | 3.02 sec                                                               | 2.86 sec: 1.06x faster                                                |
| html5lib       | 93.4 ms                                                                | 74.1 ms: 1.26x faster                                                 |
| sphinx         | 1.16 sec                                                               | 1.12 sec: 1.04x faster                                                |
| Geometric mean | (ref)                                                                  | 1.11x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241219-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-3876bc7 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none_tg         | 314 ms                                                                 | 241 ms: 1.30x faster                                                  |
| async_tree_memoization_tg  | 399 ms                                                                 | 312 ms: 1.28x faster                                                  |
| async_tree_io              | 761 ms                                                                 | 605 ms: 1.26x faster                                                  |
| async_tree_none            | 351 ms                                                                 | 284 ms: 1.24x faster                                                  |
| async_tree_io_tg           | 735 ms                                                                 | 594 ms: 1.24x faster                                                  |
| async_tree_memoization     | 428 ms                                                                 | 351 ms: 1.22x faster                                                  |
| async_tree_cpu_io_mixed_tg | 572 ms                                                                 | 489 ms: 1.17x faster                                                  |
| async_tree_cpu_io_mixed    | 596 ms                                                                 | 524 ms: 1.14x faster                                                  |
| async_generators           | 447 ms                                                                 | 430 ms: 1.04x faster                                                  |
| asyncio_websockets         | 520 ms                                                                 | 518 ms: 1.00x faster                                                  |
| Geometric mean             | (ref)                                                                  | 1.17x faster                                                          |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241219-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-3876bc7 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 115 ms                                                                 | 82.7 ms: 1.39x faster                                                 |
| pidigits       | 184 ms                                                                 | 181 ms: 1.01x faster                                                  |
| nbody          | 133 ms                                                                 | 135 ms: 1.02x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.11x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241219-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-3876bc7 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 169 ms                                                                 | 151 ms: 1.12x faster                                                  |
| regex_v8       | 24.8 ms                                                                | 23.2 ms: 1.07x faster                                                 |
| regex_dna      | 187 ms                                                                 | 181 ms: 1.03x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.05x faster                                                          |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241219-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-3876bc7 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_pure_python   | 494 us                                                                 | 372 us: 1.33x faster                                                  |
| unpickle_pure_python | 329 us                                                                 | 252 us: 1.30x faster                                                  |
| json_dumps           | 14.4 ms                                                                | 13.0 ms: 1.11x faster                                                 |
| xml_etree_process    | 73.5 ms                                                                | 69.2 ms: 1.06x faster                                                 |
| tomli_loads          | 2.56 sec                                                               | 2.50 sec: 1.03x faster                                                |
| xml_etree_iterparse  | 90.4 ms                                                                | 88.8 ms: 1.02x faster                                                 |
| json_loads           | 28.5 us                                                                | 28.3 us: 1.01x faster                                                 |
| xml_etree_generate   | 97.5 ms                                                                | 97.0 ms: 1.01x faster                                                 |
| xml_etree_parse      | 129 ms                                                                 | 131 ms: 1.01x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.09x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241219-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-3876bc7 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 17.2 ms                                                                | 17.1 ms: 1.01x faster                                                 |
| python_startup_no_site | 10.3 ms                                                                | 10.2 ms: 1.01x faster                                                 |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241219-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-3876bc7 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 49.5 ms                                                                | 43.0 ms: 1.15x faster                                                 |
| mako            | 17.1 ms                                                                | 15.6 ms: 1.10x faster                                                 |
| genshi_text     | 30.5 ms                                                                | 28.5 ms: 1.07x faster                                                 |
| genshi_xml      | 63.3 ms                                                                | 60.8 ms: 1.04x faster                                                 |
| Geometric mean  | (ref)                                                                  | 1.09x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241219-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-3876bc7 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| go                         | 243 ms                                                                 | 144 ms: 1.69x faster                                                  |
| logging_silent             | 183 ns                                                                 | 115 ns: 1.59x faster                                                  |
| raytrace                   | 494 ms                                                                 | 322 ms: 1.54x faster                                                  |
| deltablue                  | 7.41 ms                                                                | 4.84 ms: 1.53x faster                                                 |
| sqlglot_parse              | 2.38 ms                                                                | 1.61 ms: 1.48x faster                                                 |
| sqlglot_transpile          | 2.76 ms                                                                | 1.94 ms: 1.42x faster                                                 |
| float                      | 115 ms                                                                 | 82.7 ms: 1.39x faster                                                 |
| pickle_pure_python         | 494 us                                                                 | 372 us: 1.33x faster                                                  |
| chaos                      | 96.3 ms                                                                | 72.4 ms: 1.33x faster                                                 |
| scimark_sor                | 215 ms                                                                 | 162 ms: 1.33x faster                                                  |
| comprehensions             | 27.6 us                                                                | 21.0 us: 1.31x faster                                                 |
| async_tree_none_tg         | 314 ms                                                                 | 241 ms: 1.30x faster                                                  |
| unpickle_pure_python       | 329 us                                                                 | 252 us: 1.30x faster                                                  |
| pyflate                    | 646 ms                                                                 | 504 ms: 1.28x faster                                                  |
| async_tree_memoization_tg  | 399 ms                                                                 | 312 ms: 1.28x faster                                                  |
| hexiom                     | 9.67 ms                                                                | 7.61 ms: 1.27x faster                                                 |
| html5lib                   | 93.4 ms                                                                | 74.1 ms: 1.26x faster                                                 |
| async_tree_io              | 761 ms                                                                 | 605 ms: 1.26x faster                                                  |
| logging_simple             | 9.02 us                                                                | 7.26 us: 1.24x faster                                                 |
| scimark_monte_carlo        | 108 ms                                                                 | 86.9 ms: 1.24x faster                                                 |
| async_tree_none            | 351 ms                                                                 | 284 ms: 1.24x faster                                                  |
| async_tree_io_tg           | 735 ms                                                                 | 594 ms: 1.24x faster                                                  |
| logging_format             | 10.1 us                                                                | 8.26 us: 1.22x faster                                                 |
| async_tree_memoization     | 428 ms                                                                 | 351 ms: 1.22x faster                                                  |
| generators                 | 38.2 ms                                                                | 31.3 ms: 1.22x faster                                                 |
| richards                   | 67.8 ms                                                                | 56.5 ms: 1.20x faster                                                 |
| async_tree_cpu_io_mixed_tg | 572 ms                                                                 | 489 ms: 1.17x faster                                                  |
| richards_super             | 75.9 ms                                                                | 65.8 ms: 1.15x faster                                                 |
| django_template            | 49.5 ms                                                                | 43.0 ms: 1.15x faster                                                 |
| pprint_pformat             | 2.01 sec                                                               | 1.76 sec: 1.15x faster                                                |
| subparsers                 | 28.8 ms                                                                | 25.3 ms: 1.14x faster                                                 |
| async_tree_cpu_io_mixed    | 596 ms                                                                 | 524 ms: 1.14x faster                                                  |
| pprint_safe_repr           | 965 ms                                                                 | 849 ms: 1.14x faster                                                  |
| sqlalchemy_imperative      | 27.7 ms                                                                | 24.5 ms: 1.13x faster                                                 |
| pycparser                  | 1.37 sec                                                               | 1.21 sec: 1.13x faster                                                |
| scimark_lu                 | 158 ms                                                                 | 141 ms: 1.13x faster                                                  |
| regex_compile              | 169 ms                                                                 | 151 ms: 1.12x faster                                                  |
| sqlalchemy_declarative     | 198 ms                                                                 | 177 ms: 1.12x faster                                                  |
| 2to3                       | 361 ms                                                                 | 324 ms: 1.11x faster                                                  |
| json_dumps                 | 14.4 ms                                                                | 13.0 ms: 1.11x faster                                                 |
| mako                       | 17.1 ms                                                                | 15.6 ms: 1.10x faster                                                 |
| sqlglot_normalize          | 133 ms                                                                 | 121 ms: 1.09x faster                                                  |
| dulwich_log                | 90.4 ms                                                                | 82.8 ms: 1.09x faster                                                 |
| mdp                        | 2.82 sec                                                               | 2.61 sec: 1.08x faster                                                |
| thrift                     | 983 us                                                                 | 911 us: 1.08x faster                                                  |
| sqlglot_optimize           | 65.8 ms                                                                | 61.2 ms: 1.07x faster                                                 |
| deepcopy_reduce            | 3.47 us                                                                | 3.23 us: 1.07x faster                                                 |
| regex_v8                   | 24.8 ms                                                                | 23.2 ms: 1.07x faster                                                 |
| genshi_text                | 30.5 ms                                                                | 28.5 ms: 1.07x faster                                                 |
| xml_etree_process          | 73.5 ms                                                                | 69.2 ms: 1.06x faster                                                 |
| many_optionals             | 1.24 ms                                                                | 1.18 ms: 1.06x faster                                                 |
| docutils                   | 3.02 sec                                                               | 2.86 sec: 1.06x faster                                                |
| pylint                     | 364 ms                                                                 | 347 ms: 1.05x faster                                                  |
| bpe_tokeniser              | 5.03 sec                                                               | 4.81 sec: 1.05x faster                                                |
| crypto_pyaes               | 91.7 ms                                                                | 88.0 ms: 1.04x faster                                                 |
| sympy_str                  | 480 ms                                                                 | 461 ms: 1.04x faster                                                  |
| genshi_xml                 | 63.3 ms                                                                | 60.8 ms: 1.04x faster                                                 |
| async_generators           | 447 ms                                                                 | 430 ms: 1.04x faster                                                  |
| pathlib                    | 19.6 ms                                                                | 18.9 ms: 1.04x faster                                                 |
| spectral_norm              | 115 ms                                                                 | 110 ms: 1.04x faster                                                  |
| coverage                   | 102 ms                                                                 | 98.6 ms: 1.04x faster                                                 |
| sphinx                     | 1.16 sec                                                               | 1.12 sec: 1.04x faster                                                |
| regex_dna                  | 187 ms                                                                 | 181 ms: 1.03x faster                                                  |
| sympy_integrate            | 29.7 ms                                                                | 28.9 ms: 1.03x faster                                                 |
| sympy_expand               | 958 ms                                                                 | 931 ms: 1.03x faster                                                  |
| json                       | 5.14 ms                                                                | 5.00 ms: 1.03x faster                                                 |
| deepcopy_memo              | 40.4 us                                                                | 39.3 us: 1.03x faster                                                 |
| deepcopy                   | 323 us                                                                 | 314 us: 1.03x faster                                                  |
| sympy_sum                  | 351 ms                                                                 | 342 ms: 1.03x faster                                                  |
| tomli_loads                | 2.56 sec                                                               | 2.50 sec: 1.03x faster                                                |
| sqlite_synth               | 2.12 us                                                                | 2.07 us: 1.02x faster                                                 |
| typing_runtime_protocols   | 204 us                                                                 | 200 us: 1.02x faster                                                  |
| bench_mp_pool              | 108 ms                                                                 | 106 ms: 1.02x faster                                                  |
| xml_etree_iterparse        | 90.4 ms                                                                | 88.8 ms: 1.02x faster                                                 |
| bench_thread_pool          | 3.38 ms                                                                | 3.33 ms: 1.02x faster                                                 |
| shortest_path              | 550 ms                                                                 | 542 ms: 1.02x faster                                                  |
| connected_components       | 501 ms                                                                 | 494 ms: 1.02x faster                                                  |
| pidigits                   | 184 ms                                                                 | 181 ms: 1.01x faster                                                  |
| nqueens                    | 98.6 ms                                                                | 97.4 ms: 1.01x faster                                                 |
| fannkuch                   | 493 ms                                                                 | 488 ms: 1.01x faster                                                  |
| k_core                     | 2.35 sec                                                               | 2.33 sec: 1.01x faster                                                |
| python_startup             | 17.2 ms                                                                | 17.1 ms: 1.01x faster                                                 |
| python_startup_no_site     | 10.3 ms                                                                | 10.2 ms: 1.01x faster                                                 |
| json_loads                 | 28.5 us                                                                | 28.3 us: 1.01x faster                                                 |
| xml_etree_generate         | 97.5 ms                                                                | 97.0 ms: 1.01x faster                                                 |
| asyncio_websockets         | 520 ms                                                                 | 518 ms: 1.00x faster                                                  |
| scimark_sparse_mat_mult    | 5.79 ms                                                                | 5.78 ms: 1.00x faster                                                 |
| scimark_fft                | 385 ms                                                                 | 386 ms: 1.00x slower                                                  |
| create_gc_cycles           | 1.80 ms                                                                | 1.82 ms: 1.01x slower                                                 |
| xml_etree_parse            | 129 ms                                                                 | 131 ms: 1.01x slower                                                  |
| meteor_contest             | 129 ms                                                                 | 131 ms: 1.02x slower                                                  |
| nbody                      | 133 ms                                                                 | 135 ms: 1.02x slower                                                  |
| gc_traversal               | 3.20 ms                                                                | 3.50 ms: 1.10x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.12x faster                                                          |

Benchmark hidden because not significant (3): coroutines, telco, regex_effbot

- Geometric mean (including insignificant results): 1.116x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.02x