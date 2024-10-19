# Results vs. 3.12.6

- fork: mpage
- ref: gh_115999_tlbc_call
- machine: linux-x86_64
- commit hash: 819f30a
- commit date: 2024-10-18
- overall geometric mean: 1.50x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.35x slower
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241018-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-819f30a |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 410 ms: 1.55x slower                                                |
| docutils       | 2.64 sec                                               | 3.28 sec: 1.24x slower                                              |
| html5lib       | 63.6 ms                                                | 103 ms: 1.62x slower                                                |
| tornado_http   | 119 ms                                                 | 163 ms: 1.37x slower                                                |
| Geometric mean | (ref)                                                  | 1.44x slower                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241018-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-819f30a |
|--------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| asyncio_websockets | 517 ms                                                 | 519 ms: 1.00x slower                                                |
| asyncio_tcp        | 519 ms                                                 | 582 ms: 1.12x slower                                                |
| asyncio_tcp_ssl    | 1.51 sec                                               | 1.82 sec: 1.21x slower                                              |
| coroutines         | 23.9 ms                                                | 29.2 ms: 1.22x slower                                               |
| async_generators   | 384 ms                                                 | 500 ms: 1.30x slower                                                |
| Geometric mean     | (ref)                                                  | 1.17x slower                                                        |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241018-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-819f30a |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 146 ms: 1.81x slower                                                |
| nbody          | 89.3 ms                                                | 186 ms: 2.09x slower                                                |
| Geometric mean | (ref)                                                  | 1.56x slower                                                        |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241018-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-819f30a |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 3.21 ms: 1.01x slower                                               |
| regex_dna      | 168 ms                                                 | 191 ms: 1.14x slower                                                |
| regex_v8       | 20.6 ms                                                | 25.3 ms: 1.23x slower                                               |
| regex_compile  | 142 ms                                                 | 221 ms: 1.55x slower                                                |
| Geometric mean | (ref)                                                  | 1.22x slower                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241018-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-819f30a |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 132 ms: 1.05x faster                                                |
| pickle_dict          | 31.8 us                                                | 31.1 us: 1.02x faster                                               |
| pickle_list          | 4.77 us                                                | 4.90 us: 1.03x slower                                               |
| unpickle             | 14.1 us                                                | 15.0 us: 1.07x slower                                               |
| json_loads           | 26.5 us                                                | 28.3 us: 1.07x slower                                               |
| unpickle_list        | 4.67 us                                                | 5.14 us: 1.10x slower                                               |
| xml_etree_iterparse  | 96.7 ms                                                | 106 ms: 1.10x slower                                                |
| xml_etree_generate   | 85.2 ms                                                | 109 ms: 1.28x slower                                                |
| json_dumps           | 10.4 ms                                                | 15.0 ms: 1.45x slower                                               |
| xml_etree_process    | 59.0 ms                                                | 89.1 ms: 1.51x slower                                               |
| tomli_loads          | 2.11 sec                                               | 3.21 sec: 1.53x slower                                              |
| unpickle_pure_python | 221 us                                                 | 386 us: 1.75x slower                                                |
| pickle_pure_python   | 308 us                                                 | 584 us: 1.90x slower                                                |
| Geometric mean       | (ref)                                                  | 1.23x slower                                                        |

Benchmark hidden because not significant (1): pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241018-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-819f30a |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.3 ms: 1.44x slower                                               |
| python_startup         | 9.93 ms                                                | 15.7 ms: 1.58x slower                                               |
| Geometric mean         | (ref)                                                  | 1.51x slower                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241018-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-819f30a |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 80.6 ms: 1.61x slower                                               |
| genshi_text     | 22.8 ms                                                | 39.2 ms: 1.72x slower                                               |
| mako            | 11.0 ms                                                | 19.3 ms: 1.75x slower                                               |
| django_template | 34.7 ms                                                | 62.1 ms: 1.79x slower                                               |
| Geometric mean  | (ref)                                                  | 1.72x slower                                                        |

All benchmarks:
===============

| Benchmark                | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241018-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-819f30a |
|--------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| gc_traversal             | 3.46 ms                                                | 2.47 ms: 1.40x faster                                               |
| xml_etree_parse          | 139 ms                                                 | 132 ms: 1.05x faster                                                |
| pickle_dict              | 31.8 us                                                | 31.1 us: 1.02x faster                                               |
| asyncio_websockets       | 517 ms                                                 | 519 ms: 1.00x slower                                                |
| regex_effbot             | 3.17 ms                                                | 3.21 ms: 1.01x slower                                               |
| pathlib                  | 21.5 ms                                                | 21.9 ms: 1.02x slower                                               |
| pickle_list              | 4.77 us                                                | 4.90 us: 1.03x slower                                               |
| create_gc_cycles         | 1.09 ms                                                | 1.13 ms: 1.03x slower                                               |
| json                     | 5.02 ms                                                | 5.20 ms: 1.03x slower                                               |
| unpickle                 | 14.1 us                                                | 15.0 us: 1.07x slower                                               |
| json_loads               | 26.5 us                                                | 28.3 us: 1.07x slower                                               |
| sqlite_synth             | 2.20 us                                                | 2.42 us: 1.10x slower                                               |
| unpickle_list            | 4.67 us                                                | 5.14 us: 1.10x slower                                               |
| xml_etree_iterparse      | 96.7 ms                                                | 106 ms: 1.10x slower                                                |
| asyncio_tcp              | 519 ms                                                 | 582 ms: 1.12x slower                                                |
| regex_dna                | 168 ms                                                 | 191 ms: 1.14x slower                                                |
| scimark_fft              | 342 ms                                                 | 401 ms: 1.17x slower                                                |
| deepcopy                 | 352 us                                                 | 414 us: 1.18x slower                                                |
| asyncio_tcp_ssl          | 1.51 sec                                               | 1.82 sec: 1.21x slower                                              |
| bpe_tokeniser            | 4.74 sec                                               | 5.76 sec: 1.22x slower                                              |
| coroutines               | 23.9 ms                                                | 29.2 ms: 1.22x slower                                               |
| regex_v8                 | 20.6 ms                                                | 25.3 ms: 1.23x slower                                               |
| docutils                 | 2.64 sec                                               | 3.28 sec: 1.24x slower                                              |
| deepcopy_memo            | 40.3 us                                                | 50.3 us: 1.25x slower                                               |
| scimark_sparse_mat_mult  | 4.39 ms                                                | 5.52 ms: 1.26x slower                                               |
| xml_etree_generate       | 85.2 ms                                                | 109 ms: 1.28x slower                                                |
| dulwich_log              | 78.9 ms                                                | 102 ms: 1.29x slower                                                |
| mdp                      | 2.42 sec                                               | 3.13 sec: 1.30x slower                                              |
| pylint                   | 319 ms                                                 | 414 ms: 1.30x slower                                                |
| async_generators         | 384 ms                                                 | 500 ms: 1.30x slower                                                |
| meteor_contest           | 104 ms                                                 | 136 ms: 1.32x slower                                                |
| spectral_norm            | 110 ms                                                 | 147 ms: 1.34x slower                                                |
| generators               | 32.2 ms                                                | 43.1 ms: 1.34x slower                                               |
| tornado_http             | 119 ms                                                 | 163 ms: 1.37x slower                                                |
| nqueens                  | 80.1 ms                                                | 111 ms: 1.39x slower                                                |
| crypto_pyaes             | 76.6 ms                                                | 107 ms: 1.40x slower                                                |
| coverage                 | 71.4 ms                                                | 101 ms: 1.41x slower                                                |
| deepcopy_reduce          | 3.08 us                                                | 4.34 us: 1.41x slower                                               |
| pycparser                | 1.17 sec                                               | 1.66 sec: 1.42x slower                                              |
| python_startup_no_site   | 7.16 ms                                                | 10.3 ms: 1.44x slower                                               |
| json_dumps               | 10.4 ms                                                | 15.0 ms: 1.45x slower                                               |
| telco                    | 6.53 ms                                                | 9.53 ms: 1.46x slower                                               |
| typing_runtime_protocols | 163 us                                                 | 241 us: 1.47x slower                                                |
| comprehensions           | 19.8 us                                                | 29.5 us: 1.49x slower                                               |
| fannkuch                 | 372 ms                                                 | 554 ms: 1.49x slower                                                |
| xml_etree_process        | 59.0 ms                                                | 89.1 ms: 1.51x slower                                               |
| tomli_loads              | 2.11 sec                                               | 3.21 sec: 1.53x slower                                              |
| regex_compile            | 142 ms                                                 | 221 ms: 1.55x slower                                                |
| 2to3                     | 264 ms                                                 | 410 ms: 1.55x slower                                                |
| sympy_integrate          | 20.5 ms                                                | 32.2 ms: 1.57x slower                                               |
| python_startup           | 9.93 ms                                                | 15.7 ms: 1.58x slower                                               |
| genshi_xml               | 50.2 ms                                                | 80.6 ms: 1.61x slower                                               |
| sqlglot_normalize        | 107 ms                                                 | 172 ms: 1.61x slower                                                |
| thrift                   | 791 us                                                 | 1.28 ms: 1.61x slower                                               |
| html5lib                 | 63.6 ms                                                | 103 ms: 1.62x slower                                                |
| sqlglot_optimize         | 53.3 ms                                                | 86.6 ms: 1.63x slower                                               |
| pyflate                  | 448 ms                                                 | 744 ms: 1.66x slower                                                |
| pprint_safe_repr         | 743 ms                                                 | 1.26 sec: 1.69x slower                                              |
| pprint_pformat           | 1.52 sec                                               | 2.61 sec: 1.72x slower                                              |
| genshi_text              | 22.8 ms                                                | 39.2 ms: 1.72x slower                                               |
| unpickle_pure_python     | 221 us                                                 | 386 us: 1.75x slower                                                |
| mako                     | 11.0 ms                                                | 19.3 ms: 1.75x slower                                               |
| django_template          | 34.7 ms                                                | 62.1 ms: 1.79x slower                                               |
| scimark_monte_carlo      | 68.4 ms                                                | 123 ms: 1.79x slower                                                |
| logging_format           | 7.35 us                                                | 13.2 us: 1.80x slower                                               |
| float                    | 80.8 ms                                                | 146 ms: 1.81x slower                                                |
| logging_simple           | 6.63 us                                                | 12.1 us: 1.82x slower                                               |
| sympy_str                | 292 ms                                                 | 531 ms: 1.82x slower                                                |
| richards                 | 45.9 ms                                                | 86.3 ms: 1.88x slower                                               |
| chaos                    | 62.8 ms                                                | 119 ms: 1.89x slower                                                |
| pickle_pure_python       | 308 us                                                 | 584 us: 1.90x slower                                                |
| hexiom                   | 6.17 ms                                                | 11.7 ms: 1.90x slower                                               |
| logging_silent           | 109 ns                                                 | 209 ns: 1.92x slower                                                |
| sqlglot_transpile        | 1.67 ms                                                | 3.26 ms: 1.95x slower                                               |
| richards_super           | 51.9 ms                                                | 105 ms: 2.02x slower                                                |
| scimark_sor              | 130 ms                                                 | 263 ms: 2.03x slower                                                |
| scimark_lu               | 114 ms                                                 | 233 ms: 2.04x slower                                                |
| raytrace                 | 299 ms                                                 | 614 ms: 2.05x slower                                                |
| nbody                    | 89.3 ms                                                | 186 ms: 2.09x slower                                                |
| sqlglot_parse            | 1.36 ms                                                | 2.84 ms: 2.10x slower                                               |
| go                       | 139 ms                                                 | 296 ms: 2.13x slower                                                |
| sympy_expand             | 468 ms                                                 | 1.04 sec: 2.22x slower                                              |
| sympy_sum                | 166 ms                                                 | 379 ms: 2.28x slower                                                |
| deltablue                | 3.45 ms                                                | 8.76 ms: 2.54x slower                                               |
| unpack_sequence          | 52.1 ns                                                | 133 ns: 2.55x slower                                                |
| bench_thread_pool        | 941 us                                                 | 3.46 ms: 3.68x slower                                               |
| bench_mp_pool            | 10.8 ms                                                | 71.9 ms: 6.66x slower                                               |
| Geometric mean           | (ref)                                                  | 1.50x slower                                                        |

Benchmark hidden because not significant (2): pickle, pidigits
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.42x
- 95% likely to have a slowdown of 1.39x
- 99% likely to have a slowdown of 1.35x

# Memory
- memory change: 1.22x