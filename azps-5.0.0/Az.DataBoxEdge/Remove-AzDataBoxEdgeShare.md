---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeShare.md
ms.openlocfilehash: ac3282d8249eecbb6e8c7bd1fb23a5ab0f55ed95
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298704"
---
# <span data-ttu-id="cd446-101">Remove-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="cd446-101">Remove-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="cd446-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cd446-102">SYNOPSIS</span></span>
<span data-ttu-id="cd446-103">Rimuove una condivisione dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cd446-103">Removes a share from the device.</span></span>

## <span data-ttu-id="cd446-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cd446-104">SYNTAX</span></span>

### <span data-ttu-id="cd446-105">DeleteByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cd446-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd446-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd446-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeShare [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd446-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd446-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeShare [-InputObject] <PSDataBoxEdgeShare> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd446-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cd446-108">DESCRIPTION</span></span>
<span data-ttu-id="cd446-109">Il cmdlet **Remove-AzDataBoxEdgeEdgeShare** rimuove le condivisioni Edge associate per un dispositivo Edge della casella dati.</span><span class="sxs-lookup"><span data-stu-id="cd446-109">The **Remove-AzDataBoxEdgeEdgeShare** cmdlet removes the associated edge shares for a Data Box Edge device.</span></span>

## <span data-ttu-id="cd446-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cd446-110">EXAMPLES</span></span>

### <span data-ttu-id="cd446-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="cd446-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name shareName
```

## <span data-ttu-id="cd446-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cd446-112">PARAMETERS</span></span>

### <span data-ttu-id="cd446-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd446-113">-AsJob</span></span>
<span data-ttu-id="cd446-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="cd446-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd446-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd446-115">-DefaultProfile</span></span>
<span data-ttu-id="cd446-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cd446-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd446-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="cd446-117">-DeviceName</span></span>
<span data-ttu-id="cd446-118">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="cd446-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd446-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd446-119">-InputObject</span></span>
<span data-ttu-id="cd446-120">Oggetto di input</span><span class="sxs-lookup"><span data-stu-id="cd446-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd446-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="cd446-121">-Name</span></span>
<span data-ttu-id="cd446-122">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="cd446-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd446-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cd446-123">-PassThru</span></span>
<span data-ttu-id="cd446-124">Restituisce vero in caso di esito positivo</span><span class="sxs-lookup"><span data-stu-id="cd446-124">returns true if successful</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd446-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd446-125">-ResourceGroupName</span></span>
<span data-ttu-id="cd446-126">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="cd446-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd446-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd446-127">-ResourceId</span></span>
<span data-ttu-id="cd446-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd446-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd446-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cd446-129">-Confirm</span></span>
<span data-ttu-id="cd446-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd446-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd446-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd446-131">-WhatIf</span></span>
<span data-ttu-id="cd446-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cd446-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cd446-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cd446-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd446-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd446-134">CommonParameters</span></span>
<span data-ttu-id="cd446-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd446-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd446-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cd446-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd446-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cd446-137">INPUTS</span></span>

### <span data-ttu-id="cd446-138">System. String</span><span class="sxs-lookup"><span data-stu-id="cd446-138">System.String</span></span>

### <span data-ttu-id="cd446-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="cd446-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="cd446-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cd446-140">OUTPUTS</span></span>

### <span data-ttu-id="cd446-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cd446-141">System.Boolean</span></span>

## <span data-ttu-id="cd446-142">Note</span><span class="sxs-lookup"><span data-stu-id="cd446-142">NOTES</span></span>

## <span data-ttu-id="cd446-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cd446-143">RELATED LINKS</span></span>
