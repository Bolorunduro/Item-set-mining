# Item-set-mining
comparison between Aprior and FP Growth algorithm
<dependency>
  <groupId>com.github.chen0040</groupId>
      <artifactId> Java-frequent-pattern-mining</artifactId> 
      <version>1.0.1</version>
</dependency>
FP Growth
The sample code below shows how to use FP Growth to obtain the frequent item sets from a list of transactions
List<List<String>> database = new Array List< > ( );
 // each line below add a new transaction to the database
  database .add (Arrays.asList ("f", "a", "c", "d", "g", "i","m","p"));
database. add(Arrays.asList("a", "b", "c", "f", "l", "m", "o"));
database.add(Arrays.asList("b", "f", "h", "j", "o", "w"));
database.add (Arrays.asList ("b", "c", "k", "s", "p"));
database.add(Arrays.asList("a", "f", "c", "e", "l", "p", "m", "n")); 
 AssocRuleMiner  method = new FPGrowth ( );
method.setMinSupportLevel(2);
MetaData  metaData   = new MetaData(database);
 // obtain all frequent item sets with support level not below 2
Item Sets frequent_item_sets = method.minePatterns (database, metaData.getUniqueItems ());
fis .stream ( ) .for Each (item Set -> System.out.println ("item-set: " + item Set));
 // obtain the max frequent item sets
Item  Setsmax_frequent_item_sets=method.findMaxPatterns(database,metaData.getUniqueItems());
Apriori.
The sample code below shows how to use Apriori to obtain the frequent item sets from a list of transactions.
List<List<String>> database = new ArrayList<>();
// each line below add a new transaction to the database
database.add(Arrays.asList("f", "a", "c", "d", "g", "i", "m", "p"));
database.add(Arrays.asList("a", "b", "c", "f", "l", "m", "o"));
database.add(Arrays.asList("b", "f", "h", "j", "o", "w"));
database.add(Arrays.asList("b", "c", "k", "s", "p"));
database.add(Arrays .asList("a", "f", "c", "e", "l", "p", "m", "n"));
AssocRuleMiner method = new Apriori ( ); 
method.setMinSupportLevel (2);
MetaData metaData = new MetaData(database);
