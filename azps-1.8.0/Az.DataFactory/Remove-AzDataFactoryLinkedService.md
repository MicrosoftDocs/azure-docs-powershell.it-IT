---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 9425D38D-5978-421F-A438-4463068C4628
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryLinkedService.md
ms.openlocfilehash: a0e8a131b0a66c3887ecea7054a2f13b75e7f598
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836483"
---
# <span data-ttu-id="82955-101">Remove-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="82955-101">Remove-AzDataFactoryLinkedService</span></span>

## <span data-ttu-id="82955-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="82955-102">SYNOPSIS</span></span>
<span data-ttu-id="82955-103">Rimuove un servizio collegato da Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="82955-103">Removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="82955-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="82955-104">SYNTAX</span></span>

### <span data-ttu-id="82955-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="82955-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryLinkedService [-Force] [-DataFactoryName] <String> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="82955-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="82955-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryLinkedService [-Force] [-DataFactory] <PSDataFactory> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82955-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="82955-107">DESCRIPTION</span></span>
<span data-ttu-id="82955-108">Il cmdlet **Remove-AzDataFactoryLinkedService** rimuove un servizio collegato da Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="82955-108">The **Remove-AzDataFactoryLinkedService** cmdlet removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="82955-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="82955-109">EXAMPLES</span></span>

### <span data-ttu-id="82955-110">Esempio 1: rimuovere un servizio collegato</span><span class="sxs-lookup"><span data-stu-id="82955-110">Example 1: Remove a linked service</span></span>
```
PS C:\>Remove-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceTest"
Confirm
Are you sure you want to remove linked service 'LinkedServiceTest' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="82955-111">Questo comando rimuove il servizio collegato denominato LinkedServiceTest dalla data factory denominata WikiADF.</span><span class="sxs-lookup"><span data-stu-id="82955-111">This command removes the linked service named LinkedServiceTest from the data factory named WikiADF.</span></span>
<span data-ttu-id="82955-112">Questo comando restituisce un valore di $True.</span><span class="sxs-lookup"><span data-stu-id="82955-112">This command returns a value of $True.</span></span>

## <span data-ttu-id="82955-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="82955-113">PARAMETERS</span></span>

### <span data-ttu-id="82955-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="82955-114">-DataFactory</span></span>
<span data-ttu-id="82955-115">Specifica un oggetto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="82955-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="82955-116">Questo cmdlet consente di rimuovere un servizio collegato dalla data factory specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="82955-116">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="82955-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="82955-117">-DataFactoryName</span></span>
<span data-ttu-id="82955-118">Specifica il nome di una data factory.</span><span class="sxs-lookup"><span data-stu-id="82955-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="82955-119">Questo cmdlet consente di rimuovere un servizio collegato dalla data factory specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="82955-119">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82955-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82955-120">-DefaultProfile</span></span>
<span data-ttu-id="82955-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="82955-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="82955-122">-Force</span><span class="sxs-lookup"><span data-stu-id="82955-122">-Force</span></span>
<span data-ttu-id="82955-123">Indica che questo cmdlet rimuove un servizio collegato senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="82955-123">Indicates that this cmdlet removes a linked service without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="82955-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="82955-124">-Name</span></span>
<span data-ttu-id="82955-125">Specifica il nome del servizio collegato da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="82955-125">Specifies the name of the linked service to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82955-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82955-126">-ResourceGroupName</span></span>
<span data-ttu-id="82955-127">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="82955-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="82955-128">Questo cmdlet consente di rimuovere un servizio collegato dal gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="82955-128">This cmdlet removes a linked service from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="82955-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="82955-129">-Confirm</span></span>
<span data-ttu-id="82955-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82955-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82955-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82955-131">-WhatIf</span></span>
<span data-ttu-id="82955-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="82955-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82955-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="82955-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82955-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82955-134">CommonParameters</span></span>
<span data-ttu-id="82955-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82955-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82955-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82955-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82955-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="82955-137">INPUTS</span></span>

### <span data-ttu-id="82955-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="82955-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="82955-139">System. String</span><span class="sxs-lookup"><span data-stu-id="82955-139">System.String</span></span>

## <span data-ttu-id="82955-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="82955-140">OUTPUTS</span></span>

### <span data-ttu-id="82955-141">System. void</span><span class="sxs-lookup"><span data-stu-id="82955-141">System.Void</span></span>

## <span data-ttu-id="82955-142">Note</span><span class="sxs-lookup"><span data-stu-id="82955-142">NOTES</span></span>
* <span data-ttu-id="82955-143">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="82955-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="82955-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="82955-144">RELATED LINKS</span></span>

[<span data-ttu-id="82955-145">Get-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="82955-145">Get-AzDataFactoryLinkedService</span></span>](./Get-AzDataFactoryLinkedService.md)

[<span data-ttu-id="82955-146">New-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="82955-146">New-AzDataFactoryLinkedService</span></span>](./New-AzDataFactoryLinkedService.md)


