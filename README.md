# NR-INFRA-EXAMPLE
```diff
Terraform used the selected providers to generate the following execution plan. Resource actions are indicated with the following symbols:
+ create
- destroy
  -/+ destroy and then create replacement

~ Terraform will perform the following actions:

# local_file.add_file will be created
+ resource "local_file" "add_file" {
    + content              = "add_file"
    + directory_permission = "0777"
    + file_permission      = "0777"
    + filename             = "add_file"
    + id                   = (known after apply)
      }

# local_file.change_file must be replaced
-/+ resource "local_file" "change_file" {
~ content              = "old_content" -> "new_content" # forces replacement
~ id                   = "b6937a0aac63ecbdcceb684a8b4cad70d0b1b4ec" -> (known after apply)
# (3 unchanged attributes hidden)
}

# local_file.remove_file will be destroyed
# (because local_file.remove_file is not in configuration)
- resource "local_file" "remove_file" {
    - directory_permission = "0777" -> null
    - file_permission      = "0777" -> null
    - filename             = "remove_file" -> null
    - id                   = "da39a3ee5e6b4b0d3255bfef95601890afd80709" -> null
      }

Plan: 2 to add, 0 to change, 2 to destroy.
```
