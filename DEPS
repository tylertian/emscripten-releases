# Copyright 2019 the V8 project authors. All rights reserved.
# Use of this source code is governed by a BSD-style license that can be
# found in the LICENSE file.

vars = {
  'binaryen_url': 'https://chromium.googlesource.com/external/github.com/WebAssembly/binaryen',
  'emscripten_url': 'https://chromium.googlesource.com/external/github.com/emscripten-core/emscripten',
  'fastcomp_url': 'https://chromium.googlesource.com/external/github.com/emscripten-core/emscripten-fastcomp',
  'fastcomp_clang_url': 'https://chromium.googlesource.com/external/github.com/emscripten-core/emscripten-fastcomp-clang',
  'llvm_project_url': 'https://chromium.googlesource.com/external/github.com/llvm/llvm-project',
  'v8_url': 'https://chromium.googlesource.com/v8/v8',
  'wabt_url': 'https://chromium.googlesource.com/external/github.com/WebAssembly/wabt',
  'waterfall_url': 'https://chromium.googlesource.com/external/github.com/WebAssembly/waterfall',
  # TODO: v8 for testing, Gcc for torture tests, llvm test-suite

  # Three lines of non-changing comments so that
  # the commit queue can handle CLs rolling binaryen
  # and whatever else without interference from each other.
  'binaryen_revision': '4b05489435a8f7c4a149db16a11f6c82ce63d622',
  # Three lines of non-changing comments so that
  # the commit queue can handle CLs rolling emscripten
  # and whatever else without interference from each other.
  'emscripten_revision': 'fd7700585955967040ccddc526f0f7a4729b12b4',
  # Three lines of non-changing comments so that
  # the commit queue can handle CLs rolling fastcomp
  # and whatever else without interference from each other.
  'fastcomp_revision': '1b4148f39a69c7fc62edadd85e4122b68694dfb7',
  # Three lines of non-changing comments so that
  # the commit queue can handle CLs rolling fastcomp_clang
  # and whatever else without interference from each other.
  'fastcomp_clang_revision': '98df4be387dde3e3918fa5bbb5fc43e1a0e1daac',
  # Three lines of non-changing comments so that
  # the commit queue can handle CLs rolling llvm_project
  # and whatever else without interference from each other.
  'llvm_project_revision': '26d711be6e8e6d27779afe641881c02e59cd2947',
  # Three lines of non-changing comments so that
  # the commit queue can handle CLs rolling v8
  # and whatever else without interference from each other.
  'v8_revision': 'e483fb2731c13e811783bbb4bd2a70272027c15b',
  # Three lines of non-changing comments so that
  # the commit queue can handle CLs rolling wabt
  # and whatever else without interference from each other.
  'wabt_revision': '3b8dfbff5ba95537fb1b6da151ad6a526503d405',
  # Three lines of non-changing comments so that
  # the commit queue can handle CLs rolling waterfall
  # and whatever else without interference from each other.
  'waterfall_revision': '9af67185a5f38ea54e3c597c8437854eec2f0d3f',
}

deps = {
  'emscripten-releases/binaryen': Var('binaryen_url') + '@' + Var('binaryen_revision'),
  'emscripten-releases/emscripten': Var('emscripten_url') + '@' + Var('emscripten_revision'),
  'emscripten-releases/emscripten-fastcomp': Var('fastcomp_url') + '@' + Var('fastcomp_revision'),
  'emscripten-releases/emscripten-fastcomp-clang': Var('fastcomp_clang_url') + '@' + Var('fastcomp_clang_revision'),
  'emscripten-releases/llvm-project': Var('llvm_project_url') + '@' + Var('llvm_project_revision'),
  'v8': Var('v8_url') + '@' + Var('v8_revision'),
  'emscripten-releases/wabt': Var('wabt_url') + '@' + Var('wabt_revision'),
  'emscripten-releases/waterfall': Var('waterfall_url') + '@' + Var('waterfall_revision'),
}

hooks = [
  {
    'name': 'cmake',
    'pattern': '.',
    'action': ['python', 'emscripten-releases/waterfall/src/build.py',
               '--sync-include=cmake,nodejs,java','--no-build', '--no-test',
               '--prebuilt-dir=emscripten-releases', '--v8-dir=v8'],
  },
]

recursedeps = [
  'v8'
]