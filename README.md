# Bio539_Final_Project
Final Project for Bio539
This Script acts as a versitile calculator for generating Stacked Bar Plots summarizing relative abundance after resolving 
exisiting data to a higher resolution (species/OTU level from genus/class level)

At the begining of the script the User will be presented with 4 varriable inputs: 
  - Var.1 <- is assigned to the master relative abundance csv, this script should be formated as follows: 
          Columns: 
    
                Column 1 "Sample ID", these should be unique identifiying values for each sample run  
     
                Column 2 "Treatment" (incubation conditions, etc)
    
                Columns 3-(n+1) Genus or Class taxonomy names for 1-'n' with 'n' being the number of assigned taxonomies
    
                For direct reference, see 'diatom_relabund_osp.csv' used as the model in this script
 
 - Var.2 <- Is assigned to the raw counts of ASVs/OTUs, formated as follows: 
          Columns: 
      
            Column 1 called "Sample ID", Sample IDs should be identical to those in the file used for var.1, as these are        
            used for alligning the files. 
      
            Column 2 "Treatment" this column should contain details on treatment similar to Var.1 dataset "Treatment" column
      
            Columns 3-(n+1) called "ASV1" - "ASVn" with 'n' being the total number of ASVs 
      
            Final Column called "Totals" containing total counts for each sample ID, values in each row should add up to the       
            value shown in that row's "Totals" cell 
      
            For direct reference see 'pn_asv_relabund_osp.csv' 
   
   - Var.3 <- This varriable is assinged the exact number of ASVs that you will be inputing in the Var.2 csv 
              (for this example Var.3 = 10 since we are breaking out the genus into 10 ASVs) 
              
   - Var.4 <- This varriable is assigned the name of the Genus or Class in the Var.1 csv that you want to break out into ASVs
              (This must EXATLY match the name of the column in the Var.1 csv, or there will be resulting errors) 

After inputing all variables, run the R script one section at a time, and after runing the final section a Relative Abundance 
Plot of the new ASVs alongside the previously identified genera/classes will be generated for use.  
