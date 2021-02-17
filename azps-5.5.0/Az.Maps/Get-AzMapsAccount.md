---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/get-azmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccount.md
ms.openlocfilehash: edd98f284aa5bba6bba39c149d20a713b388bf4d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192254"
---
# <span data-ttu-id="e1d96-101">Get-AzMapsAccount</span><span class="sxs-lookup"><span data-stu-id="e1d96-101">Get-AzMapsAccount</span></span>

## <span data-ttu-id="e1d96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1d96-102">SYNOPSIS</span></span>
<span data-ttu-id="e1d96-103">Ottiene l'account.</span><span class="sxs-lookup"><span data-stu-id="e1d96-103">Gets the account.</span></span>

## <span data-ttu-id="e1d96-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e1d96-104">SYNTAX</span></span>

### <span data-ttu-id="e1d96-105">ResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e1d96-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzMapsAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e1d96-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1d96-106">AccountNameParameterSet</span></span>
```
Get-AzMapsAccount [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e1d96-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1d96-107">ResourceIdParameterSet</span></span>
```
Get-AzMapsAccount [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1d96-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e1d96-108">DESCRIPTION</span></span>
<span data-ttu-id="e1d96-109">Il cmdlet Get-AzMapsAccount esegue il provisioning di un account di Azure Maps, in base al nome e al gruppo di risorse o in base all'ID risorsa. Inoltre, può restituire un elenco di tutti gli account nel ResourceGroup o di tutti gli account di Azure Maps per la sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="e1d96-109">The Get-AzMapsAccount cmdlet gets a provisioned Azure Maps account, either by resource group and name, or by resource id. Additionally, it can return a list of all accounts in the ResourceGroup, or all Azure Maps accounts for the current subscription.</span></span>

## <span data-ttu-id="e1d96-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e1d96-110">EXAMPLES</span></span>

### <span data-ttu-id="e1d96-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e1d96-111">Example 1</span></span>
```powershell
PS C:\> Get-AzMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="e1d96-112">Ottiene l'account denominato MyAccount nel gruppo di risorse MyResourceGroup, se presente.</span><span class="sxs-lookup"><span data-stu-id="e1d96-112">Gets the account named MyAccount in the resource group MyResourceGroup, if it exists.</span></span>

### <span data-ttu-id="e1d96-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="e1d96-113">Example 2</span></span>
```powershell
PS C:\> Get-AzMapsAccount -ResourceGroupName MyResourceGroup

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
[...]
```

<span data-ttu-id="e1d96-114">Ottiene tutti gli account di Azure Maps nel gruppo di risorse MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="e1d96-114">Gets all Azure Maps accounts in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="e1d96-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="e1d96-115">Example 3</span></span>
```powershell
PS C:\> Get-AzMapsAccount

ResourceGroupName   AccountName            Id
-----------------   -----------            --
[...]
MyResourceGroup     MyAccount              /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
[...]
```

<span data-ttu-id="e1d96-116">Recupera tutti gli account di Mappe di Azure nella sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="e1d96-116">Gets all Azure Maps accounts in the current subscription.</span></span>

### <span data-ttu-id="e1d96-117">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="e1d96-117">Example 4</span></span>
```powershell
PS C:\> Get-AzMapsAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="e1d96-118">Ottiene l'account di Mappe specificato dall'ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="e1d96-118">Gets the Maps account specified by the Resource Id.</span></span>

## <span data-ttu-id="e1d96-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1d96-119">PARAMETERS</span></span>

### <span data-ttu-id="e1d96-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1d96-120">-DefaultProfile</span></span>
<span data-ttu-id="e1d96-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e1d96-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1d96-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e1d96-122">-Name</span></span>
<span data-ttu-id="e1d96-123">Nome account mappe.</span><span class="sxs-lookup"><span data-stu-id="e1d96-123">Maps Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases: MapsAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1d96-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1d96-124">-ResourceGroupName</span></span>
<span data-ttu-id="e1d96-125">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e1d96-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1d96-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e1d96-126">-ResourceId</span></span>
<span data-ttu-id="e1d96-127">Mappe Id ResourceId account.</span><span class="sxs-lookup"><span data-stu-id="e1d96-127">Maps Account ResourceId.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1d96-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1d96-128">CommonParameters</span></span>
<span data-ttu-id="e1d96-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1d96-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1d96-130">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1d96-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1d96-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="e1d96-131">INPUTS</span></span>

### <span data-ttu-id="e1d96-132">System.String</span><span class="sxs-lookup"><span data-stu-id="e1d96-132">System.String</span></span>

## <span data-ttu-id="e1d96-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e1d96-133">OUTPUTS</span></span>

### <span data-ttu-id="e1d96-134">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="e1d96-134">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="e1d96-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="e1d96-135">NOTES</span></span>

## <span data-ttu-id="e1d96-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e1d96-136">RELATED LINKS</span></span>
