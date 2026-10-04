# AI Coding Structure Reference

**Status:** high-level document structure and tagged skeletons  
**Classification catalogue:** populated  
**Rules, selection decisions, examples, and verification details:** placeholders  
**Implementation level:** conceptual; no working code

## Document layout

| Section | Purpose |
| --- | --- |
| 1. Purpose and scope | Define audience, intended use, authority, and exclusions |
| 2. Classification catalogue | Reference paradigms, models, styles, techniques, and approaches |
| 3. Structural vocabulary and tags | Identify elements, characteristics, and relationships |
| 4. Pattern selection | Reserve suitability, tradeoffs, and combination criteria |
| 5. Tagged skeleton catalogue | Show a common entry format and high-level pattern structures |
| 6. Structural and behavioural rules | Reserve rules for boundaries, dependencies, contracts, and execution |
| 7. Examples and prohibited structures | Reserve examples and counterexamples |
| 8. Verification | Reserve checks and expected evidence |
| 9. References and provenance | Identify sources and local conventions |

## 1. Purpose and scope

This standalone document provides a classification reference and a high-level outline for AI coding structure guidance. The classification catalogue is populated. The remaining sections use placeholders and conceptual skeletons.

| Field | Placeholder |
| --- | --- |
| Intended audience | <AUDIENCE> |
| Intended use | <USE_CASES> |
| Supported languages and environments | <LANGUAGES_AND_ENVIRONMENTS> |
| Project authority and precedence | <AUTHORITY_RULES> |
| Scope and exclusions | <SCOPE_AND_EXCLUSIONS> |

Placeholders are unresolved fields, not instructions to invent implementation details. A later project or reference revision supplies their values.

The classification is a working reference, not a normative taxonomy. Concepts may have multiple classifications. Grouping does not automatically imply inheritance.

## 2. Classification catalogue

### 2.1 Classification dimensions

| Dimension | Describes | Question answered |
| --- | --- | --- |
| Paradigm | Principles used to formulate computation | What approach to computation is used? |
| Programming model | Abstract machinery, interactions, and rules presented to the programmer | How is computation represented and executed? |
| Programming style | Organization and expression of programs | How is the code structured and written? |
| Programming technique | Concrete mechanisms used to implement behaviour | What mechanisms implement the behaviour? |
| Design / development approach | Methods used to design, develop, and validate software | How is the software conceived, built, and checked? |

These are classification dimensions, not levels in a single inheritance hierarchy. A system can combine several paradigms, models, styles, techniques, and development approaches.

### 2.2 Programming paradigms

Programming paradigms describe broad approaches to expressing computation. Some entries also describe architectural orientations or specialized computation families.

| Family or orientation | Related concepts and specializations |
| --- | --- |
| Imperative | Procedural; Structured; Modular; Object-Oriented |
| Declarative | Functional; Logic; Constraint; Rule-Based; Query; Relational; Dataflow |
| Functional | Pure Functional; Impure Functional; Higher-Order; Point-Free; Tacit; Functional-Reactive |
| Object-Oriented | Class-Based; Prototype-Based; Object-Based; Message-Oriented |
| Concurrent | Shared-Memory; Message-Passing; Actor; Communicating Processes; Dataflow |
| Parallel | Data-Parallel; Task-Parallel; Pipeline-Parallel |
| Reactive | Reactive programming |
| Event-Driven | Event-driven programming |
| Data-Oriented | Data-oriented programming |
| Data-Driven | Data-driven programming |
| Agent-Oriented | Agent-oriented programming |
| Aspect-Oriented | Aspect-oriented programming |
| Component-Oriented | Component-oriented programming |
| Service-Oriented | Service-oriented programming |
| Protocol-Oriented | Protocol-oriented programming |
| Language-Oriented | Language-oriented programming |
| Intentional | Intentional programming |
| Generic | Generic programming |
| Metaprogramming | Programs that generate, inspect, or transform programs |
| Differentiable | Differentiable programming |
| Probabilistic | Probabilistic programming |
| Quantum | Quantum programming |
| Symbolic | Symbolic programming |

#### Classification notes

- Functional programming can be classified under declarative programming and also treated as a major family in its own right.
- Object-oriented programming often uses imperative behaviour, but object orientation does not require a purely imperative implementation.
- Object-based programming is included as a related concept; it is not universally treated as a full object-oriented subtype.
- Point-free and tacit are closely related terms. Record their relationship explicitly rather than assuming they identify independent paradigms.
- Concurrent and parallel describe different concerns: managing interacting computations and executing computations simultaneously.
- Component, service, and protocol orientations also belong in architectural and design classifications.
- Generic programming and metaprogramming can describe broad approaches as well as concrete techniques.

### 2.3 Programming models

Programming models describe the conceptual computation machinery available to the programmer: execution units, memory, communication, coordination, evaluation, and processing.

#### Execution organization

| Model | Focus |
| --- | --- |
| Sequential | Ordered execution |
| Concurrent | Multiple computations whose progress overlaps |
| Parallel | Simultaneous computation |
| Distributed | Computation across communicating execution locations |

#### Memory models

| Group | Concepts |
| --- | --- |
| Memory organization and access | Shared Memory; Distributed Memory; Partitioned Global Address Space |
| Transactional access | Transactional Memory |
| Memory consistency and ordering | Memory Consistency Model; Memory Ordering |

Memory organization and memory consistency are distinct concerns. Record them separately when precision matters.

#### Communication models

- Message Passing
- Actor Model
- Communicating Sequential Processes (CSP)
- Channels
- Publish/Subscribe
- Tuple Space
- Mailbox
- Remote Invocation

#### Execution units and control abstractions

- Thread
- Process
- Event Loop
- Coroutine
- Fiber
- Green Thread
- Task
- Future/Promise
- Continuation

These entries are execution abstractions and mechanisms within programming models; they are not all complete models independently.

#### Dataflow models

- Static Dataflow
- Dynamic Dataflow
- Synchronous Dataflow
- Reactive Dataflow

#### Parallel execution and programming classifications

| Concern | Concepts |
| --- | --- |
| Execution architecture or execution arrangement | Single Instruction, Multiple Data (SIMD); Single Instruction, Multiple Threads (SIMT); Multiple Instruction, Multiple Data (MIMD) |
| Program organization | Single Program, Multiple Data (SPMD); Multiple Program, Multiple Data (MPMD) |
| Coordination and computation patterns | Fork-Join; Bulk Synchronous Parallel; MapReduce |

These groups are related but should retain their distinct classifications.

#### Processing, evaluation, and specialized computation

- Stream Processing
- Pipeline Processing
- Batch Processing
- Event Processing
- Reactive Streams
- Cellular Automata
- State-Machine
- Petri-Net
- Rule/Evaluation
- Constraint-Solving
- Logic-Inference
- Query/Evaluation
- Graph Computation
- GPU/Accelerator
- Quantum Circuit

GPU/accelerator identifies an execution target or platform concern. Associate it with the relevant programming model rather than treating all accelerator programming as one model.

### 2.4 Programming styles

Programming styles describe how programs are organized and expressed. The following groups also include practices and principles that commonly influence coding style.

| Concern | Concepts |
| --- | --- |
| General organization and expression | Procedural; Structured; Modular; Object-Oriented; Functional; Declarative; Imperative |
| Abstraction and composition | Component-Based; Interface-Driven; Contract-Driven; Protocol-Oriented; Trait-Based; Mixin-Based; Composition-Oriented |
| Data, models, and configuration | Data-Oriented; Data-Driven; Table-Driven; Metadata-Driven; Schema-Driven; Model-Driven; Configuration-Driven; Convention-Driven |
| Events, messages, and flow | Event-Driven; Message-Driven; Reactive; Stream-Oriented; Pipeline-Oriented; Flow-Based |
| State, rules, and constraints | State-Oriented; State-Machine-Based; Rule-Based; Constraint-Based |
| Extension and integration | Plugin-Based; Extension-Oriented; Callback-Based; Hook-Based; Middleware-Based |
| Structural organization and control | Layered; Hierarchical; Recursive; Iterative |
| Design sequencing and source of authority | API-First; Contract-First; Schema-First; Code-First; Model-First |
| Development orientation | Domain-Driven; Test-Driven; Behaviour-Driven; Specification-Driven; Property-Driven |
| Robustness and design principles | Defensive; Fail-Fast; Design-by-Contract; Secure-by-Design |
| Surface expression | Fluent; Point-Free; Expression-Oriented; Statement-Oriented; Literate Programming |

#### Classification notes

- API-first, contract-first, and schema-first primarily describe design sequencing; they can also influence code style.
- Test-driven and behaviour-driven primarily describe development approaches.
- Secure-by-design is a design principle with implications beyond code expression.
- Recursive and iterative identify control strategies as well as stylistic choices.
- Property-driven is context-dependent; distinguish the intended use from property-based testing or verification.

### 2.5 Programming techniques

Programming techniques are mechanisms that can be used within multiple paradigms, models, styles, and design approaches.

| Concern | Techniques, mechanisms, and associated properties |
| --- | --- |
| Control Flow | Sequence; Selection; Iteration; Recursion; Tail Recursion; Mutual Recursion; Pattern Matching; Dispatch; Continuation Passing |
| Abstraction | Encapsulation; Information Hiding; Generalization; Specialization; Parameterization; Generic Programming; Type Abstraction; Interface Abstraction |
| Composition | Function Composition; Object Composition; Delegation; Forwarding; Chaining; Pipelining; Combinators |
| Reuse | Inheritance; Composition; Mixins; Traits; Templates; Generics; Macros; Code Generation |
| Type behaviour and runtime adaptation | Polymorphism; Dynamic Dispatch; Multiple Dispatch; Duck Typing; Reflection; Introspection; Intercession; Runtime Code Generation |
| Functional | Higher-Order Functions; First-Class Functions; Closures; Currying; Partial Application; Function Composition; Immutability; Referential Transparency; Lazy Evaluation; Memoization |
| Asynchronous | Callbacks; Futures; Promises; Async/Await; Coroutines; Generators; Channels; Event Loops |
| Concurrent | Threads; Processes; Actors; Message Passing; Locks; Mutexes; Semaphores; Monitors; Barriers; Atomics; Lock-Free Algorithms; Transactional Memory |
| Data | Serialization; Deserialization; Mapping; Filtering; Reduction; Folding; Transformation; Partitioning; Indexing; Caching |
| State | Mutable State; Immutable State; State Machines; State Transition Tables; Event Sourcing; Snapshotting; State Reduction |
| Error handling and correctness | Exceptions; Error Codes; Result Types; Option/Maybe Types; Assertions; Preconditions; Postconditions; Invariants; Retry; Recovery; Compensation |
| Metaprogramming | Macros; Templates; Reflection; Introspection; Annotations; Attributes; Decorators; Code Generation; AST Transformation; Compile-Time Evaluation; Partial Evaluation |

#### Classification notes

- Polymorphism can be static or dynamic; it does not belong exclusively to dynamic behaviour.
- First-class functions are a language capability; higher-order functions use functions as arguments or results.
- Immutability and referential transparency are properties associated with functional techniques.
- Generators and coroutines can support synchronous as well as asynchronous execution.
- Preconditions, postconditions, and invariants are contract or correctness conditions.
- Annotations, attributes, and decorators have language-specific meanings. Their presence does not automatically imply program transformation.
- Abstract Syntax Tree (AST) transformation operates on a structural representation of program syntax.

### 2.6 Design and development approaches

These approaches govern software design, construction, or validation. Some also identify architectural styles.

| Concern | Approaches |
| --- | --- |
| Core design orientation | Object-Oriented Design; Functional Design; Data-Oriented Design; Domain-Driven Design |
| Models and engineering | Model-Driven Development; Model-Driven Engineering |
| Components and services | Component-Based Development; Component-Based Software Engineering; Service-Oriented Design |
| Interfaces and contracts | API-First Design; Contract-First Design; Schema-First Design; Interface-Driven Design |
| Events, messages, and processing | Event-Driven Design; Message-Driven Design; Reactive Design; Flow-Based Design; Pipeline Design |
| Extension architecture | Plugin Architecture; Extensible Architecture |
| Development and validation | Test-Driven Development; Behaviour-Driven Development; Acceptance-Test-Driven Development; Property-Based Development; Specification-Driven Development |

Property-based development should be defined for the intended context. Use the more specific term “Property-Based Testing” when test generation and property checking are the actual subject.


## 3. Structural vocabulary and tags

### 3.1 Structural concept groups

| Group | Seed concepts |
| --- | --- |
| Units | System; Subsystem; Component; Module; Package; Namespace; Class; Function; Artifact |
| Boundaries and contracts | Boundary; Interface; Port; Protocol; Contract; Schema; API |
| Responsibilities and ownership | Role; Responsibility; Concern; Owner; State; Resource; Lifecycle |
| Connections and behaviour | Dependency; Composition; Delegation; Call; Message; Event; Flow; Transition |
| Variation | Extension Point; Hook; Plugin; Adapter; Strategy; Configuration |
| Rules and evidence | Constraint; Invariant; Precondition; Postcondition; Verification; Evidence |

### 3.2 Proposed tag families

| Tag | Describes | Placeholder |
| --- | --- | --- |
| kind | Structural category | <ELEMENT_KIND> |
| role | Architectural role | <ROLE> |
| concern | Responsibility area | <CONCERN> |
| boundary | Position relative to a named boundary | <BOUNDARY_POSITION> |
| state | State characteristic | <STATE_CHARACTERISTIC> |
| execution | Execution assumption | <EXECUTION_MODEL> |
| extension | Participation in an extension mechanism | <EXTENSION_ROLE> |

Use a mapping for tags. Keep identity, responsibility, ownership, contracts, and relationships in explicit fields. These tags are a proposed local convention, not a language or framework standard.

Tags describe characteristics; they do not establish dependency direction or enforce rules. Omitted and unresolved values must not be interpreted as established defaults.

### 3.3 Semantic relationships

Use explicit relationships instead of interpreting every grouping as inheritance.

| Relationship | Meaning | Example |
| --- | --- | --- |
| `is-a` | A genuine subtype or specialization | Pure Functional Programming is-a Functional Programming |
| `classified-as` | Membership in a classification dimension or category | Actor Model classified-as Communication Model |
| `grouped-under` | Placement in an organizational view | Recursion grouped-under Control Flow |
| `uses` | Employment of another concept | An actor-based application uses Message Passing |
| `realizes` | A concrete realization of an abstraction | A runtime realizes a programming model |
| `implements` | Implementation of a specified interface, contract, or mechanism | A module implements an interface |
| `has-property` | A characteristic of a concept or artifact | A function has-property Referential Transparency |
| `constrained-by` | A governing rule or condition | An operation constrained-by a precondition |
| `related-to` | An association whose precise relationship has not yet been established | Point-Free related-to Tacit |

Prefer a precise relationship when one is known. Keep unresolved associations distinguishable from confirmed subtype, implementation, or equivalence relationships.

### 3.4 Representation rules

1. Give each concept one stable identity.
2. Allow multiple classification relationships for that identity.
3. Distinguish a concept from its label, abbreviation, and alias.
4. Treat section groupings as navigational views unless a subtype relationship is stated explicitly.
5. Distinguish paradigms, models, styles, techniques, properties, language capabilities, platforms, and development practices.
6. Qualify ambiguous terms with their context.
7. Record genuine equivalence explicitly; similar labels do not establish equivalence.
8. Preserve the direction and meaning of each relationship.

“Functional” can name a family, describe a style, or qualify a design approach. Shared wording does not prove that every qualified concept is identical. Use one identity for the same concept, and separate identities for distinct concepts linked by explicit relationships.

### 3.5 Classification example

An actor-based distributed application might be described as follows:

| Dimension | Selected concepts |
| --- | --- |
| Paradigm | Concurrent; Object-Oriented |
| Programming model | Actor Model; Distributed; Message Passing |
| Programming style | Message-Driven; Interface-Driven |
| Programming technique | Mailboxes; Asynchronous Calls; Pattern Matching |
| Design / development approach | Contract-First Design; Test-Driven Development |

These selections describe compatible aspects of one application. They do not establish a chain of inheritance between the concepts.

### 3.6 Underlying structure and views

The semantic reference is a graph of concepts and typed relationships. Tables, trees, and other grouped presentations are views of that graph.

A concept can have multiple classifications without duplicating its identity or forcing every relationship into an `is-a` hierarchy.


## 4. Pattern selection placeholders

| Pattern | Intent | Use when | Avoid when | Tradeoffs | Compatible combinations |
| --- | --- | --- | --- | --- | --- |
| Layered | <INTENT> | <USE_WHEN> | <AVOID_WHEN> | <TRADEOFFS> | <COMBINATIONS> |
| Hexagonal / Ports and Adapters | <INTENT> | <USE_WHEN> | <AVOID_WHEN> | <TRADEOFFS> | <COMBINATIONS> |
| Pipeline / Pipes and Filters | <INTENT> | <USE_WHEN> | <AVOID_WHEN> | <TRADEOFFS> | <COMBINATIONS> |
| Plugin / Extension | <INTENT> | <USE_WHEN> | <AVOID_WHEN> | <TRADEOFFS> | <COMBINATIONS> |
| <ADDITIONAL_PATTERN> | <INTENT> | <USE_WHEN> | <AVOID_WHEN> | <TRADEOFFS> | <COMBINATIONS> |

## 5. Tagged skeleton catalogue

### 5.1 Common entry structure

Each pattern entry follows the same layout:

| Field | Placeholder content |
| --- | --- |
| Identity | <PATTERN_ID>, <TITLE>, <REVISION> |
| Intent | <PROBLEM_ADDRESSED> |
| Classification | <PARADIGMS>, <MODELS>, <STYLES>, <TECHNIQUES>, <APPROACHES> |
| Selection | <USE_WHEN>, <AVOID_WHEN>, <TRADEOFFS>, <ASSUMPTIONS> |
| Components | <COMPONENT_IDS>, <TAGS>, <RESPONSIBILITIES> |
| Contracts | <INPUTS>, <OUTPUTS>, <INTERFACES>, <ERRORS>, <INVARIANTS> |
| Relationships | <SOURCE>, <RELATION>, <TARGET> |
| Ownership and lifecycle | <STATE_OWNER>, <RESOURCE_OWNER>, <LIFECYCLE> |
| Constraints | <REQUIRED_STRUCTURES>, <PROHIBITED_STRUCTURES> |
| Variation points | <REPLACEABLE_PARTS>, <EXTENSION_POINTS> |
| Verification | <CHECKS>, <EXPECTED_EVIDENCE> |

### 5.2 Generic tagged skeleton

The YAML is documentation notation. It is not executable configuration or a finalized validation schema. Placeholders are quoted so they remain literal values.

```yaml
id: "<PATTERN_ID>"
title: "<PATTERN_TITLE>"
revision: "<REFERENCE_REVISION>"
intent: "<INTENT>"

classification:
  paradigms: ["<PARADIGM>"]
  models: ["<MODEL>"]
  styles: ["<STYLE>"]
  techniques: ["<TECHNIQUE>"]
  approaches: ["<DESIGN_OR_DEVELOPMENT_APPROACH>"]

selection:
  use_when: "<USE_WHEN>"
  avoid_when: "<AVOID_WHEN>"
  tradeoffs: "<TRADEOFFS>"
  assumptions: "<ASSUMPTIONS>"

components:
  - id: "<COMPONENT_ID>"
    tags:
      kind: "<ELEMENT_KIND>"
      role: "<ROLE>"
      concern: "<CONCERN>"
      boundary: "<BOUNDARY_POSITION>"
      state: "<STATE_CHARACTERISTIC>"
      execution: "<EXECUTION_MODEL>"
      extension: "<EXTENSION_ROLE>"
    responsibility: "<RESPONSIBILITY>"
    contracts:
      inputs: "<INPUT_CONTRACT>"
      outputs: "<OUTPUT_CONTRACT>"
      interfaces: "<INTERFACE_CONTRACT>"
      errors: "<ERROR_CONTRACT>"
      invariants: "<INVARIANTS>"
    state_owner: "<STATE_OWNER>"
    resource_owner: "<RESOURCE_OWNER>"
    lifecycle: "<LIFECYCLE>"

relationships:
  - from: "<SOURCE_ID>"
    relation: "<RELATION_TYPE>"
    to: "<TARGET_ID>"

constraints:
  required: ["<REQUIRED_STRUCTURE>"]
  prohibited: ["<PROHIBITED_STRUCTURE>"]

variation_points: ["<VARIATION_POINT>"]
verification: ["<CHECK_AND_EXPECTED_EVIDENCE>"]
```

### 5.3 Layered skeleton

```yaml
id: layered
components:
  - id: presentation
    tags: {kind: module, role: entry}
    responsibility: "<PRESENTATION_RESPONSIBILITY>"
  - id: application
    tags: {kind: module, role: application}
    responsibility: "<APPLICATION_RESPONSIBILITY>"
  - id: data_access
    tags: {kind: module, role: adapter, concern: storage}
    responsibility: "<DATA_ACCESS_RESPONSIBILITY>"

relationships:
  - {from: presentation, relation: depends-on, to: application}
  - {from: application, relation: depends-on, to: data_access}

contracts: "<LAYER_CONTRACTS>"
ownership: "<STATE_AND_RESOURCE_OWNERSHIP>"
composition: "<ASSEMBLY_LOCATION_AND_METHOD>"
constraints: "<LAYER_RULES_AND_ALLOWED_EXCEPTIONS>"
verification: "<CHECKS>"
```

The dependency direction shown is one layered variant. Logical layers and deployment tiers require separate descriptions.

### 5.4 Hexagonal skeleton

```yaml
id: hexagonal
components:
  - id: application
    tags: {kind: module, role: application, boundary: inside-core}
    responsibility: "<APPLICATION_RESPONSIBILITY>"
  - id: outbound_port
    tags: {kind: interface, boundary: boundary-contract}
    responsibility: "<REQUIRED_CAPABILITY>"
  - id: inbound_adapter
    tags: {kind: module, role: adapter, boundary: outside-core}
    responsibility: "<INPUT_ADAPTATION>"
  - id: outbound_adapter
    tags: {kind: module, role: adapter, boundary: outside-core}
    responsibility: "<EXTERNAL_CAPABILITY_IMPLEMENTATION>"

relationships:
  - {from: application, relation: depends-on, to: outbound_port}
  - {from: inbound_adapter, relation: calls, to: application}
  - {from: outbound_adapter, relation: implements, to: outbound_port}

contracts: "<PORT_CONTRACTS_AND_APPLICATION_ENTRY_CONTRACT>"
ownership: "<STATE_AND_RESOURCE_OWNERSHIP>"
composition: "<ADAPTER_SELECTION_AND_WIRING>"
constraints: "<BOUNDARY_RULES>"
verification: "<CHECKS>"
```

Source-code dependencies and runtime calls are distinct relations. Additional ports remain project-specific.

### 5.5 Pipeline skeleton

```yaml
id: pipeline
components:
  - id: source
    tags: {kind: module, role: entry}
    responsibility: "<INPUT_SUPPLY>"
  - id: stage_a
    tags: {kind: module, role: stage}
    responsibility: "<TRANSFORMATION_A>"
  - id: stage_b
    tags: {kind: module, role: stage}
    responsibility: "<TRANSFORMATION_B>"
  - id: sink
    tags: {kind: module, role: output}
    responsibility: "<OUTPUT_CONSUMPTION>"

relationships:
  - {from: source, relation: flows-to, to: stage_a}
  - {from: stage_a, relation: flows-to, to: stage_b}
  - {from: stage_b, relation: flows-to, to: sink}

contracts: "<CONNECTED_INPUT_AND_OUTPUT_CONTRACTS>"
ownership: "<STATE_AND_RESOURCE_OWNERSHIP>"
composition: "<STAGE_ASSEMBLY>"
execution: "<ORDERING_BUFFERING_AND_EXECUTION_POLICY>"
constraints: "<STAGE_AND_FLOW_RULES>"
verification: "<CHECKS>"
```

Flow edges describe data movement, not imports. The number of stages and execution model remain unspecified.

### 5.6 Plugin skeleton

```yaml
id: plugin
components:
  - id: host
    tags: {kind: module, role: application}
    responsibility: "<HOST_RESPONSIBILITY>"
  - id: extension_contract
    tags: {kind: interface, extension: extension-point}
    responsibility: "<EXTENSION_CAPABILITY>"
  - id: implementation
    tags: {kind: module, extension: implementation}
    responsibility: "<PLUGIN_RESPONSIBILITY>"

relationships:
  - {from: host, relation: depends-on, to: extension_contract}
  - {from: implementation, relation: implements, to: extension_contract}

contracts: "<EXTENSION_CONTRACT>"
ownership: "<STATE_AND_RESOURCE_OWNERSHIP>"
composition: "<SELECTION_AND_REGISTRATION>"
lifecycle: "<INITIALIZATION_ACTIVATION_AND_CLEANUP>"
constraints: "<EXTENSION_RULES>"
verification: "<CHECKS>"
```

Discovery and static or dynamic loading remain project decisions.

### 5.7 Additional skeleton slots

- <ADDITIONAL_ARCHITECTURE_PATTERN>
- <PROGRAMMING_STYLE_SKELETON>
- <EXECUTION_MODEL_SKELETON>
- <TECHNIQUE_SKELETON>

Use the common entry structure to distinguish the classification and purpose of each added skeleton.

## 6. Structural and behavioural rule placeholders

| Rule group | Placeholder |
| --- | --- |
| Modules, responsibilities, and boundaries | <MODULE_AND_BOUNDARY_RULES> |
| Dependency direction and permitted references | <DEPENDENCY_RULES> |
| Interfaces and contracts | <CONTRACT_RULES> |
| State and resource ownership | <OWNERSHIP_RULES> |
| Lifecycle and cleanup | <LIFECYCLE_RULES> |
| Data and control flow | <FLOW_RULES> |
| Concurrency and cancellation | <CONCURRENCY_RULES> |
| Error translation, retry, and recovery | <FAILURE_RULES> |
| Extension and variation | <EXTENSION_RULES> |
| Composition and assembly | <COMPOSITION_RULES> |

Rule entry template:

```yaml
id: "<RULE_ID>"
applies_to: "<PATTERN_OR_COMPONENT_SCOPE>"
requirement: "<REQUIRED_OR_PROHIBITED_BEHAVIOUR>"
rationale: "<REASON>"
verification: "<CHECK_AND_EXPECTED_EVIDENCE>"
```

## 7. Example and prohibited-structure placeholders

Repeat this structure for each expanded pattern or rule.

| Slot | Placeholder |
| --- | --- |
| Component-to-file mapping | <LANGUAGE_APPROPRIATE_FILE_LAYOUT> |
| Minimal code skeleton | <TAGGED_CODE_SKELETON> |
| Permitted structure | <PERMITTED_EXAMPLE> |
| Prohibited structure | <PROHIBITED_EXAMPLE_AND_RULE_ID> |
| Permitted variation | <VARIATION_AND_TRADEOFF> |

No code implementation is supplied in this revision.

## 8. Verification placeholders

| Check family | Check | Evidence |
| --- | --- | --- |
| Identity and tags | <IDENTITY_AND_TAG_CHECK> | <EXPECTED_EVIDENCE> |
| References and dependencies | <REFERENCE_AND_DEPENDENCY_CHECK> | <EXPECTED_EVIDENCE> |
| Contract compatibility | <CONTRACT_CHECK> | <EXPECTED_EVIDENCE> |
| Ownership and lifecycle | <OWNERSHIP_AND_LIFECYCLE_CHECK> | <EXPECTED_EVIDENCE> |
| Behaviour and failures | <BEHAVIOUR_CHECK> | <EXPECTED_EVIDENCE> |
| Project scope | <REQUIREMENT_TO_COMPONENT_CHECK> | <EXPECTED_EVIDENCE> |

Tags are descriptive metadata. Verification needs separate checks and evidence; tags alone do not prove compliance.

## 9. References and provenance

The layout, tags, and skeleton notation are local proposed conventions. The sources below support established architecture concepts, not the local schema.

| Concept | Reference |
| --- | --- |
| Layers and tiers | [Microsoft Architecture Center](https://learn.microsoft.com/en-us/azure/architecture/guide/architecture-styles/n-tier) |
| Ports and adapters | [Alistair Cockburn: Hexagonal Architecture](https://alistair.cockburn.us/hexagonal-architecture) |
| Pipes and filters | [Microsoft Architecture Center](https://learn.microsoft.com/en-us/azure/architecture/patterns/pipes-and-filters) |
| Plugin contract and lifecycle | <SELECTED_PLUGIN_MODEL_REFERENCE> |
| Classification catalogue | User-supplied programming terminology; working classification |
| Additional sources | <SOURCE_TITLE_URL_AND_APPLICABLE_SECTIONS> |
