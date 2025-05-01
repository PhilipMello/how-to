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
