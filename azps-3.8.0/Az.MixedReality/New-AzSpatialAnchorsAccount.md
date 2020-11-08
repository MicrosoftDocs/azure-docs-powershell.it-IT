---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/new-azspatialanchorsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccount.md
ms.openlocfilehash: 2e4379007b296467bf86adff7c46f654eee671e1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022473"
---
# <span data-ttu-id="22e72-101">New-AzSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="22e72-101">New-AzSpatialAnchorsAccount</span></span>

## <span data-ttu-id="22e72-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="22e72-102">SYNOPSIS</span></span>
<span data-ttu-id="22e72-103">Creare un account di ancoraggio spaziale</span><span class="sxs-lookup"><span data-stu-id="22e72-103">Create Spatial Anchors Account</span></span>

## <span data-ttu-id="22e72-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="22e72-104">SYNTAX</span></span>

```
New-AzSpatialAnchorsAccount -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22e72-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="22e72-105">DESCRIPTION</span></span>
<span data-ttu-id="22e72-106">Creare un nuovo account di intelligence spaziale in determinati abbonamenti, gruppi di risorse e aree geografiche.</span><span class="sxs-lookup"><span data-stu-id="22e72-106">Create a new Spatial Intelligence Account in certain Subscription, Resource Group and Region.</span></span>

## <span data-ttu-id="22e72-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="22e72-107">EXAMPLES</span></span>

### <span data-ttu-id="22e72-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="22e72-108">Example 1</span></span>
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

<span data-ttu-id="22e72-109">Creare un nuovo account di ancoraggio spaziale "esempio" nell'abbonamento corrente, gruppo risorse "RG1" e Central US.</span><span class="sxs-lookup"><span data-stu-id="22e72-109">Create a new Spatial Anchors Account "example" in current Subscription, Resource Group "rg1" and Central US.</span></span>

## <span data-ttu-id="22e72-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="22e72-110">PARAMETERS</span></span>

### <span data-ttu-id="22e72-111">-Confermare</span><span class="sxs-lookup"><span data-stu-id="22e72-111">-Confirm</span></span>
<span data-ttu-id="22e72-112">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22e72-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22e72-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22e72-113">-DefaultProfile</span></span>
<span data-ttu-id="22e72-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="22e72-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22e72-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="22e72-115">-Location</span></span>
<span data-ttu-id="22e72-116">Posizione dell'account ancoraggi spaziali.</span><span class="sxs-lookup"><span data-stu-id="22e72-116">Spatial Anchors Account Location.</span></span>

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

### <span data-ttu-id="22e72-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="22e72-117">-Name</span></span>
<span data-ttu-id="22e72-118">Nome dell'account degli ancoraggi spaziali.</span><span class="sxs-lookup"><span data-stu-id="22e72-118">Spatial Anchors Account Name.</span></span>

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

### <span data-ttu-id="22e72-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22e72-119">-ResourceGroupName</span></span>
<span data-ttu-id="22e72-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="22e72-120">Resource Group Name.</span></span>

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

### <span data-ttu-id="22e72-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22e72-121">-WhatIf</span></span>
<span data-ttu-id="22e72-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="22e72-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22e72-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="22e72-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22e72-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22e72-124">CommonParameters</span></span>
<span data-ttu-id="22e72-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22e72-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="22e72-126">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22e72-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22e72-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="22e72-127">INPUTS</span></span>

### <span data-ttu-id="22e72-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="22e72-128">None</span></span>

## <span data-ttu-id="22e72-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="22e72-129">OUTPUTS</span></span>

### <span data-ttu-id="22e72-130">Microsoft. Azure. Commands. MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="22e72-130">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="22e72-131">Note</span><span class="sxs-lookup"><span data-stu-id="22e72-131">NOTES</span></span>

## <span data-ttu-id="22e72-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="22e72-132">RELATED LINKS</span></span>
