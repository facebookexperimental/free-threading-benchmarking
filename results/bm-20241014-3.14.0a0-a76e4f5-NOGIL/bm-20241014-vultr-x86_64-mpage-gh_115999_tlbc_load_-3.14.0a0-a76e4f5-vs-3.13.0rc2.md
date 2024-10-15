# Results vs. 3.13.0rc2

- fork: mpage
- ref: gh_115999_tlbc_load_
- machine: linux-x86_64
- commit hash: a76e4f5
- commit date: 2024-10-14
- overall geometric mean: 1.57x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.40x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241014-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-a76e4f5 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 419 ms: 1.62x slower                                                 |
| docutils       | 2.62 sec                                                     | 3.37 sec: 1.29x slower                                               |
| html5lib       | 67.0 ms                                                      | 106 ms: 1.58x slower                                                 |
| tornado_http   | 114 ms                                                       | 165 ms: 1.45x slower                                                 |
| Geometric mean | (ref)                                                        | 1.48x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241014-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-a76e4f5 |
|------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| asyncio_tcp      | 505 ms                                                       | 580 ms: 1.15x slower                                                 |
| asyncio_tcp_ssl  | 1.51 sec                                                     | 1.83 sec: 1.21x slower                                               |
| async_generators | 377 ms                                                       | 495 ms: 1.31x slower                                                 |
| coroutines       | 23.6 ms                                                      | 31.2 ms: 1.33x slower                                                |
| Geometric mean   | (ref)                                                        | 1.19x slower                                                         |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241014-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-a76e4f5 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 184 ms: 1.18x faster                                                 |
| float          | 77.5 ms                                                      | 151 ms: 1.95x slower                                                 |
| nbody          | 85.1 ms                                                      | 196 ms: 2.30x slower                                                 |
| Geometric mean | (ref)                                                        | 1.56x slower                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241014-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-a76e4f5 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 3.20 ms: 1.04x slower                                                |
| regex_dna      | 180 ms                                                       | 191 ms: 1.06x slower                                                 |
| regex_v8       | 22.7 ms                                                      | 25.9 ms: 1.14x slower                                                |
| regex_compile  | 132 ms                                                       | 233 ms: 1.76x slower                                                 |
| Geometric mean | (ref)                                                        | 1.22x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241014-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-a76e4f5 |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pickle               | 11.3 us                                                      | 10.7 us: 1.06x faster                                                |
| xml_etree_parse      | 136 ms                                                       | 133 ms: 1.03x faster                                                 |
| unpickle             | 14.3 us                                                      | 14.9 us: 1.04x slower                                                |
| json_loads           | 27.0 us                                                      | 28.7 us: 1.06x slower                                                |
| unpickle_list        | 4.71 us                                                      | 5.11 us: 1.08x slower                                                |
| xml_etree_iterparse  | 94.9 ms                                                      | 109 ms: 1.15x slower                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 114 ms: 1.33x slower                                                 |
| json_dumps           | 10.5 ms                                                      | 15.3 ms: 1.45x slower                                                |
| xml_etree_process    | 59.3 ms                                                      | 93.1 ms: 1.57x slower                                                |
| tomli_loads          | 2.01 sec                                                     | 3.27 sec: 1.63x slower                                               |
| unpickle_pure_python | 210 us                                                       | 425 us: 2.02x slower                                                 |
| pickle_pure_python   | 294 us                                                       | 623 us: 2.11x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.27x slower                                                         |

Benchmark hidden because not significant (2): pickle_list, pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241014-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-a76e4f5 |
|------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.2 ms: 1.38x slower                                                |
| python_startup         | 11.0 ms                                                      | 15.7 ms: 1.43x slower                                                |
| Geometric mean         | (ref)                                                        | 1.40x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241014-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-a76e4f5 |
|-----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 83.5 ms: 1.71x slower                                                |
| mako            | 11.3 ms                                                      | 21.1 ms: 1.86x slower                                                |
| genshi_text     | 21.5 ms                                                      | 40.4 ms: 1.88x slower                                                |
| django_template | 34.1 ms                                                      | 65.4 ms: 1.92x slower                                                |
| Geometric mean  | (ref)                                                        | 1.84x slower                                                         |

All benchmarks:
===============

| Benchmark                | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241014-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-a76e4f5 |
|--------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| gc_traversal             | 3.14 ms                                                      | 2.46 ms: 1.28x faster                                                |
| create_gc_cycles         | 1.34 ms                                                      | 1.13 ms: 1.19x faster                                                |
| pidigits                 | 217 ms                                                       | 184 ms: 1.18x faster                                                 |
| pickle                   | 11.3 us                                                      | 10.7 us: 1.06x faster                                                |
| xml_etree_parse          | 136 ms                                                       | 133 ms: 1.03x faster                                                 |
| regex_effbot             | 3.08 ms                                                      | 3.20 ms: 1.04x slower                                                |
| unpickle                 | 14.3 us                                                      | 14.9 us: 1.04x slower                                                |
| regex_dna                | 180 ms                                                       | 191 ms: 1.06x slower                                                 |
| json_loads               | 27.0 us                                                      | 28.7 us: 1.06x slower                                                |
| json                     | 4.93 ms                                                      | 5.31 ms: 1.08x slower                                                |
| unpickle_list            | 4.71 us                                                      | 5.11 us: 1.08x slower                                                |
| sqlite_synth             | 2.21 us                                                      | 2.50 us: 1.13x slower                                                |
| scimark_sparse_mat_mult  | 4.71 ms                                                      | 5.35 ms: 1.14x slower                                                |
| regex_v8                 | 22.7 ms                                                      | 25.9 ms: 1.14x slower                                                |
| asyncio_tcp              | 505 ms                                                       | 580 ms: 1.15x slower                                                 |
| xml_etree_iterparse      | 94.9 ms                                                      | 109 ms: 1.15x slower                                                 |
| scimark_fft              | 349 ms                                                       | 404 ms: 1.16x slower                                                 |
| pathlib                  | 19.2 ms                                                      | 22.3 ms: 1.16x slower                                                |
| asyncio_tcp_ssl          | 1.51 sec                                                     | 1.83 sec: 1.21x slower                                               |
| telco                    | 7.82 ms                                                      | 9.57 ms: 1.22x slower                                                |
| coverage                 | 83.0 ms                                                      | 103 ms: 1.24x slower                                                 |
| deepcopy                 | 355 us                                                       | 445 us: 1.25x slower                                                 |
| docutils                 | 2.62 sec                                                     | 3.37 sec: 1.29x slower                                               |
| async_generators         | 377 ms                                                       | 495 ms: 1.31x slower                                                 |
| coroutines               | 23.6 ms                                                      | 31.2 ms: 1.33x slower                                                |
| pylint                   | 317 ms                                                       | 422 ms: 1.33x slower                                                 |
| xml_etree_generate       | 85.4 ms                                                      | 114 ms: 1.33x slower                                                 |
| mdp                      | 2.36 sec                                                     | 3.18 sec: 1.35x slower                                               |
| python_startup_no_site   | 7.39 ms                                                      | 10.2 ms: 1.38x slower                                                |
| deepcopy_memo            | 39.1 us                                                      | 54.3 us: 1.39x slower                                                |
| dulwich_log              | 74.8 ms                                                      | 104 ms: 1.39x slower                                                 |
| meteor_contest           | 102 ms                                                       | 141 ms: 1.39x slower                                                 |
| bpe_tokeniser            | 4.45 sec                                                     | 6.22 sec: 1.40x slower                                               |
| spectral_norm            | 111 ms                                                       | 156 ms: 1.41x slower                                                 |
| python_startup           | 11.0 ms                                                      | 15.7 ms: 1.43x slower                                                |
| tornado_http             | 114 ms                                                       | 165 ms: 1.45x slower                                                 |
| json_dumps               | 10.5 ms                                                      | 15.3 ms: 1.45x slower                                                |
| generators               | 28.8 ms                                                      | 42.1 ms: 1.46x slower                                                |
| nqueens                  | 78.6 ms                                                      | 115 ms: 1.46x slower                                                 |
| deepcopy_reduce          | 3.11 us                                                      | 4.67 us: 1.50x slower                                                |
| fannkuch                 | 370 ms                                                       | 570 ms: 1.54x slower                                                 |
| pycparser                | 1.12 sec                                                     | 1.73 sec: 1.55x slower                                               |
| xml_etree_process        | 59.3 ms                                                      | 93.1 ms: 1.57x slower                                                |
| html5lib                 | 67.0 ms                                                      | 106 ms: 1.58x slower                                                 |
| typing_runtime_protocols | 155 us                                                       | 248 us: 1.61x slower                                                 |
| 2to3                     | 260 ms                                                       | 419 ms: 1.62x slower                                                 |
| crypto_pyaes             | 67.9 ms                                                      | 110 ms: 1.62x slower                                                 |
| tomli_loads              | 2.01 sec                                                     | 3.27 sec: 1.63x slower                                               |
| thrift                   | 778 us                                                       | 1.30 ms: 1.67x slower                                                |
| sympy_integrate          | 19.8 ms                                                      | 33.2 ms: 1.67x slower                                                |
| genshi_xml               | 48.8 ms                                                      | 83.5 ms: 1.71x slower                                                |
| sqlglot_normalize        | 106 ms                                                       | 183 ms: 1.73x slower                                                 |
| sqlglot_optimize         | 52.7 ms                                                      | 91.5 ms: 1.73x slower                                                |
| pyflate                  | 449 ms                                                       | 785 ms: 1.75x slower                                                 |
| regex_compile            | 132 ms                                                       | 233 ms: 1.76x slower                                                 |
| pprint_safe_repr         | 738 ms                                                       | 1.36 sec: 1.84x slower                                               |
| mako                     | 11.3 ms                                                      | 21.1 ms: 1.86x slower                                                |
| comprehensions           | 16.5 us                                                      | 30.6 us: 1.86x slower                                                |
| genshi_text              | 21.5 ms                                                      | 40.4 ms: 1.88x slower                                                |
| pprint_pformat           | 1.50 sec                                                     | 2.83 sec: 1.89x slower                                               |
| django_template          | 34.1 ms                                                      | 65.4 ms: 1.92x slower                                                |
| scimark_monte_carlo      | 65.4 ms                                                      | 126 ms: 1.93x slower                                                 |
| float                    | 77.5 ms                                                      | 151 ms: 1.95x slower                                                 |
| logging_format           | 6.84 us                                                      | 13.5 us: 1.97x slower                                                |
| sympy_str                | 275 ms                                                       | 543 ms: 1.98x slower                                                 |
| richards                 | 45.2 ms                                                      | 89.4 ms: 1.98x slower                                                |
| logging_simple           | 6.16 us                                                      | 12.3 us: 1.99x slower                                                |
| scimark_sor              | 134 ms                                                       | 268 ms: 1.99x slower                                                 |
| unpickle_pure_python     | 210 us                                                       | 425 us: 2.02x slower                                                 |
| richards_super           | 51.6 ms                                                      | 108 ms: 2.09x slower                                                 |
| hexiom                   | 5.99 ms                                                      | 12.6 ms: 2.10x slower                                                |
| pickle_pure_python       | 294 us                                                       | 623 us: 2.11x slower                                                 |
| chaos                    | 57.3 ms                                                      | 122 ms: 2.12x slower                                                 |
| scimark_lu               | 113 ms                                                       | 240 ms: 2.13x slower                                                 |
| logging_silent           | 103 ns                                                       | 219 ns: 2.14x slower                                                 |
| go                       | 141 ms                                                       | 302 ms: 2.15x slower                                                 |
| sqlglot_transpile        | 1.56 ms                                                      | 3.37 ms: 2.16x slower                                                |
| nbody                    | 85.1 ms                                                      | 196 ms: 2.30x slower                                                 |
| sympy_expand             | 457 ms                                                       | 1.06 sec: 2.32x slower                                               |
| sqlglot_parse            | 1.25 ms                                                      | 2.91 ms: 2.33x slower                                                |
| sympy_sum                | 156 ms                                                       | 382 ms: 2.46x slower                                                 |
| raytrace                 | 253 ms                                                       | 627 ms: 2.48x slower                                                 |
| deltablue                | 3.12 ms                                                      | 9.10 ms: 2.91x slower                                                |
| unpack_sequence          | 44.8 ns                                                      | 138 ns: 3.08x slower                                                 |
| bench_thread_pool        | 919 us                                                       | 3.48 ms: 3.79x slower                                                |
| bench_mp_pool            | 11.0 ms                                                      | 71.9 ms: 6.54x slower                                                |
| Geometric mean           | (ref)                                                        | 1.57x slower                                                         |

Benchmark hidden because not significant (3): pickle_list, asyncio_websockets, pickle_dict
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.47x
- 95% likely to have a slowdown of 1.45x
- 99% likely to have a slowdown of 1.40x

# Memory
- memory change: 1.20x