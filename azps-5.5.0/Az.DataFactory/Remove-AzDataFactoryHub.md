---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 4C839730-B494-45BD-B5A1-F93B02AB4B2A
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryHub.md
ms.openlocfilehash: 12a18c62d3cc3412726df323bd48acd86ed7b1fd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181007"
---
# <span data-ttu-id="2e456-101">Remove-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="2e456-101">Remove-AzDataFactoryHub</span></span>

## <span data-ttu-id="2e456-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e456-102">SYNOPSIS</span></span>
<span data-ttu-id="2e456-103">Rimuove un hub da Data factory di Azure.</span><span class="sxs-lookup"><span data-stu-id="2e456-103">Removes a hub from Azure Data Factory.</span></span>

## <span data-ttu-id="2e456-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2e456-104">SYNTAX</span></span>

### <span data-ttu-id="2e456-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="2e456-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryHub [-Name] <String> [-Force] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e456-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="2e456-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryHub [-Name] <String> [-Force] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e456-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2e456-107">DESCRIPTION</span></span>
<span data-ttu-id="2e456-108">Il cmdlet **Remove-AzDataFactoryHub** rimuove un hub da Data factory di Azure nel gruppo di risorse azure specificato e nel data factory specificato.</span><span class="sxs-lookup"><span data-stu-id="2e456-108">The **Remove-AzDataFactoryHub** cmdlet removes a hub from Azure Data Factory in the specified Azure resource group and in the specified data factory.</span></span>
<span data-ttu-id="2e456-109">Se si rimuove un hub, vengono rimossi anche tutti i servizi e le pipeline collegati nell'hub.</span><span class="sxs-lookup"><span data-stu-id="2e456-109">If you remove a hub, all linked services and pipelines in the hub are also removed.</span></span>

## <span data-ttu-id="2e456-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2e456-110">EXAMPLES</span></span>

### <span data-ttu-id="2e456-111">Esempio 1: Rimuovere un hub</span><span class="sxs-lookup"><span data-stu-id="2e456-111">Example 1: Remove a hub</span></span>
```
PS C:\>Remove-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "ContosoDataHub"
```

<span data-ttu-id="2e456-112">Questo comando rimuove l'hub denominato ContosoDataHub dal gruppo di risorse azure denominato ADFResourceGroup e dal data factory denominato ADFDataWith.</span><span class="sxs-lookup"><span data-stu-id="2e456-112">This command removes the hub named ContosoDataHub from the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="2e456-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2e456-113">PARAMETERS</span></span>

### <span data-ttu-id="2e456-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="2e456-114">-DataFactory</span></span>
<span data-ttu-id="2e456-115">Specifica un **oggetto PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="2e456-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="2e456-116">Questo cmdlet rimuove un hub dal data factory specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="2e456-116">This cmdlet removes a hub from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="2e456-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="2e456-117">-DataFactoryName</span></span>
<span data-ttu-id="2e456-118">Specifica il nome di un data factory.</span><span class="sxs-lookup"><span data-stu-id="2e456-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="2e456-119">Questo cmdlet rimuove un hub dal data factory specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="2e456-119">This cmdlet removes a hub from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="2e456-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e456-120">-DefaultProfile</span></span>
<span data-ttu-id="2e456-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="2e456-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2e456-122">-Force</span><span class="sxs-lookup"><span data-stu-id="2e456-122">-Force</span></span>
<span data-ttu-id="2e456-123">Indica che questo cmdlet rimuove un hub senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="2e456-123">Indicates that this cmdlet removes a hub without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="2e456-124">-Name</span><span class="sxs-lookup"><span data-stu-id="2e456-124">-Name</span></span>
<span data-ttu-id="2e456-125">Specifica il nome dell'hub da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="2e456-125">Specifies the name of the hub to remove.</span></span>

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

### <span data-ttu-id="2e456-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e456-126">-ResourceGroupName</span></span>
<span data-ttu-id="2e456-127">Specifica il nome di un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="2e456-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="2e456-128">Questo cmdlet rimuove un hub dal gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="2e456-128">This cmdlet removes a hub from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="2e456-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2e456-129">-Confirm</span></span>
<span data-ttu-id="2e456-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e456-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e456-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e456-131">-WhatIf</span></span>
<span data-ttu-id="2e456-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2e456-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e456-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2e456-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e456-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e456-134">CommonParameters</span></span>
<span data-ttu-id="2e456-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e456-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e456-136">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e456-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e456-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="2e456-137">INPUTS</span></span>

### <span data-ttu-id="2e456-138">System.String</span><span class="sxs-lookup"><span data-stu-id="2e456-138">System.String</span></span>

### <span data-ttu-id="2e456-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="2e456-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="2e456-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2e456-140">OUTPUTS</span></span>

### <span data-ttu-id="2e456-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2e456-141">System.Boolean</span></span>

## <span data-ttu-id="2e456-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="2e456-142">NOTES</span></span>
* <span data-ttu-id="2e456-143">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, dati, fattori</span><span class="sxs-lookup"><span data-stu-id="2e456-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="2e456-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2e456-144">RELATED LINKS</span></span>

[<span data-ttu-id="2e456-145">Get-AzDataHubHub</span><span class="sxs-lookup"><span data-stu-id="2e456-145">Get-AzDataFactoryHub</span></span>](./Get-AzDataFactoryHub.md)

[<span data-ttu-id="2e456-146">New-AzDataHubHub</span><span class="sxs-lookup"><span data-stu-id="2e456-146">New-AzDataFactoryHub</span></span>](./New-AzDataFactoryHub.md)


