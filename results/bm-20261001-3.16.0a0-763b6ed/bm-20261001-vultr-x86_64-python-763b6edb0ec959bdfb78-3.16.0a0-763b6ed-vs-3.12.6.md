# Results vs. 3.12.6

- fork: python
- ref: 763b6edb0ec959bdfb78
- machine: linux-x86_64
- commit hash: 763b6ed
- commit date: 2026-10-01
- overall geometric mean: 1.066x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261001-vultr-x86_64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 259 ms: 1.02x faster                                                  |
| docutils       | 2.64 sec                                               | 2.38 sec: 1.11x faster                                                |
| html5lib       | 63.6 ms                                                | 58.8 ms: 1.08x faster                                                 |
| Geometric mean | (ref)                                                  | 1.07x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261001-vultr-x86_64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 363 ms: 1.54x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 296 ms: 1.51x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 754 ms: 1.47x faster                                                  |
| async_tree_none            | 464 ms                                                 | 328 ms: 1.41x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 771 ms: 1.40x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 400 ms: 1.39x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 552 ms: 1.31x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 561 ms: 1.27x faster                                                  |
| async_generators           | 384 ms                                                 | 349 ms: 1.10x faster                                                  |
| coroutines                 | 23.9 ms                                                | 24.1 ms: 1.01x slower                                                 |
| asyncio_websockets         | 517 ms                                                 | 543 ms: 1.05x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.29x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261001-vultr-x86_64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 72.2 ms: 1.12x faster                                                 |
| pidigits       | 184 ms                                                 | 187 ms: 1.02x slower                                                  |
| Geometric mean | (ref)                                                  | 1.03x faster                                                          |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261001-vultr-x86_64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.64 ms: 1.20x faster                                                 |
| regex_compile  | 142 ms                                                 | 148 ms: 1.04x slower                                                  |
| regex_v8       | 20.6 ms                                                | 21.6 ms: 1.05x slower                                                 |
| regex_dna      | 168 ms                                                 | 178 ms: 1.06x slower                                                  |
| Geometric mean | (ref)                                                  | 1.01x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261001-vultr-x86_64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.84 sec: 1.14x faster                                                |
| json_dumps           | 10.4 ms                                                | 9.34 ms: 1.11x faster                                                 |
| unpickle_pure_python | 221 us                                                 | 211 us: 1.05x faster                                                  |
| xml_etree_iterparse  | 96.7 ms                                                | 92.6 ms: 1.04x faster                                                 |
| pickle_pure_python   | 308 us                                                 | 301 us: 1.02x faster                                                  |
| xml_etree_generate   | 85.2 ms                                                | 88.1 ms: 1.03x slower                                                 |
| json_loads           | 26.5 us                                                | 27.5 us: 1.04x slower                                                 |
| xml_etree_parse      | 139 ms                                                 | 145 ms: 1.04x slower                                                  |
| xml_etree_process    | 59.0 ms                                                | 62.2 ms: 1.05x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261001-vultr-x86_64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.74 ms: 1.08x slower                                                 |
| python_startup         | 9.93 ms                                                | 12.9 ms: 1.30x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.19x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261001-vultr-x86_64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.7 ms                                                | 36.9 ms: 1.06x slower                                                 |
| mako            | 11.0 ms                                                | 12.1 ms: 1.10x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.08x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261001-vultr-x86_64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 319 ms                                                 | 113 ms: 2.81x faster                                                  |
| mdp                        | 2.42 sec                                               | 1.14 sec: 2.12x faster                                                |
| async_tree_memoization_tg  | 560 ms                                                 | 363 ms: 1.54x faster                                                  |
| deepcopy                   | 352 us                                                 | 230 us: 1.53x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 296 ms: 1.51x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 754 ms: 1.47x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 28.0 us: 1.44x faster                                                 |
| async_tree_none            | 464 ms                                                 | 328 ms: 1.41x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 771 ms: 1.40x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 400 ms: 1.39x faster                                                  |
| typing_runtime_protocols   | 163 us                                                 | 118 us: 1.38x faster                                                  |
| go                         | 139 ms                                                 | 103 ms: 1.36x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 552 ms: 1.31x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 561 ms: 1.27x faster                                                  |
| comprehensions             | 19.8 us                                                | 15.8 us: 1.26x faster                                                 |
| pathlib                    | 21.5 ms                                                | 17.7 ms: 1.22x faster                                                 |
| spectral_norm              | 110 ms                                                 | 90.8 ms: 1.21x faster                                                 |
| scimark_sor                | 130 ms                                                 | 107 ms: 1.21x faster                                                  |
| raytrace                   | 299 ms                                                 | 248 ms: 1.21x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.64 ms: 1.20x faster                                                 |
| deepcopy_reduce            | 3.08 us                                                | 2.57 us: 1.20x faster                                                 |
| chaos                      | 62.8 ms                                                | 52.7 ms: 1.19x faster                                                 |
| pyflate                    | 448 ms                                                 | 380 ms: 1.18x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 68.1 ms: 1.16x faster                                                 |
| generators                 | 32.2 ms                                                | 28.2 ms: 1.15x faster                                                 |
| logging_silent             | 109 ns                                                 | 95.3 ns: 1.14x faster                                                 |
| tomli_loads                | 2.11 sec                                               | 1.84 sec: 1.14x faster                                                |
| crypto_pyaes               | 76.6 ms                                                | 67.6 ms: 1.13x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.20 sec: 1.13x faster                                                |
| float                      | 80.8 ms                                                | 72.2 ms: 1.12x faster                                                 |
| scimark_fft                | 342 ms                                                 | 308 ms: 1.11x faster                                                  |
| docutils                   | 2.64 sec                                               | 2.38 sec: 1.11x faster                                                |
| json_dumps                 | 10.4 ms                                                | 9.34 ms: 1.11x faster                                                 |
| async_generators           | 384 ms                                                 | 349 ms: 1.10x faster                                                  |
| logging_simple             | 6.63 us                                                | 6.04 us: 1.10x faster                                                 |
| hexiom                     | 6.17 ms                                                | 5.64 ms: 1.09x faster                                                 |
| logging_format             | 7.35 us                                                | 6.74 us: 1.09x faster                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 63.1 ms: 1.09x faster                                                 |
| html5lib                   | 63.6 ms                                                | 58.8 ms: 1.08x faster                                                 |
| sympy_integrate            | 20.5 ms                                                | 19.0 ms: 1.08x faster                                                 |
| nqueens                    | 80.1 ms                                                | 74.3 ms: 1.08x faster                                                 |
| sympy_sum                  | 166 ms                                                 | 155 ms: 1.07x faster                                                  |
| sympy_str                  | 292 ms                                                 | 275 ms: 1.06x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.11 sec: 1.05x faster                                                |
| richards                   | 45.9 ms                                                | 43.8 ms: 1.05x faster                                                 |
| unpickle_pure_python       | 221 us                                                 | 211 us: 1.05x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 92.6 ms: 1.04x faster                                                 |
| deltablue                  | 3.45 ms                                                | 3.31 ms: 1.04x faster                                                 |
| meteor_contest             | 104 ms                                                 | 100.0 ms: 1.04x faster                                                |
| richards_super             | 51.9 ms                                                | 50.5 ms: 1.03x faster                                                 |
| pickle_pure_python         | 308 us                                                 | 301 us: 1.02x faster                                                  |
| pprint_safe_repr           | 743 ms                                                 | 729 ms: 1.02x faster                                                  |
| 2to3                       | 264 ms                                                 | 259 ms: 1.02x faster                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.50 sec: 1.01x faster                                                |
| coroutines                 | 23.9 ms                                                | 24.1 ms: 1.01x slower                                                 |
| fannkuch                   | 372 ms                                                 | 375 ms: 1.01x slower                                                  |
| pidigits                   | 184 ms                                                 | 187 ms: 1.02x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.49 ms: 1.02x slower                                                 |
| sqlite_synth               | 2.20 us                                                | 2.25 us: 1.02x slower                                                 |
| scimark_lu                 | 114 ms                                                 | 117 ms: 1.03x slower                                                  |
| xml_etree_generate         | 85.2 ms                                                | 88.1 ms: 1.03x slower                                                 |
| json_loads                 | 26.5 us                                                | 27.5 us: 1.04x slower                                                 |
| xml_etree_parse            | 139 ms                                                 | 145 ms: 1.04x slower                                                  |
| regex_compile              | 142 ms                                                 | 148 ms: 1.04x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 21.6 ms: 1.05x slower                                                 |
| asyncio_websockets         | 517 ms                                                 | 543 ms: 1.05x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 62.2 ms: 1.05x slower                                                 |
| regex_dna                  | 168 ms                                                 | 178 ms: 1.06x slower                                                  |
| django_template            | 34.7 ms                                                | 36.9 ms: 1.06x slower                                                 |
| gc_traversal               | 3.46 ms                                                | 3.72 ms: 1.08x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 7.74 ms: 1.08x slower                                                 |
| mako                       | 11.0 ms                                                | 12.1 ms: 1.10x slower                                                 |
| coverage                   | 71.4 ms                                                | 83.2 ms: 1.16x slower                                                 |
| python_startup             | 9.93 ms                                                | 12.9 ms: 1.30x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 1.34 ms: 1.43x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.67 ms: 1.53x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 253 ms: 23.43x slower                                                 |
| telco                      | 6.53 ms                                                | 160 ms: 24.49x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.02x faster                                                          |

Benchmark hidden because not significant (4): thrift, nbody, sympy_expand, json
Ignored benchmarks (23) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20261001-3.16.0a0-763b6ed/bm-20261001-vultr-x86_64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.066x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.15x