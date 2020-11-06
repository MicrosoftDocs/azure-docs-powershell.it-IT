---
external help file: Microsoft.Azure.Commands.LocationBasedServices.dll-Help.xml
Module Name: AzureRM.LocationBasedServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.locationbasedservices/new-azurermlocationbasedservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/New-AzureRmLocationBasedServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/New-AzureRmLocationBasedServicesAccountKey.md
ms.openlocfilehash: 7116cd4c5da2dd897af4e6540593a5e5458e4eda
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514275"
---
# <span data-ttu-id="e2225-101">New-AzureRmLocationBasedServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="e2225-101">New-AzureRmLocationBasedServicesAccountKey</span></span>

## <span data-ttu-id="e2225-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e2225-102">SYNOPSIS</span></span>
<span data-ttu-id="e2225-103">Rigenera una chiave dell'account.</span><span class="sxs-lookup"><span data-stu-id="e2225-103">Regenerates an account key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2225-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e2225-104">SYNTAX</span></span>

### <span data-ttu-id="e2225-105">NameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e2225-105">NameParameterSet (Default)</span></span>
```
New-AzureRmLocationBasedServicesAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2225-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2225-106">InputObjectParameterSet</span></span>
```
New-AzureRmLocationBasedServicesAccountKey [-KeyName] <String> [-InputObject <PSLocationBasedServicesAccount>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2225-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2225-107">ResourceIdParameterSet</span></span>
```
New-AzureRmLocationBasedServicesAccountKey [-KeyName] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2225-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e2225-108">DESCRIPTION</span></span>
<span data-ttu-id="e2225-109">Il cmdlet **New-AzureRmLocationBasedServicesAccountKey** rigenera una chiave API per un account di servizi basato sulla posizione.</span><span class="sxs-lookup"><span data-stu-id="e2225-109">The **New-AzureRmLocationBasedServicesAccountKey** cmdlet regenerates an API key for a Location Based Services account.</span></span>

## <span data-ttu-id="e2225-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e2225-110">EXAMPLES</span></span>

### <span data-ttu-id="e2225-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e2225-111">Example 1</span></span>
```
PS C:\> New-AzureRmLocationBasedServicesAccountKey -ResourceGroupName MyResourceGroup -Name MyAccount -KeyName Primary

Confirm
Are you sure you want to perform this action?
Performing the operation "Regenerating Key Primary for account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y

Id                                                                                                                                              PrimaryKey                                  SecondaryKey
--                                                                                                                                              ----------                                  ------------
/subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount ******************************************* *******************************************
```

<span data-ttu-id="e2225-112">Rigenera la chiave API primaria per il conto account nel gruppo di risorse MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="e2225-112">Regenerates the Primary API Key for the account MyAccount in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="e2225-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="e2225-113">Example 2</span></span>
```
PS C:\> New-AzureRmLocationBasedServicesAccountKey -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount -KeyName Secondary

Confirm
Are you sure you want to perform this action?
Performing the operation "Regenerating Key Secondary for account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y

Id                                                                                                                                              PrimaryKey                                  SecondaryKey
--                                                                                                                                              ----------                                  ------------
/subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount ******************************************* *******************************************
```

<span data-ttu-id="e2225-114">Rigenera la chiave API secondaria per l'account dei servizi basati sulla posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="e2225-114">Regenerates the Secondary API Key for the specified Location Based Services Account.</span></span>

## <span data-ttu-id="e2225-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e2225-115">PARAMETERS</span></span>

### <span data-ttu-id="e2225-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2225-116">-DefaultProfile</span></span>
<span data-ttu-id="e2225-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e2225-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2225-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2225-118">-InputObject</span></span>
<span data-ttu-id="e2225-119">Account di servizi basati sulla posizione convogliato da [Get-AzureRmLocationBasedServicesAccount](Get-AzureRmLocationBasedServicesAccount.md).</span><span class="sxs-lookup"><span data-stu-id="e2225-119">Location Based Services Account piped from [Get-AzureRmLocationBasedServicesAccount](Get-AzureRmLocationBasedServicesAccount.md).</span></span>

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

### <span data-ttu-id="e2225-120">-Nome di file</span><span class="sxs-lookup"><span data-stu-id="e2225-120">-KeyName</span></span>
<span data-ttu-id="e2225-121">Chiave dell'account servizi basati sulla posizione.</span><span class="sxs-lookup"><span data-stu-id="e2225-121">Location Based Services Account Key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2225-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="e2225-122">-Name</span></span>
<span data-ttu-id="e2225-123">Nome account servizi basati sulla posizione.</span><span class="sxs-lookup"><span data-stu-id="e2225-123">Location Based Services Account Name.</span></span>

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

### <span data-ttu-id="e2225-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2225-124">-ResourceGroupName</span></span>
<span data-ttu-id="e2225-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e2225-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="e2225-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e2225-126">-ResourceId</span></span>
<span data-ttu-id="e2225-127">ResourceId account dei servizi basati sulla posizione.</span><span class="sxs-lookup"><span data-stu-id="e2225-127">Location Based Services Account ResourceId.</span></span>
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

### <span data-ttu-id="e2225-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e2225-128">-Confirm</span></span>
<span data-ttu-id="e2225-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2225-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2225-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2225-130">-WhatIf</span></span>
<span data-ttu-id="e2225-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e2225-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2225-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e2225-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2225-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2225-133">CommonParameters</span></span>
<span data-ttu-id="e2225-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2225-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2225-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2225-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2225-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e2225-136">INPUTS</span></span>

### <span data-ttu-id="e2225-137">System. String</span><span class="sxs-lookup"><span data-stu-id="e2225-137">System.String</span></span>
<span data-ttu-id="e2225-138">Microsoft. Azure. Commands. LocationBasedServices. NewAzureLocationBasedServicesAccountKeyCommand + KeyNameType</span><span class="sxs-lookup"><span data-stu-id="e2225-138">Microsoft.Azure.Commands.LocationBasedServices.NewAzureLocationBasedServicesAccountKeyCommand+KeyNameType</span></span>

## <span data-ttu-id="e2225-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e2225-139">OUTPUTS</span></span>

### <span data-ttu-id="e2225-140">Microsoft. Azure. Management. LocationBasedServices. Models. LocationBasedServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="e2225-140">Microsoft.Azure.Management.LocationBasedServices.Models.LocationBasedServicesAccountKeys</span></span>

## <span data-ttu-id="e2225-141">Note</span><span class="sxs-lookup"><span data-stu-id="e2225-141">NOTES</span></span>

## <span data-ttu-id="e2225-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e2225-142">RELATED LINKS</span></span>
