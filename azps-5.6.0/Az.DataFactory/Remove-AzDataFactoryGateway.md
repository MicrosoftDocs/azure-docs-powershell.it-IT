---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: E1461540-DEAE-43C3-83DF-7DF3FE8D4EC0
online version: https://docs.microsoft.com/powershell/module/az.datafactory/remove-azdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryGateway.md
ms.openlocfilehash: eb9100bf4843d7213d2fbb89ac1827ba7ee1e509
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957390"
---
# <span data-ttu-id="9b2d9-101">Remove-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="9b2d9-101">Remove-AzDataFactoryGateway</span></span>

## <span data-ttu-id="9b2d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b2d9-102">SYNOPSIS</span></span>
<span data-ttu-id="9b2d9-103">Rimuove un gateway da Data factory di Azure.</span><span class="sxs-lookup"><span data-stu-id="9b2d9-103">Removes a gateway from Azure Data Factory.</span></span>

## <span data-ttu-id="9b2d9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9b2d9-104">SYNTAX</span></span>

### <span data-ttu-id="9b2d9-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="9b2d9-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b2d9-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="9b2d9-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b2d9-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9b2d9-107">DESCRIPTION</span></span>
<span data-ttu-id="9b2d9-108">Il cmdlet **Remove-AzDataFactoryGateway** rimuove il gateway specificato da Data factory di Azure.</span><span class="sxs-lookup"><span data-stu-id="9b2d9-108">The **Remove-AzDataFactoryGateway** cmdlet removes the specified gateway from Azure Data Factory.</span></span>

## <span data-ttu-id="9b2d9-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9b2d9-109">EXAMPLES</span></span>

### <span data-ttu-id="9b2d9-110">Esempio 1: Rimuovere un gateway</span><span class="sxs-lookup"><span data-stu-id="9b2d9-110">Example 1: Remove a gateway</span></span>
```
PS C:\>Remove-AzDataFactoryGateway -Name "ContosoGateway" -DataFactoryName "WikiADF" -ResourceGroupName "ADF"
Confirm
Are you sure you want to remove gateway 'ContosoGateway' in data factory 'WikiADF'? 
 [Y] Yes  [N] No  [S] Suspend  [?] Help (default is Y): Y
True
```

<span data-ttu-id="9b2d9-111">Questo comando rimuove il gateway denominato ContosoGateway dal data factory denominato WikiADF.</span><span class="sxs-lookup"><span data-stu-id="9b2d9-111">This command removes the gateway named ContosoGateway from the data factory named WikiADF.</span></span>

## <span data-ttu-id="9b2d9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9b2d9-112">PARAMETERS</span></span>

### <span data-ttu-id="9b2d9-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="9b2d9-113">-DataFactory</span></span>
<span data-ttu-id="9b2d9-114">Specifica un **oggetto PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="9b2d9-114">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="9b2d9-115">Questo cmdlet rimuove un gateway dal data factory specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="9b2d9-115">This cmdlet removes a gateway from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="9b2d9-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="9b2d9-116">-DataFactoryName</span></span>
<span data-ttu-id="9b2d9-117">Specifica il nome di un data factory.</span><span class="sxs-lookup"><span data-stu-id="9b2d9-117">Specifies the name of a data factory.</span></span>
<span data-ttu-id="9b2d9-118">Questo cmdlet rimuove un gateway dal data factory specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="9b2d9-118">This cmdlet removes a gateway from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="9b2d9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b2d9-119">-DefaultProfile</span></span>
<span data-ttu-id="9b2d9-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="9b2d9-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9b2d9-121">-Force</span><span class="sxs-lookup"><span data-stu-id="9b2d9-121">-Force</span></span>
<span data-ttu-id="9b2d9-122">Indica che questo cmdlet rimuove un gateway senza chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="9b2d9-122">Indicates that this cmdlet removes a gateway without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="9b2d9-123">-Name</span><span class="sxs-lookup"><span data-stu-id="9b2d9-123">-Name</span></span>
<span data-ttu-id="9b2d9-124">Specifica il nome del gateway da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="9b2d9-124">Specifies the name of the gateway to remove.</span></span>

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

### <span data-ttu-id="9b2d9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b2d9-125">-ResourceGroupName</span></span>
<span data-ttu-id="9b2d9-126">Specifica il nome di un gruppo di risorse azure.</span><span class="sxs-lookup"><span data-stu-id="9b2d9-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="9b2d9-127">Questo cmdlet rimuove un gateway che appartiene al gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="9b2d9-127">This cmdlet removes a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="9b2d9-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9b2d9-128">-Confirm</span></span>
<span data-ttu-id="9b2d9-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b2d9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b2d9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b2d9-130">-WhatIf</span></span>
<span data-ttu-id="9b2d9-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9b2d9-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b2d9-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9b2d9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b2d9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b2d9-133">CommonParameters</span></span>
<span data-ttu-id="9b2d9-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b2d9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b2d9-135">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b2d9-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b2d9-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="9b2d9-136">INPUTS</span></span>

### <span data-ttu-id="9b2d9-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="9b2d9-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="9b2d9-138">System.String</span><span class="sxs-lookup"><span data-stu-id="9b2d9-138">System.String</span></span>

## <span data-ttu-id="9b2d9-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9b2d9-139">OUTPUTS</span></span>

### <span data-ttu-id="9b2d9-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9b2d9-140">System.Boolean</span></span>

## <span data-ttu-id="9b2d9-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="9b2d9-141">NOTES</span></span>
* <span data-ttu-id="9b2d9-142">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, dati, fattori</span><span class="sxs-lookup"><span data-stu-id="9b2d9-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="9b2d9-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9b2d9-143">RELATED LINKS</span></span>

[<span data-ttu-id="9b2d9-144">Get-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="9b2d9-144">Get-AzDataFactoryGateway</span></span>](./Get-AzDataFactoryGateway.md)

[<span data-ttu-id="9b2d9-145">New-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="9b2d9-145">New-AzDataFactoryGateway</span></span>](./New-AzDataFactoryGateway.md)

[<span data-ttu-id="9b2d9-146">Set-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="9b2d9-146">Set-AzDataFactoryGateway</span></span>](./Set-AzDataFactoryGateway.md)


