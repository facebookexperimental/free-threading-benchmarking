# Results vs. base

- fork: mpage
- ref: gh_115999_tlbc_load_
- machine: linux-x86_64
- commit hash: a76e4f5
- commit date: 2024-10-14
- overall geometric mean: 1.00x faster
- HPT reliability: 85.95%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241013-vultr-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db | bm-20241014-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-a76e4f5 |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 413 ms                                                                | 419 ms: 1.02x slower                                                 |
| docutils       | 3.32 sec                                                              | 3.37 sec: 1.01x slower                                               |
| html5lib       | 104 ms                                                                | 106 ms: 1.02x slower                                                 |
| tornado_http   | 163 ms                                                                | 165 ms: 1.01x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.02x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20241013-vultr-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db | bm-20241014-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-a76e4f5 |
|--------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| coroutines         | 32.1 ms                                                               | 31.2 ms: 1.03x faster                                                |
| asyncio_websockets | 523 ms                                                                | 520 ms: 1.00x faster                                                 |
| async_generators   | 492 ms                                                                | 495 ms: 1.01x slower                                                 |
| asyncio_tcp        | 575 ms                                                                | 580 ms: 1.01x slower                                                 |
| asyncio_tcp_ssl    | 1.70 sec                                                              | 1.83 sec: 1.07x slower                                               |
| Geometric mean     | (ref)                                                                 | 1.01x slower                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241013-vultr-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db | bm-20241014-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-a76e4f5 |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| nbody          | 224 ms                                                                | 196 ms: 1.14x faster                                                 |
| float          | 154 ms                                                                | 151 ms: 1.02x faster                                                 |
| pidigits       | 187 ms                                                                | 184 ms: 1.01x faster                                                 |
| Geometric mean | (ref)                                                                 | 1.06x faster                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241013-vultr-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db | bm-20241014-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-a76e4f5 |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_compile  | 228 ms                                                                | 233 ms: 1.02x slower                                                 |
| regex_v8       | 24.5 ms                                                               | 25.9 ms: 1.06x slower                                                |
| regex_effbot   | 2.96 ms                                                               | 3.20 ms: 1.08x slower                                                |
| regex_dna      | 170 ms                                                                | 191 ms: 1.12x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.07x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241013-vultr-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db | bm-20241014-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-a76e4f5 |
|----------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| json_loads           | 29.7 us                                                               | 28.7 us: 1.04x faster                                                |
| pickle               | 11.0 us                                                               | 10.7 us: 1.03x faster                                                |
| tomli_loads          | 3.31 sec                                                              | 3.27 sec: 1.01x faster                                               |
| xml_etree_parse      | 134 ms                                                                | 133 ms: 1.01x faster                                                 |
| xml_etree_process    | 93.6 ms                                                               | 93.1 ms: 1.01x faster                                                |
| xml_etree_generate   | 114 ms                                                                | 114 ms: 1.00x faster                                                 |
| pickle_pure_python   | 617 us                                                                | 623 us: 1.01x slower                                                 |
| pickle_list          | 4.88 us                                                               | 4.93 us: 1.01x slower                                                |
| unpickle_list        | 5.05 us                                                               | 5.11 us: 1.01x slower                                                |
| unpickle_pure_python | 419 us                                                                | 425 us: 1.01x slower                                                 |
| Geometric mean       | (ref)                                                                 | 1.00x faster                                                         |

Benchmark hidden because not significant (4): json_dumps, xml_etree_iterparse, unpickle, pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241013-vultr-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db | bm-20241014-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-a76e4f5 |
|------------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 10.1 ms                                                               | 10.2 ms: 1.01x slower                                                |
| python_startup         | 15.5 ms                                                               | 15.7 ms: 1.01x slower                                                |
| Geometric mean         | (ref)                                                                 | 1.01x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241013-vultr-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db | bm-20241014-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-a76e4f5 |
|-----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| django_template | 65.0 ms                                                               | 65.4 ms: 1.01x slower                                                |
| mako            | 20.9 ms                                                               | 21.1 ms: 1.01x slower                                                |
| genshi_xml      | 82.7 ms                                                               | 83.5 ms: 1.01x slower                                                |
| genshi_text     | 39.9 ms                                                               | 40.4 ms: 1.01x slower                                                |
| Geometric mean  | (ref)                                                                 | 1.01x slower                                                         |

All benchmarks:
===============

| Benchmark                | bm-20241013-vultr-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db | bm-20241014-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-a76e4f5 |
|--------------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| scimark_sparse_mat_mult  | 6.16 ms                                                               | 5.35 ms: 1.15x faster                                                |
| nbody                    | 224 ms                                                                | 196 ms: 1.14x faster                                                 |
| spectral_norm            | 179 ms                                                                | 156 ms: 1.14x faster                                                 |
| scimark_fft              | 456 ms                                                                | 404 ms: 1.13x faster                                                 |
| chaos                    | 131 ms                                                                | 122 ms: 1.07x faster                                                 |
| scimark_monte_carlo      | 132 ms                                                                | 126 ms: 1.05x faster                                                 |
| scimark_sor              | 279 ms                                                                | 268 ms: 1.04x faster                                                 |
| unpack_sequence          | 143 ns                                                                | 138 ns: 1.04x faster                                                 |
| json_loads               | 29.7 us                                                               | 28.7 us: 1.04x faster                                                |
| raytrace                 | 648 ms                                                                | 627 ms: 1.03x faster                                                 |
| nqueens                  | 119 ms                                                                | 115 ms: 1.03x faster                                                 |
| coroutines               | 32.1 ms                                                               | 31.2 ms: 1.03x faster                                                |
| coverage                 | 106 ms                                                                | 103 ms: 1.03x faster                                                 |
| pickle                   | 11.0 us                                                               | 10.7 us: 1.03x faster                                                |
| scimark_lu               | 246 ms                                                                | 240 ms: 1.02x faster                                                 |
| json                     | 5.44 ms                                                               | 5.31 ms: 1.02x faster                                                |
| fannkuch                 | 584 ms                                                                | 570 ms: 1.02x faster                                                 |
| float                    | 154 ms                                                                | 151 ms: 1.02x faster                                                 |
| richards_super           | 110 ms                                                                | 108 ms: 1.02x faster                                                 |
| pidigits                 | 187 ms                                                                | 184 ms: 1.01x faster                                                 |
| telco                    | 9.71 ms                                                               | 9.57 ms: 1.01x faster                                                |
| tomli_loads              | 3.31 sec                                                              | 3.27 sec: 1.01x faster                                               |
| pyflate                  | 795 ms                                                                | 785 ms: 1.01x faster                                                 |
| pycparser                | 1.74 sec                                                              | 1.73 sec: 1.01x faster                                               |
| xml_etree_parse          | 134 ms                                                                | 133 ms: 1.01x faster                                                 |
| crypto_pyaes             | 111 ms                                                                | 110 ms: 1.01x faster                                                 |
| bpe_tokeniser            | 6.25 sec                                                              | 6.22 sec: 1.01x faster                                               |
| create_gc_cycles         | 1.13 ms                                                               | 1.13 ms: 1.01x faster                                                |
| xml_etree_process        | 93.6 ms                                                               | 93.1 ms: 1.01x faster                                                |
| asyncio_websockets       | 523 ms                                                                | 520 ms: 1.00x faster                                                 |
| xml_etree_generate       | 114 ms                                                                | 114 ms: 1.00x faster                                                 |
| sympy_expand             | 1.06 sec                                                              | 1.06 sec: 1.00x slower                                               |
| async_generators         | 492 ms                                                                | 495 ms: 1.01x slower                                                 |
| deltablue                | 9.05 ms                                                               | 9.10 ms: 1.01x slower                                                |
| django_template          | 65.0 ms                                                               | 65.4 ms: 1.01x slower                                                |
| sympy_str                | 539 ms                                                                | 543 ms: 1.01x slower                                                 |
| pprint_safe_repr         | 1.35 sec                                                              | 1.36 sec: 1.01x slower                                               |
| pathlib                  | 22.2 ms                                                               | 22.3 ms: 1.01x slower                                                |
| sympy_integrate          | 32.9 ms                                                               | 33.2 ms: 1.01x slower                                                |
| deepcopy_reduce          | 4.64 us                                                               | 4.67 us: 1.01x slower                                                |
| asyncio_tcp              | 575 ms                                                                | 580 ms: 1.01x slower                                                 |
| mako                     | 20.9 ms                                                               | 21.1 ms: 1.01x slower                                                |
| pickle_pure_python       | 617 us                                                                | 623 us: 1.01x slower                                                 |
| genshi_xml               | 82.7 ms                                                               | 83.5 ms: 1.01x slower                                                |
| deepcopy_memo            | 53.8 us                                                               | 54.3 us: 1.01x slower                                                |
| sympy_sum                | 379 ms                                                                | 382 ms: 1.01x slower                                                 |
| comprehensions           | 30.3 us                                                               | 30.6 us: 1.01x slower                                                |
| pprint_pformat           | 2.80 sec                                                              | 2.83 sec: 1.01x slower                                               |
| pickle_list              | 4.88 us                                                               | 4.93 us: 1.01x slower                                                |
| sqlglot_parse            | 2.88 ms                                                               | 2.91 ms: 1.01x slower                                                |
| tornado_http             | 163 ms                                                                | 165 ms: 1.01x slower                                                 |
| unpickle_list            | 5.05 us                                                               | 5.11 us: 1.01x slower                                                |
| typing_runtime_protocols | 246 us                                                                | 248 us: 1.01x slower                                                 |
| python_startup_no_site   | 10.1 ms                                                               | 10.2 ms: 1.01x slower                                                |
| generators               | 41.5 ms                                                               | 42.1 ms: 1.01x slower                                                |
| python_startup           | 15.5 ms                                                               | 15.7 ms: 1.01x slower                                                |
| sqlglot_transpile        | 3.33 ms                                                               | 3.37 ms: 1.01x slower                                                |
| genshi_text              | 39.9 ms                                                               | 40.4 ms: 1.01x slower                                                |
| hexiom                   | 12.4 ms                                                               | 12.6 ms: 1.01x slower                                                |
| deepcopy                 | 439 us                                                                | 445 us: 1.01x slower                                                 |
| meteor_contest           | 139 ms                                                                | 141 ms: 1.01x slower                                                 |
| docutils                 | 3.32 sec                                                              | 3.37 sec: 1.01x slower                                               |
| unpickle_pure_python     | 419 us                                                                | 425 us: 1.01x slower                                                 |
| 2to3                     | 413 ms                                                                | 419 ms: 1.02x slower                                                 |
| sqlglot_optimize         | 90.0 ms                                                               | 91.5 ms: 1.02x slower                                                |
| bench_mp_pool            | 70.7 ms                                                               | 71.9 ms: 1.02x slower                                                |
| regex_compile            | 228 ms                                                                | 233 ms: 1.02x slower                                                 |
| logging_silent           | 215 ns                                                                | 219 ns: 1.02x slower                                                 |
| html5lib                 | 104 ms                                                                | 106 ms: 1.02x slower                                                 |
| sqlglot_normalize        | 179 ms                                                                | 183 ms: 1.02x slower                                                 |
| logging_simple           | 12.0 us                                                               | 12.3 us: 1.02x slower                                                |
| logging_format           | 13.1 us                                                               | 13.5 us: 1.03x slower                                                |
| thrift                   | 1.26 ms                                                               | 1.30 ms: 1.03x slower                                                |
| mdp                      | 3.07 sec                                                              | 3.18 sec: 1.04x slower                                               |
| regex_v8                 | 24.5 ms                                                               | 25.9 ms: 1.06x slower                                                |
| asyncio_tcp_ssl          | 1.70 sec                                                              | 1.83 sec: 1.07x slower                                               |
| regex_effbot             | 2.96 ms                                                               | 3.20 ms: 1.08x slower                                                |
| bench_thread_pool        | 3.17 ms                                                               | 3.48 ms: 1.10x slower                                                |
| regex_dna                | 170 ms                                                                | 191 ms: 1.12x slower                                                 |
| Geometric mean           | (ref)                                                                 | 1.00x faster                                                         |

Benchmark hidden because not significant (10): richards, sqlite_synth, gc_traversal, json_dumps, xml_etree_iterparse, dulwich_log, go, unpickle, pickle_dict, pylint

# HPT report

- Reliability score: 85.95% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.02x