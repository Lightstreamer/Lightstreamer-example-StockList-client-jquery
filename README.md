# Lightstreamer - Basic Stock-List Demo - HTML (jQuery, jqGrid) Client #

<!-- START DESCRIPTION lightstreamer-example-stocklist-client-jquery -->

This demo displays real-time market data for ten stocks, generated by a feed simulator in a similar way to the [Lightstreamer - Basic Stock-List Demo - HTML Client](https://github.com/Weswit/Lightstreamer-example-StockList-client-javascript#basic-stock-list-demo---html-client).<br>

<table>
  <tr>
    <td style="text-align: left">
      &nbsp;<a href="http://demos.lightstreamer.com/jqGridDemo/" target="_blank"><img src="screen_jqgrid.png"></a>&nbsp;
      
    </td>
    <td>
      &nbsp;An online demonstration is hosted on our servers at:<br>
      &nbsp;<a href="http://demos.lightstreamer.com/jqGridDemo/" target="_blank">http://demos.lightstreamer.com/jqGridDemo</a>
    </td>
  </tr>
</table>

## JQuery Grid Plugin :: Stock-List Demo ##

This page uses the <b>JavaScript Client API for Lightstreamer</b> to handle the communications with Lightstreamer Server and uses <b>jqGrid</b> to display the real-time data pushed by Lightstreamer Server. <br>
A Lightstreamer Subscription is used for subscribing to the data. The onItemUpdate callback implementation acts as a bridge between Lightstreamer and jqGrid, by injecting the real-time updates through the setRowData function.<br>
Click on the Name column header to resort the stocks in the table.<br>

The demo includes the following client-side technologies:
* A [Subscription](http://www.lightstreamer.com/docs/client_javascript_uni_api/Subscription.html) containing 10 items, subscribed to in <b>MERGE</b> mode.

<!-- END DESCRIPTION lightstreamer-example-stocklist-client-jquery -->

# Deploy #

Before you can run the demos of this project some dependencies need to be solved:

-  Get the lightstreamer.js file from the [Lightstreamer 5 Colosseo distribution](http://www.lightstreamer.com/download) 
   and put it in the "src/js" folder of the demo (if that is the case, please create it). Alternatively you can build a lightstreamer.js file from the 
   [online generator](http://www.lightstreamer.com/distros/Lightstreamer_Allegro-Presto-Vivace_5_0_Colosseo_20120803/Lightstreamer/DOCS-SDKs/sdk_client_javascript/tools/generator.html).
   In that case be sure to include the LightstreamerClient, Subscription, and StatusWidget modules and to use the "Use AMD" version.
-  Get the require.js file form [requirejs.org](http://requirejs.org/docs/download.html) and put it in the "src/js" folder of the demo.
-  In order to use jqGrid, first a UI theme css file should be loaded. Download the desired theme (or build a custom one) from [jQueryUI](www.jqueryui.com) site, get from the zip file the jquery-ui-1.x.x.custom.min.css file and "src/images" folder and put them in "src/css" folder of thie project.
-  Download the jqGrid package from the [site section downloads](www.trirand/blog). Get the i18n folder and jquery.jqGrid.min.js, jquery-1.9.0.min.js files and copy them in "src/js" folder of this project. Then get the ui.jqgrid.css file and copy it in "src/css" folder of this project.

You can deploy the demo in order to use the Lightstreamer server as Web server or in any external Web Server you are running. 
If you choose the former case please ceate the folders <LS_HOME>/pages/demos/[demo_name] then copy here the contents of the src/[demo_name] folder of this project.<br>
The client demos configuration assumes that Lightstreamer Server, Lightstreamer Adapters and this client are launched on the same machine. If you need to targeting a different Lightstreamer server please search this line:
```js
var lsClient = new LightstreamerClient(protocolToUse+"//localhost:8080","DEMO");
```
in lsClient.js and change it accordingly.<br>
Anyway the [QUOTE_ADAPTER](https://github.com/Weswit/Lightstreamer-example-Stocklist-adapter-java) and [LiteralBasedProvider](https://github.com/Weswit/Lightstreamer-example-ReusableMetadata-adapter-java) have to be deployed in your local Lightstreamer server instance. The factory configuration of Lightstreamer server already provides this adapter deployed.<br>
The demos are now ready to be launched. You can find demostrations hosted in our servers [here](http://www.lightstreamer.com/demos).

# See Also #

## Lightstreamer Adapters needed by this demo client ##

<!-- START RELATED_ENTRIES -->
* [Lightstreamer - Stock- List Demo - Java Adapter](https://github.com/Weswit/Lightstreamer-example-Stocklist-adapter-java)
* [Lightstreamer - Reusable Metadata Adapters- Java Adapter](https://github.com/Weswit/Lightstreamer-example-ReusableMetadata-adapter-java)

<!-- END RELATED_ENTRIES -->

## Similar demo clients that may interest you ##

* [Lightstreamer - Stock-List Demos - HTML Clients](https://github.com/Weswit/Lightstreamer-example-Stocklist-client-javascript)


# Lightstreamer Compatibility Notes #

- Compatible with Lightstreamer JavaScript Client library version 6.0 or newer.
