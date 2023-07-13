# bmi
  
function computeBMI(weight, height) {
    /**
     * This function computes the Body Mass Index (BMI) given the weight and height.
     * 
     * @param {number} weight - The weight of the person in kilograms.
     * @param {number} height - The height of the person in meters.
     * @returns {number} The computed BMI value.
     */
    
    try {
        // Check if the weight and height are valid numbers
        if (typeof weight !== 'number' || typeof height !== 'number') {
            throw new TypeError('Weight and height must be numbers');
        }
        
        // Check if the weight and height are positive numbers
        if (weight <= 0 || height <= 0) {
            throw new Error('Weight and height must be positive numbers');
        }
        
        // Calculate the BMI using the formula: weight / (height * height)
        const bmi = weight / (height * height);
        
        // Return the computed BMI value
        return bmi;
    } catch (error) {
        // Log the error
        console.error('Error:', error.message);
        return null;
    }
}
