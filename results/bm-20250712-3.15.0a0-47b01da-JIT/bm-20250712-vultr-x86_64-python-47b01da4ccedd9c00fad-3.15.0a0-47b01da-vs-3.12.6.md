# Results vs. 3.12.6

- fork: python
- ref: 47b01da4ccedd9c00fad
- machine: linux-x86_64
- commit hash: 47b01da
- commit date: 2025-07-12
- overall geometric mean: 1.085x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 254 ms: 1.04x faster                                                  |
| docutils       | 2.64 sec                                               | 2.60 sec: 1.01x faster                                                |
| html5lib       | 63.6 ms                                                | 61.4 ms: 1.03x faster                                                 |
| Geometric mean | (ref)                                                  | 1.03x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none            | 464 ms                                                 | 257 ms: 1.81x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 601 ms: 1.80x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 620 ms: 1.79x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 315 ms: 1.78x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 316 ms: 1.76x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 255 ms: 1.75x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 505 ms: 1.41x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 514 ms: 1.41x faster                                                  |
| async_generators           | 384 ms                                                 | 355 ms: 1.08x faster                                                  |
| asyncio_tcp                | 519 ms                                                 | 501 ms: 1.04x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.7 ms: 1.01x faster                                                 |
| asyncio_websockets         | 517 ms                                                 | 518 ms: 1.00x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.39x faster                                                          |

Benchmark hidden because not significant (1): asyncio_tcp_ssl

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 64.5 ms: 1.25x faster                                                 |
| pidigits       | 184 ms                                                 | 210 ms: 1.14x slower                                                  |
| Geometric mean | (ref)                                                  | 1.04x faster                                                          |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.76 ms: 1.15x faster                                                 |
| regex_compile  | 142 ms                                                 | 124 ms: 1.15x faster                                                  |
| regex_dna      | 168 ms                                                 | 180 ms: 1.07x slower                                                  |
| regex_v8       | 20.6 ms                                                | 22.3 ms: 1.08x slower                                                 |
| Geometric mean | (ref)                                                  | 1.03x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.75 sec: 1.21x faster                                                |
| unpickle_pure_python | 221 us                                                 | 187 us: 1.18x faster                                                  |
| xml_etree_generate   | 85.2 ms                                                | 77.9 ms: 1.09x faster                                                 |
| xml_etree_process    | 59.0 ms                                                | 54.3 ms: 1.09x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.07x faster                                                  |
| xml_etree_iterparse  | 96.7 ms                                                | 92.5 ms: 1.05x faster                                                 |
| pickle_pure_python   | 308 us                                                 | 306 us: 1.01x faster                                                  |
| unpickle             | 14.1 us                                                | 14.2 us: 1.01x slower                                                 |
| pickle_dict          | 31.8 us                                                | 32.6 us: 1.03x slower                                                 |
| json_dumps           | 10.4 ms                                                | 10.7 ms: 1.04x slower                                                 |
| unpickle_list        | 4.67 us                                                | 4.94 us: 1.06x slower                                                 |
| json_loads           | 26.5 us                                                | 28.2 us: 1.06x slower                                                 |
| pickle_list          | 4.77 us                                                | 5.19 us: 1.09x slower                                                 |
| pickle               | 10.9 us                                                | 12.4 us: 1.13x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.35 ms: 1.03x slower                                                 |
| python_startup         | 9.93 ms                                                | 12.6 ms: 1.27x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.14x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 20.8 ms: 1.10x faster                                                 |
| mako            | 11.0 ms                                                | 10.7 ms: 1.03x faster                                                 |
| genshi_xml      | 50.2 ms                                                | 49.0 ms: 1.02x faster                                                 |
| django_template | 34.7 ms                                                | 34.5 ms: 1.01x faster                                                 |
| Geometric mean  | (ref)                                                  | 1.04x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.16 sec: 2.09x faster                                                |
| async_tree_none            | 464 ms                                                 | 257 ms: 1.81x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 601 ms: 1.80x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 620 ms: 1.79x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 315 ms: 1.78x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 316 ms: 1.76x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 255 ms: 1.75x faster                                                  |
| richards                   | 45.9 ms                                                | 30.3 ms: 1.52x faster                                                 |
| richards_super             | 51.9 ms                                                | 34.4 ms: 1.51x faster                                                 |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 505 ms: 1.41x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 514 ms: 1.41x faster                                                  |
| deepcopy                   | 352 us                                                 | 255 us: 1.38x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 29.5 us: 1.37x faster                                                 |
| spectral_norm              | 110 ms                                                 | 85.0 ms: 1.30x faster                                                 |
| go                         | 139 ms                                                 | 110 ms: 1.26x faster                                                  |
| float                      | 80.8 ms                                                | 64.5 ms: 1.25x faster                                                 |
| comprehensions             | 19.8 us                                                | 16.2 us: 1.22x faster                                                 |
| deltablue                  | 3.45 ms                                                | 2.85 ms: 1.21x faster                                                 |
| tomli_loads                | 2.11 sec                                               | 1.75 sec: 1.21x faster                                                |
| scimark_sor                | 130 ms                                                 | 108 ms: 1.20x faster                                                  |
| scimark_fft                | 342 ms                                                 | 286 ms: 1.20x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.00 sec: 1.18x faster                                                |
| unpickle_pure_python       | 221 us                                                 | 187 us: 1.18x faster                                                  |
| raytrace                   | 299 ms                                                 | 254 ms: 1.18x faster                                                  |
| pyflate                    | 448 ms                                                 | 381 ms: 1.18x faster                                                  |
| generators                 | 32.2 ms                                                | 27.5 ms: 1.17x faster                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 58.7 ms: 1.17x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 67.7 ms: 1.16x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.76 ms: 1.15x faster                                                 |
| regex_compile              | 142 ms                                                 | 124 ms: 1.15x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.70 us: 1.14x faster                                                 |
| crypto_pyaes               | 76.6 ms                                                | 67.7 ms: 1.13x faster                                                 |
| pylint                     | 319 ms                                                 | 283 ms: 1.13x faster                                                  |
| logging_simple             | 6.63 us                                                | 5.89 us: 1.12x faster                                                 |
| pathlib                    | 21.5 ms                                                | 19.3 ms: 1.11x faster                                                 |
| logging_format             | 7.35 us                                                | 6.61 us: 1.11x faster                                                 |
| chaos                      | 62.8 ms                                                | 56.7 ms: 1.11x faster                                                 |
| genshi_text                | 22.8 ms                                                | 20.8 ms: 1.10x faster                                                 |
| xml_etree_generate         | 85.2 ms                                                | 77.9 ms: 1.09x faster                                                 |
| xml_etree_process          | 59.0 ms                                                | 54.3 ms: 1.09x faster                                                 |
| async_generators           | 384 ms                                                 | 355 ms: 1.08x faster                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.40 sec: 1.08x faster                                                |
| unpack_sequence            | 52.1 ns                                                | 48.2 ns: 1.08x faster                                                 |
| logging_silent             | 109 ns                                                 | 101 ns: 1.07x faster                                                  |
| sympy_integrate            | 20.5 ms                                                | 19.2 ms: 1.07x faster                                                 |
| sympy_sum                  | 166 ms                                                 | 155 ms: 1.07x faster                                                  |
| sympy_str                  | 292 ms                                                 | 273 ms: 1.07x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.07x faster                                                  |
| pprint_safe_repr           | 743 ms                                                 | 701 ms: 1.06x faster                                                  |
| typing_runtime_protocols   | 163 us                                                 | 154 us: 1.06x faster                                                  |
| meteor_contest             | 104 ms                                                 | 98.0 ms: 1.06x faster                                                 |
| hexiom                     | 6.17 ms                                                | 5.86 ms: 1.05x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 92.5 ms: 1.05x faster                                                 |
| thrift                     | 791 us                                                 | 758 us: 1.04x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.12 sec: 1.04x faster                                                |
| 2to3                       | 264 ms                                                 | 254 ms: 1.04x faster                                                  |
| asyncio_tcp                | 519 ms                                                 | 501 ms: 1.04x faster                                                  |
| html5lib                   | 63.6 ms                                                | 61.4 ms: 1.03x faster                                                 |
| mako                       | 11.0 ms                                                | 10.7 ms: 1.03x faster                                                 |
| nqueens                    | 80.1 ms                                                | 77.8 ms: 1.03x faster                                                 |
| scimark_lu                 | 114 ms                                                 | 111 ms: 1.03x faster                                                  |
| fannkuch                   | 372 ms                                                 | 363 ms: 1.03x faster                                                  |
| genshi_xml                 | 50.2 ms                                                | 49.0 ms: 1.02x faster                                                 |
| docutils                   | 2.64 sec                                               | 2.60 sec: 1.01x faster                                                |
| sqlite_synth               | 2.20 us                                                | 2.18 us: 1.01x faster                                                 |
| coroutines                 | 23.9 ms                                                | 23.7 ms: 1.01x faster                                                 |
| pickle_pure_python         | 308 us                                                 | 306 us: 1.01x faster                                                  |
| django_template            | 34.7 ms                                                | 34.5 ms: 1.01x faster                                                 |
| asyncio_websockets         | 517 ms                                                 | 518 ms: 1.00x slower                                                  |
| json                       | 5.02 ms                                                | 5.08 ms: 1.01x slower                                                 |
| unpickle                   | 14.1 us                                                | 14.2 us: 1.01x slower                                                 |
| sympy_expand               | 468 ms                                                 | 474 ms: 1.01x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.47 ms: 1.02x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 7.35 ms: 1.03x slower                                                 |
| pickle_dict                | 31.8 us                                                | 32.6 us: 1.03x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 10.7 ms: 1.04x slower                                                 |
| unpickle_list              | 4.67 us                                                | 4.94 us: 1.06x slower                                                 |
| json_loads                 | 26.5 us                                                | 28.2 us: 1.06x slower                                                 |
| regex_dna                  | 168 ms                                                 | 180 ms: 1.07x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 22.3 ms: 1.08x slower                                                 |
| pickle_list                | 4.77 us                                                | 5.19 us: 1.09x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 1.05 ms: 1.12x slower                                                 |
| pickle                     | 10.9 us                                                | 12.4 us: 1.13x slower                                                 |
| coverage                   | 71.4 ms                                                | 81.1 ms: 1.14x slower                                                 |
| pidigits                   | 184 ms                                                 | 210 ms: 1.14x slower                                                  |
| python_startup             | 9.93 ms                                                | 12.6 ms: 1.27x slower                                                 |
| gc_traversal               | 3.46 ms                                                | 4.59 ms: 1.33x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.96 ms: 1.80x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 103 ms: 9.50x slower                                                  |
| telco                      | 6.53 ms                                                | 158 ms: 24.18x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.05x faster                                                          |

Benchmark hidden because not significant (2): nbody, asyncio_tcp_ssl
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20250712-3.15.0a0-47b01da-JIT/bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.085x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.17x