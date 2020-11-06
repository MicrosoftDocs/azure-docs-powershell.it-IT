---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/update-azurermdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Update-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Update-AzureRmDataFactoryV2.md
ms.openlocfilehash: 09e13e973178444496604843336c8f483508c59e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515388"
---
# <span data-ttu-id="0fce6-101">Update-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="0fce6-101">Update-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="0fce6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0fce6-102">SYNOPSIS</span></span>
<span data-ttu-id="0fce6-103">Aggiorna le proprietà di una data factory.</span><span class="sxs-lookup"><span data-stu-id="0fce6-103">Updates the properties of a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0fce6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0fce6-104">SYNTAX</span></span>

### <span data-ttu-id="0fce6-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0fce6-105">ByFactoryName (Default)</span></span>
```
Update-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0fce6-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="0fce6-106">ByFactoryObject</span></span>
```
Update-AzureRmDataFactoryV2 [-InputObject] <PSDataFactory> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0fce6-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0fce6-107">ByResourceId</span></span>
```
Update-AzureRmDataFactoryV2 [-ResourceId] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0fce6-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0fce6-108">DESCRIPTION</span></span>
<span data-ttu-id="0fce6-109">Il cmdlet **Update-AzureRmDataFactoryV2** aggiorna i tag o le proprietà di identità di una factory di dati.</span><span class="sxs-lookup"><span data-stu-id="0fce6-109">The **Update-AzureRmDataFactoryV2** cmdlet updates tags or identity properties of a data factory.</span></span>

## <span data-ttu-id="0fce6-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0fce6-110">EXAMPLES</span></span>

### <span data-ttu-id="0fce6-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0fce6-111">Example 1</span></span>
```
PS C:\> Update-AzureRmDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF" -Tag @{myNewTagName = "myTagValue"}

Confirm
Are you sure you want to update properties of the data factory 'WikiADF' in resource group 'ADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y


DataFactoryName   : WikiADF
DataFactoryId     : /subscriptions/1e42591f-1f0c-4c5a-b7f2-a268f6105ec5/resourceGroups/adf/providers/Microsoft.DataF
                    actory/factories/wikiadf
ResourceGroupName : ADF
Location          : EastUS
Tags              : {[myNewTagName, myTagValue]}
Identity          :
ProvisioningState : Succeeded
```

<span data-ttu-id="0fce6-112">Questo comando Aggiorna i tag per la Factory WikiADF in un dizionario che contiene un tag denominato myNewTagName con il valore myTagValue.</span><span class="sxs-lookup"><span data-stu-id="0fce6-112">This command updates the tags for the factory WikiADF to a dictionary containing a tag named myNewTagName with value myTagValue.</span></span>

## <span data-ttu-id="0fce6-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0fce6-113">PARAMETERS</span></span>

### <span data-ttu-id="0fce6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fce6-114">-DefaultProfile</span></span>
<span data-ttu-id="0fce6-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0fce6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0fce6-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0fce6-116">-InputObject</span></span>
<span data-ttu-id="0fce6-117">Oggetto Data Factory.</span><span class="sxs-lookup"><span data-stu-id="0fce6-117">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0fce6-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="0fce6-118">-Name</span></span>
<span data-ttu-id="0fce6-119">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="0fce6-119">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fce6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fce6-120">-ResourceGroupName</span></span>
<span data-ttu-id="0fce6-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0fce6-121">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fce6-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0fce6-122">-ResourceId</span></span>
<span data-ttu-id="0fce6-123">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="0fce6-123">The Azure resource ID.</span></span>

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

### <span data-ttu-id="0fce6-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="0fce6-124">-Tag</span></span>
<span data-ttu-id="0fce6-125">Tag della data factory.</span><span class="sxs-lookup"><span data-stu-id="0fce6-125">The tags of the data factory.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fce6-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0fce6-126">-Confirm</span></span>
<span data-ttu-id="0fce6-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0fce6-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fce6-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fce6-128">-WhatIf</span></span>
<span data-ttu-id="0fce6-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0fce6-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0fce6-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0fce6-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fce6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fce6-131">CommonParameters</span></span>
<span data-ttu-id="0fce6-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fce6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fce6-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fce6-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fce6-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0fce6-134">INPUTS</span></span>

### <span data-ttu-id="0fce6-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="0fce6-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="0fce6-136">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0fce6-136">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="0fce6-137">System. String</span><span class="sxs-lookup"><span data-stu-id="0fce6-137">System.String</span></span>

## <span data-ttu-id="0fce6-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0fce6-138">OUTPUTS</span></span>

### <span data-ttu-id="0fce6-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="0fce6-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="0fce6-140">Note</span><span class="sxs-lookup"><span data-stu-id="0fce6-140">NOTES</span></span>

## <span data-ttu-id="0fce6-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0fce6-141">RELATED LINKS</span></span>
