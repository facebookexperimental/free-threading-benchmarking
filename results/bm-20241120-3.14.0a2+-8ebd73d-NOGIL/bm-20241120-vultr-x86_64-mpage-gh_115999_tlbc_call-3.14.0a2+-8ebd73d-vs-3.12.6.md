# Results vs. 3.12.6

- fork: mpage
- ref: gh_115999_tlbc_call
- machine: linux-x86_64
- commit hash: 8ebd73d
- commit date: 2024-11-20
- overall geometric mean: 1.50x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.34x slower
- Memory change: 1.24x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241120-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-8ebd73d |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 410 ms: 1.55x slower                                                 |
| docutils       | 2.64 sec                                               | 3.28 sec: 1.24x slower                                               |
| html5lib       | 63.6 ms                                                | 104 ms: 1.63x slower                                                 |
| Geometric mean | (ref)                                                  | 1.47x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241120-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-8ebd73d |
|--------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| asyncio_websockets | 517 ms                                                 | 523 ms: 1.01x slower                                                 |
| asyncio_tcp        | 519 ms                                                 | 584 ms: 1.13x slower                                                 |
| coroutines         | 23.9 ms                                                | 28.6 ms: 1.19x slower                                                |
| asyncio_tcp_ssl    | 1.51 sec                                               | 1.84 sec: 1.22x slower                                               |
| async_generators   | 384 ms                                                 | 485 ms: 1.26x slower                                                 |
| Geometric mean     | (ref)                                                  | 1.16x slower                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241120-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-8ebd73d |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 182 ms: 1.01x faster                                                 |
| float          | 80.8 ms                                                | 148 ms: 1.84x slower                                                 |
| nbody          | 89.3 ms                                                | 199 ms: 2.23x slower                                                 |
| Geometric mean | (ref)                                                  | 1.60x slower                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241120-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-8ebd73d |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.82 ms: 1.12x faster                                                |
| regex_dna      | 168 ms                                                 | 186 ms: 1.11x slower                                                 |
| regex_v8       | 20.6 ms                                                | 24.9 ms: 1.21x slower                                                |
| regex_compile  | 142 ms                                                 | 213 ms: 1.50x slower                                                 |
| Geometric mean | (ref)                                                  | 1.16x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241120-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-8ebd73d |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 132 ms: 1.05x faster                                                 |
| pickle_dict          | 31.8 us                                                | 31.9 us: 1.00x slower                                                |
| unpickle             | 14.1 us                                                | 14.2 us: 1.01x slower                                                |
| pickle_list          | 4.77 us                                                | 4.93 us: 1.03x slower                                                |
| json_loads           | 26.5 us                                                | 28.4 us: 1.07x slower                                                |
| xml_etree_iterparse  | 96.7 ms                                                | 105 ms: 1.09x slower                                                 |
| unpickle_list        | 4.67 us                                                | 5.11 us: 1.09x slower                                                |
| pickle               | 10.9 us                                                | 12.7 us: 1.16x slower                                                |
| xml_etree_generate   | 85.2 ms                                                | 109 ms: 1.28x slower                                                 |
| json_dumps           | 10.4 ms                                                | 15.0 ms: 1.44x slower                                                |
| tomli_loads          | 2.11 sec                                               | 3.12 sec: 1.48x slower                                               |
| xml_etree_process    | 59.0 ms                                                | 89.6 ms: 1.52x slower                                                |
| unpickle_pure_python | 221 us                                                 | 390 us: 1.77x slower                                                 |
| pickle_pure_python   | 308 us                                                 | 586 us: 1.91x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.24x slower                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241120-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-8ebd73d |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.3 ms: 1.44x slower                                                |
| python_startup         | 9.93 ms                                                | 15.8 ms: 1.59x slower                                                |
| Geometric mean         | (ref)                                                  | 1.51x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241120-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-8ebd73d |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 79.6 ms: 1.59x slower                                                |
| genshi_text     | 22.8 ms                                                | 39.2 ms: 1.72x slower                                                |
| mako            | 11.0 ms                                                | 18.9 ms: 1.72x slower                                                |
| django_template | 34.7 ms                                                | 61.4 ms: 1.77x slower                                                |
| Geometric mean  | (ref)                                                  | 1.70x slower                                                         |

All benchmarks:
===============

| Benchmark                | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241120-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-8ebd73d |
|--------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| gc_traversal             | 3.46 ms                                                | 2.68 ms: 1.29x faster                                                |
| regex_effbot             | 3.17 ms                                                | 2.82 ms: 1.12x faster                                                |
| xml_etree_parse          | 139 ms                                                 | 132 ms: 1.05x faster                                                 |
| pidigits                 | 184 ms                                                 | 182 ms: 1.01x faster                                                 |
| pickle_dict              | 31.8 us                                                | 31.9 us: 1.00x slower                                                |
| asyncio_websockets       | 517 ms                                                 | 523 ms: 1.01x slower                                                 |
| unpickle                 | 14.1 us                                                | 14.2 us: 1.01x slower                                                |
| pathlib                  | 21.5 ms                                                | 22.0 ms: 1.02x slower                                                |
| pickle_list              | 4.77 us                                                | 4.93 us: 1.03x slower                                                |
| json                     | 5.02 ms                                                | 5.22 ms: 1.04x slower                                                |
| json_loads               | 26.5 us                                                | 28.4 us: 1.07x slower                                                |
| sqlite_synth             | 2.20 us                                                | 2.39 us: 1.09x slower                                                |
| xml_etree_iterparse      | 96.7 ms                                                | 105 ms: 1.09x slower                                                 |
| create_gc_cycles         | 1.09 ms                                                | 1.19 ms: 1.09x slower                                                |
| unpickle_list            | 4.67 us                                                | 5.11 us: 1.09x slower                                                |
| regex_dna                | 168 ms                                                 | 186 ms: 1.11x slower                                                 |
| asyncio_tcp              | 519 ms                                                 | 584 ms: 1.13x slower                                                 |
| pickle                   | 10.9 us                                                | 12.7 us: 1.16x slower                                                |
| deepcopy                 | 352 us                                                 | 410 us: 1.17x slower                                                 |
| scimark_fft              | 342 ms                                                 | 404 ms: 1.18x slower                                                 |
| coroutines               | 23.9 ms                                                | 28.6 ms: 1.19x slower                                                |
| bpe_tokeniser            | 4.74 sec                                               | 5.68 sec: 1.20x slower                                               |
| regex_v8                 | 20.6 ms                                                | 24.9 ms: 1.21x slower                                                |
| deepcopy_memo            | 40.3 us                                                | 48.9 us: 1.21x slower                                                |
| asyncio_tcp_ssl          | 1.51 sec                                               | 1.84 sec: 1.22x slower                                               |
| docutils                 | 2.64 sec                                               | 3.28 sec: 1.24x slower                                               |
| async_generators         | 384 ms                                                 | 485 ms: 1.26x slower                                                 |
| xml_etree_generate       | 85.2 ms                                                | 109 ms: 1.28x slower                                                 |
| mdp                      | 2.42 sec                                               | 3.12 sec: 1.29x slower                                               |
| pylint                   | 319 ms                                                 | 412 ms: 1.29x slower                                                 |
| generators               | 32.2 ms                                                | 42.0 ms: 1.30x slower                                                |
| meteor_contest           | 104 ms                                                 | 135 ms: 1.30x slower                                                 |
| dulwich_log              | 78.9 ms                                                | 103 ms: 1.30x slower                                                 |
| scimark_sparse_mat_mult  | 4.39 ms                                                | 5.85 ms: 1.33x slower                                                |
| crypto_pyaes             | 76.6 ms                                                | 105 ms: 1.37x slower                                                 |
| spectral_norm            | 110 ms                                                 | 153 ms: 1.39x slower                                                 |
| coverage                 | 71.4 ms                                                | 99.9 ms: 1.40x slower                                                |
| nqueens                  | 80.1 ms                                                | 113 ms: 1.41x slower                                                 |
| deepcopy_reduce          | 3.08 us                                                | 4.33 us: 1.41x slower                                                |
| pycparser                | 1.17 sec                                               | 1.66 sec: 1.42x slower                                               |
| telco                    | 6.53 ms                                                | 9.33 ms: 1.43x slower                                                |
| python_startup_no_site   | 7.16 ms                                                | 10.3 ms: 1.44x slower                                                |
| json_dumps               | 10.4 ms                                                | 15.0 ms: 1.44x slower                                                |
| fannkuch                 | 372 ms                                                 | 544 ms: 1.46x slower                                                 |
| typing_runtime_protocols | 163 us                                                 | 239 us: 1.47x slower                                                 |
| comprehensions           | 19.8 us                                                | 29.2 us: 1.47x slower                                                |
| tomli_loads              | 2.11 sec                                               | 3.12 sec: 1.48x slower                                               |
| regex_compile            | 142 ms                                                 | 213 ms: 1.50x slower                                                 |
| xml_etree_process        | 59.0 ms                                                | 89.6 ms: 1.52x slower                                                |
| 2to3                     | 264 ms                                                 | 410 ms: 1.55x slower                                                 |
| sympy_integrate          | 20.5 ms                                                | 32.2 ms: 1.57x slower                                                |
| genshi_xml               | 50.2 ms                                                | 79.6 ms: 1.59x slower                                                |
| python_startup           | 9.93 ms                                                | 15.8 ms: 1.59x slower                                                |
| sqlglot_optimize         | 53.3 ms                                                | 85.4 ms: 1.60x slower                                                |
| sqlglot_normalize        | 107 ms                                                 | 171 ms: 1.61x slower                                                 |
| thrift                   | 791 us                                                 | 1.28 ms: 1.62x slower                                                |
| html5lib                 | 63.6 ms                                                | 104 ms: 1.63x slower                                                 |
| pyflate                  | 448 ms                                                 | 734 ms: 1.64x slower                                                 |
| pprint_safe_repr         | 743 ms                                                 | 1.24 sec: 1.67x slower                                               |
| pprint_pformat           | 1.52 sec                                               | 2.57 sec: 1.69x slower                                               |
| genshi_text              | 22.8 ms                                                | 39.2 ms: 1.72x slower                                                |
| mako                     | 11.0 ms                                                | 18.9 ms: 1.72x slower                                                |
| unpickle_pure_python     | 221 us                                                 | 390 us: 1.77x slower                                                 |
| django_template          | 34.7 ms                                                | 61.4 ms: 1.77x slower                                                |
| logging_simple           | 6.63 us                                                | 11.8 us: 1.78x slower                                                |
| logging_format           | 7.35 us                                                | 13.1 us: 1.79x slower                                                |
| scimark_monte_carlo      | 68.4 ms                                                | 124 ms: 1.81x slower                                                 |
| chaos                    | 62.8 ms                                                | 114 ms: 1.82x slower                                                 |
| sympy_str                | 292 ms                                                 | 530 ms: 1.82x slower                                                 |
| float                    | 80.8 ms                                                | 148 ms: 1.84x slower                                                 |
| richards                 | 45.9 ms                                                | 86.7 ms: 1.89x slower                                                |
| hexiom                   | 6.17 ms                                                | 11.7 ms: 1.89x slower                                                |
| pickle_pure_python       | 308 us                                                 | 586 us: 1.91x slower                                                 |
| logging_silent           | 109 ns                                                 | 210 ns: 1.93x slower                                                 |
| raytrace                 | 299 ms                                                 | 581 ms: 1.94x slower                                                 |
| sqlglot_transpile        | 1.67 ms                                                | 3.29 ms: 1.97x slower                                                |
| richards_super           | 51.9 ms                                                | 104 ms: 2.00x slower                                                 |
| scimark_sor              | 130 ms                                                 | 266 ms: 2.05x slower                                                 |
| scimark_lu               | 114 ms                                                 | 235 ms: 2.06x slower                                                 |
| sqlglot_parse            | 1.36 ms                                                | 2.83 ms: 2.09x slower                                                |
| go                       | 139 ms                                                 | 295 ms: 2.12x slower                                                 |
| sympy_expand             | 468 ms                                                 | 1.04 sec: 2.22x slower                                               |
| nbody                    | 89.3 ms                                                | 199 ms: 2.23x slower                                                 |
| sympy_sum                | 166 ms                                                 | 377 ms: 2.27x slower                                                 |
| deltablue                | 3.45 ms                                                | 8.82 ms: 2.56x slower                                                |
| unpack_sequence          | 52.1 ns                                                | 152 ns: 2.92x slower                                                 |
| bench_thread_pool        | 941 us                                                 | 3.47 ms: 3.68x slower                                                |
| bench_mp_pool            | 10.8 ms                                                | 69.7 ms: 6.45x slower                                                |
| Geometric mean           | (ref)                                                  | 1.50x slower                                                         |
Ignored benchmarks (17) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.41x
- 95% likely to have a slowdown of 1.40x
- 99% likely to have a slowdown of 1.34x

# Memory
- memory change: 1.24x