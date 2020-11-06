---
external help file: Microsoft.Azure.Commands.LocationBasedServices.dll-Help.xml
Module Name: AzureRM.LocationBasedServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.locationbasedservices/get-azurermlocationbasedservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/Get-AzureRmLocationBasedServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/Get-AzureRmLocationBasedServicesAccountKey.md
ms.openlocfilehash: 1f528bb0a80f039b9a2be7cb4cb6e4c7fbc740c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521432"
---
# <span data-ttu-id="01785-101">Get-AzureRmLocationBasedServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="01785-101">Get-AzureRmLocationBasedServicesAccountKey</span></span>

## <span data-ttu-id="01785-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="01785-102">SYNOPSIS</span></span>
<span data-ttu-id="01785-103">Ottiene le chiavi dell'API per un account.</span><span class="sxs-lookup"><span data-stu-id="01785-103">Gets the API keys for an account.</span></span> <span data-ttu-id="01785-104">Queste chiavi sono il meccanismo di autenticazione usato nelle chiamate successive ai servizi basati sulla posizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="01785-104">These keys are the authentication mechanism used in subsequent calls to Azure Location Based Services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01785-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="01785-105">SYNTAX</span></span>

### <span data-ttu-id="01785-106">NameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="01785-106">NameParameterSet (Default)</span></span>
```
Get-AzureRmLocationBasedServicesAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01785-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="01785-107">InputObjectParameterSet</span></span>
```
Get-AzureRmLocationBasedServicesAccountKey [-InputObject <PSLocationBasedServicesAccount>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01785-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="01785-108">ResourceIdParameterSet</span></span>
```
Get-AzureRmLocationBasedServicesAccountKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="01785-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="01785-109">DESCRIPTION</span></span>
<span data-ttu-id="01785-110">Il cmdlet **Get-AzureRmLocationBasedServicesAccountKey** ottiene le chiavi dell'API per un account di servizi basato sulla posizione di cui è stato eseguito il provisioning.</span><span class="sxs-lookup"><span data-stu-id="01785-110">The **Get-AzureRmLocationBasedServicesAccountKey** cmdlet gets the API keys for a provisioned Location Based Services account.</span></span>

<span data-ttu-id="01785-111">Un account di servizi basati sulla posizione include due chiavi API: primaria e secondaria.</span><span class="sxs-lookup"><span data-stu-id="01785-111">A Location Based Services account has two API keys: Primary and Secondary.</span></span>
<span data-ttu-id="01785-112">Le chiavi consentono l'interazione con l'endpoint dell'account dei servizi basati sulla posizione.</span><span class="sxs-lookup"><span data-stu-id="01785-112">The keys enable interaction with the Location Based Services account endpoint.</span></span>

<span data-ttu-id="01785-113">USA [New-AzureRmLocationBasedServicesAccountKey](New-AzureRmLocationBasedServicesAccountKey.md) per rigenerare una chiave.</span><span class="sxs-lookup"><span data-stu-id="01785-113">Use [New-AzureRmLocationBasedServicesAccountKey](New-AzureRmLocationBasedServicesAccountKey.md) to regenerate a key.</span></span>

## <span data-ttu-id="01785-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="01785-114">EXAMPLES</span></span>

### <span data-ttu-id="01785-115">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="01785-115">Example 1</span></span>
```
PS C:\> Get-AzureRmLocationBasedServicesAccountKey -ResourceGroupName MyResourceGroup -Name MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="01785-116">Restituisce le chiavi per l'account denominato nome account nel gruppo di risorse MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="01785-116">Returns the keys for the account named MyAccount in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="01785-117">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="01785-117">Example 2</span></span>
```
PS C:\> Get-AzureRmLocationBasedServicesAccountKey -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="01785-118">Restituisce le chiavi per l'account dei servizi basati sulla posizione specificato.</span><span class="sxs-lookup"><span data-stu-id="01785-118">Returns the keys for the specified Location Based Services Account.</span></span>

## <span data-ttu-id="01785-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="01785-119">PARAMETERS</span></span>

### <span data-ttu-id="01785-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01785-120">-DefaultProfile</span></span>
<span data-ttu-id="01785-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="01785-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01785-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="01785-122">-InputObject</span></span>
<span data-ttu-id="01785-123">Account di servizi basati sulla posizione convogliato da [Get-AzureRmLocationBasedServicesAccount](Get-AzureRmLocationBasedServicesAccount.md).</span><span class="sxs-lookup"><span data-stu-id="01785-123">Location Based Services Account piped from [Get-AzureRmLocationBasedServicesAccount](Get-AzureRmLocationBasedServicesAccount.md).</span></span>

```yaml
Type: PSLocationBasedServicesAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="01785-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="01785-124">-Name</span></span>
<span data-ttu-id="01785-125">Nome account servizi basati sulla posizione.</span><span class="sxs-lookup"><span data-stu-id="01785-125">Location Based Services Account Name.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases: LocationBasedServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01785-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01785-126">-ResourceGroupName</span></span>
<span data-ttu-id="01785-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="01785-127">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01785-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="01785-128">-ResourceId</span></span>
<span data-ttu-id="01785-129">ResourceId account dei servizi basati sulla posizione.</span><span class="sxs-lookup"><span data-stu-id="01785-129">Location Based Services Account ResourceId.</span></span>
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

### <span data-ttu-id="01785-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01785-130">CommonParameters</span></span>
<span data-ttu-id="01785-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01785-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01785-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01785-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01785-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="01785-133">INPUTS</span></span>

### <span data-ttu-id="01785-134">System. String</span><span class="sxs-lookup"><span data-stu-id="01785-134">System.String</span></span>

## <span data-ttu-id="01785-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="01785-135">OUTPUTS</span></span>

### <span data-ttu-id="01785-136">Microsoft. Azure. Commands. LocationBasedServices. Models. PSLocationBasedServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="01785-136">Microsoft.Azure.Commands.LocationBasedServices.Models.PSLocationBasedServicesAccountKeys</span></span>

### <span data-ttu-id="01785-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01785-137">CommonParameters</span></span>
<span data-ttu-id="01785-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01785-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01785-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01785-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01785-140">Note</span><span class="sxs-lookup"><span data-stu-id="01785-140">NOTES</span></span>

## <span data-ttu-id="01785-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="01785-141">RELATED LINKS</span></span>
