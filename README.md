<h1  align=center><font  size = 6>Predicting Solar Flares and Flare Area Classes</font></h1>

<br>

<h2>Statement</h2>

The purpose of this study is based on the available data, it was estimated numbers of the <i>solar flares</i> production in spesific region on sun in the following <i>24 hours (with classes)</i>. I made <i>multi-output neural network model</i> for the predict dependent variables. Accuracy can change due to parameters. Please let me know the best parameters.  You can run, modify and download your own model from codes. Accuracy can change due to parameters. Please let me know the best parameters.</p>

<br>  

<h2>Keywords</h2>

<ul>
	<li>Multi-Output</li>
	<li>Neural Networks</li>
	<li>Space</li>
	<li>Sun</li>
	<li>Classification</li>
	<li>Deep Learning</li>
</ul>  

<br>

<b>Attribute Information:</b>

<ol>
	<li>Code for class (modified Zurich class) (A,B,C,D,E,F,H)</li>
	<li>Code for largest spot size (X,R,S,A,H,K)</li>
	<li>Code for spot distribution (X,O,I,C)</li>  
	<li>Activity (1 = reduced, 2 = unchanged)</li>  
	<li>Evolution (1 = decay, 2 = no growth, 3 = growth)</li>  
	<li>Previous 24 hour flare activity code (1 = nothing as big as an M1, 2 = one M1, 3 = more activity than one M1)</li>  
	<li>Historically-complex (1 = Yes, 2 = No)</li>  
	<li>Did region become historically complex on this pass across the sun's disk (1 = yes, 2 = no)</li>  
	<li>Area (1 = small, 2 = large)</li>  
	<li>Area of the largest spot (1 = <=5, 2 = >5)</li>  
</ol>


<b>From all these predictors three classes of flares are predicted, which are represented in the last three columns.</b>  

11. <i>C-class flares</i> production by this region in the following 24 hours (common flares)
12. <i>M-class flares</i> production by this region in the following 24 hours (moderate flares)
13. <i>X-class flares</i> production by this region in the following 24 hours (severe flares)

<br>

<br>

<h2>Predicting Number of the Flares in Region (with Class)</h2>

<div align="center">
	<img width=700  height=700 src="https://raw.githubusercontent.com/doguilmak/Predicting-Solar-Flares-with-XGBoost-and-ANN/main/assets/model.png">
</div>

<br>

<p>Every class has different <i>dense layer</i> before the <i>output layer</i>. <code>c_output</code> has <i>32</i>, <code>m_output</code> has <i>64</i> and <code>x_output</code> has <i>16</i> neurons. <code>c_output</code> be retrived directly from <code>dense_3</code>, <code>m_output</code> be retrived directly from <code>dense_4</code> and <code>x_output</code> be retrived directly from <code>dense_5</code>.</p>

<br>

<h2>Predicting Flare Classes</h2>

| C Class Flares Model Accuracy | M Class Flares Model Accuracy | X Class Flares Model Accuracy |
|--|--|--|
| <img src="https://raw.githubusercontent.com/doguilmak/Predicting-Solar-Flares-with-XGBoost-and-ANN/main/assets/C-Class_flares_model_accuracy.png"> | <img src="https://raw.githubusercontent.com/doguilmak/Predicting-Solar-Flares-with-XGBoost-and-ANN/main/assets/M-Class_flares_model_accuracy.png"> | <img src="https://raw.githubusercontent.com/doguilmak/Predicting-Solar-Flares-with-XGBoost-and-ANN/main/assets/X-Class_flares_model_accuracy.png"> |
| XGBoost Accuracy score: 0.897196261682243 | XGBoost Accuracy score: 0.8785046728971962 | XGBoost Accuracy score: 0.9906542056074766 | 

<br>

