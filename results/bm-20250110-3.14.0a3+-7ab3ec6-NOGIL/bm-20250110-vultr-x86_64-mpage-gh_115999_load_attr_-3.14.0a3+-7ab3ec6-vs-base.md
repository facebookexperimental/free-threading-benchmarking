# Results vs. base

- fork: mpage
- ref: gh_115999_load_attr_
- machine: linux-x86_64
- commit hash: 7ab3ec6
- commit date: 2025-01-10
- overall geometric mean: 1.117x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250110-vultr-x86_64-python-1b39b502d33c68f52fd7-3.14.0a3+-1b39b50 | bm-20250110-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-7ab3ec6 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 344 ms                                                                 | 310 ms: 1.11x faster                                                  |
| docutils       | 2.98 sec                                                               | 2.83 sec: 1.05x faster                                                |
| html5lib       | 90.8 ms                                                                | 72.1 ms: 1.26x faster                                                 |
| sphinx         | 1.16 sec                                                               | 1.13 sec: 1.03x faster                                                |
| Geometric mean | (ref)                                                                  | 1.11x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250110-vultr-x86_64-python-1b39b502d33c68f52fd7-3.14.0a3+-1b39b50 | bm-20250110-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-7ab3ec6 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none_tg         | 311 ms                                                                 | 240 ms: 1.30x faster                                                  |
| async_tree_memoization_tg  | 397 ms                                                                 | 308 ms: 1.29x faster                                                  |
| async_tree_io              | 749 ms                                                                 | 604 ms: 1.24x faster                                                  |
| async_tree_io_tg           | 726 ms                                                                 | 589 ms: 1.23x faster                                                  |
| async_tree_memoization     | 427 ms                                                                 | 350 ms: 1.22x faster                                                  |
| async_tree_none            | 348 ms                                                                 | 286 ms: 1.22x faster                                                  |
| async_tree_cpu_io_mixed_tg | 570 ms                                                                 | 481 ms: 1.18x faster                                                  |
| async_tree_cpu_io_mixed    | 601 ms                                                                 | 523 ms: 1.15x faster                                                  |
| async_generators           | 434 ms                                                                 | 426 ms: 1.02x faster                                                  |
| coroutines                 | 24.3 ms                                                                | 24.1 ms: 1.01x faster                                                 |
| asyncio_websockets         | 518 ms                                                                 | 516 ms: 1.00x faster                                                  |
| Geometric mean             | (ref)                                                                  | 1.16x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250110-vultr-x86_64-python-1b39b502d33c68f52fd7-3.14.0a3+-1b39b50 | bm-20250110-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-7ab3ec6 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 106 ms                                                                 | 75.6 ms: 1.40x faster                                                 |
| pidigits       | 189 ms                                                                 | 194 ms: 1.02x slower                                                  |
| nbody          | 125 ms                                                                 | 130 ms: 1.04x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.10x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250110-vultr-x86_64-python-1b39b502d33c68f52fd7-3.14.0a3+-1b39b50 | bm-20250110-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-7ab3ec6 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 166 ms                                                                 | 149 ms: 1.11x faster                                                  |
| regex_dna      | 182 ms                                                                 | 175 ms: 1.04x faster                                                  |
| regex_v8       | 24.1 ms                                                                | 23.7 ms: 1.01x faster                                                 |
| regex_effbot   | 2.77 ms                                                                | 2.93 ms: 1.06x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250110-vultr-x86_64-python-1b39b502d33c68f52fd7-3.14.0a3+-1b39b50 | bm-20250110-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-7ab3ec6 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_pure_python   | 491 us                                                                 | 364 us: 1.35x faster                                                  |
| unpickle_pure_python | 321 us                                                                 | 241 us: 1.33x faster                                                  |
| json_dumps           | 14.1 ms                                                                | 12.8 ms: 1.10x faster                                                 |
| xml_etree_process    | 73.7 ms                                                                | 68.1 ms: 1.08x faster                                                 |
| xml_etree_iterparse  | 89.6 ms                                                                | 87.1 ms: 1.03x faster                                                 |
| tomli_loads          | 2.38 sec                                                               | 2.32 sec: 1.02x faster                                                |
| xml_etree_generate   | 97.8 ms                                                                | 95.7 ms: 1.02x faster                                                 |
| json_loads           | 28.8 us                                                                | 28.3 us: 1.02x faster                                                 |
| xml_etree_parse      | 130 ms                                                                 | 129 ms: 1.01x faster                                                  |
| Geometric mean       | (ref)                                                                  | 1.10x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250110-vultr-x86_64-python-1b39b502d33c68f52fd7-3.14.0a3+-1b39b50 | bm-20250110-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-7ab3ec6 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 15.7 ms                                                                | 15.5 ms: 1.01x faster                                                 |
| python_startup_no_site | 9.79 ms                                                                | 9.73 ms: 1.01x faster                                                 |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250110-vultr-x86_64-python-1b39b502d33c68f52fd7-3.14.0a3+-1b39b50 | bm-20250110-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-7ab3ec6 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 49.5 ms                                                                | 43.0 ms: 1.15x faster                                                 |
| mako            | 17.0 ms                                                                | 15.7 ms: 1.08x faster                                                 |
| genshi_xml      | 63.3 ms                                                                | 59.4 ms: 1.07x faster                                                 |
| genshi_text     | 30.2 ms                                                                | 28.4 ms: 1.06x faster                                                 |
| Geometric mean  | (ref)                                                                  | 1.09x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20250110-vultr-x86_64-python-1b39b502d33c68f52fd7-3.14.0a3+-1b39b50 | bm-20250110-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-7ab3ec6 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| go                         | 229 ms                                                                 | 136 ms: 1.68x faster                                                  |
| logging_silent             | 185 ns                                                                 | 116 ns: 1.60x faster                                                  |
| deltablue                  | 7.20 ms                                                                | 4.63 ms: 1.56x faster                                                 |
| scimark_sor                | 203 ms                                                                 | 133 ms: 1.53x faster                                                  |
| raytrace                   | 486 ms                                                                 | 323 ms: 1.50x faster                                                  |
| sqlglot_parse              | 2.26 ms                                                                | 1.58 ms: 1.43x faster                                                 |
| float                      | 106 ms                                                                 | 75.6 ms: 1.40x faster                                                 |
| sqlglot_transpile          | 2.60 ms                                                                | 1.92 ms: 1.36x faster                                                 |
| pickle_pure_python         | 491 us                                                                 | 364 us: 1.35x faster                                                  |
| chaos                      | 94.4 ms                                                                | 70.3 ms: 1.34x faster                                                 |
| unpickle_pure_python       | 321 us                                                                 | 241 us: 1.33x faster                                                  |
| pyflate                    | 629 ms                                                                 | 482 ms: 1.30x faster                                                  |
| comprehensions             | 27.0 us                                                                | 20.7 us: 1.30x faster                                                 |
| async_tree_none_tg         | 311 ms                                                                 | 240 ms: 1.30x faster                                                  |
| async_tree_memoization_tg  | 397 ms                                                                 | 308 ms: 1.29x faster                                                  |
| scimark_monte_carlo        | 103 ms                                                                 | 81.1 ms: 1.27x faster                                                 |
| html5lib                   | 90.8 ms                                                                | 72.1 ms: 1.26x faster                                                 |
| hexiom                     | 9.16 ms                                                                | 7.30 ms: 1.26x faster                                                 |
| generators                 | 38.4 ms                                                                | 30.8 ms: 1.25x faster                                                 |
| async_tree_io              | 749 ms                                                                 | 604 ms: 1.24x faster                                                  |
| async_tree_io_tg           | 726 ms                                                                 | 589 ms: 1.23x faster                                                  |
| async_tree_memoization     | 427 ms                                                                 | 350 ms: 1.22x faster                                                  |
| async_tree_none            | 348 ms                                                                 | 286 ms: 1.22x faster                                                  |
| richards                   | 66.2 ms                                                                | 54.5 ms: 1.21x faster                                                 |
| logging_simple             | 8.75 us                                                                | 7.28 us: 1.20x faster                                                 |
| logging_format             | 9.91 us                                                                | 8.31 us: 1.19x faster                                                 |
| async_tree_cpu_io_mixed_tg | 570 ms                                                                 | 481 ms: 1.18x faster                                                  |
| django_template            | 49.5 ms                                                                | 43.0 ms: 1.15x faster                                                 |
| async_tree_cpu_io_mixed    | 601 ms                                                                 | 523 ms: 1.15x faster                                                  |
| sqlalchemy_imperative      | 27.9 ms                                                                | 24.3 ms: 1.15x faster                                                 |
| richards_super             | 73.6 ms                                                                | 64.4 ms: 1.14x faster                                                 |
| pprint_safe_repr           | 934 ms                                                                 | 819 ms: 1.14x faster                                                  |
| pprint_pformat             | 1.93 sec                                                               | 1.69 sec: 1.14x faster                                                |
| scimark_lu                 | 157 ms                                                                 | 139 ms: 1.13x faster                                                  |
| subparsers                 | 28.2 ms                                                                | 25.2 ms: 1.12x faster                                                 |
| pycparser                  | 1.34 sec                                                               | 1.20 sec: 1.12x faster                                                |
| sqlalchemy_declarative     | 182 ms                                                                 | 163 ms: 1.11x faster                                                  |
| regex_compile              | 166 ms                                                                 | 149 ms: 1.11x faster                                                  |
| 2to3                       | 344 ms                                                                 | 310 ms: 1.11x faster                                                  |
| json_dumps                 | 14.1 ms                                                                | 12.8 ms: 1.10x faster                                                 |
| dulwich_log                | 90.1 ms                                                                | 82.0 ms: 1.10x faster                                                 |
| thrift                     | 993 us                                                                 | 917 us: 1.08x faster                                                  |
| mako                       | 17.0 ms                                                                | 15.7 ms: 1.08x faster                                                 |
| xml_etree_process          | 73.7 ms                                                                | 68.1 ms: 1.08x faster                                                 |
| sqlglot_normalize          | 131 ms                                                                 | 121 ms: 1.08x faster                                                  |
| sqlglot_optimize           | 66.1 ms                                                                | 61.9 ms: 1.07x faster                                                 |
| genshi_xml                 | 63.3 ms                                                                | 59.4 ms: 1.07x faster                                                 |
| genshi_text                | 30.2 ms                                                                | 28.4 ms: 1.06x faster                                                 |
| docutils                   | 2.98 sec                                                               | 2.83 sec: 1.05x faster                                                |
| pylint                     | 342 ms                                                                 | 326 ms: 1.05x faster                                                  |
| many_optionals             | 1.23 ms                                                                | 1.17 ms: 1.05x faster                                                 |
| deepcopy_memo              | 40.8 us                                                                | 38.9 us: 1.05x faster                                                 |
| bpe_tokeniser              | 4.95 sec                                                               | 4.74 sec: 1.04x faster                                                |
| sympy_str                  | 350 ms                                                                 | 335 ms: 1.04x faster                                                  |
| sympy_expand               | 572 ms                                                                 | 549 ms: 1.04x faster                                                  |
| sqlite_synth               | 2.13 us                                                                | 2.05 us: 1.04x faster                                                 |
| regex_dna                  | 182 ms                                                                 | 175 ms: 1.04x faster                                                  |
| sympy_sum                  | 193 ms                                                                 | 186 ms: 1.04x faster                                                  |
| sphinx                     | 1.16 sec                                                               | 1.13 sec: 1.03x faster                                                |
| crypto_pyaes               | 89.3 ms                                                                | 86.6 ms: 1.03x faster                                                 |
| json                       | 5.11 ms                                                                | 4.96 ms: 1.03x faster                                                 |
| sympy_integrate            | 24.9 ms                                                                | 24.2 ms: 1.03x faster                                                 |
| xml_etree_iterparse        | 89.6 ms                                                                | 87.1 ms: 1.03x faster                                                 |
| mdp                        | 2.78 sec                                                               | 2.70 sec: 1.03x faster                                                |
| deepcopy                   | 324 us                                                                 | 315 us: 1.03x faster                                                  |
| typing_runtime_protocols   | 205 us                                                                 | 199 us: 1.03x faster                                                  |
| tomli_loads                | 2.38 sec                                                               | 2.32 sec: 1.02x faster                                                |
| bench_mp_pool              | 100 ms                                                                 | 97.8 ms: 1.02x faster                                                 |
| shortest_path              | 547 ms                                                                 | 535 ms: 1.02x faster                                                  |
| xml_etree_generate         | 97.8 ms                                                                | 95.7 ms: 1.02x faster                                                 |
| gc_traversal               | 3.29 ms                                                                | 3.22 ms: 1.02x faster                                                 |
| async_generators           | 434 ms                                                                 | 426 ms: 1.02x faster                                                  |
| json_loads                 | 28.8 us                                                                | 28.3 us: 1.02x faster                                                 |
| scimark_sparse_mat_mult    | 5.62 ms                                                                | 5.52 ms: 1.02x faster                                                 |
| spectral_norm              | 114 ms                                                                 | 112 ms: 1.02x faster                                                  |
| deepcopy_reduce            | 3.37 us                                                                | 3.32 us: 1.02x faster                                                 |
| regex_v8                   | 24.1 ms                                                                | 23.7 ms: 1.01x faster                                                 |
| connected_components       | 493 ms                                                                 | 486 ms: 1.01x faster                                                  |
| bench_thread_pool          | 3.37 ms                                                                | 3.33 ms: 1.01x faster                                                 |
| k_core                     | 2.34 sec                                                               | 2.31 sec: 1.01x faster                                                |
| xml_etree_parse            | 130 ms                                                                 | 129 ms: 1.01x faster                                                  |
| python_startup             | 15.7 ms                                                                | 15.5 ms: 1.01x faster                                                 |
| fannkuch                   | 481 ms                                                                 | 477 ms: 1.01x faster                                                  |
| coroutines                 | 24.3 ms                                                                | 24.1 ms: 1.01x faster                                                 |
| pathlib                    | 19.2 ms                                                                | 19.1 ms: 1.01x faster                                                 |
| python_startup_no_site     | 9.79 ms                                                                | 9.73 ms: 1.01x faster                                                 |
| asyncio_websockets         | 518 ms                                                                 | 516 ms: 1.00x faster                                                  |
| scimark_fft                | 380 ms                                                                 | 381 ms: 1.00x slower                                                  |
| nqueens                    | 95.7 ms                                                                | 97.0 ms: 1.01x slower                                                 |
| create_gc_cycles           | 1.81 ms                                                                | 1.84 ms: 1.02x slower                                                 |
| pidigits                   | 189 ms                                                                 | 194 ms: 1.02x slower                                                  |
| nbody                      | 125 ms                                                                 | 130 ms: 1.04x slower                                                  |
| regex_effbot               | 2.77 ms                                                                | 2.93 ms: 1.06x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.12x faster                                                          |

Benchmark hidden because not significant (3): telco, coverage, meteor_contest

- Geometric mean (including insignificant results): 1.117x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.01x