# Results vs. default_base_vs_NOGIL

- fork: mpage
- ref: experiment_noinline
- machine: linux-x86_64
- commit hash: 521fae6
- commit date: 2025-04-07
- overall geometric mean: 1.048x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 255 ms                                                                 | 279 ms: 1.10x slower                                                 |
| docutils       | 2.58 sec                                                               | 2.70 sec: 1.04x slower                                               |
| sphinx         | 1000 ms                                                                | 1.06 sec: 1.06x slower                                               |
| Geometric mean | (ref)                                                                  | 1.07x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 631 ms                                                                 | 520 ms: 1.21x faster                                                 |
| async_tree_none_tg         | 265 ms                                                                 | 226 ms: 1.17x faster                                                 |
| async_tree_io              | 632 ms                                                                 | 545 ms: 1.16x faster                                                 |
| async_tree_memoization_tg  | 324 ms                                                                 | 285 ms: 1.14x faster                                                 |
| async_tree_none            | 282 ms                                                                 | 258 ms: 1.09x faster                                                 |
| coroutines                 | 24.5 ms                                                                | 22.8 ms: 1.07x faster                                                |
| async_tree_cpu_io_mixed_tg | 499 ms                                                                 | 473 ms: 1.05x faster                                                 |
| async_tree_memoization     | 321 ms                                                                 | 309 ms: 1.04x faster                                                 |
| async_tree_cpu_io_mixed    | 503 ms                                                                 | 499 ms: 1.01x faster                                                 |
| asyncio_websockets         | 517 ms                                                                 | 515 ms: 1.00x faster                                                 |
| async_generators           | 337 ms                                                                 | 367 ms: 1.09x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.08x faster                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 71.4 ms                                                                | 67.2 ms: 1.06x faster                                                |
| pidigits       | 190 ms                                                                 | 191 ms: 1.00x slower                                                 |
| nbody          | 92.6 ms                                                                | 114 ms: 1.23x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.05x slower                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 2.84 ms                                                                | 2.63 ms: 1.08x faster                                                |
| regex_v8       | 22.1 ms                                                                | 20.6 ms: 1.07x faster                                                |
| regex_dna      | 181 ms                                                                 | 173 ms: 1.05x faster                                                 |
| regex_compile  | 130 ms                                                                 | 142 ms: 1.09x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| xml_etree_iterparse  | 93.7 ms                                                                | 85.0 ms: 1.10x faster                                                |
| xml_etree_parse      | 130 ms                                                                 | 128 ms: 1.01x faster                                                 |
| pickle_pure_python   | 322 us                                                                 | 326 us: 1.01x slower                                                 |
| unpickle_pure_python | 222 us                                                                 | 229 us: 1.03x slower                                                 |
| tomli_loads          | 1.99 sec                                                               | 2.12 sec: 1.06x slower                                               |
| xml_etree_generate   | 85.1 ms                                                                | 92.2 ms: 1.08x slower                                                |
| xml_etree_process    | 60.6 ms                                                                | 65.9 ms: 1.09x slower                                                |
| json_dumps           | 11.2 ms                                                                | 12.3 ms: 1.10x slower                                                |
| json_loads           | 27.7 us                                                                | 30.6 us: 1.10x slower                                                |
| Geometric mean       | (ref)                                                                  | 1.04x slower                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup         | 15.1 ms                                                                | 15.8 ms: 1.05x slower                                                |
| python_startup_no_site | 8.64 ms                                                                | 11.1 ms: 1.29x slower                                                |
| Geometric mean         | (ref)                                                                  | 1.16x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 50.5 ms                                                                | 54.6 ms: 1.08x slower                                                |
| django_template | 36.6 ms                                                                | 39.6 ms: 1.08x slower                                                |
| genshi_text     | 22.0 ms                                                                | 25.7 ms: 1.17x slower                                                |
| mako            | 12.2 ms                                                                | 15.0 ms: 1.23x slower                                                |
| Geometric mean  | (ref)                                                                  | 1.14x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| gc_traversal               | 4.26 ms                                                                | 1.79 ms: 2.38x faster                                                |
| create_gc_cycles           | 1.84 ms                                                                | 1.35 ms: 1.36x faster                                                |
| async_tree_io_tg           | 631 ms                                                                 | 520 ms: 1.21x faster                                                 |
| async_tree_none_tg         | 265 ms                                                                 | 226 ms: 1.17x faster                                                 |
| async_tree_io              | 632 ms                                                                 | 545 ms: 1.16x faster                                                 |
| async_tree_memoization_tg  | 324 ms                                                                 | 285 ms: 1.14x faster                                                 |
| sqlite_synth               | 2.18 us                                                                | 1.97 us: 1.11x faster                                                |
| xml_etree_iterparse        | 93.7 ms                                                                | 85.0 ms: 1.10x faster                                                |
| async_tree_none            | 282 ms                                                                 | 258 ms: 1.09x faster                                                 |
| regex_effbot               | 2.84 ms                                                                | 2.63 ms: 1.08x faster                                                |
| coroutines                 | 24.5 ms                                                                | 22.8 ms: 1.07x faster                                                |
| regex_v8                   | 22.1 ms                                                                | 20.6 ms: 1.07x faster                                                |
| float                      | 71.4 ms                                                                | 67.2 ms: 1.06x faster                                                |
| async_tree_cpu_io_mixed_tg | 499 ms                                                                 | 473 ms: 1.05x faster                                                 |
| regex_dna                  | 181 ms                                                                 | 173 ms: 1.05x faster                                                 |
| pycparser                  | 1.17 sec                                                               | 1.12 sec: 1.04x faster                                               |
| async_tree_memoization     | 321 ms                                                                 | 309 ms: 1.04x faster                                                 |
| pathlib                    | 19.7 ms                                                                | 19.2 ms: 1.03x faster                                                |
| xml_etree_parse            | 130 ms                                                                 | 128 ms: 1.01x faster                                                 |
| async_tree_cpu_io_mixed    | 503 ms                                                                 | 499 ms: 1.01x faster                                                 |
| asyncio_websockets         | 517 ms                                                                 | 515 ms: 1.00x faster                                                 |
| pidigits                   | 190 ms                                                                 | 191 ms: 1.00x slower                                                 |
| generators                 | 29.2 ms                                                                | 29.5 ms: 1.01x slower                                                |
| pickle_pure_python         | 322 us                                                                 | 326 us: 1.01x slower                                                 |
| dulwich_log                | 68.9 ms                                                                | 70.6 ms: 1.02x slower                                                |
| scimark_sor                | 115 ms                                                                 | 118 ms: 1.03x slower                                                 |
| unpickle_pure_python       | 222 us                                                                 | 229 us: 1.03x slower                                                 |
| bpe_tokeniser              | 4.35 sec                                                               | 4.49 sec: 1.03x slower                                               |
| pprint_safe_repr           | 732 ms                                                                 | 764 ms: 1.04x slower                                                 |
| docutils                   | 2.58 sec                                                               | 2.70 sec: 1.04x slower                                               |
| python_startup             | 15.1 ms                                                                | 15.8 ms: 1.05x slower                                                |
| deltablue                  | 3.36 ms                                                                | 3.52 ms: 1.05x slower                                                |
| logging_silent             | 101 ns                                                                 | 106 ns: 1.05x slower                                                 |
| json                       | 4.96 ms                                                                | 5.22 ms: 1.05x slower                                                |
| nqueens                    | 80.8 ms                                                                | 85.3 ms: 1.05x slower                                                |
| pprint_pformat             | 1.49 sec                                                               | 1.58 sec: 1.06x slower                                               |
| sphinx                     | 1000 ms                                                                | 1.06 sec: 1.06x slower                                               |
| tomli_loads                | 1.99 sec                                                               | 2.12 sec: 1.06x slower                                               |
| pylint                     | 287 ms                                                                 | 306 ms: 1.06x slower                                                 |
| many_optionals             | 1.04 ms                                                                | 1.11 ms: 1.07x slower                                                |
| bench_mp_pool              | 88.9 ms                                                                | 94.8 ms: 1.07x slower                                                |
| scimark_fft                | 321 ms                                                                 | 342 ms: 1.07x slower                                                 |
| sqlglot_v2_normalize       | 106 ms                                                                 | 113 ms: 1.07x slower                                                 |
| spectral_norm              | 98.0 ms                                                                | 105 ms: 1.07x slower                                                 |
| scimark_lu                 | 117 ms                                                                 | 126 ms: 1.08x slower                                                 |
| genshi_xml                 | 50.5 ms                                                                | 54.6 ms: 1.08x slower                                                |
| deepcopy_reduce            | 2.69 us                                                                | 2.91 us: 1.08x slower                                                |
| subparsers                 | 22.5 ms                                                                | 24.4 ms: 1.08x slower                                                |
| hexiom                     | 6.12 ms                                                                | 6.63 ms: 1.08x slower                                                |
| xml_etree_generate         | 85.1 ms                                                                | 92.2 ms: 1.08x slower                                                |
| django_template            | 36.6 ms                                                                | 39.6 ms: 1.08x slower                                                |
| k_core                     | 2.06 sec                                                               | 2.24 sec: 1.08x slower                                               |
| xml_etree_process          | 60.6 ms                                                                | 65.9 ms: 1.09x slower                                                |
| go                         | 114 ms                                                                 | 124 ms: 1.09x slower                                                 |
| async_generators           | 337 ms                                                                 | 367 ms: 1.09x slower                                                 |
| logging_simple             | 6.24 us                                                                | 6.80 us: 1.09x slower                                                |
| sqlglot_v2_optimize        | 52.5 ms                                                                | 57.4 ms: 1.09x slower                                                |
| regex_compile              | 130 ms                                                                 | 142 ms: 1.09x slower                                                 |
| 2to3                       | 255 ms                                                                 | 279 ms: 1.10x slower                                                 |
| deepcopy                   | 262 us                                                                 | 288 us: 1.10x slower                                                 |
| json_dumps                 | 11.2 ms                                                                | 12.3 ms: 1.10x slower                                                |
| json_loads                 | 27.7 us                                                                | 30.6 us: 1.10x slower                                                |
| chaos                      | 55.9 ms                                                                | 61.7 ms: 1.10x slower                                                |
| mdp                        | 1.18 sec                                                               | 1.31 sec: 1.11x slower                                               |
| pyflate                    | 420 ms                                                                 | 466 ms: 1.11x slower                                                 |
| raytrace                   | 260 ms                                                                 | 289 ms: 1.11x slower                                                 |
| sqlglot_v2_transpile       | 1.59 ms                                                                | 1.77 ms: 1.11x slower                                                |
| comprehensions             | 17.3 us                                                                | 19.3 us: 1.11x slower                                                |
| sympy_expand               | 471 ms                                                                 | 526 ms: 1.12x slower                                                 |
| telco                      | 7.29 ms                                                                | 8.19 ms: 1.12x slower                                                |
| richards                   | 44.5 ms                                                                | 50.0 ms: 1.12x slower                                                |
| sympy_sum                  | 159 ms                                                                 | 179 ms: 1.13x slower                                                 |
| logging_format             | 6.92 us                                                                | 7.80 us: 1.13x slower                                                |
| sympy_str                  | 281 ms                                                                 | 317 ms: 1.13x slower                                                 |
| scimark_sparse_mat_mult    | 4.40 ms                                                                | 4.99 ms: 1.13x slower                                                |
| sympy_integrate            | 19.6 ms                                                                | 22.3 ms: 1.14x slower                                                |
| richards_super             | 50.3 ms                                                                | 57.6 ms: 1.14x slower                                                |
| sqlglot_v2_parse           | 1.28 ms                                                                | 1.47 ms: 1.14x slower                                                |
| fannkuch                   | 396 ms                                                                 | 454 ms: 1.15x slower                                                 |
| sqlalchemy_declarative     | 132 ms                                                                 | 153 ms: 1.16x slower                                                 |
| scimark_monte_carlo        | 63.8 ms                                                                | 74.1 ms: 1.16x slower                                                |
| sqlalchemy_imperative      | 20.6 ms                                                                | 24.0 ms: 1.16x slower                                                |
| genshi_text                | 22.0 ms                                                                | 25.7 ms: 1.17x slower                                                |
| typing_runtime_protocols   | 162 us                                                                 | 191 us: 1.18x slower                                                 |
| crypto_pyaes               | 69.7 ms                                                                | 83.3 ms: 1.19x slower                                                |
| deepcopy_memo              | 29.7 us                                                                | 35.7 us: 1.20x slower                                                |
| shortest_path              | 441 ms                                                                 | 532 ms: 1.21x slower                                                 |
| connected_components       | 399 ms                                                                 | 489 ms: 1.23x slower                                                 |
| nbody                      | 92.6 ms                                                                | 114 ms: 1.23x slower                                                 |
| mako                       | 12.2 ms                                                                | 15.0 ms: 1.23x slower                                                |
| meteor_contest             | 101 ms                                                                 | 124 ms: 1.24x slower                                                 |
| python_startup_no_site     | 8.64 ms                                                                | 11.1 ms: 1.29x slower                                                |
| coverage                   | 79.9 ms                                                                | 108 ms: 1.35x slower                                                 |
| bench_thread_pool          | 1.06 ms                                                                | 3.14 ms: 2.97x slower                                                |
| Geometric mean             | (ref)                                                                  | 1.06x slower                                                         |
Ignored benchmarks (1) of results/bm-20250407-3.14.0a6+-521fae6-NOGIL/bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6.json: html5lib

- Geometric mean (including insignificant results): 1.048x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.05x
- 95% likely to have a slowdown of 1.04x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.20x