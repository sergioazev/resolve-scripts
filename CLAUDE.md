# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Purpose

This repository contains operational scripts for DaVinci Resolve — scripts that have been tested and approved for active use in production workflows.

## Context

DaVinci Resolve scripting uses the Resolve API, which is accessible via Python (preferred) or Lua. Scripts interact with Resolve through its built-in scripting host; they are not run as standalone CLI tools but are executed from within Resolve's scripting console or via the Fusion page.

The Resolve Python API (`DaVinciResolveScript`) is injected at runtime by Resolve itself — it is not pip-installable. Scripts must be run inside Resolve's scripting environment or via the external scripting support that Resolve exposes on a local socket.
