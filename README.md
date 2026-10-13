# Project Ideas

## 1. Distributed RAG Pipeline with Agentic Capabilities

A Distributed Retrieval-Augmented Generation (RAG) platform that processes documents through independent ingestion, chunking, embedding, indexing, and retrieval services. This design allows each stage to scale independently and makes document processing more reliable through asynchronous workflows. AI agents use the retrieved content to generate grounded answers with source references, decide when additional retrieval or tools are needed, and request human approval before taking uncertain or high-impact actions. The platform can be used as an intelligent internal knowledge base for documents, policies, research material, or enterprise workflows.

## 2. Distributed Edge Inferencing

A Distributed Edge Inferencing platform that runs AI models on edge devices close to users, cameras, or IoT sensors instead of relying entirely on a centralized cloud service. By processing requests locally, the system reduces response latency, lowers bandwidth usage, and protects sensitive data from unnecessary transfers. A central control plane manages edge-node registration, model deployment, health checks, routing, and monitoring, while the edge nodes continue serving requests during temporary connectivity issues. This architecture is suitable for use cases such as smart retail, video analytics, industrial monitoring, and real-time anomaly detection.

## 3. Airbnb with Agentic Capabilities

An accommodation-booking platform inspired by Airbnb and enhanced with AI agent capabilities. Users can search properties, view availability, compare prices and amenities, make reservations, and manage their bookings, while hosts can create and manage listings. An AI travel assistant helps users express their needs in natural language—for example, finding a pet-friendly stay near public transportation—and converts those requests into relevant search filters and recommendations. The agent can also compare options, suggest itineraries, and prepare booking actions, while requiring explicit user confirmation before completing any reservation or other transaction-like action.

## 4. GeoRag

A geo-distributed Retrieval-Augmented Generation (RAG) platform that serves knowledge from regional nodes close to users instead of relying on a single centralized vector database. Each region runs its own ingestion, embedding, indexing and retrieval services connected through message queues, so queries are answered locally with lower latency, and documents bound by data-residency rules never leave their region. Frequently used shared documents are replicated asynchronously across regions, while other documents stay in their home region. When local knowledge is not enough, a query router forwards a lightweight request to other regions and merges the results. During network partitions, each region stays available and keeps ingesting and answering on its own. When connectivity returns, CRDT-based synchronization with vector clocks makes all regions eventually consistent, without duplicates or lost deletions. A central control plane manages region registration, health checks, failover, routing policies and monitoring. This architecture suits enterprise knowledge bases, legal and policy search, and regulated industries such as healthcare and finance.
