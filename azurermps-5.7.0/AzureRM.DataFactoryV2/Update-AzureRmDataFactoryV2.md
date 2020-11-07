---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/update-azurermdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Update-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Update-AzureRmDataFactoryV2.md
ms.openlocfilehash: d7173b75d9796eeab974973f9f997d5b7cb72b49
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686330"
---
# <span data-ttu-id="6bfbc-101">Update-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="6bfbc-101">Update-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="6bfbc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6bfbc-102">SYNOPSIS</span></span>
<span data-ttu-id="6bfbc-103">Aggiorna le proprietà di una data factory.</span><span class="sxs-lookup"><span data-stu-id="6bfbc-103">Updates the properties of a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6bfbc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6bfbc-104">SYNTAX</span></span>

### <span data-ttu-id="6bfbc-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6bfbc-105">ByFactoryName (Default)</span></span>
```
Update-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6bfbc-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="6bfbc-106">ByFactoryObject</span></span>
```
Update-AzureRmDataFactoryV2 [-InputObject] <PSDataFactory> [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6bfbc-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6bfbc-107">ByResourceId</span></span>
```
Update-AzureRmDataFactoryV2 [-ResourceId] <String> [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6bfbc-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6bfbc-108">DESCRIPTION</span></span>
<span data-ttu-id="6bfbc-109">Il cmdlet **Update-AzureRmDataFactoryV2** aggiorna i tag o le proprietà di identità di una factory di dati.</span><span class="sxs-lookup"><span data-stu-id="6bfbc-109">The **Update-AzureRmDataFactoryV2** cmdlet updates tags or identity properties of a data factory.</span></span>

## <span data-ttu-id="6bfbc-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6bfbc-110">EXAMPLES</span></span>

### <span data-ttu-id="6bfbc-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6bfbc-111">Example 1</span></span>
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

<span data-ttu-id="6bfbc-112">Questo comando Aggiorna i tag per la Factory WikiADF in un dizionario che contiene un tag denominato myNewTagName con il valore myTagValue.</span><span class="sxs-lookup"><span data-stu-id="6bfbc-112">This command updates the tags for the factory WikiADF to a dictionary containing a tag named myNewTagName with value myTagValue.</span></span>

## <span data-ttu-id="6bfbc-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6bfbc-113">PARAMETERS</span></span>

### <span data-ttu-id="6bfbc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bfbc-114">-DefaultProfile</span></span>
<span data-ttu-id="6bfbc-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6bfbc-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6bfbc-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6bfbc-116">-InputObject</span></span>
<span data-ttu-id="6bfbc-117">Oggetto Data Factory.</span><span class="sxs-lookup"><span data-stu-id="6bfbc-117">The data factory object.</span></span>

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

### <span data-ttu-id="6bfbc-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="6bfbc-118">-Name</span></span>
<span data-ttu-id="6bfbc-119">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="6bfbc-119">The data factory name.</span></span>

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

### <span data-ttu-id="6bfbc-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bfbc-120">-ResourceGroupName</span></span>
<span data-ttu-id="6bfbc-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6bfbc-121">The resource group name.</span></span>

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

### <span data-ttu-id="6bfbc-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6bfbc-122">-ResourceId</span></span>
<span data-ttu-id="6bfbc-123">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="6bfbc-123">The Azure resource ID.</span></span>

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

### <span data-ttu-id="6bfbc-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="6bfbc-124">-Tag</span></span>
<span data-ttu-id="6bfbc-125">Tag della data factory.</span><span class="sxs-lookup"><span data-stu-id="6bfbc-125">The tags of the data factory.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bfbc-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6bfbc-126">-Confirm</span></span>
<span data-ttu-id="6bfbc-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6bfbc-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bfbc-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bfbc-128">-WhatIf</span></span>
<span data-ttu-id="6bfbc-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6bfbc-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6bfbc-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6bfbc-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6bfbc-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bfbc-131">CommonParameters</span></span>
<span data-ttu-id="6bfbc-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6bfbc-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bfbc-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bfbc-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bfbc-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6bfbc-134">INPUTS</span></span>

### <span data-ttu-id="6bfbc-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="6bfbc-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="6bfbc-136">System. String Microsoft. Azure. Management. DataFactory. Models. FactoryIdentity</span><span class="sxs-lookup"><span data-stu-id="6bfbc-136">System.String Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity</span></span>

## <span data-ttu-id="6bfbc-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6bfbc-137">OUTPUTS</span></span>

### <span data-ttu-id="6bfbc-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="6bfbc-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="6bfbc-139">Note</span><span class="sxs-lookup"><span data-stu-id="6bfbc-139">NOTES</span></span>

## <span data-ttu-id="6bfbc-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6bfbc-140">RELATED LINKS</span></span>

