# Results vs. base

- fork: mpage
- ref: gh_115999_tlbc_call
- machine: linux-x86_64
- commit hash: 819f30a
- commit date: 2024-10-18
- overall geometric mean: 1.03x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241013-vultr-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db | bm-20241018-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-819f30a |
|----------------|:---------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 413 ms                                                                | 410 ms: 1.01x faster                                                |
| docutils       | 3.32 sec                                                              | 3.28 sec: 1.01x faster                                              |
| Geometric mean | (ref)                                                                 | 1.01x faster                                                        |

Benchmark hidden because not significant (2): html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20241013-vultr-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db | bm-20241018-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-819f30a |
|--------------------|:---------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| coroutines         | 32.1 ms                                                               | 29.2 ms: 1.10x faster                                               |
| asyncio_websockets | 523 ms                                                                | 519 ms: 1.01x faster                                                |
| asyncio_tcp        | 575 ms                                                                | 582 ms: 1.01x slower                                                |
| async_generators   | 492 ms                                                                | 500 ms: 1.02x slower                                                |
| asyncio_tcp_ssl    | 1.70 sec                                                              | 1.82 sec: 1.07x slower                                              |
| Geometric mean     | (ref)                                                                 | 1.00x faster                                                        |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241013-vultr-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db | bm-20241018-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-819f30a |
|----------------|:---------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| nbody          | 224 ms                                                                | 186 ms: 1.20x faster                                                |
| float          | 154 ms                                                                | 146 ms: 1.05x faster                                                |
| pidigits       | 187 ms                                                                | 184 ms: 1.02x faster                                                |
| Geometric mean | (ref)                                                                 | 1.09x faster                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241013-vultr-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db | bm-20241018-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-819f30a |
|----------------|:---------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_compile  | 228 ms                                                                | 221 ms: 1.03x faster                                                |
| regex_v8       | 24.5 ms                                                               | 25.3 ms: 1.03x slower                                               |
| regex_effbot   | 2.96 ms                                                               | 3.21 ms: 1.08x slower                                               |
| regex_dna      | 170 ms                                                                | 191 ms: 1.13x slower                                                |
| Geometric mean | (ref)                                                                 | 1.05x slower                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241013-vultr-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db | bm-20241018-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-819f30a |
|----------------------|:---------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| unpickle_pure_python | 419 us                                                                | 386 us: 1.08x faster                                                |
| pickle_pure_python   | 617 us                                                                | 584 us: 1.06x faster                                                |
| xml_etree_process    | 93.6 ms                                                               | 89.1 ms: 1.05x faster                                               |
| json_loads           | 29.7 us                                                               | 28.3 us: 1.05x faster                                               |
| xml_etree_generate   | 114 ms                                                                | 109 ms: 1.05x faster                                                |
| pickle_dict          | 32.4 us                                                               | 31.1 us: 1.04x faster                                               |
| tomli_loads          | 3.31 sec                                                              | 3.21 sec: 1.03x faster                                              |
| xml_etree_iterparse  | 109 ms                                                                | 106 ms: 1.03x faster                                                |
| json_dumps           | 15.3 ms                                                               | 15.0 ms: 1.02x faster                                               |
| xml_etree_parse      | 134 ms                                                                | 132 ms: 1.02x faster                                                |
| pickle               | 11.0 us                                                               | 10.8 us: 1.01x faster                                               |
| pickle_list          | 4.88 us                                                               | 4.90 us: 1.00x slower                                               |
| unpickle_list        | 5.05 us                                                               | 5.14 us: 1.02x slower                                               |
| Geometric mean       | (ref)                                                                 | 1.03x faster                                                        |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241013-vultr-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db | bm-20241018-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-819f30a |
|------------------------|:---------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup         | 15.5 ms                                                               | 15.7 ms: 1.02x slower                                               |
| python_startup_no_site | 10.1 ms                                                               | 10.3 ms: 1.02x slower                                               |
| Geometric mean         | (ref)                                                                 | 1.02x slower                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241013-vultr-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db | bm-20241018-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-819f30a |
|-----------------|:---------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| mako            | 20.9 ms                                                               | 19.3 ms: 1.08x faster                                               |
| django_template | 65.0 ms                                                               | 62.1 ms: 1.05x faster                                               |
| genshi_xml      | 82.7 ms                                                               | 80.6 ms: 1.03x faster                                               |
| genshi_text     | 39.9 ms                                                               | 39.2 ms: 1.02x faster                                               |
| Geometric mean  | (ref)                                                                 | 1.04x faster                                                        |

All benchmarks:
===============

| Benchmark                | bm-20241013-vultr-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db | bm-20241018-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-819f30a |
|--------------------------|:---------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| spectral_norm            | 179 ms                                                                | 147 ms: 1.21x faster                                                |
| nbody                    | 224 ms                                                                | 186 ms: 1.20x faster                                                |
| scimark_fft              | 456 ms                                                                | 401 ms: 1.14x faster                                                |
| scimark_sparse_mat_mult  | 6.16 ms                                                               | 5.52 ms: 1.12x faster                                               |
| coroutines               | 32.1 ms                                                               | 29.2 ms: 1.10x faster                                               |
| chaos                    | 131 ms                                                                | 119 ms: 1.10x faster                                                |
| bpe_tokeniser            | 6.25 sec                                                              | 5.76 sec: 1.09x faster                                              |
| unpickle_pure_python     | 419 us                                                                | 386 us: 1.08x faster                                                |
| mako                     | 20.9 ms                                                               | 19.3 ms: 1.08x faster                                               |
| scimark_monte_carlo      | 132 ms                                                                | 123 ms: 1.08x faster                                                |
| unpack_sequence          | 143 ns                                                                | 133 ns: 1.08x faster                                                |
| pprint_safe_repr         | 1.35 sec                                                              | 1.26 sec: 1.07x faster                                              |
| pprint_pformat           | 2.80 sec                                                              | 2.61 sec: 1.07x faster                                              |
| deepcopy_memo            | 53.8 us                                                               | 50.3 us: 1.07x faster                                               |
| pyflate                  | 795 ms                                                                | 744 ms: 1.07x faster                                                |
| nqueens                  | 119 ms                                                                | 111 ms: 1.07x faster                                                |
| deepcopy_reduce          | 4.64 us                                                               | 4.34 us: 1.07x faster                                               |
| hexiom                   | 12.4 ms                                                               | 11.7 ms: 1.06x faster                                               |
| deepcopy                 | 439 us                                                                | 414 us: 1.06x faster                                                |
| scimark_sor              | 279 ms                                                                | 263 ms: 1.06x faster                                                |
| pickle_pure_python       | 617 us                                                                | 584 us: 1.06x faster                                                |
| raytrace                 | 648 ms                                                                | 614 ms: 1.06x faster                                                |
| fannkuch                 | 584 ms                                                                | 554 ms: 1.05x faster                                                |
| float                    | 154 ms                                                                | 146 ms: 1.05x faster                                                |
| scimark_lu               | 246 ms                                                                | 233 ms: 1.05x faster                                                |
| coverage                 | 106 ms                                                                | 101 ms: 1.05x faster                                                |
| xml_etree_process        | 93.6 ms                                                               | 89.1 ms: 1.05x faster                                               |
| json_loads               | 29.7 us                                                               | 28.3 us: 1.05x faster                                               |
| xml_etree_generate       | 114 ms                                                                | 109 ms: 1.05x faster                                                |
| richards_super           | 110 ms                                                                | 105 ms: 1.05x faster                                                |
| json                     | 5.44 ms                                                               | 5.20 ms: 1.05x faster                                               |
| django_template          | 65.0 ms                                                               | 62.1 ms: 1.05x faster                                               |
| pycparser                | 1.74 sec                                                              | 1.66 sec: 1.05x faster                                              |
| pickle_dict              | 32.4 us                                                               | 31.1 us: 1.04x faster                                               |
| richards                 | 89.9 ms                                                               | 86.3 ms: 1.04x faster                                               |
| sqlglot_normalize        | 179 ms                                                                | 172 ms: 1.04x faster                                                |
| sqlite_synth             | 2.51 us                                                               | 2.42 us: 1.04x faster                                               |
| sqlglot_optimize         | 90.0 ms                                                               | 86.6 ms: 1.04x faster                                               |
| crypto_pyaes             | 111 ms                                                                | 107 ms: 1.03x faster                                                |
| regex_compile            | 228 ms                                                                | 221 ms: 1.03x faster                                                |
| deltablue                | 9.05 ms                                                               | 8.76 ms: 1.03x faster                                               |
| tomli_loads              | 3.31 sec                                                              | 3.21 sec: 1.03x faster                                              |
| logging_silent           | 215 ns                                                                | 209 ns: 1.03x faster                                                |
| comprehensions           | 30.3 us                                                               | 29.5 us: 1.03x faster                                               |
| xml_etree_iterparse      | 109 ms                                                                | 106 ms: 1.03x faster                                                |
| genshi_xml               | 82.7 ms                                                               | 80.6 ms: 1.03x faster                                               |
| meteor_contest           | 139 ms                                                                | 136 ms: 1.02x faster                                                |
| json_dumps               | 15.3 ms                                                               | 15.0 ms: 1.02x faster                                               |
| sympy_integrate          | 32.9 ms                                                               | 32.2 ms: 1.02x faster                                               |
| typing_runtime_protocols | 246 us                                                                | 241 us: 1.02x faster                                                |
| sqlglot_transpile        | 3.33 ms                                                               | 3.26 ms: 1.02x faster                                               |
| telco                    | 9.71 ms                                                               | 9.53 ms: 1.02x faster                                               |
| sympy_expand             | 1.06 sec                                                              | 1.04 sec: 1.02x faster                                              |
| genshi_text              | 39.9 ms                                                               | 39.2 ms: 1.02x faster                                               |
| xml_etree_parse          | 134 ms                                                                | 132 ms: 1.02x faster                                                |
| dulwich_log              | 104 ms                                                                | 102 ms: 1.02x faster                                                |
| pidigits                 | 187 ms                                                                | 184 ms: 1.02x faster                                                |
| go                       | 301 ms                                                                | 296 ms: 1.01x faster                                                |
| pickle                   | 11.0 us                                                               | 10.8 us: 1.01x faster                                               |
| sympy_str                | 539 ms                                                                | 531 ms: 1.01x faster                                                |
| sqlglot_parse            | 2.88 ms                                                               | 2.84 ms: 1.01x faster                                               |
| pathlib                  | 22.2 ms                                                               | 21.9 ms: 1.01x faster                                               |
| docutils                 | 3.32 sec                                                              | 3.28 sec: 1.01x faster                                              |
| 2to3                     | 413 ms                                                                | 410 ms: 1.01x faster                                                |
| asyncio_websockets       | 523 ms                                                                | 519 ms: 1.01x faster                                                |
| create_gc_cycles         | 1.13 ms                                                               | 1.13 ms: 1.01x faster                                               |
| pickle_list              | 4.88 us                                                               | 4.90 us: 1.00x slower                                               |
| asyncio_tcp              | 575 ms                                                                | 582 ms: 1.01x slower                                                |
| thrift                   | 1.26 ms                                                               | 1.28 ms: 1.01x slower                                               |
| python_startup           | 15.5 ms                                                               | 15.7 ms: 1.02x slower                                               |
| async_generators         | 492 ms                                                                | 500 ms: 1.02x slower                                                |
| bench_mp_pool            | 70.7 ms                                                               | 71.9 ms: 1.02x slower                                               |
| python_startup_no_site   | 10.1 ms                                                               | 10.3 ms: 1.02x slower                                               |
| unpickle_list            | 5.05 us                                                               | 5.14 us: 1.02x slower                                               |
| mdp                      | 3.07 sec                                                              | 3.13 sec: 1.02x slower                                              |
| regex_v8                 | 24.5 ms                                                               | 25.3 ms: 1.03x slower                                               |
| generators               | 41.5 ms                                                               | 43.1 ms: 1.04x slower                                               |
| asyncio_tcp_ssl          | 1.70 sec                                                              | 1.82 sec: 1.07x slower                                              |
| regex_effbot             | 2.96 ms                                                               | 3.21 ms: 1.08x slower                                               |
| bench_thread_pool        | 3.17 ms                                                               | 3.46 ms: 1.09x slower                                               |
| regex_dna                | 170 ms                                                                | 191 ms: 1.13x slower                                                |
| Geometric mean           | (ref)                                                                 | 1.03x faster                                                        |

Benchmark hidden because not significant (8): pylint, gc_traversal, html5lib, tornado_http, sympy_sum, logging_format, logging_simple, unpickle

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.02x