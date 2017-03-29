
<h1> Jie-Kai Yang </h1>
<h1>Scene recognition with bag of words<br>

<h2>Brief</h2> 
<p> 
</p><ul> 

  <li>  download <a href="http://www.vlfeat.org/download.html">VLFeat 0.9.17 binary package</a></li> 
  <li>VL Feat Matlab reference: <a href="http://www.vlfeat.org/matlab/matlab.html">http://www.vlfeat.org/matlab/matlab.html</a> 
  <li>Required files: </li>
  <li> README </li>
  <li>code/ - directory containing all your code for this assignment</li>	
  <li>html/ - directory containing all your html report for this assignment, including images</li>
  <li>html/index.html - home page for your results</li>	
</ul>
<p></p> 
 
<h2>Overview</h2> 
<p> 
The goal of this project is to introduce you to image recognition. Specifically, we will examine the task of scene recognition starting with very simple methods -- tiny images and nearest neighbor classification -- and then move on to techniques that resemble the state-of-the-art -- bags of quantized local features and linear classifiers learned by support vector machines.
</p>

</p><center><img src="./README_files/categories.png">
<p style="color: #666;">Example scenes from of each category in the 15 scene dataset. Figure from <a href="http://www.di.ens.fr/willow/pdfs/cvpr06b.pdf">Lazebnik et al. 2006</a>.</p></center><p></p>

<h2>Results</h2>

<ul>
 <li>Tiny images representation and nearest neighbor classifier (Accuracy (mean of diagonal of confusion matrix) is 0.199).</li>
 <li>Bag of SIFT representation and nearest neighbor classifier (when K=1, Accuracy is 41.5%).</li>
 <li>Bag of SIFT representation and linear SVM classifier (accuracy of 58.7%).</li>
</ul>
<p><center><img src="./README_files/file.png"></p>
<p><center><img src="./README_files/file2.png"></p>
<p style="color: #666;">Bag of SIFT representation with Machine learning algorithm (last one is 1 vs all SVM) </p>
<p style="color: #666;"> 5 fold cross-validation result </p>

<p><center><img src="./README_files/file3.png"></p>

<p><center><img src="./README_files/confusion_matrix.png"></p>


<table border=0 cellpadding=4 cellspacing=1>
<tr>
<th>Category name</th>
<th>Accuracy</th>
<th colspan=2>Sample training images</th>
<th colspan=2>Sample true positives</th>
<th colspan=2>False positives with true label</th>
<th colspan=2>False negatives with wrong predicted label</th>
</tr>
<tr>
<td>Kitchen</td>
<td>0.450</td>
<td bgcolor=LightBlue><img src="./thumbnails/Kitchen_image_0078.jpg" width=100 height=75></td>
<td bgcolor=LightBlue><img src="./thumbnails/Kitchen_image_0181.jpg" width=57 height=75></td>
<td bgcolor=LightGreen><img src="thumbnails/Kitchen_image_0071.jpg" width=100 height=75></td>
<td bgcolor=LightGreen><img src="thumbnails/Kitchen_image_0024.jpg" width=57 height=75></td>
<td bgcolor=LightCoral><img src="thumbnails/Street_image_0016.jpg" width=75 height=75><br><small>Street</small></td>
<td bgcolor=LightCoral><img src="thumbnails/Office_image_0126.jpg" width=108 height=75><br><small>Office</small></td>
<td bgcolor=#FFBB55><img src="thumbnails/Kitchen_image_0170.jpg" width=100 height=75><br><small>LivingRoom</small></td>
<td bgcolor=#FFBB55><img src="thumbnails/Kitchen_image_0031.jpg" width=57 height=75><br><small>InsideCity</small></td>
</tr>
<tr>
<td>Store</td>
<td>0.510</td>
<td bgcolor=LightBlue><img src="thumbnails/Store_image_0069.jpg" width=57 height=75></td>
<td bgcolor=LightBlue><img src="thumbnails/Store_image_0006.jpg" width=100 height=75></td>
<td bgcolor=LightGreen><img src="thumbnails/Store_image_0063.jpg" width=57 height=75></td>
<td bgcolor=LightGreen><img src="thumbnails/Store_image_0025.jpg" width=113 height=75></td>
<td bgcolor=LightCoral><img src="thumbnails/TallBuilding_image_0028.jpg" width=75 height=75><br><small>TallBuilding</small></td>
<td bgcolor=LightCoral><img src="thumbnails/InsideCity_image_0038.jpg" width=75 height=75><br><small>InsideCity</small></td>
<td bgcolor=#FFBB55><img src="thumbnails/Store_image_0106.jpg" width=85 height=75><br><small>Forest</small></td>
<td bgcolor=#FFBB55><img src="thumbnails/Store_image_0053.jpg" width=57 height=75><br><small>Street</small></td>
</tr>
<tr>
<td>Bedroom</td>
<td>0.320</td>
<td bgcolor=LightBlue><img src="thumbnails/Bedroom_image_0145.jpg" width=102 height=75></td>
<td bgcolor=LightBlue><img src="thumbnails/Bedroom_image_0111.jpg" width=116 height=75></td>
<td bgcolor=LightGreen><img src="thumbnails/Bedroom_image_0074.jpg" width=116 height=75></td>
<td bgcolor=LightGreen><img src="thumbnails/Bedroom_image_0035.jpg" width=115 height=75></td>
<td bgcolor=LightCoral><img src="thumbnails/LivingRoom_image_0056.jpg" width=112 height=75><br><small>LivingRoom</small></td>
<td bgcolor=LightCoral><img src="thumbnails/LivingRoom_image_0002.jpg" width=100 height=75><br><small>LivingRoom</small></td>
<td bgcolor=#FFBB55><img src="thumbnails/Bedroom_image_0081.jpg" width=107 height=75><br><small>LivingRoom</small></td>
<td bgcolor=#FFBB55><img src="thumbnails/Bedroom_image_0011.jpg" width=101 height=75><br><small>Kitchen</small></td>
</tr>
<tr>
<td>LivingRoom</td>
<td>0.210</td>
<td bgcolor=LightBlue><img src="thumbnails/LivingRoom_image_0269.jpg" width=100 height=75></td>
<td bgcolor=LightBlue><img src="thumbnails/LivingRoom_image_0212.jpg" width=100 height=75></td>
<td bgcolor=LightGreen><img src="thumbnails/LivingRoom_image_0061.jpg" width=100 height=75></td>
<td bgcolor=LightGreen><img src="thumbnails/LivingRoom_image_0004.jpg" width=100 height=75></td>
<td bgcolor=LightCoral><img src="thumbnails/Kitchen_image_0023.jpg" width=57 height=75><br><small>Kitchen</small></td>
<td bgcolor=LightCoral><img src="thumbnails/Store_image_0118.jpg" width=77 height=75><br><small>Store</small></td>
<td bgcolor=#FFBB55><img src="thumbnails/LivingRoom_image_0112.jpg" width=113 height=75><br><small>Store</small></td>
<td bgcolor=#FFBB55><img src="thumbnails/LivingRoom_image_0101.jpg" width=101 height=75><br><small>Store</small></td>
</tr>
<tr>
<td>Office</td>
<td>0.710</td>
<td bgcolor=LightBlue><img src="thumbnails/Office_image_0073.jpg" width=117 height=75></td>
<td bgcolor=LightBlue><img src="thumbnails/Office_image_0209.jpg" width=114 height=75></td>
<td bgcolor=LightGreen><img src="thumbnails/Office_image_0005.jpg" width=126 height=75></td>
<td bgcolor=LightGreen><img src="thumbnails/Office_image_0027.jpg" width=104 height=75></td>
<td bgcolor=LightCoral><img src="thumbnails/Store_image_0057.jpg" width=100 height=75><br><small>Store</small></td>
<td bgcolor=LightCoral><img src="thumbnails/Forest_image_0037.jpg" width=75 height=75><br><small>Forest</small></td>
<td bgcolor=#FFBB55><img src="thumbnails/Office_image_0102.jpg" width=132 height=75><br><small>Kitchen</small></td>
<td bgcolor=#FFBB55><img src="thumbnails/Office_image_0183.jpg" width=109 height=75><br><small>Suburb</small></td>
</tr>
<tr>
<td>Industrial</td>
<td>0.310</td>
<td bgcolor=LightBlue><img src="thumbnails/Industrial_image_0184.jpg" width=113 height=75></td>
<td bgcolor=LightBlue><img src="thumbnails/Industrial_image_0227.jpg" width=114 height=75></td>
<td bgcolor=LightGreen><img src="thumbnails/Industrial_image_0037.jpg" width=100 height=75></td>
<td bgcolor=LightGreen><img src="thumbnails/Industrial_image_0126.jpg" width=134 height=75></td>
<td bgcolor=LightCoral><img src="thumbnails/InsideCity_image_0133.jpg" width=75 height=75><br><small>InsideCity</small></td>
<td bgcolor=LightCoral><img src="thumbnails/Coast_image_0119.jpg" width=75 height=75><br><small>Coast</small></td>
<td bgcolor=#FFBB55><img src="thumbnails/Industrial_image_0117.jpg" width=102 height=75><br><small>Highway</small></td>
<td bgcolor=#FFBB55><img src="thumbnails/Industrial_image_0083.jpg" width=106 height=75><br><small>Coast</small></td>
</tr>
<tr>
<td>Suburb</td>
<td>0.850</td>
<td bgcolor=LightBlue><img src="thumbnails/Suburb_image_0095.jpg" width=113 height=75></td>
<td bgcolor=LightBlue><img src="thumbnails/Suburb_image_0190.jpg" width=113 height=75></td>
<td bgcolor=LightGreen><img src="thumbnails/Suburb_image_0008.jpg" width=113 height=75></td>
<td bgcolor=LightGreen><img src="thumbnails/Suburb_image_0143.jpg" width=113 height=75></td>
<td bgcolor=LightCoral><img src="thumbnails/TallBuilding_image_0051.jpg" width=75 height=75><br><small>TallBuilding</small></td>
<td bgcolor=LightCoral><img src="thumbnails/Mountain_image_0075.jpg" width=75 height=75><br><small>Mountain</small></td>
<td bgcolor=#FFBB55><img src="thumbnails/Suburb_image_0004.jpg" width=113 height=75><br><small>LivingRoom</small></td>
<td bgcolor=#FFBB55><img src="thumbnails/Suburb_image_0148.jpg" width=113 height=75><br><small>LivingRoom</small></td>
</tr>
<tr>
<td>InsideCity</td>
<td>0.470</td>
<td bgcolor=LightBlue><img src="thumbnails/InsideCity_image_0261.jpg" width=75 height=75></td>
<td bgcolor=LightBlue><img src="thumbnails/InsideCity_image_0151.jpg" width=75 height=75></td>
<td bgcolor=LightGreen><img src="thumbnails/InsideCity_image_0130.jpg" width=75 height=75></td>
<td bgcolor=LightGreen><img src="thumbnails/InsideCity_image_0119.jpg" width=75 height=75></td>
<td bgcolor=LightCoral><img src="thumbnails/Street_image_0089.jpg" width=75 height=75><br><small>Street</small></td>
<td bgcolor=LightCoral><img src="thumbnails/Forest_image_0085.jpg" width=75 height=75><br><small>Forest</small></td>
<td bgcolor=#FFBB55><img src="thumbnails/InsideCity_image_0057.jpg" width=75 height=75><br><small>TallBuilding</small></td>
<td bgcolor=#FFBB55><img src="thumbnails/InsideCity_image_0043.jpg" width=75 height=75><br><small>Industrial</small></td>
</tr>
<tr>
<td>TallBuilding</td>
<td>0.660</td>
<td bgcolor=LightBlue><img src="thumbnails/TallBuilding_image_0336.jpg" width=75 height=75></td>
<td bgcolor=LightBlue><img src="thumbnails/TallBuilding_image_0243.jpg" width=75 height=75></td>
<td bgcolor=LightGreen><img src="thumbnails/TallBuilding_image_0116.jpg" width=75 height=75></td>
<td bgcolor=LightGreen><img src="thumbnails/TallBuilding_image_0113.jpg" width=75 height=75></td>
<td bgcolor=LightCoral><img src="thumbnails/Bedroom_image_0039.jpg" width=94 height=75><br><small>Bedroom</small></td>
<td bgcolor=LightCoral><img src="thumbnails/InsideCity_image_0007.jpg" width=75 height=75><br><small>InsideCity</small></td>
<td bgcolor=#FFBB55><img src="thumbnails/TallBuilding_image_0107.jpg" width=75 height=75><br><small>Street</small></td>
<td bgcolor=#FFBB55><img src="thumbnails/TallBuilding_image_0006.jpg" width=75 height=75><br><small>Bedroom</small></td>
</tr>
<tr>
<td>Street</td>
<td>0.500</td>
<td bgcolor=LightBlue><img src="thumbnails/Street_image_0117.jpg" width=75 height=75></td>
<td bgcolor=LightBlue><img src="thumbnails/Street_image_0039.jpg" width=75 height=75></td>
<td bgcolor=LightGreen><img src="thumbnails/Street_image_0010.jpg" width=75 height=75></td>
<td bgcolor=LightGreen><img src="thumbnails/Street_image_0112.jpg" width=75 height=75></td>
<td bgcolor=LightCoral><img src="thumbnails/Highway_image_0004.jpg" width=75 height=75><br><small>Highway</small></td>
<td bgcolor=LightCoral><img src="thumbnails/Highway_image_0005.jpg" width=75 height=75><br><small>Highway</small></td>
<td bgcolor=#FFBB55><img src="thumbnails/Street_image_0083.jpg" width=75 height=75><br><small>Industrial</small></td>
<td bgcolor=#FFBB55><img src="thumbnails/Street_image_0022.jpg" width=75 height=75><br><small>Industrial</small></td>
</tr>
<tr>
<td>Highway</td>
<td>0.730</td>
<td bgcolor=LightBlue><img src="thumbnails/Highway_image_0065.jpg" width=75 height=75></td>
<td bgcolor=LightBlue><img src="thumbnails/Highway_image_0181.jpg" width=75 height=75></td>
<td bgcolor=LightGreen><img src="thumbnails/Highway_image_0008.jpg" width=75 height=75></td>
<td bgcolor=LightGreen><img src="thumbnails/Highway_image_0116.jpg" width=75 height=75></td>
<td bgcolor=LightCoral><img src="thumbnails/OpenCountry_image_0061.jpg" width=75 height=75><br><small>OpenCountry</small></td>
<td bgcolor=LightCoral><img src="thumbnails/InsideCity_image_0044.jpg" width=75 height=75><br><small>InsideCity</small></td>
<td bgcolor=#FFBB55><img src="thumbnails/Highway_image_0046.jpg" width=75 height=75><br><small>Coast</small></td>
<td bgcolor=#FFBB55><img src="thumbnails/Highway_image_0032.jpg" width=75 height=75><br><small>Street</small></td>
</tr>
<tr>
<td>OpenCountry</td>
<td>0.340</td>
<td bgcolor=LightBlue><img src="thumbnails/OpenCountry_image_0020.jpg" width=75 height=75></td>
<td bgcolor=LightBlue><img src="thumbnails/OpenCountry_image_0272.jpg" width=75 height=75></td>
<td bgcolor=LightGreen><img src="thumbnails/OpenCountry_image_0059.jpg" width=75 height=75></td>
<td bgcolor=LightGreen><img src="thumbnails/OpenCountry_image_0054.jpg" width=75 height=75></td>
<td bgcolor=LightCoral><img src="thumbnails/Coast_image_0019.jpg" width=75 height=75><br><small>Coast</small></td>
<td bgcolor=LightCoral><img src="thumbnails/Mountain_image_0119.jpg" width=75 height=75><br><small>Mountain</small></td>
<td bgcolor=#FFBB55><img src="thumbnails/OpenCountry_image_0010.jpg" width=75 height=75><br><small>Kitchen</small></td>
<td bgcolor=#FFBB55><img src="thumbnails/OpenCountry_image_0018.jpg" width=75 height=75><br><small>Bedroom</small></td>
</tr>
<tr>
<td>Coast</td>
<td>0.620</td>
<td bgcolor=LightBlue><img src="thumbnails/Coast_image_0274.jpg" width=75 height=75></td>
<td bgcolor=LightBlue><img src="thumbnails/Coast_image_0159.jpg" width=75 height=75></td>
<td bgcolor=LightGreen><img src="thumbnails/Coast_image_0078.jpg" width=75 height=75></td>
<td bgcolor=LightGreen><img src="thumbnails/Coast_image_0106.jpg" width=75 height=75></td>
<td bgcolor=LightCoral><img src="thumbnails/OpenCountry_image_0006.jpg" width=75 height=75><br><small>OpenCountry</small></td>
<td bgcolor=LightCoral><img src="thumbnails/OpenCountry_image_0011.jpg" width=75 height=75><br><small>OpenCountry</small></td>
<td bgcolor=#FFBB55><img src="thumbnails/Coast_image_0093.jpg" width=75 height=75><br><small>OpenCountry</small></td>
<td bgcolor=#FFBB55><img src="thumbnails/Coast_image_0086.jpg" width=75 height=75><br><small>Mountain</small></td>
</tr>
<tr>
<td>Mountain</td>
<td>0.760</td>
<td bgcolor=LightBlue><img src="thumbnails/Mountain_image_0067.jpg" width=75 height=75></td>
<td bgcolor=LightBlue><img src="thumbnails/Mountain_image_0002.jpg" width=75 height=75></td>
<td bgcolor=LightGreen><img src="thumbnails/Mountain_image_0011.jpg" width=75 height=75></td>
<td bgcolor=LightGreen><img src="thumbnails/Mountain_image_0066.jpg" width=75 height=75></td>
<td bgcolor=LightCoral><img src="thumbnails/TallBuilding_image_0095.jpg" width=75 height=75><br><small>TallBuilding</small></td>
<td bgcolor=LightCoral><img src="thumbnails/Bedroom_image_0069.jpg" width=100 height=75><br><small>Bedroom</small></td>
<td bgcolor=#FFBB55><img src="thumbnails/Mountain_image_0105.jpg" width=75 height=75><br><small>Suburb</small></td>
<td bgcolor=#FFBB55><img src="thumbnails/Mountain_image_0108.jpg" width=75 height=75><br><small>Forest</small></td>
</tr>
<tr>
<td>Forest</td>
<td>0.870</td>
<td bgcolor=LightBlue><img src="thumbnails/Forest_image_0272.jpg" width=75 height=75></td>
<td bgcolor=LightBlue><img src="thumbnails/Forest_image_0108.jpg" width=75 height=75></td>
<td bgcolor=LightGreen><img src="thumbnails/Forest_image_0138.jpg" width=75 height=75></td>
<td bgcolor=LightGreen><img src="thumbnails/Forest_image_0078.jpg" width=75 height=75></td>
<td bgcolor=LightCoral><img src="thumbnails/OpenCountry_image_0021.jpg" width=75 height=75><br><small>OpenCountry</small></td>
<td bgcolor=LightCoral><img src="thumbnails/Mountain_image_0100.jpg" width=75 height=75><br><small>Mountain</small></td>
<td bgcolor=#FFBB55><img src="thumbnails/Forest_image_0135.jpg" width=75 height=75><br><small>Bedroom</small></td>
<td bgcolor=#FFBB55><img src="thumbnails/Forest_image_0126.jpg" width=75 height=75><br><small>OpenCountry</small></td>
</tr>
<tr>
<th>Category name</th>
<th>Accuracy</th>
<th colspan=2>Sample training images</th>
<th colspan=2>Sample true positives</th>
<th colspan=2>False positives with true label</th>
<th colspan=2>False negatives with wrong predicted label</th>
</tr>
</table>
