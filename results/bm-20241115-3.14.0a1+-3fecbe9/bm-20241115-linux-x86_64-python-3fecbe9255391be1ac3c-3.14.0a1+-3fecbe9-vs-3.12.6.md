# Results vs. 3.12.6

- fork: python
- ref: 3fecbe9255391be1ac3c
- machine: linux-x86_64
- commit hash: 3fecbe9
- commit date: 2024-11-15
- overall geometric mean: 1.03x faster
- HPT reliability: 99.97%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241115-linux-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 431 ms: 1.06x faster                                                   |
| docutils       | 4.00 sec                                               | 3.70 sec: 1.08x faster                                                 |
| Geometric mean | (ref)                                                  | 1.05x faster                                                           |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241115-linux-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9 |
|------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_generators | 589 ms                                                 | 542 ms: 1.09x faster                                                   |
| coroutines       | 29.5 ms                                                | 33.0 ms: 1.12x slower                                                  |
| Geometric mean   | (ref)                                                  | 1.00x slower                                                           |

Benchmark hidden because not significant (3): asyncio_tcp, asyncio_tcp_ssl, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241115-linux-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 123 ms                                                 | 117 ms: 1.05x faster                                                   |
| nbody          | 119 ms                                                 | 124 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                  | 1.01x faster                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241115-linux-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.83 ms: 1.06x faster                                                  |
| regex_compile  | 187 ms                                                 | 176 ms: 1.06x faster                                                   |
| regex_v8       | 32.5 ms                                                | 34.4 ms: 1.06x slower                                                  |
| Geometric mean | (ref)                                                  | 1.01x faster                                                           |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241115-linux-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9 |
|---------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_dict         | 52.7 us                                                | 46.6 us: 1.13x faster                                                  |
| xml_etree_iterparse | 169 ms                                                 | 154 ms: 1.10x faster                                                   |
| xml_etree_parse     | 241 ms                                                 | 219 ms: 1.10x faster                                                   |
| unpickle            | 21.2 us                                                | 19.5 us: 1.09x faster                                                  |
| tomli_loads         | 2.88 sec                                               | 2.68 sec: 1.08x faster                                                 |
| xml_etree_generate  | 127 ms                                                 | 118 ms: 1.08x faster                                                   |
| unpickle_list       | 6.83 us                                                | 6.67 us: 1.02x faster                                                  |
| pickle              | 16.4 us                                                | 17.3 us: 1.05x slower                                                  |
| json_dumps          | 14.3 ms                                                | 15.3 ms: 1.07x slower                                                  |
| Geometric mean      | (ref)                                                  | 1.04x faster                                                           |

Benchmark hidden because not significant (5): json_loads, unpickle_pure_python, xml_etree_process, pickle_pure_python, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241115-linux-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 13.9 ms: 1.27x faster                                                  |
| python_startup         | 23.7 ms                                                | 20.5 ms: 1.16x faster                                                  |
| Geometric mean         | (ref)                                                  | 1.21x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241115-linux-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako           | 15.7 ms                                                | 16.5 ms: 1.05x slower                                                  |
| Geometric mean | (ref)                                                  | 1.01x slower                                                           |

Benchmark hidden because not significant (3): django_template, genshi_text, genshi_xml

All benchmarks:
===============

| Benchmark                | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241115-linux-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9 |
|--------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| deepcopy                 | 468 us                                                 | 352 us: 1.33x faster                                                   |
| deepcopy_memo            | 52.4 us                                                | 39.9 us: 1.31x faster                                                  |
| python_startup_no_site   | 17.6 ms                                                | 13.9 ms: 1.27x faster                                                  |
| comprehensions           | 27.1 us                                                | 21.9 us: 1.24x faster                                                  |
| bench_thread_pool        | 3.48 ms                                                | 2.92 ms: 1.19x faster                                                  |
| python_startup           | 23.7 ms                                                | 20.5 ms: 1.16x faster                                                  |
| pycparser                | 1.79 sec                                               | 1.56 sec: 1.15x faster                                                 |
| pyflate                  | 727 ms                                                 | 641 ms: 1.13x faster                                                   |
| pickle_dict              | 52.7 us                                                | 46.6 us: 1.13x faster                                                  |
| bpe_tokeniser            | 6.59 sec                                               | 5.83 sec: 1.13x faster                                                 |
| raytrace                 | 408 ms                                                 | 362 ms: 1.13x faster                                                   |
| logging_simple           | 9.45 us                                                | 8.48 us: 1.11x faster                                                  |
| nqueens                  | 117 ms                                                 | 105 ms: 1.11x faster                                                   |
| pathlib                  | 31.6 ms                                                | 28.6 ms: 1.11x faster                                                  |
| crypto_pyaes             | 107 ms                                                 | 97.4 ms: 1.10x faster                                                  |
| xml_etree_iterparse      | 169 ms                                                 | 154 ms: 1.10x faster                                                   |
| scimark_monte_carlo      | 96.4 ms                                                | 87.7 ms: 1.10x faster                                                  |
| xml_etree_parse          | 241 ms                                                 | 219 ms: 1.10x faster                                                   |
| unpickle                 | 21.2 us                                                | 19.5 us: 1.09x faster                                                  |
| async_generators         | 589 ms                                                 | 542 ms: 1.09x faster                                                   |
| sqlglot_normalize        | 157 ms                                                 | 145 ms: 1.08x faster                                                   |
| sqlglot_optimize         | 76.0 ms                                                | 70.2 ms: 1.08x faster                                                  |
| sympy_integrate          | 29.8 ms                                                | 27.5 ms: 1.08x faster                                                  |
| docutils                 | 4.00 sec                                               | 3.70 sec: 1.08x faster                                                 |
| fannkuch                 | 540 ms                                                 | 501 ms: 1.08x faster                                                   |
| gc_traversal             | 5.86 ms                                                | 5.44 ms: 1.08x faster                                                  |
| go                       | 172 ms                                                 | 160 ms: 1.08x faster                                                   |
| tomli_loads              | 2.88 sec                                               | 2.68 sec: 1.08x faster                                                 |
| xml_etree_generate       | 127 ms                                                 | 118 ms: 1.08x faster                                                   |
| deepcopy_reduce          | 4.04 us                                                | 3.76 us: 1.07x faster                                                  |
| sympy_str                | 385 ms                                                 | 362 ms: 1.07x faster                                                   |
| typing_runtime_protocols | 224 us                                                 | 211 us: 1.06x faster                                                   |
| regex_effbot             | 5.13 ms                                                | 4.83 ms: 1.06x faster                                                  |
| regex_compile            | 187 ms                                                 | 176 ms: 1.06x faster                                                   |
| 2to3                     | 456 ms                                                 | 431 ms: 1.06x faster                                                   |
| pprint_pformat           | 1.98 sec                                               | 1.88 sec: 1.05x faster                                                 |
| generators               | 41.1 ms                                                | 39.0 ms: 1.05x faster                                                  |
| float                    | 123 ms                                                 | 117 ms: 1.05x faster                                                   |
| mdp                      | 3.97 sec                                               | 3.79 sec: 1.05x faster                                                 |
| scimark_sparse_mat_mult  | 6.70 ms                                                | 6.39 ms: 1.05x faster                                                  |
| meteor_contest           | 146 ms                                                 | 140 ms: 1.05x faster                                                   |
| scimark_fft              | 500 ms                                                 | 480 ms: 1.04x faster                                                   |
| pprint_safe_repr         | 967 ms                                                 | 937 ms: 1.03x faster                                                   |
| unpickle_list            | 6.83 us                                                | 6.67 us: 1.02x faster                                                  |
| nbody                    | 119 ms                                                 | 124 ms: 1.04x slower                                                   |
| mako                     | 15.7 ms                                                | 16.5 ms: 1.05x slower                                                  |
| pickle                   | 16.4 us                                                | 17.3 us: 1.05x slower                                                  |
| regex_v8                 | 32.5 ms                                                | 34.4 ms: 1.06x slower                                                  |
| deltablue                | 4.27 ms                                                | 4.57 ms: 1.07x slower                                                  |
| json_dumps               | 14.3 ms                                                | 15.3 ms: 1.07x slower                                                  |
| telco                    | 9.59 ms                                                | 10.4 ms: 1.08x slower                                                  |
| coroutines               | 29.5 ms                                                | 33.0 ms: 1.12x slower                                                  |
| coverage                 | 95.4 ms                                                | 113 ms: 1.18x slower                                                   |
| create_gc_cycles         | 1.94 ms                                                | 2.42 ms: 1.25x slower                                                  |
| bench_mp_pool            | 20.7 ms                                                | 66.7 ms: 3.22x slower                                                  |
| Geometric mean           | (ref)                                                  | 1.03x faster                                                           |

Benchmark hidden because not significant (33): sympy_sum, sqlglot_transpile, json_loads, html5lib, unpickle_pure_python, pidigits, asyncio_tcp, sqlglot_parse, asyncio_tcp_ssl, richards_super, sqlite_synth, chaos, pylint, logging_format, thrift, django_template, unpack_sequence, hexiom, xml_etree_process, logging_silent, genshi_text, dulwich_log, pickle_pure_python, pickle_list, json, genshi_xml, spectral_norm, scimark_lu, asyncio_websockets, regex_dna, sympy_expand, scimark_sor, richards
Ignored benchmarks (17) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http

# HPT report

- Reliability score: 99.97% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.02x