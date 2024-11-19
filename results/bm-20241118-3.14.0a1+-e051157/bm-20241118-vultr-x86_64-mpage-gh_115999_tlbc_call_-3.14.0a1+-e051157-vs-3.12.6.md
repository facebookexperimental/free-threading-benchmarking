# Results vs. 3.12.6

- fork: mpage
- ref: gh_115999_tlbc_call_
- machine: linux-x86_64
- commit hash: e051157
- commit date: 2024-11-18
- overall geometric mean: 1.00x slower
- HPT reliability: 98.44%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a1+-e051157 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 255 ms: 1.03x faster                                                  |
| docutils       | 2.64 sec                                               | 2.62 sec: 1.01x faster                                                |
| html5lib       | 63.6 ms                                                | 65.3 ms: 1.03x slower                                                 |
| Geometric mean | (ref)                                                  | 1.01x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a1+-e051157 |
|--------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| coroutines         | 23.9 ms                                                | 22.7 ms: 1.05x faster                                                 |
| asyncio_tcp        | 519 ms                                                 | 505 ms: 1.03x faster                                                  |
| async_generators   | 384 ms                                                 | 378 ms: 1.02x faster                                                  |
| asyncio_websockets | 517 ms                                                 | 520 ms: 1.01x slower                                                  |
| asyncio_tcp_ssl    | 1.51 sec                                               | 1.52 sec: 1.01x slower                                                |
| Geometric mean     | (ref)                                                  | 1.02x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a1+-e051157 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 79.2 ms: 1.02x faster                                                 |
| nbody          | 89.3 ms                                                | 92.5 ms: 1.04x slower                                                 |
| pidigits       | 184 ms                                                 | 223 ms: 1.21x slower                                                  |
| Geometric mean | (ref)                                                  | 1.07x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a1+-e051157 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 130 ms: 1.10x faster                                                  |
| regex_effbot   | 3.17 ms                                                | 3.27 ms: 1.03x slower                                                 |
| regex_dna      | 168 ms                                                 | 183 ms: 1.09x slower                                                  |
| regex_v8       | 20.6 ms                                                | 22.9 ms: 1.11x slower                                                 |
| Geometric mean | (ref)                                                  | 1.03x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a1+-e051157 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_loads           | 26.5 us                                                | 24.9 us: 1.06x faster                                                 |
| unpickle             | 14.1 us                                                | 13.7 us: 1.03x faster                                                 |
| unpickle_pure_python | 221 us                                                 | 215 us: 1.02x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 137 ms: 1.01x faster                                                  |
| xml_etree_generate   | 85.2 ms                                                | 84.5 ms: 1.01x faster                                                 |
| xml_etree_iterparse  | 96.7 ms                                                | 96.1 ms: 1.01x faster                                                 |
| unpickle_list        | 4.67 us                                                | 4.75 us: 1.02x slower                                                 |
| pickle_dict          | 31.8 us                                                | 32.3 us: 1.02x slower                                                 |
| pickle_pure_python   | 308 us                                                 | 314 us: 1.02x slower                                                  |
| pickle_list          | 4.77 us                                                | 5.13 us: 1.08x slower                                                 |
| json_dumps           | 10.4 ms                                                | 11.5 ms: 1.11x slower                                                 |
| pickle               | 10.9 us                                                | 12.3 us: 1.12x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.01x slower                                                          |

Benchmark hidden because not significant (2): xml_etree_process, tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a1+-e051157 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.51 ms: 1.05x slower                                                 |
| python_startup         | 9.93 ms                                                | 11.2 ms: 1.12x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.09x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a1+-e051157 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 22.3 ms: 1.02x faster                                                 |
| django_template | 34.7 ms                                                | 35.7 ms: 1.03x slower                                                 |
| mako            | 11.0 ms                                                | 11.6 ms: 1.05x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.02x slower                                                          |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a1+-e051157 |
|--------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| deepcopy_memo            | 40.3 us                                                | 29.6 us: 1.36x faster                                                 |
| deepcopy                 | 352 us                                                 | 263 us: 1.34x faster                                                  |
| pathlib                  | 21.5 ms                                                | 18.3 ms: 1.18x faster                                                 |
| comprehensions           | 19.8 us                                                | 17.0 us: 1.17x faster                                                 |
| deepcopy_reduce          | 3.08 us                                                | 2.66 us: 1.16x faster                                                 |
| go                       | 139 ms                                                 | 122 ms: 1.14x faster                                                  |
| raytrace                 | 299 ms                                                 | 262 ms: 1.14x faster                                                  |
| crypto_pyaes             | 76.6 ms                                                | 68.0 ms: 1.13x faster                                                 |
| generators               | 32.2 ms                                                | 28.9 ms: 1.11x faster                                                 |
| regex_compile            | 142 ms                                                 | 130 ms: 1.10x faster                                                  |
| json                     | 5.02 ms                                                | 4.60 ms: 1.09x faster                                                 |
| bpe_tokeniser            | 4.74 sec                                               | 4.35 sec: 1.09x faster                                                |
| sympy_sum                | 166 ms                                                 | 153 ms: 1.08x faster                                                  |
| unpack_sequence          | 52.1 ns                                                | 48.4 ns: 1.08x faster                                                 |
| chaos                    | 62.8 ms                                                | 58.6 ms: 1.07x faster                                                 |
| deltablue                | 3.45 ms                                                | 3.22 ms: 1.07x faster                                                 |
| logging_simple           | 6.63 us                                                | 6.21 us: 1.07x faster                                                 |
| sympy_str                | 292 ms                                                 | 273 ms: 1.07x faster                                                  |
| json_loads               | 26.5 us                                                | 24.9 us: 1.06x faster                                                 |
| thrift                   | 791 us                                                 | 747 us: 1.06x faster                                                  |
| logging_format           | 7.35 us                                                | 6.93 us: 1.06x faster                                                 |
| logging_silent           | 109 ns                                                 | 103 ns: 1.06x faster                                                  |
| coroutines               | 23.9 ms                                                | 22.7 ms: 1.05x faster                                                 |
| dulwich_log              | 78.9 ms                                                | 75.5 ms: 1.04x faster                                                 |
| scimark_monte_carlo      | 68.4 ms                                                | 65.6 ms: 1.04x faster                                                 |
| hexiom                   | 6.17 ms                                                | 5.93 ms: 1.04x faster                                                 |
| typing_runtime_protocols | 163 us                                                 | 157 us: 1.04x faster                                                  |
| sqlglot_parse            | 1.36 ms                                                | 1.30 ms: 1.04x faster                                                 |
| sqlglot_transpile        | 1.67 ms                                                | 1.61 ms: 1.04x faster                                                 |
| pprint_safe_repr         | 743 ms                                                 | 716 ms: 1.04x faster                                                  |
| pprint_pformat           | 1.52 sec                                               | 1.47 sec: 1.04x faster                                                |
| 2to3                     | 264 ms                                                 | 255 ms: 1.03x faster                                                  |
| sympy_integrate          | 20.5 ms                                                | 19.9 ms: 1.03x faster                                                 |
| meteor_contest           | 104 ms                                                 | 100 ms: 1.03x faster                                                  |
| pycparser                | 1.17 sec                                               | 1.14 sec: 1.03x faster                                                |
| unpickle                 | 14.1 us                                                | 13.7 us: 1.03x faster                                                 |
| mdp                      | 2.42 sec                                               | 2.35 sec: 1.03x faster                                                |
| asyncio_tcp              | 519 ms                                                 | 505 ms: 1.03x faster                                                  |
| unpickle_pure_python     | 221 us                                                 | 215 us: 1.02x faster                                                  |
| genshi_text              | 22.8 ms                                                | 22.3 ms: 1.02x faster                                                 |
| float                    | 80.8 ms                                                | 79.2 ms: 1.02x faster                                                 |
| nqueens                  | 80.1 ms                                                | 78.5 ms: 1.02x faster                                                 |
| gc_traversal             | 3.46 ms                                                | 3.39 ms: 1.02x faster                                                 |
| async_generators         | 384 ms                                                 | 378 ms: 1.02x faster                                                  |
| xml_etree_parse          | 139 ms                                                 | 137 ms: 1.01x faster                                                  |
| richards                 | 45.9 ms                                                | 45.4 ms: 1.01x faster                                                 |
| docutils                 | 2.64 sec                                               | 2.62 sec: 1.01x faster                                                |
| xml_etree_generate       | 85.2 ms                                                | 84.5 ms: 1.01x faster                                                 |
| sympy_expand             | 468 ms                                                 | 464 ms: 1.01x faster                                                  |
| xml_etree_iterparse      | 96.7 ms                                                | 96.1 ms: 1.01x faster                                                 |
| scimark_fft              | 342 ms                                                 | 340 ms: 1.01x faster                                                  |
| spectral_norm            | 110 ms                                                 | 110 ms: 1.00x faster                                                  |
| sqlglot_normalize        | 107 ms                                                 | 107 ms: 1.00x slower                                                  |
| fannkuch                 | 372 ms                                                 | 374 ms: 1.00x slower                                                  |
| asyncio_websockets       | 517 ms                                                 | 520 ms: 1.01x slower                                                  |
| scimark_lu               | 114 ms                                                 | 115 ms: 1.01x slower                                                  |
| sqlglot_optimize         | 53.3 ms                                                | 53.7 ms: 1.01x slower                                                 |
| asyncio_tcp_ssl          | 1.51 sec                                               | 1.52 sec: 1.01x slower                                                |
| pyflate                  | 448 ms                                                 | 452 ms: 1.01x slower                                                  |
| unpickle_list            | 4.67 us                                                | 4.75 us: 1.02x slower                                                 |
| pickle_dict              | 31.8 us                                                | 32.3 us: 1.02x slower                                                 |
| pickle_pure_python       | 308 us                                                 | 314 us: 1.02x slower                                                  |
| html5lib                 | 63.6 ms                                                | 65.3 ms: 1.03x slower                                                 |
| django_template          | 34.7 ms                                                | 35.7 ms: 1.03x slower                                                 |
| regex_effbot             | 3.17 ms                                                | 3.27 ms: 1.03x slower                                                 |
| nbody                    | 89.3 ms                                                | 92.5 ms: 1.04x slower                                                 |
| scimark_sor              | 130 ms                                                 | 136 ms: 1.05x slower                                                  |
| python_startup_no_site   | 7.16 ms                                                | 7.51 ms: 1.05x slower                                                 |
| mako                     | 11.0 ms                                                | 11.6 ms: 1.05x slower                                                 |
| scimark_sparse_mat_mult  | 4.39 ms                                                | 4.69 ms: 1.07x slower                                                 |
| bench_thread_pool        | 941 us                                                 | 1.01 ms: 1.08x slower                                                 |
| pickle_list              | 4.77 us                                                | 5.13 us: 1.08x slower                                                 |
| regex_dna                | 168 ms                                                 | 183 ms: 1.09x slower                                                  |
| json_dumps               | 10.4 ms                                                | 11.5 ms: 1.11x slower                                                 |
| telco                    | 6.53 ms                                                | 7.25 ms: 1.11x slower                                                 |
| regex_v8                 | 20.6 ms                                                | 22.9 ms: 1.11x slower                                                 |
| pickle                   | 10.9 us                                                | 12.3 us: 1.12x slower                                                 |
| python_startup           | 9.93 ms                                                | 11.2 ms: 1.12x slower                                                 |
| coverage                 | 71.4 ms                                                | 81.3 ms: 1.14x slower                                                 |
| pidigits                 | 184 ms                                                 | 223 ms: 1.21x slower                                                  |
| create_gc_cycles         | 1.09 ms                                                | 1.37 ms: 1.26x slower                                                 |
| bench_mp_pool            | 10.8 ms                                                | 64.3 ms: 5.95x slower                                                 |
| Geometric mean           | (ref)                                                  | 1.00x slower                                                          |

Benchmark hidden because not significant (6): richards_super, sqlite_synth, pylint, xml_etree_process, genshi_xml, tomli_loads
Ignored benchmarks (17) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http

# HPT report

- Reliability score: 98.44% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.02x