---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/remove-azspatialanchorsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzSpatialAnchorsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzSpatialAnchorsAccount.md
ms.openlocfilehash: 2d164e08876b5489ec45ce146f4f3c7cee3ee6d5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93673842"
---
# <span data-ttu-id="6325a-101">Remove-AzSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="6325a-101">Remove-AzSpatialAnchorsAccount</span></span>

## <span data-ttu-id="6325a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6325a-102">SYNOPSIS</span></span>
<span data-ttu-id="6325a-103">Eliminare l'account degli ancoraggi spaziali</span><span class="sxs-lookup"><span data-stu-id="6325a-103">Delete Spatial Anchors Account</span></span>

## <span data-ttu-id="6325a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6325a-104">SYNTAX</span></span>

### <span data-ttu-id="6325a-105">DefaultParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6325a-105">DefaultParameterSet (Default)</span></span>
```
Remove-AzSpatialAnchorsAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6325a-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6325a-106">ResourceIdParameterSet</span></span>
```
Remove-AzSpatialAnchorsAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6325a-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="6325a-107">PipelineParameterSet</span></span>
```
Remove-AzSpatialAnchorsAccount -InputObject <PSSpatialAnchorsAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6325a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6325a-108">DESCRIPTION</span></span>
<span data-ttu-id="6325a-109">Eliminare l'account di ancoraggio spaziale specificato da un determinato gruppo di abbonamenti e risorse.</span><span class="sxs-lookup"><span data-stu-id="6325a-109">Delete specified Spatial Anchors Account from certain Subscription and Resource Group.</span></span>

## <span data-ttu-id="6325a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6325a-110">EXAMPLES</span></span>

### <span data-ttu-id="6325a-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6325a-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example
```

<span data-ttu-id="6325a-112">Eliminare l'account degli ancoraggi spaziali "esempio" dall'abbonamento corrente e dal gruppo di risorse "RG1".</span><span class="sxs-lookup"><span data-stu-id="6325a-112">Delete Spatial Anchors Account "example" from current Subscription and Resource Group "rg1".</span></span>

## <span data-ttu-id="6325a-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6325a-113">PARAMETERS</span></span>

### <span data-ttu-id="6325a-114">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6325a-114">-Confirm</span></span>
<span data-ttu-id="6325a-115">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6325a-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6325a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6325a-116">-DefaultProfile</span></span>
<span data-ttu-id="6325a-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6325a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6325a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6325a-118">-InputObject</span></span>
<span data-ttu-id="6325a-119">Oggetto Domain personalizzato.</span><span class="sxs-lookup"><span data-stu-id="6325a-119">The custom domain object.</span></span>

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

### <span data-ttu-id="6325a-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="6325a-120">-Name</span></span>
<span data-ttu-id="6325a-121">Nome dell'account degli ancoraggi spaziali.</span><span class="sxs-lookup"><span data-stu-id="6325a-121">Spatial Anchors Account Name.</span></span>

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

### <span data-ttu-id="6325a-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6325a-122">-PassThru</span></span>
<span data-ttu-id="6325a-123">Restituisce l'oggetto se specificato.</span><span class="sxs-lookup"><span data-stu-id="6325a-123">Return object if specified.</span></span>

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

### <span data-ttu-id="6325a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6325a-124">-ResourceGroupName</span></span>
<span data-ttu-id="6325a-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6325a-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="6325a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6325a-126">-ResourceId</span></span>
<span data-ttu-id="6325a-127">ID risorsa dell'account degli ancoraggi spaziali.</span><span class="sxs-lookup"><span data-stu-id="6325a-127">Resource ID of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="6325a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6325a-128">-WhatIf</span></span>
<span data-ttu-id="6325a-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6325a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6325a-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6325a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6325a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6325a-131">CommonParameters</span></span>
<span data-ttu-id="6325a-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6325a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="6325a-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6325a-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6325a-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6325a-134">INPUTS</span></span>

### <span data-ttu-id="6325a-135">System. String</span><span class="sxs-lookup"><span data-stu-id="6325a-135">System.String</span></span>

### <span data-ttu-id="6325a-136">Microsoft. Azure. Commands. MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="6325a-136">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

### <span data-ttu-id="6325a-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6325a-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6325a-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6325a-138">OUTPUTS</span></span>

### <span data-ttu-id="6325a-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6325a-139">System.Boolean</span></span>

## <span data-ttu-id="6325a-140">Note</span><span class="sxs-lookup"><span data-stu-id="6325a-140">NOTES</span></span>

## <span data-ttu-id="6325a-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6325a-141">RELATED LINKS</span></span>
