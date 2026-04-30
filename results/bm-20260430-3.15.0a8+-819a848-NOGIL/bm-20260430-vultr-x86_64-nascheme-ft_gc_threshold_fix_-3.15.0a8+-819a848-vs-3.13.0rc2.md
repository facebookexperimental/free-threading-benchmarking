# Results vs. 3.13.0rc2

- fork: nascheme
- ref: ft_gc_threshold_fix_
- machine: linux-x86_64
- commit hash: 819a848
- commit date: 2026-04-30
- overall geometric mean: 1.054x slower
- HPT reliability: 85.16%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.38x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260430-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8+-819a848 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 289 ms: 1.11x slower                                                     |
| docutils       | 2.62 sec                                                     | 2.80 sec: 1.07x slower                                                   |
| html5lib       | 67.0 ms                                                      | 69.1 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                        | 1.07x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260430-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8+-819a848 |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 636 ms: 1.44x faster                                                     |
| async_tree_io              | 876 ms                                                       | 673 ms: 1.30x faster                                                     |
| async_tree_memoization     | 461 ms                                                       | 379 ms: 1.22x faster                                                     |
| async_tree_none_tg         | 336 ms                                                       | 285 ms: 1.18x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 566 ms: 1.18x faster                                                     |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 550 ms: 1.16x faster                                                     |
| async_tree_memoization_tg  | 414 ms                                                       | 359 ms: 1.15x faster                                                     |
| async_tree_none            | 354 ms                                                       | 323 ms: 1.10x faster                                                     |
| asyncio_websockets         | 520 ms                                                       | 508 ms: 1.02x faster                                                     |
| coroutines                 | 23.6 ms                                                      | 23.9 ms: 1.01x slower                                                    |
| Geometric mean             | (ref)                                                        | 1.15x faster                                                             |

Benchmark hidden because not significant (1): async_generators

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260430-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8+-819a848 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 180 ms: 1.20x faster                                                     |
| float          | 77.5 ms                                                      | 78.6 ms: 1.01x slower                                                    |
| nbody          | 85.1 ms                                                      | 123 ms: 1.45x slower                                                     |
| Geometric mean | (ref)                                                        | 1.07x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260430-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8+-819a848 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 22.7 ms                                                      | 22.0 ms: 1.03x faster                                                    |
| regex_effbot   | 3.08 ms                                                      | 3.05 ms: 1.01x faster                                                    |
| regex_dna      | 180 ms                                                       | 186 ms: 1.03x slower                                                     |
| regex_compile  | 132 ms                                                       | 143 ms: 1.08x slower                                                     |
| Geometric mean | (ref)                                                        | 1.02x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260430-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8+-819a848 |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 88.8 ms: 1.07x faster                                                    |
| tomli_loads          | 2.01 sec                                                     | 1.95 sec: 1.03x faster                                                   |
| xml_etree_parse      | 136 ms                                                       | 134 ms: 1.02x faster                                                     |
| json_dumps           | 10.5 ms                                                      | 10.8 ms: 1.03x slower                                                    |
| json_loads           | 27.0 us                                                      | 29.2 us: 1.08x slower                                                    |
| unpickle_pure_python | 210 us                                                       | 236 us: 1.12x slower                                                     |
| xml_etree_generate   | 85.4 ms                                                      | 96.0 ms: 1.12x slower                                                    |
| pickle_pure_python   | 294 us                                                       | 336 us: 1.14x slower                                                     |
| xml_etree_process    | 59.3 ms                                                      | 68.5 ms: 1.15x slower                                                    |
| Geometric mean       | (ref)                                                        | 1.06x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260430-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8+-819a848 |
|------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 8.78 ms: 1.19x slower                                                    |
| python_startup         | 11.0 ms                                                      | 15.3 ms: 1.39x slower                                                    |
| Geometric mean         | (ref)                                                        | 1.29x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260430-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8+-819a848 |
|-----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| django_template | 34.1 ms                                                      | 39.9 ms: 1.17x slower                                                    |
| mako            | 11.3 ms                                                      | 15.7 ms: 1.38x slower                                                    |
| Geometric mean  | (ref)                                                        | 1.27x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260430-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8+-819a848 |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pylint                     | 317 ms                                                       | 131 ms: 2.42x faster                                                     |
| mdp                        | 2.36 sec                                                     | 1.32 sec: 1.78x faster                                                   |
| gc_traversal               | 3.14 ms                                                      | 1.88 ms: 1.67x faster                                                    |
| bench_mp_pool              | 11.0 ms                                                      | 7.05 ms: 1.56x faster                                                    |
| async_tree_io_tg           | 913 ms                                                       | 636 ms: 1.44x faster                                                     |
| deepcopy                   | 355 us                                                       | 266 us: 1.33x faster                                                     |
| async_tree_io              | 876 ms                                                       | 673 ms: 1.30x faster                                                     |
| deepcopy_memo              | 39.1 us                                                      | 31.0 us: 1.26x faster                                                    |
| async_tree_memoization     | 461 ms                                                       | 379 ms: 1.22x faster                                                     |
| pidigits                   | 217 ms                                                       | 180 ms: 1.20x faster                                                     |
| async_tree_none_tg         | 336 ms                                                       | 285 ms: 1.18x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 566 ms: 1.18x faster                                                     |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 550 ms: 1.16x faster                                                     |
| go                         | 141 ms                                                       | 122 ms: 1.16x faster                                                     |
| async_tree_memoization_tg  | 414 ms                                                       | 359 ms: 1.15x faster                                                     |
| sqlite_synth               | 2.21 us                                                      | 1.92 us: 1.15x faster                                                    |
| scimark_sor                | 134 ms                                                       | 119 ms: 1.13x faster                                                     |
| async_tree_none            | 354 ms                                                       | 323 ms: 1.10x faster                                                     |
| pathlib                    | 19.2 ms                                                      | 17.6 ms: 1.09x faster                                                    |
| deepcopy_reduce            | 3.11 us                                                      | 2.89 us: 1.08x faster                                                    |
| xml_etree_iterparse        | 94.9 ms                                                      | 88.8 ms: 1.07x faster                                                    |
| dulwich_log                | 74.8 ms                                                      | 71.5 ms: 1.05x faster                                                    |
| scimark_fft                | 349 ms                                                       | 335 ms: 1.04x faster                                                     |
| regex_v8                   | 22.7 ms                                                      | 22.0 ms: 1.03x faster                                                    |
| tomli_loads                | 2.01 sec                                                     | 1.95 sec: 1.03x faster                                                   |
| spectral_norm              | 111 ms                                                       | 108 ms: 1.03x faster                                                     |
| asyncio_websockets         | 520 ms                                                       | 508 ms: 1.02x faster                                                     |
| bpe_tokeniser              | 4.45 sec                                                     | 4.35 sec: 1.02x faster                                                   |
| xml_etree_parse            | 136 ms                                                       | 134 ms: 1.02x faster                                                     |
| regex_effbot               | 3.08 ms                                                      | 3.05 ms: 1.01x faster                                                    |
| pycparser                  | 1.12 sec                                                     | 1.13 sec: 1.01x slower                                                   |
| coroutines                 | 23.6 ms                                                      | 23.9 ms: 1.01x slower                                                    |
| float                      | 77.5 ms                                                      | 78.6 ms: 1.01x slower                                                    |
| json                       | 4.93 ms                                                      | 5.05 ms: 1.02x slower                                                    |
| json_dumps                 | 10.5 ms                                                      | 10.8 ms: 1.03x slower                                                    |
| html5lib                   | 67.0 ms                                                      | 69.1 ms: 1.03x slower                                                    |
| regex_dna                  | 180 ms                                                       | 186 ms: 1.03x slower                                                     |
| comprehensions             | 16.5 us                                                      | 17.5 us: 1.06x slower                                                    |
| docutils                   | 2.62 sec                                                     | 2.80 sec: 1.07x slower                                                   |
| pprint_safe_repr           | 738 ms                                                       | 791 ms: 1.07x slower                                                     |
| create_gc_cycles           | 1.34 ms                                                      | 1.44 ms: 1.07x slower                                                    |
| regex_compile              | 132 ms                                                       | 143 ms: 1.08x slower                                                     |
| json_loads                 | 27.0 us                                                      | 29.2 us: 1.08x slower                                                    |
| chaos                      | 57.3 ms                                                      | 62.3 ms: 1.09x slower                                                    |
| pprint_pformat             | 1.50 sec                                                     | 1.63 sec: 1.09x slower                                                   |
| sympy_integrate            | 19.8 ms                                                      | 21.9 ms: 1.10x slower                                                    |
| hexiom                     | 5.99 ms                                                      | 6.62 ms: 1.10x slower                                                    |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.21 ms: 1.11x slower                                                    |
| scimark_lu                 | 113 ms                                                       | 125 ms: 1.11x slower                                                     |
| 2to3                       | 260 ms                                                       | 289 ms: 1.11x slower                                                     |
| nqueens                    | 78.6 ms                                                      | 88.1 ms: 1.12x slower                                                    |
| unpickle_pure_python       | 210 us                                                       | 236 us: 1.12x slower                                                     |
| xml_etree_generate         | 85.4 ms                                                      | 96.0 ms: 1.12x slower                                                    |
| logging_simple             | 6.16 us                                                      | 6.93 us: 1.13x slower                                                    |
| pickle_pure_python         | 294 us                                                       | 336 us: 1.14x slower                                                     |
| logging_format             | 6.84 us                                                      | 7.82 us: 1.14x slower                                                    |
| sympy_str                  | 275 ms                                                       | 315 ms: 1.15x slower                                                     |
| sympy_expand               | 457 ms                                                       | 527 ms: 1.15x slower                                                     |
| xml_etree_process          | 59.3 ms                                                      | 68.5 ms: 1.15x slower                                                    |
| sympy_sum                  | 156 ms                                                       | 180 ms: 1.16x slower                                                     |
| richards                   | 45.2 ms                                                      | 52.5 ms: 1.16x slower                                                    |
| richards_super             | 51.6 ms                                                      | 60.2 ms: 1.16x slower                                                    |
| thrift                     | 778 us                                                       | 909 us: 1.17x slower                                                     |
| django_template            | 34.1 ms                                                      | 39.9 ms: 1.17x slower                                                    |
| deltablue                  | 3.12 ms                                                      | 3.67 ms: 1.17x slower                                                    |
| generators                 | 28.8 ms                                                      | 34.1 ms: 1.18x slower                                                    |
| python_startup_no_site     | 7.39 ms                                                      | 8.78 ms: 1.19x slower                                                    |
| raytrace                   | 253 ms                                                       | 302 ms: 1.20x slower                                                     |
| scimark_monte_carlo        | 65.4 ms                                                      | 79.0 ms: 1.21x slower                                                    |
| fannkuch                   | 370 ms                                                       | 451 ms: 1.22x slower                                                     |
| meteor_contest             | 102 ms                                                       | 126 ms: 1.24x slower                                                     |
| typing_runtime_protocols   | 155 us                                                       | 194 us: 1.25x slower                                                     |
| crypto_pyaes               | 67.9 ms                                                      | 88.2 ms: 1.30x slower                                                    |
| coverage                   | 83.0 ms                                                      | 110 ms: 1.32x slower                                                     |
| mako                       | 11.3 ms                                                      | 15.7 ms: 1.38x slower                                                    |
| python_startup             | 11.0 ms                                                      | 15.3 ms: 1.39x slower                                                    |
| nbody                      | 85.1 ms                                                      | 123 ms: 1.45x slower                                                     |
| bench_thread_pool          | 919 us                                                       | 1.46 ms: 1.59x slower                                                    |
| telco                      | 7.82 ms                                                      | 176 ms: 22.51x slower                                                    |
| Geometric mean             | (ref)                                                        | 1.05x slower                                                             |

Benchmark hidden because not significant (3): async_generators, logging_silent, pyflate
Ignored benchmarks (20) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260430-3.15.0a8+-819a848-NOGIL/bm-20260430-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8+-819a848.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.054x slower

# HPT report

- Reliability score: 85.16% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.38x