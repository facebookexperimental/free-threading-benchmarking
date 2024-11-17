# Results vs. 3.12.6

- fork: python
- ref: acbd5c9c6c62dac34d2e
- machine: linux-x86_64
- commit hash: acbd5c9
- commit date: 2024-11-17
- overall geometric mean: 1.01x faster
- HPT reliability: 99.56%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

Benchmark hidden because not significant (3): 2to3, docutils, html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241117-linux-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9 |
|------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_generators | 589 ms                                                 | 616 ms: 1.05x slower                                                   |
| coroutines       | 29.5 ms                                                | 32.1 ms: 1.09x slower                                                  |
| Geometric mean   | (ref)                                                  | 1.03x slower                                                           |

Benchmark hidden because not significant (3): asyncio_tcp, asyncio_tcp_ssl, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241117-linux-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 123 ms                                                 | 115 ms: 1.07x faster                                                   |
| pidigits       | 250 ms                                                 | 234 ms: 1.07x faster                                                   |
| nbody          | 119 ms                                                 | 132 ms: 1.11x slower                                                   |
| Geometric mean | (ref)                                                  | 1.01x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241117-linux-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 187 ms                                                 | 173 ms: 1.08x faster                                                   |
| regex_effbot   | 5.13 ms                                                | 4.80 ms: 1.07x faster                                                  |
| regex_dna      | 278 ms                                                 | 293 ms: 1.05x slower                                                   |
| regex_v8       | 32.5 ms                                                | 34.9 ms: 1.07x slower                                                  |
| Geometric mean | (ref)                                                  | 1.00x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241117-linux-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_dict    | 52.7 us                                                | 45.7 us: 1.15x faster                                                  |
| json_loads     | 37.9 us                                                | 34.0 us: 1.11x faster                                                  |
| tomli_loads    | 2.88 sec                                               | 2.73 sec: 1.06x faster                                                 |
| unpickle_list  | 6.83 us                                                | 7.19 us: 1.05x slower                                                  |
| json_dumps     | 14.3 ms                                                | 15.8 ms: 1.10x slower                                                  |
| Geometric mean | (ref)                                                  | 1.01x faster                                                           |

Benchmark hidden because not significant (9): unpickle, xml_etree_iterparse, pickle, xml_etree_generate, xml_etree_parse, pickle_pure_python, pickle_list, unpickle_pure_python, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241117-linux-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 14.0 ms: 1.26x faster                                                  |
| python_startup         | 23.7 ms                                                | 21.0 ms: 1.13x faster                                                  |
| Geometric mean         | (ref)                                                  | 1.19x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241117-linux-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 44.9 ms                                                | 47.3 ms: 1.05x slower                                                  |
| mako            | 15.7 ms                                                | 16.9 ms: 1.08x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.03x slower                                                           |

Benchmark hidden because not significant (2): genshi_xml, genshi_text

All benchmarks:
===============

| Benchmark                | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241117-linux-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9 |
|--------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site   | 17.6 ms                                                | 14.0 ms: 1.26x faster                                                  |
| deepcopy_memo            | 52.4 us                                                | 42.8 us: 1.23x faster                                                  |
| deepcopy                 | 468 us                                                 | 388 us: 1.21x faster                                                   |
| comprehensions           | 27.1 us                                                | 22.9 us: 1.18x faster                                                  |
| pathlib                  | 31.6 ms                                                | 26.9 ms: 1.17x faster                                                  |
| pycparser                | 1.79 sec                                               | 1.54 sec: 1.16x faster                                                 |
| pickle_dict              | 52.7 us                                                | 45.7 us: 1.15x faster                                                  |
| raytrace                 | 408 ms                                                 | 354 ms: 1.15x faster                                                   |
| mdp                      | 3.97 sec                                               | 3.52 sec: 1.13x faster                                                 |
| python_startup           | 23.7 ms                                                | 21.0 ms: 1.13x faster                                                  |
| json_loads               | 37.9 us                                                | 34.0 us: 1.11x faster                                                  |
| nqueens                  | 117 ms                                                 | 106 ms: 1.10x faster                                                   |
| bpe_tokeniser            | 6.59 sec                                               | 5.98 sec: 1.10x faster                                                 |
| sqlglot_normalize        | 157 ms                                                 | 143 ms: 1.10x faster                                                   |
| scimark_sparse_mat_mult  | 6.70 ms                                                | 6.19 ms: 1.08x faster                                                  |
| regex_compile            | 187 ms                                                 | 173 ms: 1.08x faster                                                   |
| pyflate                  | 727 ms                                                 | 676 ms: 1.08x faster                                                   |
| logging_simple           | 9.45 us                                                | 8.82 us: 1.07x faster                                                  |
| float                    | 123 ms                                                 | 115 ms: 1.07x faster                                                   |
| regex_effbot             | 5.13 ms                                                | 4.80 ms: 1.07x faster                                                  |
| pidigits                 | 250 ms                                                 | 234 ms: 1.07x faster                                                   |
| sympy_sum                | 222 ms                                                 | 208 ms: 1.07x faster                                                   |
| sqlglot_optimize         | 76.0 ms                                                | 71.3 ms: 1.07x faster                                                  |
| logging_format           | 9.59 us                                                | 9.00 us: 1.06x faster                                                  |
| go                       | 172 ms                                                 | 162 ms: 1.06x faster                                                   |
| tomli_loads              | 2.88 sec                                               | 2.73 sec: 1.06x faster                                                 |
| thrift                   | 1.06 ms                                                | 1.00 ms: 1.05x faster                                                  |
| scimark_fft              | 500 ms                                                 | 475 ms: 1.05x faster                                                   |
| pprint_pformat           | 1.98 sec                                               | 1.88 sec: 1.05x faster                                                 |
| pprint_safe_repr         | 967 ms                                                 | 926 ms: 1.04x faster                                                   |
| typing_runtime_protocols | 224 us                                                 | 215 us: 1.04x faster                                                   |
| deepcopy_reduce          | 4.04 us                                                | 3.87 us: 1.04x faster                                                  |
| scimark_monte_carlo      | 96.4 ms                                                | 92.7 ms: 1.04x faster                                                  |
| sympy_expand             | 582 ms                                                 | 605 ms: 1.04x slower                                                   |
| async_generators         | 589 ms                                                 | 616 ms: 1.05x slower                                                   |
| unpack_sequence          | 60.2 ns                                                | 63.1 ns: 1.05x slower                                                  |
| unpickle_list            | 6.83 us                                                | 7.19 us: 1.05x slower                                                  |
| django_template          | 44.9 ms                                                | 47.3 ms: 1.05x slower                                                  |
| regex_dna                | 278 ms                                                 | 293 ms: 1.05x slower                                                   |
| meteor_contest           | 146 ms                                                 | 154 ms: 1.06x slower                                                   |
| richards                 | 60.3 ms                                                | 63.8 ms: 1.06x slower                                                  |
| regex_v8                 | 32.5 ms                                                | 34.9 ms: 1.07x slower                                                  |
| mako                     | 15.7 ms                                                | 16.9 ms: 1.08x slower                                                  |
| coroutines               | 29.5 ms                                                | 32.1 ms: 1.09x slower                                                  |
| json_dumps               | 14.3 ms                                                | 15.8 ms: 1.10x slower                                                  |
| nbody                    | 119 ms                                                 | 132 ms: 1.11x slower                                                   |
| deltablue                | 4.27 ms                                                | 4.77 ms: 1.12x slower                                                  |
| telco                    | 9.59 ms                                                | 10.8 ms: 1.13x slower                                                  |
| coverage                 | 95.4 ms                                                | 117 ms: 1.23x slower                                                   |
| create_gc_cycles         | 1.94 ms                                                | 2.44 ms: 1.26x slower                                                  |
| bench_mp_pool            | 20.7 ms                                                | 72.4 ms: 3.50x slower                                                  |
| Geometric mean           | (ref)                                                  | 1.01x faster                                                           |

Benchmark hidden because not significant (37): bench_thread_pool, 2to3, sympy_integrate, unpickle, xml_etree_iterparse, sympy_str, pickle, json, docutils, fannkuch, crypto_pyaes, xml_etree_generate, scimark_lu, asyncio_tcp, spectral_norm, gc_traversal, html5lib, pylint, genshi_xml, xml_etree_parse, dulwich_log, asyncio_tcp_ssl, genshi_text, pickle_pure_python, chaos, asyncio_websockets, richards_super, scimark_sor, sqlglot_transpile, logging_silent, sqlite_synth, pickle_list, hexiom, unpickle_pure_python, generators, xml_etree_process, sqlglot_parse
Ignored benchmarks (17) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http

# HPT report

- Reliability score: 99.56% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.02x