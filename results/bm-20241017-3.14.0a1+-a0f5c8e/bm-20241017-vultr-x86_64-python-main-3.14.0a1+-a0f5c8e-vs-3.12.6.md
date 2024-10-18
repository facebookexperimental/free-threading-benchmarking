# Results vs. 3.12.6

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: a0f5c8e
- commit date: 2024-10-17
- overall geometric mean: 1.00x faster
- HPT reliability: 99.60%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241017-vultr-x86_64-python-main-3.14.0a1+-a0f5c8e |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 253 ms: 1.04x faster                                   |
| docutils       | 2.64 sec                                               | 2.59 sec: 1.02x faster                                 |
| html5lib       | 63.6 ms                                                | 62.7 ms: 1.01x faster                                  |
| tornado_http   | 119 ms                                                 | 114 ms: 1.05x faster                                   |
| Geometric mean | (ref)                                                  | 1.03x faster                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241017-vultr-x86_64-python-main-3.14.0a1+-a0f5c8e |
|--------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| coroutines         | 23.9 ms                                                | 22.4 ms: 1.07x faster                                  |
| async_generators   | 384 ms                                                 | 371 ms: 1.04x faster                                   |
| asyncio_tcp        | 519 ms                                                 | 504 ms: 1.03x faster                                   |
| asyncio_websockets | 517 ms                                                 | 521 ms: 1.01x slower                                   |
| asyncio_tcp_ssl    | 1.51 sec                                               | 1.52 sec: 1.01x slower                                 |
| Geometric mean     | (ref)                                                  | 1.02x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241017-vultr-x86_64-python-main-3.14.0a1+-a0f5c8e |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| float          | 80.8 ms                                                | 78.3 ms: 1.03x faster                                  |
| pidigits       | 184 ms                                                 | 185 ms: 1.01x slower                                   |
| nbody          | 89.3 ms                                                | 92.4 ms: 1.04x slower                                  |
| Geometric mean | (ref)                                                  | 1.00x slower                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241017-vultr-x86_64-python-main-3.14.0a1+-a0f5c8e |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 129 ms: 1.10x faster                                   |
| regex_effbot   | 3.17 ms                                                | 2.98 ms: 1.06x faster                                  |
| regex_dna      | 168 ms                                                 | 174 ms: 1.04x slower                                   |
| regex_v8       | 20.6 ms                                                | 23.0 ms: 1.12x slower                                  |
| Geometric mean | (ref)                                                  | 1.00x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241017-vultr-x86_64-python-main-3.14.0a1+-a0f5c8e |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| unpickle             | 14.1 us                                                | 13.5 us: 1.04x faster                                  |
| xml_etree_parse      | 139 ms                                                 | 135 ms: 1.03x faster                                   |
| pickle_dict          | 31.8 us                                                | 31.3 us: 1.02x faster                                  |
| xml_etree_iterparse  | 96.7 ms                                                | 95.2 ms: 1.02x faster                                  |
| json_loads           | 26.5 us                                                | 26.1 us: 1.02x faster                                  |
| unpickle_pure_python | 221 us                                                 | 217 us: 1.02x faster                                   |
| pickle_list          | 4.77 us                                                | 4.90 us: 1.03x slower                                  |
| unpickle_list        | 4.67 us                                                | 4.85 us: 1.04x slower                                  |
| pickle               | 10.9 us                                                | 11.6 us: 1.06x slower                                  |
| json_dumps           | 10.4 ms                                                | 11.6 ms: 1.12x slower                                  |
| Geometric mean       | (ref)                                                  | 1.01x slower                                           |

Benchmark hidden because not significant (4): tomli_loads, pickle_pure_python, xml_etree_generate, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241017-vultr-x86_64-python-main-3.14.0a1+-a0f5c8e |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.45 ms: 1.04x slower                                  |
| python_startup         | 9.93 ms                                                | 11.1 ms: 1.11x slower                                  |
| Geometric mean         | (ref)                                                  | 1.08x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241017-vultr-x86_64-python-main-3.14.0a1+-a0f5c8e |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 22.2 ms: 1.03x faster                                  |
| genshi_xml      | 50.2 ms                                                | 49.7 ms: 1.01x faster                                  |
| django_template | 34.7 ms                                                | 35.3 ms: 1.02x slower                                  |
| mako            | 11.0 ms                                                | 11.7 ms: 1.06x slower                                  |
| Geometric mean  | (ref)                                                  | 1.01x slower                                           |

All benchmarks:
===============

| Benchmark                | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241017-vultr-x86_64-python-main-3.14.0a1+-a0f5c8e |
|--------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| deepcopy                 | 352 us                                                 | 263 us: 1.34x faster                                   |
| deepcopy_memo            | 40.3 us                                                | 30.6 us: 1.32x faster                                  |
| unpack_sequence          | 52.1 ns                                                | 42.7 ns: 1.22x faster                                  |
| comprehensions           | 19.8 us                                                | 16.8 us: 1.18x faster                                  |
| pathlib                  | 21.5 ms                                                | 18.3 ms: 1.18x faster                                  |
| deepcopy_reduce          | 3.08 us                                                | 2.65 us: 1.16x faster                                  |
| crypto_pyaes             | 76.6 ms                                                | 66.3 ms: 1.15x faster                                  |
| go                       | 139 ms                                                 | 121 ms: 1.15x faster                                   |
| generators               | 32.2 ms                                                | 28.4 ms: 1.14x faster                                  |
| raytrace                 | 299 ms                                                 | 265 ms: 1.13x faster                                   |
| regex_compile            | 142 ms                                                 | 129 ms: 1.10x faster                                   |
| logging_simple           | 6.63 us                                                | 6.07 us: 1.09x faster                                  |
| bpe_tokeniser            | 4.74 sec                                               | 4.37 sec: 1.08x faster                                 |
| logging_format           | 7.35 us                                                | 6.79 us: 1.08x faster                                  |
| deltablue                | 3.45 ms                                                | 3.21 ms: 1.07x faster                                  |
| sympy_sum                | 166 ms                                                 | 155 ms: 1.07x faster                                   |
| coroutines               | 23.9 ms                                                | 22.4 ms: 1.07x faster                                  |
| dulwich_log              | 78.9 ms                                                | 74.2 ms: 1.06x faster                                  |
| regex_effbot             | 3.17 ms                                                | 2.98 ms: 1.06x faster                                  |
| sympy_str                | 292 ms                                                 | 275 ms: 1.06x faster                                   |
| chaos                    | 62.8 ms                                                | 59.3 ms: 1.06x faster                                  |
| sqlglot_parse            | 1.36 ms                                                | 1.28 ms: 1.05x faster                                  |
| sqlglot_transpile        | 1.67 ms                                                | 1.59 ms: 1.05x faster                                  |
| typing_runtime_protocols | 163 us                                                 | 156 us: 1.05x faster                                   |
| tornado_http             | 119 ms                                                 | 114 ms: 1.05x faster                                   |
| unpickle                 | 14.1 us                                                | 13.5 us: 1.04x faster                                  |
| gc_traversal             | 3.46 ms                                                | 3.32 ms: 1.04x faster                                  |
| 2to3                     | 264 ms                                                 | 253 ms: 1.04x faster                                   |
| pprint_safe_repr         | 743 ms                                                 | 714 ms: 1.04x faster                                   |
| async_generators         | 384 ms                                                 | 371 ms: 1.04x faster                                   |
| thrift                   | 791 us                                                 | 763 us: 1.04x faster                                   |
| json                     | 5.02 ms                                                | 4.85 ms: 1.04x faster                                  |
| pprint_pformat           | 1.52 sec                                               | 1.47 sec: 1.03x faster                                 |
| scimark_monte_carlo      | 68.4 ms                                                | 66.2 ms: 1.03x faster                                  |
| logging_silent           | 109 ns                                                 | 106 ns: 1.03x faster                                   |
| float                    | 80.8 ms                                                | 78.3 ms: 1.03x faster                                  |
| asyncio_tcp              | 519 ms                                                 | 504 ms: 1.03x faster                                   |
| mdp                      | 2.42 sec                                               | 2.35 sec: 1.03x faster                                 |
| genshi_text              | 22.8 ms                                                | 22.2 ms: 1.03x faster                                  |
| xml_etree_parse          | 139 ms                                                 | 135 ms: 1.03x faster                                   |
| sympy_integrate          | 20.5 ms                                                | 20.1 ms: 1.02x faster                                  |
| docutils                 | 2.64 sec                                               | 2.59 sec: 1.02x faster                                 |
| hexiom                   | 6.17 ms                                                | 6.05 ms: 1.02x faster                                  |
| pickle_dict              | 31.8 us                                                | 31.3 us: 1.02x faster                                  |
| xml_etree_iterparse      | 96.7 ms                                                | 95.2 ms: 1.02x faster                                  |
| json_loads               | 26.5 us                                                | 26.1 us: 1.02x faster                                  |
| sympy_expand             | 468 ms                                                 | 460 ms: 1.02x faster                                   |
| unpickle_pure_python     | 221 us                                                 | 217 us: 1.02x faster                                   |
| html5lib                 | 63.6 ms                                                | 62.7 ms: 1.01x faster                                  |
| scimark_lu               | 114 ms                                                 | 113 ms: 1.01x faster                                   |
| genshi_xml               | 50.2 ms                                                | 49.7 ms: 1.01x faster                                  |
| nqueens                  | 80.1 ms                                                | 79.3 ms: 1.01x faster                                  |
| scimark_fft              | 342 ms                                                 | 340 ms: 1.00x faster                                   |
| meteor_contest           | 104 ms                                                 | 103 ms: 1.00x faster                                   |
| sqlglot_optimize         | 53.3 ms                                                | 53.6 ms: 1.01x slower                                  |
| pidigits                 | 184 ms                                                 | 185 ms: 1.01x slower                                   |
| asyncio_websockets       | 517 ms                                                 | 521 ms: 1.01x slower                                   |
| pyflate                  | 448 ms                                                 | 451 ms: 1.01x slower                                   |
| asyncio_tcp_ssl          | 1.51 sec                                               | 1.52 sec: 1.01x slower                                 |
| spectral_norm            | 110 ms                                                 | 111 ms: 1.01x slower                                   |
| fannkuch                 | 372 ms                                                 | 377 ms: 1.01x slower                                   |
| scimark_sparse_mat_mult  | 4.39 ms                                                | 4.46 ms: 1.01x slower                                  |
| django_template          | 34.7 ms                                                | 35.3 ms: 1.02x slower                                  |
| pycparser                | 1.17 sec                                               | 1.20 sec: 1.02x slower                                 |
| pickle_list              | 4.77 us                                                | 4.90 us: 1.03x slower                                  |
| nbody                    | 89.3 ms                                                | 92.4 ms: 1.04x slower                                  |
| regex_dna                | 168 ms                                                 | 174 ms: 1.04x slower                                   |
| unpickle_list            | 4.67 us                                                | 4.85 us: 1.04x slower                                  |
| python_startup_no_site   | 7.16 ms                                                | 7.45 ms: 1.04x slower                                  |
| scimark_sor              | 130 ms                                                 | 136 ms: 1.04x slower                                   |
| mako                     | 11.0 ms                                                | 11.7 ms: 1.06x slower                                  |
| pickle                   | 10.9 us                                                | 11.6 us: 1.06x slower                                  |
| bench_thread_pool        | 941 us                                                 | 1.02 ms: 1.08x slower                                  |
| python_startup           | 9.93 ms                                                | 11.1 ms: 1.11x slower                                  |
| regex_v8                 | 20.6 ms                                                | 23.0 ms: 1.12x slower                                  |
| json_dumps               | 10.4 ms                                                | 11.6 ms: 1.12x slower                                  |
| telco                    | 6.53 ms                                                | 7.37 ms: 1.13x slower                                  |
| coverage                 | 71.4 ms                                                | 82.1 ms: 1.15x slower                                  |
| create_gc_cycles         | 1.09 ms                                                | 1.35 ms: 1.24x slower                                  |
| bench_mp_pool            | 10.8 ms                                                | 64.1 ms: 5.93x slower                                  |
| Geometric mean           | (ref)                                                  | 1.00x faster                                           |

Benchmark hidden because not significant (9): tomli_loads, pickle_pure_python, sqlite_synth, xml_etree_generate, sqlglot_normalize, pylint, xml_etree_process, richards_super, richards
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 99.60% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.02x