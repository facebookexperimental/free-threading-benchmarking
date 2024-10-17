# Results vs. 3.12.6

- fork: colesbury
- ref: gh_125610_STORE_ATTR
- machine: linux-x86_64
- commit hash: 3a126a8
- commit date: 2024-10-16
- overall geometric mean: 1.01x slower
- HPT reliability: 96.64%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241016-vultr-x86_64-colesbury-gh_125610_STORE_ATTR-3.14.0a1+-3a126a8 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 255 ms: 1.03x faster                                                      |
| docutils       | 2.64 sec                                               | 2.61 sec: 1.01x faster                                                    |
| tornado_http   | 119 ms                                                 | 114 ms: 1.04x faster                                                      |
| Geometric mean | (ref)                                                  | 1.02x faster                                                              |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241016-vultr-x86_64-colesbury-gh_125610_STORE_ATTR-3.14.0a1+-3a126a8 |
|--------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| coroutines         | 23.9 ms                                                | 22.3 ms: 1.07x faster                                                     |
| asyncio_tcp        | 519 ms                                                 | 501 ms: 1.04x faster                                                      |
| async_generators   | 384 ms                                                 | 371 ms: 1.04x faster                                                      |
| asyncio_websockets | 517 ms                                                 | 520 ms: 1.01x slower                                                      |
| asyncio_tcp_ssl    | 1.51 sec                                               | 1.52 sec: 1.01x slower                                                    |
| Geometric mean     | (ref)                                                  | 1.03x faster                                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241016-vultr-x86_64-colesbury-gh_125610_STORE_ATTR-3.14.0a1+-3a126a8 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 79.8 ms: 1.01x faster                                                     |
| pidigits       | 184 ms                                                 | 186 ms: 1.01x slower                                                      |
| nbody          | 89.3 ms                                                | 93.8 ms: 1.05x slower                                                     |
| Geometric mean | (ref)                                                  | 1.02x slower                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241016-vultr-x86_64-colesbury-gh_125610_STORE_ATTR-3.14.0a1+-3a126a8 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 129 ms: 1.10x faster                                                      |
| regex_effbot   | 3.17 ms                                                | 3.01 ms: 1.05x faster                                                     |
| regex_dna      | 168 ms                                                 | 179 ms: 1.07x slower                                                      |
| regex_v8       | 20.6 ms                                                | 24.5 ms: 1.19x slower                                                     |
| Geometric mean | (ref)                                                  | 1.02x slower                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241016-vultr-x86_64-colesbury-gh_125610_STORE_ATTR-3.14.0a1+-3a126a8 |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| unpickle             | 14.1 us                                                | 13.8 us: 1.02x faster                                                     |
| json_loads           | 26.5 us                                                | 26.2 us: 1.01x faster                                                     |
| unpickle_pure_python | 221 us                                                 | 218 us: 1.01x faster                                                      |
| pickle_pure_python   | 308 us                                                 | 307 us: 1.00x faster                                                      |
| xml_etree_generate   | 85.2 ms                                                | 85.0 ms: 1.00x faster                                                     |
| xml_etree_process    | 59.0 ms                                                | 59.4 ms: 1.01x slower                                                     |
| unpickle_list        | 4.67 us                                                | 4.89 us: 1.05x slower                                                     |
| pickle               | 10.9 us                                                | 11.5 us: 1.05x slower                                                     |
| pickle_list          | 4.77 us                                                | 5.03 us: 1.05x slower                                                     |
| pickle_dict          | 31.8 us                                                | 34.0 us: 1.07x slower                                                     |
| json_dumps           | 10.4 ms                                                | 11.6 ms: 1.12x slower                                                     |
| Geometric mean       | (ref)                                                  | 1.02x slower                                                              |

Benchmark hidden because not significant (3): xml_etree_parse, tomli_loads, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241016-vultr-x86_64-colesbury-gh_125610_STORE_ATTR-3.14.0a1+-3a126a8 |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.47 ms: 1.04x slower                                                     |
| python_startup         | 9.93 ms                                                | 11.1 ms: 1.12x slower                                                     |
| Geometric mean         | (ref)                                                  | 1.08x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241016-vultr-x86_64-colesbury-gh_125610_STORE_ATTR-3.14.0a1+-3a126a8 |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 22.3 ms: 1.02x faster                                                     |
| django_template | 34.7 ms                                                | 35.4 ms: 1.02x slower                                                     |
| mako            | 11.0 ms                                                | 11.7 ms: 1.06x slower                                                     |
| Geometric mean  | (ref)                                                  | 1.01x slower                                                              |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241016-vultr-x86_64-colesbury-gh_125610_STORE_ATTR-3.14.0a1+-3a126a8 |
|--------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| deepcopy_memo            | 40.3 us                                                | 30.0 us: 1.34x faster                                                     |
| deepcopy                 | 352 us                                                 | 263 us: 1.34x faster                                                      |
| pathlib                  | 21.5 ms                                                | 18.6 ms: 1.16x faster                                                     |
| deepcopy_reduce          | 3.08 us                                                | 2.66 us: 1.16x faster                                                     |
| comprehensions           | 19.8 us                                                | 17.2 us: 1.15x faster                                                     |
| go                       | 139 ms                                                 | 122 ms: 1.14x faster                                                      |
| raytrace                 | 299 ms                                                 | 266 ms: 1.12x faster                                                      |
| generators               | 32.2 ms                                                | 29.0 ms: 1.11x faster                                                     |
| crypto_pyaes             | 76.6 ms                                                | 69.1 ms: 1.11x faster                                                     |
| regex_compile            | 142 ms                                                 | 129 ms: 1.10x faster                                                      |
| logging_simple           | 6.63 us                                                | 6.10 us: 1.09x faster                                                     |
| bpe_tokeniser            | 4.74 sec                                               | 4.41 sec: 1.07x faster                                                    |
| logging_format           | 7.35 us                                                | 6.84 us: 1.07x faster                                                     |
| coroutines               | 23.9 ms                                                | 22.3 ms: 1.07x faster                                                     |
| sympy_sum                | 166 ms                                                 | 155 ms: 1.07x faster                                                      |
| sympy_str                | 292 ms                                                 | 274 ms: 1.06x faster                                                      |
| chaos                    | 62.8 ms                                                | 59.6 ms: 1.05x faster                                                     |
| regex_effbot             | 3.17 ms                                                | 3.01 ms: 1.05x faster                                                     |
| dulwich_log              | 78.9 ms                                                | 75.0 ms: 1.05x faster                                                     |
| sqlglot_parse            | 1.36 ms                                                | 1.29 ms: 1.05x faster                                                     |
| deltablue                | 3.45 ms                                                | 3.28 ms: 1.05x faster                                                     |
| gc_traversal             | 3.46 ms                                                | 3.30 ms: 1.05x faster                                                     |
| sqlglot_transpile        | 1.67 ms                                                | 1.59 ms: 1.05x faster                                                     |
| typing_runtime_protocols | 163 us                                                 | 156 us: 1.05x faster                                                      |
| pprint_safe_repr         | 743 ms                                                 | 712 ms: 1.04x faster                                                      |
| tornado_http             | 119 ms                                                 | 114 ms: 1.04x faster                                                      |
| thrift                   | 791 us                                                 | 762 us: 1.04x faster                                                      |
| asyncio_tcp              | 519 ms                                                 | 501 ms: 1.04x faster                                                      |
| async_generators         | 384 ms                                                 | 371 ms: 1.04x faster                                                      |
| pprint_pformat           | 1.52 sec                                               | 1.47 sec: 1.03x faster                                                    |
| 2to3                     | 264 ms                                                 | 255 ms: 1.03x faster                                                      |
| scimark_monte_carlo      | 68.4 ms                                                | 66.5 ms: 1.03x faster                                                     |
| logging_silent           | 109 ns                                                 | 106 ns: 1.03x faster                                                      |
| mdp                      | 2.42 sec                                               | 2.36 sec: 1.03x faster                                                    |
| sympy_integrate          | 20.5 ms                                                | 20.1 ms: 1.02x faster                                                     |
| genshi_text              | 22.8 ms                                                | 22.3 ms: 1.02x faster                                                     |
| unpickle                 | 14.1 us                                                | 13.8 us: 1.02x faster                                                     |
| unpack_sequence          | 52.1 ns                                                | 51.0 ns: 1.02x faster                                                     |
| hexiom                   | 6.17 ms                                                | 6.05 ms: 1.02x faster                                                     |
| nqueens                  | 80.1 ms                                                | 78.6 ms: 1.02x faster                                                     |
| json                     | 5.02 ms                                                | 4.93 ms: 1.02x faster                                                     |
| sympy_expand             | 468 ms                                                 | 460 ms: 1.02x faster                                                      |
| scimark_lu               | 114 ms                                                 | 113 ms: 1.01x faster                                                      |
| float                    | 80.8 ms                                                | 79.8 ms: 1.01x faster                                                     |
| json_loads               | 26.5 us                                                | 26.2 us: 1.01x faster                                                     |
| unpickle_pure_python     | 221 us                                                 | 218 us: 1.01x faster                                                      |
| docutils                 | 2.64 sec                                               | 2.61 sec: 1.01x faster                                                    |
| sqlglot_normalize        | 107 ms                                                 | 106 ms: 1.01x faster                                                      |
| pickle_pure_python       | 308 us                                                 | 307 us: 1.00x faster                                                      |
| xml_etree_generate       | 85.2 ms                                                | 85.0 ms: 1.00x faster                                                     |
| meteor_contest           | 104 ms                                                 | 104 ms: 1.00x slower                                                      |
| sqlglot_optimize         | 53.3 ms                                                | 53.5 ms: 1.01x slower                                                     |
| asyncio_websockets       | 517 ms                                                 | 520 ms: 1.01x slower                                                      |
| xml_etree_process        | 59.0 ms                                                | 59.4 ms: 1.01x slower                                                     |
| asyncio_tcp_ssl          | 1.51 sec                                               | 1.52 sec: 1.01x slower                                                    |
| fannkuch                 | 372 ms                                                 | 376 ms: 1.01x slower                                                      |
| pidigits                 | 184 ms                                                 | 186 ms: 1.01x slower                                                      |
| richards_super           | 51.9 ms                                                | 52.4 ms: 1.01x slower                                                     |
| scimark_fft              | 342 ms                                                 | 346 ms: 1.01x slower                                                      |
| richards                 | 45.9 ms                                                | 46.7 ms: 1.02x slower                                                     |
| django_template          | 34.7 ms                                                | 35.4 ms: 1.02x slower                                                     |
| pyflate                  | 448 ms                                                 | 458 ms: 1.02x slower                                                      |
| spectral_norm            | 110 ms                                                 | 113 ms: 1.03x slower                                                      |
| pycparser                | 1.17 sec                                               | 1.21 sec: 1.04x slower                                                    |
| python_startup_no_site   | 7.16 ms                                                | 7.47 ms: 1.04x slower                                                     |
| unpickle_list            | 4.67 us                                                | 4.89 us: 1.05x slower                                                     |
| nbody                    | 89.3 ms                                                | 93.8 ms: 1.05x slower                                                     |
| scimark_sparse_mat_mult  | 4.39 ms                                                | 4.62 ms: 1.05x slower                                                     |
| scimark_sor              | 130 ms                                                 | 137 ms: 1.05x slower                                                      |
| pickle                   | 10.9 us                                                | 11.5 us: 1.05x slower                                                     |
| pickle_list              | 4.77 us                                                | 5.03 us: 1.05x slower                                                     |
| mako                     | 11.0 ms                                                | 11.7 ms: 1.06x slower                                                     |
| regex_dna                | 168 ms                                                 | 179 ms: 1.07x slower                                                      |
| pickle_dict              | 31.8 us                                                | 34.0 us: 1.07x slower                                                     |
| bench_thread_pool        | 941 us                                                 | 1.01 ms: 1.08x slower                                                     |
| python_startup           | 9.93 ms                                                | 11.1 ms: 1.12x slower                                                     |
| json_dumps               | 10.4 ms                                                | 11.6 ms: 1.12x slower                                                     |
| coverage                 | 71.4 ms                                                | 81.1 ms: 1.14x slower                                                     |
| telco                    | 6.53 ms                                                | 7.43 ms: 1.14x slower                                                     |
| regex_v8                 | 20.6 ms                                                | 24.5 ms: 1.19x slower                                                     |
| create_gc_cycles         | 1.09 ms                                                | 1.38 ms: 1.26x slower                                                     |
| bench_mp_pool            | 10.8 ms                                                | 64.0 ms: 5.92x slower                                                     |
| Geometric mean           | (ref)                                                  | 1.01x slower                                                              |

Benchmark hidden because not significant (7): html5lib, xml_etree_parse, tomli_loads, xml_etree_iterparse, sqlite_synth, genshi_xml, pylint
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 96.64% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.02x