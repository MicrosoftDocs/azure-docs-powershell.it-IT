---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/update-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2.md
ms.openlocfilehash: 57c0a05c5b0f279fa7c9f06cd561385de87698bf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93865222"
---
# <span data-ttu-id="1a44a-101">Update-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="1a44a-101">Update-AzDataFactoryV2</span></span>

## <span data-ttu-id="1a44a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1a44a-102">SYNOPSIS</span></span>
<span data-ttu-id="1a44a-103">Aggiorna le proprietà di una data factory.</span><span class="sxs-lookup"><span data-stu-id="1a44a-103">Updates the properties of a data factory.</span></span>

## <span data-ttu-id="1a44a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1a44a-104">SYNTAX</span></span>

### <span data-ttu-id="1a44a-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1a44a-105">ByFactoryName (Default)</span></span>
```
Update-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a44a-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="1a44a-106">ByFactoryObject</span></span>
```
Update-AzDataFactoryV2 [-InputObject] <PSDataFactory> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a44a-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1a44a-107">ByResourceId</span></span>
```
Update-AzDataFactoryV2 [-ResourceId] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a44a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1a44a-108">DESCRIPTION</span></span>
<span data-ttu-id="1a44a-109">Il cmdlet **Update-AzDataFactoryV2** aggiorna i tag o le proprietà di identità di una factory di dati.</span><span class="sxs-lookup"><span data-stu-id="1a44a-109">The **Update-AzDataFactoryV2** cmdlet updates tags or identity properties of a data factory.</span></span>

## <span data-ttu-id="1a44a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1a44a-110">EXAMPLES</span></span>

### <span data-ttu-id="1a44a-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1a44a-111">Example 1</span></span>
```
PS C:\> Update-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF" -Tag @{myNewTagName = "myTagValue"}

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

<span data-ttu-id="1a44a-112">Questo comando Aggiorna i tag per la Factory WikiADF in un dizionario che contiene un tag denominato myNewTagName con il valore myTagValue.</span><span class="sxs-lookup"><span data-stu-id="1a44a-112">This command updates the tags for the factory WikiADF to a dictionary containing a tag named myNewTagName with value myTagValue.</span></span>

## <span data-ttu-id="1a44a-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1a44a-113">PARAMETERS</span></span>

### <span data-ttu-id="1a44a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a44a-114">-DefaultProfile</span></span>
<span data-ttu-id="1a44a-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1a44a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a44a-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1a44a-116">-InputObject</span></span>
<span data-ttu-id="1a44a-117">Oggetto Data Factory.</span><span class="sxs-lookup"><span data-stu-id="1a44a-117">The data factory object.</span></span>

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

### <span data-ttu-id="1a44a-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="1a44a-118">-Name</span></span>
<span data-ttu-id="1a44a-119">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="1a44a-119">The data factory name.</span></span>

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

### <span data-ttu-id="1a44a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a44a-120">-ResourceGroupName</span></span>
<span data-ttu-id="1a44a-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1a44a-121">The resource group name.</span></span>

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

### <span data-ttu-id="1a44a-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1a44a-122">-ResourceId</span></span>
<span data-ttu-id="1a44a-123">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="1a44a-123">The Azure resource ID.</span></span>

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

### <span data-ttu-id="1a44a-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="1a44a-124">-Tag</span></span>
<span data-ttu-id="1a44a-125">Tag della data factory.</span><span class="sxs-lookup"><span data-stu-id="1a44a-125">The tags of the data factory.</span></span>

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

### <span data-ttu-id="1a44a-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1a44a-126">-Confirm</span></span>
<span data-ttu-id="1a44a-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a44a-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a44a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a44a-128">-WhatIf</span></span>
<span data-ttu-id="1a44a-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1a44a-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1a44a-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1a44a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a44a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a44a-131">CommonParameters</span></span>
<span data-ttu-id="1a44a-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a44a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a44a-133">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a44a-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a44a-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1a44a-134">INPUTS</span></span>

### <span data-ttu-id="1a44a-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="1a44a-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="1a44a-136">System. String</span><span class="sxs-lookup"><span data-stu-id="1a44a-136">System.String</span></span>

## <span data-ttu-id="1a44a-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1a44a-137">OUTPUTS</span></span>

### <span data-ttu-id="1a44a-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="1a44a-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="1a44a-139">Note</span><span class="sxs-lookup"><span data-stu-id="1a44a-139">NOTES</span></span>

## <span data-ttu-id="1a44a-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1a44a-140">RELATED LINKS</span></span>
