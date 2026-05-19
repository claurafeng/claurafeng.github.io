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
     col =<span class="string">"red"</span>)
     </pre>
     <img src="/images/employment_clfpr_summary.png" alt="Summary of CLFPR" style="width:100%; border-radius:6px; margin-top:0.75rem;">
      <img src="/images/employment_clfpr_histogram.png" alt="Histogram of CLFPR" style="width:100%; border-radius:6px; margin-top:0.75rem;">
      <p>The graph shows the relationship between the charities’ overall rating and accountability & transparency score. There is no simple curve that gives the points a better fit, meaning that a linear model is appropriate. The graph shows a strong, positive correlation. Thus, charities with relatively high accountability & transparency scores tend to have higher overall ratings as well.
</p>
    </div>
  </div>

  <div class="step">
    <div class="step-num">3</div>
    <div class="step-content">
      <h4>Scatterplot: Overall Score vs. Audited Financial Statements</h4>
      <p>For the binary AF variable, the x-axis labels are converted from 0/1 to "No"/"Yes" for clarity.</p>
      <pre><span class="comment"># Convert AF to a labeled factor</span>
charities$AF_label &lt;- <span class="fn">factor</span>(charities$AF,
                            levels = <span class="fn">c</span>(0, 1),
                            labels = <span class="fn">c</span>(<span class="string">"No"</span>, <span class="string">"Yes"</span>))

<span class="comment"># Scatterplot: OS vs AF with labeled axis</span>
charities_af_plot &lt;- <span class="fn">ggplot</span>(charities, <span class="fn">aes</span>(x = AF_label, y = OS)) +
<span class="fn">geom_point</span>(color = "blue", alpha = 0.7) +
<span class="fn">labs</span>(title = <span class="string">"Relationship Between Overall Score and Audited Financial Statement Provision"</span>, x = <span class="string">"Audited Financial Statement Provision"</span>, y = <span class="string">"Overall Score"</span>) +
<span class="fn">theme_minimal</span>()
<span class="fn">print</span>(charities_af_plot)     
</pre>
      <img src="/images/charities_af_plot.png" alt="Scatterplot of Overall Score vs AF" style="width:100%; border-radius:6px; margin-top:0.75rem;">
      <p>The graph shows the relationship between the charities’ overall rating and whether they provided the audited financial statement on their website. Since no simple curves can be discerned from the scatterplot, a linear model is appropriate. The center of the line representing charities that provide audited financial statements on their websites seems to be higher than the center of the line of charities that do not provide them. This moderately indicates that charities with audited financial statements accessible on their website tend to have higher overall ratings as well, suggesting a positive correlation between the two.
</p>
    </div>
  </div>

  <div class="step">
    <div class="step-num">4</div>
    <div class="step-content">
      <h4>Correlation test: OS and ATS</h4>
      <p>Run a Pearson correlation to get the r statistic and p-value for the OS–ATS relationship.</p>
      <pre><span class="comment"># Pearson correlation: OS vs ATS</span>
<span class="fn">cor.test</span>(charities$OS, charities$ATS, method = <span class="string">"pearson"</span>)</pre>
    </div>
  </div>

  <div class="step">
    <div class="step-num">5</div>
    <div class="step-content">
      <h4>Correlation test: OS and AF</h4>
      <p>Run a Pearson correlation to get the r statistic and p-value for the OS–AF relationship.</p>
      <pre><span class="comment"># Pearson correlation: OS vs AF</span>
<span class="fn">cor.test</span>(charities$OS, charities$AF, method = <span class="string">"pearson"</span>)</pre>
    </div>
  </div>

</div>

---

<div class="section-block"><h2>Results</h2></div>

<div class="stats-grid">
  <div class="stat-card">
    <span class="stat-value">r = 0.707</span>
    <span class="stat-label">OS × ATS Correlation</span>
  </div>
  <div class="stat-card">
    <span class="stat-value">p &lt; 2.2e-16</span>
    <span class="stat-label">OS × ATS p-value</span>
  </div>
</div>

<div class="finding-box">
  <h4>Overall Score & Accountability / Transparency Score</h4>
  <p>The correlation statistic and p-value suggest that the relationship between the charities’ overall rating and accountability & transparency score has a strong positive correlation and is statistically significant. The p-value (less than 2.2e-16) is less than 0.05, indicating that the relationship is statistically significant. This means that the correlation is likely not due to random chance. The correlation (r), which is 0.707, is greater than 0.5, which means that there is a strong positive correlation between the two variables. The statistically significant, strongly positive correlation suggests that charities with higher accountability & transparency scores tend to also have higher overall ratings.
</p>
</div>

<div class="stats-grid">
  <div class="stat-card">
    <span class="stat-value">r = 0.421</span>
    <span class="stat-label">OS × AF Correlation</span>
  </div>
  <div class="stat-card">
    <span class="stat-value">p = 3.55e-14</span>
    <span class="stat-label">OS × AF p-value</span>
  </div>
  </div>

<div class="finding-box green">
  <h4>Overall Score & Audited Financial Statements</h4>
  <p>The correlation statistic for the relationship between the charities’ overall rating and whether they provided the audited financial statement on their website indicates a statistically significant, moderately positive correlation between the two. The p-value (3.546e-14) is less than 0.05, indicating that the relationship is statistically significant. This means that the correlation is likely not due to random chance. The correlation (r), which is 0.421, is between 0.3 and 0.5, which means that there is a moderate positive correlation between the two variables. The moderately positive, statistically significant correlation between the charities’ overall rating and audited financial statement provision shows that charities that provide an audited financial statement on their website tend to have higher overall scores.
</p>
</div>

---

<div class="section-block"><h2>Summary</h2></div>

To sum up the findings, charities perceived to be more transparent with their operations (through their accountability & transparency scores and accessibility of their audited financial statement on their website) tend to have a **higher** overall score as well. Although both are positively correlated, the correlation between the charities’ overall rating and accountability & transparency score is **stronger** than the correlation between their overall rating and whether they provided the financial statements on their website.

---
