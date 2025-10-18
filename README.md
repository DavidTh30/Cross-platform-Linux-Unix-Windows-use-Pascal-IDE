# Cross-platform-Linux-Unix-Windows-use-Pascal-IDE
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
