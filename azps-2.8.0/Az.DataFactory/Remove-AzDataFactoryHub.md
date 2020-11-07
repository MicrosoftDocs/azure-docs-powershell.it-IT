---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 4C839730-B494-45BD-B5A1-F93B02AB4B2A
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryHub.md
ms.openlocfilehash: 0136927eea72911e706c3e0062dbc444cf1f9b25
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674964"
---
# <span data-ttu-id="fdc99-101">Remove-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="fdc99-101">Remove-AzDataFactoryHub</span></span>

## <span data-ttu-id="fdc99-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fdc99-102">SYNOPSIS</span></span>
<span data-ttu-id="fdc99-103">Rimuove un hub da Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="fdc99-103">Removes a hub from Azure Data Factory.</span></span>

## <span data-ttu-id="fdc99-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fdc99-104">SYNTAX</span></span>

### <span data-ttu-id="fdc99-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fdc99-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryHub [-Name] <String> [-Force] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdc99-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="fdc99-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryHub [-Name] <String> [-Force] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fdc99-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fdc99-107">DESCRIPTION</span></span>
<span data-ttu-id="fdc99-108">Il cmdlet **Remove-AzDataFactoryHub** rimuove un hub da Azure Data Factory nel gruppo di risorse Azure specificato e nella Factory di dati specificata.</span><span class="sxs-lookup"><span data-stu-id="fdc99-108">The **Remove-AzDataFactoryHub** cmdlet removes a hub from Azure Data Factory in the specified Azure resource group and in the specified data factory.</span></span>
<span data-ttu-id="fdc99-109">Se si rimuove un hub, vengono rimossi anche tutti i servizi collegati e le pipeline nell'hub.</span><span class="sxs-lookup"><span data-stu-id="fdc99-109">If you remove a hub, all linked services and pipelines in the hub are also removed.</span></span>

## <span data-ttu-id="fdc99-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fdc99-110">EXAMPLES</span></span>

### <span data-ttu-id="fdc99-111">Esempio 1: rimuovere un hub</span><span class="sxs-lookup"><span data-stu-id="fdc99-111">Example 1: Remove a hub</span></span>
```
PS C:\>Remove-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "ContosoDataHub"
```

<span data-ttu-id="fdc99-112">Questo comando rimuove l'Hub denominato ContosoDataHub dal gruppo di risorse di Azure denominato ADFResourceGroup e dalla data factory denominata ADFDataFactory.</span><span class="sxs-lookup"><span data-stu-id="fdc99-112">This command removes the hub named ContosoDataHub from the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="fdc99-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fdc99-113">PARAMETERS</span></span>

### <span data-ttu-id="fdc99-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="fdc99-114">-DataFactory</span></span>
<span data-ttu-id="fdc99-115">Specifica un oggetto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="fdc99-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="fdc99-116">Questo cmdlet consente di rimuovere un hub dalla data factory specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="fdc99-116">This cmdlet removes a hub from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="fdc99-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="fdc99-117">-DataFactoryName</span></span>
<span data-ttu-id="fdc99-118">Specifica il nome di una data factory.</span><span class="sxs-lookup"><span data-stu-id="fdc99-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="fdc99-119">Questo cmdlet consente di rimuovere un hub dalla data factory specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="fdc99-119">This cmdlet removes a hub from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="fdc99-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdc99-120">-DefaultProfile</span></span>
<span data-ttu-id="fdc99-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="fdc99-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fdc99-122">-Force</span><span class="sxs-lookup"><span data-stu-id="fdc99-122">-Force</span></span>
<span data-ttu-id="fdc99-123">Indica che questo cmdlet rimuove un hub senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="fdc99-123">Indicates that this cmdlet removes a hub without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="fdc99-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="fdc99-124">-Name</span></span>
<span data-ttu-id="fdc99-125">Specifica il nome dell'hub da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="fdc99-125">Specifies the name of the hub to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdc99-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdc99-126">-ResourceGroupName</span></span>
<span data-ttu-id="fdc99-127">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="fdc99-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="fdc99-128">Questo cmdlet consente di rimuovere un hub dal gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="fdc99-128">This cmdlet removes a hub from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="fdc99-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fdc99-129">-Confirm</span></span>
<span data-ttu-id="fdc99-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fdc99-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fdc99-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fdc99-131">-WhatIf</span></span>
<span data-ttu-id="fdc99-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fdc99-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fdc99-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fdc99-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fdc99-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdc99-134">CommonParameters</span></span>
<span data-ttu-id="fdc99-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdc99-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdc99-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdc99-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdc99-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fdc99-137">INPUTS</span></span>

### <span data-ttu-id="fdc99-138">System. String</span><span class="sxs-lookup"><span data-stu-id="fdc99-138">System.String</span></span>

### <span data-ttu-id="fdc99-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="fdc99-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="fdc99-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fdc99-140">OUTPUTS</span></span>

### <span data-ttu-id="fdc99-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fdc99-141">System.Boolean</span></span>

## <span data-ttu-id="fdc99-142">Note</span><span class="sxs-lookup"><span data-stu-id="fdc99-142">NOTES</span></span>
* <span data-ttu-id="fdc99-143">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="fdc99-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="fdc99-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fdc99-144">RELATED LINKS</span></span>

[<span data-ttu-id="fdc99-145">Get-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="fdc99-145">Get-AzDataFactoryHub</span></span>](./Get-AzDataFactoryHub.md)

[<span data-ttu-id="fdc99-146">New-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="fdc99-146">New-AzDataFactoryHub</span></span>](./New-AzDataFactoryHub.md)


