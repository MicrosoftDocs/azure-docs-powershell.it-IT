---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2LinkedService.md
ms.openlocfilehash: acd3fadd45dfc32c745af943013f4c0f00b663ad
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298308"
---
# <span data-ttu-id="3445d-101">Remove-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="3445d-101">Remove-AzDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="3445d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3445d-102">SYNOPSIS</span></span>
<span data-ttu-id="3445d-103">Rimuove un servizio collegato da data factory.</span><span class="sxs-lookup"><span data-stu-id="3445d-103">Removes a linked service from Data Factory.</span></span>

## <span data-ttu-id="3445d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3445d-104">SYNTAX</span></span>

### <span data-ttu-id="3445d-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3445d-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2LinkedService [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3445d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="3445d-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2LinkedService [-InputObject] <PSLinkedService> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3445d-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3445d-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2LinkedService [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3445d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3445d-108">DESCRIPTION</span></span>
<span data-ttu-id="3445d-109">Il cmdlet Remove-AzDataFactoryV2LinkedService rimuove un servizio collegato da Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="3445d-109">The Remove-AzDataFactoryV2LinkedService cmdlet removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="3445d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3445d-110">EXAMPLES</span></span>

### <span data-ttu-id="3445d-111">Esempio 1: rimuovere un servizio collegato</span><span class="sxs-lookup"><span data-stu-id="3445d-111">Example 1: Remove a linked service</span></span>
```
PS C:\> Remove-AzDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceTest"
          Confirm
          Are you sure you want to remove linked service 'LinkedServiceTest' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="3445d-112">Questo comando rimuove il servizio collegato denominato LinkedServiceTest dalla data factory denominata WikiADF.</span><span class="sxs-lookup"><span data-stu-id="3445d-112">This command removes the linked service named LinkedServiceTest from the data factory named WikiADF.</span></span>
<span data-ttu-id="3445d-113">Questo comando restituisce un valore di $True.</span><span class="sxs-lookup"><span data-stu-id="3445d-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="3445d-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3445d-114">PARAMETERS</span></span>

### <span data-ttu-id="3445d-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="3445d-115">-DataFactoryName</span></span>
<span data-ttu-id="3445d-116">Specifica il nome di una data factory.</span><span class="sxs-lookup"><span data-stu-id="3445d-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="3445d-117">Questo cmdlet consente di rimuovere un servizio collegato dalla data factory specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="3445d-117">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="3445d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3445d-118">-DefaultProfile</span></span>
<span data-ttu-id="3445d-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3445d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3445d-120">-Force</span><span class="sxs-lookup"><span data-stu-id="3445d-120">-Force</span></span>
<span data-ttu-id="3445d-121">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="3445d-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="3445d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3445d-122">-InputObject</span></span>
<span data-ttu-id="3445d-123">Specifica l'oggetto LinkedService da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="3445d-123">Specifies the LinkedService object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3445d-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="3445d-124">-Name</span></span>
<span data-ttu-id="3445d-125">Specifica il nome del servizio collegato da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="3445d-125">Specifies the name of the linked service to remove.</span></span>
<span data-ttu-id="3445d-126">Nome del servizio collegato.</span><span class="sxs-lookup"><span data-stu-id="3445d-126">Name of the linked service.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3445d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3445d-127">-ResourceGroupName</span></span>
<span data-ttu-id="3445d-128">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="3445d-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="3445d-129">Questo cmdlet consente di rimuovere un servizio collegato dal gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="3445d-129">This cmdlet removes a linked service from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="3445d-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3445d-130">-ResourceId</span></span>
<span data-ttu-id="3445d-131">ID risorsa Azure del servizio collegato da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="3445d-131">The Azure resource ID of the linked service to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3445d-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3445d-132">-Confirm</span></span>
<span data-ttu-id="3445d-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3445d-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3445d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3445d-134">-WhatIf</span></span>
<span data-ttu-id="3445d-135">Mostra cosa succede se il cmdlet viene eseguito, ma il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3445d-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3445d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3445d-136">CommonParameters</span></span>
<span data-ttu-id="3445d-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3445d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3445d-138">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3445d-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3445d-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3445d-139">INPUTS</span></span>

### <span data-ttu-id="3445d-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="3445d-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>

### <span data-ttu-id="3445d-141">System. String</span><span class="sxs-lookup"><span data-stu-id="3445d-141">System.String</span></span>

## <span data-ttu-id="3445d-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3445d-142">OUTPUTS</span></span>

### <span data-ttu-id="3445d-143">System. void</span><span class="sxs-lookup"><span data-stu-id="3445d-143">System.Void</span></span>

## <span data-ttu-id="3445d-144">Note</span><span class="sxs-lookup"><span data-stu-id="3445d-144">NOTES</span></span>
<span data-ttu-id="3445d-145">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="3445d-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="3445d-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3445d-146">RELATED LINKS</span></span>

[<span data-ttu-id="3445d-147">Get-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="3445d-147">Get-AzDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="3445d-148">Set-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="3445d-148">Set-AzDataFactoryV2LinkedService</span></span>]()

