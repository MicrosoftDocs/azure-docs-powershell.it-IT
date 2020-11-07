---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/new-azspatialanchorsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccount.md
ms.openlocfilehash: 2d3d4247aa801124f0bad54b40386fa45493f777
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93673845"
---
# <span data-ttu-id="23f46-101">New-AzSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="23f46-101">New-AzSpatialAnchorsAccount</span></span>

## <span data-ttu-id="23f46-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="23f46-102">SYNOPSIS</span></span>
<span data-ttu-id="23f46-103">Creare un account di ancoraggio spaziale</span><span class="sxs-lookup"><span data-stu-id="23f46-103">Create Spatial Anchors Account</span></span>

## <span data-ttu-id="23f46-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="23f46-104">SYNTAX</span></span>

```
New-AzSpatialAnchorsAccount -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23f46-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="23f46-105">DESCRIPTION</span></span>
<span data-ttu-id="23f46-106">Creare un nuovo account di intelligence spaziale in determinati abbonamenti, gruppi di risorse e aree geografiche.</span><span class="sxs-lookup"><span data-stu-id="23f46-106">Create a new Spatial Intelligence Account in certain Subscription, Resource Group and Region.</span></span>

## <span data-ttu-id="23f46-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="23f46-107">EXAMPLES</span></span>

### <span data-ttu-id="23f46-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="23f46-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmSpatialAnchorsAccount -ResourceGroup rg1 -Name example -Location centralus

ResourceGroupName   : rg1
AccountId           : 5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef/
AccountDomain       : mixedreality.azure.com
Tags                : {}
Location            : centralus
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/SpatialAnchorsAccounts/example
Name                : example
Type                : Microsoft.MixedReality/SpatialAnchorsAccounts
```

<span data-ttu-id="23f46-109">Creare un nuovo account di ancoraggio spaziale "esempio" nell'abbonamento corrente, gruppo risorse "RG1" e Central US.</span><span class="sxs-lookup"><span data-stu-id="23f46-109">Create a new Spatial Anchors Account "example" in current Subscription, Resource Group "rg1" and Central US.</span></span>

## <span data-ttu-id="23f46-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="23f46-110">PARAMETERS</span></span>

### <span data-ttu-id="23f46-111">-Confermare</span><span class="sxs-lookup"><span data-stu-id="23f46-111">-Confirm</span></span>
<span data-ttu-id="23f46-112">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23f46-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23f46-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23f46-113">-DefaultProfile</span></span>
<span data-ttu-id="23f46-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="23f46-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23f46-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="23f46-115">-Location</span></span>
<span data-ttu-id="23f46-116">Posizione dell'account ancoraggi spaziali.</span><span class="sxs-lookup"><span data-stu-id="23f46-116">Spatial Anchors Account Location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23f46-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="23f46-117">-Name</span></span>
<span data-ttu-id="23f46-118">Nome dell'account degli ancoraggi spaziali.</span><span class="sxs-lookup"><span data-stu-id="23f46-118">Spatial Anchors Account Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SpatialAnchorsAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23f46-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23f46-119">-ResourceGroupName</span></span>
<span data-ttu-id="23f46-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="23f46-120">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23f46-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23f46-121">-WhatIf</span></span>
<span data-ttu-id="23f46-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="23f46-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23f46-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="23f46-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23f46-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23f46-124">CommonParameters</span></span>
<span data-ttu-id="23f46-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23f46-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="23f46-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23f46-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23f46-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="23f46-127">INPUTS</span></span>

### <span data-ttu-id="23f46-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="23f46-128">None</span></span>

## <span data-ttu-id="23f46-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="23f46-129">OUTPUTS</span></span>

### <span data-ttu-id="23f46-130">Microsoft. Azure. Commands. MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="23f46-130">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="23f46-131">Note</span><span class="sxs-lookup"><span data-stu-id="23f46-131">NOTES</span></span>

## <span data-ttu-id="23f46-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="23f46-132">RELATED LINKS</span></span>
