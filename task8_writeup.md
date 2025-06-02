# Task 8: LangChain Integration – Logical Inference Engine

For this task, I implemented a symbolic reasoning system using LangChain in Python, hosted in Google Colab. The core idea was to reimplement a simplified version of logic-aware systems like Logic-LM or LINC using LangChain's RAG capabilities.

I started by defining a small knowledge base of symbolic facts and rules, expressed in a Prolog-style format. This included facts such as `animal(sparrow)` and `flies(sparrow)`, and rules like `bird(X) :- animal(X), flies(X).`.

Next, I used LangChain’s `Document` abstraction to represent these facts and rules, and embedded them using HuggingFace's `sentence-transformers`. These embeddings were indexed using FAISS to enable similarity-based retrieval.

I then tested the system with queries like “Can a sparrow fly?” using LangChain's retriever. The correct relevant facts and rules were successfully retrieved, demonstrating the RAG-based logic retrieval worked.

While this system doesn’t yet include full reasoning chains (e.g., CoT), it lays the groundwork for symbolic inference via neural RAG pipelines. This setup is lightweight and modular, making it a useful prototype for future extensions.

GitHub repo: [INSERT YOUR GITHUB LINK]

