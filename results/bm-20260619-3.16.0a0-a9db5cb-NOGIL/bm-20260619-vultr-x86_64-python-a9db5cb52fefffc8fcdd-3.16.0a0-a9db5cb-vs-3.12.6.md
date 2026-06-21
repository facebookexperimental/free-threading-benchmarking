# Results vs. 3.12.6

- fork: python
- ref: a9db5cb52fefffc8fcdd
- machine: linux-x86_64
- commit hash: a9db5cb
- commit date: 2026-06-19
- overall geometric mean: 1.036x slower
- HPT reliability: 92.81%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 293 ms: 1.11x slower                                                  |
| docutils       | 2.64 sec                                               | 2.97 sec: 1.12x slower                                                |
| html5lib       | 63.6 ms                                                | 69.0 ms: 1.09x slower                                                 |
| Geometric mean | (ref)                                                  | 1.11x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 677 ms: 1.64x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 699 ms: 1.55x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 391 ms: 1.43x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 322 ms: 1.39x faster                                                  |
| async_tree_none            | 464 ms                                                 | 337 ms: 1.38x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 416 ms: 1.34x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 578 ms: 1.25x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 601 ms: 1.19x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 514 ms: 1.01x faster                                                  |
| async_generators           | 384 ms                                                 | 386 ms: 1.00x slower                                                  |
| coroutines                 | 23.9 ms                                                | 24.6 ms: 1.03x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.27x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 181 ms: 1.02x faster                                                  |
| float          | 80.8 ms                                                | 86.2 ms: 1.07x slower                                                 |
| nbody          | 89.3 ms                                                | 127 ms: 1.43x slower                                                  |
| Geometric mean | (ref)                                                  | 1.14x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 141 ms: 1.01x faster                                                  |
| regex_effbot   | 3.17 ms                                                | 3.19 ms: 1.01x slower                                                 |
| regex_v8       | 20.6 ms                                                | 21.5 ms: 1.04x slower                                                 |
| regex_dna      | 168 ms                                                 | 188 ms: 1.12x slower                                                  |
| Geometric mean | (ref)                                                  | 1.04x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.95 sec: 1.08x faster                                                |
| xml_etree_iterparse  | 96.7 ms                                                | 95.2 ms: 1.02x faster                                                 |
| json_dumps           | 10.4 ms                                                | 10.6 ms: 1.02x slower                                                 |
| xml_etree_parse      | 139 ms                                                 | 142 ms: 1.02x slower                                                  |
| unpickle_pure_python | 221 us                                                 | 237 us: 1.07x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 338 us: 1.10x slower                                                  |
| json_loads           | 26.5 us                                                | 30.3 us: 1.14x slower                                                 |
| xml_etree_generate   | 85.2 ms                                                | 101 ms: 1.19x slower                                                  |
| xml_etree_process    | 59.0 ms                                                | 74.6 ms: 1.27x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.08x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.18 ms: 1.28x slower                                                 |
| python_startup         | 9.93 ms                                                | 15.4 ms: 1.55x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.41x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.7 ms                                                | 41.1 ms: 1.18x slower                                                 |
| mako            | 11.0 ms                                                | 16.3 ms: 1.48x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.32x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 319 ms                                                 | 133 ms: 2.39x faster                                                  |
| gc_traversal               | 3.46 ms                                                | 1.76 ms: 1.97x faster                                                 |
| mdp                        | 2.42 sec                                               | 1.30 sec: 1.86x faster                                                |
| async_tree_io_tg           | 1.11 sec                                               | 677 ms: 1.64x faster                                                  |
| bench_mp_pool              | 10.8 ms                                                | 6.86 ms: 1.57x faster                                                 |
| async_tree_io              | 1.08 sec                                               | 699 ms: 1.55x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 391 ms: 1.43x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 322 ms: 1.39x faster                                                  |
| async_tree_none            | 464 ms                                                 | 337 ms: 1.38x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 416 ms: 1.34x faster                                                  |
| deepcopy                   | 352 us                                                 | 265 us: 1.33x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 31.1 us: 1.30x faster                                                 |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 578 ms: 1.25x faster                                                  |
| pathlib                    | 21.5 ms                                                | 17.6 ms: 1.22x faster                                                 |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 601 ms: 1.19x faster                                                  |
| go                         | 139 ms                                                 | 120 ms: 1.16x faster                                                  |
| comprehensions             | 19.8 us                                                | 17.3 us: 1.15x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 69.9 ms: 1.13x faster                                                 |
| typing_runtime_protocols   | 163 us                                                 | 145 us: 1.12x faster                                                  |
| sqlite_synth               | 2.20 us                                                | 1.96 us: 1.12x faster                                                 |
| scimark_sor                | 130 ms                                                 | 120 ms: 1.08x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.39 sec: 1.08x faster                                                |
| tomli_loads                | 2.11 sec                                               | 1.95 sec: 1.08x faster                                                |
| deepcopy_reduce            | 3.08 us                                                | 2.87 us: 1.07x faster                                                 |
| logging_silent             | 109 ns                                                 | 104 ns: 1.05x faster                                                  |
| pidigits                   | 184 ms                                                 | 181 ms: 1.02x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 95.2 ms: 1.02x faster                                                 |
| generators                 | 32.2 ms                                                | 31.8 ms: 1.01x faster                                                 |
| regex_compile              | 142 ms                                                 | 141 ms: 1.01x faster                                                  |
| spectral_norm              | 110 ms                                                 | 109 ms: 1.01x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 514 ms: 1.01x faster                                                  |
| async_generators           | 384 ms                                                 | 386 ms: 1.00x slower                                                  |
| pycparser                  | 1.17 sec                                               | 1.17 sec: 1.00x slower                                                |
| regex_effbot               | 3.17 ms                                                | 3.19 ms: 1.01x slower                                                 |
| chaos                      | 62.8 ms                                                | 63.3 ms: 1.01x slower                                                 |
| pyflate                    | 448 ms                                                 | 454 ms: 1.01x slower                                                  |
| raytrace                   | 299 ms                                                 | 306 ms: 1.02x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 10.6 ms: 1.02x slower                                                 |
| xml_etree_parse            | 139 ms                                                 | 142 ms: 1.02x slower                                                  |
| coroutines                 | 23.9 ms                                                | 24.6 ms: 1.03x slower                                                 |
| scimark_fft                | 342 ms                                                 | 353 ms: 1.03x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 21.5 ms: 1.04x slower                                                 |
| logging_simple             | 6.63 us                                                | 6.94 us: 1.05x slower                                                 |
| json                       | 5.02 ms                                                | 5.30 ms: 1.06x slower                                                 |
| logging_format             | 7.35 us                                                | 7.79 us: 1.06x slower                                                 |
| deltablue                  | 3.45 ms                                                | 3.66 ms: 1.06x slower                                                 |
| float                      | 80.8 ms                                                | 86.2 ms: 1.07x slower                                                 |
| pprint_safe_repr           | 743 ms                                                 | 797 ms: 1.07x slower                                                  |
| unpickle_pure_python       | 221 us                                                 | 237 us: 1.07x slower                                                  |
| sympy_integrate            | 20.5 ms                                                | 22.0 ms: 1.07x slower                                                 |
| hexiom                     | 6.17 ms                                                | 6.63 ms: 1.07x slower                                                 |
| sympy_str                  | 292 ms                                                 | 316 ms: 1.08x slower                                                  |
| html5lib                   | 63.6 ms                                                | 69.0 ms: 1.09x slower                                                 |
| pprint_pformat             | 1.52 sec                                               | 1.65 sec: 1.09x slower                                                |
| nqueens                    | 80.1 ms                                                | 87.3 ms: 1.09x slower                                                 |
| sympy_sum                  | 166 ms                                                 | 182 ms: 1.09x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 338 us: 1.10x slower                                                  |
| 2to3                       | 264 ms                                                 | 293 ms: 1.11x slower                                                  |
| regex_dna                  | 168 ms                                                 | 188 ms: 1.12x slower                                                  |
| docutils                   | 2.64 sec                                               | 2.97 sec: 1.12x slower                                                |
| sympy_expand               | 468 ms                                                 | 527 ms: 1.13x slower                                                  |
| json_loads                 | 26.5 us                                                | 30.3 us: 1.14x slower                                                 |
| scimark_lu                 | 114 ms                                                 | 131 ms: 1.14x slower                                                  |
| richards                   | 45.9 ms                                                | 52.7 ms: 1.15x slower                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 79.0 ms: 1.16x slower                                                 |
| thrift                     | 791 us                                                 | 926 us: 1.17x slower                                                  |
| richards_super             | 51.9 ms                                                | 60.7 ms: 1.17x slower                                                 |
| crypto_pyaes               | 76.6 ms                                                | 90.6 ms: 1.18x slower                                                 |
| django_template            | 34.7 ms                                                | 41.1 ms: 1.18x slower                                                 |
| xml_etree_generate         | 85.2 ms                                                | 101 ms: 1.19x slower                                                  |
| meteor_contest             | 104 ms                                                 | 127 ms: 1.23x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.34 ms: 1.23x slower                                                 |
| fannkuch                   | 372 ms                                                 | 464 ms: 1.25x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.54 ms: 1.26x slower                                                 |
| xml_etree_process          | 59.0 ms                                                | 74.6 ms: 1.27x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 9.18 ms: 1.28x slower                                                 |
| nbody                      | 89.3 ms                                                | 127 ms: 1.43x slower                                                  |
| mako                       | 11.0 ms                                                | 16.3 ms: 1.48x slower                                                 |
| python_startup             | 9.93 ms                                                | 15.4 ms: 1.55x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 1.47 ms: 1.56x slower                                                 |
| coverage                   | 71.4 ms                                                | 114 ms: 1.60x slower                                                  |
| telco                      | 6.53 ms                                                | 175 ms: 26.78x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.03x slower                                                          |
Ignored benchmarks (23) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260619-3.16.0a0-a9db5cb-NOGIL/bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.036x slower

# HPT report

- Reliability score: 92.81% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.36x