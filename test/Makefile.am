## Licensed under the Apache License, Version 2.0 (the "License"); you may not
## use this file except in compliance with the License. You may obtain a copy of
## the License at
##
##   http://www.apache.org/licenses/LICENSE-2.0
##
## Unless required by applicable law or agreed to in writing, software
## distributed under the License is distributed on an "AS IS" BASIS, WITHOUT
## WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the
## License for the specific language governing permissions and limitations under
## the License.

noinst_SCRIPTS = run bench

DISTCLEANFILES = temp.*

EXTRA_DIST = \
	001-load-modules.t \
	002-load-driver.t

run: run.tpl
	sed -e "s|%abs_top_srcdir%|@abs_top_srcdir@|g" \
		-e "s|%abs_top_builddir%|@abs_top_builddir@|g" \
	> $@ < $<
	chmod +x $@

bench: bench.tpl
	sed -e "s|%abs_top_srcdir%|@abs_top_srcdir@|g" \
		-e "s|%abs_top_builddir%|@abs_top_builddir@|g" \
	> $@ < $<
	chmod +x $@

check:
	./run

