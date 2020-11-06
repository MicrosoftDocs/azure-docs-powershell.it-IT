---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: E1461540-DEAE-43C3-83DF-7DF3FE8D4EC0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryGateway.md
ms.openlocfilehash: b781207bae8b967acadf4a9ef3ae50c5ffc9cfef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515768"
---
# <span data-ttu-id="1c5e6-101">Remove-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="1c5e6-101">Remove-AzureRmDataFactoryGateway</span></span>

## <span data-ttu-id="1c5e6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1c5e6-102">SYNOPSIS</span></span>
<span data-ttu-id="1c5e6-103">Rimuove un gateway da Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="1c5e6-103">Removes a gateway from Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c5e6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1c5e6-104">SYNTAX</span></span>

### <span data-ttu-id="1c5e6-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1c5e6-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1c5e6-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="1c5e6-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c5e6-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1c5e6-107">DESCRIPTION</span></span>
<span data-ttu-id="1c5e6-108">Il cmdlet **Remove-AzureRmDataFactoryGateway** rimuove il gateway specificato da Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="1c5e6-108">The **Remove-AzureRmDataFactoryGateway** cmdlet removes the specified gateway from Azure Data Factory.</span></span>

## <span data-ttu-id="1c5e6-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1c5e6-109">EXAMPLES</span></span>

### <span data-ttu-id="1c5e6-110">Esempio 1: rimuovere un gateway</span><span class="sxs-lookup"><span data-stu-id="1c5e6-110">Example 1: Remove a gateway</span></span>
```
PS C:\>Remove-AzureRmDataFactoryGateway -Name "ContosoGateway" -DataFactoryName "WikiADF" -ResourceGroupName "ADF"
Confirm
Are you sure you want to remove gateway 'ContosoGateway' in data factory 'WikiADF'? 
 [Y] Yes  [N] No  [S] Suspend  [?] Help (default is Y): Y
True
```

<span data-ttu-id="1c5e6-111">Questo comando rimuove il gateway denominato ContosoGateway dalla data factory denominata WikiADF.</span><span class="sxs-lookup"><span data-stu-id="1c5e6-111">This command removes the gateway named ContosoGateway from the data factory named WikiADF.</span></span>

## <span data-ttu-id="1c5e6-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1c5e6-112">PARAMETERS</span></span>

### <span data-ttu-id="1c5e6-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="1c5e6-113">-DataFactory</span></span>
<span data-ttu-id="1c5e6-114">Specifica un oggetto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="1c5e6-114">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="1c5e6-115">Questo cmdlet consente di rimuovere un gateway dalla data factory specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="1c5e6-115">This cmdlet removes a gateway from the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c5e6-116">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="1c5e6-116">-DataFactoryName</span></span>
<span data-ttu-id="1c5e6-117">Specifica il nome di una data factory.</span><span class="sxs-lookup"><span data-stu-id="1c5e6-117">Specifies the name of a data factory.</span></span>
<span data-ttu-id="1c5e6-118">Questo cmdlet consente di rimuovere un gateway dalla data factory specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="1c5e6-118">This cmdlet removes a gateway from the data factory that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c5e6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c5e6-119">-DefaultProfile</span></span>
<span data-ttu-id="1c5e6-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="1c5e6-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1c5e6-121">-Force</span><span class="sxs-lookup"><span data-stu-id="1c5e6-121">-Force</span></span>
<span data-ttu-id="1c5e6-122">Indica che questo cmdlet rimuove un gateway senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="1c5e6-122">Indicates that this cmdlet removes a gateway without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="1c5e6-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="1c5e6-123">-Name</span></span>
<span data-ttu-id="1c5e6-124">Specifica il nome del gateway da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="1c5e6-124">Specifies the name of the gateway to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c5e6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c5e6-125">-ResourceGroupName</span></span>
<span data-ttu-id="1c5e6-126">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="1c5e6-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="1c5e6-127">Questo cmdlet consente di rimuovere un gateway che appartiene al gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="1c5e6-127">This cmdlet removes a gateway that belongs to the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c5e6-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1c5e6-128">-Confirm</span></span>
<span data-ttu-id="1c5e6-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c5e6-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c5e6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c5e6-130">-WhatIf</span></span>
<span data-ttu-id="1c5e6-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1c5e6-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c5e6-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1c5e6-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c5e6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c5e6-133">CommonParameters</span></span>
<span data-ttu-id="1c5e6-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c5e6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c5e6-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c5e6-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c5e6-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1c5e6-136">INPUTS</span></span>

### <span data-ttu-id="1c5e6-137">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1c5e6-137">None</span></span>
<span data-ttu-id="1c5e6-138">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="1c5e6-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1c5e6-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1c5e6-139">OUTPUTS</span></span>

### <span data-ttu-id="1c5e6-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1c5e6-140">System.Boolean</span></span>

## <span data-ttu-id="1c5e6-141">Note</span><span class="sxs-lookup"><span data-stu-id="1c5e6-141">NOTES</span></span>
* <span data-ttu-id="1c5e6-142">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="1c5e6-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="1c5e6-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1c5e6-143">RELATED LINKS</span></span>

[<span data-ttu-id="1c5e6-144">Get-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="1c5e6-144">Get-AzureRmDataFactoryGateway</span></span>](./Get-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="1c5e6-145">New-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="1c5e6-145">New-AzureRmDataFactoryGateway</span></span>](./New-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="1c5e6-146">Set-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="1c5e6-146">Set-AzureRmDataFactoryGateway</span></span>](./Set-AzureRmDataFactoryGateway.md)


