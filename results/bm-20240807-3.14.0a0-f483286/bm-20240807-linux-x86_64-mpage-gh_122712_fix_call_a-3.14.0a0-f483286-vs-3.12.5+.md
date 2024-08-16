# Results vs. 3.12.5+

- fork: mpage
- ref: gh_122712_fix_call_a
- machine: linux-x86_64
- commit hash: f483286
- commit date: 2024-08-07
- overall geometric mean: 1.06x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------|:----------------------------------------------------:|:--------------------------------------------------------------------:|
| docutils       | 4.05 sec                                             | 3.95 sec: 1.02x faster                                               |
| html5lib       | 100 ms                                               | 91.1 ms: 1.10x faster                                                |
| Geometric mean | (ref)                                                | 1.03x faster                                                         |

Benchmark hidden because not significant (2): 2to3, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------------------|:----------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_none            | 820 ms                                               | 512 ms: 1.60x faster                                                 |
| async_tree_none_tg         | 726 ms                                               | 456 ms: 1.59x faster                                                 |
| async_tree_memoization     | 975 ms                                               | 643 ms: 1.52x faster                                                 |
| async_tree_memoization_tg  | 912 ms                                               | 609 ms: 1.50x faster                                                 |
| async_tree_io_tg           | 1.87 sec                                             | 1.29 sec: 1.45x faster                                               |
| async_tree_io              | 1.86 sec                                             | 1.30 sec: 1.43x faster                                               |
| async_tree_cpu_io_mixed    | 1.14 sec                                             | 819 ms: 1.39x faster                                                 |
| async_tree_cpu_io_mixed_tg | 1.12 sec                                             | 826 ms: 1.36x faster                                                 |
| asyncio_tcp                | 988 ms                                               | 925 ms: 1.07x faster                                                 |
| async_generators           | 615 ms                                               | 588 ms: 1.04x faster                                                 |
| Geometric mean             | (ref)                                                | 1.28x faster                                                         |

Benchmark hidden because not significant (3): asyncio_tcp_ssl, asyncio_websockets, coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------|:----------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 124 ms                                               | 117 ms: 1.06x faster                                                 |
| nbody          | 117 ms                                               | 111 ms: 1.05x faster                                                 |
| pidigits       | 256 ms                                               | 245 ms: 1.05x faster                                                 |
| Geometric mean | (ref)                                                | 1.05x faster                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------|:----------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_compile  | 186 ms                                               | 178 ms: 1.05x faster                                                 |
| regex_dna      | 268 ms                                               | 283 ms: 1.06x slower                                                 |
| regex_v8       | 29.9 ms                                              | 34.2 ms: 1.14x slower                                                |
| Geometric mean | (ref)                                                | 1.03x slower                                                         |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------------|:----------------------------------------------------:|:--------------------------------------------------------------------:|
| xml_etree_generate   | 138 ms                                               | 120 ms: 1.15x faster                                                 |
| xml_etree_parse      | 244 ms                                               | 222 ms: 1.10x faster                                                 |
| xml_etree_process    | 82.7 ms                                              | 76.7 ms: 1.08x faster                                                |
| unpickle_pure_python | 304 us                                               | 282 us: 1.08x faster                                                 |
| unpickle             | 21.6 us                                              | 20.4 us: 1.06x faster                                                |
| tomli_loads          | 2.86 sec                                             | 2.74 sec: 1.04x faster                                               |
| unpickle_list        | 6.83 us                                              | 7.43 us: 1.09x slower                                                |
| json_dumps           | 14.0 ms                                              | 15.7 ms: 1.12x slower                                                |
| Geometric mean       | (ref)                                                | 1.03x faster                                                         |

Benchmark hidden because not significant (6): xml_etree_iterparse, pickle_pure_python, pickle, pickle_dict, pickle_list, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|------------------------|:----------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 16.2 ms                                              | 14.9 ms: 1.09x faster                                                |
| python_startup         | 22.7 ms                                              | 21.6 ms: 1.05x faster                                                |
| Geometric mean         | (ref)                                                | 1.07x faster                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------|:----------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_text    | 30.3 ms                                              | 32.3 ms: 1.07x slower                                                |
| Geometric mean | (ref)                                                | 1.01x slower                                                         |

Benchmark hidden because not significant (3): genshi_xml, django_template, mako

All benchmarks:
===============

| Benchmark                  | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------------------|:----------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_none            | 820 ms                                               | 512 ms: 1.60x faster                                                 |
| async_tree_none_tg         | 726 ms                                               | 456 ms: 1.59x faster                                                 |
| async_tree_memoization     | 975 ms                                               | 643 ms: 1.52x faster                                                 |
| async_tree_memoization_tg  | 912 ms                                               | 609 ms: 1.50x faster                                                 |
| async_tree_io_tg           | 1.87 sec                                             | 1.29 sec: 1.45x faster                                               |
| async_tree_io              | 1.86 sec                                             | 1.30 sec: 1.43x faster                                               |
| deepcopy                   | 486 us                                               | 346 us: 1.40x faster                                                 |
| async_tree_cpu_io_mixed    | 1.14 sec                                             | 819 ms: 1.39x faster                                                 |
| async_tree_cpu_io_mixed_tg | 1.12 sec                                             | 826 ms: 1.36x faster                                                 |
| comprehensions             | 28.6 us                                              | 21.7 us: 1.32x faster                                                |
| deepcopy_memo              | 51.0 us                                              | 40.8 us: 1.25x faster                                                |
| raytrace                   | 405 ms                                               | 331 ms: 1.22x faster                                                 |
| deepcopy_reduce            | 4.18 us                                              | 3.50 us: 1.19x faster                                                |
| gc_traversal               | 6.42 ms                                              | 5.46 ms: 1.18x faster                                                |
| logging_simple             | 9.68 us                                              | 8.40 us: 1.15x faster                                                |
| xml_etree_generate         | 138 ms                                               | 120 ms: 1.15x faster                                                 |
| sqlglot_optimize           | 80.2 ms                                              | 70.4 ms: 1.14x faster                                                |
| generators                 | 44.7 ms                                              | 40.2 ms: 1.11x faster                                                |
| chaos                      | 92.1 ms                                              | 83.3 ms: 1.11x faster                                                |
| xml_etree_parse            | 244 ms                                               | 222 ms: 1.10x faster                                                 |
| pathlib                    | 31.6 ms                                              | 28.8 ms: 1.10x faster                                                |
| html5lib                   | 100 ms                                               | 91.1 ms: 1.10x faster                                                |
| scimark_lu                 | 155 ms                                               | 142 ms: 1.09x faster                                                 |
| python_startup_no_site     | 16.2 ms                                              | 14.9 ms: 1.09x faster                                                |
| logging_silent             | 139 ns                                               | 128 ns: 1.09x faster                                                 |
| scimark_monte_carlo        | 96.8 ms                                              | 89.4 ms: 1.08x faster                                                |
| xml_etree_process          | 82.7 ms                                              | 76.7 ms: 1.08x faster                                                |
| unpickle_pure_python       | 304 us                                               | 282 us: 1.08x faster                                                 |
| bpe_tokeniser              | 6.76 sec                                             | 6.28 sec: 1.08x faster                                               |
| sqlglot_parse              | 1.85 ms                                              | 1.73 ms: 1.07x faster                                                |
| scimark_sparse_mat_mult    | 6.94 ms                                              | 6.49 ms: 1.07x faster                                                |
| asyncio_tcp                | 988 ms                                               | 925 ms: 1.07x faster                                                 |
| nqueens                    | 116 ms                                               | 108 ms: 1.07x faster                                                 |
| unpickle                   | 21.6 us                                              | 20.4 us: 1.06x faster                                                |
| float                      | 124 ms                                               | 117 ms: 1.06x faster                                                 |
| pycparser                  | 1.68 sec                                             | 1.58 sec: 1.06x faster                                               |
| nbody                      | 117 ms                                               | 111 ms: 1.05x faster                                                 |
| python_startup             | 22.7 ms                                              | 21.6 ms: 1.05x faster                                                |
| regex_compile              | 186 ms                                               | 178 ms: 1.05x faster                                                 |
| pidigits                   | 256 ms                                               | 245 ms: 1.05x faster                                                 |
| async_generators           | 615 ms                                               | 588 ms: 1.04x faster                                                 |
| tomli_loads                | 2.86 sec                                             | 2.74 sec: 1.04x faster                                               |
| scimark_sor                | 170 ms                                               | 163 ms: 1.04x faster                                                 |
| meteor_contest             | 146 ms                                               | 140 ms: 1.04x faster                                                 |
| mdp                        | 3.77 sec                                             | 3.62 sec: 1.04x faster                                               |
| sympy_str                  | 379 ms                                               | 367 ms: 1.03x faster                                                 |
| pprint_pformat             | 1.99 sec                                             | 1.93 sec: 1.03x faster                                               |
| docutils                   | 4.05 sec                                             | 3.95 sec: 1.02x faster                                               |
| sympy_expand               | 591 ms                                               | 618 ms: 1.05x slower                                                 |
| regex_dna                  | 268 ms                                               | 283 ms: 1.06x slower                                                 |
| genshi_text                | 30.3 ms                                              | 32.3 ms: 1.07x slower                                                |
| create_gc_cycles           | 2.00 ms                                              | 2.14 ms: 1.07x slower                                                |
| unpack_sequence            | 70.8 ns                                              | 76.4 ns: 1.08x slower                                                |
| unpickle_list              | 6.83 us                                              | 7.43 us: 1.09x slower                                                |
| spectral_norm              | 136 ms                                               | 152 ms: 1.12x slower                                                 |
| json_dumps                 | 14.0 ms                                              | 15.7 ms: 1.12x slower                                                |
| go                         | 173 ms                                               | 195 ms: 1.13x slower                                                 |
| telco                      | 9.53 ms                                              | 10.8 ms: 1.13x slower                                                |
| coverage                   | 96.9 ms                                              | 111 ms: 1.14x slower                                                 |
| regex_v8                   | 29.9 ms                                              | 34.2 ms: 1.14x slower                                                |
| Geometric mean             | (ref)                                                | 1.06x faster                                                         |

Benchmark hidden because not significant (36): xml_etree_iterparse, richards, pickle_pure_python, sqlglot_transpile, 2to3, bench_thread_pool, typing_runtime_protocols, pickle, pylint, json, crypto_pyaes, genshi_xml, regex_effbot, logging_format, asyncio_tcp_ssl, pickle_dict, django_template, pprint_safe_repr, pickle_list, scimark_fft, mako, sqlglot_normalize, sqlite_synth, fannkuch, asyncio_websockets, pyflate, sympy_sum, coroutines, thrift, json_loads, deltablue, tornado_http, hexiom, richards_super, sympy_integrate, bench_mp_pool
Ignored benchmarks (9) of results/bm-20240814-3.12.5+-9f153a2/bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.01x