mp3cleaner - tool to rename filenames and cleanup id3 tags on mp3 file
    Usage:
    -h --help              Prints this
    -v --version           Prints version
    -a --action            rename (removes the expression from file name)
                           cleantag (removes the expression from id3 tags)
    -t --target            target to process.
                           target can be either a file or a directory
                           If not set will process current directory
    -e --expression        Expression to clean from the ID3 tags
    -p --print             Print all current [tags|filename] of target
                           this option ignores investigation
    -c --compare           Print prospective changes to [tags|filename] to target
                           Ignore this flag to make the change
    -i --investiagate      Print current id3 tags and filename of target

    Example 1:

    % mp3cleaner -a cleantag -t /opt/music/album -e "STRING"

    The above command will traverse the path /opt/music/album and will
    remove the expression STRING from all ID3 tags.

    If the -t tag is not used, the action will happen on current directory

    Example 2:

    % mp3cleaner -a rename -t /opt/music/album -e "STRING"

    The above command will traverse the path /opt/music/album and will
    remove the expression STRING from all file names.

    If the -t tag is not used, the action will happen on current directory

    Example 3:

    % mp3cleaner -t /opt/music/album -i

    The above command will traverse the path and will display current id3 tags
    and filenames. The path can also be a filename.

    If the -t tag is not used, the action will happen on current directory

    Example 4:

    % mp3cleaner -a cleantag -t /opt/music/album -e "String" -c

    The above command will display the comparison of cleaned up filename or
    id3 tags.

    If the -t tag is not used, the action will happen on current directory