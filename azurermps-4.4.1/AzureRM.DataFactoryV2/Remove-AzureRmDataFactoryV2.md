---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 73cc7df9dcb32dac592df56f16ad819219e06b7d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687532"
---
# <span data-ttu-id="9d184-101">Remove-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="9d184-101">Remove-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="9d184-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9d184-102">SYNOPSIS</span></span>
<span data-ttu-id="9d184-103">Rimuove una data factory.</span><span class="sxs-lookup"><span data-stu-id="9d184-103">Removes a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d184-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9d184-104">SYNTAX</span></span>

### <span data-ttu-id="9d184-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9d184-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="9d184-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="9d184-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryV2 [-InputObject] <PSDataFactory> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="9d184-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9d184-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2 [-ResourceId] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="9d184-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9d184-108">DESCRIPTION</span></span>
<span data-ttu-id="9d184-109">Il cmdlet Remove-AzureRmDataFactoryV2 rimuove una data factory.</span><span class="sxs-lookup"><span data-stu-id="9d184-109">The Remove-AzureRmDataFactoryV2 cmdlet removes a data factory.</span></span>

## <span data-ttu-id="9d184-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9d184-110">EXAMPLES</span></span>

### <span data-ttu-id="9d184-111">Esempio 1: rimuovere una data factory</span><span class="sxs-lookup"><span data-stu-id="9d184-111">Example 1: Remove a data factory</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2 -Name "WikiADF" -ResourceGroupName "ADF"
          Confirm
          Are you sure you want to remove data factory 'WikiADF' in resource group 'ADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="9d184-112">Questo comando rimuove la factory di dati denominata WikiADF dal gruppo di risorse denominato ADF.</span><span class="sxs-lookup"><span data-stu-id="9d184-112">This command removes the data factory named WikiADF from the resource group named ADF.</span></span>
<span data-ttu-id="9d184-113">Questo comando restituisce un valore di $True.</span><span class="sxs-lookup"><span data-stu-id="9d184-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="9d184-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9d184-114">PARAMETERS</span></span>

### <span data-ttu-id="9d184-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9d184-115">-Confirm</span></span>
<span data-ttu-id="9d184-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d184-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d184-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9d184-117">-InputObject</span></span>
<span data-ttu-id="9d184-118">Specifica l'oggetto DataFactory da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="9d184-118">Specifies the DataFactory object to remove.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d184-119">-Force</span><span class="sxs-lookup"><span data-stu-id="9d184-119">-Force</span></span>
<span data-ttu-id="9d184-120">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="9d184-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="9d184-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="9d184-121">-Name</span></span>
<span data-ttu-id="9d184-122">Specifica il nome della factory di dati da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="9d184-122">Specifies the name of the data factory to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d184-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d184-123">-ResourceGroupName</span></span>
<span data-ttu-id="9d184-124">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="9d184-124">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="9d184-125">Questo cmdlet consente di rimuovere una data factory dal gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="9d184-125">This cmdlet removes a data factory from the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d184-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9d184-126">-ResourceId</span></span>
<span data-ttu-id="9d184-127">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="9d184-127">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d184-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d184-128">-WhatIf</span></span>
<span data-ttu-id="9d184-129">Mostra cosa succede se il cmdlet viene eseguito, ma il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9d184-129">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="9d184-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9d184-130">INPUTS</span></span>

### <span data-ttu-id="9d184-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="9d184-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="9d184-132">System. String</span><span class="sxs-lookup"><span data-stu-id="9d184-132">System.String</span></span>


## <span data-ttu-id="9d184-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9d184-133">OUTPUTS</span></span>

### <span data-ttu-id="9d184-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="9d184-134">System.Object</span></span>

## <span data-ttu-id="9d184-135">Note</span><span class="sxs-lookup"><span data-stu-id="9d184-135">NOTES</span></span>
<span data-ttu-id="9d184-136">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="9d184-136">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="9d184-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9d184-137">RELATED LINKS</span></span>
[<span data-ttu-id="9d184-138">Get-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="9d184-138">Get-AzureRmDataFactoryV2</span></span>]()

[<span data-ttu-id="9d184-139">Set-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="9d184-139">Set-AzureRmDataFactoryV2</span></span>]()
