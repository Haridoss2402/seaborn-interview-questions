# seaborn-interview-questions

### seaborn 

🔵 1. What is Seaborn?

Definition:
A high-level Python data visualization library built on Matplotlib, mainly for statistical graphics.

Example:
import seaborn as sns

🔵 2. Why use Seaborn instead of Matplotlib?

Definition:
Seaborn provides more beautiful, easier, and statistical plots by default.

Example (Matplotlib vs Seaborn):
sns.set_theme()
sns.lineplot(x=[1,2,3], y=[4,5,6])

🔵 3. What is sns.load_dataset()?

Definition:
Loads built-in demonstration datasets.

Example:
df = sns.load_dataset("tips")
df.head()

🔵 4. What are Seaborn styles?

Definition:
Themes for default plot appearance like darkgrid, whitegrid.

Example:
sns.set_style("darkgrid")

🔵 5. What is sns.set_theme()?

Definition:
Applies the default theme for all plots.

Example:
sns.set_theme(style="whitegrid")

🔵 6. What is a Pairplot?

Definition:
Shows pairwise relationships among multiple variables.

Example:
df = sns.load_dataset("iris")
sns.pairplot(df, hue="species")

🔵 7. What is a Jointplot?

Definition:
Shows bivariate relationship + univariate distributions.

Example:
sns.jointplot(x="total_bill", y="tip", data=sns.load_dataset("tips"))

🔵 8. What is a Heatmap?

Definition:
Visualizes matrix or correlation values using colors.

Example:
df = sns.load_dataset("iris")
sns.heatmap(df.corr(), annot=True, cmap="coolwarm")

🔵 9. What is a Countplot?

Definition:
Shows the count of each category.

Example:
sns.countplot(x="day", data=sns.load_dataset("tips"))

🔵 10. What is a Boxplot?

Definition:
Shows distribution, median, quartiles, and outliers.

Example:
sns.boxplot(x="day", y="total_bill", data=sns.load_dataset("tips"))

🔵 11. What is a Violin Plot?

Definition:
Shows distribution + KDE + quartiles.

Example:
sns.violinplot(x="day", y="total_bill", data=sns.load_dataset("tips"))

🔵 12. What is a KDE Plot?

Definition:
Shows smoothed probability density.

Example:
sns.kdeplot(data=sns.load_dataset("iris")["sepal_length"])

🔵 13. What is a Barplot?

Definition:
Shows mean or aggregated value for each category.

Example:
sns.barplot(x="day", y="total_bill", data=sns.load_dataset("tips"))

🔵 14. What is a Lineplot?

Definition:
Shows trends over continuous values or time.

Example:
sns.lineplot(x="size", y="total_bill", data=sns.load_dataset("tips"))

🔵 15. Difference between Countplot and Barplot?

Definition:

countplot → counts of categories

barplot → aggregated values (mean, median, etc.)

Example:
sns.countplot(x="sex", data=df)     # frequency
sns.barplot(x="sex", y="tip", data=df)  # mean tip by sex

🔵 16. What is hue in Seaborn?

Definition:
Adds color grouping based on a categorical variable.

Example:
sns.scatterplot(x="total_bill", y="tip", hue="time", data=sns.load_dataset("tips"))

🔵 17. What is palette?

Definition:
Color scheme for the plot.

Example:
sns.countplot(x="day", data=df, palette="coolwarm")

🔵 18. What is sns.relplot()?

Definition:
A figure-level function for relational plots (scatter & line).

Example:
sns.relplot(x="total_bill", y="tip", data=df)

🔵 19. What is sns.catplot()?

Definition:
A figure-level function for categorical plots (box, violin, bar, count).

Example:
sns.catplot(x="day", y="total_bill", kind="box", data=df)

🔵 20. What is FacetGrid?

Definition:
Creates separate subplots for subsets of data.

Example:
g = sns.FacetGrid(df, col="day")
g.map(sns.scatterplot, "total_bill", "tip")

🔵 21. What is swarmplot?

Definition:
Categorical scatterplot where points do not overlap.

Example:
sns.swarmplot(x="day", y="total_bill", data=df)

🔵 22. What is stripplot?

Definition:
Categorical scatter plot with overlapping points.

Example:
sns.stripplot(x="day", y="total_bill", data=df)

🔵 23. What is lmplot?

Definition:
Scatter plot + linear regression line.

Example:
sns.lmplot(x="total_bill", y="tip", data=df)

🔵 24. What is displot()?

Definition:
Figure-level distribution plot (hist, KDE).

Example:
sns.displot(df["total_bill"], kde=True)

🔵 25. What is the difference between figure-level and axis-level functions?

Definition:

Figure-level: creates a new figure (e.g., relplot, displot, catplot).

Axis-level: draws inside one axis (e.g., scatterplot, boxplot).

Example:
sns.scatterplot(x="tip", y="total_bill", data=df)  # axis-level
sns.relplot(x="tip", y="total_bill", data=df)       # figure-level

🔵 26. What is ci in Seaborn?

Definition:
Confidence interval shown on barplot/lineplot.

Example:
sns.lineplot(x="size", y="tip", data=df, ci=95)

🔵 27. What is dodge?

Definition:
Separates overlapping bars or points for different hue categories.

Example:
sns.barplot(x="day", y="total_bill", hue="sex", data=df, dodge=True)

🔵 28. What is aspect and height?

Definition:
Controls the size and shape of figure-level plots.

Example:
sns.catplot(x="day", y="total_bill", data=df, height=5, aspect=1.5)

🔵 29. What is a Regression Plot?

Definition:
A plot that shows the relationship between variables with a fitted regression line.

Example:
sns.regplot(x="total_bill", y="tip", data=df)

🔵 30. What is sns.corrplot()?

Definition:
Older function used for correlation visualization (now replaced by heatmap).
