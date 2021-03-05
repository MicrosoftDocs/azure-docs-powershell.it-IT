---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EE3D2BA0-32E7-4A37-BCAF-F0E8FAAC43CE
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
ms.openlocfilehash: 08a9fbd9798a3fd3b53d7d71aca9ebd607d23164
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973694"
---
# Get-AzWebAppSSLBinding

## SYNOPSIS
Ottiene un binding SSL del certificato Web App di Azure.

## SINTASSI

### S1
```
Get-AzWebAppSSLBinding [[-Name] <String>] [-ResourceGroupName] <String> [-WebAppName] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### S2
```
Get-AzWebAppSSLBinding [[-Name] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Get-AzWebAppSSLBinding** ottiene un binding SSL (Secure Sockets Layer) per un'app Web di Azure.
Le associazioni SSL vengono usate per associare un'app Web a un certificato caricato.
Le app Web possono essere associate a più certificati.

## ESEMPI

### Esempio 1: Ottenere i binding SSL per un'app Web
```
PS C:\>Get-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp"
```

Questo comando recupera le associazioni SSL per l'app Web ContosoWebApp, associata al gruppo di risorse ContosoResourceGroup.

### Esempio 2: Usare un riferimento a un oggetto per ottenere i binding SSL per un'app Web
```
PS C:\>$WebApp = Get-AzWebApp -Name "ContosoWebApp"
PS C:\> Get-AzWebAppSSLBinding -WebApp $WebApp
```

I comandi di questo esempio ottengono anche i binding SSL per l'app Web ContosoWebApp; In questo caso, invece del nome dell'app Web e del gruppo di risorse associato, viene usato un riferimento a un oggetto.
Questo riferimento all'oggetto viene creato dal primo comando dell'esempio, che usa **Get-AzWebApp** per creare un riferimento a un oggetto all'app Web denominato ContosoWebApp.
Il riferimento all'oggetto viene archiviato in una variabile denominata $WebApp.
Questa variabile e il cmdlet **Get-AzWebAppSSLBinding** vengono quindi usati dal secondo comando per ottenere le associazioni SSL.

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

### -Name
Specifica il nome del binding SSL.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
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
Specifica uno slot di distribuzione di Web App.
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
Per ottenere un'app Web, usare il cmdlet Get-AzWebApp.

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
Specifica il nome dell'app Web da cui il cmdlet ottiene le associazioni SSL.
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

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUT

### Microsoft.Azure.Commands.WebApps.Models.PSSite

## OUTPUT

### Microsoft.Azure.Management.WebSites.Models.HostNameSslState

## NOTE

## COLLEGAMENTI CORRELATI

[New-AzWebAppSSLBinding](./New-AzWebAppSSLBinding.md)

[Remove-AzWebAppSSLBinding](./Remove-AzWebAppSSLBinding.md)

[Get-AzWebApp](./Get-AzWebApp.md)


