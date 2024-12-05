<h1>BI Tableau Report for Axiom Inc.</h1>
<h2>Objective</h2>
<p>To enable data-driven insights into travel expenses, routes, and geospatial trends by combining employee travel data, Oceanic airline data, and US airport geocoding information.</p>
<br/>
<h2>Data Preparation Steps</h2>
<h3>1. Employee Flight Data</h3>
<ul>
            <li>Removed unnecessary columns (e.g., <code>Row Number</code>).</li>
            <li>Grouped airline names (e.g., "American Airlines" variants) into a single category.</li>
        </ul>

<h3>2. Oceanic Airline Data</h3>
        <ul>
            <li>Created calculated fields for <b>Airline</b> and route data.</li>
            <li>Joined Employee Flight data with Oceanic files using a <b>UNION</b>.</li>
            <li>Renamed fields (<code>Route1</code> → <code>Origin Airport</code>, <code>Route2</code> → <code>Destination Airport</code>).</li>
        </ul> 

  <h3>3. US Airport Data</h3>
        <ul>
            <li>Adjusted airport codes and joined geospatial data:</li>
            <ul>
                <li><b>JOIN1:</b> Mapped <code>Origin Airport Code</code> with US airport data.</li>
                <li><b>JOIN3:</b> Mapped <code>Destination Airport Code</code> with US airport data.</li>
            </ul>
            <li>Renamed fields for clarity (e.g., <code>Latitude</code> → <code>Origin Latitude</code>).</li>
        </ul>

<h3>4. Cleanup</h3>
        <ul>
            <li>Removed unnecessary fields (e.g., <code>File Paths</code>, <code>Row ID</code>).</li>
            <li>Merged and grouped similar fields (e.g., <code>Ticket Type</code> → <code>Fare Type</code>).</li>
        </ul>

<h3>5. Output</h3>
<ul>
<li>The final dataset integrates travel data, airline data, and geocoding information, ready for visualization.</li>
        </ul>
        
 <h2>Visualization Approach</h2>
 <p>The report uses a <b>hybrid approach</b> combining <b>exploratory</b> and <b>explanatory</b> techniques:</p>
        <ul>
            <li><b>Exploratory:</b> To identify patterns and trends.</li>
            <li><b>Explanatory:</b> To present specific insights and KPIs.</li>
        </ul>


 <h2>Key KPIs and Visualizations</h2>
        <h3>1. Most Expensive Routes (Bar Chart - Exploratory)</h3>
        <ul>
            <li><b>Purpose:</b> Identify routes with the highest ticket prices.</li>
            <li><b>Insight:</b> Airport route <code>Houston (DAL-HOU)</code> consistently emerges as the most expensive.</li>
        </ul>

<h3>2. Purchase Time (Text Table - Exploratory/Explanatory)</h3>
        <ul>
            <li><b>Purpose:</b> Analyze the time between ticket purchase and travel.</li>
            <li><b>Insight:</b> Increased travel during <b>Q1 and Q2</b>, with peak ticket prices in <b>Q3</b> for routes like <code>DAL-AMA</code>.</li>
        </ul>    
     


<h3>3. Geocoding Visualization (Map - Explanatory)</h3>
        <ul>
            <li><b>Purpose:</b> Display geographical data, including latitude, longitude, and ticket prices.</li>
            <li><b>Insight:</b> Provides spatial patterns and cost distribution across airports.</li>
        </ul>

<h3>4. Travel Date and Ticket Price (Scatter Plot - Exploratory)</h3>
        <ul>
            <li><b>Purpose:</b> Correlate travel dates and ticket prices for specific airports.</li>
            <li><b>Insight:</b> In <b>Q3 2018</b>, ticket prices peaked at <b>$4593</b>.</li>
        </ul>     




<h2>Dashboard Features</h2>
        <ul>
            <li><b>Hybrid Dashboard:</b> Combines bar charts, scatter plots, and geospatial maps for comprehensive insights.</li>
            <li><b>Interactive Filters:</b> Enable users to focus on specific airports, routes, or time periods.</li>
            <li><b>Consistent Design:</b> Includes clear titles, labels, and axes for better user experience.</li>
        </ul>
        
<h3>Summary</h3>
        <p>
            This BI report empowers the <b>Finance Manager</b> at Axiom Inc. to make informed, data-driven decisions regarding travel expenses. By integrating and visualizing key data, it ensures financial efficiency and supports actionable insights.
        </p>
    

























        
