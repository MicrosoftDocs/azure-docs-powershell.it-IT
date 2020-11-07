---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/update-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Update-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Update-AzDevSpacesController.md
ms.openlocfilehash: 2a94d74fb8c6ba6cc9f6c2873269f3009c2f7e9d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684422"
---
# <span data-ttu-id="1d12d-101">Update-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="1d12d-101">Update-AzDevSpacesController</span></span>

## <span data-ttu-id="1d12d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1d12d-102">SYNOPSIS</span></span>
<span data-ttu-id="1d12d-103">Aggiornare il controller DevSpaces per aggiungere tag.</span><span class="sxs-lookup"><span data-stu-id="1d12d-103">Update the DevSpaces controller to add tags.</span></span>

## <span data-ttu-id="1d12d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1d12d-104">SYNTAX</span></span>

### <span data-ttu-id="1d12d-105">DevSpacesControllerNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1d12d-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Update-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d12d-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1d12d-106">ResourceIdParameterSet</span></span>
```
Update-AzDevSpacesController -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d12d-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1d12d-107">InputObjectParameterSet</span></span>
```
Update-AzDevSpacesController -InputObject <PSController> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d12d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1d12d-108">DESCRIPTION</span></span>
<span data-ttu-id="1d12d-109">Aggiornare il controller DevSpaces per aggiungere tag.</span><span class="sxs-lookup"><span data-stu-id="1d12d-109">Update the DevSpaces controller to add tags.</span></span>

## <span data-ttu-id="1d12d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1d12d-110">EXAMPLES</span></span>

### <span data-ttu-id="1d12d-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1d12d-111">Example 1</span></span>
```powershell
PS C:\> Update-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName -Tag @{ tagKey="tagValue"}

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="1d12d-112">Contrassegnare un contoller DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="1d12d-112">Tag a DevSpaces contoller.</span></span>

## <span data-ttu-id="1d12d-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1d12d-113">PARAMETERS</span></span>

### <span data-ttu-id="1d12d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d12d-114">-DefaultProfile</span></span>
<span data-ttu-id="1d12d-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1d12d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d12d-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1d12d-116">-InputObject</span></span>
<span data-ttu-id="1d12d-117">Un oggetto PSController, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="1d12d-117">A PSController object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="1d12d-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="1d12d-118">-Name</span></span>
<span data-ttu-id="1d12d-119">Nome del controller DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="1d12d-119">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="1d12d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d12d-120">-ResourceGroupName</span></span>
<span data-ttu-id="1d12d-121">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="1d12d-121">Resource group name</span></span>

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

### <span data-ttu-id="1d12d-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1d12d-122">-ResourceId</span></span>
<span data-ttu-id="1d12d-123">ID risorsa DevSpaces</span><span class="sxs-lookup"><span data-stu-id="1d12d-123">The DevSpaces resource id</span></span>

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

### <span data-ttu-id="1d12d-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="1d12d-124">-Tag</span></span>
<span data-ttu-id="1d12d-125">Tabella hash che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="1d12d-125">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="1d12d-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1d12d-126">-Confirm</span></span>
<span data-ttu-id="1d12d-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d12d-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d12d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d12d-128">-WhatIf</span></span>
<span data-ttu-id="1d12d-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1d12d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d12d-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1d12d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d12d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d12d-131">CommonParameters</span></span>
<span data-ttu-id="1d12d-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d12d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d12d-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d12d-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d12d-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1d12d-134">INPUTS</span></span>

### <span data-ttu-id="1d12d-135">System. String</span><span class="sxs-lookup"><span data-stu-id="1d12d-135">System.String</span></span>

### <span data-ttu-id="1d12d-136">Microsoft. Azure. Commands. DevSpaces. Models. PSController</span><span class="sxs-lookup"><span data-stu-id="1d12d-136">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="1d12d-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1d12d-137">OUTPUTS</span></span>

### <span data-ttu-id="1d12d-138">Microsoft. Azure. Commands. DevSpaces. Models. PSController</span><span class="sxs-lookup"><span data-stu-id="1d12d-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="1d12d-139">Note</span><span class="sxs-lookup"><span data-stu-id="1d12d-139">NOTES</span></span>

## <span data-ttu-id="1d12d-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1d12d-140">RELATED LINKS</span></span>