---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/get-azspatialanchorsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccountKey.md
ms.openlocfilehash: ec84b4def7b1dfd19b2c85c71dc6562fa4cae763
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93673846"
---
# <span data-ttu-id="39cbe-101">Get-AzSpatialAnchorsAccountKey</span><span class="sxs-lookup"><span data-stu-id="39cbe-101">Get-AzSpatialAnchorsAccountKey</span></span>

## <span data-ttu-id="39cbe-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="39cbe-102">SYNOPSIS</span></span>
<span data-ttu-id="39cbe-103">Ottenere le chiavi dell'account degli ancoraggi spaziali</span><span class="sxs-lookup"><span data-stu-id="39cbe-103">Get keys of Spatial Anchors Account</span></span>

## <span data-ttu-id="39cbe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="39cbe-104">SYNTAX</span></span>

### <span data-ttu-id="39cbe-105">DefaultParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="39cbe-105">DefaultParameterSet (Default)</span></span>
```
Get-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39cbe-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="39cbe-106">ResourceIdParameterSet</span></span>
```
Get-AzSpatialAnchorsAccountKey -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39cbe-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="39cbe-107">PipelineParameterSet</span></span>
```
Get-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39cbe-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="39cbe-108">DESCRIPTION</span></span>
<span data-ttu-id="39cbe-109">Ottenere le chiavi dello sviluppatore dell'account degli ancoraggi spaziali.</span><span class="sxs-lookup"><span data-stu-id="39cbe-109">Get developer keys of Spatial Anchors Account.</span></span>

## <span data-ttu-id="39cbe-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="39cbe-110">EXAMPLES</span></span>

### <span data-ttu-id="39cbe-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="39cbe-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccountKey -ResourceGroup rg1 -Name example

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="39cbe-112">Ottenere le chiavi dello sviluppatore dell'account degli ancoraggi spaziali "esempio" dall'abbonamento corrente e dal gruppo di risorse "RG1".</span><span class="sxs-lookup"><span data-stu-id="39cbe-112">Get developer keys of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1".</span></span>

### <span data-ttu-id="39cbe-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="39cbe-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example | Get-AzSpatialAnchorsAccountKey 

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="39cbe-114">Ottenere le chiavi dello sviluppatore dell'account degli ancoraggi spaziali "esempio" dall'abbonamento corrente e dal gruppo di risorse "RG1" con piping.</span><span class="sxs-lookup"><span data-stu-id="39cbe-114">Get developer keys of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="39cbe-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="39cbe-115">PARAMETERS</span></span>

### <span data-ttu-id="39cbe-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39cbe-116">-DefaultProfile</span></span>
<span data-ttu-id="39cbe-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="39cbe-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39cbe-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="39cbe-118">-InputObject</span></span>
<span data-ttu-id="39cbe-119">Oggetto Domain personalizzato.</span><span class="sxs-lookup"><span data-stu-id="39cbe-119">The custom domain object.</span></span>

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

### <span data-ttu-id="39cbe-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="39cbe-120">-Name</span></span>
<span data-ttu-id="39cbe-121">Nome dell'account degli ancoraggi spaziali.</span><span class="sxs-lookup"><span data-stu-id="39cbe-121">Spatial Anchors Account Name.</span></span>

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

### <span data-ttu-id="39cbe-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39cbe-122">-ResourceGroupName</span></span>
<span data-ttu-id="39cbe-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="39cbe-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="39cbe-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="39cbe-124">-ResourceId</span></span>
<span data-ttu-id="39cbe-125">ID risorsa dell'account degli ancoraggi spaziali.</span><span class="sxs-lookup"><span data-stu-id="39cbe-125">Resource ID of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="39cbe-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39cbe-126">CommonParameters</span></span>
<span data-ttu-id="39cbe-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39cbe-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="39cbe-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39cbe-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39cbe-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="39cbe-129">INPUTS</span></span>

### <span data-ttu-id="39cbe-130">System. String</span><span class="sxs-lookup"><span data-stu-id="39cbe-130">System.String</span></span>

### <span data-ttu-id="39cbe-131">Microsoft. Azure. Commands. MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="39cbe-131">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="39cbe-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="39cbe-132">OUTPUTS</span></span>

### <span data-ttu-id="39cbe-133">Microsoft. Azure. Commands. MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccountKeys</span><span class="sxs-lookup"><span data-stu-id="39cbe-133">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccountKeys</span></span>

## <span data-ttu-id="39cbe-134">Note</span><span class="sxs-lookup"><span data-stu-id="39cbe-134">NOTES</span></span>

## <span data-ttu-id="39cbe-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="39cbe-135">RELATED LINKS</span></span>
