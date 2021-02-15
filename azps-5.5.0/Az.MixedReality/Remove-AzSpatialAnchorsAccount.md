---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/remove-azspatialanchorsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzSpatialAnchorsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzSpatialAnchorsAccount.md
ms.openlocfilehash: 5ba079a17dcfb0a263766237adbbec9beb4cc64c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203578"
---
# <span data-ttu-id="9647b-101">Remove-AzSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="9647b-101">Remove-AzSpatialAnchorsAccount</span></span>

## <span data-ttu-id="9647b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9647b-102">SYNOPSIS</span></span>
<span data-ttu-id="9647b-103">Delete Spatial Anchors Account</span><span class="sxs-lookup"><span data-stu-id="9647b-103">Delete Spatial Anchors Account</span></span>

## <span data-ttu-id="9647b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9647b-104">SYNTAX</span></span>

### <span data-ttu-id="9647b-105">DefaultParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="9647b-105">DefaultParameterSet (Default)</span></span>
```
Remove-AzSpatialAnchorsAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9647b-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9647b-106">ResourceIdParameterSet</span></span>
```
Remove-AzSpatialAnchorsAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9647b-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="9647b-107">PipelineParameterSet</span></span>
```
Remove-AzSpatialAnchorsAccount -InputObject <PSSpatialAnchorsAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9647b-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9647b-108">DESCRIPTION</span></span>
<span data-ttu-id="9647b-109">Eliminare l'account degli ancoraggi nello stato spaziale specificato da determinati gruppi di risorse e sottoscrizioni.</span><span class="sxs-lookup"><span data-stu-id="9647b-109">Delete specified Spatial Anchors Account from certain Subscription and Resource Group.</span></span>

## <span data-ttu-id="9647b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9647b-110">EXAMPLES</span></span>

### <span data-ttu-id="9647b-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9647b-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example
```

<span data-ttu-id="9647b-112">Delete Spatial Anchors Account "example" from current Subscription and Resource Group "rg1".</span><span class="sxs-lookup"><span data-stu-id="9647b-112">Delete Spatial Anchors Account "example" from current Subscription and Resource Group "rg1".</span></span>

## <span data-ttu-id="9647b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9647b-113">PARAMETERS</span></span>

### <span data-ttu-id="9647b-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9647b-114">-Confirm</span></span>
<span data-ttu-id="9647b-115">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9647b-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9647b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9647b-116">-DefaultProfile</span></span>
<span data-ttu-id="9647b-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9647b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9647b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9647b-118">-InputObject</span></span>
<span data-ttu-id="9647b-119">L'oggetto dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="9647b-119">The custom domain object.</span></span>

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

### <span data-ttu-id="9647b-120">-Name</span><span class="sxs-lookup"><span data-stu-id="9647b-120">-Name</span></span>
<span data-ttu-id="9647b-121">Nome account per gli ancoraggi nello spaziale.</span><span class="sxs-lookup"><span data-stu-id="9647b-121">Spatial Anchors Account Name.</span></span>

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

### <span data-ttu-id="9647b-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9647b-122">-PassThru</span></span>
<span data-ttu-id="9647b-123">Oggetto restituito, se specificato.</span><span class="sxs-lookup"><span data-stu-id="9647b-123">Return object if specified.</span></span>

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

### <span data-ttu-id="9647b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9647b-124">-ResourceGroupName</span></span>
<span data-ttu-id="9647b-125">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9647b-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="9647b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9647b-126">-ResourceId</span></span>
<span data-ttu-id="9647b-127">ID risorsa dell'account degli ancoraggi nello stato spaziale.</span><span class="sxs-lookup"><span data-stu-id="9647b-127">Resource ID of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="9647b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9647b-128">-WhatIf</span></span>
<span data-ttu-id="9647b-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9647b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9647b-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9647b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9647b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9647b-131">CommonParameters</span></span>
<span data-ttu-id="9647b-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9647b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="9647b-133">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9647b-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9647b-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="9647b-134">INPUTS</span></span>

### <span data-ttu-id="9647b-135">System.String</span><span class="sxs-lookup"><span data-stu-id="9647b-135">System.String</span></span>

### <span data-ttu-id="9647b-136">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="9647b-136">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

### <span data-ttu-id="9647b-137">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9647b-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9647b-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9647b-138">OUTPUTS</span></span>

### <span data-ttu-id="9647b-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9647b-139">System.Boolean</span></span>

## <span data-ttu-id="9647b-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="9647b-140">NOTES</span></span>

## <span data-ttu-id="9647b-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9647b-141">RELATED LINKS</span></span>
