// Module 1 Smart Contract Project
contract SmartContractArlos 
{
  uint private arlosvalue;

  //On this contract, I have name a function, setArlosValue that takes an input _value. 
  function setArlosValue(uint _value) external 
  {
    //Require Statement
    //This statement checks if the input value is not greater than 100. 
    //If it is less than 100, it throws an exception with the provided error message.
    require(_value >= 100, "Value should be greater than 100");

    //Assert Statement
    //This statement validates a condition and will throw an error if it evaluates to false. 
    //In this case, It verifies that _value is greater than or equal to 100.
    assert(_value >= 100);

    //Revert Statement 
    //This statement is used to exit the function execution and revert any changes made before calling this function if a certain condition is met. 
    //Here, we check if _value exceeds 1000, in which case we throw an exception with the specified error message.
    if (_value > 1000) 
    {
      revert("Value cannot be greater than 1000");
    }

    arlosvalue =_value;

  }
  
}
