---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredAsn.md
ms.openlocfilehash: d43fe033b58ba6295728bc0c21ddb1d853587b59
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330823"
---
# <span data-ttu-id="6a073-101">Remove-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="6a073-101">Remove-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="6a073-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6a073-102">SYNOPSIS</span></span>
<span data-ttu-id="6a073-103">Eliminare o rimuovere un ASN registrato dalla risorsa peering padre.</span><span class="sxs-lookup"><span data-stu-id="6a073-103">Delete or remove a registered ASN from the parent peering resource.</span></span>

## <span data-ttu-id="6a073-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6a073-104">SYNTAX</span></span>

### <span data-ttu-id="6a073-105">ByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6a073-105">ByName (Default)</span></span>
```
Remove-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String> [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a073-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="6a073-106">InputObject</span></span>
```
Remove-AzPeeringRegisteredAsn -InputObject <PSPeeringServicePrefix> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a073-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6a073-107">ByResourceId</span></span>
```
Remove-AzPeeringRegisteredAsn [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a073-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6a073-108">DESCRIPTION</span></span>
<span data-ttu-id="6a073-109">Consente la rimozione di ASN registrato dalla risorsa peering padre.</span><span class="sxs-lookup"><span data-stu-id="6a073-109">Allows the removal of registered ASN from parent peering resource.</span></span>

## <span data-ttu-id="6a073-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6a073-110">EXAMPLES</span></span>

### <span data-ttu-id="6a073-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6a073-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzPeeringRegisteredAsn -ResourceId $resourceId
```

<span data-ttu-id="6a073-112">Rimuovi un ID di risorsa per la registrazione ASN.</span><span class="sxs-lookup"><span data-stu-id="6a073-112">Remove a registerd ASN by resource id.</span></span>

## <span data-ttu-id="6a073-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6a073-113">PARAMETERS</span></span>

### <span data-ttu-id="6a073-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6a073-114">-AsJob</span></span>
<span data-ttu-id="6a073-115">Eseguire in background.</span><span class="sxs-lookup"><span data-stu-id="6a073-115">Run in the background.</span></span>

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

### <span data-ttu-id="6a073-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a073-116">-DefaultProfile</span></span>
<span data-ttu-id="6a073-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6a073-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a073-118">-Force</span><span class="sxs-lookup"><span data-stu-id="6a073-118">-Force</span></span>
<span data-ttu-id="6a073-119">Forzare il completamento dell'operazione</span><span class="sxs-lookup"><span data-stu-id="6a073-119">Force the operation to complete</span></span>

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

### <span data-ttu-id="6a073-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6a073-120">-InputObject</span></span>
<span data-ttu-id="6a073-121">Usare un Get-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="6a073-121">Use a Get-AzPeeringServicePrefix</span></span>

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

### <span data-ttu-id="6a073-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="6a073-122">-Name</span></span>
<span data-ttu-id="6a073-123">Nome dell'ASN registrato</span><span class="sxs-lookup"><span data-stu-id="6a073-123">The name of the registered ASN</span></span>

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

### <span data-ttu-id="6a073-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6a073-124">-PassThru</span></span>
<span data-ttu-id="6a073-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="6a073-125">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="6a073-126">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="6a073-126">-PeeringName</span></span>
<span data-ttu-id="6a073-127">Nome univoco di PSPeering.</span><span class="sxs-lookup"><span data-stu-id="6a073-127">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="6a073-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a073-128">-ResourceGroupName</span></span>
<span data-ttu-id="6a073-129">Il nome della risorsa crea o usa un gruppo di risorse esistente.</span><span class="sxs-lookup"><span data-stu-id="6a073-129">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="6a073-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6a073-130">-ResourceId</span></span>
<span data-ttu-id="6a073-131">Nome della stringa ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="6a073-131">The resource id string name.</span></span>

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

### <span data-ttu-id="6a073-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6a073-132">-Confirm</span></span>
<span data-ttu-id="6a073-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a073-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a073-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a073-134">-WhatIf</span></span>
<span data-ttu-id="6a073-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6a073-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a073-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6a073-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a073-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a073-137">CommonParameters</span></span>
<span data-ttu-id="6a073-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a073-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a073-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6a073-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a073-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6a073-140">INPUTS</span></span>

### <span data-ttu-id="6a073-141">Microsoft. Azure. PowerShell. Cmdlets. peering. Models. PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="6a073-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

### <span data-ttu-id="6a073-142">System. String</span><span class="sxs-lookup"><span data-stu-id="6a073-142">System.String</span></span>

## <span data-ttu-id="6a073-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6a073-143">OUTPUTS</span></span>

### <span data-ttu-id="6a073-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6a073-144">System.Boolean</span></span>

## <span data-ttu-id="6a073-145">Note</span><span class="sxs-lookup"><span data-stu-id="6a073-145">NOTES</span></span>

## <span data-ttu-id="6a073-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6a073-146">RELATED LINKS</span></span>
