# Results vs. default_base_vs_NOGIL

- fork: mpage
- ref: gh_115999_load_attr_
- machine: linux-x86_64
- commit hash: 7ab3ec6
- commit date: 2025-01-10
- overall geometric mean: 1.142x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.12x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250110-vultr-x86_64-python-1b39b502d33c68f52fd7-3.14.0a3+-1b39b50 | bm-20250110-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-7ab3ec6 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 252 ms                                                                 | 310 ms: 1.23x slower                                                  |
| docutils       | 2.53 sec                                                               | 2.83 sec: 1.12x slower                                                |
| sphinx         | 977 ms                                                                 | 1.13 sec: 1.15x slower                                                |
| Geometric mean | (ref)                                                                  | 1.17x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250110-vultr-x86_64-python-1b39b502d33c68f52fd7-3.14.0a3+-1b39b50 | bm-20250110-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-7ab3ec6 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none_tg         | 252 ms                                                                 | 240 ms: 1.05x faster                                                  |
| async_tree_io_tg           | 602 ms                                                                 | 589 ms: 1.02x faster                                                  |
| asyncio_websockets         | 523 ms                                                                 | 516 ms: 1.01x faster                                                  |
| async_tree_cpu_io_mixed_tg | 470 ms                                                                 | 481 ms: 1.02x slower                                                  |
| async_tree_memoization_tg  | 300 ms                                                                 | 308 ms: 1.03x slower                                                  |
| async_tree_none            | 268 ms                                                                 | 286 ms: 1.07x slower                                                  |
| async_tree_cpu_io_mixed    | 490 ms                                                                 | 523 ms: 1.07x slower                                                  |
| async_tree_memoization     | 324 ms                                                                 | 350 ms: 1.08x slower                                                  |
| coroutines                 | 21.0 ms                                                                | 24.1 ms: 1.14x slower                                                 |
| async_generators           | 358 ms                                                                 | 426 ms: 1.19x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.04x slower                                                          |

Benchmark hidden because not significant (1): async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250110-vultr-x86_64-python-1b39b502d33c68f52fd7-3.14.0a3+-1b39b50 | bm-20250110-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-7ab3ec6 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 184 ms                                                                 | 194 ms: 1.05x slower                                                  |
| float          | 71.8 ms                                                                | 75.6 ms: 1.05x slower                                                 |
| nbody          | 89.9 ms                                                                | 130 ms: 1.45x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.17x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250110-vultr-x86_64-python-1b39b502d33c68f52fd7-3.14.0a3+-1b39b50 | bm-20250110-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-7ab3ec6 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_dna      | 182 ms                                                                 | 175 ms: 1.04x faster                                                  |
| regex_v8       | 24.4 ms                                                                | 23.7 ms: 1.03x faster                                                 |
| regex_effbot   | 2.82 ms                                                                | 2.93 ms: 1.04x slower                                                 |
| regex_compile  | 125 ms                                                                 | 149 ms: 1.19x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.04x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250110-vultr-x86_64-python-1b39b502d33c68f52fd7-3.14.0a3+-1b39b50 | bm-20250110-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-7ab3ec6 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 90.3 ms                                                                | 87.1 ms: 1.04x faster                                                 |
| xml_etree_parse      | 128 ms                                                                 | 129 ms: 1.01x slower                                                  |
| json_loads           | 25.8 us                                                                | 28.3 us: 1.10x slower                                                 |
| json_dumps           | 11.4 ms                                                                | 12.8 ms: 1.13x slower                                                 |
| unpickle_pure_python | 209 us                                                                 | 241 us: 1.15x slower                                                  |
| xml_etree_generate   | 82.5 ms                                                                | 95.7 ms: 1.16x slower                                                 |
| xml_etree_process    | 56.9 ms                                                                | 68.1 ms: 1.20x slower                                                 |
| pickle_pure_python   | 303 us                                                                 | 364 us: 1.20x slower                                                  |
| tomli_loads          | 1.89 sec                                                               | 2.32 sec: 1.23x slower                                                |
| Geometric mean       | (ref)                                                                  | 1.12x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250110-vultr-x86_64-python-1b39b502d33c68f52fd7-3.14.0a3+-1b39b50 | bm-20250110-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-7ab3ec6 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                                | 15.5 ms: 1.06x slower                                                 |
| python_startup_no_site | 7.48 ms                                                                | 9.73 ms: 1.30x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.18x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250110-vultr-x86_64-python-1b39b502d33c68f52fd7-3.14.0a3+-1b39b50 | bm-20250110-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-7ab3ec6 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 48.7 ms                                                                | 59.4 ms: 1.22x slower                                                 |
| django_template | 34.6 ms                                                                | 43.0 ms: 1.24x slower                                                 |
| mako            | 11.6 ms                                                                | 15.7 ms: 1.35x slower                                                 |
| genshi_text     | 21.0 ms                                                                | 28.4 ms: 1.35x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.29x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20250110-vultr-x86_64-python-1b39b502d33c68f52fd7-3.14.0a3+-1b39b50 | bm-20250110-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-7ab3ec6 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal               | 4.39 ms                                                                | 3.22 ms: 1.36x faster                                                 |
| sqlite_synth               | 2.20 us                                                                | 2.05 us: 1.07x faster                                                 |
| async_tree_none_tg         | 252 ms                                                                 | 240 ms: 1.05x faster                                                  |
| xml_etree_iterparse        | 90.3 ms                                                                | 87.1 ms: 1.04x faster                                                 |
| regex_dna                  | 182 ms                                                                 | 175 ms: 1.04x faster                                                  |
| regex_v8                   | 24.4 ms                                                                | 23.7 ms: 1.03x faster                                                 |
| async_tree_io_tg           | 602 ms                                                                 | 589 ms: 1.02x faster                                                  |
| asyncio_websockets         | 523 ms                                                                 | 516 ms: 1.01x faster                                                  |
| create_gc_cycles           | 1.85 ms                                                                | 1.84 ms: 1.01x faster                                                 |
| xml_etree_parse            | 128 ms                                                                 | 129 ms: 1.01x slower                                                  |
| async_tree_cpu_io_mixed_tg | 470 ms                                                                 | 481 ms: 1.02x slower                                                  |
| async_tree_memoization_tg  | 300 ms                                                                 | 308 ms: 1.03x slower                                                  |
| regex_effbot               | 2.82 ms                                                                | 2.93 ms: 1.04x slower                                                 |
| json                       | 4.73 ms                                                                | 4.96 ms: 1.05x slower                                                 |
| pidigits                   | 184 ms                                                                 | 194 ms: 1.05x slower                                                  |
| float                      | 71.8 ms                                                                | 75.6 ms: 1.05x slower                                                 |
| python_startup             | 14.6 ms                                                                | 15.5 ms: 1.06x slower                                                 |
| async_tree_none            | 268 ms                                                                 | 286 ms: 1.07x slower                                                  |
| async_tree_cpu_io_mixed    | 490 ms                                                                 | 523 ms: 1.07x slower                                                  |
| pathlib                    | 17.8 ms                                                                | 19.1 ms: 1.07x slower                                                 |
| async_tree_memoization     | 324 ms                                                                 | 350 ms: 1.08x slower                                                  |
| pycparser                  | 1.11 sec                                                               | 1.20 sec: 1.08x slower                                                |
| dulwich_log                | 75.0 ms                                                                | 82.0 ms: 1.09x slower                                                 |
| json_loads                 | 25.8 us                                                                | 28.3 us: 1.10x slower                                                 |
| spectral_norm              | 102 ms                                                                 | 112 ms: 1.10x slower                                                  |
| bench_mp_pool              | 88.8 ms                                                                | 97.8 ms: 1.10x slower                                                 |
| logging_silent             | 104 ns                                                                 | 116 ns: 1.12x slower                                                  |
| docutils                   | 2.53 sec                                                               | 2.83 sec: 1.12x slower                                                |
| bpe_tokeniser              | 4.23 sec                                                               | 4.74 sec: 1.12x slower                                                |
| generators                 | 27.4 ms                                                                | 30.8 ms: 1.12x slower                                                 |
| json_dumps                 | 11.4 ms                                                                | 12.8 ms: 1.13x slower                                                 |
| k_core                     | 2.05 sec                                                               | 2.31 sec: 1.13x slower                                                |
| many_optionals             | 1.02 ms                                                                | 1.17 ms: 1.14x slower                                                 |
| coroutines                 | 21.0 ms                                                                | 24.1 ms: 1.14x slower                                                 |
| sphinx                     | 977 ms                                                                 | 1.13 sec: 1.15x slower                                                |
| unpickle_pure_python       | 209 us                                                                 | 241 us: 1.15x slower                                                  |
| scimark_sor                | 114 ms                                                                 | 133 ms: 1.16x slower                                                  |
| xml_etree_generate         | 82.5 ms                                                                | 95.7 ms: 1.16x slower                                                 |
| pyflate                    | 413 ms                                                                 | 482 ms: 1.17x slower                                                  |
| pylint                     | 279 ms                                                                 | 326 ms: 1.17x slower                                                  |
| subparsers                 | 21.5 ms                                                                | 25.2 ms: 1.17x slower                                                 |
| mdp                        | 2.30 sec                                                               | 2.70 sec: 1.18x slower                                                |
| sqlglot_normalize          | 102 ms                                                                 | 121 ms: 1.19x slower                                                  |
| regex_compile              | 125 ms                                                                 | 149 ms: 1.19x slower                                                  |
| async_generators           | 358 ms                                                                 | 426 ms: 1.19x slower                                                  |
| logging_simple             | 6.11 us                                                                | 7.28 us: 1.19x slower                                                 |
| xml_etree_process          | 56.9 ms                                                                | 68.1 ms: 1.20x slower                                                 |
| sqlglot_optimize           | 51.8 ms                                                                | 61.9 ms: 1.20x slower                                                 |
| pprint_safe_repr           | 682 ms                                                                 | 819 ms: 1.20x slower                                                  |
| pickle_pure_python         | 303 us                                                                 | 364 us: 1.20x slower                                                  |
| go                         | 113 ms                                                                 | 136 ms: 1.20x slower                                                  |
| sympy_expand               | 454 ms                                                                 | 549 ms: 1.21x slower                                                  |
| logging_format             | 6.85 us                                                                | 8.31 us: 1.21x slower                                                 |
| telco                      | 7.20 ms                                                                | 8.73 ms: 1.21x slower                                                 |
| pprint_pformat             | 1.39 sec                                                               | 1.69 sec: 1.22x slower                                                |
| genshi_xml                 | 48.7 ms                                                                | 59.4 ms: 1.22x slower                                                 |
| scimark_fft                | 312 ms                                                                 | 381 ms: 1.22x slower                                                  |
| chaos                      | 57.3 ms                                                                | 70.3 ms: 1.23x slower                                                 |
| 2to3                       | 252 ms                                                                 | 310 ms: 1.23x slower                                                  |
| tomli_loads                | 1.89 sec                                                               | 2.32 sec: 1.23x slower                                                |
| sympy_sum                  | 151 ms                                                                 | 186 ms: 1.23x slower                                                  |
| comprehensions             | 16.8 us                                                                | 20.7 us: 1.23x slower                                                 |
| sympy_integrate            | 19.6 ms                                                                | 24.2 ms: 1.24x slower                                                 |
| sympy_str                  | 270 ms                                                                 | 335 ms: 1.24x slower                                                  |
| shortest_path              | 431 ms                                                                 | 535 ms: 1.24x slower                                                  |
| sqlglot_transpile          | 1.54 ms                                                                | 1.92 ms: 1.24x slower                                                 |
| django_template            | 34.6 ms                                                                | 43.0 ms: 1.24x slower                                                 |
| nqueens                    | 77.7 ms                                                                | 97.0 ms: 1.25x slower                                                 |
| scimark_sparse_mat_mult    | 4.42 ms                                                                | 5.52 ms: 1.25x slower                                                 |
| connected_components       | 389 ms                                                                 | 486 ms: 1.25x slower                                                  |
| deepcopy                   | 251 us                                                                 | 315 us: 1.25x slower                                                  |
| coverage                   | 79.1 ms                                                                | 99.2 ms: 1.25x slower                                                 |
| raytrace                   | 256 ms                                                                 | 323 ms: 1.26x slower                                                  |
| thrift                     | 725 us                                                                 | 917 us: 1.26x slower                                                  |
| scimark_lu                 | 110 ms                                                                 | 139 ms: 1.27x slower                                                  |
| sqlalchemy_imperative      | 19.2 ms                                                                | 24.3 ms: 1.27x slower                                                 |
| sqlglot_parse              | 1.24 ms                                                                | 1.58 ms: 1.27x slower                                                 |
| sqlalchemy_declarative     | 127 ms                                                                 | 163 ms: 1.28x slower                                                  |
| hexiom                     | 5.69 ms                                                                | 7.30 ms: 1.28x slower                                                 |
| typing_runtime_protocols   | 155 us                                                                 | 199 us: 1.29x slower                                                  |
| python_startup_no_site     | 7.48 ms                                                                | 9.73 ms: 1.30x slower                                                 |
| deepcopy_reduce            | 2.54 us                                                                | 3.32 us: 1.30x slower                                                 |
| richards                   | 41.7 ms                                                                | 54.5 ms: 1.31x slower                                                 |
| fannkuch                   | 364 ms                                                                 | 477 ms: 1.31x slower                                                  |
| deepcopy_memo              | 29.7 us                                                                | 38.9 us: 1.31x slower                                                 |
| scimark_monte_carlo        | 61.7 ms                                                                | 81.1 ms: 1.31x slower                                                 |
| meteor_contest             | 98.5 ms                                                                | 131 ms: 1.33x slower                                                  |
| crypto_pyaes               | 64.9 ms                                                                | 86.6 ms: 1.33x slower                                                 |
| richards_super             | 47.8 ms                                                                | 64.4 ms: 1.35x slower                                                 |
| mako                       | 11.6 ms                                                                | 15.7 ms: 1.35x slower                                                 |
| genshi_text                | 21.0 ms                                                                | 28.4 ms: 1.35x slower                                                 |
| nbody                      | 89.9 ms                                                                | 130 ms: 1.45x slower                                                  |
| deltablue                  | 3.12 ms                                                                | 4.63 ms: 1.48x slower                                                 |
| bench_thread_pool          | 1.03 ms                                                                | 3.33 ms: 3.23x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.18x slower                                                          |

Benchmark hidden because not significant (1): async_tree_io
Ignored benchmarks (1) of results/bm-20250110-3.14.0a3+-7ab3ec6-NOGIL/bm-20250110-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-7ab3ec6.json: html5lib

- Geometric mean (including insignificant results): 1.142x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.14x
- 95% likely to have a slowdown of 1.14x
- 99% likely to have a slowdown of 1.12x

# Memory
- memory change: 1.20x