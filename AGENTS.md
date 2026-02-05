# AGENTS.md

This file provides guidance to WARP (warp.dev) when working with code in this repository.

## Project Overview

A minimal Python web application using the Pyramid framework. Serves a configurable greeting message at the root endpoint.

## Commands

### Install dependencies
```powershell
pip install -r requirements.txt
```

### Run the server
```powershell
python server.py
```
Requires `PORT` environment variable to be set. Optionally set `NAME` to customize the greeting.

### Run with environment variables (Windows PowerShell)
```powershell
$env:PORT=8000; $env:NAME="World"; python server.py
```

## Architecture

- `server.py` - Single-file Pyramid WSGI application with one route (`/`) that returns a greeting message
- Environment variables:
  - `PORT` (required) - Server port
  - `NAME` (optional) - Name used in greeting, defaults to "world"
