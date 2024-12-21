# NextAuth Session Undefined in API Route

This repository demonstrates a common issue when using NextAuth.js with API routes: the session object is consistently undefined, even though authentication appears successful.

## Problem Description

The `session` object returned by `unstable_getServerSession` is always `null` in the API route, regardless of authentication status. This is inconsistent with behavior in pages, which correctly retrieve the session.

## Solution

The solution typically involves correctly importing `unstable_getServerSession` and ensuring the API route has access to the request and response objects.