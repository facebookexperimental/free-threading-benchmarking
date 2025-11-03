# Results vs. 3.12.6

- fork: python
- ref: e66f87ca73516efb4aec
- machine: linux-x86_64
- commit hash: e66f87c
- commit date: 2025-11-02
- overall geometric mean: 1.079x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251102-vultr-x86_64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 247 ms: 1.06x faster                                                   |
| docutils       | 2.64 sec                                               | 2.57 sec: 1.03x faster                                                 |
| html5lib       | 63.6 ms                                                | 60.8 ms: 1.05x faster                                                  |
| Geometric mean | (ref)                                                  | 1.05x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251102-vultr-x86_64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 1.08 sec                                               | 557 ms: 1.94x faster                                                   |
| async_tree_none            | 464 ms                                                 | 246 ms: 1.89x faster                                                   |
| async_tree_io_tg           | 1.11 sec                                               | 593 ms: 1.87x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 308 ms: 1.81x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 246 ms: 1.81x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 308 ms: 1.80x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 509 ms: 1.42x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 510 ms: 1.40x faster                                                   |
| async_generators           | 384 ms                                                 | 337 ms: 1.14x faster                                                   |
| coroutines                 | 23.9 ms                                                | 24.1 ms: 1.01x slower                                                  |
| asyncio_websockets         | 517 ms                                                 | 545 ms: 1.05x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.50x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251102-vultr-x86_64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 69.2 ms: 1.17x faster                                                  |
| nbody          | 89.3 ms                                                | 86.9 ms: 1.03x faster                                                  |
| pidigits       | 184 ms                                                 | 214 ms: 1.16x slower                                                   |
| Geometric mean | (ref)                                                  | 1.01x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251102-vultr-x86_64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.64 ms: 1.20x faster                                                  |
| regex_compile  | 142 ms                                                 | 124 ms: 1.15x faster                                                   |
| regex_dna      | 168 ms                                                 | 173 ms: 1.03x slower                                                   |
| regex_v8       | 20.6 ms                                                | 22.2 ms: 1.08x slower                                                  |
| Geometric mean | (ref)                                                  | 1.06x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251102-vultr-x86_64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 84.4 ms: 1.15x faster                                                  |
| tomli_loads          | 2.11 sec                                               | 1.90 sec: 1.11x faster                                                 |
| json_dumps           | 10.4 ms                                                | 9.49 ms: 1.09x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.08x faster                                                   |
| unpickle_pure_python | 221 us                                                 | 211 us: 1.04x faster                                                   |
| xml_etree_generate   | 85.2 ms                                                | 82.4 ms: 1.03x faster                                                  |
| xml_etree_process    | 59.0 ms                                                | 58.4 ms: 1.01x faster                                                  |
| pickle_pure_python   | 308 us                                                 | 306 us: 1.00x faster                                                   |
| json_loads           | 26.5 us                                                | 27.9 us: 1.05x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.05x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251102-vultr-x86_64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.20 ms: 1.01x slower                                                  |
| python_startup         | 9.93 ms                                                | 12.3 ms: 1.24x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.12x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251102-vultr-x86_64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 20.6 ms: 1.11x faster                                                  |
| genshi_xml      | 50.2 ms                                                | 47.8 ms: 1.05x faster                                                  |
| django_template | 34.7 ms                                                | 35.1 ms: 1.01x slower                                                  |
| mako            | 11.0 ms                                                | 11.9 ms: 1.08x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.01x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251102-vultr-x86_64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.14 sec: 2.11x faster                                                 |
| async_tree_io              | 1.08 sec                                               | 557 ms: 1.94x faster                                                   |
| async_tree_none            | 464 ms                                                 | 246 ms: 1.89x faster                                                   |
| async_tree_io_tg           | 1.11 sec                                               | 593 ms: 1.87x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 308 ms: 1.81x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 246 ms: 1.81x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 308 ms: 1.80x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 26.5 us: 1.52x faster                                                  |
| deepcopy                   | 352 us                                                 | 245 us: 1.44x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 509 ms: 1.42x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 510 ms: 1.40x faster                                                   |
| go                         | 139 ms                                                 | 105 ms: 1.33x faster                                                   |
| comprehensions             | 19.8 us                                                | 15.9 us: 1.25x faster                                                  |
| pathlib                    | 21.5 ms                                                | 17.7 ms: 1.22x faster                                                  |
| scimark_sor                | 130 ms                                                 | 107 ms: 1.21x faster                                                   |
| raytrace                   | 299 ms                                                 | 249 ms: 1.20x faster                                                   |
| regex_effbot               | 3.17 ms                                                | 2.64 ms: 1.20x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.58 us: 1.19x faster                                                  |
| float                      | 80.8 ms                                                | 69.2 ms: 1.17x faster                                                  |
| spectral_norm              | 110 ms                                                 | 95.0 ms: 1.16x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 68.4 ms: 1.15x faster                                                  |
| regex_compile              | 142 ms                                                 | 124 ms: 1.15x faster                                                   |
| xml_etree_iterparse        | 96.7 ms                                                | 84.4 ms: 1.15x faster                                                  |
| generators                 | 32.2 ms                                                | 28.2 ms: 1.15x faster                                                  |
| logging_simple             | 6.63 us                                                | 5.79 us: 1.14x faster                                                  |
| async_generators           | 384 ms                                                 | 337 ms: 1.14x faster                                                   |
| bpe_tokeniser              | 4.74 sec                                               | 4.20 sec: 1.13x faster                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 61.0 ms: 1.12x faster                                                  |
| chaos                      | 62.8 ms                                                | 56.0 ms: 1.12x faster                                                  |
| scimark_fft                | 342 ms                                                 | 305 ms: 1.12x faster                                                   |
| logging_format             | 7.35 us                                                | 6.58 us: 1.12x faster                                                  |
| genshi_text                | 22.8 ms                                                | 20.6 ms: 1.11x faster                                                  |
| hexiom                     | 6.17 ms                                                | 5.57 ms: 1.11x faster                                                  |
| pylint                     | 319 ms                                                 | 287 ms: 1.11x faster                                                   |
| tomli_loads                | 2.11 sec                                               | 1.90 sec: 1.11x faster                                                 |
| crypto_pyaes               | 76.6 ms                                                | 69.3 ms: 1.11x faster                                                  |
| pyflate                    | 448 ms                                                 | 406 ms: 1.10x faster                                                   |
| json_dumps                 | 10.4 ms                                                | 9.49 ms: 1.09x faster                                                  |
| richards                   | 45.9 ms                                                | 42.2 ms: 1.09x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.07 sec: 1.09x faster                                                 |
| richards_super             | 51.9 ms                                                | 47.8 ms: 1.09x faster                                                  |
| sympy_integrate            | 20.5 ms                                                | 19.0 ms: 1.08x faster                                                  |
| logging_silent             | 109 ns                                                 | 101 ns: 1.08x faster                                                   |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.08x faster                                                   |
| pprint_pformat             | 1.52 sec                                               | 1.42 sec: 1.07x faster                                                 |
| sympy_sum                  | 166 ms                                                 | 155 ms: 1.07x faster                                                   |
| pprint_safe_repr           | 743 ms                                                 | 696 ms: 1.07x faster                                                   |
| 2to3                       | 264 ms                                                 | 247 ms: 1.06x faster                                                   |
| sympy_str                  | 292 ms                                                 | 274 ms: 1.06x faster                                                   |
| scimark_lu                 | 114 ms                                                 | 108 ms: 1.06x faster                                                   |
| typing_runtime_protocols   | 163 us                                                 | 155 us: 1.05x faster                                                   |
| thrift                     | 791 us                                                 | 754 us: 1.05x faster                                                   |
| genshi_xml                 | 50.2 ms                                                | 47.8 ms: 1.05x faster                                                  |
| html5lib                   | 63.6 ms                                                | 60.8 ms: 1.05x faster                                                  |
| unpickle_pure_python       | 221 us                                                 | 211 us: 1.04x faster                                                   |
| deltablue                  | 3.45 ms                                                | 3.31 ms: 1.04x faster                                                  |
| nqueens                    | 80.1 ms                                                | 77.2 ms: 1.04x faster                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.24 ms: 1.04x faster                                                  |
| xml_etree_generate         | 85.2 ms                                                | 82.4 ms: 1.03x faster                                                  |
| nbody                      | 89.3 ms                                                | 86.9 ms: 1.03x faster                                                  |
| docutils                   | 2.64 sec                                               | 2.57 sec: 1.03x faster                                                 |
| meteor_contest             | 104 ms                                                 | 101 ms: 1.03x faster                                                   |
| xml_etree_process          | 59.0 ms                                                | 58.4 ms: 1.01x faster                                                  |
| pickle_pure_python         | 308 us                                                 | 306 us: 1.00x faster                                                   |
| python_startup_no_site     | 7.16 ms                                                | 7.20 ms: 1.01x slower                                                  |
| coroutines                 | 23.9 ms                                                | 24.1 ms: 1.01x slower                                                  |
| django_template            | 34.7 ms                                                | 35.1 ms: 1.01x slower                                                  |
| sympy_expand               | 468 ms                                                 | 475 ms: 1.02x slower                                                   |
| sqlite_synth               | 2.20 us                                                | 2.26 us: 1.03x slower                                                  |
| regex_dna                  | 168 ms                                                 | 173 ms: 1.03x slower                                                   |
| fannkuch                   | 372 ms                                                 | 387 ms: 1.04x slower                                                   |
| json_loads                 | 26.5 us                                                | 27.9 us: 1.05x slower                                                  |
| asyncio_websockets         | 517 ms                                                 | 545 ms: 1.05x slower                                                   |
| bench_thread_pool          | 941 us                                                 | 1.00 ms: 1.06x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 22.2 ms: 1.08x slower                                                  |
| mako                       | 11.0 ms                                                | 11.9 ms: 1.08x slower                                                  |
| coverage                   | 71.4 ms                                                | 81.1 ms: 1.14x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 12.4 ms: 1.15x slower                                                  |
| pidigits                   | 184 ms                                                 | 214 ms: 1.16x slower                                                   |
| gc_traversal               | 3.46 ms                                                | 4.09 ms: 1.18x slower                                                  |
| python_startup             | 9.93 ms                                                | 12.3 ms: 1.24x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.92 ms: 1.76x slower                                                  |
| telco                      | 6.53 ms                                                | 157 ms: 24.13x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.08x faster                                                           |

Benchmark hidden because not significant (1): json
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251102-3.15.0a1+-e66f87c/bm-20251102-vultr-x86_64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.079x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.16x