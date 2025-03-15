# Results vs. default_base_vs_NOGIL

- fork: mpage
- ref: measure_bc_atomics
- machine: linux-x86_64
- commit hash: 94fe18c
- commit date: 2025-03-15
- overall geometric mean: 1.098x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.09x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 | bm-20250315-vultr-x86_64-mpage-measure_bc_atomics-3.14.0a5+-94fe18c |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 258 ms                                                                 | 297 ms: 1.15x slower                                                |
| docutils       | 2.61 sec                                                               | 2.79 sec: 1.07x slower                                              |
| sphinx         | 995 ms                                                                 | 1.09 sec: 1.09x slower                                              |
| Geometric mean | (ref)                                                                  | 1.10x slower                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 | bm-20250315-vultr-x86_64-mpage-measure_bc_atomics-3.14.0a5+-94fe18c |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_io_tg           | 628 ms                                                                 | 547 ms: 1.15x faster                                                |
| async_tree_none_tg         | 267 ms                                                                 | 236 ms: 1.13x faster                                                |
| async_tree_io              | 630 ms                                                                 | 583 ms: 1.08x faster                                                |
| async_tree_memoization_tg  | 318 ms                                                                 | 304 ms: 1.05x faster                                                |
| async_tree_cpu_io_mixed_tg | 504 ms                                                                 | 486 ms: 1.04x faster                                                |
| coroutines                 | 23.4 ms                                                                | 23.9 ms: 1.02x slower                                               |
| async_tree_memoization     | 329 ms                                                                 | 337 ms: 1.02x slower                                                |
| async_generators           | 339 ms                                                                 | 374 ms: 1.10x slower                                                |
| Geometric mean             | (ref)                                                                  | 1.03x faster                                                        |

Benchmark hidden because not significant (3): async_tree_none, asyncio_websockets, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 | bm-20250315-vultr-x86_64-mpage-measure_bc_atomics-3.14.0a5+-94fe18c |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| pidigits       | 187 ms                                                                 | 202 ms: 1.08x slower                                                |
| nbody          | 102 ms                                                                 | 131 ms: 1.28x slower                                                |
| Geometric mean | (ref)                                                                  | 1.12x slower                                                        |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 | bm-20250315-vultr-x86_64-mpage-measure_bc_atomics-3.14.0a5+-94fe18c |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_dna      | 179 ms                                                                 | 169 ms: 1.06x faster                                                |
| regex_v8       | 24.5 ms                                                                | 23.6 ms: 1.04x faster                                               |
| regex_effbot   | 2.77 ms                                                                | 2.79 ms: 1.00x slower                                               |
| regex_compile  | 130 ms                                                                 | 156 ms: 1.20x slower                                                |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 | bm-20250315-vultr-x86_64-mpage-measure_bc_atomics-3.14.0a5+-94fe18c |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| xml_etree_iterparse  | 93.4 ms                                                                | 87.9 ms: 1.06x faster                                               |
| json_loads           | 27.0 us                                                                | 29.1 us: 1.08x slower                                               |
| pickle_pure_python   | 324 us                                                                 | 357 us: 1.10x slower                                                |
| xml_etree_generate   | 86.5 ms                                                                | 96.7 ms: 1.12x slower                                               |
| unpickle_pure_python | 224 us                                                                 | 254 us: 1.13x slower                                                |
| json_dumps           | 11.2 ms                                                                | 12.8 ms: 1.14x slower                                               |
| xml_etree_process    | 60.1 ms                                                                | 70.5 ms: 1.17x slower                                               |
| tomli_loads          | 2.00 sec                                                               | 2.37 sec: 1.18x slower                                              |
| Geometric mean       | (ref)                                                                  | 1.09x slower                                                        |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 | bm-20250315-vultr-x86_64-mpage-measure_bc_atomics-3.14.0a5+-94fe18c |
|------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup         | 14.9 ms                                                                | 15.7 ms: 1.05x slower                                               |
| python_startup_no_site | 8.63 ms                                                                | 11.1 ms: 1.28x slower                                               |
| Geometric mean         | (ref)                                                                  | 1.16x slower                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 | bm-20250315-vultr-x86_64-mpage-measure_bc_atomics-3.14.0a5+-94fe18c |
|-----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| django_template | 37.2 ms                                                                | 43.1 ms: 1.16x slower                                               |
| genshi_xml      | 51.0 ms                                                                | 59.9 ms: 1.17x slower                                               |
| genshi_text     | 21.9 ms                                                                | 27.9 ms: 1.28x slower                                               |
| mako            | 12.1 ms                                                                | 15.7 ms: 1.30x slower                                               |
| Geometric mean  | (ref)                                                                  | 1.22x slower                                                        |

All benchmarks:
===============

| Benchmark                  | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 | bm-20250315-vultr-x86_64-mpage-measure_bc_atomics-3.14.0a5+-94fe18c |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| gc_traversal               | 4.76 ms                                                                | 1.74 ms: 2.73x faster                                               |
| create_gc_cycles           | 1.83 ms                                                                | 1.33 ms: 1.37x faster                                               |
| async_tree_io_tg           | 628 ms                                                                 | 547 ms: 1.15x faster                                                |
| async_tree_none_tg         | 267 ms                                                                 | 236 ms: 1.13x faster                                                |
| async_tree_io              | 630 ms                                                                 | 583 ms: 1.08x faster                                                |
| sqlite_synth               | 2.21 us                                                                | 2.05 us: 1.08x faster                                               |
| xml_etree_iterparse        | 93.4 ms                                                                | 87.9 ms: 1.06x faster                                               |
| regex_dna                  | 179 ms                                                                 | 169 ms: 1.06x faster                                                |
| async_tree_memoization_tg  | 318 ms                                                                 | 304 ms: 1.05x faster                                                |
| regex_v8                   | 24.5 ms                                                                | 23.6 ms: 1.04x faster                                               |
| async_tree_cpu_io_mixed_tg | 504 ms                                                                 | 486 ms: 1.04x faster                                                |
| regex_effbot               | 2.77 ms                                                                | 2.79 ms: 1.00x slower                                               |
| pathlib                    | 19.6 ms                                                                | 19.7 ms: 1.01x slower                                               |
| pycparser                  | 1.16 sec                                                               | 1.19 sec: 1.02x slower                                              |
| coroutines                 | 23.4 ms                                                                | 23.9 ms: 1.02x slower                                               |
| async_tree_memoization     | 329 ms                                                                 | 337 ms: 1.02x slower                                                |
| json                       | 4.89 ms                                                                | 5.06 ms: 1.03x slower                                               |
| python_startup             | 14.9 ms                                                                | 15.7 ms: 1.05x slower                                               |
| docutils                   | 2.61 sec                                                               | 2.79 sec: 1.07x slower                                              |
| bench_mp_pool              | 88.2 ms                                                                | 94.9 ms: 1.08x slower                                               |
| json_loads                 | 27.0 us                                                                | 29.1 us: 1.08x slower                                               |
| dulwich_log                | 67.5 ms                                                                | 73.0 ms: 1.08x slower                                               |
| pidigits                   | 187 ms                                                                 | 202 ms: 1.08x slower                                                |
| generators                 | 29.7 ms                                                                | 32.3 ms: 1.09x slower                                               |
| bpe_tokeniser              | 4.43 sec                                                               | 4.82 sec: 1.09x slower                                              |
| pylint                     | 285 ms                                                                 | 312 ms: 1.09x slower                                                |
| sphinx                     | 995 ms                                                                 | 1.09 sec: 1.09x slower                                              |
| pickle_pure_python         | 324 us                                                                 | 357 us: 1.10x slower                                                |
| async_generators           | 339 ms                                                                 | 374 ms: 1.10x slower                                                |
| mdp                        | 2.50 sec                                                               | 2.78 sec: 1.11x slower                                              |
| subparsers                 | 22.7 ms                                                                | 25.4 ms: 1.12x slower                                               |
| many_optionals             | 1.04 ms                                                                | 1.16 ms: 1.12x slower                                               |
| xml_etree_generate         | 86.5 ms                                                                | 96.7 ms: 1.12x slower                                               |
| pprint_safe_repr           | 737 ms                                                                 | 828 ms: 1.12x slower                                                |
| k_core                     | 2.06 sec                                                               | 2.32 sec: 1.12x slower                                              |
| logging_silent             | 99.6 ns                                                                | 112 ns: 1.13x slower                                                |
| unpickle_pure_python       | 224 us                                                                 | 254 us: 1.13x slower                                                |
| json_dumps                 | 11.2 ms                                                                | 12.8 ms: 1.14x slower                                               |
| pprint_pformat             | 1.50 sec                                                               | 1.71 sec: 1.14x slower                                              |
| thrift                     | 754 us                                                                 | 862 us: 1.14x slower                                                |
| deepcopy_reduce            | 2.73 us                                                                | 3.13 us: 1.15x slower                                               |
| 2to3                       | 258 ms                                                                 | 297 ms: 1.15x slower                                                |
| sqlglot_normalize          | 104 ms                                                                 | 120 ms: 1.15x slower                                                |
| telco                      | 7.64 ms                                                                | 8.84 ms: 1.16x slower                                               |
| django_template            | 37.2 ms                                                                | 43.1 ms: 1.16x slower                                               |
| sqlglot_optimize           | 52.7 ms                                                                | 61.2 ms: 1.16x slower                                               |
| logging_simple             | 6.05 us                                                                | 7.05 us: 1.16x slower                                               |
| scimark_sor                | 116 ms                                                                 | 135 ms: 1.17x slower                                                |
| genshi_xml                 | 51.0 ms                                                                | 59.9 ms: 1.17x slower                                               |
| xml_etree_process          | 60.1 ms                                                                | 70.5 ms: 1.17x slower                                               |
| sqlglot_transpile          | 1.62 ms                                                                | 1.90 ms: 1.17x slower                                               |
| scimark_fft                | 334 ms                                                                 | 394 ms: 1.18x slower                                                |
| spectral_norm              | 95.9 ms                                                                | 113 ms: 1.18x slower                                                |
| chaos                      | 58.5 ms                                                                | 69.0 ms: 1.18x slower                                               |
| tomli_loads                | 2.00 sec                                                               | 2.37 sec: 1.18x slower                                              |
| sympy_expand               | 465 ms                                                                 | 551 ms: 1.18x slower                                                |
| sqlalchemy_imperative      | 19.8 ms                                                                | 23.5 ms: 1.19x slower                                               |
| comprehensions             | 17.2 us                                                                | 20.5 us: 1.19x slower                                               |
| sympy_integrate            | 20.1 ms                                                                | 23.9 ms: 1.19x slower                                               |
| pyflate                    | 425 ms                                                                 | 507 ms: 1.19x slower                                                |
| deepcopy                   | 261 us                                                                 | 312 us: 1.19x slower                                                |
| sqlalchemy_declarative     | 131 ms                                                                 | 157 ms: 1.19x slower                                                |
| sympy_sum                  | 156 ms                                                                 | 187 ms: 1.20x slower                                                |
| logging_format             | 6.73 us                                                                | 8.08 us: 1.20x slower                                               |
| regex_compile              | 130 ms                                                                 | 156 ms: 1.20x slower                                                |
| sqlglot_parse              | 1.32 ms                                                                | 1.58 ms: 1.20x slower                                               |
| coverage                   | 81.1 ms                                                                | 97.5 ms: 1.20x slower                                               |
| sympy_str                  | 278 ms                                                                 | 335 ms: 1.20x slower                                                |
| raytrace                   | 267 ms                                                                 | 322 ms: 1.20x slower                                                |
| nqueens                    | 81.4 ms                                                                | 98.5 ms: 1.21x slower                                               |
| crypto_pyaes               | 71.5 ms                                                                | 87.4 ms: 1.22x slower                                               |
| shortest_path              | 445 ms                                                                 | 548 ms: 1.23x slower                                                |
| scimark_lu                 | 114 ms                                                                 | 141 ms: 1.23x slower                                                |
| scimark_sparse_mat_mult    | 4.70 ms                                                                | 5.79 ms: 1.23x slower                                               |
| typing_runtime_protocols   | 158 us                                                                 | 195 us: 1.24x slower                                                |
| go                         | 113 ms                                                                 | 141 ms: 1.24x slower                                                |
| fannkuch                   | 401 ms                                                                 | 497 ms: 1.24x slower                                                |
| scimark_monte_carlo        | 66.6 ms                                                                | 82.6 ms: 1.24x slower                                               |
| deltablue                  | 3.12 ms                                                                | 3.87 ms: 1.24x slower                                               |
| hexiom                     | 6.10 ms                                                                | 7.57 ms: 1.24x slower                                               |
| connected_components       | 402 ms                                                                 | 501 ms: 1.25x slower                                                |
| deepcopy_memo              | 30.8 us                                                                | 38.6 us: 1.25x slower                                               |
| richards                   | 42.7 ms                                                                | 53.7 ms: 1.26x slower                                               |
| richards_super             | 49.8 ms                                                                | 63.2 ms: 1.27x slower                                               |
| genshi_text                | 21.9 ms                                                                | 27.9 ms: 1.28x slower                                               |
| nbody                      | 102 ms                                                                 | 131 ms: 1.28x slower                                                |
| python_startup_no_site     | 8.63 ms                                                                | 11.1 ms: 1.28x slower                                               |
| mako                       | 12.1 ms                                                                | 15.7 ms: 1.30x slower                                               |
| meteor_contest             | 101 ms                                                                 | 132 ms: 1.30x slower                                                |
| bench_thread_pool          | 1.05 ms                                                                | 3.15 ms: 2.99x slower                                               |
| Geometric mean             | (ref)                                                                  | 1.12x slower                                                        |

Benchmark hidden because not significant (5): async_tree_none, xml_etree_parse, asyncio_websockets, float, async_tree_cpu_io_mixed
Ignored benchmarks (1) of results/bm-20250315-3.14.0a5+-94fe18c-NOGIL/bm-20250315-vultr-x86_64-mpage-measure_bc_atomics-3.14.0a5+-94fe18c.json: html5lib

- Geometric mean (including insignificant results): 1.098x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.10x
- 95% likely to have a slowdown of 1.10x
- 99% likely to have a slowdown of 1.09x

# Memory
- memory change: 1.20x