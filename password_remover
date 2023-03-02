import PyPDF2

# Open the encrypted PDF file
with open('PATH/TO/PDF/FILE.pdf', mode='rb') as file:
    # Create a PDF reader object
    reader = PyPDF2.PdfFileReader(file)

    # Check if the file is encrypted
    if reader.isEncrypted:
        # Enter the password to decrypt the file
        password = input("Enter the password: ")
        reader.decrypt(password)

        # Create a new PDF writer object
        writer = PyPDF2.PdfFileWriter()

        # Copy the decrypted pages to the new PDF writer object
        for pageNum in range(reader.numPages):
            writer.addPage(reader.getPage(pageNum))

        # Write the decrypted PDF to a new file
        with open('decrypted_file.pdf', mode='wb') as new_file:
            writer.write(new_file)
