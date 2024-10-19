# Results vs. 3.12.6

- fork: colesbury
- ref: gh_125610_STORE_ATTR
- machine: linux-x86_64
- commit hash: 3a126a8
- commit date: 2024-10-16
- overall geometric mean: 1.00x faster
- HPT reliability: 99.29%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241016-vultr-x86_64-colesbury-gh_125610_STORE_ATTR-3.14.0a1+-3a126a8 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 253 ms: 1.04x faster                                                      |
| docutils       | 2.64 sec                                               | 2.60 sec: 1.02x faster                                                    |
| tornado_http   | 119 ms                                                 | 113 ms: 1.05x faster                                                      |
| Geometric mean | (ref)                                                  | 1.03x faster                                                              |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241016-vultr-x86_64-colesbury-gh_125610_STORE_ATTR-3.14.0a1+-3a126a8 |
|--------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| coroutines         | 23.9 ms                                                | 22.1 ms: 1.08x faster                                                     |
| async_generators   | 384 ms                                                 | 371 ms: 1.04x faster                                                      |
| asyncio_tcp        | 519 ms                                                 | 503 ms: 1.03x faster                                                      |
| asyncio_websockets | 517 ms                                                 | 520 ms: 1.01x slower                                                      |
| asyncio_tcp_ssl    | 1.51 sec                                               | 1.52 sec: 1.01x slower                                                    |
| Geometric mean     | (ref)                                                  | 1.03x faster                                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241016-vultr-x86_64-colesbury-gh_125610_STORE_ATTR-3.14.0a1+-3a126a8 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 78.9 ms: 1.02x faster                                                     |
| pidigits       | 184 ms                                                 | 185 ms: 1.00x slower                                                      |
| nbody          | 89.3 ms                                                | 94.7 ms: 1.06x slower                                                     |
| Geometric mean | (ref)                                                  | 1.01x slower                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241016-vultr-x86_64-colesbury-gh_125610_STORE_ATTR-3.14.0a1+-3a126a8 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 130 ms: 1.10x faster                                                      |
| regex_effbot   | 3.17 ms                                                | 3.19 ms: 1.01x slower                                                     |
| regex_dna      | 168 ms                                                 | 183 ms: 1.09x slower                                                      |
| regex_v8       | 20.6 ms                                                | 24.2 ms: 1.17x slower                                                     |
| Geometric mean | (ref)                                                  | 1.04x slower                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241016-vultr-x86_64-colesbury-gh_125610_STORE_ATTR-3.14.0a1+-3a126a8 |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| unpickle             | 14.1 us                                                | 13.2 us: 1.06x faster                                                     |
| unpickle_pure_python | 221 us                                                 | 215 us: 1.03x faster                                                      |
| json_loads           | 26.5 us                                                | 25.9 us: 1.02x faster                                                     |
| xml_etree_parse      | 139 ms                                                 | 136 ms: 1.02x faster                                                      |
| unpickle_list        | 4.67 us                                                | 4.61 us: 1.01x faster                                                     |
| tomli_loads          | 2.11 sec                                               | 2.09 sec: 1.01x faster                                                    |
| xml_etree_iterparse  | 96.7 ms                                                | 96.1 ms: 1.01x faster                                                     |
| xml_etree_generate   | 85.2 ms                                                | 84.9 ms: 1.00x faster                                                     |
| xml_etree_process    | 59.0 ms                                                | 59.3 ms: 1.01x slower                                                     |
| pickle_dict          | 31.8 us                                                | 33.0 us: 1.04x slower                                                     |
| pickle               | 10.9 us                                                | 11.4 us: 1.04x slower                                                     |
| pickle_list          | 4.77 us                                                | 5.10 us: 1.07x slower                                                     |
| json_dumps           | 10.4 ms                                                | 11.7 ms: 1.13x slower                                                     |
| Geometric mean       | (ref)                                                  | 1.01x slower                                                              |

Benchmark hidden because not significant (1): pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241016-vultr-x86_64-colesbury-gh_125610_STORE_ATTR-3.14.0a1+-3a126a8 |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.40 ms: 1.03x slower                                                     |
| python_startup         | 9.93 ms                                                | 11.0 ms: 1.11x slower                                                     |
| Geometric mean         | (ref)                                                  | 1.07x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241016-vultr-x86_64-colesbury-gh_125610_STORE_ATTR-3.14.0a1+-3a126a8 |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 22.2 ms: 1.03x faster                                                     |
| django_template | 34.7 ms                                                | 35.2 ms: 1.01x slower                                                     |
| mako            | 11.0 ms                                                | 11.8 ms: 1.07x slower                                                     |
| Geometric mean  | (ref)                                                  | 1.01x slower                                                              |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241016-vultr-x86_64-colesbury-gh_125610_STORE_ATTR-3.14.0a1+-3a126a8 |
|--------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| deepcopy                 | 352 us                                                 | 260 us: 1.35x faster                                                      |
| deepcopy_memo            | 40.3 us                                                | 30.4 us: 1.33x faster                                                     |
| unpack_sequence          | 52.1 ns                                                | 42.1 ns: 1.24x faster                                                     |
| go                       | 139 ms                                                 | 118 ms: 1.18x faster                                                      |
| deepcopy_reduce          | 3.08 us                                                | 2.62 us: 1.17x faster                                                     |
| comprehensions           | 19.8 us                                                | 17.0 us: 1.16x faster                                                     |
| raytrace                 | 299 ms                                                 | 260 ms: 1.15x faster                                                      |
| pathlib                  | 21.5 ms                                                | 18.7 ms: 1.15x faster                                                     |
| generators               | 32.2 ms                                                | 28.4 ms: 1.14x faster                                                     |
| crypto_pyaes             | 76.6 ms                                                | 67.7 ms: 1.13x faster                                                     |
| regex_compile            | 142 ms                                                 | 130 ms: 1.10x faster                                                      |
| logging_simple           | 6.63 us                                                | 6.07 us: 1.09x faster                                                     |
| logging_format           | 7.35 us                                                | 6.75 us: 1.09x faster                                                     |
| bpe_tokeniser            | 4.74 sec                                               | 4.35 sec: 1.09x faster                                                    |
| coroutines               | 23.9 ms                                                | 22.1 ms: 1.08x faster                                                     |
| sympy_sum                | 166 ms                                                 | 154 ms: 1.08x faster                                                      |
| deltablue                | 3.45 ms                                                | 3.21 ms: 1.07x faster                                                     |
| sympy_str                | 292 ms                                                 | 272 ms: 1.07x faster                                                      |
| chaos                    | 62.8 ms                                                | 59.2 ms: 1.06x faster                                                     |
| unpickle                 | 14.1 us                                                | 13.2 us: 1.06x faster                                                     |
| gc_traversal             | 3.46 ms                                                | 3.26 ms: 1.06x faster                                                     |
| logging_silent           | 109 ns                                                 | 103 ns: 1.06x faster                                                      |
| thrift                   | 791 us                                                 | 750 us: 1.06x faster                                                      |
| dulwich_log              | 78.9 ms                                                | 74.8 ms: 1.05x faster                                                     |
| sqlglot_parse            | 1.36 ms                                                | 1.29 ms: 1.05x faster                                                     |
| sqlglot_transpile        | 1.67 ms                                                | 1.59 ms: 1.05x faster                                                     |
| tornado_http             | 119 ms                                                 | 113 ms: 1.05x faster                                                      |
| hexiom                   | 6.17 ms                                                | 5.91 ms: 1.04x faster                                                     |
| typing_runtime_protocols | 163 us                                                 | 157 us: 1.04x faster                                                      |
| 2to3                     | 264 ms                                                 | 253 ms: 1.04x faster                                                      |
| pprint_safe_repr         | 743 ms                                                 | 716 ms: 1.04x faster                                                      |
| async_generators         | 384 ms                                                 | 371 ms: 1.04x faster                                                      |
| scimark_monte_carlo      | 68.4 ms                                                | 66.3 ms: 1.03x faster                                                     |
| json                     | 5.02 ms                                                | 4.87 ms: 1.03x faster                                                     |
| asyncio_tcp              | 519 ms                                                 | 503 ms: 1.03x faster                                                      |
| pprint_pformat           | 1.52 sec                                               | 1.48 sec: 1.03x faster                                                    |
| sympy_integrate          | 20.5 ms                                                | 20.0 ms: 1.03x faster                                                     |
| unpickle_pure_python     | 221 us                                                 | 215 us: 1.03x faster                                                      |
| genshi_text              | 22.8 ms                                                | 22.2 ms: 1.03x faster                                                     |
| mdp                      | 2.42 sec                                               | 2.36 sec: 1.03x faster                                                    |
| json_loads               | 26.5 us                                                | 25.9 us: 1.02x faster                                                     |
| float                    | 80.8 ms                                                | 78.9 ms: 1.02x faster                                                     |
| richards                 | 45.9 ms                                                | 44.9 ms: 1.02x faster                                                     |
| richards_super           | 51.9 ms                                                | 50.8 ms: 1.02x faster                                                     |
| xml_etree_parse          | 139 ms                                                 | 136 ms: 1.02x faster                                                      |
| meteor_contest           | 104 ms                                                 | 102 ms: 1.02x faster                                                      |
| docutils                 | 2.64 sec                                               | 2.60 sec: 1.02x faster                                                    |
| nqueens                  | 80.1 ms                                                | 78.9 ms: 1.02x faster                                                     |
| sympy_expand             | 468 ms                                                 | 461 ms: 1.01x faster                                                      |
| unpickle_list            | 4.67 us                                                | 4.61 us: 1.01x faster                                                     |
| tomli_loads              | 2.11 sec                                               | 2.09 sec: 1.01x faster                                                    |
| spectral_norm            | 110 ms                                                 | 109 ms: 1.01x faster                                                      |
| xml_etree_iterparse      | 96.7 ms                                                | 96.1 ms: 1.01x faster                                                     |
| xml_etree_generate       | 85.2 ms                                                | 84.9 ms: 1.00x faster                                                     |
| sqlglot_optimize         | 53.3 ms                                                | 53.4 ms: 1.00x slower                                                     |
| pidigits                 | 184 ms                                                 | 185 ms: 1.00x slower                                                      |
| xml_etree_process        | 59.0 ms                                                | 59.3 ms: 1.01x slower                                                     |
| asyncio_websockets       | 517 ms                                                 | 520 ms: 1.01x slower                                                      |
| regex_effbot             | 3.17 ms                                                | 3.19 ms: 1.01x slower                                                     |
| asyncio_tcp_ssl          | 1.51 sec                                               | 1.52 sec: 1.01x slower                                                    |
| scimark_fft              | 342 ms                                                 | 345 ms: 1.01x slower                                                      |
| scimark_lu               | 114 ms                                                 | 115 ms: 1.01x slower                                                      |
| django_template          | 34.7 ms                                                | 35.2 ms: 1.01x slower                                                     |
| sqlite_synth             | 2.20 us                                                | 2.23 us: 1.02x slower                                                     |
| pyflate                  | 448 ms                                                 | 457 ms: 1.02x slower                                                      |
| python_startup_no_site   | 7.16 ms                                                | 7.40 ms: 1.03x slower                                                     |
| scimark_sor              | 130 ms                                                 | 135 ms: 1.04x slower                                                      |
| pycparser                | 1.17 sec                                               | 1.21 sec: 1.04x slower                                                    |
| pickle_dict              | 31.8 us                                                | 33.0 us: 1.04x slower                                                     |
| fannkuch                 | 372 ms                                                 | 387 ms: 1.04x slower                                                      |
| pickle                   | 10.9 us                                                | 11.4 us: 1.04x slower                                                     |
| nbody                    | 89.3 ms                                                | 94.7 ms: 1.06x slower                                                     |
| scimark_sparse_mat_mult  | 4.39 ms                                                | 4.70 ms: 1.07x slower                                                     |
| pickle_list              | 4.77 us                                                | 5.10 us: 1.07x slower                                                     |
| mako                     | 11.0 ms                                                | 11.8 ms: 1.07x slower                                                     |
| bench_thread_pool        | 941 us                                                 | 1.01 ms: 1.08x slower                                                     |
| regex_dna                | 168 ms                                                 | 183 ms: 1.09x slower                                                      |
| python_startup           | 9.93 ms                                                | 11.0 ms: 1.11x slower                                                     |
| json_dumps               | 10.4 ms                                                | 11.7 ms: 1.13x slower                                                     |
| coverage                 | 71.4 ms                                                | 81.1 ms: 1.14x slower                                                     |
| telco                    | 6.53 ms                                                | 7.45 ms: 1.14x slower                                                     |
| regex_v8                 | 20.6 ms                                                | 24.2 ms: 1.17x slower                                                     |
| create_gc_cycles         | 1.09 ms                                                | 1.35 ms: 1.24x slower                                                     |
| bench_mp_pool            | 10.8 ms                                                | 63.2 ms: 5.86x slower                                                     |
| Geometric mean           | (ref)                                                  | 1.00x faster                                                              |

Benchmark hidden because not significant (5): pylint, pickle_pure_python, genshi_xml, sqlglot_normalize, html5lib
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 99.29% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.02x