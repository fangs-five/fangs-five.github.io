# About the Framework

This section explains what the framework is and how to use it. It also
provides recommendations on how to extend or modify the core principles
outlined in this playbook.

## Dimensions

The framework discusses two major dimensions that a consultant would
need to consider throughout the lifecycle of the contract. These
dimensions are “security” and “infrastructure.” By defining a clear and
manageable scope for both of these areas, the consultant can begin to
provide value to the organization while avoiding common pitfalls.

Interestingly, the research shows that, if a consulting party can
enumerate the inventory for both dimensions, then pitfalls in one will
often lead to a corresponding issue or weakness in the other. For
example, suppose a network

### Security

Although this dimension encapsulates everything related to security
(including physical or perimeter security), this framework places an
emphasis on I.T. Security specifically. For small and mid-sized
businesses, the emphasis is on Network Security in particular. The
research suggests that many of these organizations are more likely to
use effective physical security (perimeter and internal cameras),
third-party applications or services to build web applications (such as
Wix), and so forth.

In general, NetSec is still a “blind spot” for many organizations; the
consultant will find it manageable to focus on this dimension first,
then branch out to others on a needs basis. For example, if the
organization uses a legacy point-of-sale system written in C++, the
consultant should identify this as an area of risk. On the other hand,
if they host their web applications in something like GoDaddy, and use
the platform’s site-builder, this is out-of-scope; otherwise, the
consultant would need to write a contract to test the third-party
platform, and among other concerns, this alone would imply liability.

This should provide a narrow-enough scope for the consultant to bring
value to the organization, while at the same time avoiding “scope
creep.” This scope also helps the consultant avoid liability by
preventing them from speaking to a security field with which they may
have little or no experience.

### Infrastructure

In this framework, “Infrastructure” refers to the components of the
on-premise worksite that facilitate the business needs through the I.T.
structures. The framework emphasizes the “Network” portion of this
because networking is a common blind-spot with small and mid-sized
businesses.

The infrastructure is considered with respect to its ability to add
performance; for example, if Wi-Fi is used, can everyone in the building
connect with usable speeds? In some cases, the placement of the
organization’s hotspots are the root cause; in other cases, ideal
performance and wireless-network ranges will never fully become realized
because of the physical properties of the building (for example, because
the walls are made of materials that naturally block radio frequencies).
For many organizations, a cable-management inventory is essential to
identifying the root causes of performance issues.

## Risk and Infrastructure Scores

One major goal of this framework is to generate a score for risk and
infrastructure. Each metric is valuable; however, the meaning will
differ with respect to the organization. A healthy organization will
yield a low risk score and a high infrastructure (performance) score.
Conversely, a high risk or low infrastructure score will provide a
consultant with the opportunity to discuss the weaknesses in the
organization. Although this second case is unfavorable for the client,
it does effectively become the opportunity for the consultant to provide
tangible recommendations, set a clear scope-of-work, and ultimately
provide value to the customer.

It should be noted that each score is more like a “starting point” for
the process of providing recommendations. Each is based on the results
of security and I.T. experts, along with well-established security and
networking research. With that in mind, a consultant should be careful
to explain the meaning of each result, and not to rely on it as a means
unto itself. In other words, if a client brings in *another,*
well-informed party to audit either score, it is the consultant’s
responsibility to speak to the context and concrete meanings behind each
score. Failure to do so will ultimately undermine the consultant’s
reputation and, likely, their business.

Each score is built on several questions for each dimension. These
questions are driven by algorithms (even very simple ones) as well as
budgetary considerations (for the client). Each of these have their own
rationales and caveats.

Finally, these “total” scores should have some kind of clear, simple
meaning. The framework’s creators encourage the use of simple states
like “ACCEPTABLE” and “NEEDS IMPROVEMENT.” This provides the client with
a simple meaning to digest each individual metric as well as the
aggregate metrics. Ultimately, the client is encouraged to use
nomenclature and terms that resonate with their audience, while still
holding true to the meaning of each dimension’s scores. Failure to
interpret the numbers in a way that is meaningful for client could cause
the client to lose faith in the consultant’s ability to faithfully
perform their work.

### Algorithms

For each dimension, there is a set of questions, each of which has a
corresponding algorithm. The goal of each algorithm is to determine the
score for that question alone. A collection of question scores becomes
the overall “risk” or “infrastructure” score for that dimension. The
framework’s creators provide their recommendations for how to rate the
risk or infrastructure of each question given a low-budget organization.

For example, a small business with a single router implies far less risk
than an enterprise that uses the same kind of network. Conversely, a
small business with ten routers may find itself using stale technology
that someone set up and no one maintains anymore. This second case
implies a lot more risk for a small business because unmaintained
devices can be tampered without anyone knowing.

With that in mind, the framework is intentionally flexible. It avoids
any concrete implementation of any algorithm because of the nature of
business and the ever-changing nature of I.T. Security and
Infrastructure. In general, the consultant is encouraged to tweak the
algorithms that generate scores if it is appropriate or necessary for
conveying a meaningful snapshot of the organization. The goal is not to
rely on fixed numbers, but to leverage meaning through the numbers that
are generated.

### Budgetary considerations

Budget is considered in this framework insofar as financial means can
drive a client’s ability to actually implement change in the
organization. The framework’s creators promote three “generic”
categories of budget: low, medium, and high. The low and high budget
ranges should be fairly easy to identify; we can infer that a local
coffee shop will almost certainly have a low budget, whereas an
enterprise software company might have a high budget. Defining the
“medium” budget ranges is not fixed; however, there is still a need ot
identify these organizations, as they are often just large enough to
find themselves the target of a security incident, but just small enough
not to be taken seriously when trying to proactively implement security
controls or infrastructure improvements.

The consultant is encouraged to use the budget as a means to tune their
recommendations and implementation plan. This is normal in most software
I.T. business models, regardless of the specialization or specifics of
the implementation. The framework’s creators recognize the importance of
“putting the client first” as the means to maintaining a healthy
professional relationship.

### Considerations for budgets and score-generations

In general, the consultant is encouraged to prioritize the
organization’s budget over any algorithm. Failure to do so could result
in an inability for the consultant’s vision to be realized. The creators
of the framework promote the idea that “perfection should never be the
enemy of greatness.” In other words, if the client cannot afford to
implement a consultant’s vision and plan, the contract will almost
certainly find itself at risk, because no one can afford to implement
it. In such a case, it makes sense to scale back the price of the
changes in order to find a compromise.

## Reporting

The goal of the reporting section is to present aggregate metrics and
the results of each dimension’s score. All data should be presented in a
way that is digestible at a high level; information here is conveyed at
a high level.

The framework’s creators provide the following recommendations for
starting points based on the two key dimensions:

- **Risk score**: Lower scores are better

- **Infrastructure score**: Higher scores are better

- For each score, the top *N* weaknesses

- Graphs showing the total scores after the implementation plan is
  completed

- Total budgetary needs to implement changes

The top weaknesses should map to a question from the dimension’s set of
questions.

## Appendices

The appendices will be any list or collection of information that is
necessary for the implementation plan, but is not necessary to generate
metrics. The consultant can and should track arbitrary information about
the client. This could include a list of routers, compatible and
up-to-date wiring, and so forth. While these are useful, they are not
essential to the framework per se. These can change depending on the
client and budget. In addition, the consultant is encouraged to make
appendices that are specialized to the client. (Beef this section up.)
