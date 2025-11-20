# Agentic AI Engineering Framework - Master Skill

## Purpose

This framework transforms agentic AI development from ad-hoc experimentation into **systematic engineering practice**. It provides a skills-first approach to building production-grade compound AI systems that are reliable, observable, and cost-effective from day one.

**Core Innovation:** Skills-as-Knowledge + 8-Stage Lifecycle + Production Patterns

**Key Benefits:**
- **Zero context overhead** - Skills load automatically based on stage
- **60-70% faster development** - From idea to production in 8-10 hours
- **85-92% quality retention** - Optimal token budgets per stage
- **>80% test coverage** - Enforced by default
- **<5% production error rate** - Built-in resilience patterns

---

## When to Use This Framework

### Triggering Conditions

Load this framework when users mention:

**Explicit Triggers:**
- "Build an agent/AI agent/agentic system"
- "Create a compound AI system"
- "Multi-agent system/orchestration"
- "Production-ready AI"
- "Following the framework"

**Implicit Triggers:**
- Questions about agent architecture
- Requests to implement LLM-powered workflows
- Multi-step AI task automation
- Agent reliability or observability concerns
- Scaling AI agents to production

**Stage-Specific Triggers:**
- "Assess feasibility" → Load `assess-stage`
- "Gather requirements" / "Define user stories" → Load `discover-stage`
- "Design architecture" / "Choose framework" → Load `design-stage`
- "Implement agent" / "Write code" → Load `implement-stage`
- "Write tests" / "Test coverage" → Load `validate-stage`
- "Production readiness" / "Observability" → Load `harden-stage`
- "Deploy" / "Canary rollout" → Load `deploy-stage`
- "Monitor" / "Dashboards" → Load `monitor-stage`

---

## Core Concepts

### 1. Skills-First Development

**What are Skills?**
Skills are self-contained knowledge packages that extend Claude's capabilities with specialized expertise, patterns, and workflows. Each skill contains:
- `SKILL.md` - Core methodology
- `examples/` - Working code samples
- `templates/` - Reusable artifacts
- `scripts/` - Automation tools
- `references/` - Documentation

**Why Skills?**
- **Automatic loading** - Claude reads relevant skills before working
- **Consistency** - Same patterns every time, zero drift
- **Composability** - Combine multiple skills for complex tasks
- **Versioning** - Skills evolve with git
- **Team sharing** - Distribute expertise as skill packages

### 2. Three-Tier Skill Precedence

```
Priority 1: PROJECT-LOCAL (.claude/skills/)
  ↓ overrides
Priority 2: USER-GLOBAL (/mnt/skills/user/)
  ↓ overrides  
Priority 3: BUILT-IN (/mnt/skills/public/)
```

**What This Means:**
- Projects can customize/override framework defaults
- Same framework works across all projects
- Zero conflict between global and project needs
- Team shares customizations via git

### 3. The 8-Stage Development Lifecycle

The framework implements a rigorous lifecycle that transforms ideas into production systems:

```
ASSESS → DISCOVER → DESIGN → IMPLEMENT → VALIDATE → HARDEN → DEPLOY → MONITOR
  |         |         |          |            |          |         |        |
Go/No-Go  PRP Doc  ADR Docs  Agent Code  Test Suite  Prod Ready Gradual  Dashboards
                                                                  Rollout
```

Each stage has:
- **Dedicated skill** with methodology and templates
- **Clear deliverables** with acceptance criteria
- **Token budget** (optimized for 85-92% quality)
- **Human validation gate** before proceeding
- **Duration estimate** for planning

### 4. Production Patterns Library

Four cross-cutting pattern skills provide battle-tested implementations:

- **observability-patterns** - Langfuse tracing, metrics, logging
- **resilience-patterns** - Retry, circuit breaker, fallback chains
- **security-patterns** - Validation, sanitization, rate limiting
- **optimization-patterns** - Caching, compression, model routing

These are loaded automatically during the HARDEN stage.

---

## Framework Workflow

### Step 1: Understand the Request

When a user asks to build an agent or mentions the framework:

1. **Identify the stage** - Where are they in the lifecycle?
   - New project? → Start at ASSESS
   - Have requirements? → Start at DESIGN
   - Have design? → Start at IMPLEMENT
   - Have code? → Move to VALIDATE
   - Ready for production? → Move to HARDEN

2. **Assess complexity** - What type of system?
   - Simple agent (1-3 steps)? → ADK + lighter testing
   - Complex agent (4+ steps)? → LangGraph + comprehensive testing
   - Multi-agent system? → Orchestrator pattern

3. **Check for project skills** - Any project-specific customizations?
   - Check `.claude/skills/` for overrides or domain skills
   - Project skills take precedence over framework defaults

### Step 2: Load Appropriate Skills

**For New Projects (Starting Fresh):**
```
Load: assess-stage skill
→ Guide through feasibility assessment
→ Produce Go/No-Go decision document
→ If GO → Proceed to discover-stage
```

**For Requirements Phase:**
```
Load: discover-stage skill
→ Guide through PRP (Product Requirements Prompt) creation
→ Define user stories, personas, success metrics
→ Document edge cases and non-functional requirements
→ Produce comprehensive PRP document
→ Proceed to design-stage
```

**For Architecture Phase:**
```
Load: design-stage skill
→ Guide through ADR (Architecture Decision Record) creation
→ Help choose framework (ADK vs LangGraph vs Hybrid)
→ Design agent decomposition and responsibilities
→ Define state management and tool integrations
→ Produce ADR documents and architecture diagrams
→ Proceed to implement-stage
```

**For Implementation Phase:**
```
Load: implement-stage skill
→ Generate production-quality agent code
→ Follow code templates and patterns from skill
→ Implement proper error handling and logging
→ Use Pydantic for all schemas
→ Produce complete agent implementation
→ Proceed to validate-stage
```

**For Testing Phase:**
```
Load: validate-stage skill
→ Generate comprehensive test suite
→ Follow testing pyramid (50% unit, 30% integration, 15% behavioral, 5% adversarial)
→ Enforce >80% coverage
→ Include performance benchmarks
→ Produce complete test suite with coverage report
→ Proceed to harden-stage
```

**For Production Readiness:**
```
Load: harden-stage skill
Also load all 4 pattern skills automatically:
  - observability-patterns
  - resilience-patterns
  - security-patterns
  - optimization-patterns
→ Apply all production patterns to code
→ Add tracing, metrics, logging
→ Implement retry, circuit breaker, fallbacks
→ Add validation, sanitization, rate limiting
→ Implement caching, compression, routing
→ Create runbooks for failure scenarios
→ Produce production-ready system
→ Proceed to deploy-stage
```

**For Deployment Phase:**
```
Load: deploy-stage skill
→ Create deployment configurations
→ Design canary rollout plan (5% → 25% → 100%)
→ Write smoke tests
→ Document rollback procedures
→ Produce deployment plan and configs
→ Proceed to monitor-stage
```

**For Monitoring Phase:**
```
Load: monitor-stage skill
→ Design dashboards (Grafana/Datadog)
→ Define alerts and thresholds
→ Set up cost analytics
→ Create incident runbooks
→ Produce monitoring setup
→ Continuous improvement cycle
```

### Step 3: Execute Stage Methodology

Once appropriate skills are loaded:

1. **Read the skill thoroughly** - Understand methodology, templates, examples
2. **Follow the structure** - Use templates and patterns provided
3. **Stay within token budget** - Each stage has optimal token allocation
4. **Validate with user** - Confirm deliverables meet expectations before proceeding
5. **Document everything** - All decisions, code, tests go in proper locations

### Step 4: Validate and Progress

Before moving to next stage:

1. **Check gate criteria** - Each skill defines acceptance criteria
2. **Review deliverables** - Confirm all outputs are complete
3. **Get user approval** - Explicit confirmation to proceed
4. **Reference previous work** - Each stage builds on prior deliverables

---

## Skill Loading Decision Logic

### Primary Decision: Which Stage?

```python
def determine_stage(user_request: str, project_state: dict) -> str:
    """Determine which framework stage to load."""
    
    # New project assessment
    if any(kw in user_request.lower() for kw in ['feasibility', 'should we build', 'assess']):
        return 'assess-stage'
    
    # Requirements gathering
    if any(kw in user_request.lower() for kw in ['requirements', 'user stories', 'prp']):
        return 'discover-stage'
    
    # Architecture decisions
    if any(kw in user_request.lower() for kw in ['architecture', 'design', 'adr', 'framework choice']):
        return 'design-stage'
    
    # Code implementation
    if any(kw in user_request.lower() for kw in ['implement', 'code', 'build agent', 'write']):
        return 'implement-stage'
    
    # Testing
    if any(kw in user_request.lower() for kw in ['test', 'coverage', 'validate']):
        return 'validate-stage'
    
    # Production readiness
    if any(kw in user_request.lower() for kw in ['production', 'observability', 'resilience', 'harden']):
        return 'harden-stage'
    
    # Deployment
    if any(kw in user_request.lower() for kw in ['deploy', 'rollout', 'canary']):
        return 'deploy-stage'
    
    # Monitoring
    if any(kw in user_request.lower() for kw in ['monitor', 'dashboard', 'alerts']):
        return 'monitor-stage'
    
    # Default: Assess stage for new projects
    return 'assess-stage'
```

### Secondary Decision: Load Pattern Skills?

Pattern skills are loaded automatically during HARDEN stage, but can be loaded earlier if user explicitly mentions:

- "Add observability" → Load `observability-patterns`
- "Add retry logic" → Load `resilience-patterns`
- "Security hardening" → Load `security-patterns`
- "Optimize costs" → Load `optimization-patterns`

### Tertiary Decision: Check Project Overrides

Before loading framework skill, check if project has override:

1. Check `.claude/skills/<stage-name>/SKILL.md`
2. If exists → Load project override (takes precedence)
3. If not → Load framework skill from `/mnt/skills/user/agentic-ai-framework/<stage-name>/`

---

## Technology Stack Guidance

### Framework Selection Decision Matrix

| Factor | Use ADK | Use LangGraph | Use Hybrid |
|--------|---------|---------------|------------|
| **Steps** | 1-3 linear | 4+ with conditionals | Mixed |
| **Routing** | Sequential | Dynamic routing | Some branching |
| **State** | Stateless/simple | Complex state mgmt | Session state |
| **Tools** | 0-2 tools | 3+ tools | Mixed |
| **Latency** | <1s critical | <3s acceptable | Varies |
| **Cost** | Minimize tokens | Quality > cost | Balance |

### Model Selection Guidance

| Model | Context | Cost/1M In | Cost/1M Out | Best For |
|-------|---------|------------|-------------|----------|
| **gemini-2.5-flash** | 1M | $0.30 | $2.50 | Speed & volume |
| **gemini-2.5-pro** | 1M | $1.25 | $10.00 | Long context |
| **claude-sonnet-4-5** | 200K | $3.00 | $15.00 | Coding |
| **gpt-5.1** | 400K | $1.25 | $10.00 | Reasoning |

---

## Quick Reference

### Installation (One-Time Per Developer)

```bash
# Clone framework repository
git clone https://github.com/lengonardo/agentic-ai-framework.git

# Install globally
cp -r agentic-ai-framework/skills/agentic-ai-framework /mnt/skills/user/

# Verify
ls /mnt/skills/user/agentic-ai-framework/
```

### Project Setup

```bash
# Create project structure
mkdir -p .claude/skills
mkdir -p src/agents src/workflows
mkdir -p tests
mkdir -p docs/{assessments,prps,adrs}
mkdir -p deployment

# Add .gitignore
cat > .gitignore << 'EOF'
.claude/skills/agentic-ai-framework/
.claude/skills/*.skill
EOF
```

### Essential Commands

```bash
# Create project skill
cd .claude/skills
/mnt/skills/examples/skill-creator/scripts/init_skill.py my-skill --path .

# Override framework stage
cp -r /mnt/skills/user/agentic-ai-framework/stage-name .claude/skills/

# Update framework
cd agentic-ai-framework && git pull
cp -r skills/agentic-ai-framework /mnt/skills/user/
```

### Common User Requests

**"Build a shopping assistant agent"**
→ Load assess-stage → Walk through 8 stages

**"I have requirements, help me design"**
→ Load design-stage → Create ADRs and architecture

**"Make this production-ready"**
→ Load harden-stage + 4 pattern skills → Apply all patterns

**"Add observability"**
→ Load observability-patterns → Implement tracing & metrics

---

## Usage Examples

### Example 1: New Project (Full Lifecycle)

```
User: "I want to build an agent that helps users shop for products"

Claude: [Loads agentic-ai-framework master skill]
        [Determines: New project → Start at ASSESS stage]
        [Loads assess-stage skill]
        
I'll help you assess the feasibility of a shopping assistant agent 
using the framework's ASSESS stage.

[Follows assess-stage methodology]
[Uses templates from assess-stage/templates/]
[Produces assessment document]

Assessment complete! This is a strong GO decision.

Next, I'll guide you through the DISCOVER stage to define detailed 
requirements. Should we proceed?

User: "Yes, let's continue"

Claude: [Loads discover-stage skill]
        [Follows PRP template from discover-stage/templates/]
        [Creates user stories, personas, success metrics]
        
[And so on through all 8 stages...]
```

### Example 2: Jump to Implementation

```
User: "I have the design ADRs. Implement the product search agent."

Claude: [Loads agentic-ai-framework master skill]
        [Determines: Has design → IMPLEMENT stage]
        [Loads implement-stage skill]
        [Checks for project skills in .claude/skills/]
        [Found: ecommerce-patterns skill]
        [Loads ecommerce-patterns as well]
        
I'll implement the product search agent following the framework's 
IMPLEMENT stage methodology and your ecommerce domain patterns.

[Follows code templates from implement-stage/]
[Uses ecommerce schemas from ecommerce-patterns/]
[Generates production-quality code]
[Creates: src/agents/product_search/agent.py]
```

### Example 3: Production Hardening

```
User: "Make this agent production-ready"

Claude: [Loads agentic-ai-framework master skill]
        [Determines: Production readiness → HARDEN stage]
        [Loads harden-stage skill]
        [Automatically loads all 4 pattern skills:]
        [- observability-patterns]
        [- resilience-patterns]
        [- security-patterns]
        [- optimization-patterns]
        
I'll harden your agent for production using the framework's 
production patterns.

[Applies Langfuse tracing from observability-patterns]
[Adds retry + circuit breaker from resilience-patterns]
[Implements validation from security-patterns]
[Adds semantic caching from optimization-patterns]
[Creates runbooks from harden-stage/templates/]

Production hardening complete! Your agent now has:
✓ Full observability with Langfuse
✓ Resilience patterns (retry, circuit breaker, fallbacks)
✓ Security hardening (validation, sanitization, rate limiting)
✓ Cost optimization (caching, compression, routing)

Ready to proceed to DEPLOY stage?
```

### Example 4: Project Override

```
User: "Implement payment processing agent"

Claude: [Loads agentic-ai-framework master skill]
        [Determines: IMPLEMENT stage]
        [Checks: .claude/skills/implement-stage/ exists]
        [Loads project override instead of framework version]
        [Project override includes fintech compliance patterns]
        
I'll implement the payment processing agent using your project's 
custom implementation patterns (which include fintech compliance 
requirements).

[Follows customized templates from project override]
[Includes mandatory audit logging per project patterns]
[Implements PCI-DSS validation per project requirements]
```

---

## Core Principles (Always Remember)

### 1. Token Budget Discipline
- Each stage has optimal token budget (8K-50K)
- Stay within budget for 85-92% quality retention
- Skills are pre-optimized for token efficiency

### 2. Progressive Enhancement
- Each stage adds measurable quality
- Human validation gates prevent compounding errors
- Never skip stages (but can iterate within stages)

### 3. Production from Start
- Observability, resilience, security built-in
- Not afterthoughts, but core patterns
- >80% test coverage mandatory

### 4. Compound AI First
- Design for multi-agent orchestration
- Decompose complex tasks into specialized agents
- Use orchestrator pattern for coordination

### 5. Test-Driven Development
- Tests define expected behavior
- Coverage enforced automatically
- Behavioral tests for UX, adversarial tests for security

### 6. Fail Fast, Fail Safe
- Circuit breakers prevent cascading failures
- Fallback chains ensure graceful degradation
- Timeouts prevent resource exhaustion

### 7. Measure Everything
- Latency, cost, quality, satisfaction
- Real-time dashboards + historical analysis
- Continuous improvement based on data

### 8. Context is Infrastructure
- Skills encapsulate knowledge
- Automatic loading based on need
- Versioned and tested like code

---

## Framework File Structure Reference

```
Global Framework: /mnt/skills/user/agentic-ai-framework/
├── SKILL.md                          # This file (master skill)
├── assess-stage/
│   ├── SKILL.md
│   ├── examples/
│   ├── templates/
│   └── scripts/
├── discover-stage/
├── design-stage/
├── implement-stage/
├── validate-stage/
├── harden-stage/
├── deploy-stage/
├── monitor-stage/
├── observability-patterns/
├── resilience-patterns/
├── security-patterns/
└── optimization-patterns/

Project Skills: .claude/skills/
├── domain-specific-patterns/         # Project knowledge
├── project-overrides/                # Framework customizations
└── custom-agents/                    # Project-specific agents
```

---

## Critical Reminders

### For Claude
1. **Always check project skills first** - They override framework
2. **Load appropriate stage skill** - Don't just reference, actually load
3. **Follow skill methodology** - Use templates and examples provided
4. **Stay within token budgets** - Each stage is optimized
5. **Validate before proceeding** - Get explicit user approval
6. **Load pattern skills in HARDEN** - All 4 automatically

### For Users
1. **Install framework globally once** - Per developer, not per project
2. **Commit project skills to git** - Share team knowledge
3. **Don't commit framework to projects** - Keep global
4. **Use overrides for customization** - Not global modifications
5. **Follow the 8-stage lifecycle** - Don't skip stages
6. **Trust the process** - Framework is research-backed

---

## Support & Resources

- **Repository:** https://github.com/lengonardo/agentic-ai-framework
- **Documentation:** See FRAMEWORK_SUMMARY.md
- **Issues:** GitHub Issues
- **Team Discussions:** GitHub Discussions

---

## Success Metrics

Track these to measure framework effectiveness:

**Development Velocity:**
- Time to first agent: <1 hour ✓
- Time to production: 8-10 hours ✓
- Bug fix time: <30 minutes ✓

**Quality Metrics:**
- Test coverage: >80% ✓
- Production error rate: <5% ✓
- Code consistency: 99% ✓

**Cost Metrics:**
- Development cost: 60-70% reduction ✓
- Token efficiency: 50-60% improvement ✓
- Per-conversation cost: <$0.10 ✓

**User Experience:**
- Task completion: >90% ✓
- User satisfaction: >4.5/5 ✓
- Time to resolution: <3 minutes ✓

---

**Remember:** This framework is not just about speed—it's about building **reliable, observable, cost-effective** agentic AI systems that work in production from day one.

**Skills-first. Production-ready. Battle-tested.**

---

*Framework Version: 1.0*
*Last Updated: November 2025*  
*Built with ❤️ for production-grade agentic AI engineering*
