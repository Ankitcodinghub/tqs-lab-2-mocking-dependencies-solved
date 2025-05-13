# tqs-lab-2-mocking-dependencies-solved
**TO GET THIS SOLUTION VISIT:** [TQS Lab 2-Mocking dependencies Solved](https://www.ankitcodinghub.com/product/tqs-lab-2-mocking-dependencies-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;93884&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;0&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;0&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;0\/5 - (0 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;TQS Lab 2-Mocking dependencies Solved&quot;,&quot;width&quot;:&quot;0&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 0px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            <span class="kksr-muted">Rate this product</span>
    </div>
    </div>
<div class="page" title="Page 5">
<div class="layoutArea">
<div class="column">
Lab 2 Mocking dependencies (for unit testing)

Context and key points Learning objectives

<ul>
<li>⎯ &nbsp;Prepare a project to run unit tests (JUnit 5) and mocks (Mockito 3.x), with mocks injection (@Mock).</li>
<li>⎯ &nbsp;Write and execute unit tests with mocked dependencies.</li>
<li>⎯ &nbsp;Experiment with mock behaviors: strict/lenient verifications, advanced verifications, etc.
Preparation

Get familiar with sections 1 to 3 in the Mockito (Javadoc) documentation. Explore
</li>
</ul>
– There is a recent book on JUnit and Mockito available from OReilly. The lessons are available as short videos too.

2.1 Stocks

Consider the example in Figure 1: the StocksPortfolio holds a collection of Stocks; the current value of the portfolio depends on the current condition of the Stock Market. StockPortfolio#getTotalValue() method calculates the value of the portfolio (by summing the current value of owned stock, looked up in the stock market service).

</div>
</div>
<div class="layoutArea">
<div class="column">
TQS LABS | 5

</div>
</div>
</div>
<div class="page" title="Page 6">
<div class="layoutArea">
<div class="column">
1a/

Implement (at least) one test to verify the implementation of StockPortfolio#getTotalValue(). Given that test should have predictable results, you need to address the problem of having non- deterministic answers from the IStockmarketService interface.

Figure 1: Classes for the StocksPortfolio use case.

<ol>
<li>a) &nbsp;Create the classes. You may write the implementation of the services before or after the tests.</li>
<li>b) &nbsp;Create the test for the getTotalValue(). As a guideline, you may adopt this outline:
<ol>
<li>Prepare a mock to substitute the remote service (@Mock annotation)</li>
<li>Create an instance of the subject under test (SuT) and use the mock to set
<pre>            the (remote) service instance.
</pre>
</li>
<li>Load the mock with the proper expectations (when…thenReturn)</li>
<li>Execute the test (use the service in the SuT)</li>
<li>Verify the result (assert) and the use of the mock (verify)</li>
</ol>
</li>
</ol>
Notes:

<ul>
<li>⎯ &nbsp;Consider use these Maven dependencies for your POM (JUnit5, Mockito).</li>
<li>⎯ &nbsp;Mind the JUnit version. For JUnit 5, you should use the @ExtendWith annotation to integrate the Mockito framework.
@ExtendWith(MockitoExtension.class) class StocksPortfolioTest { … }
</li>
<li>⎯ &nbsp;See a quick reference of Mockito syntax and operations.
1b/ Instead of the JUnit core asserts, you may use the Hamcrest library to create more human- readable assertions. Replace the “Assert” statements in the previous example, to use Hamcrest constructs. E.g.:

assertThat(result, is(14.0));

2.2 Geocoding

Consider an application that needs to perform reverse geocoding to find a zip code for a given set of GPS coordinates. This service can be assisted by public APIs (e.g.: using the MapQuest API).

Let as create a very simple application to perform (reverse) geocoding and set a few tests.
</li>
</ul>
a) Create the objects represented in Figure 1. At this point, do not implement TqsBasicHttpClient; in fact, you should provide a substitute for it.

</div>
</div>
</div>
<div class="page" title="Page 7">
<div class="layoutArea">
<div class="column">
45426 Teste e Qualidade de Software

</div>
</div>
<div class="layoutArea">
<div class="column">
<ol start="2">
<li>b) &nbsp;Consider that we want to test the behavior of AddressResolver#findAddressForLocation, which invokes a remote geocoding service, available in a REST interface, passing the site coordinates.
Which is the SuT (subject under test)? Which is the service to mock?
</li>
<li>c) &nbsp;To create a test for findAddressForLocation, you will need to mimic the exact (JSON) response
of the geocoding service for a request. Study/try the MapQuest API (e.g.: example 1).
</li>
<li>d) &nbsp;Implement a test for AddressResolver#findAddressForLocation (using a mock).</li>
<li>e) &nbsp;Besides the “success” case, consider also testing for alternatives (e.g.: bad coordinates;…). You may need to change the implementation.</li>
</ol>
This getting started project [gs-mockForHttpClient] can be used in your implementation.

</div>
</div>
<div class="layoutArea">
<div class="column">
Figure 2: Classes for the geocoding use case.

2.3 Integration

Consider you are implementing an integration test for the previous example, and, in this case, you would use the real implementation of the module, not the mocks, in the test.

(This section can be included with the previous, continuing the same project.)

Create a test class (AddressResolverIT), in a separate test package, and be sure its name ends with “IT”. Copy the tests from the previous exercise into this new test class but remove any support for mocking (no Mockito imports in this test).

Correct/complete the test implementation so it uses the real HttpClient implementation.

Run your test (and confirm that the remote API is invoked in the test execution).

Be sure the “failsafe” maven plugin is configured. You should get different results with:

<pre>     $ mvn test
     and
     $ mvn install failsafe:integration-test
</pre>
(Note the number of tests and the time required to run the tests…).

</div>
</div>
<div class="layoutArea">
<div class="column">
TQS LABS | 7

</div>
</div>
</div>
