+++
author = "Alexey Kondratov"
title = "Test Post"
date = "2025-04-06"
description = "Test Post."
tags = [
    "markdown",
    "code",
]
+++

Donec lorem urna, condimentum sit amet suscipit sit amet, varius sed ipsum. Phasellus sem leo, elementum in ultricies nec, aliquam a dolor. Pellentesque et lectus nulla. Vestibulum risus quam, porta nec erat eu, laoreet consectetur metus. Proin lacinia ultrices faucibus. Aliquam erat volutpat. Vivamus nisl urna, tristique sed tortor non, condimentum rhoncus lectus. Quisque venenatis a neque in mollis. Ut molestie ligula nec felis condimentum, eu imperdiet sapien facilisis. Morbi in consectetur lacus, non placerat arcu.

Maecenas laoreet magna ut ullamcorper aliquet. Cras vulputate aliquet libero, pharetra ultricies felis tempor ut. Vivamus et rhoncus tellus, nec sagittis odio. Nam sit amet dolor massa. Etiam in velit sapien. Nullam ullamcorper justo lacus, et sollicitudin felis euismod vitae. Morbi eget massa sit amet tellus mollis euismod vitae in urna. Phasellus commodo, est at varius feugiat, nibh leo molestie massa, vitae venenatis neque nibh sed lectus. Donec ut massa tortor.

```c
/*
 * Write a piece of ptrack map to file and update CRC32 value.
 */
static void
ptrack_write_chunk(int fd, pg_crc32c *crc, char *chunk, size_t size)
{
	COMP_CRC32C(*crc, (char *) chunk, size);

	if (write(fd, chunk, size) != size)
	{
		/* If write didn't set errno, assume problem is no disk space */
		if (errno == 0)
			errno = ENOSPC;

		ereport(ERROR,
				(errcode_for_file_access(),
				 errmsg("could not write file \"%s\": %m", PTRACK_PATH_TMP)));
	}
}
```
