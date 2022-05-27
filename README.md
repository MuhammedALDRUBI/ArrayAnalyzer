# ArrayAnalyzer
Class for Analyzing an array and handling its values

##usable Methodes :

## HandleindexedArray(Array $indexedArray , $ElementPrefix = " " , $ElementSuffix = " " ,  $stringCapsulation = true) 
### this method handling indexed arraies ,  where  : 
- @indexedArray is an indexed array that you want to adding an @ElementPrefix before its value , and want to adding an @ElementSuffix after that value
- if @stringCapsulation is false the string values will not encapsulate in a double quotation (you will need it when you handling an sql query)
- Ex :
 $ArrayAnalyzerOb = new ArrayAnalyzer();
 $indexedArray = array("users" , "posts" , "comemnts");
  $ElementPrefix = " Table_";
  $ElementSuffix = " , ";
  $stringCapsulation = false;
 echo $ArrayAnalyzerOb->HandleindexedArray($indexedArray , $ElementPrefix  , $ElementSuffix  ,  $stringCapsulation) ;
 #### output : 
 <code>

    "Table_users , Table_posts , Table_comments"


</code>


## if an multidimensional array will be received .... the method will be able to handle it .. don't worry

<hr>


## HandleAssocArray(Array $AssocArray ,   $keyPrefix = " " , $textBetween = " " , $valSuffix = " " , $stringCapsulation = true)
### this method handling  Associative arraies ,  where  : 
- @AssocArray is an Associative array that you want to adding an @keyPrefix before each its key , and want to adding an @valSuffix after that key's value
  and want to adding @textBetween between that key and its value
- if @stringCapsulation is false the string values will not encapsulate in a double quotation (you will need it when you handling an sql query)
- Ex :
 $ArrayAnalyzerOb = new ArrayAnalyzer();
 $AssocArray = array("users" => array("FirstName" , "LastName") , "posts" => array("title" , "content") , "comemnts" => array("comment"));
  $keyPrefix = " ";
  $textBetween = ".";
  $valSuffix = " , ";
  $stringCapsulation = false;
 echo $ArrayAnalyzerOb->HandleAssocArray( $AssocArray ,   $keyPrefix , $textBetween  , $valSuffix  , $stringCapsulation  );
 #### output : 
 <code>

  
  
    " users.FirstName , users.LastName , posts.title , posts.content , comments.comment "


</code>

## if an multidimensional array will be received .... the method will be able to handle it .. don't worry

<hr>

## getArrayDimension(Array $array)
### this method will return the dimension of any array will be passing into it
### it is used by HandleindexedArray and HandleAssocArray methodes to check if they could handling the array that they received or need to call multiDimensional Methodes


<hr>

## isIndexed(Array $array)
### it is a simple method to check if an array is indexed array or not
