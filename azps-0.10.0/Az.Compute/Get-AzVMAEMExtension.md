---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 212281F0-9A3E-4652-919F-400455E3950E
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMAEMExtension.md
ms.openlocfilehash: 5efda3a73cc94d2e196b5817d5b3c1e507192da0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863790"
---
# Get-AzVMAEMExtension

## Sinossi
Ottiene informazioni sull'estensione AEM.

## SINTASSI

```
Get-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [[-OSType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzVMAEMExtension** ottiene informazioni sull'estensione AEM (Azure Enhanced Monitoring).

## ESEMPI

### Esempio 1: ottenere l'estensione AEM
```
PS C:\> Get-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

Questo comando ottiene le informazioni per l'estensione AEM per la macchina virtuale denominata Contoso-server.

## PARAMETRI

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Specifica il nome di una macchina virtuale.
Questo cmdlet consente di ottenere informazioni sull'estensione AEM nella macchina virtuale specificata da questo cmdlet.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OSType
Specifica il tipo di sistema operativo del disco del sistema operativo.
Se il disco del sistema operativo non ha un tipo, è necessario specificare questo parametro.
I valori accettabili per questo parametro sono: Windows e Linux.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Specifica il nome del gruppo di risorse di una macchina virtuale.
Questo cmdlet recupera le informazioni per l'estensione AEM in quella macchina virtuale.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Stato
Indica che questo cmdlet ottiene solo la visualizzazione dell'istanza dell'estensione AEM.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
Specifica il nome di una macchina virtuale.
Questo cmdlet ottiene informazioni sull'estensione AEM per la macchina virtuale specificata da questo parametro.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Nessuno
Questo cmdlet non accetta alcun input.

## OUTPUT

### Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineExtension

## Note

## COLLEGAMENTI CORRELATI

[Remove-AzVMAEMExtension](./Remove-AzVMAEMExtension.md)

[Set-AzVMAEMExtension](./Set-AzVMAEMExtension.md)

[Test-AzVMAEMExtension](./Test-AzVMAEMExtension.md)

