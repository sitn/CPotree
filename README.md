# CPotree
 
# write output to stdout
.\PotreeElevationProfile.exe "D:/dev/pointclouds/converted/CA13/cloud.js" ^
 --coordinates "{693550.968, 3915914.169},{693890.618, 3916387.819},{694584.820, 3916458.180},{694786.239, 3916307.199}" ^
 --width 14.0 --min-level 0 --max-level 3 ^
 --stdout  
 
# write output to "result.las"
.\PotreeElevationProfile.exe "D:/dev/pointclouds/converted/CA13/cloud.js" ^
 --coordinates "{693550.968, 3915914.169},{693890.618, 3916387.819},{694584.820, 3916458.180},{694786.239, 3916307.199}" ^
 --width 14.0 --min-level 0 --max-level 3 ^
 -o result.las
 
# write output to "result.potree"
.\PotreeElevationProfile.exe "D:/dev/pointclouds/converted/CA13/cloud.js" ^
 --coordinates "{693550.968, 3915914.169},{693890.618, 3916387.819},{694584.820, 3916458.180},{694786.239, 3916307.199}" ^
 --width 14.0 --min-level 0 --max-level 3 ^
 -o result.potree
 
# only write POSITION_CARTESIAN and INTENSITY attributes to the output
.\PotreeElevationProfile.exe "D:/dev/pointclouds/converted/CA13/cloud.js" ^
 --coordinates "{693550.968, 3915914.169},{693890.618, 3916387.819},{694584.820, 3916458.180},{694786.239, 3916307.199}" ^
 --width 14.0 --min-level 0 --max-level 3 ^
 --stdout --output-attributes POSITION_CARTESIAN RGB

 

.\PotreeExtractRegion.exe ^
 "D:/dev/pointclouds/converted/CA13/cloud.js" ^
 --box "169.1, 0, 0, 0, 0, 169.1, 0, 0, 0, 0, 269.95, 0, 694704.38, 3916411, 17.9, 1" ^
 --min-level 0 ^
 --max-level 8 ^
 -o result.las
 
 
--output-format			POTREE, LAS, CSV
						default: POTREE
	
--output-attributes		POSITION_CARTESIAN, POSITION_PROJECTED_PROFILE, COLOR_PACKED, RGB, RGBA, INTENSITY, CLASSIFICATION		
						default: same as input point cloud + POSITION_PROJECTED_PROFILE
						
--stdout <format>		Write the result to stdout in the given file format.
						<format>: POTREE, LAS, CSV
	
-o <file>				Write the result to the specified file. Supported file types are .potree, .las and .csv
						default: no file
					
--estimate-workload		Instead of points, return an estimation of how many nodes and points will have to be processed.

--width					Width of the profile

--coordinates			Vertices of the polyline, specified as "{x1,y1},{x2,y2},..."

--min-level				The result will contain points starting from this level 

--max-level				The result will contain points up to this level










 

