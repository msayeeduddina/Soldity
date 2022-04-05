next slab wide segment lobster brother range kitchen exchange below cliff happy


//SPDX-License-Identifier: MIT

pragma solidity ^0.8.6;

//{event}
// contract Mycontract{
//     uint a;

//     event NewTrade(
//         uint indexed date,
//         address indexed from,
//         address indexed to,
//         uint amount
//     );
//     function trade (address to, uint amount)external{
//         emit NewTrade(now, msg.sender,to,amount);
//     }
// }


// contract events{
//     address public fromAccount;
//     uint public toBalanceAccount;

//     event transferred (address,address,uint);

//     function transfer(address payable _toaccountId) public payable {
//         fromAccount= msg.sender;
//         _toaccountId.transfer(msg.value);
//         toBalanceAccount=_toaccountId.balance;
//         emit transferred(fromAccount,_toaccountId,msg.value);
//     }
// }



//{emit events in solidity}
// contract events{
//     address public fromAccount;
//     uint public toAccountBalance;

//     event tranferred (address,address,uint);

//     function transfer(address payable _toaccountId) public payable{
//         fromAccount=msg.sender;
//         _toaccountId.transfer(msg.value);
//         toAccountBalance=_toaccountId.balance;

//         emit tranferred (fromAccount,_toaccountId,msg.value);
//     }
// }

// contract events {
//     event balance(address account,string message,uint val);

//     function setData(uint _val) public {
//         emit balance(msg.sender,"has a value",_val);
//     }
// }



//{ loop - break- continue}
// contract Overflow{
//     uint public number=1;
//     function breakstatement() public {
//         uint i=0;
//         while (i<=10){
//             i +=1;
//             if (i==5){
//                 break;
//             }
//         }
//             number=i;
//         }

//      function continuestatement() public{
//          uint i=0;
//          while(i<10){
//              i +=1;
//              if(i==5){
//                  continue;
//              }
//              i +=1;

//          }
//          number=i;
//      }   
// }




// //{Enum}
// contract Enum{

// enum Status{
//     Pending,
//     Shipped,
//     Rejected,
//     Accepted,
//     Cancel
// }

// Status public status;


// function getStatus() public view returns (Status){
//     return status;
// }

// function setStatus(Status _status) public{
//     status= _status;
// }


// function rej() public {
//     status=Status.Rejected;
// }

// function reset() public {
//     delete status;
// }

// }


// contract status{
//     enum user{
//         allowed,
//         notallowed,
//         wait
//             }
//    user public u1=user.allowed;
//    user public u2=user.notallowed;
//    user public u3=user.wait;

//    uint public lottery=1000;
//    function owner() public {
//        if (u1==user.allowed){
//            lottery=0;
//        }
//    }
// function changeOwner() public {
//     u1=user.notallowed;
// }
// }



// contract Enums{
//     enum Level{Spider,Snake,Bat,Iron}
//     Level public level = Level.Spider;

//     function completelevel() public returns(uint){
//         nextlevel(); 
//         return uint(level);
//     }

//     function nextlevel() public {
//         level =Level(uint(level)+1);
//     }
// }


// {struct}
// struct Student{
//     uint roll;
//     string name;
// }

// contract School{
//     Student public s1;
//     constructor (uint _roll,string memory _name) {
//         s1.roll=_roll;
//         s1.name=_name;
//     }
    
//     function changeS (uint _roll,string memory _name) public{
//         Student memory newStudent=Student({
//             roll:_roll,
//             name:_name
//           });
//         s1=newStudent;
//     }
// }




//{mapping}
// contract Mapping{
//     mapping (uint=>string) public emp_id;


//     function setempid() public {      //key:value
//         emp_id[1]= " Delhi";
//         emp_id[2]= " Pune";
//         emp_id[3]= " Mumbai ";
//         emp_id[4]= " Bangalore ";
//         emp_id[5]= " London ";
//     }
//     function getempid(uint _id ) public view returns (string memory){
//         return emp_id[_id];
//     }
// }


                //struct   // File level

// contract advmapping{

//     struct donor_info{     // contract level
//     string name;
//     uint age;
//     string add;
//     uint donation;
//     }

//     mapping(address=>donor_info) public acc_info;
//     function setinfo(string memory _name,uint _age,string memory _add,uint _donation) public{
//     acc_info[msg.sender]=donor_info(_name,_age,_add,acc_info[msg.sender].donation+_donation);
//     }

//     function deleteinfo() public{
//         delete acc_info[msg.sender];
//     }
// }


// //Storage //	Memory	// Stack
// Permanent Storage	/ temporary	/temporary
// It contains keys and value like a hashtable	/ Byte Array  /	Byte Array
// Uses state variables /	Local variables defined in function calls /	Local values of value types are stored
// Contract state variable	/ memory variables / stack variables
// Expensive gas operation  / Does not cost gas and inexpensive operation / Inexpensive gas operation
// keyword in solidity	/ keyword in solidity	/ Keyword in solidity
// Like a comp HDD / Like a RAM

// {storage vs memory}
// contract store{
//     string[] public Tour = ['Delhi','Pune','Mumbai'];

//     function mem() public view {    //if not done changes in state variable then put- view   
//         string[] memory s1=Tour;
//         s1[0]='Mohali';
//     }
//     function sto() public {
//         string[] storage s1=Tour;
//         s1[0]='Bangalore';
//     }
// }




14/03/22


//"SPDX-License-Identifier: MIT

pragma solidity ^0.8.0;


// contract Counter{
//     uint public count=0;     // another way to view count value to public by adding public

// // constructor ()  {
// //     count = 0;           //another way to give count value as 0 initial
// // }

// event Increment (uint value);
// event Decrement (uint value);

// function getCount() view public returns(uint){    //view count value to public by making function
//     return count;
// }
//     function increment( ) public {
//         count +=1;
//         emit Increment(count);
//     }
//     function decrement( ) public {
//         count -=1;
//         emit Decrement(count);
//     }
// }
















// //SPDX-License-Identifier: MIT
// pragma solidity ^0.6.0;

// interface IERC20{

//     function totalSupply() external view returns(uint256);
//     function balanceOf(address account) external view returns (uint256);
//     function transfer(address recipient, uint256 amount) external returns(bool);

//     event Transfer(address indexed from, address indexed to, uint256 value);
// }

// contract CGCToken is IERC20{

//     string public name;
//     string public symbol;
//     uint8 public decimals;

//     event Approval(address indexed tokenOwner, address indexed spender, uint tokens);
//     event Transfer(address indexed from, address indexed to, uint tokens);

//     mapping(address=>uint256) balances;
//     mapping(address=> mapping(address=>uint256)) allowed;

//     uint256 totalSupply_;
//     address admin;

//     constructor(string memory _name, string memory _symbol, uint8 _decimal, uint256 _tsupply) public {
//         totalSupply_ = _tsupply;
//         balances[msg.sender] = totalSupply_;
//         name = _name;
//         symbol = _symbol;
//         decimals = _decimal;
//         admin = msg.sender;
//     }


// function totalSupply() public override view returns (uint256){
//     return totalSupply_;
//     }

// function balanceOf(address tokenOwner) public override view returns (uint256){
//     return balances[tokenOwner];
//     }

// function transfer(address reciever, uint256 numTokens) public override returns (bool){
//     require(numTokens <= balances[msg.sender]);
//     balances[msg.sender] -= numTokens;
//     balances[reciever] += numTokens;
//     emit Transfer(msg.sender,reciever,numTokens);
//     return true;
//     }

// modifier onlyAdmin {
//     require (msg.sender == admin, "Only admin can run this function");
//     _;
//     }

// function mint(uint256 _qty) public onlyAdmin returns(uint256){
//     totalSupply_ += _qty;
//     balances[msg.sender] += _qty;
//     return totalSupply_;
//     }

// function burn(uint256 _qty) public onlyAdmin returns(uint256){
//     require(balances[msg.sender] >= _qty);
//     totalSupply_ -= _qty;
//     balances[msg.sender] -= _qty;
//     return totalSupply_;
//     }

// }
















// 15/03/2022


// //SPDX-License-Identifier: MIT

// pragma solidity ^0.8.6;


// contract Lottery {
//     address public manager;
//     address payable[] public players;

//     constructor() {
//        manager=msg.sender;
//     }


//     function alreadyExist() private view returns(bool) {
//         for(uint i=0; i<players.length; i++) {
//             if(players[i]==msg.sender)
//             return true;
//         }
//         return false;
//     }
//     function enter() public payable {
//         require(msg.sender != manager, "Manager Can't Participate");
//         require(alreadyExist() == false , "Player exists");
//         require(msg.value >= 1 ether , "Min amount must be paid");
//         players.push(payable(msg.sender));
//     }

//     function random() private view returns(uint) {
//         return uint(keccak256(abi.encodePacked(block.difficulty, block.number, players)));
//     }
//     function pickwinner() public {
//         require(msg.sender == manager, "Only manager can select winner");
//         uint index = random() % players.length;   //winner index
//         address contractAddress = address(this);
//         players[index].transfer(contractAddress.balance);
//         players = new address payable[](0);       // resetting of lottery
//     }
//     function getPlayers() public view returns(address payable[] memory) {
//         return players;
//     }

// }
















16/03/2022


// //SPDX-License-Identifier: MIT


// pragma solidity ^0.8.0;

// contract pay{

//     address payable user=payable(0x617F2E2fD72FD9D5503197092aC168c91465E7f2);    //should mention payable() bcz after ^0.8.0
//     function payEther() public payable{
//     }
//     function getBalance() public view returns(uint){
//         return address(this).balance;
//     }
//     function sendEther() public {
//         user.transfer(1 ether);
//     }
// }




{ Storage, Memory, CallBack }
// contract dataLocation {
//     uint[] public arr =[1,3,7,9,22];

//     function Storage() public {
//         uint [] storage arrs = arr;
//         arrs[3]=99;
//     }
//     function mem() public view {
//         uint [] memory arrm = arr;
//         arrm[1]=192;
//     }


//     function Memory1(string memory str1,uint[] memory arr1) public{
//                                     //execution cost  =  25333 gas
//     }
//     function Calldata1(string calldata str1,uint[] calldata arr1) public{
//                                     //execution cost  =  23305 gas
//     }



//     function Memory2(string memory str2,uint[] memory arr2) public{
//             getInMem(arr2);
//             //getInCall(arr2);
//     }
//     function Calldata2(string calldata str2,uint[] calldata arr2) public{
//               getInMem(arr2);
//               getInCall(arr2);                     
//     }
//     function getInMem(uint[] memory arr2) public {
        
//     }
//     function getInCall(uint[] calldata arr2) public {

//     }
    

// }
















17/03/2022

{Solidity CrowdFunding Project}

// //SPDX-License-Identifier: MIT

// pragma solidity ^0.8.0;


// contract Crowdfunding{

//     mapping(address=>uint) public spenders;
//     address public host;
//     uint public lowlimitCntrbtn;
//     uint public timelimit;
//     uint public goal;    
//     uint public raisedCntrbtn;
//     uint public numSpender;


//     struct Request{
//         string description;
//         address payable recipient;
//         uint value;
//         bool completed;
//         uint numVoters;
//         mapping(address=>bool) voters;
//     }

//     mapping(uint=>Request) requests;
//     uint public numRequests;


//     constructor (uint _goal, uint _timelimit) {
//         host = msg.sender;
//         goal = _goal;
//         timelimit = block.timestamp + _timelimit;
//         lowlimitCntrbtn = 100 wei;
//     }


//     function sendAmnt() public payable {
//         require(block.timestamp<timelimit, "You have crossed timelimit to spend") ;
//         require(msg.value > lowlimitCntrbtn , " Please spend more amount than lowlimitCntrbtn ");

//         if(spenders[msg.sender] == 0){
//             numSpender++;
//         }
//         spenders[msg.sender] += msg.value;
//         raisedCntrbtn += msg.value;
//     }
//     function getContractBalance() public view returns(uint) {
//         return address(this).balance;
//     }
//     function payback() public {
//         require(block.timestamp>timelimit && goal>raisedCntrbtn, "Sorry you are not eligible");
//         require(spenders[msg.sender]>0);
//         address payable user = payable (msg.sender);
//         user.transfer(spenders[msg.sender]);
//         spenders[msg.sender]=0;
//     }


//     modifier onlyhost(){
//         require(msg.sender==host, "Only host can call this");
//         _;
//     }
//     function createRequests(string memory _description, address payable _recipient, uint _value) public onlyhost{
//         Request storage newRequest = requests[numRequests];
//         numRequests++;
//         newRequest.description=_description;
//         newRequest.recipient=_recipient;
//         newRequest.value=_value;
//         newRequest.completed=false;
//         newRequest.numVoters=0;
//     }
//     function voterRequest(uint _requestno) public {
//         require(spenders[msg.sender]>0, "you must be a spender first");
//         Request storage thisRequest = requests[_requestno];
//         require(thisRequest.voters[msg.sender] == false, "you have already voted");
//         thisRequest.voters[msg.sender] = true;
//         thisRequest.numVoters++;
//     }
//     function makePayment(uint _requestno) public onlyhost{
//         require(raisedCntrbtn>=goal);
//         Request storage thisRequest = requests[_requestno];
//         require(thisRequest.completed==false, "The request have been completed");
//         require(thisRequest.numVoters > numSpender/2, "Majority have not supportecd this");
//         thisRequest.recipient.transfer(thisRequest.value);
//         thisRequest.completed = true;
//     }


// }






{Mapping-Struct}


// //SPDX-License-Identifier: MIT

// pragma solidity ^0.8.0;

// contract Courses{


//     struct Instructor{
//         uint age;
//         string fName;
//         string lName;
//     }

//     mapping(address=>Instructor) public instructors;
 
//     function setInstructor(address _address, uint _age, string memory _fname, string memory _lName) public {
//         instructors[_address]=Instructor(_age,_fname,_lName);      
//     }
    

// }





















{30/3/2022}

// Wow-Coin

//SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

interface IERC20{

    function totalSupply() external view returns(uint256);
    function balanceOf(address account) external view returns (uint256);
    function transfer(address recipient, uint256 amount) external returns(bool);

    event Transfer(address indexed from, address indexed to, uint256 value);
}

contract WowCoin is IERC20{

    string public name;
    string public symbol;
    uint8 public decimals;

    event Approval(address indexed tokenOwner, address indexed spender, uint tokens);

    mapping(address=>uint256) balances;
    mapping(address=> mapping(address=>uint256)) allowed;

    uint256 totalSupply_;
    address admin;

    constructor() {
        totalSupply_ = 10000000;
        balances[msg.sender] = totalSupply_;
        name = "Wow-Coin";
        symbol = "wow";
        decimals = 18;
        admin = msg.sender;
    }


function totalSupply() public override view returns (uint256){
    return totalSupply_;
    }

function balanceOf(address tokenOwner) public override view returns (uint256){
    return balances[tokenOwner];
    }

function transfer(address reciever, uint256 numTokens) public override returns (bool){
    require(numTokens <= balances[msg.sender]);
    balances[msg.sender] -= numTokens;
    balances[reciever] += numTokens;
    emit Transfer(msg.sender,reciever,numTokens);
    return true;
    }

modifier onlyAdmin {
    require (msg.sender == admin, "Only admin can run this function");
    _;
    }

function mint(uint256 _qty) public onlyAdmin returns(uint256){
    totalSupply_ += _qty;
    balances[msg.sender] += _qty;
    return totalSupply_;
    }

function burn(uint256 _qty) public onlyAdmin returns(uint256){
    require(balances[msg.sender] >= _qty);
    totalSupply_ -= _qty;
    balances[msg.sender] -= _qty;
    return totalSupply_;
    }

}
















{30/3/2022}

// Keccak256



//SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;


contract Hashfunc{

    function hash(string memory name1, uint num1, address _add1)external pure returns(bytes32){
     return keccak256(abi.encodePacked(name1,num1,_add1));
    }

    function encodefunc(string memory name2, string memory name3, uint num2) external pure returns(bytes memory){
        return abi.encode(name2,name3,num2);              // "abcd" "efgh" =(no equal bytes)= "abc" "defgh"
    }

    function encodePackedfunc(string memory name4, string memory name5, uint num2) external pure returns(bytes memory){
        return abi.encodePacked(name4,name5,num2);              // "abcd" "efgh" =(equal bytes)= "abc" "defgh"
    }

    function collisionencodePackedfunc(string memory name6, uint num3, string memory name7) external pure returns(bytes32){
        return keccak256(abi.encodePacked(name6,num3,name7));           // "abcd" 1234 "efgh" =(no equal bytes)= "abc" 1234 "defgh"
    }

}
















{4/4/2022}

//SPDX-License-Identifier: MIT

pragma solidity ^0.8.0;    


// contract Identity {
//     string name;
//     uint age;

//     constructor() {
//          name="john";
//          age= 30;
//     }

//     function getName(string memory) public view returns(string memory){
//         return name;
//     }
//     function getAge(uint) public view returns(uint){
//         return age;
//     }
//     function setAge()public{
//         age= age+1;
//     }

// }



contract state{

    uint age=10;
    function ageStore()view public returns(uint){
        
    return age;
    }
    function getter() private view returns(uint ){
        return age;
    }
    function setter() public {
     age=age+1;
    }
}

contract local{
    string name;
    uint age;

    function getName() public view returns(string memory){
     return name;
    }
    function setName(string memory _name) public {
        name=_name;
    }
}



contract localage {
    uint public age=10;

    function getroll() public pure returns(uint){
        uint roll=100;
        return roll;
    }
}



contract constructtor{
    uint public ages;
    string public name;
    string public names="john";

    constructor(uint _ages){
        ages=_ages;
        name="hello";
    }
}


contract integers{
    // int8 public num=128;
    // uint8 public num=25;
    int16 public num1=128;
}





// pragma solidity ^0.8.10; 
// contract integers1{
   
//     uint8 public num=255;

//     function setNum() public{
//         num = num + 1;
//     }

// }




contract array{
    uint[4] public arr = [12,34,22,66];
    function setArr(uint index,uint value) public{
        arr[index]=value;
    }
}



contract ArrayPLP{
    uint[] public arrA;

    function pushA(uint item) public{
        arrA.push(item);
    }
    function lengt() public view returns(uint){
      return arrA.length;
    }
    function popA() public {
        arrA.pop();
    }
}



contract arrayByte{
    bytes3 public b3;
    bytes2 public b2;

    function setter() public{
        b3="abc";
        b2="ab";
        // b3[0]="d";    // immutable
    }
}

contract arrayByteP{
    bytes public b1="abc";
    function setter() public{
        b1.push('d');
    }
}






contract arrayLpfunc{
    uint[3] public arr;
    uint public count;

function whilearray() public{
    while(count<arr.length){
        arr[count]=count;
        count++;
     }
    }

function forarray() public{
    for(uint i=count;i<arr.length;i++){
        arr[count]=count;
        count++;
    }
}   
function dowhilearray() public {
    do{
    arr[count]=count;
    count++;
     }while(count<arr.length);
    }
}





contract bools{
    bool public value1;
    bool public value2=true;
}
















{05/04/2022}

//kalika//WOWCOIN

//SPDX-License-Identifier: MIT

pragma solidity ^0.8.0;

interface IBEP20 {
  /**
   * @dev Returns the amount of tokens in existence.
   */
  function totalSupply() external view returns (uint256);

  /**
   * @dev Returns the token decimals.
   */
  function decimals() external view returns (uint8);

  /**
   * @dev Returns the token symbol.
   */
  function symbol() external view returns (string memory);

  /**
  * @dev Returns the token name.
  */
  function name() external view returns (string memory);

  /**
   * @dev Returns the bep token owner.
   */
  function getOwner() external view returns (address);

  /**
   * @dev Returns the amount of tokens owned by `account`.
   */
  function balanceOf(address account) external view returns (uint256);

  /**
   * @dev Moves `amount` tokens from the caller's account to `recipient`.
   *
   * Returns a boolean value indicating whether the operation succeeded.
   *
   * Emits a {Transfer} event.
   */
  function transfer(address recipient, uint256 amount) external returns (bool);

  /**
   * @dev Returns the remaining number of tokens that `spender` will be
   * allowed to spend on behalf of `owner` through {transferFrom}. This is
   * zero by default.
   *
   * This value changes when {approve} or {transferFrom} are called.
   */
  function allowance(address _owner, address spender) external view returns (uint256);

  /**
   * @dev Sets `amount` as the allowance of `spender` over the caller's tokens.
   *
   * Returns a boolean value indicating whether the operation succeeded.
   *
   * IMPORTANT: Beware that changing an allowance with this method brings the risk
   * that someone may use both the old and the new allowance by unfortunate
   * transaction ordering. One possible solution to mitigate this race
   * condition is to first reduce the spender's allowance to 0 and set the
   * desired value afterwards:
   * https://github.com/ethereum/EIPs/issues/20#issuecomment-263524729
   *
   * Emits an {Approval} event.
   */
  function approve(address spender, uint256 amount) external returns (bool);

  /**
   * @dev Moves `amount` tokens from `sender` to `recipient` using the
   * allowance mechanism. `amount` is then deducted from the caller's
   * allowance.
   *
   * Returns a boolean value indicating whether the operation succeeded.
   *
   * Emits a {Transfer} event.
   */
  function transferFrom(address sender, address recipient, uint256 amount) external returns (bool);

  /**
   * @dev Emitted when `value` tokens are moved from one account (`from`) to
   * another (`to`).
   *
   * Note that `value` may be zero.
   */
  event Transfer(address indexed from, address indexed to, uint256 value);

  /**
   * @dev Emitted when the allowance of a `spender` for an `owner` is set by
   * a call to {approve}. `value` is the new allowance.
   */
  event Approval(address indexed owner, address indexed spender, uint256 value);
}

/*
 * @dev Provides information about the current execution context, including the
 * sender of the transaction and its data. While these are generally available
 * via msg.sender and msg.data, they should not be accessed in such a direct
 * manner, since when dealing with GSN meta-transactions the account sending and
 * paying for execution may not be the actual sender (as far as an application
 * is concerned).
 *
 * This contract is only required for intermediate, library-like contracts.
 */
contract Context {
  // Empty internal constructor, to prevent people from mistakenly deploying
  // an instance of this contract, which should be used via inheritance.
  constructor ()  { }

  function _msgSender() internal view returns (address payable) {
    return payable(msg.sender);
  }

  function _msgData() internal view returns (bytes memory) {
    this; // silence state mutability warning without generating bytecode - see https://github.com/ethereum/solidity/issues/2691
    return msg.data;
  }
}

/**
 * @dev Wrappers over Solidity's arithmetic operations with added overflow
 * checks.
 *
 * Arithmetic operations in Solidity wrap on overflow. This can easily result
 * in bugs, because programmers usually assume that an overflow raises an
 * error, which is the standard behavior in high level programming languages.
 * `SafeMath` restores this intuition by reverting the transaction when an
 * operation overflows.
 *
 * Using this library instead of the unchecked operations eliminates an entire
 * class of bugs, so it's recommended to use it always.
 */
library SafeMath {
  /**
   * @dev Returns the addition of two unsigned integers, reverting on
   * overflow.
   *
   * Counterpart to Solidity's `+` operator.
   *
   * Requirements:
   * - Addition cannot overflow.
   */
  function add(uint256 a, uint256 b) internal pure returns (uint256) {
    uint256 c = a + b;
    require(c >= a, "SafeMath: addition overflow");

    return c;
  }

  /**
   * @dev Returns the subtraction of two unsigned integers, reverting on
   * overflow (when the result is negative).
   *
   * Counterpart to Solidity's `-` operator.
   *
   * Requirements:
   * - Subtraction cannot overflow.
   */
  function sub(uint256 a, uint256 b) internal pure returns (uint256) {
    return sub(a, b, "SafeMath: subtraction overflow");
  }

  /**
   * @dev Returns the subtraction of two unsigned integers, reverting with custom message on
   * overflow (when the result is negative).
   *
   * Counterpart to Solidity's `-` operator.
   *
   * Requirements:
   * - Subtraction cannot overflow.
   */
  function sub(uint256 a, uint256 b, string memory errorMessage) internal pure returns (uint256) {
    require(b <= a, errorMessage);
    uint256 c = a - b;

    return c;
  }

  /**
   * @dev Returns the multiplication of two unsigned integers, reverting on
   * overflow.
   *
   * Counterpart to Solidity's `*` operator.
   *
   * Requirements:
   * - Multiplication cannot overflow.
   */
  function mul(uint256 a, uint256 b) internal pure returns (uint256) {
    // Gas optimization: this is cheaper than requiring 'a' not being zero, but the
    // benefit is lost if 'b' is also tested.
    // See: https://github.com/OpenZeppelin/openzeppelin-contracts/pull/522
    if (a == 0) {
      return 0;
    }

    uint256 c = a * b;
    require(c / a == b, "SafeMath: multiplication overflow");

    return c;
  }

  /**
   * @dev Returns the integer division of two unsigned integers. Reverts on
   * division by zero. The result is rounded towards zero.
   *
   * Counterpart to Solidity's `/` operator. Note: this function uses a
   * `revert` opcode (which leaves remaining gas untouched) while Solidity
   * uses an invalid opcode to revert (consuming all remaining gas).
   *
   * Requirements:
   * - The divisor cannot be zero.
   */
  function div(uint256 a, uint256 b) internal pure returns (uint256) {
    return div(a, b, "SafeMath: division by zero");
  }

  /**
   * @dev Returns the integer division of two unsigned integers. Reverts with custom message on
   * division by zero. The result is rounded towards zero.
   *
   * Counterpart to Solidity's `/` operator. Note: this function uses a
   * `revert` opcode (which leaves remaining gas untouched) while Solidity
   * uses an invalid opcode to revert (consuming all remaining gas).
   *
   * Requirements:
   * - The divisor cannot be zero.
   */
  function div(uint256 a, uint256 b, string memory errorMessage) internal pure returns (uint256) {
    // Solidity only automatically asserts when dividing by 0
    require(b > 0, errorMessage);
    uint256 c = a / b;
    // assert(a == b * c + a % b); // There is no case in which this doesn't hold

    return c;
  }

  /**
   * @dev Returns the remainder of dividing two unsigned integers. (unsigned integer modulo),
   * Reverts when dividing by zero.
   *
   * Counterpart to Solidity's `%` operator. This function uses a `revert`
   * opcode (which leaves remaining gas untouched) while Solidity uses an
   * invalid opcode to revert (consuming all remaining gas).
   *
   * Requirements:
   * - The divisor cannot be zero.
   */
  function mod(uint256 a, uint256 b) internal pure returns (uint256) {
    return mod(a, b, "SafeMath: modulo by zero");
  }

  /**
   * @dev Returns the remainder of dividing two unsigned integers. (unsigned integer modulo),
   * Reverts with custom message when dividing by zero.
   *
   * Counterpart to Solidity's `%` operator. This function uses a `revert`
   * opcode (which leaves remaining gas untouched) while Solidity uses an
   * invalid opcode to revert (consuming all remaining gas).
   *
   * Requirements:
   * - The divisor cannot be zero.
   */
  function mod(uint256 a, uint256 b, string memory errorMessage) internal pure returns (uint256) {
    require(b != 0, errorMessage);
    return a % b;
  }
}

/**
 * @dev Contract module which provides a basic access control mechanism, where
 * there is an account (an owner) that can be granted exclusive access to
 * specific functions.
 *
 * By default, the owner account will be the one that deploys the contract. This
 * can later be changed with {transferOwnership}.
 *
 * This module is used through inheritance. It will make available the modifier
 * `onlyOwner`, which can be applied to your functions to restrict their use to
 * the owner.
 */
contract Ownable is Context {
  address private _owner;

  event OwnershipTransferred(address indexed previousOwner, address indexed newOwner);

  /**
   * @dev Initializes the contract setting the deployer as the initial owner.
   */
  constructor () {
    address msgSender = _msgSender();
    _owner = msgSender;
    emit OwnershipTransferred(address(0), msgSender);
  }

  /**
   * @dev Returns the address of the current owner.
   */
  function owner() public view returns (address) {
    return _owner;
  }

  /**
   * @dev Throws if called by any account other than the owner.
   */
  modifier onlyOwner() {
    require(_owner == _msgSender(), "Ownable: caller is not the owner");
    _;
  }

  /**
   * @dev Leaves the contract without owner. It will not be possible to call
   * `onlyOwner` functions anymore. Can only be called by the current owner.
   *
   * NOTE: Renouncing ownership will leave the contract without an owner,
   * thereby removing any functionality that is only available to the owner.
   */
  function renounceOwnership() public onlyOwner {
    emit OwnershipTransferred(_owner, address(0));
    _owner = address(0);
  }

  /**
   * @dev Transfers ownership of the contract to a new account (`newOwner`).
   * Can only be called by the current owner.
   */
  function transferOwnership(address newOwner) public onlyOwner {
    _transferOwnership(newOwner);
  }

  /**
   * @dev Transfers ownership of the contract to a new account (`newOwner`).
   */
  function _transferOwnership(address newOwner) internal {
    require(newOwner != address(0), "Ownable: new owner is the zero address");
    emit OwnershipTransferred(_owner, newOwner);
    _owner = newOwner;
  }
}

contract BEP20Token is Context, IBEP20, Ownable {
  using SafeMath for uint256;

  mapping (address => uint256) private _balances;

  mapping (address => mapping (address => uint256)) private _allowances;

  uint256 private _totalSupply;
  uint8 private _decimals;
  string private _symbol;
  string private _name;

  constructor() {
    _name = "Kalika";
    _symbol = "KL";
    _decimals = 18;
    _totalSupply = 5000000000 *10 ** 18;
    _balances[msg.sender] = _totalSupply;

    emit Transfer(address(0), msg.sender, _totalSupply);
  }

  /**
   * @dev Returns the bep token owner.
   */
  function getOwner() external view returns (address) {
    return owner();
  }

  /**
   * @dev Returns the token decimals.
   */
  function decimals() external view returns (uint8) {
    return _decimals;
  }

  /**
   * @dev Returns the token symbol.
   */
  function symbol() external view returns (string memory) {
    return _symbol;
  }

  /**
  * @dev Returns the token name.
  */
  function name() external view returns (string memory) {
    return _name;
  }

  /**
   * @dev See {BEP20-totalSupply}.
   */
  function totalSupply() external view returns (uint256) {
    return _totalSupply;
  }

  /**
   * @dev See {BEP20-balanceOf}.
   */
  function balanceOf(address account) external view returns (uint256) {
    return _balances[account];
  }

  /**
   * @dev See {BEP20-transfer}.
   *
   * Requirements:
   *
   * - `recipient` cannot be the zero address.
   * - the caller must have a balance of at least `amount`.
   */
  function transfer(address recipient, uint256 amount) external returns (bool) {
    _transfer(_msgSender(), recipient, amount);
    return true;
  }

  /**
   * @dev See {BEP20-allowance}.
   */
  function allowance(address owner, address spender) external view returns (uint256) {
    return _allowances[owner][spender];
  }

  /**
   * @dev See {BEP20-approve}.
   *
   * Requirements:
   *
   * - `spender` cannot be the zero address.
   */
  function approve(address spender, uint256 amount) external returns (bool) {
    _approve(_msgSender(), spender, amount);
    return true;
  }

  /**
   * @dev See {BEP20-transferFrom}.
   *
   * Emits an {Approval} event indicating the updated allowance. This is not
   * required by the EIP. See the note at the beginning of {BEP20};
   *
   * Requirements:
   * - `sender` and `recipient` cannot be the zero address.
   * - `sender` must have a balance of at least `amount`.
   * - the caller must have allowance for `sender`'s tokens of at least
   * `amount`.
   */
  function transferFrom(address sender, address recipient, uint256 amount) external returns (bool) {
    _transfer(sender, recipient, amount);
    _approve(sender, _msgSender(), _allowances[sender][_msgSender()].sub(amount, "BEP20: transfer amount exceeds allowance"));
    return true;
  }

  /**
   * @dev Atomically increases the allowance granted to `spender` by the caller.
   *
   * This is an alternative to {approve} that can be used as a mitigation for
   * problems described in {BEP20-approve}.
   *
   * Emits an {Approval} event indicating the updated allowance.
   *
   * Requirements:
   *
   * - `spender` cannot be the zero address.
   */
  function increaseAllowance(address spender, uint256 addedValue) public returns (bool) {
    _approve(_msgSender(), spender, _allowances[_msgSender()][spender].add(addedValue));
    return true;
  }

  /**
   * @dev Atomically decreases the allowance granted to `spender` by the caller.
   *
   * This is an alternative to {approve} that can be used as a mitigation for
   * problems described in {BEP20-approve}.
   *
   * Emits an {Approval} event indicating the updated allowance.
   *
   * Requirements:
   *
   * - `spender` cannot be the zero address.
   * - `spender` must have allowance for the caller of at least
   * `subtractedValue`.
   */
  function decreaseAllowance(address spender, uint256 subtractedValue) public returns (bool) {
    _approve(_msgSender(), spender, _allowances[_msgSender()][spender].sub(subtractedValue, "BEP20: decreased allowance below zero"));
    return true;
  }

  /**
   * @dev Creates `amount` tokens and assigns them to `msg.sender`, increasing
   * the total supply.
   *
   * Requirements
   *
   * - `msg.sender` must be the token owner
   */
  function mint(uint256 amount) public onlyOwner returns (bool) {
    _mint(_msgSender(), amount);
    return true;
  }

  /**
   * @dev Moves tokens `amount` from `sender` to `recipient`.
   *
   * This is internal function is equivalent to {transfer}, and can be used to
   * e.g. implement automatic token fees, slashing mechanisms, etc.
   *
   * Emits a {Transfer} event.
   *
   * Requirements:
   *
   * - `sender` cannot be the zero address.
   * - `recipient` cannot be the zero address.
   * - `sender` must have a balance of at least `amount`.
   */
  function _transfer(address sender, address recipient, uint256 amount) internal {
    require(sender != address(0), "BEP20: transfer from the zero address");
    require(recipient != address(0), "BEP20: transfer to the zero address");

    _balances[sender] = _balances[sender].sub(amount, "BEP20: transfer amount exceeds balance");
    _balances[recipient] = _balances[recipient].add(amount);
    emit Transfer(sender, recipient, amount);
  }

  /** @dev Creates `amount` tokens and assigns them to `account`, increasing
   * the total supply.
   *
   * Emits a {Transfer} event with `from` set to the zero address.
   *
   * Requirements
   *
   * - `to` cannot be the zero address.
   */
  function _mint(address account, uint256 amount) internal {
    require(account != address(0), "BEP20: mint to the zero address");

    _totalSupply = _totalSupply.add(amount);
    _balances[account] = _balances[account].add(amount);
    emit Transfer(address(0), account, amount);
  }

  /**
   * @dev Destroys `amount` tokens from `account`, reducing the
   * total supply.
   *
   * Emits a {Transfer} event with `to` set to the zero address.
   *
   * Requirements
   *
   * - `account` cannot be the zero address.
   * - `account` must have at least `amount` tokens.
   */
  function _burn(address account, uint256 amount) internal {
    require(account != address(0), "BEP20: burn from the zero address");

    _balances[account] = _balances[account].sub(amount, "BEP20: burn amount exceeds balance");
    _totalSupply = _totalSupply.sub(amount);
    emit Transfer(account, address(0), amount);
  }

  /**
   * @dev Sets `amount` as the allowance of `spender` over the `owner`s tokens.
   *
   * This is internal function is equivalent to `approve`, and can be used to
   * e.g. set automatic allowances for certain subsystems, etc.
   *
   * Emits an {Approval} event.
   *
   * Requirements:
   *
   * - `owner` cannot be the zero address.
   * - `spender` cannot be the zero address.
   */
  function _approve(address owner, address spender, uint256 amount) internal {
    require(owner != address(0), "BEP20: approve from the zero address");
    require(spender != address(0), "BEP20: approve to the zero address");

    _allowances[owner][spender] = amount;
    emit Approval(owner, spender, amount);
  }

  /**
   * @dev Destroys `amount` tokens from `account`.`amount` is then deducted
   * from the caller's allowance.
   *
   * See {_burn} and {_approve}.
   */
  function _burnFrom(address account, uint256 amount) internal {
    _burn(account, amount);
    _approve(account, _msgSender(), _allowances[account][_msgSender()].sub(amount, "BEP20: burn amount exceeds allowance"));
  }
}
