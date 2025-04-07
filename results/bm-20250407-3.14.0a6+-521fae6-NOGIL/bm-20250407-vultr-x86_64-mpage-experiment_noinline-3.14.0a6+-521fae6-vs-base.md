# Results vs. base

- fork: mpage
- ref: experiment_noinline
- machine: linux-x86_64
- commit hash: 521fae6
- commit date: 2025-04-07
- overall geometric mean: 1.113x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.09x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 310 ms                                                                 | 279 ms: 1.11x faster                                                 |
| docutils       | 2.91 sec                                                               | 2.70 sec: 1.08x faster                                               |
| html5lib       | 75.8 ms                                                                | 64.3 ms: 1.18x faster                                                |
| sphinx         | 1.15 sec                                                               | 1.06 sec: 1.09x faster                                               |
| Geometric mean | (ref)                                                                  | 1.11x faster                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| coroutines                 | 27.0 ms                                                                | 22.8 ms: 1.19x faster                                                |
| async_tree_memoization_tg  | 312 ms                                                                 | 285 ms: 1.10x faster                                                 |
| async_tree_memoization     | 339 ms                                                                 | 309 ms: 1.10x faster                                                 |
| async_tree_io              | 597 ms                                                                 | 545 ms: 1.10x faster                                                 |
| async_tree_io_tg           | 567 ms                                                                 | 520 ms: 1.09x faster                                                 |
| async_tree_none_tg         | 246 ms                                                                 | 226 ms: 1.09x faster                                                 |
| async_tree_none            | 280 ms                                                                 | 258 ms: 1.08x faster                                                 |
| async_generators           | 387 ms                                                                 | 367 ms: 1.05x faster                                                 |
| async_tree_cpu_io_mixed    | 525 ms                                                                 | 499 ms: 1.05x faster                                                 |
| async_tree_cpu_io_mixed_tg | 498 ms                                                                 | 473 ms: 1.05x faster                                                 |
| Geometric mean             | (ref)                                                                  | 1.08x faster                                                         |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| nbody          | 140 ms                                                                 | 114 ms: 1.23x faster                                                 |
| float          | 77.6 ms                                                                | 67.2 ms: 1.16x faster                                                |
| pidigits       | 191 ms                                                                 | 191 ms: 1.00x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.13x faster                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_compile  | 169 ms                                                                 | 142 ms: 1.19x faster                                                 |
| regex_effbot   | 2.96 ms                                                                | 2.63 ms: 1.12x faster                                                |
| regex_v8       | 21.7 ms                                                                | 20.6 ms: 1.05x faster                                                |
| regex_dna      | 180 ms                                                                 | 173 ms: 1.04x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.10x faster                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| tomli_loads          | 2.51 sec                                                               | 2.12 sec: 1.19x faster                                               |
| unpickle_pure_python | 270 us                                                                 | 229 us: 1.18x faster                                                 |
| pickle_pure_python   | 381 us                                                                 | 326 us: 1.17x faster                                                 |
| xml_etree_process    | 74.2 ms                                                                | 65.9 ms: 1.13x faster                                                |
| xml_etree_generate   | 101 ms                                                                 | 92.2 ms: 1.10x faster                                                |
| xml_etree_iterparse  | 93.1 ms                                                                | 85.0 ms: 1.10x faster                                                |
| json_dumps           | 13.2 ms                                                                | 12.3 ms: 1.07x faster                                                |
| xml_etree_parse      | 130 ms                                                                 | 128 ms: 1.02x faster                                                 |
| json_loads           | 30.3 us                                                                | 30.6 us: 1.01x slower                                                |
| Geometric mean       | (ref)                                                                  | 1.10x faster                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup         | 16.0 ms                                                                | 15.8 ms: 1.01x faster                                                |
| python_startup_no_site | 11.2 ms                                                                | 11.1 ms: 1.01x faster                                                |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 68.4 ms                                                                | 54.6 ms: 1.25x faster                                                |
| genshi_text     | 31.4 ms                                                                | 25.7 ms: 1.22x faster                                                |
| django_template | 45.1 ms                                                                | 39.6 ms: 1.14x faster                                                |
| mako            | 16.5 ms                                                                | 15.0 ms: 1.10x faster                                                |
| Geometric mean  | (ref)                                                                  | 1.18x faster                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| generators                 | 44.5 ms                                                                | 29.5 ms: 1.51x faster                                                |
| scimark_sor                | 151 ms                                                                 | 118 ms: 1.28x faster                                                 |
| deltablue                  | 4.45 ms                                                                | 3.52 ms: 1.26x faster                                                |
| genshi_xml                 | 68.4 ms                                                                | 54.6 ms: 1.25x faster                                                |
| logging_simple             | 8.42 us                                                                | 6.80 us: 1.24x faster                                                |
| nbody                      | 140 ms                                                                 | 114 ms: 1.23x faster                                                 |
| go                         | 153 ms                                                                 | 124 ms: 1.23x faster                                                 |
| logging_format             | 9.56 us                                                                | 7.80 us: 1.23x faster                                                |
| genshi_text                | 31.4 ms                                                                | 25.7 ms: 1.22x faster                                                |
| hexiom                     | 8.08 ms                                                                | 6.63 ms: 1.22x faster                                                |
| richards                   | 59.8 ms                                                                | 50.0 ms: 1.20x faster                                                |
| regex_compile              | 169 ms                                                                 | 142 ms: 1.19x faster                                                 |
| tomli_loads                | 2.51 sec                                                               | 2.12 sec: 1.19x faster                                               |
| richards_super             | 68.3 ms                                                                | 57.6 ms: 1.19x faster                                                |
| coroutines                 | 27.0 ms                                                                | 22.8 ms: 1.19x faster                                                |
| unpickle_pure_python       | 270 us                                                                 | 229 us: 1.18x faster                                                 |
| html5lib                   | 75.8 ms                                                                | 64.3 ms: 1.18x faster                                                |
| raytrace                   | 341 ms                                                                 | 289 ms: 1.18x faster                                                 |
| logging_silent             | 124 ns                                                                 | 106 ns: 1.18x faster                                                 |
| nqueens                    | 100 ms                                                                 | 85.3 ms: 1.17x faster                                                |
| pprint_pformat             | 1.85 sec                                                               | 1.58 sec: 1.17x faster                                               |
| pickle_pure_python         | 381 us                                                                 | 326 us: 1.17x faster                                                 |
| pprint_safe_repr           | 890 ms                                                                 | 764 ms: 1.17x faster                                                 |
| scimark_monte_carlo        | 86.4 ms                                                                | 74.1 ms: 1.17x faster                                                |
| chaos                      | 71.8 ms                                                                | 61.7 ms: 1.16x faster                                                |
| float                      | 77.6 ms                                                                | 67.2 ms: 1.16x faster                                                |
| comprehensions             | 22.0 us                                                                | 19.3 us: 1.14x faster                                                |
| django_template            | 45.1 ms                                                                | 39.6 ms: 1.14x faster                                                |
| deepcopy                   | 327 us                                                                 | 288 us: 1.13x faster                                                 |
| pyflate                    | 529 ms                                                                 | 466 ms: 1.13x faster                                                 |
| sqlglot_v2_normalize       | 128 ms                                                                 | 113 ms: 1.13x faster                                                 |
| fannkuch                   | 514 ms                                                                 | 454 ms: 1.13x faster                                                 |
| scimark_lu                 | 142 ms                                                                 | 126 ms: 1.13x faster                                                 |
| sqlglot_v2_transpile       | 2.00 ms                                                                | 1.77 ms: 1.13x faster                                                |
| xml_etree_process          | 74.2 ms                                                                | 65.9 ms: 1.13x faster                                                |
| spectral_norm              | 118 ms                                                                 | 105 ms: 1.13x faster                                                 |
| mdp                        | 1.47 sec                                                               | 1.31 sec: 1.13x faster                                               |
| deepcopy_memo              | 40.2 us                                                                | 35.7 us: 1.12x faster                                                |
| deepcopy_reduce            | 3.27 us                                                                | 2.91 us: 1.12x faster                                                |
| sqlglot_v2_parse           | 1.65 ms                                                                | 1.47 ms: 1.12x faster                                                |
| regex_effbot               | 2.96 ms                                                                | 2.63 ms: 1.12x faster                                                |
| scimark_sparse_mat_mult    | 5.59 ms                                                                | 4.99 ms: 1.12x faster                                                |
| sqlglot_v2_optimize        | 64.1 ms                                                                | 57.4 ms: 1.12x faster                                                |
| pycparser                  | 1.25 sec                                                               | 1.12 sec: 1.12x faster                                               |
| sympy_str                  | 352 ms                                                                 | 317 ms: 1.11x faster                                                 |
| 2to3                       | 310 ms                                                                 | 279 ms: 1.11x faster                                                 |
| sympy_expand               | 584 ms                                                                 | 526 ms: 1.11x faster                                                 |
| dulwich_log                | 78.3 ms                                                                | 70.6 ms: 1.11x faster                                                |
| scimark_fft                | 379 ms                                                                 | 342 ms: 1.11x faster                                                 |
| subparsers                 | 26.9 ms                                                                | 24.4 ms: 1.10x faster                                                |
| bpe_tokeniser              | 4.94 sec                                                               | 4.49 sec: 1.10x faster                                               |
| xml_etree_generate         | 101 ms                                                                 | 92.2 ms: 1.10x faster                                                |
| mako                       | 16.5 ms                                                                | 15.0 ms: 1.10x faster                                                |
| async_tree_memoization_tg  | 312 ms                                                                 | 285 ms: 1.10x faster                                                 |
| xml_etree_iterparse        | 93.1 ms                                                                | 85.0 ms: 1.10x faster                                                |
| async_tree_memoization     | 339 ms                                                                 | 309 ms: 1.10x faster                                                 |
| async_tree_io              | 597 ms                                                                 | 545 ms: 1.10x faster                                                 |
| crypto_pyaes               | 90.9 ms                                                                | 83.3 ms: 1.09x faster                                                |
| many_optionals             | 1.21 ms                                                                | 1.11 ms: 1.09x faster                                                |
| sympy_sum                  | 195 ms                                                                 | 179 ms: 1.09x faster                                                 |
| async_tree_io_tg           | 567 ms                                                                 | 520 ms: 1.09x faster                                                 |
| meteor_contest             | 136 ms                                                                 | 124 ms: 1.09x faster                                                 |
| sphinx                     | 1.15 sec                                                               | 1.06 sec: 1.09x faster                                               |
| sympy_integrate            | 24.2 ms                                                                | 22.3 ms: 1.09x faster                                                |
| async_tree_none_tg         | 246 ms                                                                 | 226 ms: 1.09x faster                                                 |
| async_tree_none            | 280 ms                                                                 | 258 ms: 1.08x faster                                                 |
| pylint                     | 331 ms                                                                 | 306 ms: 1.08x faster                                                 |
| typing_runtime_protocols   | 206 us                                                                 | 191 us: 1.08x faster                                                 |
| docutils                   | 2.91 sec                                                               | 2.70 sec: 1.08x faster                                               |
| sqlalchemy_declarative     | 165 ms                                                                 | 153 ms: 1.08x faster                                                 |
| json_dumps                 | 13.2 ms                                                                | 12.3 ms: 1.07x faster                                                |
| sqlalchemy_imperative      | 25.3 ms                                                                | 24.0 ms: 1.06x faster                                                |
| telco                      | 8.64 ms                                                                | 8.19 ms: 1.06x faster                                                |
| async_generators           | 387 ms                                                                 | 367 ms: 1.05x faster                                                 |
| regex_v8                   | 21.7 ms                                                                | 20.6 ms: 1.05x faster                                                |
| async_tree_cpu_io_mixed    | 525 ms                                                                 | 499 ms: 1.05x faster                                                 |
| async_tree_cpu_io_mixed_tg | 498 ms                                                                 | 473 ms: 1.05x faster                                                 |
| connected_components       | 512 ms                                                                 | 489 ms: 1.05x faster                                                 |
| shortest_path              | 556 ms                                                                 | 532 ms: 1.05x faster                                                 |
| sqlite_synth               | 2.06 us                                                                | 1.97 us: 1.04x faster                                                |
| regex_dna                  | 180 ms                                                                 | 173 ms: 1.04x faster                                                 |
| pathlib                    | 19.9 ms                                                                | 19.2 ms: 1.04x faster                                                |
| bench_mp_pool              | 97.4 ms                                                                | 94.8 ms: 1.03x faster                                                |
| k_core                     | 2.29 sec                                                               | 2.24 sec: 1.02x faster                                               |
| coverage                   | 111 ms                                                                 | 108 ms: 1.02x faster                                                 |
| xml_etree_parse            | 130 ms                                                                 | 128 ms: 1.02x faster                                                 |
| bench_thread_pool          | 3.18 ms                                                                | 3.14 ms: 1.02x faster                                                |
| python_startup             | 16.0 ms                                                                | 15.8 ms: 1.01x faster                                                |
| python_startup_no_site     | 11.2 ms                                                                | 11.1 ms: 1.01x faster                                                |
| pidigits                   | 191 ms                                                                 | 191 ms: 1.00x faster                                                 |
| gc_traversal               | 1.78 ms                                                                | 1.79 ms: 1.01x slower                                                |
| json_loads                 | 30.3 us                                                                | 30.6 us: 1.01x slower                                                |
| create_gc_cycles           | 1.33 ms                                                                | 1.35 ms: 1.02x slower                                                |
| json                       | 5.11 ms                                                                | 5.22 ms: 1.02x slower                                                |
| Geometric mean             | (ref)                                                                  | 1.11x faster                                                         |

Benchmark hidden because not significant (1): asyncio_websockets

- Geometric mean (including insignificant results): 1.113x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.09x
- 99% likely to have a speedup of 1.09x

# Memory
- memory change: 1.01x