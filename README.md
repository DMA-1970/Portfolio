# Navigate to your repository directory
cd path_to_your_repository

# Create assets directory if it doesn't exist
mkdir -p assets

# Move your image to the assets directory
mv path_to_your_image/050324-3.578-2.jpg assets/

# Create or edit README.md
echo "# David Mobolaji Abiodun

![David Mobolaji Abiodun](assets/050324-3.578-2.jpg)

## Work Experience
### Enterprise Technology Manager @ MillTechFX

## Certification
- ITIL
- Azure
- Microsoft

## Education
### University of Essex
MSc Enterprise IT Management

## Projects
### DMA-1970/Portfolio
This is my GitHub portfolio.
" > README.md

# Add changes to git
git add README.md assets/050324-3.578-2.jpg

# Commit the changes
git commit -m "Add portfolio structure and image"

# Push the changes to the remote repository
git push origin main
