# Results vs. 3.12.6

- fork: mpage
- ref: gh_115999_tlbc_call
- machine: linux-x86_64
- commit hash: 39a19e1
- commit date: 2024-10-24
- overall geometric mean: 1.49x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.34x slower
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241024-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-39a19e1 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 408 ms: 1.55x slower                                                |
| docutils       | 2.64 sec                                               | 3.25 sec: 1.23x slower                                              |
| html5lib       | 63.6 ms                                                | 102 ms: 1.60x slower                                                |
| tornado_http   | 119 ms                                                 | 161 ms: 1.35x slower                                                |
| Geometric mean | (ref)                                                  | 1.42x slower                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241024-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-39a19e1 |
|--------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| asyncio_websockets | 517 ms                                                 | 520 ms: 1.01x slower                                                |
| asyncio_tcp        | 519 ms                                                 | 581 ms: 1.12x slower                                                |
| coroutines         | 23.9 ms                                                | 28.7 ms: 1.20x slower                                               |
| asyncio_tcp_ssl    | 1.51 sec                                               | 1.83 sec: 1.21x slower                                              |
| async_generators   | 384 ms                                                 | 487 ms: 1.27x slower                                                |
| Geometric mean     | (ref)                                                  | 1.16x slower                                                        |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241024-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-39a19e1 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 223 ms: 1.21x slower                                                |
| float          | 80.8 ms                                                | 146 ms: 1.81x slower                                                |
| nbody          | 89.3 ms                                                | 187 ms: 2.10x slower                                                |
| Geometric mean | (ref)                                                  | 1.66x slower                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241024-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-39a19e1 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 3.05 ms: 1.04x faster                                               |
| regex_dna      | 168 ms                                                 | 191 ms: 1.14x slower                                                |
| regex_v8       | 20.6 ms                                                | 25.8 ms: 1.25x slower                                               |
| regex_compile  | 142 ms                                                 | 215 ms: 1.51x slower                                                |
| Geometric mean | (ref)                                                  | 1.20x slower                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241024-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-39a19e1 |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| pickle_dict          | 31.8 us                                                | 29.7 us: 1.07x faster                                               |
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.05x faster                                                |
| pickle_list          | 4.77 us                                                | 4.74 us: 1.01x faster                                               |
| unpickle             | 14.1 us                                                | 14.6 us: 1.04x slower                                               |
| pickle               | 10.9 us                                                | 11.4 us: 1.04x slower                                               |
| json_loads           | 26.5 us                                                | 28.2 us: 1.06x slower                                               |
| unpickle_list        | 4.67 us                                                | 5.07 us: 1.09x slower                                               |
| xml_etree_iterparse  | 96.7 ms                                                | 106 ms: 1.09x slower                                                |
| xml_etree_generate   | 85.2 ms                                                | 108 ms: 1.27x slower                                                |
| json_dumps           | 10.4 ms                                                | 15.1 ms: 1.46x slower                                               |
| xml_etree_process    | 59.0 ms                                                | 88.1 ms: 1.49x slower                                               |
| tomli_loads          | 2.11 sec                                               | 3.18 sec: 1.51x slower                                              |
| unpickle_pure_python | 221 us                                                 | 389 us: 1.76x slower                                                |
| pickle_pure_python   | 308 us                                                 | 572 us: 1.86x slower                                                |
| Geometric mean       | (ref)                                                  | 1.22x slower                                                        |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241024-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-39a19e1 |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.3 ms: 1.43x slower                                               |
| python_startup         | 9.93 ms                                                | 15.7 ms: 1.58x slower                                               |
| Geometric mean         | (ref)                                                  | 1.51x slower                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241024-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-39a19e1 |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 78.9 ms: 1.57x slower                                               |
| genshi_text     | 22.8 ms                                                | 38.8 ms: 1.70x slower                                               |
| mako            | 11.0 ms                                                | 19.2 ms: 1.74x slower                                               |
| django_template | 34.7 ms                                                | 62.3 ms: 1.80x slower                                               |
| Geometric mean  | (ref)                                                  | 1.70x slower                                                        |

All benchmarks:
===============

| Benchmark                | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241024-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-39a19e1 |
|--------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| gc_traversal             | 3.46 ms                                                | 2.48 ms: 1.40x faster                                               |
| pickle_dict              | 31.8 us                                                | 29.7 us: 1.07x faster                                               |
| xml_etree_parse          | 139 ms                                                 | 131 ms: 1.05x faster                                                |
| regex_effbot             | 3.17 ms                                                | 3.05 ms: 1.04x faster                                               |
| pickle_list              | 4.77 us                                                | 4.74 us: 1.01x faster                                               |
| asyncio_websockets       | 517 ms                                                 | 520 ms: 1.01x slower                                                |
| pathlib                  | 21.5 ms                                                | 21.6 ms: 1.01x slower                                               |
| json                     | 5.02 ms                                                | 5.20 ms: 1.04x slower                                               |
| create_gc_cycles         | 1.09 ms                                                | 1.13 ms: 1.04x slower                                               |
| unpickle                 | 14.1 us                                                | 14.6 us: 1.04x slower                                               |
| pickle                   | 10.9 us                                                | 11.4 us: 1.04x slower                                               |
| json_loads               | 26.5 us                                                | 28.2 us: 1.06x slower                                               |
| unpickle_list            | 4.67 us                                                | 5.07 us: 1.09x slower                                               |
| xml_etree_iterparse      | 96.7 ms                                                | 106 ms: 1.09x slower                                                |
| sqlite_synth             | 2.20 us                                                | 2.44 us: 1.11x slower                                               |
| asyncio_tcp              | 519 ms                                                 | 581 ms: 1.12x slower                                                |
| scimark_fft              | 342 ms                                                 | 387 ms: 1.13x slower                                                |
| regex_dna                | 168 ms                                                 | 191 ms: 1.14x slower                                                |
| deepcopy                 | 352 us                                                 | 411 us: 1.17x slower                                                |
| coroutines               | 23.9 ms                                                | 28.7 ms: 1.20x slower                                               |
| pidigits                 | 184 ms                                                 | 223 ms: 1.21x slower                                                |
| asyncio_tcp_ssl          | 1.51 sec                                               | 1.83 sec: 1.21x slower                                              |
| deepcopy_memo            | 40.3 us                                                | 49.1 us: 1.22x slower                                               |
| bpe_tokeniser            | 4.74 sec                                               | 5.79 sec: 1.22x slower                                              |
| docutils                 | 2.64 sec                                               | 3.25 sec: 1.23x slower                                              |
| regex_v8                 | 20.6 ms                                                | 25.8 ms: 1.25x slower                                               |
| async_generators         | 384 ms                                                 | 487 ms: 1.27x slower                                                |
| xml_etree_generate       | 85.2 ms                                                | 108 ms: 1.27x slower                                                |
| scimark_sparse_mat_mult  | 4.39 ms                                                | 5.61 ms: 1.28x slower                                               |
| dulwich_log              | 78.9 ms                                                | 101 ms: 1.28x slower                                                |
| pylint                   | 319 ms                                                 | 411 ms: 1.29x slower                                                |
| generators               | 32.2 ms                                                | 42.0 ms: 1.30x slower                                               |
| meteor_contest           | 104 ms                                                 | 137 ms: 1.32x slower                                                |
| mdp                      | 2.42 sec                                               | 3.21 sec: 1.33x slower                                              |
| spectral_norm            | 110 ms                                                 | 147 ms: 1.34x slower                                                |
| tornado_http             | 119 ms                                                 | 161 ms: 1.35x slower                                                |
| deepcopy_reduce          | 3.08 us                                                | 4.29 us: 1.39x slower                                               |
| crypto_pyaes             | 76.6 ms                                                | 107 ms: 1.40x slower                                                |
| coverage                 | 71.4 ms                                                | 100 ms: 1.40x slower                                                |
| nqueens                  | 80.1 ms                                                | 112 ms: 1.40x slower                                                |
| pycparser                | 1.17 sec                                               | 1.64 sec: 1.41x slower                                              |
| python_startup_no_site   | 7.16 ms                                                | 10.3 ms: 1.43x slower                                               |
| telco                    | 6.53 ms                                                | 9.43 ms: 1.45x slower                                               |
| json_dumps               | 10.4 ms                                                | 15.1 ms: 1.46x slower                                               |
| typing_runtime_protocols | 163 us                                                 | 240 us: 1.47x slower                                                |
| comprehensions           | 19.8 us                                                | 29.2 us: 1.47x slower                                               |
| fannkuch                 | 372 ms                                                 | 554 ms: 1.49x slower                                                |
| xml_etree_process        | 59.0 ms                                                | 88.1 ms: 1.49x slower                                               |
| tomli_loads              | 2.11 sec                                               | 3.18 sec: 1.51x slower                                              |
| regex_compile            | 142 ms                                                 | 215 ms: 1.51x slower                                                |
| 2to3                     | 264 ms                                                 | 408 ms: 1.55x slower                                                |
| thrift                   | 791 us                                                 | 1.23 ms: 1.55x slower                                               |
| sympy_integrate          | 20.5 ms                                                | 32.2 ms: 1.57x slower                                               |
| genshi_xml               | 50.2 ms                                                | 78.9 ms: 1.57x slower                                               |
| python_startup           | 9.93 ms                                                | 15.7 ms: 1.58x slower                                               |
| html5lib                 | 63.6 ms                                                | 102 ms: 1.60x slower                                                |
| sqlglot_normalize        | 107 ms                                                 | 171 ms: 1.60x slower                                                |
| sqlglot_optimize         | 53.3 ms                                                | 85.5 ms: 1.60x slower                                               |
| pyflate                  | 448 ms                                                 | 735 ms: 1.64x slower                                                |
| pprint_safe_repr         | 743 ms                                                 | 1.25 sec: 1.68x slower                                              |
| genshi_text              | 22.8 ms                                                | 38.8 ms: 1.70x slower                                               |
| pprint_pformat           | 1.52 sec                                               | 2.60 sec: 1.71x slower                                              |
| mako                     | 11.0 ms                                                | 19.2 ms: 1.74x slower                                               |
| unpickle_pure_python     | 221 us                                                 | 389 us: 1.76x slower                                                |
| scimark_monte_carlo      | 68.4 ms                                                | 122 ms: 1.79x slower                                                |
| chaos                    | 62.8 ms                                                | 112 ms: 1.79x slower                                                |
| logging_format           | 7.35 us                                                | 13.2 us: 1.79x slower                                               |
| logging_simple           | 6.63 us                                                | 11.9 us: 1.79x slower                                               |
| django_template          | 34.7 ms                                                | 62.3 ms: 1.80x slower                                               |
| sympy_str                | 292 ms                                                 | 526 ms: 1.80x slower                                                |
| float                    | 80.8 ms                                                | 146 ms: 1.81x slower                                                |
| richards                 | 45.9 ms                                                | 85.4 ms: 1.86x slower                                               |
| pickle_pure_python       | 308 us                                                 | 572 us: 1.86x slower                                                |
| hexiom                   | 6.17 ms                                                | 11.8 ms: 1.91x slower                                               |
| logging_silent           | 109 ns                                                 | 210 ns: 1.93x slower                                                |
| raytrace                 | 299 ms                                                 | 580 ms: 1.94x slower                                                |
| sqlglot_transpile        | 1.67 ms                                                | 3.26 ms: 1.95x slower                                               |
| richards_super           | 51.9 ms                                                | 103 ms: 1.98x slower                                                |
| scimark_sor              | 130 ms                                                 | 261 ms: 2.01x slower                                                |
| scimark_lu               | 114 ms                                                 | 233 ms: 2.04x slower                                                |
| sqlglot_parse            | 1.36 ms                                                | 2.82 ms: 2.08x slower                                               |
| go                       | 139 ms                                                 | 290 ms: 2.08x slower                                                |
| nbody                    | 89.3 ms                                                | 187 ms: 2.10x slower                                                |
| sympy_expand             | 468 ms                                                 | 1.03 sec: 2.21x slower                                              |
| sympy_sum                | 166 ms                                                 | 376 ms: 2.26x slower                                                |
| deltablue                | 3.45 ms                                                | 8.61 ms: 2.50x slower                                               |
| unpack_sequence          | 52.1 ns                                                | 137 ns: 2.63x slower                                                |
| bench_thread_pool        | 941 us                                                 | 3.45 ms: 3.67x slower                                               |
| bench_mp_pool            | 10.8 ms                                                | 71.7 ms: 6.64x slower                                               |
| Geometric mean           | (ref)                                                  | 1.49x slower                                                        |
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.40x
- 95% likely to have a slowdown of 1.39x
- 99% likely to have a slowdown of 1.34x

# Memory
- memory change: 1.22x