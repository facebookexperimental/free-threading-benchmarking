# Results vs. 3.12.6

- fork: colesbury
- ref: cheaper_steal
- machine: linux-x86_64
- commit hash: ed7085a
- commit date: 2024-11-18
- overall geometric mean: 1.52x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.36x slower
- Memory change: 1.24x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241118-vultr-x86_64-colesbury-cheaper_steal-3.14.0a1+-ed7085a |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 410 ms: 1.56x slower                                               |
| docutils       | 2.64 sec                                               | 3.34 sec: 1.27x slower                                             |
| html5lib       | 63.6 ms                                                | 102 ms: 1.61x slower                                               |
| Geometric mean | (ref)                                                  | 1.47x slower                                                       |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241118-vultr-x86_64-colesbury-cheaper_steal-3.14.0a1+-ed7085a |
|--------------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| asyncio_websockets | 517 ms                                                 | 523 ms: 1.01x slower                                               |
| asyncio_tcp        | 519 ms                                                 | 582 ms: 1.12x slower                                               |
| asyncio_tcp_ssl    | 1.51 sec                                               | 1.80 sec: 1.19x slower                                             |
| coroutines         | 23.9 ms                                                | 29.3 ms: 1.23x slower                                              |
| async_generators   | 384 ms                                                 | 485 ms: 1.26x slower                                               |
| Geometric mean     | (ref)                                                  | 1.16x slower                                                       |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241118-vultr-x86_64-colesbury-cheaper_steal-3.14.0a1+-ed7085a |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 186 ms: 1.01x slower                                               |
| float          | 80.8 ms                                                | 147 ms: 1.82x slower                                               |
| nbody          | 89.3 ms                                                | 192 ms: 2.15x slower                                               |
| Geometric mean | (ref)                                                  | 1.58x slower                                                       |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241118-vultr-x86_64-colesbury-cheaper_steal-3.14.0a1+-ed7085a |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.85 ms: 1.11x faster                                              |
| regex_dna      | 168 ms                                                 | 191 ms: 1.14x slower                                               |
| regex_v8       | 20.6 ms                                                | 25.3 ms: 1.23x slower                                              |
| regex_compile  | 142 ms                                                 | 226 ms: 1.59x slower                                               |
| Geometric mean | (ref)                                                  | 1.19x slower                                                       |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241118-vultr-x86_64-colesbury-cheaper_steal-3.14.0a1+-ed7085a |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 134 ms: 1.03x faster                                               |
| pickle_dict          | 31.8 us                                                | 32.7 us: 1.03x slower                                              |
| unpickle             | 14.1 us                                                | 14.7 us: 1.04x slower                                              |
| pickle_list          | 4.77 us                                                | 5.07 us: 1.06x slower                                              |
| json_loads           | 26.5 us                                                | 28.4 us: 1.07x slower                                              |
| unpickle_list        | 4.67 us                                                | 5.09 us: 1.09x slower                                              |
| pickle               | 10.9 us                                                | 12.2 us: 1.11x slower                                              |
| xml_etree_iterparse  | 96.7 ms                                                | 108 ms: 1.11x slower                                               |
| xml_etree_generate   | 85.2 ms                                                | 112 ms: 1.31x slower                                               |
| json_dumps           | 10.4 ms                                                | 15.1 ms: 1.46x slower                                              |
| tomli_loads          | 2.11 sec                                               | 3.14 sec: 1.49x slower                                             |
| xml_etree_process    | 59.0 ms                                                | 92.2 ms: 1.56x slower                                              |
| unpickle_pure_python | 221 us                                                 | 422 us: 1.91x slower                                               |
| pickle_pure_python   | 308 us                                                 | 620 us: 2.02x slower                                               |
| Geometric mean       | (ref)                                                  | 1.27x slower                                                       |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241118-vultr-x86_64-colesbury-cheaper_steal-3.14.0a1+-ed7085a |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.3 ms: 1.44x slower                                              |
| python_startup         | 9.93 ms                                                | 15.8 ms: 1.59x slower                                              |
| Geometric mean         | (ref)                                                  | 1.52x slower                                                       |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241118-vultr-x86_64-colesbury-cheaper_steal-3.14.0a1+-ed7085a |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 78.5 ms: 1.56x slower                                              |
| genshi_text     | 22.8 ms                                                | 38.9 ms: 1.71x slower                                              |
| django_template | 34.7 ms                                                | 63.2 ms: 1.82x slower                                              |
| mako            | 11.0 ms                                                | 21.4 ms: 1.95x slower                                              |
| Geometric mean  | (ref)                                                  | 1.75x slower                                                       |

All benchmarks:
===============

| Benchmark                | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241118-vultr-x86_64-colesbury-cheaper_steal-3.14.0a1+-ed7085a |
|--------------------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| gc_traversal             | 3.46 ms                                                | 2.71 ms: 1.28x faster                                              |
| regex_effbot             | 3.17 ms                                                | 2.85 ms: 1.11x faster                                              |
| xml_etree_parse          | 139 ms                                                 | 134 ms: 1.03x faster                                               |
| pidigits                 | 184 ms                                                 | 186 ms: 1.01x slower                                               |
| pathlib                  | 21.5 ms                                                | 21.7 ms: 1.01x slower                                              |
| asyncio_websockets       | 517 ms                                                 | 523 ms: 1.01x slower                                               |
| pickle_dict              | 31.8 us                                                | 32.7 us: 1.03x slower                                              |
| json                     | 5.02 ms                                                | 5.19 ms: 1.03x slower                                              |
| unpickle                 | 14.1 us                                                | 14.7 us: 1.04x slower                                              |
| pickle_list              | 4.77 us                                                | 5.07 us: 1.06x slower                                              |
| json_loads               | 26.5 us                                                | 28.4 us: 1.07x slower                                              |
| unpickle_list            | 4.67 us                                                | 5.09 us: 1.09x slower                                              |
| pickle                   | 10.9 us                                                | 12.2 us: 1.11x slower                                              |
| xml_etree_iterparse      | 96.7 ms                                                | 108 ms: 1.11x slower                                               |
| sqlite_synth             | 2.20 us                                                | 2.46 us: 1.12x slower                                              |
| create_gc_cycles         | 1.09 ms                                                | 1.22 ms: 1.12x slower                                              |
| asyncio_tcp              | 519 ms                                                 | 582 ms: 1.12x slower                                               |
| regex_dna                | 168 ms                                                 | 191 ms: 1.14x slower                                               |
| scimark_fft              | 342 ms                                                 | 404 ms: 1.18x slower                                               |
| asyncio_tcp_ssl          | 1.51 sec                                               | 1.80 sec: 1.19x slower                                             |
| deepcopy                 | 352 us                                                 | 425 us: 1.21x slower                                               |
| generators               | 32.2 ms                                                | 39.1 ms: 1.21x slower                                              |
| coroutines               | 23.9 ms                                                | 29.3 ms: 1.23x slower                                              |
| regex_v8                 | 20.6 ms                                                | 25.3 ms: 1.23x slower                                              |
| mdp                      | 2.42 sec                                               | 3.00 sec: 1.24x slower                                             |
| async_generators         | 384 ms                                                 | 485 ms: 1.26x slower                                               |
| docutils                 | 2.64 sec                                               | 3.34 sec: 1.27x slower                                             |
| bpe_tokeniser            | 4.74 sec                                               | 6.10 sec: 1.29x slower                                             |
| scimark_sparse_mat_mult  | 4.39 ms                                                | 5.72 ms: 1.30x slower                                              |
| pylint                   | 319 ms                                                 | 416 ms: 1.31x slower                                               |
| dulwich_log              | 78.9 ms                                                | 104 ms: 1.31x slower                                               |
| xml_etree_generate       | 85.2 ms                                                | 112 ms: 1.31x slower                                               |
| deepcopy_memo            | 40.3 us                                                | 53.4 us: 1.32x slower                                              |
| meteor_contest           | 104 ms                                                 | 137 ms: 1.33x slower                                               |
| crypto_pyaes             | 76.6 ms                                                | 107 ms: 1.40x slower                                               |
| nqueens                  | 80.1 ms                                                | 113 ms: 1.41x slower                                               |
| coverage                 | 71.4 ms                                                | 101 ms: 1.42x slower                                               |
| telco                    | 6.53 ms                                                | 9.39 ms: 1.44x slower                                              |
| python_startup_no_site   | 7.16 ms                                                | 10.3 ms: 1.44x slower                                              |
| pycparser                | 1.17 sec                                               | 1.69 sec: 1.45x slower                                             |
| deepcopy_reduce          | 3.08 us                                                | 4.47 us: 1.45x slower                                              |
| json_dumps               | 10.4 ms                                                | 15.1 ms: 1.46x slower                                              |
| spectral_norm            | 110 ms                                                 | 161 ms: 1.46x slower                                               |
| tomli_loads              | 2.11 sec                                               | 3.14 sec: 1.49x slower                                             |
| fannkuch                 | 372 ms                                                 | 560 ms: 1.50x slower                                               |
| comprehensions           | 19.8 us                                                | 30.3 us: 1.53x slower                                              |
| typing_runtime_protocols | 163 us                                                 | 251 us: 1.53x slower                                               |
| 2to3                     | 264 ms                                                 | 410 ms: 1.56x slower                                               |
| xml_etree_process        | 59.0 ms                                                | 92.2 ms: 1.56x slower                                              |
| genshi_xml               | 50.2 ms                                                | 78.5 ms: 1.56x slower                                              |
| regex_compile            | 142 ms                                                 | 226 ms: 1.59x slower                                               |
| thrift                   | 791 us                                                 | 1.26 ms: 1.59x slower                                              |
| python_startup           | 9.93 ms                                                | 15.8 ms: 1.59x slower                                              |
| sympy_integrate          | 20.5 ms                                                | 32.9 ms: 1.60x slower                                              |
| html5lib                 | 63.6 ms                                                | 102 ms: 1.61x slower                                               |
| sqlglot_normalize        | 107 ms                                                 | 179 ms: 1.68x slower                                               |
| sqlglot_optimize         | 53.3 ms                                                | 89.5 ms: 1.68x slower                                              |
| pyflate                  | 448 ms                                                 | 761 ms: 1.70x slower                                               |
| genshi_text              | 22.8 ms                                                | 38.9 ms: 1.71x slower                                              |
| pprint_safe_repr         | 743 ms                                                 | 1.32 sec: 1.77x slower                                             |
| logging_format           | 7.35 us                                                | 13.2 us: 1.79x slower                                              |
| pprint_pformat           | 1.52 sec                                               | 2.72 sec: 1.79x slower                                             |
| logging_simple           | 6.63 us                                                | 11.9 us: 1.79x slower                                              |
| django_template          | 34.7 ms                                                | 63.2 ms: 1.82x slower                                              |
| float                    | 80.8 ms                                                | 147 ms: 1.82x slower                                               |
| scimark_monte_carlo      | 68.4 ms                                                | 125 ms: 1.82x slower                                               |
| sympy_str                | 292 ms                                                 | 537 ms: 1.84x slower                                               |
| logging_silent           | 109 ns                                                 | 206 ns: 1.90x slower                                               |
| chaos                    | 62.8 ms                                                | 120 ms: 1.91x slower                                               |
| unpickle_pure_python     | 221 us                                                 | 422 us: 1.91x slower                                               |
| richards                 | 45.9 ms                                                | 88.6 ms: 1.93x slower                                              |
| mako                     | 11.0 ms                                                | 21.4 ms: 1.95x slower                                              |
| sqlglot_transpile        | 1.67 ms                                                | 3.29 ms: 1.97x slower                                              |
| hexiom                   | 6.17 ms                                                | 12.2 ms: 1.98x slower                                              |
| pickle_pure_python       | 308 us                                                 | 620 us: 2.02x slower                                               |
| scimark_sor              | 130 ms                                                 | 263 ms: 2.03x slower                                               |
| richards_super           | 51.9 ms                                                | 107 ms: 2.05x slower                                               |
| sqlglot_parse            | 1.36 ms                                                | 2.80 ms: 2.07x slower                                              |
| raytrace                 | 299 ms                                                 | 624 ms: 2.09x slower                                               |
| go                       | 139 ms                                                 | 296 ms: 2.12x slower                                               |
| scimark_lu               | 114 ms                                                 | 243 ms: 2.13x slower                                               |
| nbody                    | 89.3 ms                                                | 192 ms: 2.15x slower                                               |
| sympy_expand             | 468 ms                                                 | 1.05 sec: 2.25x slower                                             |
| sympy_sum                | 166 ms                                                 | 379 ms: 2.29x slower                                               |
| deltablue                | 3.45 ms                                                | 9.11 ms: 2.64x slower                                              |
| unpack_sequence          | 52.1 ns                                                | 145 ns: 2.78x slower                                               |
| bench_thread_pool        | 941 us                                                 | 3.48 ms: 3.69x slower                                              |
| bench_mp_pool            | 10.8 ms                                                | 69.7 ms: 6.45x slower                                              |
| Geometric mean           | (ref)                                                  | 1.52x slower                                                       |
Ignored benchmarks (17) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.44x
- 95% likely to have a slowdown of 1.42x
- 99% likely to have a slowdown of 1.36x

# Memory
- memory change: 1.24x