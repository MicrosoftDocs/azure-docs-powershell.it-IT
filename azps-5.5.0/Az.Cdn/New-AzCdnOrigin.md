---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOrigin.md
ms.openlocfilehash: a9ef1687333851e2ac67dfb3f0146509f3b77183
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200822"
---
# <span data-ttu-id="da0d2-101">New-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="da0d2-101">New-AzCdnOrigin</span></span>

## <span data-ttu-id="da0d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da0d2-102">SYNOPSIS</span></span>
<span data-ttu-id="da0d2-103">Crea una nuova origine CDN</span><span class="sxs-lookup"><span data-stu-id="da0d2-103">Creates a new CDN origin</span></span>

## <span data-ttu-id="da0d2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="da0d2-104">SYNTAX</span></span>

### <span data-ttu-id="da0d2-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="da0d2-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="da0d2-106">ByFieldsPrivateLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="da0d2-106">ByFieldsPrivateLinkParameterSet</span></span>
```
New-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 [-PrivateLinkApprovalMessage <String>] -PrivateLinkLocation <String> -PrivateLinkResourceId <String>
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="da0d2-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="da0d2-107">ByObjectParameterSet</span></span>
```
New-AzCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="da0d2-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="da0d2-108">DESCRIPTION</span></span>
<span data-ttu-id="da0d2-109">La New-AzCdnOrigin creerà una nuova origine CDN all'interno dell'endpoint specificato.</span><span class="sxs-lookup"><span data-stu-id="da0d2-109">The New-AzCdnOrigin will create a new CDN origin within the specified endpoint.</span></span>

## <span data-ttu-id="da0d2-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="da0d2-110">EXAMPLES</span></span>

### <span data-ttu-id="da0d2-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="da0d2-111">Example 1</span></span>
```powershell
PS C:\> New-AzCdnOrigin -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginName $originName -HostName $hostName
```

<span data-ttu-id="da0d2-112">Questo cmdlet creerà una nuova origine CDN per l'endpoint specificato.</span><span class="sxs-lookup"><span data-stu-id="da0d2-112">This cmdlet will create a new CDN origin for the specified endpoint.</span></span> <span data-ttu-id="da0d2-113">Userà il nome host specificato come origine.</span><span class="sxs-lookup"><span data-stu-id="da0d2-113">It will use the provided hostname as the origin.</span></span> 

## <span data-ttu-id="da0d2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da0d2-114">PARAMETERS</span></span>

### <span data-ttu-id="da0d2-115">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="da0d2-115">-CdnOrigin</span></span>
<span data-ttu-id="da0d2-116">Oggetto origine CDN.</span><span class="sxs-lookup"><span data-stu-id="da0d2-116">The CDN origin object.</span></span>

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

### <span data-ttu-id="da0d2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da0d2-117">-DefaultProfile</span></span>
<span data-ttu-id="da0d2-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="da0d2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da0d2-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="da0d2-119">-EndpointName</span></span>
<span data-ttu-id="da0d2-120">Nome dell'endpoint della rete CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="da0d2-120">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="da0d2-121">-HostName</span><span class="sxs-lookup"><span data-stu-id="da0d2-121">-HostName</span></span>
<span data-ttu-id="da0d2-122">Nome host origine CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="da0d2-122">Azure CDN origin host name.</span></span>

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

### <span data-ttu-id="da0d2-123">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="da0d2-123">-HttpPort</span></span>
<span data-ttu-id="da0d2-124">Porta HTTP per l'origine HTTP della rete CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="da0d2-124">Azure CDN origin http port.</span></span>

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

### <span data-ttu-id="da0d2-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="da0d2-125">-HttpsPort</span></span>
<span data-ttu-id="da0d2-126">Porta https di origine della rete CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="da0d2-126">Azure CDN origin https port.</span></span>

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

### <span data-ttu-id="da0d2-127">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="da0d2-127">-OriginHostHeader</span></span>
<span data-ttu-id="da0d2-128">Intestazione host origine CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="da0d2-128">Azure CDN origin host header.</span></span>

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

### <span data-ttu-id="da0d2-129">-OriginName</span><span class="sxs-lookup"><span data-stu-id="da0d2-129">-OriginName</span></span>
<span data-ttu-id="da0d2-130">Nome di origine della rete CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="da0d2-130">Azure CDN origin name.</span></span>

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

### <span data-ttu-id="da0d2-131">-Priority</span><span class="sxs-lookup"><span data-stu-id="da0d2-131">-Priority</span></span>
<span data-ttu-id="da0d2-132">Priorità origine CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="da0d2-132">Azure CDN origin priority.</span></span>

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

### <span data-ttu-id="da0d2-133">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="da0d2-133">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="da0d2-134">Messaggio personalizzato da includere nella richiesta di approvazione per la connessione al collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="da0d2-134">A custom message to be included in the approval request to connect to the Private Link.</span></span>

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

### <span data-ttu-id="da0d2-135">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="da0d2-135">-PrivateLinkLocation</span></span>
<span data-ttu-id="da0d2-136">Percorso del collegamento privato di origine CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="da0d2-136">Azure CDN origin private link location.</span></span>

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

### <span data-ttu-id="da0d2-137">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="da0d2-137">-PrivateLinkResourceId</span></span>
<span data-ttu-id="da0d2-138">ID risorsa collegamento privato origine CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="da0d2-138">Azure CDN origin private link resource id.</span></span>

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

### <span data-ttu-id="da0d2-139">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="da0d2-139">-ProfileName</span></span>
<span data-ttu-id="da0d2-140">Nome del profilo CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="da0d2-140">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="da0d2-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da0d2-141">-ResourceGroupName</span></span>
<span data-ttu-id="da0d2-142">Gruppo di risorse del profilo della rete CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="da0d2-142">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="da0d2-143">-Spessore</span><span class="sxs-lookup"><span data-stu-id="da0d2-143">-Weight</span></span>
<span data-ttu-id="da0d2-144">Peso origine rete CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="da0d2-144">Azure CDN origin weight.</span></span>

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

### <span data-ttu-id="da0d2-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="da0d2-145">-Confirm</span></span>
<span data-ttu-id="da0d2-146">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da0d2-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da0d2-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da0d2-147">-WhatIf</span></span>
<span data-ttu-id="da0d2-148">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="da0d2-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="da0d2-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="da0d2-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da0d2-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da0d2-150">CommonParameters</span></span>
<span data-ttu-id="da0d2-151">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da0d2-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da0d2-152">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="da0d2-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da0d2-153">INPUT</span><span class="sxs-lookup"><span data-stu-id="da0d2-153">INPUTS</span></span>

### <span data-ttu-id="da0d2-154">Nessuno</span><span class="sxs-lookup"><span data-stu-id="da0d2-154">None</span></span>

## <span data-ttu-id="da0d2-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="da0d2-155">OUTPUTS</span></span>

### <span data-ttu-id="da0d2-156">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span><span class="sxs-lookup"><span data-stu-id="da0d2-156">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="da0d2-157">NOTE</span><span class="sxs-lookup"><span data-stu-id="da0d2-157">NOTES</span></span>

## <span data-ttu-id="da0d2-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="da0d2-158">RELATED LINKS</span></span>
