---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/get-azspatialanchorsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccountKey.md
ms.openlocfilehash: 81bce36cb1b8cd4737141e58ad3e220199e726cf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194071"
---
# <span data-ttu-id="7527e-101">Get-AzSpatialAnchorsAccountKey</span><span class="sxs-lookup"><span data-stu-id="7527e-101">Get-AzSpatialAnchorsAccountKey</span></span>

## <span data-ttu-id="7527e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7527e-102">SYNOPSIS</span></span>
<span data-ttu-id="7527e-103">Ottenere le chiavi dell'account degli ancoraggi nello stato spaziale</span><span class="sxs-lookup"><span data-stu-id="7527e-103">Get keys of Spatial Anchors Account</span></span>

## <span data-ttu-id="7527e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7527e-104">SYNTAX</span></span>

### <span data-ttu-id="7527e-105">DefaultParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="7527e-105">DefaultParameterSet (Default)</span></span>
```
Get-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7527e-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7527e-106">ResourceIdParameterSet</span></span>
```
Get-AzSpatialAnchorsAccountKey -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7527e-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="7527e-107">PipelineParameterSet</span></span>
```
Get-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7527e-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7527e-108">DESCRIPTION</span></span>
<span data-ttu-id="7527e-109">Ottenere le chiavi per sviluppatori dell'account degli ancoraggi nello stato spaziale.</span><span class="sxs-lookup"><span data-stu-id="7527e-109">Get developer keys of Spatial Anchors Account.</span></span>

## <span data-ttu-id="7527e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7527e-110">EXAMPLES</span></span>

### <span data-ttu-id="7527e-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7527e-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccountKey -ResourceGroup rg1 -Name example

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="7527e-112">Ottenere le chiavi per sviluppatori dell'account degli ancoraggi nello stato attivo "esempio" dalla sottoscrizione corrente e dal gruppo di risorse "rg1".</span><span class="sxs-lookup"><span data-stu-id="7527e-112">Get developer keys of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1".</span></span>

### <span data-ttu-id="7527e-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="7527e-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example | Get-AzSpatialAnchorsAccountKey 

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="7527e-114">Ottenere le chiavi di sviluppo dell'account degli ancoraggi nello stato spaziale "esempio" dalla sottoscrizione corrente e dal gruppo di risorse "rg1" con piping.</span><span class="sxs-lookup"><span data-stu-id="7527e-114">Get developer keys of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="7527e-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7527e-115">PARAMETERS</span></span>

### <span data-ttu-id="7527e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7527e-116">-DefaultProfile</span></span>
<span data-ttu-id="7527e-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7527e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7527e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7527e-118">-InputObject</span></span>
<span data-ttu-id="7527e-119">L'oggetto dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="7527e-119">The custom domain object.</span></span>

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

### <span data-ttu-id="7527e-120">-Name</span><span class="sxs-lookup"><span data-stu-id="7527e-120">-Name</span></span>
<span data-ttu-id="7527e-121">Nome account per gli ancoraggi nello spaziale.</span><span class="sxs-lookup"><span data-stu-id="7527e-121">Spatial Anchors Account Name.</span></span>

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

### <span data-ttu-id="7527e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7527e-122">-ResourceGroupName</span></span>
<span data-ttu-id="7527e-123">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7527e-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="7527e-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7527e-124">-ResourceId</span></span>
<span data-ttu-id="7527e-125">ID risorsa dell'account degli ancoraggi nello stato spaziale.</span><span class="sxs-lookup"><span data-stu-id="7527e-125">Resource ID of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="7527e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7527e-126">CommonParameters</span></span>
<span data-ttu-id="7527e-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7527e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="7527e-128">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7527e-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7527e-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="7527e-129">INPUTS</span></span>

### <span data-ttu-id="7527e-130">System.String</span><span class="sxs-lookup"><span data-stu-id="7527e-130">System.String</span></span>

### <span data-ttu-id="7527e-131">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="7527e-131">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="7527e-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7527e-132">OUTPUTS</span></span>

### <span data-ttu-id="7527e-133">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="7527e-133">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSAccountKeys</span></span>

## <span data-ttu-id="7527e-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="7527e-134">NOTES</span></span>

## <span data-ttu-id="7527e-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7527e-135">RELATED LINKS</span></span>
