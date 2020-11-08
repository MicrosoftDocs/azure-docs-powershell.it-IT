---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/update-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Update-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Update-AzDevSpacesController.md
ms.openlocfilehash: 9de9f5e5870aed99a9ef7203bfea4797e78e5f8c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020326"
---
# <span data-ttu-id="1e868-101">Update-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="1e868-101">Update-AzDevSpacesController</span></span>

## <span data-ttu-id="1e868-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1e868-102">SYNOPSIS</span></span>
<span data-ttu-id="1e868-103">Aggiornare il controller DevSpaces per aggiungere tag.</span><span class="sxs-lookup"><span data-stu-id="1e868-103">Update the DevSpaces controller to add tags.</span></span>

## <span data-ttu-id="1e868-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1e868-104">SYNTAX</span></span>

### <span data-ttu-id="1e868-105">DevSpacesControllerNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1e868-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Update-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e868-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e868-106">ResourceIdParameterSet</span></span>
```
Update-AzDevSpacesController -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e868-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e868-107">InputObjectParameterSet</span></span>
```
Update-AzDevSpacesController -InputObject <PSController> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e868-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1e868-108">DESCRIPTION</span></span>
<span data-ttu-id="1e868-109">Aggiornare il controller DevSpaces per aggiungere tag.</span><span class="sxs-lookup"><span data-stu-id="1e868-109">Update the DevSpaces controller to add tags.</span></span>

## <span data-ttu-id="1e868-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1e868-110">EXAMPLES</span></span>

### <span data-ttu-id="1e868-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1e868-111">Example 1</span></span>
```powershell
PS C:\> Update-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName -Tag @{ tagKey="tagValue"}

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="1e868-112">Contrassegnare un controller DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="1e868-112">Tag a DevSpaces controller.</span></span>

## <span data-ttu-id="1e868-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1e868-113">PARAMETERS</span></span>

### <span data-ttu-id="1e868-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e868-114">-DefaultProfile</span></span>
<span data-ttu-id="1e868-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1e868-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e868-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1e868-116">-InputObject</span></span>
<span data-ttu-id="1e868-117">Un oggetto PSController, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="1e868-117">A PSController object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="1e868-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="1e868-118">-Name</span></span>
<span data-ttu-id="1e868-119">Nome del controller DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="1e868-119">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="1e868-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e868-120">-ResourceGroupName</span></span>
<span data-ttu-id="1e868-121">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="1e868-121">Resource group name</span></span>

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

### <span data-ttu-id="1e868-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1e868-122">-ResourceId</span></span>
<span data-ttu-id="1e868-123">ID risorsa DevSpaces</span><span class="sxs-lookup"><span data-stu-id="1e868-123">The DevSpaces resource id</span></span>

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

### <span data-ttu-id="1e868-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="1e868-124">-Tag</span></span>
<span data-ttu-id="1e868-125">Tabella hash che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="1e868-125">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="1e868-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1e868-126">-Confirm</span></span>
<span data-ttu-id="1e868-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e868-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e868-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e868-128">-WhatIf</span></span>
<span data-ttu-id="1e868-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1e868-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e868-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1e868-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e868-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e868-131">CommonParameters</span></span>
<span data-ttu-id="1e868-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e868-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e868-133">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e868-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e868-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1e868-134">INPUTS</span></span>

### <span data-ttu-id="1e868-135">System. String</span><span class="sxs-lookup"><span data-stu-id="1e868-135">System.String</span></span>

### <span data-ttu-id="1e868-136">Microsoft. Azure. Commands. DevSpaces. Models. PSController</span><span class="sxs-lookup"><span data-stu-id="1e868-136">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="1e868-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1e868-137">OUTPUTS</span></span>

### <span data-ttu-id="1e868-138">Microsoft. Azure. Commands. DevSpaces. Models. PSController</span><span class="sxs-lookup"><span data-stu-id="1e868-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="1e868-139">Note</span><span class="sxs-lookup"><span data-stu-id="1e868-139">NOTES</span></span>

## <span data-ttu-id="1e868-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1e868-140">RELATED LINKS</span></span>
