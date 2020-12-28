## ASER
sementic: Thing (or Object), Activity, State, Event, Place, Path, Property, Amount, etc.
ASER is a eventuality-centric knowledge graph.
### Motivation
1. Classic KGs(Knowledge graphs) is limited by their small scales.
2. Big KGS not only need knowledges about things or objects ,but also about activities, states and events

### Effect
1. new KG, the units is enentualityies. big enough to capture the richness and complexity of eventualities and their relations.
2. Provide several ways to infer by ASER.
3. Efficiency and application. 

### Details
1. Simplify the PDTB, concern the relationship between 2 events. Use little bias conective words as seed words.
2. KG definition (keep high precision):
   1. eventuality **E** is hyperedge linking of vertices **v**. v is word in vocabulary list. Relationship between Ei and Ej is **Ri**. Ri has a type **t** belonges to T. **H** includes {e,v,r,t}
   2. Ei connect multiple words Vi1-Vin in vocabulary list.
   3. 14 descourse relation typoes 
   4. 5 types of relations : Temporal, Comparison, Expansion, Co-Occurrence,Contingency.
   5. store the events and the relation in 2 tables. Events include id, all words,words relations and frequency; relation includes id of head and tail events and relations.
3. Knowledge extraction:
   1. for each sentence: if over 2 events, generate training case includes 2 events and original sentence.
   2. Preprocess: filtered sentence contained clauses; extract all verbs and make sure not too complicated;omit all optional edges to make sure the eventualities are semantically complete.
   3. For each verb,put it to v1 and try to find all positive dependency edges(valid event) and check for negetive edges; if not,keep it as valid event.otherwise to disqualify it.
   4. relation between events: seed relation using connection words;NN train classifier; predict the relation and add to the corresponding class.
4. Inference：
   1. One hop/two hop(one hop*one hop,bayes rule)
   2. Eventuality retrieval can easily find out that some events will lead to specific events which is like our insight.
5. full version precision is lower than core version, but have more knowledge.