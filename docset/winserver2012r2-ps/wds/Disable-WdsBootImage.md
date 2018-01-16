---
external help file: MSFT_WdsBootImage_v1.0.cdxml-help.xml
Module Name: WDS
online version: 
schema: 2.0.0
title: Disable-WdsBootImage
description: 
keywords: powershell, cmdlet
author: brianlic
manager: alanth
ms.date: 2017-10-30
ms.topic: reference
ms.prod: powershell
ms.technology: powershell
ms.assetid: F5843663-6E03-403E-BE78-7F57843B028A
---

# Disable-WdsBootImage

## SYNOPSIS
Disables a boot image.

## SYNTAX

```
Disable-WdsBootImage -ImageName <String> [-FileName <String>] -Architecture <Architecture>
 [-CimSession <CimSession[]>] [-ThrottleLimit <Int32>] [-AsJob] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Disable-WdsBootImage** cmdlet disables a boot image in the Windows Deployment Services Image Store.
When you disable a boot image, Windows Deployment Services does not offer the boot image to clients that use Pre-Boot Execution Environment (PXE) to boot to the Windows Deployment Services server.
You can add driver packages to a boot image while it is disabled.

Specify the boot image by using the **ImageName** and **Architecture** parameters.
If the image name and architecture do not uniquely identify the image, also specify the **FileName** parameter.

## EXAMPLES

### Example 1: Disable a boot image for the x86 architecture
```
PS C:\> Disable-WdsBootImage -Architecture x86 -ImageName "Fabrikam LOB setup (x86)"
```

This command disables the boot image named Fabrikam LOB setup (x86) for the x86 architecture.

## PARAMETERS

### -Architecture
Specifies an architecture.
This is the architecture of the boot image.
Because you can use the same image name for boot images in different architectures, specify this this parameter to ensure that you disable the correct image.
The acceptable values for this parameter are:

- ARM
- ia64
- x64
- x86

```yaml
Type: Architecture
Parameter Sets: (All)
Aliases: 
Accepted values: X86, Ia64, X64, Arm

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AsJob
ps_cimcommon_asjob

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CimSession
Runs the cmdlet in a remote session or on a remote computer.
Enter a computer name or a session object, such as the output of a New-CimSessionhttp://go.microsoft.com/fwlink/p/?LinkId=227967 or Get-CimSessionhttp://go.microsoft.com/fwlink/p/?LinkId=227966 cmdlet.
The default is the current session on the local computer.

```yaml
Type: CimSession[]
Parameter Sets: (All)
Aliases: Session

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FileName
Specifies a file name.
This is the file name of the boot image.
Use this parameter to specify the file name for the boot image if the boot image name does not uniquely identify the image.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ImageName
Specifies the name of an image.
This is the name of the image to disable.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ThrottleLimit
Specifies the maximum number of concurrent operations that can be established to run the cmdlet.
If this parameter is omitted or a value of `0` is entered, then Windows PowerShell® calculates an optimum throttle limit for the cmdlet based on the number of CIM cmdlets that are running on the computer.
The throttle limit applies only to the current cmdlet, not to the session or to the computer.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Shows what would happen if the cmdlet runs. The cmdlet is not run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### Microsoft.Management.Infrastructure.CimInstance#MSFT_WdsBootImage

## NOTES

## RELATED LINKS

[Get-WdsBootImage](./Get-WdsBootImage.md)

[Set-WdsBootImage](./Set-WdsBootImage.md)

[Enable-WdsBootImage](./Enable-WdsBootImage.md)

[Remove-WdsBootImage](./Remove-WdsBootImage.md)

[Import-WdsBootImage](./Import-WdsBootImage.md)

[Export-WdsBootImage](./Export-WdsBootImage.md)
