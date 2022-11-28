title:: Reconciling Level of Detail Expressions With the View Level of Detail (highlights)
author:: [[help.tableau.com]]
full-title:: "Reconciling Level of Detail Expressions With the View Level of Detail"
category:: #articles
url:: https://help.tableau.com/current/pro/desktop/en-us/calculations_calculatedfields_lod_replication.htm

- Highlights first synced by [[Readwise]] [[Nov 28th, 2022]]
	- An expression has a coarser level of detail than the view when it references a subset of the dimensions in the view.
	- An expression has a finer level of detail than the view when it references a superset of the dimensions in the view. When you use such an expression in the view, Tableau will aggregate results up to the view level.
	- INCLUDE level of detail expressions will have either the same level of detail as the view or a finer level of detail than the view. Therefore, values will never be replicated.
	- FIXED level of detail expressions can have a finer level of detail than the view, a coarser level of detail, or the same level of detail. The need to aggregate the results of a FIXED level of detail depends on what dimensions are in the view.
	- EXCLUDE level of detail expressions always cause replicated values to appear in the view. When calculations including EXCLUDE level of detail expressions are placed on a shelf, Tableau defaults to the ATTR aggregation (as opposed to SUM or AVG) to indicate that the expression is not actually being aggregated and that changing the aggregation will have no effect on the view.