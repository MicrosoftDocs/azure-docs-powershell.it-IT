---
external help file: Microsoft.Azure.Commands.LocationBasedServices.dll-Help.xml
Module Name: AzureRM.LocationBasedServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.locationbasedservices/get-azurermlocationbasedservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/Get-AzureRmLocationBasedServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/Get-AzureRmLocationBasedServicesAccount.md
ms.openlocfilehash: 18f492147e897b8061795434c309cc63729bec5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512543"
---
# <span data-ttu-id="4c4a7-101">Get-AzureRmLocationBasedServicesAccount</span><span class="sxs-lookup"><span data-stu-id="4c4a7-101">Get-AzureRmLocationBasedServicesAccount</span></span>

## <span data-ttu-id="4c4a7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4c4a7-102">SYNOPSIS</span></span>
<span data-ttu-id="4c4a7-103">Ottiene l'account.</span><span class="sxs-lookup"><span data-stu-id="4c4a7-103">Gets the account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c4a7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4c4a7-104">SYNTAX</span></span>

### <span data-ttu-id="4c4a7-105">ResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4c4a7-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmLocationBasedServicesAccount [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c4a7-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c4a7-106">AccountNameParameterSet</span></span>
```
Get-AzureRmLocationBasedServicesAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c4a7-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c4a7-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmLocationBasedServicesAccount [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4c4a7-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4c4a7-108">DESCRIPTION</span></span>
<span data-ttu-id="4c4a7-109">Il cmdlet **Get-AzureRmLocationBasedServicesAccount** ottiene un account di servizi basato sulla posizione di cui è stato eseguito il provisioning, in base al gruppo di risorse e al nome o all'ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="4c4a7-109">The **Get-AzureRmLocationBasedServicesAccount** cmdlet gets a provisioned Location Based Services account, either by resource group and name, or by resource id.</span></span>

<span data-ttu-id="4c4a7-110">Può inoltre restituire un elenco di tutti gli account di ResourceGroup oppure tutti gli account dei servizi basati sulla posizione per l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="4c4a7-110">Additionally, it can return a list of all accounts in the ResourceGroup, or all Location Based Services accounts for the current subscription.</span></span>

## <span data-ttu-id="4c4a7-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4c4a7-111">EXAMPLES</span></span>

### <span data-ttu-id="4c4a7-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4c4a7-112">Example 1</span></span>
```
PS C:\> Get-AzureRmLocationBasedServicesAccount -ResourceGroupName MyResourceGroup -Name MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount
```

<span data-ttu-id="4c4a7-113">Ottiene l'account denominato account nel gruppo di risorse MyResourceGroup, se esistente.</span><span class="sxs-lookup"><span data-stu-id="4c4a7-113">Gets the account named MyAccount in the resource group MyResourceGroup, if it exists.</span></span>

### <span data-ttu-id="4c4a7-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="4c4a7-114">Example 2</span></span>
```
PS C:\> Get-AzureRmLocationBasedServicesAccount -ResourceGroupName MyResourceGroup

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount
[...]
```

<span data-ttu-id="4c4a7-115">Ottiene tutti gli account dei servizi basati sulla posizione nel gruppo di risorse MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="4c4a7-115">Gets all Location Based Services accounts in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="4c4a7-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="4c4a7-116">Example 3</span></span>
```
PS C:\> Get-AzureRmLocationBasedServicesAccount

ResourceGroupName   AccountName            Id
-----------------   -----------            --
[...]
MyResourceGroup     MyAccount              /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount
[...]
```

<span data-ttu-id="4c4a7-117">Ottiene tutti gli account dei servizi basati sulla posizione nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="4c4a7-117">Gets all Location Based Services accounts in the current subscription.</span></span>

### <span data-ttu-id="4c4a7-118">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="4c4a7-118">Example 4</span></span>
```
PS C:\> Get-AzureRmLocationBasedServicesAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount
```

<span data-ttu-id="4c4a7-119">Ottiene l'account dei servizi basati sulla posizione specificato dall'ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="4c4a7-119">Gets the Location Based Services account specified by the Resource Id.</span></span>

## <span data-ttu-id="4c4a7-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4c4a7-120">PARAMETERS</span></span>

### <span data-ttu-id="4c4a7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c4a7-121">-DefaultProfile</span></span>
<span data-ttu-id="4c4a7-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4c4a7-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c4a7-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="4c4a7-123">-Name</span></span>
<span data-ttu-id="4c4a7-124">Nome account servizi basati sulla posizione.</span><span class="sxs-lookup"><span data-stu-id="4c4a7-124">Location Based Services Account Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountNameParameterSet
Aliases: LocationBasedServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c4a7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c4a7-125">-ResourceGroupName</span></span>
<span data-ttu-id="4c4a7-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4c4a7-126">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c4a7-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4c4a7-127">-ResourceId</span></span>
<span data-ttu-id="4c4a7-128">ResourceId account dei servizi basati sulla posizione.</span><span class="sxs-lookup"><span data-stu-id="4c4a7-128">Location Based Services Account ResourceId.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c4a7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c4a7-129">CommonParameters</span></span>
<span data-ttu-id="4c4a7-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c4a7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c4a7-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c4a7-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c4a7-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4c4a7-132">INPUTS</span></span>

### <span data-ttu-id="4c4a7-133">System. String</span><span class="sxs-lookup"><span data-stu-id="4c4a7-133">System.String</span></span>

## <span data-ttu-id="4c4a7-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4c4a7-134">OUTPUTS</span></span>

### <span data-ttu-id="4c4a7-135">Microsoft. Azure. Commands. LocationBasedServices. Models. PSLocationBasedServicesAccount</span><span class="sxs-lookup"><span data-stu-id="4c4a7-135">Microsoft.Azure.Commands.LocationBasedServices.Models.PSLocationBasedServicesAccount</span></span>
<span data-ttu-id="4c4a7-136">Questo cmdlet restituisce un oggetto **PSLocationBasedServicesAccount** .</span><span class="sxs-lookup"><span data-stu-id="4c4a7-136">This cmdlet returns a **PSLocationBasedServicesAccount** object.</span></span>
<span data-ttu-id="4c4a7-137">Puoi modificare questo oggetto e quindi applicare le modifiche usando **set-AzureRmLocationBasedServices**.</span><span class="sxs-lookup"><span data-stu-id="4c4a7-137">You can modify this object, and then apply changes by using **Set-AzureRmLocationBasedServices**.</span></span>

## <span data-ttu-id="4c4a7-138">Note</span><span class="sxs-lookup"><span data-stu-id="4c4a7-138">NOTES</span></span>

## <span data-ttu-id="4c4a7-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4c4a7-139">RELATED LINKS</span></span>
