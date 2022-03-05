# Brownie Simple Storage

## Pre-reqs
**source:** https://github.com/eth-brownie/brownie

1. Install brownie

```bash
    pip install eth-brownie
```
   
> NOTES:
>  
>   - Tried using pipx with Windows 10, but ran into a few issues.
> 
>   - Needed to add system environment variable for brownie - restart required

---

## Notes

- Natively integrate account into brownie

    ```bash
    brownie accounts new <account-name>
    ```

- Delete account from brownie

    ```bash
    brownie accounts delete <account-name>
    ```

- List accounts from brownie

    ```bash
    brownie accounts list
    ```
- When running tests (pytest)...

    ```bash
    brownie test # complete test

    brownie test -k <testname> # test one particular test

    brownie test --pdb # returns a terminal

    brownie test -s # complete test with print lines

    Sample output:

        tests/test_simple_storage.py::test_deploy PASSED
        tests/test_simple_storage.py::test_updating_storage PASSED

        ================= 2 passed in 8.46s ======================== 
            
    ```
- List available network
  
  ```bash
  brownie networks list
  ```

- Deploy to a testnet
    
    Add your WEB3_INFURA_PROJECT_ID from Infura to your .env 

    ```bash
    brownie run scripts/deploy.py --network rinkeby
    ```

- Run

    ```bash
    brownie run script/deploy.py
    ```

- Interactive brownie console

    ```bash
    brownie console

    quit()
    ```