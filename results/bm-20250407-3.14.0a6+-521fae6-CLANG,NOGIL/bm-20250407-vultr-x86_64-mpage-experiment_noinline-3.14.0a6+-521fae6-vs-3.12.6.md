# Results vs. 3.12.6

- fork: mpage
- ref: experiment_noinline
- machine: linux-x86_64
- commit hash: 521fae6
- commit date: 2025-04-07
- overall geometric mean: 1.086x faster
- HPT reliability: 98.16%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.41x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 271 ms: 1.03x slower                                                 |
| docutils       | 2.64 sec                                               | 2.62 sec: 1.01x faster                                               |
| html5lib       | 63.6 ms                                                | 60.8 ms: 1.05x faster                                                |
| Geometric mean | (ref)                                                  | 1.01x faster                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 481 ms: 2.31x faster                                                 |
| async_tree_none_tg         | 446 ms                                                 | 209 ms: 2.13x faster                                                 |
| async_tree_memoization_tg  | 560 ms                                                 | 262 ms: 2.13x faster                                                 |
| async_tree_io              | 1.08 sec                                               | 509 ms: 2.13x faster                                                 |
| async_tree_none            | 464 ms                                                 | 243 ms: 1.91x faster                                                 |
| async_tree_memoization     | 555 ms                                                 | 291 ms: 1.91x faster                                                 |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 426 ms: 1.70x faster                                                 |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 454 ms: 1.58x faster                                                 |
| coroutines                 | 23.9 ms                                                | 19.7 ms: 1.22x faster                                                |
| async_generators           | 384 ms                                                 | 321 ms: 1.20x faster                                                 |
| Geometric mean             | (ref)                                                  | 1.69x faster                                                         |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 63.8 ms: 1.27x faster                                                |
| pidigits       | 184 ms                                                 | 186 ms: 1.01x slower                                                 |
| nbody          | 89.3 ms                                                | 108 ms: 1.21x slower                                                 |
| Geometric mean | (ref)                                                  | 1.01x faster                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.96 ms: 1.07x faster                                                |
| regex_compile  | 142 ms                                                 | 133 ms: 1.07x faster                                                 |
| regex_v8       | 20.6 ms                                                | 21.6 ms: 1.05x slower                                                |
| regex_dna      | 168 ms                                                 | 179 ms: 1.07x slower                                                 |
| Geometric mean | (ref)                                                  | 1.00x faster                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 84.3 ms: 1.15x faster                                                |
| tomli_loads          | 2.11 sec                                               | 1.97 sec: 1.07x faster                                               |
| xml_etree_generate   | 85.2 ms                                                | 83.5 ms: 1.02x faster                                                |
| unpickle_pure_python | 221 us                                                 | 222 us: 1.01x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 59.6 ms: 1.01x slower                                                |
| xml_etree_parse      | 139 ms                                                 | 141 ms: 1.01x slower                                                 |
| pickle_pure_python   | 308 us                                                 | 317 us: 1.03x slower                                                 |
| json_loads           | 26.5 us                                                | 29.5 us: 1.11x slower                                                |
| json_dumps           | 10.4 ms                                                | 12.7 ms: 1.23x slower                                                |
| Geometric mean       | (ref)                                                  | 1.02x slower                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 11.0 ms: 1.54x slower                                                |
| python_startup         | 9.93 ms                                                | 15.5 ms: 1.56x slower                                                |
| Geometric mean         | (ref)                                                  | 1.55x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 51.2 ms: 1.02x slower                                                |
| genshi_text     | 22.8 ms                                                | 23.6 ms: 1.03x slower                                                |
| django_template | 34.7 ms                                                | 37.4 ms: 1.08x slower                                                |
| mako            | 11.0 ms                                                | 14.4 ms: 1.30x slower                                                |
| Geometric mean  | (ref)                                                  | 1.10x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 481 ms: 2.31x faster                                                 |
| async_tree_none_tg         | 446 ms                                                 | 209 ms: 2.13x faster                                                 |
| async_tree_memoization_tg  | 560 ms                                                 | 262 ms: 2.13x faster                                                 |
| async_tree_io              | 1.08 sec                                               | 509 ms: 2.13x faster                                                 |
| mdp                        | 2.42 sec                                               | 1.25 sec: 1.94x faster                                               |
| async_tree_none            | 464 ms                                                 | 243 ms: 1.91x faster                                                 |
| async_tree_memoization     | 555 ms                                                 | 291 ms: 1.91x faster                                                 |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 426 ms: 1.70x faster                                                 |
| gc_traversal               | 3.46 ms                                                | 2.09 ms: 1.66x faster                                                |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 454 ms: 1.58x faster                                                 |
| deepcopy                   | 352 us                                                 | 255 us: 1.38x faster                                                 |
| logging_silent             | 109 ns                                                 | 83.9 ns: 1.30x faster                                                |
| float                      | 80.8 ms                                                | 63.8 ms: 1.27x faster                                                |
| deepcopy_memo              | 40.3 us                                                | 32.2 us: 1.25x faster                                                |
| coroutines                 | 23.9 ms                                                | 19.7 ms: 1.22x faster                                                |
| async_generators           | 384 ms                                                 | 321 ms: 1.20x faster                                                 |
| scimark_sor                | 130 ms                                                 | 108 ms: 1.20x faster                                                 |
| deepcopy_reduce            | 3.08 us                                                | 2.59 us: 1.19x faster                                                |
| go                         | 139 ms                                                 | 117 ms: 1.19x faster                                                 |
| comprehensions             | 19.8 us                                                | 17.0 us: 1.17x faster                                                |
| pathlib                    | 21.5 ms                                                | 18.5 ms: 1.16x faster                                                |
| spectral_norm              | 110 ms                                                 | 95.1 ms: 1.16x faster                                                |
| xml_etree_iterparse        | 96.7 ms                                                | 84.3 ms: 1.15x faster                                                |
| generators                 | 32.2 ms                                                | 28.1 ms: 1.15x faster                                                |
| chaos                      | 62.8 ms                                                | 55.7 ms: 1.13x faster                                                |
| dulwich_log                | 78.9 ms                                                | 70.6 ms: 1.12x faster                                                |
| sqlite_synth               | 2.20 us                                                | 1.97 us: 1.12x faster                                                |
| bpe_tokeniser              | 4.74 sec                                               | 4.27 sec: 1.11x faster                                               |
| raytrace                   | 299 ms                                                 | 270 ms: 1.11x faster                                                 |
| pylint                     | 319 ms                                                 | 291 ms: 1.10x faster                                                 |
| scimark_fft                | 342 ms                                                 | 313 ms: 1.09x faster                                                 |
| tomli_loads                | 2.11 sec                                               | 1.97 sec: 1.07x faster                                               |
| regex_effbot               | 3.17 ms                                                | 2.96 ms: 1.07x faster                                                |
| regex_compile              | 142 ms                                                 | 133 ms: 1.07x faster                                                 |
| pycparser                  | 1.17 sec                                               | 1.11 sec: 1.05x faster                                               |
| html5lib                   | 63.6 ms                                                | 60.8 ms: 1.05x faster                                                |
| logging_simple             | 6.63 us                                                | 6.44 us: 1.03x faster                                                |
| scimark_monte_carlo        | 68.4 ms                                                | 66.4 ms: 1.03x faster                                                |
| scimark_lu                 | 114 ms                                                 | 111 ms: 1.03x faster                                                 |
| xml_etree_generate         | 85.2 ms                                                | 83.5 ms: 1.02x faster                                                |
| nqueens                    | 80.1 ms                                                | 78.6 ms: 1.02x faster                                                |
| richards                   | 45.9 ms                                                | 45.3 ms: 1.02x faster                                                |
| pyflate                    | 448 ms                                                 | 442 ms: 1.01x faster                                                 |
| docutils                   | 2.64 sec                                               | 2.62 sec: 1.01x faster                                               |
| unpickle_pure_python       | 221 us                                                 | 222 us: 1.01x slower                                                 |
| deltablue                  | 3.45 ms                                                | 3.47 ms: 1.01x slower                                                |
| sympy_integrate            | 20.5 ms                                                | 20.7 ms: 1.01x slower                                                |
| pprint_safe_repr           | 743 ms                                                 | 750 ms: 1.01x slower                                                 |
| pidigits                   | 184 ms                                                 | 186 ms: 1.01x slower                                                 |
| pprint_pformat             | 1.52 sec                                               | 1.54 sec: 1.01x slower                                               |
| xml_etree_process          | 59.0 ms                                                | 59.6 ms: 1.01x slower                                                |
| hexiom                     | 6.17 ms                                                | 6.25 ms: 1.01x slower                                                |
| sympy_sum                  | 166 ms                                                 | 168 ms: 1.01x slower                                                 |
| xml_etree_parse            | 139 ms                                                 | 141 ms: 1.01x slower                                                 |
| genshi_xml                 | 50.2 ms                                                | 51.2 ms: 1.02x slower                                                |
| crypto_pyaes               | 76.6 ms                                                | 78.3 ms: 1.02x slower                                                |
| json                       | 5.02 ms                                                | 5.16 ms: 1.03x slower                                                |
| sympy_str                  | 292 ms                                                 | 300 ms: 1.03x slower                                                 |
| richards_super             | 51.9 ms                                                | 53.3 ms: 1.03x slower                                                |
| sqlalchemy_declarative     | 143 ms                                                 | 147 ms: 1.03x slower                                                 |
| 2to3                       | 264 ms                                                 | 271 ms: 1.03x slower                                                 |
| pickle_pure_python         | 308 us                                                 | 317 us: 1.03x slower                                                 |
| sqlalchemy_imperative      | 21.8 ms                                                | 22.5 ms: 1.03x slower                                                |
| genshi_text                | 22.8 ms                                                | 23.6 ms: 1.03x slower                                                |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.58 ms: 1.04x slower                                                |
| regex_v8                   | 20.6 ms                                                | 21.6 ms: 1.05x slower                                                |
| sympy_expand               | 468 ms                                                 | 497 ms: 1.06x slower                                                 |
| typing_runtime_protocols   | 163 us                                                 | 174 us: 1.07x slower                                                 |
| regex_dna                  | 168 ms                                                 | 179 ms: 1.07x slower                                                 |
| django_template            | 34.7 ms                                                | 37.4 ms: 1.08x slower                                                |
| fannkuch                   | 372 ms                                                 | 409 ms: 1.10x slower                                                 |
| json_loads                 | 26.5 us                                                | 29.5 us: 1.11x slower                                                |
| telco                      | 6.53 ms                                                | 7.60 ms: 1.16x slower                                                |
| meteor_contest             | 104 ms                                                 | 122 ms: 1.18x slower                                                 |
| nbody                      | 89.3 ms                                                | 108 ms: 1.21x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.33 ms: 1.22x slower                                                |
| json_dumps                 | 10.4 ms                                                | 12.7 ms: 1.23x slower                                                |
| mako                       | 11.0 ms                                                | 14.4 ms: 1.30x slower                                                |
| coverage                   | 71.4 ms                                                | 94.9 ms: 1.33x slower                                                |
| python_startup_no_site     | 7.16 ms                                                | 11.0 ms: 1.54x slower                                                |
| python_startup             | 9.93 ms                                                | 15.5 ms: 1.56x slower                                                |
| bench_thread_pool          | 941 us                                                 | 3.07 ms: 3.27x slower                                                |
| bench_mp_pool              | 10.8 ms                                                | 93.7 ms: 8.68x slower                                                |
| Geometric mean             | (ref)                                                  | 1.05x faster                                                         |

Benchmark hidden because not significant (2): asyncio_websockets, logging_format
Ignored benchmarks (20) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250407-3.14.0a6+-521fae6-CLANG,NOGIL/bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.086x faster

# HPT report

- Reliability score: 98.16% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.41x