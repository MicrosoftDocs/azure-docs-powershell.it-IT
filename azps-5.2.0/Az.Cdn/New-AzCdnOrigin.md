---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOrigin.md
ms.openlocfilehash: a9ef1687333851e2ac67dfb3f0146509f3b77183
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98353263"
---
# <span data-ttu-id="2e610-101">New-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="2e610-101">New-AzCdnOrigin</span></span>

## <span data-ttu-id="2e610-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2e610-102">SYNOPSIS</span></span>
<span data-ttu-id="2e610-103">Crea una nuova origine CDN</span><span class="sxs-lookup"><span data-stu-id="2e610-103">Creates a new CDN origin</span></span>

## <span data-ttu-id="2e610-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2e610-104">SYNTAX</span></span>

### <span data-ttu-id="2e610-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2e610-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2e610-106">ByFieldsPrivateLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e610-106">ByFieldsPrivateLinkParameterSet</span></span>
```
New-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 [-PrivateLinkApprovalMessage <String>] -PrivateLinkLocation <String> -PrivateLinkResourceId <String>
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2e610-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e610-107">ByObjectParameterSet</span></span>
```
New-AzCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2e610-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2e610-108">DESCRIPTION</span></span>
<span data-ttu-id="2e610-109">L'New-AzCdnOrigin creerà una nuova origine CDN nell'endpoint specificato.</span><span class="sxs-lookup"><span data-stu-id="2e610-109">The New-AzCdnOrigin will create a new CDN origin within the specified endpoint.</span></span>

## <span data-ttu-id="2e610-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2e610-110">EXAMPLES</span></span>

### <span data-ttu-id="2e610-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2e610-111">Example 1</span></span>
```powershell
PS C:\> New-AzCdnOrigin -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginName $originName -HostName $hostName
```

<span data-ttu-id="2e610-112">Questo cmdlet creerà una nuova origine CDN per l'endpoint specificato.</span><span class="sxs-lookup"><span data-stu-id="2e610-112">This cmdlet will create a new CDN origin for the specified endpoint.</span></span> <span data-ttu-id="2e610-113">Userà il nome host specificato come origine.</span><span class="sxs-lookup"><span data-stu-id="2e610-113">It will use the provided hostname as the origin.</span></span> 

## <span data-ttu-id="2e610-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2e610-114">PARAMETERS</span></span>

### <span data-ttu-id="2e610-115">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="2e610-115">-CdnOrigin</span></span>
<span data-ttu-id="2e610-116">Oggetto origine CDN.</span><span class="sxs-lookup"><span data-stu-id="2e610-116">The CDN origin object.</span></span>

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

### <span data-ttu-id="2e610-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e610-117">-DefaultProfile</span></span>
<span data-ttu-id="2e610-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2e610-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e610-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="2e610-119">-EndpointName</span></span>
<span data-ttu-id="2e610-120">Nome dell'endpoint CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="2e610-120">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="2e610-121">-HostName</span><span class="sxs-lookup"><span data-stu-id="2e610-121">-HostName</span></span>
<span data-ttu-id="2e610-122">Nome host di origine CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="2e610-122">Azure CDN origin host name.</span></span>

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

### <span data-ttu-id="2e610-123">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="2e610-123">-HttpPort</span></span>
<span data-ttu-id="2e610-124">Porta http di origine CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="2e610-124">Azure CDN origin http port.</span></span>

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

### <span data-ttu-id="2e610-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="2e610-125">-HttpsPort</span></span>
<span data-ttu-id="2e610-126">Porta HTTPS di origine CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="2e610-126">Azure CDN origin https port.</span></span>

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

### <span data-ttu-id="2e610-127">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="2e610-127">-OriginHostHeader</span></span>
<span data-ttu-id="2e610-128">Intestazione dell'host della rete CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="2e610-128">Azure CDN origin host header.</span></span>

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

### <span data-ttu-id="2e610-129">-Originname</span><span class="sxs-lookup"><span data-stu-id="2e610-129">-OriginName</span></span>
<span data-ttu-id="2e610-130">Nome origine di Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="2e610-130">Azure CDN origin name.</span></span>

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

### <span data-ttu-id="2e610-131">-Priorità</span><span class="sxs-lookup"><span data-stu-id="2e610-131">-Priority</span></span>
<span data-ttu-id="2e610-132">Priorità di origine della rete CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="2e610-132">Azure CDN origin priority.</span></span>

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

### <span data-ttu-id="2e610-133">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="2e610-133">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="2e610-134">Messaggio personalizzato da includere nella richiesta di approvazione per la connessione al collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="2e610-134">A custom message to be included in the approval request to connect to the Private Link.</span></span>

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

### <span data-ttu-id="2e610-135">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="2e610-135">-PrivateLinkLocation</span></span>
<span data-ttu-id="2e610-136">Posizione del collegamento privato in Azure CDN Origin.</span><span class="sxs-lookup"><span data-stu-id="2e610-136">Azure CDN origin private link location.</span></span>

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

### <span data-ttu-id="2e610-137">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="2e610-137">-PrivateLinkResourceId</span></span>
<span data-ttu-id="2e610-138">ID risorsa collegamento privato di Azure CDN Origin.</span><span class="sxs-lookup"><span data-stu-id="2e610-138">Azure CDN origin private link resource id.</span></span>

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

### <span data-ttu-id="2e610-139">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="2e610-139">-ProfileName</span></span>
<span data-ttu-id="2e610-140">Nome del profilo CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="2e610-140">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="2e610-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e610-141">-ResourceGroupName</span></span>
<span data-ttu-id="2e610-142">Gruppo risorse del profilo CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="2e610-142">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="2e610-143">-Peso</span><span class="sxs-lookup"><span data-stu-id="2e610-143">-Weight</span></span>
<span data-ttu-id="2e610-144">Peso origine di Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="2e610-144">Azure CDN origin weight.</span></span>

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

### <span data-ttu-id="2e610-145">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2e610-145">-Confirm</span></span>
<span data-ttu-id="2e610-146">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e610-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e610-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e610-147">-WhatIf</span></span>
<span data-ttu-id="2e610-148">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2e610-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2e610-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2e610-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e610-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e610-150">CommonParameters</span></span>
<span data-ttu-id="2e610-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e610-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e610-152">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2e610-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e610-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2e610-153">INPUTS</span></span>

### <span data-ttu-id="2e610-154">Nessuno</span><span class="sxs-lookup"><span data-stu-id="2e610-154">None</span></span>

## <span data-ttu-id="2e610-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2e610-155">OUTPUTS</span></span>

### <span data-ttu-id="2e610-156">Microsoft. Azure. Commands. CDN. Models. Origin. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="2e610-156">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="2e610-157">Note</span><span class="sxs-lookup"><span data-stu-id="2e610-157">NOTES</span></span>

## <span data-ttu-id="2e610-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2e610-158">RELATED LINKS</span></span>
