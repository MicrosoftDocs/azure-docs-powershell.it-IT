---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 9425D38D-5978-421F-A438-4463068C4628
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryLinkedService.md
ms.openlocfilehash: d3ea4c3f221a3d05c9d43e780cde359ff36843f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686342"
---
# <span data-ttu-id="ee7d2-101">Remove-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="ee7d2-101">Remove-AzureRmDataFactoryLinkedService</span></span>

## <span data-ttu-id="ee7d2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ee7d2-102">SYNOPSIS</span></span>
<span data-ttu-id="ee7d2-103">Rimuove un servizio collegato da Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="ee7d2-103">Removes a linked service from Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee7d2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ee7d2-104">SYNTAX</span></span>

### <span data-ttu-id="ee7d2-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ee7d2-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryLinkedService [-Force] [-DataFactoryName] <String> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ee7d2-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="ee7d2-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryLinkedService [-Force] [-DataFactory] <PSDataFactory> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee7d2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee7d2-107">DESCRIPTION</span></span>
<span data-ttu-id="ee7d2-108">Il cmdlet **Remove-AzureRmDataFactoryLinkedService** rimuove un servizio collegato da Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="ee7d2-108">The **Remove-AzureRmDataFactoryLinkedService** cmdlet removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="ee7d2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ee7d2-109">EXAMPLES</span></span>

### <span data-ttu-id="ee7d2-110">Esempio 1: rimuovere un servizio collegato</span><span class="sxs-lookup"><span data-stu-id="ee7d2-110">Example 1: Remove a linked service</span></span>
```
PS C:\>Remove-AzureRmDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceTest"
Confirm
Are you sure you want to remove linked service 'LinkedServiceTest' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="ee7d2-111">Questo comando rimuove il servizio collegato denominato LinkedServiceTest dalla data factory denominata WikiADF.</span><span class="sxs-lookup"><span data-stu-id="ee7d2-111">This command removes the linked service named LinkedServiceTest from the data factory named WikiADF.</span></span>
<span data-ttu-id="ee7d2-112">Questo comando restituisce un valore di $True.</span><span class="sxs-lookup"><span data-stu-id="ee7d2-112">This command returns a value of $True.</span></span>

## <span data-ttu-id="ee7d2-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ee7d2-113">PARAMETERS</span></span>

### <span data-ttu-id="ee7d2-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="ee7d2-114">-DataFactory</span></span>
<span data-ttu-id="ee7d2-115">Specifica un oggetto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="ee7d2-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="ee7d2-116">Questo cmdlet consente di rimuovere un servizio collegato dalla data factory specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="ee7d2-116">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ee7d2-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="ee7d2-117">-DataFactoryName</span></span>
<span data-ttu-id="ee7d2-118">Specifica il nome di una data factory.</span><span class="sxs-lookup"><span data-stu-id="ee7d2-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="ee7d2-119">Questo cmdlet consente di rimuovere un servizio collegato dalla data factory specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="ee7d2-119">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ee7d2-120">-Force</span><span class="sxs-lookup"><span data-stu-id="ee7d2-120">-Force</span></span>
<span data-ttu-id="ee7d2-121">Indica che questo cmdlet rimuove un servizio collegato senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="ee7d2-121">Indicates that this cmdlet removes a linked service without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="ee7d2-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="ee7d2-122">-Name</span></span>
<span data-ttu-id="ee7d2-123">Specifica il nome del servizio collegato da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="ee7d2-123">Specifies the name of the linked service to remove.</span></span>

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

### <span data-ttu-id="ee7d2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee7d2-124">-ResourceGroupName</span></span>
<span data-ttu-id="ee7d2-125">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="ee7d2-125">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="ee7d2-126">Questo cmdlet consente di rimuovere un servizio collegato dal gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="ee7d2-126">This cmdlet removes a linked service from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ee7d2-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ee7d2-127">-Confirm</span></span>
<span data-ttu-id="ee7d2-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee7d2-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee7d2-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee7d2-129">-WhatIf</span></span>
<span data-ttu-id="ee7d2-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ee7d2-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee7d2-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ee7d2-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee7d2-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee7d2-132">-DefaultProfile</span></span>
<span data-ttu-id="ee7d2-133">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ee7d2-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee7d2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee7d2-134">CommonParameters</span></span>
<span data-ttu-id="ee7d2-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee7d2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee7d2-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee7d2-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee7d2-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ee7d2-137">INPUTS</span></span>

## <span data-ttu-id="ee7d2-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ee7d2-138">OUTPUTS</span></span>

### <span data-ttu-id="ee7d2-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ee7d2-139">System.Boolean</span></span>

## <span data-ttu-id="ee7d2-140">Note</span><span class="sxs-lookup"><span data-stu-id="ee7d2-140">NOTES</span></span>
* <span data-ttu-id="ee7d2-141">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="ee7d2-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="ee7d2-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ee7d2-142">RELATED LINKS</span></span>

[<span data-ttu-id="ee7d2-143">Get-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="ee7d2-143">Get-AzureRmDataFactoryLinkedService</span></span>](./Get-AzureRmDataFactoryLinkedService.md)

[<span data-ttu-id="ee7d2-144">New-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="ee7d2-144">New-AzureRmDataFactoryLinkedService</span></span>](./New-AzureRmDataFactoryLinkedService.md)


