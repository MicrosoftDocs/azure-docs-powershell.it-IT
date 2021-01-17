---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 0EB9F1C9-54CC-4794-9E37-108342341FE5
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
ms.openlocfilehash: 1c3b195f868db5d4e579aa833c4d9ce5a6203c56
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477971"
---
# <span data-ttu-id="60a91-101">Set-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="60a91-101">Set-AzCdnOrigin</span></span>

## <span data-ttu-id="60a91-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="60a91-102">SYNOPSIS</span></span>
<span data-ttu-id="60a91-103">Aggiorna un server di origine CDN.</span><span class="sxs-lookup"><span data-stu-id="60a91-103">Updates a CDN origin server.</span></span>

## <span data-ttu-id="60a91-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="60a91-104">SYNTAX</span></span>

### <span data-ttu-id="60a91-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="60a91-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="60a91-106">ByFieldsPrivateLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="60a91-106">ByFieldsPrivateLinkParameterSet</span></span>
```
Set-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 [-PrivateLinkApprovalMessage <String>] -PrivateLinkLocation <String> -PrivateLinkResourceId <String>
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="60a91-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="60a91-107">ByObjectParameterSet</span></span>
```
Set-AzCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="60a91-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="60a91-108">DESCRIPTION</span></span>
<span data-ttu-id="60a91-109">Il cmdlet **set-AzCdnOrigin** aggiorna un server di origine della rete CDN (Azure Content Delivery Network).</span><span class="sxs-lookup"><span data-stu-id="60a91-109">The **Set-AzCdnOrigin** cmdlet updates an Azure Content Delivery Network (CDN) origin server.</span></span>

## <span data-ttu-id="60a91-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="60a91-110">EXAMPLES</span></span>

## <span data-ttu-id="60a91-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="60a91-111">PARAMETERS</span></span>

### <span data-ttu-id="60a91-112">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="60a91-112">-CdnOrigin</span></span>
<span data-ttu-id="60a91-113">Specifica il server di origine che questo cmdlet aggiorna.</span><span class="sxs-lookup"><span data-stu-id="60a91-113">Specifies the origin server that this cmdlet updates.</span></span>

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

### <span data-ttu-id="60a91-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60a91-114">-DefaultProfile</span></span>
<span data-ttu-id="60a91-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="60a91-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="60a91-116">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="60a91-116">-EndpointName</span></span>
<span data-ttu-id="60a91-117">Nome dell'endpoint CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="60a91-117">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="60a91-118">-HostName</span><span class="sxs-lookup"><span data-stu-id="60a91-118">-HostName</span></span>
<span data-ttu-id="60a91-119">Nome host di origine CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="60a91-119">Azure CDN origin host name.</span></span>

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

### <span data-ttu-id="60a91-120">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="60a91-120">-HttpPort</span></span>
<span data-ttu-id="60a91-121">Porta http di origine CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="60a91-121">Azure CDN origin http port.</span></span>

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

### <span data-ttu-id="60a91-122">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="60a91-122">-HttpsPort</span></span>
<span data-ttu-id="60a91-123">Porta HTTPS di origine CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="60a91-123">Azure CDN origin https port.</span></span>

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

### <span data-ttu-id="60a91-124">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="60a91-124">-OriginHostHeader</span></span>
<span data-ttu-id="60a91-125">Intestazione dell'host della rete CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="60a91-125">Azure CDN origin host header.</span></span>

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

### <span data-ttu-id="60a91-126">-Originname</span><span class="sxs-lookup"><span data-stu-id="60a91-126">-OriginName</span></span>
<span data-ttu-id="60a91-127">Nome origine di Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="60a91-127">Azure CDN origin name.</span></span>

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

### <span data-ttu-id="60a91-128">-Priorità</span><span class="sxs-lookup"><span data-stu-id="60a91-128">-Priority</span></span>
<span data-ttu-id="60a91-129">Priorità di origine della rete CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="60a91-129">Azure CDN origin priority.</span></span>

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

### <span data-ttu-id="60a91-130">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="60a91-130">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="60a91-131">Messaggio personalizzato da includere nella richiesta di approvazione per la connessione al collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="60a91-131">A custom message to be included in the approval request to connect to the Private Link.</span></span>

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

### <span data-ttu-id="60a91-132">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="60a91-132">-PrivateLinkLocation</span></span>
<span data-ttu-id="60a91-133">Posizione del collegamento privato in Azure CDN Origin.</span><span class="sxs-lookup"><span data-stu-id="60a91-133">Azure CDN origin private link location.</span></span>

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

### <span data-ttu-id="60a91-134">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="60a91-134">-PrivateLinkResourceId</span></span>
<span data-ttu-id="60a91-135">ID risorsa collegamento privato di Azure CDN Origin.</span><span class="sxs-lookup"><span data-stu-id="60a91-135">Azure CDN origin private link resource id.</span></span>

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

### <span data-ttu-id="60a91-136">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="60a91-136">-ProfileName</span></span>
<span data-ttu-id="60a91-137">Nome del profilo CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="60a91-137">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="60a91-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60a91-138">-ResourceGroupName</span></span>
<span data-ttu-id="60a91-139">Gruppo risorse del profilo CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="60a91-139">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="60a91-140">-Peso</span><span class="sxs-lookup"><span data-stu-id="60a91-140">-Weight</span></span>
<span data-ttu-id="60a91-141">Peso origine di Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="60a91-141">Azure CDN origin weight.</span></span>

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

### <span data-ttu-id="60a91-142">-Confermare</span><span class="sxs-lookup"><span data-stu-id="60a91-142">-Confirm</span></span>
<span data-ttu-id="60a91-143">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60a91-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60a91-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60a91-144">-WhatIf</span></span>
<span data-ttu-id="60a91-145">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="60a91-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="60a91-146">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="60a91-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60a91-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60a91-147">CommonParameters</span></span>
<span data-ttu-id="60a91-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60a91-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60a91-149">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="60a91-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60a91-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="60a91-150">INPUTS</span></span>

### <span data-ttu-id="60a91-151">Microsoft. Azure. Commands. CDN. Models. Origin. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="60a91-151">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="60a91-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="60a91-152">OUTPUTS</span></span>

### <span data-ttu-id="60a91-153">Microsoft. Azure. Commands. CDN. Models. Origin. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="60a91-153">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="60a91-154">Note</span><span class="sxs-lookup"><span data-stu-id="60a91-154">NOTES</span></span>

## <span data-ttu-id="60a91-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="60a91-155">RELATED LINKS</span></span>

[<span data-ttu-id="60a91-156">Get-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="60a91-156">Get-AzCdnOrigin</span></span>](./Get-AzCdnOrigin.md)


