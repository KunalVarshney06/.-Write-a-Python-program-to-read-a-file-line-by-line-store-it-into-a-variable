# .-Write-a-Python-program-to-read-a-file-line-by-line-store-it-into-a-variable
def read_file_into_variable(file_path):
    file_contents = ""
    try:
        with open(file_path, 'r') as file:
            file_contents = file.read()
    except FileNotFoundError:
        print("File not found.")
    except IOError:
        print("An error occurred while reading the file.")
    return file_contents

# Example usage
file_path = 'path/to/your/text/file.txt'  # Replace with the actual file path
file_contents = read_file_into_variable(file_path)
print("File contents:")
print(file_contents)
