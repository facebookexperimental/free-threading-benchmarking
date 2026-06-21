# Results vs. 3.12.6

- fork: python
- ref: a9db5cb52fefffc8fcdd
- machine: linux-x86_64
- commit hash: a9db5cb
- commit date: 2026-06-19
- overall geometric mean: 1.078x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 256 ms: 1.03x faster                                                  |
| docutils       | 2.64 sec                                               | 2.40 sec: 1.10x faster                                                |
| html5lib       | 63.6 ms                                                | 60.0 ms: 1.06x faster                                                 |
| Geometric mean | (ref)                                                  | 1.06x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none            | 464 ms                                                 | 291 ms: 1.60x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 361 ms: 1.55x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 295 ms: 1.51x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 716 ms: 1.51x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 378 ms: 1.47x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 755 ms: 1.47x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 543 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 557 ms: 1.30x faster                                                  |
| async_generators           | 384 ms                                                 | 336 ms: 1.14x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.5 ms: 1.02x faster                                                 |
| asyncio_websockets         | 517 ms                                                 | 543 ms: 1.05x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.33x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 73.4 ms: 1.10x faster                                                 |
| pidigits       | 184 ms                                                 | 188 ms: 1.02x slower                                                  |
| Geometric mean | (ref)                                                  | 1.02x faster                                                          |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.69 ms: 1.18x faster                                                 |
| regex_compile  | 142 ms                                                 | 122 ms: 1.17x faster                                                  |
| regex_v8       | 20.6 ms                                                | 21.1 ms: 1.03x slower                                                 |
| regex_dna      | 168 ms                                                 | 175 ms: 1.04x slower                                                  |
| Geometric mean | (ref)                                                  | 1.06x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.83 sec: 1.15x faster                                                |
| xml_etree_iterparse  | 96.7 ms                                                | 89.6 ms: 1.08x faster                                                 |
| json_dumps           | 10.4 ms                                                | 9.76 ms: 1.06x faster                                                 |
| unpickle_pure_python | 221 us                                                 | 209 us: 1.05x faster                                                  |
| xml_etree_generate   | 85.2 ms                                                | 85.9 ms: 1.01x slower                                                 |
| json_loads           | 26.5 us                                                | 27.2 us: 1.03x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 60.6 ms: 1.03x slower                                                 |
| xml_etree_parse      | 139 ms                                                 | 144 ms: 1.04x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.03x faster                                                          |

Benchmark hidden because not significant (1): pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 6.94 ms: 1.03x faster                                                 |
| python_startup         | 9.93 ms                                                | 12.3 ms: 1.24x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.10x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.7 ms                                                | 35.1 ms: 1.01x slower                                                 |
| mako            | 11.0 ms                                                | 12.4 ms: 1.13x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.07x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 319 ms                                                 | 115 ms: 2.78x faster                                                  |
| mdp                        | 2.42 sec                                               | 1.13 sec: 2.14x faster                                                |
| async_tree_none            | 464 ms                                                 | 291 ms: 1.60x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 361 ms: 1.55x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 26.3 us: 1.53x faster                                                 |
| deepcopy                   | 352 us                                                 | 232 us: 1.51x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 295 ms: 1.51x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 716 ms: 1.51x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 378 ms: 1.47x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 755 ms: 1.47x faster                                                  |
| typing_runtime_protocols   | 163 us                                                 | 118 us: 1.38x faster                                                  |
| go                         | 139 ms                                                 | 102 ms: 1.37x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 543 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 557 ms: 1.30x faster                                                  |
| comprehensions             | 19.8 us                                                | 15.8 us: 1.26x faster                                                 |
| pathlib                    | 21.5 ms                                                | 17.7 ms: 1.22x faster                                                 |
| scimark_sor                | 130 ms                                                 | 107 ms: 1.21x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.57 us: 1.20x faster                                                 |
| spectral_norm              | 110 ms                                                 | 92.1 ms: 1.20x faster                                                 |
| raytrace                   | 299 ms                                                 | 251 ms: 1.19x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.69 ms: 1.18x faster                                                 |
| chaos                      | 62.8 ms                                                | 53.7 ms: 1.17x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 67.6 ms: 1.17x faster                                                 |
| regex_compile              | 142 ms                                                 | 122 ms: 1.17x faster                                                  |
| tomli_loads                | 2.11 sec                                               | 1.83 sec: 1.15x faster                                                |
| async_generators           | 384 ms                                                 | 336 ms: 1.14x faster                                                  |
| logging_simple             | 6.63 us                                                | 5.88 us: 1.13x faster                                                 |
| generators                 | 32.2 ms                                                | 28.6 ms: 1.13x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.22 sec: 1.12x faster                                                |
| logging_silent             | 109 ns                                                 | 98.0 ns: 1.11x faster                                                 |
| logging_format             | 7.35 us                                                | 6.62 us: 1.11x faster                                                 |
| pyflate                    | 448 ms                                                 | 404 ms: 1.11x faster                                                  |
| crypto_pyaes               | 76.6 ms                                                | 69.4 ms: 1.10x faster                                                 |
| float                      | 80.8 ms                                                | 73.4 ms: 1.10x faster                                                 |
| hexiom                     | 6.17 ms                                                | 5.61 ms: 1.10x faster                                                 |
| docutils                   | 2.64 sec                                               | 2.40 sec: 1.10x faster                                                |
| nqueens                    | 80.1 ms                                                | 73.1 ms: 1.10x faster                                                 |
| deltablue                  | 3.45 ms                                                | 3.18 ms: 1.08x faster                                                 |
| sympy_integrate            | 20.5 ms                                                | 19.0 ms: 1.08x faster                                                 |
| richards                   | 45.9 ms                                                | 42.6 ms: 1.08x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 89.6 ms: 1.08x faster                                                 |
| scimark_fft                | 342 ms                                                 | 316 ms: 1.08x faster                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 63.4 ms: 1.08x faster                                                 |
| richards_super             | 51.9 ms                                                | 48.4 ms: 1.07x faster                                                 |
| sympy_str                  | 292 ms                                                 | 273 ms: 1.07x faster                                                  |
| json_dumps                 | 10.4 ms                                                | 9.76 ms: 1.06x faster                                                 |
| html5lib                   | 63.6 ms                                                | 60.0 ms: 1.06x faster                                                 |
| sympy_sum                  | 166 ms                                                 | 157 ms: 1.06x faster                                                  |
| unpickle_pure_python       | 221 us                                                 | 209 us: 1.05x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.11 sec: 1.05x faster                                                |
| pprint_safe_repr           | 743 ms                                                 | 714 ms: 1.04x faster                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.46 sec: 1.04x faster                                                |
| python_startup_no_site     | 7.16 ms                                                | 6.94 ms: 1.03x faster                                                 |
| meteor_contest             | 104 ms                                                 | 100 ms: 1.03x faster                                                  |
| 2to3                       | 264 ms                                                 | 256 ms: 1.03x faster                                                  |
| thrift                     | 791 us                                                 | 772 us: 1.03x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.5 ms: 1.02x faster                                                 |
| sympy_expand               | 468 ms                                                 | 460 ms: 1.02x faster                                                  |
| xml_etree_generate         | 85.2 ms                                                | 85.9 ms: 1.01x slower                                                 |
| json                       | 5.02 ms                                                | 5.09 ms: 1.01x slower                                                 |
| django_template            | 34.7 ms                                                | 35.1 ms: 1.01x slower                                                 |
| pidigits                   | 184 ms                                                 | 188 ms: 1.02x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.49 ms: 1.02x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 21.1 ms: 1.03x slower                                                 |
| json_loads                 | 26.5 us                                                | 27.2 us: 1.03x slower                                                 |
| xml_etree_process          | 59.0 ms                                                | 60.6 ms: 1.03x slower                                                 |
| xml_etree_parse            | 139 ms                                                 | 144 ms: 1.04x slower                                                  |
| regex_dna                  | 168 ms                                                 | 175 ms: 1.04x slower                                                  |
| asyncio_websockets         | 517 ms                                                 | 543 ms: 1.05x slower                                                  |
| gc_traversal               | 3.46 ms                                                | 3.77 ms: 1.09x slower                                                 |
| mako                       | 11.0 ms                                                | 12.4 ms: 1.13x slower                                                 |
| coverage                   | 71.4 ms                                                | 83.4 ms: 1.17x slower                                                 |
| python_startup             | 9.93 ms                                                | 12.3 ms: 1.24x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 1.34 ms: 1.43x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.68 ms: 1.54x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 248 ms: 22.93x slower                                                 |
| telco                      | 6.53 ms                                                | 158 ms: 24.21x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.03x faster                                                          |

Benchmark hidden because not significant (5): scimark_lu, pickle_pure_python, fannkuch, sqlite_synth, nbody
Ignored benchmarks (23) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260619-3.16.0a0-a9db5cb/bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.078x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.14x