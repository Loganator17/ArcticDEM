gdalwarp -t_srs 'EPSG:4326' SETSM_WV01_20160331_102001004E1B7F00_102001004ECD0F00_seg1_2m_v3.0_dem.tif small.tif
gdal_translate -of GMT small.tif dem2.grd
gmt grdcut dem2.grd -R-16.9/-16.51777/64.77/65 -Gdem2cut.grd
