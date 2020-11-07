---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/get-azspatialanchorsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccount.md
ms.openlocfilehash: 3008ff1f824f70d61ec626cdf51a962b3547a7d1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93673848"
---
# <span data-ttu-id="447b2-101">Get-AzSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="447b2-101">Get-AzSpatialAnchorsAccount</span></span>

## <span data-ttu-id="447b2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="447b2-102">SYNOPSIS</span></span>
<span data-ttu-id="447b2-103">Ottenere l'account degli ancoraggi spaziali</span><span class="sxs-lookup"><span data-stu-id="447b2-103">Get Spatial Anchors Account</span></span>

## <span data-ttu-id="447b2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="447b2-104">SYNTAX</span></span>

### <span data-ttu-id="447b2-105">ListParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="447b2-105">ListParameterSet (Default)</span></span>
```
Get-AzSpatialAnchorsAccount [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="447b2-106">Getparameterst (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="447b2-106">GetParameterSet (Default)</span></span>
```
Get-AzSpatialAnchorsAccount -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="447b2-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="447b2-107">ResourceIdParameterSet</span></span>
```
Get-AzSpatialAnchorsAccount -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="447b2-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="447b2-108">DESCRIPTION</span></span>
<span data-ttu-id="447b2-109">Ottenere o elencare gli account degli ancoraggi spaziali in un determinato gruppo di abbonamenti e risorse.</span><span class="sxs-lookup"><span data-stu-id="447b2-109">Get or list Spatial Anchors Account(s) in certain Subscription and Resource Group.</span></span>

## <span data-ttu-id="447b2-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="447b2-110">EXAMPLES</span></span>

### <span data-ttu-id="447b2-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="447b2-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccount -ResourceGroup rg1

ResourceGroupName   : rg1
AccountId           : 5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef/
AccountDomain       : mixedreality.azure.com
Tags                : {}
Location            : eastus2
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/SpatialAnchorsAccounts/example
Name                : example
Type                : Microsoft.MixedReality/SpatialAnchorsAccounts

ResourceGroupName   : rg1
AccountId           : 2f7443d0-2c2b-4514-9b29-a78072a1556f
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/2f7443d0-2c2b-4514-9b29-a78072a1556f/
AccountDomain       : mixedreality.azure.com
Tags                : {}
Location            : eastus2
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/SpatialAnchorsAccounts/demo
Name                : demo
Type                : Microsoft.MixedReality/SpatialAnchorsAccounts

ResourceGroupName   : rg1
AccountId           : ed3273ce-1eeb-42c7-b3b8-fb9896b9801c
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/ed3273ce-1eeb-42c7-b3b8-fb9896b9801c/
AccountDomain       : mixedreality.azure.com
Tags                : {}
Location            : eastus2
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/SpatialAnchorsAccounts/foobar
Name                : foobar
Type                : Microsoft.MixedReality/SpatialAnchorsAccounts
```

<span data-ttu-id="447b2-112">Elencare tutti gli account di ancoraggio spaziali nel gruppo di risorse "RG1".</span><span class="sxs-lookup"><span data-stu-id="447b2-112">List all Spatial Anchors Account in Resource Group "rg1".</span></span> 

### <span data-ttu-id="447b2-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="447b2-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example

ResourceGroupName   : rg1
AccountId           : 5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef/
AccountDomain       : mrc-anchor-prod.trafficmanager.net
Tags                : {}
Location            : eastus2
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/SpatialAnchorsAccounts/example
Name                : example
Type                : Microsoft.MixedReality/SpatialAnchorsAccounts
```

<span data-ttu-id="447b2-114">Ottenere l'account degli ancoraggi spaziali "esempio" nel gruppo di risorse "RG1".</span><span class="sxs-lookup"><span data-stu-id="447b2-114">Get Spatial Anchors Account "example" in Resource Group "rg1".</span></span> 

## <span data-ttu-id="447b2-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="447b2-115">PARAMETERS</span></span>

### <span data-ttu-id="447b2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="447b2-116">-DefaultProfile</span></span>
<span data-ttu-id="447b2-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="447b2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="447b2-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="447b2-118">-Name</span></span>
<span data-ttu-id="447b2-119">Nome dell'account degli ancoraggi spaziali.</span><span class="sxs-lookup"><span data-stu-id="447b2-119">Spatial Anchors Account Name.</span></span>

```yaml
Type: String
Parameter Sets: GetParameterSet
Aliases: SpatialAnchorsAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="447b2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="447b2-120">-ResourceGroupName</span></span>
<span data-ttu-id="447b2-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="447b2-121">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ListParameterSet
Aliases: ResourceGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="447b2-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="447b2-122">-ResourceId</span></span>
<span data-ttu-id="447b2-123">ID risorsa dell'account degli ancoraggi spaziali.</span><span class="sxs-lookup"><span data-stu-id="447b2-123">Resource ID of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="447b2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="447b2-124">CommonParameters</span></span>
<span data-ttu-id="447b2-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="447b2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="447b2-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="447b2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="447b2-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="447b2-127">INPUTS</span></span>

### <span data-ttu-id="447b2-128">System. String</span><span class="sxs-lookup"><span data-stu-id="447b2-128">System.String</span></span>

## <span data-ttu-id="447b2-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="447b2-129">OUTPUTS</span></span>

### <span data-ttu-id="447b2-130">Microsoft. Azure. Commands. MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="447b2-130">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="447b2-131">Note</span><span class="sxs-lookup"><span data-stu-id="447b2-131">NOTES</span></span>

## <span data-ttu-id="447b2-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="447b2-132">RELATED LINKS</span></span>
