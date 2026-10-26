<!--
  <meta:header>
    <meta:licence>
      Copyright (C) 2026 by Wizzard Solutions Ltd, wizzard@metagrid.co.uk

      This information is free software: you can redistribute it and/or modify
      it under the terms of the GNU General Public License as published by
      the Free Software Foundation, either version 3 of the License, or
      (at your option) any later version.

      This information is distributed in the hope that it will be useful,
      but WITHOUT ANY WARRANTY; without even the implied warranty of
      MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
      GNU General Public License for more details.

      You should have received a copy of the GNU General Public License
      along with this program.  If not, see <http://www.gnu.org/licenses/>.
    </meta:licence>
  </meta:header>

  AIMetrics: [
      {
      "interval": "2026-10-26T05:06:08/2026-10-26T05:08:00",
      "name": "@deepseek-ai/dsh",
      "version": "0.2.0-rc.2",
      "model": "deepseek-v4.1-flash-1017",
      "contribution": {
        "value": 100,
        "units": "%"
        }
      }
    ]
-->

# Deprecated: `dsh/`

This directory no longer holds the harness home. It is an empty placeholder,
kept only so that an older clone, note or command that expects `dsh/` to exist
does not silently start writing to a new, local directory instead.

The live DeepSeek Harness home is a **separate directory on the host**, mounted
over `/opt/dsh`:

```bash
--env    "DSH_HOME=/opt/dsh" \
--volume "${DSH_HOME:?}:/opt/dsh:rw,Z" \
```

That host directory holds the sessions, storages, profiles, backups and
`.credentials.yaml`. It is backed up independently and must not be copied back
into this repository.

Do not write here. See [Running the container](../README.md#running-the-container)
and the current launch note `notes/20261025-03-launch.txt`.

This placeholder can be removed once the project split has stabilised.
