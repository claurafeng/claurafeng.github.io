---
title: "Effects of Economic Conditions on Labor Force Partcipation"
permalink: /portfolio/economic_condition_effects_on_labor_force/
layout: single
author_profile: true
---

<style>
.project-meta {
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
  margin-bottom: 1.5rem;
}
.badge {
  display: inline-block;
  font-size: 0.78em;
  padding: 3px 10px;
  border-radius: 12px;
  font-weight: 500;
}
.badge-blue  { background: #dbeafe; color: #1e40af; }
.badge-green { background: #dcfce7; color: #166534; }
.badge-gray  { background: #f1f5f9; color: #475569; }

.section-block {
  border-left: 3px solid #52adc8;
  padding-left: 1rem;
  margin: 2rem 0 1rem;
  border-radius: 0;
}
.section-block h2 { margin: 0; font-size: 1.2em; }

.stats-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(160px, 1fr));
  gap: 1rem;
  margin: 1.25rem 0;
}
.stat-card {
  background: #f8fafc;
  border: 1px solid #e2e8f0;
  border-radius: 8px;
  padding: 0.9rem 1rem;
  text-align: center;
}
.stat-card .stat-value { font-size: 1.5em; font-weight: bold; color: #0f172a; display: block; }
.stat-card .stat-label { font-size: 0.8em; color: #64748b; margin-top: 2px; display: block; }

.finding-box {
  background: #f0f9ff;
  border: 1px solid #bae6fd;
  border-radius: 8px;
  padding: 1rem 1.2rem;
  margin: 1rem 0;
}
.finding-box.green { background: #f0fdf4; border-color: #bbf7d0; }
.finding-box h4 { margin: 0 0 0.4rem 0; font-size: 0.95em; color: #0369a1; }
.finding-box.green h4 { color: #166534; }
.finding-box p { margin: 0; font-size: 0.9em; }

.var-table {
  width: 100%; border-collapse: collapse; font-size: 0.9em; margin: 1rem 0;
}
.var-table th {
  background: #f1f5f9; text-align: left; padding: 7px 12px;
  border: 1px solid #e2e8f0; font-weight: 600;
}
.var-table td { padding: 7px 12px; border: 1px solid #e2e8f0; vertical-align: top; }
.var-table tr:nth-child(even) td { background: #f8fafc; }

/* Dataset link box */
.dataset-box {
  display: flex;
  align-items: center;
  gap: 1rem;
  background: #fafafa;
  border: 1px solid #e2e8f0;
  border-radius: 8px;
  padding: 0.9rem 1.2rem;
  margin: 1rem 0;
}
.dataset-box .ds-icon {
  font-size: 1.6em;
  flex-shrink: 0;
}
.dataset-box .ds-text { flex: 1; }
.dataset-box .ds-text strong { display: block; font-size: 0.95em; margin-bottom: 2px; }
.dataset-box .ds-text span { font-size: 0.82em; color: #64748b; }
.dataset-box a.ds-btn {
  display: inline-block;
  font-size: 0.82em;
  padding: 5px 14px;
  background: #52adc8;
  color: #fff;
  border-radius: 6px;
  text-decoration: none;
  white-space: nowrap;
  flex-shrink: 0;
}
.dataset-box a.ds-btn:hover { background: #3a8fa8; }

/* Step-by-step code blocks */
.step-list { margin: 1rem 0; }
.step {
  display: flex;
  gap: 1rem;
  margin-bottom: 1.75rem;
  align-items: flex-start;
}
.step-num {
  width: 28px;
  height: 28px;
  border-radius: 50%;
  background: #52adc8;
  color: #fff;
  font-size: 0.82em;
  font-weight: bold;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-shrink: 0;
  margin-top: 2px;
}
.step-content { flex: 1; min-width: 0; }
.step-content h4 { margin: 0 0 0.35rem 0; font-size: 0.95em; color: #0f172a; }
.step-content p { margin: 0 0 0.5rem 0; font-size: 0.87em; color: #475569; line-height: 1.5; }
.step-content pre {
  background: #1e293b;
  color: #e2e8f0;
  border-radius: 8px;
  padding: 0.9rem 1rem;
  font-size: 0.82em;
  overflow-x: auto;
  margin: 0;
  line-height: 1.6;
}
.step-content pre .comment { color: #94a3b8; }
.step-content pre .string  { color: #86efac; }
.step-content pre .fn      { color: #93c5fd; }

.back-link {
  display: inline-block;
  margin-bottom: 1.5rem;
  font-size: 0.9em;
  color: #52adc8;
  text-decoration: none;
}
.back-link:hover { text-decoration: underline; }
</style>

<a class="back-link" href="/portfolio/">← Back to Portfolio</a>

<div class="project-meta">
  <span class="badge badge-blue">R / RStudio</span>
  <span class="badge badge-blue">Histogram</span>
  <span class="badge badge-blue">Scatterplot</span>
  <span class="badge badge-blue">Correlation Analysis</span>
  <span class="badge badge-blue">Simple Regression</span>
  <span class="badge badge-blue">Residual Analyses</span>
  <span class="badge badge-gray">46 observations</span>
  <span class="badge badge-gray">Federal Reserve Bank of St. Louis</span>
</div>

---

<div class="section-block"><h2>Overview</h2></div>

This project analyzes how economic conditions (measured using the civilian unemployment rate from the [Federal Reserve Bank of St. Louis](https://fred.stlouisfed.org/series/UNRATE)) can predict the percentage of people who join the labor force (measured by the labor force participation rate from the [Federal Reserve Bank of St. Louis](https://fred.stlouisfed.org/series/CIVPART))) in the United States from 1980-2025. The analysis would reveal which one of two different economic theories (discouraged worker effect and added worker effect) is better supported by the employment data through a regression to predict and quantify the relationship.

When looking at the relationship holistically in regards to time period, no statistically significant relationship emerged. Thus, the full period will be split into **two eras** (1980-2008 and 2009-2025) to conduct the regression. In the end, a residual analysis would be conducted to test whether the regression model is appropriate and identify outliers. The data consists of three variables: **year**, **labor force participation rate (CLFPR)**, and **unemployment rate (CUNR)**.

---

<div class="section-block"><h2>Data</h2></div>

The dataset contains employment information on **46 years** (1980-2025) from the Federal Reserve Bank of St. Louis. The three variables used in this analysis are:

<table class="var-table">
  <thead>
    <tr><th>Variable</th><th>Abbreviation</th><th>Type</th><th>Description</th></tr>
  </thead>
  <tbody>
    <tr>
      <td>Year</td>
      <td>Year</td>
      <td>Numeric (discrete)</td>
      <td>Year in which the data was recorded</td>
    </tr>
    <tr>
      <td>Civilian Labor Force Participation Rate</td>
      <td>CLFPR</td>
      <td>Numeric (continuous)</td>
      <td>Percentage of the population that is either working or actively looking for work</td>
    </tr>
    <tr>
      <td>Civilian Unemployment Rate</td>
      <td>CUNR</td>
      <td>Numeric (continuous)</td>
      <td>Percentage of the labor force that is unemployed</td>
    </tr>
  </tbody>
</table>

<div class="dataset-box">
  <span class="ds-icon">📄</span>
  <div class="ds-text">
    <strong>Employment Dataset (.csv)</strong>
    <span>years 1980-2025 · sourced from Federal Reserve Bank of St. Louis</span>
  </div>
  <a class="ds-btn" href="(https://docs.google.com/spreadsheets/d/1KMYsLpdXuXHFCHlSGkyiei_idV9minj4bWV-vmCqolo/edit?gid=0#gid=0)" target="_blank">View Dataset →</a>
</div>

---

<div class="section-block"><h2>Step-by-Step Analysis in R</h2></div>

<div class="step-list">

  <div class="step">
    <div class="step-num">1</div>
    <div class="step-content">
      <h4>Import the data</h4>
      <p>Load the CSV file into RStudio and install relevant package.</p>
      <pre><span class="comment"># Import data from CSV</span>
employment &lt;- <span class="fn">read.csv</span>(<span class="string">"Documents/Regression/RData/employment.csv"</span>)

<span class="comment"># Install ggplot2 package</span>
<span class="fn">install.packages</span>("ggplot2")
<span class="fn">library</span>("ggplot2")</pre>
    </div>
  </div>

  <div class="step">
    <div class="step-num">2</div>
    <div class="step-content">
      <h4>Distribution: Labor Force Participation Rate</h4>
      <p>Visualize the distribution's shape for labor force participation rate through a histogram and summary.</p>
      <pre><span class="comment"># Summary: CLFPR</span>
<span class="fn">summary</span>(employment$CLFPR)

<span class="comment"># Histogram: CLFPR</span>
<span class="fn">hist</span>(employment$CLFPR, 
        main = <span class="string">"Distribution of Labor Force Participation Rate"</span>,
        xlab = <span class="string">"Labor Force Participation Rate"</span>,
        col =<span class="string">"red"</span>)</pre>
    <img src="/images/employment_clfpr_summary.png" alt="Summary of CLFPR" style="width:100%; border-radius:6px; margin-top:0.75rem;">
    <img src="/images/employment_clfpr_histogram.png" alt="Histogram of CLFPR" style="width:100%; border-radius:6px; margin-top:0.75rem;">
      <p>To understand the shape of distribution of the labor force participation rate, the above histogram is analyzed. The shape of the data is relatively symmetric with the mean being around the middle of the minimum and maximum. The dip in the middle suggests that values tended to fall below or above the typical labor force participation rate (64.89%). The mean is also close to the median, which indicates that the data is not very skewed. There are no clear univariate outliers present because all the values lie within a reasonable distance from the center and do not appear isolated from the rest of the distribution.
</p>
    </div>
  </div>

  <div class="step">
    <div class="step-num">3</div>
    <div class="step-content">
      <h4>Distribution: Unemployment Rate</h4>
      <p>Visualize the distribution's shape for unemployment rate through a histogram and summary.</p>
      <pre><span class="comment"># Summary: CUNR</span>
<span class="fn">summary</span>(employment$CUNR)

<span class="comment"># Histogram: CUNR</span>
<span class="fn">hist</span>(employment$CUNR, 
        main = <span class="string">"Distribution of Unemployment Rate"</span>,
        xlab = <span class="string">"Unemployment Rate"</span>,
        col =<span class="string">"orange"</span>)</pre>
    <img src="/images/employment_cunr_summary.png" alt="Summary of CUNR" style="width:100%; border-radius:6px; margin-top:0.75rem;">
    <img src="/images/employment_cunr_histogram.png" alt="Histogram of CUNR" style="width:100%; border-radius:6px; margin-top:0.75rem;">
      <p>The above histogram shows the distribution of the unemployment rate. The shape of the data appears right-skewed, tapering off gradually on the right compared to the left with most observations clustering between approximately 4% and 7%. The max value is further from the central tendencies compared to the min value, which further indicates that the histogram is skewed. While the 10.4% unemployment rate value is further from the rest of the values, it does not violate the 1.5 x IQR rule, meaning that it is not an univariate outlier.
</p>
    </div>
  </div>


  <div class="step">
    <div class="step-num">4</div>
    <div class="step-content">
      <h4>Correlation test: Labor Force Participation Rate and Unemployment Rate</h4>
      <p>Visualize the relationship between CLFPR and CUNR using a scatterplot.</p>
      <pre><span class="comment"># Scatterplot: CLFPR vs CUNR</span>
employment_scatterplot &lt;- <span class="fn">ggplot</span>(employment, <span class="fn">aes</span>(x = CUNR, y = CLFPR)) +
        <span class="fn">geom_point</span>(color = <span class="string">"blue"</span>, alpha = 0.7) +
        <span class="fn">labs</span>(title = <span class="string">"Relationship Between Unemployment Rate and Labor Force Participation Rate"</span>, x = <span class="string">"Unemployment Rate"</span>, y = <span class="string">"Labor Force Participation Rate"</span>) +
        <span class="fn">theme_minimal</span>()
<span class="fn">print</span>(employment_scatterplot)

<span class="comment"># Pearson correlation: CLFPR vs CUNR</span>
<span class="fn">cor.test</span>(employment$CUNR,employment$CLFPR, method = <span class="string">"pearson"</span>)</pre>
        <img src="/images/employment_clfpr_cunr_scatterplot.png" alt="CLFPR vs CUNR Scatterplot" style="width:100%; border-radius:6px; margin-top:0.75rem;">
        <img src="/images/employment_clfpr_cunr_correlation_test.png" alt="CLFPR vs CUNR Correlation Test" style="width:100%; border-radius:6px; margin-top:0.75rem;">
      <p>	The following scatterplot shows the relationship between unemployment rate and labor force participation over the span of 1980 to 2025. This initial bivariate analysis does not indicate a strong linear relationship, and the points appear dispersed without a consistent upward or downward trend. Examining the correlation statistics revealed that the model is not statistically significant because the p-value is 0.89, which is greater than 0.05. The variables also appear to not or have little relationship with each other with a r value of -0.02, which has an absolute value less than 0.1. A different approach would have to be taken to predict the relationship.
</p>

    </div>
  </div>

  <div class="step">
    <div class="step-num">5</div>
    <div class="step-content">
      <h4>Bivariate Analysis (1980-2008 and 2008-2025 Subsets): CLFPR vs CUNR</h4>
      <p>Visualize the relationship with a scatterplot and run a correlation analysis on the relationship between CLFPR and CUNR for two different time periods (1980-2008 and 2008-2025).</p>
      <pre><span class="comment"># Label the years 2008 and before "1980-2008" and the rest "2009-2025"</span>
employment$period &lt;- <span class="fn">ifelse</span>(employment$Year <= 2008, <span class="string">"1980-2008"</span>, <span class="string">"2009-2025"</span>)
  
<span class="comment"># Scatterplot: CLFPR vs CUNR (Time Period Subsets)</span>
<span class="fn">plot</span>(employment$CUNR, employment$CLFPR,
        col = <span class="fn">ifelse</span>(employment$period == <span class="string">"1980-2008"</span>, <span class="string">"red"</span>, <span class="string">"blue"</span>),
        pch = 19,
        main = <span class="string">"Relationship Between Unemployment Rate and Labor Force Participation Rate"</span>,
        xlab = <span class="string">"Unemployment Rate"</span>,
        ylab = <span class="string">"Labor Force Participation Rate"</span>
<span class="fn">legend</span>(<span class="string">"topright"</span>,
        legend = <span class="fn">c</span>(<span class="string">"1980-2008"</span>, <span class="string">"2009-2025"</span>),
        col = <span class="fn">c</span>(<span class="string">"red"</span>, <span class="string">"blue"</span>),
        pch = 19)

        
<span class="comment"># Split data into two periods for correlation analysis</span>
period1 &lt;- <span class="fn">subset</span>(employment, Year <= 2008)
period2 &lt;- <span class="fn">subset</span>(employment, Year >= 2009)

<span class="comment"># Pearson correlation: CLFPR vs CUNR (Time Period Subsets)</span>
<span class="fn">cor.test</span>(period1$CUNR, period1$CLFPR)
<span class="fn">cor.test</span>(period2$CUNR, period2$CLFPR)</pre>
        <img src="/images/employment_clfpr_cunr_year_subsets_scatterplot.png" alt="CLFPR vs CUNR Subset Scatterplot" style="width:100%; border-radius:6px; margin-top:0.75rem;">
        <img src="/images/employment_clfpr_cunr_period1_correlation_test.png" alt="CLFPR vs CUNR 1980-2008 Correlation Test" style="width:100%; border-radius:6px; margin-top:0.75rem;">
        <img src="/images/employment_clfpr_cunr_period2_correlation_test.png" alt="CLFPR vs CUNR 2009-2025 Correlation Test" style="width:100%; border-radius:6px; margin-top:0.75rem;">
      <p>The full time period for the data is split into two different time periods: 1980-2008 and 2008-2025. Unlike with the full time period, having two different periods allows for predictive analyses. The separated graphs do not have simple curves that can fit the values better than a line, implying a linear relationship. The spread of points is also roughly constant across the values, implying homoscedasticity. There are also no extreme outliers apparent in the graph. The correlation analyses of the two lines also indicate appropriateness for regression. The correlation analysis for 1980-2008 indicates that the model is statistically significant with p-value<0.01, which is less than 0.05, and the variables have a strong relationship with the absolute value of r being 0.79, which is greater than 0.5. Meanwhile, 2009-2025 has p-value<0.01, indicating statistical significance too as it’s less than 0.05. It has a r value of 0.68, which also indicates a strong relationship between variables.
</p>

    </div>
  </div>

  <div class="step">
    <div class="step-num">6</div>
    <div class="step-content">
      <h4>Regression Analysis (1980-2008 and 2008-2025 Subsets): CLFPR vs CUNR</h4>
      <p>Run regression analyses for the two time periods to show how the unemployment rate can be used to predict the labor force participation rate in the two different time periods.</p>
<pre><span class="comment"># Regression analysis: CLFPR vs CUNR (1980-2008)</span>
<span class="fn">summary</span>(<span class="fn">lm</span>(CLFPR ~ CUNR, data = period1))

<span class="comment"># Regression analysis: CLFPR vs CUNR (2009-2025)</span>
<span class="fn">summary</span>(<span class="fn">lm</span>(CLFPR ~ CUNR, data = period2))</pre>
        <img src="/images/employment_reg_analysis_period1.png" alt="Regression Analysis 1980-2008" style="width:100%; border-radius:6px; margin-top:0.75rem;">
        <img src="/images/employment_reg_analysis_period2.png" alt="Regression Analysis 2009-2025" style="width:100%; border-radius:6px; margin-top:0.75rem;">
      <p>The regression equation for 1980-2008 is estimated CLFPR = 69.66 - 0.62 CUNR. The coefficient indicates that for every 1% increase in unemployment rate, the labor force participation rate decreases by 0.62%. The model for this time period is statistically significant because p-value<0.01 is less than 0.05. R2 is 0.61, which indicates that approximately 61% of the variation in labor force participation is explained by unemployment during this period. Meanwhile, the regression equation for 2009-2025 is estimated CLFPR = 61.28 + 0.33 CUNR. The coefficient indicates that for every 1% increase in unemployment rate, the labor force participation rate increases by 0.33%. The model for this time period is statistically significant because p-value<0.01 is less than 0.05. R2 is 0.46, which indicates that approximately 46% of the variation in labor force participation is explained by unemployment during this period.
</p>

    </div>
  </div>

  <div class="step">
    <div class="step-num">7</div>
    <div class="step-content">
      <h4>Residual Analysis (1980-2008 and 2009-2025 Subsets): CLFPR vs CUNR</h4>
      <p>Run residual analyses for the two time periods to identify potential outliers.</p>
<pre><span class="comment"># Standardized Residual analysis: 1980-2008</span>
<span class="fn">summary</span>(<span class="fn">lm</span>(CLFPR ~ CUNR, data = period1))
<span class="fn">plot</span>(period1$CUNR, period1$Std_Resid,
     main = <span class="string">"Standardized Residuals: 1980-2008"</span>,
     xlab = <span class="string">"CUNR"</span>, ylab = <span class="string">"Standardized Residuals"</span>,
     pch = 16, col = <span class="fn">ifelse</span>(<span class="fn">abs</span>(period1$Std_Resid) > 2, <span class="string">"red"</span>, <span class="string">"black"</span>))
<span class="fn">abline</span>(h = 0, col = <span class="string">"gray"</span>, lty = 2)
<span class="fn">abline</span>(h = <span class="fn">c</span>(-2, 2), col = <span class="string">"red"</span>, lty = 3)
<span class="fn">text(period1$CUNR[abs(period1$Std_Resid) > 2],
     period1$Std_Resid[<span class="fn">abs</span>(period1$Std_Resid) > 2],
     labels = period1$Year[<span class="fn">abs</span>(period1$Std_Resid) > 2],
     pos = 3, cex = 0.8)

<span class="comment"># Standardized Residual analysis: 2009-2025</span>
<span class="fn">plot</span>(period2$CUNR, period2$Std_Resid,
     main = <span class="string">"Standardized Residuals: 2009-2025"</span>,
     xlab = <span class="string">"CUNR"</span>, ylab = <span class="string">"Standardized Residuals"</span>,
     pch = 16, col = <span class="fn">ifelse</span>(<span class="fn">abs</span>(period2$Std_Resid) > 2, <span class="string">"blue"</span>, <span class="string">"black"</span>))
<span class="fn">abline</span>(h = 0, col = <span class="string">"gray"</span>, lty = 2)
<span class="fn">abline</span>(h = <span class="fn"c</span>(-2, 2), col = <span class="string">"blue"</span>, lty = 3)
<span class="fn">text</span>(period2$CUNR[<span class="fn">abs</span>(period2$Std_Resid) > 2],
     period2$Std_Resid[<span class="fn">abs</span>(period2$Std_Resid) > 2],
     labels = period2$Year[<span class="fn">abs</span>(period2$Std_Resid) > 2],
     pos = 3, cex = 0.8)


<span class="comment"># Calculate Cook's Distance and Threshold to Plot on a Scatterplot (1980-2008)</span>
period1$Cooks &lt;- <span class="fn">cooks.distance</span>(period1_model)
thresh1 &lt;- 4 / <span class="fn">nrow</span>(period1)

<span class="fn">plot</span>(period1$Year, period1$Cooks,
     main = <span class="string">"Cook's Distance: 1980-2008"</span>,
     xlab = <span class="string">"Year"</span>, ylab = <span class="string">"Cook's Distance"</span>,
     pch = 16, col = <span class="fn">ifelse</span>(period1$Cooks > thresh1, <span class="string">"red"</span>, <span class="string">"black"</span>))
<span class="fn">abline</span>(h = thresh1, col = <span class="string">"red"</span>, lty = 2)
<span class="fn">text</span>(period1$Year[period1$Cooks > thresh1],
     period1$Cooks[period1$Cooks > thresh1],
     labels = period1$Year[period1$Cooks > thresh1],
     pos = 3, cex = 0.8)

<span class="comment"># Calculate Cook's Distance and Threshold to Plot on a Scatterplot (2009-2025)</span>
period2$Cooks &lt;- <span class="fn">cooks.distance</span>(period2_model)
thresh2 &lt;- 4 / <span class="fn">nrow</span>(period2)

<span class="fn">plot</span>(period2$Year, period2$Cooks,
     main = <span class="string">"Cook's Distance: 2009-2025"</span>,
     xlab = <span class="string">"Year"</span>, ylab = <span class="string">"Cook's Distance"</span>,
     pch = 16, col = <span class="fn">ifelse</span>(period2$Cooks > thresh2, <span class="string">"blue"</span>, <span class="string">"black"</span>))
<span class="fn">abline</span>(h = thresh2, col = <span class="string">"blue"</span>, lty = 2)
<span class="fn">text</span>(period2$Year[period2$Cooks > thresh2],
     period2$Cooks[period2$Cooks > thresh2],
     labels = period2$Year[period2$Cooks > thresh2],
     pos = 3, cex = 0.8)</pre>
        <img src="/images/employment_std_resid_scatterplot_period1.png" alt="Standardized Residuals from 1980-2008" style="width:100%; border-radius:6px; margin-top:0.75rem;">
        <img src="/images/employment_std_resid_scatterplot_period2.png" alt="Standardized Residuals from 2009-2025" style="width:100%; border-radius:6px; margin-top:0.75rem;">
        <img src="/images/employment_cooks_scatterplot_period1.png" alt="Standardized Residuals from 1980-2008" style="width:100%; border-radius:6px; margin-top:0.75rem;">
        <img src="/images/employment_cooks_scatterplot_period2.png" alt="Standardized Residuals from 2009-2025" style="width:100%; border-radius:6px; margin-top:0.75rem;">
      <p>The residual analyses have been computed to identify potential outliers. In the 1980-2008 model, standardized residuals greater than |2| were observed in 1980, which indicates that year being a potential bivariate outlier. Cook’s identified 1983 as influential. These were likely due to the recessions in the United States during that time period. Meanwhile, in the 2009-2025 model, standardized residuals greater than |2| were observed in 2009 and 2021, which indicates those years being potential bivariate outliers. Cook’s identified 2009 as influential. The observation made in 2009 is most likely due to the Great Recession. Standardized residuals identify observations with large prediction errors while Cook’s measures overall influence on the regression line. As a result, an observation may have a large residual but not strongly influence the slope and vice versa.
</p>
    </div>
  </div>

</div>

---

<div class="section-block"><h2>Results</h2></div>

<div class="stats-grid">
  <div class="stat-card">
    <span class="stat-value">CLFPR = 69.66 - 0.62 CUNR</span>
    <span class="stat-label">1980-2008</span>
  </div>
  
  <div class="stat-card">
    <span class="stat-value">p &lt; 0.001</span>
    <span class="stat-label">Statistically Significant</span>
  <div class="stat-card">
    <span class="stat-value">R2 = 0.61</span>
    <span class="stat-label">approximately 61% of the variation in labor force participation is explained by unemployment</span>
  </div>
</div>

<div class="finding-box">
  <h4>1980-2008: Supports Discouraged Worker Effect</h4>
  <p>From the period of 1980-2008, the discouraged worker effect is supported because higher unemployment rates tended to correspond with lower labor force participation rates.
</p>
</div>


<div class="stats-grid">
  <div class="stat-card">
    <span class="stat-value">CLFPR = 61.28 + 0.33 CUNR</span>
    <span class="stat-label">2009-2025</span>
  </div>
  
  <div class="stat-card">
    <span class="stat-value">p = 0.003</span>
    <span class="stat-label">Statistically Significant</span>
  <div class="stat-card">
    <span class="stat-value">R2 = 0.42</span>
    <span class="stat-label">approximately 42% of the variation in labor force participation is explained by unemployment</span>
  </div>
</div>

<div class="finding-box">
  <h4>2009-2025: Supports Added Worker Effect</h4>
  <p>From the period of 2009-2025, the added worker effect is supported because higher unemployment rates tended to correspond with higher labor force participation rates.
</p>
</div>

---

<div class="section-block"><h2>Summary</h2></div>

In conclusion, the relationship between unemployment and labor force participation **changed** across the two time periods, each supporting a different theory. No statistically significant linear relationship was found when analyzing over the whole period of 1980-2025. However, after dividing it into two time periods, two different relationships emerged from the variables, with the **earlier** period corresponding to a **negative** correlation while the **later** period corresponded to a **positive** correlation.

---
