---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/update-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2.md
ms.openlocfilehash: 85bd5f6eef9c4f10d8a40ee58817f531a542d9ff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836423"
---
# <span data-ttu-id="22e26-101">Update-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="22e26-101">Update-AzDataFactoryV2</span></span>

## <span data-ttu-id="22e26-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="22e26-102">SYNOPSIS</span></span>
<span data-ttu-id="22e26-103">Aggiorna le proprietà di una data factory.</span><span class="sxs-lookup"><span data-stu-id="22e26-103">Updates the properties of a data factory.</span></span>

## <span data-ttu-id="22e26-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="22e26-104">SYNTAX</span></span>

### <span data-ttu-id="22e26-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="22e26-105">ByFactoryName (Default)</span></span>
```
Update-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22e26-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="22e26-106">ByFactoryObject</span></span>
```
Update-AzDataFactoryV2 [-InputObject] <PSDataFactory> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22e26-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="22e26-107">ByResourceId</span></span>
```
Update-AzDataFactoryV2 [-ResourceId] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22e26-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="22e26-108">DESCRIPTION</span></span>
<span data-ttu-id="22e26-109">Il cmdlet **Update-AzDataFactoryV2** aggiorna i tag o le proprietà di identità di una factory di dati.</span><span class="sxs-lookup"><span data-stu-id="22e26-109">The **Update-AzDataFactoryV2** cmdlet updates tags or identity properties of a data factory.</span></span>

## <span data-ttu-id="22e26-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="22e26-110">EXAMPLES</span></span>

### <span data-ttu-id="22e26-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="22e26-111">Example 1</span></span>
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

<span data-ttu-id="22e26-112">Questo comando Aggiorna i tag per la Factory WikiADF in un dizionario che contiene un tag denominato myNewTagName con il valore myTagValue.</span><span class="sxs-lookup"><span data-stu-id="22e26-112">This command updates the tags for the factory WikiADF to a dictionary containing a tag named myNewTagName with value myTagValue.</span></span>

## <span data-ttu-id="22e26-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="22e26-113">PARAMETERS</span></span>

### <span data-ttu-id="22e26-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22e26-114">-DefaultProfile</span></span>
<span data-ttu-id="22e26-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="22e26-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22e26-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="22e26-116">-InputObject</span></span>
<span data-ttu-id="22e26-117">Oggetto Data Factory.</span><span class="sxs-lookup"><span data-stu-id="22e26-117">The data factory object.</span></span>

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

### <span data-ttu-id="22e26-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="22e26-118">-Name</span></span>
<span data-ttu-id="22e26-119">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="22e26-119">The data factory name.</span></span>

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

### <span data-ttu-id="22e26-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22e26-120">-ResourceGroupName</span></span>
<span data-ttu-id="22e26-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="22e26-121">The resource group name.</span></span>

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

### <span data-ttu-id="22e26-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="22e26-122">-ResourceId</span></span>
<span data-ttu-id="22e26-123">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="22e26-123">The Azure resource ID.</span></span>

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

### <span data-ttu-id="22e26-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="22e26-124">-Tag</span></span>
<span data-ttu-id="22e26-125">Tag della data factory.</span><span class="sxs-lookup"><span data-stu-id="22e26-125">The tags of the data factory.</span></span>

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

### <span data-ttu-id="22e26-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="22e26-126">-Confirm</span></span>
<span data-ttu-id="22e26-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22e26-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22e26-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22e26-128">-WhatIf</span></span>
<span data-ttu-id="22e26-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="22e26-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="22e26-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="22e26-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22e26-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22e26-131">CommonParameters</span></span>
<span data-ttu-id="22e26-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22e26-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22e26-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22e26-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22e26-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="22e26-134">INPUTS</span></span>

### <span data-ttu-id="22e26-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="22e26-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="22e26-136">System. String</span><span class="sxs-lookup"><span data-stu-id="22e26-136">System.String</span></span>

## <span data-ttu-id="22e26-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="22e26-137">OUTPUTS</span></span>

### <span data-ttu-id="22e26-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="22e26-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="22e26-139">Note</span><span class="sxs-lookup"><span data-stu-id="22e26-139">NOTES</span></span>

## <span data-ttu-id="22e26-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="22e26-140">RELATED LINKS</span></span>
