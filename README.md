# Home Sales Analysis 🏡📈

This project is my deep dive into analyzing home sales data using PySpark and SparkSQL. Along the way, I faced some tricky errors and learned how important it is to register tables correctly, manage cached data, and write precise queries — all valuable lessons in handling real-world datasets.

Throughout this work, I focused on answering questions like:

- What’s the average price of a 4-bedroom home sold each year?  
- How do prices vary by the year homes were built, bedrooms, bathrooms, and other features?  
- How does the “view” rating affect average home prices?

## Environment 💻

All code for this project was written and executed in Google Colab, which made it easy to work with PySpark in the cloud without needing to install anything locally. 

## About the Parquet Data and Performance 📦⚡

In this project, I also worked with the home sales data saved in Parquet format, which is a special way of storing data that optimizes how Spark reads and processes it. Parquet stores data in columns rather than rows, which helps speed up queries because Spark can read only the columns it needs instead of the whole dataset.

When I compared the runtimes:

- Parquet data query: ~0.92 seconds
- Cached temporary table query: ~0.48 seconds
- Uncached temporary view query: ~1.01 seconds

This shows that working with Parquet files was faster than querying the uncached temporary view — because Parquet’s columnar format is more efficient. However, caching the data in memory made the queries even faster, since Spark can skip reading from disk entirely.

So, using Parquet helps improve query speed, especially for repeated queries, and combining it with caching gives the best performance boost.

---

✨ Thanks for checking out my work. I’m excited to keep improving my data skills and learning new ways to analyze complex datasets! ✨

---

📊 Data provided by edX Boot Camps LLC for educational purposes.
