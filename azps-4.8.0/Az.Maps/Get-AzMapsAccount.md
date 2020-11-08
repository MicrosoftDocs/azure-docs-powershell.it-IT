---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/get-azmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccount.md
ms.openlocfilehash: edd98f284aa5bba6bba39c149d20a713b388bf4d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032482"
---
# <span data-ttu-id="1a51e-101">Get-AzMapsAccount</span><span class="sxs-lookup"><span data-stu-id="1a51e-101">Get-AzMapsAccount</span></span>

## <span data-ttu-id="1a51e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1a51e-102">SYNOPSIS</span></span>
<span data-ttu-id="1a51e-103">Ottiene l'account.</span><span class="sxs-lookup"><span data-stu-id="1a51e-103">Gets the account.</span></span>

## <span data-ttu-id="1a51e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1a51e-104">SYNTAX</span></span>

### <span data-ttu-id="1a51e-105">ResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1a51e-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzMapsAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1a51e-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a51e-106">AccountNameParameterSet</span></span>
```
Get-AzMapsAccount [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1a51e-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a51e-107">ResourceIdParameterSet</span></span>
```
Get-AzMapsAccount [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a51e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1a51e-108">DESCRIPTION</span></span>
<span data-ttu-id="1a51e-109">Il cmdlet Get-AzMapsAccount ottiene un account di mappe di Azure di cui è stato eseguito il provisioning, in base al gruppo di risorse e al nome o all'ID risorsa. Inoltre, può restituire un elenco di tutti gli account di ResourceGroup oppure tutti gli account in Azure Maps per l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="1a51e-109">The Get-AzMapsAccount cmdlet gets a provisioned Azure Maps account, either by resource group and name, or by resource id. Additionally, it can return a list of all accounts in the ResourceGroup, or all Azure Maps accounts for the current subscription.</span></span>

## <span data-ttu-id="1a51e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1a51e-110">EXAMPLES</span></span>

### <span data-ttu-id="1a51e-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1a51e-111">Example 1</span></span>
```powershell
PS C:\> Get-AzMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="1a51e-112">Ottiene l'account denominato account nel gruppo di risorse MyResourceGroup, se esistente.</span><span class="sxs-lookup"><span data-stu-id="1a51e-112">Gets the account named MyAccount in the resource group MyResourceGroup, if it exists.</span></span>

### <span data-ttu-id="1a51e-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="1a51e-113">Example 2</span></span>
```powershell
PS C:\> Get-AzMapsAccount -ResourceGroupName MyResourceGroup

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
[...]
```

<span data-ttu-id="1a51e-114">Ottiene tutti gli account di mappe di Azure nel gruppo di risorse MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1a51e-114">Gets all Azure Maps accounts in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="1a51e-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="1a51e-115">Example 3</span></span>
```powershell
PS C:\> Get-AzMapsAccount

ResourceGroupName   AccountName            Id
-----------------   -----------            --
[...]
MyResourceGroup     MyAccount              /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
[...]
```

<span data-ttu-id="1a51e-116">Ottiene tutti gli account di mappe Azure nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="1a51e-116">Gets all Azure Maps accounts in the current subscription.</span></span>

### <span data-ttu-id="1a51e-117">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="1a51e-117">Example 4</span></span>
```powershell
PS C:\> Get-AzMapsAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="1a51e-118">Ottiene l'account Maps specificato dall'ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="1a51e-118">Gets the Maps account specified by the Resource Id.</span></span>

## <span data-ttu-id="1a51e-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1a51e-119">PARAMETERS</span></span>

### <span data-ttu-id="1a51e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a51e-120">-DefaultProfile</span></span>
<span data-ttu-id="1a51e-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1a51e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a51e-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="1a51e-122">-Name</span></span>
<span data-ttu-id="1a51e-123">Nome dell'account mappe.</span><span class="sxs-lookup"><span data-stu-id="1a51e-123">Maps Account Name.</span></span>

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

### <span data-ttu-id="1a51e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a51e-124">-ResourceGroupName</span></span>
<span data-ttu-id="1a51e-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1a51e-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="1a51e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1a51e-126">-ResourceId</span></span>
<span data-ttu-id="1a51e-127">Mappe dell'account ResourceId.</span><span class="sxs-lookup"><span data-stu-id="1a51e-127">Maps Account ResourceId.</span></span>

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

### <span data-ttu-id="1a51e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a51e-128">CommonParameters</span></span>
<span data-ttu-id="1a51e-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a51e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a51e-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a51e-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a51e-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1a51e-131">INPUTS</span></span>

### <span data-ttu-id="1a51e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="1a51e-132">System.String</span></span>

## <span data-ttu-id="1a51e-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1a51e-133">OUTPUTS</span></span>

### <span data-ttu-id="1a51e-134">Microsoft. Azure. Commands. maps. Models. PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="1a51e-134">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="1a51e-135">Note</span><span class="sxs-lookup"><span data-stu-id="1a51e-135">NOTES</span></span>

## <span data-ttu-id="1a51e-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1a51e-136">RELATED LINKS</span></span>
