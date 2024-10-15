# Results vs. 3.12.6

- fork: mpage
- ref: gh_115999_tlbc_load_
- machine: linux-x86_64
- commit hash: cf0f4ec
- commit date: 2024-10-14
- overall geometric mean: 1.45x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.31x slower
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241014-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-cf0f4ec |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 404 ms: 1.53x slower                                                 |
| docutils       | 2.64 sec                                               | 3.22 sec: 1.22x slower                                               |
| html5lib       | 63.6 ms                                                | 100 ms: 1.57x slower                                                 |
| tornado_http   | 119 ms                                                 | 158 ms: 1.33x slower                                                 |
| Geometric mean | (ref)                                                  | 1.41x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241014-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-cf0f4ec |
|--------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| asyncio_websockets | 517 ms                                                 | 519 ms: 1.00x slower                                                 |
| asyncio_tcp        | 519 ms                                                 | 569 ms: 1.10x slower                                                 |
| coroutines         | 23.9 ms                                                | 28.1 ms: 1.17x slower                                                |
| asyncio_tcp_ssl    | 1.51 sec                                               | 1.81 sec: 1.20x slower                                               |
| async_generators   | 384 ms                                                 | 482 ms: 1.25x slower                                                 |
| Geometric mean     | (ref)                                                  | 1.14x slower                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241014-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-cf0f4ec |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 184 ms: 1.00x faster                                                 |
| float          | 80.8 ms                                                | 145 ms: 1.80x slower                                                 |
| nbody          | 89.3 ms                                                | 184 ms: 2.06x slower                                                 |
| Geometric mean | (ref)                                                  | 1.54x slower                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241014-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-cf0f4ec |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 3.06 ms: 1.03x faster                                                |
| regex_dna      | 168 ms                                                 | 189 ms: 1.13x slower                                                 |
| regex_v8       | 20.6 ms                                                | 25.0 ms: 1.21x slower                                                |
| regex_compile  | 142 ms                                                 | 204 ms: 1.43x slower                                                 |
| Geometric mean | (ref)                                                  | 1.17x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241014-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-cf0f4ec |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 132 ms: 1.05x faster                                                 |
| pickle_dict          | 31.8 us                                                | 31.7 us: 1.00x faster                                                |
| pickle_list          | 4.77 us                                                | 4.85 us: 1.02x slower                                                |
| xml_etree_iterparse  | 96.7 ms                                                | 102 ms: 1.05x slower                                                 |
| unpickle             | 14.1 us                                                | 14.9 us: 1.06x slower                                                |
| json_loads           | 26.5 us                                                | 28.7 us: 1.08x slower                                                |
| unpickle_list        | 4.67 us                                                | 5.21 us: 1.12x slower                                                |
| xml_etree_generate   | 85.2 ms                                                | 106 ms: 1.25x slower                                                 |
| json_dumps           | 10.4 ms                                                | 14.6 ms: 1.41x slower                                                |
| tomli_loads          | 2.11 sec                                               | 2.99 sec: 1.42x slower                                               |
| xml_etree_process    | 59.0 ms                                                | 85.8 ms: 1.46x slower                                                |
| unpickle_pure_python | 221 us                                                 | 379 us: 1.72x slower                                                 |
| pickle_pure_python   | 308 us                                                 | 557 us: 1.81x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.21x slower                                                         |

Benchmark hidden because not significant (1): pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241014-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-cf0f4ec |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.2 ms: 1.42x slower                                                |
| python_startup         | 9.93 ms                                                | 15.6 ms: 1.57x slower                                                |
| Geometric mean         | (ref)                                                  | 1.49x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241014-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-cf0f4ec |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 73.0 ms: 1.45x slower                                                |
| genshi_text     | 22.8 ms                                                | 35.7 ms: 1.56x slower                                                |
| django_template | 34.7 ms                                                | 58.0 ms: 1.67x slower                                                |
| mako            | 11.0 ms                                                | 20.0 ms: 1.82x slower                                                |
| Geometric mean  | (ref)                                                  | 1.62x slower                                                         |

All benchmarks:
===============

| Benchmark                | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241014-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-cf0f4ec |
|--------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| gc_traversal             | 3.46 ms                                                | 2.45 ms: 1.41x faster                                                |
| xml_etree_parse          | 139 ms                                                 | 132 ms: 1.05x faster                                                 |
| regex_effbot             | 3.17 ms                                                | 3.06 ms: 1.03x faster                                                |
| pathlib                  | 21.5 ms                                                | 21.2 ms: 1.02x faster                                                |
| pidigits                 | 184 ms                                                 | 184 ms: 1.00x faster                                                 |
| pickle_dict              | 31.8 us                                                | 31.7 us: 1.00x faster                                                |
| asyncio_websockets       | 517 ms                                                 | 519 ms: 1.00x slower                                                 |
| create_gc_cycles         | 1.09 ms                                                | 1.10 ms: 1.01x slower                                                |
| pickle_list              | 4.77 us                                                | 4.85 us: 1.02x slower                                                |
| json                     | 5.02 ms                                                | 5.16 ms: 1.03x slower                                                |
| xml_etree_iterparse      | 96.7 ms                                                | 102 ms: 1.05x slower                                                 |
| unpickle                 | 14.1 us                                                | 14.9 us: 1.06x slower                                                |
| deepcopy                 | 352 us                                                 | 376 us: 1.07x slower                                                 |
| json_loads               | 26.5 us                                                | 28.7 us: 1.08x slower                                                |
| asyncio_tcp              | 519 ms                                                 | 569 ms: 1.10x slower                                                 |
| sqlite_synth             | 2.20 us                                                | 2.42 us: 1.10x slower                                                |
| unpickle_list            | 4.67 us                                                | 5.21 us: 1.12x slower                                                |
| regex_dna                | 168 ms                                                 | 189 ms: 1.13x slower                                                 |
| deepcopy_memo            | 40.3 us                                                | 46.0 us: 1.14x slower                                                |
| scimark_fft              | 342 ms                                                 | 392 ms: 1.15x slower                                                 |
| coroutines               | 23.9 ms                                                | 28.1 ms: 1.17x slower                                                |
| asyncio_tcp_ssl          | 1.51 sec                                               | 1.81 sec: 1.20x slower                                               |
| regex_v8                 | 20.6 ms                                                | 25.0 ms: 1.21x slower                                                |
| scimark_sparse_mat_mult  | 4.39 ms                                                | 5.34 ms: 1.22x slower                                                |
| bpe_tokeniser            | 4.74 sec                                               | 5.76 sec: 1.22x slower                                               |
| docutils                 | 2.64 sec                                               | 3.22 sec: 1.22x slower                                               |
| mdp                      | 2.42 sec                                               | 2.96 sec: 1.22x slower                                               |
| generators               | 32.2 ms                                                | 39.6 ms: 1.23x slower                                                |
| xml_etree_generate       | 85.2 ms                                                | 106 ms: 1.25x slower                                                 |
| async_generators         | 384 ms                                                 | 482 ms: 1.25x slower                                                 |
| pylint                   | 319 ms                                                 | 400 ms: 1.26x slower                                                 |
| dulwich_log              | 78.9 ms                                                | 99.4 ms: 1.26x slower                                                |
| deepcopy_reduce          | 3.08 us                                                | 3.92 us: 1.27x slower                                                |
| typing_runtime_protocols | 163 us                                                 | 213 us: 1.31x slower                                                 |
| meteor_contest           | 104 ms                                                 | 136 ms: 1.31x slower                                                 |
| spectral_norm            | 110 ms                                                 | 145 ms: 1.32x slower                                                 |
| tornado_http             | 119 ms                                                 | 158 ms: 1.33x slower                                                 |
| nqueens                  | 80.1 ms                                                | 108 ms: 1.35x slower                                                 |
| crypto_pyaes             | 76.6 ms                                                | 105 ms: 1.38x slower                                                 |
| coverage                 | 71.4 ms                                                | 99.6 ms: 1.39x slower                                                |
| pycparser                | 1.17 sec                                               | 1.64 sec: 1.40x slower                                               |
| json_dumps               | 10.4 ms                                                | 14.6 ms: 1.41x slower                                                |
| tomli_loads              | 2.11 sec                                               | 2.99 sec: 1.42x slower                                               |
| python_startup_no_site   | 7.16 ms                                                | 10.2 ms: 1.42x slower                                                |
| regex_compile            | 142 ms                                                 | 204 ms: 1.43x slower                                                 |
| genshi_xml               | 50.2 ms                                                | 73.0 ms: 1.45x slower                                                |
| telco                    | 6.53 ms                                                | 9.49 ms: 1.45x slower                                                |
| xml_etree_process        | 59.0 ms                                                | 85.8 ms: 1.46x slower                                                |
| fannkuch                 | 372 ms                                                 | 547 ms: 1.47x slower                                                 |
| comprehensions           | 19.8 us                                                | 29.3 us: 1.48x slower                                                |
| sqlglot_normalize        | 107 ms                                                 | 158 ms: 1.48x slower                                                 |
| sqlglot_optimize         | 53.3 ms                                                | 80.0 ms: 1.50x slower                                                |
| 2to3                     | 264 ms                                                 | 404 ms: 1.53x slower                                                 |
| sympy_integrate          | 20.5 ms                                                | 31.6 ms: 1.54x slower                                                |
| pprint_safe_repr         | 743 ms                                                 | 1.15 sec: 1.55x slower                                               |
| genshi_text              | 22.8 ms                                                | 35.7 ms: 1.56x slower                                                |
| thrift                   | 791 us                                                 | 1.24 ms: 1.57x slower                                                |
| python_startup           | 9.93 ms                                                | 15.6 ms: 1.57x slower                                                |
| html5lib                 | 63.6 ms                                                | 100 ms: 1.57x slower                                                 |
| pprint_pformat           | 1.52 sec                                               | 2.40 sec: 1.58x slower                                               |
| django_template          | 34.7 ms                                                | 58.0 ms: 1.67x slower                                                |
| pyflate                  | 448 ms                                                 | 750 ms: 1.67x slower                                                 |
| logging_format           | 7.35 us                                                | 12.5 us: 1.70x slower                                                |
| unpickle_pure_python     | 221 us                                                 | 379 us: 1.72x slower                                                 |
| logging_simple           | 6.63 us                                                | 11.4 us: 1.72x slower                                                |
| scimark_monte_carlo      | 68.4 ms                                                | 119 ms: 1.74x slower                                                 |
| sympy_str                | 292 ms                                                 | 517 ms: 1.77x slower                                                 |
| float                    | 80.8 ms                                                | 145 ms: 1.80x slower                                                 |
| scimark_lu               | 114 ms                                                 | 206 ms: 1.80x slower                                                 |
| pickle_pure_python       | 308 us                                                 | 557 us: 1.81x slower                                                 |
| mako                     | 11.0 ms                                                | 20.0 ms: 1.82x slower                                                |
| chaos                    | 62.8 ms                                                | 114 ms: 1.82x slower                                                 |
| richards                 | 45.9 ms                                                | 83.8 ms: 1.82x slower                                                |
| hexiom                   | 6.17 ms                                                | 11.3 ms: 1.83x slower                                                |
| logging_silent           | 109 ns                                                 | 207 ns: 1.90x slower                                                 |
| sqlglot_transpile        | 1.67 ms                                                | 3.23 ms: 1.93x slower                                                |
| richards_super           | 51.9 ms                                                | 101 ms: 1.94x slower                                                 |
| scimark_sor              | 130 ms                                                 | 257 ms: 1.98x slower                                                 |
| sqlglot_parse            | 1.36 ms                                                | 2.78 ms: 2.05x slower                                                |
| go                       | 139 ms                                                 | 286 ms: 2.05x slower                                                 |
| nbody                    | 89.3 ms                                                | 184 ms: 2.06x slower                                                 |
| raytrace                 | 299 ms                                                 | 617 ms: 2.06x slower                                                 |
| sympy_expand             | 468 ms                                                 | 1.02 sec: 2.18x slower                                               |
| sympy_sum                | 166 ms                                                 | 369 ms: 2.23x slower                                                 |
| deltablue                | 3.45 ms                                                | 8.61 ms: 2.50x slower                                                |
| unpack_sequence          | 52.1 ns                                                | 132 ns: 2.53x slower                                                 |
| bench_thread_pool        | 941 us                                                 | 3.44 ms: 3.66x slower                                                |
| bench_mp_pool            | 10.8 ms                                                | 71.1 ms: 6.59x slower                                                |
| Geometric mean           | (ref)                                                  | 1.45x slower                                                         |

Benchmark hidden because not significant (1): pickle
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.37x
- 95% likely to have a slowdown of 1.34x
- 99% likely to have a slowdown of 1.31x

# Memory
- memory change: 1.22x