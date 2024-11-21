# Results vs. 3.12.6

- fork: mpage
- ref: gh_115999_tlbc_call
- machine: linux-x86_64
- commit hash: 8ebd73d
- commit date: 2024-11-20
- overall geometric mean: 1.00x slower
- HPT reliability: 90.85%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241120-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-8ebd73d |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 255 ms: 1.03x faster                                                 |
| docutils       | 2.64 sec                                               | 2.59 sec: 1.02x faster                                               |
| html5lib       | 63.6 ms                                                | 64.9 ms: 1.02x slower                                                |
| Geometric mean | (ref)                                                  | 1.01x faster                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241120-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-8ebd73d |
|--------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| coroutines         | 23.9 ms                                                | 23.1 ms: 1.03x faster                                                |
| asyncio_tcp        | 519 ms                                                 | 504 ms: 1.03x faster                                                 |
| asyncio_websockets | 517 ms                                                 | 521 ms: 1.01x slower                                                 |
| asyncio_tcp_ssl    | 1.51 sec                                               | 1.53 sec: 1.01x slower                                               |
| Geometric mean     | (ref)                                                  | 1.01x faster                                                         |

Benchmark hidden because not significant (1): async_generators

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241120-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-8ebd73d |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 79.8 ms: 1.01x faster                                                |
| pidigits       | 184 ms                                                 | 186 ms: 1.01x slower                                                 |
| nbody          | 89.3 ms                                                | 95.2 ms: 1.07x slower                                                |
| Geometric mean | (ref)                                                  | 1.02x slower                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241120-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-8ebd73d |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.70 ms: 1.17x faster                                                |
| regex_compile  | 142 ms                                                 | 130 ms: 1.09x faster                                                 |
| regex_dna      | 168 ms                                                 | 177 ms: 1.06x slower                                                 |
| regex_v8       | 20.6 ms                                                | 22.7 ms: 1.10x slower                                                |
| Geometric mean | (ref)                                                  | 1.02x faster                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241120-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-8ebd73d |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| json_loads           | 26.5 us                                                | 25.0 us: 1.06x faster                                                |
| pickle_dict          | 31.8 us                                                | 31.0 us: 1.02x faster                                                |
| unpickle_pure_python | 221 us                                                 | 216 us: 1.02x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 137 ms: 1.02x faster                                                 |
| xml_etree_generate   | 85.2 ms                                                | 84.8 ms: 1.01x faster                                                |
| xml_etree_process    | 59.0 ms                                                | 59.4 ms: 1.01x slower                                                |
| tomli_loads          | 2.11 sec                                               | 2.13 sec: 1.01x slower                                               |
| pickle_pure_python   | 308 us                                                 | 314 us: 1.02x slower                                                 |
| pickle_list          | 4.77 us                                                | 5.02 us: 1.05x slower                                                |
| json_dumps           | 10.4 ms                                                | 11.4 ms: 1.10x slower                                                |
| pickle               | 10.9 us                                                | 12.4 us: 1.13x slower                                                |
| Geometric mean       | (ref)                                                  | 1.01x slower                                                         |

Benchmark hidden because not significant (3): unpickle, xml_etree_iterparse, unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241120-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-8ebd73d |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.42 ms: 1.04x slower                                                |
| python_startup         | 9.93 ms                                                | 11.1 ms: 1.12x slower                                                |
| Geometric mean         | (ref)                                                  | 1.08x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241120-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-8ebd73d |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 22.4 ms: 1.02x faster                                                |
| genshi_xml      | 50.2 ms                                                | 50.6 ms: 1.01x slower                                                |
| django_template | 34.7 ms                                                | 35.3 ms: 1.02x slower                                                |
| mako            | 11.0 ms                                                | 11.8 ms: 1.07x slower                                                |
| Geometric mean  | (ref)                                                  | 1.02x slower                                                         |

All benchmarks:
===============

| Benchmark                | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241120-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-8ebd73d |
|--------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| deepcopy                 | 352 us                                                 | 264 us: 1.33x faster                                                 |
| deepcopy_memo            | 40.3 us                                                | 30.8 us: 1.31x faster                                                |
| pylint                   | 319 ms                                                 | 270 ms: 1.18x faster                                                 |
| pathlib                  | 21.5 ms                                                | 18.3 ms: 1.17x faster                                                |
| regex_effbot             | 3.17 ms                                                | 2.70 ms: 1.17x faster                                                |
| go                       | 139 ms                                                 | 121 ms: 1.16x faster                                                 |
| deepcopy_reduce          | 3.08 us                                                | 2.67 us: 1.15x faster                                                |
| comprehensions           | 19.8 us                                                | 17.2 us: 1.15x faster                                                |
| raytrace                 | 299 ms                                                 | 264 ms: 1.13x faster                                                 |
| crypto_pyaes             | 76.6 ms                                                | 68.0 ms: 1.13x faster                                                |
| unpack_sequence          | 52.1 ns                                                | 46.8 ns: 1.11x faster                                                |
| regex_compile            | 142 ms                                                 | 130 ms: 1.09x faster                                                 |
| generators               | 32.2 ms                                                | 29.6 ms: 1.09x faster                                                |
| sympy_sum                | 166 ms                                                 | 153 ms: 1.09x faster                                                 |
| logging_format           | 7.35 us                                                | 6.79 us: 1.08x faster                                                |
| json                     | 5.02 ms                                                | 4.66 ms: 1.08x faster                                                |
| bpe_tokeniser            | 4.74 sec                                               | 4.40 sec: 1.08x faster                                               |
| chaos                    | 62.8 ms                                                | 58.3 ms: 1.08x faster                                                |
| logging_simple           | 6.63 us                                                | 6.16 us: 1.08x faster                                                |
| sympy_str                | 292 ms                                                 | 273 ms: 1.07x faster                                                 |
| json_loads               | 26.5 us                                                | 25.0 us: 1.06x faster                                                |
| thrift                   | 791 us                                                 | 747 us: 1.06x faster                                                 |
| scimark_monte_carlo      | 68.4 ms                                                | 65.4 ms: 1.05x faster                                                |
| sqlglot_parse            | 1.36 ms                                                | 1.30 ms: 1.04x faster                                                |
| sqlglot_transpile        | 1.67 ms                                                | 1.60 ms: 1.04x faster                                                |
| dulwich_log              | 78.9 ms                                                | 75.8 ms: 1.04x faster                                                |
| coroutines               | 23.9 ms                                                | 23.1 ms: 1.03x faster                                                |
| 2to3                     | 264 ms                                                 | 255 ms: 1.03x faster                                                 |
| typing_runtime_protocols | 163 us                                                 | 158 us: 1.03x faster                                                 |
| sympy_integrate          | 20.5 ms                                                | 19.9 ms: 1.03x faster                                                |
| asyncio_tcp              | 519 ms                                                 | 504 ms: 1.03x faster                                                 |
| pycparser                | 1.17 sec                                               | 1.14 sec: 1.03x faster                                               |
| meteor_contest           | 104 ms                                                 | 101 ms: 1.03x faster                                                 |
| pprint_safe_repr         | 743 ms                                                 | 723 ms: 1.03x faster                                                 |
| hexiom                   | 6.17 ms                                                | 6.02 ms: 1.03x faster                                                |
| pickle_dict              | 31.8 us                                                | 31.0 us: 1.02x faster                                                |
| genshi_text              | 22.8 ms                                                | 22.4 ms: 1.02x faster                                                |
| gc_traversal             | 3.46 ms                                                | 3.39 ms: 1.02x faster                                                |
| unpickle_pure_python     | 221 us                                                 | 216 us: 1.02x faster                                                 |
| pprint_pformat           | 1.52 sec                                               | 1.49 sec: 1.02x faster                                               |
| scimark_lu               | 114 ms                                                 | 112 ms: 1.02x faster                                                 |
| docutils                 | 2.64 sec                                               | 2.59 sec: 1.02x faster                                               |
| nqueens                  | 80.1 ms                                                | 78.8 ms: 1.02x faster                                                |
| xml_etree_parse          | 139 ms                                                 | 137 ms: 1.02x faster                                                 |
| sympy_expand             | 468 ms                                                 | 461 ms: 1.01x faster                                                 |
| float                    | 80.8 ms                                                | 79.8 ms: 1.01x faster                                                |
| scimark_fft              | 342 ms                                                 | 337 ms: 1.01x faster                                                 |
| xml_etree_generate       | 85.2 ms                                                | 84.8 ms: 1.01x faster                                                |
| sqlglot_normalize        | 107 ms                                                 | 107 ms: 1.01x slower                                                 |
| xml_etree_process        | 59.0 ms                                                | 59.4 ms: 1.01x slower                                                |
| asyncio_websockets       | 517 ms                                                 | 521 ms: 1.01x slower                                                 |
| genshi_xml               | 50.2 ms                                                | 50.6 ms: 1.01x slower                                                |
| pidigits                 | 184 ms                                                 | 186 ms: 1.01x slower                                                 |
| fannkuch                 | 372 ms                                                 | 376 ms: 1.01x slower                                                 |
| pyflate                  | 448 ms                                                 | 452 ms: 1.01x slower                                                 |
| sqlglot_optimize         | 53.3 ms                                                | 53.9 ms: 1.01x slower                                                |
| asyncio_tcp_ssl          | 1.51 sec                                               | 1.53 sec: 1.01x slower                                               |
| tomli_loads              | 2.11 sec                                               | 2.13 sec: 1.01x slower                                               |
| django_template          | 34.7 ms                                                | 35.3 ms: 1.02x slower                                                |
| pickle_pure_python       | 308 us                                                 | 314 us: 1.02x slower                                                 |
| html5lib                 | 63.6 ms                                                | 64.9 ms: 1.02x slower                                                |
| mdp                      | 2.42 sec                                               | 2.51 sec: 1.04x slower                                               |
| python_startup_no_site   | 7.16 ms                                                | 7.42 ms: 1.04x slower                                                |
| spectral_norm            | 110 ms                                                 | 115 ms: 1.05x slower                                                 |
| scimark_sparse_mat_mult  | 4.39 ms                                                | 4.62 ms: 1.05x slower                                                |
| pickle_list              | 4.77 us                                                | 5.02 us: 1.05x slower                                                |
| scimark_sor              | 130 ms                                                 | 137 ms: 1.06x slower                                                 |
| regex_dna                | 168 ms                                                 | 177 ms: 1.06x slower                                                 |
| nbody                    | 89.3 ms                                                | 95.2 ms: 1.07x slower                                                |
| mako                     | 11.0 ms                                                | 11.8 ms: 1.07x slower                                                |
| bench_thread_pool        | 941 us                                                 | 1.02 ms: 1.08x slower                                                |
| json_dumps               | 10.4 ms                                                | 11.4 ms: 1.10x slower                                                |
| regex_v8                 | 20.6 ms                                                | 22.7 ms: 1.10x slower                                                |
| python_startup           | 9.93 ms                                                | 11.1 ms: 1.12x slower                                                |
| telco                    | 6.53 ms                                                | 7.29 ms: 1.12x slower                                                |
| pickle                   | 10.9 us                                                | 12.4 us: 1.13x slower                                                |
| coverage                 | 71.4 ms                                                | 81.7 ms: 1.14x slower                                                |
| create_gc_cycles         | 1.09 ms                                                | 1.36 ms: 1.24x slower                                                |
| bench_mp_pool            | 10.8 ms                                                | 63.5 ms: 5.88x slower                                                |
| Geometric mean           | (ref)                                                  | 1.00x slower                                                         |

Benchmark hidden because not significant (9): unpickle, xml_etree_iterparse, richards, deltablue, unpickle_list, async_generators, richards_super, sqlite_synth, logging_silent
Ignored benchmarks (17) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http

# HPT report

- Reliability score: 90.85% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.02x