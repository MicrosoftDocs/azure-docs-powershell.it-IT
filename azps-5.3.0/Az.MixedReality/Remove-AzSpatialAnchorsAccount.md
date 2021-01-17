---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/remove-azspatialanchorsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzSpatialAnchorsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzSpatialAnchorsAccount.md
ms.openlocfilehash: 5ba079a17dcfb0a263766237adbbec9beb4cc64c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476433"
---
# <span data-ttu-id="6605d-101">Remove-AzSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="6605d-101">Remove-AzSpatialAnchorsAccount</span></span>

## <span data-ttu-id="6605d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6605d-102">SYNOPSIS</span></span>
<span data-ttu-id="6605d-103">Eliminare l'account degli ancoraggi spaziali</span><span class="sxs-lookup"><span data-stu-id="6605d-103">Delete Spatial Anchors Account</span></span>

## <span data-ttu-id="6605d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6605d-104">SYNTAX</span></span>

### <span data-ttu-id="6605d-105">DefaultParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6605d-105">DefaultParameterSet (Default)</span></span>
```
Remove-AzSpatialAnchorsAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6605d-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6605d-106">ResourceIdParameterSet</span></span>
```
Remove-AzSpatialAnchorsAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6605d-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="6605d-107">PipelineParameterSet</span></span>
```
Remove-AzSpatialAnchorsAccount -InputObject <PSSpatialAnchorsAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6605d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6605d-108">DESCRIPTION</span></span>
<span data-ttu-id="6605d-109">Eliminare l'account di ancoraggio spaziale specificato da un determinato gruppo di abbonamenti e risorse.</span><span class="sxs-lookup"><span data-stu-id="6605d-109">Delete specified Spatial Anchors Account from certain Subscription and Resource Group.</span></span>

## <span data-ttu-id="6605d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6605d-110">EXAMPLES</span></span>

### <span data-ttu-id="6605d-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6605d-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example
```

<span data-ttu-id="6605d-112">Eliminare l'account degli ancoraggi spaziali "esempio" dall'abbonamento corrente e dal gruppo di risorse "RG1".</span><span class="sxs-lookup"><span data-stu-id="6605d-112">Delete Spatial Anchors Account "example" from current Subscription and Resource Group "rg1".</span></span>

## <span data-ttu-id="6605d-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6605d-113">PARAMETERS</span></span>

### <span data-ttu-id="6605d-114">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6605d-114">-Confirm</span></span>
<span data-ttu-id="6605d-115">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6605d-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6605d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6605d-116">-DefaultProfile</span></span>
<span data-ttu-id="6605d-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6605d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6605d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6605d-118">-InputObject</span></span>
<span data-ttu-id="6605d-119">Oggetto Domain personalizzato.</span><span class="sxs-lookup"><span data-stu-id="6605d-119">The custom domain object.</span></span>

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

### <span data-ttu-id="6605d-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="6605d-120">-Name</span></span>
<span data-ttu-id="6605d-121">Nome dell'account degli ancoraggi spaziali.</span><span class="sxs-lookup"><span data-stu-id="6605d-121">Spatial Anchors Account Name.</span></span>

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

### <span data-ttu-id="6605d-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6605d-122">-PassThru</span></span>
<span data-ttu-id="6605d-123">Restituisce l'oggetto se specificato.</span><span class="sxs-lookup"><span data-stu-id="6605d-123">Return object if specified.</span></span>

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

### <span data-ttu-id="6605d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6605d-124">-ResourceGroupName</span></span>
<span data-ttu-id="6605d-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6605d-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="6605d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6605d-126">-ResourceId</span></span>
<span data-ttu-id="6605d-127">ID risorsa dell'account degli ancoraggi spaziali.</span><span class="sxs-lookup"><span data-stu-id="6605d-127">Resource ID of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="6605d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6605d-128">-WhatIf</span></span>
<span data-ttu-id="6605d-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6605d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6605d-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6605d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6605d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6605d-131">CommonParameters</span></span>
<span data-ttu-id="6605d-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6605d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="6605d-133">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6605d-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6605d-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6605d-134">INPUTS</span></span>

### <span data-ttu-id="6605d-135">System. String</span><span class="sxs-lookup"><span data-stu-id="6605d-135">System.String</span></span>

### <span data-ttu-id="6605d-136">Microsoft. Azure. Commands. MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="6605d-136">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

### <span data-ttu-id="6605d-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6605d-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6605d-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6605d-138">OUTPUTS</span></span>

### <span data-ttu-id="6605d-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6605d-139">System.Boolean</span></span>

## <span data-ttu-id="6605d-140">Note</span><span class="sxs-lookup"><span data-stu-id="6605d-140">NOTES</span></span>

## <span data-ttu-id="6605d-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6605d-141">RELATED LINKS</span></span>
