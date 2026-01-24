# Results vs. 3.12.6

- fork: Fidget-Spinner
- ref: loop_2000
- machine: linux-x86_64
- commit hash: cec96a9
- commit date: 2026-01-24
- overall geometric mean: 1.137x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260124-vultr-x86_64-Fidget%2dSpinner-loop_2000-3.15.0a5+-cec96a9 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 254 ms: 1.04x faster                                                  |
| docutils       | 2.64 sec                                               | 2.66 sec: 1.01x slower                                                |
| Geometric mean | (ref)                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260124-vultr-x86_64-Fidget%2dSpinner-loop_2000-3.15.0a5+-cec96a9 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 555 ms: 2.00x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 541 ms: 2.00x faster                                                  |
| async_tree_none            | 464 ms                                                 | 236 ms: 1.97x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 292 ms: 1.92x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 292 ms: 1.90x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 243 ms: 1.84x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 479 ms: 1.49x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 487 ms: 1.48x faster                                                  |
| async_generators           | 384 ms                                                 | 355 ms: 1.08x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.5 ms: 1.02x faster                                                 |
| asyncio_websockets         | 517 ms                                                 | 545 ms: 1.06x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.55x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260124-vultr-x86_64-Fidget%2dSpinner-loop_2000-3.15.0a5+-cec96a9 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 57.9 ms: 1.40x faster                                                 |
| nbody          | 89.3 ms                                                | 72.8 ms: 1.23x faster                                                 |
| pidigits       | 184 ms                                                 | 197 ms: 1.07x slower                                                  |
| Geometric mean | (ref)                                                  | 1.17x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260124-vultr-x86_64-Fidget%2dSpinner-loop_2000-3.15.0a5+-cec96a9 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.65 ms: 1.19x faster                                                 |
| regex_compile  | 142 ms                                                 | 122 ms: 1.17x faster                                                  |
| regex_dna      | 168 ms                                                 | 168 ms: 1.00x slower                                                  |
| regex_v8       | 20.6 ms                                                | 20.8 ms: 1.01x slower                                                 |
| Geometric mean | (ref)                                                  | 1.08x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260124-vultr-x86_64-Fidget%2dSpinner-loop_2000-3.15.0a5+-cec96a9 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.67 sec: 1.26x faster                                                |
| unpickle_pure_python | 221 us                                                 | 178 us: 1.24x faster                                                  |
| xml_etree_iterparse  | 96.7 ms                                                | 83.4 ms: 1.16x faster                                                 |
| json_dumps           | 10.4 ms                                                | 9.01 ms: 1.15x faster                                                 |
| pickle_pure_python   | 308 us                                                 | 278 us: 1.11x faster                                                  |
| xml_etree_generate   | 85.2 ms                                                | 77.2 ms: 1.10x faster                                                 |
| xml_etree_process    | 59.0 ms                                                | 53.6 ms: 1.10x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.08x faster                                                  |
| json_loads           | 26.5 us                                                | 28.1 us: 1.06x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.12x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260124-vultr-x86_64-Fidget%2dSpinner-loop_2000-3.15.0a5+-cec96a9 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.37 ms: 1.03x slower                                                 |
| python_startup         | 9.93 ms                                                | 12.6 ms: 1.27x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.14x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260124-vultr-x86_64-Fidget%2dSpinner-loop_2000-3.15.0a5+-cec96a9 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 20.7 ms: 1.10x faster                                                 |
| mako            | 11.0 ms                                                | 10.3 ms: 1.07x faster                                                 |
| django_template | 34.7 ms                                                | 35.4 ms: 1.02x slower                                                 |
| genshi_xml      | 50.2 ms                                                | 51.3 ms: 1.02x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.03x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260124-vultr-x86_64-Fidget%2dSpinner-loop_2000-3.15.0a5+-cec96a9 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| richards                   | 45.9 ms                                                | 17.4 ms: 2.63x faster                                                 |
| richards_super             | 51.9 ms                                                | 21.0 ms: 2.47x faster                                                 |
| async_tree_io_tg           | 1.11 sec                                               | 555 ms: 2.00x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 541 ms: 2.00x faster                                                  |
| async_tree_none            | 464 ms                                                 | 236 ms: 1.97x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 292 ms: 1.92x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 292 ms: 1.90x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 243 ms: 1.84x faster                                                  |
| mdp                        | 2.42 sec                                               | 1.36 sec: 1.78x faster                                                |
| deepcopy_memo              | 40.3 us                                                | 22.6 us: 1.78x faster                                                 |
| deepcopy                   | 352 us                                                 | 222 us: 1.58x faster                                                  |
| scimark_sor                | 130 ms                                                 | 84.8 ms: 1.53x faster                                                 |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 479 ms: 1.49x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 487 ms: 1.48x faster                                                  |
| scimark_lu                 | 114 ms                                                 | 77.5 ms: 1.47x faster                                                 |
| float                      | 80.8 ms                                                | 57.9 ms: 1.40x faster                                                 |
| spectral_norm              | 110 ms                                                 | 80.9 ms: 1.36x faster                                                 |
| go                         | 139 ms                                                 | 103 ms: 1.35x faster                                                  |
| logging_silent             | 109 ns                                                 | 81.2 ns: 1.34x faster                                                 |
| scimark_fft                | 342 ms                                                 | 255 ms: 1.34x faster                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 52.1 ms: 1.31x faster                                                 |
| deepcopy_reduce            | 3.08 us                                                | 2.38 us: 1.29x faster                                                 |
| tomli_loads                | 2.11 sec                                               | 1.67 sec: 1.26x faster                                                |
| deltablue                  | 3.45 ms                                                | 2.74 ms: 1.26x faster                                                 |
| pathlib                    | 21.5 ms                                                | 17.3 ms: 1.24x faster                                                 |
| unpickle_pure_python       | 221 us                                                 | 178 us: 1.24x faster                                                  |
| comprehensions             | 19.8 us                                                | 16.1 us: 1.23x faster                                                 |
| nbody                      | 89.3 ms                                                | 72.8 ms: 1.23x faster                                                 |
| pprint_pformat             | 1.52 sec                                               | 1.25 sec: 1.21x faster                                                |
| pyflate                    | 448 ms                                                 | 372 ms: 1.21x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 3.94 sec: 1.20x faster                                                |
| pprint_safe_repr           | 743 ms                                                 | 621 ms: 1.20x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.65 ms: 1.19x faster                                                 |
| crypto_pyaes               | 76.6 ms                                                | 65.1 ms: 1.18x faster                                                 |
| regex_compile              | 142 ms                                                 | 122 ms: 1.17x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 83.4 ms: 1.16x faster                                                 |
| chaos                      | 62.8 ms                                                | 54.2 ms: 1.16x faster                                                 |
| json_dumps                 | 10.4 ms                                                | 9.01 ms: 1.15x faster                                                 |
| generators                 | 32.2 ms                                                | 28.2 ms: 1.14x faster                                                 |
| raytrace                   | 299 ms                                                 | 265 ms: 1.13x faster                                                  |
| pickle_pure_python         | 308 us                                                 | 278 us: 1.11x faster                                                  |
| xml_etree_generate         | 85.2 ms                                                | 77.2 ms: 1.10x faster                                                 |
| genshi_text                | 22.8 ms                                                | 20.7 ms: 1.10x faster                                                 |
| xml_etree_process          | 59.0 ms                                                | 53.6 ms: 1.10x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 72.3 ms: 1.09x faster                                                 |
| async_generators           | 384 ms                                                 | 355 ms: 1.08x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.08x faster                                                  |
| fannkuch                   | 372 ms                                                 | 347 ms: 1.07x faster                                                  |
| logging_simple             | 6.63 us                                                | 6.17 us: 1.07x faster                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.09 ms: 1.07x faster                                                 |
| mako                       | 11.0 ms                                                | 10.3 ms: 1.07x faster                                                 |
| logging_format             | 7.35 us                                                | 7.00 us: 1.05x faster                                                 |
| typing_runtime_protocols   | 163 us                                                 | 156 us: 1.05x faster                                                  |
| thrift                     | 791 us                                                 | 756 us: 1.05x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.13 sec: 1.04x faster                                                |
| 2to3                       | 264 ms                                                 | 254 ms: 1.04x faster                                                  |
| json                       | 5.02 ms                                                | 4.86 ms: 1.03x faster                                                 |
| meteor_contest             | 104 ms                                                 | 100 ms: 1.03x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.5 ms: 1.02x faster                                                 |
| nqueens                    | 80.1 ms                                                | 78.9 ms: 1.01x faster                                                 |
| regex_dna                  | 168 ms                                                 | 168 ms: 1.00x slower                                                  |
| hexiom                     | 6.17 ms                                                | 6.20 ms: 1.00x slower                                                 |
| docutils                   | 2.64 sec                                               | 2.66 sec: 1.01x slower                                                |
| regex_v8                   | 20.6 ms                                                | 20.8 ms: 1.01x slower                                                 |
| sympy_integrate            | 20.5 ms                                                | 20.9 ms: 1.02x slower                                                 |
| django_template            | 34.7 ms                                                | 35.4 ms: 1.02x slower                                                 |
| genshi_xml                 | 50.2 ms                                                | 51.3 ms: 1.02x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 7.37 ms: 1.03x slower                                                 |
| asyncio_websockets         | 517 ms                                                 | 545 ms: 1.06x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 176 ms: 1.06x slower                                                  |
| json_loads                 | 26.5 us                                                | 28.1 us: 1.06x slower                                                 |
| sympy_str                  | 292 ms                                                 | 310 ms: 1.06x slower                                                  |
| pidigits                   | 184 ms                                                 | 197 ms: 1.07x slower                                                  |
| sympy_expand               | 468 ms                                                 | 517 ms: 1.11x slower                                                  |
| coverage                   | 71.4 ms                                                | 81.9 ms: 1.15x slower                                                 |
| gc_traversal               | 3.46 ms                                                | 4.35 ms: 1.26x slower                                                 |
| python_startup             | 9.93 ms                                                | 12.6 ms: 1.27x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 1.32 ms: 1.40x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.85 ms: 1.69x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 183 ms: 16.98x slower                                                 |
| telco                      | 6.53 ms                                                | 166 ms: 25.44x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.09x faster                                                          |

Benchmark hidden because not significant (3): html5lib, sqlite_synth, pylint
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260124-3.15.0a5+-cec96a9-JIT/bm-20260124-vultr-x86_64-Fidget%2dSpinner-loop_2000-3.15.0a5+-cec96a9.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.137x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.10x
- 95% likely to have a speedup of 1.09x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: 1.19x