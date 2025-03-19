# Results vs. 3.12.6

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: c1b42db
- commit date: 2025-03-18
- overall geometric mean: 1.049x faster
- HPT reliability: 53.59%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.40x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250318-vultr-x86_64-python-main-3.14.0a6+-c1b42db |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 275 ms: 1.04x slower                                   |
| html5lib       | 63.6 ms                                                | 65.3 ms: 1.03x slower                                  |
| Geometric mean | (ref)                                                  | 1.02x slower                                           |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250318-vultr-x86_64-python-main-3.14.0a6+-c1b42db |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 492 ms: 2.25x faster                                   |
| async_tree_none_tg         | 446 ms                                                 | 215 ms: 2.07x faster                                   |
| async_tree_io              | 1.08 sec                                               | 529 ms: 2.05x faster                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 275 ms: 2.03x faster                                   |
| async_tree_none            | 464 ms                                                 | 252 ms: 1.84x faster                                   |
| async_tree_memoization     | 555 ms                                                 | 310 ms: 1.79x faster                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 431 ms: 1.68x faster                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 466 ms: 1.53x faster                                   |
| async_generators           | 384 ms                                                 | 324 ms: 1.19x faster                                   |
| coroutines                 | 23.9 ms                                                | 20.2 ms: 1.18x faster                                  |
| Geometric mean             | (ref)                                                  | 1.64x faster                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250318-vultr-x86_64-python-main-3.14.0a6+-c1b42db |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| float          | 80.8 ms                                                | 68.0 ms: 1.19x faster                                  |
| pidigits       | 184 ms                                                 | 186 ms: 1.01x slower                                   |
| nbody          | 89.3 ms                                                | 119 ms: 1.34x slower                                   |
| Geometric mean | (ref)                                                  | 1.04x slower                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250318-vultr-x86_64-python-main-3.14.0a6+-c1b42db |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 138 ms: 1.03x faster                                   |
| regex_effbot   | 3.17 ms                                                | 3.26 ms: 1.03x slower                                  |
| regex_v8       | 20.6 ms                                                | 21.3 ms: 1.04x slower                                  |
| regex_dna      | 168 ms                                                 | 202 ms: 1.20x slower                                   |
| Geometric mean | (ref)                                                  | 1.06x slower                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250318-vultr-x86_64-python-main-3.14.0a6+-c1b42db |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 84.3 ms: 1.15x faster                                  |
| xml_etree_parse      | 139 ms                                                 | 139 ms: 1.00x slower                                   |
| tomli_loads          | 2.11 sec                                               | 2.13 sec: 1.01x slower                                 |
| unpickle_pure_python | 221 us                                                 | 224 us: 1.02x slower                                   |
| xml_etree_process    | 59.0 ms                                                | 60.0 ms: 1.02x slower                                  |
| pickle_pure_python   | 308 us                                                 | 325 us: 1.06x slower                                   |
| json_loads           | 26.5 us                                                | 29.7 us: 1.12x slower                                  |
| json_dumps           | 10.4 ms                                                | 12.5 ms: 1.21x slower                                  |
| Geometric mean       | (ref)                                                  | 1.03x slower                                           |

Benchmark hidden because not significant (1): xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250318-vultr-x86_64-python-main-3.14.0a6+-c1b42db |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 11.0 ms: 1.53x slower                                  |
| python_startup         | 9.93 ms                                                | 15.5 ms: 1.56x slower                                  |
| Geometric mean         | (ref)                                                  | 1.55x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250318-vultr-x86_64-python-main-3.14.0a6+-c1b42db |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 52.0 ms: 1.04x slower                                  |
| genshi_text     | 22.8 ms                                                | 24.2 ms: 1.06x slower                                  |
| django_template | 34.7 ms                                                | 37.0 ms: 1.07x slower                                  |
| mako            | 11.0 ms                                                | 14.8 ms: 1.34x slower                                  |
| Geometric mean  | (ref)                                                  | 1.12x slower                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250318-vultr-x86_64-python-main-3.14.0a6+-c1b42db |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 492 ms: 2.25x faster                                   |
| async_tree_none_tg         | 446 ms                                                 | 215 ms: 2.07x faster                                   |
| async_tree_io              | 1.08 sec                                               | 529 ms: 2.05x faster                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 275 ms: 2.03x faster                                   |
| async_tree_none            | 464 ms                                                 | 252 ms: 1.84x faster                                   |
| async_tree_memoization     | 555 ms                                                 | 310 ms: 1.79x faster                                   |
| gc_traversal               | 3.46 ms                                                | 1.94 ms: 1.78x faster                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 431 ms: 1.68x faster                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 466 ms: 1.53x faster                                   |
| deepcopy                   | 352 us                                                 | 268 us: 1.31x faster                                   |
| logging_silent             | 109 ns                                                 | 87.0 ns: 1.25x faster                                  |
| deepcopy_memo              | 40.3 us                                                | 33.7 us: 1.19x faster                                  |
| float                      | 80.8 ms                                                | 68.0 ms: 1.19x faster                                  |
| generators                 | 32.2 ms                                                | 27.1 ms: 1.19x faster                                  |
| async_generators           | 384 ms                                                 | 324 ms: 1.19x faster                                   |
| coroutines                 | 23.9 ms                                                | 20.2 ms: 1.18x faster                                  |
| scimark_sor                | 130 ms                                                 | 112 ms: 1.16x faster                                   |
| spectral_norm              | 110 ms                                                 | 96.1 ms: 1.15x faster                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 84.3 ms: 1.15x faster                                  |
| go                         | 139 ms                                                 | 122 ms: 1.14x faster                                   |
| pathlib                    | 21.5 ms                                                | 19.0 ms: 1.13x faster                                  |
| comprehensions             | 19.8 us                                                | 17.6 us: 1.13x faster                                  |
| dulwich_log                | 78.9 ms                                                | 70.4 ms: 1.12x faster                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.77 us: 1.11x faster                                  |
| pylint                     | 319 ms                                                 | 291 ms: 1.09x faster                                   |
| sqlite_synth               | 2.20 us                                                | 2.02 us: 1.09x faster                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.39 sec: 1.08x faster                                 |
| raytrace                   | 299 ms                                                 | 283 ms: 1.06x faster                                   |
| pycparser                  | 1.17 sec                                               | 1.12 sec: 1.04x faster                                 |
| chaos                      | 62.8 ms                                                | 60.7 ms: 1.04x faster                                  |
| regex_compile              | 142 ms                                                 | 138 ms: 1.03x faster                                   |
| logging_simple             | 6.63 us                                                | 6.48 us: 1.02x faster                                  |
| pyflate                    | 448 ms                                                 | 443 ms: 1.01x faster                                   |
| xml_etree_parse            | 139 ms                                                 | 139 ms: 1.00x slower                                   |
| logging_format             | 7.35 us                                                | 7.41 us: 1.01x slower                                  |
| tomli_loads                | 2.11 sec                                               | 2.13 sec: 1.01x slower                                 |
| scimark_lu                 | 114 ms                                                 | 115 ms: 1.01x slower                                   |
| pidigits                   | 184 ms                                                 | 186 ms: 1.01x slower                                   |
| scimark_monte_carlo        | 68.4 ms                                                | 69.3 ms: 1.01x slower                                  |
| richards                   | 45.9 ms                                                | 46.6 ms: 1.01x slower                                  |
| unpickle_pure_python       | 221 us                                                 | 224 us: 1.02x slower                                   |
| xml_etree_process          | 59.0 ms                                                | 60.0 ms: 1.02x slower                                  |
| deltablue                  | 3.45 ms                                                | 3.52 ms: 1.02x slower                                  |
| html5lib                   | 63.6 ms                                                | 65.3 ms: 1.03x slower                                  |
| regex_effbot               | 3.17 ms                                                | 3.26 ms: 1.03x slower                                  |
| sqlalchemy_imperative      | 21.8 ms                                                | 22.5 ms: 1.03x slower                                  |
| sympy_sum                  | 166 ms                                                 | 171 ms: 1.03x slower                                   |
| json                       | 5.02 ms                                                | 5.18 ms: 1.03x slower                                  |
| pprint_safe_repr           | 743 ms                                                 | 769 ms: 1.04x slower                                   |
| regex_v8                   | 20.6 ms                                                | 21.3 ms: 1.04x slower                                  |
| genshi_xml                 | 50.2 ms                                                | 52.0 ms: 1.04x slower                                  |
| crypto_pyaes               | 76.6 ms                                                | 79.5 ms: 1.04x slower                                  |
| sqlalchemy_declarative     | 143 ms                                                 | 149 ms: 1.04x slower                                   |
| sympy_str                  | 292 ms                                                 | 304 ms: 1.04x slower                                   |
| 2to3                       | 264 ms                                                 | 275 ms: 1.04x slower                                   |
| pprint_pformat             | 1.52 sec                                               | 1.59 sec: 1.05x slower                                 |
| thrift                     | 791 us                                                 | 832 us: 1.05x slower                                   |
| typing_runtime_protocols   | 163 us                                                 | 172 us: 1.05x slower                                   |
| pickle_pure_python         | 308 us                                                 | 325 us: 1.06x slower                                   |
| nqueens                    | 80.1 ms                                                | 84.7 ms: 1.06x slower                                  |
| richards_super             | 51.9 ms                                                | 55.0 ms: 1.06x slower                                  |
| genshi_text                | 22.8 ms                                                | 24.2 ms: 1.06x slower                                  |
| hexiom                     | 6.17 ms                                                | 6.57 ms: 1.06x slower                                  |
| django_template            | 34.7 ms                                                | 37.0 ms: 1.07x slower                                  |
| sympy_integrate            | 20.5 ms                                                | 22.0 ms: 1.07x slower                                  |
| sympy_expand               | 468 ms                                                 | 500 ms: 1.07x slower                                   |
| json_loads                 | 26.5 us                                                | 29.7 us: 1.12x slower                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.92 ms: 1.12x slower                                  |
| mdp                        | 2.42 sec                                               | 2.74 sec: 1.13x slower                                 |
| fannkuch                   | 372 ms                                                 | 435 ms: 1.17x slower                                   |
| meteor_contest             | 104 ms                                                 | 122 ms: 1.18x slower                                   |
| coverage                   | 71.4 ms                                                | 85.3 ms: 1.19x slower                                  |
| regex_dna                  | 168 ms                                                 | 202 ms: 1.20x slower                                   |
| json_dumps                 | 10.4 ms                                                | 12.5 ms: 1.21x slower                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.34 ms: 1.23x slower                                  |
| telco                      | 6.53 ms                                                | 8.02 ms: 1.23x slower                                  |
| nbody                      | 89.3 ms                                                | 119 ms: 1.34x slower                                   |
| mako                       | 11.0 ms                                                | 14.8 ms: 1.34x slower                                  |
| python_startup_no_site     | 7.16 ms                                                | 11.0 ms: 1.53x slower                                  |
| python_startup             | 9.93 ms                                                | 15.5 ms: 1.56x slower                                  |
| bench_thread_pool          | 941 us                                                 | 3.11 ms: 3.30x slower                                  |
| bench_mp_pool              | 10.8 ms                                                | 95.1 ms: 8.81x slower                                  |
| Geometric mean             | (ref)                                                  | 1.01x faster                                           |

Benchmark hidden because not significant (4): docutils, scimark_fft, xml_etree_generate, asyncio_websockets
Ignored benchmarks (19) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250318-3.14.0a6+-c1b42db-CLANG,NOGIL/bm-20250318-vultr-x86_64-python-main-3.14.0a6+-c1b42db.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.049x faster

# HPT report

- Reliability score: 53.59% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.40x