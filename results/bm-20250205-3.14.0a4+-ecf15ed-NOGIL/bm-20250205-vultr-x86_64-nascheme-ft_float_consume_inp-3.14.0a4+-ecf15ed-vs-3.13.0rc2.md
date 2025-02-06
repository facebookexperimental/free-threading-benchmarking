# Results vs. 3.13.0rc2

- fork: nascheme
- ref: ft_float_consume_inp
- machine: linux-x86_64
- commit hash: ecf15ed
- commit date: 2025-02-05
- overall geometric mean: 1.075x slower
- HPT reliability: 99.97%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250205-vultr-x86_64-nascheme-ft_float_consume_inp-3.14.0a4+-ecf15ed |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 302 ms: 1.16x slower                                                     |
| docutils       | 2.62 sec                                                     | 2.80 sec: 1.07x slower                                                   |
| html5lib       | 67.0 ms                                                      | 71.8 ms: 1.07x slower                                                    |
| Geometric mean | (ref)                                                        | 1.10x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250205-vultr-x86_64-nascheme-ft_float_consume_inp-3.14.0a4+-ecf15ed |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 575 ms: 1.59x faster                                                     |
| async_tree_io              | 876 ms                                                       | 603 ms: 1.45x faster                                                     |
| async_tree_none_tg         | 336 ms                                                       | 248 ms: 1.36x faster                                                     |
| async_tree_memoization     | 461 ms                                                       | 348 ms: 1.32x faster                                                     |
| async_tree_memoization_tg  | 414 ms                                                       | 319 ms: 1.30x faster                                                     |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 504 ms: 1.26x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 533 ms: 1.25x faster                                                     |
| async_tree_none            | 354 ms                                                       | 284 ms: 1.25x faster                                                     |
| async_generators           | 377 ms                                                       | 370 ms: 1.02x faster                                                     |
| asyncio_websockets         | 520 ms                                                       | 515 ms: 1.01x faster                                                     |
| coroutines                 | 23.6 ms                                                      | 23.5 ms: 1.00x faster                                                    |
| Geometric mean             | (ref)                                                        | 1.24x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250205-vultr-x86_64-nascheme-ft_float_consume_inp-3.14.0a4+-ecf15ed |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 198 ms: 1.09x faster                                                     |
| float          | 77.5 ms                                                      | 76.2 ms: 1.02x faster                                                    |
| nbody          | 85.1 ms                                                      | 130 ms: 1.53x slower                                                     |
| Geometric mean | (ref)                                                        | 1.11x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250205-vultr-x86_64-nascheme-ft_float_consume_inp-3.14.0a4+-ecf15ed |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.79 ms: 1.10x faster                                                    |
| regex_dna      | 180 ms                                                       | 182 ms: 1.01x slower                                                     |
| regex_v8       | 22.7 ms                                                      | 24.0 ms: 1.06x slower                                                    |
| regex_compile  | 132 ms                                                       | 150 ms: 1.13x slower                                                     |
| Geometric mean | (ref)                                                        | 1.02x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250205-vultr-x86_64-nascheme-ft_float_consume_inp-3.14.0a4+-ecf15ed |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 88.0 ms: 1.08x faster                                                    |
| xml_etree_parse      | 136 ms                                                       | 128 ms: 1.06x faster                                                     |
| xml_etree_generate   | 85.4 ms                                                      | 96.1 ms: 1.12x slower                                                    |
| xml_etree_process    | 59.3 ms                                                      | 68.4 ms: 1.15x slower                                                    |
| json_loads           | 27.0 us                                                      | 31.2 us: 1.15x slower                                                    |
| tomli_loads          | 2.01 sec                                                     | 2.34 sec: 1.16x slower                                                   |
| unpickle_pure_python | 210 us                                                       | 246 us: 1.17x slower                                                     |
| json_dumps           | 10.5 ms                                                      | 13.1 ms: 1.24x slower                                                    |
| pickle_pure_python   | 294 us                                                       | 367 us: 1.25x slower                                                     |
| Geometric mean       | (ref)                                                        | 1.12x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250205-vultr-x86_64-nascheme-ft_float_consume_inp-3.14.0a4+-ecf15ed |
|------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.68 ms: 1.31x slower                                                    |
| python_startup         | 11.0 ms                                                      | 15.4 ms: 1.40x slower                                                    |
| Geometric mean         | (ref)                                                        | 1.35x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250205-vultr-x86_64-nascheme-ft_float_consume_inp-3.14.0a4+-ecf15ed |
|-----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 58.9 ms: 1.21x slower                                                    |
| django_template | 34.1 ms                                                      | 42.7 ms: 1.25x slower                                                    |
| genshi_text     | 21.5 ms                                                      | 27.8 ms: 1.29x slower                                                    |
| mako            | 11.3 ms                                                      | 16.0 ms: 1.41x slower                                                    |
| Geometric mean  | (ref)                                                        | 1.29x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250205-vultr-x86_64-nascheme-ft_float_consume_inp-3.14.0a4+-ecf15ed |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal               | 3.14 ms                                                      | 1.67 ms: 1.88x faster                                                    |
| async_tree_io_tg           | 913 ms                                                       | 575 ms: 1.59x faster                                                     |
| async_tree_io              | 876 ms                                                       | 603 ms: 1.45x faster                                                     |
| async_tree_none_tg         | 336 ms                                                       | 248 ms: 1.36x faster                                                     |
| async_tree_memoization     | 461 ms                                                       | 348 ms: 1.32x faster                                                     |
| async_tree_memoization_tg  | 414 ms                                                       | 319 ms: 1.30x faster                                                     |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 504 ms: 1.26x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 533 ms: 1.25x faster                                                     |
| async_tree_none            | 354 ms                                                       | 284 ms: 1.25x faster                                                     |
| deepcopy                   | 355 us                                                       | 310 us: 1.15x faster                                                     |
| regex_effbot               | 3.08 ms                                                      | 2.79 ms: 1.10x faster                                                    |
| pidigits                   | 217 ms                                                       | 198 ms: 1.09x faster                                                     |
| sqlite_synth               | 2.21 us                                                      | 2.03 us: 1.09x faster                                                    |
| xml_etree_iterparse        | 94.9 ms                                                      | 88.0 ms: 1.08x faster                                                    |
| xml_etree_parse            | 136 ms                                                       | 128 ms: 1.06x faster                                                     |
| spectral_norm              | 111 ms                                                       | 105 ms: 1.05x faster                                                     |
| deepcopy_memo              | 39.1 us                                                      | 37.5 us: 1.04x faster                                                    |
| scimark_sor                | 134 ms                                                       | 131 ms: 1.03x faster                                                     |
| pathlib                    | 19.2 ms                                                      | 18.7 ms: 1.03x faster                                                    |
| async_generators           | 377 ms                                                       | 370 ms: 1.02x faster                                                     |
| float                      | 77.5 ms                                                      | 76.2 ms: 1.02x faster                                                    |
| go                         | 141 ms                                                       | 139 ms: 1.02x faster                                                     |
| asyncio_websockets         | 520 ms                                                       | 515 ms: 1.01x faster                                                     |
| coroutines                 | 23.6 ms                                                      | 23.5 ms: 1.00x faster                                                    |
| regex_dna                  | 180 ms                                                       | 182 ms: 1.01x slower                                                     |
| deepcopy_reduce            | 3.11 us                                                      | 3.15 us: 1.01x slower                                                    |
| pycparser                  | 1.12 sec                                                     | 1.17 sec: 1.04x slower                                                   |
| create_gc_cycles           | 1.34 ms                                                      | 1.40 ms: 1.05x slower                                                    |
| bpe_tokeniser              | 4.45 sec                                                     | 4.67 sec: 1.05x slower                                                   |
| regex_v8                   | 22.7 ms                                                      | 24.0 ms: 1.06x slower                                                    |
| html5lib                   | 67.0 ms                                                      | 71.8 ms: 1.07x slower                                                    |
| docutils                   | 2.62 sec                                                     | 2.80 sec: 1.07x slower                                                   |
| scimark_fft                | 349 ms                                                       | 380 ms: 1.09x slower                                                     |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.13 ms: 1.09x slower                                                    |
| dulwich_log                | 74.8 ms                                                      | 81.6 ms: 1.09x slower                                                    |
| telco                      | 7.82 ms                                                      | 8.57 ms: 1.10x slower                                                    |
| json                       | 4.93 ms                                                      | 5.40 ms: 1.10x slower                                                    |
| pprint_safe_repr           | 738 ms                                                       | 808 ms: 1.10x slower                                                     |
| pprint_pformat             | 1.50 sec                                                     | 1.67 sec: 1.11x slower                                                   |
| generators                 | 28.8 ms                                                      | 32.1 ms: 1.11x slower                                                    |
| logging_silent             | 103 ns                                                       | 115 ns: 1.12x slower                                                     |
| xml_etree_generate         | 85.4 ms                                                      | 96.1 ms: 1.12x slower                                                    |
| regex_compile              | 132 ms                                                       | 150 ms: 1.13x slower                                                     |
| sqlglot_normalize          | 106 ms                                                       | 120 ms: 1.13x slower                                                     |
| pyflate                    | 449 ms                                                       | 512 ms: 1.14x slower                                                     |
| mdp                        | 2.36 sec                                                     | 2.69 sec: 1.14x slower                                                   |
| thrift                     | 778 us                                                       | 891 us: 1.15x slower                                                     |
| xml_etree_process          | 59.3 ms                                                      | 68.4 ms: 1.15x slower                                                    |
| json_loads                 | 27.0 us                                                      | 31.2 us: 1.15x slower                                                    |
| sqlglot_optimize           | 52.7 ms                                                      | 61.0 ms: 1.16x slower                                                    |
| 2to3                       | 260 ms                                                       | 302 ms: 1.16x slower                                                     |
| tomli_loads                | 2.01 sec                                                     | 2.34 sec: 1.16x slower                                                   |
| unpickle_pure_python       | 210 us                                                       | 246 us: 1.17x slower                                                     |
| coverage                   | 83.0 ms                                                      | 97.5 ms: 1.18x slower                                                    |
| logging_simple             | 6.16 us                                                      | 7.28 us: 1.18x slower                                                    |
| scimark_lu                 | 113 ms                                                       | 135 ms: 1.20x slower                                                     |
| sympy_sum                  | 156 ms                                                       | 187 ms: 1.20x slower                                                     |
| sympy_expand               | 457 ms                                                       | 549 ms: 1.20x slower                                                     |
| comprehensions             | 16.5 us                                                      | 19.8 us: 1.20x slower                                                    |
| sympy_integrate            | 19.8 ms                                                      | 23.9 ms: 1.21x slower                                                    |
| genshi_xml                 | 48.8 ms                                                      | 58.9 ms: 1.21x slower                                                    |
| chaos                      | 57.3 ms                                                      | 69.4 ms: 1.21x slower                                                    |
| logging_format             | 6.84 us                                                      | 8.30 us: 1.21x slower                                                    |
| sympy_str                  | 275 ms                                                       | 335 ms: 1.22x slower                                                     |
| sqlglot_transpile          | 1.56 ms                                                      | 1.91 ms: 1.22x slower                                                    |
| nqueens                    | 78.6 ms                                                      | 96.5 ms: 1.23x slower                                                    |
| hexiom                     | 5.99 ms                                                      | 7.37 ms: 1.23x slower                                                    |
| json_dumps                 | 10.5 ms                                                      | 13.1 ms: 1.24x slower                                                    |
| pickle_pure_python         | 294 us                                                       | 367 us: 1.25x slower                                                     |
| django_template            | 34.1 ms                                                      | 42.7 ms: 1.25x slower                                                    |
| richards                   | 45.2 ms                                                      | 56.6 ms: 1.25x slower                                                    |
| scimark_monte_carlo        | 65.4 ms                                                      | 81.9 ms: 1.25x slower                                                    |
| sqlglot_parse              | 1.25 ms                                                      | 1.58 ms: 1.27x slower                                                    |
| richards_super             | 51.6 ms                                                      | 65.8 ms: 1.27x slower                                                    |
| meteor_contest             | 102 ms                                                       | 130 ms: 1.28x slower                                                     |
| raytrace                   | 253 ms                                                       | 325 ms: 1.29x slower                                                     |
| genshi_text                | 21.5 ms                                                      | 27.8 ms: 1.29x slower                                                    |
| typing_runtime_protocols   | 155 us                                                       | 200 us: 1.29x slower                                                     |
| python_startup_no_site     | 7.39 ms                                                      | 9.68 ms: 1.31x slower                                                    |
| crypto_pyaes               | 67.9 ms                                                      | 89.4 ms: 1.32x slower                                                    |
| fannkuch                   | 370 ms                                                       | 491 ms: 1.33x slower                                                     |
| python_startup             | 11.0 ms                                                      | 15.4 ms: 1.40x slower                                                    |
| mako                       | 11.3 ms                                                      | 16.0 ms: 1.41x slower                                                    |
| deltablue                  | 3.12 ms                                                      | 4.72 ms: 1.51x slower                                                    |
| nbody                      | 85.1 ms                                                      | 130 ms: 1.53x slower                                                     |
| bench_thread_pool          | 919 us                                                       | 3.32 ms: 3.61x slower                                                    |
| bench_mp_pool              | 11.0 ms                                                      | 93.7 ms: 8.52x slower                                                    |
| Geometric mean             | (ref)                                                        | 1.12x slower                                                             |

Benchmark hidden because not significant (1): pylint
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250205-3.14.0a4+-ecf15ed-NOGIL/bm-20250205-vultr-x86_64-nascheme-ft_float_consume_inp-3.14.0a4+-ecf15ed.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.075x slower

# HPT report

- Reliability score: 99.97% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.34x