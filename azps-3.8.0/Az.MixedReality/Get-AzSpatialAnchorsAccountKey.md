---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/get-azspatialanchorsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccountKey.md
ms.openlocfilehash: c5fc1c497bc0cb6f73aab4ddcfbc1ce127cc4545
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022474"
---
# <span data-ttu-id="316c5-101">Get-AzSpatialAnchorsAccountKey</span><span class="sxs-lookup"><span data-stu-id="316c5-101">Get-AzSpatialAnchorsAccountKey</span></span>

## <span data-ttu-id="316c5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="316c5-102">SYNOPSIS</span></span>
<span data-ttu-id="316c5-103">Ottenere le chiavi dell'account degli ancoraggi spaziali</span><span class="sxs-lookup"><span data-stu-id="316c5-103">Get keys of Spatial Anchors Account</span></span>

## <span data-ttu-id="316c5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="316c5-104">SYNTAX</span></span>

### <span data-ttu-id="316c5-105">DefaultParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="316c5-105">DefaultParameterSet (Default)</span></span>
```
Get-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="316c5-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="316c5-106">ResourceIdParameterSet</span></span>
```
Get-AzSpatialAnchorsAccountKey -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="316c5-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="316c5-107">PipelineParameterSet</span></span>
```
Get-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="316c5-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="316c5-108">DESCRIPTION</span></span>
<span data-ttu-id="316c5-109">Ottenere le chiavi dello sviluppatore dell'account degli ancoraggi spaziali.</span><span class="sxs-lookup"><span data-stu-id="316c5-109">Get developer keys of Spatial Anchors Account.</span></span>

## <span data-ttu-id="316c5-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="316c5-110">EXAMPLES</span></span>

### <span data-ttu-id="316c5-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="316c5-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccountKey -ResourceGroup rg1 -Name example

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="316c5-112">Ottenere le chiavi dello sviluppatore dell'account degli ancoraggi spaziali "esempio" dall'abbonamento corrente e dal gruppo di risorse "RG1".</span><span class="sxs-lookup"><span data-stu-id="316c5-112">Get developer keys of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1".</span></span>

### <span data-ttu-id="316c5-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="316c5-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example | Get-AzSpatialAnchorsAccountKey 

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="316c5-114">Ottenere le chiavi dello sviluppatore dell'account degli ancoraggi spaziali "esempio" dall'abbonamento corrente e dal gruppo di risorse "RG1" con piping.</span><span class="sxs-lookup"><span data-stu-id="316c5-114">Get developer keys of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="316c5-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="316c5-115">PARAMETERS</span></span>

### <span data-ttu-id="316c5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="316c5-116">-DefaultProfile</span></span>
<span data-ttu-id="316c5-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="316c5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="316c5-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="316c5-118">-InputObject</span></span>
<span data-ttu-id="316c5-119">Oggetto Domain personalizzato.</span><span class="sxs-lookup"><span data-stu-id="316c5-119">The custom domain object.</span></span>

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

### <span data-ttu-id="316c5-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="316c5-120">-Name</span></span>
<span data-ttu-id="316c5-121">Nome dell'account degli ancoraggi spaziali.</span><span class="sxs-lookup"><span data-stu-id="316c5-121">Spatial Anchors Account Name.</span></span>

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

### <span data-ttu-id="316c5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="316c5-122">-ResourceGroupName</span></span>
<span data-ttu-id="316c5-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="316c5-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="316c5-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="316c5-124">-ResourceId</span></span>
<span data-ttu-id="316c5-125">ID risorsa dell'account degli ancoraggi spaziali.</span><span class="sxs-lookup"><span data-stu-id="316c5-125">Resource ID of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="316c5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="316c5-126">CommonParameters</span></span>
<span data-ttu-id="316c5-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="316c5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="316c5-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="316c5-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="316c5-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="316c5-129">INPUTS</span></span>

### <span data-ttu-id="316c5-130">System. String</span><span class="sxs-lookup"><span data-stu-id="316c5-130">System.String</span></span>

### <span data-ttu-id="316c5-131">Microsoft. Azure. Commands. MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="316c5-131">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="316c5-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="316c5-132">OUTPUTS</span></span>

### <span data-ttu-id="316c5-133">Microsoft. Azure. Commands. MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccountKeys</span><span class="sxs-lookup"><span data-stu-id="316c5-133">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccountKeys</span></span>

## <span data-ttu-id="316c5-134">Note</span><span class="sxs-lookup"><span data-stu-id="316c5-134">NOTES</span></span>

## <span data-ttu-id="316c5-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="316c5-135">RELATED LINKS</span></span>
