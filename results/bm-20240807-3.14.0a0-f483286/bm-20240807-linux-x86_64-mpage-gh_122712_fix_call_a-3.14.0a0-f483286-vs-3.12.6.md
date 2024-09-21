# Results vs. 3.12.6

- fork: mpage
- ref: gh_122712_fix_call_a
- machine: linux-x86_64
- commit hash: f483286
- commit date: 2024-08-07
- overall geometric mean: 1.06x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

Benchmark hidden because not significant (4): 2to3, docutils, html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_none_tg         | 704 ms                                                 | 456 ms: 1.54x faster                                                 |
| async_tree_memoization_tg  | 930 ms                                                 | 609 ms: 1.53x faster                                                 |
| async_tree_memoization     | 977 ms                                                 | 643 ms: 1.52x faster                                                 |
| async_tree_io_tg           | 1.93 sec                                               | 1.29 sec: 1.50x faster                                               |
| async_tree_none            | 741 ms                                                 | 512 ms: 1.45x faster                                                 |
| async_tree_io              | 1.85 sec                                               | 1.30 sec: 1.42x faster                                               |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 826 ms: 1.33x faster                                                 |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 819 ms: 1.32x faster                                                 |
| coroutines                 | 29.5 ms                                                | 31.1 ms: 1.05x slower                                                |
| Geometric mean             | (ref)                                                  | 1.25x faster                                                         |

Benchmark hidden because not significant (4): asyncio_tcp_ssl, async_generators, asyncio_tcp, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| nbody          | 119 ms                                                 | 111 ms: 1.08x faster                                                 |
| float          | 123 ms                                                 | 117 ms: 1.05x faster                                                 |
| Geometric mean | (ref)                                                  | 1.05x faster                                                         |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_compile  | 187 ms                                                 | 178 ms: 1.05x faster                                                 |
| regex_v8       | 32.5 ms                                                | 34.2 ms: 1.05x slower                                                |
| Geometric mean | (ref)                                                  | 1.00x faster                                                         |

Benchmark hidden because not significant (2): regex_effbot, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| pickle_dict          | 52.7 us                                                | 45.2 us: 1.17x faster                                                |
| xml_etree_process    | 83.7 ms                                                | 76.7 ms: 1.09x faster                                                |
| xml_etree_parse      | 241 ms                                                 | 222 ms: 1.09x faster                                                 |
| unpickle_pure_python | 300 us                                                 | 282 us: 1.06x faster                                                 |
| xml_etree_generate   | 127 ms                                                 | 120 ms: 1.06x faster                                                 |
| pickle               | 16.4 us                                                | 15.5 us: 1.06x faster                                                |
| tomli_loads          | 2.88 sec                                               | 2.74 sec: 1.05x faster                                               |
| unpickle_list        | 6.83 us                                                | 7.43 us: 1.09x slower                                                |
| json_dumps           | 14.3 ms                                                | 15.7 ms: 1.10x slower                                                |
| Geometric mean       | (ref)                                                  | 1.04x faster                                                         |

Benchmark hidden because not significant (5): unpickle, pickle_pure_python, json_loads, xml_etree_iterparse, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 14.9 ms: 1.18x faster                                                |
| python_startup         | 23.7 ms                                                | 21.6 ms: 1.10x faster                                                |
| Geometric mean         | (ref)                                                  | 1.14x faster                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_text    | 30.2 ms                                                | 32.3 ms: 1.07x slower                                                |
| Geometric mean | (ref)                                                  | 1.03x slower                                                         |

Benchmark hidden because not significant (3): django_template, genshi_xml, mako

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_none_tg         | 704 ms                                                 | 456 ms: 1.54x faster                                                 |
| async_tree_memoization_tg  | 930 ms                                                 | 609 ms: 1.53x faster                                                 |
| async_tree_memoization     | 977 ms                                                 | 643 ms: 1.52x faster                                                 |
| async_tree_io_tg           | 1.93 sec                                               | 1.29 sec: 1.50x faster                                               |
| async_tree_none            | 741 ms                                                 | 512 ms: 1.45x faster                                                 |
| async_tree_io              | 1.85 sec                                               | 1.30 sec: 1.42x faster                                               |
| deepcopy                   | 468 us                                                 | 346 us: 1.35x faster                                                 |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 826 ms: 1.33x faster                                                 |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 819 ms: 1.32x faster                                                 |
| deepcopy_memo              | 52.4 us                                                | 40.8 us: 1.29x faster                                                |
| comprehensions             | 27.1 us                                                | 21.7 us: 1.25x faster                                                |
| raytrace                   | 408 ms                                                 | 331 ms: 1.23x faster                                                 |
| python_startup_no_site     | 17.6 ms                                                | 14.9 ms: 1.18x faster                                                |
| pickle_dict                | 52.7 us                                                | 45.2 us: 1.17x faster                                                |
| deepcopy_reduce            | 4.04 us                                                | 3.50 us: 1.15x faster                                                |
| pycparser                  | 1.79 sec                                               | 1.58 sec: 1.13x faster                                               |
| logging_simple             | 9.45 us                                                | 8.40 us: 1.12x faster                                                |
| pathlib                    | 31.6 ms                                                | 28.8 ms: 1.10x faster                                                |
| mdp                        | 3.97 sec                                               | 3.62 sec: 1.10x faster                                               |
| python_startup             | 23.7 ms                                                | 21.6 ms: 1.10x faster                                                |
| xml_etree_process          | 83.7 ms                                                | 76.7 ms: 1.09x faster                                                |
| sqlglot_normalize          | 157 ms                                                 | 144 ms: 1.09x faster                                                 |
| xml_etree_parse            | 241 ms                                                 | 222 ms: 1.09x faster                                                 |
| logging_silent             | 139 ns                                                 | 128 ns: 1.09x faster                                                 |
| pyflate                    | 727 ms                                                 | 671 ms: 1.08x faster                                                 |
| sqlglot_optimize           | 76.0 ms                                                | 70.4 ms: 1.08x faster                                                |
| scimark_monte_carlo        | 96.4 ms                                                | 89.4 ms: 1.08x faster                                                |
| nqueens                    | 117 ms                                                 | 108 ms: 1.08x faster                                                 |
| nbody                      | 119 ms                                                 | 111 ms: 1.08x faster                                                 |
| gc_traversal               | 5.86 ms                                                | 5.46 ms: 1.07x faster                                                |
| scimark_lu                 | 152 ms                                                 | 142 ms: 1.07x faster                                                 |
| unpickle_pure_python       | 300 us                                                 | 282 us: 1.06x faster                                                 |
| xml_etree_generate         | 127 ms                                                 | 120 ms: 1.06x faster                                                 |
| pickle                     | 16.4 us                                                | 15.5 us: 1.06x faster                                                |
| tomli_loads                | 2.88 sec                                               | 2.74 sec: 1.05x faster                                               |
| sympy_str                  | 385 ms                                                 | 367 ms: 1.05x faster                                                 |
| bpe_tokeniser              | 6.59 sec                                               | 6.28 sec: 1.05x faster                                               |
| float                      | 123 ms                                                 | 117 ms: 1.05x faster                                                 |
| regex_compile              | 187 ms                                                 | 178 ms: 1.05x faster                                                 |
| meteor_contest             | 146 ms                                                 | 140 ms: 1.04x faster                                                 |
| scimark_fft                | 500 ms                                                 | 480 ms: 1.04x faster                                                 |
| pprint_pformat             | 1.98 sec                                               | 1.93 sec: 1.02x faster                                               |
| regex_v8                   | 32.5 ms                                                | 34.2 ms: 1.05x slower                                                |
| coroutines                 | 29.5 ms                                                | 31.1 ms: 1.05x slower                                                |
| sympy_expand               | 582 ms                                                 | 618 ms: 1.06x slower                                                 |
| thrift                     | 1.06 ms                                                | 1.13 ms: 1.06x slower                                                |
| genshi_text                | 30.2 ms                                                | 32.3 ms: 1.07x slower                                                |
| deltablue                  | 4.27 ms                                                | 4.57 ms: 1.07x slower                                                |
| unpickle_list              | 6.83 us                                                | 7.43 us: 1.09x slower                                                |
| bench_mp_pool              | 20.7 ms                                                | 22.7 ms: 1.10x slower                                                |
| json_dumps                 | 14.3 ms                                                | 15.7 ms: 1.10x slower                                                |
| create_gc_cycles           | 1.94 ms                                                | 2.14 ms: 1.10x slower                                                |
| telco                      | 9.59 ms                                                | 10.8 ms: 1.12x slower                                                |
| go                         | 172 ms                                                 | 195 ms: 1.13x slower                                                 |
| coverage                   | 95.4 ms                                                | 111 ms: 1.16x slower                                                 |
| unpack_sequence            | 60.2 ns                                                | 76.4 ns: 1.27x slower                                                |
| Geometric mean             | (ref)                                                  | 1.06x faster                                                         |

Benchmark hidden because not significant (40): bench_thread_pool, sqlglot_transpile, unpickle, 2to3, pickle_pure_python, regex_effbot, sqlglot_parse, scimark_sparse_mat_mult, typing_runtime_protocols, json_loads, xml_etree_iterparse, generators, fannkuch, spectral_norm, sqlite_synth, scimark_sor, pidigits, chaos, richards_super, logging_format, docutils, asyncio_tcp_ssl, richards, sympy_sum, async_generators, asyncio_tcp, pprint_safe_repr, pickle_list, django_template, crypto_pyaes, tornado_http, genshi_xml, pylint, sympy_integrate, asyncio_websockets, hexiom, regex_dna, json, mako, html5lib
Ignored benchmarks (9) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.01x