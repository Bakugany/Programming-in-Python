The DrugBank database is a publicly available and free database of information about drugs (medicinal substances). It was created in 2006 by a team led by Craig Knox and David Wishart from the Faculty of Computing Science and Biological Sciences at the University of Alberta in Canada. It combines data from the fields of chemistry, biochemistry, genetics, pharmacology, and pharmacokinetics.

Since access to the full database requires creating an account, filling out a form with a justification for the access request, and obtaining approval, for the purposes of this assignment you will be provided with the file `drugbank_partial.xml` containing a reduced version of the database. This file includes data for 100 drugs (the full database, published on 2024-03-14, contains information on over 16,000 drugs).

The assignment involves analyzing the content of the reduced version of the database and creating various tables and charts summarizing the drug database.

## Tasks

1. **Drug Information DataFrame**  
   Create a DataFrame that for each drug contains the following information: the unique drug identifier in the DrugBank database, the drug's name, type, description, the form in which the drug appears, indications, mechanism of action, and information about the foods with which the drug interacts. 

2. **Synonyms DataFrame & Graph**  
   Create a DataFrame that allows searching for all synonyms under which a drug appears by its DrugBank ID. Write a function that, for a given DrugBank ID, creates and plots a synonyms graph using the NetworkX library. Ensure that the generated plot is clear and legible. 

3. **Pharmaceutical Products DataFrame**  
   Create a DataFrame for pharmaceutical products containing a given drug (medicinal substance). The DataFrame should include information about the drug ID, product name, manufacturer, the USA National Drug Code, the form in which the product appears, method of application, dosage information, the country, and the regulatory agency for the product. 

4. **Pathways DataFrame**  
   Create a DataFrame containing information about all pathways of all types (e.g., signaling, metabolic, etc.) with which any drug interacts. Provide the total number of these pathways. 

5. **Drug-Pathway Interaction Analysis**  
   For each signaling/metabolic pathway in the database, list the drugs that interact with it. Present the results both as a DataFrame and in a graphical format of your design. An example of such a visualization may be a bipartite graph where the two types of vertices are signaling pathways and drugs, and the edges represent the interaction between a drug and a signaling pathway. Ensure the presentation is clear and visually appealing. 

6. **Histogram of Pathway Interactions per Drug**  
   For each drug in the database, provide the number of pathways with which it interacts. Present the results as a histogram with appropriately labeled axes. 

7. **Protein Targets DataFrame**  
   Create a DataFrame containing information about the proteins with which individual drugs interact. These proteins are known as targets. The DataFrame should include at least the following: the target’s DrugBank ID, information about the external database (*source*, e.g., Swiss-Prot), the identifier in the external database, the peptide name, the gene name coding for the peptide, the GenAtlas gene ID, the chromosome number, and the cellular localization. 

8. **Pie Chart of Target Cellular Localization**  
   Create a pie chart showing the percentage distribution of target proteins in different parts of the cell. 

9. **Drug Status DataFrame & Pie Chart**  
   Create a DataFrame showing the number of drugs that have been approved, withdrawn, are in the experimental (or investigational) phase, and are approved for use in animal treatments. Present these data in a pie chart. Also, provide the number of approved drugs that have not been withdrawn. 

10. **Potential Drug-Drug Interactions DataFrame**  
    Create a DataFrame containing information regarding potential interactions between a given drug and other drugs. 

11. **Custom Graphical Presentation**  
    Develop a custom graphical presentation containing information about a specific gene (or genes), the medicinal substances that interact with that gene/genes, and the pharmaceutical products that contain the given medicinal substance. It is up to you to decide whether the presentation is made for a specific gene or for all genes simultaneously. Make sure that your presentation is both clear and visually attractive. 

12. **Self-Designed Data Analysis and Visualization**  
    Propose your own analysis and visualization of drug-related data. You may use additional information from other biomedical and bioinformatics databases available online. However, ensure that the chosen database allows automated data retrieval by a program. For instance, the GeneCards database explicitly prohibits this, as indicated in red on their website. Examples of databases to consider include [UniProt](https://www.uniprot.org/), [Small Molecule Pathway Database](https://smpdb.ca/), and [The Human Protein Atlas](https://www.proteinatlas.org/).

13. **Test Database Simulator**  
    Create a simulator that generates a test database containing 20,000 drugs. The generated values for 19,900 drugs in the “DrugBank Id” column should have consecutive numbers, while the values for the remaining columns should be randomly selected from the values of the existing 100 drugs. Save the results in a file named `drugbank_partial_and_generated.xml`. Conduct the analysis specified in tasks 1-12 on this test database.

14. **Unit Testing**  
    Prepare unit tests using the pytest library. 

15. **Web Service for Histogram Data (Task 6)**  
    Implement task 6 in such a way that it is possible to send a drug ID to your server, which will return the result in the response (use FastAPI and Uvicorn; it is sufficient to demonstrate sending the data via a POST request, as per the Execute feature in the documentation). 
```
