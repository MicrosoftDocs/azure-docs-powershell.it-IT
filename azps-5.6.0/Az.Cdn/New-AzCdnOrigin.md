---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/new-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOrigin.md
ms.openlocfilehash: cc7350fb76091d3bf2f8bdab5c037a5afbe8b57a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983421"
---
# <span data-ttu-id="5a483-101">New-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="5a483-101">New-AzCdnOrigin</span></span>

## <span data-ttu-id="5a483-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a483-102">SYNOPSIS</span></span>
<span data-ttu-id="5a483-103">Crea una nuova origine CDN</span><span class="sxs-lookup"><span data-stu-id="5a483-103">Creates a new CDN origin</span></span>

## <span data-ttu-id="5a483-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5a483-104">SYNTAX</span></span>

### <span data-ttu-id="5a483-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5a483-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5a483-106">ByFieldsPrivateLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a483-106">ByFieldsPrivateLinkParameterSet</span></span>
```
New-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 [-PrivateLinkApprovalMessage <String>] -PrivateLinkLocation <String> -PrivateLinkResourceId <String>
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5a483-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a483-107">ByObjectParameterSet</span></span>
```
New-AzCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5a483-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5a483-108">DESCRIPTION</span></span>
<span data-ttu-id="5a483-109">La New-AzCdnOrigin creerà una nuova origine CDN all'interno dell'endpoint specificato.</span><span class="sxs-lookup"><span data-stu-id="5a483-109">The New-AzCdnOrigin will create a new CDN origin within the specified endpoint.</span></span>

## <span data-ttu-id="5a483-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5a483-110">EXAMPLES</span></span>

### <span data-ttu-id="5a483-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5a483-111">Example 1</span></span>
```powershell
PS C:\> New-AzCdnOrigin -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginName $originName -HostName $hostName
```

<span data-ttu-id="5a483-112">Questo cmdlet creerà una nuova origine CDN per l'endpoint specificato.</span><span class="sxs-lookup"><span data-stu-id="5a483-112">This cmdlet will create a new CDN origin for the specified endpoint.</span></span> <span data-ttu-id="5a483-113">Userà il nome host fornito come origine.</span><span class="sxs-lookup"><span data-stu-id="5a483-113">It will use the provided hostname as the origin.</span></span> 

## <span data-ttu-id="5a483-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5a483-114">PARAMETERS</span></span>

### <span data-ttu-id="5a483-115">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="5a483-115">-CdnOrigin</span></span>
<span data-ttu-id="5a483-116">Oggetto origine CDN.</span><span class="sxs-lookup"><span data-stu-id="5a483-116">The CDN origin object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a483-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a483-117">-DefaultProfile</span></span>
<span data-ttu-id="5a483-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5a483-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a483-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="5a483-119">-EndpointName</span></span>
<span data-ttu-id="5a483-120">Nome dell'endpoint della rete CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="5a483-120">Azure CDN endpoint name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a483-121">-HostName</span><span class="sxs-lookup"><span data-stu-id="5a483-121">-HostName</span></span>
<span data-ttu-id="5a483-122">Nome host origine CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="5a483-122">Azure CDN origin host name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a483-123">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="5a483-123">-HttpPort</span></span>
<span data-ttu-id="5a483-124">Porta HTTP di origine della rete CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="5a483-124">Azure CDN origin http port.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a483-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="5a483-125">-HttpsPort</span></span>
<span data-ttu-id="5a483-126">Porta https di origine della rete CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="5a483-126">Azure CDN origin https port.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a483-127">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="5a483-127">-OriginHostHeader</span></span>
<span data-ttu-id="5a483-128">Intestazione host origine CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="5a483-128">Azure CDN origin host header.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a483-129">-OriginName</span><span class="sxs-lookup"><span data-stu-id="5a483-129">-OriginName</span></span>
<span data-ttu-id="5a483-130">Nome di origine della rete CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="5a483-130">Azure CDN origin name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a483-131">-Priority</span><span class="sxs-lookup"><span data-stu-id="5a483-131">-Priority</span></span>
<span data-ttu-id="5a483-132">Priorità di origine della rete CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="5a483-132">Azure CDN origin priority.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a483-133">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="5a483-133">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="5a483-134">Messaggio personalizzato da includere nella richiesta di approvazione per la connessione al collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="5a483-134">A custom message to be included in the approval request to connect to the Private Link.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a483-135">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="5a483-135">-PrivateLinkLocation</span></span>
<span data-ttu-id="5a483-136">Posizione del collegamento privato dell'origine CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="5a483-136">Azure CDN origin private link location.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a483-137">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="5a483-137">-PrivateLinkResourceId</span></span>
<span data-ttu-id="5a483-138">ID risorsa collegamento privato origine CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="5a483-138">Azure CDN origin private link resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a483-139">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="5a483-139">-ProfileName</span></span>
<span data-ttu-id="5a483-140">Nome del profilo CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="5a483-140">Azure CDN profile name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a483-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a483-141">-ResourceGroupName</span></span>
<span data-ttu-id="5a483-142">Gruppo di risorse del profilo della rete CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="5a483-142">The resource group of the Azure CDN profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a483-143">-Spessore</span><span class="sxs-lookup"><span data-stu-id="5a483-143">-Weight</span></span>
<span data-ttu-id="5a483-144">Peso origine rete CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="5a483-144">Azure CDN origin weight.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a483-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5a483-145">-Confirm</span></span>
<span data-ttu-id="5a483-146">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a483-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a483-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a483-147">-WhatIf</span></span>
<span data-ttu-id="5a483-148">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5a483-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5a483-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5a483-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a483-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a483-150">CommonParameters</span></span>
<span data-ttu-id="5a483-151">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a483-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a483-152">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5a483-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a483-153">INPUT</span><span class="sxs-lookup"><span data-stu-id="5a483-153">INPUTS</span></span>

### <span data-ttu-id="5a483-154">Nessuno</span><span class="sxs-lookup"><span data-stu-id="5a483-154">None</span></span>

## <span data-ttu-id="5a483-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5a483-155">OUTPUTS</span></span>

### <span data-ttu-id="5a483-156">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span><span class="sxs-lookup"><span data-stu-id="5a483-156">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="5a483-157">NOTE</span><span class="sxs-lookup"><span data-stu-id="5a483-157">NOTES</span></span>

## <span data-ttu-id="5a483-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5a483-158">RELATED LINKS</span></span>
