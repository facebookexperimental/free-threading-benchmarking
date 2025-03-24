# Results vs. default_base_vs_NOGIL

- fork: mpage
- ref: measure_latest_lfb
- machine: linux-x86_64
- commit hash: 80fc5aa
- commit date: 2025-03-23
- overall geometric mean: 1.090x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250323-vultr-x86_64-python-ef06508f8ef1d2943b2f-3.14.0a6+-ef06508 | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 256 ms                                                                 | 289 ms: 1.13x slower                                                |
| docutils       | 2.59 sec                                                               | 2.75 sec: 1.06x slower                                              |
| sphinx         | 998 ms                                                                 | 1.09 sec: 1.09x slower                                              |
| Geometric mean | (ref)                                                                  | 1.09x slower                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250323-vultr-x86_64-python-ef06508f8ef1d2943b2f-3.14.0a6+-ef06508 | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_io_tg           | 652 ms                                                                 | 541 ms: 1.20x faster                                                |
| async_tree_none_tg         | 262 ms                                                                 | 233 ms: 1.12x faster                                                |
| async_tree_io              | 630 ms                                                                 | 573 ms: 1.10x faster                                                |
| async_tree_memoization_tg  | 313 ms                                                                 | 294 ms: 1.06x faster                                                |
| async_tree_cpu_io_mixed_tg | 497 ms                                                                 | 478 ms: 1.04x faster                                                |
| async_tree_none            | 280 ms                                                                 | 274 ms: 1.02x faster                                                |
| async_tree_memoization     | 324 ms                                                                 | 326 ms: 1.01x slower                                                |
| async_generators           | 334 ms                                                                 | 380 ms: 1.14x slower                                                |
| Geometric mean             | (ref)                                                                  | 1.04x faster                                                        |

Benchmark hidden because not significant (3): asyncio_websockets, async_tree_cpu_io_mixed, coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250323-vultr-x86_64-python-ef06508f8ef1d2943b2f-3.14.0a6+-ef06508 | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| pidigits       | 208 ms                                                                 | 198 ms: 1.05x faster                                                |
| float          | 74.6 ms                                                                | 71.8 ms: 1.04x faster                                               |
| nbody          | 99.6 ms                                                                | 120 ms: 1.21x slower                                                |
| Geometric mean | (ref)                                                                  | 1.04x slower                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250323-vultr-x86_64-python-ef06508f8ef1d2943b2f-3.14.0a6+-ef06508 | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_v8       | 21.7 ms                                                                | 21.3 ms: 1.02x faster                                               |
| regex_dna      | 170 ms                                                                 | 168 ms: 1.01x faster                                                |
| regex_effbot   | 2.60 ms                                                                | 2.73 ms: 1.05x slower                                               |
| regex_compile  | 129 ms                                                                 | 153 ms: 1.19x slower                                                |
| Geometric mean | (ref)                                                                  | 1.05x slower                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250323-vultr-x86_64-python-ef06508f8ef1d2943b2f-3.14.0a6+-ef06508 | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| xml_etree_iterparse  | 92.6 ms                                                                | 87.6 ms: 1.06x faster                                               |
| xml_etree_parse      | 130 ms                                                                 | 128 ms: 1.02x faster                                                |
| json_loads           | 27.8 us                                                                | 29.8 us: 1.07x slower                                               |
| pickle_pure_python   | 318 us                                                                 | 343 us: 1.08x slower                                                |
| unpickle_pure_python | 222 us                                                                 | 244 us: 1.10x slower                                                |
| xml_etree_generate   | 85.6 ms                                                                | 96.7 ms: 1.13x slower                                               |
| tomli_loads          | 1.97 sec                                                               | 2.25 sec: 1.14x slower                                              |
| json_dumps           | 11.2 ms                                                                | 12.8 ms: 1.14x slower                                               |
| xml_etree_process    | 60.0 ms                                                                | 70.7 ms: 1.18x slower                                               |
| Geometric mean       | (ref)                                                                  | 1.08x slower                                                        |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250323-vultr-x86_64-python-ef06508f8ef1d2943b2f-3.14.0a6+-ef06508 | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup         | 14.9 ms                                                                | 15.8 ms: 1.06x slower                                               |
| python_startup_no_site | 8.61 ms                                                                | 11.1 ms: 1.29x slower                                               |
| Geometric mean         | (ref)                                                                  | 1.17x slower                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250323-vultr-x86_64-python-ef06508f8ef1d2943b2f-3.14.0a6+-ef06508 | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|-----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| genshi_xml      | 50.9 ms                                                                | 57.8 ms: 1.14x slower                                               |
| django_template | 36.5 ms                                                                | 41.8 ms: 1.14x slower                                               |
| genshi_text     | 22.5 ms                                                                | 27.1 ms: 1.21x slower                                               |
| mako            | 12.0 ms                                                                | 15.7 ms: 1.31x slower                                               |
| Geometric mean  | (ref)                                                                  | 1.20x slower                                                        |

All benchmarks:
===============

| Benchmark                  | bm-20250323-vultr-x86_64-python-ef06508f8ef1d2943b2f-3.14.0a6+-ef06508 | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| gc_traversal               | 4.44 ms                                                                | 1.79 ms: 2.48x faster                                               |
| create_gc_cycles           | 1.85 ms                                                                | 1.34 ms: 1.38x faster                                               |
| async_tree_io_tg           | 652 ms                                                                 | 541 ms: 1.20x faster                                                |
| async_tree_none_tg         | 262 ms                                                                 | 233 ms: 1.12x faster                                                |
| sqlite_synth               | 2.23 us                                                                | 2.00 us: 1.11x faster                                               |
| async_tree_io              | 630 ms                                                                 | 573 ms: 1.10x faster                                                |
| async_tree_memoization_tg  | 313 ms                                                                 | 294 ms: 1.06x faster                                                |
| xml_etree_iterparse        | 92.6 ms                                                                | 87.6 ms: 1.06x faster                                               |
| pidigits                   | 208 ms                                                                 | 198 ms: 1.05x faster                                                |
| async_tree_cpu_io_mixed_tg | 497 ms                                                                 | 478 ms: 1.04x faster                                                |
| float                      | 74.6 ms                                                                | 71.8 ms: 1.04x faster                                               |
| async_tree_none            | 280 ms                                                                 | 274 ms: 1.02x faster                                                |
| regex_v8                   | 21.7 ms                                                                | 21.3 ms: 1.02x faster                                               |
| xml_etree_parse            | 130 ms                                                                 | 128 ms: 1.02x faster                                                |
| regex_dna                  | 170 ms                                                                 | 168 ms: 1.01x faster                                                |
| async_tree_memoization     | 324 ms                                                                 | 326 ms: 1.01x slower                                                |
| pathlib                    | 19.5 ms                                                                | 19.8 ms: 1.01x slower                                               |
| pycparser                  | 1.15 sec                                                               | 1.18 sec: 1.02x slower                                              |
| json                       | 4.86 ms                                                                | 5.04 ms: 1.04x slower                                               |
| regex_effbot               | 2.60 ms                                                                | 2.73 ms: 1.05x slower                                               |
| python_startup             | 14.9 ms                                                                | 15.8 ms: 1.06x slower                                               |
| docutils                   | 2.59 sec                                                               | 2.75 sec: 1.06x slower                                              |
| json_loads                 | 27.8 us                                                                | 29.8 us: 1.07x slower                                               |
| pickle_pure_python         | 318 us                                                                 | 343 us: 1.08x slower                                                |
| bench_mp_pool              | 89.6 ms                                                                | 97.1 ms: 1.08x slower                                               |
| logging_silent             | 102 ns                                                                 | 111 ns: 1.09x slower                                                |
| bpe_tokeniser              | 4.34 sec                                                               | 4.72 sec: 1.09x slower                                              |
| k_core                     | 2.07 sec                                                               | 2.26 sec: 1.09x slower                                              |
| sphinx                     | 998 ms                                                                 | 1.09 sec: 1.09x slower                                              |
| generators                 | 30.7 ms                                                                | 33.7 ms: 1.10x slower                                               |
| dulwich_log                | 67.6 ms                                                                | 74.2 ms: 1.10x slower                                               |
| unpickle_pure_python       | 222 us                                                                 | 244 us: 1.10x slower                                                |
| deepcopy_reduce            | 2.81 us                                                                | 3.10 us: 1.10x slower                                               |
| many_optionals             | 1.04 ms                                                                | 1.15 ms: 1.10x slower                                               |
| scimark_fft                | 330 ms                                                                 | 364 ms: 1.10x slower                                                |
| pprint_safe_repr           | 732 ms                                                                 | 816 ms: 1.12x slower                                                |
| pylint                     | 284 ms                                                                 | 316 ms: 1.12x slower                                                |
| deepcopy                   | 268 us                                                                 | 301 us: 1.12x slower                                                |
| scimark_sparse_mat_mult    | 4.65 ms                                                                | 5.21 ms: 1.12x slower                                               |
| subparsers                 | 22.4 ms                                                                | 25.2 ms: 1.13x slower                                               |
| pprint_pformat             | 1.49 sec                                                               | 1.68 sec: 1.13x slower                                              |
| 2to3                       | 256 ms                                                                 | 289 ms: 1.13x slower                                                |
| xml_etree_generate         | 85.6 ms                                                                | 96.7 ms: 1.13x slower                                               |
| scimark_sor                | 114 ms                                                                 | 129 ms: 1.13x slower                                                |
| genshi_xml                 | 50.9 ms                                                                | 57.8 ms: 1.14x slower                                               |
| async_generators           | 334 ms                                                                 | 380 ms: 1.14x slower                                                |
| thrift                     | 767 us                                                                 | 872 us: 1.14x slower                                                |
| sqlglot_v2_optimize        | 52.7 ms                                                                | 59.9 ms: 1.14x slower                                               |
| raytrace                   | 269 ms                                                                 | 307 ms: 1.14x slower                                                |
| tomli_loads                | 1.97 sec                                                               | 2.25 sec: 1.14x slower                                              |
| json_dumps                 | 11.2 ms                                                                | 12.8 ms: 1.14x slower                                               |
| django_template            | 36.5 ms                                                                | 41.8 ms: 1.14x slower                                               |
| sqlglot_v2_normalize       | 104 ms                                                                 | 119 ms: 1.15x slower                                                |
| sqlglot_v2_transpile       | 1.61 ms                                                                | 1.85 ms: 1.15x slower                                               |
| chaos                      | 57.4 ms                                                                | 66.4 ms: 1.16x slower                                               |
| nqueens                    | 83.1 ms                                                                | 96.6 ms: 1.16x slower                                               |
| fannkuch                   | 400 ms                                                                 | 466 ms: 1.16x slower                                                |
| pyflate                    | 421 ms                                                                 | 489 ms: 1.16x slower                                                |
| scimark_monte_carlo        | 67.5 ms                                                                | 78.9 ms: 1.17x slower                                               |
| sqlglot_v2_parse           | 1.30 ms                                                                | 1.52 ms: 1.17x slower                                               |
| deltablue                  | 3.14 ms                                                                | 3.70 ms: 1.18x slower                                               |
| xml_etree_process          | 60.0 ms                                                                | 70.7 ms: 1.18x slower                                               |
| mdp                        | 2.32 sec                                                               | 2.74 sec: 1.18x slower                                              |
| go                         | 114 ms                                                                 | 135 ms: 1.18x slower                                                |
| sympy_integrate            | 19.8 ms                                                                | 23.4 ms: 1.18x slower                                               |
| regex_compile              | 129 ms                                                                 | 153 ms: 1.19x slower                                                |
| sympy_expand               | 469 ms                                                                 | 558 ms: 1.19x slower                                                |
| sympy_sum                  | 157 ms                                                                 | 187 ms: 1.19x slower                                                |
| sympy_str                  | 279 ms                                                                 | 332 ms: 1.19x slower                                                |
| scimark_lu                 | 116 ms                                                                 | 138 ms: 1.20x slower                                                |
| comprehensions             | 17.0 us                                                                | 20.4 us: 1.20x slower                                               |
| spectral_norm              | 90.9 ms                                                                | 109 ms: 1.20x slower                                                |
| genshi_text                | 22.5 ms                                                                | 27.1 ms: 1.21x slower                                               |
| nbody                      | 99.6 ms                                                                | 120 ms: 1.21x slower                                                |
| shortest_path              | 442 ms                                                                 | 535 ms: 1.21x slower                                                |
| hexiom                     | 6.13 ms                                                                | 7.42 ms: 1.21x slower                                               |
| telco                      | 7.37 ms                                                                | 8.94 ms: 1.21x slower                                               |
| crypto_pyaes               | 70.7 ms                                                                | 85.9 ms: 1.22x slower                                               |
| logging_simple             | 6.01 us                                                                | 7.32 us: 1.22x slower                                               |
| sqlalchemy_declarative     | 130 ms                                                                 | 158 ms: 1.22x slower                                                |
| logging_format             | 6.66 us                                                                | 8.16 us: 1.22x slower                                               |
| sqlalchemy_imperative      | 19.7 ms                                                                | 24.1 ms: 1.23x slower                                               |
| richards                   | 43.8 ms                                                                | 53.8 ms: 1.23x slower                                               |
| deepcopy_memo              | 30.4 us                                                                | 37.3 us: 1.23x slower                                               |
| typing_runtime_protocols   | 156 us                                                                 | 194 us: 1.24x slower                                                |
| connected_components       | 394 ms                                                                 | 490 ms: 1.24x slower                                                |
| richards_super             | 49.7 ms                                                                | 62.1 ms: 1.25x slower                                               |
| meteor_contest             | 101 ms                                                                 | 128 ms: 1.27x slower                                                |
| python_startup_no_site     | 8.61 ms                                                                | 11.1 ms: 1.29x slower                                               |
| mako                       | 12.0 ms                                                                | 15.7 ms: 1.31x slower                                               |
| coverage                   | 79.4 ms                                                                | 107 ms: 1.35x slower                                                |
| bench_thread_pool          | 1.05 ms                                                                | 3.14 ms: 3.00x slower                                               |
| Geometric mean             | (ref)                                                                  | 1.11x slower                                                        |

Benchmark hidden because not significant (3): asyncio_websockets, async_tree_cpu_io_mixed, coroutines
Ignored benchmarks (1) of results/bm-20250323-3.14.0a6+-80fc5aa-NOGIL/bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa.json: html5lib

- Geometric mean (including insignificant results): 1.090x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.10x
- 95% likely to have a slowdown of 1.09x
- 99% likely to have a slowdown of 1.08x

# Memory
- memory change: 1.20x