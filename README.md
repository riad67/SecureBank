# SecureBank Architecture Explorer

**An interactive guide to banking architecture, infrastructure, and security concepts.**

[Click Here --> Explore the live site](https://riad67.github.io/securebank/) · [Report an issue](https://github.com/riad67/securebank/issues)

SecureBank Architecture Explorer brings a conceptual banking lab into a single interactive interface. It helps learners and reviewers navigate a supplied project structure, explore architecture diagrams, follow example transaction flows, and examine the relationships between application, network, data, security, and operational concepts.

> **About the model:** SecureBank is an educational architecture explorer. Its diagrams, flows, controls, and proposed lab blueprints are illustrative. They do not establish that a component is deployed, connected, or operational, and the site does not display live telemetry.

## Explore the system

| View | What you can explore |
| --- | --- |
| **Overview** | A high-level map of the modeled environment and its major components. |
| **Filesystem Explorer** | A searchable, expandable representation of the supplied project structure. |
| **OSI Layer Architecture** | Network concepts and controls organized around the seven-layer OSI model. |
| **Application Architecture** | Conceptual application components and their relationships. |
| **Banking Transaction Flow** | An illustrative path through components involved in a transaction. |
| **Network Topology** | Network zones and example connections between components. |
| **Security Architecture** | Security controls and trust relationships in the model. |
| **DevSecOps Pipeline** | Illustrative stages in a secure software delivery workflow. |
| **Database Architecture** | Conceptual data stores and their relationships. |
| **Observability & SOC** | Monitoring and security operations concepts. |
| **Documentation Explorer & System Dependencies** | Documentation and relationships among modeled components. |
| **Proposed lab blueprints** | System, virtual network, transfer sequence, Docker topology, and trust-boundary diagrams. |
| **Practice & assessment** | Scenarios, an editable network flow matrix, evidence annotations, and a maturity radar. |

## Getting started

Visit the **[live explorer](https://riad67.github.io/securebank/)** in a modern browser with JavaScript enabled.

1. Select a view from the sidebar. On smaller screens, open the navigation using the menu button.
2. Select a node, layer, file, or folder to inspect its details and learning material.
3. In graph views, drag to pan and use the mouse wheel or on-screen controls to zoom. Use the available fit or reset controls to reorient the diagram.
4. Use the filesystem search and expand or collapse folders to explore the supplied structure.
5. Choose a learning level, review the legend, and try the available scenarios and assessment tools.

The inspector content and controls vary by view. Color and evidence labels are explained in the site's legend.

## How to read the model

The views offer different perspectives on the same conceptual environment. Application and transaction diagrams focus on software and business flow; network and security diagrams focus on connections, boundaries, and controls; database, operations, and delivery views cover supporting concerns. The OSI view provides a networking reference across these areas.

The filesystem tree reflects a supplied project structure. Some descriptions are inferred from names and are identified as such in the explorer. The page does not read the actual project files. Verify relationships, security controls, and implementation claims against the real source code, configuration, and deployment records before relying on them.

## How the site works

The site is a static, browser-based application. Its `index.html` contains the page markup, CSS, embedded model data, and JavaScript responsible for diagrams, navigation, search, and the inspector. No build step or package installation is required to serve the current page.

```text
index.html
├── HTML        Page structure and navigation
├── CSS         Styling, layout, and responsive behavior
└── JavaScript  Model data, diagrams, interactions, and local state
```

The explorer is not a banking application or a live infrastructure platform. An API, database, Docker service, or security tool shown in a diagram is part of the model; the page does not install or operate it.

## Run locally

Clone the repository and open `index.html` in a browser:

```bash
git clone https://github.com/riad67/securebank.git
cd securebank
```

You can also serve the folder locally using Python:

```bash
python -m http.server 8000
```

Then visit <http://localhost:8000/>. Stop the server with `Ctrl+C`. The browser may keep separate local storage for the local file, localhost, and the hosted site.

## Data and privacy

Some preferences and user-entered assessment information are saved in the browser using `localStorage`. These records stay associated with that browser and site origin, do not automatically sync across devices, and can be removed when browser site data is cleared. Avoid entering secrets or sensitive customer information, especially on shared devices.

GitHub Pages serves this site publicly. Review repository content for sensitive information before publishing changes.

## Updating the site

1. Edit `index.html`. The embedded `filesystemText` supplies the filesystem tree; diagrams and learning content are also defined in the file.
2. Open the updated page and check navigation, search, diagrams, the inspector, and any features affected by your changes.
3. Commit and push the updated file to the branch configured in **Settings → Pages**. GitHub Pages will publish changes from the configured source.

Keep proposed designs and inferred descriptions clearly labeled, and validate technical claims against the actual system. For GitHub Pages configuration, see the [official publishing guide](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site).

## Feedback

Found an error or have an idea for an improvement? [Open an issue](https://github.com/riad67/securebank/issues) with the affected view, what you expected, and any relevant details.
