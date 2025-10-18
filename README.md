# Cross-platform-Linux-Unix-Windows-use-Pascal-IDE

//To use
#ifdef _WIN32
    // Original code
#else // !_WIN32
    // Linux code
#endif // _WIN32

//Example
uses
{$IFNDEF WIN32}
  {$IFNDEF NO_LIBC}
  Libc,
  KernelIoctl,
  {$ELSE}
  termio, baseunix, unix,
  {$ENDIF}
  {$IFNDEF FPC}
  Types,
  {$ENDIF}
{$ELSE}
  Windows, registry,
  {$IFDEF FPC}
  winver,
  {$ENDIF}
{$ENDIF}
  synafpc,
  Classes, SysUtils, synautil;
