def process_file(input_filename, output_filename):
    try:
        with open(input_filename, "r") as infile:
            content = infile.read() 

        modified_content = content.upper()

        with open(output_filename, "w") as outfile:
            outfile.write(modified_content)

        print(f"Modified content written to '{output_filename}' successfully!")

    except FileNotFoundError:
        print(f"Error: The file '{input_filename}' does not exist.")
    except IOError:
        print(f"Error: Cannot read/write file '{input_filename}'.")

input_file = input("Enter the filename to read: ")
output_file = "modified_" + input_file
process_file(input_file, output_file)
