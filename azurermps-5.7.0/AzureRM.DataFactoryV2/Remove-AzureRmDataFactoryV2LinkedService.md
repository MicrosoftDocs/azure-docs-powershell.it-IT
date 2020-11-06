---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2LinkedService.md
ms.openlocfilehash: a636dcfabe3f1736f9705724ed302ab40d3637a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508211"
---
# <span data-ttu-id="aa2bf-101">Remove-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="aa2bf-101">Remove-AzureRmDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="aa2bf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="aa2bf-102">SYNOPSIS</span></span>
<span data-ttu-id="aa2bf-103">Rimuove un servizio collegato da data factory.</span><span class="sxs-lookup"><span data-stu-id="aa2bf-103">Removes a linked service from Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa2bf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aa2bf-104">SYNTAX</span></span>

### <span data-ttu-id="aa2bf-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="aa2bf-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2LinkedService [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aa2bf-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="aa2bf-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2LinkedService [-InputObject] <PSLinkedService> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa2bf-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="aa2bf-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2LinkedService [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa2bf-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aa2bf-108">DESCRIPTION</span></span>
<span data-ttu-id="aa2bf-109">Il cmdlet Remove-AzureRmDataFactoryV2LinkedService rimuove un servizio collegato da Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="aa2bf-109">The Remove-AzureRmDataFactoryV2LinkedService cmdlet removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="aa2bf-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aa2bf-110">EXAMPLES</span></span>

### <span data-ttu-id="aa2bf-111">Esempio 1: rimuovere un servizio collegato</span><span class="sxs-lookup"><span data-stu-id="aa2bf-111">Example 1: Remove a linked service</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceTest"
          Confirm
          Are you sure you want to remove linked service 'LinkedServiceTest' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="aa2bf-112">Questo comando rimuove il servizio collegato denominato LinkedServiceTest dalla data factory denominata WikiADF.</span><span class="sxs-lookup"><span data-stu-id="aa2bf-112">This command removes the linked service named LinkedServiceTest from the data factory named WikiADF.</span></span>
<span data-ttu-id="aa2bf-113">Questo comando restituisce un valore di $True.</span><span class="sxs-lookup"><span data-stu-id="aa2bf-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="aa2bf-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="aa2bf-114">PARAMETERS</span></span>

### <span data-ttu-id="aa2bf-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="aa2bf-115">-DataFactoryName</span></span>
<span data-ttu-id="aa2bf-116">Specifica il nome di una data factory.</span><span class="sxs-lookup"><span data-stu-id="aa2bf-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="aa2bf-117">Questo cmdlet consente di rimuovere un servizio collegato dalla data factory specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="aa2bf-117">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="aa2bf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa2bf-118">-DefaultProfile</span></span>
<span data-ttu-id="aa2bf-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="aa2bf-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa2bf-120">-Force</span><span class="sxs-lookup"><span data-stu-id="aa2bf-120">-Force</span></span>
<span data-ttu-id="aa2bf-121">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="aa2bf-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="aa2bf-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aa2bf-122">-InputObject</span></span>
<span data-ttu-id="aa2bf-123">Specifica l'oggetto LinkedService da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="aa2bf-123">Specifies the LinkedService object to remove.</span></span>

```yaml
Type: PSLinkedService
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aa2bf-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="aa2bf-124">-Name</span></span>
<span data-ttu-id="aa2bf-125">Specifica il nome del servizio collegato da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="aa2bf-125">Specifies the name of the linked service to remove.</span></span>
<span data-ttu-id="aa2bf-126">Nome del servizio collegato.</span><span class="sxs-lookup"><span data-stu-id="aa2bf-126">Name of the linked service.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa2bf-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa2bf-127">-ResourceGroupName</span></span>
<span data-ttu-id="aa2bf-128">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="aa2bf-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="aa2bf-129">Questo cmdlet consente di rimuovere un servizio collegato dal gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="aa2bf-129">This cmdlet removes a linked service from the group that this parameter specifies.</span></span>


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

### <span data-ttu-id="aa2bf-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aa2bf-130">-ResourceId</span></span>
<span data-ttu-id="aa2bf-131">ID risorsa Azure del servizio collegato da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="aa2bf-131">The Azure resource ID of the linked service to remove.</span></span>

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

### <span data-ttu-id="aa2bf-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="aa2bf-132">-Confirm</span></span>
<span data-ttu-id="aa2bf-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa2bf-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa2bf-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa2bf-134">-WhatIf</span></span>
<span data-ttu-id="aa2bf-135">Mostra cosa succede se il cmdlet viene eseguito, ma il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aa2bf-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="aa2bf-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa2bf-136">CommonParameters</span></span>
<span data-ttu-id="aa2bf-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa2bf-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa2bf-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa2bf-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa2bf-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="aa2bf-139">INPUTS</span></span>

### <span data-ttu-id="aa2bf-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="aa2bf-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>
<span data-ttu-id="aa2bf-141">System. String</span><span class="sxs-lookup"><span data-stu-id="aa2bf-141">System.String</span></span>

## <span data-ttu-id="aa2bf-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aa2bf-142">OUTPUTS</span></span>

### <span data-ttu-id="aa2bf-143">System. Object</span><span class="sxs-lookup"><span data-stu-id="aa2bf-143">System.Object</span></span>

## <span data-ttu-id="aa2bf-144">Note</span><span class="sxs-lookup"><span data-stu-id="aa2bf-144">NOTES</span></span>
<span data-ttu-id="aa2bf-145">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="aa2bf-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="aa2bf-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aa2bf-146">RELATED LINKS</span></span>

[<span data-ttu-id="aa2bf-147">Get-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="aa2bf-147">Get-AzureRmDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="aa2bf-148">Set-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="aa2bf-148">Set-AzureRmDataFactoryV2LinkedService</span></span>]()

