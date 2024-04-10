# SHA1 Cracker

SHA1 Cracker is a command-line tool that searches for a password in a wordlist based on its SHA1 hash.

## Prerequisites

Rust programming language (https://www.rust-lang.org/tools/install)

## Usage

- Clone the repository or download the source code files.

- Open a terminal or command prompt and navigate to the project directory.

- Build and run the program by executing the following command:

```shell
cargo run --release -- <wordlist> <sha1_hash>
```

Replace <wordlist> with the path to the file containing the list of passwords to search, and <sha1_hash> with the SHA1 hash of the password you want to find.

- The program will compare each line in the wordlist file to the provided SHA1 hash. If a match is found, it will display the corresponding password and terminate. If no match is found, it will indicate that the password was not found in the wordlist.

## Example

Suppose you have a wordlist file named "wordlist.txt" containing a list of passwords, and you want to find the password that corresponds to the SHA1 hash "5baa61e4c9b93f3f0682250b6cf8331b7ee68fd8". You can run the program as follows:

```shell
cargo run --release -- wordlist.txt 5baa61e4c9b93f3f0682250b6cf8331b7ee68fd8
```

If the password is present in the wordlist, the program will display the following output:

```shell
Password found: password123
```

Otherwise, it will display:

```shell
Password not found in wordlist
```

## Dependencies

The program relies on the following external crates:

- sha1 (version 0.6.0): A library for computing the SHA1 hash function.
- hex (version 0.4.3): A library for encoding and decoding hexadecimal values.
  These dependencies will be automatically fetched and managed by Cargo, the Rust package manager.
