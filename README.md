# 🚀 Automated Ticket Clustering and JIRA Integration

## 📌 Overview

<img width="1327" alt="image" src="https://github.com/user-attachments/assets/30350665-3e44-43d4-ac50-f69ef8f7f683" />

[Project Presentation](https://github.com/user-attachments/files/20830357/Project.Presentation.pdf)


This project automates the triaging of ServiceNow tickets using unsupervised clustering (HDBSCAN) combined with OpenAI language models. Clustered tickets are automatically converted into structured JIRA Issues and Sub-Tasks, streamlining IT operations and improving response efficiency.

---

## 🔧 Tech Stack

* **ServiceNow API** – Ticket source system
* **Python** – Core logic and automation scripting
* **HDBSCAN** – Clustering algorithm for grouping similar tickets
* **OpenAI Embeddings** – For semantic understanding of ticket content
* **JIRA API** – For automated issue and sub-task creation

---

## 🔄 Workflow

1. **Fetch Tickets**: Pull open tickets from ServiceNow via API.
2. **Text Embedding**: Convert ticket descriptions to embeddings using OpenAI.
3. **Clustering**: Group similar tickets using HDBSCAN.
4. **Generate Cluster Metadata**: Assign a cluster title and description (can be manual or generated).
5. **JIRA Issue Creation**:
   * One **JIRA Issue** per cluster.
   * One **Sub-Task** per individual ticket.
   * Optional: Generate **proposed solutions** using OpenAI LLMs.
6. **Traceability**: Include original ServiceNow Ticket IDs in JIRA fields/comments.

---

## 📂 JIRA Structure

```
JIRA Issue (Cluster)
├── Title: Cluster summary
├── Description: Aggregated issue description
└── Sub-Tasks:
    ├── Title: Ticket title
    ├── Description: Ticket details
    ├── Comments: Notes, metadata
    └── Proposed Solution: (LLM-generated)
```

---

## ✅ Benefits

* Eliminates manual triaging of repetitive tickets
* Surfaces patterns across large ticket volumes
* Automates structured JIRA entry for downstream resolution
* Integrates seamlessly with existing ITSM workflows

---

## 🛠 Future Improvements

* Feedback loop for improving cluster accuracy
* Epic-level grouping in JIRA for long-term problem tracking

---

## 📜 License

MIT License (or your preferred open-source license)
