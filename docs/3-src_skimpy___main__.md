# Src Skimpy Main

[_Documentation generated by Documatic_](https://www.documatic.com)

<!---Documatic-section-Codebase Structure-start--->
## Codebase Structure

<!---Documatic-block-system_architecture-start--->
```mermaid
flowchart LR
__main__([__main__])
__init__([__init__])
__main__-->__init__
```
<!---Documatic-block-system_architecture-end--->

# #
<!---Documatic-section-Codebase Structure-end--->

<!---Documatic-section-src.skimpy.__main__.main-start--->
## src.skimpy.__main__.main

<!---Documatic-section-main-start--->
```mermaid
flowchart LR
src.skimpy.__main__.main-->src.skimpy.__init__.skim
src.skimpy.__init__.skim-->src.skimpy.__init__._infer_datatypes
src.skimpy.__init__.skim-->src.skimpy.__init__._dataframe_to_rich_table
src.skimpy.__init__._dataframe_to_rich_table-->src.skimpy.__init__._map_row_positions_to_text_style
src.skimpy.__init__._dataframe_to_rich_table-->src.skimpy.__init__._simplify_datetimes_in_array
src.skimpy.__init__.skim-->src.skimpy.__init__._round_dataframe
```

### Object Calls

* src.skimpy.__init__.skim

<!---Documatic-block-src.skimpy.__main__.main-start--->
<details>
	<summary><code>src.skimpy.__main__.main</code> code snippet</summary>

```python
@click.command()
@click.version_option()
@click.argument('input')
def main(input) -> None:
    df = pd.read_csv(input, infer_datetime_format=True, parse_dates=True)
    df = df.infer_objects()
    skim(df)
```
</details>
<!---Documatic-block-src.skimpy.__main__.main-end--->
<!---Documatic-section-main-end--->

# #
<!---Documatic-section-src.skimpy.__main__.main-end--->

[_Documentation generated by Documatic_](https://www.documatic.com)