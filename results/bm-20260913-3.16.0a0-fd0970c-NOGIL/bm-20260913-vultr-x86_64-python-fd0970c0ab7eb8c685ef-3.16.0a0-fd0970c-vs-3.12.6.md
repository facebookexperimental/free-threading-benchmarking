# Results vs. 3.12.6

- fork: python
- ref: fd0970c0ab7eb8c685ef
- machine: linux-x86_64
- commit hash: fd0970c
- commit date: 2026-09-13
- overall geometric mean: 1.049x slower
- HPT reliability: 92.03%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.37x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260913-vultr-x86_64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 298 ms: 1.13x slower                                                  |
| docutils       | 2.64 sec                                               | 2.95 sec: 1.12x slower                                                |
| html5lib       | 63.6 ms                                                | 67.6 ms: 1.06x slower                                                 |
| Geometric mean | (ref)                                                  | 1.10x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260913-vultr-x86_64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 695 ms: 1.60x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 723 ms: 1.50x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 399 ms: 1.40x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 332 ms: 1.34x faster                                                  |
| async_tree_none            | 464 ms                                                 | 373 ms: 1.25x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 583 ms: 1.24x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 449 ms: 1.24x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 611 ms: 1.17x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 512 ms: 1.01x faster                                                  |
| coroutines                 | 23.9 ms                                                | 25.4 ms: 1.06x slower                                                 |
| async_generators           | 384 ms                                                 | 415 ms: 1.08x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.22x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260913-vultr-x86_64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 180 ms: 1.03x faster                                                  |
| float          | 80.8 ms                                                | 85.4 ms: 1.06x slower                                                 |
| nbody          | 89.3 ms                                                | 122 ms: 1.37x slower                                                  |
| Geometric mean | (ref)                                                  | 1.12x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260913-vultr-x86_64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.98 ms: 1.06x faster                                                 |
| regex_v8       | 20.6 ms                                                | 20.8 ms: 1.01x slower                                                 |
| regex_dna      | 168 ms                                                 | 184 ms: 1.09x slower                                                  |
| regex_compile  | 142 ms                                                 | 171 ms: 1.20x slower                                                  |
| Geometric mean | (ref)                                                  | 1.06x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260913-vultr-x86_64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.95 sec: 1.08x faster                                                |
| json_dumps           | 10.4 ms                                                | 10.0 ms: 1.03x faster                                                 |
| xml_etree_iterparse  | 96.7 ms                                                | 96.2 ms: 1.01x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 144 ms: 1.04x slower                                                  |
| unpickle_pure_python | 221 us                                                 | 241 us: 1.09x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 338 us: 1.10x slower                                                  |
| json_loads           | 26.5 us                                                | 30.6 us: 1.15x slower                                                 |
| xml_etree_generate   | 85.2 ms                                                | 103 ms: 1.21x slower                                                  |
| xml_etree_process    | 59.0 ms                                                | 76.2 ms: 1.29x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.08x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260913-vultr-x86_64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.96 ms: 1.39x slower                                                 |
| python_startup         | 9.93 ms                                                | 16.4 ms: 1.66x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.52x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260913-vultr-x86_64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.7 ms                                                | 41.8 ms: 1.20x slower                                                 |
| mako            | 11.0 ms                                                | 15.9 ms: 1.44x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.32x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260913-vultr-x86_64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 319 ms                                                 | 130 ms: 2.44x faster                                                  |
| gc_traversal               | 3.46 ms                                                | 1.78 ms: 1.94x faster                                                 |
| mdp                        | 2.42 sec                                               | 1.31 sec: 1.85x faster                                                |
| bench_mp_pool              | 10.8 ms                                                | 6.73 ms: 1.60x faster                                                 |
| async_tree_io_tg           | 1.11 sec                                               | 695 ms: 1.60x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 723 ms: 1.50x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 399 ms: 1.40x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 332 ms: 1.34x faster                                                  |
| deepcopy                   | 352 us                                                 | 274 us: 1.28x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 31.8 us: 1.27x faster                                                 |
| async_tree_none            | 464 ms                                                 | 373 ms: 1.25x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 583 ms: 1.24x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 449 ms: 1.24x faster                                                  |
| pathlib                    | 21.5 ms                                                | 18.1 ms: 1.19x faster                                                 |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 611 ms: 1.17x faster                                                  |
| go                         | 139 ms                                                 | 121 ms: 1.15x faster                                                  |
| sqlite_synth               | 2.20 us                                                | 1.94 us: 1.13x faster                                                 |
| comprehensions             | 19.8 us                                                | 17.9 us: 1.11x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 71.3 ms: 1.11x faster                                                 |
| typing_runtime_protocols   | 163 us                                                 | 148 us: 1.10x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.35 sec: 1.09x faster                                                |
| tomli_loads                | 2.11 sec                                               | 1.95 sec: 1.08x faster                                                |
| regex_effbot               | 3.17 ms                                                | 2.98 ms: 1.06x faster                                                 |
| scimark_sor                | 130 ms                                                 | 123 ms: 1.06x faster                                                  |
| json_dumps                 | 10.4 ms                                                | 10.0 ms: 1.03x faster                                                 |
| logging_silent             | 109 ns                                                 | 106 ns: 1.03x faster                                                  |
| chaos                      | 62.8 ms                                                | 61.2 ms: 1.03x faster                                                 |
| pidigits                   | 184 ms                                                 | 180 ms: 1.03x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 3.02 us: 1.02x faster                                                 |
| spectral_norm              | 110 ms                                                 | 108 ms: 1.02x faster                                                  |
| raytrace                   | 299 ms                                                 | 295 ms: 1.02x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 512 ms: 1.01x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 96.2 ms: 1.01x faster                                                 |
| pycparser                  | 1.17 sec                                               | 1.18 sec: 1.01x slower                                                |
| regex_v8                   | 20.6 ms                                                | 20.8 ms: 1.01x slower                                                 |
| scimark_fft                | 342 ms                                                 | 346 ms: 1.01x slower                                                  |
| pyflate                    | 448 ms                                                 | 461 ms: 1.03x slower                                                  |
| xml_etree_parse            | 139 ms                                                 | 144 ms: 1.04x slower                                                  |
| generators                 | 32.2 ms                                                | 34.0 ms: 1.05x slower                                                 |
| float                      | 80.8 ms                                                | 85.4 ms: 1.06x slower                                                 |
| coroutines                 | 23.9 ms                                                | 25.4 ms: 1.06x slower                                                 |
| html5lib                   | 63.6 ms                                                | 67.6 ms: 1.06x slower                                                 |
| hexiom                     | 6.17 ms                                                | 6.58 ms: 1.07x slower                                                 |
| logging_simple             | 6.63 us                                                | 7.12 us: 1.07x slower                                                 |
| json                       | 5.02 ms                                                | 5.40 ms: 1.07x slower                                                 |
| sympy_integrate            | 20.5 ms                                                | 22.2 ms: 1.08x slower                                                 |
| async_generators           | 384 ms                                                 | 415 ms: 1.08x slower                                                  |
| deltablue                  | 3.45 ms                                                | 3.73 ms: 1.08x slower                                                 |
| unpickle_pure_python       | 221 us                                                 | 241 us: 1.09x slower                                                  |
| regex_dna                  | 168 ms                                                 | 184 ms: 1.09x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 338 us: 1.10x slower                                                  |
| sympy_str                  | 292 ms                                                 | 321 ms: 1.10x slower                                                  |
| pprint_safe_repr           | 743 ms                                                 | 824 ms: 1.11x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 185 ms: 1.11x slower                                                  |
| logging_format             | 7.35 us                                                | 8.20 us: 1.12x slower                                                 |
| docutils                   | 2.64 sec                                               | 2.95 sec: 1.12x slower                                                |
| pprint_pformat             | 1.52 sec                                               | 1.70 sec: 1.12x slower                                                |
| nqueens                    | 80.1 ms                                                | 89.6 ms: 1.12x slower                                                 |
| 2to3                       | 264 ms                                                 | 298 ms: 1.13x slower                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 77.9 ms: 1.14x slower                                                 |
| json_loads                 | 26.5 us                                                | 30.6 us: 1.15x slower                                                 |
| sympy_expand               | 468 ms                                                 | 541 ms: 1.16x slower                                                  |
| thrift                     | 791 us                                                 | 916 us: 1.16x slower                                                  |
| richards                   | 45.9 ms                                                | 53.3 ms: 1.16x slower                                                 |
| crypto_pyaes               | 76.6 ms                                                | 88.8 ms: 1.16x slower                                                 |
| scimark_lu                 | 114 ms                                                 | 133 ms: 1.16x slower                                                  |
| richards_super             | 51.9 ms                                                | 60.9 ms: 1.17x slower                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.25 ms: 1.20x slower                                                 |
| regex_compile              | 142 ms                                                 | 171 ms: 1.20x slower                                                  |
| django_template            | 34.7 ms                                                | 41.8 ms: 1.20x slower                                                 |
| xml_etree_generate         | 85.2 ms                                                | 103 ms: 1.21x slower                                                  |
| meteor_contest             | 104 ms                                                 | 129 ms: 1.24x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.38 ms: 1.26x slower                                                 |
| fannkuch                   | 372 ms                                                 | 472 ms: 1.27x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 76.2 ms: 1.29x slower                                                 |
| nbody                      | 89.3 ms                                                | 122 ms: 1.37x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 9.96 ms: 1.39x slower                                                 |
| mako                       | 11.0 ms                                                | 15.9 ms: 1.44x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 1.49 ms: 1.58x slower                                                 |
| coverage                   | 71.4 ms                                                | 117 ms: 1.64x slower                                                  |
| python_startup             | 9.93 ms                                                | 16.4 ms: 1.66x slower                                                 |
| telco                      | 6.53 ms                                                | 175 ms: 26.89x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.05x slower                                                          |
Ignored benchmarks (23) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260913-3.16.0a0-fd0970c-NOGIL/bm-20260913-vultr-x86_64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.049x slower

# HPT report

- Reliability score: 92.03% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.37x