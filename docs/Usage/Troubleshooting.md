# Level Sequence Playback Issues

## Context

During development, we observed some behavior where if there was a Level Sequence on the level already with Auto Play enabled it would conflict with the Test Manager.

The Test Manager creates a new Level Sequence Actor based with custom settings instead of using any pre-existing Level Sequence Actor on the level. This is to minimize any weird configuration errors stemming from parameters not controlled by Test Manager.

## Fix

To resolve any weird playback issues, remove any extra Level Sequences or disable automatic playback on them.

# Multiple Test Managers

Not currently supported. Will look to add a warning about multiple Test Managers.

# Passing Score Appears Lower Than Expected

## Context
The [[Score System]] is based on the total frame count of the Level Sequence. By default, Level Sequences are created at 30 FPS and our plugin should automatically detect and multiply that value by 2x to account for the 60FPS target.

However, non-standard FPS targets are not supported but will continue to be accepted. We have added some log warnings to help raise visibility to this potential issue.

We may also look into alternatives on how to calculate passing score criterias so that setup continues to need minimal effort.

## Fix

To resolve the passing score being lower than expected, developers should adjust the Sequence Display Rate of the Level Sequence being used for the Performance Benchmark. Our plugin can account for values of 30, 60 and 120 FPS, but we recommend selecting 60 FPS.

![[SequenceDisplayRateFix.png]]
