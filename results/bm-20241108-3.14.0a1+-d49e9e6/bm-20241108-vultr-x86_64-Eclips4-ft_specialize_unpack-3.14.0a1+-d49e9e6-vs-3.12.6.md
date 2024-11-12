# Results vs. 3.12.6

- fork: Eclips4
- ref: ft_specialize_unpack
- machine: linux-x86_64
- commit hash: d49e9e6
- commit date: 2024-11-08
- overall geometric mean: 1.00x slower
- HPT reliability: 98.49%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1+-d49e9e6 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 254 ms: 1.04x faster                                                    |
| docutils       | 2.64 sec                                               | 2.61 sec: 1.01x faster                                                  |
| html5lib       | 63.6 ms                                                | 66.2 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                  | 1.00x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1+-d49e9e6 |
|--------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_generators   | 384 ms                                                 | 366 ms: 1.05x faster                                                    |
| asyncio_tcp        | 519 ms                                                 | 506 ms: 1.03x faster                                                    |
| coroutines         | 23.9 ms                                                | 23.3 ms: 1.03x faster                                                   |
| asyncio_websockets | 517 ms                                                 | 521 ms: 1.01x slower                                                    |
| asyncio_tcp_ssl    | 1.51 sec                                               | 1.52 sec: 1.01x slower                                                  |
| Geometric mean     | (ref)                                                  | 1.02x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1+-d49e9e6 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 78.1 ms: 1.03x faster                                                   |
| nbody          | 89.3 ms                                                | 93.8 ms: 1.05x slower                                                   |
| pidigits       | 184 ms                                                 | 224 ms: 1.21x slower                                                    |
| Geometric mean | (ref)                                                  | 1.07x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1+-d49e9e6 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 129 ms: 1.11x faster                                                    |
| regex_effbot   | 3.17 ms                                                | 3.35 ms: 1.06x slower                                                   |
| regex_dna      | 168 ms                                                 | 183 ms: 1.09x slower                                                    |
| regex_v8       | 20.6 ms                                                | 23.6 ms: 1.14x slower                                                   |
| Geometric mean | (ref)                                                  | 1.04x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1+-d49e9e6 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| unpickle_pure_python | 221 us                                                 | 214 us: 1.03x faster                                                    |
| json_loads           | 26.5 us                                                | 26.0 us: 1.02x faster                                                   |
| xml_etree_parse      | 139 ms                                                 | 137 ms: 1.01x faster                                                    |
| xml_etree_iterparse  | 96.7 ms                                                | 95.9 ms: 1.01x faster                                                   |
| xml_etree_generate   | 85.2 ms                                                | 85.9 ms: 1.01x slower                                                   |
| xml_etree_process    | 59.0 ms                                                | 59.5 ms: 1.01x slower                                                   |
| pickle_dict          | 31.8 us                                                | 32.2 us: 1.01x slower                                                   |
| pickle_pure_python   | 308 us                                                 | 317 us: 1.03x slower                                                    |
| pickle_list          | 4.77 us                                                | 5.08 us: 1.07x slower                                                   |
| unpickle_list        | 4.67 us                                                | 4.99 us: 1.07x slower                                                   |
| json_dumps           | 10.4 ms                                                | 11.6 ms: 1.12x slower                                                   |
| pickle               | 10.9 us                                                | 12.6 us: 1.15x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.03x slower                                                            |

Benchmark hidden because not significant (2): unpickle, tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1+-d49e9e6 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.48 ms: 1.04x slower                                                   |
| python_startup         | 9.93 ms                                                | 11.1 ms: 1.12x slower                                                   |
| Geometric mean         | (ref)                                                  | 1.08x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1+-d49e9e6 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 22.3 ms: 1.02x faster                                                   |
| django_template | 34.7 ms                                                | 34.9 ms: 1.01x slower                                                   |
| mako            | 11.0 ms                                                | 11.8 ms: 1.07x slower                                                   |
| Geometric mean  | (ref)                                                  | 1.01x slower                                                            |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1+-d49e9e6 |
|--------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| deepcopy_memo            | 40.3 us                                                | 29.9 us: 1.35x faster                                                   |
| deepcopy                 | 352 us                                                 | 262 us: 1.34x faster                                                    |
| pathlib                  | 21.5 ms                                                | 18.1 ms: 1.19x faster                                                   |
| deepcopy_reduce          | 3.08 us                                                | 2.61 us: 1.18x faster                                                   |
| raytrace                 | 299 ms                                                 | 259 ms: 1.16x faster                                                    |
| comprehensions           | 19.8 us                                                | 17.2 us: 1.15x faster                                                   |
| go                       | 139 ms                                                 | 121 ms: 1.15x faster                                                    |
| crypto_pyaes             | 76.6 ms                                                | 66.9 ms: 1.15x faster                                                   |
| unpack_sequence          | 52.1 ns                                                | 45.5 ns: 1.14x faster                                                   |
| regex_compile            | 142 ms                                                 | 129 ms: 1.11x faster                                                    |
| generators               | 32.2 ms                                                | 29.3 ms: 1.10x faster                                                   |
| logging_simple           | 6.63 us                                                | 6.04 us: 1.10x faster                                                   |
| bpe_tokeniser            | 4.74 sec                                               | 4.35 sec: 1.09x faster                                                  |
| logging_format           | 7.35 us                                                | 6.77 us: 1.09x faster                                                   |
| sympy_sum                | 166 ms                                                 | 154 ms: 1.08x faster                                                    |
| chaos                    | 62.8 ms                                                | 58.3 ms: 1.08x faster                                                   |
| deltablue                | 3.45 ms                                                | 3.21 ms: 1.07x faster                                                   |
| sympy_str                | 292 ms                                                 | 272 ms: 1.07x faster                                                    |
| gc_traversal             | 3.46 ms                                                | 3.25 ms: 1.06x faster                                                   |
| thrift                   | 791 us                                                 | 747 us: 1.06x faster                                                    |
| sqlglot_transpile        | 1.67 ms                                                | 1.58 ms: 1.06x faster                                                   |
| logging_silent           | 109 ns                                                 | 103 ns: 1.06x faster                                                    |
| sqlglot_parse            | 1.36 ms                                                | 1.28 ms: 1.06x faster                                                   |
| pprint_safe_repr         | 743 ms                                                 | 704 ms: 1.06x faster                                                    |
| scimark_monte_carlo      | 68.4 ms                                                | 65.0 ms: 1.05x faster                                                   |
| async_generators         | 384 ms                                                 | 366 ms: 1.05x faster                                                    |
| dulwich_log              | 78.9 ms                                                | 75.5 ms: 1.04x faster                                                   |
| pprint_pformat           | 1.52 sec                                               | 1.46 sec: 1.04x faster                                                  |
| typing_runtime_protocols | 163 us                                                 | 157 us: 1.04x faster                                                    |
| 2to3                     | 264 ms                                                 | 254 ms: 1.04x faster                                                    |
| float                    | 80.8 ms                                                | 78.1 ms: 1.03x faster                                                   |
| sympy_integrate          | 20.5 ms                                                | 19.9 ms: 1.03x faster                                                   |
| pycparser                | 1.17 sec                                               | 1.13 sec: 1.03x faster                                                  |
| hexiom                   | 6.17 ms                                                | 5.97 ms: 1.03x faster                                                   |
| unpickle_pure_python     | 221 us                                                 | 214 us: 1.03x faster                                                    |
| meteor_contest           | 104 ms                                                 | 101 ms: 1.03x faster                                                    |
| mdp                      | 2.42 sec                                               | 2.35 sec: 1.03x faster                                                  |
| json                     | 5.02 ms                                                | 4.89 ms: 1.03x faster                                                   |
| asyncio_tcp              | 519 ms                                                 | 506 ms: 1.03x faster                                                    |
| coroutines               | 23.9 ms                                                | 23.3 ms: 1.03x faster                                                   |
| genshi_text              | 22.8 ms                                                | 22.3 ms: 1.02x faster                                                   |
| sympy_expand             | 468 ms                                                 | 459 ms: 1.02x faster                                                    |
| json_loads               | 26.5 us                                                | 26.0 us: 1.02x faster                                                   |
| nqueens                  | 80.1 ms                                                | 78.6 ms: 1.02x faster                                                   |
| xml_etree_parse          | 139 ms                                                 | 137 ms: 1.01x faster                                                    |
| docutils                 | 2.64 sec                                               | 2.61 sec: 1.01x faster                                                  |
| scimark_fft              | 342 ms                                                 | 338 ms: 1.01x faster                                                    |
| xml_etree_iterparse      | 96.7 ms                                                | 95.9 ms: 1.01x faster                                                   |
| pyflate                  | 448 ms                                                 | 445 ms: 1.01x faster                                                    |
| scimark_lu               | 114 ms                                                 | 115 ms: 1.01x slower                                                    |
| asyncio_websockets       | 517 ms                                                 | 521 ms: 1.01x slower                                                    |
| django_template          | 34.7 ms                                                | 34.9 ms: 1.01x slower                                                   |
| xml_etree_generate       | 85.2 ms                                                | 85.9 ms: 1.01x slower                                                   |
| asyncio_tcp_ssl          | 1.51 sec                                               | 1.52 sec: 1.01x slower                                                  |
| sqlglot_optimize         | 53.3 ms                                                | 53.7 ms: 1.01x slower                                                   |
| xml_etree_process        | 59.0 ms                                                | 59.5 ms: 1.01x slower                                                   |
| fannkuch                 | 372 ms                                                 | 377 ms: 1.01x slower                                                    |
| pickle_dict              | 31.8 us                                                | 32.2 us: 1.01x slower                                                   |
| sqlite_synth             | 2.20 us                                                | 2.24 us: 1.02x slower                                                   |
| spectral_norm            | 110 ms                                                 | 113 ms: 1.02x slower                                                    |
| scimark_sor              | 130 ms                                                 | 133 ms: 1.02x slower                                                    |
| pickle_pure_python       | 308 us                                                 | 317 us: 1.03x slower                                                    |
| html5lib                 | 63.6 ms                                                | 66.2 ms: 1.04x slower                                                   |
| python_startup_no_site   | 7.16 ms                                                | 7.48 ms: 1.04x slower                                                   |
| nbody                    | 89.3 ms                                                | 93.8 ms: 1.05x slower                                                   |
| regex_effbot             | 3.17 ms                                                | 3.35 ms: 1.06x slower                                                   |
| scimark_sparse_mat_mult  | 4.39 ms                                                | 4.66 ms: 1.06x slower                                                   |
| pickle_list              | 4.77 us                                                | 5.08 us: 1.07x slower                                                   |
| mako                     | 11.0 ms                                                | 11.8 ms: 1.07x slower                                                   |
| unpickle_list            | 4.67 us                                                | 4.99 us: 1.07x slower                                                   |
| bench_thread_pool        | 941 us                                                 | 1.02 ms: 1.09x slower                                                   |
| regex_dna                | 168 ms                                                 | 183 ms: 1.09x slower                                                    |
| json_dumps               | 10.4 ms                                                | 11.6 ms: 1.12x slower                                                   |
| python_startup           | 9.93 ms                                                | 11.1 ms: 1.12x slower                                                   |
| coverage                 | 71.4 ms                                                | 81.3 ms: 1.14x slower                                                   |
| telco                    | 6.53 ms                                                | 7.43 ms: 1.14x slower                                                   |
| regex_v8                 | 20.6 ms                                                | 23.6 ms: 1.14x slower                                                   |
| pickle                   | 10.9 us                                                | 12.6 us: 1.15x slower                                                   |
| pidigits                 | 184 ms                                                 | 224 ms: 1.21x slower                                                    |
| create_gc_cycles         | 1.09 ms                                                | 1.36 ms: 1.25x slower                                                   |
| bench_mp_pool            | 10.8 ms                                                | 64.2 ms: 5.94x slower                                                   |
| Geometric mean           | (ref)                                                  | 1.00x slower                                                            |

Benchmark hidden because not significant (7): richards, richards_super, pylint, unpickle, sqlglot_normalize, tomli_loads, genshi_xml
Ignored benchmarks (17) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http

# HPT report

- Reliability score: 98.49% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.02x