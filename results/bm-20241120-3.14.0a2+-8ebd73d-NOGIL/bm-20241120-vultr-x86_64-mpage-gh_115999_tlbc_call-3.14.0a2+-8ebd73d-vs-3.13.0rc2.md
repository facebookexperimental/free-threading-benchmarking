# Results vs. 3.13.0rc2

- fork: mpage
- ref: gh_115999_tlbc_call
- machine: linux-x86_64
- commit hash: 8ebd73d
- commit date: 2024-11-20
- overall geometric mean: 1.52x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.37x slower
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241120-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-8ebd73d |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 410 ms: 1.58x slower                                                 |
| docutils       | 2.62 sec                                                     | 3.28 sec: 1.25x slower                                               |
| html5lib       | 67.0 ms                                                      | 104 ms: 1.55x slower                                                 |
| Geometric mean | (ref)                                                        | 1.45x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241120-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-8ebd73d |
|--------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| asyncio_websockets | 520 ms                                                       | 523 ms: 1.00x slower                                                 |
| asyncio_tcp        | 505 ms                                                       | 584 ms: 1.15x slower                                                 |
| coroutines         | 23.6 ms                                                      | 28.6 ms: 1.21x slower                                                |
| asyncio_tcp_ssl    | 1.51 sec                                                     | 1.84 sec: 1.22x slower                                               |
| async_generators   | 377 ms                                                       | 485 ms: 1.28x slower                                                 |
| Geometric mean     | (ref)                                                        | 1.17x slower                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241120-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-8ebd73d |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 182 ms: 1.19x faster                                                 |
| float          | 77.5 ms                                                      | 148 ms: 1.92x slower                                                 |
| nbody          | 85.1 ms                                                      | 199 ms: 2.34x slower                                                 |
| Geometric mean | (ref)                                                        | 1.56x slower                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241120-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-8ebd73d |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.82 ms: 1.09x faster                                                |
| regex_dna      | 180 ms                                                       | 186 ms: 1.03x slower                                                 |
| regex_v8       | 22.7 ms                                                      | 24.9 ms: 1.10x slower                                                |
| regex_compile  | 132 ms                                                       | 213 ms: 1.61x slower                                                 |
| Geometric mean | (ref)                                                        | 1.14x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241120-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-8ebd73d |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                       | 132 ms: 1.04x faster                                                 |
| pickle_dict          | 32.5 us                                                      | 31.9 us: 1.02x faster                                                |
| json_loads           | 27.0 us                                                      | 28.4 us: 1.05x slower                                                |
| unpickle_list        | 4.71 us                                                      | 5.11 us: 1.08x slower                                                |
| xml_etree_iterparse  | 94.9 ms                                                      | 105 ms: 1.11x slower                                                 |
| pickle               | 11.3 us                                                      | 12.7 us: 1.12x slower                                                |
| xml_etree_generate   | 85.4 ms                                                      | 109 ms: 1.28x slower                                                 |
| json_dumps           | 10.5 ms                                                      | 15.0 ms: 1.42x slower                                                |
| xml_etree_process    | 59.3 ms                                                      | 89.6 ms: 1.51x slower                                                |
| tomli_loads          | 2.01 sec                                                     | 3.12 sec: 1.55x slower                                               |
| unpickle_pure_python | 210 us                                                       | 390 us: 1.86x slower                                                 |
| pickle_pure_python   | 294 us                                                       | 586 us: 1.99x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.24x slower                                                         |

Benchmark hidden because not significant (2): unpickle, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241120-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-8ebd73d |
|------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.3 ms: 1.40x slower                                                |
| python_startup         | 11.0 ms                                                      | 15.8 ms: 1.44x slower                                                |
| Geometric mean         | (ref)                                                        | 1.42x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241120-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-8ebd73d |
|-----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 79.6 ms: 1.63x slower                                                |
| mako            | 11.3 ms                                                      | 18.9 ms: 1.67x slower                                                |
| django_template | 34.1 ms                                                      | 61.4 ms: 1.80x slower                                                |
| genshi_text     | 21.5 ms                                                      | 39.2 ms: 1.82x slower                                                |
| Geometric mean  | (ref)                                                        | 1.73x slower                                                         |

All benchmarks:
===============

| Benchmark                | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241120-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-8ebd73d |
|--------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pidigits                 | 217 ms                                                       | 182 ms: 1.19x faster                                                 |
| gc_traversal             | 3.14 ms                                                      | 2.68 ms: 1.17x faster                                                |
| create_gc_cycles         | 1.34 ms                                                      | 1.19 ms: 1.12x faster                                                |
| regex_effbot             | 3.08 ms                                                      | 2.82 ms: 1.09x faster                                                |
| xml_etree_parse          | 136 ms                                                       | 132 ms: 1.04x faster                                                 |
| pickle_dict              | 32.5 us                                                      | 31.9 us: 1.02x faster                                                |
| asyncio_websockets       | 520 ms                                                       | 523 ms: 1.00x slower                                                 |
| regex_dna                | 180 ms                                                       | 186 ms: 1.03x slower                                                 |
| json_loads               | 27.0 us                                                      | 28.4 us: 1.05x slower                                                |
| json                     | 4.93 ms                                                      | 5.22 ms: 1.06x slower                                                |
| sqlite_synth             | 2.21 us                                                      | 2.39 us: 1.08x slower                                                |
| unpickle_list            | 4.71 us                                                      | 5.11 us: 1.08x slower                                                |
| regex_v8                 | 22.7 ms                                                      | 24.9 ms: 1.10x slower                                                |
| xml_etree_iterparse      | 94.9 ms                                                      | 105 ms: 1.11x slower                                                 |
| pickle                   | 11.3 us                                                      | 12.7 us: 1.12x slower                                                |
| pathlib                  | 19.2 ms                                                      | 22.0 ms: 1.15x slower                                                |
| deepcopy                 | 355 us                                                       | 410 us: 1.15x slower                                                 |
| asyncio_tcp              | 505 ms                                                       | 584 ms: 1.15x slower                                                 |
| scimark_fft              | 349 ms                                                       | 404 ms: 1.16x slower                                                 |
| telco                    | 7.82 ms                                                      | 9.33 ms: 1.19x slower                                                |
| coverage                 | 83.0 ms                                                      | 99.9 ms: 1.20x slower                                                |
| coroutines               | 23.6 ms                                                      | 28.6 ms: 1.21x slower                                                |
| asyncio_tcp_ssl          | 1.51 sec                                                     | 1.84 sec: 1.22x slower                                               |
| scimark_sparse_mat_mult  | 4.71 ms                                                      | 5.85 ms: 1.24x slower                                                |
| deepcopy_memo            | 39.1 us                                                      | 48.9 us: 1.25x slower                                                |
| docutils                 | 2.62 sec                                                     | 3.28 sec: 1.25x slower                                               |
| xml_etree_generate       | 85.4 ms                                                      | 109 ms: 1.28x slower                                                 |
| bpe_tokeniser            | 4.45 sec                                                     | 5.68 sec: 1.28x slower                                               |
| async_generators         | 377 ms                                                       | 485 ms: 1.28x slower                                                 |
| pylint                   | 317 ms                                                       | 412 ms: 1.30x slower                                                 |
| mdp                      | 2.36 sec                                                     | 3.12 sec: 1.32x slower                                               |
| meteor_contest           | 102 ms                                                       | 135 ms: 1.33x slower                                                 |
| dulwich_log              | 74.8 ms                                                      | 103 ms: 1.38x slower                                                 |
| spectral_norm            | 111 ms                                                       | 153 ms: 1.38x slower                                                 |
| deepcopy_reduce          | 3.11 us                                                      | 4.33 us: 1.39x slower                                                |
| python_startup_no_site   | 7.39 ms                                                      | 10.3 ms: 1.40x slower                                                |
| json_dumps               | 10.5 ms                                                      | 15.0 ms: 1.42x slower                                                |
| nqueens                  | 78.6 ms                                                      | 113 ms: 1.43x slower                                                 |
| python_startup           | 11.0 ms                                                      | 15.8 ms: 1.44x slower                                                |
| generators               | 28.8 ms                                                      | 42.0 ms: 1.46x slower                                                |
| fannkuch                 | 370 ms                                                       | 544 ms: 1.47x slower                                                 |
| pycparser                | 1.12 sec                                                     | 1.66 sec: 1.49x slower                                               |
| xml_etree_process        | 59.3 ms                                                      | 89.6 ms: 1.51x slower                                                |
| crypto_pyaes             | 67.9 ms                                                      | 105 ms: 1.55x slower                                                 |
| typing_runtime_protocols | 155 us                                                       | 239 us: 1.55x slower                                                 |
| html5lib                 | 67.0 ms                                                      | 104 ms: 1.55x slower                                                 |
| tomli_loads              | 2.01 sec                                                     | 3.12 sec: 1.55x slower                                               |
| 2to3                     | 260 ms                                                       | 410 ms: 1.58x slower                                                 |
| regex_compile            | 132 ms                                                       | 213 ms: 1.61x slower                                                 |
| sqlglot_normalize        | 106 ms                                                       | 171 ms: 1.62x slower                                                 |
| sqlglot_optimize         | 52.7 ms                                                      | 85.4 ms: 1.62x slower                                                |
| sympy_integrate          | 19.8 ms                                                      | 32.2 ms: 1.62x slower                                                |
| genshi_xml               | 48.8 ms                                                      | 79.6 ms: 1.63x slower                                                |
| pyflate                  | 449 ms                                                       | 734 ms: 1.64x slower                                                 |
| thrift                   | 778 us                                                       | 1.28 ms: 1.65x slower                                                |
| mako                     | 11.3 ms                                                      | 18.9 ms: 1.67x slower                                                |
| pprint_safe_repr         | 738 ms                                                       | 1.24 sec: 1.68x slower                                               |
| pprint_pformat           | 1.50 sec                                                     | 2.57 sec: 1.72x slower                                               |
| comprehensions           | 16.5 us                                                      | 29.2 us: 1.77x slower                                                |
| django_template          | 34.1 ms                                                      | 61.4 ms: 1.80x slower                                                |
| genshi_text              | 21.5 ms                                                      | 39.2 ms: 1.82x slower                                                |
| unpickle_pure_python     | 210 us                                                       | 390 us: 1.86x slower                                                 |
| scimark_monte_carlo      | 65.4 ms                                                      | 124 ms: 1.90x slower                                                 |
| logging_simple           | 6.16 us                                                      | 11.8 us: 1.91x slower                                                |
| float                    | 77.5 ms                                                      | 148 ms: 1.92x slower                                                 |
| richards                 | 45.2 ms                                                      | 86.7 ms: 1.92x slower                                                |
| logging_format           | 6.84 us                                                      | 13.1 us: 1.92x slower                                                |
| sympy_str                | 275 ms                                                       | 530 ms: 1.93x slower                                                 |
| hexiom                   | 5.99 ms                                                      | 11.7 ms: 1.95x slower                                                |
| scimark_sor              | 134 ms                                                       | 266 ms: 1.98x slower                                                 |
| pickle_pure_python       | 294 us                                                       | 586 us: 1.99x slower                                                 |
| chaos                    | 57.3 ms                                                      | 114 ms: 1.99x slower                                                 |
| richards_super           | 51.6 ms                                                      | 104 ms: 2.01x slower                                                 |
| logging_silent           | 103 ns                                                       | 210 ns: 2.05x slower                                                 |
| scimark_lu               | 113 ms                                                       | 235 ms: 2.08x slower                                                 |
| go                       | 141 ms                                                       | 295 ms: 2.10x slower                                                 |
| sqlglot_transpile        | 1.56 ms                                                      | 3.29 ms: 2.11x slower                                                |
| sqlglot_parse            | 1.25 ms                                                      | 2.83 ms: 2.26x slower                                                |
| sympy_expand             | 457 ms                                                       | 1.04 sec: 2.27x slower                                               |
| raytrace                 | 253 ms                                                       | 581 ms: 2.30x slower                                                 |
| nbody                    | 85.1 ms                                                      | 199 ms: 2.34x slower                                                 |
| sympy_sum                | 156 ms                                                       | 377 ms: 2.43x slower                                                 |
| deltablue                | 3.12 ms                                                      | 8.82 ms: 2.82x slower                                                |
| unpack_sequence          | 44.8 ns                                                      | 152 ns: 3.40x slower                                                 |
| bench_thread_pool        | 919 us                                                       | 3.47 ms: 3.77x slower                                                |
| bench_mp_pool            | 11.0 ms                                                      | 69.7 ms: 6.34x slower                                                |
| Geometric mean           | (ref)                                                        | 1.52x slower                                                         |

Benchmark hidden because not significant (2): unpickle, pickle_list
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.44x
- 95% likely to have a slowdown of 1.42x
- 99% likely to have a slowdown of 1.37x

# Memory
- memory change: 1.22x