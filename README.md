# fictional-carnival - just a random name provided by Github

## Generating new programID for our Program

1. `rm $HOME/.config/solana/id.json` - This will remove the Solana CLI wallet

2. `rm $HOME/.config/solana/cli/config.yml` - This will remove the config.yml file

3. set the provier to localhost first `solana config set --url localhost` This is useful

4. we need to delete the generated keypair fromm the project file from the target deploy folder. As the program did not get deployed,
   our ProgramID got stuck now and we can't append it anymore! So we need a new keypair!

5. make sure we are in 	`myepicproject` folder. from there type `rm target/deploy/myepicproject-keypair.json myepicproject.so` This will remove
   both the keypair file and the program we builded earlier.

6. Now we need to create a new keypair file in Solana CLI so that we can use it for deploy! Type `solana-keyegen new` and then hit ENTER!
   You can enter a password for the file, but I recommend not to do so.

7. `solana airdrop 2` to get some fake SOL. Enter this command as many times as you want

8. we need a new keypair file in the deploy/target folder so that we get a programID for our lib.rs file to be deployed on the devent. for that make sure we are in `myepicproject` folder. We need to make changes in two of the files, named `lib.rs` (location - `programs/src/lib.rs`) and ``Anchor.toml``

9. copy and paste the files I have provided in their desired location. This files are the original files we get before building, deploying that stuff!!

10. `solana config get` and make sure we are on localhost. Now type `anchor test`, just to check that our program is working and we are getting the correct output.

11. If we are getting the desired output after testing, we are all good!
