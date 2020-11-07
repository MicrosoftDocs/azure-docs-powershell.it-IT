---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 3D2E9FAE-FE34-457A-BE95-BC61D025B07A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactory.md
ms.openlocfilehash: 74e72488d8a7a98b9f81b85599ed7e0867ed2ba6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687334"
---
# <span data-ttu-id="a9cbb-101">Remove-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="a9cbb-101">Remove-AzureRmDataFactory</span></span>

## <span data-ttu-id="a9cbb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a9cbb-102">SYNOPSIS</span></span>
<span data-ttu-id="a9cbb-103">Rimuove una data factory.</span><span class="sxs-lookup"><span data-stu-id="a9cbb-103">Removes a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9cbb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a9cbb-104">SYNTAX</span></span>

### <span data-ttu-id="a9cbb-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a9cbb-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactory [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9cbb-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="a9cbb-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactory [-DataFactory] <PSDataFactory> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9cbb-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a9cbb-107">DESCRIPTION</span></span>
<span data-ttu-id="a9cbb-108">Il cmdlet **Remove-AzureRmDataFactory** rimuove una data factory.</span><span class="sxs-lookup"><span data-stu-id="a9cbb-108">The **Remove-AzureRmDataFactory** cmdlet removes a data factory.</span></span>

## <span data-ttu-id="a9cbb-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a9cbb-109">EXAMPLES</span></span>

### <span data-ttu-id="a9cbb-110">Esempio 1: rimuovere una data factory</span><span class="sxs-lookup"><span data-stu-id="a9cbb-110">Example 1: Remove a data factory</span></span>
```
PS C:\>Remove-AzureRmDataFactory -Name "WikiADF" -ResourceGroupName "ADF"
Confirm
Are you sure you want to remove data factory 'WikiADF' in resource group 'ADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="a9cbb-111">Questo comando rimuove la factory di dati denominata WikiADF dal gruppo di risorse denominato ADF.</span><span class="sxs-lookup"><span data-stu-id="a9cbb-111">This command removes the data factory named WikiADF from the resource group named ADF.</span></span>
<span data-ttu-id="a9cbb-112">Questo comando restituisce un valore di $True.</span><span class="sxs-lookup"><span data-stu-id="a9cbb-112">This command returns a value of $True.</span></span>

## <span data-ttu-id="a9cbb-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a9cbb-113">PARAMETERS</span></span>

### <span data-ttu-id="a9cbb-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="a9cbb-114">-DataFactory</span></span>
<span data-ttu-id="a9cbb-115">Specifica l'oggetto **PSDataFactory** da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="a9cbb-115">Specifies the **PSDataFactory** object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9cbb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9cbb-116">-DefaultProfile</span></span>
<span data-ttu-id="a9cbb-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a9cbb-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a9cbb-118">-Force</span><span class="sxs-lookup"><span data-stu-id="a9cbb-118">-Force</span></span>
<span data-ttu-id="a9cbb-119">Indica che questo cmdlet rimuove una data factory senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="a9cbb-119">Indicates that this cmdlet removes a data factory without prompting you for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9cbb-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="a9cbb-120">-Name</span></span>
<span data-ttu-id="a9cbb-121">Specifica il nome della factory di dati da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="a9cbb-121">Specifies the name of the data factory to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9cbb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9cbb-122">-ResourceGroupName</span></span>
<span data-ttu-id="a9cbb-123">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="a9cbb-123">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="a9cbb-124">Questo cmdlet consente di rimuovere una data factory dal gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="a9cbb-124">This cmdlet removes a data factory from the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9cbb-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a9cbb-125">-Confirm</span></span>
<span data-ttu-id="a9cbb-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9cbb-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9cbb-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9cbb-127">-WhatIf</span></span>
<span data-ttu-id="a9cbb-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a9cbb-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9cbb-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a9cbb-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9cbb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9cbb-130">CommonParameters</span></span>
<span data-ttu-id="a9cbb-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9cbb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9cbb-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9cbb-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9cbb-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a9cbb-133">INPUTS</span></span>

### <span data-ttu-id="a9cbb-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a9cbb-134">System.String</span></span>

### <span data-ttu-id="a9cbb-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="a9cbb-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="a9cbb-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a9cbb-136">OUTPUTS</span></span>

### <span data-ttu-id="a9cbb-137">System. void</span><span class="sxs-lookup"><span data-stu-id="a9cbb-137">System.Void</span></span>

## <span data-ttu-id="a9cbb-138">Note</span><span class="sxs-lookup"><span data-stu-id="a9cbb-138">NOTES</span></span>
* <span data-ttu-id="a9cbb-139">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="a9cbb-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="a9cbb-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a9cbb-140">RELATED LINKS</span></span>

[<span data-ttu-id="a9cbb-141">Get-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="a9cbb-141">Get-AzureRmDataFactory</span></span>](./Get-AzureRmDataFactory.md)

[<span data-ttu-id="a9cbb-142">New-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="a9cbb-142">New-AzureRmDataFactory</span></span>](./New-AzureRmDataFactory.md)


