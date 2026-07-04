# Tiny Reddit

## Overview

This project is a simplified system design implementation of a Reddit-like platform. It focuses on modeling the core components behind a large-scale content aggregation system, including posts, comments, voting, and feed generation.

The goal is to understand how read-heavy social platforms are structured, how ranking systems work at a high level, and how data models support scalable feed delivery.

---

## Problem Statement

Large social platforms like Reddit must efficiently handle massive amounts of user-generated content while serving fast, personalized feeds to users. This project explores how to design a simplified version of such a system that supports content creation, engagement (votes/comments), and feed retrieval while considering scalability and performance tradeoffs.

---

## Learning Objectives

- Understand read-heavy system design patterns
- Design scalable content and feed models
- Learn how voting and ranking systems influence feed ordering
- Explore tradeoffs between real-time and precomputed feeds
- Understand data modeling for social interactions
- Build intuition for high-throughput backend systems

---

## Core Features

### Content System
- Create posts
- Retrieve posts
- Organize posts by communities (subreddits conceptually)

### Interaction System
- Upvote / downvote functionality
- Comment threads (nested or flat model)
- Engagement tracking

### Feed System
- Generate home feed
- Community-specific feeds
- Sorting by time, score, or hybrid ranking

### Ranking (Conceptual)
- Score-based ranking (upvotes - downvotes)
- Time decay considerations
- Basic hot ranking algorithm

---

## Architecture (Conceptual)

### API Layer
- Handles post creation and retrieval
- Manages voting and comments
- Serves feed requests

### Data Layer
- Stores posts, comments, and votes
- Supports efficient retrieval by community or user feed

### Feed Generation Layer
- Computes or retrieves ordered post lists
- May use precomputation or on-demand aggregation (conceptual)

---

## Engineering Considerations

- Read-heavy vs write-heavy tradeoffs
- Feed generation complexity at scale
- Hot partitions (popular communities/posts)
- Ranking algorithm performance
- Consistency of votes under concurrency
- Pagination and efficient querying

---

## Integration Ideas

- Caching system (feed optimization)
- Rate limiter (prevent vote abuse)
- Database design (schema for posts/comments/votes)
- Distributed systems (feed fanout strategies)
- Monitoring (tracking engagement metrics)

---

## Status

🟡 Planned
```
