# Results vs. 3.12.6

- fork: python
- ref: 2a6b6b33dfe0f3c435ab
- machine: linux-x86_64
- commit hash: 2a6b6b3
- commit date: 2024-11-06
- overall geometric mean: 1.01x faster
- HPT reliability: 97.17%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241106-linux-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 434 ms: 1.05x faster                                                   |
| docutils       | 4.00 sec                                               | 3.75 sec: 1.07x faster                                                 |
| Geometric mean | (ref)                                                  | 1.04x faster                                                           |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241106-linux-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| asyncio_tcp    | 923 ms                                                 | 884 ms: 1.04x faster                                                   |
| coroutines     | 29.5 ms                                                | 32.4 ms: 1.10x slower                                                  |
| Geometric mean | (ref)                                                  | 1.00x slower                                                           |

Benchmark hidden because not significant (3): async_generators, asyncio_tcp_ssl, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241106-linux-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 123 ms                                                 | 117 ms: 1.05x faster                                                   |
| nbody          | 119 ms                                                 | 134 ms: 1.12x slower                                                   |
| Geometric mean | (ref)                                                  | 1.02x slower                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241106-linux-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 187 ms                                                 | 169 ms: 1.10x faster                                                   |
| Geometric mean | (ref)                                                  | 1.02x faster                                                           |

Benchmark hidden because not significant (3): regex_effbot, regex_v8, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark          | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241106-linux-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3 |
|--------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_dict        | 52.7 us                                                | 46.1 us: 1.14x faster                                                  |
| pickle             | 16.4 us                                                | 15.4 us: 1.06x faster                                                  |
| tomli_loads        | 2.88 sec                                               | 2.77 sec: 1.04x faster                                                 |
| pickle_pure_python | 436 us                                                 | 463 us: 1.06x slower                                                   |
| json_dumps         | 14.3 ms                                                | 15.9 ms: 1.11x slower                                                  |
| Geometric mean     | (ref)                                                  | 1.01x faster                                                           |

Benchmark hidden because not significant (9): unpickle, xml_etree_generate, xml_etree_parse, unpickle_pure_python, pickle_list, json_loads, xml_etree_iterparse, unpickle_list, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241106-linux-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 13.9 ms: 1.26x faster                                                  |
| python_startup         | 23.7 ms                                                | 20.1 ms: 1.18x faster                                                  |
| Geometric mean         | (ref)                                                  | 1.22x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241106-linux-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 44.9 ms                                                | 48.7 ms: 1.08x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.03x slower                                                           |

Benchmark hidden because not significant (3): mako, genshi_xml, genshi_text

All benchmarks:
===============

| Benchmark                | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241106-linux-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3 |
|--------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site   | 17.6 ms                                                | 13.9 ms: 1.26x faster                                                  |
| deepcopy                 | 468 us                                                 | 373 us: 1.25x faster                                                   |
| bench_thread_pool        | 3.48 ms                                                | 2.80 ms: 1.24x faster                                                  |
| deepcopy_memo            | 52.4 us                                                | 42.9 us: 1.22x faster                                                  |
| python_startup           | 23.7 ms                                                | 20.1 ms: 1.18x faster                                                  |
| logging_simple           | 9.45 us                                                | 8.09 us: 1.17x faster                                                  |
| raytrace                 | 408 ms                                                 | 354 ms: 1.15x faster                                                   |
| mdp                      | 3.97 sec                                               | 3.45 sec: 1.15x faster                                                 |
| pickle_dict              | 52.7 us                                                | 46.1 us: 1.14x faster                                                  |
| comprehensions           | 27.1 us                                                | 23.8 us: 1.14x faster                                                  |
| bpe_tokeniser            | 6.59 sec                                               | 5.84 sec: 1.13x faster                                                 |
| pycparser                | 1.79 sec                                               | 1.59 sec: 1.13x faster                                                 |
| pyflate                  | 727 ms                                                 | 649 ms: 1.12x faster                                                   |
| pathlib                  | 31.6 ms                                                | 28.6 ms: 1.10x faster                                                  |
| regex_compile            | 187 ms                                                 | 169 ms: 1.10x faster                                                   |
| scimark_monte_carlo      | 96.4 ms                                                | 88.4 ms: 1.09x faster                                                  |
| sqlglot_normalize        | 157 ms                                                 | 146 ms: 1.08x faster                                                   |
| deepcopy_reduce          | 4.04 us                                                | 3.77 us: 1.07x faster                                                  |
| generators               | 41.1 ms                                                | 38.5 ms: 1.07x faster                                                  |
| sympy_sum                | 222 ms                                                 | 208 ms: 1.07x faster                                                   |
| docutils                 | 4.00 sec                                               | 3.75 sec: 1.07x faster                                                 |
| pickle                   | 16.4 us                                                | 15.4 us: 1.06x faster                                                  |
| typing_runtime_protocols | 224 us                                                 | 212 us: 1.06x faster                                                   |
| 2to3                     | 456 ms                                                 | 434 ms: 1.05x faster                                                   |
| float                    | 123 ms                                                 | 117 ms: 1.05x faster                                                   |
| asyncio_tcp              | 923 ms                                                 | 884 ms: 1.04x faster                                                   |
| gc_traversal             | 5.86 ms                                                | 5.61 ms: 1.04x faster                                                  |
| go                       | 172 ms                                                 | 165 ms: 1.04x faster                                                   |
| tomli_loads              | 2.88 sec                                               | 2.77 sec: 1.04x faster                                                 |
| sympy_str                | 385 ms                                                 | 371 ms: 1.04x faster                                                   |
| sympy_expand             | 582 ms                                                 | 604 ms: 1.04x slower                                                   |
| pickle_pure_python       | 436 us                                                 | 463 us: 1.06x slower                                                   |
| django_template          | 44.9 ms                                                | 48.7 ms: 1.08x slower                                                  |
| deltablue                | 4.27 ms                                                | 4.64 ms: 1.09x slower                                                  |
| coroutines               | 29.5 ms                                                | 32.4 ms: 1.10x slower                                                  |
| scimark_sor              | 167 ms                                                 | 183 ms: 1.10x slower                                                   |
| json_dumps               | 14.3 ms                                                | 15.9 ms: 1.11x slower                                                  |
| telco                    | 9.59 ms                                                | 10.7 ms: 1.11x slower                                                  |
| thrift                   | 1.06 ms                                                | 1.19 ms: 1.12x slower                                                  |
| nbody                    | 119 ms                                                 | 134 ms: 1.12x slower                                                   |
| logging_format           | 9.59 us                                                | 10.8 us: 1.13x slower                                                  |
| coverage                 | 95.4 ms                                                | 111 ms: 1.16x slower                                                   |
| richards                 | 60.3 ms                                                | 70.1 ms: 1.16x slower                                                  |
| create_gc_cycles         | 1.94 ms                                                | 2.48 ms: 1.28x slower                                                  |
| bench_mp_pool            | 20.7 ms                                                | 67.7 ms: 3.27x slower                                                  |
| Geometric mean           | (ref)                                                  | 1.01x faster                                                           |

Benchmark hidden because not significant (43): dulwich_log, unpickle, crypto_pyaes, xml_etree_generate, nqueens, xml_etree_parse, scimark_sparse_mat_mult, json, unpickle_pure_python, pidigits, regex_effbot, sqlglot_optimize, pprint_pformat, html5lib, async_generators, asyncio_tcp_ssl, pylint, mako, asyncio_websockets, scimark_fft, pickle_list, regex_v8, json_loads, fannkuch, richards_super, sympy_integrate, xml_etree_iterparse, logging_silent, chaos, sqlite_synth, spectral_norm, unpickle_list, meteor_contest, genshi_xml, hexiom, scimark_lu, unpack_sequence, pprint_safe_repr, sqlglot_parse, xml_etree_process, sqlglot_transpile, regex_dna, genshi_text
Ignored benchmarks (17) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http

# HPT report

- Reliability score: 97.17% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.02x