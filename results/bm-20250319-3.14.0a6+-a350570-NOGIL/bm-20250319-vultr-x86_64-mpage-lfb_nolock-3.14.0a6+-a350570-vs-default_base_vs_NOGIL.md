# Results vs. default_base_vs_NOGIL

- fork: mpage
- ref: lfb_nolock
- machine: linux-x86_64
- commit hash: a350570
- commit date: 2025-03-19
- overall geometric mean: 1.067x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x slower
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6+-fd545d7 | bm-20250319-vultr-x86_64-mpage-lfb_nolock-3.14.0a6+-a350570 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| 2to3           | 258 ms                                                                 | 288 ms: 1.11x slower                                        |
| docutils       | 2.61 sec                                                               | 2.75 sec: 1.05x slower                                      |
| sphinx         | 1.00 sec                                                               | 1.08 sec: 1.07x slower                                      |
| Geometric mean | (ref)                                                                  | 1.08x slower                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6+-fd545d7 | bm-20250319-vultr-x86_64-mpage-lfb_nolock-3.14.0a6+-a350570 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| async_tree_io_tg           | 628 ms                                                                 | 525 ms: 1.20x faster                                        |
| async_tree_none_tg         | 260 ms                                                                 | 225 ms: 1.15x faster                                        |
| async_tree_io              | 630 ms                                                                 | 557 ms: 1.13x faster                                        |
| async_tree_memoization_tg  | 315 ms                                                                 | 289 ms: 1.09x faster                                        |
| async_tree_none            | 274 ms                                                                 | 261 ms: 1.05x faster                                        |
| async_tree_memoization     | 327 ms                                                                 | 322 ms: 1.02x faster                                        |
| async_generators           | 340 ms                                                                 | 372 ms: 1.09x slower                                        |
| async_tree_cpu_io_mixed_tg | 498 ms                                                                 | 555 ms: 1.12x slower                                        |
| async_tree_cpu_io_mixed    | 512 ms                                                                 | 587 ms: 1.15x slower                                        |
| Geometric mean             | (ref)                                                                  | 1.02x faster                                                |

Benchmark hidden because not significant (2): coroutines, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6+-fd545d7 | bm-20250319-vultr-x86_64-mpage-lfb_nolock-3.14.0a6+-a350570 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| float          | 74.5 ms                                                                | 65.3 ms: 1.14x faster                                       |
| nbody          | 99.0 ms                                                                | 105 ms: 1.06x slower                                        |
| pidigits       | 206 ms                                                                 | 228 ms: 1.11x slower                                        |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6+-fd545d7 | bm-20250319-vultr-x86_64-mpage-lfb_nolock-3.14.0a6+-a350570 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| regex_v8       | 24.3 ms                                                                | 21.0 ms: 1.16x faster                                       |
| regex_dna      | 177 ms                                                                 | 165 ms: 1.07x faster                                        |
| regex_effbot   | 2.64 ms                                                                | 2.63 ms: 1.00x faster                                       |
| regex_compile  | 128 ms                                                                 | 151 ms: 1.18x slower                                        |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6+-fd545d7 | bm-20250319-vultr-x86_64-mpage-lfb_nolock-3.14.0a6+-a350570 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| xml_etree_iterparse  | 93.6 ms                                                                | 88.5 ms: 1.06x faster                                       |
| xml_etree_parse      | 130 ms                                                                 | 128 ms: 1.01x faster                                        |
| json_loads           | 28.4 us                                                                | 29.5 us: 1.04x slower                                       |
| unpickle_pure_python | 223 us                                                                 | 236 us: 1.06x slower                                        |
| pickle_pure_python   | 322 us                                                                 | 342 us: 1.06x slower                                        |
| xml_etree_generate   | 85.7 ms                                                                | 96.3 ms: 1.12x slower                                       |
| tomli_loads          | 1.98 sec                                                               | 2.26 sec: 1.14x slower                                      |
| json_dumps           | 11.2 ms                                                                | 12.8 ms: 1.14x slower                                       |
| xml_etree_process    | 59.7 ms                                                                | 68.7 ms: 1.15x slower                                       |
| Geometric mean       | (ref)                                                                  | 1.07x slower                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6+-fd545d7 | bm-20250319-vultr-x86_64-mpage-lfb_nolock-3.14.0a6+-a350570 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| python_startup         | 15.0 ms                                                                | 15.7 ms: 1.05x slower                                       |
| python_startup_no_site | 8.62 ms                                                                | 11.1 ms: 1.29x slower                                       |
| Geometric mean         | (ref)                                                                  | 1.16x slower                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6+-fd545d7 | bm-20250319-vultr-x86_64-mpage-lfb_nolock-3.14.0a6+-a350570 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| django_template | 36.5 ms                                                                | 41.4 ms: 1.13x slower                                       |
| genshi_xml      | 51.0 ms                                                                | 57.9 ms: 1.13x slower                                       |
| genshi_text     | 22.5 ms                                                                | 26.9 ms: 1.20x slower                                       |
| mako            | 12.2 ms                                                                | 15.6 ms: 1.28x slower                                       |
| Geometric mean  | (ref)                                                                  | 1.18x slower                                                |

All benchmarks:
===============

| Benchmark                  | bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6+-fd545d7 | bm-20250319-vultr-x86_64-mpage-lfb_nolock-3.14.0a6+-a350570 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| gc_traversal               | 4.16 ms                                                                | 1.79 ms: 2.32x faster                                       |
| create_gc_cycles           | 1.82 ms                                                                | 1.35 ms: 1.35x faster                                       |
| async_tree_io_tg           | 628 ms                                                                 | 525 ms: 1.20x faster                                        |
| regex_v8                   | 24.3 ms                                                                | 21.0 ms: 1.16x faster                                       |
| async_tree_none_tg         | 260 ms                                                                 | 225 ms: 1.15x faster                                        |
| float                      | 74.5 ms                                                                | 65.3 ms: 1.14x faster                                       |
| async_tree_io              | 630 ms                                                                 | 557 ms: 1.13x faster                                        |
| async_tree_memoization_tg  | 315 ms                                                                 | 289 ms: 1.09x faster                                        |
| sqlite_synth               | 2.19 us                                                                | 2.02 us: 1.08x faster                                       |
| regex_dna                  | 177 ms                                                                 | 165 ms: 1.07x faster                                        |
| xml_etree_iterparse        | 93.6 ms                                                                | 88.5 ms: 1.06x faster                                       |
| async_tree_none            | 274 ms                                                                 | 261 ms: 1.05x faster                                        |
| async_tree_memoization     | 327 ms                                                                 | 322 ms: 1.02x faster                                        |
| pycparser                  | 1.15 sec                                                               | 1.13 sec: 1.02x faster                                      |
| xml_etree_parse            | 130 ms                                                                 | 128 ms: 1.01x faster                                        |
| regex_effbot               | 2.64 ms                                                                | 2.63 ms: 1.00x faster                                       |
| pathlib                    | 19.3 ms                                                                | 19.6 ms: 1.01x slower                                       |
| logging_silent             | 103 ns                                                                 | 105 ns: 1.02x slower                                        |
| json_loads                 | 28.4 us                                                                | 29.5 us: 1.04x slower                                       |
| bpe_tokeniser              | 4.37 sec                                                               | 4.57 sec: 1.04x slower                                      |
| docutils                   | 2.61 sec                                                               | 2.75 sec: 1.05x slower                                      |
| python_startup             | 15.0 ms                                                                | 15.7 ms: 1.05x slower                                       |
| scimark_fft                | 329 ms                                                                 | 347 ms: 1.05x slower                                        |
| unpickle_pure_python       | 223 us                                                                 | 236 us: 1.06x slower                                        |
| pickle_pure_python         | 322 us                                                                 | 342 us: 1.06x slower                                        |
| nbody                      | 99.0 ms                                                                | 105 ms: 1.06x slower                                        |
| sphinx                     | 1.00 sec                                                               | 1.08 sec: 1.07x slower                                      |
| scimark_sparse_mat_mult    | 4.84 ms                                                                | 5.19 ms: 1.07x slower                                       |
| dulwich_log                | 68.0 ms                                                                | 73.1 ms: 1.07x slower                                       |
| raytrace                   | 271 ms                                                                 | 292 ms: 1.07x slower                                        |
| pyflate                    | 427 ms                                                                 | 460 ms: 1.08x slower                                        |
| chaos                      | 59.0 ms                                                                | 63.6 ms: 1.08x slower                                       |
| pprint_safe_repr           | 736 ms                                                                 | 798 ms: 1.08x slower                                        |
| generators                 | 29.7 ms                                                                | 32.2 ms: 1.08x slower                                       |
| k_core                     | 2.07 sec                                                               | 2.25 sec: 1.09x slower                                      |
| subparsers                 | 22.9 ms                                                                | 24.9 ms: 1.09x slower                                       |
| pprint_pformat             | 1.52 sec                                                               | 1.65 sec: 1.09x slower                                      |
| many_optionals             | 1.04 ms                                                                | 1.14 ms: 1.09x slower                                       |
| go                         | 116 ms                                                                 | 127 ms: 1.09x slower                                        |
| bench_mp_pool              | 88.4 ms                                                                | 96.7 ms: 1.09x slower                                       |
| async_generators           | 340 ms                                                                 | 372 ms: 1.09x slower                                        |
| deltablue                  | 3.17 ms                                                                | 3.47 ms: 1.10x slower                                       |
| pylint                     | 284 ms                                                                 | 313 ms: 1.10x slower                                        |
| scimark_sor                | 115 ms                                                                 | 127 ms: 1.10x slower                                        |
| nqueens                    | 83.8 ms                                                                | 92.4 ms: 1.10x slower                                       |
| scimark_monte_carlo        | 67.1 ms                                                                | 74.1 ms: 1.10x slower                                       |
| pidigits                   | 206 ms                                                                 | 228 ms: 1.11x slower                                        |
| 2to3                       | 258 ms                                                                 | 288 ms: 1.11x slower                                        |
| async_tree_cpu_io_mixed_tg | 498 ms                                                                 | 555 ms: 1.12x slower                                        |
| thrift                     | 748 us                                                                 | 837 us: 1.12x slower                                        |
| fannkuch                   | 403 ms                                                                 | 452 ms: 1.12x slower                                        |
| deepcopy                   | 266 us                                                                 | 299 us: 1.12x slower                                        |
| xml_etree_generate         | 85.7 ms                                                                | 96.3 ms: 1.12x slower                                       |
| deepcopy_reduce            | 2.74 us                                                                | 3.09 us: 1.13x slower                                       |
| django_template            | 36.5 ms                                                                | 41.4 ms: 1.13x slower                                       |
| genshi_xml                 | 51.0 ms                                                                | 57.9 ms: 1.13x slower                                       |
| tomli_loads                | 1.98 sec                                                               | 2.26 sec: 1.14x slower                                      |
| logging_simple             | 6.14 us                                                                | 7.02 us: 1.14x slower                                       |
| json_dumps                 | 11.2 ms                                                                | 12.8 ms: 1.14x slower                                       |
| spectral_norm              | 93.1 ms                                                                | 107 ms: 1.15x slower                                        |
| async_tree_cpu_io_mixed    | 512 ms                                                                 | 587 ms: 1.15x slower                                        |
| telco                      | 7.56 ms                                                                | 8.68 ms: 1.15x slower                                       |
| sympy_expand               | 475 ms                                                                 | 546 ms: 1.15x slower                                        |
| scimark_lu                 | 117 ms                                                                 | 135 ms: 1.15x slower                                        |
| xml_etree_process          | 59.7 ms                                                                | 68.7 ms: 1.15x slower                                       |
| mdp                        | 2.35 sec                                                               | 2.73 sec: 1.16x slower                                      |
| comprehensions             | 17.0 us                                                                | 19.8 us: 1.16x slower                                       |
| crypto_pyaes               | 71.8 ms                                                                | 83.4 ms: 1.16x slower                                       |
| logging_format             | 6.83 us                                                                | 7.99 us: 1.17x slower                                       |
| sympy_integrate            | 20.1 ms                                                                | 23.6 ms: 1.17x slower                                       |
| sympy_sum                  | 157 ms                                                                 | 185 ms: 1.18x slower                                        |
| coverage                   | 81.1 ms                                                                | 95.7 ms: 1.18x slower                                       |
| regex_compile              | 128 ms                                                                 | 151 ms: 1.18x slower                                        |
| sympy_str                  | 280 ms                                                                 | 332 ms: 1.19x slower                                        |
| deepcopy_memo              | 30.8 us                                                                | 36.5 us: 1.19x slower                                       |
| hexiom                     | 6.10 ms                                                                | 7.27 ms: 1.19x slower                                       |
| richards                   | 43.2 ms                                                                | 51.5 ms: 1.19x slower                                       |
| genshi_text                | 22.5 ms                                                                | 26.9 ms: 1.20x slower                                       |
| sqlalchemy_declarative     | 131 ms                                                                 | 158 ms: 1.20x slower                                        |
| shortest_path              | 443 ms                                                                 | 533 ms: 1.21x slower                                        |
| meteor_contest             | 105 ms                                                                 | 126 ms: 1.21x slower                                        |
| connected_components       | 403 ms                                                                 | 486 ms: 1.21x slower                                        |
| richards_super             | 49.2 ms                                                                | 60.2 ms: 1.23x slower                                       |
| sqlalchemy_imperative      | 19.5 ms                                                                | 23.9 ms: 1.23x slower                                       |
| typing_runtime_protocols   | 157 us                                                                 | 194 us: 1.24x slower                                        |
| mako                       | 12.2 ms                                                                | 15.6 ms: 1.28x slower                                       |
| python_startup_no_site     | 8.62 ms                                                                | 11.1 ms: 1.29x slower                                       |
| bench_thread_pool          | 1.05 ms                                                                | 3.13 ms: 2.99x slower                                       |
| Geometric mean             | (ref)                                                                  | 1.08x slower                                                |

Benchmark hidden because not significant (3): json, coroutines, asyncio_websockets
Ignored benchmarks (4) of results/bm-20250317-3.14.0a6+-fd545d7/bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6+-fd545d7.json: sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile
Ignored benchmarks (5) of results/bm-20250319-3.14.0a6+-a350570-NOGIL/bm-20250319-vultr-x86_64-mpage-lfb_nolock-3.14.0a6+-a350570.json: html5lib, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.067x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.06x

# Memory
- memory change: 1.21x