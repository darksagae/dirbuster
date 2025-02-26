# dirbuster
DirBuster is a powerful directory and file brute-forcing tool included in Kali Linux. It is used to find hidden directories and files on web servers by launching a dictionary attack. Here’s how to use it, along with examples and expected outputs.

### Installation

DirBuster is usually pre-installed in Kali Linux. If it’s not available, you can install it using:

```bash
sudo apt update
sudo apt install dirbuster
```

### Basic Usage

DirBuster can be run from the command line or through its graphical user interface (GUI). To launch the GUI, you can simply type:

```bash
dirbuster
```

### Basic Options

When using DirBuster, you can set various options:

- **Target URL**: The URL of the website you want to scan.
- **Wordlist**: A list of common directory and file names to search for.
- **File Extensions**: Specify any file extensions to include in the scan.
- **Request Method**: Choose between GET or POST requests.
- **Threads**: Set the number of concurrent threads for faster scanning.

### Examples

#### Example 1: Basic Scan Using GUI

1. Open DirBuster from the applications menu or terminal.
2. Enter the target URL, e.g., `http://example.com`.
3. Select a wordlist from the built-in options.
4. Click "Start" to begin the scan.

**Expected Output**:
DirBuster will display found directories and files in real-time. The output might look like this:

```
Found: /images/ (200)
Found: /css/ (200)
Found: /index.html (200)
Found: /admin/ (403)
```

#### Example 2: Command Line Usage

You can also run DirBuster from the command line using:

```bash
java -jar dirbuster.jar -u http://example.com -l /path/to/wordlist.txt -t 20
```

**Expected Output**:
The command will scan the specified URL using the provided wordlist and show results similar to the GUI output:

```
---- Scanning URL: http://example.com/ ----
+ /index.php (200)
+ /admin/ (403)
+ /uploads/ (200)
```

### Additional Options

- **-e**: To specify file extensions to search for, e.g., `-e .php,.html`.
- **-r**: To enable recursive scanning of found directories.
- **-o**: To save the output to a specified file.

### Conclusion

DirBuster is a robust tool for discovering hidden files and directories on web servers. By utilizing various wordlists and options, you can tailor your scans for effective results. Always ensure you have permission to scan the target website to avoid legal issues.


                                ALTERNATIVE
### DirBuster: Directory Buster Tool in Kali Linux

DirBuster is a multi-threaded Java application used to brute-force directories and files on web servers. It is particularly effective for discovering hidden resources.

### Installation

DirBuster is typically pre-installed in Kali Linux. If it’s not installed, you can use:

```bash
sudo apt update
sudo apt install dirbuster
```

### Basic Usage

1. **Launching DirBuster**

   You can start DirBuster from the terminal by typing:

   ```bash
   dirbuster
   ```

   Alternatively, you can find it in the applications menu under the "Web Applications" section.

2. **Setting Up a Scan**

   - **Target URL**: Enter the URL of the target website (e.g., `http://example.com`).
   - **Wordlist**: Select a wordlist to use for the scan. DirBuster comes with several pre-installed wordlists located in `/usr/share/dirb/wordlists`.

3. **Options**:
   - **File Extensions**: You can specify file extensions to search for (e.g., `.php`, `.html`).
   - **Number of Threads**: Adjust the number of threads for the scan to control the speed.
   - **Recursive Scanning**: Enable this option to scan directories found during the initial scan.

### Examples

#### Example 1: Basic Scan

1. **Target**: `http://example.com`
2. **Wordlist**: Use the default wordlist.

**Expected Output**:
```
Scanning URL: http://example.com/
Found: /index.php (200)
Found: /admin/ (301)
Found: /uploads/ (200)
```

#### Example 2: Specifying File Extensions

1. **Target**: `http://example.com`
2. **Wordlist**: Default wordlist
3. **File Extensions**: `.php`

**Expected Output**:
```
Scanning URL: http://example.com/
Found: /index.php (200)
Found: /login.php (200)
```

#### Example 3: Recursive Scan

1. **Target**: `http://example.com`
2. **Wordlist**: Default wordlist
3. **Enable Recursive Scanning**

**Expected Output**:
```
Scanning URL: http://example.com/
Found: /images/ (301)
Scanning URL: http://example.com/images/
Found: /images/logo.png (200)
```

### Conclusion

DirBuster is a powerful tool for discovering hidden directories and files on web servers. By using various options and custom wordlists, you can tailor your scans for effective reconnaissance. Always ensure you have permission to scan the target website to avoid legal issues.



                          ALTERNATIVE
Understood. Here is how to use the dirbuster tool in Kali Linux, along with examples and expected outputs:

### What is dirbuster?

dirbuster is a GUI-based web content discovery tool included in the Kali Linux distribution. It is used to find hidden web directories and files on web servers by brute-forcing URLs.

### Installation

dirbuster is typically pre-installed in Kali Linux. If it's not installed, you can install it using the following command:

```bash
sudo apt update
sudo apt install dirbuster
```

### Basic Usage

To start dirbuster, you can launch it from the Kali Linux application menu or run the following command in the terminal:

```bash
dirbuster
```

This will open the dirbuster GUI, where you can configure the scan settings.

### Examples

#### Example 1: Basic Scan of a Website

1. In the dirbuster GUI, enter the target URL in the "URL to scan" field, e.g., `http://example.com`.
2. Select the wordlist you want to use for the scan. dirbuster comes with several built-in wordlists, or you can choose a custom wordlist.
3. Click the "Start" button to begin the scan.

**Expected Output:**
dirbuster will display a list of discovered directories and files on the target website. The output will show the URL, HTTP response code, and file size for each discovered resource.

#### Example 2: Scan with a Custom Wordlist

1. In the dirbuster GUI, enter the target URL in the "URL to scan" field.
2. Click the "Select" button next to the "Wordlist" field and navigate to the custom wordlist file you want to use, e.g., `/path/to/your/custom/wordlist.txt`.
3. Click the "Start" button to begin the scan.

**Expected Output:**
The scan results will be based on the content of the custom wordlist you provided, which may differ from the results of the default wordlist.

#### Example 3: Recursive Scan

1. In the dirbuster GUI, enter the target URL in the "URL to scan" field.
2. Check the "Recursive" option.
3. Click the "Start" button to begin the recursive scan.

**Expected Output:**
dirbuster will scan not only the base URL but also the directories found during the scan, providing a more in-depth exploration of the target website.

### Additional Options

dirbuster offers several other options that you can configure, such as:

- Specifying a proxy server
- Limiting the scan to certain file extensions
- Excluding specific directories or files from the scan
- Adjusting the number of threads used for the scan
- Saving the scan results to a file

You can explore these options in the dirbuster GUI or by consulting the tool's documentation.

Remember to always use dirbuster (and any web scanning tool) responsibly and with permission, as unauthorized scanning can be considered illegal in some jurisdictions.



                               ALTERNATIVE
DirBuster is a GUI-based tool in Kali Linux used for brute-forcing directories and files on a web server. It's not the same as DIRB, which is a command-line tool. Here's how to use DirBuster:

**Starting DirBuster**

Open DirBuster in Kali Linux by navigating to Applications > Web Application Analysis > Web Crawlers > DirBuster.

**Basic Usage**

1. Enter the target URL in the "Target URL" field.
2. Select a wordlist from the "Wordlist" dropdown menu or provide a custom wordlist file.
3. Choose the number of threads (default is 10).
4. Click "Start" to begin the scan.

**Examples**

1. **Basic Scan**

Target URL: `http://example.com`
Wordlist: `default_wordlist.txt`

 Output: DirBuster will display a list of found directories and files, including hidden ones.

2. **Custom Wordlist Scan**

Target URL: `http://example.com`
Wordlist: `/usr/share/wordlists/dirb/common.txt`

Output: DirBuster will use the custom wordlist to scan the target and display the results.

3. **Recursive Scan**

Target URL: `http://example.com`
Wordlist: `default_wordlist.txt`
Recursive: Enabled

Output: DirBuster will recursively scan the target and display the results, including directories within found directories.

**Output**

The output will display a list of found directories and files, including their HTTP status codes and sizes. The output may look like this:

```
http://example.com/admin/ (200)
http://example.com/images/ (200)
http://example.com/index.php (200)
http://example.com/css/style.css (200)
```

**Tips**

* Always ensure you have permission to scan the target website.
* Be cautious when using DirBuster, as it can generate a significant amount of traffic and potentially lead to detection.
* Analyze the output carefully to identify potential vulnerabilities or sensitive information.

Note that DirBuster is a GUI-based tool, so the usage and output may differ from the command-line tool DIRB.




         DirBuster is a powerful tool included in Kali Linux that is used for brute-forcing directories and files on web servers. It is particularly useful for discovering hidden resources that may not be linked on the website. Here’s how to use DirBuster, along with examples and expected outputs.

### Installation

DirBuster is typically pre-installed in Kali Linux. If it is not available, you can install it using the following command:

```bash
sudo apt update
sudo apt install dirbuster
```

### Basic Usage

DirBuster can be run from the command line or through its graphical user interface (GUI). The basic command-line syntax is:

```bash
dirbuster -u <url> -w <wordlist>
```

- `-u <url>`: The target URL you want to scan.
- `-w <wordlist>`: The path to the wordlist file you want to use for brute-forcing.

### Examples

#### Example 1: Basic Directory Scan

To perform a basic scan on a website using a default wordlist:

```bash
dirbuster -u http://example.com -w /usr/share/wordlists/dirb/common.txt
```

**Expected Output:**

The output will display a list of found directories and files, including their HTTP response codes. For example:

```
Found: /admin/ (Status: 200)
Found: /uploads/ (Status: 200)
Found: /config.php (Status: 403)
```

#### Example 2: Using a Custom Wordlist

You can specify a custom wordlist to target specific directories or files:

```bash
dirbuster -u http://example.com -w /path/to/custom_wordlist.txt
```

**Expected Output:**

The results will depend on the contents of the custom wordlist. You might see:

```
Found: /images/ (Status: 200)
Found: /backup/ (Status: 200)
```

#### Example 3: Recursive Scanning

To enable recursive scanning, which will look for directories within found directories, you can use the GUI option or specify it in the command line if supported.

**Expected Output:**

The output will show additional layers of directories if they are found:

```
Found: /admin/settings/ (Status: 200)
Found: /admin/settings/config/ (Status: 403)
```

#### Example 4: Saving Output to a File

To save the results of the scan to a file for later analysis:

```bash
dirbuster -u http://example.com -w /usr/share/wordlists/dirb/common.txt -o output.txt
```

**Expected Output:**

The scan results will be saved in `output.txt`, which you can review later.

### Conclusion

DirBuster is a robust tool for discovering hidden directories and files on web servers. By using different wordlists and options, you can tailor your scans to uncover valuable information for security assessments. Always ensure you have permission before scanning any web application.

---
Learn more:
1. [dirb | Kali Linux Tools](https://www.kali.org/tools/dirb/)
2. [Introduction to Dirb - Kali Linux - GeeksforGeeks](https://www.geeksforgeeks.org/introduction-to-dirb-kali-linux/)
3. [Comprehensive Guide on Dirb Tool - Hacking Articles](https://www.hackingarticles.in/comprehensive-guide-on-dirb-tool/)                       ALTERNATIVE
