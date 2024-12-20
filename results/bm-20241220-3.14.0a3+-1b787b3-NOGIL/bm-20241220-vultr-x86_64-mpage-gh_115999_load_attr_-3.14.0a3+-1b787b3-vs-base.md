# Results vs. base

- fork: mpage
- ref: gh_115999_load_attr_
- machine: linux-x86_64
- commit hash: 1b787b3
- commit date: 2024-12-20
- overall geometric mean: 1.122x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-1b787b3 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 361 ms                                                                 | 322 ms: 1.12x faster                                                  |
| docutils       | 3.02 sec                                                               | 2.85 sec: 1.06x faster                                                |
| html5lib       | 93.4 ms                                                                | 73.7 ms: 1.27x faster                                                 |
| sphinx         | 1.16 sec                                                               | 1.11 sec: 1.04x faster                                                |
| Geometric mean | (ref)                                                                  | 1.12x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-1b787b3 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none_tg         | 314 ms                                                                 | 239 ms: 1.32x faster                                                  |
| async_tree_memoization_tg  | 399 ms                                                                 | 311 ms: 1.28x faster                                                  |
| async_tree_io              | 761 ms                                                                 | 606 ms: 1.26x faster                                                  |
| async_tree_io_tg           | 735 ms                                                                 | 591 ms: 1.24x faster                                                  |
| async_tree_none            | 351 ms                                                                 | 284 ms: 1.24x faster                                                  |
| async_tree_memoization     | 428 ms                                                                 | 349 ms: 1.22x faster                                                  |
| async_tree_cpu_io_mixed_tg | 572 ms                                                                 | 483 ms: 1.18x faster                                                  |
| async_tree_cpu_io_mixed    | 596 ms                                                                 | 520 ms: 1.15x faster                                                  |
| async_generators           | 447 ms                                                                 | 414 ms: 1.08x faster                                                  |
| coroutines                 | 24.9 ms                                                                | 24.4 ms: 1.02x faster                                                 |
| Geometric mean             | (ref)                                                                  | 1.18x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-1b787b3 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 115 ms                                                                 | 81.3 ms: 1.41x faster                                                 |
| nbody          | 133 ms                                                                 | 130 ms: 1.02x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.13x faster                                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-1b787b3 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 169 ms                                                                 | 150 ms: 1.12x faster                                                  |
| regex_dna      | 187 ms                                                                 | 172 ms: 1.09x faster                                                  |
| regex_v8       | 24.8 ms                                                                | 23.5 ms: 1.06x faster                                                 |
| regex_effbot   | 2.76 ms                                                                | 2.68 ms: 1.03x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.07x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-1b787b3 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_pure_python   | 494 us                                                                 | 370 us: 1.34x faster                                                  |
| unpickle_pure_python | 329 us                                                                 | 254 us: 1.29x faster                                                  |
| json_dumps           | 14.4 ms                                                                | 13.1 ms: 1.10x faster                                                 |
| xml_etree_process    | 73.5 ms                                                                | 68.2 ms: 1.08x faster                                                 |
| xml_etree_iterparse  | 90.4 ms                                                                | 88.3 ms: 1.02x faster                                                 |
| tomli_loads          | 2.56 sec                                                               | 2.52 sec: 1.02x faster                                                |
| xml_etree_generate   | 97.5 ms                                                                | 96.0 ms: 1.02x faster                                                 |
| json_loads           | 28.5 us                                                                | 28.1 us: 1.01x faster                                                 |
| Geometric mean       | (ref)                                                                  | 1.09x faster                                                          |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-1b787b3 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 17.2 ms                                                                | 17.1 ms: 1.01x faster                                                 |
| python_startup_no_site | 10.3 ms                                                                | 10.2 ms: 1.01x faster                                                 |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-1b787b3 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 49.5 ms                                                                | 42.4 ms: 1.17x faster                                                 |
| mako            | 17.1 ms                                                                | 15.6 ms: 1.09x faster                                                 |
| genshi_text     | 30.5 ms                                                                | 28.3 ms: 1.08x faster                                                 |
| genshi_xml      | 63.3 ms                                                                | 60.0 ms: 1.05x faster                                                 |
| Geometric mean  | (ref)                                                                  | 1.10x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-1b787b3 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| go                         | 243 ms                                                                 | 143 ms: 1.70x faster                                                  |
| logging_silent             | 183 ns                                                                 | 113 ns: 1.62x faster                                                  |
| deltablue                  | 7.41 ms                                                                | 4.82 ms: 1.54x faster                                                 |
| raytrace                   | 494 ms                                                                 | 322 ms: 1.54x faster                                                  |
| sqlglot_parse              | 2.38 ms                                                                | 1.60 ms: 1.49x faster                                                 |
| sqlglot_transpile          | 2.76 ms                                                                | 1.93 ms: 1.43x faster                                                 |
| float                      | 115 ms                                                                 | 81.3 ms: 1.41x faster                                                 |
| chaos                      | 96.3 ms                                                                | 71.0 ms: 1.35x faster                                                 |
| pickle_pure_python         | 494 us                                                                 | 370 us: 1.34x faster                                                  |
| scimark_sor                | 215 ms                                                                 | 161 ms: 1.33x faster                                                  |
| async_tree_none_tg         | 314 ms                                                                 | 239 ms: 1.32x faster                                                  |
| unpickle_pure_python       | 329 us                                                                 | 254 us: 1.29x faster                                                  |
| comprehensions             | 27.6 us                                                                | 21.4 us: 1.29x faster                                                 |
| async_tree_memoization_tg  | 399 ms                                                                 | 311 ms: 1.28x faster                                                  |
| scimark_monte_carlo        | 108 ms                                                                 | 84.6 ms: 1.27x faster                                                 |
| html5lib                   | 93.4 ms                                                                | 73.7 ms: 1.27x faster                                                 |
| hexiom                     | 9.67 ms                                                                | 7.66 ms: 1.26x faster                                                 |
| async_tree_io              | 761 ms                                                                 | 606 ms: 1.26x faster                                                  |
| logging_simple             | 9.02 us                                                                | 7.21 us: 1.25x faster                                                 |
| pyflate                    | 646 ms                                                                 | 516 ms: 1.25x faster                                                  |
| generators                 | 38.2 ms                                                                | 30.5 ms: 1.25x faster                                                 |
| async_tree_io_tg           | 735 ms                                                                 | 591 ms: 1.24x faster                                                  |
| richards                   | 67.8 ms                                                                | 54.8 ms: 1.24x faster                                                 |
| async_tree_none            | 351 ms                                                                 | 284 ms: 1.24x faster                                                  |
| async_tree_memoization     | 428 ms                                                                 | 349 ms: 1.22x faster                                                  |
| logging_format             | 10.1 us                                                                | 8.27 us: 1.22x faster                                                 |
| richards_super             | 75.9 ms                                                                | 63.8 ms: 1.19x faster                                                 |
| async_tree_cpu_io_mixed_tg | 572 ms                                                                 | 483 ms: 1.18x faster                                                  |
| django_template            | 49.5 ms                                                                | 42.4 ms: 1.17x faster                                                 |
| pprint_pformat             | 2.01 sec                                                               | 1.75 sec: 1.15x faster                                                |
| async_tree_cpu_io_mixed    | 596 ms                                                                 | 520 ms: 1.15x faster                                                  |
| pprint_safe_repr           | 965 ms                                                                 | 850 ms: 1.14x faster                                                  |
| subparsers                 | 28.8 ms                                                                | 25.4 ms: 1.14x faster                                                 |
| sqlalchemy_imperative      | 27.7 ms                                                                | 24.5 ms: 1.13x faster                                                 |
| sqlalchemy_declarative     | 198 ms                                                                 | 176 ms: 1.13x faster                                                  |
| regex_compile              | 169 ms                                                                 | 150 ms: 1.12x faster                                                  |
| pycparser                  | 1.37 sec                                                               | 1.22 sec: 1.12x faster                                                |
| 2to3                       | 361 ms                                                                 | 322 ms: 1.12x faster                                                  |
| scimark_lu                 | 158 ms                                                                 | 142 ms: 1.11x faster                                                  |
| json_dumps                 | 14.4 ms                                                                | 13.1 ms: 1.10x faster                                                 |
| dulwich_log                | 90.4 ms                                                                | 82.3 ms: 1.10x faster                                                 |
| sqlglot_normalize          | 133 ms                                                                 | 121 ms: 1.10x faster                                                  |
| mako                       | 17.1 ms                                                                | 15.6 ms: 1.09x faster                                                 |
| thrift                     | 983 us                                                                 | 905 us: 1.09x faster                                                  |
| regex_dna                  | 187 ms                                                                 | 172 ms: 1.09x faster                                                  |
| async_generators           | 447 ms                                                                 | 414 ms: 1.08x faster                                                  |
| sqlglot_optimize           | 65.8 ms                                                                | 60.9 ms: 1.08x faster                                                 |
| xml_etree_process          | 73.5 ms                                                                | 68.2 ms: 1.08x faster                                                 |
| genshi_text                | 30.5 ms                                                                | 28.3 ms: 1.08x faster                                                 |
| deepcopy_reduce            | 3.47 us                                                                | 3.23 us: 1.07x faster                                                 |
| docutils                   | 3.02 sec                                                               | 2.85 sec: 1.06x faster                                                |
| regex_v8                   | 24.8 ms                                                                | 23.5 ms: 1.06x faster                                                 |
| many_optionals             | 1.24 ms                                                                | 1.18 ms: 1.06x faster                                                 |
| bpe_tokeniser              | 5.03 sec                                                               | 4.76 sec: 1.06x faster                                                |
| pylint                     | 364 ms                                                                 | 344 ms: 1.06x faster                                                  |
| genshi_xml                 | 63.3 ms                                                                | 60.0 ms: 1.05x faster                                                 |
| deepcopy_memo              | 40.4 us                                                                | 38.4 us: 1.05x faster                                                 |
| sympy_str                  | 480 ms                                                                 | 458 ms: 1.05x faster                                                  |
| crypto_pyaes               | 91.7 ms                                                                | 87.5 ms: 1.05x faster                                                 |
| pathlib                    | 19.6 ms                                                                | 18.8 ms: 1.04x faster                                                 |
| sphinx                     | 1.16 sec                                                               | 1.11 sec: 1.04x faster                                                |
| deepcopy                   | 323 us                                                                 | 311 us: 1.04x faster                                                  |
| json                       | 5.14 ms                                                                | 4.96 ms: 1.04x faster                                                 |
| sympy_integrate            | 29.7 ms                                                                | 28.7 ms: 1.03x faster                                                 |
| sympy_expand               | 958 ms                                                                 | 926 ms: 1.03x faster                                                  |
| sympy_sum                  | 351 ms                                                                 | 341 ms: 1.03x faster                                                  |
| regex_effbot               | 2.76 ms                                                                | 2.68 ms: 1.03x faster                                                 |
| typing_runtime_protocols   | 204 us                                                                 | 199 us: 1.03x faster                                                  |
| connected_components       | 501 ms                                                                 | 489 ms: 1.02x faster                                                  |
| sqlite_synth               | 2.12 us                                                                | 2.07 us: 1.02x faster                                                 |
| xml_etree_iterparse        | 90.4 ms                                                                | 88.3 ms: 1.02x faster                                                 |
| bench_mp_pool              | 108 ms                                                                 | 105 ms: 1.02x faster                                                  |
| coverage                   | 102 ms                                                                 | 100.0 ms: 1.02x faster                                                |
| scimark_sparse_mat_mult    | 5.79 ms                                                                | 5.67 ms: 1.02x faster                                                 |
| coroutines                 | 24.9 ms                                                                | 24.4 ms: 1.02x faster                                                 |
| spectral_norm              | 115 ms                                                                 | 113 ms: 1.02x faster                                                  |
| tomli_loads                | 2.56 sec                                                               | 2.52 sec: 1.02x faster                                                |
| shortest_path              | 550 ms                                                                 | 541 ms: 1.02x faster                                                  |
| bench_thread_pool          | 3.38 ms                                                                | 3.33 ms: 1.02x faster                                                 |
| nbody                      | 133 ms                                                                 | 130 ms: 1.02x faster                                                  |
| nqueens                    | 98.6 ms                                                                | 97.1 ms: 1.02x faster                                                 |
| xml_etree_generate         | 97.5 ms                                                                | 96.0 ms: 1.02x faster                                                 |
| mdp                        | 2.82 sec                                                               | 2.78 sec: 1.01x faster                                                |
| json_loads                 | 28.5 us                                                                | 28.1 us: 1.01x faster                                                 |
| k_core                     | 2.35 sec                                                               | 2.32 sec: 1.01x faster                                                |
| python_startup             | 17.2 ms                                                                | 17.1 ms: 1.01x faster                                                 |
| python_startup_no_site     | 10.3 ms                                                                | 10.2 ms: 1.01x faster                                                 |
| telco                      | 8.58 ms                                                                | 8.50 ms: 1.01x faster                                                 |
| fannkuch                   | 493 ms                                                                 | 489 ms: 1.01x faster                                                  |
| scimark_fft                | 385 ms                                                                 | 383 ms: 1.01x faster                                                  |
| create_gc_cycles           | 1.80 ms                                                                | 1.82 ms: 1.01x slower                                                 |
| gc_traversal               | 3.20 ms                                                                | 3.49 ms: 1.09x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.12x faster                                                          |

Benchmark hidden because not significant (4): xml_etree_parse, pidigits, asyncio_websockets, meteor_contest

- Geometric mean (including insignificant results): 1.122x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.02x