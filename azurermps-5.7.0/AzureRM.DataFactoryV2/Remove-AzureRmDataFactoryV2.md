---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2.md
ms.openlocfilehash: 330bcf3622faa515a58ea8f1e087d1383b9f154a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508220"
---
# <span data-ttu-id="026b3-101">Remove-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="026b3-101">Remove-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="026b3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="026b3-102">SYNOPSIS</span></span>
<span data-ttu-id="026b3-103">Rimuove una data factory.</span><span class="sxs-lookup"><span data-stu-id="026b3-103">Removes a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="026b3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="026b3-104">SYNTAX</span></span>

### <span data-ttu-id="026b3-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="026b3-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="026b3-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="026b3-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryV2 [-InputObject] <PSDataFactory> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="026b3-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="026b3-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2 [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="026b3-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="026b3-108">DESCRIPTION</span></span>
<span data-ttu-id="026b3-109">Il cmdlet Remove-AzureRmDataFactoryV2 rimuove una data factory.</span><span class="sxs-lookup"><span data-stu-id="026b3-109">The Remove-AzureRmDataFactoryV2 cmdlet removes a data factory.</span></span>

## <span data-ttu-id="026b3-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="026b3-110">EXAMPLES</span></span>

### <span data-ttu-id="026b3-111">Esempio 1: rimuovere una data factory</span><span class="sxs-lookup"><span data-stu-id="026b3-111">Example 1: Remove a data factory</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2 -Name "WikiADF" -ResourceGroupName "ADF"
          Confirm
          Are you sure you want to remove data factory 'WikiADF' in resource group 'ADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="026b3-112">Questo comando rimuove la factory di dati denominata WikiADF dal gruppo di risorse denominato ADF.</span><span class="sxs-lookup"><span data-stu-id="026b3-112">This command removes the data factory named WikiADF from the resource group named ADF.</span></span>
<span data-ttu-id="026b3-113">Questo comando restituisce un valore di $True.</span><span class="sxs-lookup"><span data-stu-id="026b3-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="026b3-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="026b3-114">PARAMETERS</span></span>

### <span data-ttu-id="026b3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="026b3-115">-DefaultProfile</span></span>
<span data-ttu-id="026b3-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="026b3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="026b3-117">-Force</span><span class="sxs-lookup"><span data-stu-id="026b3-117">-Force</span></span>
<span data-ttu-id="026b3-118">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="026b3-118">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="026b3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="026b3-119">-InputObject</span></span>
<span data-ttu-id="026b3-120">Specifica l'oggetto DataFactory da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="026b3-120">Specifies the DataFactory object to remove.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="026b3-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="026b3-121">-Name</span></span>
<span data-ttu-id="026b3-122">Specifica il nome della factory di dati da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="026b3-122">Specifies the name of the data factory to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="026b3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="026b3-123">-ResourceGroupName</span></span>
<span data-ttu-id="026b3-124">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="026b3-124">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="026b3-125">Questo cmdlet consente di rimuovere una data factory dal gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="026b3-125">This cmdlet removes a data factory from the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="026b3-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="026b3-126">-ResourceId</span></span>
<span data-ttu-id="026b3-127">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="026b3-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="026b3-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="026b3-128">-Confirm</span></span>
<span data-ttu-id="026b3-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="026b3-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="026b3-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="026b3-130">-WhatIf</span></span>
<span data-ttu-id="026b3-131">Mostra cosa succede se il cmdlet viene eseguito, ma il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="026b3-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="026b3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="026b3-132">CommonParameters</span></span>
<span data-ttu-id="026b3-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="026b3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="026b3-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="026b3-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="026b3-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="026b3-135">INPUTS</span></span>

### <span data-ttu-id="026b3-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="026b3-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="026b3-137">System. String</span><span class="sxs-lookup"><span data-stu-id="026b3-137">System.String</span></span>

## <span data-ttu-id="026b3-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="026b3-138">OUTPUTS</span></span>

### <span data-ttu-id="026b3-139">System. Object</span><span class="sxs-lookup"><span data-stu-id="026b3-139">System.Object</span></span>

## <span data-ttu-id="026b3-140">Note</span><span class="sxs-lookup"><span data-stu-id="026b3-140">NOTES</span></span>
<span data-ttu-id="026b3-141">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="026b3-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="026b3-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="026b3-142">RELATED LINKS</span></span>

[<span data-ttu-id="026b3-143">Get-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="026b3-143">Get-AzureRmDataFactoryV2</span></span>]()

[<span data-ttu-id="026b3-144">Set-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="026b3-144">Set-AzureRmDataFactoryV2</span></span>]()
