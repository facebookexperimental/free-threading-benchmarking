# Results vs. 3.12.6

- fork: python
- ref: d0bfff47fb2aea9272b5
- machine: linux-x86_64
- commit hash: d0bfff4
- commit date: 2024-10-21
- overall geometric mean: 1.00x faster
- HPT reliability: 80.43%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

Benchmark hidden because not significant (4): 2to3, docutils, html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241021-linux-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4 |
|--------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| asyncio_websockets | 748 ms                                                 | 771 ms: 1.03x slower                                                   |
| asyncio_tcp        | 923 ms                                                 | 968 ms: 1.05x slower                                                   |
| coroutines         | 29.5 ms                                                | 31.7 ms: 1.07x slower                                                  |
| Geometric mean     | (ref)                                                  | 1.03x slower                                                           |

Benchmark hidden because not significant (2): async_generators, asyncio_tcp_ssl

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241021-linux-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 123 ms                                                 | 112 ms: 1.10x faster                                                   |
| nbody          | 119 ms                                                 | 124 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                  | 1.02x faster                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241021-linux-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_dna      | 278 ms                                                 | 290 ms: 1.04x slower                                                   |
| regex_v8       | 32.5 ms                                                | 34.5 ms: 1.06x slower                                                  |
| Geometric mean | (ref)                                                  | 1.01x slower                                                           |

Benchmark hidden because not significant (2): regex_compile, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241021-linux-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_dict          | 52.7 us                                                | 44.7 us: 1.18x faster                                                  |
| json_loads           | 37.9 us                                                | 35.0 us: 1.08x faster                                                  |
| xml_etree_generate   | 127 ms                                                 | 118 ms: 1.07x faster                                                   |
| pickle_list          | 6.97 us                                                | 6.51 us: 1.07x faster                                                  |
| xml_etree_iterparse  | 169 ms                                                 | 158 ms: 1.07x faster                                                   |
| xml_etree_parse      | 241 ms                                                 | 226 ms: 1.06x faster                                                   |
| pickle               | 16.4 us                                                | 15.6 us: 1.05x faster                                                  |
| json_dumps           | 14.3 ms                                                | 15.1 ms: 1.06x slower                                                  |
| unpickle_pure_python | 300 us                                                 | 331 us: 1.11x slower                                                   |
| unpickle_list        | 6.83 us                                                | 7.63 us: 1.12x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                           |

Benchmark hidden because not significant (4): unpickle, tomli_loads, xml_etree_process, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241021-linux-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 15.3 ms: 1.15x faster                                                  |
| python_startup         | 23.7 ms                                                | 22.3 ms: 1.06x faster                                                  |
| Geometric mean         | (ref)                                                  | 1.10x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241021-linux-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako           | 15.7 ms                                                | 16.6 ms: 1.05x slower                                                  |
| genshi_xml     | 67.6 ms                                                | 71.7 ms: 1.06x slower                                                  |
| genshi_text    | 30.2 ms                                                | 32.7 ms: 1.08x slower                                                  |
| Geometric mean | (ref)                                                  | 1.05x slower                                                           |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark               | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241021-linux-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4 |
|-------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| deepcopy_memo           | 52.4 us                                                | 40.2 us: 1.30x faster                                                  |
| deepcopy                | 468 us                                                 | 366 us: 1.28x faster                                                   |
| bench_thread_pool       | 3.48 ms                                                | 2.79 ms: 1.25x faster                                                  |
| comprehensions          | 27.1 us                                                | 22.5 us: 1.20x faster                                                  |
| pickle_dict             | 52.7 us                                                | 44.7 us: 1.18x faster                                                  |
| raytrace                | 408 ms                                                 | 354 ms: 1.15x faster                                                   |
| python_startup_no_site  | 17.6 ms                                                | 15.3 ms: 1.15x faster                                                  |
| pycparser               | 1.79 sec                                               | 1.57 sec: 1.14x faster                                                 |
| deepcopy_reduce         | 4.04 us                                                | 3.61 us: 1.12x faster                                                  |
| crypto_pyaes            | 107 ms                                                 | 96.1 ms: 1.12x faster                                                  |
| pathlib                 | 31.6 ms                                                | 28.5 ms: 1.11x faster                                                  |
| float                   | 123 ms                                                 | 112 ms: 1.10x faster                                                   |
| gc_traversal            | 5.86 ms                                                | 5.38 ms: 1.09x faster                                                  |
| logging_simple          | 9.45 us                                                | 8.71 us: 1.09x faster                                                  |
| bpe_tokeniser           | 6.59 sec                                               | 6.08 sec: 1.08x faster                                                 |
| json_loads              | 37.9 us                                                | 35.0 us: 1.08x faster                                                  |
| sqlglot_normalize       | 157 ms                                                 | 146 ms: 1.08x faster                                                   |
| pyflate                 | 727 ms                                                 | 674 ms: 1.08x faster                                                   |
| xml_etree_generate      | 127 ms                                                 | 118 ms: 1.07x faster                                                   |
| pickle_list             | 6.97 us                                                | 6.51 us: 1.07x faster                                                  |
| xml_etree_iterparse     | 169 ms                                                 | 158 ms: 1.07x faster                                                   |
| dulwich_log             | 100 ms                                                 | 94.0 ms: 1.07x faster                                                  |
| xml_etree_parse         | 241 ms                                                 | 226 ms: 1.06x faster                                                   |
| python_startup          | 23.7 ms                                                | 22.3 ms: 1.06x faster                                                  |
| go                      | 172 ms                                                 | 163 ms: 1.06x faster                                                   |
| sympy_str               | 385 ms                                                 | 365 ms: 1.05x faster                                                   |
| scimark_monte_carlo     | 96.4 ms                                                | 91.4 ms: 1.05x faster                                                  |
| pickle                  | 16.4 us                                                | 15.6 us: 1.05x faster                                                  |
| fannkuch                | 540 ms                                                 | 517 ms: 1.04x faster                                                   |
| logging_silent          | 139 ns                                                 | 133 ns: 1.04x faster                                                   |
| scimark_fft             | 500 ms                                                 | 481 ms: 1.04x faster                                                   |
| generators              | 41.1 ms                                                | 39.6 ms: 1.04x faster                                                  |
| asyncio_websockets      | 748 ms                                                 | 771 ms: 1.03x slower                                                   |
| nbody                   | 119 ms                                                 | 124 ms: 1.04x slower                                                   |
| scimark_sor             | 167 ms                                                 | 173 ms: 1.04x slower                                                   |
| deltablue               | 4.27 ms                                                | 4.43 ms: 1.04x slower                                                  |
| regex_dna               | 278 ms                                                 | 290 ms: 1.04x slower                                                   |
| asyncio_tcp             | 923 ms                                                 | 968 ms: 1.05x slower                                                   |
| mako                    | 15.7 ms                                                | 16.6 ms: 1.05x slower                                                  |
| sympy_expand            | 582 ms                                                 | 613 ms: 1.05x slower                                                   |
| json_dumps              | 14.3 ms                                                | 15.1 ms: 1.06x slower                                                  |
| genshi_xml              | 67.6 ms                                                | 71.7 ms: 1.06x slower                                                  |
| regex_v8                | 32.5 ms                                                | 34.5 ms: 1.06x slower                                                  |
| sqlite_synth            | 3.87 us                                                | 4.13 us: 1.07x slower                                                  |
| coroutines              | 29.5 ms                                                | 31.7 ms: 1.07x slower                                                  |
| scimark_sparse_mat_mult | 6.70 ms                                                | 7.24 ms: 1.08x slower                                                  |
| genshi_text             | 30.2 ms                                                | 32.7 ms: 1.08x slower                                                  |
| unpack_sequence         | 60.2 ns                                                | 66.1 ns: 1.10x slower                                                  |
| unpickle_pure_python    | 300 us                                                 | 331 us: 1.11x slower                                                   |
| unpickle_list           | 6.83 us                                                | 7.63 us: 1.12x slower                                                  |
| telco                   | 9.59 ms                                                | 11.2 ms: 1.16x slower                                                  |
| coverage                | 95.4 ms                                                | 115 ms: 1.20x slower                                                   |
| create_gc_cycles        | 1.94 ms                                                | 2.43 ms: 1.26x slower                                                  |
| bench_mp_pool           | 20.7 ms                                                | 69.4 ms: 3.35x slower                                                  |
| Geometric mean          | (ref)                                                  | 1.00x faster                                                           |

Benchmark hidden because not significant (35): nqueens, richards_super, regex_compile, unpickle, sympy_sum, regex_effbot, 2to3, typing_runtime_protocols, html5lib, pprint_safe_repr, chaos, logging_format, meteor_contest, richards, sqlglot_parse, pprint_pformat, mdp, tomli_loads, async_generators, asyncio_tcp_ssl, pidigits, json, xml_etree_process, docutils, spectral_norm, sqlglot_transpile, django_template, scimark_lu, sympy_integrate, pickle_pure_python, sqlglot_optimize, thrift, hexiom, tornado_http, pylint
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 80.43% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.02x