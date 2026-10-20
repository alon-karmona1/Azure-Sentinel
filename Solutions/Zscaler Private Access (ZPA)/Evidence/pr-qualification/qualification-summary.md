# PR Qualification & Validation Summary — Zscaler Private Access (ZPA) (`3.2.2`)

- **Solution:** Zscaler Private Access (ZPA)
- **Version:** `3.2.2` (Previous: `None (new or baseline)`)
- **Qualification Mode:** Migration + Qualification
- **Detected Content Types:** `solution-package`, `analytic-rules`, `xdr-detections`, `workbooks`, `xdr-workbooks`, `data-connectors`, `parsers`, `hunting-queries`, `logos`
- **Generated (UTC):** `2026-10-20T18:24:27Z`
- **Interactive Full Report:** [qualification-report.html](qualification-report.html)

## Executive Rollup Status

| Checklist / Track | Rollup Status |
| :--- | :--- |
| **Validation** | **Validation Failed** |
| **Qualification** | **Qualification Failed** |
| **Migration** | **Migration Failed** |

### Summary Counts

| Passed | Waived with Author Evidence | Human Review Required | Failed | Skipped | Not Applicable | Applicable / Total |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| 43 | 0 | 4 | 30 | 0 | 4 | 77 / 81 |

## Reviewer Action Queue

### **FAIL - SolutionMetadata.json, Data/Solution_*.json, ReleaseNotes.md, and Package/&lt;version&gt;.zip version quartet match** (`VAL-PKG-02`)
- **Checklist / Content Type:** Validation / `solution-package`
- **What We Checked:** Compared semantic version quartet across SolutionMetadata.json, Data/Solution_*.json, ReleaseNotes.md, and Package/&lt;version&gt;.zip.
- **What We Observed:** Quartet versions: SolutionMetadata.json=3.2.2, Data/Solution_Zscaler Private Access (ZPA).json=3.2.2, ReleaseNotes.md=3.0.4, Package/3.2.2.zip=3.2.2.
- **Why:** Version quartet mismatch or missing entries (missing=[], distinctVersions=[&#x27;3.0.4&#x27;, &#x27;3.2.2&#x27;]).
- **Gathered Evidence Files:** [SolutionMetadata.json](../../SolutionMetadata.json), [Solution Data JSON](../../Data/Solution_Zscaler%20Private%20Access%20%28ZPA%29.json), [ReleaseNotes.md](../../ReleaseNotes.md), [Package zip](../../Package/1.0.2.zip), [Package zip](../../Package/2.0.0.zip), [Package zip](../../Package/2.0.1.zip), [Package zip](../../Package/3.0.0.zip), [Package zip](../../Package/3.0.1.zip), [Package zip](../../Package/3.0.2.zip), [Package zip](../../Package/3.0.3.zip), [Package zip](../../Package/3.0.4.zip), [Package zip](../../Package/3.2.2.zip)
- **Reviewer Action Required:** Resolve the failing check or provide an approved author exception with supporting evidence

### **FAIL - Complete subject inventory accounted for (100% packaged or exclusions explicitly acknowledged by author)** (`E2E-V01`)
- **Checklist / Content Type:** Validation / `solution-package`
- **What We Checked:** Compared discovered solution content items against packaged inventory and author-acknowledged exclusions.
- **What We Observed:** Total items=36, packaged=35, unacknowledged missing/excluded=1: XDR Workbooks/ZscalerZPA.json.
- **Why:** Incomplete inventory: 1 item(s) omitted without author acknowledgment (XDR Workbooks/ZscalerZPA.json).
- **Gathered Evidence Files:** [Solution Data manifest](../../Data/Solution_Zscaler%20Private%20Access%20%28ZPA%29.json)
- **Reviewer Action Required:** Resolve the failing check or provide an approved author exception with supporting evidence

### **FAIL - Detection mock data (mock.json) exists and is schema-valid JSON for every packaged detection** (`E2E-V02`)
- **Checklist / Content Type:** Validation / `analytic-rules,xdr-detections,sample-data`
- **What We Checked:** Verified offline mock.json existence and JSON schema for 20 packaged detection(s).
- **What We Observed:** Valid mock files=0, total records=0; issue: No mock.json found for packaged detections.
- **Why:** Detection mock data validation failed: No mock.json found for packaged detections.
- **Gathered Evidence Files:** —
- **Reviewer Action Required:** Resolve the failing check or provide an approved author exception with supporting evidence

### **FAIL - Workbook mock data exists and is schema-valid JSON covering every packaged Workbook** (`E2E-V03`)
- **Checklist / Content Type:** Validation / `workbooks,xdr-workbooks,sample-data`
- **What We Checked:** Verified offline workbook mock data existence and JSON schema for 2 packaged workbook(s).
- **What We Observed:** Valid mock files=0, total records=0; issue: No workbook mock data JSON found.
- **Why:** Workbook mock data validation failed: No workbook mock data JSON found.
- **Gathered Evidence Files:** —
- **Reviewer Action Required:** Resolve the failing check or provide an approved author exception with supporting evidence

### **FAIL - Validation checklist passed (Hard prerequisite: Validation rollup is Validated or Partially Validated)** (`QUAL-00`)
- **Checklist / Content Type:** Qualification / `solution-package`
- **What We Checked:** Verified that the Validation checklist rollup status is Validated or Partially Validated.
- **What We Observed:** Validation rollup is &#x27;Validation Failed&#x27;; unwaived failing/skipped checks: VAL-PKG-02, E2E-V01, E2E-V02, E2E-V03.
- **Why:** Hard prerequisite failed: validationStatus=&#x27;Validation Failed&#x27; due to VAL-PKG-02, E2E-V01, E2E-V02, E2E-V03.
- **Gathered Evidence Files:** [Validation checklist rollup](./pr-qualification-result.json#validationStatus)
- **Reviewer Action Required:** Resolve the failing check or provide an approved author exception with supporting evidence

### **FAIL - No simulated fallbacks in Qualification mode (live Azure/KQL/browser provider receipts verified)** (`E2E-G01`)
- **Checklist / Content Type:** Qualification / `solution-package`
- **What We Checked:** Inspected provider execution receipts and flags for live Azure, KQL, and browser qualification receipts.
- **What We Observed:** 0 live provider receipts found in qualification_evidence or workflow_state.
- **Why:** Fail-closed: no live provider receipts supplied for Qualification mode.
- **Gathered Evidence Files:** [Provider receipts check](../qualification-evidence.json#providerReceipts)
- **Reviewer Action Required:** Resolve the failing check or provide an approved author exception with supporting evidence

### **FAIL - Solution ARM template deployed to lab workspace and verified via GET readback** (`QUAL-DEP-01`)
- **Checklist / Content Type:** Qualification / `solution-package`
- **What We Checked:** Verified disabled lab deployment of Package/mainTemplate.json and independent Azure GET readback.
- **What We Observed:** Deployment/readback evidence missing or unverified (simulated=False, deployment={&#x27;name&#x27;: &#x27;deployment&#x27;, &#x27;status&#x27;: &#x27;notRequired&#x27;, &#x27;attempts&#x27;: 0, &#x27;startedAt&#x27;: None, &#x27;completedAt&#x27;: None, &#x27;message&#x27;: &#x27;not required for the authoring workflow&#x27;, &#x27;artifacts&#x27;: {}, &#x27;evidence&#x27;: []}).
- **Why:** ARM template lab deployment and independent GET readback were not verified.
- **Gathered Evidence Files:** [ARM deployment &amp; GET readback receipt](../qualification-evidence.json#deployment)
- **Reviewer Action Required:** Resolve the failing check or provide an approved author exception with supporting evidence

### **FAIL - Mock data for all detections and workbooks injected into live lab workspace via DCR and verified in target tables** (`E2E-Q01`)
- **Checklist / Content Type:** Qualification / `analytic-rules,xdr-detections,workbooks,xdr-workbooks,sample-data`
- **What We Checked:** Verified live DCR ingestion of mock.json payloads and KQL landing verification in target tables.
- **What We Observed:** DCR mock ingestion unverified (verified=False, rowCount=2, simulated=False).
- **Why:** Live DCR mock data ingestion and target table landing were not verified.
- **Gathered Evidence Files:** [DCR mock ingestion receipt](../qualification-evidence.json#mockIngestion)
- **Reviewer Action Required:** Resolve the failing check or provide an approved author exception with supporting evidence

### **FAIL - Controlled alert lifecycle &amp; firing (TK-Q11: verified disabled at start, enabled, fires &gt;= 1 real alert, and returned to disabled)** (`E2E-Q02`)
- **Checklist / Content Type:** Qualification / `analytic-rules,xdr-detections`
- **What We Checked:** Verified controlled alert lifecycle (disabled at start -&gt; enabled -&gt; &gt;=1 real alert fired -&gt; returned to disabled).
- **What We Observed:** No live alert lifecycle evidence supplied for 20 detection(s).
- **Why:** Controlled alert lifecycle or post-test disabled state restoration was not verified.
- **Gathered Evidence Files:** [Alert lifecycle &amp; firing receipt](../qualification-evidence.json#alertLifecycle)
- **Reviewer Action Required:** Resolve the failing check or provide an approved author exception with supporting evidence

### **FAIL - Every Workbook query executes against injected lab data and returns non-empty data (rowCount &gt; 0)** (`E2E-Q04`)
- **Checklist / Content Type:** Qualification / `workbooks,xdr-workbooks`
- **What We Checked:** Executed every packaged Workbook KQL query against injected lab data and verified rowCount &gt; 0.
- **What We Observed:** No live workbook query execution evidence supplied.
- **Why:** One or more Workbook queries returned rowCount == 0, failed execution, or lacked live evidence.
- **Gathered Evidence Files:** [Workbook query execution evidence](../qualification-evidence.json#workbookQualification)
- **Reviewer Action Required:** Resolve the failing check or provide an approved author exception with supporting evidence

### **FAIL - UI agent traverses all user-facing content in the portal and captures DOM + screenshot evidence** (`E2E-Q05`)
- **Checklist / Content Type:** Qualification / `analytic-rules,xdr-detections,workbooks,xdr-workbooks,data-connectors`
- **What We Checked:** Verified UI agent portal traversal across user-facing Detections, Workbooks (tabs/pickers), and Data Connectors.
- **What We Observed:** No UI agent portal traversal or screenshot evidence found.
- **Why:** Missing live UI agent portal traversal evidence.
- **Gathered Evidence Files:** [Portal UI traversal &amp; screenshots](../qualification-evidence.json#uiTraversal)
- **Reviewer Action Required:** Resolve the failing check or provide an approved author exception with supporting evidence

### **FAIL - UI agent verifies all images, logos, SVG diagrams, and visualizations render properly (naturalWidth &gt; 0, HTTP 200, 0 broken assets)** (`E2E-Q06`)
- **Checklist / Content Type:** Qualification / `logos,workbooks,xdr-workbooks,data-connectors`
- **What We Checked:** Verified all images, logos, SVG diagrams, and chart visualizations render with naturalWidth &gt; 0 and HTTP 200.
- **What We Observed:** No UI image/logo/SVG rendering verification evidence supplied.
- **Why:** Missing UI asset rendering verification evidence.
- **Gathered Evidence Files:** [Visual asset &amp; logo rendering evidence](../qualification-evidence.json#imageRendering)
- **Reviewer Action Required:** Resolve the failing check or provide an approved author exception with supporting evidence

### **FAIL - Changed URLs opened and verified in browser** (`QUAL-URL-01`)
- **Checklist / Content Type:** Qualification / `solution-package,logos`
- **What We Checked:** Opened and verified all changed documentation, aka.ms, and logo URLs in a live browser.
- **What We Observed:** No browser URL verification evidence supplied.
- **Why:** Missing browser URL verification evidence.
- **Gathered Evidence Files:** [Browser URL verification](../qualification-evidence.json#urlVerification)
- **Reviewer Action Required:** Resolve the failing check or provide an approved author exception with supporting evidence

### **HUMAN REVIEW REQUIRED - Reviewer confirmation of supplied XDR / portal behavioral artifacts** (`QUAL-HR-01`)
- **Checklist / Content Type:** Qualification / `solution-package`
- **What We Checked:** Assembled portal screenshots, alert lifecycle receipts, and decision manifest hashes for human PR reviewer confirmation.
- **What We Observed:** Collected 1 evidence artifact reference(s) for reviewer sign-off (humanReviewApproved=False).
- **Why:** Automated evidence gathered; awaiting human PR reviewer confirmation of behavioral artifacts.
- **Gathered Evidence Files:** [Portal &amp; behavioral evidence bundle](../qualification-evidence.json)
- **Reviewer Action Required:** Confirm portal screenshots, alert firing/disabling evidence, and decision-manifest.json hashes.

### **FAIL - Locked Non-production Target Verification** (`TK-G02`)
- **Checklist / Content Type:** Qualification / `all`
- **What We Checked:** Bind the selected tenant, subscription, workspace and exact resource identities and reject scope mismatches.
- **What We Observed:** No live qualification evidence supplied for TK-G02.
- **Why:** Missing live qualification evidence.
- **Gathered Evidence Files:** [TK-G02 evidence](../qualification-evidence.json)
- **Reviewer Action Required:** Resolve the failing check or provide an approved author exception with supporting evidence

### **FAIL - Explicit Exact-scope Authorization** (`TK-G03`)
- **Checklist / Content Type:** Qualification / `all`
- **What We Checked:** Require separate current approvals for reads, browser execution, deployment, ingestion, activation and cleanup.
- **What We Observed:** No live qualification evidence supplied for TK-G03.
- **Why:** Missing live qualification evidence.
- **Gathered Evidence Files:** [TK-G03 evidence](../qualification-evidence.json)
- **Reviewer Action Required:** Resolve the failing check or provide an approved author exception with supporting evidence

### **FAIL - Effective Access and Provider Readiness** (`TK-G04`)
- **Checklist / Content Type:** Qualification / `all`
- **What We Checked:** Inspect effective permissions, applicable roles and deny assignments separately from approval.
- **What We Observed:** No live qualification evidence supplied for TK-G04.
- **Why:** Missing live qualification evidence.
- **Gathered Evidence Files:** [TK-G04 evidence](../qualification-evidence.json)
- **Reviewer Action Required:** Resolve the failing check or provide an approved author exception with supporting evidence

### **FAIL - Mock Scenario Semantic Qualification** (`QUAL-MOCK-01`)
- **Checklist / Content Type:** Qualification / `all`
- **What We Checked:** Sample values support all data types and scenarios and represent the product-appliance data experience.
- **What We Observed:** No live qualification evidence supplied for QUAL-MOCK-01.
- **Why:** Missing live qualification evidence.
- **Gathered Evidence Files:** [QUAL-MOCK-01 evidence](../qualification-evidence.json)
- **Reviewer Action Required:** Resolve the failing check or provide an approved author exception with supporting evidence

### **FAIL - DCR Ingestion Contract Compatibility** (`TK-Q08`)
- **Checklist / Content Type:** Qualification / `all`
- **What We Checked:** Prove the exact stream, transform, destination schema and endpoint are compatible with the shared fixture.
- **What We Observed:** No live qualification evidence supplied for TK-Q08.
- **Why:** Missing live qualification evidence.
- **Gathered Evidence Files:** [TK-Q08 evidence](../qualification-evidence.json)
- **Reviewer Action Required:** Resolve the failing check or provide an approved author exception with supporting evidence

### **FAIL - Packaged Content Runtime Query Validation** (`QUAL-RUNTIME-01`)
- **Checklist / Content Type:** Qualification / `all`
- **What We Checked:** Test regular rules when the PR contains XDR detections; installed hunting and connector queries run without errors.
- **What We Observed:** No live qualification evidence supplied for QUAL-RUNTIME-01.
- **Why:** Missing live qualification evidence.
- **Gathered Evidence Files:** [QUAL-RUNTIME-01 evidence](../qualification-evidence.json)
- **Reviewer Action Required:** Resolve the failing check or provide an approved author exception with supporting evidence

### **FAIL - Controlled Alert Lifecycle and Disabled-state Cleanup** (`TK-Q11`)
- **Checklist / Content Type:** Qualification / `all`
- **What We Checked:** Verify disabled starting state, enable only reviewed detections and disable every test detection after success or failure.
- **What We Observed:** No live qualification evidence supplied for TK-Q11.
- **Why:** Missing live qualification evidence.
- **Gathered Evidence Files:** [TK-Q11 evidence](../qualification-evidence.json)
- **Reviewer Action Required:** Resolve the failing check or provide an approved author exception with supporting evidence

### **FAIL - Approved Browser Scope and Session Verification** (`TK-G06`)
- **Checklist / Content Type:** Qualification / `all`
- **What We Checked:** Use reviewed exact URLs, selectors, expected identities, bounded actions and network scope without Save/Edit or automatic sign-in.
- **What We Observed:** No live qualification evidence supplied for TK-G06.
- **Why:** Missing live qualification evidence.
- **Gathered Evidence Files:** [TK-G06 evidence](../qualification-evidence.json)
- **Reviewer Action Required:** Resolve the failing check or provide an approved author exception with supporting evidence

### **FAIL - Workbook Picker Filter Navigation and Layout Qualification** (`TK-Q06`)
- **Checklist / Content Type:** Qualification / `workbooks`
- **What We Checked:** Verify pickers, dependent refresh, filters, drill-down, reload, layout and conditional visibility with reviewed expectations.
- **What We Observed:** No live qualification evidence supplied for TK-Q06.
- **Why:** Missing live qualification evidence.
- **Gathered Evidence Files:** [TK-Q06 evidence](../qualification-evidence.json)
- **Reviewer Action Required:** Resolve the failing check or provide an approved author exception with supporting evidence

### **FAIL - Live Installation Registration and Managed Update Verification** (`TK-Q07`)
- **Checklist / Content Type:** Qualification / `solution-package`
- **What We Checked:** Verify independent installation and registration/provenance readback and repeat-install/update contracts.
- **What We Observed:** No live qualification evidence supplied for TK-Q07.
- **Why:** Missing live qualification evidence.
- **Gathered Evidence Files:** [TK-Q07 evidence](../qualification-evidence.json)
- **Reviewer Action Required:** Resolve the failing check or provide an approved author exception with supporting evidence

### **FAIL - Live Dependency Metadata Reconciliation** (`TK-Q04`)
- **Checklist / Content Type:** Qualification / `all`
- **What We Checked:** Compare exact-query live input metadata with declared workloads, connectors and data types.
- **What We Observed:** No live qualification evidence supplied for TK-Q04.
- **Why:** Missing live qualification evidence.
- **Gathered Evidence Files:** [TK-Q04 evidence](../qualification-evidence.json)
- **Reviewer Action Required:** Resolve the failing check or provide an approved author exception with supporting evidence

### **HUMAN REVIEW REQUIRED - Analytic Rule and Hunting Query Semantic Review** (`QUAL-RULE-01`)
- **Checklist / Content Type:** Qualification / `all`
- **What We Checked:** Description matches query intent; frequency, period, trigger and threshold match the expected outcome and entity mappings are meaningful.
- **What We Observed:** Automated evidence assembled for human review check QUAL-RULE-01 on Zscaler Private Access (ZPA).
- **Why:** Awaiting human reviewer confirmation.
- **Gathered Evidence Files:** [QUAL-RULE-01 evidence](../qualification-evidence.json)
- **Reviewer Action Required:** Human reviewer confirmation required for QUAL-RULE-01: verify supplied portal screenshots, alert lifecycle artifacts, and behavioral evidence.

### **FAIL - Threat Intelligence Matching Qualification** (`QUAL-TI-01`)
- **Checklist / Content Type:** Qualification / `all`
- **What We Checked:** Filter inactive indicators, use applicable IP indicators and fields, and select the latest indicator before checking active state.
- **What We Observed:** No live qualification evidence supplied for QUAL-TI-01.
- **Why:** Missing live qualification evidence.
- **Gathered Evidence Files:** [QUAL-TI-01 evidence](../qualification-evidence.json)
- **Reviewer Action Required:** Resolve the failing check or provide an approved author exception with supporting evidence

### **FAIL - Parser Runtime and ASIM Mapping Qualification** (`QUAL-PARSER-01`)
- **Checklist / Content Type:** Qualification / `parsers`
- **What We Checked:** Parser deploys, runs on sample data and returns extended fields; relevant source fields map correctly to ASIM.
- **What We Observed:** No live qualification evidence supplied for QUAL-PARSER-01.
- **Why:** Missing live qualification evidence.
- **Gathered Evidence Files:** [QUAL-PARSER-01 evidence](../qualification-evidence.json)
- **Reviewer Action Required:** Resolve the failing check or provide an approved author exception with supporting evidence

### **FAIL - Data Connector Operational Qualification** (`QUAL-DC-01`)
- **Checklist / Content Type:** Qualification / `data-connectors`
- **What We Checked:** Connector queries work; Azure Function deployment and execution are checked, including authentication, filtering, pagination, batching and invocation logs.
- **What We Observed:** No live qualification evidence supplied for QUAL-DC-01.
- **Why:** Missing live qualification evidence.
- **Gathered Evidence Files:** [QUAL-DC-01 evidence](../qualification-evidence.json)
- **Reviewer Action Required:** Resolve the failing check or provide an approved author exception with supporting evidence

### **HUMAN REVIEW REQUIRED - Content Explanation and Presentation Review** (`QUAL-TEXT-01`)
- **Checklist / Content Type:** Qualification / `all`
- **What We Checked:** Descriptions are meaningful and grammatically correct, provider/appliance names exist, and images and workbook content are useful.
- **What We Observed:** Automated evidence assembled for human review check QUAL-TEXT-01 on Zscaler Private Access (ZPA).
- **Why:** Awaiting human reviewer confirmation.
- **Gathered Evidence Files:** [QUAL-TEXT-01 evidence](../qualification-evidence.json)
- **Reviewer Action Required:** Human reviewer confirmation required for QUAL-TEXT-01: verify supplied portal screenshots, alert lifecycle artifacts, and behavioral evidence.

### **HUMAN REVIEW REQUIRED - Ownership Publication and Removal Review** (`QUAL-RELEASE-01`)
- **Checklist / Content Type:** Qualification / `solution-package`
- **What We Checked:** Confirm solution ownership, Partner Center listing requirements, post-merge gallery/shortlinks and Connector team approval before removing a Function App connector.
- **What We Observed:** Automated evidence assembled for human review check QUAL-RELEASE-01 on Zscaler Private Access (ZPA).
- **Why:** Awaiting human reviewer confirmation.
- **Gathered Evidence Files:** [QUAL-RELEASE-01 evidence](../qualification-evidence.json)
- **Reviewer Action Required:** Human reviewer confirmation required for QUAL-RELEASE-01: verify supplied portal screenshots, alert lifecycle artifacts, and behavioral evidence.

### **FAIL - Qualification Coverage and Evidence Reconciliation** (`E2E-V04`)
- **Checklist / Content Type:** Qualification / `all`
- **What We Checked:** Reconcile every required item and check against real evidence; missing, simulated or skipped results are not successful live checks.
- **What We Observed:** No live qualification evidence supplied for E2E-V04.
- **Why:** Missing live qualification evidence.
- **Gathered Evidence Files:** [E2E-V04 evidence](../qualification-evidence.json)
- **Reviewer Action Required:** Resolve the failing check or provide an approved author exception with supporting evidence

### **FAIL - Dual-surface runtime KQL execution (TK-Q01..Q03: Sentinel Log Analytics + Defender XDR Advanced Hunting output-schema binding)** (`MIG-Q01`)
- **Checklist / Content Type:** Migration / `analytic-rules,xdr-detections,workbooks,xdr-workbooks`
- **What We Checked:** Verified dual-surface KQL execution on Sentinel Log Analytics and Defender XDR Advanced Hunting.
- **What We Observed:** Dual-surface KQL execution unverified (simulated=False, evidence={}).
- **Why:** Dual-surface Sentinel LA + Defender XDR AH runtime KQL execution was not verified.
- **Gathered Evidence Files:** [Dual-surface KQL execution receipt](../qualification-evidence.json#dualSurfaceKql)
- **Reviewer Action Required:** Resolve the failing check or provide an approved author exception with supporting evidence

### **FAIL - Sentinel Analytic Rule &lt;-&gt; Defender XDR Custom Detection strict alert parity from shared mock injection (TK-Q09/Q10)** (`E2E-Q03`)
- **Checklist / Content Type:** Migration / `analytic-rules,xdr-detections`
- **What We Checked:** Verified strict alert parity between Sentinel Analytic Rules and migrated Defender XDR Custom Detections from shared mock data.
- **What We Observed:** Alert parity unverified (simulated=False, alertParity={&#x27;name&#x27;: &#x27;alertParity&#x27;, &#x27;status&#x27;: &#x27;notRequired&#x27;, &#x27;attempts&#x27;: 0, &#x27;startedAt&#x27;: None, &#x27;completedAt&#x27;: None, &#x27;message&#x27;: &#x27;not required for the authoring workflow&#x27;, &#x27;artifacts&#x27;: {}, &#x27;evidence&#x27;: []}).
- **Why:** Strict alert parity between Sentinel AR and Defender XDR CD was not verified.
- **Gathered Evidence Files:** [Sentinel &lt;-&gt; XDR alert parity receipt](../qualification-evidence.json#alertParity)
- **Reviewer Action Required:** Resolve the failing check or provide an approved author exception with supporting evidence

## Detailed Check Highlights

- **PASS - Existing PR validations / CI checks passed** (`VAL-CI-01`): All repository JSON/YAML artifacts parsed cleanly and CI checks passed.
- **PASS - Package version incremented from latest live version and &gt;= 3.2.2** (`VAL-PKG-01`): Solution version 3.2.2 satisfies the &gt;= 3.2.2 qualification requirement.
- **FAIL - SolutionMetadata.json, Data/Solution_*.json, ReleaseNotes.md, and Package/&lt;version&gt;.zip version quartet match** (`VAL-PKG-02`): Version quartet mismatch or missing entries (missing=[], distinctVersions=[&#x27;3.0.4&#x27;, &#x27;3.2.2&#x27;]).
- **PASS - createUiDefinition.json Basics and Manage step component counts match packaged resources** (`VAL-PKG-03`): createUiDefinition.json structure and step counts align with packaged ARM resources.
- **PASS - Required XDR properties exist in mainTemplate.json (requiredWorkloads, requiredDataConnectors, extra.customDetections / Defender workbook metadata)** (`VAL-PKG-04`): Required XDR workload, connector, and resource properties are present in mainTemplate.json.
- **PASS - Short URLs (aka.ms) and changed documentation/logo URLs are valid and formatted properly** (`VAL-URL-01`): All discovered URLs and logo links are properly formatted HTTPS URIs.
- **PASS - Analytic Rule YAML schema, GUID format, MITRE ATT&amp;CK mappings, severity, and entity mappings valid** (`VAL-AR-01`): All detection YAML files satisfy schema, GUID, MITRE, and entity mapping rules.
- **PASS - Workbook JSON schema, top-level items, and ARM template embedding valid** (`VAL-WB-01`): All Workbook JSON files have valid structure and non-empty items arrays.
- **PASS - Data Connector JSON/CCF structure, table definitions, and configuration instructions valid** (`VAL-DC-01`): All Data Connector files are structurally valid.
- **PASS - Parser YAML structure and KQL function definition valid** (`VAL-PRS-01`): All Parser YAML definitions are valid.
- **FAIL - Complete subject inventory accounted for (100% packaged or exclusions explicitly acknowledged by author)** (`E2E-V01`): Incomplete inventory: 1 item(s) omitted without author acknowledgment (XDR Workbooks/ZscalerZPA.json).
- **FAIL - Detection mock data (mock.json) exists and is schema-valid JSON for every packaged detection** (`E2E-V02`): Detection mock data validation failed: No mock.json found for packaged detections.
- **FAIL - Workbook mock data exists and is schema-valid JSON covering every packaged Workbook** (`E2E-V03`): Workbook mock data validation failed: No workbook mock data JSON found.
- **PASS - Solution Metadata and Branding Validation** (`VAL-META-01`): Custom validation check passed.
- **PASS - Detection and Hunting Query Contract Validation** (`VAL-RULE-01`): Custom validation check passed.
- **PASS - Function App Connector Artifact Validation** (`VAL-DC-02`): Custom validation check passed.
- **PASS - Sample Data Structure and Sanitization** (`VAL-SAMPLE-01`): Custom validation check passed.
- **PASS - SVG Logo Technical Validation** (`VAL-LOGO-01`): Custom validation check passed.
- **PASS - Parser Structure and Test Input Validation** (`VAL-PARSER-01`): Custom validation check passed.
- **NOT APPLICABLE - Playbook Template and Documentation Validation** (`VAL-PLAYBOOK-01`): Not applicable: required content type(s) playbooks not present.
- **NOT APPLICABLE - Notebook Structure and Dependency Validation** (`VAL-NOTEBOOK-01`): Not applicable: required content type(s) notebooks not present.
- **PASS - Release Notes Format and Coverage** (`VAL-RELEASE-01`): Custom validation check passed.
- **PASS - PR Review Information and Change Accounting** (`VAL-PR-01`): Custom validation check passed.
- **PASS - XDR Artifact Completeness and Source Protection** (`VAL-ARTIFACT-01`): Custom validation check passed.
- **PASS - Workload and Connector Dependency Provenance** (`TK-V06`): Custom validation check passed.
- **PASS - Workbook Function Dependency Integrity** (`TK-V07`): Custom validation check passed.
- **PASS - Package Candidate and Archive Integrity** (`TK-V10`): Custom validation check passed.
- **PASS - XDR Package Properties and Registration Integrity** (`TK-V11`): Custom validation check passed.
- **PASS - Official Validation Receipt Integrity** (`TK-V12`): Custom validation check passed.
- **PASS - ARM Template and Bounded Scope Validation** (`TK-V13`): Custom validation check passed.
- **PASS - Privacy and Safe Evidence Export** (`TK-G07`): Custom validation check passed.
- **PASS - Durable Workflow and Decision Integrity** (`VAL-OPS-01`): Custom validation check passed.
- **FAIL - Validation checklist passed (Hard prerequisite: Validation rollup is Validated or Partially Validated)** (`QUAL-00`): Hard prerequisite failed: validationStatus=&#x27;Validation Failed&#x27; due to VAL-PKG-02, E2E-V01, E2E-V02, E2E-V03.
- **FAIL - No simulated fallbacks in Qualification mode (live Azure/KQL/browser provider receipts verified)** (`E2E-G01`): Fail-closed: no live provider receipts supplied for Qualification mode.
- **FAIL - Solution ARM template deployed to lab workspace and verified via GET readback** (`QUAL-DEP-01`): ARM template lab deployment and independent GET readback were not verified.
- **FAIL - Mock data for all detections and workbooks injected into live lab workspace via DCR and verified in target tables** (`E2E-Q01`): Live DCR mock data ingestion and target table landing were not verified.
- **FAIL - Controlled alert lifecycle &amp; firing (TK-Q11: verified disabled at start, enabled, fires &gt;= 1 real alert, and returned to disabled)** (`E2E-Q02`): Controlled alert lifecycle or post-test disabled state restoration was not verified.
- **FAIL - Every Workbook query executes against injected lab data and returns non-empty data (rowCount &gt; 0)** (`E2E-Q04`): One or more Workbook queries returned rowCount == 0, failed execution, or lacked live evidence.
- **FAIL - UI agent traverses all user-facing content in the portal and captures DOM + screenshot evidence** (`E2E-Q05`): Missing live UI agent portal traversal evidence.
- **FAIL - UI agent verifies all images, logos, SVG diagrams, and visualizations render properly (naturalWidth &gt; 0, HTTP 200, 0 broken assets)** (`E2E-Q06`): Missing UI asset rendering verification evidence.
- **FAIL - Changed URLs opened and verified in browser** (`QUAL-URL-01`): Missing browser URL verification evidence.
- **HUMAN REVIEW REQUIRED - Reviewer confirmation of supplied XDR / portal behavioral artifacts** (`QUAL-HR-01`): Automated evidence gathered; awaiting human PR reviewer confirmation of behavioral artifacts.
- **FAIL - Locked Non-production Target Verification** (`TK-G02`): Missing live qualification evidence.
- **FAIL - Explicit Exact-scope Authorization** (`TK-G03`): Missing live qualification evidence.
- **FAIL - Effective Access and Provider Readiness** (`TK-G04`): Missing live qualification evidence.
- **FAIL - Mock Scenario Semantic Qualification** (`QUAL-MOCK-01`): Missing live qualification evidence.
- **FAIL - DCR Ingestion Contract Compatibility** (`TK-Q08`): Missing live qualification evidence.
- **FAIL - Packaged Content Runtime Query Validation** (`QUAL-RUNTIME-01`): Missing live qualification evidence.
- **FAIL - Controlled Alert Lifecycle and Disabled-state Cleanup** (`TK-Q11`): Missing live qualification evidence.
- **FAIL - Approved Browser Scope and Session Verification** (`TK-G06`): Missing live qualification evidence.
- **FAIL - Workbook Picker Filter Navigation and Layout Qualification** (`TK-Q06`): Missing live qualification evidence.
- **FAIL - Live Installation Registration and Managed Update Verification** (`TK-Q07`): Missing live qualification evidence.
- **FAIL - Live Dependency Metadata Reconciliation** (`TK-Q04`): Missing live qualification evidence.
- **HUMAN REVIEW REQUIRED - Analytic Rule and Hunting Query Semantic Review** (`QUAL-RULE-01`): Awaiting human reviewer confirmation.
- **FAIL - Threat Intelligence Matching Qualification** (`QUAL-TI-01`): Missing live qualification evidence.
- **FAIL - Parser Runtime and ASIM Mapping Qualification** (`QUAL-PARSER-01`): Missing live qualification evidence.
- **FAIL - Data Connector Operational Qualification** (`QUAL-DC-01`): Missing live qualification evidence.
- **NOT APPLICABLE - Playbook Deployment and Functional Qualification** (`QUAL-PLAYBOOK-01`): Not applicable: required content type(s) playbooks not present.
- **NOT APPLICABLE - Notebook Usability Runtime and MSTIC Review** (`QUAL-NOTEBOOK-01`): Not applicable: required content type(s) notebooks not present.
- **HUMAN REVIEW REQUIRED - Content Explanation and Presentation Review** (`QUAL-TEXT-01`): Awaiting human reviewer confirmation.
- **HUMAN REVIEW REQUIRED - Ownership Publication and Removal Review** (`QUAL-RELEASE-01`): Awaiting human reviewer confirmation.
- **FAIL - Qualification Coverage and Evidence Reconciliation** (`E2E-V04`): Missing live qualification evidence.
- **PASS - XDR detection identity contract (TK-V02: xdr-&lt;source GUID&gt;, source path &amp; SHA-256 provenance)** (`MIG-V01`): All XDR detections satisfy the TK-V02 xdr-&lt;source GUID&gt; and SHA-256 provenance contract.
- **PASS - NRT (kind: NRT) and schedule contract (TK-V03: PT0S Continuous eligibility, cosmetic summarize rewrite, or PT1H fallback documented)** (`MIG-V02`): All XDR detections satisfy the TK-V03 NRT and schedule contract.
- **PASS - XDR entity binding and custom-detail column integrity (TK-V04/V05)** (`MIG-V03`): All XDR detections have valid entity mappings and custom-detail column bindings.
- **FAIL - Dual-surface runtime KQL execution (TK-Q01..Q03: Sentinel Log Analytics + Defender XDR Advanced Hunting output-schema binding)** (`MIG-Q01`): Dual-surface Sentinel LA + Defender XDR AH runtime KQL execution was not verified.
- **FAIL - Sentinel Analytic Rule &lt;-&gt; Defender XDR Custom Detection strict alert parity from shared mock injection (TK-Q09/Q10)** (`E2E-Q03`): Strict alert parity between Sentinel AR and Defender XDR CD was not verified.
- **PASS - Complete Migration Inventory and Pairing** (`TK-V01`): Migration check satisfied.
- **PASS - Sentinel-derived XDR Identity Validation** (`TK-V02`): Migration check satisfied.
- **PASS - NRT and Schedule Migration Contract** (`TK-V03`): Migration check satisfied.
- **PASS - Migrated XDR Entity Binding Integrity** (`TK-V04`): Migration check satisfied.
- **PASS - Migrated Custom-detail Integrity** (`TK-V05`): Migration check satisfied.
- **PASS - Migration Package Selection Integrity** (`TK-V08`): Migration check satisfied.
- **PASS - Migration Coverage and Partial Publication Accounting** (`TK-V09`): Migration check satisfied.
- **PASS - Workbook Migration Query and Provenance Integrity** (`MIG-WB-01`): Migration check satisfied.
- **PASS - Sentinel LA and XDR Advanced Hunting Runtime Validation** (`TK-Q01`): Migration check satisfied.
- **PASS - Migrated Runtime Output-schema Binding** (`TK-Q02`): Migration check satisfied.
- **PASS - Provider-family Completeness and Failure Classification** (`TK-Q03`): Migration check satisfied.
- **PASS - Paired Workbook Exact-result Qualification** (`TK-Q05`): Migration check satisfied.
- **PASS - Shared Scenario Source-row Query Parity** (`TK-Q09`): Migration check satisfied.
- **PASS - Strict Sentinel and XDR Alert Comparison** (`TK-Q10`): Migration check satisfied.

## 1. Validation Checklist

Structural, schema, metadata, version, and ARM template checks.

| Check ID & Source | Reviewer Criterion | Category | Status | Evidence Details (Checked / Observed / Why) | Detailed Evidence Files |
| :--- | :--- | :--- | :--- | :--- | :--- |
| `VAL-CI-01` (solution-package · pr-checklist-2-docx) | **Existing PR validations / CI checks passed**<br>Verify all existing repository PR validation workflows and CI syntax checks pass. | `validation` | **PASS** (`PASS`) | **Checked:** Parsed all JSON and YAML files in solution scope and inspected CI validation status.<br>**Observed:** Validated 10 JSON file(s) and 31 YAML file(s) with 0 syntax/schema errors.<br>**Why:** All repository JSON/YAML artifacts parsed cleanly and CI checks passed. | [Validated solution-package file](../../Data/Solution_Zscaler%20Private%20Access%20%28ZPA%29.json), [Validated solution-package file](../../Package/1.0.2.zip), [Validated solution-package file](../../Package/2.0.0.zip), [Validated solution-package file](../../Package/2.0.1.zip), [Validated solution-package file](../../Package/3.0.0.zip) |
| `VAL-PKG-01` (solution-package · pr-checklist-2-docx + toolkit-contract) | **Package version incremented from latest live version and &gt;= 3.2.2**<br>Verify the solution package version is incremented above the live version and is at least 3.2.2. | `validation` | **PASS** (`PASS`) | **Checked:** Verified solution package version &gt;= 3.2.2 and incremented from live baseline.<br>**Observed:** Observed version &#x27;3.2.2&#x27; &gt;= &#x27;3.2.2&#x27;.<br>**Why:** Solution version 3.2.2 satisfies the &gt;= 3.2.2 qualification requirement. | [SolutionMetadata.json](../../SolutionMetadata.json), [Solution Data JSON](../../Data/Solution_Zscaler%20Private%20Access%20%28ZPA%29.json), [ReleaseNotes.md](../../ReleaseNotes.md) |
| `VAL-PKG-02` (solution-package · master-excel + toolkit-contract) | **SolutionMetadata.json, Data/Solution_*.json, ReleaseNotes.md, and Package/&lt;version&gt;.zip version quartet match**<br>Verify the version string matches across SolutionMetadata.json, Data/Solution_*.json, ReleaseNotes.md, and Package/&lt;version&gt;.zip. | `validation` | **FAIL** (`FAIL`) | **Checked:** Compared semantic version quartet across SolutionMetadata.json, Data/Solution_*.json, ReleaseNotes.md, and Package/&lt;version&gt;.zip.<br>**Observed:** Quartet versions: SolutionMetadata.json=3.2.2, Data/Solution_Zscaler Private Access (ZPA).json=3.2.2, ReleaseNotes.md=3.0.4, Package/3.2.2.zip=3.2.2.<br>**Why:** Version quartet mismatch or missing entries (missing=[], distinctVersions=[&#x27;3.0.4&#x27;, &#x27;3.2.2&#x27;]). | [SolutionMetadata.json](../../SolutionMetadata.json), [Solution Data JSON](../../Data/Solution_Zscaler%20Private%20Access%20%28ZPA%29.json), [ReleaseNotes.md](../../ReleaseNotes.md), [Package zip](../../Package/1.0.2.zip), [Package zip](../../Package/2.0.0.zip), [Package zip](../../Package/2.0.1.zip), [Package zip](../../Package/3.0.0.zip), [Package zip](../../Package/3.0.1.zip), [Package zip](../../Package/3.0.2.zip), [Package zip](../../Package/3.0.3.zip), [Package zip](../../Package/3.0.4.zip), [Package zip](../../Package/3.2.2.zip) |
| `VAL-PKG-03` (solution-package · pr-checklist-2-docx) | **createUiDefinition.json Basics and Manage step component counts match packaged resources**<br>Verify createUiDefinition.json Basics description and Manage steps match the resources packaged in mainTemplate.json. | `validation` | **PASS** (`PASS`) | **Checked:** Compared createUiDefinition.json Basics/Manage steps against mainTemplate.json resources.<br>**Observed:** Verified createUiDefinition.json (4 step(s), 2 basic element(s)) against mainTemplate.json (46 top-level resource entry/entries).<br>**Why:** createUiDefinition.json structure and step counts align with packaged ARM resources. | [createUiDefinition.json](../../Package/createUiDefinition.json), [mainTemplate.json](../../Package/mainTemplate.json) |
| `VAL-PKG-04` (xdr-detections,xdr-workbooks · pr-checklist-2-docx) | **Required XDR properties exist in mainTemplate.json (requiredWorkloads, requiredDataConnectors, extra.customDetections / Defender workbook metadata)**<br>Verify requiredWorkloads, requiredDataConnectors, and extra.customDetections / Defender workbook metadata exist in mainTemplate.json. | `validation` | **PASS** (`PASS`) | **Checked:** Inspected Package/mainTemplate.json for requiredWorkloads, requiredDataConnectors, and extra.customDetections / XDR workbook metadata.<br>**Observed:** Verified XDR metadata markers in Package/mainTemplate.json: requiredWorkloads, requiredDataConnectors, extra, xdr, microsoft.insights/workbooks.<br>**Why:** Required XDR workload, connector, and resource properties are present in mainTemplate.json. | [mainTemplate.json](../../Package/mainTemplate.json) |
| `VAL-URL-01` (solution-package,logos · pr-checklist-2-docx + master-excel) | **Short URLs (aka.ms) and changed documentation/logo URLs are valid and formatted properly**<br>Verify short URLs (aka.ms) and all changed documentation or logo URLs use valid HTTPS formatting. | `validation` | **PASS** (`PASS`) | **Checked:** Extracted and validated all documentation, short-link (aka.ms), and logo URLs across solution files.<br>**Observed:** Validated 207 URL(s) (20 aka.ms short link(s)) across solution metadata and content with 0 malformed or insecure URLs.<br>**Why:** All discovered URLs and logo links are properly formatted HTTPS URIs. | [URL-checked file](../../Data/Solution_Zscaler%20Private%20Access%20%28ZPA%29.json), [URL-checked file](../../Package/createUiDefinition.json), [URL-checked file](../../Package/mainTemplate.json), [URL-checked file](../../ReleaseNotes.md) |
| `VAL-AR-01` (analytic-rules,xdr-detections · master-excel) | **Analytic Rule YAML schema, GUID format, MITRE ATT&amp;CK mappings, severity, and entity mappings valid**<br>Verify Analytic Rule YAML schema fields, GUID format, MITRE ATT&amp;CK tactics/techniques, severity, and entity mappings. | `validation` | **PASS** (`PASS`) | **Checked:** Validated YAML schema, GUID format, MITRE ATT&amp;CK techniques, severity, and query presence across detection files.<br>**Observed:** Validated 20 detection YAML file(s) (10 Analytic Rule(s), 10 XDR Detection(s)) with valid GUIDs, severities, MITRE mappings, and KQL queries.<br>**Why:** All detection YAML files satisfy schema, GUID, MITRE, and entity mapping rules. | [Analytic Rule YAML](../../Analytic%20Rules/ZscalerSharedZPASession.yaml), [Analytic Rule YAML](../../Analytic%20Rules/ZscalerUnexpectedCountEventResult.yaml), [Analytic Rule YAML](../../Analytic%20Rules/ZscalerUnexpectedCountries.yaml), [Analytic Rule YAML](../../Analytic%20Rules/ZscalerUnexpectedUpdateOperation.yaml), [Analytic Rule YAML](../../Analytic%20Rules/ZscalerZPAConnectionsByDormantUser.yaml), [Analytic Rule YAML](../../Analytic%20Rules/ZscalerZPAConnectionsByNewUser.yaml), [Analytic Rule YAML](../../Analytic%20Rules/ZscalerZPAConnectionsFromNewCountry.yaml), [Analytic Rule YAML](../../Analytic%20Rules/ZscalerZPAConnectionsFromNewIP.yaml), [Analytic Rule YAML](../../Analytic%20Rules/ZscalerZPAConnectionsOutsideOperationalHours.yaml), [Analytic Rule YAML](../../Analytic%20Rules/ZscalerZPAUnexpectedSessionDuration.yaml), [XDR Detection YAML](../../XDR%20Detections/ZscalerSharedZPASession.yaml), [XDR Detection YAML](../../XDR%20Detections/ZscalerUnexpectedCountEventResult.yaml), [XDR Detection YAML](../../XDR%20Detections/ZscalerUnexpectedCountries.yaml), [XDR Detection YAML](../../XDR%20Detections/ZscalerUnexpectedUpdateOperation.yaml), [XDR Detection YAML](../../XDR%20Detections/ZscalerZPAConnectionsByDormantUser.yaml), [XDR Detection YAML](../../XDR%20Detections/ZscalerZPAConnectionsByNewUser.yaml), [XDR Detection YAML](../../XDR%20Detections/ZscalerZPAConnectionsFromNewCountry.yaml), [XDR Detection YAML](../../XDR%20Detections/ZscalerZPAConnectionsFromNewIP.yaml), [XDR Detection YAML](../../XDR%20Detections/ZscalerZPAConnectionsOutsideOperationalHours.yaml), [XDR Detection YAML](../../XDR%20Detections/ZscalerZPAUnexpectedSessionDuration.yaml) |
| `VAL-WB-01` (workbooks,xdr-workbooks · master-excel) | **Workbook JSON schema, top-level items, and ARM template embedding valid**<br>Verify Workbook JSON schema structure, top-level items array, and mainTemplate.json embedding. | `validation` | **PASS** (`PASS`) | **Checked:** Validated Workbook JSON schema, version header, and top-level items array.<br>**Observed:** Validated 2 workbook JSON file(s) containing 20 top-level item(s).<br>**Why:** All Workbook JSON files have valid structure and non-empty items arrays. | [Workbook JSON](../../Workbooks/ZscalerZPA.json), [Workbook JSON](../../XDR%20Workbooks/ZscalerZPA.json) |
| `VAL-DC-01` (data-connectors · master-excel) | **Data Connector JSON/CCF structure, table definitions, and configuration instructions valid**<br>Verify Data Connector JSON/CCF definitions, target table declarations, and configuration instruction steps. | `validation` | **PASS** (`PASS`) | **Checked:** Validated Data Connector JSON/CCF structure, table declarations, and instruction steps.<br>**Observed:** Validated 1 Data Connector definition file(s) with valid table and instruction metadata.<br>**Why:** All Data Connector files are structurally valid. | [Data Connector definition](../../Data%20Connectors/Connector_LogAnalytics_agent_Zscaler_ZPA.json) |
| `VAL-PRS-01` (parsers · master-excel) | **Parser YAML structure and KQL function definition valid**<br>Verify Parser YAML metadata structure, function alias, and non-empty KQL body. | `validation` | **PASS** (`PASS`) | **Checked:** Validated Parser YAML metadata and KQL function body.<br>**Observed:** Validated 1 Parser YAML file(s) with non-empty KQL function queries.<br>**Why:** All Parser YAML definitions are valid. | [Parser YAML](../../Parsers/ZPAEvent.yaml) |
| `E2E-V01` (solution-package · user-e2e-requirement) | **Complete subject inventory accounted for (100% packaged or exclusions explicitly acknowledged by author)**<br>Verify 100% of solution content items are packaged or any partial exclusions are explicitly acknowledged in decision-manifest.json / acknowledged_exclusions. | `validation` | **FAIL** (`FAIL`) | **Checked:** Compared discovered solution content items against packaged inventory and author-acknowledged exclusions.<br>**Observed:** Total items=36, packaged=35, unacknowledged missing/excluded=1: XDR Workbooks/ZscalerZPA.json.<br>**Why:** Incomplete inventory: 1 item(s) omitted without author acknowledgment (XDR Workbooks/ZscalerZPA.json). | [Solution Data manifest](../../Data/Solution_Zscaler%20Private%20Access%20%28ZPA%29.json) |
| `E2E-V02` (analytic-rules,xdr-detections,sample-data · user-e2e-requirement) | **Detection mock data (mock.json) exists and is schema-valid JSON for every packaged detection**<br>Verify mock.json exists and contains schema-valid JSON records covering every packaged Sentinel Analytic Rule and Defender XDR Custom Detection. | `validation` | **FAIL** (`FAIL`) | **Checked:** Verified offline mock.json existence and JSON schema for 20 packaged detection(s).<br>**Observed:** Valid mock files=0, total records=0; issue: No mock.json found for packaged detections.<br>**Why:** Detection mock data validation failed: No mock.json found for packaged detections. | — |
| `E2E-V03` (workbooks,xdr-workbooks,sample-data · user-e2e-requirement) | **Workbook mock data exists and is schema-valid JSON covering every packaged Workbook**<br>Verify mock data exists and contains schema-valid JSON records covering every packaged Sentinel and Defender XDR Workbook. | `validation` | **FAIL** (`FAIL`) | **Checked:** Verified offline workbook mock data existence and JSON schema for 2 packaged workbook(s).<br>**Observed:** Valid mock files=0, total records=0; issue: No workbook mock data JSON found.<br>**Why:** Workbook mock data validation failed: No workbook mock data JSON found. | — |
| `VAL-META-01` (solution-package · master-excel) | **Solution Metadata and Branding Validation**<br>Verify metadata, support information, author/provider details, domains, and Microsoft Sentinel branding. | `validation` | **PASS** (`PASS`) | **Checked:** Verify metadata, support information, author/provider details, domains, and Microsoft Sentinel branding.<br>**Observed:** Validated custom check VAL-META-01 on Zscaler Private Access (ZPA).<br>**Why:** Custom validation check passed. | — |
| `VAL-RULE-01` (all · master-excel) | **Detection and Hunting Query Contract Validation**<br>Id is GUID and not duplicated; YAML structure is correct; review names, descriptions, dependencies, tactics, techniques and query fields. | `validation` | **PASS** (`PASS`) | **Checked:** Id is GUID and not duplicated; YAML structure is correct; review names, descriptions, dependencies, tactics, techniques and query fields.<br>**Observed:** Validated custom check VAL-RULE-01 on Zscaler Private Access (ZPA).<br>**Why:** Custom validation check passed. | — |
| `VAL-DC-02` (data-connectors · master-excel) | **Function App Connector Artifact Validation**<br>Validate deployment and execution files, Function App ZIP contents, function-name bounds and template variables. | `validation` | **PASS** (`PASS`) | **Checked:** Validate deployment and execution files, Function App ZIP contents, function-name bounds and template variables.<br>**Observed:** Validated custom check VAL-DC-02 on Zscaler Private Access (ZPA).<br>**Why:** Custom validation check passed. | — |
| `VAL-SAMPLE-01` (all · master-excel) | **Sample Data Structure and Sanitization**<br>Sample values are populated and sanitized for customer or PII information. | `validation` | **PASS** (`PASS`) | **Checked:** Sample values are populated and sanitized for customer or PII information.<br>**Observed:** Validated custom check VAL-SAMPLE-01 on Zscaler Private Access (ZPA).<br>**Why:** Custom validation check passed. | — |
| `VAL-LOGO-01` (logos · master-excel) | **SVG Logo Technical Validation**<br>Logo needs to be in SVG format and under 5 Kb; prohibited constructs are absent and IDs are uniquely identifiable. | `validation` | **PASS** (`PASS`) | **Checked:** Logo needs to be in SVG format and under 5 Kb; prohibited constructs are absent and IDs are uniquely identifiable.<br>**Observed:** Validated custom check VAL-LOGO-01 on Zscaler Private Access (ZPA).<br>**Why:** Custom validation check passed. | — |
| `VAL-PARSER-01` (parsers · master-excel) | **Parser Structure and Test Input Validation**<br>Sample data is available for testing; parser definitions and relevant ASIM schema are identified. | `validation` | **PASS** (`PASS`) | **Checked:** Sample data is available for testing; parser definitions and relevant ASIM schema are identified.<br>**Observed:** Validated custom check VAL-PARSER-01 on Zscaler Private Access (ZPA).<br>**Why:** Custom validation check passed. | — |
| `VAL-PLAYBOOK-01` (playbooks · master-excel) | **Playbook Template and Documentation Validation**<br>Validate the Playbooks folder and Readme, templatization, connection variables and Deploy to Azure/Gov buttons. | `validation` | **NOT APPLICABLE** (`NOT_APPLICABLE`) | **Checked:** Validate the Playbooks folder and Readme, templatization, connection variables and Deploy to Azure/Gov buttons.<br>**Observed:** 0 matching content items for VAL-PLAYBOOK-01 in solution Zscaler Private Access (ZPA).<br>**Why:** Not applicable: required content type(s) playbooks not present. | — |
| `VAL-NOTEBOOK-01` (notebooks · master-excel) | **Notebook Structure and Dependency Validation**<br>Notebook uses standard header information, documented dependencies and configuration; sample data is provided when possible. | `validation` | **NOT APPLICABLE** (`NOT_APPLICABLE`) | **Checked:** Notebook uses standard header information, documented dependencies and configuration; sample data is provided when possible.<br>**Observed:** 0 matching content items for VAL-NOTEBOOK-01 in solution Zscaler Private Access (ZPA).<br>**Why:** Not applicable: required content type(s) notebooks not present. | — |
| `VAL-RELEASE-01` (solution-package · master-excel) | **Release Notes Format and Coverage**<br>Check release note text and format. | `validation` | **PASS** (`PASS`) | **Checked:** Check release note text and format.<br>**Observed:** Validated custom check VAL-RELEASE-01 on Zscaler Private Access (ZPA).<br>**Why:** Custom validation check passed. | — |
| `VAL-PR-01` (all · master-excel) | **PR Review Information and Change Accounting**<br>Ensure the PR review template is filled out; double-check deletions and merge-conflict resolutions. | `validation` | **PASS** (`PASS`) | **Checked:** Ensure the PR review template is filled out; double-check deletions and merge-conflict resolutions.<br>**Observed:** Validated custom check VAL-PR-01 on Zscaler Private Access (ZPA).<br>**Why:** Custom validation check passed. | — |
| `VAL-ARTIFACT-01` (all · pr-checklist-2-docx) | **XDR Artifact Completeness and Source Protection**<br>Verify XDR artifacts shared in the PR; if absent, ask the author to provide them. | `validation` | **PASS** (`PASS`) | **Checked:** Verify XDR artifacts shared in the PR; if absent, ask the author to provide them.<br>**Observed:** Validated custom check VAL-ARTIFACT-01 on Zscaler Private Access (ZPA).<br>**Why:** Custom validation check passed. | — |
| `TK-V06` (all · toolkit-contract) | **Workload and Connector Dependency Provenance**<br>Validate workload vocabulary and dependency records; unresolved dependency review blocks readiness. | `validation` | **PASS** (`PASS`) | **Checked:** Validate workload vocabulary and dependency records; unresolved dependency review blocks readiness.<br>**Observed:** Validated custom check TK-V06 on Zscaler Private Access (ZPA).<br>**Why:** Custom validation check passed. | — |
| `TK-V07` (workbooks · toolkit-contract) | **Workbook Function Dependency Integrity**<br>Bind required workspace functions to packaged definitions, aliases and current hashes; resolve actual parser installation dependencies. | `validation` | **PASS** (`PASS`) | **Checked:** Bind required workspace functions to packaged definitions, aliases and current hashes; resolve actual parser installation dependencies.<br>**Observed:** Validated custom check TK-V07 on Zscaler Private Access (ZPA).<br>**Why:** Custom validation check passed. | — |
| `TK-V10` (solution-package · toolkit-contract) | **Package Candidate and Archive Integrity**<br>Bind candidate inputs and artifacts and verify exact ZIP contents without stale, duplicate or operational entries. | `validation` | **PASS** (`PASS`) | **Checked:** Bind candidate inputs and artifacts and verify exact ZIP contents without stale, duplicate or operational entries.<br>**Observed:** Validated custom check TK-V10 on Zscaler Private Access (ZPA).<br>**Why:** Custom validation check passed. | — |
| `TK-V11` (solution-package · toolkit-contract) | **XDR Package Properties and Registration Integrity**<br>Verify required XDR content properties and exact installation/registration identity, version and dependency contracts. | `validation` | **PASS** (`PASS`) | **Checked:** Verify required XDR content properties and exact installation/registration identity, version and dependency contracts.<br>**Observed:** Validated custom check TK-V11 on Zscaler Private Access (ZPA).<br>**Why:** Custom validation check passed. | — |
| `TK-V12` (all · toolkit-contract) | **Official Validation Receipt Integrity**<br>Require complete producer-bound validation receipts for the current candidate and preserve individual statuses. | `validation` | **PASS** (`PASS`) | **Checked:** Require complete producer-bound validation receipts for the current candidate and preserve individual statuses.<br>**Observed:** Validated custom check TK-V12 on Zscaler Private Access (ZPA).<br>**Why:** Custom validation check passed. | — |
| `TK-V13` (solution-package · toolkit-contract) | **ARM Template and Bounded Scope Validation**<br>Resolve resource types, parameters, conditions and nested scopes and retain applicable official ARM validation checks. | `validation` | **PASS** (`PASS`) | **Checked:** Resolve resource types, parameters, conditions and nested scopes and retain applicable official ARM validation checks.<br>**Observed:** Validated custom check TK-V13 on Zscaler Private Access (ZPA).<br>**Why:** Custom validation check passed. | — |
| `TK-G07` (all · toolkit-contract) | **Privacy and Safe Evidence Export**<br>Keep secrets, private target identifiers, personal data, local paths and operational receipts out of published content and evidence. | `validation` | **PASS** (`PASS`) | **Checked:** Keep secrets, private target identifiers, personal data, local paths and operational receipts out of published content and evidence.<br>**Observed:** Validated custom check TK-G07 on Zscaler Private Access (ZPA).<br>**Why:** Custom validation check passed. | — |
| `VAL-OPS-01` (all · toolkit-contract) | **Durable Workflow and Decision Integrity**<br>Preserve attempts and failures, use bounded execution, prevent duplicate owners and version consumption, and retain accountable review decisions. | `validation` | **PASS** (`PASS`) | **Checked:** Preserve attempts and failures, use bounded execution, prevent duplicate owners and version consumption, and retain accountable review decisions.<br>**Observed:** Validated custom check VAL-OPS-01 on Zscaler Private Access (ZPA).<br>**Why:** Custom validation check passed. | — |

## 2. Qualification Checklist

Runtime deployment, ingestion, query execution, connector, and content qualification checks.

| Check ID & Source | Reviewer Criterion | Category | Status | Evidence Details (Checked / Observed / Why) | Detailed Evidence Files |
| :--- | :--- | :--- | :--- | :--- | :--- |
| `QUAL-00` (solution-package · user-e2e-requirement + pr-checklist-2-docx) | **Validation checklist passed (Hard prerequisite: Validation rollup is Validated or Partially Validated)**<br>Require Validation checklist rollup to be Validated or Partially Validated before Qualification can pass. | `qualification` | **FAIL** (`FAIL`) | **Checked:** Verified that the Validation checklist rollup status is Validated or Partially Validated.<br>**Observed:** Validation rollup is &#x27;Validation Failed&#x27;; unwaived failing/skipped checks: VAL-PKG-02, E2E-V01, E2E-V02, E2E-V03.<br>**Why:** Hard prerequisite failed: validationStatus=&#x27;Validation Failed&#x27; due to VAL-PKG-02, E2E-V01, E2E-V02, E2E-V03. | [Validation checklist rollup](./pr-qualification-result.json#validationStatus) |
| `E2E-G01` (solution-package · user-e2e-requirement + toolkit-contract) | **No simulated fallbacks in Qualification mode (live Azure/KQL/browser provider receipts verified)**<br>Verify live Azure, KQL, and browser provider receipts were used; fail closed if dry-run or simulated fallback stubs were used. | `qualification` | **FAIL** (`FAIL`) | **Checked:** Inspected provider execution receipts and flags for live Azure, KQL, and browser qualification receipts.<br>**Observed:** 0 live provider receipts found in qualification_evidence or workflow_state.<br>**Why:** Fail-closed: no live provider receipts supplied for Qualification mode. | [Provider receipts check](../qualification-evidence.json#providerReceipts) |
| `QUAL-DEP-01` (solution-package · toolkit-contract) | **Solution ARM template deployed to lab workspace and verified via GET readback**<br>Deploy the packaged solution ARM template disabled to the lab workspace and verify deployed resources via independent GET readback. | `qualification` | **FAIL** (`FAIL`) | **Checked:** Verified disabled lab deployment of Package/mainTemplate.json and independent Azure GET readback.<br>**Observed:** Deployment/readback evidence missing or unverified (simulated=False, deployment={&#x27;name&#x27;: &#x27;deployment&#x27;, &#x27;status&#x27;: &#x27;notRequired&#x27;, &#x27;attempts&#x27;: 0, &#x27;startedAt&#x27;: None, &#x27;completedAt&#x27;: None, &#x27;message&#x27;: &#x27;not required for the authoring workflow&#x27;, &#x27;artifacts&#x27;: {}, &#x27;evidence&#x27;: []}).<br>**Why:** ARM template lab deployment and independent GET readback were not verified. | [ARM deployment &amp; GET readback receipt](../qualification-evidence.json#deployment) |
| `E2E-Q01` (analytic-rules,xdr-detections,workbooks,xdr-workbooks,sample-data · user-e2e-requirement) | **Mock data for all detections and workbooks injected into live lab workspace via DCR and verified in target tables**<br>Inject synthetic mock data via DCR into the live lab workspace and verify row landing across all target tables. | `qualification` | **FAIL** (`FAIL`) | **Checked:** Verified live DCR ingestion of mock.json payloads and KQL landing verification in target tables.<br>**Observed:** DCR mock ingestion unverified (verified=False, rowCount=2, simulated=False).<br>**Why:** Live DCR mock data ingestion and target table landing were not verified. | [DCR mock ingestion receipt](../qualification-evidence.json#mockIngestion) |
| `E2E-Q02` (analytic-rules,xdr-detections · user-e2e-requirement + toolkit-contract) | **Controlled alert lifecycle &amp; firing (TK-Q11: verified disabled at start, enabled, fires &gt;= 1 real alert, and returned to disabled)**<br>Verify every packaged detection starts disabled, is enabled in a controlled window, fires at least 1 real alert correlated to the injected mock scenario, and is returned to disabled. | `qualification` | **FAIL** (`FAIL`) | **Checked:** Verified controlled alert lifecycle (disabled at start -&gt; enabled -&gt; &gt;=1 real alert fired -&gt; returned to disabled).<br>**Observed:** No live alert lifecycle evidence supplied for 20 detection(s).<br>**Why:** Controlled alert lifecycle or post-test disabled state restoration was not verified. | [Alert lifecycle &amp; firing receipt](../qualification-evidence.json#alertLifecycle) |
| `E2E-Q04` (workbooks,xdr-workbooks · user-e2e-requirement) | **Every Workbook query executes against injected lab data and returns non-empty data (rowCount &gt; 0)**<br>Execute every Workbook KQL query against the injected lab telemetry and verify rowCount &gt; 0 with non-zero scenario values. | `qualification` | **FAIL** (`FAIL`) | **Checked:** Executed every packaged Workbook KQL query against injected lab data and verified rowCount &gt; 0.<br>**Observed:** No live workbook query execution evidence supplied.<br>**Why:** One or more Workbook queries returned rowCount == 0, failed execution, or lacked live evidence. | [Workbook query execution evidence](../qualification-evidence.json#workbookQualification) |
| `E2E-Q05` (analytic-rules,xdr-detections,workbooks,xdr-workbooks,data-connectors · user-e2e-requirement) | **UI agent traverses all user-facing content in the portal and captures DOM + screenshot evidence**<br>Traverse Detections, Workbooks across tabs/pickers, and Data Connectors in the portal via UI agent and capture DOM + screenshot evidence. | `qualification` | **FAIL** (`FAIL`) | **Checked:** Verified UI agent portal traversal across user-facing Detections, Workbooks (tabs/pickers), and Data Connectors.<br>**Observed:** No UI agent portal traversal or screenshot evidence found.<br>**Why:** Missing live UI agent portal traversal evidence. | [Portal UI traversal &amp; screenshots](../qualification-evidence.json#uiTraversal) |
| `E2E-Q06` (logos,workbooks,xdr-workbooks,data-connectors · user-e2e-requirement + master-excel) | **UI agent verifies all images, logos, SVG diagrams, and visualizations render properly (naturalWidth &gt; 0, HTTP 200, 0 broken assets)**<br>Verify all images, logos, SVG diagrams, and chart visualizations render in the browser with naturalWidth &gt; 0, HTTP 200, and 0 broken assets. | `qualification` | **FAIL** (`FAIL`) | **Checked:** Verified all images, logos, SVG diagrams, and chart visualizations render with naturalWidth &gt; 0 and HTTP 200.<br>**Observed:** No UI image/logo/SVG rendering verification evidence supplied.<br>**Why:** Missing UI asset rendering verification evidence. | [Visual asset &amp; logo rendering evidence](../qualification-evidence.json#imageRendering) |
| `QUAL-URL-01` (solution-package,logos · pr-checklist-2-docx) | **Changed URLs opened and verified in browser**<br>Open and verify all changed documentation, short-link, and logo URLs in a live browser session. | `qualification` | **FAIL** (`FAIL`) | **Checked:** Opened and verified all changed documentation, aka.ms, and logo URLs in a live browser.<br>**Observed:** No browser URL verification evidence supplied.<br>**Why:** Missing browser URL verification evidence. | [Browser URL verification](../qualification-evidence.json#urlVerification) |
| `QUAL-HR-01` (solution-package · pr-checklist-2-docx) | **Reviewer confirmation of supplied XDR / portal behavioral artifacts**<br>Human reviewer confirmation of supplied portal screenshots, alert lifecycle receipts, and behavioral artifacts. | `human-review` | **HUMAN REVIEW REQUIRED** (`HUMAN_REVIEW_REQUIRED`) | **Checked:** Assembled portal screenshots, alert lifecycle receipts, and decision manifest hashes for human PR reviewer confirmation.<br>**Observed:** Collected 1 evidence artifact reference(s) for reviewer sign-off (humanReviewApproved=False).<br>**Why:** Automated evidence gathered; awaiting human PR reviewer confirmation of behavioral artifacts. | [Portal &amp; behavioral evidence bundle](../qualification-evidence.json) |
| `TK-G02` (all · toolkit-contract) | **Locked Non-production Target Verification**<br>Bind the selected tenant, subscription, workspace and exact resource identities and reject scope mismatches. | `validation` | **FAIL** (`FAIL`) | **Checked:** Bind the selected tenant, subscription, workspace and exact resource identities and reject scope mismatches.<br>**Observed:** No live qualification evidence supplied for TK-G02.<br>**Why:** Missing live qualification evidence. | [TK-G02 evidence](../qualification-evidence.json) |
| `TK-G03` (all · toolkit-contract) | **Explicit Exact-scope Authorization**<br>Require separate current approvals for reads, browser execution, deployment, ingestion, activation and cleanup. | `validation` | **FAIL** (`FAIL`) | **Checked:** Require separate current approvals for reads, browser execution, deployment, ingestion, activation and cleanup.<br>**Observed:** No live qualification evidence supplied for TK-G03.<br>**Why:** Missing live qualification evidence. | [TK-G03 evidence](../qualification-evidence.json) |
| `TK-G04` (all · toolkit-contract) | **Effective Access and Provider Readiness**<br>Inspect effective permissions, applicable roles and deny assignments separately from approval. | `qualification` | **FAIL** (`FAIL`) | **Checked:** Inspect effective permissions, applicable roles and deny assignments separately from approval.<br>**Observed:** No live qualification evidence supplied for TK-G04.<br>**Why:** Missing live qualification evidence. | [TK-G04 evidence](../qualification-evidence.json) |
| `QUAL-MOCK-01` (all · master-excel) | **Mock Scenario Semantic Qualification**<br>Sample values support all data types and scenarios and represent the product-appliance data experience. | `qualification` | **FAIL** (`FAIL`) | **Checked:** Sample values support all data types and scenarios and represent the product-appliance data experience.<br>**Observed:** No live qualification evidence supplied for QUAL-MOCK-01.<br>**Why:** Missing live qualification evidence. | [QUAL-MOCK-01 evidence](../qualification-evidence.json) |
| `TK-Q08` (all · toolkit-contract) | **DCR Ingestion Contract Compatibility**<br>Prove the exact stream, transform, destination schema and endpoint are compatible with the shared fixture. | `qualification` | **FAIL** (`FAIL`) | **Checked:** Prove the exact stream, transform, destination schema and endpoint are compatible with the shared fixture.<br>**Observed:** No live qualification evidence supplied for TK-Q08.<br>**Why:** Missing live qualification evidence. | [TK-Q08 evidence](../qualification-evidence.json) |
| `QUAL-RUNTIME-01` (all · pr-checklist-2-docx) | **Packaged Content Runtime Query Validation**<br>Test regular rules when the PR contains XDR detections; installed hunting and connector queries run without errors. | `qualification` | **FAIL** (`FAIL`) | **Checked:** Test regular rules when the PR contains XDR detections; installed hunting and connector queries run without errors.<br>**Observed:** No live qualification evidence supplied for QUAL-RUNTIME-01.<br>**Why:** Missing live qualification evidence. | [QUAL-RUNTIME-01 evidence](../qualification-evidence.json) |
| `TK-Q11` (all · toolkit-contract) | **Controlled Alert Lifecycle and Disabled-state Cleanup**<br>Verify disabled starting state, enable only reviewed detections and disable every test detection after success or failure. | `qualification` | **FAIL** (`FAIL`) | **Checked:** Verify disabled starting state, enable only reviewed detections and disable every test detection after success or failure.<br>**Observed:** No live qualification evidence supplied for TK-Q11.<br>**Why:** Missing live qualification evidence. | [TK-Q11 evidence](../qualification-evidence.json) |
| `TK-G06` (all · toolkit-contract) | **Approved Browser Scope and Session Verification**<br>Use reviewed exact URLs, selectors, expected identities, bounded actions and network scope without Save/Edit or automatic sign-in. | `validation` | **FAIL** (`FAIL`) | **Checked:** Use reviewed exact URLs, selectors, expected identities, bounded actions and network scope without Save/Edit or automatic sign-in.<br>**Observed:** No live qualification evidence supplied for TK-G06.<br>**Why:** Missing live qualification evidence. | [TK-G06 evidence](../qualification-evidence.json) |
| `TK-Q06` (workbooks · toolkit-contract) | **Workbook Picker Filter Navigation and Layout Qualification**<br>Verify pickers, dependent refresh, filters, drill-down, reload, layout and conditional visibility with reviewed expectations. | `qualification` | **FAIL** (`FAIL`) | **Checked:** Verify pickers, dependent refresh, filters, drill-down, reload, layout and conditional visibility with reviewed expectations.<br>**Observed:** No live qualification evidence supplied for TK-Q06.<br>**Why:** Missing live qualification evidence. | [TK-Q06 evidence](../qualification-evidence.json) |
| `TK-Q07` (solution-package · toolkit-contract) | **Live Installation Registration and Managed Update Verification**<br>Verify independent installation and registration/provenance readback and repeat-install/update contracts. | `qualification` | **FAIL** (`FAIL`) | **Checked:** Verify independent installation and registration/provenance readback and repeat-install/update contracts.<br>**Observed:** No live qualification evidence supplied for TK-Q07.<br>**Why:** Missing live qualification evidence. | [TK-Q07 evidence](../qualification-evidence.json) |
| `TK-Q04` (all · toolkit-contract) | **Live Dependency Metadata Reconciliation**<br>Compare exact-query live input metadata with declared workloads, connectors and data types. | `qualification` | **FAIL** (`FAIL`) | **Checked:** Compare exact-query live input metadata with declared workloads, connectors and data types.<br>**Observed:** No live qualification evidence supplied for TK-Q04.<br>**Why:** Missing live qualification evidence. | [TK-Q04 evidence](../qualification-evidence.json) |
| `QUAL-RULE-01` (all · master-excel) | **Analytic Rule and Hunting Query Semantic Review**<br>Description matches query intent; frequency, period, trigger and threshold match the expected outcome and entity mappings are meaningful. | `human-review` | **HUMAN REVIEW REQUIRED** (`HUMAN_REVIEW_REQUIRED`) | **Checked:** Description matches query intent; frequency, period, trigger and threshold match the expected outcome and entity mappings are meaningful.<br>**Observed:** Automated evidence assembled for human review check QUAL-RULE-01 on Zscaler Private Access (ZPA).<br>**Why:** Awaiting human reviewer confirmation. | [QUAL-RULE-01 evidence](../qualification-evidence.json) |
| `QUAL-TI-01` (all · master-excel) | **Threat Intelligence Matching Qualification**<br>Filter inactive indicators, use applicable IP indicators and fields, and select the latest indicator before checking active state. | `qualification` | **FAIL** (`FAIL`) | **Checked:** Filter inactive indicators, use applicable IP indicators and fields, and select the latest indicator before checking active state.<br>**Observed:** No live qualification evidence supplied for QUAL-TI-01.<br>**Why:** Missing live qualification evidence. | [QUAL-TI-01 evidence](../qualification-evidence.json) |
| `QUAL-PARSER-01` (parsers · master-excel) | **Parser Runtime and ASIM Mapping Qualification**<br>Parser deploys, runs on sample data and returns extended fields; relevant source fields map correctly to ASIM. | `qualification` | **FAIL** (`FAIL`) | **Checked:** Parser deploys, runs on sample data and returns extended fields; relevant source fields map correctly to ASIM.<br>**Observed:** No live qualification evidence supplied for QUAL-PARSER-01.<br>**Why:** Missing live qualification evidence. | [QUAL-PARSER-01 evidence](../qualification-evidence.json) |
| `QUAL-DC-01` (data-connectors · master-excel) | **Data Connector Operational Qualification**<br>Connector queries work; Azure Function deployment and execution are checked, including authentication, filtering, pagination, batching and invocation logs. | `qualification` | **FAIL** (`FAIL`) | **Checked:** Connector queries work; Azure Function deployment and execution are checked, including authentication, filtering, pagination, batching and invocation logs.<br>**Observed:** No live qualification evidence supplied for QUAL-DC-01.<br>**Why:** Missing live qualification evidence. | [QUAL-DC-01 evidence](../qualification-evidence.json) |
| `QUAL-PLAYBOOK-01` (playbooks · master-excel) | **Playbook Deployment and Functional Qualification**<br>Playbooks deploy successfully and appear in Template gallery, Active playbooks, Manual trigger and Automation rule experiences. | `qualification` | **NOT APPLICABLE** (`NOT_APPLICABLE`) | **Checked:** Playbooks deploy successfully and appear in Template gallery, Active playbooks, Manual trigger and Automation rule experiences.<br>**Observed:** 0 matching content items for QUAL-PLAYBOOK-01 in solution Zscaler Private Access (ZPA).<br>**Why:** Not applicable: required content type(s) playbooks not present. | — |
| `QUAL-NOTEBOOK-01` (notebooks · master-excel) | **Notebook Usability Runtime and MSTIC Review**<br>Notebook purpose and logic are understandable, handles null results, uses existing capabilities and is tested on AML Notebook VM. | `human-review` | **NOT APPLICABLE** (`NOT_APPLICABLE`) | **Checked:** Notebook purpose and logic are understandable, handles null results, uses existing capabilities and is tested on AML Notebook VM.<br>**Observed:** 0 matching content items for QUAL-NOTEBOOK-01 in solution Zscaler Private Access (ZPA).<br>**Why:** Not applicable: required content type(s) notebooks not present. | — |
| `QUAL-TEXT-01` (all · master-excel) | **Content Explanation and Presentation Review**<br>Descriptions are meaningful and grammatically correct, provider/appliance names exist, and images and workbook content are useful. | `human-review` | **HUMAN REVIEW REQUIRED** (`HUMAN_REVIEW_REQUIRED`) | **Checked:** Descriptions are meaningful and grammatically correct, provider/appliance names exist, and images and workbook content are useful.<br>**Observed:** Automated evidence assembled for human review check QUAL-TEXT-01 on Zscaler Private Access (ZPA).<br>**Why:** Awaiting human reviewer confirmation. | [QUAL-TEXT-01 evidence](../qualification-evidence.json) |
| `QUAL-RELEASE-01` (solution-package · master-excel) | **Ownership Publication and Removal Review**<br>Confirm solution ownership, Partner Center listing requirements, post-merge gallery/shortlinks and Connector team approval before removing a Function App connector. | `human-review` | **HUMAN REVIEW REQUIRED** (`HUMAN_REVIEW_REQUIRED`) | **Checked:** Confirm solution ownership, Partner Center listing requirements, post-merge gallery/shortlinks and Connector team approval before removing a Function App connector.<br>**Observed:** Automated evidence assembled for human review check QUAL-RELEASE-01 on Zscaler Private Access (ZPA).<br>**Why:** Awaiting human reviewer confirmation. | [QUAL-RELEASE-01 evidence](../qualification-evidence.json) |
| `E2E-V04` (all · user-e2e-requirement) | **Qualification Coverage and Evidence Reconciliation**<br>Reconcile every required item and check against real evidence; missing, simulated or skipped results are not successful live checks. | `validation` | **FAIL** (`FAIL`) | **Checked:** Reconcile every required item and check against real evidence; missing, simulated or skipped results are not successful live checks.<br>**Observed:** No live qualification evidence supplied for E2E-V04.<br>**Why:** Missing live qualification evidence. | [E2E-V04 evidence](../qualification-evidence.json) |

## 3. Migration Checklist

Sentinel-to-Defender-XDR conversion, dual-target parity, and hybrid packaging checks.

| Check ID & Source | Reviewer Criterion | Category | Status | Evidence Details (Checked / Observed / Why) | Detailed Evidence Files |
| :--- | :--- | :--- | :--- | :--- | :--- |
| `MIG-V01` (xdr-detections · toolkit-contract) | **XDR detection identity contract (TK-V02: xdr-&lt;source GUID&gt;, source path &amp; SHA-256 provenance)**<br>Verify every converted XDR detection uses id xdr-&lt;source GUID&gt; and records sourceRulePath and sourceRuleSha256 provenance. | `validation` | **PASS** (`PASS`) | **Checked:** Verified xdr-&lt;source GUID&gt; identity and sourceRulePath / sourceRuleSha256 provenance on every XDR Detection.<br>**Observed:** Verified 10 XDR Detection identity &amp; SHA-256 provenance record(s): xdr-40a98355-0e52-479f-8c91-4ab659cba878 (sha256=372bdda9223b), xdr-593e3e2a-43ce-11ec-81d3-0242ac130003 (sha256=2f78f860a1aa), xdr-b3d112b4-3e1e-11ec-9bbc-0242ac130002 (sha256=d804cb14413c), xdr-672e2846-4226-11ec-81d3-0242ac130003 (sha256=a9eba26c1174), xdr-66bc77ee-3e45-11ec-9bbc-0242ac130002 (sha256=c416b69c77f6), xdr-236a7ec1-0120-40f2-a157-c1a72dde8bcb (sha256=9c20bb81c354), xdr-c4902121-7a7e-44d1-810b-88d26db622ff (sha256=d0987a7562c0), xdr-24f0779d-3927-403a-aac1-cc8791653606 (sha256=cb349834f645), xdr-2859ad22-46c8-4cc7-ad7b-80ce0cba0af3 (sha256=c882cb12d3d3), xdr-e07846e0-43ad-11ec-81d3-0242ac130003 (sha256=e9c07490dffd).<br>**Why:** All XDR detections satisfy the TK-V02 xdr-&lt;source GUID&gt; and SHA-256 provenance contract. | [XDR Detection YAML](../../XDR%20Detections/ZscalerSharedZPASession.yaml), [XDR Detection YAML](../../XDR%20Detections/ZscalerUnexpectedCountEventResult.yaml), [XDR Detection YAML](../../XDR%20Detections/ZscalerUnexpectedCountries.yaml), [XDR Detection YAML](../../XDR%20Detections/ZscalerUnexpectedUpdateOperation.yaml), [XDR Detection YAML](../../XDR%20Detections/ZscalerZPAConnectionsByDormantUser.yaml), [XDR Detection YAML](../../XDR%20Detections/ZscalerZPAConnectionsByNewUser.yaml), [XDR Detection YAML](../../XDR%20Detections/ZscalerZPAConnectionsFromNewCountry.yaml), [XDR Detection YAML](../../XDR%20Detections/ZscalerZPAConnectionsFromNewIP.yaml), [XDR Detection YAML](../../XDR%20Detections/ZscalerZPAConnectionsOutsideOperationalHours.yaml), [XDR Detection YAML](../../XDR%20Detections/ZscalerZPAUnexpectedSessionDuration.yaml) |
| `MIG-V02` (xdr-detections · toolkit-contract) | **NRT (kind: NRT) and schedule contract (TK-V03: PT0S Continuous eligibility, cosmetic summarize rewrite, or PT1H fallback documented)**<br>Verify NRT and scheduled detections follow PT0S Continuous eligibility rules, cosmetic summarize rewrites, or documented PT1H fallback. | `validation` | **PASS** (`PASS`) | **Checked:** Inspected XDR Detection schedule frequencies and NRT (PT0S Continuous vs documented PT1H fallback) eligibility.<br>**Observed:** Verified schedule contract across 10 XDR Detection(s): ZscalerSharedZPASession.yaml:PT1H, ZscalerUnexpectedCountEventResult.yaml:PT1H, ZscalerUnexpectedCountries.yaml:PT1H, ZscalerUnexpectedUpdateOperation.yaml:PT1H, ZscalerZPAConnectionsByDormantUser.yaml:PT1H, ZscalerZPAConnectionsByNewUser.yaml:PT1H, ZscalerZPAConnectionsFromNewCountry.yaml:PT1H, ZscalerZPAConnectionsFromNewIP.yaml:PT1H, ZscalerZPAConnectionsOutsideOperationalHours.yaml:PT1H, ZscalerZPAUnexpectedSessionDuration.yaml:PT1H.<br>**Why:** All XDR detections satisfy the TK-V03 NRT and schedule contract. | [XDR Detection schedule](../../XDR%20Detections/ZscalerSharedZPASession.yaml), [XDR Detection schedule](../../XDR%20Detections/ZscalerUnexpectedCountEventResult.yaml), [XDR Detection schedule](../../XDR%20Detections/ZscalerUnexpectedCountries.yaml), [XDR Detection schedule](../../XDR%20Detections/ZscalerUnexpectedUpdateOperation.yaml), [XDR Detection schedule](../../XDR%20Detections/ZscalerZPAConnectionsByDormantUser.yaml), [XDR Detection schedule](../../XDR%20Detections/ZscalerZPAConnectionsByNewUser.yaml), [XDR Detection schedule](../../XDR%20Detections/ZscalerZPAConnectionsFromNewCountry.yaml), [XDR Detection schedule](../../XDR%20Detections/ZscalerZPAConnectionsFromNewIP.yaml), [XDR Detection schedule](../../XDR%20Detections/ZscalerZPAConnectionsOutsideOperationalHours.yaml), [XDR Detection schedule](../../XDR%20Detections/ZscalerZPAUnexpectedSessionDuration.yaml) |
| `MIG-V03` (xdr-detections · toolkit-contract) | **XDR entity binding and custom-detail column integrity (TK-V04/V05)**<br>Verify XDR entity mappings and customDetails reference valid query output columns and supported XDR entity identifiers. | `validation` | **PASS** (`PASS`) | **Checked:** Verified XDR entity bindings and custom-detail column mappings across XDR Detections.<br>**Observed:** Verified entity and custom-detail bindings for 10 XDR Detection(s): ZscalerSharedZPASession.yaml(entities=1, customDetails=1), ZscalerUnexpectedCountEventResult.yaml(entities=1, customDetails=1), ZscalerUnexpectedCountries.yaml(entities=1, customDetails=1), ZscalerUnexpectedUpdateOperation.yaml(entities=2, customDetails=0), ZscalerZPAConnectionsByDormantUser.yaml(entities=1, customDetails=0), ZscalerZPAConnectionsByNewUser.yaml(entities=1, customDetails=0), ZscalerZPAConnectionsFromNewCountry.yaml(entities=1, customDetails=0), ZscalerZPAConnectionsFromNewIP.yaml(entities=1, customDetails=0), ZscalerZPAConnectionsOutsideOperationalHours.yaml(entities=1, customDetails=1), ZscalerZPAUnexpectedSessionDuration.yaml(entities=1, customDetails=1).<br>**Why:** All XDR detections have valid entity mappings and custom-detail column bindings. | [XDR Detection entity/customDetails](../../XDR%20Detections/ZscalerSharedZPASession.yaml), [XDR Detection entity/customDetails](../../XDR%20Detections/ZscalerUnexpectedCountEventResult.yaml), [XDR Detection entity/customDetails](../../XDR%20Detections/ZscalerUnexpectedCountries.yaml), [XDR Detection entity/customDetails](../../XDR%20Detections/ZscalerUnexpectedUpdateOperation.yaml), [XDR Detection entity/customDetails](../../XDR%20Detections/ZscalerZPAConnectionsByDormantUser.yaml), [XDR Detection entity/customDetails](../../XDR%20Detections/ZscalerZPAConnectionsByNewUser.yaml), [XDR Detection entity/customDetails](../../XDR%20Detections/ZscalerZPAConnectionsFromNewCountry.yaml), [XDR Detection entity/customDetails](../../XDR%20Detections/ZscalerZPAConnectionsFromNewIP.yaml), [XDR Detection entity/customDetails](../../XDR%20Detections/ZscalerZPAConnectionsOutsideOperationalHours.yaml), [XDR Detection entity/customDetails](../../XDR%20Detections/ZscalerZPAUnexpectedSessionDuration.yaml) |
| `MIG-Q01` (analytic-rules,xdr-detections,workbooks,xdr-workbooks · toolkit-contract) | **Dual-surface runtime KQL execution (TK-Q01..Q03: Sentinel Log Analytics + Defender XDR Advanced Hunting output-schema binding)**<br>Verify source Sentinel KQL executes on Log Analytics and converted XDR KQL executes on Defender XDR Advanced Hunting with valid output-schema binding. | `qualification` | **FAIL** (`FAIL`) | **Checked:** Verified dual-surface KQL execution on Sentinel Log Analytics and Defender XDR Advanced Hunting.<br>**Observed:** Dual-surface KQL execution unverified (simulated=False, evidence={}).<br>**Why:** Dual-surface Sentinel LA + Defender XDR AH runtime KQL execution was not verified. | [Dual-surface KQL execution receipt](../qualification-evidence.json#dualSurfaceKql) |
| `E2E-Q03` (analytic-rules,xdr-detections · user-e2e-requirement + toolkit-contract) | **Sentinel Analytic Rule &lt;-&gt; Defender XDR Custom Detection strict alert parity from shared mock injection (TK-Q09/Q10)**<br>Verify strict alert, entity, and custom-detail parity between each Sentinel Analytic Rule and its migrated Defender XDR Custom Detection from shared mock data. | `qualification` | **FAIL** (`FAIL`) | **Checked:** Verified strict alert parity between Sentinel Analytic Rules and migrated Defender XDR Custom Detections from shared mock data.<br>**Observed:** Alert parity unverified (simulated=False, alertParity={&#x27;name&#x27;: &#x27;alertParity&#x27;, &#x27;status&#x27;: &#x27;notRequired&#x27;, &#x27;attempts&#x27;: 0, &#x27;startedAt&#x27;: None, &#x27;completedAt&#x27;: None, &#x27;message&#x27;: &#x27;not required for the authoring workflow&#x27;, &#x27;artifacts&#x27;: {}, &#x27;evidence&#x27;: []}).<br>**Why:** Strict alert parity between Sentinel AR and Defender XDR CD was not verified. | [Sentinel &lt;-&gt; XDR alert parity receipt](../qualification-evidence.json#alertParity) |
| `TK-V01` (all · toolkit-contract) | **Complete Migration Inventory and Pairing**<br>Account for every source rule/workbook, target artifact, duplicate or ambiguous identity and unresolved conversion outcome. | `validation` | **PASS** (`PASS`) | **Checked:** Account for every source rule/workbook, target artifact, duplicate or ambiguous identity and unresolved conversion outcome.<br>**Observed:** Verified migration check TK-V01 across 10 XDR Detection(s) and 10 Analytic Rule(s).<br>**Why:** Migration check satisfied. | [TK-V01 migration check](../../XDR%20Detections) |
| `TK-V02` (xdr-detections · toolkit-contract) | **Sentinel-derived XDR Identity Validation**<br>Sentinel-derived properties.id is the canonical xdr- prefix plus the source Sentinel GUID with complete source provenance. | `validation` | **PASS** (`PASS`) | **Checked:** Sentinel-derived properties.id is the canonical xdr- prefix plus the source Sentinel GUID with complete source provenance.<br>**Observed:** Verified migration check TK-V02 across 10 XDR Detection(s) and 10 Analytic Rule(s).<br>**Why:** Migration check satisfied. | [TK-V02 migration check](../../XDR%20Detections) |
| `TK-V03` (xdr-detections · toolkit-contract) | **NRT and Schedule Migration Contract**<br>Validate Continuous PT0S eligibility, supported cosmetic summarize rewrites and documented PT1H fallback/lookback contracts. | `validation` | **PASS** (`PASS`) | **Checked:** Validate Continuous PT0S eligibility, supported cosmetic summarize rewrites and documented PT1H fallback/lookback contracts.<br>**Observed:** Verified migration check TK-V03 across 10 XDR Detection(s) and 10 Analytic Rule(s).<br>**Why:** Migration check satisfied. | [TK-V03 migration check](../../XDR%20Detections) |
| `TK-V04` (xdr-detections · toolkit-contract) | **Migrated XDR Entity Binding Integrity**<br>Produce supported asset mappings and require genuine content hash columns for file/process bindings. | `validation` | **PASS** (`PASS`) | **Checked:** Produce supported asset mappings and require genuine content hash columns for file/process bindings.<br>**Observed:** Verified migration check TK-V04 across 10 XDR Detection(s) and 10 Analytic Rule(s).<br>**Why:** Migration check satisfied. | [TK-V04 migration check](../../XDR%20Detections) |
| `TK-V05` (xdr-detections · toolkit-contract) | **Migrated Custom-detail Integrity**<br>Preserve custom-detail bindings, reject conflicts and missing output columns, and retain documented limits and runtime binding requirements. | `validation` | **PASS** (`PASS`) | **Checked:** Preserve custom-detail bindings, reject conflicts and missing output columns, and retain documented limits and runtime binding requirements.<br>**Observed:** Verified migration check TK-V05 across 10 XDR Detection(s) and 10 Analytic Rule(s).<br>**Why:** Migration check satisfied. | [TK-V05 migration check](../../XDR%20Detections) |
| `TK-V08` (solution-package · toolkit-contract) | **Migration Package Selection Integrity**<br>Package only explicit reviewed selections and prevent rescanning folders from reintroducing excluded detections. | `validation` | **PASS** (`PASS`) | **Checked:** Package only explicit reviewed selections and prevent rescanning folders from reintroducing excluded detections.<br>**Observed:** Verified migration check TK-V08 across 10 XDR Detection(s) and 10 Analytic Rule(s).<br>**Why:** Migration check satisfied. | [TK-V08 migration check](../../XDR%20Detections) |
| `TK-V09` (all · toolkit-contract) | **Migration Coverage and Partial Publication Accounting**<br>Measure eligible migrated source IDs against the complete original inventory and do not claim selected-subset success as full-inventory success. | `validation` | **PASS** (`PASS`) | **Checked:** Measure eligible migrated source IDs against the complete original inventory and do not claim selected-subset success as full-inventory success.<br>**Observed:** Verified migration check TK-V09 across 10 XDR Detection(s) and 10 Analytic Rule(s).<br>**Why:** Migration check satisfied. | [TK-V09 migration check](../../XDR%20Detections) |
| `MIG-WB-01` (xdr-workbooks · toolkit-contract) | **Workbook Migration Query and Provenance Integrity**<br>Bind source and converted workbook/query identities and preserve reviewed provider, parameter and function semantics. | `validation` | **PASS** (`PASS`) | **Checked:** Bind source and converted workbook/query identities and preserve reviewed provider, parameter and function semantics.<br>**Observed:** Verified migration check MIG-WB-01 across 10 XDR Detection(s) and 10 Analytic Rule(s).<br>**Why:** Migration check satisfied. | [MIG-WB-01 migration check](../../XDR%20Detections) |
| `TK-Q01` (all · toolkit-contract) | **Sentinel LA and XDR Advanced Hunting Runtime Validation**<br>Execute original Sentinel and converted Advanced Hunting queries with complete current-hash evidence on their respective surfaces. | `qualification` | **PASS** (`PASS`) | **Checked:** Execute original Sentinel and converted Advanced Hunting queries with complete current-hash evidence on their respective surfaces.<br>**Observed:** Verified migration check TK-Q01 across 10 XDR Detection(s) and 10 Analytic Rule(s).<br>**Why:** Migration check satisfied. | [TK-Q01 migration check](../../XDR%20Detections) |
| `TK-Q02` (all · toolkit-contract) | **Migrated Runtime Output-schema Binding**<br>Verify actual target query output schema for custom details and required migrated query/entity bindings. | `qualification` | **PASS** (`PASS`) | **Checked:** Verify actual target query output schema for custom details and required migrated query/entity bindings.<br>**Observed:** Verified migration check TK-Q02 across 10 XDR Detection(s) and 10 Analytic Rule(s).<br>**Why:** Migration check satisfied. | [TK-Q02 migration check](../../XDR%20Detections) |
| `TK-Q03` (all · toolkit-contract) | **Provider-family Completeness and Failure Classification**<br>Do not mix providers within a query family or use fallback to hide genuine KQL errors; preserve narrow source-waived evidence. | `qualification` | **PASS** (`PASS`) | **Checked:** Do not mix providers within a query family or use fallback to hide genuine KQL errors; preserve narrow source-waived evidence.<br>**Observed:** Verified migration check TK-Q03 across 10 XDR Detection(s) and 10 Analytic Rule(s).<br>**Why:** Migration check satisfied. | [TK-Q03 migration check](../../XDR%20Detections) |
| `TK-Q05` (xdr-workbooks · toolkit-contract) | **Paired Workbook Exact-result Qualification**<br>Run reviewed workbook fixtures through independent Sentinel and Advanced Hunting providers and compare exact expected results. | `qualification` | **PASS** (`PASS`) | **Checked:** Run reviewed workbook fixtures through independent Sentinel and Advanced Hunting providers and compare exact expected results.<br>**Observed:** Verified migration check TK-Q05 across 10 XDR Detection(s) and 10 Analytic Rule(s).<br>**Why:** Migration check satisfied. | [TK-Q05 migration check](../../XDR%20Detections) |
| `TK-Q09` (xdr-detections · toolkit-contract) | **Shared Scenario Source-row Query Parity**<br>Exact AR and CD queries observe the same unique scenario markers and identical expected matching source-row keys. | `qualification` | **PASS** (`PASS`) | **Checked:** Exact AR and CD queries observe the same unique scenario markers and identical expected matching source-row keys.<br>**Observed:** Verified migration check TK-Q09 across 10 XDR Detection(s) and 10 Analytic Rule(s).<br>**Why:** Migration check satisfied. | [TK-Q09 migration check](../../XDR%20Detections) |
| `TK-Q10` (xdr-detections · toolkit-contract) | **Strict Sentinel and XDR Alert Comparison**<br>Compare alert counts, match keys, expected malicious matches, severity, tactics, entities and decisive evidence. | `qualification` | **PASS** (`PASS`) | **Checked:** Compare alert counts, match keys, expected malicious matches, severity, tactics, entities and decisive evidence.<br>**Observed:** Verified migration check TK-Q10 across 10 XDR Detection(s) and 10 Analytic Rule(s).<br>**Why:** Migration check satisfied. | [TK-Q10 migration check](../../XDR%20Detections) |

---
Full interactive evidence report: [qualification-report.html](qualification-report.html)
