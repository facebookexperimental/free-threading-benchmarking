# Results vs. 3.13.0rc2

- fork: python
- ref: 47b01da4ccedd9c00fad
- machine: linux-x86_64
- commit hash: 47b01da
- commit date: 2025-07-12
- overall geometric mean: 1.049x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 254 ms: 1.02x faster                                                  |
| docutils       | 2.62 sec                                                     | 2.60 sec: 1.01x faster                                                |
| html5lib       | 67.0 ms                                                      | 61.4 ms: 1.09x faster                                                 |
| Geometric mean | (ref)                                                        | 1.04x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 620 ms: 1.47x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 316 ms: 1.46x faster                                                  |
| async_tree_io              | 876 ms                                                       | 601 ms: 1.46x faster                                                  |
| async_tree_none            | 354 ms                                                       | 257 ms: 1.38x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 505 ms: 1.32x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 255 ms: 1.32x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 315 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 514 ms: 1.24x faster                                                  |
| async_generators           | 377 ms                                                       | 355 ms: 1.06x faster                                                  |
| asyncio_tcp                | 505 ms                                                       | 501 ms: 1.01x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 518 ms: 1.00x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 23.7 ms: 1.01x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.22x faster                                                          |

Benchmark hidden because not significant (1): asyncio_tcp_ssl

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 64.5 ms: 1.20x faster                                                 |
| pidigits       | 217 ms                                                       | 210 ms: 1.03x faster                                                  |
| nbody          | 85.1 ms                                                      | 88.5 ms: 1.04x slower                                                 |
| Geometric mean | (ref)                                                        | 1.06x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.76 ms: 1.12x faster                                                 |
| regex_compile  | 132 ms                                                       | 124 ms: 1.06x faster                                                  |
| regex_v8       | 22.7 ms                                                      | 22.3 ms: 1.02x faster                                                 |
| Geometric mean | (ref)                                                        | 1.05x faster                                                          |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                     | 1.75 sec: 1.15x faster                                                |
| unpickle_pure_python | 210 us                                                       | 187 us: 1.12x faster                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 77.9 ms: 1.10x faster                                                 |
| xml_etree_process    | 59.3 ms                                                      | 54.3 ms: 1.09x faster                                                 |
| xml_etree_parse      | 136 ms                                                       | 130 ms: 1.05x faster                                                  |
| xml_etree_iterparse  | 94.9 ms                                                      | 92.5 ms: 1.03x faster                                                 |
| pickle_dict          | 32.5 us                                                      | 32.6 us: 1.00x slower                                                 |
| json_dumps           | 10.5 ms                                                      | 10.7 ms: 1.02x slower                                                 |
| pickle_pure_python   | 294 us                                                       | 306 us: 1.04x slower                                                  |
| json_loads           | 27.0 us                                                      | 28.2 us: 1.04x slower                                                 |
| unpickle_list        | 4.71 us                                                      | 4.94 us: 1.05x slower                                                 |
| pickle_list          | 4.93 us                                                      | 5.19 us: 1.05x slower                                                 |
| pickle               | 11.3 us                                                      | 12.4 us: 1.09x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.02x faster                                                          |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.35 ms: 1.01x faster                                                 |
| python_startup         | 11.0 ms                                                      | 12.6 ms: 1.15x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.07x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 11.3 ms                                                      | 10.7 ms: 1.06x faster                                                 |
| genshi_text     | 21.5 ms                                                      | 20.8 ms: 1.04x faster                                                 |
| genshi_xml      | 48.8 ms                                                      | 49.0 ms: 1.00x slower                                                 |
| django_template | 34.1 ms                                                      | 34.5 ms: 1.01x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.02x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.16 sec: 2.03x faster                                                |
| richards_super             | 51.6 ms                                                      | 34.4 ms: 1.50x faster                                                 |
| richards                   | 45.2 ms                                                      | 30.3 ms: 1.49x faster                                                 |
| async_tree_io_tg           | 913 ms                                                       | 620 ms: 1.47x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 316 ms: 1.46x faster                                                  |
| async_tree_io              | 876 ms                                                       | 601 ms: 1.46x faster                                                  |
| deepcopy                   | 355 us                                                       | 255 us: 1.39x faster                                                  |
| async_tree_none            | 354 ms                                                       | 257 ms: 1.38x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 29.5 us: 1.33x faster                                                 |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 505 ms: 1.32x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 255 ms: 1.32x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 315 ms: 1.32x faster                                                  |
| spectral_norm              | 111 ms                                                       | 85.0 ms: 1.31x faster                                                 |
| go                         | 141 ms                                                       | 110 ms: 1.27x faster                                                  |
| scimark_sor                | 134 ms                                                       | 108 ms: 1.25x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 514 ms: 1.24x faster                                                  |
| scimark_fft                | 349 ms                                                       | 286 ms: 1.22x faster                                                  |
| float                      | 77.5 ms                                                      | 64.5 ms: 1.20x faster                                                 |
| pyflate                    | 449 ms                                                       | 381 ms: 1.18x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 2.70 us: 1.15x faster                                                 |
| tomli_loads                | 2.01 sec                                                     | 1.75 sec: 1.15x faster                                                |
| unpickle_pure_python       | 210 us                                                       | 187 us: 1.12x faster                                                  |
| pylint                     | 317 ms                                                       | 283 ms: 1.12x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.76 ms: 1.12x faster                                                 |
| scimark_monte_carlo        | 65.4 ms                                                      | 58.7 ms: 1.11x faster                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 4.00 sec: 1.11x faster                                                |
| dulwich_log                | 74.8 ms                                                      | 67.7 ms: 1.10x faster                                                 |
| xml_etree_generate         | 85.4 ms                                                      | 77.9 ms: 1.10x faster                                                 |
| deltablue                  | 3.12 ms                                                      | 2.85 ms: 1.09x faster                                                 |
| xml_etree_process          | 59.3 ms                                                      | 54.3 ms: 1.09x faster                                                 |
| html5lib                   | 67.0 ms                                                      | 61.4 ms: 1.09x faster                                                 |
| pprint_pformat             | 1.50 sec                                                     | 1.40 sec: 1.07x faster                                                |
| regex_compile              | 132 ms                                                       | 124 ms: 1.06x faster                                                  |
| async_generators           | 377 ms                                                       | 355 ms: 1.06x faster                                                  |
| mako                       | 11.3 ms                                                      | 10.7 ms: 1.06x faster                                                 |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.47 ms: 1.05x faster                                                 |
| pprint_safe_repr           | 738 ms                                                       | 701 ms: 1.05x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 130 ms: 1.05x faster                                                  |
| generators                 | 28.8 ms                                                      | 27.5 ms: 1.05x faster                                                 |
| logging_simple             | 6.16 us                                                      | 5.89 us: 1.05x faster                                                 |
| meteor_contest             | 102 ms                                                       | 98.0 ms: 1.04x faster                                                 |
| genshi_text                | 21.5 ms                                                      | 20.8 ms: 1.04x faster                                                 |
| logging_format             | 6.84 us                                                      | 6.61 us: 1.03x faster                                                 |
| sympy_integrate            | 19.8 ms                                                      | 19.2 ms: 1.03x faster                                                 |
| pidigits                   | 217 ms                                                       | 210 ms: 1.03x faster                                                  |
| thrift                     | 778 us                                                       | 758 us: 1.03x faster                                                  |
| xml_etree_iterparse        | 94.9 ms                                                      | 92.5 ms: 1.03x faster                                                 |
| hexiom                     | 5.99 ms                                                      | 5.86 ms: 1.02x faster                                                 |
| coverage                   | 83.0 ms                                                      | 81.1 ms: 1.02x faster                                                 |
| 2to3                       | 260 ms                                                       | 254 ms: 1.02x faster                                                  |
| fannkuch                   | 370 ms                                                       | 363 ms: 1.02x faster                                                  |
| regex_v8                   | 22.7 ms                                                      | 22.3 ms: 1.02x faster                                                 |
| scimark_lu                 | 113 ms                                                       | 111 ms: 1.01x faster                                                  |
| sqlite_synth               | 2.21 us                                                      | 2.18 us: 1.01x faster                                                 |
| comprehensions             | 16.5 us                                                      | 16.2 us: 1.01x faster                                                 |
| logging_silent             | 103 ns                                                       | 101 ns: 1.01x faster                                                  |
| chaos                      | 57.3 ms                                                      | 56.7 ms: 1.01x faster                                                 |
| nqueens                    | 78.6 ms                                                      | 77.8 ms: 1.01x faster                                                 |
| asyncio_tcp                | 505 ms                                                       | 501 ms: 1.01x faster                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 7.35 ms: 1.01x faster                                                 |
| docutils                   | 2.62 sec                                                     | 2.60 sec: 1.01x faster                                                |
| sympy_str                  | 275 ms                                                       | 273 ms: 1.01x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 518 ms: 1.00x faster                                                  |
| pickle_dict                | 32.5 us                                                      | 32.6 us: 1.00x slower                                                 |
| genshi_xml                 | 48.8 ms                                                      | 49.0 ms: 1.00x slower                                                 |
| pycparser                  | 1.12 sec                                                     | 1.12 sec: 1.01x slower                                                |
| coroutines                 | 23.6 ms                                                      | 23.7 ms: 1.01x slower                                                 |
| pathlib                    | 19.2 ms                                                      | 19.3 ms: 1.01x slower                                                 |
| raytrace                   | 253 ms                                                       | 254 ms: 1.01x slower                                                  |
| django_template            | 34.1 ms                                                      | 34.5 ms: 1.01x slower                                                 |
| json_dumps                 | 10.5 ms                                                      | 10.7 ms: 1.02x slower                                                 |
| json                       | 4.93 ms                                                      | 5.08 ms: 1.03x slower                                                 |
| sympy_expand               | 457 ms                                                       | 474 ms: 1.04x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 306 us: 1.04x slower                                                  |
| nbody                      | 85.1 ms                                                      | 88.5 ms: 1.04x slower                                                 |
| json_loads                 | 27.0 us                                                      | 28.2 us: 1.04x slower                                                 |
| unpickle_list              | 4.71 us                                                      | 4.94 us: 1.05x slower                                                 |
| pickle_list                | 4.93 us                                                      | 5.19 us: 1.05x slower                                                 |
| unpack_sequence            | 44.8 ns                                                      | 48.2 ns: 1.08x slower                                                 |
| pickle                     | 11.3 us                                                      | 12.4 us: 1.09x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 1.05 ms: 1.15x slower                                                 |
| python_startup             | 11.0 ms                                                      | 12.6 ms: 1.15x slower                                                 |
| gc_traversal               | 3.14 ms                                                      | 4.59 ms: 1.46x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.96 ms: 1.47x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 103 ms: 9.33x slower                                                  |
| telco                      | 7.82 ms                                                      | 158 ms: 20.17x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.01x faster                                                          |

Benchmark hidden because not significant (6): unpickle, crypto_pyaes, typing_runtime_protocols, regex_dna, sympy_sum, asyncio_tcp_ssl
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20250712-3.15.0a0-47b01da-JIT/bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.049x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.16x