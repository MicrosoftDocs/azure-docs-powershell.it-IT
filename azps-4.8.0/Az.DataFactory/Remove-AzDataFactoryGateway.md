---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: E1461540-DEAE-43C3-83DF-7DF3FE8D4EC0
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryGateway.md
ms.openlocfilehash: 6831395c4f3d63dc056729b22573a16d863013e1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190275"
---
# <span data-ttu-id="948c8-101">Remove-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="948c8-101">Remove-AzDataFactoryGateway</span></span>

## <span data-ttu-id="948c8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="948c8-102">SYNOPSIS</span></span>
<span data-ttu-id="948c8-103">Rimuove un gateway da Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="948c8-103">Removes a gateway from Azure Data Factory.</span></span>

## <span data-ttu-id="948c8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="948c8-104">SYNTAX</span></span>

### <span data-ttu-id="948c8-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="948c8-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="948c8-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="948c8-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="948c8-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="948c8-107">DESCRIPTION</span></span>
<span data-ttu-id="948c8-108">Il cmdlet **Remove-AzDataFactoryGateway** rimuove il gateway specificato da Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="948c8-108">The **Remove-AzDataFactoryGateway** cmdlet removes the specified gateway from Azure Data Factory.</span></span>

## <span data-ttu-id="948c8-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="948c8-109">EXAMPLES</span></span>

### <span data-ttu-id="948c8-110">Esempio 1: rimuovere un gateway</span><span class="sxs-lookup"><span data-stu-id="948c8-110">Example 1: Remove a gateway</span></span>
```
PS C:\>Remove-AzDataFactoryGateway -Name "ContosoGateway" -DataFactoryName "WikiADF" -ResourceGroupName "ADF"
Confirm
Are you sure you want to remove gateway 'ContosoGateway' in data factory 'WikiADF'? 
 [Y] Yes  [N] No  [S] Suspend  [?] Help (default is Y): Y
True
```

<span data-ttu-id="948c8-111">Questo comando rimuove il gateway denominato ContosoGateway dalla data factory denominata WikiADF.</span><span class="sxs-lookup"><span data-stu-id="948c8-111">This command removes the gateway named ContosoGateway from the data factory named WikiADF.</span></span>

## <span data-ttu-id="948c8-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="948c8-112">PARAMETERS</span></span>

### <span data-ttu-id="948c8-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="948c8-113">-DataFactory</span></span>
<span data-ttu-id="948c8-114">Specifica un oggetto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="948c8-114">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="948c8-115">Questo cmdlet consente di rimuovere un gateway dalla data factory specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="948c8-115">This cmdlet removes a gateway from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="948c8-116">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="948c8-116">-DataFactoryName</span></span>
<span data-ttu-id="948c8-117">Specifica il nome di una data factory.</span><span class="sxs-lookup"><span data-stu-id="948c8-117">Specifies the name of a data factory.</span></span>
<span data-ttu-id="948c8-118">Questo cmdlet consente di rimuovere un gateway dalla data factory specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="948c8-118">This cmdlet removes a gateway from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="948c8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="948c8-119">-DefaultProfile</span></span>
<span data-ttu-id="948c8-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="948c8-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="948c8-121">-Force</span><span class="sxs-lookup"><span data-stu-id="948c8-121">-Force</span></span>
<span data-ttu-id="948c8-122">Indica che questo cmdlet rimuove un gateway senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="948c8-122">Indicates that this cmdlet removes a gateway without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="948c8-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="948c8-123">-Name</span></span>
<span data-ttu-id="948c8-124">Specifica il nome del gateway da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="948c8-124">Specifies the name of the gateway to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="948c8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="948c8-125">-ResourceGroupName</span></span>
<span data-ttu-id="948c8-126">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="948c8-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="948c8-127">Questo cmdlet consente di rimuovere un gateway che appartiene al gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="948c8-127">This cmdlet removes a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="948c8-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="948c8-128">-Confirm</span></span>
<span data-ttu-id="948c8-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="948c8-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="948c8-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="948c8-130">-WhatIf</span></span>
<span data-ttu-id="948c8-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="948c8-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="948c8-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="948c8-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="948c8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="948c8-133">CommonParameters</span></span>
<span data-ttu-id="948c8-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="948c8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="948c8-135">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="948c8-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="948c8-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="948c8-136">INPUTS</span></span>

### <span data-ttu-id="948c8-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="948c8-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="948c8-138">System. String</span><span class="sxs-lookup"><span data-stu-id="948c8-138">System.String</span></span>

## <span data-ttu-id="948c8-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="948c8-139">OUTPUTS</span></span>

### <span data-ttu-id="948c8-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="948c8-140">System.Boolean</span></span>

## <span data-ttu-id="948c8-141">Note</span><span class="sxs-lookup"><span data-stu-id="948c8-141">NOTES</span></span>
* <span data-ttu-id="948c8-142">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="948c8-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="948c8-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="948c8-143">RELATED LINKS</span></span>

[<span data-ttu-id="948c8-144">Get-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="948c8-144">Get-AzDataFactoryGateway</span></span>](./Get-AzDataFactoryGateway.md)

[<span data-ttu-id="948c8-145">New-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="948c8-145">New-AzDataFactoryGateway</span></span>](./New-AzDataFactoryGateway.md)

[<span data-ttu-id="948c8-146">Set-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="948c8-146">Set-AzDataFactoryGateway</span></span>](./Set-AzDataFactoryGateway.md)

