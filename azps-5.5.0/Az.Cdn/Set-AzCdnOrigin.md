---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 0EB9F1C9-54CC-4794-9E37-108342341FE5
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
ms.openlocfilehash: 1c3b195f868db5d4e579aa833c4d9ce5a6203c56
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100210162"
---
# <span data-ttu-id="85665-101">Set-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="85665-101">Set-AzCdnOrigin</span></span>

## <span data-ttu-id="85665-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85665-102">SYNOPSIS</span></span>
<span data-ttu-id="85665-103">Aggiorna un server di origine CDN.</span><span class="sxs-lookup"><span data-stu-id="85665-103">Updates a CDN origin server.</span></span>

## <span data-ttu-id="85665-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="85665-104">SYNTAX</span></span>

### <span data-ttu-id="85665-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="85665-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="85665-106">ByFieldsPrivateLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="85665-106">ByFieldsPrivateLinkParameterSet</span></span>
```
Set-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 [-PrivateLinkApprovalMessage <String>] -PrivateLinkLocation <String> -PrivateLinkResourceId <String>
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="85665-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="85665-107">ByObjectParameterSet</span></span>
```
Set-AzCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="85665-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="85665-108">DESCRIPTION</span></span>
<span data-ttu-id="85665-109">Il cmdlet **Set-AzCdnOrigin** aggiorna un server di origine della rete per la distribuzione di contenuti (CDN) di Azure.</span><span class="sxs-lookup"><span data-stu-id="85665-109">The **Set-AzCdnOrigin** cmdlet updates an Azure Content Delivery Network (CDN) origin server.</span></span>

## <span data-ttu-id="85665-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="85665-110">EXAMPLES</span></span>

## <span data-ttu-id="85665-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="85665-111">PARAMETERS</span></span>

### <span data-ttu-id="85665-112">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="85665-112">-CdnOrigin</span></span>
<span data-ttu-id="85665-113">Specifica il server di origine aggiornato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85665-113">Specifies the origin server that this cmdlet updates.</span></span>

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

### <span data-ttu-id="85665-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85665-114">-DefaultProfile</span></span>
<span data-ttu-id="85665-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="85665-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="85665-116">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="85665-116">-EndpointName</span></span>
<span data-ttu-id="85665-117">Nome dell'endpoint della rete CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="85665-117">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="85665-118">-HostName</span><span class="sxs-lookup"><span data-stu-id="85665-118">-HostName</span></span>
<span data-ttu-id="85665-119">Nome host origine CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="85665-119">Azure CDN origin host name.</span></span>

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

### <span data-ttu-id="85665-120">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="85665-120">-HttpPort</span></span>
<span data-ttu-id="85665-121">Porta HTTP per l'origine HTTP della rete CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="85665-121">Azure CDN origin http port.</span></span>

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

### <span data-ttu-id="85665-122">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="85665-122">-HttpsPort</span></span>
<span data-ttu-id="85665-123">Porta https di origine della rete CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="85665-123">Azure CDN origin https port.</span></span>

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

### <span data-ttu-id="85665-124">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="85665-124">-OriginHostHeader</span></span>
<span data-ttu-id="85665-125">Intestazione host origine CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="85665-125">Azure CDN origin host header.</span></span>

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

### <span data-ttu-id="85665-126">-OriginName</span><span class="sxs-lookup"><span data-stu-id="85665-126">-OriginName</span></span>
<span data-ttu-id="85665-127">Nome di origine della rete CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="85665-127">Azure CDN origin name.</span></span>

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

### <span data-ttu-id="85665-128">-Priority</span><span class="sxs-lookup"><span data-stu-id="85665-128">-Priority</span></span>
<span data-ttu-id="85665-129">Priorità origine CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="85665-129">Azure CDN origin priority.</span></span>

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

### <span data-ttu-id="85665-130">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="85665-130">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="85665-131">Messaggio personalizzato da includere nella richiesta di approvazione per la connessione al collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="85665-131">A custom message to be included in the approval request to connect to the Private Link.</span></span>

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

### <span data-ttu-id="85665-132">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="85665-132">-PrivateLinkLocation</span></span>
<span data-ttu-id="85665-133">Percorso del collegamento privato di origine CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="85665-133">Azure CDN origin private link location.</span></span>

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

### <span data-ttu-id="85665-134">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="85665-134">-PrivateLinkResourceId</span></span>
<span data-ttu-id="85665-135">ID risorsa collegamento privato origine CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="85665-135">Azure CDN origin private link resource id.</span></span>

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

### <span data-ttu-id="85665-136">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="85665-136">-ProfileName</span></span>
<span data-ttu-id="85665-137">Nome del profilo CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="85665-137">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="85665-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85665-138">-ResourceGroupName</span></span>
<span data-ttu-id="85665-139">Gruppo di risorse del profilo della rete CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="85665-139">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="85665-140">-Spessore</span><span class="sxs-lookup"><span data-stu-id="85665-140">-Weight</span></span>
<span data-ttu-id="85665-141">Peso origine rete CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="85665-141">Azure CDN origin weight.</span></span>

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

### <span data-ttu-id="85665-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="85665-142">-Confirm</span></span>
<span data-ttu-id="85665-143">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85665-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85665-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85665-144">-WhatIf</span></span>
<span data-ttu-id="85665-145">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="85665-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="85665-146">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="85665-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85665-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85665-147">CommonParameters</span></span>
<span data-ttu-id="85665-148">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85665-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85665-149">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="85665-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85665-150">INPUT</span><span class="sxs-lookup"><span data-stu-id="85665-150">INPUTS</span></span>

### <span data-ttu-id="85665-151">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span><span class="sxs-lookup"><span data-stu-id="85665-151">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="85665-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="85665-152">OUTPUTS</span></span>

### <span data-ttu-id="85665-153">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span><span class="sxs-lookup"><span data-stu-id="85665-153">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="85665-154">NOTE</span><span class="sxs-lookup"><span data-stu-id="85665-154">NOTES</span></span>

## <span data-ttu-id="85665-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="85665-155">RELATED LINKS</span></span>

[<span data-ttu-id="85665-156">Get-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="85665-156">Get-AzCdnOrigin</span></span>](./Get-AzCdnOrigin.md)


