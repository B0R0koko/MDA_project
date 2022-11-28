<h2>CEO Characteristics and firm perfomance: evidence from Fortune 1000 companies</h2>
<h3>Goals</h3>
<ul>
    <li>Find patterns in CEO dataset and determine how CEO's characteristics affect company's performance</li>
    <li>Cluster CEOs into groups based on their prior work experience</li>
    <li>Study how CEOs differ in various sectors</li>
</ul>
<h3>Team: Milton Friedman</h3>
<ol>
    <li>Mikhail Mironov</li>
    <li>Vera Garmanova</li>
</ol>

<h3>About dataset</h3>
<p>Initially our dataset has been inspired by kaggle <a href="https://www.kaggle.com/datasets/winston56/fortune-500-data-2021">Fortune 1000 companies dataset</a>. It has some financial data on the companies such as profits, revenue, ticker (if company is publically traded) and some basic information on CEO of the company such as name and some other descriptive dummy variables. We decided to expand on this data, so we handcrafted our dataset with additional data on CEOs as we wanted to study them more closely. We used primarily Python for both data collection and analysis, some analysis has been done in R, since there is simply no implementation of some algorithms in Python.</p>

<h4>Data Collection techniques applied to the project</h4>
<ul>
    <li>Data on CEOs experience has been collected from LinkedIn profiles using Selenium</li>
    <li>Other data on age and salaries of CEOs has been collected from MorningStar using requests library</li>
</ul>

<h4>Data analysis techniques applied</h4>
<ul>
    <li>Principal Component Dimension reduction for plotting clusters and analysis with correlations</li>
    <li>Multidimensional Scaling using various distances: mainly focused on Euclidean and Manhattan</li>
    <li>Hierarchical clustering with various distances using scipy implementation</li>
    <li>Scree plot of distance between merged clusters to find optimal number of clusters for Hierarchical clustering</li>
    <li>Bootstrapping of Hierarchical clustering using pvclust module from R to check cluster stability</li>
    <li>Applying Euclidean KMeans with various linkage methods, mainly we focused on Ward and Complete</li>
    <li>WSS Scree plot and Calinski-Harabasz statistic to find optimal number of clusters</li>
    <li>Additionally we have applied Silhouette Analysis to study the separation distance between the resulting clusters</li>
    <li>After obtaining promising results from Manhattan Hierarchical clustering we went for KMeans with Manhattan distances as well</li>
    <li>Bootstrapping Kmeans to see how often KMeans assigns datapoints to same clusters</li>
</ul>
