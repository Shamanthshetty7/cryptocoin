// SPDX-License-Identifier: RANDOM_TEXT

pragma solidity 0.8.7;
contract SoscErc20{
    event Transfer(address indexed_form,address indexed_to,uint256 _value);
     event Approval(address indexed_ownner,address indexed_spender,uint256 _value);

     string public constant name="sosc coin";
     string public constant symbol="sosc";
     uint8 public constant decimals=18;

     mapping (address =>uint256) balances;
     mapping (address => mapping(address=>uint256)) approved;
     uint256 totalSupply_;

     constructor(uint256 total){
         totalSupply_=total;
         balances[msg.sender]=total;
     }

     function totalSupply() public view returns (uint256){
         return totalSupply_;
     }
     function balanceOf(address tokenOwner) public view returns (uint256){
         return balances[tokenOwner];
     }
     function trasfer(address reciever,uint value)public returns(bool ){
          require(value <=balances[msg.sender]);
          balances[reciever]+=value;
          balances[msg.sender]-=value;
          emit Transfer(msg.sender,reciever,value);
        return true;
     }
}
