![green_drime_python](https://github.com/user-attachments/assets/266b24ad-653c-456e-a2dd-f1a13d38661a)

# Drime Package

`drime` is a Python client library for interacting with the Drime API.

## Installation

To install the `drime` package, you can use pip:

```bash
pip install drime
```

## Usage

Here is a quick guide on how to use the Drime package:

```python
import drime

# Initialize the Drime API client with your API token
drime_api = drime.DrimeAPI(token="your_api_token")

# Login to your account
response = drime_api.login(email="your_email@example.com", password="your_password")
print(response)

# Create a new folder
folder_response = drime_api.create_folder(name="New Folder")
print(folder_response)

# Upload a file
upload_response = drime_api.upload_file(file_path="/path/to/your/file.txt")
print(upload_response)

# Get file entries
file_entries = drime_api.get_file_entries()
print(file_entries)

# Delete file entries
delete_response = drime_api.delete_file_entries(entry_ids=["file_id_1", "file_id_2"], permanent=True)
print(delete_response)

# Move file entries
move_response = drime_api.move_file_entries(entry_ids=["file_id_1"], target_folder_id="new_folder_id")
print(move_response)

# Share a file entry
share_response = drime_api.share_file_entry(entry_id="file_id_1", user_email="user@example.com")
print(share_response)

# Create a shareable link
link_response = drime_api.create_shareable_link(entry_id="file_id_1")
print(link_response)
```

Make by PainDe0Mie (painde0miie)
