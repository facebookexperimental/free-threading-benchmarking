# Results vs. 3.12.6

- fork: python
- ref: cdfdf7bb73a5751ecec7
- machine: linux-x86_64
- commit hash: cdfdf7b
- commit date: 2026-10-08
- overall geometric mean: 1.042x slower
- HPT reliability: 78.07%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261008-vultr-x86_64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 296 ms: 1.12x slower                                                  |
| docutils       | 2.64 sec                                               | 2.90 sec: 1.10x slower                                                |
| html5lib       | 63.6 ms                                                | 67.4 ms: 1.06x slower                                                 |
| Geometric mean | (ref)                                                  | 1.09x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261008-vultr-x86_64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 698 ms: 1.59x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 708 ms: 1.53x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 400 ms: 1.40x faster                                                  |
| async_tree_none            | 464 ms                                                 | 343 ms: 1.36x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 333 ms: 1.34x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 423 ms: 1.31x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 612 ms: 1.18x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 632 ms: 1.13x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 506 ms: 1.02x faster                                                  |
| async_generators           | 384 ms                                                 | 421 ms: 1.10x slower                                                  |
| coroutines                 | 23.9 ms                                                | 27.1 ms: 1.13x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.22x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261008-vultr-x86_64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 85.2 ms: 1.05x slower                                                 |
| pidigits       | 184 ms                                                 | 197 ms: 1.07x slower                                                  |
| nbody          | 89.3 ms                                                | 117 ms: 1.30x slower                                                  |
| Geometric mean | (ref)                                                  | 1.14x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261008-vultr-x86_64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.98 ms: 1.06x faster                                                 |
| regex_v8       | 20.6 ms                                                | 21.1 ms: 1.02x slower                                                 |
| regex_dna      | 168 ms                                                 | 178 ms: 1.06x slower                                                  |
| regex_compile  | 142 ms                                                 | 169 ms: 1.19x slower                                                  |
| Geometric mean | (ref)                                                  | 1.05x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261008-vultr-x86_64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.96 sec: 1.08x faster                                                |
| json_dumps           | 10.4 ms                                                | 9.99 ms: 1.04x faster                                                 |
| xml_etree_iterparse  | 96.7 ms                                                | 96.1 ms: 1.01x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 140 ms: 1.01x slower                                                  |
| unpickle_pure_python | 221 us                                                 | 240 us: 1.09x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 335 us: 1.09x slower                                                  |
| json_loads           | 26.5 us                                                | 30.5 us: 1.15x slower                                                 |
| xml_etree_generate   | 85.2 ms                                                | 101 ms: 1.19x slower                                                  |
| xml_etree_process    | 59.0 ms                                                | 75.5 ms: 1.28x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.07x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261008-vultr-x86_64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.70 ms: 1.35x slower                                                 |
| python_startup         | 9.93 ms                                                | 16.3 ms: 1.65x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.49x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261008-vultr-x86_64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.7 ms                                                | 41.5 ms: 1.20x slower                                                 |
| mako            | 11.0 ms                                                | 15.9 ms: 1.44x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.31x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261008-vultr-x86_64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 319 ms                                                 | 131 ms: 2.44x faster                                                  |
| gc_traversal               | 3.46 ms                                                | 1.77 ms: 1.96x faster                                                 |
| mdp                        | 2.42 sec                                               | 1.30 sec: 1.85x faster                                                |
| bench_mp_pool              | 10.8 ms                                                | 6.75 ms: 1.60x faster                                                 |
| async_tree_io_tg           | 1.11 sec                                               | 698 ms: 1.59x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 708 ms: 1.53x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 400 ms: 1.40x faster                                                  |
| async_tree_none            | 464 ms                                                 | 343 ms: 1.36x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 333 ms: 1.34x faster                                                  |
| deepcopy                   | 352 us                                                 | 266 us: 1.32x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 423 ms: 1.31x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 32.9 us: 1.22x faster                                                 |
| pathlib                    | 21.5 ms                                                | 18.1 ms: 1.19x faster                                                 |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 612 ms: 1.18x faster                                                  |
| go                         | 139 ms                                                 | 120 ms: 1.16x faster                                                  |
| sqlite_synth               | 2.20 us                                                | 1.91 us: 1.15x faster                                                 |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 632 ms: 1.13x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 70.1 ms: 1.12x faster                                                 |
| typing_runtime_protocols   | 163 us                                                 | 146 us: 1.12x faster                                                  |
| comprehensions             | 19.8 us                                                | 18.4 us: 1.08x faster                                                 |
| tomli_loads                | 2.11 sec                                               | 1.96 sec: 1.08x faster                                                |
| scimark_sor                | 130 ms                                                 | 121 ms: 1.07x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.44 sec: 1.07x faster                                                |
| spectral_norm              | 110 ms                                                 | 103 ms: 1.06x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.98 ms: 1.06x faster                                                 |
| deepcopy_reduce            | 3.08 us                                                | 2.91 us: 1.06x faster                                                 |
| chaos                      | 62.8 ms                                                | 59.6 ms: 1.05x faster                                                 |
| scimark_fft                | 342 ms                                                 | 327 ms: 1.04x faster                                                  |
| json_dumps                 | 10.4 ms                                                | 9.99 ms: 1.04x faster                                                 |
| pycparser                  | 1.17 sec                                               | 1.14 sec: 1.03x faster                                                |
| raytrace                   | 299 ms                                                 | 291 ms: 1.03x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 506 ms: 1.02x faster                                                  |
| logging_silent             | 109 ns                                                 | 107 ns: 1.02x faster                                                  |
| pyflate                    | 448 ms                                                 | 443 ms: 1.01x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 96.1 ms: 1.01x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 140 ms: 1.01x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 21.1 ms: 1.02x slower                                                 |
| float                      | 80.8 ms                                                | 85.2 ms: 1.05x slower                                                 |
| html5lib                   | 63.6 ms                                                | 67.4 ms: 1.06x slower                                                 |
| regex_dna                  | 168 ms                                                 | 178 ms: 1.06x slower                                                  |
| sympy_integrate            | 20.5 ms                                                | 21.8 ms: 1.06x slower                                                 |
| pidigits                   | 184 ms                                                 | 197 ms: 1.07x slower                                                  |
| logging_simple             | 6.63 us                                                | 7.09 us: 1.07x slower                                                 |
| json                       | 5.02 ms                                                | 5.41 ms: 1.08x slower                                                 |
| sympy_str                  | 292 ms                                                 | 316 ms: 1.08x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 180 ms: 1.08x slower                                                  |
| hexiom                     | 6.17 ms                                                | 6.69 ms: 1.08x slower                                                 |
| unpickle_pure_python       | 221 us                                                 | 240 us: 1.09x slower                                                  |
| pprint_safe_repr           | 743 ms                                                 | 808 ms: 1.09x slower                                                  |
| generators                 | 32.2 ms                                                | 35.1 ms: 1.09x slower                                                 |
| logging_format             | 7.35 us                                                | 7.99 us: 1.09x slower                                                 |
| pickle_pure_python         | 308 us                                                 | 335 us: 1.09x slower                                                  |
| nqueens                    | 80.1 ms                                                | 87.2 ms: 1.09x slower                                                 |
| deltablue                  | 3.45 ms                                                | 3.77 ms: 1.09x slower                                                 |
| async_generators           | 384 ms                                                 | 421 ms: 1.10x slower                                                  |
| docutils                   | 2.64 sec                                               | 2.90 sec: 1.10x slower                                                |
| pprint_pformat             | 1.52 sec                                               | 1.67 sec: 1.10x slower                                                |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.86 ms: 1.11x slower                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 76.9 ms: 1.12x slower                                                 |
| 2to3                       | 264 ms                                                 | 296 ms: 1.12x slower                                                  |
| sympy_expand               | 468 ms                                                 | 529 ms: 1.13x slower                                                  |
| coroutines                 | 23.9 ms                                                | 27.1 ms: 1.13x slower                                                 |
| crypto_pyaes               | 76.6 ms                                                | 87.1 ms: 1.14x slower                                                 |
| scimark_lu                 | 114 ms                                                 | 130 ms: 1.14x slower                                                  |
| json_loads                 | 26.5 us                                                | 30.5 us: 1.15x slower                                                 |
| richards                   | 45.9 ms                                                | 53.1 ms: 1.16x slower                                                 |
| richards_super             | 51.9 ms                                                | 60.7 ms: 1.17x slower                                                 |
| thrift                     | 791 us                                                 | 936 us: 1.18x slower                                                  |
| regex_compile              | 142 ms                                                 | 169 ms: 1.19x slower                                                  |
| xml_etree_generate         | 85.2 ms                                                | 101 ms: 1.19x slower                                                  |
| django_template            | 34.7 ms                                                | 41.5 ms: 1.20x slower                                                 |
| meteor_contest             | 104 ms                                                 | 128 ms: 1.23x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.36 ms: 1.24x slower                                                 |
| fannkuch                   | 372 ms                                                 | 465 ms: 1.25x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 75.5 ms: 1.28x slower                                                 |
| nbody                      | 89.3 ms                                                | 117 ms: 1.30x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 9.70 ms: 1.35x slower                                                 |
| mako                       | 11.0 ms                                                | 15.9 ms: 1.44x slower                                                 |
| coverage                   | 71.4 ms                                                | 117 ms: 1.64x slower                                                  |
| python_startup             | 9.93 ms                                                | 16.3 ms: 1.65x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 1.64 ms: 1.74x slower                                                 |
| telco                      | 6.53 ms                                                | 176 ms: 27.03x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.04x slower                                                          |
Ignored benchmarks (23) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20261008-3.16.0a0-cdfdf7b-NOGIL/bm-20261008-vultr-x86_64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.042x slower

# HPT report

- Reliability score: 78.07% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.36x