# PLP-WEEK-4
Plp Assignments on Python
def modify_file_content(input_filename, output_filename):
    try:
        # Open the input file and read its content
        with open(input_filename, "r") as infile:
            content = infile.read()

        # Modify content (convert to uppercase)
        modified_content = content.upper()

        # Write to the new file
        with open(output_filename, "w") as outfile:
            outfile.write(modified_content)

        print(f"✅ Modified content written to {output_filename}")

    except FileNotFoundError:
        print("❌ Error: The file does not exist. Please check the filename and try again.")
    except PermissionError:
        print("❌ Error: You do not have permission to read this file.")
    except Exception as e:
        print(f"❌ An unexpected error occurred: {e}")

# User input for filename
input_filename = input("Enter the filename to read: ")
output_filename = "modified_" + input_filename  # Creates a new file with a modified name

modify_file_content(input_filename, output_filename)
