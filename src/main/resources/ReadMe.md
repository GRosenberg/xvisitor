### XVisitor

A tool for generating customized Antlr4 parse-trees visitors using grammar-style definitions.

#### Summary

XVisitor enables multiple XPath-styled probes to be evaluated in parallel against the parse-tree.  When any XPath is matched, actions defined in the grammar specific to that XPath are invoked.  Actions for either or both 'onEntry' and 'onExit' states can be defined.  Consistent with standard Antlr grammars, actions are implemented using target language code.  Token and rule '$'-styled references give actions direct access to the currently matched context and token attributes.

#### Benefits

* Natural order of results:
	* the XPath match actions are invoked in natural (parse-tree) order by the visitor
* Clarity:
	* 'onEntry' and 'onExit' actions can be separately defined for each XPath
	* the grammar definition is simple and conceptually similar to standard Antlr grammars
	* symbolic context references are available for use in actions
	* the actual path traversed to reach a matched XPath is recorded and available in actions
* Flexibilty:
	* concurrent evaluation fully supports overlapping XPaths
	* supports XPath wildcards: '//', '*', and '?'
* Efficiency:
	* complex path state analysis can be reduced to a set of simply-defined path matches
	* parse-tree branches that cannot be matched are skipped [TBI]
	
#### Documentation

See the accompanying Grammar and Use files.

#### License

Antlr-standard BSD License.  See the accompanying License.txt file.

#### Dependencies

* antlr-4.5.2-complete.jar