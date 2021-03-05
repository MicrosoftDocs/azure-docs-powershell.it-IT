---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/powershell/module/az.mixedreality/remove-azspatialanchorsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzSpatialAnchorsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzSpatialAnchorsAccount.md
ms.openlocfilehash: 502b7b7c97752758003c1a7f0ad007e3e6cf67e1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980366"
---
# <span data-ttu-id="a6afa-101">Remove-AzSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="a6afa-101">Remove-AzSpatialAnchorsAccount</span></span>

## <span data-ttu-id="a6afa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6afa-102">SYNOPSIS</span></span>
<span data-ttu-id="a6afa-103">Delete Spatial Anchors Account</span><span class="sxs-lookup"><span data-stu-id="a6afa-103">Delete Spatial Anchors Account</span></span>

## <span data-ttu-id="a6afa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a6afa-104">SYNTAX</span></span>

### <span data-ttu-id="a6afa-105">DefaultParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="a6afa-105">DefaultParameterSet (Default)</span></span>
```
Remove-AzSpatialAnchorsAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6afa-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6afa-106">ResourceIdParameterSet</span></span>
```
Remove-AzSpatialAnchorsAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6afa-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6afa-107">PipelineParameterSet</span></span>
```
Remove-AzSpatialAnchorsAccount -InputObject <PSSpatialAnchorsAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6afa-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a6afa-108">DESCRIPTION</span></span>
<span data-ttu-id="a6afa-109">Eliminare l'account degli ancoraggi nello stato spaziale specificato da determinati gruppi di risorse e sottoscrizioni.</span><span class="sxs-lookup"><span data-stu-id="a6afa-109">Delete specified Spatial Anchors Account from certain Subscription and Resource Group.</span></span>

## <span data-ttu-id="a6afa-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a6afa-110">EXAMPLES</span></span>

### <span data-ttu-id="a6afa-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a6afa-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example
```

<span data-ttu-id="a6afa-112">Delete Spatial Anchors Account "example" from current Subscription and Resource Group "rg1".</span><span class="sxs-lookup"><span data-stu-id="a6afa-112">Delete Spatial Anchors Account "example" from current Subscription and Resource Group "rg1".</span></span>

## <span data-ttu-id="a6afa-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a6afa-113">PARAMETERS</span></span>

### <span data-ttu-id="a6afa-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a6afa-114">-Confirm</span></span>
<span data-ttu-id="a6afa-115">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6afa-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6afa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6afa-116">-DefaultProfile</span></span>
<span data-ttu-id="a6afa-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a6afa-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6afa-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a6afa-118">-InputObject</span></span>
<span data-ttu-id="a6afa-119">Oggetto dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="a6afa-119">The custom domain object.</span></span>

```yaml
Type: PSSpatialAnchorsAccount
Parameter Sets: PipelineParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6afa-120">-Name</span><span class="sxs-lookup"><span data-stu-id="a6afa-120">-Name</span></span>
<span data-ttu-id="a6afa-121">Nome account per gli ancoraggi nello spaziale.</span><span class="sxs-lookup"><span data-stu-id="a6afa-121">Spatial Anchors Account Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: SpatialAnchorsAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6afa-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a6afa-122">-PassThru</span></span>
<span data-ttu-id="a6afa-123">Oggetto restituito, se specificato.</span><span class="sxs-lookup"><span data-stu-id="a6afa-123">Return object if specified.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6afa-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6afa-124">-ResourceGroupName</span></span>
<span data-ttu-id="a6afa-125">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a6afa-125">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6afa-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a6afa-126">-ResourceId</span></span>
<span data-ttu-id="a6afa-127">ID risorsa dell'account degli ancoraggi nello stato spaziale.</span><span class="sxs-lookup"><span data-stu-id="a6afa-127">Resource ID of Spatial Anchors Account.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6afa-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6afa-128">-WhatIf</span></span>
<span data-ttu-id="a6afa-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a6afa-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6afa-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a6afa-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6afa-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6afa-131">CommonParameters</span></span>
<span data-ttu-id="a6afa-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6afa-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a6afa-133">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6afa-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6afa-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="a6afa-134">INPUTS</span></span>

### <span data-ttu-id="a6afa-135">System.String</span><span class="sxs-lookup"><span data-stu-id="a6afa-135">System.String</span></span>

### <span data-ttu-id="a6afa-136">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="a6afa-136">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

### <span data-ttu-id="a6afa-137">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a6afa-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a6afa-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a6afa-138">OUTPUTS</span></span>

### <span data-ttu-id="a6afa-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a6afa-139">System.Boolean</span></span>

## <span data-ttu-id="a6afa-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="a6afa-140">NOTES</span></span>

## <span data-ttu-id="a6afa-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a6afa-141">RELATED LINKS</span></span>
