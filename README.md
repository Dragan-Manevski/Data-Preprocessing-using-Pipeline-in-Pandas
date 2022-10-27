-------------------------------------------------------------------------------------------------------------------------------------------------------------------
# Data Preprocessing using Pipeline in Pandas
-------------------------------------------------------------------------------------------------------------------------------------------------------------------
## Pipe function:
- a **Pandas built-in function**
- used to **combine and execute multiple functions into a single pipeline by passing the result of the previous function to the next one in the chain**
- applies **chainable functions that expect Series or DataFrames**

        pandas.DataFrame.pipe
        DataFrame.pipe(func, *args, **kwargs)
-  general **syntax**:

        final_dataset = (original_data
                        pipe(first_function, "single_column").
                        pipe(second_function, "[col1, ...colN]").
                        pipe(third_function).
                        ...
                        pipe(my_nth_function)
                        )

       where:
          - final_dateset - Final preprocessed dataset after applying all the functions
          - original_data - Raw dataset
          - pipe(first_function, "single_column") - means that first_function needs single_column to complete the task
          - pipe(second_function, "[col1, ..., colN]") - means that second_function needs [col1, ..., colN] to complete the task
          - pipe(third_function,) - means that there is no need to specify the column name
- **link to Pipe** function: https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.pipe.html    

-------------------------------------------------------------------------------------------------------------------------------------------------------------------
## Project Objective: Use Pandas Pipe for multiple functions chaining
Create a model that applies chainable functions to preprocess data from created dataset.

-------------------------------------------------------------------------------------------------------------------------------------------------------------------
