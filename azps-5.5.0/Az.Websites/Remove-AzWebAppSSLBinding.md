---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3AB3D398-E5DB-4214-BA27-6E3B7D225550
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSSLBinding.md
ms.openlocfilehash: bed5cb961fd39975b3f10debe8791a418fd5dcda
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208843"
---
# Remove-AzWebAppSSLBinding

## SYNOPSIS
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

## DESCRIZIONE
Il cmdlet **Remove-AzWebAppSSLBinding** rimuove un binding SSL (Secure Sockets Layer) da un'app Web di Azure.
Le associazioni SSL vengono usate per associare un'app Web a un certificato.

## ESEMPI

### Esempio 1: Rimuovere un binding SSL per un'app Web
```
PS C:\>Remove-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com"
```

Questo comando rimuove il binding SSL per l'app Web ContosoWebApp.
Poiché il *parametro DeleteCertificate* non è incluso, il certificato verrà eliminato se non ha più binding SSL.

### Esempio 2: Rimuovere un binding SSL senza rimuovere il certificato
```
PS C:\>Remove-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com" -DeleteCertificate $False
```

Come nell'esempio 1, questo comando rimuove anche il binding SSL per l'app Web ContosoWebApp.
In questo caso, tuttavia, è incluso *il parametro DeleteCertificate* e il relativo valore è impostato su $False.
Questo significa che il certificato non verrà eliminato indipendentemente dal fatto che abbia o meno binding SSL.

### Esempio 3: Usare un riferimento a un oggetto per rimuovere un binding SSL
```
PS C:\>$WebApp = Get-AzWebApp -Name "ContosoWebApp"
PS C:\> Remove-AzWebAppSSLBinding -WebApp $WebApp -Name "www.contoso.com"
```

In questo esempio viene utilizzato un riferimento a un oggetto per il sito Web dell'app Web per rimuovere il binding SSL per un'app Web.
Il primo comando usa il cmdlet Get-AzWebApp per creare un riferimento a un oggetto all'app Web denominato ContosoWebApp.
Il riferimento all'oggetto viene archiviato in una variabile denominata $WebApp.
Il secondo comando usa il riferimento all'oggetto e il cmdlet **Remove-AzWebAppSSLBinding** per rimuovere il binding SSL.

## PARAMETERS

### -DefaultProfile
Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.

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
Se *DeleteCertificate* è impostato su $False, il certificato non verrà eliminato quando viene eliminato il binding.
Se *DeleteCertificate* è impostato su $True o non è incluso nel comando, il certificato verrà eliminato insieme al binding SSL.
Il certificato verrà eliminato solo se il binding SSL da rimuovere è l'unico binding usato dal certificato.
Se il certificato ha più di una associazione, il certificato non verrà rimosso indipendentemente dal valore del *parametro DeleteCertificate.*

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
Forza l'esecuzione del comando senza chiedere conferma all'utente.

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

### -Name
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
Non è possibile usare *il parametro ResourceGroupName* e il *parametro WebApp* nello stesso comando.

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
Specifica lo slot di distribuzione di Web App.
Per ottenere uno slot di distribuzione, usare il cmdlet Get-AzWebAppSlot distribuzione.

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

### -WebApp
Specifica un'app Web.
Per ottenere un'app Web, usare il cmdlet Get-AzWebApp web app.
Non è possibile usare *il parametro WebApp* nello stesso comando del *parametro ResourceGroupName* e/o *WebAppName.*

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
Non è possibile usare *il parametro WebAppName* e il *parametro WebApp* nello stesso comando.

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

### -Confirm
Chiede conferma prima di eseguire il cmdlet.

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
Mostra cosa accadrebbe se il cmdlet viene eseguito.
Il cmdlet non viene eseguito. Mostra cosa accadrebbe se il cmdlet viene eseguito.
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
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUT

### Microsoft.Azure.Commands.WebApps.Models.PSSite

## OUTPUT

### System.Void

## NOTE

## COLLEGAMENTI CORRELATI

[Get-AzWebAppSSLBinding](./Get-AzWebAppSSLBinding.md)

[New-AzWebAppSSLBinding](./New-AzWebAppSSLBinding.md)

[Get-AzWebAppSlot](./Get-AzWebAppSlot.md)

[Get-AzWebApp](./Get-AzWebApp.md)


