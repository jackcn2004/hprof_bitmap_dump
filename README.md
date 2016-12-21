# Android HPROF Bitmap Dump

This small utility helps to investigate memory usage problems in Android applications. It parses Java heap dump files (hprof), extraxts bitmap from them and saves bitmaps as PNG files in current directory. Looking at produced bitmap images you can get some insights about how bitmaps in your application use memory.

Pre-built JAR file (Java 8): https://github.com/dtrounine/hprof_bitmap_dump/releases/download/v0.0.0/hprof_bitmap_dump.jar

# Usage

1. Get HPROF file from a running application and save it on disk

2. Convert the obtained HPROF file using hprof-conv from Android SDK

3. Run from command line: 
   
   java -jar hprof_bitmap_dump.jar <converted_hprof_file>
   
   It will generate PNG files in current directory, one for every android.graphics.Bitmap instance in the heap dump.
   
   
