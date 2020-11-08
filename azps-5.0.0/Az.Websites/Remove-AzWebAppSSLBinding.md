---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3AB3D398-E5DB-4214-BA27-6E3B7D225550
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSSLBinding.md
ms.openlocfilehash: bed5cb961fd39975b3f10debe8791a418fd5dcda
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202713"
---
# Remove-AzWebAppSSLBinding

## Sinossi
Rimuove un binding SSL da un certificato caricato.

## SINTASSI

### S1
```
Remove-AzWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force]
 [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### S2
```
Remove-AzWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Remove-AzWebAppSSLBinding** rimuove un binding SSL (Secure Sockets Layer) da un'app Web di Azure.
I binding SSL vengono usati per associare un'app Web a un certificato.

## ESEMPI

### Esempio 1: rimuovere un binding SSL per un'app Web
```
PS C:\>Remove-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com"
```

Questo comando rimuove il binding SSL per l'app Web ContosoWebApp.
Dato che il parametro *DeleteCertificate* non è incluso, il certificato verrà eliminato se non ha più binding SSL.

### Esempio 2: rimuovere un binding SSL senza rimuovere il certificato
```
PS C:\>Remove-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com" -DeleteCertificate $False
```

Analogamente all'esempio 1, questo comando rimuove anche il binding SSL per l'app Web ContosoWebApp.
In questo caso, tuttavia, il parametro *DeleteCertificate* è incluso e il valore del parametro è impostato su $false.
Ciò significa che il certificato non verrà eliminato indipendentemente dal fatto che disponga di binding SSL o meno.

### Esempio 3: usare un riferimento a un oggetto per rimuovere un binding SSL
```
PS C:\>$WebApp = Get-AzWebApp -Name "ContosoWebApp"
PS C:\> Remove-AzWebAppSSLBinding -WebApp $WebApp -Name "www.contoso.com"
```

In questo esempio viene usato un riferimento a un oggetto al sito Web dell'app per rimuovere il binding SSL per un'app Web.
Il primo comando usa il cmdlet Get-AzWebApp per creare un riferimento a un oggetto all'app Web denominata ContosoWebApp.
Il riferimento a un oggetto viene archiviato in una variabile denominata $WebApp.
Il secondo comando usa il riferimento oggetto e il cmdlet **Remove-AzWebAppSSLBinding** per rimuovere il binding SSL.

## PARAMETRI

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeleteCertificate
Specifica l'azione da eseguire se il binding SSL da rimuovere è l'unico binding usato dal certificato.
Se *DeleteCertificate* è impostato su $false, il certificato non verrà eliminato quando l'associazione viene eliminata.
Se *DeleteCertificate* è impostato su $true o non è incluso nel comando, il certificato verrà eliminato insieme al binding SSL.
Il certificato verrà eliminato solo se il binding SSL da rimuovere è l'unico binding usato dal certificato.
Se il certificato contiene più di un binding, il certificato non verrà rimosso indipendentemente dal valore del parametro *DeleteCertificate* .

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Impone l'esecuzione del comando senza richiedere la conferma dell'utente.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Specifica il nome dell'app Web.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Specifica il nome del gruppo di risorse a cui è assegnato il certificato.
Non è possibile usare il parametro *ResourceGroupName* e il parametro *Web App* nello stesso comando.

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Slot
Specifica lo slot di distribuzione dell'app Web.
Per ottenere uno slot di distribuzione, usare il cmdlet Get-AzWebAppSlot.

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Web App
Specifica un'app Web.
Per ottenere un'app Web, usa il cmdlet Get-AzWebApp.
Non è possibile usare il parametro *Web App* nello stesso comando del parametro *ResourceGroupName* e/o *WebAppName*.

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WebAppName
Specifica il nome dell'app Web.
Non è possibile usare il parametro *WebAppName* e il parametro *Web App* nello stesso comando.

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confermare
Richiede la conferma prima di eseguire il cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra cosa succede se il cmdlet viene eseguito.
Il cmdlet non viene eseguito. Mostra cosa succede se il cmdlet viene eseguito.
Il cmdlet non viene eseguito.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Microsoft. Azure. Commands. webapps. Models. PSSite

## OUTPUT

### System. void

## Note

## COLLEGAMENTI CORRELATI

[Get-AzWebAppSSLBinding](./Get-AzWebAppSSLBinding.md)

[New-AzWebAppSSLBinding](./New-AzWebAppSSLBinding.md)

[Get-AzWebAppSlot](./Get-AzWebAppSlot.md)

[Get-AzWebApp](./Get-AzWebApp.md)


