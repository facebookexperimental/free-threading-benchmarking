# Results vs. 3.12.6

- fork: python
- ref: bcc9a5dddb777c8195b5
- machine: linux-x86_64
- commit hash: bcc9a5d
- commit date: 2025-02-18
- overall geometric mean: 1.046x slower
- HPT reliability: 99.98%
- HPT 99th percentile: 1.03x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250218-vultr-x86_64-python-bcc9a5dddb777c8195b5-3.14.0a5+-bcc9a5d |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 302 ms: 1.15x slower                                                   |
| docutils       | 2.64 sec                                               | 2.80 sec: 1.06x slower                                                 |
| html5lib       | 63.6 ms                                                | 72.1 ms: 1.13x slower                                                  |
| Geometric mean | (ref)                                                  | 1.11x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250218-vultr-x86_64-python-bcc9a5dddb777c8195b5-3.14.0a5+-bcc9a5d |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 574 ms: 1.93x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 248 ms: 1.80x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 607 ms: 1.78x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 319 ms: 1.75x faster                                                   |
| async_tree_none            | 464 ms                                                 | 286 ms: 1.62x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 352 ms: 1.58x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 513 ms: 1.41x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 547 ms: 1.31x faster                                                   |
| async_generators           | 384 ms                                                 | 374 ms: 1.03x faster                                                   |
| coroutines                 | 23.9 ms                                                | 23.8 ms: 1.01x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 515 ms: 1.00x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.44x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250218-vultr-x86_64-python-bcc9a5dddb777c8195b5-3.14.0a5+-bcc9a5d |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 75.8 ms: 1.07x faster                                                  |
| pidigits       | 184 ms                                                 | 199 ms: 1.08x slower                                                   |
| nbody          | 89.3 ms                                                | 129 ms: 1.44x slower                                                   |
| Geometric mean | (ref)                                                  | 1.14x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250218-vultr-x86_64-python-bcc9a5dddb777c8195b5-3.14.0a5+-bcc9a5d |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.84 ms: 1.11x faster                                                  |
| regex_compile  | 142 ms                                                 | 154 ms: 1.08x slower                                                   |
| regex_dna      | 168 ms                                                 | 183 ms: 1.09x slower                                                   |
| regex_v8       | 20.6 ms                                                | 23.6 ms: 1.15x slower                                                  |
| Geometric mean | (ref)                                                  | 1.05x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250218-vultr-x86_64-python-bcc9a5dddb777c8195b5-3.14.0a5+-bcc9a5d |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 88.0 ms: 1.10x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 128 ms: 1.08x faster                                                   |
| tomli_loads          | 2.11 sec                                               | 2.32 sec: 1.10x slower                                                 |
| xml_etree_generate   | 85.2 ms                                                | 96.6 ms: 1.13x slower                                                  |
| unpickle_pure_python | 221 us                                                 | 252 us: 1.14x slower                                                   |
| pickle_pure_python   | 308 us                                                 | 360 us: 1.17x slower                                                   |
| json_loads           | 26.5 us                                                | 31.2 us: 1.18x slower                                                  |
| xml_etree_process    | 59.0 ms                                                | 70.3 ms: 1.19x slower                                                  |
| json_dumps           | 10.4 ms                                                | 12.9 ms: 1.25x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.10x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250218-vultr-x86_64-python-bcc9a5dddb777c8195b5-3.14.0a5+-bcc9a5d |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.62 ms: 1.34x slower                                                  |
| python_startup         | 9.93 ms                                                | 15.3 ms: 1.54x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.44x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250218-vultr-x86_64-python-bcc9a5dddb777c8195b5-3.14.0a5+-bcc9a5d |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 59.8 ms: 1.19x slower                                                  |
| genshi_text     | 22.8 ms                                                | 28.1 ms: 1.23x slower                                                  |
| django_template | 34.7 ms                                                | 42.7 ms: 1.23x slower                                                  |
| mako            | 11.0 ms                                                | 15.7 ms: 1.42x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.27x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250218-vultr-x86_64-python-bcc9a5dddb777c8195b5-3.14.0a5+-bcc9a5d |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| gc_traversal               | 3.46 ms                                                | 1.73 ms: 2.00x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 574 ms: 1.93x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 248 ms: 1.80x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 607 ms: 1.78x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 319 ms: 1.75x faster                                                   |
| async_tree_none            | 464 ms                                                 | 286 ms: 1.62x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 352 ms: 1.58x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 513 ms: 1.41x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 547 ms: 1.31x faster                                                   |
| deepcopy                   | 352 us                                                 | 310 us: 1.14x faster                                                   |
| regex_effbot               | 3.17 ms                                                | 2.84 ms: 1.11x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 88.0 ms: 1.10x faster                                                  |
| pathlib                    | 21.5 ms                                                | 19.8 ms: 1.09x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 128 ms: 1.08x faster                                                   |
| sqlite_synth               | 2.20 us                                                | 2.03 us: 1.08x faster                                                  |
| float                      | 80.8 ms                                                | 75.8 ms: 1.07x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 38.4 us: 1.05x faster                                                  |
| async_generators           | 384 ms                                                 | 374 ms: 1.03x faster                                                   |
| spectral_norm              | 110 ms                                                 | 109 ms: 1.01x faster                                                   |
| bpe_tokeniser              | 4.74 sec                                               | 4.68 sec: 1.01x faster                                                 |
| coroutines                 | 23.9 ms                                                | 23.8 ms: 1.01x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 515 ms: 1.00x faster                                                   |
| go                         | 139 ms                                                 | 140 ms: 1.00x slower                                                   |
| comprehensions             | 19.8 us                                                | 19.9 us: 1.00x slower                                                  |
| scimark_sor                | 130 ms                                                 | 132 ms: 1.02x slower                                                   |
| pycparser                  | 1.17 sec                                               | 1.20 sec: 1.03x slower                                                 |
| deepcopy_reduce            | 3.08 us                                                | 3.18 us: 1.03x slower                                                  |
| logging_silent             | 109 ns                                                 | 114 ns: 1.05x slower                                                   |
| dulwich_log                | 78.9 ms                                                | 82.7 ms: 1.05x slower                                                  |
| docutils                   | 2.64 sec                                               | 2.80 sec: 1.06x slower                                                 |
| logging_simple             | 6.63 us                                                | 7.06 us: 1.06x slower                                                  |
| json                       | 5.02 ms                                                | 5.41 ms: 1.08x slower                                                  |
| regex_compile              | 142 ms                                                 | 154 ms: 1.08x slower                                                   |
| mdp                        | 2.42 sec                                               | 2.61 sec: 1.08x slower                                                 |
| raytrace                   | 299 ms                                                 | 324 ms: 1.08x slower                                                   |
| pidigits                   | 184 ms                                                 | 199 ms: 1.08x slower                                                   |
| regex_dna                  | 168 ms                                                 | 183 ms: 1.09x slower                                                   |
| sqlalchemy_imperative      | 21.8 ms                                                | 23.8 ms: 1.09x slower                                                  |
| sqlalchemy_declarative     | 143 ms                                                 | 157 ms: 1.10x slower                                                   |
| tomli_loads                | 2.11 sec                                               | 2.32 sec: 1.10x slower                                                 |
| logging_format             | 7.35 us                                                | 8.13 us: 1.11x slower                                                  |
| pyflate                    | 448 ms                                                 | 496 ms: 1.11x slower                                                   |
| pprint_safe_repr           | 743 ms                                                 | 825 ms: 1.11x slower                                                   |
| chaos                      | 62.8 ms                                                | 70.0 ms: 1.11x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.70 sec: 1.12x slower                                                 |
| deltablue                  | 3.45 ms                                                | 3.87 ms: 1.12x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 187 ms: 1.13x slower                                                   |
| thrift                     | 791 us                                                 | 893 us: 1.13x slower                                                   |
| sqlglot_normalize          | 107 ms                                                 | 120 ms: 1.13x slower                                                   |
| scimark_fft                | 342 ms                                                 | 386 ms: 1.13x slower                                                   |
| html5lib                   | 63.6 ms                                                | 72.1 ms: 1.13x slower                                                  |
| xml_etree_generate         | 85.2 ms                                                | 96.6 ms: 1.13x slower                                                  |
| crypto_pyaes               | 76.6 ms                                                | 87.2 ms: 1.14x slower                                                  |
| unpickle_pure_python       | 221 us                                                 | 252 us: 1.14x slower                                                   |
| sqlglot_transpile          | 1.67 ms                                                | 1.91 ms: 1.14x slower                                                  |
| sympy_str                  | 292 ms                                                 | 334 ms: 1.15x slower                                                   |
| regex_v8                   | 20.6 ms                                                | 23.6 ms: 1.15x slower                                                  |
| 2to3                       | 264 ms                                                 | 302 ms: 1.15x slower                                                   |
| sqlglot_optimize           | 53.3 ms                                                | 61.4 ms: 1.15x slower                                                  |
| sympy_expand               | 468 ms                                                 | 546 ms: 1.17x slower                                                   |
| sqlglot_parse              | 1.36 ms                                                | 1.58 ms: 1.17x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 360 us: 1.17x slower                                                   |
| sympy_integrate            | 20.5 ms                                                | 24.1 ms: 1.17x slower                                                  |
| json_loads                 | 26.5 us                                                | 31.2 us: 1.18x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 70.3 ms: 1.19x slower                                                  |
| genshi_xml                 | 50.2 ms                                                | 59.8 ms: 1.19x slower                                                  |
| hexiom                     | 6.17 ms                                                | 7.41 ms: 1.20x slower                                                  |
| nqueens                    | 80.1 ms                                                | 96.3 ms: 1.20x slower                                                  |
| richards                   | 45.9 ms                                                | 55.4 ms: 1.21x slower                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 82.6 ms: 1.21x slower                                                  |
| scimark_lu                 | 114 ms                                                 | 139 ms: 1.22x slower                                                   |
| typing_runtime_protocols   | 163 us                                                 | 200 us: 1.22x slower                                                   |
| genshi_text                | 22.8 ms                                                | 28.1 ms: 1.23x slower                                                  |
| django_template            | 34.7 ms                                                | 42.7 ms: 1.23x slower                                                  |
| richards_super             | 51.9 ms                                                | 64.3 ms: 1.24x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 12.9 ms: 1.25x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.48 ms: 1.25x slower                                                  |
| meteor_contest             | 104 ms                                                 | 130 ms: 1.25x slower                                                   |
| create_gc_cycles           | 1.09 ms                                                | 1.37 ms: 1.26x slower                                                  |
| telco                      | 6.53 ms                                                | 8.49 ms: 1.30x slower                                                  |
| fannkuch                   | 372 ms                                                 | 492 ms: 1.32x slower                                                   |
| python_startup_no_site     | 7.16 ms                                                | 9.62 ms: 1.34x slower                                                  |
| coverage                   | 71.4 ms                                                | 97.9 ms: 1.37x slower                                                  |
| mako                       | 11.0 ms                                                | 15.7 ms: 1.42x slower                                                  |
| nbody                      | 89.3 ms                                                | 129 ms: 1.44x slower                                                   |
| python_startup             | 9.93 ms                                                | 15.3 ms: 1.54x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 3.30 ms: 3.51x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 94.9 ms: 8.79x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.09x slower                                                           |

Benchmark hidden because not significant (2): pylint, generators
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250218-3.14.0a5+-bcc9a5d-NOGIL/bm-20250218-vultr-x86_64-python-bcc9a5dddb777c8195b5-3.14.0a5+-bcc9a5d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.046x slower

# HPT report

- Reliability score: 99.98% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: 1.36x