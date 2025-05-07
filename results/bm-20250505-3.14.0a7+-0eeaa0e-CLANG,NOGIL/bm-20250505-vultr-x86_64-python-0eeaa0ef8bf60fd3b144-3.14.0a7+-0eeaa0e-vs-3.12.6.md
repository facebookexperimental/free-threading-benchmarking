# Results vs. 3.12.6

- fork: python
- ref: 0eeaa0ef8bf60fd3b144
- machine: linux-x86_64
- commit hash: 0eeaa0e
- commit date: 2025-05-05
- overall geometric mean: 1.054x faster
- HPT reliability: 61.57%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.46x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250505-vultr-x86_64-python-0eeaa0ef8bf60fd3b144-3.14.0a7+-0eeaa0e |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 268 ms: 1.02x slower                                                   |
| docutils       | 2.64 sec                                               | 2.67 sec: 1.01x slower                                                 |
| Geometric mean | (ref)                                                  | 1.01x slower                                                           |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250505-vultr-x86_64-python-0eeaa0ef8bf60fd3b144-3.14.0a7+-0eeaa0e |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 488 ms: 2.27x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 212 ms: 2.11x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 517 ms: 2.09x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 269 ms: 2.08x faster                                                   |
| async_tree_none            | 464 ms                                                 | 247 ms: 1.88x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 301 ms: 1.85x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 444 ms: 1.63x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 470 ms: 1.52x faster                                                   |
| coroutines                 | 23.9 ms                                                | 20.8 ms: 1.15x faster                                                  |
| async_generators           | 384 ms                                                 | 334 ms: 1.15x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.64x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250505-vultr-x86_64-python-0eeaa0ef8bf60fd3b144-3.14.0a7+-0eeaa0e |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 66.3 ms: 1.22x faster                                                  |
| pidigits       | 184 ms                                                 | 187 ms: 1.02x slower                                                   |
| nbody          | 89.3 ms                                                | 113 ms: 1.27x slower                                                   |
| Geometric mean | (ref)                                                  | 1.02x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250505-vultr-x86_64-python-0eeaa0ef8bf60fd3b144-3.14.0a7+-0eeaa0e |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 138 ms: 1.04x faster                                                   |
| regex_effbot   | 3.17 ms                                                | 3.47 ms: 1.10x slower                                                  |
| regex_v8       | 20.6 ms                                                | 24.6 ms: 1.19x slower                                                  |
| regex_dna      | 168 ms                                                 | 209 ms: 1.25x slower                                                   |
| Geometric mean | (ref)                                                  | 1.12x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250505-vultr-x86_64-python-0eeaa0ef8bf60fd3b144-3.14.0a7+-0eeaa0e |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 85.4 ms: 1.13x faster                                                  |
| tomli_loads          | 2.11 sec                                               | 1.97 sec: 1.07x faster                                                 |
| xml_etree_generate   | 85.2 ms                                                | 86.9 ms: 1.02x slower                                                  |
| xml_etree_parse      | 139 ms                                                 | 142 ms: 1.02x slower                                                   |
| unpickle_pure_python | 221 us                                                 | 227 us: 1.03x slower                                                   |
| xml_etree_process    | 59.0 ms                                                | 61.5 ms: 1.04x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 326 us: 1.06x slower                                                   |
| json_loads           | 26.5 us                                                | 29.7 us: 1.12x slower                                                  |
| json_dumps           | 10.4 ms                                                | 12.9 ms: 1.24x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.03x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250505-vultr-x86_64-python-0eeaa0ef8bf60fd3b144-3.14.0a7+-0eeaa0e |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.42 ms: 1.32x slower                                                  |
| python_startup         | 9.93 ms                                                | 15.6 ms: 1.58x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.44x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250505-vultr-x86_64-python-0eeaa0ef8bf60fd3b144-3.14.0a7+-0eeaa0e |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 51.4 ms: 1.02x slower                                                  |
| genshi_text     | 22.8 ms                                                | 24.1 ms: 1.06x slower                                                  |
| django_template | 34.7 ms                                                | 37.0 ms: 1.07x slower                                                  |
| mako            | 11.0 ms                                                | 14.7 ms: 1.34x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.11x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250505-vultr-x86_64-python-0eeaa0ef8bf60fd3b144-3.14.0a7+-0eeaa0e |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 488 ms: 2.27x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 212 ms: 2.11x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 517 ms: 2.09x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 269 ms: 2.08x faster                                                   |
| mdp                        | 2.42 sec                                               | 1.28 sec: 1.88x faster                                                 |
| async_tree_none            | 464 ms                                                 | 247 ms: 1.88x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 301 ms: 1.85x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 444 ms: 1.63x faster                                                   |
| gc_traversal               | 3.46 ms                                                | 2.13 ms: 1.62x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 470 ms: 1.52x faster                                                   |
| deepcopy                   | 352 us                                                 | 260 us: 1.35x faster                                                   |
| logging_silent             | 109 ns                                                 | 85.5 ns: 1.27x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 32.9 us: 1.23x faster                                                  |
| float                      | 80.8 ms                                                | 66.3 ms: 1.22x faster                                                  |
| go                         | 139 ms                                                 | 119 ms: 1.17x faster                                                   |
| coroutines                 | 23.9 ms                                                | 20.8 ms: 1.15x faster                                                  |
| async_generators           | 384 ms                                                 | 334 ms: 1.15x faster                                                   |
| deepcopy_reduce            | 3.08 us                                                | 2.68 us: 1.15x faster                                                  |
| pathlib                    | 21.5 ms                                                | 18.8 ms: 1.15x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 85.4 ms: 1.13x faster                                                  |
| comprehensions             | 19.8 us                                                | 17.5 us: 1.13x faster                                                  |
| generators                 | 32.2 ms                                                | 28.5 ms: 1.13x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.20 sec: 1.13x faster                                                 |
| scimark_sor                | 130 ms                                                 | 116 ms: 1.12x faster                                                   |
| spectral_norm              | 110 ms                                                 | 99.1 ms: 1.11x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 71.8 ms: 1.10x faster                                                  |
| sqlite_synth               | 2.20 us                                                | 2.03 us: 1.09x faster                                                  |
| pylint                     | 319 ms                                                 | 294 ms: 1.08x faster                                                   |
| chaos                      | 62.8 ms                                                | 58.3 ms: 1.08x faster                                                  |
| raytrace                   | 299 ms                                                 | 278 ms: 1.08x faster                                                   |
| tomli_loads                | 2.11 sec                                               | 1.97 sec: 1.07x faster                                                 |
| regex_compile              | 142 ms                                                 | 138 ms: 1.04x faster                                                   |
| pycparser                  | 1.17 sec                                               | 1.13 sec: 1.03x faster                                                 |
| deltablue                  | 3.45 ms                                                | 3.40 ms: 1.01x faster                                                  |
| pyflate                    | 448 ms                                                 | 444 ms: 1.01x faster                                                   |
| hexiom                     | 6.17 ms                                                | 6.23 ms: 1.01x slower                                                  |
| docutils                   | 2.64 sec                                               | 2.67 sec: 1.01x slower                                                 |
| pprint_safe_repr           | 743 ms                                                 | 754 ms: 1.01x slower                                                   |
| sympy_integrate            | 20.5 ms                                                | 20.9 ms: 1.02x slower                                                  |
| pidigits                   | 184 ms                                                 | 187 ms: 1.02x slower                                                   |
| 2to3                       | 264 ms                                                 | 268 ms: 1.02x slower                                                   |
| xml_etree_generate         | 85.2 ms                                                | 86.9 ms: 1.02x slower                                                  |
| sympy_str                  | 292 ms                                                 | 298 ms: 1.02x slower                                                   |
| xml_etree_parse            | 139 ms                                                 | 142 ms: 1.02x slower                                                   |
| nqueens                    | 80.1 ms                                                | 82.0 ms: 1.02x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.56 sec: 1.02x slower                                                 |
| genshi_xml                 | 50.2 ms                                                | 51.4 ms: 1.02x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 170 ms: 1.03x slower                                                   |
| unpickle_pure_python       | 221 us                                                 | 227 us: 1.03x slower                                                   |
| xml_etree_process          | 59.0 ms                                                | 61.5 ms: 1.04x slower                                                  |
| json                       | 5.02 ms                                                | 5.25 ms: 1.04x slower                                                  |
| sqlalchemy_declarative     | 143 ms                                                 | 150 ms: 1.05x slower                                                   |
| crypto_pyaes               | 76.6 ms                                                | 80.7 ms: 1.05x slower                                                  |
| richards                   | 45.9 ms                                                | 48.5 ms: 1.06x slower                                                  |
| sqlalchemy_imperative      | 21.8 ms                                                | 23.0 ms: 1.06x slower                                                  |
| genshi_text                | 22.8 ms                                                | 24.1 ms: 1.06x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 326 us: 1.06x slower                                                   |
| django_template            | 34.7 ms                                                | 37.0 ms: 1.07x slower                                                  |
| typing_runtime_protocols   | 163 us                                                 | 174 us: 1.07x slower                                                   |
| scimark_lu                 | 114 ms                                                 | 122 ms: 1.07x slower                                                   |
| scimark_monte_carlo        | 68.4 ms                                                | 73.5 ms: 1.07x slower                                                  |
| scimark_fft                | 342 ms                                                 | 367 ms: 1.07x slower                                                   |
| sympy_expand               | 468 ms                                                 | 507 ms: 1.08x slower                                                   |
| regex_effbot               | 3.17 ms                                                | 3.47 ms: 1.10x slower                                                  |
| richards_super             | 51.9 ms                                                | 57.2 ms: 1.10x slower                                                  |
| fannkuch                   | 372 ms                                                 | 412 ms: 1.11x slower                                                   |
| json_loads                 | 26.5 us                                                | 29.7 us: 1.12x slower                                                  |
| meteor_contest             | 104 ms                                                 | 120 ms: 1.16x slower                                                   |
| regex_v8                   | 20.6 ms                                                | 24.6 ms: 1.19x slower                                                  |
| telco                      | 6.53 ms                                                | 8.10 ms: 1.24x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 12.9 ms: 1.24x slower                                                  |
| regex_dna                  | 168 ms                                                 | 209 ms: 1.25x slower                                                   |
| nbody                      | 89.3 ms                                                | 113 ms: 1.27x slower                                                   |
| create_gc_cycles           | 1.09 ms                                                | 1.39 ms: 1.28x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 9.42 ms: 1.32x slower                                                  |
| mako                       | 11.0 ms                                                | 14.7 ms: 1.34x slower                                                  |
| coverage                   | 71.4 ms                                                | 96.5 ms: 1.35x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 6.16 ms: 1.40x slower                                                  |
| python_startup             | 9.93 ms                                                | 15.6 ms: 1.58x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 3.11 ms: 3.31x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 84.6 ms: 7.84x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.02x faster                                                           |

Benchmark hidden because not significant (4): html5lib, logging_simple, asyncio_websockets, logging_format
Ignored benchmarks (20) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250505-3.14.0a7+-0eeaa0e-CLANG,NOGIL/bm-20250505-vultr-x86_64-python-0eeaa0ef8bf60fd3b144-3.14.0a7+-0eeaa0e.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.054x faster

# HPT report

- Reliability score: 61.57% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.46x