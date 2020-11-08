---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/update-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Update-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Update-AzDevSpacesController.md
ms.openlocfilehash: 9de9f5e5870aed99a9ef7203bfea4797e78e5f8c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190749"
---
# <span data-ttu-id="4647f-101">Update-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="4647f-101">Update-AzDevSpacesController</span></span>

## <span data-ttu-id="4647f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4647f-102">SYNOPSIS</span></span>
<span data-ttu-id="4647f-103">Aggiornare il controller DevSpaces per aggiungere tag.</span><span class="sxs-lookup"><span data-stu-id="4647f-103">Update the DevSpaces controller to add tags.</span></span>

## <span data-ttu-id="4647f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4647f-104">SYNTAX</span></span>

### <span data-ttu-id="4647f-105">DevSpacesControllerNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4647f-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Update-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4647f-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4647f-106">ResourceIdParameterSet</span></span>
```
Update-AzDevSpacesController -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4647f-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4647f-107">InputObjectParameterSet</span></span>
```
Update-AzDevSpacesController -InputObject <PSController> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4647f-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4647f-108">DESCRIPTION</span></span>
<span data-ttu-id="4647f-109">Aggiornare il controller DevSpaces per aggiungere tag.</span><span class="sxs-lookup"><span data-stu-id="4647f-109">Update the DevSpaces controller to add tags.</span></span>

## <span data-ttu-id="4647f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4647f-110">EXAMPLES</span></span>

### <span data-ttu-id="4647f-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4647f-111">Example 1</span></span>
```powershell
PS C:\> Update-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName -Tag @{ tagKey="tagValue"}

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="4647f-112">Contrassegnare un controller DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="4647f-112">Tag a DevSpaces controller.</span></span>

## <span data-ttu-id="4647f-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4647f-113">PARAMETERS</span></span>

### <span data-ttu-id="4647f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4647f-114">-DefaultProfile</span></span>
<span data-ttu-id="4647f-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4647f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4647f-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4647f-116">-InputObject</span></span>
<span data-ttu-id="4647f-117">Un oggetto PSController, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="4647f-117">A PSController object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="4647f-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="4647f-118">-Name</span></span>
<span data-ttu-id="4647f-119">Nome del controller DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="4647f-119">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="4647f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4647f-120">-ResourceGroupName</span></span>
<span data-ttu-id="4647f-121">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="4647f-121">Resource group name</span></span>

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

### <span data-ttu-id="4647f-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4647f-122">-ResourceId</span></span>
<span data-ttu-id="4647f-123">ID risorsa DevSpaces</span><span class="sxs-lookup"><span data-stu-id="4647f-123">The DevSpaces resource id</span></span>

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

### <span data-ttu-id="4647f-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="4647f-124">-Tag</span></span>
<span data-ttu-id="4647f-125">Tabella hash che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="4647f-125">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="4647f-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4647f-126">-Confirm</span></span>
<span data-ttu-id="4647f-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4647f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4647f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4647f-128">-WhatIf</span></span>
<span data-ttu-id="4647f-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4647f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4647f-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4647f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4647f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4647f-131">CommonParameters</span></span>
<span data-ttu-id="4647f-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4647f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4647f-133">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4647f-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4647f-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4647f-134">INPUTS</span></span>

### <span data-ttu-id="4647f-135">System. String</span><span class="sxs-lookup"><span data-stu-id="4647f-135">System.String</span></span>

### <span data-ttu-id="4647f-136">Microsoft. Azure. Commands. DevSpaces. Models. PSController</span><span class="sxs-lookup"><span data-stu-id="4647f-136">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="4647f-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4647f-137">OUTPUTS</span></span>

### <span data-ttu-id="4647f-138">Microsoft. Azure. Commands. DevSpaces. Models. PSController</span><span class="sxs-lookup"><span data-stu-id="4647f-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="4647f-139">Note</span><span class="sxs-lookup"><span data-stu-id="4647f-139">NOTES</span></span>

## <span data-ttu-id="4647f-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4647f-140">RELATED LINKS</span></span>