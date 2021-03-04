---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/powershell/module/az.mixedreality/get-azspatialanchorsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccountKey.md
ms.openlocfilehash: 351b7a2412a861fcebc456d165e9fc4eddea5122
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957069"
---
# <span data-ttu-id="56c0e-101">Get-AzSpatialAnchorsAccountKey</span><span class="sxs-lookup"><span data-stu-id="56c0e-101">Get-AzSpatialAnchorsAccountKey</span></span>

## <span data-ttu-id="56c0e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56c0e-102">SYNOPSIS</span></span>
<span data-ttu-id="56c0e-103">Ottenere le chiavi dell'account degli ancoraggi nello stato spaziale</span><span class="sxs-lookup"><span data-stu-id="56c0e-103">Get keys of Spatial Anchors Account</span></span>

## <span data-ttu-id="56c0e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="56c0e-104">SYNTAX</span></span>

### <span data-ttu-id="56c0e-105">DefaultParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="56c0e-105">DefaultParameterSet (Default)</span></span>
```
Get-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56c0e-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="56c0e-106">ResourceIdParameterSet</span></span>
```
Get-AzSpatialAnchorsAccountKey -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56c0e-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="56c0e-107">PipelineParameterSet</span></span>
```
Get-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56c0e-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="56c0e-108">DESCRIPTION</span></span>
<span data-ttu-id="56c0e-109">Ottenere le chiavi per sviluppatori dell'account degli ancoraggi nello stato spaziale.</span><span class="sxs-lookup"><span data-stu-id="56c0e-109">Get developer keys of Spatial Anchors Account.</span></span>

## <span data-ttu-id="56c0e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="56c0e-110">EXAMPLES</span></span>

### <span data-ttu-id="56c0e-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="56c0e-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccountKey -ResourceGroup rg1 -Name example

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="56c0e-112">Ottenere le chiavi per sviluppatori dell'account degli ancoraggi nello stato attivo "esempio" dalla sottoscrizione corrente e dal gruppo di risorse "rg1".</span><span class="sxs-lookup"><span data-stu-id="56c0e-112">Get developer keys of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1".</span></span>

### <span data-ttu-id="56c0e-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="56c0e-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example | Get-AzSpatialAnchorsAccountKey 

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="56c0e-114">Ottenere le chiavi di sviluppo dell'account degli ancoraggi nello stato spaziale "esempio" dalla sottoscrizione corrente e dal gruppo di risorse "rg1" con piping.</span><span class="sxs-lookup"><span data-stu-id="56c0e-114">Get developer keys of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="56c0e-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="56c0e-115">PARAMETERS</span></span>

### <span data-ttu-id="56c0e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56c0e-116">-DefaultProfile</span></span>
<span data-ttu-id="56c0e-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="56c0e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56c0e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="56c0e-118">-InputObject</span></span>
<span data-ttu-id="56c0e-119">L'oggetto dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="56c0e-119">The custom domain object.</span></span>

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

### <span data-ttu-id="56c0e-120">-Name</span><span class="sxs-lookup"><span data-stu-id="56c0e-120">-Name</span></span>
<span data-ttu-id="56c0e-121">Nome account per gli ancoraggi nello spaziale.</span><span class="sxs-lookup"><span data-stu-id="56c0e-121">Spatial Anchors Account Name.</span></span>

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

### <span data-ttu-id="56c0e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56c0e-122">-ResourceGroupName</span></span>
<span data-ttu-id="56c0e-123">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="56c0e-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="56c0e-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="56c0e-124">-ResourceId</span></span>
<span data-ttu-id="56c0e-125">ID risorsa dell'account degli ancoraggi nello stato spaziale.</span><span class="sxs-lookup"><span data-stu-id="56c0e-125">Resource ID of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="56c0e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56c0e-126">CommonParameters</span></span>
<span data-ttu-id="56c0e-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56c0e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="56c0e-128">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56c0e-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56c0e-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="56c0e-129">INPUTS</span></span>

### <span data-ttu-id="56c0e-130">System.String</span><span class="sxs-lookup"><span data-stu-id="56c0e-130">System.String</span></span>

### <span data-ttu-id="56c0e-131">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="56c0e-131">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="56c0e-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="56c0e-132">OUTPUTS</span></span>

### <span data-ttu-id="56c0e-133">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="56c0e-133">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSAccountKeys</span></span>

## <span data-ttu-id="56c0e-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="56c0e-134">NOTES</span></span>

## <span data-ttu-id="56c0e-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="56c0e-135">RELATED LINKS</span></span>
