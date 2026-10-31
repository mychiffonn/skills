# Chart Type Catalog

Use this reference to pick a chart type by analytical purpose, then check the Tufte stance before committing.

Sources:
- Chart names and purpose categories: visualizing.org (https://www.visualizing.org/#chart-types), which documents 180+ types. Category labels below mirror the site's.
- Fit rules for the core types: CASRAI, "Designing Effective Scientific Figures".
- The `Stance` column is this skill's judgment (Tufte: data-ink, graphical integrity, comparison), not the site's.

Stance legend:
- **Prefer**: carries data densely with little ink; default choice for its purpose.
- **OK**: fine when the stated condition holds.
- **Caution**: easy to misread, ink-heavy, or decoration-prone. Use only if no simpler chart answers the question, and justify it.

Names of chart types are searchable at `https://www.visualizing.org/<kebab-case-name>` (e.g., `/ridgeline-plot`) for definitions, examples, and code.

## 0. Start Here: Question to Chart

| The reader needs to... | Start with | Escalate to |
| --- | --- | --- |
| Compare a value across a few categories | Bar, dot plot | Lollipop, dumbbell, grouped bar |
| Compare many categories | Sorted dot plot, wrapped bar | Small multiples |
| See change over time (one to five series) | Line | Slope, step line |
| See change over time (many series) | Small multiples of lines, sparklines | Horizon, lasagna, DenseLines |
| See before/after for many items | Slope, dumbbell | Bump (ranks) |
| See a distribution of one variable | Histogram, ECDF, strip/beeswarm | Density, violin, raincloud, ridgeline |
| Compare distributions across groups | Dot-boxplot, strip + interval | Raincloud, ridgeline, violin |
| See a relationship between two variables | Scatter | Hexbin or contour (large n), connected scatter (time) |
| See relationships among many variables | Correlogram, pair plot | Parallel coordinates |
| See composition (parts of a whole) | Sorted bar or table of shares | Stacked bar (few parts), treemap (hierarchy) |
| See composition over time | Small multiples of lines, stacked area (few parts) | 100% stacked area |
| Follow flow between stages | Sankey, alluvial | Parallel sets |
| See a hierarchy | Indented tree, treemap | Sunburst, dendrogram |
| See a network | Adjacency matrix (dense), node-link (sparse) | Arc, chord, hive |
| Locate values in geography | Choropleth (rates), proportional symbol (counts) | Tile grid, cartogram, flow map |
| Show uncertainty or effect sizes | Dot-and-whisker, forest, fan chart | Half-eye, caterpillar |
| Show set overlap | UpSet (three or more sets) | Venn or Euler (two to three sets) |
| Pack exact values with trend | Table + sparklines | Small multiples |

## 1. Comparison (Magnitude Across Categories)

| Chart | Use when | Stance |
| --- | --- | --- |
| Bar chart | Compare one measure across discrete categories; baseline at zero | Prefer |
| Column chart | Vertical bars; short category labels | OK |
| Grouped bar chart | Compare sub-groups within categories; two categorical variables | OK (limit to about 3 to 4 groups) |
| Dot plot | Minimal-ink categorical comparison; non-zero baseline allowed since position, not length, encodes value | Prefer |
| Lollipop chart | Many categories; lighter than bars | OK |
| Dumbbell chart | Gap between two paired values per item | Prefer |
| Range chart | Min to max spread per category | OK |
| Bullet chart | Actual vs. target within performance bands | OK |
| Slope chart | Two time points, many items (also under Time Series) | Prefer |
| Small multiples | Same chart repeated over data slices | Prefer |
| Wrapped bar graph | Many categories; bars wrap onto several rows | OK |
| Population pyramid | Two groups across ordered bands (e.g., age) | OK |
| Quadrant chart | Scatter split into four labelled zones for classification | OK (only if thresholds are meaningful) |
| Pictogram chart | Countable units for lay audiences | Caution (icons are ink without data) |
| Radial bar chart | Compact variant of bars bent into a circle | Caution (outer bars look longer; hard to compare) |
| Nightingale rose chart | Cyclic or historical display, equal-angle wedges encoding area | Caution (area encodes a linear quantity) |

## 2. Distribution

| Chart | Use when | Stance |
| --- | --- | --- |
| Histogram | Shape of one variable; choose bin width deliberately and report it | Prefer |
| Spike histogram | Same as histogram with thin lines; lighter | OK |
| ECDF plot | Read percentiles directly; compare groups without binning | Prefer |
| Density plot | Smooth shape of a distribution | OK (bandwidth is a choice; state it) |
| Box plot | Compact spread and outlier summary across many groups | OK (hides multimodality) |
| Dot-boxplot | Box plot with raw points overlaid | Prefer |
| Strip plot | Raw points along one axis; small n | Prefer |
| Jitter plot | Strip plot with noise to reveal density | OK |
| Beeswarm plot | Every point visible and non-overlapping | Prefer |
| Violin plot | Full distribution shape per group | OK (smoothing can invent tails) |
| Half-eye plot | Half density plus point-interval summary | Prefer |
| Raincloud plot | Density, box summary, and raw data together | Prefer |
| Ridgeline plot | Compare many distributions stacked along a shared axis | OK |
| Stem-and-leaf plot | Small data sets; keeps exact values | OK |
| Q-Q plot | Check whether data follow a theoretical distribution (tails) | Prefer (diagnostic) |
| P-P plot | Compare cumulative probabilities; center-sensitive | OK (diagnostic) |
| Radial histogram | Cyclical data (hour of day, month) | Caution (use only when cyclic wrap-around matters) |

## 3. Correlation / Relationship

| Chart | Use when | Stance |
| --- | --- | --- |
| Scatter plot | Two continuous variables on the same observations | Prefer (alpha/size for overplotting) |
| Bubble chart | Third variable as size | Caution (area is hard to read; label values or use color/facets) |
| Connected scatter plot | Two variables co-evolving over time | OK (label start, end, and key years) |
| Hexbin plot | Large n scatter | Prefer |
| Contour plot | Bivariate density regions | OK |
| Correlogram | Matrix of pairwise correlations | OK (diverging palette symmetric around zero; order variables) |
| Pair plot | All pairwise scatters with marginals | OK |
| Solar correlation map | One variable's correlations with many others in a radial layout | Caution (a sorted bar is clearer) |
| 1D heatmap | One row of color-coded values | Caution (color is the weakest channel; prefer bars) |

## 4. Part-to-Whole (Composition)

Composition is hard to read precisely. Prefer sorted bars or a table of shares; use area/angle encodings only for rough proportion.

| Chart | Use when | Stance |
| --- | --- | --- |
| Stacked bar chart | Totals and composition together; few parts | OK (only the baseline segment is comparable) |
| 100% stacked bar chart | Compare mix, not totals | OK |
| Diverging stacked bar chart | Sentiment or Likert, split around a neutral center | Prefer for Likert |
| Marimekko chart | Two-dimensional composition with variable widths | Caution |
| Treemap | Hierarchical shares, many leaves | OK |
| Icicle chart | Hierarchical partition, rectangular | OK |
| Sunburst chart | Hierarchical shares, radial | Caution |
| Circle packing | Nested circles for hierarchy | Caution |
| Voronoi treemap / Bubble treemap | Decorative hierarchy layouts | Caution |
| Waffle chart | Single proportion with countable units (e.g., 23 of 100) | OK |
| Icon array | Risk communication to lay audiences | OK |
| Parliament chart | Seat shares | OK |
| Funnel chart | Staged drop-off | OK (a labelled bar list is usually clearer) |
| Pie chart | Few parts, one dominant share, rough read | Caution (angle and area are hard to compare; use sorted bars) |
| Donut chart | Same as pie with a headline number | Caution |
| Semi-circle donut / Gauge chart | One value vs. scale | Caution (a bullet chart or a number carries the same data in less ink) |

## 5. Time Series

| Chart | Use when | Stance |
| --- | --- | --- |
| Line chart | Trend over continuous or ordered variable; about five lines or fewer | Prefer |
| Sparkline | Word-sized trend inline in tables or text, with latest value | Prefer |
| Slope chart | Compare two time points across many items | Prefer |
| Step line chart | Values that change abruptly and hold | OK |
| Bump chart | Rank changes over time | OK |
| Area chart | Volume under a single line | OK (single series only) |
| Stacked area chart | Parts of a total over time | Caution (upper layers lack a common baseline) |
| Streamgraph | Many layers, aesthetic emphasis | Caution |
| Spline chart | Smooth interpolation | Caution (interpolation implies values that were not measured) |
| Horizon chart | Many compact series in little vertical space | OK (requires reader training) |
| Lasagna plot | Many longitudinal series as stacked heatmap rows | OK |
| DenseLines | Hundreds of overlapping series as density | OK |
| Calendar heatmap | Daily values with weekday and seasonal pattern | OK |
| Gantt chart | Project schedules | OK |
| Barcode chart | Events along a time axis | OK |
| Fan chart | Forecast uncertainty bands widening over time | Prefer |
| Cumulative flow diagram | Work items across workflow stages | OK |
| Lexis diagram | Age by calendar-time events | OK (specialist) |

## 6. Flow and Process

| Chart | Use when | Stance |
| --- | --- | --- |
| Sankey diagram | Flow quantities between stages; band width proportional to quantity | OK (limit nodes) |
| Alluvial diagram | Group membership shifts across time or dimensions | OK |
| Parallel sets | Multi-dimensional categorical ribbons | OK |
| Waterfall chart | Sequential gains and losses to a total | Prefer |
| Double waterfall chart | Two decompositions side by side | OK |

## 7. Hierarchy

| Chart | Use when | Stance |
| --- | --- | --- |
| Indented tree | Outline-style, many levels, with labels | Prefer (high label density) |
| Tree diagram | Classic root-to-leaf | OK |
| Dendrogram | Clustering with distance-encoded branch heights | Prefer (for clustering) |
| Phylogenetic tree | Evolutionary relationships | OK (domain standard) |
| Organizational chart | Reporting lines | OK |
| Flame chart / Flame map | Profiler call stacks | OK (domain standard) |
| Radial tree | Circular hierarchy | Caution |
| Hyperbolic tree / Cone tree | Interactive focus-plus-context navigation | Caution (interactive novelty; not for print) |

## 8. Network

| Chart | Use when | Stance |
| --- | --- | --- |
| Adjacency matrix / Matrix diagram | Dense networks; no edge crossings | Prefer for dense graphs |
| Node-link diagram | Small, sparse networks | OK |
| Ego network diagram | One node and its neighbors | OK |
| Force-directed graph | Cluster discovery in small to medium graphs | Caution (layout is arbitrary; position carries no meaning) |
| Arc diagram | Ordered nodes on a line | OK |
| Chord diagram | Flow magnitudes between groups | Caution (hard to read quantities) |
| Non-ribbon chord diagram | Dense many-to-many | Caution |
| Hierarchical edge bundling / Force-directed edge bundling | Reduce clutter in dense links | OK |
| Bipartite graph | Two node sets | OK |
| Hive plot | Attribute-positioned nodes for comparable layouts | OK |
| Circular layout graph | Nodes on a circle | Caution |
| BioFabric | Dense large networks without overlap | OK (specialist) |
| Circos plot | Genomic and other circular relations | OK (domain standard) |
| Hypergraph visualization | Edges linking more than two nodes | OK (specialist) |

## 9. Geospatial

Check first whether a sorted bar chart or table answers the question; maps mostly encode land area, not the data.

| Chart | Use when | Stance |
| --- | --- | --- |
| Choropleth map | Rates or normalized values by region | OK (never raw counts; beware area bias) |
| Dasymetric map | Choropleth refined with ancillary density data | OK |
| Value-by-alpha map | Color for value, transparency for confidence | OK |
| Tile grid map | Equal-sized tiles that remove area bias | Prefer |
| Bivariate tile grid map | Two variables per tile | Caution (legend burden) |
| Cartogram / Dorling / Demers / Non-contiguous | Distort or replace regions to encode a variable | OK (Dorling, Demers); Caution (distorting cartograms) |
| Proportional symbol map / Bubble map | Counts at locations | OK |
| Spike map | Magnitude as spike height | OK |
| Dot density map | Distribution of units | OK |
| Flow map / Connection map | Movement or links between places | OK |
| Hexbin map | Aggregate point data by hexagon | Prefer |
| Isarithmic map / Geographic heat map | Continuous surfaces | OK |
| Voronoi map | Nearest-point partition | OK |
| Necklace map | Glyphs along a region outline | Caution |
| Prism map / Space-time cube | 3D extrusions | Caution (occlusion and perspective distortion) |

## 10. Statistical

| Chart | Use when | Stance |
| --- | --- | --- |
| Dot-and-whisker plot | Regression coefficients with CI | Prefer |
| Forest plot | Effect sizes with CI across studies | Prefer |
| Caterpillar plot | Ranked random effects with CI | Prefer |
| Funnel plot (statistical) | Publication bias in meta-analysis | OK |
| Galbraith plot / L'Abbe plot | Heterogeneity; treatment vs. control rates | OK (specialist) |
| ROC curve | Classifier TPR vs FPR across thresholds; report AUC | OK |
| Precision-recall curve | Imbalanced classification | Prefer for imbalanced classes |
| Calibration plot | Predicted probability vs. observed rate | Prefer |
| Bland-Altman plot | Agreement between two measurement methods | Prefer |
| Control chart / CUSUM / EWMA | Process stability and small shifts | OK |
| Pareto chart | Rank causes with cumulative line | OK |
| Response surface plot | Response over two factors | Caution (3D surface; prefer contour) |

## 11. Financial

| Chart | Use when | Stance |
| --- | --- | --- |
| Candlestick / OHLC | Open-high-low-close over time | OK (OHLC has less ink) |
| Heikin-Ashi / Kagi / Renko / Point-and-figure / Three line break / Range bar | Price-action filters that ignore time or smooth noise | Caution (derived transformations; state the rule) |
| EquiVolume | Price range height by volume width | OK |

## 12. Scientific (Domain Specific)

| Chart | Use when | Stance |
| --- | --- | --- |
| Volcano plot | Fold change vs. significance (differential expression) | OK |
| MA plot | Log ratio vs. mean intensity (normalization QC) | OK |
| Manhattan plot | Genome-wide significance across chromosomes | OK |
| Kaplan-Meier curve | Survival over time; show numbers at risk and CI | Prefer |
| Sequence logo | Information content per sequence position | OK |
| Ternary plot | Three components summing to a constant | OK |
| Piper diagram / Durov diagram | Water chemistry composition | OK (domain standard) |
| Recurrence plot / Phase portrait / Poincare plot | Dynamical systems and time-series structure | OK (specialist) |

## 13. Sets

| Chart | Use when | Stance |
| --- | --- | --- |
| UpSet plot | Intersections among three or more sets | Prefer |
| Venn diagram | Two to three sets, all intersections | OK |
| Euler diagram | Only the existing relationships | OK |
| Kelp diagram | Set membership over space or time | OK (specialist) |

## 14. Multi-dimensional

| Chart | Use when | Stance |
| --- | --- | --- |
| Small multiples | Prefer over any single complex encoding | Prefer |
| Parallel coordinates plot | Many numeric variables per record; limit records or use brushing | OK |
| Mosaic plot | Categorical contingency tables | OK |
| Heatmap (matrix) | Value across two ordered or categorical axes; perceptually uniform colormap | OK |
| Radar chart / Star plot | Profiles on several axes | Caution (area depends on axis order; use dot plots or small multiples) |
| RadViz / Star coordinates | Exploratory projection | Caution (exploratory only) |
| Chernoff faces | Face-feature encoding | Caution (avoid for analysis; features are not perceptually comparable) |

## Selection Notes

- Sort categories by value unless they have a natural order.
- Prefer direct labels over legends. For lines, label at the line end.
- When the catalog says "Caution", try small multiples or a sorted dot plot first.
- When a single chart needs more than one chart type's job, split it into panels (see `figure-design-practice.md` section 2).
- Show uncertainty and sample size wherever the chart encodes an estimate.
