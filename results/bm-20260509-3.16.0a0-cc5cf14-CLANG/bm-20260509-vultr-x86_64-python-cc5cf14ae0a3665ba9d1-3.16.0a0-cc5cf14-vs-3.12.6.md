# Results vs. 3.12.6

- fork: python
- ref: cc5cf14ae0a3665ba9d1
- machine: linux-x86_64
- commit hash: cc5cf14
- commit date: 2026-05-09
- overall geometric mean: 1.091x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| docutils       | 2.64 sec                                               | 2.34 sec: 1.13x faster                                                |
| html5lib       | 63.6 ms                                                | 58.6 ms: 1.09x faster                                                 |
| Geometric mean | (ref)                                                  | 1.11x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none            | 464 ms                                                 | 283 ms: 1.64x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 359 ms: 1.56x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 294 ms: 1.52x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 715 ms: 1.51x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 367 ms: 1.51x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 763 ms: 1.45x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 524 ms: 1.37x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 540 ms: 1.34x faster                                                  |
| asyncio_tcp                | 519 ms                                                 | 450 ms: 1.15x faster                                                  |
| async_generators           | 384 ms                                                 | 335 ms: 1.15x faster                                                  |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.48 sec: 1.02x faster                                                |
| coroutines                 | 23.9 ms                                                | 24.1 ms: 1.00x slower                                                 |
| asyncio_websockets         | 517 ms                                                 | 543 ms: 1.05x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.30x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 73.9 ms: 1.09x faster                                                 |
| nbody          | 89.3 ms                                                | 83.6 ms: 1.07x faster                                                 |
| pidigits       | 184 ms                                                 | 191 ms: 1.04x slower                                                  |
| Geometric mean | (ref)                                                  | 1.04x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 122 ms: 1.17x faster                                                  |
| regex_effbot   | 3.17 ms                                                | 3.11 ms: 1.02x faster                                                 |
| regex_v8       | 20.6 ms                                                | 22.2 ms: 1.08x slower                                                 |
| regex_dna      | 168 ms                                                 | 193 ms: 1.15x slower                                                  |
| Geometric mean | (ref)                                                  | 1.01x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.83 sec: 1.15x faster                                                |
| json_dumps           | 10.4 ms                                                | 9.36 ms: 1.11x faster                                                 |
| unpickle_pure_python | 221 us                                                 | 213 us: 1.03x faster                                                  |
| xml_etree_iterparse  | 96.7 ms                                                | 93.7 ms: 1.03x faster                                                 |
| xml_etree_process    | 59.0 ms                                                | 57.6 ms: 1.02x faster                                                 |
| xml_etree_generate   | 85.2 ms                                                | 83.7 ms: 1.02x faster                                                 |
| pickle_dict          | 31.8 us                                                | 31.9 us: 1.00x slower                                                 |
| pickle_pure_python   | 308 us                                                 | 312 us: 1.01x slower                                                  |
| pickle_list          | 4.77 us                                                | 4.88 us: 1.02x slower                                                 |
| unpickle             | 14.1 us                                                | 15.5 us: 1.10x slower                                                 |
| xml_etree_parse      | 139 ms                                                 | 160 ms: 1.15x slower                                                  |
| pickle               | 10.9 us                                                | 13.2 us: 1.21x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.01x slower                                                          |

Benchmark hidden because not significant (2): unpickle_list, json_loads

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.7 ms                                                | 33.3 ms: 1.04x faster                                                 |
| mako            | 11.0 ms                                                | 12.9 ms: 1.17x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.06x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 319 ms                                                 | 114 ms: 2.81x faster                                                  |
| mdp                        | 2.42 sec                                               | 1.10 sec: 2.20x faster                                                |
| async_tree_none            | 464 ms                                                 | 283 ms: 1.64x faster                                                  |
| deepcopy                   | 352 us                                                 | 222 us: 1.59x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 359 ms: 1.56x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 26.2 us: 1.54x faster                                                 |
| async_tree_none_tg         | 446 ms                                                 | 294 ms: 1.52x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 715 ms: 1.51x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 367 ms: 1.51x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 763 ms: 1.45x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 524 ms: 1.37x faster                                                  |
| comprehensions             | 19.8 us                                                | 14.7 us: 1.35x faster                                                 |
| go                         | 139 ms                                                 | 104 ms: 1.34x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 540 ms: 1.34x faster                                                  |
| logging_silent             | 109 ns                                                 | 83.0 ns: 1.31x faster                                                 |
| spectral_norm              | 110 ms                                                 | 86.0 ms: 1.28x faster                                                 |
| deepcopy_reduce            | 3.08 us                                                | 2.42 us: 1.27x faster                                                 |
| pathlib                    | 21.5 ms                                                | 17.4 ms: 1.24x faster                                                 |
| scimark_sor                | 130 ms                                                 | 106 ms: 1.22x faster                                                  |
| raytrace                   | 299 ms                                                 | 245 ms: 1.22x faster                                                  |
| chaos                      | 62.8 ms                                                | 52.3 ms: 1.20x faster                                                 |
| logging_simple             | 6.63 us                                                | 5.54 us: 1.20x faster                                                 |
| logging_format             | 7.35 us                                                | 6.23 us: 1.18x faster                                                 |
| scimark_fft                | 342 ms                                                 | 291 ms: 1.18x faster                                                  |
| regex_compile              | 142 ms                                                 | 122 ms: 1.17x faster                                                  |
| richards                   | 45.9 ms                                                | 39.3 ms: 1.17x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 68.1 ms: 1.16x faster                                                 |
| richards_super             | 51.9 ms                                                | 44.8 ms: 1.16x faster                                                 |
| tomli_loads                | 2.11 sec                                               | 1.83 sec: 1.15x faster                                                |
| asyncio_tcp                | 519 ms                                                 | 450 ms: 1.15x faster                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 59.4 ms: 1.15x faster                                                 |
| deltablue                  | 3.45 ms                                                | 3.00 ms: 1.15x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.13 sec: 1.15x faster                                                |
| async_generators           | 384 ms                                                 | 335 ms: 1.15x faster                                                  |
| docutils                   | 2.64 sec                                               | 2.34 sec: 1.13x faster                                                |
| sympy_integrate            | 20.5 ms                                                | 18.3 ms: 1.12x faster                                                 |
| generators                 | 32.2 ms                                                | 28.8 ms: 1.12x faster                                                 |
| typing_runtime_protocols   | 163 us                                                 | 146 us: 1.12x faster                                                  |
| sympy_sum                  | 166 ms                                                 | 149 ms: 1.11x faster                                                  |
| nqueens                    | 80.1 ms                                                | 72.3 ms: 1.11x faster                                                 |
| json_dumps                 | 10.4 ms                                                | 9.36 ms: 1.11x faster                                                 |
| sympy_str                  | 292 ms                                                 | 264 ms: 1.10x faster                                                  |
| pyflate                    | 448 ms                                                 | 407 ms: 1.10x faster                                                  |
| float                      | 80.8 ms                                                | 73.9 ms: 1.09x faster                                                 |
| html5lib                   | 63.6 ms                                                | 58.6 ms: 1.09x faster                                                 |
| crypto_pyaes               | 76.6 ms                                                | 70.9 ms: 1.08x faster                                                 |
| hexiom                     | 6.17 ms                                                | 5.74 ms: 1.07x faster                                                 |
| nbody                      | 89.3 ms                                                | 83.6 ms: 1.07x faster                                                 |
| scimark_lu                 | 114 ms                                                 | 107 ms: 1.06x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.10 sec: 1.06x faster                                                |
| sympy_expand               | 468 ms                                                 | 444 ms: 1.05x faster                                                  |
| thrift                     | 791 us                                                 | 754 us: 1.05x faster                                                  |
| django_template            | 34.7 ms                                                | 33.3 ms: 1.04x faster                                                 |
| unpickle_pure_python       | 221 us                                                 | 213 us: 1.03x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 93.7 ms: 1.03x faster                                                 |
| pprint_pformat             | 1.52 sec                                               | 1.48 sec: 1.03x faster                                                |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.28 ms: 1.03x faster                                                 |
| xml_etree_process          | 59.0 ms                                                | 57.6 ms: 1.02x faster                                                 |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.48 sec: 1.02x faster                                                |
| pprint_safe_repr           | 743 ms                                                 | 729 ms: 1.02x faster                                                  |
| xml_etree_generate         | 85.2 ms                                                | 83.7 ms: 1.02x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 3.11 ms: 1.02x faster                                                 |
| sqlite_synth               | 2.20 us                                                | 2.18 us: 1.01x faster                                                 |
| pickle_dict                | 31.8 us                                                | 31.9 us: 1.00x slower                                                 |
| coroutines                 | 23.9 ms                                                | 24.1 ms: 1.00x slower                                                 |
| unpack_sequence            | 52.1 ns                                                | 52.5 ns: 1.01x slower                                                 |
| pickle_pure_python         | 308 us                                                 | 312 us: 1.01x slower                                                  |
| pickle_list                | 4.77 us                                                | 4.88 us: 1.02x slower                                                 |
| meteor_contest             | 104 ms                                                 | 107 ms: 1.04x slower                                                  |
| pidigits                   | 184 ms                                                 | 191 ms: 1.04x slower                                                  |
| asyncio_websockets         | 517 ms                                                 | 543 ms: 1.05x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 22.2 ms: 1.08x slower                                                 |
| unpickle                   | 14.1 us                                                | 15.5 us: 1.10x slower                                                 |
| coverage                   | 71.4 ms                                                | 79.6 ms: 1.11x slower                                                 |
| regex_dna                  | 168 ms                                                 | 193 ms: 1.15x slower                                                  |
| gc_traversal               | 3.46 ms                                                | 3.97 ms: 1.15x slower                                                 |
| xml_etree_parse            | 139 ms                                                 | 160 ms: 1.15x slower                                                  |
| mako                       | 11.0 ms                                                | 12.9 ms: 1.17x slower                                                 |
| pickle                     | 10.9 us                                                | 13.2 us: 1.21x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 1.29 ms: 1.37x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.95 ms: 1.78x slower                                                 |
| telco                      | 6.53 ms                                                | 157 ms: 23.98x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 313 ms: 29.00x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.04x faster                                                          |

Benchmark hidden because not significant (4): unpickle_list, fannkuch, json, json_loads
Ignored benchmarks (18) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: 2to3, aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20260509-3.16.0a0-cc5cf14-CLANG/bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.091x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.20x