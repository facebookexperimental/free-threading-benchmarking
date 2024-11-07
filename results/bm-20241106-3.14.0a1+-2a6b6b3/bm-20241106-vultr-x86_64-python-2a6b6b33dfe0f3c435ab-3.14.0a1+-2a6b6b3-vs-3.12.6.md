# Results vs. 3.12.6

- fork: python
- ref: 2a6b6b33dfe0f3c435ab
- machine: linux-x86_64
- commit hash: 2a6b6b3
- commit date: 2024-11-06
- overall geometric mean: 1.01x slower
- HPT reliability: 91.58%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241106-vultr-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 254 ms: 1.04x faster                                                   |
| docutils       | 2.64 sec                                               | 2.61 sec: 1.01x faster                                                 |
| html5lib       | 63.6 ms                                                | 66.5 ms: 1.04x slower                                                  |
| Geometric mean | (ref)                                                  | 1.00x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241106-vultr-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3 |
|--------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_generators   | 384 ms                                                 | 373 ms: 1.03x faster                                                   |
| asyncio_tcp        | 519 ms                                                 | 506 ms: 1.02x faster                                                   |
| coroutines         | 23.9 ms                                                | 23.6 ms: 1.02x faster                                                  |
| asyncio_websockets | 517 ms                                                 | 520 ms: 1.01x slower                                                   |
| asyncio_tcp_ssl    | 1.51 sec                                               | 1.52 sec: 1.01x slower                                                 |
| Geometric mean     | (ref)                                                  | 1.01x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241106-vultr-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 79.7 ms: 1.01x faster                                                  |
| nbody          | 89.3 ms                                                | 95.6 ms: 1.07x slower                                                  |
| pidigits       | 184 ms                                                 | 222 ms: 1.21x slower                                                   |
| Geometric mean | (ref)                                                  | 1.08x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241106-vultr-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 132 ms: 1.08x faster                                                   |
| regex_effbot   | 3.17 ms                                                | 3.18 ms: 1.00x slower                                                  |
| regex_dna      | 168 ms                                                 | 184 ms: 1.10x slower                                                   |
| regex_v8       | 20.6 ms                                                | 24.6 ms: 1.19x slower                                                  |
| Geometric mean | (ref)                                                  | 1.05x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241106-vultr-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| unpickle             | 14.1 us                                                | 13.3 us: 1.06x faster                                                  |
| json_loads           | 26.5 us                                                | 25.7 us: 1.03x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 135 ms: 1.02x faster                                                   |
| unpickle_pure_python | 221 us                                                 | 217 us: 1.02x faster                                                   |
| xml_etree_iterparse  | 96.7 ms                                                | 95.9 ms: 1.01x faster                                                  |
| xml_etree_generate   | 85.2 ms                                                | 85.4 ms: 1.00x slower                                                  |
| xml_etree_process    | 59.0 ms                                                | 59.5 ms: 1.01x slower                                                  |
| pickle_list          | 4.77 us                                                | 4.90 us: 1.03x slower                                                  |
| pickle               | 10.9 us                                                | 11.3 us: 1.03x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 317 us: 1.03x slower                                                   |
| pickle_dict          | 31.8 us                                                | 32.8 us: 1.03x slower                                                  |
| json_dumps           | 10.4 ms                                                | 11.6 ms: 1.12x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.01x slower                                                           |

Benchmark hidden because not significant (2): tomli_loads, unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241106-vultr-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.41 ms: 1.03x slower                                                  |
| python_startup         | 9.93 ms                                                | 11.0 ms: 1.11x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.07x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241106-vultr-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 22.6 ms: 1.01x faster                                                  |
| django_template | 34.7 ms                                                | 35.2 ms: 1.01x slower                                                  |
| genshi_xml      | 50.2 ms                                                | 50.9 ms: 1.02x slower                                                  |
| mako            | 11.0 ms                                                | 12.0 ms: 1.09x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.03x slower                                                           |

All benchmarks:
===============

| Benchmark                | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241106-vultr-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3 |
|--------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| deepcopy_memo            | 40.3 us                                                | 30.0 us: 1.34x faster                                                  |
| deepcopy                 | 352 us                                                 | 265 us: 1.33x faster                                                   |
| pathlib                  | 21.5 ms                                                | 18.1 ms: 1.19x faster                                                  |
| comprehensions           | 19.8 us                                                | 17.2 us: 1.15x faster                                                  |
| go                       | 139 ms                                                 | 122 ms: 1.14x faster                                                   |
| deepcopy_reduce          | 3.08 us                                                | 2.72 us: 1.13x faster                                                  |
| crypto_pyaes             | 76.6 ms                                                | 67.8 ms: 1.13x faster                                                  |
| raytrace                 | 299 ms                                                 | 266 ms: 1.13x faster                                                   |
| generators               | 32.2 ms                                                | 28.8 ms: 1.12x faster                                                  |
| bpe_tokeniser            | 4.74 sec                                               | 4.35 sec: 1.09x faster                                                 |
| sympy_sum                | 166 ms                                                 | 153 ms: 1.09x faster                                                   |
| regex_compile            | 142 ms                                                 | 132 ms: 1.08x faster                                                   |
| gc_traversal             | 3.46 ms                                                | 3.24 ms: 1.07x faster                                                  |
| logging_simple           | 6.63 us                                                | 6.22 us: 1.07x faster                                                  |
| logging_format           | 7.35 us                                                | 6.91 us: 1.06x faster                                                  |
| sympy_str                | 292 ms                                                 | 274 ms: 1.06x faster                                                   |
| unpickle                 | 14.1 us                                                | 13.3 us: 1.06x faster                                                  |
| chaos                    | 62.8 ms                                                | 59.3 ms: 1.06x faster                                                  |
| thrift                   | 791 us                                                 | 750 us: 1.06x faster                                                   |
| deltablue                | 3.45 ms                                                | 3.28 ms: 1.05x faster                                                  |
| scimark_monte_carlo      | 68.4 ms                                                | 65.4 ms: 1.05x faster                                                  |
| dulwich_log              | 78.9 ms                                                | 75.8 ms: 1.04x faster                                                  |
| sqlglot_transpile        | 1.67 ms                                                | 1.61 ms: 1.04x faster                                                  |
| 2to3                     | 264 ms                                                 | 254 ms: 1.04x faster                                                   |
| pprint_safe_repr         | 743 ms                                                 | 717 ms: 1.04x faster                                                   |
| sqlglot_parse            | 1.36 ms                                                | 1.31 ms: 1.03x faster                                                  |
| json_loads               | 26.5 us                                                | 25.7 us: 1.03x faster                                                  |
| async_generators         | 384 ms                                                 | 373 ms: 1.03x faster                                                   |
| meteor_contest           | 104 ms                                                 | 100 ms: 1.03x faster                                                   |
| json                     | 5.02 ms                                                | 4.88 ms: 1.03x faster                                                  |
| pprint_pformat           | 1.52 sec                                               | 1.48 sec: 1.03x faster                                                 |
| logging_silent           | 109 ns                                                 | 106 ns: 1.03x faster                                                   |
| sympy_integrate          | 20.5 ms                                                | 20.0 ms: 1.03x faster                                                  |
| pycparser                | 1.17 sec                                               | 1.14 sec: 1.03x faster                                                 |
| asyncio_tcp              | 519 ms                                                 | 506 ms: 1.02x faster                                                   |
| typing_runtime_protocols | 163 us                                                 | 159 us: 1.02x faster                                                   |
| xml_etree_parse          | 139 ms                                                 | 135 ms: 1.02x faster                                                   |
| mdp                      | 2.42 sec                                               | 2.37 sec: 1.02x faster                                                 |
| hexiom                   | 6.17 ms                                                | 6.07 ms: 1.02x faster                                                  |
| coroutines               | 23.9 ms                                                | 23.6 ms: 1.02x faster                                                  |
| unpickle_pure_python     | 221 us                                                 | 217 us: 1.02x faster                                                   |
| float                    | 80.8 ms                                                | 79.7 ms: 1.01x faster                                                  |
| sympy_expand             | 468 ms                                                 | 461 ms: 1.01x faster                                                   |
| genshi_text              | 22.8 ms                                                | 22.6 ms: 1.01x faster                                                  |
| docutils                 | 2.64 sec                                               | 2.61 sec: 1.01x faster                                                 |
| nqueens                  | 80.1 ms                                                | 79.3 ms: 1.01x faster                                                  |
| unpack_sequence          | 52.1 ns                                                | 51.6 ns: 1.01x faster                                                  |
| xml_etree_iterparse      | 96.7 ms                                                | 95.9 ms: 1.01x faster                                                  |
| xml_etree_generate       | 85.2 ms                                                | 85.4 ms: 1.00x slower                                                  |
| regex_effbot             | 3.17 ms                                                | 3.18 ms: 1.00x slower                                                  |
| sqlglot_normalize        | 107 ms                                                 | 107 ms: 1.01x slower                                                   |
| asyncio_websockets       | 517 ms                                                 | 520 ms: 1.01x slower                                                   |
| richards_super           | 51.9 ms                                                | 52.3 ms: 1.01x slower                                                  |
| xml_etree_process        | 59.0 ms                                                | 59.5 ms: 1.01x slower                                                  |
| asyncio_tcp_ssl          | 1.51 sec                                               | 1.52 sec: 1.01x slower                                                 |
| scimark_fft              | 342 ms                                                 | 345 ms: 1.01x slower                                                   |
| sqlglot_optimize         | 53.3 ms                                                | 53.8 ms: 1.01x slower                                                  |
| fannkuch                 | 372 ms                                                 | 377 ms: 1.01x slower                                                   |
| django_template          | 34.7 ms                                                | 35.2 ms: 1.01x slower                                                  |
| genshi_xml               | 50.2 ms                                                | 50.9 ms: 1.02x slower                                                  |
| scimark_lu               | 114 ms                                                 | 116 ms: 1.02x slower                                                   |
| richards                 | 45.9 ms                                                | 47.0 ms: 1.02x slower                                                  |
| pickle_list              | 4.77 us                                                | 4.90 us: 1.03x slower                                                  |
| pickle                   | 10.9 us                                                | 11.3 us: 1.03x slower                                                  |
| pickle_pure_python       | 308 us                                                 | 317 us: 1.03x slower                                                   |
| pickle_dict              | 31.8 us                                                | 32.8 us: 1.03x slower                                                  |
| spectral_norm            | 110 ms                                                 | 114 ms: 1.03x slower                                                   |
| python_startup_no_site   | 7.16 ms                                                | 7.41 ms: 1.03x slower                                                  |
| html5lib                 | 63.6 ms                                                | 66.5 ms: 1.04x slower                                                  |
| scimark_sor              | 130 ms                                                 | 136 ms: 1.05x slower                                                   |
| nbody                    | 89.3 ms                                                | 95.6 ms: 1.07x slower                                                  |
| bench_thread_pool        | 941 us                                                 | 1.01 ms: 1.08x slower                                                  |
| scimark_sparse_mat_mult  | 4.39 ms                                                | 4.73 ms: 1.08x slower                                                  |
| mako                     | 11.0 ms                                                | 12.0 ms: 1.09x slower                                                  |
| regex_dna                | 168 ms                                                 | 184 ms: 1.10x slower                                                   |
| python_startup           | 9.93 ms                                                | 11.0 ms: 1.11x slower                                                  |
| json_dumps               | 10.4 ms                                                | 11.6 ms: 1.12x slower                                                  |
| coverage                 | 71.4 ms                                                | 81.1 ms: 1.14x slower                                                  |
| telco                    | 6.53 ms                                                | 7.44 ms: 1.14x slower                                                  |
| regex_v8                 | 20.6 ms                                                | 24.6 ms: 1.19x slower                                                  |
| pidigits                 | 184 ms                                                 | 222 ms: 1.21x slower                                                   |
| create_gc_cycles         | 1.09 ms                                                | 1.35 ms: 1.24x slower                                                  |
| bench_mp_pool            | 10.8 ms                                                | 63.5 ms: 5.88x slower                                                  |
| Geometric mean           | (ref)                                                  | 1.01x slower                                                           |

Benchmark hidden because not significant (5): sqlite_synth, pylint, tomli_loads, unpickle_list, pyflate
Ignored benchmarks (17) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http

# HPT report

- Reliability score: 91.58% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.02x