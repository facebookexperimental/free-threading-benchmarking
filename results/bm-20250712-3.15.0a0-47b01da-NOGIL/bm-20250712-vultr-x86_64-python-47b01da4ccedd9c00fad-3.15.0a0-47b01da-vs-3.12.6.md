# Results vs. 3.12.6

- fork: python
- ref: 47b01da4ccedd9c00fad
- machine: linux-x86_64
- commit hash: 47b01da
- commit date: 2025-07-12
- overall geometric mean: 1.028x slower
- HPT reliability: 95.20%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.40x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 285 ms: 1.08x slower                                                  |
| docutils       | 2.64 sec                                               | 2.70 sec: 1.02x slower                                                |
| html5lib       | 63.6 ms                                                | 66.1 ms: 1.04x slower                                                 |
| Geometric mean | (ref)                                                  | 1.05x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 536 ms: 2.07x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 564 ms: 1.92x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 233 ms: 1.92x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 294 ms: 1.91x faster                                                  |
| async_tree_none            | 464 ms                                                 | 264 ms: 1.76x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 322 ms: 1.73x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 488 ms: 1.48x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 515 ms: 1.39x faster                                                  |
| async_generators           | 384 ms                                                 | 371 ms: 1.04x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 512 ms: 1.01x faster                                                  |
| coroutines                 | 23.9 ms                                                | 24.7 ms: 1.03x slower                                                 |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.81 sec: 1.20x slower                                                |
| Geometric mean             | (ref)                                                  | 1.40x faster                                                          |

Benchmark hidden because not significant (1): asyncio_tcp

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 69.9 ms: 1.16x faster                                                 |
| pidigits       | 184 ms                                                 | 195 ms: 1.06x slower                                                  |
| nbody          | 89.3 ms                                                | 122 ms: 1.37x slower                                                  |
| Geometric mean | (ref)                                                  | 1.08x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.66 ms: 1.19x faster                                                 |
| regex_compile  | 142 ms                                                 | 144 ms: 1.01x slower                                                  |
| regex_dna      | 168 ms                                                 | 174 ms: 1.04x slower                                                  |
| Geometric mean | (ref)                                                  | 1.03x faster                                                          |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 87.4 ms: 1.11x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.07x faster                                                  |
| tomli_loads          | 2.11 sec                                               | 2.16 sec: 1.03x slower                                                |
| pickle_dict          | 31.8 us                                                | 32.8 us: 1.03x slower                                                 |
| unpickle_pure_python | 221 us                                                 | 231 us: 1.05x slower                                                  |
| pickle_list          | 4.77 us                                                | 5.22 us: 1.10x slower                                                 |
| pickle_pure_python   | 308 us                                                 | 339 us: 1.10x slower                                                  |
| unpickle             | 14.1 us                                                | 15.7 us: 1.12x slower                                                 |
| xml_etree_generate   | 85.2 ms                                                | 96.1 ms: 1.13x slower                                                 |
| pickle               | 10.9 us                                                | 12.4 us: 1.13x slower                                                 |
| unpickle_list        | 4.67 us                                                | 5.33 us: 1.14x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 69.4 ms: 1.18x slower                                                 |
| json_dumps           | 10.4 ms                                                | 12.2 ms: 1.18x slower                                                 |
| json_loads           | 26.5 us                                                | 31.3 us: 1.18x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.08x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.57 ms: 1.34x slower                                                 |
| python_startup         | 9.93 ms                                                | 16.0 ms: 1.61x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.47x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 57.8 ms: 1.15x slower                                                 |
| django_template | 34.7 ms                                                | 40.2 ms: 1.16x slower                                                 |
| genshi_text     | 22.8 ms                                                | 26.9 ms: 1.18x slower                                                 |
| mako            | 11.0 ms                                                | 15.5 ms: 1.41x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.22x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 536 ms: 2.07x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 564 ms: 1.92x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 233 ms: 1.92x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 294 ms: 1.91x faster                                                  |
| gc_traversal               | 3.46 ms                                                | 1.88 ms: 1.83x faster                                                 |
| mdp                        | 2.42 sec                                               | 1.33 sec: 1.82x faster                                                |
| async_tree_none            | 464 ms                                                 | 264 ms: 1.76x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 322 ms: 1.73x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 488 ms: 1.48x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 515 ms: 1.39x faster                                                  |
| deepcopy                   | 352 us                                                 | 294 us: 1.20x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.66 ms: 1.19x faster                                                 |
| deepcopy_memo              | 40.3 us                                                | 34.7 us: 1.16x faster                                                 |
| float                      | 80.8 ms                                                | 69.9 ms: 1.16x faster                                                 |
| go                         | 139 ms                                                 | 121 ms: 1.15x faster                                                  |
| comprehensions             | 19.8 us                                                | 17.8 us: 1.12x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 87.4 ms: 1.11x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 71.8 ms: 1.10x faster                                                 |
| pathlib                    | 21.5 ms                                                | 19.7 ms: 1.09x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.39 sec: 1.08x faster                                                |
| sqlite_synth               | 2.20 us                                                | 2.04 us: 1.08x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.07x faster                                                  |
| logging_silent             | 109 ns                                                 | 105 ns: 1.04x faster                                                  |
| async_generators           | 384 ms                                                 | 371 ms: 1.04x faster                                                  |
| scimark_sor                | 130 ms                                                 | 125 ms: 1.03x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 3.01 us: 1.02x faster                                                 |
| pycparser                  | 1.17 sec                                               | 1.14 sec: 1.02x faster                                                |
| asyncio_websockets         | 517 ms                                                 | 512 ms: 1.01x faster                                                  |
| raytrace                   | 299 ms                                                 | 302 ms: 1.01x slower                                                  |
| regex_compile              | 142 ms                                                 | 144 ms: 1.01x slower                                                  |
| docutils                   | 2.64 sec                                               | 2.70 sec: 1.02x slower                                                |
| tomli_loads                | 2.11 sec                                               | 2.16 sec: 1.03x slower                                                |
| spectral_norm              | 110 ms                                                 | 113 ms: 1.03x slower                                                  |
| coroutines                 | 23.9 ms                                                | 24.7 ms: 1.03x slower                                                 |
| pickle_dict                | 31.8 us                                                | 32.8 us: 1.03x slower                                                 |
| regex_dna                  | 168 ms                                                 | 174 ms: 1.04x slower                                                  |
| html5lib                   | 63.6 ms                                                | 66.1 ms: 1.04x slower                                                 |
| pyflate                    | 448 ms                                                 | 467 ms: 1.04x slower                                                  |
| unpickle_pure_python       | 221 us                                                 | 231 us: 1.05x slower                                                  |
| pprint_safe_repr           | 743 ms                                                 | 783 ms: 1.05x slower                                                  |
| hexiom                     | 6.17 ms                                                | 6.51 ms: 1.06x slower                                                 |
| logging_simple             | 6.63 us                                                | 7.02 us: 1.06x slower                                                 |
| deltablue                  | 3.45 ms                                                | 3.65 ms: 1.06x slower                                                 |
| pidigits                   | 184 ms                                                 | 195 ms: 1.06x slower                                                  |
| json                       | 5.02 ms                                                | 5.35 ms: 1.06x slower                                                 |
| unpack_sequence            | 52.1 ns                                                | 55.5 ns: 1.07x slower                                                 |
| pprint_pformat             | 1.52 sec                                               | 1.63 sec: 1.07x slower                                                |
| sympy_integrate            | 20.5 ms                                                | 22.1 ms: 1.08x slower                                                 |
| sympy_str                  | 292 ms                                                 | 314 ms: 1.08x slower                                                  |
| 2to3                       | 264 ms                                                 | 285 ms: 1.08x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 181 ms: 1.09x slower                                                  |
| scimark_fft                | 342 ms                                                 | 373 ms: 1.09x slower                                                  |
| pickle_list                | 4.77 us                                                | 5.22 us: 1.10x slower                                                 |
| logging_format             | 7.35 us                                                | 8.07 us: 1.10x slower                                                 |
| pickle_pure_python         | 308 us                                                 | 339 us: 1.10x slower                                                  |
| nqueens                    | 80.1 ms                                                | 88.9 ms: 1.11x slower                                                 |
| thrift                     | 791 us                                                 | 885 us: 1.12x slower                                                  |
| unpickle                   | 14.1 us                                                | 15.7 us: 1.12x slower                                                 |
| richards                   | 45.9 ms                                                | 51.4 ms: 1.12x slower                                                 |
| xml_etree_generate         | 85.2 ms                                                | 96.1 ms: 1.13x slower                                                 |
| sympy_expand               | 468 ms                                                 | 528 ms: 1.13x slower                                                  |
| crypto_pyaes               | 76.6 ms                                                | 86.7 ms: 1.13x slower                                                 |
| pickle                     | 10.9 us                                                | 12.4 us: 1.13x slower                                                 |
| richards_super             | 51.9 ms                                                | 59.0 ms: 1.14x slower                                                 |
| scimark_lu                 | 114 ms                                                 | 130 ms: 1.14x slower                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 77.9 ms: 1.14x slower                                                 |
| unpickle_list              | 4.67 us                                                | 5.33 us: 1.14x slower                                                 |
| meteor_contest             | 104 ms                                                 | 119 ms: 1.15x slower                                                  |
| genshi_xml                 | 50.2 ms                                                | 57.8 ms: 1.15x slower                                                 |
| django_template            | 34.7 ms                                                | 40.2 ms: 1.16x slower                                                 |
| typing_runtime_protocols   | 163 us                                                 | 191 us: 1.17x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 69.4 ms: 1.18x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 12.2 ms: 1.18x slower                                                 |
| json_loads                 | 26.5 us                                                | 31.3 us: 1.18x slower                                                 |
| genshi_text                | 22.8 ms                                                | 26.9 ms: 1.18x slower                                                 |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.81 sec: 1.20x slower                                                |
| fannkuch                   | 372 ms                                                 | 454 ms: 1.22x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.57 ms: 1.27x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 9.57 ms: 1.34x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.46 ms: 1.34x slower                                                 |
| nbody                      | 89.3 ms                                                | 122 ms: 1.37x slower                                                  |
| mako                       | 11.0 ms                                                | 15.5 ms: 1.41x slower                                                 |
| coverage                   | 71.4 ms                                                | 111 ms: 1.55x slower                                                  |
| python_startup             | 9.93 ms                                                | 16.0 ms: 1.61x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 3.16 ms: 3.36x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 109 ms: 10.06x slower                                                 |
| telco                      | 6.53 ms                                                | 177 ms: 27.05x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.07x slower                                                          |

Benchmark hidden because not significant (5): pylint, chaos, asyncio_tcp, generators, regex_v8
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20250712-3.15.0a0-47b01da-NOGIL/bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.028x slower

# HPT report

- Reliability score: 95.20% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.40x