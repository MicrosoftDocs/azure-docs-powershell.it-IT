---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/update-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2.md
ms.openlocfilehash: 57c0a05c5b0f279fa7c9f06cd561385de87698bf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186223"
---
# <span data-ttu-id="81bb1-101">Update-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="81bb1-101">Update-AzDataFactoryV2</span></span>

## <span data-ttu-id="81bb1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81bb1-102">SYNOPSIS</span></span>
<span data-ttu-id="81bb1-103">Aggiorna le proprietà di un data factory.</span><span class="sxs-lookup"><span data-stu-id="81bb1-103">Updates the properties of a data factory.</span></span>

## <span data-ttu-id="81bb1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="81bb1-104">SYNTAX</span></span>

### <span data-ttu-id="81bb1-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="81bb1-105">ByFactoryName (Default)</span></span>
```
Update-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81bb1-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="81bb1-106">ByFactoryObject</span></span>
```
Update-AzDataFactoryV2 [-InputObject] <PSDataFactory> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81bb1-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="81bb1-107">ByResourceId</span></span>
```
Update-AzDataFactoryV2 [-ResourceId] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81bb1-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="81bb1-108">DESCRIPTION</span></span>
<span data-ttu-id="81bb1-109">Il cmdlet **Update-AzDataFactoryV2** aggiorna i tag o le proprietà di identità di un data factory.</span><span class="sxs-lookup"><span data-stu-id="81bb1-109">The **Update-AzDataFactoryV2** cmdlet updates tags or identity properties of a data factory.</span></span>

## <span data-ttu-id="81bb1-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="81bb1-110">EXAMPLES</span></span>

### <span data-ttu-id="81bb1-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="81bb1-111">Example 1</span></span>
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

<span data-ttu-id="81bb1-112">Questo comando aggiorna i tag per il produttore WikiADF in un dizionario contenente un tag denominato myNewTagName con il valore myTagValue.</span><span class="sxs-lookup"><span data-stu-id="81bb1-112">This command updates the tags for the factory WikiADF to a dictionary containing a tag named myNewTagName with value myTagValue.</span></span>

## <span data-ttu-id="81bb1-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="81bb1-113">PARAMETERS</span></span>

### <span data-ttu-id="81bb1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81bb1-114">-DefaultProfile</span></span>
<span data-ttu-id="81bb1-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="81bb1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81bb1-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="81bb1-116">-InputObject</span></span>
<span data-ttu-id="81bb1-117">Oggetto data factory.</span><span class="sxs-lookup"><span data-stu-id="81bb1-117">The data factory object.</span></span>

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

### <span data-ttu-id="81bb1-118">-Name</span><span class="sxs-lookup"><span data-stu-id="81bb1-118">-Name</span></span>
<span data-ttu-id="81bb1-119">Nome del data factory.</span><span class="sxs-lookup"><span data-stu-id="81bb1-119">The data factory name.</span></span>

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

### <span data-ttu-id="81bb1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81bb1-120">-ResourceGroupName</span></span>
<span data-ttu-id="81bb1-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="81bb1-121">The resource group name.</span></span>

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

### <span data-ttu-id="81bb1-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="81bb1-122">-ResourceId</span></span>
<span data-ttu-id="81bb1-123">ID della risorsa Azure.</span><span class="sxs-lookup"><span data-stu-id="81bb1-123">The Azure resource ID.</span></span>

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

### <span data-ttu-id="81bb1-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="81bb1-124">-Tag</span></span>
<span data-ttu-id="81bb1-125">I tag del data factory.</span><span class="sxs-lookup"><span data-stu-id="81bb1-125">The tags of the data factory.</span></span>

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

### <span data-ttu-id="81bb1-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="81bb1-126">-Confirm</span></span>
<span data-ttu-id="81bb1-127">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81bb1-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81bb1-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81bb1-128">-WhatIf</span></span>
<span data-ttu-id="81bb1-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="81bb1-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="81bb1-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="81bb1-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81bb1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81bb1-131">CommonParameters</span></span>
<span data-ttu-id="81bb1-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81bb1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81bb1-133">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81bb1-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81bb1-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="81bb1-134">INPUTS</span></span>

### <span data-ttu-id="81bb1-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="81bb1-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="81bb1-136">System.String</span><span class="sxs-lookup"><span data-stu-id="81bb1-136">System.String</span></span>

## <span data-ttu-id="81bb1-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="81bb1-137">OUTPUTS</span></span>

### <span data-ttu-id="81bb1-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="81bb1-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="81bb1-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="81bb1-139">NOTES</span></span>

## <span data-ttu-id="81bb1-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="81bb1-140">RELATED LINKS</span></span>
