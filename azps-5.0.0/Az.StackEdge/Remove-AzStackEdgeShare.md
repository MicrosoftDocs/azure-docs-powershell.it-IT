---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeShare.md
ms.openlocfilehash: 3f5855d329daba44b26e2c79cbc07608222db5f9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94199638"
---
# <span data-ttu-id="84d0c-101">Remove-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="84d0c-101">Remove-AzStackEdgeShare</span></span>

## <span data-ttu-id="84d0c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="84d0c-102">SYNOPSIS</span></span>
<span data-ttu-id="84d0c-103">Rimuove una condivisione dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="84d0c-103">Removes a share from the device.</span></span>

## <span data-ttu-id="84d0c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="84d0c-104">SYNTAX</span></span>

### <span data-ttu-id="84d0c-105">DeleteByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="84d0c-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84d0c-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="84d0c-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeShare [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84d0c-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="84d0c-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeShare [-InputObject] <PSStackEdgeShare> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84d0c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="84d0c-108">DESCRIPTION</span></span>
<span data-ttu-id="84d0c-109">Il cmdlet **Remove-AzStackEdgeEdgeShare** rimuove le condivisioni Edge associate per un dispositivo a bordo dello stack.</span><span class="sxs-lookup"><span data-stu-id="84d0c-109">The **Remove-AzStackEdgeEdgeShare** cmdlet removes the associated edge shares for a Stack Edge device.</span></span>

## <span data-ttu-id="84d0c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="84d0c-110">EXAMPLES</span></span>

### <span data-ttu-id="84d0c-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="84d0c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name shareName
```

## <span data-ttu-id="84d0c-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="84d0c-112">PARAMETERS</span></span>

### <span data-ttu-id="84d0c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="84d0c-113">-AsJob</span></span>
<span data-ttu-id="84d0c-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="84d0c-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="84d0c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84d0c-115">-DefaultProfile</span></span>
<span data-ttu-id="84d0c-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="84d0c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84d0c-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="84d0c-117">-DeviceName</span></span>
<span data-ttu-id="84d0c-118">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="84d0c-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84d0c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="84d0c-119">-InputObject</span></span>
<span data-ttu-id="84d0c-120">Oggetto di input</span><span class="sxs-lookup"><span data-stu-id="84d0c-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: EdgeShare

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="84d0c-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="84d0c-121">-Name</span></span>
<span data-ttu-id="84d0c-122">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="84d0c-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: EdgeShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84d0c-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="84d0c-123">-PassThru</span></span>
<span data-ttu-id="84d0c-124">Restituisce vero in caso di esito positivo</span><span class="sxs-lookup"><span data-stu-id="84d0c-124">returns true if successful</span></span>

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

### <span data-ttu-id="84d0c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84d0c-125">-ResourceGroupName</span></span>
<span data-ttu-id="84d0c-126">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="84d0c-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84d0c-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="84d0c-127">-ResourceId</span></span>
<span data-ttu-id="84d0c-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="84d0c-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="84d0c-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="84d0c-129">-Confirm</span></span>
<span data-ttu-id="84d0c-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84d0c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84d0c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84d0c-131">-WhatIf</span></span>
<span data-ttu-id="84d0c-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="84d0c-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="84d0c-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="84d0c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84d0c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84d0c-134">CommonParameters</span></span>
<span data-ttu-id="84d0c-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84d0c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84d0c-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="84d0c-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84d0c-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="84d0c-137">INPUTS</span></span>

### <span data-ttu-id="84d0c-138">System. String</span><span class="sxs-lookup"><span data-stu-id="84d0c-138">System.String</span></span>

### <span data-ttu-id="84d0c-139">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="84d0c-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="84d0c-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="84d0c-140">OUTPUTS</span></span>

### <span data-ttu-id="84d0c-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="84d0c-141">System.Boolean</span></span>

## <span data-ttu-id="84d0c-142">Note</span><span class="sxs-lookup"><span data-stu-id="84d0c-142">NOTES</span></span>

## <span data-ttu-id="84d0c-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="84d0c-143">RELATED LINKS</span></span>
