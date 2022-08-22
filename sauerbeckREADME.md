@echo off
cls
:menu
cls

echo               MENU TAREFAS
echo * 1 - Limpar temporarios
echo * 2 - Montar versao do Sistema Operacional
echo * 3 - Help
echo * 4 - Sair

set /p opcao= Eschola a opcao:
echo
if %opcao% equ 1 goto opcao1
if %opcao% equ 2 goto opcao2
if %opcao% equ 3 goto opcao3
if %opcao% equ 4 goto opcao4

:opcao1
cls
del /s /f /q c:\windows\temp\*.*
rd /s /q c:\windows\temp
md c:\windows\temp
del /s /f /q C:\WINDOWS\Prefetch
del /s /f /q C:\Windows\SoftwareDistribution\Download
del /s /f /q %temp%\*.*
rd /s /q %temp%
md %temp%
deltree /y c:\windows\tempor~1
deltree /y c:\windows\temp
deltree /y c:\windows\tmp
deltree /y c:\windows\ff*.tmp
deltree /y c:\windows\history
deltree /y c:\windows\cookies
deltree /y c:\windows\recent
deltree /y c:\windows\spool\printers
del c:\WIN386.SWP
echo -----------------------------------
echo -       TEMPORARIO LIMPOS         -
echo -----------------------------------
pause
goto menu

:opcao2
cls
winver
pause
goto menu

:opcao3
cls
echo ----------------------------------------------------------
echo - Digite o numero desejado para executar a acao desejada -
echo ----------------------------------------------------------
pause
goto menu

opcao4
cls
exit

