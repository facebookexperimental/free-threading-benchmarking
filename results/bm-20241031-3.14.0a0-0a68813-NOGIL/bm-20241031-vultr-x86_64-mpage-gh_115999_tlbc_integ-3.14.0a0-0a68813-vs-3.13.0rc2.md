# Results vs. 3.13.0rc2

- fork: mpage
- ref: gh_115999_tlbc_integ
- machine: linux-x86_64
- commit hash: 0a68813
- commit date: 2024-10-31
- overall geometric mean: 1.47x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.34x slower
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241031-vultr-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 407 ms: 1.57x slower                                                 |
| docutils       | 2.62 sec                                                     | 3.20 sec: 1.22x slower                                               |
| html5lib       | 67.0 ms                                                      | 101 ms: 1.50x slower                                                 |
| tornado_http   | 114 ms                                                       | 159 ms: 1.39x slower                                                 |
| Geometric mean | (ref)                                                        | 1.42x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241031-vultr-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| coroutines       | 23.6 ms                                                      | 26.9 ms: 1.14x slower                                                |
| asyncio_tcp      | 505 ms                                                       | 582 ms: 1.15x slower                                                 |
| asyncio_tcp_ssl  | 1.51 sec                                                     | 1.80 sec: 1.19x slower                                               |
| async_generators | 377 ms                                                       | 489 ms: 1.30x slower                                                 |
| Geometric mean   | (ref)                                                        | 1.15x slower                                                         |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241031-vultr-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 183 ms: 1.18x faster                                                 |
| float          | 77.5 ms                                                      | 144 ms: 1.86x slower                                                 |
| nbody          | 85.1 ms                                                      | 191 ms: 2.24x slower                                                 |
| Geometric mean | (ref)                                                        | 1.52x slower                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241031-vultr-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 3.15 ms: 1.02x slower                                                |
| regex_dna      | 180 ms                                                       | 188 ms: 1.04x slower                                                 |
| regex_v8       | 22.7 ms                                                      | 25.9 ms: 1.14x slower                                                |
| regex_compile  | 132 ms                                                       | 201 ms: 1.52x slower                                                 |
| Geometric mean | (ref)                                                        | 1.17x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241031-vultr-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pickle               | 11.3 us                                                      | 10.4 us: 1.09x faster                                                |
| pickle_dict          | 32.5 us                                                      | 31.1 us: 1.05x faster                                                |
| pickle_list          | 4.93 us                                                      | 4.79 us: 1.03x faster                                                |
| xml_etree_parse      | 136 ms                                                       | 133 ms: 1.02x faster                                                 |
| unpickle             | 14.3 us                                                      | 15.0 us: 1.05x slower                                                |
| xml_etree_iterparse  | 94.9 ms                                                      | 100 ms: 1.06x slower                                                 |
| json_loads           | 27.0 us                                                      | 28.7 us: 1.06x slower                                                |
| unpickle_list        | 4.71 us                                                      | 5.16 us: 1.10x slower                                                |
| xml_etree_generate   | 85.4 ms                                                      | 104 ms: 1.22x slower                                                 |
| json_dumps           | 10.5 ms                                                      | 14.6 ms: 1.39x slower                                                |
| xml_etree_process    | 59.3 ms                                                      | 85.2 ms: 1.43x slower                                                |
| tomli_loads          | 2.01 sec                                                     | 3.07 sec: 1.53x slower                                               |
| unpickle_pure_python | 210 us                                                       | 353 us: 1.68x slower                                                 |
| pickle_pure_python   | 294 us                                                       | 530 us: 1.80x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.19x slower                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241031-vultr-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.3 ms: 1.39x slower                                                |
| python_startup         | 11.0 ms                                                      | 15.8 ms: 1.43x slower                                                |
| Geometric mean         | (ref)                                                        | 1.41x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241031-vultr-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|-----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 73.3 ms: 1.50x slower                                                |
| mako            | 11.3 ms                                                      | 18.6 ms: 1.64x slower                                                |
| genshi_text     | 21.5 ms                                                      | 35.6 ms: 1.65x slower                                                |
| django_template | 34.1 ms                                                      | 56.5 ms: 1.66x slower                                                |
| Geometric mean  | (ref)                                                        | 1.61x slower                                                         |

All benchmarks:
===============

| Benchmark                | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241031-vultr-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|--------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| gc_traversal             | 3.14 ms                                                      | 2.48 ms: 1.27x faster                                                |
| create_gc_cycles         | 1.34 ms                                                      | 1.13 ms: 1.19x faster                                                |
| pidigits                 | 217 ms                                                       | 183 ms: 1.18x faster                                                 |
| pickle                   | 11.3 us                                                      | 10.4 us: 1.09x faster                                                |
| pickle_dict              | 32.5 us                                                      | 31.1 us: 1.05x faster                                                |
| pickle_list              | 4.93 us                                                      | 4.79 us: 1.03x faster                                                |
| xml_etree_parse          | 136 ms                                                       | 133 ms: 1.02x faster                                                 |
| deepcopy                 | 355 us                                                       | 362 us: 1.02x slower                                                 |
| regex_effbot             | 3.08 ms                                                      | 3.15 ms: 1.02x slower                                                |
| regex_dna                | 180 ms                                                       | 188 ms: 1.04x slower                                                 |
| unpickle                 | 14.3 us                                                      | 15.0 us: 1.05x slower                                                |
| xml_etree_iterparse      | 94.9 ms                                                      | 100 ms: 1.06x slower                                                 |
| json                     | 4.93 ms                                                      | 5.22 ms: 1.06x slower                                                |
| json_loads               | 27.0 us                                                      | 28.7 us: 1.06x slower                                                |
| sqlite_synth             | 2.21 us                                                      | 2.36 us: 1.07x slower                                                |
| deepcopy_memo            | 39.1 us                                                      | 42.7 us: 1.09x slower                                                |
| unpickle_list            | 4.71 us                                                      | 5.16 us: 1.10x slower                                                |
| pathlib                  | 19.2 ms                                                      | 21.1 ms: 1.10x slower                                                |
| regex_v8                 | 22.7 ms                                                      | 25.9 ms: 1.14x slower                                                |
| coroutines               | 23.6 ms                                                      | 26.9 ms: 1.14x slower                                                |
| scimark_fft              | 349 ms                                                       | 400 ms: 1.15x slower                                                 |
| asyncio_tcp              | 505 ms                                                       | 582 ms: 1.15x slower                                                 |
| scimark_sparse_mat_mult  | 4.71 ms                                                      | 5.54 ms: 1.18x slower                                                |
| asyncio_tcp_ssl          | 1.51 sec                                                     | 1.80 sec: 1.19x slower                                               |
| coverage                 | 83.0 ms                                                      | 99.8 ms: 1.20x slower                                                |
| bpe_tokeniser            | 4.45 sec                                                     | 5.38 sec: 1.21x slower                                               |
| deepcopy_reduce          | 3.11 us                                                      | 3.77 us: 1.21x slower                                                |
| telco                    | 7.82 ms                                                      | 9.52 ms: 1.22x slower                                                |
| xml_etree_generate       | 85.4 ms                                                      | 104 ms: 1.22x slower                                                 |
| docutils                 | 2.62 sec                                                     | 3.20 sec: 1.22x slower                                               |
| pylint                   | 317 ms                                                       | 400 ms: 1.26x slower                                                 |
| async_generators         | 377 ms                                                       | 489 ms: 1.30x slower                                                 |
| meteor_contest           | 102 ms                                                       | 133 ms: 1.31x slower                                                 |
| spectral_norm            | 111 ms                                                       | 147 ms: 1.33x slower                                                 |
| typing_runtime_protocols | 155 us                                                       | 207 us: 1.34x slower                                                 |
| mdp                      | 2.36 sec                                                     | 3.15 sec: 1.34x slower                                               |
| dulwich_log              | 74.8 ms                                                      | 100 ms: 1.34x slower                                                 |
| json_dumps               | 10.5 ms                                                      | 14.6 ms: 1.39x slower                                                |
| tornado_http             | 114 ms                                                       | 159 ms: 1.39x slower                                                 |
| python_startup_no_site   | 7.39 ms                                                      | 10.3 ms: 1.39x slower                                                |
| nqueens                  | 78.6 ms                                                      | 110 ms: 1.39x slower                                                 |
| python_startup           | 11.0 ms                                                      | 15.8 ms: 1.43x slower                                                |
| xml_etree_process        | 59.3 ms                                                      | 85.2 ms: 1.43x slower                                                |
| sqlglot_normalize        | 106 ms                                                       | 152 ms: 1.44x slower                                                 |
| sqlglot_optimize         | 52.7 ms                                                      | 76.9 ms: 1.46x slower                                                |
| pycparser                | 1.12 sec                                                     | 1.64 sec: 1.46x slower                                               |
| generators               | 28.8 ms                                                      | 42.5 ms: 1.47x slower                                                |
| pprint_safe_repr         | 738 ms                                                       | 1.09 sec: 1.48x slower                                               |
| html5lib                 | 67.0 ms                                                      | 101 ms: 1.50x slower                                                 |
| genshi_xml               | 48.8 ms                                                      | 73.3 ms: 1.50x slower                                                |
| fannkuch                 | 370 ms                                                       | 561 ms: 1.52x slower                                                 |
| regex_compile            | 132 ms                                                       | 201 ms: 1.52x slower                                                 |
| pprint_pformat           | 1.50 sec                                                     | 2.28 sec: 1.52x slower                                               |
| tomli_loads              | 2.01 sec                                                     | 3.07 sec: 1.53x slower                                               |
| thrift                   | 778 us                                                       | 1.22 ms: 1.56x slower                                                |
| 2to3                     | 260 ms                                                       | 407 ms: 1.57x slower                                                 |
| sympy_integrate          | 19.8 ms                                                      | 31.3 ms: 1.58x slower                                                |
| crypto_pyaes             | 67.9 ms                                                      | 107 ms: 1.58x slower                                                 |
| mako                     | 11.3 ms                                                      | 18.6 ms: 1.64x slower                                                |
| pyflate                  | 449 ms                                                       | 741 ms: 1.65x slower                                                 |
| genshi_text              | 21.5 ms                                                      | 35.6 ms: 1.65x slower                                                |
| django_template          | 34.1 ms                                                      | 56.5 ms: 1.66x slower                                                |
| unpickle_pure_python     | 210 us                                                       | 353 us: 1.68x slower                                                 |
| comprehensions           | 16.5 us                                                      | 28.8 us: 1.75x slower                                                |
| scimark_lu               | 113 ms                                                       | 202 ms: 1.79x slower                                                 |
| pickle_pure_python       | 294 us                                                       | 530 us: 1.80x slower                                                 |
| richards                 | 45.2 ms                                                      | 82.6 ms: 1.83x slower                                                |
| logging_format           | 6.84 us                                                      | 12.5 us: 1.83x slower                                                |
| scimark_monte_carlo      | 65.4 ms                                                      | 120 ms: 1.84x slower                                                 |
| logging_simple           | 6.16 us                                                      | 11.4 us: 1.85x slower                                                |
| float                    | 77.5 ms                                                      | 144 ms: 1.86x slower                                                 |
| hexiom                   | 5.99 ms                                                      | 11.2 ms: 1.87x slower                                                |
| sympy_str                | 275 ms                                                       | 513 ms: 1.87x slower                                                 |
| richards_super           | 51.6 ms                                                      | 99.7 ms: 1.93x slower                                                |
| logging_silent           | 103 ns                                                       | 199 ns: 1.94x slower                                                 |
| chaos                    | 57.3 ms                                                      | 112 ms: 1.95x slower                                                 |
| scimark_sor              | 134 ms                                                       | 264 ms: 1.96x slower                                                 |
| sqlglot_transpile        | 1.56 ms                                                      | 3.20 ms: 2.05x slower                                                |
| go                       | 141 ms                                                       | 288 ms: 2.05x slower                                                 |
| sympy_expand             | 457 ms                                                       | 1.01 sec: 2.21x slower                                               |
| sqlglot_parse            | 1.25 ms                                                      | 2.78 ms: 2.23x slower                                                |
| nbody                    | 85.1 ms                                                      | 191 ms: 2.24x slower                                                 |
| raytrace                 | 253 ms                                                       | 577 ms: 2.28x slower                                                 |
| sympy_sum                | 156 ms                                                       | 367 ms: 2.36x slower                                                 |
| deltablue                | 3.12 ms                                                      | 8.43 ms: 2.70x slower                                                |
| unpack_sequence          | 44.8 ns                                                      | 142 ns: 3.16x slower                                                 |
| bench_thread_pool        | 919 us                                                       | 3.44 ms: 3.74x slower                                                |
| bench_mp_pool            | 11.0 ms                                                      | 71.7 ms: 6.52x slower                                                |
| Geometric mean           | (ref)                                                        | 1.47x slower                                                         |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.39x
- 95% likely to have a slowdown of 1.38x
- 99% likely to have a slowdown of 1.34x

# Memory
- memory change: 1.21x