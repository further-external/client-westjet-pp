# client-westjet-pp

<h1>Overview</h1>
<p>
  This repository contains the necessary specifications to build an event driven
  data layer and Adobe Launch libraries reference for each WestJet
  environments.&nbsp;&nbsp;
</p>
<h1>Implement Launch script to Page</h1>
<p>
  The embed code is a&nbsp;&lt;script&gt;&nbsp;tag that you put on the pages of
  your site to load and execute the logic you build in Launch. If you load the
  library asynchronously, the browser continues to load the page, retrieves the
  Launch library, and executes it in parallel. In this case, there is only one
  embed code, which you put in the&nbsp;&lt;head&gt;.
</p>
<p>&nbsp;</p>
<p>
  Development, Staging, and Production environments correspond to the typical
  environments in the code development and release process. Code is first
  written by developers in a Development environment. When they have completed
  their work, they send it to a Staging environment for QA and other teams to
  review. After the QA and other teams are satisfied, the code is published to
  the Production environment, which is the public-facing environment which your
  visitors experience when they come to your website.
</p>
<p>&nbsp;</p>
<p>
  Launch permits additional Development environments, which is useful in large
  organizations where multiple developers work on different projects at the same
  time.
</p>
<p>&nbsp;</p>
<p>
  The embed code should be implemented in the&nbsp;&lt;head&gt;&nbsp;element of
  all HTML pages that share the property. You might have one or several template
  files that control the&nbsp;&lt;head&gt;&nbsp;globally across the site, making
  it a straightforward process to add Launch.
</p>
<p>&nbsp;</p>
<p>
  For the scope of RBF Apollo PoC we intent to deploy the Launch scripts in
  below environments:
</p>
<p>&nbsp;</p>
<ol>
  <li>Dev: <a href="https://dev.westjet.com">https://dev.westjet.com</a></li>

  <li>QA: <a href="https://qa.westjet.com">https://qa.westjet.com</a></li>

  <li>
    Staging&nbsp;:
    <a href="https://staging.westjet.com">https://staging.westjet.com</a>
  </li>

  <li>Prod: <a href="https://www.westjet.com">https://www.westjet.com</a></li>
</ol>
<p>&nbsp;</p>
<table width="99%">
  <tbody>
    <tr>
      <td width="618">
        <p><strong>// DEV</strong></p>

        <p><strong>&nbsp;</strong></p>

        <p>
          &lt;script
          src="https://dev.westjet.com/web-data/dtm?app=rbfPaymentPortalEventDriven"
          async&gt;&lt;/script&gt;
        </p>
        <p>&nbsp;</p>
        <p><strong>// QA</strong></p>
        <p>&nbsp;</p>
        <p>
          &lt;script
          src="https://qa.westjet.com/web-data/dtm?app=rbfPaymentPortalEventDriven"
          async&gt;&lt;/script&gt;
        </p>
        <p>&nbsp;</p>
        <p><strong>// Staging</strong></p>
        <p>&nbsp;</p>
        <p>
          &lt;script src="<a href="https://staging.westjet.com/web-data/dtm?app=rbfPaymentPortalEventDriven">https://staging.westjet.com/web-data/dtm?app=rbfeventdriven</a>" async&gt;&lt;/script&gt;
        </p>
        <p>&nbsp;</p>
        <p><strong>// Production</strong></p>
        <p>&nbsp;</p>
        <p>
          &lt;script
          src="https://www.westjet.com/web-data/dtm?app=rbfPaymentPortalEventDriven"
          async&gt;&lt;/script&gt;
        </p>
      </td>
    </tr>
  </tbody>
</table>
<p>&nbsp;</p>
<table>
  <tbody>
    <tr>
      <td width="598">
        <p>
          <strong>Note: </strong>The Adobe Launch libraries above will need to
          load with reference to the 'app=rbfPaymentPortalEventDriven' .com file
          (for maintenance kill switch purposes).
        </p>
      </td>
    </tr>
  </tbody>
</table>
<p>&nbsp;</p>
<p>
  The script tag will load the below respective Launch library in each
  environment.
</p>
<table width="618">
  <tbody>
    <tr>
      <td width="139">
        <p><strong>&nbsp;</strong></p>
      </td>
      <td width="215">
        <p><strong>.com Location</strong></p>
      </td>
      <td width="264">
        <p><strong>Launch Environment Script</strong></p>
      </td>
    </tr>
    <tr>
      <td width="139">
        <p><strong>Dev Header</strong></p>
        <p>(https://dev.westjet.com)</p>
      </td>
      <td width="215">
        <p>
          &lt;script
          src="https://dev.westjet.com/web-data/dtm?app=rbfPaymentPortalEventDriven"
          async&gt;&lt;/script&gt;
        </p>
      </td>
      <td width="264">
        <p>
          &lt;script
          src="https://assets.adobedtm.com/d36a486549b5/bbdf023a6674/launch-331c62585069-development.min.js"
          async&gt;&lt;/script&gt;
        </p>
      </td>
    </tr>
    <tr>
      <td width="139">
        <p><strong>QA Header </strong></p>
        <p>(https://qa.westjet.com)</p>
      </td>
      <td width="215">
        <p>
          &lt;script
          src="https://qa.westjet.com/web-data/dtm?app=rbfPaymentPortalEventDriven"
          async&gt; &lt;/script&gt;
        </p>
      </td>
      <td width="264">
        <p>
          &lt;script
          src="https://assets.adobedtm.com/d36a486549b5/bbdf023a6674/launch-941d04afe3e4-development.min.js"
          async&gt;&lt;/script&gt;
        </p>
      </td>
    </tr>
    <tr>
      <td width="139">
        <p><strong>Staging Header </strong></p>
        <p>(https://staging.westjet.com)</p>
      </td>
      <td width="215">
        <p>
          &lt;script
          src="https://staging.westjet.com/web-data/dtm?app=rbfPaymentPortalEventDriven"
          async&gt; &lt;/script&gt;
        </p>
      </td>
      <td width="264">
        <p>
          &lt;script
          src="https://assets.adobedtm.com/d36a486549b5/bbdf023a6674/launch-a201bdb1a2c9-staging.min.js"
          async&gt;&lt;/script&gt;
        </p>
      </td>
    </tr>
    <tr>
      <td width="139">
        <p><strong>Production Header</strong></p>
        <p>(https://www.westjet.com)</p>
      </td>
      <td width="215">
        <p>
          &lt;script
          src="https://www.westjet.com/web-data/dtm?app=rbfPaymentPortalEventDriven"
          async&gt; &lt;/script&gt;
        </p>
      </td>
      <td width="264">
        <p>
          &lt;script
          src="https://assets.adobedtm.com/d36a486549b5/bbdf023a6674/launch-d35fbd9cf85d.min.js"
          async&gt;&lt;/script&gt;
        </p>
      </td>
    </tr>
  </tbody>
</table>
<p><strong>Data Layer</strong></p>
<p><strong>What is data layer?</strong></p>
<ul>
  <li>
    A "Data Layer" is a term for a centralized location to store variables and
    values related to the user behavioral and page/screen level information.
  </li>
  <li>
    Data layer plugs in the backend data systems and then pulls the data points
    and puts in a well-organized place. Once in central place, so you can
    reference once central data layer for all different tags, application pixels
    that are running on the website.
  </li>
</ul>
<p><strong> </strong></p>
<p>
  A Data Layer is like a bucket that stores certain information. It's a central
  place (virtual layer) of website where you, your developers or 3<sup>rd</sup>
  party tools can temporarily store data about user, page content, etc. From
  there the tag management system like Adobe Launch reads that information, uses
  it in tags/triggers/variables or sends further to other marketing/ advertising
  tools. Data Layers are an essential part of analytics implementations. They
  provide a level of abstraction between your analytics tool and your
  developers.
</p>
<p><strong>&nbsp;</strong></p>
<p>In technical terms, a data layer is a Java Script array which is used:</p>
<ul>
  <li>
    To store all the key attributes of a web page (like page title page URL)
    etc.
  </li>

  <li>
    To store all the key information the marketing and analytics tags currently
    need (like user ID, client ID, productID etc.)
  </li>

  <li>
    To store all the key information, you may need soon, for additional tracking
  </li>

  <li>To send information from website to Tag Management system</li>
</ul>
<p>&nbsp;</p>
<p>
  Each file inside the&nbsp;events&nbsp;folder corresponds to a single use case
  or site event that needs to be implemented. These events are leveraged to
  trigger tracking rules in the tag management tool of choice and share data
  with the analytics reporting tool.
</p>
<p>
  As the data layer is event-based, the order in which the events are fired is
  critical. In general, events should be pushed onto the data layer in the
  following sequence when a page load (virtual or otherwise) occurs:
</p>
<p>
  Page Load Started &gt; <em>Other Page-level Events</em>\\ &gt; Page Load
  Completed
</p>
<p>
  If an Event is part of the page load sequence, it will be indicated in the
  corresponding event file.
</p>
<p>
  Events that occur outside of the page load sequence should be pushed onto the
  data layer as they occur.
</p>
<p><strong>Questions/Comments</strong></p>
<p>
  For any questions or comments, please contact&nbsp;<a href="mailto:maushami.desai@westjet.com">maushami.desai@westjet.com</a>
</p>