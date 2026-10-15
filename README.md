
[README (2).md](https://github.com/user-attachments/files/33494199/README.2.md)
# NumPy Sales Data Filter & Report Engine

A query and reporting engine built **only with NumPy** that simulates one year of sales for 10 stores and filters/reports on it.

## Problem
Given a (stores x months) sales matrix, answer questions like: *Which months beat the growth target? Which stores are below average? What were the best months for stores 2, 5 and 8?*

## Approach
| Step | NumPy features |
|------|----------------|
| Data creation | `np.arange`, `np.random.randint`, `reshape` |
| Quarter / store slicing | 2D slicing, negative indices |
| Growth targets | `np.linspace`, broadcasting |
| Filtering | boolean masks with `&`, `\|`, `~` |
| Selection | fancy indexing, `np.ix_`, `np.argsort` |
| Reporting | `sum`, `mean`, `argmax`, `np.where` |

## Run it
**Colab:** open `sales_report_engine.ipynb` in Google Colab and click *Runtime > Run all*.
(Add your badge: `[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](YOUR_COLAB_LINK)`)

**Locally:**
```bash
pip install -r requirements.txt
jupyter notebook sales_report_engine.ipynb
```

## Sample query
```python
query(store_ids=[1, 4, 7], month_nums=[1, 2, 3], min_sales=500)
```

## Output
![report](sales_report.png)

## Future work
Load real CSV data with `np.genfromtxt`, add a product dimension (3D array), year-over-year growth.

## Author
Your Name | [LinkedIn](#) | [GitHub](#)
