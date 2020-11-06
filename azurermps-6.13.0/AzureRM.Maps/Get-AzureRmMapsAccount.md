---
external help file: Microsoft.Azure.Commands.Maps.dll-Help.xml
Module Name: AzureRM.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.maps/get-azurermmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/Get-AzureRmMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/Get-AzureRmMapsAccount.md
ms.openlocfilehash: 68ccff91f6e233862ba1ee5aa94a3a3d0d8422b9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520953"
---
# <span data-ttu-id="ab00d-101">Get-AzureRmMapsAccount</span><span class="sxs-lookup"><span data-stu-id="ab00d-101">Get-AzureRmMapsAccount</span></span>

## <span data-ttu-id="ab00d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ab00d-102">SYNOPSIS</span></span>
<span data-ttu-id="ab00d-103">Ottiene l'account.</span><span class="sxs-lookup"><span data-stu-id="ab00d-103">Gets the account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab00d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ab00d-104">SYNTAX</span></span>

### <span data-ttu-id="ab00d-105">ResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ab00d-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmMapsAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ab00d-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab00d-106">AccountNameParameterSet</span></span>
```
Get-AzureRmMapsAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab00d-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab00d-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmMapsAccount [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab00d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ab00d-108">DESCRIPTION</span></span>
<span data-ttu-id="ab00d-109">Il cmdlet Get-AzureRmMapsAccount ottiene un account di mappe di Azure di cui è stato eseguito il provisioning, in base al gruppo di risorse e al nome o all'ID risorsa. Inoltre, può restituire un elenco di tutti gli account di ResourceGroup oppure tutti gli account in Azure Maps per l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="ab00d-109">The Get-AzureRmMapsAccount cmdlet gets a provisioned Azure Maps account, either by resource group and name, or by resource id. Additionally, it can return a list of all accounts in the ResourceGroup, or all Azure Maps accounts for the current subscription.</span></span>

## <span data-ttu-id="ab00d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ab00d-110">EXAMPLES</span></span>

### <span data-ttu-id="ab00d-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ab00d-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="ab00d-112">Ottiene l'account denominato account nel gruppo di risorse MyResourceGroup, se esistente.</span><span class="sxs-lookup"><span data-stu-id="ab00d-112">Gets the account named MyAccount in the resource group MyResourceGroup, if it exists.</span></span>

### <span data-ttu-id="ab00d-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="ab00d-113">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmMapsAccount -ResourceGroupName MyResourceGroup

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
[...]
```

<span data-ttu-id="ab00d-114">Ottiene tutti gli account di mappe di Azure nel gruppo di risorse MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ab00d-114">Gets all Azure Maps accounts in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="ab00d-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="ab00d-115">Example 3</span></span>
```powershell
PS C:\> Get-AzureRmMapsAccount

ResourceGroupName   AccountName            Id
-----------------   -----------            --
[...]
MyResourceGroup     MyAccount              /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
[...]
```

<span data-ttu-id="ab00d-116">Ottiene tutti gli account di mappe Azure nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="ab00d-116">Gets all Azure Maps accounts in the current subscription.</span></span>

### <span data-ttu-id="ab00d-117">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="ab00d-117">Example 4</span></span>
```powershell
PS C:\> Get-AzureRmMapsAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="ab00d-118">Ottiene l'account Maps specificato dall'ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="ab00d-118">Gets the Maps account specified by the Resource Id.</span></span>

## <span data-ttu-id="ab00d-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ab00d-119">PARAMETERS</span></span>

### <span data-ttu-id="ab00d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab00d-120">-DefaultProfile</span></span>
<span data-ttu-id="ab00d-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ab00d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab00d-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="ab00d-122">-Name</span></span>
<span data-ttu-id="ab00d-123">Nome dell'account mappe.</span><span class="sxs-lookup"><span data-stu-id="ab00d-123">Maps Account Name.</span></span>

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

### <span data-ttu-id="ab00d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab00d-124">-ResourceGroupName</span></span>
<span data-ttu-id="ab00d-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ab00d-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="ab00d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ab00d-126">-ResourceId</span></span>
<span data-ttu-id="ab00d-127">Mappe dell'account ResourceId.</span><span class="sxs-lookup"><span data-stu-id="ab00d-127">Maps Account ResourceId.</span></span>

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

### <span data-ttu-id="ab00d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab00d-128">CommonParameters</span></span>
<span data-ttu-id="ab00d-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab00d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab00d-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab00d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab00d-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ab00d-131">INPUTS</span></span>

### <span data-ttu-id="ab00d-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ab00d-132">System.String</span></span>

## <span data-ttu-id="ab00d-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ab00d-133">OUTPUTS</span></span>

### <span data-ttu-id="ab00d-134">Microsoft. Azure. Commands. maps. Models. PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="ab00d-134">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="ab00d-135">Note</span><span class="sxs-lookup"><span data-stu-id="ab00d-135">NOTES</span></span>

## <span data-ttu-id="ab00d-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ab00d-136">RELATED LINKS</span></span>
