---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 53BD6ED4-EA66-448B-8B18-F078C0738AF5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 90f02a261dc804f46a7ef503879a8ce9f43fad35
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/08/2020
ms.locfileid: "94030862"
---
# New-WAPackQuickVM

## Sinossi
Crea una macchina virtuale basata su un modello.

## SINTASSI

```
New-WAPackQuickVM -Name <String> -Template <VMTemplate> -VMCredential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Descrizione
Questi argomenti sono deprecati e verranno rimossi in futuro.
Questo argomento descrive il cmdlet nella versione 0.8.1 del modulo PowerShell di Microsoft Azure.
Per scoprire la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .

Il cmdlet **New-WAPackQuickVM** crea una macchina virtuale basata su un modello.

## ESEMPI

### Esempio 1: creare una macchina virtuale basata su un modello
```
PS C:\> $Credentials = Get-Credential
PS C:\> $TemplateId = Get-WAPackVMTemplate -Id 66242D17-189F-480D-87CF-8E1D749998C8
PS C:\> New-WAPackQuickVM -Name "VirtualMachine023" -Template $TemplateId -VMCredential $Credentials
```

Il primo comando crea un oggetto **PSCredential** e lo archivia nella variabile $Credentials.
Il cmdlet richiede l'accesso a un account e una password.
Per altre informazioni, digitare `Get-Help Get-Credential` .

Il secondo comando ottiene un modello usando il cmdlet **Get-WAPackVMTemplate** .
Il comando specifica l'ID di un modello.
Il comando Archivia l'oggetto modello nella variabile $TemplateID.

Il comando finale crea una macchina virtuale denominata VirtualMachine023.
Il comando basa la macchina virtuale nel modello archiviato in $TemplateId.

## PARAMETRI

### -Nome
Specifica un nome per la macchina virtuale.

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

### -Profile
Specifica il profilo Azure da cui viene letto il cmdlet.
Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Modello
Specifica un modello.
Il cmdlet crea una macchina virtuale in base al modello specificato.
Per ottenere un oggetto modello, usare il cmdlet **Get-WAPackVMTemplate** .

```yaml
Type: VMTemplate
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMCredential
Specifica le credenziali per l'account di amministratore locale.
Per ottenere un oggetto **PSCredential** , usare il cmdlet **Get-Credential** .
Per altre informazioni, digitare `Get-Help Get-Credential` .

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

## OUTPUT

## Note

## COLLEGAMENTI CORRELATI

[New-WAPackVM](./New-WAPackVM.md)

[Get-WAPackVMTemplate](./Get-WAPackVMTemplate.md)


