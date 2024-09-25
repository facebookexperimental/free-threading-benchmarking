# Results vs. 3.13.0rc1+

- fork: python
- ref: ef4b69d2becf49daaea2
- machine: linux-x86_64
- commit hash: ef4b69d
- commit date: 2024-09-06
- overall geometric mean: 1.02x slower
- HPT reliability: 99.87%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|----------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| docutils       | 4.01 sec                                                | 4.22 sec: 1.05x slower                                                |
| Geometric mean | (ref)                                                   | 1.02x slower                                                          |

Benchmark hidden because not significant (3): 2to3, html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark              | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|------------------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization | 745 ms                                                  | 647 ms: 1.15x faster                                                  |
| async_tree_none        | 576 ms                                                  | 523 ms: 1.10x faster                                                  |
| async_tree_io_tg       | 1.46 sec                                                | 1.33 sec: 1.10x faster                                                |
| async_tree_none_tg     | 521 ms                                                  | 494 ms: 1.05x faster                                                  |
| asyncio_tcp_ssl        | 2.79 sec                                                | 2.90 sec: 1.04x slower                                                |
| Geometric mean         | (ref)                                                   | 1.02x faster                                                          |

Benchmark hidden because not significant (8): async_tree_memoization_tg, asyncio_tcp, async_tree_cpu_io_mixed, async_generators, asyncio_websockets, coroutines, async_tree_cpu_io_mixed_tg, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|----------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 115 ms                                                  | 125 ms: 1.09x slower                                                  |
| Geometric mean | (ref)                                                   | 1.05x slower                                                          |

Benchmark hidden because not significant (2): pidigits, nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|----------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 177 ms                                                  | 189 ms: 1.07x slower                                                  |
| regex_effbot   | 4.84 ms                                                 | 5.19 ms: 1.07x slower                                                 |
| regex_dna      | 288 ms                                                  | 310 ms: 1.08x slower                                                  |
| regex_v8       | 32.4 ms                                                 | 36.2 ms: 1.12x slower                                                 |
| Geometric mean | (ref)                                                   | 1.08x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark       | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|-----------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads     | 2.80 sec                                                | 2.72 sec: 1.03x faster                                                |
| json_loads      | 36.1 us                                                 | 37.8 us: 1.05x slower                                                 |
| pickle_list     | 6.82 us                                                 | 7.25 us: 1.06x slower                                                 |
| xml_etree_parse | 236 ms                                                  | 253 ms: 1.07x slower                                                  |
| unpickle_list   | 6.67 us                                                 | 7.18 us: 1.08x slower                                                 |
| Geometric mean  | (ref)                                                   | 1.02x slower                                                          |

Benchmark hidden because not significant (9): unpickle, pickle_dict, xml_etree_generate, xml_etree_process, pickle_pure_python, unpickle_pure_python, pickle, xml_etree_iterparse, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|------------------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 22.0 ms                                                 | 26.1 ms: 1.18x slower                                                 |
| python_startup_no_site | 14.6 ms                                                 | 17.7 ms: 1.21x slower                                                 |
| Geometric mean         | (ref)                                                   | 1.20x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|----------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml     | 68.3 ms                                                 | 72.3 ms: 1.06x slower                                                 |
| mako           | 16.1 ms                                                 | 18.5 ms: 1.15x slower                                                 |
| Geometric mean | (ref)                                                   | 1.05x slower                                                          |

Benchmark hidden because not significant (2): genshi_text, django_template

All benchmarks:
===============

| Benchmark                | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|--------------------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| deepcopy                 | 484 us                                                  | 362 us: 1.34x faster                                                  |
| deepcopy_memo            | 51.7 us                                                 | 39.5 us: 1.31x faster                                                 |
| go                       | 195 ms                                                  | 168 ms: 1.16x faster                                                  |
| async_tree_memoization   | 745 ms                                                  | 647 ms: 1.15x faster                                                  |
| scimark_sparse_mat_mult  | 6.98 ms                                                 | 6.13 ms: 1.14x faster                                                 |
| async_tree_none          | 576 ms                                                  | 523 ms: 1.10x faster                                                  |
| async_tree_io_tg         | 1.46 sec                                                | 1.33 sec: 1.10x faster                                                |
| richards_super           | 76.3 ms                                                 | 71.0 ms: 1.07x faster                                                 |
| async_tree_none_tg       | 521 ms                                                  | 494 ms: 1.05x faster                                                  |
| crypto_pyaes             | 99.8 ms                                                 | 95.7 ms: 1.04x faster                                                 |
| tomli_loads              | 2.80 sec                                                | 2.72 sec: 1.03x faster                                                |
| bpe_tokeniser            | 6.25 sec                                                | 6.41 sec: 1.03x slower                                                |
| mdp                      | 3.80 sec                                                | 3.93 sec: 1.04x slower                                                |
| asyncio_tcp_ssl          | 2.79 sec                                                | 2.90 sec: 1.04x slower                                                |
| pprint_safe_repr         | 959 ms                                                  | 1.00 sec: 1.04x slower                                                |
| json_loads               | 36.1 us                                                 | 37.8 us: 1.05x slower                                                 |
| generators               | 39.2 ms                                                 | 41.1 ms: 1.05x slower                                                 |
| nqueens                  | 108 ms                                                  | 114 ms: 1.05x slower                                                  |
| comprehensions           | 20.9 us                                                 | 22.1 us: 1.05x slower                                                 |
| docutils                 | 4.01 sec                                                | 4.22 sec: 1.05x slower                                                |
| genshi_xml               | 68.3 ms                                                 | 72.3 ms: 1.06x slower                                                 |
| pickle_list              | 6.82 us                                                 | 7.25 us: 1.06x slower                                                 |
| regex_compile            | 177 ms                                                  | 189 ms: 1.07x slower                                                  |
| typing_runtime_protocols | 216 us                                                  | 231 us: 1.07x slower                                                  |
| regex_effbot             | 4.84 ms                                                 | 5.19 ms: 1.07x slower                                                 |
| xml_etree_parse          | 236 ms                                                  | 253 ms: 1.07x slower                                                  |
| regex_dna                | 288 ms                                                  | 310 ms: 1.08x slower                                                  |
| dulwich_log              | 100.0 ms                                                | 108 ms: 1.08x slower                                                  |
| unpickle_list            | 6.67 us                                                 | 7.18 us: 1.08x slower                                                 |
| float                    | 115 ms                                                  | 125 ms: 1.09x slower                                                  |
| sympy_str                | 367 ms                                                  | 402 ms: 1.09x slower                                                  |
| json                     | 6.55 ms                                                 | 7.18 ms: 1.10x slower                                                 |
| create_gc_cycles         | 2.46 ms                                                 | 2.70 ms: 1.10x slower                                                 |
| coverage                 | 110 ms                                                  | 121 ms: 1.10x slower                                                  |
| logging_silent           | 130 ns                                                  | 143 ns: 1.10x slower                                                  |
| hexiom                   | 8.35 ms                                                 | 9.21 ms: 1.10x slower                                                 |
| pyflate                  | 661 ms                                                  | 735 ms: 1.11x slower                                                  |
| regex_v8                 | 32.4 ms                                                 | 36.2 ms: 1.12x slower                                                 |
| pycparser                | 1.57 sec                                                | 1.79 sec: 1.14x slower                                                |
| mako                     | 16.1 ms                                                 | 18.5 ms: 1.15x slower                                                 |
| python_startup           | 22.0 ms                                                 | 26.1 ms: 1.18x slower                                                 |
| python_startup_no_site   | 14.6 ms                                                 | 17.7 ms: 1.21x slower                                                 |
| bench_thread_pool        | 3.06 ms                                                 | 3.89 ms: 1.27x slower                                                 |
| bench_mp_pool            | 19.4 ms                                                 | 26.6 ms: 1.37x slower                                                 |
| Geometric mean           | (ref)                                                   | 1.02x slower                                                          |

Benchmark hidden because not significant (53): async_tree_memoization_tg, logging_simple, deepcopy_reduce, html5lib, scimark_lu, unpickle, meteor_contest, unpack_sequence, pickle_dict, genshi_text, scimark_fft, asyncio_tcp, chaos, sqlite_synth, xml_etree_generate, sympy_sum, sqlglot_transpile, async_tree_cpu_io_mixed, scimark_monte_carlo, django_template, pprint_pformat, scimark_sor, async_generators, xml_etree_process, pickle_pure_python, richards, sympy_expand, sqlglot_optimize, sympy_integrate, spectral_norm, unpickle_pure_python, pickle, telco, asyncio_websockets, 2to3, logging_format, coroutines, pidigits, raytrace, async_tree_cpu_io_mixed_tg, xml_etree_iterparse, async_tree_io, json_dumps, sqlglot_parse, fannkuch, sqlglot_normalize, nbody, pathlib, gc_traversal, deltablue, thrift, tornado_http, pylint
Ignored benchmarks (5) of results/bm-20240814-3.13.0rc1+-79452b1/bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1.json: aiohttp, chameleon, dask, flaskblogging, gunicorn

# HPT report

- Reliability score: 99.87% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.01x