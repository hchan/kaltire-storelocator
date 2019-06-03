# Postman Demo for Kaltire
This repo shows an alternative to using `Arquillian`
Why?
* developers may be `contaminated` in testing their own rest api.  You know what works ... but is that a good or bad thing?
* developers may cheat and reuse Java code (i.e. `public static final String PAYLOAD` ) from `src/main/java`
   * test REST api's which no knowledge of the code ... black box testing with the contract as the interface
* if the rest API serves as a contract ( putting CDC, Consumer Driven Design aside for now ), is the developer who implemented the contract the person who should verify it?  For `unit` tests, the answer is `yes`.  But if this `api` is public, then shouldn't someone else verify it?
* expertise ... in my previous companies, we had a developer spearhead `Postman` tests and then we hired new grads to write the `Postman` tests ( fyi, postman's scripting language is `Javascript` ).  Do you expect a new grad to learn `Arquillian`?
    * Another way to think about it ... if your core `developers` are on a critical path, do you want to pull them away to write edge cases for a REST api?
    * Learning curve is not as steep
* Postman is one of the top *3* most popular REST API testing frameworks.  (at least that's what Google says as of May/2019)
    * Most people have probably used `Postman` for exploratory API testing.
    * Hopefully I can take this to the next level to automated tests (`newman`) in your CI
    * Fun fact, on my last contract ( MEC ), we used `Dynamics 365`.  Even `D365` [endorses](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/developer/webapi/setup-postman-environment) `Postman`
* TDD ... what if your qa team is *AHEAD* of your developers (omg, what a <sarcasm>WEIRD</sarcasm> concept)
    * `Postman` mock servers to the rescue
* I want to send my REST api to my customers with `documentation`.
    * `Postman` Api documentation to the rescue ( similar to `swagger` )
