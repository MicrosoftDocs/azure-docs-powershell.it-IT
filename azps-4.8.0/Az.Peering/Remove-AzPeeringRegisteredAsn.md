---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredAsn.md
ms.openlocfilehash: d43fe033b58ba6295728bc0c21ddb1d853587b59
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192676"
---
# <span data-ttu-id="b6816-101">Remove-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="b6816-101">Remove-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="b6816-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b6816-102">SYNOPSIS</span></span>
<span data-ttu-id="b6816-103">Eliminare o rimuovere un ASN registrato dalla risorsa peering padre.</span><span class="sxs-lookup"><span data-stu-id="b6816-103">Delete or remove a registered ASN from the parent peering resource.</span></span>

## <span data-ttu-id="b6816-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b6816-104">SYNTAX</span></span>

### <span data-ttu-id="b6816-105">ByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b6816-105">ByName (Default)</span></span>
```
Remove-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String> [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6816-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="b6816-106">InputObject</span></span>
```
Remove-AzPeeringRegisteredAsn -InputObject <PSPeeringServicePrefix> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6816-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b6816-107">ByResourceId</span></span>
```
Remove-AzPeeringRegisteredAsn [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6816-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b6816-108">DESCRIPTION</span></span>
<span data-ttu-id="b6816-109">Consente la rimozione di ASN registrato dalla risorsa peering padre.</span><span class="sxs-lookup"><span data-stu-id="b6816-109">Allows the removal of registered ASN from parent peering resource.</span></span>

## <span data-ttu-id="b6816-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b6816-110">EXAMPLES</span></span>

### <span data-ttu-id="b6816-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b6816-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzPeeringRegisteredAsn -ResourceId $resourceId
```

<span data-ttu-id="b6816-112">Rimuovi un ID di risorsa per la registrazione ASN.</span><span class="sxs-lookup"><span data-stu-id="b6816-112">Remove a registerd ASN by resource id.</span></span>

## <span data-ttu-id="b6816-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b6816-113">PARAMETERS</span></span>

### <span data-ttu-id="b6816-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b6816-114">-AsJob</span></span>
<span data-ttu-id="b6816-115">Eseguire in background.</span><span class="sxs-lookup"><span data-stu-id="b6816-115">Run in the background.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6816-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6816-116">-DefaultProfile</span></span>
<span data-ttu-id="b6816-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b6816-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6816-118">-Force</span><span class="sxs-lookup"><span data-stu-id="b6816-118">-Force</span></span>
<span data-ttu-id="b6816-119">Forzare il completamento dell'operazione</span><span class="sxs-lookup"><span data-stu-id="b6816-119">Force the operation to complete</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6816-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b6816-120">-InputObject</span></span>
<span data-ttu-id="b6816-121">Usare un Get-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="b6816-121">Use a Get-AzPeeringServicePrefix</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6816-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="b6816-122">-Name</span></span>
<span data-ttu-id="b6816-123">Nome dell'ASN registrato</span><span class="sxs-lookup"><span data-stu-id="b6816-123">The name of the registered ASN</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6816-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b6816-124">-PassThru</span></span>
<span data-ttu-id="b6816-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="b6816-125">{{ Fill PassThru Description }}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6816-126">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="b6816-126">-PeeringName</span></span>
<span data-ttu-id="b6816-127">Nome univoco di PSPeering.</span><span class="sxs-lookup"><span data-stu-id="b6816-127">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6816-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6816-128">-ResourceGroupName</span></span>
<span data-ttu-id="b6816-129">Il nome della risorsa crea o usa un gruppo di risorse esistente.</span><span class="sxs-lookup"><span data-stu-id="b6816-129">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6816-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b6816-130">-ResourceId</span></span>
<span data-ttu-id="b6816-131">Nome della stringa ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="b6816-131">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6816-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b6816-132">-Confirm</span></span>
<span data-ttu-id="b6816-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6816-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6816-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6816-134">-WhatIf</span></span>
<span data-ttu-id="b6816-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b6816-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6816-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b6816-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6816-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6816-137">CommonParameters</span></span>
<span data-ttu-id="b6816-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6816-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6816-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b6816-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6816-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b6816-140">INPUTS</span></span>

### <span data-ttu-id="b6816-141">Microsoft. Azure. PowerShell. Cmdlets. peering. Models. PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="b6816-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

### <span data-ttu-id="b6816-142">System. String</span><span class="sxs-lookup"><span data-stu-id="b6816-142">System.String</span></span>

## <span data-ttu-id="b6816-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b6816-143">OUTPUTS</span></span>

### <span data-ttu-id="b6816-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b6816-144">System.Boolean</span></span>

## <span data-ttu-id="b6816-145">Note</span><span class="sxs-lookup"><span data-stu-id="b6816-145">NOTES</span></span>

## <span data-ttu-id="b6816-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b6816-146">RELATED LINKS</span></span>
