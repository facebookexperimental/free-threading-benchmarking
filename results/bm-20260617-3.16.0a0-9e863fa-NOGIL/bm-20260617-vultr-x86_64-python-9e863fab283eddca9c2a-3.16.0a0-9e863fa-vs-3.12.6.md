# Results vs. 3.12.6

- fork: python
- ref: 9e863fab283eddca9c2a
- machine: linux-x86_64
- commit hash: 9e863fa
- commit date: 2026-06-17
- overall geometric mean: 1.033x slower
- HPT reliability: 89.57%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260617-vultr-x86_64-python-9e863fab283eddca9c2a-3.16.0a0-9e863fa |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 295 ms: 1.12x slower                                                  |
| docutils       | 2.64 sec                                               | 2.94 sec: 1.11x slower                                                |
| html5lib       | 63.6 ms                                                | 68.5 ms: 1.08x slower                                                 |
| Geometric mean | (ref)                                                  | 1.10x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260617-vultr-x86_64-python-9e863fab283eddca9c2a-3.16.0a0-9e863fa |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 677 ms: 1.64x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 698 ms: 1.55x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 390 ms: 1.44x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 319 ms: 1.40x faster                                                  |
| async_tree_none            | 464 ms                                                 | 340 ms: 1.37x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 417 ms: 1.33x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 579 ms: 1.25x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 606 ms: 1.18x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 514 ms: 1.01x faster                                                  |
| async_generators           | 384 ms                                                 | 388 ms: 1.01x slower                                                  |
| coroutines                 | 23.9 ms                                                | 24.7 ms: 1.03x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.26x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260617-vultr-x86_64-python-9e863fab283eddca9c2a-3.16.0a0-9e863fa |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 180 ms: 1.02x faster                                                  |
| float          | 80.8 ms                                                | 86.4 ms: 1.07x slower                                                 |
| nbody          | 89.3 ms                                                | 127 ms: 1.42x slower                                                  |
| Geometric mean | (ref)                                                  | 1.14x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260617-vultr-x86_64-python-9e863fab283eddca9c2a-3.16.0a0-9e863fa |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 3.02 ms: 1.05x faster                                                 |
| regex_v8       | 20.6 ms                                                | 20.1 ms: 1.02x faster                                                 |
| regex_compile  | 142 ms                                                 | 141 ms: 1.01x faster                                                  |
| regex_dna      | 168 ms                                                 | 177 ms: 1.05x slower                                                  |
| Geometric mean | (ref)                                                  | 1.01x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260617-vultr-x86_64-python-9e863fab283eddca9c2a-3.16.0a0-9e863fa |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.97 sec: 1.07x faster                                                |
| xml_etree_iterparse  | 96.7 ms                                                | 94.9 ms: 1.02x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 141 ms: 1.01x slower                                                  |
| json_dumps           | 10.4 ms                                                | 10.6 ms: 1.02x slower                                                 |
| unpickle_pure_python | 221 us                                                 | 239 us: 1.08x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 337 us: 1.09x slower                                                  |
| json_loads           | 26.5 us                                                | 30.5 us: 1.15x slower                                                 |
| xml_etree_generate   | 85.2 ms                                                | 99.2 ms: 1.16x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 74.4 ms: 1.26x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.07x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260617-vultr-x86_64-python-9e863fab283eddca9c2a-3.16.0a0-9e863fa |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.15 ms: 1.28x slower                                                 |
| python_startup         | 9.93 ms                                                | 15.4 ms: 1.55x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.41x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260617-vultr-x86_64-python-9e863fab283eddca9c2a-3.16.0a0-9e863fa |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.7 ms                                                | 40.1 ms: 1.16x slower                                                 |
| mako            | 11.0 ms                                                | 15.9 ms: 1.44x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.29x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260617-vultr-x86_64-python-9e863fab283eddca9c2a-3.16.0a0-9e863fa |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 319 ms                                                 | 132 ms: 2.41x faster                                                  |
| gc_traversal               | 3.46 ms                                                | 1.77 ms: 1.96x faster                                                 |
| mdp                        | 2.42 sec                                               | 1.32 sec: 1.84x faster                                                |
| async_tree_io_tg           | 1.11 sec                                               | 677 ms: 1.64x faster                                                  |
| bench_mp_pool              | 10.8 ms                                                | 6.79 ms: 1.59x faster                                                 |
| async_tree_io              | 1.08 sec                                               | 698 ms: 1.55x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 390 ms: 1.44x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 319 ms: 1.40x faster                                                  |
| async_tree_none            | 464 ms                                                 | 340 ms: 1.37x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 417 ms: 1.33x faster                                                  |
| deepcopy                   | 352 us                                                 | 265 us: 1.33x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 31.1 us: 1.29x faster                                                 |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 579 ms: 1.25x faster                                                  |
| pathlib                    | 21.5 ms                                                | 17.7 ms: 1.22x faster                                                 |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 606 ms: 1.18x faster                                                  |
| go                         | 139 ms                                                 | 122 ms: 1.14x faster                                                  |
| sqlite_synth               | 2.20 us                                                | 1.94 us: 1.13x faster                                                 |
| comprehensions             | 19.8 us                                                | 17.8 us: 1.11x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 71.0 ms: 1.11x faster                                                 |
| typing_runtime_protocols   | 163 us                                                 | 148 us: 1.10x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.37 sec: 1.08x faster                                                |
| tomli_loads                | 2.11 sec                                               | 1.97 sec: 1.07x faster                                                |
| deepcopy_reduce            | 3.08 us                                                | 2.90 us: 1.06x faster                                                 |
| scimark_sor                | 130 ms                                                 | 123 ms: 1.06x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 3.02 ms: 1.05x faster                                                 |
| pycparser                  | 1.17 sec                                               | 1.14 sec: 1.03x faster                                                |
| pidigits                   | 184 ms                                                 | 180 ms: 1.02x faster                                                  |
| regex_v8                   | 20.6 ms                                                | 20.1 ms: 1.02x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 94.9 ms: 1.02x faster                                                 |
| logging_silent             | 109 ns                                                 | 107 ns: 1.02x faster                                                  |
| regex_compile              | 142 ms                                                 | 141 ms: 1.01x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 514 ms: 1.01x faster                                                  |
| async_generators           | 384 ms                                                 | 388 ms: 1.01x slower                                                  |
| xml_etree_parse            | 139 ms                                                 | 141 ms: 1.01x slower                                                  |
| raytrace                   | 299 ms                                                 | 304 ms: 1.01x slower                                                  |
| spectral_norm              | 110 ms                                                 | 112 ms: 1.02x slower                                                  |
| pyflate                    | 448 ms                                                 | 457 ms: 1.02x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 10.6 ms: 1.02x slower                                                 |
| scimark_fft                | 342 ms                                                 | 351 ms: 1.03x slower                                                  |
| logging_simple             | 6.63 us                                                | 6.81 us: 1.03x slower                                                 |
| coroutines                 | 23.9 ms                                                | 24.7 ms: 1.03x slower                                                 |
| generators                 | 32.2 ms                                                | 33.4 ms: 1.03x slower                                                 |
| json                       | 5.02 ms                                                | 5.23 ms: 1.04x slower                                                 |
| regex_dna                  | 168 ms                                                 | 177 ms: 1.05x slower                                                  |
| logging_format             | 7.35 us                                                | 7.77 us: 1.06x slower                                                 |
| sympy_integrate            | 20.5 ms                                                | 21.8 ms: 1.06x slower                                                 |
| sympy_str                  | 292 ms                                                 | 309 ms: 1.06x slower                                                  |
| float                      | 80.8 ms                                                | 86.4 ms: 1.07x slower                                                 |
| deltablue                  | 3.45 ms                                                | 3.69 ms: 1.07x slower                                                 |
| sympy_sum                  | 166 ms                                                 | 178 ms: 1.07x slower                                                  |
| pprint_safe_repr           | 743 ms                                                 | 795 ms: 1.07x slower                                                  |
| html5lib                   | 63.6 ms                                                | 68.5 ms: 1.08x slower                                                 |
| unpickle_pure_python       | 221 us                                                 | 239 us: 1.08x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.65 sec: 1.08x slower                                                |
| hexiom                     | 6.17 ms                                                | 6.71 ms: 1.09x slower                                                 |
| pickle_pure_python         | 308 us                                                 | 337 us: 1.09x slower                                                  |
| nqueens                    | 80.1 ms                                                | 87.7 ms: 1.10x slower                                                 |
| sympy_expand               | 468 ms                                                 | 518 ms: 1.11x slower                                                  |
| docutils                   | 2.64 sec                                               | 2.94 sec: 1.11x slower                                                |
| 2to3                       | 264 ms                                                 | 295 ms: 1.12x slower                                                  |
| thrift                     | 791 us                                                 | 902 us: 1.14x slower                                                  |
| scimark_lu                 | 114 ms                                                 | 130 ms: 1.14x slower                                                  |
| json_loads                 | 26.5 us                                                | 30.5 us: 1.15x slower                                                 |
| django_template            | 34.7 ms                                                | 40.1 ms: 1.16x slower                                                 |
| richards                   | 45.9 ms                                                | 53.2 ms: 1.16x slower                                                 |
| richards_super             | 51.9 ms                                                | 60.2 ms: 1.16x slower                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 79.5 ms: 1.16x slower                                                 |
| xml_etree_generate         | 85.2 ms                                                | 99.2 ms: 1.16x slower                                                 |
| crypto_pyaes               | 76.6 ms                                                | 89.6 ms: 1.17x slower                                                 |
| meteor_contest             | 104 ms                                                 | 124 ms: 1.20x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.42 ms: 1.23x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.36 ms: 1.25x slower                                                 |
| xml_etree_process          | 59.0 ms                                                | 74.4 ms: 1.26x slower                                                 |
| fannkuch                   | 372 ms                                                 | 470 ms: 1.26x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 9.15 ms: 1.28x slower                                                 |
| nbody                      | 89.3 ms                                                | 127 ms: 1.42x slower                                                  |
| mako                       | 11.0 ms                                                | 15.9 ms: 1.44x slower                                                 |
| python_startup             | 9.93 ms                                                | 15.4 ms: 1.55x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 1.47 ms: 1.56x slower                                                 |
| coverage                   | 71.4 ms                                                | 114 ms: 1.60x slower                                                  |
| telco                      | 6.53 ms                                                | 175 ms: 26.86x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.03x slower                                                          |

Benchmark hidden because not significant (1): chaos
Ignored benchmarks (23) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260617-3.16.0a0-9e863fa-NOGIL/bm-20260617-vultr-x86_64-python-9e863fab283eddca9c2a-3.16.0a0-9e863fa.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.033x slower

# HPT report

- Reliability score: 89.57% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.36x