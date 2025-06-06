# Results vs. 3.13.0rc2

- fork: nascheme
- ref: gh_132380_tp_getattr
- machine: linux-x86_64
- commit hash: 04ccde3
- commit date: 2025-06-05
- overall geometric mean: 1.020x slower
- HPT reliability: 95.66%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.40x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250605-vultr-x86_64-nascheme-gh_132380_tp_getattr-3.15.0a0-04ccde3 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 281 ms: 1.08x slower                                                    |
| docutils       | 2.63 sec                                                               | 2.65 sec: 1.01x slower                                                  |
| html5lib       | 68.6 ms                                                                | 66.4 ms: 1.03x faster                                                   |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250605-vultr-x86_64-nascheme-gh_132380_tp_getattr-3.15.0a0-04ccde3 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 519 ms: 1.74x faster                                                    |
| async_tree_io              | 881 ms                                                                 | 549 ms: 1.60x faster                                                    |
| async_tree_none_tg         | 333 ms                                                                 | 227 ms: 1.47x faster                                                    |
| async_tree_memoization     | 459 ms                                                                 | 315 ms: 1.46x faster                                                    |
| async_tree_memoization_tg  | 410 ms                                                                 | 285 ms: 1.44x faster                                                    |
| async_tree_none            | 353 ms                                                                 | 260 ms: 1.36x faster                                                    |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 471 ms: 1.35x faster                                                    |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 499 ms: 1.33x faster                                                    |
| async_generators           | 375 ms                                                                 | 365 ms: 1.03x faster                                                    |
| coroutines                 | 23.3 ms                                                                | 24.0 ms: 1.03x slower                                                   |
| Geometric mean             | (ref)                                                                  | 1.32x faster                                                            |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250605-vultr-x86_64-nascheme-gh_132380_tp_getattr-3.15.0a0-04ccde3 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 189 ms: 1.15x faster                                                    |
| float          | 76.7 ms                                                                | 69.7 ms: 1.10x faster                                                   |
| nbody          | 85.3 ms                                                                | 121 ms: 1.42x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.04x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250605-vultr-x86_64-nascheme-gh_132380_tp_getattr-3.15.0a0-04ccde3 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.63 ms: 1.22x faster                                                   |
| regex_v8       | 23.2 ms                                                                | 20.7 ms: 1.12x faster                                                   |
| regex_dna      | 189 ms                                                                 | 170 ms: 1.11x faster                                                    |
| regex_compile  | 131 ms                                                                 | 143 ms: 1.09x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.09x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250605-vultr-x86_64-nascheme-gh_132380_tp_getattr-3.15.0a0-04ccde3 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 87.5 ms: 1.08x faster                                                   |
| xml_etree_parse      | 136 ms                                                                 | 130 ms: 1.05x faster                                                    |
| tomli_loads          | 2.01 sec                                                               | 2.16 sec: 1.07x slower                                                  |
| unpickle_pure_python | 208 us                                                                 | 231 us: 1.11x slower                                                    |
| xml_etree_generate   | 85.4 ms                                                                | 95.5 ms: 1.12x slower                                                   |
| json_dumps           | 10.6 ms                                                                | 12.1 ms: 1.14x slower                                                   |
| json_loads           | 27.3 us                                                                | 31.2 us: 1.14x slower                                                   |
| pickle_pure_python   | 292 us                                                                 | 334 us: 1.15x slower                                                    |
| xml_etree_process    | 59.2 ms                                                                | 68.8 ms: 1.16x slower                                                   |
| Geometric mean       | (ref)                                                                  | 1.08x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250605-vultr-x86_64-nascheme-gh_132380_tp_getattr-3.15.0a0-04ccde3 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 9.54 ms: 1.29x slower                                                   |
| python_startup         | 11.0 ms                                                                | 15.9 ms: 1.44x slower                                                   |
| Geometric mean         | (ref)                                                                  | 1.36x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250605-vultr-x86_64-nascheme-gh_132380_tp_getattr-3.15.0a0-04ccde3 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| django_template | 34.2 ms                                                                | 40.6 ms: 1.19x slower                                                   |
| genshi_xml      | 49.1 ms                                                                | 58.4 ms: 1.19x slower                                                   |
| genshi_text     | 21.7 ms                                                                | 26.5 ms: 1.22x slower                                                   |
| mako            | 11.2 ms                                                                | 15.6 ms: 1.39x slower                                                   |
| Geometric mean  | (ref)                                                                  | 1.24x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250605-vultr-x86_64-nascheme-gh_132380_tp_getattr-3.15.0a0-04ccde3 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                        | 2.34 sec                                                               | 1.32 sec: 1.78x faster                                                  |
| gc_traversal               | 3.32 ms                                                                | 1.89 ms: 1.76x faster                                                   |
| async_tree_io_tg           | 901 ms                                                                 | 519 ms: 1.74x faster                                                    |
| async_tree_io              | 881 ms                                                                 | 549 ms: 1.60x faster                                                    |
| async_tree_none_tg         | 333 ms                                                                 | 227 ms: 1.47x faster                                                    |
| async_tree_memoization     | 459 ms                                                                 | 315 ms: 1.46x faster                                                    |
| async_tree_memoization_tg  | 410 ms                                                                 | 285 ms: 1.44x faster                                                    |
| async_tree_none            | 353 ms                                                                 | 260 ms: 1.36x faster                                                    |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 471 ms: 1.35x faster                                                    |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 499 ms: 1.33x faster                                                    |
| deepcopy                   | 357 us                                                                 | 291 us: 1.23x faster                                                    |
| regex_effbot               | 3.21 ms                                                                | 2.63 ms: 1.22x faster                                                   |
| go                         | 141 ms                                                                 | 121 ms: 1.16x faster                                                    |
| pidigits                   | 216 ms                                                                 | 189 ms: 1.15x faster                                                    |
| regex_v8                   | 23.2 ms                                                                | 20.7 ms: 1.12x faster                                                   |
| regex_dna                  | 189 ms                                                                 | 170 ms: 1.11x faster                                                    |
| sqlite_synth               | 2.25 us                                                                | 2.04 us: 1.10x faster                                                   |
| float                      | 76.7 ms                                                                | 69.7 ms: 1.10x faster                                                   |
| deepcopy_memo              | 38.1 us                                                                | 34.7 us: 1.10x faster                                                   |
| scimark_sor                | 134 ms                                                                 | 123 ms: 1.08x faster                                                    |
| xml_etree_iterparse        | 94.4 ms                                                                | 87.5 ms: 1.08x faster                                                   |
| dulwich_log                | 74.5 ms                                                                | 70.9 ms: 1.05x faster                                                   |
| xml_etree_parse            | 136 ms                                                                 | 130 ms: 1.05x faster                                                    |
| deepcopy_reduce            | 3.12 us                                                                | 3.00 us: 1.04x faster                                                   |
| html5lib                   | 68.6 ms                                                                | 66.4 ms: 1.03x faster                                                   |
| async_generators           | 375 ms                                                                 | 365 ms: 1.03x faster                                                    |
| bpe_tokeniser              | 4.46 sec                                                               | 4.36 sec: 1.02x faster                                                  |
| docutils                   | 2.63 sec                                                               | 2.65 sec: 1.01x slower                                                  |
| pathlib                    | 19.3 ms                                                                | 19.4 ms: 1.01x slower                                                   |
| pycparser                  | 1.12 sec                                                               | 1.13 sec: 1.01x slower                                                  |
| coroutines                 | 23.3 ms                                                                | 24.0 ms: 1.03x slower                                                   |
| pyflate                    | 449 ms                                                                 | 466 ms: 1.04x slower                                                    |
| comprehensions             | 16.6 us                                                                | 17.4 us: 1.05x slower                                                   |
| spectral_norm              | 108 ms                                                                 | 114 ms: 1.06x slower                                                    |
| json                       | 4.98 ms                                                                | 5.29 ms: 1.06x slower                                                   |
| scimark_fft                | 348 ms                                                                 | 370 ms: 1.06x slower                                                    |
| hexiom                     | 5.95 ms                                                                | 6.35 ms: 1.07x slower                                                   |
| tomli_loads                | 2.01 sec                                                               | 2.16 sec: 1.07x slower                                                  |
| 2to3                       | 259 ms                                                                 | 281 ms: 1.08x slower                                                    |
| regex_compile              | 131 ms                                                                 | 143 ms: 1.09x slower                                                    |
| create_gc_cycles           | 1.33 ms                                                                | 1.46 ms: 1.09x slower                                                   |
| nqueens                    | 77.7 ms                                                                | 85.4 ms: 1.10x slower                                                   |
| telco                      | 7.77 ms                                                                | 8.56 ms: 1.10x slower                                                   |
| generators                 | 28.5 ms                                                                | 31.6 ms: 1.11x slower                                                   |
| unpickle_pure_python       | 208 us                                                                 | 231 us: 1.11x slower                                                    |
| sympy_integrate            | 19.7 ms                                                                | 21.9 ms: 1.11x slower                                                   |
| chaos                      | 56.3 ms                                                                | 62.9 ms: 1.12x slower                                                   |
| xml_etree_generate         | 85.4 ms                                                                | 95.5 ms: 1.12x slower                                                   |
| thrift                     | 772 us                                                                 | 868 us: 1.13x slower                                                    |
| json_dumps                 | 10.6 ms                                                                | 12.1 ms: 1.14x slower                                                   |
| json_loads                 | 27.3 us                                                                | 31.2 us: 1.14x slower                                                   |
| pickle_pure_python         | 292 us                                                                 | 334 us: 1.15x slower                                                    |
| richards                   | 44.4 ms                                                                | 51.0 ms: 1.15x slower                                                   |
| sympy_str                  | 274 ms                                                                 | 316 ms: 1.15x slower                                                    |
| deltablue                  | 3.10 ms                                                                | 3.59 ms: 1.16x slower                                                   |
| xml_etree_process          | 59.2 ms                                                                | 68.8 ms: 1.16x slower                                                   |
| sympy_sum                  | 154 ms                                                                 | 180 ms: 1.16x slower                                                    |
| richards_super             | 50.4 ms                                                                | 58.7 ms: 1.16x slower                                                   |
| scimark_monte_carlo        | 65.8 ms                                                                | 76.9 ms: 1.17x slower                                                   |
| scimark_lu                 | 112 ms                                                                 | 131 ms: 1.17x slower                                                    |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.56 ms: 1.17x slower                                                   |
| sympy_expand               | 454 ms                                                                 | 531 ms: 1.17x slower                                                    |
| raytrace                   | 250 ms                                                                 | 294 ms: 1.18x slower                                                    |
| meteor_contest             | 101 ms                                                                 | 120 ms: 1.18x slower                                                    |
| django_template            | 34.2 ms                                                                | 40.6 ms: 1.19x slower                                                   |
| genshi_xml                 | 49.1 ms                                                                | 58.4 ms: 1.19x slower                                                   |
| typing_runtime_protocols   | 156 us                                                                 | 187 us: 1.20x slower                                                    |
| pprint_safe_repr           | 719 ms                                                                 | 866 ms: 1.20x slower                                                    |
| fannkuch                   | 376 ms                                                                 | 457 ms: 1.22x slower                                                    |
| genshi_text                | 21.7 ms                                                                | 26.5 ms: 1.22x slower                                                   |
| pprint_pformat             | 1.46 sec                                                               | 1.79 sec: 1.23x slower                                                  |
| logging_simple             | 6.14 us                                                                | 7.63 us: 1.24x slower                                                   |
| logging_format             | 6.92 us                                                                | 8.69 us: 1.26x slower                                                   |
| crypto_pyaes               | 68.2 ms                                                                | 85.8 ms: 1.26x slower                                                   |
| python_startup_no_site     | 7.41 ms                                                                | 9.54 ms: 1.29x slower                                                   |
| coverage                   | 82.5 ms                                                                | 112 ms: 1.35x slower                                                    |
| mako                       | 11.2 ms                                                                | 15.6 ms: 1.39x slower                                                   |
| nbody                      | 85.3 ms                                                                | 121 ms: 1.42x slower                                                    |
| python_startup             | 11.0 ms                                                                | 15.9 ms: 1.44x slower                                                   |
| bench_thread_pool          | 924 us                                                                 | 3.10 ms: 3.36x slower                                                   |
| logging_silent             | 98.2 ns                                                                | 528 ns: 5.37x slower                                                    |
| bench_mp_pool              | 11.0 ms                                                                | 102 ms: 9.27x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.08x slower                                                            |

Benchmark hidden because not significant (2): pylint, asyncio_websockets
Ignored benchmarks (18) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250605-3.15.0a0-04ccde3-NOGIL/bm-20250605-vultr-x86_64-nascheme-gh_132380_tp_getattr-3.15.0a0-04ccde3.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.020x slower

# HPT report

- Reliability score: 95.66% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.40x