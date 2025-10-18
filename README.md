# Cross-platform-Linux-Unix-Windows-use-Pascal-IDE

//To use

{$IFNDEF WIN32}

    // Original code
    
{$ELSE} // !_WIN32

    // Linux code
    
{$ENDIF} // _WIN32


//Example 01

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

//Example 02
uses
{$ifdef FPC}
  ZStream,
{$else}
  ZLib,
{$endif}
  synafpc,
  Classes, SysUtils, synautil;
