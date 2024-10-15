# Results vs. base

- fork: mpage
- ref: gh_115999_tlbc_load_
- machine: linux-x86_64
- commit hash: cf0f4ec
- commit date: 2024-10-14
- overall geometric mean: 1.06x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.03x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241013-vultr-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db | bm-20241014-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-cf0f4ec |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 413 ms                                                                | 404 ms: 1.02x faster                                                 |
| docutils       | 3.32 sec                                                              | 3.22 sec: 1.03x faster                                               |
| html5lib       | 104 ms                                                                | 100 ms: 1.04x faster                                                 |
| tornado_http   | 163 ms                                                                | 158 ms: 1.03x faster                                                 |
| Geometric mean | (ref)                                                                 | 1.03x faster                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20241013-vultr-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db | bm-20241014-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-cf0f4ec |
|--------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| coroutines         | 32.1 ms                                                               | 28.1 ms: 1.14x faster                                                |
| async_generators   | 492 ms                                                                | 482 ms: 1.02x faster                                                 |
| asyncio_tcp        | 575 ms                                                                | 569 ms: 1.01x faster                                                 |
| asyncio_websockets | 523 ms                                                                | 519 ms: 1.01x faster                                                 |
| asyncio_tcp_ssl    | 1.70 sec                                                              | 1.81 sec: 1.06x slower                                               |
| Geometric mean     | (ref)                                                                 | 1.02x faster                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241013-vultr-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db | bm-20241014-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-cf0f4ec |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| nbody          | 224 ms                                                                | 184 ms: 1.22x faster                                                 |
| float          | 154 ms                                                                | 145 ms: 1.06x faster                                                 |
| pidigits       | 187 ms                                                                | 184 ms: 1.02x faster                                                 |
| Geometric mean | (ref)                                                                 | 1.10x faster                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241013-vultr-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db | bm-20241014-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-cf0f4ec |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_compile  | 228 ms                                                                | 204 ms: 1.12x faster                                                 |
| regex_v8       | 24.5 ms                                                               | 25.0 ms: 1.02x slower                                                |
| regex_effbot   | 2.96 ms                                                               | 3.06 ms: 1.04x slower                                                |
| regex_dna      | 170 ms                                                                | 189 ms: 1.12x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.01x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241013-vultr-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db | bm-20241014-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-cf0f4ec |
|----------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pickle_pure_python   | 617 us                                                                | 557 us: 1.11x faster                                                 |
| tomli_loads          | 3.31 sec                                                              | 2.99 sec: 1.11x faster                                               |
| unpickle_pure_python | 419 us                                                                | 379 us: 1.11x faster                                                 |
| xml_etree_process    | 93.6 ms                                                               | 85.8 ms: 1.09x faster                                                |
| xml_etree_generate   | 114 ms                                                                | 106 ms: 1.08x faster                                                 |
| xml_etree_iterparse  | 109 ms                                                                | 102 ms: 1.07x faster                                                 |
| json_dumps           | 15.3 ms                                                               | 14.6 ms: 1.05x faster                                                |
| json_loads           | 29.7 us                                                               | 28.7 us: 1.04x faster                                                |
| pickle_dict          | 32.4 us                                                               | 31.7 us: 1.02x faster                                                |
| xml_etree_parse      | 134 ms                                                                | 132 ms: 1.01x faster                                                 |
| pickle_list          | 4.88 us                                                               | 4.85 us: 1.01x faster                                                |
| unpickle_list        | 5.05 us                                                               | 5.21 us: 1.03x slower                                                |
| Geometric mean       | (ref)                                                                 | 1.04x faster                                                         |

Benchmark hidden because not significant (2): unpickle, pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241013-vultr-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db | bm-20241014-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-cf0f4ec |
|------------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 10.1 ms                                                               | 10.2 ms: 1.01x slower                                                |
| python_startup         | 15.5 ms                                                               | 15.6 ms: 1.01x slower                                                |
| Geometric mean         | (ref)                                                                 | 1.01x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241013-vultr-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db | bm-20241014-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-cf0f4ec |
|-----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 82.7 ms                                                               | 73.0 ms: 1.13x faster                                                |
| django_template | 65.0 ms                                                               | 58.0 ms: 1.12x faster                                                |
| genshi_text     | 39.9 ms                                                               | 35.7 ms: 1.12x faster                                                |
| mako            | 20.9 ms                                                               | 20.0 ms: 1.05x faster                                                |
| Geometric mean  | (ref)                                                                 | 1.10x faster                                                         |

All benchmarks:
===============

| Benchmark                | bm-20241013-vultr-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db | bm-20241014-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-cf0f4ec |
|--------------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| spectral_norm            | 179 ms                                                                | 145 ms: 1.23x faster                                                 |
| nbody                    | 224 ms                                                                | 184 ms: 1.22x faster                                                 |
| scimark_lu               | 246 ms                                                                | 206 ms: 1.19x faster                                                 |
| deepcopy_reduce          | 4.64 us                                                               | 3.92 us: 1.18x faster                                                |
| pprint_safe_repr         | 1.35 sec                                                              | 1.15 sec: 1.17x faster                                               |
| deepcopy_memo            | 53.8 us                                                               | 46.0 us: 1.17x faster                                                |
| deepcopy                 | 439 us                                                                | 376 us: 1.17x faster                                                 |
| pprint_pformat           | 2.80 sec                                                              | 2.40 sec: 1.17x faster                                               |
| scimark_fft              | 456 ms                                                                | 392 ms: 1.16x faster                                                 |
| scimark_sparse_mat_mult  | 6.16 ms                                                               | 5.34 ms: 1.15x faster                                                |
| typing_runtime_protocols | 246 us                                                                | 213 us: 1.15x faster                                                 |
| chaos                    | 131 ms                                                                | 114 ms: 1.14x faster                                                 |
| coroutines               | 32.1 ms                                                               | 28.1 ms: 1.14x faster                                                |
| genshi_xml               | 82.7 ms                                                               | 73.0 ms: 1.13x faster                                                |
| sqlglot_normalize        | 179 ms                                                                | 158 ms: 1.13x faster                                                 |
| sqlglot_optimize         | 90.0 ms                                                               | 80.0 ms: 1.12x faster                                                |
| django_template          | 65.0 ms                                                               | 58.0 ms: 1.12x faster                                                |
| genshi_text              | 39.9 ms                                                               | 35.7 ms: 1.12x faster                                                |
| regex_compile            | 228 ms                                                                | 204 ms: 1.12x faster                                                 |
| scimark_monte_carlo      | 132 ms                                                                | 119 ms: 1.11x faster                                                 |
| pickle_pure_python       | 617 us                                                                | 557 us: 1.11x faster                                                 |
| tomli_loads              | 3.31 sec                                                              | 2.99 sec: 1.11x faster                                               |
| unpickle_pure_python     | 419 us                                                                | 379 us: 1.11x faster                                                 |
| hexiom                   | 12.4 ms                                                               | 11.3 ms: 1.10x faster                                                |
| nqueens                  | 119 ms                                                                | 108 ms: 1.10x faster                                                 |
| xml_etree_process        | 93.6 ms                                                               | 85.8 ms: 1.09x faster                                                |
| richards_super           | 110 ms                                                                | 101 ms: 1.09x faster                                                 |
| scimark_sor              | 279 ms                                                                | 257 ms: 1.09x faster                                                 |
| bpe_tokeniser            | 6.25 sec                                                              | 5.76 sec: 1.09x faster                                               |
| unpack_sequence          | 143 ns                                                                | 132 ns: 1.09x faster                                                 |
| xml_etree_generate       | 114 ms                                                                | 106 ms: 1.08x faster                                                 |
| xml_etree_iterparse      | 109 ms                                                                | 102 ms: 1.07x faster                                                 |
| richards                 | 89.9 ms                                                               | 83.8 ms: 1.07x faster                                                |
| fannkuch                 | 584 ms                                                                | 547 ms: 1.07x faster                                                 |
| coverage                 | 106 ms                                                                | 99.6 ms: 1.06x faster                                                |
| pyflate                  | 795 ms                                                                | 750 ms: 1.06x faster                                                 |
| float                    | 154 ms                                                                | 145 ms: 1.06x faster                                                 |
| pycparser                | 1.74 sec                                                              | 1.64 sec: 1.06x faster                                               |
| json                     | 5.44 ms                                                               | 5.16 ms: 1.06x faster                                                |
| deltablue                | 9.05 ms                                                               | 8.61 ms: 1.05x faster                                                |
| go                       | 301 ms                                                                | 286 ms: 1.05x faster                                                 |
| logging_simple           | 12.0 us                                                               | 11.4 us: 1.05x faster                                                |
| raytrace                 | 648 ms                                                                | 617 ms: 1.05x faster                                                 |
| generators               | 41.5 ms                                                               | 39.6 ms: 1.05x faster                                                |
| logging_format           | 13.1 us                                                               | 12.5 us: 1.05x faster                                                |
| crypto_pyaes             | 111 ms                                                                | 105 ms: 1.05x faster                                                 |
| json_dumps               | 15.3 ms                                                               | 14.6 ms: 1.05x faster                                                |
| pathlib                  | 22.2 ms                                                               | 21.2 ms: 1.05x faster                                                |
| mako                     | 20.9 ms                                                               | 20.0 ms: 1.05x faster                                                |
| sympy_integrate          | 32.9 ms                                                               | 31.6 ms: 1.04x faster                                                |
| dulwich_log              | 104 ms                                                                | 99.4 ms: 1.04x faster                                                |
| logging_silent           | 215 ns                                                                | 207 ns: 1.04x faster                                                 |
| sympy_str                | 539 ms                                                                | 517 ms: 1.04x faster                                                 |
| pylint                   | 416 ms                                                                | 400 ms: 1.04x faster                                                 |
| mdp                      | 3.07 sec                                                              | 2.96 sec: 1.04x faster                                               |
| sqlglot_parse            | 2.88 ms                                                               | 2.78 ms: 1.04x faster                                                |
| sqlite_synth             | 2.51 us                                                               | 2.42 us: 1.04x faster                                                |
| json_loads               | 29.7 us                                                               | 28.7 us: 1.04x faster                                                |
| sympy_expand             | 1.06 sec                                                              | 1.02 sec: 1.04x faster                                               |
| html5lib                 | 104 ms                                                                | 100 ms: 1.04x faster                                                 |
| comprehensions           | 30.3 us                                                               | 29.3 us: 1.03x faster                                                |
| tornado_http             | 163 ms                                                                | 158 ms: 1.03x faster                                                 |
| sqlglot_transpile        | 3.33 ms                                                               | 3.23 ms: 1.03x faster                                                |
| docutils                 | 3.32 sec                                                              | 3.22 sec: 1.03x faster                                               |
| meteor_contest           | 139 ms                                                                | 136 ms: 1.03x faster                                                 |
| create_gc_cycles         | 1.13 ms                                                               | 1.10 ms: 1.03x faster                                                |
| sympy_sum                | 379 ms                                                                | 369 ms: 1.03x faster                                                 |
| telco                    | 9.71 ms                                                               | 9.49 ms: 1.02x faster                                                |
| 2to3                     | 413 ms                                                                | 404 ms: 1.02x faster                                                 |
| pickle_dict              | 32.4 us                                                               | 31.7 us: 1.02x faster                                                |
| async_generators         | 492 ms                                                                | 482 ms: 1.02x faster                                                 |
| pidigits                 | 187 ms                                                                | 184 ms: 1.02x faster                                                 |
| thrift                   | 1.26 ms                                                               | 1.24 ms: 1.01x faster                                                |
| xml_etree_parse          | 134 ms                                                                | 132 ms: 1.01x faster                                                 |
| asyncio_tcp              | 575 ms                                                                | 569 ms: 1.01x faster                                                 |
| gc_traversal             | 2.47 ms                                                               | 2.45 ms: 1.01x faster                                                |
| asyncio_websockets       | 523 ms                                                                | 519 ms: 1.01x faster                                                 |
| pickle_list              | 4.88 us                                                               | 4.85 us: 1.01x faster                                                |
| bench_mp_pool            | 70.7 ms                                                               | 71.1 ms: 1.01x slower                                                |
| python_startup_no_site   | 10.1 ms                                                               | 10.2 ms: 1.01x slower                                                |
| python_startup           | 15.5 ms                                                               | 15.6 ms: 1.01x slower                                                |
| regex_v8                 | 24.5 ms                                                               | 25.0 ms: 1.02x slower                                                |
| unpickle_list            | 5.05 us                                                               | 5.21 us: 1.03x slower                                                |
| regex_effbot             | 2.96 ms                                                               | 3.06 ms: 1.04x slower                                                |
| asyncio_tcp_ssl          | 1.70 sec                                                              | 1.81 sec: 1.06x slower                                               |
| bench_thread_pool        | 3.17 ms                                                               | 3.44 ms: 1.09x slower                                                |
| regex_dna                | 170 ms                                                                | 189 ms: 1.12x slower                                                 |
| Geometric mean           | (ref)                                                                 | 1.06x faster                                                         |

Benchmark hidden because not significant (2): unpickle, pickle

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.03x