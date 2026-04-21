# Scalable-Intelligence-A-Distributed-LLM-Inference-System-hpc
📌 Project Overview
This project implements a Master-Worker Distributed Inference System designed to scale Large Language Model (LLM) processing across multiple computing nodes. By utilizing a centralized Master Node to orchestrate requests to multiple Worker Nodes, the system achieves higher throughput and significantly reduced total execution time compared to traditional sequential processing.
🚀 Key Features
Horizontal Scalability: Easily add or remove worker nodes to the cluster by updating the Master's registry.

Parallel Inference: Utilizes ThreadPoolExecutor to process multiple prompts simultaneously across the cluster.

Round-Robin Load Balancing: Tasks are distributed evenly among healthy workers to optimize resource utilization.

Real-time Health Monitoring: The Master node pings a /health endpoint to verify worker status before assigning tasks.

Secure Tunneling: Bridges local worker sessions (e.g., Google Colab) into a unified global cluster using Ngrok.
🛠️ Tech StackComponentTechnologyModelTinyLlama-1.1B-Chat (GGUF Format)Inference Enginellama-cpp-pythonAPI FrameworkFastAPI & UvicornNetworkingPyngrok (Ngrok Tunneling)ConcurrencyThreadPoolExecutor (Master-side parallelization)
