Work in progress.

Generates valid EPUB 3.0 files with additional EPUB 2.0 table of contents ([as seen here](https://github.com/bmaupin/epub-samples)) for maximum backwards-compatibility.

**Current API:**

    // Create a new EPUB
	e, err := epub.NewEpub("My title")
	if err != nil {
		fmt.Println("epub.NewEpub error: %s", err)
	}

    // Set the author
	e.SetAuthor("Hingle McCringleberry")

    // Add a section
	section1Content := `    <h1>Section 1</h1>
    <p>This is a paragraph.</p>`
	e.AddSection("Section 1", section1Content)

	section2Content := `    <h1>Section 2</h1>
    <p>This is a paragraph.</p>`
	e.AddSection("Section 2", section2Content)

    // Write the EPUB
	err = e.Write("My EPUB.epub")
	if err != nil {
		fmt.Println("epub.Write error: %s", err)
	}

**Wishlist:**

- Clean up error handling
- Add support for cover pages
- Add documentation
- Add tests
- Add support for CSS
- Add functionality to read EPUB files
