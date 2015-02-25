# multiplication_table.rb
#multiplication table
 def multiplication_table( max, heading, decorate )
 
+  puts max
   max2 = ( max ).to_s.length
 #  puts max2
 
   puts heading.to_s
 
   if decorate == true
-
-  for column in 1..(max.to_i)
+    for column in 1..(max.to_i)
       maxcolumn = max*column
-
+      print '=' #*
       column_s = maxcolumn.to_s.length
-
       print '='*(column_s)
-      print '='
     end
+    print '=' #+
   end
-  print '='
   puts
 
   for row in 1..max.to_i
           print " "
 #        end
 
+    max_s = 1
+    maxcolumn_s = 1
     for column in 1..max.to_i
-      if ( (max).to_s.length == 1 ) && ((max*column).to_s.length == 1)
-
+#    for max_s in 1..2
+      if ( (max).to_s.length == max_s ) && ((max*column).to_s.length == 1 )
         print "%1d" %  (row * column)
-      end
-
-      if ( (max).to_s.length == 1 ) && ((max*column).to_s.length == 2)
-        print "%2d" %  (row * column)
-      end
-      if ( (max).to_s.length == 2 ) && ((max*column).to_s.length == 2)
+      elsif
+        ( (max).to_s.length == max_s) && ((max*column).to_s.length == 2 )
         print "%2d" %  (row * column)
       end
 
-      if ( (max).to_s.length == 2 ) && ((max*column).to_s.length == 3)
+      if ( (max).to_s.length == (max_s+1) ) && ((max*column).to_s.length == 2 )
+        print "%2d" %  (row * column)
+      elsif ( (max).to_s.length == (max_s+1)) && ((max*column).to_s.length == 3 )
         print "%3d" %  (row * column)
-      end
-       if ( (max).to_s.length == 2 ) && ((max*column).to_s.length == 4)
+      elsif ( (max).to_s.length == (max_s+1)) && ((max*column).to_s.length == 4)
         print "%4d" %  (row * column)
       end
       print " "
     end
+#=end
     puts
   end
 
 multiplication_table (integer, heading = '', decorate = false)
 returns a string object.
 =end 
-table1 = multiplication_table 40, 'Times Table to 40', true
+table1 = multiplication_table 32, 'Times Table to 1', true
 table2 = multiplication_table 9, '', true
+table3 = multiplication_table 20, '', true
+table4 = multiplication_table 32, '', true
 
 puts table1
 puts
 puts table2
+puts
+puts table3
+puts
+puts table4
+puts
+
