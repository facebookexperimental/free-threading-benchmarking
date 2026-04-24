# Results vs. 3.13.0rc2

- fork: nascheme
- ref: ft_gc_threshold_fix_
- machine: linux-x86_64
- commit hash: ac09833
- commit date: 2026-04-23
- overall geometric mean: 1.054x slower
- HPT reliability: 89.64%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.41x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260423-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8+-ac09833 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 287 ms: 1.10x slower                                                     |
| docutils       | 2.62 sec                                                     | 2.76 sec: 1.05x slower                                                   |
| html5lib       | 67.0 ms                                                      | 68.9 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                        | 1.06x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260423-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8+-ac09833 |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 646 ms: 1.41x faster                                                     |
| async_tree_io              | 876 ms                                                       | 650 ms: 1.35x faster                                                     |
| async_tree_memoization     | 461 ms                                                       | 382 ms: 1.21x faster                                                     |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 545 ms: 1.17x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 570 ms: 1.17x faster                                                     |
| async_tree_memoization_tg  | 414 ms                                                       | 357 ms: 1.16x faster                                                     |
| async_tree_none_tg         | 336 ms                                                       | 293 ms: 1.15x faster                                                     |
| async_tree_none            | 354 ms                                                       | 309 ms: 1.15x faster                                                     |
| asyncio_websockets         | 520 ms                                                       | 513 ms: 1.01x faster                                                     |
| coroutines                 | 23.6 ms                                                      | 24.6 ms: 1.05x slower                                                    |
| Geometric mean             | (ref)                                                        | 1.15x faster                                                             |

Benchmark hidden because not significant (1): async_generators

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260423-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8+-ac09833 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 180 ms: 1.20x faster                                                     |
| float          | 77.5 ms                                                      | 77.9 ms: 1.01x slower                                                    |
| nbody          | 85.1 ms                                                      | 122 ms: 1.44x slower                                                     |
| Geometric mean | (ref)                                                        | 1.06x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260423-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8+-ac09833 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 22.7 ms                                                      | 21.5 ms: 1.06x faster                                                    |
| regex_effbot   | 3.08 ms                                                      | 3.06 ms: 1.01x faster                                                    |
| regex_dna      | 180 ms                                                       | 184 ms: 1.02x slower                                                     |
| regex_compile  | 132 ms                                                       | 141 ms: 1.07x slower                                                     |
| Geometric mean | (ref)                                                        | 1.01x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260423-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8+-ac09833 |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 87.1 ms: 1.09x faster                                                    |
| tomli_loads          | 2.01 sec                                                     | 1.92 sec: 1.05x faster                                                   |
| xml_etree_parse      | 136 ms                                                       | 134 ms: 1.02x faster                                                     |
| json_dumps           | 10.5 ms                                                      | 10.7 ms: 1.01x slower                                                    |
| xml_etree_generate   | 85.4 ms                                                      | 95.4 ms: 1.12x slower                                                    |
| json_loads           | 27.0 us                                                      | 30.4 us: 1.12x slower                                                    |
| unpickle_pure_python | 210 us                                                       | 237 us: 1.13x slower                                                     |
| pickle_pure_python   | 294 us                                                       | 336 us: 1.14x slower                                                     |
| xml_etree_process    | 59.3 ms                                                      | 68.2 ms: 1.15x slower                                                    |
| Geometric mean       | (ref)                                                        | 1.06x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260423-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8+-ac09833 |
|------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 8.95 ms: 1.21x slower                                                    |
| python_startup         | 11.0 ms                                                      | 15.5 ms: 1.41x slower                                                    |
| Geometric mean         | (ref)                                                        | 1.30x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260423-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8+-ac09833 |
|-----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 54.3 ms: 1.11x slower                                                    |
| django_template | 34.1 ms                                                      | 39.0 ms: 1.14x slower                                                    |
| genshi_text     | 21.5 ms                                                      | 25.7 ms: 1.19x slower                                                    |
| mako            | 11.3 ms                                                      | 15.5 ms: 1.37x slower                                                    |
| Geometric mean  | (ref)                                                        | 1.20x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260423-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8+-ac09833 |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pylint                     | 317 ms                                                       | 131 ms: 2.41x faster                                                     |
| mdp                        | 2.36 sec                                                     | 1.31 sec: 1.80x faster                                                   |
| gc_traversal               | 3.14 ms                                                      | 1.91 ms: 1.64x faster                                                    |
| bench_mp_pool              | 11.0 ms                                                      | 7.27 ms: 1.51x faster                                                    |
| async_tree_io_tg           | 913 ms                                                       | 646 ms: 1.41x faster                                                     |
| async_tree_io              | 876 ms                                                       | 650 ms: 1.35x faster                                                     |
| deepcopy                   | 355 us                                                       | 267 us: 1.33x faster                                                     |
| deepcopy_memo              | 39.1 us                                                      | 31.5 us: 1.24x faster                                                    |
| async_tree_memoization     | 461 ms                                                       | 382 ms: 1.21x faster                                                     |
| pidigits                   | 217 ms                                                       | 180 ms: 1.20x faster                                                     |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 545 ms: 1.17x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 570 ms: 1.17x faster                                                     |
| sqlite_synth               | 2.21 us                                                      | 1.90 us: 1.16x faster                                                    |
| go                         | 141 ms                                                       | 121 ms: 1.16x faster                                                     |
| async_tree_memoization_tg  | 414 ms                                                       | 357 ms: 1.16x faster                                                     |
| async_tree_none_tg         | 336 ms                                                       | 293 ms: 1.15x faster                                                     |
| async_tree_none            | 354 ms                                                       | 309 ms: 1.15x faster                                                     |
| scimark_sor                | 134 ms                                                       | 119 ms: 1.13x faster                                                     |
| xml_etree_iterparse        | 94.9 ms                                                      | 87.1 ms: 1.09x faster                                                    |
| pathlib                    | 19.2 ms                                                      | 17.7 ms: 1.08x faster                                                    |
| dulwich_log                | 74.8 ms                                                      | 69.6 ms: 1.07x faster                                                    |
| deepcopy_reduce            | 3.11 us                                                      | 2.91 us: 1.07x faster                                                    |
| regex_v8                   | 22.7 ms                                                      | 21.5 ms: 1.06x faster                                                    |
| tomli_loads                | 2.01 sec                                                     | 1.92 sec: 1.05x faster                                                   |
| scimark_fft                | 349 ms                                                       | 337 ms: 1.04x faster                                                     |
| bpe_tokeniser              | 4.45 sec                                                     | 4.32 sec: 1.03x faster                                                   |
| xml_etree_parse            | 136 ms                                                       | 134 ms: 1.02x faster                                                     |
| asyncio_websockets         | 520 ms                                                       | 513 ms: 1.01x faster                                                     |
| regex_effbot               | 3.08 ms                                                      | 3.06 ms: 1.01x faster                                                    |
| pycparser                  | 1.12 sec                                                     | 1.12 sec: 1.01x slower                                                   |
| float                      | 77.5 ms                                                      | 77.9 ms: 1.01x slower                                                    |
| pyflate                    | 449 ms                                                       | 454 ms: 1.01x slower                                                     |
| json_dumps                 | 10.5 ms                                                      | 10.7 ms: 1.01x slower                                                    |
| logging_silent             | 103 ns                                                       | 104 ns: 1.02x slower                                                     |
| regex_dna                  | 180 ms                                                       | 184 ms: 1.02x slower                                                     |
| html5lib                   | 67.0 ms                                                      | 68.9 ms: 1.03x slower                                                    |
| coroutines                 | 23.6 ms                                                      | 24.6 ms: 1.05x slower                                                    |
| docutils                   | 2.62 sec                                                     | 2.76 sec: 1.05x slower                                                   |
| json                       | 4.93 ms                                                      | 5.24 ms: 1.06x slower                                                    |
| comprehensions             | 16.5 us                                                      | 17.6 us: 1.07x slower                                                    |
| regex_compile              | 132 ms                                                       | 141 ms: 1.07x slower                                                     |
| hexiom                     | 5.99 ms                                                      | 6.49 ms: 1.08x slower                                                    |
| pprint_safe_repr           | 738 ms                                                       | 800 ms: 1.09x slower                                                     |
| chaos                      | 57.3 ms                                                      | 62.7 ms: 1.09x slower                                                    |
| scimark_lu                 | 113 ms                                                       | 123 ms: 1.10x slower                                                     |
| nqueens                    | 78.6 ms                                                      | 86.3 ms: 1.10x slower                                                    |
| logging_simple             | 6.16 us                                                      | 6.76 us: 1.10x slower                                                    |
| sympy_integrate            | 19.8 ms                                                      | 21.8 ms: 1.10x slower                                                    |
| 2to3                       | 260 ms                                                       | 287 ms: 1.10x slower                                                     |
| pprint_pformat             | 1.50 sec                                                     | 1.66 sec: 1.11x slower                                                   |
| generators                 | 28.8 ms                                                      | 32.0 ms: 1.11x slower                                                    |
| genshi_xml                 | 48.8 ms                                                      | 54.3 ms: 1.11x slower                                                    |
| create_gc_cycles           | 1.34 ms                                                      | 1.49 ms: 1.11x slower                                                    |
| xml_etree_generate         | 85.4 ms                                                      | 95.4 ms: 1.12x slower                                                    |
| json_loads                 | 27.0 us                                                      | 30.4 us: 1.12x slower                                                    |
| logging_format             | 6.84 us                                                      | 7.70 us: 1.13x slower                                                    |
| unpickle_pure_python       | 210 us                                                       | 237 us: 1.13x slower                                                     |
| sympy_sum                  | 156 ms                                                       | 176 ms: 1.13x slower                                                     |
| sympy_str                  | 275 ms                                                       | 312 ms: 1.14x slower                                                     |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.36 ms: 1.14x slower                                                    |
| sympy_expand               | 457 ms                                                       | 520 ms: 1.14x slower                                                     |
| pickle_pure_python         | 294 us                                                       | 336 us: 1.14x slower                                                     |
| django_template            | 34.1 ms                                                      | 39.0 ms: 1.14x slower                                                    |
| thrift                     | 778 us                                                       | 893 us: 1.15x slower                                                     |
| xml_etree_process          | 59.3 ms                                                      | 68.2 ms: 1.15x slower                                                    |
| richards_super             | 51.6 ms                                                      | 59.5 ms: 1.15x slower                                                    |
| deltablue                  | 3.12 ms                                                      | 3.64 ms: 1.16x slower                                                    |
| richards                   | 45.2 ms                                                      | 52.7 ms: 1.17x slower                                                    |
| scimark_monte_carlo        | 65.4 ms                                                      | 77.4 ms: 1.18x slower                                                    |
| genshi_text                | 21.5 ms                                                      | 25.7 ms: 1.19x slower                                                    |
| raytrace                   | 253 ms                                                       | 303 ms: 1.20x slower                                                     |
| python_startup_no_site     | 7.39 ms                                                      | 8.95 ms: 1.21x slower                                                    |
| fannkuch                   | 370 ms                                                       | 458 ms: 1.24x slower                                                     |
| meteor_contest             | 102 ms                                                       | 127 ms: 1.25x slower                                                     |
| typing_runtime_protocols   | 155 us                                                       | 194 us: 1.26x slower                                                     |
| crypto_pyaes               | 67.9 ms                                                      | 87.1 ms: 1.28x slower                                                    |
| coverage                   | 83.0 ms                                                      | 110 ms: 1.32x slower                                                     |
| mako                       | 11.3 ms                                                      | 15.5 ms: 1.37x slower                                                    |
| python_startup             | 11.0 ms                                                      | 15.5 ms: 1.41x slower                                                    |
| nbody                      | 85.1 ms                                                      | 122 ms: 1.44x slower                                                     |
| bench_thread_pool          | 919 us                                                       | 1.46 ms: 1.59x slower                                                    |
| telco                      | 7.82 ms                                                      | 172 ms: 22.01x slower                                                    |
| Geometric mean             | (ref)                                                        | 1.05x slower                                                             |

Benchmark hidden because not significant (2): spectral_norm, async_generators
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260423-3.15.0a8+-ac09833-NOGIL/bm-20260423-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8+-ac09833.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.054x slower

# HPT report

- Reliability score: 89.64% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.41x