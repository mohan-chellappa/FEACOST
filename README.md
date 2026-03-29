# FeaCost: RFQ Cost & Feasibility System

An enterprise-grade Costing and Technical Feasibility Tracker built to replace clunky, multi-page corporate quoting systems. FeaCost represents complex Bills of Materials (BOM), Process Flow Diagrams (PFD), and technical Parameters (PARAM) simultaneously within a single, unified interface.

## 🚀 The "Flattened TreeGrid" Architecture

We completely abandoned traditional "nested boxes inside boxes" and restrictive "Master-Detail" dual-pane layouts. Instead, FeaCost utilizes a custom **Flattened TreeGrid**. 

*   **Mathematically:** It functions as a deeply nested parent-child tree.
*   **Visually:** It renders as a blazing-fast, continuous vertical spreadsheet.

Engineers and costing teams can instantly view the structural depth of their parts without losing the strict alignments of a financial table.

## ✨ Core Features

### 🎯 Intuitive Visual Hierarchy
*   **IDE-Style Branching:** JavaScript dynamically constructs precise text-based vertical alignment bars (`├──` and `└──`).
*   **Parent Anchoring:** The immediate parent assembly is explicitly printed for every child row, removing all ambiguity.
*   **Dynamic Color Banding:** Deeper nested rows escalate in dark tinting to visually group parent-child blocks.
*   **Auto-Hiding Fold Controls:** Standard `+` / `-` toggle switches expand and collapse assemblies cleanly.

### 🧮 Real-Time Calculus & Rollups
*   **Instant Aggregation:** A recursive parsing engine traverses the tree bottom-up in milliseconds upon any keystroke.
*   **Smart Node Recognition:** Costable physical parts (`[BOM]` and `[PFD]`) automatically roll up child costs, while technical specification branches (`[PARAM]`) retain parent costs without interfering with physical totals.
*   **Global Metrics:** Instantly calculates Total Part Cost, Tooling Allocations, Weighted Feasibility %, and Facility Risk Status.

### 🔐 Role-Based Access Control (RBAC)
Mocks strict database column-level security for collaborative relay-race workflows:
*   **Engineering:** Can structure the BOM and modify parameters, but financial columns are physically hidden.
*   **Commercial:** Can modify costs, but all structural buttons (add/delete/rename) are removed.
*   **Viewers:** Completely restricted to a read-only table.

### 💾 Offline-First CSV Engine
Complete structural persistence without a database:
*   Perfect serialization of complex 3D tree structures into a flat CSV format using randomized UUIDs and ParentIDs.
*   Rapid two-pass reconstruction upon import that physically recreates the DOM and re-nests elements perfectly.

### 🖨️ Print & Audit Ready
*   **Print Optimization:** Strips Dark Mode and interactive UI elements for a stark, high-contrast financial document (`Ctrl+P`).
*   **Soft-Deletion:** Locked or approved nodes require an Audit Deletion Reason, retaining the negotiation history as crossed-out text rather than deleting it.

## 🛠️ Technology Stack

FeaCost is engineered to be blazing fast and easily integrated into larger backend architectures (like a WAMP stack).
*   **HTML5**
*   **CSS3** (Vanilla, customized Dark Mode)
*   **JavaScript** (ES6+, Vanilla, zero external framework dependencies)

## 📦 Usage

Because this project is built entirely without external dependencies or build steps, getting started is immediate:

1. Clone or download the repository.
2. Open `rfq.html` directly in any modern web browser.
3. Start building your BOM.

