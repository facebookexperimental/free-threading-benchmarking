# Results vs. 3.12.6

- fork: python
- ref: cf6758ff9ebd6df8ac2a
- machine: linux-x86_64
- commit hash: cf6758f
- commit date: 2025-12-24
- overall geometric mean: 1.030x slower
- HPT reliability: 87.22%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.40x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251224-vultr-x86_64-python-cf6758ff9ebd6df8ac2a-3.15.0a3+-cf6758f |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 276 ms: 1.05x slower                                                   |
| docutils       | 2.64 sec                                               | 2.74 sec: 1.04x slower                                                 |
| html5lib       | 63.6 ms                                                | 65.8 ms: 1.03x slower                                                  |
| Geometric mean | (ref)                                                  | 1.04x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251224-vultr-x86_64-python-cf6758ff9ebd6df8ac2a-3.15.0a3+-cf6758f |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 600 ms: 1.85x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 606 ms: 1.79x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 321 ms: 1.74x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 260 ms: 1.72x faster                                                   |
| async_tree_none            | 464 ms                                                 | 284 ms: 1.63x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 350 ms: 1.59x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 520 ms: 1.39x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 542 ms: 1.32x faster                                                   |
| async_generators           | 384 ms                                                 | 377 ms: 1.02x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 509 ms: 1.01x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.42x faster                                                           |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251224-vultr-x86_64-python-cf6758ff9ebd6df8ac2a-3.15.0a3+-cf6758f |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 73.9 ms: 1.09x faster                                                  |
| pidigits       | 184 ms                                                 | 195 ms: 1.06x slower                                                   |
| nbody          | 89.3 ms                                                | 125 ms: 1.41x slower                                                   |
| Geometric mean | (ref)                                                  | 1.11x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251224-vultr-x86_64-python-cf6758ff9ebd6df8ac2a-3.15.0a3+-cf6758f |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.89 ms: 1.10x faster                                                  |
| regex_compile  | 142 ms                                                 | 141 ms: 1.01x faster                                                   |
| regex_v8       | 20.6 ms                                                | 21.0 ms: 1.02x slower                                                  |
| Geometric mean | (ref)                                                  | 1.02x faster                                                           |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251224-vultr-x86_64-python-cf6758ff9ebd6df8ac2a-3.15.0a3+-cf6758f |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 88.4 ms: 1.09x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 132 ms: 1.05x faster                                                   |
| json_dumps           | 10.4 ms                                                | 11.1 ms: 1.07x slower                                                  |
| unpickle_pure_python | 221 us                                                 | 236 us: 1.07x slower                                                   |
| pickle_pure_python   | 308 us                                                 | 332 us: 1.08x slower                                                   |
| tomli_loads          | 2.11 sec                                               | 2.28 sec: 1.08x slower                                                 |
| xml_etree_generate   | 85.2 ms                                                | 96.7 ms: 1.14x slower                                                  |
| xml_etree_process    | 59.0 ms                                                | 69.5 ms: 1.18x slower                                                  |
| json_loads           | 26.5 us                                                | 31.5 us: 1.19x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.07x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251224-vultr-x86_64-python-cf6758ff9ebd6df8ac2a-3.15.0a3+-cf6758f |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.66 ms: 1.35x slower                                                  |
| python_startup         | 9.93 ms                                                | 15.8 ms: 1.59x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.46x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251224-vultr-x86_64-python-cf6758ff9ebd6df8ac2a-3.15.0a3+-cf6758f |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 57.6 ms: 1.15x slower                                                  |
| django_template | 34.7 ms                                                | 40.9 ms: 1.18x slower                                                  |
| genshi_text     | 22.8 ms                                                | 27.0 ms: 1.19x slower                                                  |
| mako            | 11.0 ms                                                | 15.9 ms: 1.45x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.23x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251224-vultr-x86_64-python-cf6758ff9ebd6df8ac2a-3.15.0a3+-cf6758f |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.31 sec: 1.85x faster                                                 |
| async_tree_io_tg           | 1.11 sec                                               | 600 ms: 1.85x faster                                                   |
| gc_traversal               | 3.46 ms                                                | 1.91 ms: 1.81x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 606 ms: 1.79x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 321 ms: 1.74x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 260 ms: 1.72x faster                                                   |
| async_tree_none            | 464 ms                                                 | 284 ms: 1.63x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 350 ms: 1.59x faster                                                   |
| bench_mp_pool              | 10.8 ms                                                | 7.09 ms: 1.52x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 520 ms: 1.39x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 30.2 us: 1.33x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 542 ms: 1.32x faster                                                   |
| deepcopy                   | 352 us                                                 | 274 us: 1.29x faster                                                   |
| pathlib                    | 21.5 ms                                                | 18.1 ms: 1.19x faster                                                  |
| go                         | 139 ms                                                 | 119 ms: 1.17x faster                                                   |
| dulwich_log                | 78.9 ms                                                | 69.9 ms: 1.13x faster                                                  |
| comprehensions             | 19.8 us                                                | 17.8 us: 1.12x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.89 ms: 1.10x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 88.4 ms: 1.09x faster                                                  |
| float                      | 80.8 ms                                                | 73.9 ms: 1.09x faster                                                  |
| logging_silent             | 109 ns                                                 | 100 ns: 1.09x faster                                                   |
| bpe_tokeniser              | 4.74 sec                                               | 4.39 sec: 1.08x faster                                                 |
| scimark_sor                | 130 ms                                                 | 121 ms: 1.08x faster                                                   |
| sqlite_synth               | 2.20 us                                                | 2.06 us: 1.07x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 132 ms: 1.05x faster                                                   |
| pylint                     | 319 ms                                                 | 303 ms: 1.05x faster                                                   |
| pycparser                  | 1.17 sec                                               | 1.12 sec: 1.04x faster                                                 |
| deepcopy_reduce            | 3.08 us                                                | 2.96 us: 1.04x faster                                                  |
| async_generators           | 384 ms                                                 | 377 ms: 1.02x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 509 ms: 1.01x faster                                                   |
| regex_compile              | 142 ms                                                 | 141 ms: 1.01x faster                                                   |
| raytrace                   | 299 ms                                                 | 296 ms: 1.01x faster                                                   |
| chaos                      | 62.8 ms                                                | 63.5 ms: 1.01x slower                                                  |
| scimark_fft                | 342 ms                                                 | 349 ms: 1.02x slower                                                   |
| regex_v8                   | 20.6 ms                                                | 21.0 ms: 1.02x slower                                                  |
| logging_simple             | 6.63 us                                                | 6.85 us: 1.03x slower                                                  |
| html5lib                   | 63.6 ms                                                | 65.8 ms: 1.03x slower                                                  |
| pprint_safe_repr           | 743 ms                                                 | 769 ms: 1.03x slower                                                   |
| docutils                   | 2.64 sec                                               | 2.74 sec: 1.04x slower                                                 |
| pyflate                    | 448 ms                                                 | 466 ms: 1.04x slower                                                   |
| deltablue                  | 3.45 ms                                                | 3.59 ms: 1.04x slower                                                  |
| spectral_norm              | 110 ms                                                 | 115 ms: 1.04x slower                                                   |
| hexiom                     | 6.17 ms                                                | 6.46 ms: 1.05x slower                                                  |
| 2to3                       | 264 ms                                                 | 276 ms: 1.05x slower                                                   |
| pprint_pformat             | 1.52 sec                                               | 1.59 sec: 1.05x slower                                                 |
| sympy_sum                  | 166 ms                                                 | 174 ms: 1.05x slower                                                   |
| sympy_integrate            | 20.5 ms                                                | 21.6 ms: 1.05x slower                                                  |
| sympy_str                  | 292 ms                                                 | 307 ms: 1.05x slower                                                   |
| generators                 | 32.2 ms                                                | 34.0 ms: 1.06x slower                                                  |
| pidigits                   | 184 ms                                                 | 195 ms: 1.06x slower                                                   |
| json                       | 5.02 ms                                                | 5.35 ms: 1.06x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 11.1 ms: 1.07x slower                                                  |
| logging_format             | 7.35 us                                                | 7.85 us: 1.07x slower                                                  |
| unpickle_pure_python       | 221 us                                                 | 236 us: 1.07x slower                                                   |
| pickle_pure_python         | 308 us                                                 | 332 us: 1.08x slower                                                   |
| tomli_loads                | 2.11 sec                                               | 2.28 sec: 1.08x slower                                                 |
| nqueens                    | 80.1 ms                                                | 88.9 ms: 1.11x slower                                                  |
| sympy_expand               | 468 ms                                                 | 520 ms: 1.11x slower                                                   |
| thrift                     | 791 us                                                 | 881 us: 1.11x slower                                                   |
| scimark_lu                 | 114 ms                                                 | 129 ms: 1.13x slower                                                   |
| xml_etree_generate         | 85.2 ms                                                | 96.7 ms: 1.14x slower                                                  |
| richards                   | 45.9 ms                                                | 52.2 ms: 1.14x slower                                                  |
| crypto_pyaes               | 76.6 ms                                                | 87.2 ms: 1.14x slower                                                  |
| genshi_xml                 | 50.2 ms                                                | 57.6 ms: 1.15x slower                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 78.8 ms: 1.15x slower                                                  |
| richards_super             | 51.9 ms                                                | 60.1 ms: 1.16x slower                                                  |
| meteor_contest             | 104 ms                                                 | 121 ms: 1.17x slower                                                   |
| typing_runtime_protocols   | 163 us                                                 | 192 us: 1.18x slower                                                   |
| xml_etree_process          | 59.0 ms                                                | 69.5 ms: 1.18x slower                                                  |
| django_template            | 34.7 ms                                                | 40.9 ms: 1.18x slower                                                  |
| genshi_text                | 22.8 ms                                                | 27.0 ms: 1.19x slower                                                  |
| json_loads                 | 26.5 us                                                | 31.5 us: 1.19x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.36 ms: 1.22x slower                                                  |
| fannkuch                   | 372 ms                                                 | 463 ms: 1.24x slower                                                   |
| python_startup_no_site     | 7.16 ms                                                | 9.66 ms: 1.35x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.48 ms: 1.36x slower                                                  |
| nbody                      | 89.3 ms                                                | 125 ms: 1.41x slower                                                   |
| mako                       | 11.0 ms                                                | 15.9 ms: 1.45x slower                                                  |
| coverage                   | 71.4 ms                                                | 112 ms: 1.57x slower                                                   |
| bench_thread_pool          | 941 us                                                 | 1.48 ms: 1.57x slower                                                  |
| python_startup             | 9.93 ms                                                | 15.8 ms: 1.59x slower                                                  |
| telco                      | 6.53 ms                                                | 173 ms: 26.57x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.03x slower                                                           |

Benchmark hidden because not significant (2): coroutines, regex_dna
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251224-3.15.0a3+-cf6758f-NOGIL/bm-20251224-vultr-x86_64-python-cf6758ff9ebd6df8ac2a-3.15.0a3+-cf6758f.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.030x slower

# HPT report

- Reliability score: 87.22% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.40x