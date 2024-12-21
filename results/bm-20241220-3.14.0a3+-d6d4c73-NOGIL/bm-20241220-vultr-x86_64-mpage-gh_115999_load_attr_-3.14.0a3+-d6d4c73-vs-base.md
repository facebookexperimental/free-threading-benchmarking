# Results vs. base

- fork: mpage
- ref: gh_115999_load_attr_
- machine: linux-x86_64
- commit hash: d6d4c73
- commit date: 2024-12-20
- overall geometric mean: 1.120x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 361 ms                                                                 | 322 ms: 1.12x faster                                                  |
| docutils       | 3.02 sec                                                               | 2.84 sec: 1.06x faster                                                |
| html5lib       | 93.4 ms                                                                | 71.4 ms: 1.31x faster                                                 |
| sphinx         | 1.16 sec                                                               | 1.12 sec: 1.04x faster                                                |
| Geometric mean | (ref)                                                                  | 1.13x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none_tg         | 314 ms                                                                 | 241 ms: 1.30x faster                                                  |
| async_tree_memoization_tg  | 399 ms                                                                 | 315 ms: 1.27x faster                                                  |
| async_tree_io              | 761 ms                                                                 | 604 ms: 1.26x faster                                                  |
| async_tree_io_tg           | 735 ms                                                                 | 586 ms: 1.25x faster                                                  |
| async_tree_none            | 351 ms                                                                 | 284 ms: 1.24x faster                                                  |
| async_tree_memoization     | 428 ms                                                                 | 350 ms: 1.22x faster                                                  |
| async_tree_cpu_io_mixed_tg | 572 ms                                                                 | 484 ms: 1.18x faster                                                  |
| async_tree_cpu_io_mixed    | 596 ms                                                                 | 518 ms: 1.15x faster                                                  |
| async_generators           | 447 ms                                                                 | 420 ms: 1.07x faster                                                  |
| coroutines                 | 24.9 ms                                                                | 24.0 ms: 1.04x faster                                                 |
| asyncio_websockets         | 520 ms                                                                 | 518 ms: 1.00x faster                                                  |
| Geometric mean             | (ref)                                                                  | 1.18x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 115 ms                                                                 | 81.9 ms: 1.40x faster                                                 |
| pidigits       | 184 ms                                                                 | 184 ms: 1.00x faster                                                  |
| nbody          | 133 ms                                                                 | 136 ms: 1.03x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.11x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 169 ms                                                                 | 151 ms: 1.12x faster                                                  |
| regex_dna      | 187 ms                                                                 | 177 ms: 1.05x faster                                                  |
| regex_v8       | 24.8 ms                                                                | 24.3 ms: 1.02x faster                                                 |
| regex_effbot   | 2.76 ms                                                                | 2.92 ms: 1.06x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_pure_python   | 494 us                                                                 | 370 us: 1.34x faster                                                  |
| unpickle_pure_python | 329 us                                                                 | 247 us: 1.33x faster                                                  |
| json_dumps           | 14.4 ms                                                                | 13.1 ms: 1.10x faster                                                 |
| xml_etree_process    | 73.5 ms                                                                | 68.6 ms: 1.07x faster                                                 |
| tomli_loads          | 2.56 sec                                                               | 2.49 sec: 1.03x faster                                                |
| xml_etree_iterparse  | 90.4 ms                                                                | 88.5 ms: 1.02x faster                                                 |
| json_loads           | 28.5 us                                                                | 27.9 us: 1.02x faster                                                 |
| xml_etree_generate   | 97.5 ms                                                                | 96.8 ms: 1.01x faster                                                 |
| xml_etree_parse      | 129 ms                                                                 | 130 ms: 1.01x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.09x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 17.2 ms                                                                | 17.1 ms: 1.01x faster                                                 |
| python_startup_no_site | 10.3 ms                                                                | 10.2 ms: 1.01x faster                                                 |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 49.5 ms                                                                | 42.9 ms: 1.15x faster                                                 |
| mako            | 17.1 ms                                                                | 15.8 ms: 1.08x faster                                                 |
| genshi_text     | 30.5 ms                                                                | 28.5 ms: 1.07x faster                                                 |
| genshi_xml      | 63.3 ms                                                                | 60.1 ms: 1.05x faster                                                 |
| Geometric mean  | (ref)                                                                  | 1.09x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| go                         | 243 ms                                                                 | 143 ms: 1.70x faster                                                  |
| logging_silent             | 183 ns                                                                 | 116 ns: 1.57x faster                                                  |
| deltablue                  | 7.41 ms                                                                | 4.84 ms: 1.53x faster                                                 |
| raytrace                   | 494 ms                                                                 | 323 ms: 1.53x faster                                                  |
| sqlglot_parse              | 2.38 ms                                                                | 1.60 ms: 1.49x faster                                                 |
| sqlglot_transpile          | 2.76 ms                                                                | 1.93 ms: 1.43x faster                                                 |
| float                      | 115 ms                                                                 | 81.9 ms: 1.40x faster                                                 |
| chaos                      | 96.3 ms                                                                | 71.1 ms: 1.35x faster                                                 |
| pickle_pure_python         | 494 us                                                                 | 370 us: 1.34x faster                                                  |
| scimark_sor                | 215 ms                                                                 | 162 ms: 1.33x faster                                                  |
| unpickle_pure_python       | 329 us                                                                 | 247 us: 1.33x faster                                                  |
| comprehensions             | 27.6 us                                                                | 21.0 us: 1.31x faster                                                 |
| html5lib                   | 93.4 ms                                                                | 71.4 ms: 1.31x faster                                                 |
| async_tree_none_tg         | 314 ms                                                                 | 241 ms: 1.30x faster                                                  |
| pyflate                    | 646 ms                                                                 | 497 ms: 1.30x faster                                                  |
| scimark_monte_carlo        | 108 ms                                                                 | 84.5 ms: 1.27x faster                                                 |
| hexiom                     | 9.67 ms                                                                | 7.62 ms: 1.27x faster                                                 |
| async_tree_memoization_tg  | 399 ms                                                                 | 315 ms: 1.27x faster                                                  |
| async_tree_io              | 761 ms                                                                 | 604 ms: 1.26x faster                                                  |
| async_tree_io_tg           | 735 ms                                                                 | 586 ms: 1.25x faster                                                  |
| async_tree_none            | 351 ms                                                                 | 284 ms: 1.24x faster                                                  |
| async_tree_memoization     | 428 ms                                                                 | 350 ms: 1.22x faster                                                  |
| generators                 | 38.2 ms                                                                | 31.3 ms: 1.22x faster                                                 |
| logging_simple             | 9.02 us                                                                | 7.42 us: 1.22x faster                                                 |
| logging_format             | 10.1 us                                                                | 8.39 us: 1.20x faster                                                 |
| richards                   | 67.8 ms                                                                | 56.9 ms: 1.19x faster                                                 |
| async_tree_cpu_io_mixed_tg | 572 ms                                                                 | 484 ms: 1.18x faster                                                  |
| pprint_pformat             | 2.01 sec                                                               | 1.74 sec: 1.15x faster                                                |
| django_template            | 49.5 ms                                                                | 42.9 ms: 1.15x faster                                                 |
| richards_super             | 75.9 ms                                                                | 65.9 ms: 1.15x faster                                                 |
| async_tree_cpu_io_mixed    | 596 ms                                                                 | 518 ms: 1.15x faster                                                  |
| pprint_safe_repr           | 965 ms                                                                 | 841 ms: 1.15x faster                                                  |
| sqlalchemy_imperative      | 27.7 ms                                                                | 24.4 ms: 1.14x faster                                                 |
| pycparser                  | 1.37 sec                                                               | 1.22 sec: 1.13x faster                                                |
| subparsers                 | 28.8 ms                                                                | 25.7 ms: 1.12x faster                                                 |
| sqlalchemy_declarative     | 198 ms                                                                 | 176 ms: 1.12x faster                                                  |
| 2to3                       | 361 ms                                                                 | 322 ms: 1.12x faster                                                  |
| regex_compile              | 169 ms                                                                 | 151 ms: 1.12x faster                                                  |
| scimark_lu                 | 158 ms                                                                 | 142 ms: 1.12x faster                                                  |
| json_dumps                 | 14.4 ms                                                                | 13.1 ms: 1.10x faster                                                 |
| sqlglot_normalize          | 133 ms                                                                 | 121 ms: 1.10x faster                                                  |
| dulwich_log                | 90.4 ms                                                                | 82.5 ms: 1.10x faster                                                 |
| mdp                        | 2.82 sec                                                               | 2.60 sec: 1.08x faster                                                |
| mako                       | 17.1 ms                                                                | 15.8 ms: 1.08x faster                                                 |
| thrift                     | 983 us                                                                 | 915 us: 1.07x faster                                                  |
| deepcopy_reduce            | 3.47 us                                                                | 3.23 us: 1.07x faster                                                 |
| sqlglot_optimize           | 65.8 ms                                                                | 61.4 ms: 1.07x faster                                                 |
| xml_etree_process          | 73.5 ms                                                                | 68.6 ms: 1.07x faster                                                 |
| genshi_text                | 30.5 ms                                                                | 28.5 ms: 1.07x faster                                                 |
| async_generators           | 447 ms                                                                 | 420 ms: 1.07x faster                                                  |
| docutils                   | 3.02 sec                                                               | 2.84 sec: 1.06x faster                                                |
| crypto_pyaes               | 91.7 ms                                                                | 86.8 ms: 1.06x faster                                                 |
| many_optionals             | 1.24 ms                                                                | 1.18 ms: 1.06x faster                                                 |
| regex_dna                  | 187 ms                                                                 | 177 ms: 1.05x faster                                                  |
| genshi_xml                 | 63.3 ms                                                                | 60.1 ms: 1.05x faster                                                 |
| json                       | 5.14 ms                                                                | 4.89 ms: 1.05x faster                                                 |
| pylint                     | 364 ms                                                                 | 346 ms: 1.05x faster                                                  |
| bpe_tokeniser              | 5.03 sec                                                               | 4.79 sec: 1.05x faster                                                |
| sympy_str                  | 480 ms                                                                 | 459 ms: 1.05x faster                                                  |
| deepcopy_memo              | 40.4 us                                                                | 38.7 us: 1.04x faster                                                 |
| sphinx                     | 1.16 sec                                                               | 1.12 sec: 1.04x faster                                                |
| coroutines                 | 24.9 ms                                                                | 24.0 ms: 1.04x faster                                                 |
| sympy_expand               | 958 ms                                                                 | 929 ms: 1.03x faster                                                  |
| sympy_integrate            | 29.7 ms                                                                | 28.9 ms: 1.03x faster                                                 |
| deepcopy                   | 323 us                                                                 | 314 us: 1.03x faster                                                  |
| coverage                   | 102 ms                                                                 | 99.3 ms: 1.03x faster                                                 |
| tomli_loads                | 2.56 sec                                                               | 2.49 sec: 1.03x faster                                                |
| typing_runtime_protocols   | 204 us                                                                 | 199 us: 1.03x faster                                                  |
| sympy_sum                  | 351 ms                                                                 | 343 ms: 1.02x faster                                                  |
| regex_v8                   | 24.8 ms                                                                | 24.3 ms: 1.02x faster                                                 |
| pathlib                    | 19.6 ms                                                                | 19.1 ms: 1.02x faster                                                 |
| sqlite_synth               | 2.12 us                                                                | 2.07 us: 1.02x faster                                                 |
| bench_mp_pool              | 108 ms                                                                 | 105 ms: 1.02x faster                                                  |
| xml_etree_iterparse        | 90.4 ms                                                                | 88.5 ms: 1.02x faster                                                 |
| json_loads                 | 28.5 us                                                                | 27.9 us: 1.02x faster                                                 |
| scimark_sparse_mat_mult    | 5.79 ms                                                                | 5.69 ms: 1.02x faster                                                 |
| connected_components       | 501 ms                                                                 | 494 ms: 1.02x faster                                                  |
| k_core                     | 2.35 sec                                                               | 2.32 sec: 1.01x faster                                                |
| bench_thread_pool          | 3.38 ms                                                                | 3.34 ms: 1.01x faster                                                 |
| scimark_fft                | 385 ms                                                                 | 380 ms: 1.01x faster                                                  |
| telco                      | 8.58 ms                                                                | 8.47 ms: 1.01x faster                                                 |
| shortest_path              | 550 ms                                                                 | 544 ms: 1.01x faster                                                  |
| nqueens                    | 98.6 ms                                                                | 97.5 ms: 1.01x faster                                                 |
| python_startup             | 17.2 ms                                                                | 17.1 ms: 1.01x faster                                                 |
| python_startup_no_site     | 10.3 ms                                                                | 10.2 ms: 1.01x faster                                                 |
| xml_etree_generate         | 97.5 ms                                                                | 96.8 ms: 1.01x faster                                                 |
| fannkuch                   | 493 ms                                                                 | 490 ms: 1.01x faster                                                  |
| create_gc_cycles           | 1.80 ms                                                                | 1.79 ms: 1.01x faster                                                 |
| asyncio_websockets         | 520 ms                                                                 | 518 ms: 1.00x faster                                                  |
| pidigits                   | 184 ms                                                                 | 184 ms: 1.00x faster                                                  |
| xml_etree_parse            | 129 ms                                                                 | 130 ms: 1.01x slower                                                  |
| meteor_contest             | 129 ms                                                                 | 130 ms: 1.01x slower                                                  |
| nbody                      | 133 ms                                                                 | 136 ms: 1.03x slower                                                  |
| gc_traversal               | 3.20 ms                                                                | 3.29 ms: 1.03x slower                                                 |
| regex_effbot               | 2.76 ms                                                                | 2.92 ms: 1.06x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.12x faster                                                          |

Benchmark hidden because not significant (1): spectral_norm

- Geometric mean (including insignificant results): 1.120x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.02x