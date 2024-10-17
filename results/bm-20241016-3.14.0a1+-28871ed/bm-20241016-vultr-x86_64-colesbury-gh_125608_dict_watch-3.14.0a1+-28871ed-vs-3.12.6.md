# Results vs. 3.12.6

- fork: colesbury
- ref: gh_125608_dict_watch
- machine: linux-x86_64
- commit hash: 28871ed
- commit date: 2024-10-16
- overall geometric mean: 1.00x faster
- HPT reliability: 99.91%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241016-vultr-x86_64-colesbury-gh_125608_dict_watch-3.14.0a1+-28871ed |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 253 ms: 1.04x faster                                                      |
| docutils       | 2.64 sec                                               | 2.58 sec: 1.02x faster                                                    |
| html5lib       | 63.6 ms                                                | 62.6 ms: 1.02x faster                                                     |
| tornado_http   | 119 ms                                                 | 113 ms: 1.05x faster                                                      |
| Geometric mean | (ref)                                                  | 1.03x faster                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241016-vultr-x86_64-colesbury-gh_125608_dict_watch-3.14.0a1+-28871ed |
|--------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| coroutines         | 23.9 ms                                                | 22.2 ms: 1.08x faster                                                     |
| async_generators   | 384 ms                                                 | 374 ms: 1.03x faster                                                      |
| asyncio_tcp        | 519 ms                                                 | 506 ms: 1.02x faster                                                      |
| asyncio_websockets | 517 ms                                                 | 521 ms: 1.01x slower                                                      |
| asyncio_tcp_ssl    | 1.51 sec                                               | 1.52 sec: 1.01x slower                                                    |
| Geometric mean     | (ref)                                                  | 1.02x faster                                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241016-vultr-x86_64-colesbury-gh_125608_dict_watch-3.14.0a1+-28871ed |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 78.5 ms: 1.03x faster                                                     |
| pidigits       | 184 ms                                                 | 185 ms: 1.00x slower                                                      |
| nbody          | 89.3 ms                                                | 93.6 ms: 1.05x slower                                                     |
| Geometric mean | (ref)                                                  | 1.01x slower                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241016-vultr-x86_64-colesbury-gh_125608_dict_watch-3.14.0a1+-28871ed |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 129 ms: 1.11x faster                                                      |
| regex_effbot   | 3.17 ms                                                | 3.09 ms: 1.03x faster                                                     |
| regex_dna      | 168 ms                                                 | 169 ms: 1.01x slower                                                      |
| regex_v8       | 20.6 ms                                                | 23.5 ms: 1.14x slower                                                     |
| Geometric mean | (ref)                                                  | 1.00x slower                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241016-vultr-x86_64-colesbury-gh_125608_dict_watch-3.14.0a1+-28871ed |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| unpickle             | 14.1 us                                                | 13.5 us: 1.04x faster                                                     |
| xml_etree_parse      | 139 ms                                                 | 136 ms: 1.02x faster                                                      |
| unpickle_pure_python | 221 us                                                 | 216 us: 1.02x faster                                                      |
| json_loads           | 26.5 us                                                | 26.0 us: 1.02x faster                                                     |
| tomli_loads          | 2.11 sec                                               | 2.08 sec: 1.01x faster                                                    |
| unpickle_list        | 4.67 us                                                | 4.65 us: 1.01x faster                                                     |
| pickle_pure_python   | 308 us                                                 | 307 us: 1.00x faster                                                      |
| pickle               | 10.9 us                                                | 11.2 us: 1.02x slower                                                     |
| pickle_dict          | 31.8 us                                                | 33.0 us: 1.04x slower                                                     |
| pickle_list          | 4.77 us                                                | 4.99 us: 1.05x slower                                                     |
| json_dumps           | 10.4 ms                                                | 11.6 ms: 1.12x slower                                                     |
| Geometric mean       | (ref)                                                  | 1.01x slower                                                              |

Benchmark hidden because not significant (3): xml_etree_generate, xml_etree_iterparse, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241016-vultr-x86_64-colesbury-gh_125608_dict_watch-3.14.0a1+-28871ed |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.40 ms: 1.03x slower                                                     |
| python_startup         | 9.93 ms                                                | 11.0 ms: 1.11x slower                                                     |
| Geometric mean         | (ref)                                                  | 1.07x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241016-vultr-x86_64-colesbury-gh_125608_dict_watch-3.14.0a1+-28871ed |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 22.3 ms: 1.02x faster                                                     |
| genshi_xml      | 50.2 ms                                                | 49.7 ms: 1.01x faster                                                     |
| django_template | 34.7 ms                                                | 35.4 ms: 1.02x slower                                                     |
| mako            | 11.0 ms                                                | 11.8 ms: 1.07x slower                                                     |
| Geometric mean  | (ref)                                                  | 1.01x slower                                                              |

All benchmarks:
===============

| Benchmark                | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241016-vultr-x86_64-colesbury-gh_125608_dict_watch-3.14.0a1+-28871ed |
|--------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| deepcopy                 | 352 us                                                 | 263 us: 1.34x faster                                                      |
| deepcopy_memo            | 40.3 us                                                | 30.5 us: 1.32x faster                                                     |
| comprehensions           | 19.8 us                                                | 17.1 us: 1.16x faster                                                     |
| deepcopy_reduce          | 3.08 us                                                | 2.66 us: 1.16x faster                                                     |
| go                       | 139 ms                                                 | 121 ms: 1.15x faster                                                      |
| pathlib                  | 21.5 ms                                                | 18.7 ms: 1.15x faster                                                     |
| raytrace                 | 299 ms                                                 | 260 ms: 1.15x faster                                                      |
| generators               | 32.2 ms                                                | 28.6 ms: 1.13x faster                                                     |
| crypto_pyaes             | 76.6 ms                                                | 68.4 ms: 1.12x faster                                                     |
| regex_compile            | 142 ms                                                 | 129 ms: 1.11x faster                                                      |
| bpe_tokeniser            | 4.74 sec                                               | 4.32 sec: 1.10x faster                                                    |
| logging_simple           | 6.63 us                                                | 6.05 us: 1.09x faster                                                     |
| logging_format           | 7.35 us                                                | 6.73 us: 1.09x faster                                                     |
| logging_silent           | 109 ns                                                 | 100 ns: 1.09x faster                                                      |
| sympy_sum                | 166 ms                                                 | 154 ms: 1.08x faster                                                      |
| coroutines               | 23.9 ms                                                | 22.2 ms: 1.08x faster                                                     |
| sympy_str                | 292 ms                                                 | 272 ms: 1.07x faster                                                      |
| deltablue                | 3.45 ms                                                | 3.22 ms: 1.07x faster                                                     |
| chaos                    | 62.8 ms                                                | 58.8 ms: 1.07x faster                                                     |
| dulwich_log              | 78.9 ms                                                | 74.6 ms: 1.06x faster                                                     |
| thrift                   | 791 us                                                 | 754 us: 1.05x faster                                                      |
| tornado_http             | 119 ms                                                 | 113 ms: 1.05x faster                                                      |
| sqlglot_parse            | 1.36 ms                                                | 1.30 ms: 1.05x faster                                                     |
| unpickle                 | 14.1 us                                                | 13.5 us: 1.04x faster                                                     |
| sqlglot_transpile        | 1.67 ms                                                | 1.60 ms: 1.04x faster                                                     |
| 2to3                     | 264 ms                                                 | 253 ms: 1.04x faster                                                      |
| typing_runtime_protocols | 163 us                                                 | 157 us: 1.04x faster                                                      |
| pprint_safe_repr         | 743 ms                                                 | 714 ms: 1.04x faster                                                      |
| scimark_monte_carlo      | 68.4 ms                                                | 66.0 ms: 1.04x faster                                                     |
| pprint_pformat           | 1.52 sec                                               | 1.47 sec: 1.04x faster                                                    |
| json                     | 5.02 ms                                                | 4.87 ms: 1.03x faster                                                     |
| hexiom                   | 6.17 ms                                                | 5.98 ms: 1.03x faster                                                     |
| float                    | 80.8 ms                                                | 78.5 ms: 1.03x faster                                                     |
| async_generators         | 384 ms                                                 | 374 ms: 1.03x faster                                                      |
| pycparser                | 1.17 sec                                               | 1.14 sec: 1.03x faster                                                    |
| sympy_integrate          | 20.5 ms                                                | 20.0 ms: 1.03x faster                                                     |
| sympy_expand             | 468 ms                                                 | 455 ms: 1.03x faster                                                      |
| regex_effbot             | 3.17 ms                                                | 3.09 ms: 1.03x faster                                                     |
| asyncio_tcp              | 519 ms                                                 | 506 ms: 1.02x faster                                                      |
| genshi_text              | 22.8 ms                                                | 22.3 ms: 1.02x faster                                                     |
| nqueens                  | 80.1 ms                                                | 78.2 ms: 1.02x faster                                                     |
| scimark_lu               | 114 ms                                                 | 112 ms: 1.02x faster                                                      |
| xml_etree_parse          | 139 ms                                                 | 136 ms: 1.02x faster                                                      |
| docutils                 | 2.64 sec                                               | 2.58 sec: 1.02x faster                                                    |
| unpickle_pure_python     | 221 us                                                 | 216 us: 1.02x faster                                                      |
| json_loads               | 26.5 us                                                | 26.0 us: 1.02x faster                                                     |
| meteor_contest           | 104 ms                                                 | 102 ms: 1.02x faster                                                      |
| scimark_fft              | 342 ms                                                 | 336 ms: 1.02x faster                                                      |
| html5lib                 | 63.6 ms                                                | 62.6 ms: 1.02x faster                                                     |
| spectral_norm            | 110 ms                                                 | 108 ms: 1.02x faster                                                      |
| tomli_loads              | 2.11 sec                                               | 2.08 sec: 1.01x faster                                                    |
| genshi_xml               | 50.2 ms                                                | 49.7 ms: 1.01x faster                                                     |
| pyflate                  | 448 ms                                                 | 445 ms: 1.01x faster                                                      |
| unpickle_list            | 4.67 us                                                | 4.65 us: 1.01x faster                                                     |
| pickle_pure_python       | 308 us                                                 | 307 us: 1.00x faster                                                      |
| gc_traversal             | 3.46 ms                                                | 3.47 ms: 1.00x slower                                                     |
| pidigits                 | 184 ms                                                 | 185 ms: 1.00x slower                                                      |
| asyncio_websockets       | 517 ms                                                 | 521 ms: 1.01x slower                                                      |
| regex_dna                | 168 ms                                                 | 169 ms: 1.01x slower                                                      |
| sqlglot_optimize         | 53.3 ms                                                | 53.8 ms: 1.01x slower                                                     |
| asyncio_tcp_ssl          | 1.51 sec                                               | 1.52 sec: 1.01x slower                                                    |
| fannkuch                 | 372 ms                                                 | 377 ms: 1.01x slower                                                      |
| unpack_sequence          | 52.1 ns                                                | 53.0 ns: 1.02x slower                                                     |
| django_template          | 34.7 ms                                                | 35.4 ms: 1.02x slower                                                     |
| scimark_sparse_mat_mult  | 4.39 ms                                                | 4.49 ms: 1.02x slower                                                     |
| pickle                   | 10.9 us                                                | 11.2 us: 1.02x slower                                                     |
| mdp                      | 2.42 sec                                               | 2.48 sec: 1.03x slower                                                    |
| python_startup_no_site   | 7.16 ms                                                | 7.40 ms: 1.03x slower                                                     |
| pickle_dict              | 31.8 us                                                | 33.0 us: 1.04x slower                                                     |
| scimark_sor              | 130 ms                                                 | 135 ms: 1.04x slower                                                      |
| pickle_list              | 4.77 us                                                | 4.99 us: 1.05x slower                                                     |
| nbody                    | 89.3 ms                                                | 93.6 ms: 1.05x slower                                                     |
| mako                     | 11.0 ms                                                | 11.8 ms: 1.07x slower                                                     |
| bench_thread_pool        | 941 us                                                 | 1.02 ms: 1.08x slower                                                     |
| python_startup           | 9.93 ms                                                | 11.0 ms: 1.11x slower                                                     |
| json_dumps               | 10.4 ms                                                | 11.6 ms: 1.12x slower                                                     |
| telco                    | 6.53 ms                                                | 7.34 ms: 1.12x slower                                                     |
| regex_v8                 | 20.6 ms                                                | 23.5 ms: 1.14x slower                                                     |
| coverage                 | 71.4 ms                                                | 82.6 ms: 1.16x slower                                                     |
| create_gc_cycles         | 1.09 ms                                                | 1.35 ms: 1.24x slower                                                     |
| bench_mp_pool            | 10.8 ms                                                | 63.4 ms: 5.87x slower                                                     |
| Geometric mean           | (ref)                                                  | 1.00x faster                                                              |

Benchmark hidden because not significant (8): richards, pylint, sqlglot_normalize, richards_super, xml_etree_generate, xml_etree_iterparse, sqlite_synth, xml_etree_process
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 99.91% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.02x