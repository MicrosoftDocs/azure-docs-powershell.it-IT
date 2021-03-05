---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/new-azcdndeliveryruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleAction.md
ms.openlocfilehash: 127c73a34b030a991b5875f141ea8dd850a4f0a1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009246"
---
# New-AzCdnDeliveryRuleAction

## SYNOPSIS
Crea un'azione di recapito.

## SINTASSI

### CacheExpirationActionParameterSet (impostazione predefinita)
```
New-AzCdnDeliveryRuleAction -CacheBehavior <String> [-CacheDuration <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### HeaderActionParameterSet
```
New-AzCdnDeliveryRuleAction -HeaderActionType <String> -Action <String> -HeaderName <String> [-Value <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### UrlRedirectActionParameterSet
```
New-AzCdnDeliveryRuleAction -RedirectType <String> [-DestinationProtocol <String>] [-CustomPath <String>]
 [-CustomHostname <String>] [-CustomQueryString <String>] [-CustomFragment <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### CacheKeyQueryStringActionParameterSet
```
New-AzCdnDeliveryRuleAction -QueryStringBehavior <String> [-QueryParameter <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### UrlRewriteActionParameterSet
```
New-AzCdnDeliveryRuleAction -SourcePattern <String> -Destination <String> [-PreservePath]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **New-AzCdnDeliveryRule** crea una regola di recapito per la creazione dell'endpoint CDN.

## ESEMPI

### Esempio 1
```powershell
PS C:\> New-AzCdnDeliveryRuleAction -HeaderActionType ModifyRequestHeader -Action Append -HeaderName "Accept-Encoding" -Value "gzip"

HeaderActionType    Action HeaderName      Value
----------------    ------ ----------      -----
ModifyRequestHeader Append Accept-Encoding gzip
```

Creare una regola di recapito semplice.

## PARAMETERS

### -Action
Azione da eseguire.

```yaml
Type: System.String
Parameter Sets: HeaderActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CacheBehavior
Comportamento della memorizzazione nella cache per l'azione

```yaml
Type: System.String
Parameter Sets: CacheExpirationActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CacheDuration
Durata per cui il contenuto deve essere memorizzato nella cache.
Il formato consentito è \[ d. \] hh:mm:ss

```yaml
Type: System.String
Parameter Sets: CacheExpirationActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Custom Deframment
Frammento da aggiungere all'URL di reindirizzamento.
Frammento è la parte dell'URL che viene dopo #.
Non includere il valore di errore #.

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomHostname
Host da reindirizzare.
Lasciare vuoto per usare l'host della posta in arrivo come host di destinazione.

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomPath
Percorso completo da reindirizzare.
Il percorso non può essere vuoto e deve iniziare con /.
Lasciare vuoto per usare il percorso in ingresso come percorso di destinazione.

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomQueryString
Set di stringhe di query da inserire nell'URL di reindirizzamento.
L'impostazione di questo valore sostituirebbe qualsiasi stringa di query esistente; lasciare vuoto per mantenere la stringa di query in ingresso.
La stringa di query deve essere nel \<key\> = \<value\> formato.
? e & verranno aggiunti automaticamente, in modo da non includerli.

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -Destination
Definire l'URL relativo con cui verranno riscritte le richieste precedenti.

```yaml
Type: System.String
Parameter Sets: UrlRewriteActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationProtocol
Protocollo da usare per il reindirizzamento.
Il valore predefinito è MatchRequest.

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HeaderActionType
Se modificare l'intestazione o l'intestazione della risposta della richiesta

```yaml
Type: System.String
Parameter Sets: HeaderActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HeaderName
Nome dell'intestazione da modificare.

```yaml
Type: System.String
Parameter Sets: HeaderActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PreservePath
Se mantenere il percorso non corrispondente.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UrlRewriteActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -QueryParameter
Parametri di query da includere o escludere (separati da virgola).

```yaml
Type: System.String[]
Parameter Sets: CacheKeyQueryStringActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -QueryStringBehavior
Comportamento di QueryString per le richieste

```yaml
Type: System.String
Parameter Sets: CacheKeyQueryStringActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RedirectType
Tipo di reindirizzamento che la regola userà per il reindirizzamento del traffico

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Source Sistema
Definire un criterio URI della richiesta che identifichi il tipo di richieste che possono essere riscritte. Se il valore è vuoto, viene trovata una corrispondenza per tutte le stringhe.

```yaml
Type: System.String
Parameter Sets: UrlRewriteActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Value
Valore per l'azione specificata.

```yaml
Type: System.String
Parameter Sets: HeaderActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### Nessuno

## OUTPUT

### Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction

## NOTE

## COLLEGAMENTI CORRELATI
