# 💾 `cfdisk` - Partition Table Editor

## Description
The `cfdisk` command is a text-based partitioning tool used to create, delete, and modify partitions on a disk. It provides a user-friendly interface to manage disk partitions.

---

## 🚀 Usage

```bash
cfdisk [options] [device]
```

## Options

- **options**: Flags to modify the behavior of `cfdisk`.
- **device**: The disk or partition to be edited (e.g., `/dev/sda`).

## Common Options

- `-z`: Reset the partition table to empty (destructive).
- `-h`: Show help.
- `-l`: List the available partitions.

## 📊 Examples
1. Launch cfdisk on a specific device
Run cfdisk on a device (e.g., /dev/sda) to view and modify the partition table.
```bash
cfdisk /dev/sda
```
- Example:
  - Running cfdisk will display an interactive menu with available partitions and free space.

## 2. List the current partitions
To list the partitions on a disk without editing, use the -l option.
```bash
cfdisk -l
```
### Example Output:
```bash
Disk /dev/sda: 500 GB, 500107862016 bytes
Device    Boot   Start       End    Sectors   Size   Type
/dev/sda1 *     2048      1026047 1024000   500M   Linux filesystem
/dev/sda2      1026048  500107863 499855816 238.2G Linux filesystem
```

### 3. Use cfdisk with the -z option (destructive)
If you want to completely reset the partition table (this will erase all data on the disk), you can use the -z option.
```bash
cfdisk -z /dev/sda
```
- Example:
  - This command will clear all partitions and reset the partition table on /dev/sda. Be careful as this is destructive!
 
## 4. Use cfdisk in non-interactive mode (only to create or delete partitions)
While cfdisk is primarily used interactively, it can be scripted in some cases using the -z option to erase or -l to list partitions.

## 📝 Notes
cfdisk requires root privileges to modify the partition table. Use sudo to execute the command if necessary.

Always back up important data before modifying partitions to avoid accidental data loss.

## 🔒 Conclusion
The cfdisk command is a powerful and simple-to-use partitioning tool for Linux users. It provides a straightforward interface for managing partitions, allowing users to create, delete, and resize partitions with ease.

For more detailed partitioning tasks, you may need to use tools like parted or gparted.

---

# 🛑 `wipefs` - The `wipefs` command in Linux is used to wipe (erase) file system signatures from a device or partition.

## Usage:
```bash
wipefs [options] <device>
```
- **<device>**: The disk or partition on which to remove the file system signatures (e.g., `/dev/sda1`).

## Common Options:

- `-a` or `--all`: Wipes all detected signatures (default if no signature type is specified).
- `-f` or `--force`: Forces the wiping of file system signatures without prompting for confirmation.
- `-n` or `--no-act`: Simulates the action without actually making changes (dry-run).
- `-t <type>` or `--type <type>`: Specify the type of filesystem to wipe, such as `ext4`, `xfs`, `btrfs`, etc. You can wipe specific filesystem signatures instead of all.
- `-l` or `--list`: Lists the detected file system signatures on the device without actually wiping anything.

## Examples:
1. Wipe all filesystem signatures from a device
This command wipes all filesystem signatures (including partition tables) from the device /dev/sda.
```bash
sudo wipefs /dev/sda
```

## 2. Wipe a specific file system signature
This command wipes only the ext4 file system signature from the device /dev/sda1.
```bash
sudo wipefs -t ext4 /dev/sda1
```

## 3. Force wipe all signatures
This command wipes all detected file system signatures from the device /dev/sda, without any confirmation prompts.
```bash
sudo wipefs -f /dev/sda
```

## 4. Simulate the wipe operation (dry-run)
This command will show you what will be wiped but won't actually perform any changes. It's useful for testing what would happen before running the actual command.
```bash
sudo wipefs -n /dev/sda
```

## 5. List filesystem signatures
This command lists all detected filesystem signatures on the device /dev/sda without wiping anything.
```bash
sudo wipefs -l /dev/sda
```

## Why Use `wipefs`?

- **Clean Disk Before Reformatting**: Before creating new filesystems or partitions, you can use `wipefs` to remove the old filesystem signatures.
- **Erase File System Information**: If you're planning to sell or dispose of a disk and want to ensure that no filesystem information is left behind, `wipefs` can help you clear that.
- **Fix Corrupted Filesystems**: Sometimes, corrupted filesystem signatures may prevent the system from recognizing the partition correctly. Running `wipefs` can help fix this.

## Important Considerations:

- **Does not wipe data**: It only removes the filesystem signatures and metadata; the actual data on the disk is still there. If you need to securely erase data, you will need other tools like `shred` or `dd`.
- **Be cautious**: `wipefs` can remove partition tables and filesystems, rendering the partition unreadable until it's reformatted. Always double-check the device you are working with to avoid accidental data loss.

---

In summary, `wipefs` is a tool to remove file system signatures, making the disk appear unformatted or allowing you to prepare a disk for new partitions and filesystems.
