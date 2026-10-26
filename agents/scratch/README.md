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

# Deprecated: `agents/scratch/`

Scratch space for agents is no longer kept inside a project clone. It is a
shared mount, so every project container sees the same files:

```
/Zarquan/agents/scratch      |
/Calycopis/agents/scratch    |  the same directory
```

Both paths are the same mount in the developer container, so a file written
under one is visible under the other, and to any other container that mounts
that host directory.

This directory is an empty placeholder. Anything written here is local to this
clone and invisible to the other projects, which is exactly what the move to a
shared mount was meant to avoid.

Do not write here. See [Running the container](../../README.md#running-the-container)
and the current launch note `notes/20261025-03-launch.txt`.

This placeholder can be removed once the project split has stabilised.
