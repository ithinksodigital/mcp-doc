

# Code Examples for Triggered Campaign Data in Marketing Cloud Engagement
Emails

Marketing Cloud Personalization sends recommendations and other trigger-
related catalog data, such as abandoned cart items, to Marketing Cloud
Engagement in JSON format. You can render the data in your Engagement emails
using Guided Template Language and Server-Side JavaScript. These code examples
show how to render triggered campaign data in an email recommendations block.

You can modify the code blocks to change the number of rendered items, update
fonts, change table properties, and add HTML for styling. For more advanced
formatting, work with a developer.

## JSON Data Sent by the Default Template

    
    
    [
       {
           "price": 40,
           "imageUrl": "https://www.northerntrailoutfitters.com/on/demandware.static/-/Sites-nto-apparel/default/dw111991b2/images/large/2031004BI9-0.jpg",
           "name": "Women's Classic Mini Shorts",
           "id": "2031004",
           "url": "https://www.northerntrailoutfitters.com/default/women%E2%80%99s-classic-mini-shorts-2031004BI9.html"
       },
       {
           "price": 200,
           "imageUrl": "https://www.northerntrailoutfitters.com/on/demandware.static/-/Sites-nto-apparel/default/dw10dbfcd0/images/large/1010414AP0-0.jpg",
           "name": "Men's Rainier L4 Windproof Soft Shell Hoodie",
           "id": "1010414",
           "url": "https://www.northerntrailoutfitters.com/default/men%27s-rainier-l4-windproof-soft-shell-hoodie-1010414AP0.html"
       }
    ]
    

## Guided Template Language Code Block

    
    
    %%[
      /**
          Get JSON data from the Marketing Cloud event Data Extension
          and store it in the @Catalog_Data Ampscript variable.
          You should change the field name passed to the AttributeValue
          function depending on the trigger type, use-case and your template
          configuration. Refer to the "Triggered Campaign Templates" documentation
          for more information about the standard field names.
      */
      SET @Catalog_Data = AttributeValue("Recommendations")
    ]%%
     
    <div style="max-height: 100%; max-width: 600px; position: relative; overflow: hidden; margin: 20px auto; text-align: center;">
      <div style="display: table; width: 100%; max-height: 100%;">
          {{.datasource JSONVar type=variable maxRows=8}}
          {{.data}}
              { "target" : "@Catalog_Data" }
          {{/data}}
     
          <span style="display: inline-block; margin-top: 10px;">
              <!-- %%[ SET @href = TreatAsContent("{{url}}") ]%% -->
              <a href="%%=RedirectTo(@href)=%%" style="display: block; width: 300px; overflow: hidden;">
                  <img src="{{imageUrl}}" style="border: 0; width: 90%; margin: 10px;">
              </a>
              <div style="padding: 0px; margin: 0px; width: 300px; overflow: hidden;">
                  <h3 style="padding: 0px; margin: 10px; font-size: 16px; line-height: 20px; height: 40px; overflow: hidden;">
                      {{name}}
                  </h3>
                  <p style="padding: 0px; margin: 10px; font-size: 14px;">
                      Price: {{=FormatCurrency(price, "en-US")}}
                  </p>
              </div>
          </span>
            
          {{/datasource}}
      </div>
    </div>

## Server-Side JavaScript Code Block

    
    
    <script runat="server">
       Platform.Load("core", "1.1");
     
       var html = '<div style="max-height: 100%; max-width: 600px; position: relative; overflow: hidden; margin: 20px auto; text-align: center;">';
       html += '<div style="display: table; width: 100%; max-height: 100%;">';
     
       try{
           /**
               Get JSON data from the Marketing Cloud event Data Extension
               and store it in the Catalog_Data variable.
               You should change the field name passed to the Attribute.GetValue
               function depending on the trigger type, use-case and your template
               configuration. Refer to the "Triggered Campaign Templates" documentation
               for more information about the standard field names.
           */
           var Catalog_Data = Platform.Function.ParseJSON(Attribute.GetValue('Recommendations'));
     
           for(var i = 0; i < Catalog_Data.length; i++){
               html += '<span style="display: inline-block; margin-top: 10px;">';
               html += '    <a href="' + Catalog_Data[i].url + '" style="display: block; width: 300px; overflow: hidden;">';
               html += '        <img src="' + Catalog_Data[i].imageUrl + '" style="border: 0; width: 90%; margin: 10px;">';
               html += '    </a>';
               html += '    <div style="padding: 0px; margin: 0px; width: 300px; overflow: hidden;">';
               html += '        <h3 style="padding: 0px; margin: 10px; font-size: 16px; line-height: 20px; height: 40px; overflow: hidden;">';
               html += '            ' + Catalog_Data[i].name;
               html += '        </h3>';
               html += '        <p style="padding: 0px; margin: 10px; font-size: 14px;">';
               html += '            Price: ' + Catalog_Data[i].price;
               html += '        </p>';
               html += '    </div>';
               html += '</span>';
           }
       }
       catch(err){
           html += '<!--smth went wrong when rendering items-->';
       }
     
       html += '</div>';
       html += '</div>';
      
       Write(html);
    </script>

#### See Also

  * [Guided Language](https://help.salesforce.com/s/articleView?id=sf.mc_guide_template_language.htm&language=en_US&type=5)
  * [ _Developer Documentation_ : Server-Side JavaScript](https://developer.salesforce.com/docs/marketing/marketing-cloud/guide/ssjs_serverSideJavaScript.html)

