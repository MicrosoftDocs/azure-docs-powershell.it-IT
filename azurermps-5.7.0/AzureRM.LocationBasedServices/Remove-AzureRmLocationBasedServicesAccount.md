---
external help file: Microsoft.Azure.Commands.LocationBasedServices.dll-Help.xml
Module Name: AzureRM.LocationBasedServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.locationbasedservices/remove-azurermlocationbasedservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/Remove-AzureRmLocationBasedServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/Remove-AzureRmLocationBasedServicesAccount.md
ms.openlocfilehash: 0496fcdba082370654b3259f101987d1a78621fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519448"
---
# <span data-ttu-id="9e979-101">Remove-AzureRmLocationBasedServicesAccount</span><span class="sxs-lookup"><span data-stu-id="9e979-101">Remove-AzureRmLocationBasedServicesAccount</span></span>

## <span data-ttu-id="9e979-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9e979-102">SYNOPSIS</span></span>
<span data-ttu-id="9e979-103">Elimina un account di servizi basato sulla posizione.</span><span class="sxs-lookup"><span data-stu-id="9e979-103">Deletes a Location Based Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e979-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9e979-104">SYNTAX</span></span>

### <span data-ttu-id="9e979-105">NameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9e979-105">NameParameterSet (Default)</span></span>
```
Remove-AzureRmLocationBasedServicesAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e979-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e979-106">InputObjectParameterSet</span></span>
```
Remove-AzureRmLocationBasedServicesAccount [-InputObject <PSLocationBasedServicesAccount>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e979-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e979-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmLocationBasedServicesAccount [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e979-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9e979-108">DESCRIPTION</span></span>
<span data-ttu-id="9e979-109">Il cmdlet **Remove-AzureRmLocationBasedServicesAccount** Elimina l'account dei servizi basati sulla posizione specificato.</span><span class="sxs-lookup"><span data-stu-id="9e979-109">The **Remove-AzureRmLocationBasedServicesAccount** cmdlet deletes the specified Location Based Services account.</span></span>

## <span data-ttu-id="9e979-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9e979-110">EXAMPLES</span></span>

### <span data-ttu-id="9e979-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9e979-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmLocationBasedServicesAccount -ResourceGroupName MyResourceGroup -Name MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="9e979-112">Consente di eliminare l'account dal gruppo di risorse MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="9e979-112">Deletes the account MyAccount from the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="9e979-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="9e979-113">Example 2</span></span>
```
PS C:\> Remove-AzureRmLocationBasedServicesAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="9e979-114">Elimina l'account dei servizi basati sulla posizione specificato.</span><span class="sxs-lookup"><span data-stu-id="9e979-114">Deletes the specified Location Based Services Account.</span></span>

## <span data-ttu-id="9e979-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9e979-115">PARAMETERS</span></span>

### <span data-ttu-id="9e979-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e979-116">-DefaultProfile</span></span>
<span data-ttu-id="9e979-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9e979-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e979-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9e979-118">-InputObject</span></span>
<span data-ttu-id="9e979-119">Account di servizi basati sulla posizione convogliato da [Get-AzureRmLocationBasedServicesAccount](Get-AzureRmLocationBasedServicesAccount.md).</span><span class="sxs-lookup"><span data-stu-id="9e979-119">Location Based Services Account piped from [Get-AzureRmLocationBasedServicesAccount](Get-AzureRmLocationBasedServicesAccount.md).</span></span>

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

### <span data-ttu-id="9e979-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="9e979-120">-Name</span></span>
<span data-ttu-id="9e979-121">Nome account servizi basati sulla posizione.</span><span class="sxs-lookup"><span data-stu-id="9e979-121">Location Based Services Account Name.</span></span>

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

### <span data-ttu-id="9e979-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e979-122">-ResourceGroupName</span></span>
<span data-ttu-id="9e979-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9e979-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="9e979-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9e979-124">-ResourceId</span></span>
<span data-ttu-id="9e979-125">ResourceId account dei servizi basati sulla posizione.</span><span class="sxs-lookup"><span data-stu-id="9e979-125">Location Based Services Account ResourceId.</span></span>
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

### <span data-ttu-id="9e979-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9e979-126">-Confirm</span></span>
<span data-ttu-id="9e979-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e979-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e979-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e979-128">-WhatIf</span></span>
<span data-ttu-id="9e979-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9e979-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e979-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9e979-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e979-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e979-131">CommonParameters</span></span>
<span data-ttu-id="9e979-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e979-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e979-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e979-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e979-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9e979-134">INPUTS</span></span>

### <span data-ttu-id="9e979-135">System. String</span><span class="sxs-lookup"><span data-stu-id="9e979-135">System.String</span></span>

## <span data-ttu-id="9e979-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9e979-136">OUTPUTS</span></span>

### <span data-ttu-id="9e979-137">System. Object</span><span class="sxs-lookup"><span data-stu-id="9e979-137">System.Object</span></span>

## <span data-ttu-id="9e979-138">Note</span><span class="sxs-lookup"><span data-stu-id="9e979-138">NOTES</span></span>

## <span data-ttu-id="9e979-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9e979-139">RELATED LINKS</span></span>
