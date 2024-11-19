# Results vs. 3.12.6

- fork: mpage
- ref: gh_115999_tlbc_call_
- machine: linux-x86_64
- commit hash: e051157
- commit date: 2024-11-18
- overall geometric mean: 1.55x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.38x slower
- Memory change: 1.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a1+-e051157 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 417 ms: 1.58x slower                                                  |
| docutils       | 2.64 sec                                               | 3.38 sec: 1.28x slower                                                |
| html5lib       | 63.6 ms                                                | 105 ms: 1.65x slower                                                  |
| Geometric mean | (ref)                                                  | 1.50x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a1+-e051157 |
|------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| asyncio_tcp      | 519 ms                                                 | 584 ms: 1.13x slower                                                  |
| asyncio_tcp_ssl  | 1.51 sec                                               | 1.82 sec: 1.21x slower                                                |
| async_generators | 384 ms                                                 | 490 ms: 1.28x slower                                                  |
| coroutines       | 23.9 ms                                                | 31.5 ms: 1.32x slower                                                 |
| Geometric mean   | (ref)                                                  | 1.18x slower                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a1+-e051157 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 185 ms: 1.00x slower                                                  |
| float          | 80.8 ms                                                | 153 ms: 1.89x slower                                                  |
| nbody          | 89.3 ms                                                | 205 ms: 2.30x slower                                                  |
| Geometric mean | (ref)                                                  | 1.63x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a1+-e051157 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.99 ms: 1.06x faster                                                 |
| regex_dna      | 168 ms                                                 | 189 ms: 1.13x slower                                                  |
| regex_v8       | 20.6 ms                                                | 24.7 ms: 1.20x slower                                                 |
| regex_compile  | 142 ms                                                 | 229 ms: 1.61x slower                                                  |
| Geometric mean | (ref)                                                  | 1.20x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a1+-e051157 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 135 ms: 1.03x faster                                                  |
| pickle_dict          | 31.8 us                                                | 32.0 us: 1.01x slower                                                 |
| unpickle             | 14.1 us                                                | 14.6 us: 1.04x slower                                                 |
| json_loads           | 26.5 us                                                | 28.6 us: 1.08x slower                                                 |
| unpickle_list        | 4.67 us                                                | 5.06 us: 1.08x slower                                                 |
| pickle_list          | 4.77 us                                                | 5.23 us: 1.10x slower                                                 |
| xml_etree_iterparse  | 96.7 ms                                                | 109 ms: 1.13x slower                                                  |
| pickle               | 10.9 us                                                | 13.5 us: 1.23x slower                                                 |
| xml_etree_generate   | 85.2 ms                                                | 113 ms: 1.33x slower                                                  |
| json_dumps           | 10.4 ms                                                | 15.3 ms: 1.48x slower                                                 |
| tomli_loads          | 2.11 sec                                               | 3.24 sec: 1.54x slower                                                |
| xml_etree_process    | 59.0 ms                                                | 93.4 ms: 1.58x slower                                                 |
| unpickle_pure_python | 221 us                                                 | 423 us: 1.92x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 622 us: 2.02x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.29x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a1+-e051157 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.3 ms: 1.43x slower                                                 |
| python_startup         | 9.93 ms                                                | 15.7 ms: 1.58x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.51x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a1+-e051157 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 82.9 ms: 1.65x slower                                                 |
| genshi_text     | 22.8 ms                                                | 41.0 ms: 1.80x slower                                                 |
| django_template | 34.7 ms                                                | 64.9 ms: 1.87x slower                                                 |
| mako            | 11.0 ms                                                | 20.8 ms: 1.89x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.80x slower                                                          |

All benchmarks:
===============

| Benchmark                | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a1+-e051157 |
|--------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal             | 3.46 ms                                                | 2.38 ms: 1.45x faster                                                 |
| regex_effbot             | 3.17 ms                                                | 2.99 ms: 1.06x faster                                                 |
| xml_etree_parse          | 139 ms                                                 | 135 ms: 1.03x faster                                                  |
| pidigits                 | 184 ms                                                 | 185 ms: 1.00x slower                                                  |
| pickle_dict              | 31.8 us                                                | 32.0 us: 1.01x slower                                                 |
| pathlib                  | 21.5 ms                                                | 21.7 ms: 1.01x slower                                                 |
| unpickle                 | 14.1 us                                                | 14.6 us: 1.04x slower                                                 |
| create_gc_cycles         | 1.09 ms                                                | 1.15 ms: 1.05x slower                                                 |
| json                     | 5.02 ms                                                | 5.30 ms: 1.05x slower                                                 |
| json_loads               | 26.5 us                                                | 28.6 us: 1.08x slower                                                 |
| unpickle_list            | 4.67 us                                                | 5.06 us: 1.08x slower                                                 |
| pickle_list              | 4.77 us                                                | 5.23 us: 1.10x slower                                                 |
| sqlite_synth             | 2.20 us                                                | 2.47 us: 1.12x slower                                                 |
| regex_dna                | 168 ms                                                 | 189 ms: 1.13x slower                                                  |
| asyncio_tcp              | 519 ms                                                 | 584 ms: 1.13x slower                                                  |
| xml_etree_iterparse      | 96.7 ms                                                | 109 ms: 1.13x slower                                                  |
| regex_v8                 | 20.6 ms                                                | 24.7 ms: 1.20x slower                                                 |
| asyncio_tcp_ssl          | 1.51 sec                                               | 1.82 sec: 1.21x slower                                                |
| deepcopy                 | 352 us                                                 | 433 us: 1.23x slower                                                  |
| pickle                   | 10.9 us                                                | 13.5 us: 1.23x slower                                                 |
| scimark_fft              | 342 ms                                                 | 425 ms: 1.25x slower                                                  |
| async_generators         | 384 ms                                                 | 490 ms: 1.28x slower                                                  |
| docutils                 | 2.64 sec                                               | 3.38 sec: 1.28x slower                                                |
| generators               | 32.2 ms                                                | 41.5 ms: 1.29x slower                                                 |
| bpe_tokeniser            | 4.74 sec                                               | 6.16 sec: 1.30x slower                                                |
| mdp                      | 2.42 sec                                               | 3.16 sec: 1.31x slower                                                |
| coroutines               | 23.9 ms                                                | 31.5 ms: 1.32x slower                                                 |
| meteor_contest           | 104 ms                                                 | 137 ms: 1.32x slower                                                  |
| pylint                   | 319 ms                                                 | 422 ms: 1.32x slower                                                  |
| dulwich_log              | 78.9 ms                                                | 105 ms: 1.33x slower                                                  |
| deepcopy_memo            | 40.3 us                                                | 53.6 us: 1.33x slower                                                 |
| xml_etree_generate       | 85.2 ms                                                | 113 ms: 1.33x slower                                                  |
| scimark_sparse_mat_mult  | 4.39 ms                                                | 6.05 ms: 1.38x slower                                                 |
| crypto_pyaes             | 76.6 ms                                                | 109 ms: 1.42x slower                                                  |
| telco                    | 6.53 ms                                                | 9.29 ms: 1.42x slower                                                 |
| coverage                 | 71.4 ms                                                | 102 ms: 1.43x slower                                                  |
| python_startup_no_site   | 7.16 ms                                                | 10.3 ms: 1.43x slower                                                 |
| spectral_norm            | 110 ms                                                 | 159 ms: 1.45x slower                                                  |
| nqueens                  | 80.1 ms                                                | 116 ms: 1.45x slower                                                  |
| json_dumps               | 10.4 ms                                                | 15.3 ms: 1.48x slower                                                 |
| pycparser                | 1.17 sec                                               | 1.73 sec: 1.48x slower                                                |
| deepcopy_reduce          | 3.08 us                                                | 4.59 us: 1.49x slower                                                 |
| fannkuch                 | 372 ms                                                 | 564 ms: 1.52x slower                                                  |
| tomli_loads              | 2.11 sec                                               | 3.24 sec: 1.54x slower                                                |
| typing_runtime_protocols | 163 us                                                 | 252 us: 1.54x slower                                                  |
| comprehensions           | 19.8 us                                                | 30.6 us: 1.54x slower                                                 |
| xml_etree_process        | 59.0 ms                                                | 93.4 ms: 1.58x slower                                                 |
| python_startup           | 9.93 ms                                                | 15.7 ms: 1.58x slower                                                 |
| 2to3                     | 264 ms                                                 | 417 ms: 1.58x slower                                                  |
| regex_compile            | 142 ms                                                 | 229 ms: 1.61x slower                                                  |
| sympy_integrate          | 20.5 ms                                                | 33.3 ms: 1.62x slower                                                 |
| thrift                   | 791 us                                                 | 1.30 ms: 1.64x slower                                                 |
| html5lib                 | 63.6 ms                                                | 105 ms: 1.65x slower                                                  |
| genshi_xml               | 50.2 ms                                                | 82.9 ms: 1.65x slower                                                 |
| sqlglot_normalize        | 107 ms                                                 | 182 ms: 1.71x slower                                                  |
| sqlglot_optimize         | 53.3 ms                                                | 91.3 ms: 1.71x slower                                                 |
| pyflate                  | 448 ms                                                 | 786 ms: 1.75x slower                                                  |
| pprint_safe_repr         | 743 ms                                                 | 1.33 sec: 1.79x slower                                                |
| genshi_text              | 22.8 ms                                                | 41.0 ms: 1.80x slower                                                 |
| pprint_pformat           | 1.52 sec                                               | 2.77 sec: 1.82x slower                                                |
| logging_simple           | 6.63 us                                                | 12.2 us: 1.84x slower                                                 |
| logging_format           | 7.35 us                                                | 13.6 us: 1.85x slower                                                 |
| sympy_str                | 292 ms                                                 | 543 ms: 1.86x slower                                                  |
| django_template          | 34.7 ms                                                | 64.9 ms: 1.87x slower                                                 |
| float                    | 80.8 ms                                                | 153 ms: 1.89x slower                                                  |
| scimark_monte_carlo      | 68.4 ms                                                | 130 ms: 1.89x slower                                                  |
| mako                     | 11.0 ms                                                | 20.8 ms: 1.89x slower                                                 |
| unpickle_pure_python     | 221 us                                                 | 423 us: 1.92x slower                                                  |
| chaos                    | 62.8 ms                                                | 124 ms: 1.97x slower                                                  |
| logging_silent           | 109 ns                                                 | 216 ns: 1.98x slower                                                  |
| sqlglot_transpile        | 1.67 ms                                                | 3.33 ms: 1.99x slower                                                 |
| richards                 | 45.9 ms                                                | 91.6 ms: 1.99x slower                                                 |
| pickle_pure_python       | 308 us                                                 | 622 us: 2.02x slower                                                  |
| hexiom                   | 6.17 ms                                                | 12.5 ms: 2.02x slower                                                 |
| scimark_sor              | 130 ms                                                 | 270 ms: 2.08x slower                                                  |
| sqlglot_parse            | 1.36 ms                                                | 2.88 ms: 2.12x slower                                                 |
| raytrace                 | 299 ms                                                 | 647 ms: 2.16x slower                                                  |
| go                       | 139 ms                                                 | 301 ms: 2.16x slower                                                  |
| scimark_lu               | 114 ms                                                 | 248 ms: 2.18x slower                                                  |
| richards_super           | 51.9 ms                                                | 113 ms: 2.18x slower                                                  |
| sympy_expand             | 468 ms                                                 | 1.06 sec: 2.27x slower                                                |
| sympy_sum                | 166 ms                                                 | 382 ms: 2.30x slower                                                  |
| nbody                    | 89.3 ms                                                | 205 ms: 2.30x slower                                                  |
| deltablue                | 3.45 ms                                                | 9.26 ms: 2.69x slower                                                 |
| unpack_sequence          | 52.1 ns                                                | 142 ns: 2.73x slower                                                  |
| bench_thread_pool        | 941 us                                                 | 3.49 ms: 3.71x slower                                                 |
| bench_mp_pool            | 10.8 ms                                                | 72.7 ms: 6.73x slower                                                 |
| Geometric mean           | (ref)                                                  | 1.55x slower                                                          |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (17) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.45x
- 95% likely to have a slowdown of 1.44x
- 99% likely to have a slowdown of 1.38x

# Memory
- memory change: 1.23x