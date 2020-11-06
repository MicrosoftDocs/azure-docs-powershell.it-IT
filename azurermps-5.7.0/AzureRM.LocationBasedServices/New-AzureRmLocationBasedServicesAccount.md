---
external help file: Microsoft.Azure.Commands.LocationBasedServices.dll-Help.xml
Module Name: AzureRM.LocationBasedServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.locationbasedservices/new-azurermlocationbasedservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/New-AzureRmLocationBasedServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/New-AzureRmLocationBasedServicesAccount.md
ms.openlocfilehash: 739ce121e26f1010c5c13ff3330dadffa02053af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511164"
---
# <span data-ttu-id="4e305-101">New-AzureRmLocationBasedServicesAccount</span><span class="sxs-lookup"><span data-stu-id="4e305-101">New-AzureRmLocationBasedServicesAccount</span></span>

## <span data-ttu-id="4e305-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4e305-102">SYNOPSIS</span></span>
<span data-ttu-id="4e305-103">Crea un account di servizi basato sulla posizione.</span><span class="sxs-lookup"><span data-stu-id="4e305-103">Creates a Location Based Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e305-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4e305-104">SYNTAX</span></span>

```
New-AzureRmLocationBasedServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String>
 [-Tag <Hashtable[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4e305-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4e305-105">DESCRIPTION</span></span>
<span data-ttu-id="4e305-106">Il cmdlet **New-AzureRmLocationBasedServicesAccount** crea un account di servizi basato sulla posizione con l'USK specificata.</span><span class="sxs-lookup"><span data-stu-id="4e305-106">The **New-AzureRmLocationBasedServicesAccount** cmdlet creates a Location Based Services account with the specified SKU.</span></span>

## <span data-ttu-id="4e305-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4e305-107">EXAMPLES</span></span>

### <span data-ttu-id="4e305-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4e305-108">Example 1</span></span>
```
PS C:\> New-AzureRmLocationBasedServicesAccount -ResourceGroupName MyResourceGroup -Name MyAccount -SkuName S0 -Tags @{Name="test";Value="true"}

Notice
By creating a Location Based Account, you are consenting to the terms of use (see https://azure.microsoft.com/en-us/support/legal/preview-supplemental-terms/).
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"): y

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount
```

<span data-ttu-id="4e305-109">Crea un nuovo account di servizi basati sulla posizione denominato account nel gruppo di risorse MyResourceGroup con il SKU S0 e un tag.</span><span class="sxs-lookup"><span data-stu-id="4e305-109">Creates a new Location Based Services account named MyAccount in the resource group MyResourceGroup with the SKU S0 and a tag.</span></span>

## <span data-ttu-id="4e305-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4e305-110">PARAMETERS</span></span>

### <span data-ttu-id="4e305-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e305-111">-DefaultProfile</span></span>
<span data-ttu-id="4e305-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4e305-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e305-113">-Force</span><span class="sxs-lookup"><span data-stu-id="4e305-113">-Force</span></span>
<span data-ttu-id="4e305-114">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="4e305-114">Don't ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e305-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="4e305-115">-Name</span></span>
<span data-ttu-id="4e305-116">Nome account servizi basati sulla posizione.</span><span class="sxs-lookup"><span data-stu-id="4e305-116">Location Based Services Account Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: LocationBasedServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e305-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e305-117">-ResourceGroupName</span></span>
<span data-ttu-id="4e305-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4e305-118">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e305-119">-SkuName</span><span class="sxs-lookup"><span data-stu-id="4e305-119">-SkuName</span></span>
<span data-ttu-id="4e305-120">Nome SKU dell'account dei servizi basati sulla posizione.</span><span class="sxs-lookup"><span data-stu-id="4e305-120">Location Based Services Account Sku Name.</span></span>

<span data-ttu-id="4e305-121">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="4e305-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4e305-122">S0</span><span class="sxs-lookup"><span data-stu-id="4e305-122">S0</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: S0

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e305-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="4e305-123">-Tag</span></span>
<span data-ttu-id="4e305-124">Tag di account dei servizi basati sulla posizione.</span><span class="sxs-lookup"><span data-stu-id="4e305-124">Location Based Services Account Tags.</span></span>

```yaml
Type: Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e305-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4e305-125">-Confirm</span></span>
<span data-ttu-id="4e305-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e305-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e305-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e305-127">-WhatIf</span></span>
<span data-ttu-id="4e305-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4e305-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e305-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4e305-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e305-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e305-130">CommonParameters</span></span>
<span data-ttu-id="4e305-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e305-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e305-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e305-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e305-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4e305-133">INPUTS</span></span>

### <span data-ttu-id="4e305-134">System. String</span><span class="sxs-lookup"><span data-stu-id="4e305-134">System.String</span></span>

## <span data-ttu-id="4e305-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4e305-135">OUTPUTS</span></span>

### <span data-ttu-id="4e305-136">Microsoft. Azure. Commands. LocationBasedServices. Models. PSLocationBasedServicesAccount</span><span class="sxs-lookup"><span data-stu-id="4e305-136">Microsoft.Azure.Commands.LocationBasedServices.Models.PSLocationBasedServicesAccount</span></span>

## <span data-ttu-id="4e305-137">Note</span><span class="sxs-lookup"><span data-stu-id="4e305-137">NOTES</span></span>

<span data-ttu-id="4e305-138">La creazione di un account di servizi basato sulla posizione richiede la risposta a una richiesta di accettazione di termini (vedere https://azure.microsoft.com/en-us/support/legal/preview-supplemental-terms/) .</span><span class="sxs-lookup"><span data-stu-id="4e305-138">Creating a Location Based Services account requires answering a prompt to accept terms (see https://azure.microsoft.com/en-us/support/legal/preview-supplemental-terms/).</span></span>  <span data-ttu-id="4e305-139">Il parametro-Force può essere usato per indicare l'accettazione dei termini.</span><span class="sxs-lookup"><span data-stu-id="4e305-139">The -Force parameter can be used to indicate acceptance of the terms.</span></span>

## <span data-ttu-id="4e305-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4e305-140">RELATED LINKS</span></span>
