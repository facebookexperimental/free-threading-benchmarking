# Results vs. 3.12.6

- fork: python
- ref: 0bbdb4e897ae909af39c
- machine: linux-x86_64
- commit hash: 0bbdb4e
- commit date: 2026-02-18
- overall geometric mean: 1.031x slower
- HPT reliability: 75.51%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.43x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260218-vultr-x86_64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 278 ms: 1.05x slower                                                   |
| docutils       | 2.64 sec                                               | 2.76 sec: 1.05x slower                                                 |
| html5lib       | 63.6 ms                                                | 66.4 ms: 1.04x slower                                                  |
| Geometric mean | (ref)                                                  | 1.05x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260218-vultr-x86_64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 606 ms: 1.83x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 629 ms: 1.72x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 325 ms: 1.72x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 264 ms: 1.69x faster                                                   |
| async_tree_none            | 464 ms                                                 | 287 ms: 1.62x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 355 ms: 1.56x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 553 ms: 1.31x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 578 ms: 1.24x faster                                                   |
| coroutines                 | 23.9 ms                                                | 23.4 ms: 1.02x faster                                                  |
| async_generators           | 384 ms                                                 | 377 ms: 1.02x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 514 ms: 1.01x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.40x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260218-vultr-x86_64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 73.5 ms: 1.10x faster                                                  |
| pidigits       | 184 ms                                                 | 209 ms: 1.13x slower                                                   |
| nbody          | 89.3 ms                                                | 122 ms: 1.36x slower                                                   |
| Geometric mean | (ref)                                                  | 1.12x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260218-vultr-x86_64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.93 ms: 1.08x faster                                                  |
| regex_compile  | 142 ms                                                 | 142 ms: 1.00x faster                                                   |
| regex_v8       | 20.6 ms                                                | 21.5 ms: 1.05x slower                                                  |
| regex_dna      | 168 ms                                                 | 181 ms: 1.08x slower                                                   |
| Geometric mean | (ref)                                                  | 1.01x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260218-vultr-x86_64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 88.3 ms: 1.10x faster                                                  |
| tomli_loads          | 2.11 sec                                               | 1.97 sec: 1.07x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 132 ms: 1.05x faster                                                   |
| unpickle_pure_python | 221 us                                                 | 235 us: 1.07x slower                                                   |
| json_dumps           | 10.4 ms                                                | 11.1 ms: 1.08x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 332 us: 1.08x slower                                                   |
| xml_etree_generate   | 85.2 ms                                                | 95.3 ms: 1.12x slower                                                  |
| xml_etree_process    | 59.0 ms                                                | 68.7 ms: 1.17x slower                                                  |
| json_loads           | 26.5 us                                                | 32.4 us: 1.22x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.05x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260218-vultr-x86_64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.76 ms: 1.36x slower                                                  |
| python_startup         | 9.93 ms                                                | 16.0 ms: 1.61x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.48x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260218-vultr-x86_64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 54.6 ms: 1.09x slower                                                  |
| genshi_text     | 22.8 ms                                                | 25.9 ms: 1.13x slower                                                  |
| django_template | 34.7 ms                                                | 40.4 ms: 1.17x slower                                                  |
| mako            | 11.0 ms                                                | 15.9 ms: 1.44x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.20x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260218-vultr-x86_64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.31 sec: 1.84x faster                                                 |
| async_tree_io_tg           | 1.11 sec                                               | 606 ms: 1.83x faster                                                   |
| gc_traversal               | 3.46 ms                                                | 1.93 ms: 1.80x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 629 ms: 1.72x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 325 ms: 1.72x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 264 ms: 1.69x faster                                                   |
| async_tree_none            | 464 ms                                                 | 287 ms: 1.62x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 355 ms: 1.56x faster                                                   |
| bench_mp_pool              | 10.8 ms                                                | 7.11 ms: 1.52x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 30.6 us: 1.32x faster                                                  |
| deepcopy                   | 352 us                                                 | 268 us: 1.31x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 553 ms: 1.31x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 578 ms: 1.24x faster                                                   |
| pathlib                    | 21.5 ms                                                | 17.6 ms: 1.22x faster                                                  |
| go                         | 139 ms                                                 | 121 ms: 1.15x faster                                                   |
| sqlite_synth               | 2.20 us                                                | 1.93 us: 1.14x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 71.3 ms: 1.11x faster                                                  |
| float                      | 80.8 ms                                                | 73.5 ms: 1.10x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 88.3 ms: 1.10x faster                                                  |
| pylint                     | 319 ms                                                 | 292 ms: 1.09x faster                                                   |
| comprehensions             | 19.8 us                                                | 18.2 us: 1.09x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.36 sec: 1.09x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.93 ms: 1.08x faster                                                  |
| scimark_sor                | 130 ms                                                 | 121 ms: 1.07x faster                                                   |
| logging_silent             | 109 ns                                                 | 102 ns: 1.07x faster                                                   |
| tomli_loads                | 2.11 sec                                               | 1.97 sec: 1.07x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 132 ms: 1.05x faster                                                   |
| deepcopy_reduce            | 3.08 us                                                | 2.93 us: 1.05x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.13 sec: 1.03x faster                                                 |
| coroutines                 | 23.9 ms                                                | 23.4 ms: 1.02x faster                                                  |
| async_generators           | 384 ms                                                 | 377 ms: 1.02x faster                                                   |
| raytrace                   | 299 ms                                                 | 295 ms: 1.02x faster                                                   |
| spectral_norm              | 110 ms                                                 | 109 ms: 1.01x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 514 ms: 1.01x faster                                                   |
| regex_compile              | 142 ms                                                 | 142 ms: 1.00x faster                                                   |
| scimark_fft                | 342 ms                                                 | 340 ms: 1.00x faster                                                   |
| chaos                      | 62.8 ms                                                | 63.3 ms: 1.01x slower                                                  |
| generators                 | 32.2 ms                                                | 32.8 ms: 1.02x slower                                                  |
| pyflate                    | 448 ms                                                 | 456 ms: 1.02x slower                                                   |
| logging_simple             | 6.63 us                                                | 6.77 us: 1.02x slower                                                  |
| logging_format             | 7.35 us                                                | 7.64 us: 1.04x slower                                                  |
| html5lib                   | 63.6 ms                                                | 66.4 ms: 1.04x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 21.5 ms: 1.05x slower                                                  |
| docutils                   | 2.64 sec                                               | 2.76 sec: 1.05x slower                                                 |
| deltablue                  | 3.45 ms                                                | 3.61 ms: 1.05x slower                                                  |
| pprint_safe_repr           | 743 ms                                                 | 779 ms: 1.05x slower                                                   |
| 2to3                       | 264 ms                                                 | 278 ms: 1.05x slower                                                   |
| hexiom                     | 6.17 ms                                                | 6.51 ms: 1.06x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.62 sec: 1.06x slower                                                 |
| unpickle_pure_python       | 221 us                                                 | 235 us: 1.07x slower                                                   |
| sympy_integrate            | 20.5 ms                                                | 22.1 ms: 1.07x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 11.1 ms: 1.08x slower                                                  |
| sympy_str                  | 292 ms                                                 | 314 ms: 1.08x slower                                                   |
| regex_dna                  | 168 ms                                                 | 181 ms: 1.08x slower                                                   |
| pickle_pure_python         | 308 us                                                 | 332 us: 1.08x slower                                                   |
| json                       | 5.02 ms                                                | 5.43 ms: 1.08x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 181 ms: 1.09x slower                                                   |
| genshi_xml                 | 50.2 ms                                                | 54.6 ms: 1.09x slower                                                  |
| scimark_lu                 | 114 ms                                                 | 125 ms: 1.09x slower                                                   |
| xml_etree_generate         | 85.2 ms                                                | 95.3 ms: 1.12x slower                                                  |
| nqueens                    | 80.1 ms                                                | 89.6 ms: 1.12x slower                                                  |
| sympy_expand               | 468 ms                                                 | 526 ms: 1.12x slower                                                   |
| richards                   | 45.9 ms                                                | 51.8 ms: 1.13x slower                                                  |
| pidigits                   | 184 ms                                                 | 209 ms: 1.13x slower                                                   |
| genshi_text                | 22.8 ms                                                | 25.9 ms: 1.13x slower                                                  |
| crypto_pyaes               | 76.6 ms                                                | 87.0 ms: 1.14x slower                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 78.0 ms: 1.14x slower                                                  |
| richards_super             | 51.9 ms                                                | 59.3 ms: 1.14x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 68.7 ms: 1.17x slower                                                  |
| django_template            | 34.7 ms                                                | 40.4 ms: 1.17x slower                                                  |
| thrift                     | 791 us                                                 | 924 us: 1.17x slower                                                   |
| meteor_contest             | 104 ms                                                 | 125 ms: 1.21x slower                                                   |
| typing_runtime_protocols   | 163 us                                                 | 199 us: 1.22x slower                                                   |
| json_loads                 | 26.5 us                                                | 32.4 us: 1.22x slower                                                  |
| fannkuch                   | 372 ms                                                 | 456 ms: 1.22x slower                                                   |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.43 ms: 1.24x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.49 ms: 1.36x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 9.76 ms: 1.36x slower                                                  |
| nbody                      | 89.3 ms                                                | 122 ms: 1.36x slower                                                   |
| mako                       | 11.0 ms                                                | 15.9 ms: 1.44x slower                                                  |
| coverage                   | 71.4 ms                                                | 111 ms: 1.55x slower                                                   |
| python_startup             | 9.93 ms                                                | 16.0 ms: 1.61x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 1.62 ms: 1.73x slower                                                  |
| telco                      | 6.53 ms                                                | 172 ms: 26.34x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.03x slower                                                           |
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260218-3.15.0a6+-0bbdb4e-NOGIL/bm-20260218-vultr-x86_64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.031x slower

# HPT report

- Reliability score: 75.51% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.43x