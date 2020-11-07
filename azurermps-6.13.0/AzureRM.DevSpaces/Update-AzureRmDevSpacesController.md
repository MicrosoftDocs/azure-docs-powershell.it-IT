---
external help file: Microsoft.Azure.Commands.DevSpaces.dll-Help.xml
Module Name: AzureRM.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devspaces/update-azureevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevSpaces/Commands.DevSpaces/help/Update-AzureRmDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevSpaces/Commands.DevSpaces/help/Update-AzureRmDevSpacesController.md
ms.openlocfilehash: b413311fea0d7e2235bc5e4ddb04e40db6d81162
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687594"
---
# <span data-ttu-id="643c7-101">Update-AzureRmDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="643c7-101">Update-AzureRmDevSpacesController</span></span>

## <span data-ttu-id="643c7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="643c7-102">SYNOPSIS</span></span>
<span data-ttu-id="643c7-103">Aggiornare il controller DevSpaces per aggiungere tag.</span><span class="sxs-lookup"><span data-stu-id="643c7-103">Update the DevSpaces controller to add tags.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="643c7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="643c7-104">SYNTAX</span></span>

### <span data-ttu-id="643c7-105">DevSpacesControllerNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="643c7-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Update-AzureRmDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="643c7-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="643c7-106">ResourceIdParameterSet</span></span>
```
Update-AzureRmDevSpacesController -ResourceId <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="643c7-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="643c7-107">InputObjectParameterSet</span></span>
```
Update-AzureRmDevSpacesController -InputObject <PSController> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="643c7-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="643c7-108">DESCRIPTION</span></span>
<span data-ttu-id="643c7-109">Aggiornare il controller DevSpaces per aggiungere tag.</span><span class="sxs-lookup"><span data-stu-id="643c7-109">Update the DevSpaces controller to add tags.</span></span> 

## <span data-ttu-id="643c7-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="643c7-110">EXAMPLES</span></span>

### <span data-ttu-id="643c7-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="643c7-111">Example 1</span></span>
```powershell
PS C:\> Update-AzureRmDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName -Tag @{ tagKey="tagValue"}

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="643c7-112">Contrassegnare un contoller DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="643c7-112">Tag a DevSpaces contoller.</span></span>

## <span data-ttu-id="643c7-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="643c7-113">PARAMETERS</span></span>

### <span data-ttu-id="643c7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="643c7-114">-DefaultProfile</span></span>
<span data-ttu-id="643c7-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="643c7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="643c7-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="643c7-116">-InputObject</span></span>
<span data-ttu-id="643c7-117">Un oggetto PSController, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="643c7-117">A PSController object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DevSpaces.Models.PSController
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="643c7-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="643c7-118">-Name</span></span>
<span data-ttu-id="643c7-119">Nome del controller DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="643c7-119">DevSpaces controller name.</span></span>

```yaml
Type: System.String
Parameter Sets: DevSpacesControllerNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="643c7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="643c7-120">-ResourceGroupName</span></span>
<span data-ttu-id="643c7-121">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="643c7-121">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DevSpacesControllerNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="643c7-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="643c7-122">-ResourceId</span></span>
<span data-ttu-id="643c7-123">ID risorsa DevSpaces</span><span class="sxs-lookup"><span data-stu-id="643c7-123">The DevSpaces resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="643c7-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="643c7-124">-Tag</span></span>
<span data-ttu-id="643c7-125">Tabella hash che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="643c7-125">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="643c7-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="643c7-126">-Confirm</span></span>
<span data-ttu-id="643c7-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="643c7-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="643c7-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="643c7-128">-WhatIf</span></span>
<span data-ttu-id="643c7-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="643c7-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="643c7-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="643c7-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="643c7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="643c7-131">CommonParameters</span></span>
<span data-ttu-id="643c7-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="643c7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="643c7-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="643c7-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="643c7-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="643c7-134">INPUTS</span></span>

### <span data-ttu-id="643c7-135">System. String</span><span class="sxs-lookup"><span data-stu-id="643c7-135">System.String</span></span>

### <span data-ttu-id="643c7-136">Microsoft. Azure. Commands. DevSpaces. Models. PSController</span><span class="sxs-lookup"><span data-stu-id="643c7-136">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>
<span data-ttu-id="643c7-137">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="643c7-137">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="643c7-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="643c7-138">OUTPUTS</span></span>

### <span data-ttu-id="643c7-139">Microsoft. Azure. Commands. DevSpaces. Models. PSController</span><span class="sxs-lookup"><span data-stu-id="643c7-139">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="643c7-140">Note</span><span class="sxs-lookup"><span data-stu-id="643c7-140">NOTES</span></span>

## <span data-ttu-id="643c7-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="643c7-141">RELATED LINKS</span></span>
